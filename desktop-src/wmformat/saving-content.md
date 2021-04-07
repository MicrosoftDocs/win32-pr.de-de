---
title: Speichern von Inhalt
description: Speichern von Inhalt
ms.assetid: 22f4e580-43a4-48b5-8eb3-90e1346a1093
keywords:
- Windows Media-Format-SDK, Speichern von Inhalten
- Windows Media-Format-SDK, schnelles Cache Streaming
- Advanced Systems Format (ASF), Speichern von Inhalten
- ASF (Advanced Systems Format), Speichern von Inhalten
- Advanced Systems Format (ASF), schnelles Cache Streaming
- ASF (Advanced Systems Format), schnelles Cache Streaming
- Streams, Speichern von Inhalten
- Schnelles Cache Streaming, Speichern von Inhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c215a81accef29f8943ed52ca24264f785d94
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724083"
---
# <a name="saving-content"></a><span data-ttu-id="13a90-111">Speichern von Inhalt</span><span class="sxs-lookup"><span data-stu-id="13a90-111">Saving Content</span></span>

<span data-ttu-id="13a90-112">Mithilfe dieses SDK kann eine Anwendung heruntergeladenen oder gestreamt-Inhalt auf dem lokalen Computer des Benutzers speichern, indem die [**IWMReaderAdvanced2:: savefileas**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) -Methode für das Reader-Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="13a90-112">By using this SDK, an application can save downloaded or streamed content to the user's local computer, by calling the [**IWMReaderAdvanced2::SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) method on the reader object.</span></span> <span data-ttu-id="13a90-113">Für gestreamt-Inhalte muss der Server schnelles Cache Streaming verwenden, das im Abschnitt [Aktivieren von schnellem Cache Streaming vom Client](enabling-fast-cache-streaming-from-the-client.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="13a90-113">For streamed content, the server must be using Fast Cache streaming, which is described in the section [Enabling Fast Cache Streaming from the Client](enabling-fast-cache-streaming-from-the-client.md).</span></span> <span data-ttu-id="13a90-114">Für gestreamt-Inhalte erstellt die **savefileas** -Methode eine ASX-Datei, die auf eine ASF-Datei verweist, die den gespeicherten Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="13a90-114">For streamed content, the **SaveFileAs** method creates an ASX file that points to an ASF file containing the saved content.</span></span> <span data-ttu-id="13a90-115">Wenn das Reader-Objekt eine serverseitige Wiedergabeliste gestreamt, wird jeder Eintrag als separate ASF-Datei gespeichert, und die Datei "ASX" verweist auf jede der ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="13a90-115">If the reader object is streaming a server-side playlist, each entry is saved as a separate ASF file, and the ASX file points to each of the ASF files.</span></span> <span data-ttu-id="13a90-116">Für heruntergeladene Inhalte erstellt die **savefileas** -Methode einfach eine ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="13a90-116">For downloaded content, the **SaveFileAs** method simply creates an ASF file.</span></span>

<span data-ttu-id="13a90-117">Gehen Sie folgendermaßen vor, um Inhalt in einer lokalen Datei zu speichern:</span><span class="sxs-lookup"><span data-stu-id="13a90-117">To save content to a local file, do the following:</span></span>

1.  <span data-ttu-id="13a90-118">Nennen Sie [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) mit der URL.</span><span class="sxs-lookup"><span data-stu-id="13a90-118">Call [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) with the URL.</span></span> <span data-ttu-id="13a90-119">**Open** ist ein asynchroner-Rückruf, und wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13a90-119">**Open** is an asynchronous call, and returns immediately.</span></span> <span data-ttu-id="13a90-120">Warten Sie, bis der Vorgang beendet wurde, wie in so [Erstellen Sie einen Reader und Öffnen einer Datei](to-create-a-reader-and-open-a-file.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="13a90-120">Wait for the operation to complete, as described in [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md).</span></span>
2.  <span data-ttu-id="13a90-121">Fragen Sie das Reader-Objekt für die [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="13a90-121">Query the reader object for the [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) interface.</span></span>
3.  <span data-ttu-id="13a90-122">Überprüfen Sie, ob der Inhalt durch Aufrufen der [**IWMReaderAdvanced4:: cansavefileas**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) -Methode gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="13a90-122">Check whether the content can be saved by calling the [**IWMReaderAdvanced4::CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) method.</span></span> <span data-ttu-id="13a90-123">Wenn die Methode false zurückgibt, kann der Inhalt nicht lokal gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="13a90-123">If the method returns False, the content cannot be saved locally.</span></span> <span data-ttu-id="13a90-124">Fahren Sie andernfalls mit Schritt 4 fort.</span><span class="sxs-lookup"><span data-stu-id="13a90-124">Otherwise, proceed to step 4.</span></span>
4.  <span data-ttu-id="13a90-125">Aufrufen der [**IWMReaderAdvanced4:: isusingfastcache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) -Methode, um zu bestimmen, ob der Server schnelles Cache Streaming verwendet.</span><span class="sxs-lookup"><span data-stu-id="13a90-125">Call the [**IWMReaderAdvanced4::IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) method to determine whether the server is using Fast Cache streaming.</span></span>
5.  <span data-ttu-id="13a90-126">Nennen Sie die Datei " [**IWMReaderAdvanced2:: savefileas**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) " mit einem Dateinamen für die lokale Datei.</span><span class="sxs-lookup"><span data-stu-id="13a90-126">Call the [**IWMReaderAdvanced2::SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) with a file name for the local file.</span></span> <span data-ttu-id="13a90-127">Wenn die **isusingfastcache** -Methode "true" zurückgegeben hat, benennen Sie die Datei mit der Erweiterung ". asx".</span><span class="sxs-lookup"><span data-stu-id="13a90-127">If the **IsUsingFastCache** method returned True, give the file name an .asx extension.</span></span> <span data-ttu-id="13a90-128">Andernfalls sollten Sie dem Dateinamen die Erweiterung. ASF,. WMA oder. wmv übergeben.</span><span class="sxs-lookup"><span data-stu-id="13a90-128">Otherwise, give the file name an .asf, .wma, or .wmv extension.</span></span>

<span data-ttu-id="13a90-129">Die Anwendung kann den Speichervorgang abbrechen, während Sie ausgeführt wird, indem die [**IWMReaderAdvanced4:: cancelsavefileas**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="13a90-129">The application can cancel the save operation while it is in progress, by calling the [**IWMReaderAdvanced4::CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) method.</span></span>

<span data-ttu-id="13a90-130">Der gespeicherte Inhalt ist möglicherweise mit DRM geschützt, sodass es möglicherweise nicht möglich ist, die Datei auf einem anderen Computer wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="13a90-130">The saved content might be protected with DRM, so it may not be possible to play the file on another computer.</span></span> <span data-ttu-id="13a90-131">Weitere Informationen zum Schutz von Inhalten finden Sie unter [Funktionen für digitale Rights Management](digital-rights-management-features.md).</span><span class="sxs-lookup"><span data-stu-id="13a90-131">For more information on content protection, see [Digital Rights Management Features](digital-rights-management-features.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="13a90-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="13a90-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13a90-133">**Iwmreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="13a90-133">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="13a90-134">**IWMReaderAdvanced2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="13a90-134">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




