**SapMM** is Simple As Possible memory manager for Delphi XE-XE3, designed especially for memory-intensive multithreaded applications.
Should also work with other versions of Delphi (may require tiny code modifications).
SapMM scales very (I mean VERY) well under multithreaded use. If you use [OmniThreadLibrary](https://code.google.com/p/omnithreadlibrary), you definetely should take a look at SapMM.

---


To use SapMM simply add to your uses clause SapInstall unit as the first unit of your project (in the dpr file).

---


**NOTE!** Currently SapMM supports **only 32-bit mode** and can not be used with 64-bit applications. Contributors who can add 64-bit support are welcome, any help appreciated.

---


At the present moment SapMM is well tested only with Delphi XE and XE3 and is used in production (multi-user document flow system) since June 2013.
Version 1.01 is stable and can be used in production.

---


Author of the code is Alexei Nedoria, PM and software guru from Ivanovo, Russia. You can contact him directly via his email ned@iname.com

Current maintainer of the code is Anton Alisov, PM and software developer from Ivanovo, Russia. You can contact me via GoogleCode, email: alan008@bk.ru, Skype: antonalisov.

---


You can tune up the manager in some ways using SapDefs.pas unit. The most interesting constants here are:

  * **cOSBlockSize** - minimal block size, requested from OS as one piece
  * **cMaxOSBlocksInPool** - number of freed OS blocks, which are not returned to the OS by your app and stay in memory pool for future reuse. I.e. cOSBlockSize x cMaxOSBlocksInPool is maximum amount of memory your app will always hold for future reuse. Forced pool cleanup may happen in insufficient memory conditions.


---

Articles about SapMM:

[Article by Arnaud Bouchez](http://blog.synopse.info/post/2013/12/05/New-Open-Source-Multi-Thread-ready-Memory-Manager%3A-SAPMM)

[Article by Primoz Gabrijelcic / Anton Alisov](http://www.thedelphigeek.com/2013/12/sapmm.html)
