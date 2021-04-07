---
title: Indexer-Objekt
description: Indexer-Objekt
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- Windows Media-Format-SDK, Indexer-Objekte
- Advanced Systems Format (ASF), Indexer-Objekte
- ASF (Advanced Systems Format), Indexer-Objekte
- Objekte, Indexer-Objekte
- Indexer-Objekte
- Indizes, Indexer-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c9aa8c1c3ff694ae8e125e17dc0190451c7f21
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104038667"
---
# <a name="indexer-object"></a><span data-ttu-id="202fa-109">Indexer-Objekt</span><span class="sxs-lookup"><span data-stu-id="202fa-109">Indexer Object</span></span>

<span data-ttu-id="202fa-110">Das Indexer-Objekt erstellt einen Index in einer ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="202fa-110">The indexer object creates an index in an ASF file.</span></span> <span data-ttu-id="202fa-111">Ein Index ist ein Standard Teil einer ASF-Datei, der Videobeispiele mit Uhrzeiten, Frame Nummern oder (falls zutreffend) Struktur von Bewegungsbild-und Fernseh Technikern (SMPTE) Standardzeit Stempeln zuweist.</span><span class="sxs-lookup"><span data-stu-id="202fa-111">An index is a standard part of an ASF file that equates video samples with times, frame numbers, or (if applicable) Society of Motion Picture and Television Engineers (SMPTE) standard time stamps.</span></span> <span data-ttu-id="202fa-112">Ohne einen Index kann weder das Reader-Objekt noch das synchrone Reader-Objekt zu einem Punkt in der Mitte einer Datei suchen.</span><span class="sxs-lookup"><span data-stu-id="202fa-112">Without an index, neither the reader object nor the synchronous reader object can seek to a point in the middle of a file.</span></span>

<span data-ttu-id="202fa-113">Indizes, die von diesem-Objekt erstellt wurden, sind nur erforderlich, wenn die Datei mindestens einen Videostream enthält.</span><span class="sxs-lookup"><span data-stu-id="202fa-113">Indexes created by this object are only necessary if the file contains one or more video streams.</span></span> <span data-ttu-id="202fa-114">Dies liegt daran, dass Audiodaten nicht temporlig komprimiert werden, sodass eine bestimmte Uhrzeit in einem Audiostream leicht zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="202fa-114">This is because audio data is not temporally compressed, making it easy to find a given time in an audio stream.</span></span>

<span data-ttu-id="202fa-115">Das Indexer-Objekt wird von der [**wmkreateindexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) -Funktion erstellt, mit der ein Zeiger auf eine **iwmindexer** -Schnittstelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="202fa-115">The indexer object is created by the [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) function, which sets a pointer to an **IWMIndexer** interface.</span></span> <span data-ttu-id="202fa-116">Die anderen Schnittstellen des Indexer-Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="202fa-116">The other interfaces of the indexer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="202fa-117">Die folgenden Schnittstellen werden vom Indexer-Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="202fa-117">The following interfaces are supported by the indexer object.</span></span>



| <span data-ttu-id="202fa-118">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="202fa-118">Interface</span></span>                          | <span data-ttu-id="202fa-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="202fa-119">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="202fa-120">**Iwmindexer**</span><span class="sxs-lookup"><span data-stu-id="202fa-120">**IWMIndexer**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | <span data-ttu-id="202fa-121">Startet und beendet den Index Vorgang.</span><span class="sxs-lookup"><span data-stu-id="202fa-121">Starts and stops the indexing process.</span></span>                                              |
| [<span data-ttu-id="202fa-122">**IWMIndexer2**</span><span class="sxs-lookup"><span data-stu-id="202fa-122">**IWMIndexer2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | <span data-ttu-id="202fa-123">Konfiguriert den Indexer, um die Indizierung nach Frame, Zeit oder SMPTE-Zeit Code zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="202fa-123">Configures the indexer, enabling indexing by frame, by time, or by SMPTE time code.</span></span> |



 

<span data-ttu-id="202fa-124">Die folgende Rückruf Schnittstelle muss von der Anwendung implementiert werden, damit das Indexer-Objekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="202fa-124">The following callback interface must be implemented by the application in order to use the indexer object.</span></span>



| <span data-ttu-id="202fa-125">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="202fa-125">Interface</span></span>                                      | <span data-ttu-id="202fa-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="202fa-126">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="202fa-127">**Iwmstatus Callback**</span><span class="sxs-lookup"><span data-stu-id="202fa-127">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="202fa-128">Empfängt Statusmeldungen von Prozessen, die in einem separaten Thread ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="202fa-128">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="202fa-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="202fa-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="202fa-130">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="202fa-130">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="202fa-131">**Arbeiten mit Indizes**</span><span class="sxs-lookup"><span data-stu-id="202fa-131">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




