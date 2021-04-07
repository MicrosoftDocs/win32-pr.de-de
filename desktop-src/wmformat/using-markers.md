---
title: Verwenden von Markern
description: Verwenden von Markern
ms.assetid: b801c985-4ec7-441e-9f8a-40c69b1299a9
keywords:
- Windows Media-Format-SDK, Marker
- Advanced Systems Format (ASF), Marker
- ASF (Advanced Systems Format), Marker
- Advanced Systems Format (ASF), suchen nach Markern
- ASF (Advanced Systems Format), suchen nach Markern
- Marker, Info
- Marker, hinzufügen
- Marker, entfernen
- Marker, Abrufen
- Marker, suchen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cc585b8c71e3bfbae85953650809ad031d36a2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724115"
---
# <a name="using-markers"></a><span data-ttu-id="09a4c-113">Verwenden von Markern</span><span class="sxs-lookup"><span data-stu-id="09a4c-113">Using Markers</span></span>

<span data-ttu-id="09a4c-114">Ein *Marker* ist ein benannter Punkt innerhalb einer ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="09a4c-114">A *marker* is a named point within an ASF file.</span></span> <span data-ttu-id="09a4c-115">Jeder Marker besteht aus einem Namen und einem zugeordneten Zeitpunkt, gemessen als Offset vom Anfang der Datei.</span><span class="sxs-lookup"><span data-stu-id="09a4c-115">Each marker consists of a name and an associated time, measured as an offset from the start of the file.</span></span> <span data-ttu-id="09a4c-116">Eine Anwendung kann Marker verwenden, um verschiedenen Punkten innerhalb des Inhalts Namen zuzuweisen, diese Namen dem Benutzer anzuzeigen und dann die Markerpositionen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="09a4c-116">An application can use markers to assign names to various points within the content, display those names to the user, and then seek to the marker positions.</span></span> <span data-ttu-id="09a4c-117">Eine Anwendung kann Marker zu einer vorhandenen ASF-Datei hinzufügen oder daraus entfernen.</span><span class="sxs-lookup"><span data-stu-id="09a4c-117">An application can add or remove markers from an existing ASF file.</span></span>

<span data-ttu-id="09a4c-118">Die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle enthält Methoden zum Arbeiten mit Markern.</span><span class="sxs-lookup"><span data-stu-id="09a4c-118">The [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface contains methods for working with markers.</span></span> <span data-ttu-id="09a4c-119">Das Metadateneditor Objekt unterstützt das Hinzufügen und Entfernen von Markern</span><span class="sxs-lookup"><span data-stu-id="09a4c-119">The metadata editor object supports adding and removing markers.</span></span> <span data-ttu-id="09a4c-120">Die Writer-und Reader-Objekte können Marker abrufen, aber keine Marker hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="09a4c-120">The writer and reader objects can retrieve markers but cannot add or remove markers.</span></span>

## <a name="adding-markers"></a><span data-ttu-id="09a4c-121">Marker werden hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="09a4c-121">Adding Markers</span></span>

<span data-ttu-id="09a4c-122">Fragen Sie zum Hinzufügen eines Markers den Metadateneditor nach der **iwmheaderinfo** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="09a4c-122">To add a marker, query the metadata editor for the **IWMHeaderInfo** interface.</span></span> <span data-ttu-id="09a4c-123">Anschließend wird die Methode [**iwmheaderinfo:: AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) aufgerufen, wobei der markerName als breit Zeichen-Zeichenfolge und die Zeit in 100-Nanosecond-Einheiten angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="09a4c-123">Then call the [**IWMHeaderInfo::AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) method, specifying the marker name as a wide-character string and the time in 100-nanosecond units.</span></span> <span data-ttu-id="09a4c-124">Die Zeit darf die Datei Dauer nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="09a4c-124">The time must not exceed the file duration.</span></span> <span data-ttu-id="09a4c-125">Zwei Marker können gleichzeitig vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="09a4c-125">Two markers can have the same time.</span></span>

<span data-ttu-id="09a4c-126">Im folgenden Beispiel werden einer Datei mehrere Marker hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="09a4c-126">The following example adds several markers to a file:</span></span>


```C++
IWMMetadataEditor *pEdit = 0;
IWMHeaderInfo     *pInfo = 0;

// Create the metadata editor object.

WMCreateEditor(&pEdit);
pEdit->Open(L"C:\\example.wmv");
pEdit->QueryInterface(IID_IWMHeaderInfo, (void**)&pInfo);

// Add the markers. Note that we add the last ones first. Do this when possible
// for improved performance when writing the markers to the file.
hr = pInfo->AddMarker(L"End",  520000000);   // 52 sec.
hr = pInfo->AddMarker(L"Segue",  350000000); // 35 sec.
hr = pInfo->AddMarker(L"Intro",  15000000);  // 1.5 sec.

// Commit changes and clean up.

pEdit->Flush();
pEdit->Close(); 
pInfo->Release();
pEdit->Release();

```



## <a name="removing-markers"></a><span data-ttu-id="09a4c-127">Entfernen von Markern</span><span class="sxs-lookup"><span data-stu-id="09a4c-127">Removing Markers</span></span>

<span data-ttu-id="09a4c-128">Um einen Marker zu entfernen, geben Sie [**iwmheaderinfo:: RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker)an, und geben Sie dabei den Index des zu entfernenden Markers an.</span><span class="sxs-lookup"><span data-stu-id="09a4c-128">To remove a marker, call [**IWMHeaderInfo::RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), specifying the index of the marker to remove.</span></span> <span data-ttu-id="09a4c-129">Marker werden automatisch in zunehmender Reihenfolge sortiert, sodass Index 0 immer der erste Marker ist.</span><span class="sxs-lookup"><span data-stu-id="09a4c-129">Markers are automatically sorted in increasing time order, so index 0 is always the first marker.</span></span> <span data-ttu-id="09a4c-130">Beachten Sie, dass durch den Aufruf von **RemoveMarker** die Indexnummern aller folgenden Marker geändert werden.</span><span class="sxs-lookup"><span data-stu-id="09a4c-130">Note that calling **RemoveMarker** changes the index numbers of any markers that follow.</span></span> <span data-ttu-id="09a4c-131">Der folgende Code, in dem *pinfo* ein Zeiger auf eine **iwmheaderinfo** -Schnittstelle ist, entfernt alle Marker aus einer Datei:</span><span class="sxs-lookup"><span data-stu-id="09a4c-131">The following code, where *pInfo* is a pointer to an **IWMHeaderInfo** interface, removes all the markers from a file:</span></span>


```C++
WORD count = 0;
pInfo->GetMarkerCount(&count);
while (count--)
{
    pInfo->RemoveMarker(0);
}

```



## <a name="retrieving-markers"></a><span data-ttu-id="09a4c-132">Abrufen von Markern</span><span class="sxs-lookup"><span data-stu-id="09a4c-132">Retrieving Markers</span></span>

<span data-ttu-id="09a4c-133">Um den Namen und die Uhrzeit eines Markers abzurufen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="09a4c-133">To retrieve the name and time of a marker, perform the following steps:</span></span>

1.  <span data-ttu-id="09a4c-134">Aufrufen der [**iwmheaderinfo:: getmarkercount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) -Methode, um zu bestimmen, wie viele Marker die Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="09a4c-134">Call the [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) method to determine how many markers the file contains.</span></span>
2.  <span data-ttu-id="09a4c-135">Ruft die Größe der Zeichenfolge ab, die der markerName enthalten muss.</span><span class="sxs-lookup"><span data-stu-id="09a4c-135">Retrieve the size of the string needed to contain the marker name.</span></span> <span data-ttu-id="09a4c-136">Aufrufen Sie hierzu die [**iwmheaderinfo:: getmarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) -Methode.</span><span class="sxs-lookup"><span data-stu-id="09a4c-136">To do so, call the [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) method.</span></span> <span data-ttu-id="09a4c-137">Geben Sie den Index des abzurufenden Markers und **null** für den Zeichen folgen Puffer an (den *pwszmarkername* -Parameter).</span><span class="sxs-lookup"><span data-stu-id="09a4c-137">Specify the index of the marker to retrieve, and **NULL** for the string buffer (the *pwszMarkerName* parameter).</span></span> <span data-ttu-id="09a4c-138">Die-Methode gibt die Länge der Zeichenfolge, einschließlich des abschließenden ' \\ 0 '-Zeichens, im *pcchmarkernamelen* -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="09a4c-138">The method returns the length of the string, including the terminating '\\0' character, in the *pcchMarkerNameLen* parameter.</span></span>
3.  <span data-ttu-id="09a4c-139">Weisen Sie eine Zeichenfolge mit breit Zeichen zu, um den Namen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="09a4c-139">Allocate a wide-character string to receive the name.</span></span>
4.  <span data-ttu-id="09a4c-140">Erneutes Aufrufen von **getmarker** , aber dieses Mal wird die Adresse der Zeichenfolge im *pwszmarkername* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="09a4c-140">Call **GetMarker** again, but this time pass the address of the string in the *pwszMarkerName* parameter.</span></span> <span data-ttu-id="09a4c-141">Die-Methode schreibt den Markernamen in die Zeichenfolge und gibt die *Markerzeit im pcnsmarkertime* -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="09a4c-141">The method writes the marker name into the string, and returns the marker time in the *pcnsMarkerTime* parameter.</span></span>

<span data-ttu-id="09a4c-142">Der folgende Code durchläuft alle Markierungen in der richtigen Reihenfolge und ruft den Namen und die Uhrzeit ab:</span><span class="sxs-lookup"><span data-stu-id="09a4c-142">The following code loops through every marker in order and retrieves the name and time:</span></span>


```C++
WORD cMarkers = 0;
HRESULT hr = pInfo->GetMarkerCount(&cMarkers);

WCHAR *wszName = 0;
WORD  len = 0;
for (WORD iMarker = 0; iMarker < cMarkers; ++iMarker)
{
    QWORD rtTime = 0;
    WORD req_len = 0;
    hr = pInfo->GetMarker(iMarker, 0, &req_len, &rtTime);
    
    // Reallocate if necessary.
    if (len < req_len)
    {
        delete[] wszName;
        wszName = new WCHAR[req_len];
        len = req_len;
    }
    hr = pInfo->GetMarker(iMarker, wszName, &req_len, &rtTime);
    // Display the name...
}
delete[] wszName;

```



## <a name="seeking-to-a-marker"></a><span data-ttu-id="09a4c-143">Suchen nach einem Marker</span><span class="sxs-lookup"><span data-stu-id="09a4c-143">Seeking to a Marker</span></span>

<span data-ttu-id="09a4c-144">Um die Wiedergabe von einem markerspeicherort aus zu starten, müssen Sie die [**IWMReaderAdvanced2:: startatmarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) -Methode des Reader-Objekts aufzurufen und den Index der Markierung angeben.</span><span class="sxs-lookup"><span data-stu-id="09a4c-144">To start playback from a marker location, call the reader object's [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) method, specifying the index of the marker.</span></span> <span data-ttu-id="09a4c-145">Die restlichen Parameter sind identisch mit denen für die [**iwmreader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) -Methode.</span><span class="sxs-lookup"><span data-stu-id="09a4c-145">The remaining parameters are identical to those for the [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) method.</span></span> <span data-ttu-id="09a4c-146">Im folgenden Beispiel wird der Reader nach der [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) -Schnittstelle abgefragt und der erste Marker gesucht.</span><span class="sxs-lookup"><span data-stu-id="09a4c-146">The following example queries the reader for the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface and seeks to the first marker.</span></span>


```C++
IWMReaderAdvanced2 *pReader2 = 0
WORD iMarkerIndex = 0;
hr = pReader->QueryInterface(IID_IWMReaderAdvanced2, (void**)&pReader2);
if (SUCCEEDED(hr))
{
    hr = pPlayer2->StartAtMarker(iMarkerIndex, 0, 1.0, 0);
    pPlayer2->Release();
}

```



## <a name="related-topics"></a><span data-ttu-id="09a4c-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="09a4c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09a4c-148">**Iwmheaderinfo-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="09a4c-148">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="09a4c-149">**IWMReaderAdvanced2:: startatmarker**</span><span class="sxs-lookup"><span data-stu-id="09a4c-149">**IWMReaderAdvanced2::StartAtMarker**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)
</dt> <dt>

[<span data-ttu-id="09a4c-150">**Arbeiten mit Metadaten**</span><span class="sxs-lookup"><span data-stu-id="09a4c-150">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




