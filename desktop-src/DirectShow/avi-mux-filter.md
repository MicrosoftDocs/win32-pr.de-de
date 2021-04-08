---
description: AVI MUX-Filter
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: AVI MUX-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3755a4d5f63e824ae08eb736a5999dcac3d7ab32
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860476"
---
# <a name="avi-mux-filter"></a><span data-ttu-id="de53e-103">AVI MUX-Filter</span><span class="sxs-lookup"><span data-stu-id="de53e-103">AVI Mux Filter</span></span>

<span data-ttu-id="de53e-104">Der AVI MUX-Filter akzeptiert mehrere Eingabestreams und interverlässt Sie in das AVI-Format.</span><span class="sxs-lookup"><span data-stu-id="de53e-104">The AVI Mux filter accepts multiple input streams and interleaves them into AVI format.</span></span> <span data-ttu-id="de53e-105">Der Filter verwendet separate Eingabe Pins für jeden Eingabestream und eine Ausgabe-PIN für den AVI-Stream.</span><span class="sxs-lookup"><span data-stu-id="de53e-105">The filter uses separate input pins for each input stream, and one output pin for the AVI stream.</span></span>

<span data-ttu-id="de53e-106">Video Erfassungs-oder Authoring Anwendungen können diesen Filter verwenden, um Dateien im AVI-Format auf dem Datenträger zu speichern.</span><span class="sxs-lookup"><span data-stu-id="de53e-106">Video capture or authoring applications can use this filter to save files to disk in AVI format.</span></span> <span data-ttu-id="de53e-107">Der Filter ist in der Regel mit dem [Datei Schreiber](file-writer-filter.md) Filter verbunden, kann jedoch eine Verbindung mit jedem Filter herstellen, dessen eingabepin die IStream-und [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="de53e-107">The filter is typically connected to the [File Writer](file-writer-filter.md) filter, but it can connect to any filter whose input pin supports the IStream and [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de53e-108">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="de53e-108">Filter Interfaces</span></span></td>
<td><span data-ttu-id="de53e-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>Ibasefilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>iconfigavimux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>iconfiginterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>imediaseeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>ipersistmediapropertybag</strong></a>, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="de53e-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de53e-110">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="de53e-110">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="de53e-111">Jeder Haupttyp, der einem FourCC im alten Stil entspricht, oder MEDIATYPE_AUXLine21Data.</span><span class="sxs-lookup"><span data-stu-id="de53e-111">Any major type that corresponds to an old-style FOURCC, or MEDIATYPE_AUXLine21Data.</span></span> <span data-ttu-id="de53e-112">(Weitere Informationen finden Sie unter <a href="fourccmap.md"><strong>fourccmap-Klasse</strong></a>.)</span><span class="sxs-lookup"><span data-stu-id="de53e-112">(For more information, see <a href="fourccmap.md"><strong>FOURCCMap Class</strong></a>.)</span></span>
<ul>
<li><span data-ttu-id="de53e-113">Wenn der Haupttyp MEDIATYPE_Audio ist, muss das Format FORMAT_WaveFormatEx sein.</span><span class="sxs-lookup"><span data-stu-id="de53e-113">If the major type is MEDIATYPE_Audio, the format must be FORMAT_WaveFormatEx.</span></span></li>
<li><span data-ttu-id="de53e-114">Wenn der Haupttyp MEDIATYPE_Video ist, muss das Format FORMAT_VideoInfo oder FORMAT_DvInfo sein.</span><span class="sxs-lookup"><span data-stu-id="de53e-114">If the major type is MEDIATYPE_Video, the format must be FORMAT_VideoInfo or FORMAT_DvInfo.</span></span></li>
<li><span data-ttu-id="de53e-115">Wenn der Haupttyp MEDIATYPE_Interleaved ist, muss das Format FORMAT_DvInfo sein.</span><span class="sxs-lookup"><span data-stu-id="de53e-115">If the major type is MEDIATYPE_Interleaved, the format must be FORMAT_DvInfo.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de53e-116">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="de53e-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="de53e-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>Iamstreamcontrol</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="de53e-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de53e-118">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="de53e-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="de53e-119">MEDIATYPE_Stream MEDIASUBTYPE_Avi</span><span class="sxs-lookup"><span data-stu-id="de53e-119">MEDIATYPE_Stream, MEDIASUBTYPE_Avi</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de53e-120">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="de53e-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="de53e-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>iqualitycontrol</strong></a></span><span class="sxs-lookup"><span data-stu-id="de53e-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de53e-122">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="de53e-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="de53e-123">CLSID_AviDest</span><span class="sxs-lookup"><span data-stu-id="de53e-123">CLSID_AviDest</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de53e-124">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="de53e-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="de53e-125">CLSID_AviMuxProptyPage CLSID_AviMuxProptyPage1</span><span class="sxs-lookup"><span data-stu-id="de53e-125">CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de53e-126">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="de53e-126">Executable</span></span></td>
<td><span data-ttu-id="de53e-127">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="de53e-127">qcap.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de53e-128"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="de53e-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="de53e-129">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="de53e-129">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de53e-130"><a href="filter-categories.md">Filter Kategorie</a></span><span class="sxs-lookup"><span data-stu-id="de53e-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="de53e-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="de53e-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a><span data-ttu-id="de53e-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de53e-132">Remarks</span></span>

<span data-ttu-id="de53e-133">Die folgenden Hinweise beschreiben verschiedene Aspekte der Funktionalität des AVI MUX-Filters.</span><span class="sxs-lookup"><span data-stu-id="de53e-133">The following remarks describe various aspects of the AVI Mux filter's functionality.</span></span>

<span data-ttu-id="de53e-134">Pins</span><span class="sxs-lookup"><span data-stu-id="de53e-134">Pins</span></span>

<span data-ttu-id="de53e-135">Wenn der AVI MUX-Filter erstellt wird, verfügt er über eine Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="de53e-135">When the AVI Mux filter is created, it has one input pin.</span></span> <span data-ttu-id="de53e-136">Wenn jede Eingabe-PIN verbunden ist, erstellt der Filter eine neue Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="de53e-136">As each input pin is connected, the filter creates a new input pin.</span></span>

<span data-ttu-id="de53e-137">Streameigenschaften</span><span class="sxs-lookup"><span data-stu-id="de53e-137">Stream Properties</span></span>

<span data-ttu-id="de53e-138">Die Eingabe Pins unterstützen die IPropertyBag-Schnittstelle für das Festlegen von Eigenschaften für einzelne Streams.</span><span class="sxs-lookup"><span data-stu-id="de53e-138">The input pins support the IPropertyBag interface for setting properties on individual streams.</span></span> <span data-ttu-id="de53e-139">Derzeit ist die folgende Eigenschaft definiert:</span><span class="sxs-lookup"><span data-stu-id="de53e-139">Currently, the following property is defined:</span></span>



| <span data-ttu-id="de53e-140">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="de53e-140">Property</span></span> | <span data-ttu-id="de53e-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de53e-141">Description</span></span>                                                           |
|----------|-----------------------------------------------------------------------|
| <span data-ttu-id="de53e-142">name</span><span class="sxs-lookup"><span data-stu-id="de53e-142">name</span></span>     | <span data-ttu-id="de53e-143">Der Name des Datenstroms.</span><span class="sxs-lookup"><span data-stu-id="de53e-143">The name of the stream.</span></span> <span data-ttu-id="de53e-144">Diese Eigenschaft wird als Block geschrieben `'strn'` .</span><span class="sxs-lookup"><span data-stu-id="de53e-144">This property is written as a `'strn'` chunk.</span></span> |



 

<span data-ttu-id="de53e-145">Wenn der Filter ausgeführt oder angehalten wird, gibt die IPropertyBag:: Write-Methode den falschen VFW- \_ \_ Status zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="de53e-145">If the filter is running or paused, the IPropertyBag::Write method returns VFW\_E\_WRONG\_STATE.</span></span>

<span data-ttu-id="de53e-146">Frame Raten</span><span class="sxs-lookup"><span data-stu-id="de53e-146">Frame Rates</span></span>

<span data-ttu-id="de53e-147">Wenn der Upstream-Filter keine Framerate im **avgtimeperframe** -Member der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur angibt, verwendet das AVI MUX die Zeitstempel des ersten Video Frames.</span><span class="sxs-lookup"><span data-stu-id="de53e-147">If the upstream filter does not specify a frame rate in the **AvgTimePerFrame** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, the AVI Mux uses the time stamps on the first video frame.</span></span> <span data-ttu-id="de53e-148">Das AVI-Dateiformat unterstützt keine Variablen Rahmenraten.</span><span class="sxs-lookup"><span data-stu-id="de53e-148">The AVI file format does not support variable frame rates.</span></span>

<span data-ttu-id="de53e-149">Verworfene Frames</span><span class="sxs-lookup"><span data-stu-id="de53e-149">Dropped Frames</span></span>

<span data-ttu-id="de53e-150">Der AVI MUX-Filter berechnet gelöschte Frames basierend auf den Medien Zeiten jedes Beispiels, falls verfügbar, oder andernfalls den Zeitstempeln des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="de53e-150">The AVI Mux filter calculates dropped frames based on each sample's media times, if available, or else the sample's time stamps.</span></span> <span data-ttu-id="de53e-151">Er schreibt einen Index Eintrag mit der Länge 0 (null) für jeden gelöschten Frame.</span><span class="sxs-lookup"><span data-stu-id="de53e-151">It writes a zero-length index entry for every dropped frame.</span></span>

<span data-ttu-id="de53e-152">Imediaseeking</span><span class="sxs-lookup"><span data-stu-id="de53e-152">IMediaSeeking</span></span>

<span data-ttu-id="de53e-153">Der AVI MUX-Filter implementiert die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle wie folgt:</span><span class="sxs-lookup"><span data-stu-id="de53e-153">The AVI Mux filter implements the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface as follows:</span></span>

-   <span data-ttu-id="de53e-154">Die [**GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) -Methode gibt den aktuellen Fortschritt des Multiplexing zurück.</span><span class="sxs-lookup"><span data-stu-id="de53e-154">The [**GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method returns the current progress of the multiplexing.</span></span> <span data-ttu-id="de53e-155">Wenn Sie eine Datei (langsamer als die tatsächliche Zeit) transcodieren, ist dieser Wert präziser als der vom Filter Graph-Manager zurückgegebene Wert.</span><span class="sxs-lookup"><span data-stu-id="de53e-155">If you are transcoding a file (slower than real time), this value is more accurate than the value returned by the Filter Graph Manager.</span></span> <span data-ttu-id="de53e-156">Weitere Informationen finden Sie im Abschnitt "Hinweise" auf der Referenzseite zu GetCurrentPosition.</span><span class="sxs-lookup"><span data-stu-id="de53e-156">For more information, see the Remarks section of the GetCurrentPosition reference page.</span></span>
-   <span data-ttu-id="de53e-157">Die [**getduration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) -Methode fragt jeden Upstream-Filter ab und gibt die Dauer des längsten Streams zurück.</span><span class="sxs-lookup"><span data-stu-id="de53e-157">The [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method queries each upstream filter and returns the duration of the longest stream.</span></span> <span data-ttu-id="de53e-158">Wenn bei einem dieser Filter der getduration-Befehl fehlschlägt (oder imediaseeking nicht unterstützt), gibt das AVI MUX einen Fehlercode zurück und füllt den *pduration* -Parameter mit der längsten gefundenen Dauer aus.</span><span class="sxs-lookup"><span data-stu-id="de53e-158">If any of these filters fails the GetDuration call (or does not support IMediaSeeking), the AVI Mux returns a failure code and fills in the *pDuration* parameter with the longest duration found.</span></span> <span data-ttu-id="de53e-159">Der Wert von " *pduration* " in diesem Fall ist jedoch nicht notwendigerweise die Länge des längsten Eingabestreams.</span><span class="sxs-lookup"><span data-stu-id="de53e-159">However, the value of *pDuration* in this case is not necessarily the length of the longest input stream.</span></span>
-   <span data-ttu-id="de53e-160">Der AVI MUX implementiert nicht die Methoden getstopposition, getpositions, getavailable, getrate oder getpreroll. Außerdem implementiert es keine Set- \* Methoden für die Suche.</span><span class="sxs-lookup"><span data-stu-id="de53e-160">The AVI Mux does not implement the GetStopPosition, GetPositions, GetAvailable, GetRate, or GetPreroll methods; nor does it implement any Set\* methods for seeking.</span></span>

<span data-ttu-id="de53e-161">Datei Format Erweiterungen für AVI 2,0</span><span class="sxs-lookup"><span data-stu-id="de53e-161">AVI 2.0 File Format Extensions</span></span>

<span data-ttu-id="de53e-162">DirectShow unterstützt derzeit die folgenden AVI 2,0-Dateiformat Erweiterungen:</span><span class="sxs-lookup"><span data-stu-id="de53e-162">DirectShow currently supports the following AVI 2.0 file format extensions:</span></span>

-   <span data-ttu-id="de53e-163">Erweiterte AVI-Dateigröße (mehr als 1 GB)</span><span class="sxs-lookup"><span data-stu-id="de53e-163">Increased AVI file size (greater than 1 GB)</span></span>
-   <span data-ttu-id="de53e-164">Hierarchische Indizierung</span><span class="sxs-lookup"><span data-stu-id="de53e-164">Hierarchical indexing</span></span>

<span data-ttu-id="de53e-165">Weitere Informationen finden Sie unter Version 1,02 der "OpenDML-Dateiformat Erweiterungen", die vom OpenDML AVI M-JPEG-Dateiformat-Unterausschuss veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="de53e-165">For more information, see version 1.02 of the "OpenDML AVI File Format Extensions" published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de53e-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="de53e-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de53e-167">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="de53e-167">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



