## mvn clean package

先看命令的执行过程

![img](maven之package与install的区别.assets/560071-20180917194214143-1200865291.png)

![img](maven之package与install的区别.assets/560071-20180917194509450-463987791.png)

 

## mvn clean install

同样先看执行过程

![img](maven之package与install的区别.assets/560071-20180917194914403-844177866.png)

![img](maven之package与install的区别.assets/560071-20180917195014983-1023692953.png)

- mvn clean package依次执行了clean、resources、compile、testResources、testCompile、test、war(jar)(打包)７个阶段;
- mvn clean install依次执行了clean、resources、compile、testResources、testCompile、test、war(jar)(打包)、install8个阶段;
-  maven-war-plugin将工程打包成war，而maven-install-plugin会将打好的war包放入本地开发环境的maven版本库中。