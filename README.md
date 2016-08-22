# myMachineLearningNotes
##Background:
	*A machine learning group was built in our company,as a start group for machine learning.I am one of them.
	
	*Now my task is to research all the frameworks,and compare their performance,expandance,
		and consider whether it is suitable for business,etc.
	*Select a suitable framework for our follow-up task:such as data-mining,data-visualizing,modeling,etc.
	
	*Thought all I know about Machine-learing comes from Andrew NG's coursera,
		but I wanna become en expert of this area.I believe will.
	
##TODO & Notes:

      1.比较框架的支持度、速度、对数据库如mangoDB等的支持、可拓展性
      2.目前考虑的框架有：sparkMlib,systemML,weka
	  3.目前我们所使用的主要算法有：决策树、深度学习、神经网络、分类、聚类


	  
	  深度学习热度排名：https://github.com/aymericdamien/TopDeepLearning
	  
	  weka：
		包含算法：
			数据预处理、分类、回归、聚类、关联规则、可视化
		一个具有图形界面的基于java的库，可以运行小数据集的实验。
		缺点：
			缺少相应文档，api设计糟糕，不适用于生产

Weka：
	Weka在Hadoop3.7中开始包含分布式处理的封装器。weka具有大量的工具，虽然其分类器和回归器可以用在Hadoop平台上，但是大多数不能进行并行化。这些算法本来是作为集合进行训练的，对小数据子集进行分别训练，然后使用投票技术进行结合，而不是在reduce阶段结合到最终模型中。这样做也许是由于缺乏并行算法。
	distributedWekaBase：提供不依赖于平台的map和reduce任务，在未来有被添加到新平台的潜力
	distributedWekaHadoop：提供Hadoop特有的工具，包括HDFS的loaders和savers以及Hadoop任务的配置。仅可用于Hadoop1.1.2，也就是说，只能运行于MapReduce之上
	distributedWekaSpark：目前只能接受csv格式文件输入
	Weka是使用Java开发的用户数据挖掘的开源项目。Weka作为一个公开的数据挖掘工作平台，集合了大量能够承担数据挖掘人物的机器学习算法，包括了对数据进行预处理、分类、回归、聚类等等。同时，Weka实现了对大数据的可视化，通过Java设计的新式交互界面上，实现人与程序的交互

		
systemML： 一门灵活的、可伸缩的机器学习 (ML) 语言，支持描述性分析、分类、聚类、回归、矩阵分解以及生存分析等算法。
SystemML有多种执行模式。在独立模式下，SystemML能够运行在单台机器上，这样数据科学家就能够在本地开发算法，不需要分布式集群。另外还可以将算法分发到Hadoop或者Spark上，从而利用已有的资源和技能。SystemML能够运行于Windows、 Linux以及MacOS上。
SystemML使用Java语言编写，开发人员能够使用类似于R或者Python的语法表达算法，通过Java、Scala以及Python操作SystemML。
文档方面，SystemML基本集中于GitHub上，包括构建、测试、独立模式运行命令以及一个线性回归的示例。

H2O	：0xdata的旗舰产品，针对欺诈或者趋势预测
java,python,R,Scala
在这些工具中，H2O是唯一一个可以被称为产品的，而不只是项目。
最突出的特性:提供了图形界面;提供了许多深度神经网络工具。深度学习是H2O的一个重要特性。
相对于其他开源的机器学习算法包，h2o是一个机器学习产品，更加好用适用，从实际问题出发，结合产品的思维，开发实现的机器学习框架，适合工业应用。
	
			可拓展性如何衡量
			易用性
			
对于一般的需求，MLib和H2O是非常好的选择，这两个框架的速度都很快，可扩展性（对不同大小的数据集的支持）都很好。
这两个框架对算法的选择有相当大的不同。
MLib在大部分机器学习领域提供了更好的选择，H2O则是唯一具有深度学习解决方案的工具。
可用性：			   两者都提供了多种编程语言的api，但是H2O提供了GUI图形界面。
	
SAMOA和Mahout专注于提供平台给用户接入自己的学习算法。SAMOA允许用户创建数据流算法，是唯一一个为真正的实时数据流设计的框架，使其成为最快和最具扩展性的选项。SAMOA还没有活跃的社区，只是提供了详细的文档。

在算法覆盖率方面Mahout和MLib是最面面俱到的大数据框架，都可以与Spark和H2O协同工作。
MLib有更加宽广的算法选择和更大、更多专门致力于此的团队.
Mahout比其他框架更成熟，在推荐算法方面具有最多的选择。但是由于对MapReduce的依赖Mahout正在被抛弃，但是这一现象在最新的版本出来之后也许有所改观。


推荐算法：电子商务或者社交网络 --商品推荐或用户推荐  Mahout, MLlib, Flink-ML, and Oryx
社群媒体、物联网：实时分析结果 --Storm、Flink
医疗保健：不相关数据 需要一种批量和流混合的处理方式 --Flink, Oryx, or Spark




处理平台的选择：
	MapReduce：一度是大数据项目的事实标准，由于缓慢、缺乏迭代算法的支持，在机器学习社区正变得越来越过时，在大多数项目中不推荐使用
	Spark：MapReduce继任者，基于MapReduce,因此不难从MapReduce转换到Spark。它提供了迭代任务，因此能够支持所有MapReduce支持的机器学习库，另外还支持其他库。
	
	Storm、Flink:实时解决方案，提供真正的流式处理，而Spark只是使用微批量流处理，在获取结果时有微小的延迟。对其他机器学习算法的支持不是很好。
	
	H2O则是唯一具有深度学习解决方案的工具，具有图形界面支持，支持比其他机器学习工具更多的机器学习方案，可拓展性、兼容性更好。
	









