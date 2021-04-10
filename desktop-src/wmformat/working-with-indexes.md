---
title: Arbeiten mit Indizes
description: Arbeiten mit Indizes
ms.assetid: 7daa4b29-0597-462d-ad65-135d0ef7362d
keywords:
- Windows Media-Format-SDK, Indizes
- Advanced Systems Format (ASF), Indizes
- ASF (Advanced Systems Format), Indizes
- Indizes, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34057046223daf2e16950e0e38b1b0db5df32c4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855764"
---
# <a name="working-with-indexes"></a><span data-ttu-id="7cb6c-107">Arbeiten mit Indizes</span><span class="sxs-lookup"><span data-stu-id="7cb6c-107">Working with Indexes</span></span>

<span data-ttu-id="7cb6c-108">Das Windows Media-Format-SDK unterstützt das Suchen und Durchsuchen von Inhalten durch Inhalte.</span><span class="sxs-lookup"><span data-stu-id="7cb6c-108">The Windows Media Format SDK supports seeking and striding through content.</span></span> <span data-ttu-id="7cb6c-109">Durchsuchen können Sie einen Speicherort auf der Zeitachse der Datei angeben, um die Wiedergabe zu starten.</span><span class="sxs-lookup"><span data-stu-id="7cb6c-109">Seeking enables you to specify a place on the file's timeline to begin playback.</span></span> <span data-ttu-id="7cb6c-110">Mithilfe von Strichs können Sie die Ausgabe einer Datei schnell vorwärts und zurückspulen.</span><span class="sxs-lookup"><span data-stu-id="7cb6c-110">Striding enables you to fast-forward and rewind the output of a file.</span></span> <span data-ttu-id="7cb6c-111">Dateien müssen indiziert werden, um diese Features nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="7cb6c-111">Files must be indexed to take advantage of these features.</span></span> <span data-ttu-id="7cb6c-112">Ein Index ist eine Reihe von Werten, die Positionen in der Datei (Präsentations Zeiten, Frame Nummern oder SMTPE-Zeit Codes) mit entsprechenden Offsets im Daten Abschnitt der Datei für jeden darstellen.</span><span class="sxs-lookup"><span data-stu-id="7cb6c-112">An index is a series of values representing positions in the file (either presentation times, frame numbers, or SMTPE time codes) with corresponding offsets into the data section of the file for each.</span></span> <span data-ttu-id="7cb6c-113">Die Indizierung ist für Videostreams besonders wichtig, da die Audiodatenstrom-Präsentationszeit leicht geschätzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7cb6c-113">Indexing is most important for video streams, as audio stream presentation time can be easily estimated.</span></span> <span data-ttu-id="7cb6c-114">Einige Audiodatenströme erfordern jedoch möglicherweise auch Indizes.</span><span class="sxs-lookup"><span data-stu-id="7cb6c-114">However, some audio streams may require indexes as well.</span></span> <span data-ttu-id="7cb6c-115">Standardmäßig indiziert der Writer alle neuen ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="7cb6c-115">By default, the writer will index every new ASF file.</span></span> <span data-ttu-id="7cb6c-116">Wenn Änderungen am Inhalt einer Datei vorgenommen werden, müssen Sie den Index selbst mithilfe des Indexer-Objekts aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7cb6c-116">If changes are made to the content of a file, you must refresh the index yourself using the indexer object.</span></span>

<span data-ttu-id="7cb6c-117">Der Indexer unterstützt sowohl eine temporale als auch eine Frame basierte Indizierung sowie die Indizierung auf der Grundlage von SMPTE-Zeit Codes (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="7cb6c-117">The indexer supports both temporal and frame-based indexing as well as indexing based on SMPTE time codes (if present).</span></span> <span data-ttu-id="7cb6c-118">Der Writer erstellt standardmäßig einen temporalen Index für jeden neuen Videostream, der in einer Datei codiert ist.</span><span class="sxs-lookup"><span data-stu-id="7cb6c-118">The writer will create a temporal index by default for every new video stream encoded to a file.</span></span> <span data-ttu-id="7cb6c-119">Der Indexer muss explizit konfiguriert und aufgerufen werden, um einen Frame-oder SMPTE-Zeit Code Index zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7cb6c-119">You must explicitly configure and call the indexer to create a frame-based or SMPTE time code index.</span></span>

<span data-ttu-id="7cb6c-120">Wenn Änderungen am Inhalt einer ASF-Datei vorgenommen werden, muss Sie erneut indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="7cb6c-120">When changes are made to the content of an ASF file, it must be indexed again.</span></span>

<span data-ttu-id="7cb6c-121">Die folgenden Abschnitte enthalten Beispielcode zum Ausführen allgemeiner Indizierungs Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="7cb6c-121">The following sections present example code for performing common indexing tasks.</span></span>

-   [<span data-ttu-id="7cb6c-122">So deaktivieren Sie die automatische Indizierung</span><span class="sxs-lookup"><span data-stu-id="7cb6c-122">To Disable Automatic Indexing</span></span>](to-disable-automatic-indexing.md)
-   [<span data-ttu-id="7cb6c-123">So konfigurieren Sie den Indexer</span><span class="sxs-lookup"><span data-stu-id="7cb6c-123">To Configure the Indexer</span></span>](to-configure-the-indexer.md)
-   [<span data-ttu-id="7cb6c-124">So indizieren Sie eine ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="7cb6c-124">To Index an ASF File</span></span>](to-index-an-asf-file.md)
-   [<span data-ttu-id="7cb6c-125">So verhindern Sie die Ausführung der Indizierung</span><span class="sxs-lookup"><span data-stu-id="7cb6c-125">To Stop Indexing in Progress</span></span>](to-stop-indexing-in-progress.md)

<span data-ttu-id="7cb6c-126">Außerdem wird in der Beispielanwendung dscopy die Verwendung des Indexers veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="7cb6c-126">In addition, the DSCopy sample application illustrates the use of the indexer.</span></span> <span data-ttu-id="7cb6c-127">Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="7cb6c-127">For more information, see [Sample Applications](sample-applications.md).</span></span>

 

 




