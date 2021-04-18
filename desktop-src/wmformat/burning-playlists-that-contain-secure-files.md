---
title: Brennen von Wiedergabelisten, die sichere Dateien enthalten
description: Brennen von Wiedergabelisten, die sichere Dateien enthalten
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows Media-Format-SDK, Brennen von Wiedergabelisten mit sicheren Dateien
- Windows Media-Format-SDK, Wiedergabelisten mit sicheren Dateien
- Advanced Systems Format (ASF), Brennen von Wiedergabelisten mit sicheren Dateien
- ASF (Advanced Systems Format), Brennen von Wiedergabelisten mit sicheren Dateien
- Advanced Systems Format (ASF), Wiedergabelisten mit sicheren Dateien
- ASF (Advanced Systems Format), Wiedergabelisten mit sicheren Dateien
- Digital Rights Management (DRM), Brennen von Wiedergabelisten mit sicheren Dateien
- DRM (Digital Rights Management), Brennen von Wiedergabelisten mit sicheren Dateien
- Digital Rights Management (DRM), Wiedergabelisten mit sicheren Dateien
- DRM (Digital Rights Management), Wiedergabelisten mit sicheren Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214c1dbd4ee08f90b3e5e8aa6186508af5044f29
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "106337211"
---
# <a name="burning-playlists-that-contain-secure-files"></a><span data-ttu-id="ff3ed-113">Brennen von Wiedergabelisten, die sichere Dateien enthalten</span><span class="sxs-lookup"><span data-stu-id="ff3ed-113">Burning Playlists That Contain Secure Files</span></span>

<span data-ttu-id="ff3ed-114">Lizenzen, die mithilfe der Objekte des Windows Media Rights Manager 10 SDK erstellt wurden, können angeben, dass eine Datei im Rahmen einer Wiedergabeliste auf eine kompakte CD kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-114">Licenses created by using the objects of the Windows Media Rights Manager 10 SDK can specify the right to copy a file to compact disc as part of a playlist.</span></span> <span data-ttu-id="ff3ed-115">Diese Funktion, die als Wiedergabelisten brennen bezeichnet wird, erfordert, dass Sie die Lizenzen aller Dateien in der Wiedergabeliste überprüfen, bevor Sie mit dem Kopieren der Daten beginnen.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-115">This feature, called playlist burning, requires that you verify the licenses of all of the files in the playlist before starting to copy data.</span></span> <span data-ttu-id="ff3ed-116">Das Windows Media-Format-SDK stellt die [**iwmreaderplaylistburn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) -Schnittstelle bereit, um die Dateiüberprüfung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-116">The Windows Media Format SDK provides the [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) interface to perform file verification for you.</span></span>

<span data-ttu-id="ff3ed-117">Führen Sie die folgenden Schritte aus, um die Wiedergabelisten Verbrennung zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="ff3ed-117">To implement playlist burning, perform the following steps:</span></span>

1.  <span data-ttu-id="ff3ed-118">Erstellen Sie eine Instanz des Reader-Objekts oder des synchronen Reader-Objekts.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-118">Create an instance of the reader object, or the synchronous reader object.</span></span> <span data-ttu-id="ff3ed-119">Weitere Informationen finden Sie unter [Lesen von ASF-Dateien](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="ff3ed-119">For more information, see [Reading ASF Files](reading-asf-files.md).</span></span>
2.  <span data-ttu-id="ff3ed-120">Rufen Sie die **QueryInterface** -Methode der Reader-Schnittstelle ([**iwmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) oder [**iwmsynkreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) auf, um einen Zeiger auf die [**iwmreaderplaylistburn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-120">Call the **QueryInterface** method of the reader interface ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) or [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) to obtain a pointer to the [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) interface.</span></span>
3.  <span data-ttu-id="ff3ed-121">Kopieren Sie die Dateinamen aus der Wiedergabeliste in ein Array von Zeichen folgen mit breit Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-121">Copy the file names from the playlist into an array of wide-character strings.</span></span> <span data-ttu-id="ff3ed-122">Die Dateinamen im-Array müssen in derselben Reihenfolge vorliegen, in der Sie in der Wiedergabeliste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-122">The file names in the array must be in the same order as they appear in the playlist.</span></span>
4.  <span data-ttu-id="ff3ed-123">Nennen Sie die [**iwmreaderplaylistburn:: initplaylistburn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) -Methode, und übergeben Sie einen Zeiger auf das in Schritt 3 erstellte Array, um die Lizenz Überprüfung für die Dateien zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-123">Call the [**IWMReaderPlaylistBurn::InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) method, passing in a pointer to the array created in step 3, to initialize the license verification for the files.</span></span>
5.  <span data-ttu-id="ff3ed-124">Wenn die Lizenz Überprüfung abgeschlossen ist, sendet das Reader-Objekt eine WMT-init-Wiedergabelisten- \_ \_ Burn- \_ Meldung an Ihre Implementierung der [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Rückruf Methode.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-124">When the license verification is completed, the reader object sends a WMT\_INIT\_PLAYLIST\_BURN message to your implementation of the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="ff3ed-125">Wenn Ihr Rückruf diese Nachricht empfängt, rufen Sie die [**iwmreaderplaylistburn:: getinitresults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) -Methode auf, um die Ergebnisse der Lizenzprüfung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-125">When your callback receives this message, call the [**IWMReaderPlaylistBurn::GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) method to get the results of the license check.</span></span> <span data-ttu-id="ff3ed-126">Diese Methode verwendet ein Array von **HRESULT** -Variablen, die den Dateinamen im-Array entsprechen, die an **initplaylistburn** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-126">This method takes an array of **HRESULT** variables that correspond to the file names in the array passed to **InitPlaylistBurn**.</span></span> <span data-ttu-id="ff3ed-127">Wenn alle Werte im Ergebnis Array gleich S \_ OK sind, können Sie den Vorgang fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-127">If all of the values in the result array are equal to S\_OK, you can continue.</span></span> <span data-ttu-id="ff3ed-128">Wenn ein Ergebnis ein Fehlercode ist, darf die Wiedergabeliste nicht kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-128">If any result is an error code, the playlist must not be copied.</span></span>
6.  <span data-ttu-id="ff3ed-129">Wenn Sie die gleiche Instanz des Readers verwenden, öffnen Sie jede Datei, und lesen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-129">Using the same instance of the reader, open and read each file.</span></span> <span data-ttu-id="ff3ed-130">Sie müssen die Dateien in der Reihenfolge öffnen, in der die Dateinamen im Dateinamen Array in **initplaylistburn** übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-130">You must open the files in the order in which the file names appeared in the file name array passed to **InitPlaylistBurn**.</span></span>
7.  <span data-ttu-id="ff3ed-131">Wenn Sie alle Dateien in der Wiedergabeliste kopiert haben, nennen Sie die Datei " [**iwmreaderplaylistburn:: endplaylistburn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) ", um den Wiedergabe Prozess der Wiedergabeliste abzuschließen und die vom Reader verwendeten Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-131">When you have copied all of the files in the playlist, call the [**IWMReaderPlaylistBurn::EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) to complete the playlist burn process and free the resources used by the reader.</span></span>

> [!Note]  
> <span data-ttu-id="ff3ed-132">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-132">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ff3ed-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ff3ed-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff3ed-134">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="ff3ed-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




