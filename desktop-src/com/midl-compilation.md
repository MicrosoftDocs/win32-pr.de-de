---
title: Kompilierung in mittlerer l
description: Kompilierung in mittlerer l
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281fa66ec1b8f997dd58fc55a67c19a801d2d36
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474341"
---
# <a name="midl-compilation"></a><span data-ttu-id="7d09c-103">Kompilierung in mittlerer l</span><span class="sxs-lookup"><span data-stu-id="7d09c-103">MIDL Compilation</span></span>

<span data-ttu-id="7d09c-104">Wenn eine IDL-Datei, wie z [. b. "example2". idl](anatomy-of-an-idl-file.md), eine oder mehrere COM-Schnittstellen und eine Typbibliothek definiert, generiert der mittlerer l-Compiler (Midl.exe) die in der folgenden Tabelle beschriebenen Dateien als Standardausgabe.</span><span class="sxs-lookup"><span data-stu-id="7d09c-104">Given an IDL file, such as [Example2.idl](anatomy-of-an-idl-file.md), that defines one or more COM interfaces and a type library, the MIDL compiler (Midl.exe) generates the files described in the following table as the default output.</span></span>



| <span data-ttu-id="7d09c-105">Dateiname</span><span class="sxs-lookup"><span data-stu-id="7d09c-105">Filename</span></span>                 | <span data-ttu-id="7d09c-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d09c-106">Description</span></span>                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d09c-107">"Example2". h</span><span class="sxs-lookup"><span data-stu-id="7d09c-107">Example2.h</span></span><br/>    | <span data-ttu-id="7d09c-108">Die Header Datei, die Typdefinitionen und Funktions Deklarationen für alle Schnittstellen enthält, die in der IDL-Datei definiert sind, sowie vorwärts Deklarationen für Routinen, die vom stubbefehl aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7d09c-108">The header file, containing type definitions and function declarations for all of the interfaces defined in the IDL file as well as forward declarations for routines that the stubs call.</span></span><br/> |
| <span data-ttu-id="7d09c-109">"Example2" \_ p. c</span><span class="sxs-lookup"><span data-stu-id="7d09c-109">Example2\_p.c</span></span><br/> | <span data-ttu-id="7d09c-110">Die Proxy-/Stubdatei, die die Ersatz Einstiegspunkte für-Clients und für-Server enthält.</span><span class="sxs-lookup"><span data-stu-id="7d09c-110">The proxy/stub file, which includes the surrogate entry points both for clients and for servers.</span></span><br/>                                                                                           |
| <span data-ttu-id="7d09c-111">"Example2" \_ i. c</span><span class="sxs-lookup"><span data-stu-id="7d09c-111">Example2\_i.c</span></span><br/> | <span data-ttu-id="7d09c-112">Die Schnittstellen-ID-Datei, die die GUID für jede Schnittstelle definiert, die in der IDL-Datei angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7d09c-112">The interface ID file, which defines the GUID for every interface specified in the IDL file.</span></span><br/>                                                                                               |
| <span data-ttu-id="7d09c-113">"Example2". tlb</span><span class="sxs-lookup"><span data-stu-id="7d09c-113">Example2.tlb</span></span><br/>  | <span data-ttu-id="7d09c-114">Eine Verbund Dokument Datei, die Informationen zu Typen und Objekten enthält.</span><span class="sxs-lookup"><span data-stu-id="7d09c-114">A compound document file that contains information about types and objects.</span></span><br/>                                                                                                                |
| <span data-ttu-id="7d09c-115">Dlldata. c</span><span class="sxs-lookup"><span data-stu-id="7d09c-115">Dlldata.c</span></span><br/>     | <span data-ttu-id="7d09c-116">Enthält die Daten, die Sie benötigen, um eine Proxy-/Stub-DLL zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7d09c-116">Contains the data you need to create a proxy/stub DLL.</span></span><br/>                                                                                                                                     |



 

<span data-ttu-id="7d09c-117">Verwenden Sie die Header Datei und alle c-Dateien, um [eine Proxy-dll zu erstellen](building-and-registering-a-proxy-dll.md) , die die-Schnittstelle unterstützen kann, wenn Sie sowohl von Client Anwendungen als auch von Objekt Servern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7d09c-117">You use the header file and all of the .c files to [create a proxy DLL](building-and-registering-a-proxy-dll.md) that can support the interface when used both by client applications and by object servers.</span></span> <span data-ttu-id="7d09c-118">\_Beim Erstellen der ausführbaren Datei für eine Client Anwendung, die die-Schnittstelle verwendet, verwenden Sie die Schnittstellen Header Datei ("example2". h) und die Interface-ID-Datei ("example2" i. c).</span><span class="sxs-lookup"><span data-stu-id="7d09c-118">You use the interface header file (Example2.h) and the interface ID (Example2\_i.c) file when creating the executable file for a client application that uses the interface.</span></span> <span data-ttu-id="7d09c-119">Sie können wählen, ob Sie die Typbibliotheks Datei als Ressource in die exe-oder DLL-Datei einschließen möchten, oder Sie können Sie als separate Datei versenden.</span><span class="sxs-lookup"><span data-stu-id="7d09c-119">You can choose to include the type library file as a resource in your EXE or DLL, or you can ship it as a separate file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d09c-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7d09c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d09c-121">Für eine COM-Schnittstelle generierte Dateien</span><span class="sxs-lookup"><span data-stu-id="7d09c-121">Files Generated for a COM Interface</span></span>](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[<span data-ttu-id="7d09c-122">Mittel l-Compileroptionen</span><span class="sxs-lookup"><span data-stu-id="7d09c-122">MIDL Compiler Options</span></span>](midl-compiler-options.md)
</dt> </dl>

 

