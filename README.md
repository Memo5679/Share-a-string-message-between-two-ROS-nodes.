# Share-a-String-Message-between-Two-ROS-Nodes

# Create a ROS Workspace
1- Create workspace folder called Memo_ws

    * mkdir Memo_ws
    * cd Memo_ws/
    
2- create a folder called src

    * mkdir src  (ROS packages will reside here)
    
3- initialize the folder as workspace, inside src type

    * cd src/
    * catkin_init_workspace
    
  Cmakefile.txt created in src (ready to compile)
    
4- to compile workspace return back to Memo_ws and type :

    * cd ..
    * catkin_make 
    
 Build, devel, src should be created in Memo_ws
# Create a New Package
1- to create package go to src and type: 

    * catkin_create_pkg Memo_package rospy roscpp std_msgs
   
  Cmakelist.txt, include, package.xml,	src should be created in Memo_package
  
2- to compile same go to Memo_ws and type:

    * catkin_make (it will identify the package)
    
# Create a Publisher and Subscriber using Python
1- Go to package Memo_package and create new folder called scripts 

    * cd /scripts
Copy and paste the python files inside 'scripts'

2- To run them go to Memo_ws and type

    * source devel/setup.bash
    * roscore  (in seperate terminal)
    * rosrun Memo_package Publisher.py   (it will publich the string message to a topic called 'hello')
    * rosrun Memo_package Subscriber.py  (it will receive the published string message from the topic and print it)
you can see the graph by typing (in seperate terminal):

    * rosrun rqt_graph rqt_graph

![Capture](https://user-images.githubusercontent.com/67188835/86829356-fb31d680-c09c-11ea-9da6-5ea477ad966d.PNG)


