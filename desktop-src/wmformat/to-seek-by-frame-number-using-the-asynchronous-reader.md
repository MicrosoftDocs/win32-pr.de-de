---
title: So suchen Sie nach der Frame Nummer mithilfe des asynchronen Readers
description: So suchen Sie nach der Frame Nummer mithilfe des asynchronen Readers
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- Advanced Systems Format (ASF), Suche nach Frame Nummern
- ASF (Advanced Systems Format), Suche nach Frame Nummern
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- asynchrone Leser, suchen nach Frame Nummern
- Videostreams, suchen nach Frame Nummern
- Videostreams, asynchrone Leser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 169f5e1ac1e6034bc1db6f610e80af50dd3a0215
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038539"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a><span data-ttu-id="343e2-110">So suchen Sie nach der Frame Nummer mithilfe des asynchronen Readers</span><span class="sxs-lookup"><span data-stu-id="343e2-110">To Seek By Frame Number Using the Asynchronous Reader</span></span>

<span data-ttu-id="343e2-111">Das asynchrone Reader-Objekt kann verwendet werden, um die Frame Nummern von Videostreams in einer ASF-Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="343e2-111">The asynchronous reader object can be used to seek to the frame numbers of video streams in an ASF file.</span></span> <span data-ttu-id="343e2-112">Um Frame basiertes suchen zu verwenden, muss die im Reader geladene Datei nach Frame indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="343e2-112">To use frame-based seeking, the file loaded in the reader must be indexed by frame.</span></span> <span data-ttu-id="343e2-113">Jeder einzelne Videostream kann indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="343e2-113">Each individual video stream can be indexed.</span></span> <span data-ttu-id="343e2-114">Um zu ermitteln, ob ein Stream nach Frame indiziert wurde, können Sie das \_ Attribut g wszwmnumofframes im Header der Datei durch Aufrufen von [**iwmheaderinfo:: getattributebyname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)überprüfen.</span><span class="sxs-lookup"><span data-stu-id="343e2-114">To determine whether a stream has been indexed by frame, you can check the g\_wszWMNumberOfFrames attribute in the header of the file by calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span>

<span data-ttu-id="343e2-115">Führen Sie die folgenden Schritte aus, um mithilfe des asynchronen Readers Daten in einer ASF-Datei nach Frame Nummer zu suchen.</span><span class="sxs-lookup"><span data-stu-id="343e2-115">To seek data in an ASF file by frame number using the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="343e2-116">Abrufen eines Zeigers auf die [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) -Schnittstelle des Reader-Objekts durch Aufrufen von **iwmreader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="343e2-116">Obtain a pointer to the [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="343e2-117">Legen Sie die Nummer und Dauer des Start Rahmens durch Aufrufen von [**IWMReaderAdvanced3:: startatposition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition)fest.</span><span class="sxs-lookup"><span data-stu-id="343e2-117">Set the starting frame number and duration by calling [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span></span> <span data-ttu-id="343e2-118">Sie müssen die streamnummer eines Frame indizierten Videostreams angeben.</span><span class="sxs-lookup"><span data-stu-id="343e2-118">You must specify the stream number of a frame-indexed video stream.</span></span> <span data-ttu-id="343e2-119">Der Reader synchronisiert den Rest der Ausgaben mit der Präsentationszeit des angegebenen Frames des angegebenen Streams und beginnt damit, Ausgabe Beispiele bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="343e2-119">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
3.  <span data-ttu-id="343e2-120">Behandeln Sie die Beispiele wie in der Implementierung der **iwmreadercallback:: onsample** -Methode.</span><span class="sxs-lookup"><span data-stu-id="343e2-120">Handle the samples as you normally would in your implementation of the **IWMReaderCallback::OnSample** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="343e2-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="343e2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="343e2-122">**Lesen von Dateien mit dem asynchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="343e2-122">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="343e2-123">**Lesen von Metadaten bei der Wiedergabe**</span><span class="sxs-lookup"><span data-stu-id="343e2-123">**Reading Metadata at Playback**</span></span>](reading-metadata-at-playback.md)
</dt> <dt>

[<span data-ttu-id="343e2-124">**Arbeiten mit Indizes**</span><span class="sxs-lookup"><span data-stu-id="343e2-124">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




