---
title: Erstellen und Registrieren einer Proxy-DLL
description: Wenn Sie das Proxy-/Stub-Marshalling für Ihre Anwendung ausgewählt haben, müssen die C- und H-Dateien, die MIDL generiert hat, kompiliert und verknüpft werden, um eine Proxy-DLL zu erstellen, und diese DLL muss in die Systemregistrierung eingegeben werden, damit Clients Ihre Schnittstellen finden können.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d4cafbe2be56d9e9a02a451e3daf905496c424
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826805"
---
# <a name="building-and-registering-a-proxy-dll"></a><span data-ttu-id="d7028-103">Erstellen und Registrieren einer Proxy-DLL</span><span class="sxs-lookup"><span data-stu-id="d7028-103">Building and Registering a Proxy DLL</span></span>

<span data-ttu-id="d7028-104">Wenn Sie das Proxy-/Stub-Marshalling für Ihre Anwendung ausgewählt haben, müssen die C- und H-Dateien, die MIDL generiert hat, kompiliert und verknüpft werden, um eine Proxy-DLL zu erstellen, und diese DLL muss in die Systemregistrierung eingegeben werden, damit Clients Ihre Schnittstellen finden können.</span><span class="sxs-lookup"><span data-stu-id="d7028-104">If you chose proxy/stub marshaling for your application, the .c and .h files that MIDL generated must be compiled and linked to create a proxy DLL, and that DLL must be entered into the system registry so that clients can locate your interfaces.</span></span> <span data-ttu-id="d7028-105">Die MIDL-generierte Datei Dlldata.c enthält die erforderlichen Routinen und andere Informationen zum Erstellen und Registrieren einer Proxy-/Stub-DLL.</span><span class="sxs-lookup"><span data-stu-id="d7028-105">The MIDL-generated file Dlldata.c contains the necessary routines and other information to build and register a proxy/stub DLL.</span></span>

<span data-ttu-id="d7028-106">Der erste Schritt beim Erstellen der DLL besteht darin, eine Moduldefinitionsdatei für den Linker zu schreiben, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d7028-106">The first step in building the DLL is to write a module definition file for the linker, as shown in the following example:</span></span>

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

<span data-ttu-id="d7028-107">Alternativ können Sie diese exportierten Funktionen in der LINK-Befehlszeile Ihres Makefiles angeben.</span><span class="sxs-lookup"><span data-stu-id="d7028-107">Alternatively, you can specify these exported functions on the LINK command line of your makefile.</span></span>

<span data-ttu-id="d7028-108">Die exportierten Funktionen werden in rpcproxy.h deklariert, was dlldata.c enthält, und Standardimplementierungen sind Teil der RPC-Laufzeitbibliothek.</span><span class="sxs-lookup"><span data-stu-id="d7028-108">The exported functions are declared in Rpcproxy.h, which Dlldata.c includes, and default implementations are part of the RPC run-time library.</span></span> <span data-ttu-id="d7028-109">COM verwendet diese Funktionen, um eine Klassenfactory zu erstellen, DLLs zu entladen (nachdem sichergestellt wurde, dass keine Objekte oder Sperren vorhanden sind), Informationen über die Proxy-DLL abzurufen und die Proxy-DLL selbst zu registrieren und die Registrierung aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="d7028-109">COM uses these functions to create a class factory, unload DLLs (after making sure that no objects or locks exist), retrieve information about the proxy DLL, and to self-register and unregister the proxy DLL.</span></span> <span data-ttu-id="d7028-110">Um diese vordefinierten Funktionen nutzen zu können, müssen Sie die Option Cpreprocessor /D (oder -D) aufrufen, wenn Sie die Dateien Dlldata.c und Example \_ p.c kompilieren, wie im folgenden Makefile gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d7028-110">To take advantage of these predefined functions, you need to invoke the Cpreprocessor /D (or -D) option when you compile the Dlldata.c and Example\_p.c files, as shown in the following makefile:</span></span>

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcndr.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJS) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

<span data-ttu-id="d7028-111">Wenn Sie diese Präprozessordefinitionen zur Kompilierzeit nicht angeben, werden diese Funktionen nicht automatisch definiert.</span><span class="sxs-lookup"><span data-stu-id="d7028-111">If you do not specify these preprocessor definitions at compile time, these functions are not automatically defined.</span></span> <span data-ttu-id="d7028-112">(Das heißt, die Makros in Rpcproxy.c werden auf nichts erweitert.) Sie müssten sie explizit in einer anderen Quelldatei definiert haben, deren Modul auch in der endgültigen Verknüpfung und Kompilierung in der C-Compilerbefehlszeile enthalten wäre.</span><span class="sxs-lookup"><span data-stu-id="d7028-112">(That is, the macros in Rpcproxy.c expand to nothing.) You would have to have defined them explicitly in another source file, whose module would also be included in the final linking and compilation on the C compiler command line.</span></span>

<span data-ttu-id="d7028-113">Wenn REGISTER \_ PROXY \_ DLL definiert ist, stellt Rpcproxy.h zusätzliche Steuerungen für die bedingte Kompilierung mit PROXY \_ CLSID=*guid,* PROXY \_ CLSID \_ IS=*explizitem Wert von GUID* und ENTRY \_ PREFIX=*Präfixzeichenfolge* bereit.</span><span class="sxs-lookup"><span data-stu-id="d7028-113">When REGISTER\_PROXY\_DLL is defined, Rpcproxy.h provides for additional conditional compilation control with PROXY\_CLSID=*guid*, PROXY\_CLSID\_IS=*explicit value of guid*, and ENTRY\_PREFIX=*prefix string*.</span></span> <span data-ttu-id="d7028-114">Diese Makrodefinitionen werden im MIDL-Programmierhandbuch unter [C-Compilerdefinitionen für Proxys/Stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d7028-114">These macro definitions are described in greater detail in [C-Compiler Definitions for Proxy/Stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) in the MIDL Programmer's Guide.</span></span>

## <a name="manually-registering-the-proxy-dll"></a><span data-ttu-id="d7028-115">Manuelles Registrieren der Proxy-DLL</span><span class="sxs-lookup"><span data-stu-id="d7028-115">Manually Registering the Proxy DLL</span></span>

<span data-ttu-id="d7028-116">Wenn Sie aus irgendeinem Grund die Standardroutinen für die Proxystubregistrierung nicht verwenden können, können Sie die DLL manuell registrieren, indem Sie der Systemregistrierung mithilfe von Regedt32.exe die folgenden Einträge hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d7028-116">If for some reason you cannot use the default proxy stub registration routines, you can manually register the DLL by adding the following entries to the system registry, using Regedt32.exe.</span></span>

```
HKEY_CLASSES_ROOT
   Interface
      iid
         (Default) = ICustomInterfaceName
         ProxyStubClsid32 = {clsid}
```

```
HKEY_CLASSES_ROOT
   CLSID
      clsid
         (Default) = ICustomInterfaceName_PSFactory
         InprocServer32 = proxstub.dll
```

## <a name="related-topics"></a><span data-ttu-id="d7028-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7028-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7028-118">C-Compilerdefinitionen für Proxys/Stubs</span><span class="sxs-lookup"><span data-stu-id="d7028-118">C-Compiler Definitions for Proxy/Stubs</span></span>](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[<span data-ttu-id="d7028-119">Registrieren von COM-Servern</span><span class="sxs-lookup"><span data-stu-id="d7028-119">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="d7028-120">Selbstregistrierung</span><span class="sxs-lookup"><span data-stu-id="d7028-120">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 
