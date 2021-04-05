---
title: C-compilerdefinitionen für Proxy/Stub
description: Die Header Datei Rpcproxy. h enthält die folgenden Makro Definitionen, die bei der Erstellung verteilter com-Anwendungen möglicherweise praktisch sind. Diese Makros werden mit dem präprozessorschalter/D (oder-D) zum Zeitpunkt der C-Kompilierung aufgerufen.
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- Mittel l-compilermittell, C-Compiler, Definitionen für Proxy/Stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1504c600c3f86a934ab3daa132b041c7310af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037358"
---
# <a name="c-compiler-definitions-for-proxystubs"></a><span data-ttu-id="ae5e4-105">C-compilerdefinitionen für Proxy/Stub</span><span class="sxs-lookup"><span data-stu-id="ae5e4-105">C-Compiler Definitions for Proxy/Stubs</span></span>

<span data-ttu-id="ae5e4-106">Die Header Datei Rpcproxy. h enthält die folgenden Makro Definitionen, die bei der Erstellung verteilter com-Anwendungen möglicherweise praktisch sind.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-106">The header file Rpcproxy.h includes the following macro definitions, each of which may be convenient when building distributed COM application.</span></span> <span data-ttu-id="ae5e4-107">Diese Makros werden mit dem präprozessorschalter [**/D**](-d.md) (oder-D) zum Zeitpunkt der C-Kompilierung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-107">These macros are invoked with the [**/D**](-d.md) (or -D) preprocessor switch at the C-compile time.</span></span>



| <span data-ttu-id="ae5e4-108">MACRO</span><span class="sxs-lookup"><span data-stu-id="ae5e4-108">MACRO</span></span>                                                                                                                                                                                           | <span data-ttu-id="ae5e4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ae5e4-109">Description</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae5e4-110">\_Proxy- \_ dll registrieren</span><span class="sxs-lookup"><span data-stu-id="ae5e4-110">REGISTER\_PROXY\_DLL</span></span>                                                                                                                                                                            | <span data-ttu-id="ae5e4-111">Generiert die Funktionen **DllMain**, **DllRegisterServer** und **DllUnregisterServer** für die automatische Registrierung einer Proxy-dll.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-111">Generates **DllMain**, **DllRegisterServer**, and **DllUnregisterServer** functions for automatically registering a proxy DLL.</span></span>                                                                                       |
| <span data-ttu-id="ae5e4-112">Proxy- \_ CLSID =<clsid></span><span class="sxs-lookup"><span data-stu-id="ae5e4-112">PROXY\_CLSID=<clsid></span></span>                                                                                                                                                                      | <span data-ttu-id="ae5e4-113">Gibt einen Klassen Bezeichner für den Server an.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-113">Specifies a class identifier for the server.</span></span> <span data-ttu-id="ae5e4-114">Wenn dieses Makro nicht definiert ist, ist die Standard-CLSID der erste Schnittstellen Bezeichner, den der Mittell-Compiler in der IDL-Spezifikation für den Proxy-/Stubserver trifft.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-114">If this macro is not defined, the default CLSID is the first interface identifier that the MIDL compiler encounters in the IDL specification for the Proxy/Stub server.</span></span> |
| <span data-ttu-id="ae5e4-115">Proxy- \_ CLSID \_ ist = {0x *8hexziffern*, 0x *4hexziffern*, 0x *4 Hexziffern*, {0x *2hexziffern*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexziffern*, 0x *2hexdigits*, 0x *2hexziffern*, 0x *2hexdigits*,}}</span><span class="sxs-lookup"><span data-stu-id="ae5e4-115">PROXY\_CLSID\_IS={0x *8hexdigits*, 0x *4hexdigits*,0x *4hexdigits*, {0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*,}}</span></span> | <span data-ttu-id="ae5e4-116">Gibt den Wert des Klassen Bezeichners des Servers im binären Hex-Format an.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-116">Specifies the value of the server's class identifier in binary hex format.</span></span>                                                                                                                                           |



 

<span data-ttu-id="ae5e4-117">Durch die Definition des Makros " **\_ Proxy- \_ dll registrieren** " beim Kompilieren von "dlldata. c" enthält die Proxy-/Stub-marshallingdll automatisch Standarddefinitionen für die Funktionen " **DllMain**", " **DllRegisterServer**" und " **DllUnregisterServer** ".</span><span class="sxs-lookup"><span data-stu-id="ae5e4-117">By defining the **REGISTER\_PROXY\_DLL** macro when compiling Dlldata.c, your proxy/stub marshaling DLL will automatically include default definitions for the **DllMain**, **DllRegisterServer**, and **DllUnregisterServer** functions.</span></span> <span data-ttu-id="ae5e4-118">Mit diesen Funktionen können Sie Ihre Proxy-dll selbst in der Systemregistrierung registrieren.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-118">You can use these functions to self-register your proxy DLL in the system registry.</span></span>

<span data-ttu-id="ae5e4-119">Dieser Standard Registrierungscode verwendet die GUID der ersten Schnittstelle, die als CLSID für die Registrierung des gesamten Proxy-/Stub-DLL-Servers gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-119">This default registration code uses the GUID of the first interface encountered as the CLSID for registering the entire proxy/stub DLL server.</span></span> <span data-ttu-id="ae5e4-120">COM verwendet diese CLSID später, um den kompilierten Proxy-/Stubserver für das Marshalling der Schnittstellen zu suchen und zu laden, die der Server für die Verarbeitung registriert hat.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-120">COM later uses this CLSID to locate and load the compiled proxy/stub server for the marshaling of any of the interfaces the server is registered to handle.</span></span> <span data-ttu-id="ae5e4-121">Wenn eine Anwendung einen Schnittstellen Methoden aufzurufen, der Thread-, Prozess-oder Computer Grenzen überschreitet, verwendet com den Registrierungs Eintrag der Schnittstellen Kennung, um den CLSID-Registrierungs Eintrag für den Proxy-/Stub-marshallingserver zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-121">When an application makes an interface method call that crosses thread, process, or computer boundaries, COM uses the interface identifier registry entry to locate the CLSID registry entry for the proxy/stub marshaling server.</span></span> <span data-ttu-id="ae5e4-122">Anschließend wird diese CLSID verwendet, um den Server zu laden (falls er nicht bereits geladen wurde), sodass der Schnittstellen Aufrufvorgang gemarshallt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-122">It then uses this CLSID to load the server (if it isn't already loaded) so that the interface call can then be marshaled.</span></span>

<span data-ttu-id="ae5e4-123">Verwenden Sie das **Proxy- \_ CLSID** = <clsid> -Makro, wenn Sie die CLSID des Proxy-/stubservers explizit angeben möchten, anstatt die Standard-CLSID zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-123">Use the **PROXY\_CLSID**=<clsid> macro when you want to explicitly specify the proxy/stub server's CLSID rather than rely on the default CLSID.</span></span> <span data-ttu-id="ae5e4-124">Wenn Sie z. b. eine standardmäßige marshallingdll als eigenen Prozess internen com-Server entwickeln, oder wenn Sie einen eigenen **DllMain** definieren müssen, um das Anfügen von dll-Prozessen zu verarbeiten \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ae5e4-124">For example, if you are building a standard marshaling DLL as your own in-process COM server, or if you need to define your own **DllMain** to handle DLL\_PROCESS\_ATTACH.</span></span>

<span data-ttu-id="ae5e4-125">Verwenden Sie die **Proxy- \_ CLSID \_ is**= Macro anstelle der **Proxy- \_ CLSID** , um den Wert der CLSID im binären Hexadezimal Format zu definieren, das das **definierende \_ GUID** -Makro verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-125">Use **PROXY\_CLSID\_IS**= macro instead of **PROXY\_CLSID** to define the value of the CLSID in the binary hexadecimal format that the **DEFINE\_GUID** macro uses.</span></span>

<span data-ttu-id="ae5e4-126">Beachten Sie auch, dass beim Ausführen der standardmäßigen **DllRegisterServer** -Funktion der Server bei ThreadingModel = both registriert wird.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-126">Also note that when the default **DllRegisterServer** function runs, it registers the server with ThreadingModel=Both.</span></span>

<span data-ttu-id="ae5e4-127">Im folgenden Makefile-Beispiel werden die Makros **Register \_ Proxy \_ dll** und **Proxy \_ CLSID**= verwendet:</span><span class="sxs-lookup"><span data-stu-id="ae5e4-127">The following makefile example uses the **REGISTER\_PROXY\_DLL** and **PROXY\_CLSID**= macros:</span></span>

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL \
    /DPROXY_CLSID=7a98c250-6808-11cf-b73b-00aa00b677a7
example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
```

<span data-ttu-id="ae5e4-128">Weitere Informationen zur [**/D**](-d.md) -Präprozessoroption finden Sie in der C-Compilerdokumentation.</span><span class="sxs-lookup"><span data-stu-id="ae5e4-128">For more information on the [**/D**](-d.md) preprocessor option, see your C compiler documentation.</span></span>

 

 




