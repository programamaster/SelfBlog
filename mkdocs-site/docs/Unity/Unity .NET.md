# Unity .NET

.NET和Unity的未来(英文)：[Unity and .NET,what's next](https://blog.unity.com/engine-platform/unity-and-net-whats-next)  
.NET和Unity的未来(中文)：[.NET和Unity的未来](https://developer.unity.cn/projects/62bbc040edbc2a7848d45ae8)    
Unity .NET 兼容性问题：[在Unity中使用.NET 4.x](https://learn.microsoft.com/zh-cn/visualstudio/gamedev/unity/unity-scripting-upgrade)  
Microsoft官方文档（英文）：[.NET documentatio](https://learn.microsoft.com/en-us/dotnet/)  
Microsoft官方文档（中文）：[.NET 文档](https://learn.microsoft.com/zh-cn/dotnet/)

更高效地利用内存空间！Unity正逐步移植到CoreCLR GC：[更高效地利用内存空间！Unity正逐步移植到CoreCLR GC](https://developer.unity.cn/projects/65438ad2edbc2a002127b720)


请简要说明.Net跨语言和跨平台的原理（往往是面试时的口头询问）？

1.跨语言

.Net制定了了CLI公共语言基础结构的规则(CLS(Common Language Specification))，只要是按照该规则设计的语言在进行.Net相关开发时，编译器会将源代码（C#、VB等等）编译为CIL通用中间代码。也就是说不管什么原因进行开发，最终都会统一规范变为中间代码,最终通过CLR（公共语言运行时或者称为.Net虚拟）将中间代码翻译为对应操作系统的原生代码（机器码）,在操作系统上运行

2.跨平台
由于.Net Framework中利用CLI和CLR实现了跨语言，CLR主要起到一个翻译、运行、管理中间代码的作用,.Net Cor和Mono就是利用了CLR的这一特点，为不同操作系统实现对应CLR（公共语言运行时或.Net虚拟机）,那么不同操作系统对应的CLR就会将IL中间代码翻译为对应系统可以执行的原生代码（机器码）,达到跨平台的目的
