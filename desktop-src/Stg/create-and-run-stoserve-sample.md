---
title: Beispiel zum Erstellen und Ausführen von stoservice
description: Das Client Beispiel und andere verwandte Beispiele müssen kompiliert werden, bevor Sie den Client ausführen können.
ms.assetid: 7d8fe758-0008-495d-89ae-a814cb07ea19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46645351eb75ceb6b4f6129049b9e8f2db59dbef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341440"
---
# <a name="create-and-run-stoserve-sample"></a><span data-ttu-id="00324-103">Beispiel zum Erstellen und Ausführen von stoservice</span><span class="sxs-lookup"><span data-stu-id="00324-103">Create and Run StoServe Sample</span></span>

<span data-ttu-id="00324-104">Das Client Beispiel und andere verwandte Beispiele müssen kompiliert werden, bevor Sie den Client ausführen können.</span><span class="sxs-lookup"><span data-stu-id="00324-104">The client sample and other related samples must be compiled before you can run the client.</span></span> <span data-ttu-id="00324-105">Weitere Informationen zum Erstellen der Beispiele finden Sie unter [Erstellen von Beispielen](how-to-build-samples.md).</span><span class="sxs-lookup"><span data-stu-id="00324-105">For more details on building the samples, see [How to Build Samples](how-to-build-samples.md).</span></span> <span data-ttu-id="00324-106">Wenn Sie bereits die entsprechenden Beispiele erstellt haben, ist STOCLIEN.EXE die ausführbare Client Datei, die für das **stoservice** -Beispiel ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="00324-106">If you have already built the appropriate samples, STOCLIEN.EXE is the client executable to run for the **StoServe** sample.</span></span>

## <a name="code-tour"></a><span data-ttu-id="00324-107">Codetour</span><span class="sxs-lookup"><span data-stu-id="00324-107">Code Tour</span></span>

<span data-ttu-id="00324-108">In der folgenden Tabelle sind die für das **stoservice** -Beispiel relevanten Dateien aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="00324-108">The following table lists the files pertinent to the **StoServe** sample.</span></span>



| <span data-ttu-id="00324-109">Dateien</span><span class="sxs-lookup"><span data-stu-id="00324-109">Files</span></span>        | <span data-ttu-id="00324-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00324-110">Description</span></span>                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00324-111">STOSERVE.TXT</span><span class="sxs-lookup"><span data-stu-id="00324-111">STOSERVE.TXT</span></span> | <span data-ttu-id="00324-112">Kurze Beispiel Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00324-112">Short sample description</span></span>                                                                                                  |
| <span data-ttu-id="00324-113">Makefile</span><span class="sxs-lookup"><span data-stu-id="00324-113">MAKEFILE</span></span>     | <span data-ttu-id="00324-114">Das generische Makefile zum Entwickeln des STOSERVE.DLL Code Beispiels für diese Lektion.</span><span class="sxs-lookup"><span data-stu-id="00324-114">The generic makefile for building the STOSERVE.DLL code sample of this lesson.</span></span>                                            |
| <span data-ttu-id="00324-115">Stoservice. Micha</span><span class="sxs-lookup"><span data-stu-id="00324-115">STOSERVE.H</span></span>   | <span data-ttu-id="00324-116">Die Includedatei zum Deklarieren als importiert oder definiert als exportierter Dienstfunktionen in STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="00324-116">The include file for declaring as imported or defining as exported the service functions in STOSERVE.DLL.</span></span>                 |
| <span data-ttu-id="00324-117">Stoservice. CPP</span><span class="sxs-lookup"><span data-stu-id="00324-117">STOSERVE.CPP</span></span> | <span data-ttu-id="00324-118">Die Haupt Implementierungs Datei für STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="00324-118">The main implementation file for STOSERVE.DLL.</span></span> <span data-ttu-id="00324-119">Verfügt über die DllMain-und die com-Serverfunktionen (z. b. DllGetClassObject).</span><span class="sxs-lookup"><span data-stu-id="00324-119">Has DllMain and the COM server functions (for example, DllGetClassObject).</span></span> |
| <span data-ttu-id="00324-120">Stoservice. Auflösenden</span><span class="sxs-lookup"><span data-stu-id="00324-120">STOSERVE.DEF</span></span> | <span data-ttu-id="00324-121">Die Modul Definitionsdatei.</span><span class="sxs-lookup"><span data-stu-id="00324-121">The module definition file.</span></span> <span data-ttu-id="00324-122">Exportiert Server-Wohnfunktionen.</span><span class="sxs-lookup"><span data-stu-id="00324-122">Exports server housing functions.</span></span>                                                             |
| <span data-ttu-id="00324-123">Stoservice. RC</span><span class="sxs-lookup"><span data-stu-id="00324-123">STOSERVE.RC</span></span>  | <span data-ttu-id="00324-124">Die dll-Ressourcen Definitionsdatei für die ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="00324-124">The DLL resource definition file for the executable.</span></span>                                                                      |
| <span data-ttu-id="00324-125">Stoservice. ICO</span><span class="sxs-lookup"><span data-stu-id="00324-125">STOSERVE.ICO</span></span> | <span data-ttu-id="00324-126">Die Symbol Ressource für die ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="00324-126">The icon resource for the executable.</span></span>                                                                                     |
| <span data-ttu-id="00324-127">Servers. Micha</span><span class="sxs-lookup"><span data-stu-id="00324-127">SERVER.H</span></span>     | <span data-ttu-id="00324-128">Die Includedatei für das Server Steuerelement C++-Objekt.</span><span class="sxs-lookup"><span data-stu-id="00324-128">The include file for the server control C++ object.</span></span>                                                                       |
| <span data-ttu-id="00324-129">Servers. CPP</span><span class="sxs-lookup"><span data-stu-id="00324-129">SERVER.CPP</span></span>   | <span data-ttu-id="00324-130">Die Implementierungs Datei für das Server Steuerelement C++-Objekt.</span><span class="sxs-lookup"><span data-stu-id="00324-130">The implementation file for the server control C++ object.</span></span>                                                                |
| <span data-ttu-id="00324-131">Schen. Micha</span><span class="sxs-lookup"><span data-stu-id="00324-131">FACTORY.H</span></span>    | <span data-ttu-id="00324-132">Die Includedatei für die Klassenfactory-com-Objekte des Servers.</span><span class="sxs-lookup"><span data-stu-id="00324-132">The include file for the server's class factory COM objects.</span></span>                                                              |
| <span data-ttu-id="00324-133">Schen. CPP</span><span class="sxs-lookup"><span data-stu-id="00324-133">FACTORY.CPP</span></span>  | <span data-ttu-id="00324-134">Die Implementierungs Datei für die Klassenfactorys des Servers.</span><span class="sxs-lookup"><span data-stu-id="00324-134">The implementation file for the server's class factories.</span></span>                                                                 |
| <span data-ttu-id="00324-135">Herzustellen. Micha</span><span class="sxs-lookup"><span data-stu-id="00324-135">CONNECT.H</span></span>    | <span data-ttu-id="00324-136">Die Includedatei für den Verbindungspunkt-Enumerator, den Verbindungspunkt und die Verbindungs Enumeratorklassen.</span><span class="sxs-lookup"><span data-stu-id="00324-136">The include file for the connection point enumerator, connection point, and connection enumerator classes.</span></span>                |
| <span data-ttu-id="00324-137">Herzustellen. CPP</span><span class="sxs-lookup"><span data-stu-id="00324-137">CONNECT.CPP</span></span>  | <span data-ttu-id="00324-138">Die Implementierungs Datei für den Verbindungspunkt-Enumerator, den Verbindungspunkt und die Verbindungs Enumeratorobjekte.</span><span class="sxs-lookup"><span data-stu-id="00324-138">The implementation file for the connection point enumerator, connection point, and connection enumerator objects.</span></span>         |
| <span data-ttu-id="00324-139">Zeitung. Micha</span><span class="sxs-lookup"><span data-stu-id="00324-139">PAPER.H</span></span>      | <span data-ttu-id="00324-140">Die Includedatei für die copaper-com-Objektklasse.</span><span class="sxs-lookup"><span data-stu-id="00324-140">The include file for the COPaper COM object class.</span></span>                                                                        |
| <span data-ttu-id="00324-141">Zeitung. CPP</span><span class="sxs-lookup"><span data-stu-id="00324-141">PAPER.CPP</span></span>    | <span data-ttu-id="00324-142">Die Implementierungs Datei für die copaper-com-Objektklasse und die Verbindungspunkte.</span><span class="sxs-lookup"><span data-stu-id="00324-142">The implementation file for the COPaper COM object class and the connection points.</span></span>                                       |
| <span data-ttu-id="00324-143">Stoservice. DSP</span><span class="sxs-lookup"><span data-stu-id="00324-143">STOSERVE.DSP</span></span> | <span data-ttu-id="00324-144">Microsoft Visual Studio Projektdatei.</span><span class="sxs-lookup"><span data-stu-id="00324-144">Microsoft Visual Studio Project file.</span></span>                                                                                     |



 

<span data-ttu-id="00324-145">Die wichtigsten Themen, die in dieser codetour behandelt werden, sind:</span><span class="sxs-lookup"><span data-stu-id="00324-145">The major topics covered in this code tour are:</span></span>

-   <span data-ttu-id="00324-146">Die [**iPaper**](ipaper-methods.md) -Schnittstellen Methoden.</span><span class="sxs-lookup"><span data-stu-id="00324-146">The [**IPaper**](ipaper-methods.md) interface methods.</span></span>
-   <span data-ttu-id="00324-147">Verwendung der [**ipapersink**](ipapersink-methods.md) -Schnittstelle für Client Benachrichtigungen durch copaper.</span><span class="sxs-lookup"><span data-stu-id="00324-147">COPaper's use of the [**IPaperSink**](ipapersink-methods.md) interface for client notifications.</span></span>
-   <span data-ttu-id="00324-148">[**Strukturen**](structures---stoserve.md) in stoservice.</span><span class="sxs-lookup"><span data-stu-id="00324-148">[**Structures**](structures---stoserve.md) in StoServe.</span></span>
-   <span data-ttu-id="00324-149">[Überlegungen zu Unicode](unicode-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="00324-149">[Unicode considerations](unicode-considerations.md).</span></span>

 

 




