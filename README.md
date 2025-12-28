# twain_library-csharp_demo
C# demo programs using the <a href="https://github.com/dynarithmic/twain_library" target="_blank">DTWAIN Library</a>.

This demo consists of two folders, **FullDemo**, and **FullDemo_Dynamic**.  

The **FullDemo** folder contains a Visual Studio project **CSharp_FullDemo.sln** that shows the usage of auto loading the DTWAIN DLL using the **dtwain32u.cs** or **dtwain64u.cs** interface file.  Automatically loading the library means that your application shouldn't attempt to load the DTWAIN DLL "manually", instead C# / .NET will load the library.

The **FullDemo_Dynamic** folder contains a Visual Studio project **CSharp_FullDemo.sln** that shows the usage of dynamically loading the DTWAIN DLL using the **dtwain_dynamic.cs** interface file.  The main application is responsible for loading the DLL (see the **DTwainDemo.cs** file and the **public DTwainDemo()** constructor to see how to load the proper library at runtime), and not the .NET runtime.  

To build the demos, simply load the appropriate solution (.sln file) into Visual Studio (at least VS 2019), and choose **Build -> Build Solution** from the Visual Studio main menu.

Once built, the demos assumes that <a href="https://github.com/dynarithmic/twain_library/tree/master/binaries" target="_blank">the DTWAIN DLL's</a> are available (either on the system PATH or in the same directory as the executable) when the demo is run.  

In addition, please remember that the DTWAIN [text resources](https://github.com/dynarithmic/twain_library/tree/master/text_resources) also need to be available (perferably in the same directory as the DTWAIN DLL's).
