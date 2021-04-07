---
title: Microsoft Interface Definition Language
description: Der Microsoft Interface Definition Language (mittlerer l) definiert Schnittstellen zwischen Client-und Serverprogrammen.
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- Mittel l
- Mittel l-Mitte (siehe Microsoft Interface Definition Language-Mitte)
- Microsoft Interface Definition Language-Mittell
- Microsoft Interface Definition Language-Mittell, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e274d66ae234205f5db1f41b2d191ea409561bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038887"
---
# <a name="microsoft-interface-definition-language"></a><span data-ttu-id="9e0d7-107">Microsoft Interface Definition Language</span><span class="sxs-lookup"><span data-stu-id="9e0d7-107">Microsoft Interface Definition Language</span></span>

## <a name="purpose"></a><span data-ttu-id="9e0d7-108">Zweck</span><span class="sxs-lookup"><span data-stu-id="9e0d7-108">Purpose</span></span>

<span data-ttu-id="9e0d7-109">Der Microsoft Interface Definition Language (mittlerer l) definiert Schnittstellen zwischen Client-und Serverprogrammen.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-109">The Microsoft Interface Definition Language (MIDL) defines interfaces between client and server programs.</span></span> <span data-ttu-id="9e0d7-110">Microsoft umfasst den Mittel l-Compiler mit dem Platform Software Development Kit (SDK), mit dem Entwickler die IDL-Dateien (Interface Definition Language) und die Anwendungs Konfigurationsdateien (ACF) erstellen können, die für Remote Prozedur Aufrufe (RPC)-Schnittstellen und com/DCOM-Schnittstellen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-110">Microsoft includes the MIDL compiler with the Platform Software Development Kit (SDK) to enable developers to create the interface definition language (IDL) files and application configuration files (ACF) required for remote procedure call (RPC) interfaces and COM/DCOM interfaces.</span></span> <span data-ttu-id="9e0d7-111">Die Generierung von Typbibliotheken für OLE-Automatisierung wird von der mittleren l ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-111">MIDL also supports the generation of type libraries for OLE Automation.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="9e0d7-112">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="9e0d7-112">Where applicable</span></span>

<span data-ttu-id="9e0d7-113">Die mittlere Größe kann in allen Client-/Server-Anwendungen verwendet werden, die auf Windows-Betriebssystemen basieren.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-113">MIDL can be used in all client/server applications based on Windows operating systems.</span></span> <span data-ttu-id="9e0d7-114">Sie kann auch zum Erstellen von Client-und Serverprogrammen für heterogene Netzwerkumgebungen verwendet werden, die solche Betriebssysteme wie UNIX und Apple enthalten.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-114">It can also be used to create client and server programs for heterogeneous network environments that include such operating systems as Unix and Apple.</span></span> <span data-ttu-id="9e0d7-115">Microsoft unterstützt den Open Group-DCE-Standard (früher als Open Software Foundation bezeichnet) für die RPC-Interoperabilität.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-115">Microsoft supports the Open Group (formerly known as the Open Software Foundation) DCE standard for RPC interoperability.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9e0d7-116">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="9e0d7-116">Developer audience</span></span>

<span data-ttu-id="9e0d7-117">Bei Verwendung von "Mittel l" mit RPC ist Vertrautheit mit der C/C++-Programmierung und dem RPC-Paradigma erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-117">When using MIDL with RPC, familiarity with C/C++ programming and the RPC paradigm is required.</span></span> <span data-ttu-id="9e0d7-118">Bei Verwendung von "Mittel l mit com" ist Vertrautheit mit der C++-Programmierung und dem RPC-Paradigma für com erforderlich, oder alternativ müssen Sie sich mit der Skripterstellung für OLE-Automatisierungs Modelle und Typbibliotheken vertraut machen.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-118">When using MIDL with COM, familiarity with C++ programming and the RPC paradigm as it applies to COM is required, or alternatively, familiarity with OLE Automation model scripting and type libraries is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9e0d7-119">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="9e0d7-119">Run-time requirements</span></span>

<span data-ttu-id="9e0d7-120">Die entsprechenden Laufzeitbibliotheken für die Verwendung von "Mittel l" sind in Windows enthalten.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-120">The appropriate run-time libraries for using MIDL are included with Windows.</span></span> <span data-ttu-id="9e0d7-121">Der mittlerer l-Compiler und die Komponenten der RPC-Entwicklungsumgebung werden installiert, wenn Sie die Windows SDK installieren.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-121">The MIDL compiler and the components of the RPC development environment are installed when you install the Windows SDK.</span></span> <span data-ttu-id="9e0d7-122">Weitere Informationen finden Sie unter [Verwenden des Mittel l-Compilers](using-the-midl-compiler-2.md) und [Installieren der RPC-Programmierumgebung](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span><span class="sxs-lookup"><span data-stu-id="9e0d7-122">For more information, see [Using the MIDL Compiler](using-the-midl-compiler-2.md) and [Installing the RPC Programming Environment](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9e0d7-123">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9e0d7-123">In this section</span></span>



| <span data-ttu-id="9e0d7-124">Thema</span><span class="sxs-lookup"><span data-stu-id="9e0d7-124">Topic</span></span>                                                                                               | <span data-ttu-id="9e0d7-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e0d7-125">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="9e0d7-126">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9e0d7-126">Overview</span></span>](about-this-guide-2.md)<br/>                                                       | <span data-ttu-id="9e0d7-127">Allgemeine Informationen über die Mitte und den Mittel l-Compiler.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-127">General information about MIDL and the MIDL compiler.</span></span><br/>                   |
| [<span data-ttu-id="9e0d7-128">Verwenden des Mittel l-Compilers</span><span class="sxs-lookup"><span data-stu-id="9e0d7-128">Using the MIDL Compiler</span></span>](using-the-midl-compiler-2.md)<br/>                                 | <span data-ttu-id="9e0d7-129">Informationen zum Verwenden des-Mittell-Compilers zum Generieren von RPC-Stubdaten.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-129">Information about using the MIDL compilter to generate RPC stubs.</span></span><br/>       |
| [<span data-ttu-id="9e0d7-130">Schnittstellendefinitionen und Typbibliotheken</span><span class="sxs-lookup"><span data-stu-id="9e0d7-130">Interface Definitions and Type Libraries</span></span>](interface-definitions-and-type-libraries.md)<br/> | <span data-ttu-id="9e0d7-131">Dokumentation zu RPC-spezifischen Schnittstellendefinitionen und Typbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-131">Documentation of RPC-specific interface definitions and type libraries.</span></span><br/> |
| [<span data-ttu-id="9e0d7-132">Mittlere Command-Line Referenz</span><span class="sxs-lookup"><span data-stu-id="9e0d7-132">MIDL Command-Line Reference</span></span>](midl-command-line-reference.md)<br/>                           | <span data-ttu-id="9e0d7-133">Dokumentation der Mittell-compilerbefehlszeilenschalter.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-133">Documentation of the MIDL compiler command-line switches.</span></span><br/>               |
| [<span data-ttu-id="9e0d7-134">Mittel l-Sprachreferenz</span><span class="sxs-lookup"><span data-stu-id="9e0d7-134">MIDL Language Reference</span></span>](midl-language-reference.md)<br/>                                   | <span data-ttu-id="9e0d7-135">Die Mittel l-compilersprachreferenz.</span><span class="sxs-lookup"><span data-stu-id="9e0d7-135">The MIDL compiler language reference.</span></span><br/>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="9e0d7-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e0d7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e0d7-137">Remote Prozedur Aufruf (RPC)</span><span class="sxs-lookup"><span data-stu-id="9e0d7-137">Remote Procedure Call (RPC)</span></span>](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

