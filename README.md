# SerialPortLibrary
android RS232串口通信

#how to use 

##1将library库引入要用的项目
``` 
      //如果是读卡器之类的 只需要设置串口地址 和 波特率 
      SerialHelper serialHelper=new SerialHelper("dev/s4",9600){//String sPort,String sBaudRate
		/**
		接收到串口返回的数据
		**/
		protected void onDataReceived(ComBean data) {

		}
	};
      serialHelper.open();
      //-----------------------------------------
      
      //其他帮助方法 获取所有串口地址
       SerialPortFinder mSerialPortFinder= new SerialPortFinder();
      String[] entryValues = mSerialPortFinder.getAllDevicesPath();
      List<String> allDevices = new ArrayList<String>();
      for (int i = 0; i < entryValues.length; i++) {
	  allDevices.add(entryValues[i]);
      }
      //发送数据给串口上的硬件设备
      serialHelper.send(..);
      //--------------------------------
    
    
      ``` 
      
      
