tomcat启动顺序：
bootstrap的静态块初始化和加载环境 然后bootstrap的一切操作其实都是对catalinadd dcaozuo
bootstrap:start --> catalina:start-->server:start(其实调用接口Lifecycle的抽象实现LifecycleBase的start方法而LifecycleBase的start的方法里其实调用了抽象
方法startInternal,server的StandarServer实现了抽象LifecycleBase的startInternal方法，所以即使调用StandardServer的startInternal方法）service:start(StandarService:startinternal)-->Connector:start(Connector: startInternal) --> ProtocolHandler:start --> AbstractEndpoint:start(AbstractEndpoint:startInternal )AbstractEndpoint的startInternal方法是抽象方法 AbstractEndpoint的子类就是一个endpoint，用于接收请求的
