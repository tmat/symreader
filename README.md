# Microsoft.DiaSymReader

Provides managed definitions for COM interfaces exposed by DiaSymReader APIs ([ISymUnmanagedReader](https://msdn.microsoft.com/en-us/library/ms232131.aspx), [ISymUnmanagedBinder](https://msdn.microsoft.com/en-us/library/ms232451.aspx), etc.) for reading Windows and [Portable PDBs](https://github.com/dotnet/core/blob/master/Documentation/diagnostics/portable_pdb.md).

The implementation of these interfaces for Windows PDBs is provided by [Microsoft.DiaSymReader.Native](https://www.nuget.org/packages/Microsoft.DiaSymReader.Native) package. The implementation for Portable PDBs is provided by [Microsoft.DiaSymReader.PortablePdb](https://www.nuget.org/packages/Microsoft.DiaSymReader.PortablePdb) package. 

It is recommended that new applications and libraries read Portable PDBs directly using APIs provided by [System.Reflection.Metadata](https://www.nuget.org/packages/System.Reflection.Metadata) package. These APIs are much more efficient than DiaSymReader APIs. Microsoft.DiaSymReader.PortablePdb bridge is recommended for existings apps that already use DiaSymReader APIs and need to be able to read Portable PDBs without significant changes to their source.

Pre-release builds are available on MyGet gallery: https://dotnet.myget.org/Gallery/symreader.

[//]: # (Begin current test results)

|    | x64 Debug|x64 Release|
|:--:|:--:|:--:|
|**Windows**|[![Build Status](https://ci.dot.net/job/dotnet_symreader/job/master/job/Windows_NT_Debug/badge/icon)](https://ci.dot.net/job/dotnet_symreader/job/master/job/Windows_NT_Debug/)|[![Build Status](https://ci.dot.net/job/dotnet_symreader/job/master/job/Windows_NT_Release/badge/icon)](https://ci.dot.net/job/dotnet_symreader/job/master/job/Windows_NT_Release/)|
|**Ubuntu 16.04**|[![Build Status](https://ci.dot.net/job/dotnet_symreader/job/master/job/Ubuntu16.04_Debug/badge/icon)](https://ci.dot.net/job/dotnet_symreader/job/master/job/Ubuntu16.04_Debug/)|[![Build Status](https://ci.dot.net/job/dotnet_symreader/job/master/job/Ubuntu16.04_Release/badge/icon)](https://ci.dot.net/job/dotnet_symreader/job/master/job/Ubuntu16.04_Release/)|

[//]: # (End current test results)


This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
