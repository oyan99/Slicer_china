# 第二章  3D Slicer入门
## 2.1  获取并安装最新的3D Slicer
### 2.1.1  3D Slicer的获取
3D Slicer具有一个自由开源的BSD风格的授权许可，并且支持Windows，Mac OS X和Linux三种操作系统。经过测试，并且明确支持的操作系统版本包括微软公司的Windows XP，Vista，和Windows 7操作系统，苹果公司的Mac OS X 10.5 (Leopard)，10.6 (Snow Leopard)，和10.7 (Lion)操作系统，以及一些知名的Linux发布版本。

Slicer4的最小系统硬件要求为1GB 内存以及4GB硬盘空间，其他硬件都未作明确要求。但是如果想要流畅地运行Slicer4，内存最好大于1GB，并且GPU最好能够支持OpenGL。
当前，最新的Slicer稳定版本是2012年11月发布的Slicer4.2，获取最新版或者稳定版的3D Slicer的URL为：http://download.slicer.org/用户可以获取的Slicer安装包，包括稳定版和最新版两种，其中前者的功着重于稳定但是版本更迭较慢，而后者包括一些未经大量测试的模块及功能，版本更新很快。

表2-1  可获取的Slicer安装文件列表
		Windows	Mac OS X	Linux
稳定版	64bit	√	√	√
	32bit	√	×	×
最新版	64bit	√	√	√
	32bit	√	×	×

### 2.1.2  3D Slicer的安装
以Windows环境下的安装为例，简述其安装步骤。

(1)双击获取到的安装文件，显示安装向导“欢迎”对话框，如图2-1所示。


图2-1  欢迎界面

(2)在图2-1对话框中单击下一步按钮，进入许可证协议对话框，如图2-2所示。


图2-2  接受许可证协议
(3)单击“我接受”按钮，Slicer软件安装进入“安装路径选择”对话框，如图2-3所示。

图2-3  安装位置选择

(4)单击下一步，进入快捷方式选择对话框，如图2-4所示。


图2-4  快捷方式创建选择
(5)单击安装，安装程序进行安装。如图2-5所示。


图2-5  正在安装

(6)等待安装完成，单击完成按钮，完成安装，如图2-6所示。


图2-6  安装完成
2.2  Slicer4的用户环境
Slicer4的主界面对最常用的功能提供了最直接的调用方式，并将它们按逻辑顺序分组，这些功能在图形用户界面中以一些接口面板的方式呈现。
界面在设计过程中以易于学习并掌握，易于在Slicer的庞大功能中被定位，当用户不需要的时候易于卸载和隐藏等为目标。Slicer的主界面如图2.7所示。


图2-7  Slicer程序主界面

Slicer的软件界面主要由如下几个部分组成。
系统主菜单：对Slicer的功能进行统一管理。
工具栏：提供Slicer功能的快捷方式。
模块面板：显示模块界面，Slicer中功能通过模块化的方式实现。
切片窗口：用以显示三个切片分量，分为冠状面，矢状面，水平面三个两两垂直的平面，分别使用“R”，“Y”，“G”表示。
三维视图窗口：将切片视图进行三维显示，直接显示各个组织的空间位置信息。
数据探针：用于显示鼠标在切片视图中移动时的实时坐标信息。
以下着重介绍主菜单、工具栏、切片视图以及3D视图等内容。
2.2.1  系统主菜单
Slicer4的应用菜单包含很多有用的功能，主菜单一共有四个。
1)  菜单项“File”
菜单项“File”，实现文件的管理功能，包含加载各种类型数据的选项，从互联网下载样本数据集或不同类型的单个数据集的选项，此外还提供了用于保存数据的选项。各个子菜单项的功能如下。
Add Data：添加一般Slicer数据，打开数据添加对话框，通过该对话框添加数据到当前场景，可以添加整个文件夹数据或者单个数据。
DICOM：添加DICOM数据，打开DICOM数据添加对话框，通过该对话框添加DICOM文件。
Down Sample Data：下载样本数据。
Save：打开保存文件对话框，用于保存文件。
Recently Loaded：最近加载文件。
Close Scene：关闭场景，关闭当前的场景。
Exit：退出程序。
2) 菜单项“Edit”
菜单项“Edit”实现程序的设置功能以及对图像进行编辑时使用的复制、剪切、粘贴等功能，除此之外，3D Slicer提供了一种用来记录和播放宏的简便方法，包含录制和播放两种功能，分别用于记录进行的动作，以及回放已记录的动作。这两种功能都无需用户的输入任何参数，开发人员一般使用此功能来记录教程和测试3DSlicer的应用程序。具体包含的子菜单选项如下。
Application Setting：应用程序设置，打开应用程序设置面板，该界面允许用户定制已安装的软件：设置各种类型的Slicer模块加载或不加载；Python交互器的显示与否；选择自定义字体，指定一个临时目录，以及一些其他的自定义选项。
Cut：剪切。
Copy：复制。
Paste：粘贴。
Record Macro：录制宏。
Play Macro：播放宏。
默认情况下，菜单项“录制宏”和“播放宏”是不显示的，要启用它必须通过应用程序设置界面的“QTtesting”选项卡中的设置。
3) 菜单项“View”
该菜单包含的选项，用来打开Python的交互器和错误日志，两者都是非常有用的开发工具。此外该菜单选项还提供了切换布局，还可以切换显示的个人工具栏和模块GUI面板。具体包含的子菜单选项如下。
Python Interactor：Python交互器，打开Python交互器窗口，在该窗口中进行Python代码的写入和执行。3D Slicer内置Python解析器，可以对Python代码进行解析执行，方便熟悉Python脚本语言的使用者和开发人员进行功能的使用以及开发。
Extension Manager：扩展管理工具，打开扩展管理窗口，下载，安装扩展功能模块。
Module Panel：模块面板，控制模块面板的显示与否。
Toolbars：工具栏管理，管理在界面上显示的工具栏。
Layout：布局管理，定义切片视图和3D 视图的显示方式。
Error Log：错误日志，显示程序运行过程中发生的错误。
4） 菜单项“Help”
Keyboard Shortcuts：键盘的快捷方式，汇总所有键盘快捷方式。
Interface Documentation：通过浏览器访问Slicer文档总页面。
Browse tutorials：通过浏览器访问Slicer的培训页面。
Slicer Publication：通过浏览器浏览关于Slicer的论文。
Visual Blog：可视化日志，通过浏览器浏览Slicer官方的图像资料。
Report a bug：报告一个Bug。
About 3D Slicer：关于软件，关于Slicer软件的资料。
2.2.2  工具栏
工具栏提供了许多有用功能的快捷方式，可以通过主菜单设置每一个工具栏的显示与否，以下分别介绍这些工具栏的功能。
1)  打开和保存
打开和保存工具栏是主菜单项“File”中的“Add Data”，“Add DICOM Data”以及“Save”子菜单的快捷方式，通过图标来实现功能，如图2-8所示。


图2-8  打开保存工具栏
2)  模块导航工具栏
模块的选择和导航工具栏用于搜索模块名称，从模块菜单中选择模块，程序可以根据选择历史将模块向前或向后移动，将常用的模块放到突出的位置，该工具栏如图2-9所示。


图2-9  模块导航工具栏

3)  核心模块
核心模块工具栏提供了一些最常用模块的快捷方式，Slicer的核心模块，包括模型，变换，数据，体数据，注释，交互式编辑器等，这些模块往往提供程序的一些基础功能，在对医学图像进行处理与分析时非常有用，如图2-10所示。


图2-10  核心模块工具栏

4)  布局
考虑到用户显示设备之间差异，例如宽屏、窄屏显示屏的差异，显示设备尺寸的差异，以及需要显示内容、显示习惯的差异，Slicer为3D视图、切片视图提供了多种布局方式。用户可以通过系统主菜单或者布局工具栏来进行选择，如图2-11所示。默认情况下，Slicer中视图布局的方式为“Conventional”，即3个切片视图水平排列，3D视图在其上方，而使用宽屏显示设备的用户更适合“Conventional Widescreen”方式，这种布局方式可以更加充分地利用显示设备。此外“Tabbed slice”将所有切片以标签页的形式排列，“Three over three”不显示3D 视图，而将切片视图扩展到6个，并以2排3列的形式排列，等等。

图2-11  布局工具栏

5)  鼠标模式
用户在使用Slicer的过程中，很多情况下都会需要在3D视图或者切片视图中做一些标记，例如标记一个点，划定一块感兴趣区域等。为了方便用户进行此类的操作，开发人员为鼠标的操作定义了两种模式：图像控制模式和注释放置模式。

图2-12  鼠标模式工具栏
图像控制模式是Slicer中鼠标鼠标的默认模式，该模式下，允许交互式旋转，平移和缩放等操作。
注释放置模式，允许对象进行交互式的注释放置，包括基准点（Fiducial）放置，标尺（Ruler）放置和感兴趣区域（ROI）放置三种类型，如图2-12所示。默认情况下，选中放置模式的图标，只对下一次鼠标的操作产生作用，例如选中“Fiducial”图标，那么在图像中点击左键一次，将会有一个“基准点”添加到图像中，而再次点击鼠标的左键时，将不会再次放置“基准点”。如果需要重复放置多个注释，则可以勾选工具栏的“Persistent”选项。
6)  截图和场景视图


图2-13  快照和场景视图工具栏

该工具栏包含3个选项，分别用于场景快照（Screen Shot），捕获场景视图（Scene View），和恢复或删除场景视图(Restore or delete scene view)。
场景快照选项用于捕获当前3D视图或者切片视图，保存为PNG格式，需要注意的是，在捕获完毕一副当前场景的图像时，该图像并没有保存到磁盘中，而是将该图像保存到“保存文件”界面的列表中。只有通过保存文件操作，才能真正的保存该图像。
场景视图是对当时MRML场景状态的一种描述，对场景视图的捕捉，实际上是对某一个MRML场景当前的状态信息的记录，该记录不能独立于该MRML场景独自存在，如果该MRML场景被关闭，则场景视图也同时被删除。类似于截图，场景视图也可以通过保存对话框进行保存。
恢复或删除场景视图选项可以在任何时候恢复保存的场景状态。这种机制可以为一个复杂的数据集准备和查看多个有趣的演示。
7)  十字准线选项
十字准线工具栏提供了一组选项来定制所有Slicer可用的十字准线的外观和行为。默认情况下，设置为无十字准线（No crosshair）。
用户可以通过不同的选项来定制合适的十字准线的形状，比如十字准线的大小，交叉处是否显示，线条的粗细等。值得注意的是“Navigation”选项，当用户选中该菜单项时，表示某一个切片视图的十字准线的两个轴分别代表其他两个与之垂直的切片。例如在横断面（Axial）中的十字准线分别代表了冠状面（coronal）和矢状面（sagittal），鼠标移动十字准线，则冠状面的切片视图以及矢状面的切片视图将会根据十字准线相应的移动。

图2-14  十字准线工具栏

2.2.3  应用程序设置



3D Slicer的应用程序设置部分目前一共有8个选项卡，如图2-15所示。
1）常规设置（General）：设置程序的字体，提示消息等。
2）模块设置（Modules）：关于模块加载的设置。
3）扩展设置（Extensions）：关于扩展功能的设置。
4）缓存（Cache）：该选项卡提供软件下载数据时的缓存有关的设置和功能。
5）国际化设置（Internationalization）：启用/关闭国际化功能设置，如果启用国际化，那么在常规设置面板上会出现语言选择的下拉菜单，由于3D Slicer4.2版本未能支持国际化，该功能仅可用作开发人员测试使用。
6）Slicer宏设置（QTtesting）：显示/隐藏Slicer宏功能菜单。
7）Python设置：用于Python交互窗口中的设置，例如文字颜色，字体等。
8）渲染设置（Volume  rendering）：用于设置渲染方式，显存等。
2.2.4  3D视图窗口
将鼠标移动到3D视图窗口的左上角的图钉图标，可以对3D视图进行控制。单击“图钉”图标，可以使得3D视图控制界面持续显示，再点击可以恢复。“图钉”图标右侧的按钮，显示当前3D 视图的编号，可以通过该按钮在不同的3D 视图之间进行切换。

图2-16  3D视图控制

3D 视图控制界面中的控制选项包含视角设置，以及一些配置3D视图的外观和行为的选项。这些选项分别为：
	场景居中显示；      	放大、缩小3D 图像；
	图像旋转，点击一次，图像转过一定角度；
	图像帧数显示，显示当前图像的实时帧数；
	图像旋转显示，图像保持旋转；
	图像摆动显示，点击该图标，图像进行左右摆动显示；
	3D图像转换图标，单击该图标打开一个下拉菜单，该菜单选项包含将图像转			换为四种3D显示方式：红蓝3D显示，偏振3D显示，快门式3D显示；
	辅助项目显示选项，单击该图标将打开一个下拉菜单，菜单项包含了3D 视图			中的辅助项目的显示与否，例如3D 视图中默认显示的立方体、坐标轴、背景			颜色等。
	透视/正视角度切换；
2.2.5  切片视图
Slicer的切片视图同样有一个视图控制器对其显示的图像进行控制，通过鼠标移动到切片视图的左上角的“图钉”图标来打开，单击“图钉”图标可以永久性的打开该控制界面。“图钉”图标右侧的标签“R”“Y”“G”用于区分不同的切片视图视图。切片标签的右侧滚动条提供了手动浏览切片的方式，右上角显示的小部件还显示了特定切片的索引。
每个切片视图包含显示每个层（前景层、背景层和标签层）的选项。对于前景层和标签层，该层的透明度控制工具条可以控制其透明度。此外，标签层的可见与否可以通过“标签轮廓”进行模式的切换。
切片视图的配置选项，可以通过“链接”图标按钮，应用到所有切片视图。当断开链接时，选项仅适用于正在调整的视图；而当视图“链接”后，该选项将适用于所有的切片视图。


图2-17  切片视图控制
2.3  Slicer的图像控制
1)  窗宽/窗位调整（Window/level）
W/L值既可以通过使用左键单击W/L工具条并拖动鼠标进行调整，也可以通过垂直移动鼠标调整Level值，水平移动鼠标调整Window值。此外，Slicer的体数据模块提供了一个接口界面提供更精确的调整。
2)  不透明度调整
长按Ctrl键并单击鼠标左键进行拖动，可以在一个Slicer视图中拖动调整不透明度。垂直移动鼠标调整前景的不透明度，水平移动鼠标调整标签不透明度。此外，Slicer的体数据模块提供了一个接口界面提供更精确的调整。
3)  选择与操作
当图像显示的比例较大时，图像窗口不能完全显示整个图像，这时需要通过抓手工具来拖动画面，以显示图像的不同部位，鼠标悬停在任何的“可选取”对象上，Slicer的视图将使得光标从一个“指针”改变成“手”。当光标显示“手”的时候，左键单击并拖动鼠标将选择和操纵的对象。释放鼠标按钮将取消选择的对象。
4)  操作关联
在任何Slicer视图中按住Shift键的同时移动鼠标，会导致其他Slicer视图交互方式滚动到相同的RAS鼠标的索引位置。当进行多配准的研究时，此功能非常有用。
5）  视图的缩放、平移和旋转
表2-2  Slicer视图的基本控制
功能	操作方法
缩放	1.鼠标滚轮操作
2.长按鼠标右键上下移动
平移	长按Shift + 长按鼠标左键拖拽
旋转	长按鼠标左键并拖拽

2.4  加载数据
2.4.1  支持的文件格式
Slicer支持多种医学图像数据的处理，如下表2.2所示，数据类型包括场景数据、影像图数据、模型数据、基准点数据、变换数据、颜色表数据等。由于Slicer的功能通过模块实现，故这些数据类型也由模块来进行使用，某一个模块支持的数据类型可能有多种，例如数据模块（Data）可以对场景数据（Scenes）进行读取、写入的操作；体数据模块（Volumes）对影像图数据（Raster Images）提供支持，这些影像图数据的格式不仅包括jpeg、png等Windows操作系统下最常见的图像文件格式，还包括标准的医学影像数据DICOM（Digitalimaging and Communications in Medicine）等。

文件格式	文件扩展名	读取	写入
场景数据（Scenes）	数据模块（Data）
MRML	.mrml	√	√
MRB	.mrb, .zip	√	√（.mrb），×（.zip）
影像图数据（Raster Images）	体数据模块（Volumes）
DICOM	.dcm ...	√	×
NRRD	.nrrd, .nhdr	√	√
MetaImage	.mhd, .mha	√	√
VTK	.vtk	√	√
Analyze	.hdr, .img, .img.gz	√	√
NifTI	.nia, .nii, .nii.gz	√	√
BMP	.bmp	√	√
BioRad	.pic	√	√
Brains2	.mask	√	√
GIPL	.gipl .gipl.gz	√	√
JPEG	.jpg, .jpeg	√	√
LSM	.lsm	√	√
PNG	.png	√	√
Stimulate	.spr	√	√
TIFF	.tif, .tiff	√	√
MGH-NMR	.mgz	√	√
模型数据（Models）	模型模块（Models）
VTK多边形数据	.vtk, .vtp	√	√
STL	.stl	√	√
OBJ	.obj	√	×
基准点数据（Fiducials）	注释模块（Annotations）
CSV	.fcsv	√	√
Text	.txt	√	√
变换数据（Transforms）	变换模块（Transforms）
Transform	.tfm, .mat	√	√
Text	.txt	√	√
转换功能（Transfer Functions）	渲染模块（Volume Rendering）
渲染参数文件	.vp	√	√
Text	.txt	√	√
颜色表数据（Lookup tables）	颜色模块（colors）
Text	.txt, .ctbl	√	√
双列表数据（Double Arrays）	颜色模块（colors）
CSV	.csv	√	√

如表2-3所示，Slicer支持的场景数据有MRML格式，MRB格式和ZIP格式三种。MRML（Medical Reality Modeling Language）用于描述医学图像三维场景，是3D Slicer独创的一种数据格式。每一个MRML Scene数据对象都包含了Slicer 应用程序的状态、原始数据和可视化参数等多种数据，例如（Volumes，体数据； Models，模型数据；Transforms，图像变换方式数据；Fiducials，基准点数据等等）。每一个数据类型是由特定的MRML Node（MRML节点）来表示的。MRML Scene 是MRML Nodes 的集合。
MRB格式的文件事实上是一个压缩文件，这个压缩文件中不仅包含了一个场景的MRML数据，还包含了所有加载到该场景的其他数据，如果将MRB文件的后缀名改为“.zip”，那么便可以使用普通工具查看（或修改）其中的内容。而以“zip”为后缀名的场景数据文件实际上就是3D Slicer旧版本使用的压缩场景数据格式，如果将文件扩展名从zip改变为MRB，就可以使用3D Slicer4直接打开。
3D Slicer为了能够处理不同医学影像产生的医学图像，引入了对DICOM格式文件的支持。DICOM即数字影像和通信标准，该标准拥有一个庞大的数据字典，几乎涵括了所有的医疗数据，从而能够表达医疗设备和患者信息，也能表述医学影像数据的相关信息。
虽然3D Slicer支持DICOM数据格式有着良好的支持，但是对于医学影像设备厂商生产的设备产生的扩散张量成像（DWI）数据并不完全符合DICOM标准，因此，为了更好的处理DWI成像，3D Slicer引入了一种新的数据格式，即NRRD数据格式。NRRD数据可以完全表示DWI图像的所有信息，使用两种后缀名，“nrrd”和“nhrd”，后者一般在旧版本的Slicer中使用。
除了DICOM数据格式外，3D Slicer还对神经影像学的另外两种数据，Analyze和NIfTI数据提供支持。Analyze格式储存的每组数据组包含2个文件，一个为数据文件，其扩展名为.img，包含二进制的图像资料；另外一个为头文件，扩展名为.hdr，包含图像的元数据。在fMRI的早期，Analyze格式最常用的格式，但现在逐渐被NIfTI格式所取代。Analyze格式主要不足就是头文件不能真正反映元数据。
NIfTI格式最重要的特征就是能反应MRI仪器的像素指数与空间位置。如果使用得当，能帮助我们准确定向，如能帮我们确定哪边代表的是左脑。标准NIfTI图像的扩展名是.nii，包含了头文件及图像资料。由于NIfTI格式和Analyze格式的关系，因此NIfTI格式也可使用独立的图像文件（.img）和头文件（.hdr）。单独的.nii格式文件的优势就是可以用标准的压缩软件（如gzip），而且一些分析软件包（如FSL）可以直接读取和写入压缩的.nii文件（扩展名为.nii.gz）。
2.4.2  添加数据
Slicer通过功能模块实现功能，虽然这些功能模块数量众多，支持的数据格式也不尽相同。Slicer将除DICOM数据之外的所有数据类型添加到Slicer中的过程都是通过“添加数据对话框”来完成，数据被添加到现有的场景。而DICOM数据由于标准较多，通过一个独立的功能模块进行添加，这个功能模块的详细信息在下一章做具体介绍。
“添加数据对话框”既可以通过主菜单打开，也可以通过工具栏、快捷键等多种方式打开，该对话框的界面如下图所示。


图2-18  添加数据对话框

“添加数据对话框”按钮功能如下：
Choose Directory to Add 	按钮添加所选目录文件夹中的所有文件。
Choose Files(s) to Add	按钮添加所有选定的文件。
Show Options 	复选框显示/隐藏加载一个对象时的属性的各种选项。
Reset 	按钮清除整个加载的文件列表。
Ok	按钮确认加载。
Cancel	按钮取消加载。
通过添加文件夹或者添加文件功能按钮将文件选中后，这些文件在“添加数据对话框”中列出，如下图所示，并可以通过文件名前面的复选框来确认加载与否。由于不同的功能模块可以拥有相同的数据类型，如果某种数据格式被多个功能模块使用，那么程序将无法判断该文件是何种类型的数据，需要进行手动选择。“添加数据对话框”中“Description”列的下拉菜单显示自动检测到的文件类型，用户通过该下拉菜单进行手动选择。

图2-19  文件添加列表

图2-20  更多选项
在加载之前，许多对象可以添加额外的说明，选中“Show Options”复选框，显示额外的可加载选项。

2.4.3  获取示例数据
Add Sample Data模块提供了大量的从互联网上下载样本数据集的快捷方式。这些数据集可用于测试的Slicer的功能。
2.5  保存数据
Slicer可以保存当前场景（包括所有场景快照，基准点列表等）或者单个数据集，界面如图所示。


为了给保存数据提供更加丰富的选项，“保存场景对话框”的界面并没有使用系统自带的资源管理器，界面中按钮及图标的功能如下：
选择场景和发生修改的数据；
只选择发生修改的数据；
保存当前场景以及其他文件为MRB文件；
为选中的文件修改保存路径（Change Directory for selected files）：
保存（Save）：确认保存；
取消（Cancel）：取消保存；
文件名（File Name）：输入保存文件名；
文件格式（File Format）：选择需要保存文件的保存格式；
路径（Directory）：为需要保存的文件修改保存路径；
其他选项（show options）：
选项（Options）：
节点名（Node name)：
节点类型（Node type）：
状态（Status）：
2.5.1 选择要保存的数据
当用户需要保存数据被时，打开“保存数据对话框”，当前场景文件、场景快照、注释等被添加到保存文件列表中等待用户的选择，用户可以通过文件名左边的复选框选中/取消保存，在面板的左上方的两个图标按钮提供了常用选择的快捷方式：选择所有文件和仅选择发生修改的文件。
“保存”选项将打开保存数据界面，它提供了多种选项，用于保存MRML场景，单个数据集和的医疗现实束（. MRB）文件。
2.5.2 选择要保存的路径
改变所有选定的文件的保存路径可以使用左下角的所有“改变选中文件路径（change directory for all selected files）”按钮，这个按钮将打开一个目录浏览器，用于选择和改变所有选择的文件保存路径。
改变某个场景文件或者但个数据集的保存路径，可以点击文件列表中的“Data Directory”列的文件路径来做出改变。如果该文件未被选中，则改变路径后将会被自动选中。
要恢复默认的保存目录，单击Cancel按钮，然后重新打开对话框，每次打开该对话框时的保存路径都是默认路径。
2.5.3 修改文件名和格式
文件列表的“File name”列可以通过单击修改保存文件的文件名，“File Format”列可以选择要保存文件的存储类型，该列的文件类型可以更新。如果数据集的名称或格式做出修改，先前没有被选中文件会被自动选中。
指定保存一个场景文件：场景的描述一般会出现在保存文件列表中，如果这个场景文件是从MRML文件中加载，那么该MRML文件的文件名将会默认为保存文件的名称。如果要保存文件到一个新的MRML文件，可以改变要保存文件的文件名或者路径。
在完成上述步骤后，点击“OK”按钮，完成保存。
2.6  获取帮助