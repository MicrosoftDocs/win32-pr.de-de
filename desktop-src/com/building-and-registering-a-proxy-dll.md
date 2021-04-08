---
title: Entwickeln und Registrieren einer Proxy-dll
description: Wenn Sie Proxy/Stub-Marshalling für Ihre Anwendung ausgewählt haben, müssen die. c-und. h-Dateien, die von der mittleren l generiert werden, kompiliert und verknüpft werden, um eine Proxy-dll zu erstellen, und diese DLL muss in die Systemregistrierung eingegeben werden, damit Clients ihre Schnittstellen suchen können.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b0dcd28359172ff2f90391d44a66f8f51a4cbf
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730513"
---
# <a name="building-and-registering-a-proxy-dll"></a><span data-ttu-id="90f61-103">Entwickeln und Registrieren einer Proxy-dll</span><span class="sxs-lookup"><span data-stu-id="90f61-103">Building and Registering a Proxy DLL</span></span>

<span data-ttu-id="90f61-104">Wenn Sie Proxy/Stub-Marshalling für Ihre Anwendung ausgewählt haben, müssen die. c-und. h-Dateien, die von der mittleren l generiert werden, kompiliert und verknüpft werden, um eine Proxy-dll zu erstellen, und diese DLL muss in die Systemregistrierung eingegeben werden, damit Clients ihre Schnittstellen suchen können.</span><span class="sxs-lookup"><span data-stu-id="90f61-104">If you chose proxy/stub marshaling for your application, the .c and .h files that MIDL generated must be compiled and linked to create a proxy DLL, and that DLL must be entered into the system registry so that clients can locate your interfaces.</span></span> <span data-ttu-id="90f61-105">Die von der Mitte generierte Datei "dlldata. c" enthält die erforderlichen Routinen und weitere Informationen zum Erstellen und Registrieren einer Proxy-/Stub-DLL.</span><span class="sxs-lookup"><span data-stu-id="90f61-105">The MIDL-generated file Dlldata.c contains the necessary routines and other information to build and register a proxy/stub DLL.</span></span>

<span data-ttu-id="90f61-106">Der erste Schritt beim Erstellen der dll besteht darin, eine Modul Definitionsdatei für den Linker zu schreiben, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="90f61-106">The first step in building the DLL is to write a module definition file for the linker, as shown in the following example:</span></span>

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

<span data-ttu-id="90f61-107">Alternativ können Sie diese exportierten Funktionen in der Link Befehlszeile Ihres Makefile angeben.</span><span class="sxs-lookup"><span data-stu-id="90f61-107">Alternatively, you can specify these exported functions on the LINK command line of your makefile.</span></span>

<span data-ttu-id="90f61-108">Die exportierten Funktionen werden in RpcProxy. h deklariert, was dlldata. c umfasst, und Standard Implementierungen sind Teil der RPC-Lauf Zeit Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="90f61-108">The exported functions are declared in Rpcproxy.h, which Dlldata.c includes, and default implementations are part of the RPC run-time library.</span></span> <span data-ttu-id="90f61-109">COM verwendet diese Funktionen zum Erstellen einer Klassenfactory, zum Entladen von DLLs (nachdem sichergestellt ist, dass keine Objekte oder Sperren vorhanden sind), zum Abrufen von Informationen über die Proxy-dll und zum selbst registrieren und Aufheben der Registrierung der Proxy-dll.</span><span class="sxs-lookup"><span data-stu-id="90f61-109">COM uses these functions to create a class factory, unload DLLs (after making sure that no objects or locks exist), retrieve information about the proxy DLL, and to self-register and unregister the proxy DLL.</span></span> <span data-ttu-id="90f61-110">Um diese vordefinierten Funktionen nutzen zu können, müssen Sie die Option "cpreprocessor/D (oder-D)" aufrufen, wenn Sie die Dateien "dlldata. c" und "example \_ p. c" kompilieren, wie im folgenden Makefile gezeigt:</span><span class="sxs-lookup"><span data-stu-id="90f61-110">To take advantage of these predefined functions, you need to invoke the Cpreprocessor /D (or -D) option when you compile the Dlldata.c and Example\_p.c files, as shown in the following makefile:</span></span>

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
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(ORIXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

<span data-ttu-id="90f61-111">Wenn Sie diese Präprozessordefinitionen nicht zum Zeitpunkt der Kompilierung angeben, werden diese Funktionen nicht automatisch definiert.</span><span class="sxs-lookup"><span data-stu-id="90f61-111">If you do not specify these preprocessor definitions at compile time, these functions are not automatically defined.</span></span> <span data-ttu-id="90f61-112">(Das heißt, die Makros in RpcProxy. c werden zu Nothing erweitert.) Sie müssten diese explizit in einer anderen Quelldatei definieren, deren Modul auch in der endgültigen Verknüpfung und Kompilierung in der C-Compilerbefehlszeile enthalten wäre.</span><span class="sxs-lookup"><span data-stu-id="90f61-112">(That is, the macros in Rpcproxy.c expand to nothing.) You would have to have defined them explicitly in another source file, whose module would also be included in the final linking and compilation on the C compiler command line.</span></span>

<span data-ttu-id="90f61-113">Wenn \_ Proxy- \_ dll registrieren definiert ist, bietet RpcProxy. h zusätzliche bedingte Kompilierungs Steuerung mit Proxy \_ CLSID =*GUID*, Proxy \_ CLSID \_ ist =*expliziter Wert der GUID* und Eintrags \_ Präfix =*Präfix Zeichenfolge*.</span><span class="sxs-lookup"><span data-stu-id="90f61-113">When REGISTER\_PROXY\_DLL is defined, Rpcproxy.h provides for additional conditional compilation control with PROXY\_CLSID=*guid*, PROXY\_CLSID\_IS=*explicit value of guid*, and ENTRY\_PREFIX=*prefix string*.</span></span> <span data-ttu-id="90f61-114">Diese Makro Definitionen werden ausführlicher in [C-compilerdefinitionen für Proxy/Stub](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) im Programmier Handbuch für Mittel l beschrieben.</span><span class="sxs-lookup"><span data-stu-id="90f61-114">These macro definitions are described in greater detail in [C-Compiler Definitions for Proxy/Stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) in the MIDL Programmer's Guide.</span></span>

## <a name="manually-registering-the-proxy-dll"></a><span data-ttu-id="90f61-115">Manuelles Registrieren der Proxy-dll</span><span class="sxs-lookup"><span data-stu-id="90f61-115">Manually Registering the Proxy DLL</span></span>

<span data-ttu-id="90f61-116">Wenn Sie die standardmäßigen ProxyStub-Registrierungs Routinen aus irgendeinem Grund nicht verwenden können, können Sie die dll manuell registrieren, indem Sie die folgenden Einträge in der Systemregistrierung mithilfe von Regedt32.exe hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="90f61-116">If for some reason you cannot use the default proxy stub registration routines, you can manually register the DLL by adding the following entries to the system registry, using Regedt32.exe.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="90f61-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90f61-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90f61-118">C-compilerdefinitionen für Proxy/Stub</span><span class="sxs-lookup"><span data-stu-id="90f61-118">C-Compiler Definitions for Proxy/Stubs</span></span>](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[<span data-ttu-id="90f61-119">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="90f61-119">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="90f61-120">Selbstregistrierung</span><span class="sxs-lookup"><span data-stu-id="90f61-120">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 