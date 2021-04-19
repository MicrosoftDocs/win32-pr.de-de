---
description: In diesem Abschnitt wird der allgemeine Entwurf von Microsoft Media Foundation beschrieben. Weitere Informationen zum Verwenden von Media Foundation für bestimmte Programmieraufgaben finden Sie unter Media Foundation Programming Guide.
ms.assetid: 33820c6a-859d-4df6-a605-4e0f64f45c5b
title: Media Foundation-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0914b0f4c43966edcdc6d30efa7c9dbdbbd4e8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363035"
---
# <a name="media-foundation-architecture"></a><span data-ttu-id="3ef11-104">Media Foundation-Architektur</span><span class="sxs-lookup"><span data-stu-id="3ef11-104">Media Foundation Architecture</span></span>

<span data-ttu-id="3ef11-105">In diesem Abschnitt wird der allgemeine Entwurf von Microsoft Media Foundation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3ef11-105">This section describes the general design of Microsoft Media Foundation.</span></span> <span data-ttu-id="3ef11-106">Weitere Informationen zum Verwenden von Media Foundation für bestimmte Programmieraufgaben finden Sie unter [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span><span class="sxs-lookup"><span data-stu-id="3ef11-106">For information about using Media Foundation for specific programming tasks, see [Media Foundation Programming Guide](media-foundation-programming-guide.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3ef11-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="3ef11-107">In this section</span></span>



| <span data-ttu-id="3ef11-108">Thema</span><span class="sxs-lookup"><span data-stu-id="3ef11-108">Topic</span></span>                                                                                                         | <span data-ttu-id="3ef11-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ef11-109">Description</span></span>                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ef11-110">Übersicht über die Media Foundation-Architektur</span><span class="sxs-lookup"><span data-stu-id="3ef11-110">Overview of the Media Foundation Architecture</span></span>](overview-of-the-media-foundation-architecture.md)<br/> | <span data-ttu-id="3ef11-111">Bietet eine allgemeine Übersicht über die Media Foundation Architektur.</span><span class="sxs-lookup"><span data-stu-id="3ef11-111">Gives a high-level overview of the Media Foundation architecture.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="3ef11-112">Media Foundation primitiver</span><span class="sxs-lookup"><span data-stu-id="3ef11-112">Media Foundation Primitives</span></span>](media-foundation-primitives.md)<br/>                                     | <span data-ttu-id="3ef11-113">Beschreibt einige grundlegende Schnittstellen, die in Media Foundation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ef11-113">Describes some basic interfaces that are used throughout Media Foundation.</span></span><br/> <span data-ttu-id="3ef11-114">Fast alle Media Foundation Anwendungen verwenden diese Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="3ef11-114">Almost all Media Foundation applications will use these interfaces.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="3ef11-115">Media Foundation Plattform-APIs</span><span class="sxs-lookup"><span data-stu-id="3ef11-115">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)<br/>                               | <span data-ttu-id="3ef11-116">Beschreibt Kern Media Foundation Funktionen, z. b. asynchrone Rückrufe und Arbeits Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="3ef11-116">Describes core Media Foundation functions, such as asynchronous callbacks and work queues.</span></span><br/> <span data-ttu-id="3ef11-117">Einige Anwendungen verwenden möglicherweise Schnittstellen auf Platt Form Ebene.</span><span class="sxs-lookup"><span data-stu-id="3ef11-117">Some applications might use platform-level interfaces.</span></span> <span data-ttu-id="3ef11-118">Außerdem verwenden benutzerdefinierte Plug-ins, z. b. Medienquellen und MFTs, diese Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="3ef11-118">Also, custom plug-ins, such as media sources and MFTs, use these interfaces.</span></span><br/>                                       |
| [<span data-ttu-id="3ef11-119">Media Foundation Pipeline</span><span class="sxs-lookup"><span data-stu-id="3ef11-119">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)<br/>                                         | <span data-ttu-id="3ef11-120">Die Media Foundation Pipeline Schicht besteht aus Medienquellen, MFTs und Medien senken.</span><span class="sxs-lookup"><span data-stu-id="3ef11-120">The Media Foundation pipeline layer consists of media sources, MFTs, and media sinks.</span></span> <span data-ttu-id="3ef11-121">Die meisten Anwendungen werden Methoden nicht direkt auf der Pipeline Ebene aufruft.</span><span class="sxs-lookup"><span data-stu-id="3ef11-121">Most applications do not call methods directly on the pipeline layer.</span></span> <span data-ttu-id="3ef11-122">Stattdessen verwenden Anwendungen eine der höheren Ebenen, wie z. b. die Medien Sitzung oder den Quell-und senderwriter.</span><span class="sxs-lookup"><span data-stu-id="3ef11-122">Instead, applications use one of the higher layers, such as the Media Session or the Source Reader and Sink Writer.</span></span><br/> |
| [<span data-ttu-id="3ef11-123">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="3ef11-123">Media Session</span></span>](media-session.md)<br/>                                                                 | <span data-ttu-id="3ef11-124">Die Medien Sitzung verwaltet den Datenfluss in der Media Foundation Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3ef11-124">The Media Session manages data flow in the Media Foundation pipeline.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="3ef11-125">Quell Leser</span><span class="sxs-lookup"><span data-stu-id="3ef11-125">Source Reader</span></span>](source-reader.md)<br/>                                                                 | <span data-ttu-id="3ef11-126">Der Quell Reader ermöglicht einer Anwendung das Abrufen von Daten aus einer Medienquelle, ohne dass die Anwendung die Medienquellen-APIs direkt abrufen muss.</span><span class="sxs-lookup"><span data-stu-id="3ef11-126">The Source Reader enables an application to get data from a media source, without the applicating needing to call the media source APIs directly.</span></span> <span data-ttu-id="3ef11-127">Der Quell Leser kann auch die Decodierung von komprimierten Datenströmen ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ef11-127">The Source Reader can also perform decoding of compressed streams.</span></span><br/>                                                            |
| [<span data-ttu-id="3ef11-128">Geschützter Medien Pfad</span><span class="sxs-lookup"><span data-stu-id="3ef11-128">Protected Media Path</span></span>](protected-media-path.md)<br/>                                                   | <span data-ttu-id="3ef11-129">Der geschützte Medien Pfad (PMP) bietet eine geschützte Umgebung für die Wiedergabe von Premium-Videoinhalten.</span><span class="sxs-lookup"><span data-stu-id="3ef11-129">The protected media path (PMP) provides a protected environment for playing premium video content.</span></span> <span data-ttu-id="3ef11-130">Das PMP muss beim Schreiben einer Media Foundation Anwendung nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ef11-130">It is not necessary to use the PMP when writing a Media Foundation application.</span></span> <br/>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="3ef11-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3ef11-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ef11-132">Info über Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3ef11-132">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="3ef11-133">Media Foundation: Grundlegende Konzepte</span><span class="sxs-lookup"><span data-stu-id="3ef11-133">Media Foundation: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[<span data-ttu-id="3ef11-134">Media Foundation und com</span><span class="sxs-lookup"><span data-stu-id="3ef11-134">Media Foundation and COM</span></span>](media-foundation-and-com.md)
</dt> <dt>

[<span data-ttu-id="3ef11-135">Media Foundation-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="3ef11-135">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




