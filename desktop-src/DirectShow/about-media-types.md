---
description: Erfahren Sie mehr über Medientypen in DirectShow. Der Medientyp ist eine universelle und erweiterbare Möglichkeit, digitale Medienformate zu beschreiben.
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Informationen zu Medientypen (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b1489543b33f5eeb2c288add48148b37f31915
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010893"
---
# <a name="about-media-types-directshow"></a><span data-ttu-id="d8c69-104">Informationen zu Medientypen (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="d8c69-104">About Media Types (DirectShow)</span></span>

<span data-ttu-id="d8c69-105">Da DirectShow modular aufgebaut ist, ist es erforderlich, das Format der Daten an jedem Punkt im Filterdiagramm zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d8c69-105">Because DirectShow is modular, it requires a way to describe the format of the data at each point in the filter graph.</span></span> <span data-ttu-id="d8c69-106">Betrachten Sie beispielsweise die AVI-Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="d8c69-106">For example, consider AVI playback.</span></span> <span data-ttu-id="d8c69-107">Daten werden in den Graphen als Stream vonUNK-Blocken übertragen.</span><span class="sxs-lookup"><span data-stu-id="d8c69-107">Data enters the graph as a stream of RIFF chunks.</span></span> <span data-ttu-id="d8c69-108">Diese werden in Video- und Audiostreams analysiert.</span><span class="sxs-lookup"><span data-stu-id="d8c69-108">These are parsed into video and audio streams.</span></span> <span data-ttu-id="d8c69-109">Der Videostream besteht aus Videoframes, die wahrscheinlich komprimiert sind.</span><span class="sxs-lookup"><span data-stu-id="d8c69-109">The video stream consists of video frames, which are probably compressed.</span></span> <span data-ttu-id="d8c69-110">Nach der Decodierung besteht der Videostream aus einer Reihe nicht komprimierter Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="d8c69-110">After decoding, the video stream is a series of uncompressed bitmaps.</span></span> <span data-ttu-id="d8c69-111">Der Audiostream durchläuft einen ähnlichen Prozess.</span><span class="sxs-lookup"><span data-stu-id="d8c69-111">The audio stream goes through a similar process.</span></span>

<span data-ttu-id="d8c69-112">Medientypen: Wie DirectShow Formate darstellt</span><span class="sxs-lookup"><span data-stu-id="d8c69-112">Media Types: How DirectShow Represents Formats</span></span>

<span data-ttu-id="d8c69-113">Der *Medientyp ist* eine universelle und erweiterbare Möglichkeit, digitale Medienformate zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d8c69-113">The *media type* is a universal and extensible way to describe digital media formats.</span></span> <span data-ttu-id="d8c69-114">Wenn zwei Filter eine Verbindung herstellen, stimmen sie einem Medientyp zu.</span><span class="sxs-lookup"><span data-stu-id="d8c69-114">When two filters connect, they agree on a media type.</span></span> <span data-ttu-id="d8c69-115">Der Medientyp gibt an, welche Art von Daten der Upstreamfilter an den Downstreamfilter liefert, und das physische Layout der Daten.</span><span class="sxs-lookup"><span data-stu-id="d8c69-115">The media type identifies what kind of data the upstream filter will deliver to the downstream filter, and the physical layout of the data.</span></span> <span data-ttu-id="d8c69-116">Wenn sich zwei Filter nicht auf einen Medientyp einigen können, wird keine Verbindung hergestellt.</span><span class="sxs-lookup"><span data-stu-id="d8c69-116">If two filters cannot agree on a media type, they will not connect.</span></span>

<span data-ttu-id="d8c69-117">Bei einigen Anwendungen müssen Sie sich keine Gedanken über Medientypen machen.</span><span class="sxs-lookup"><span data-stu-id="d8c69-117">For some applications, you will never have to worry about media types.</span></span> <span data-ttu-id="d8c69-118">Bei der Dateiwiedergabe verarbeitet DirectShow beispielsweise alle Details.</span><span class="sxs-lookup"><span data-stu-id="d8c69-118">In file playback, for example, DirectShow handles all of the details.</span></span> <span data-ttu-id="d8c69-119">Andere Arten von Anwendungen müssen möglicherweise direkt mit Medientypen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d8c69-119">Other kinds of applications may need to work directly with media types.</span></span>

<span data-ttu-id="d8c69-120">Medientypen werden mithilfe der [**AM \_ MEDIA \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) definiert.</span><span class="sxs-lookup"><span data-stu-id="d8c69-120">Media types are defined using the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="d8c69-121">Diese Struktur enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="d8c69-121">This structure contains the following information:</span></span>

-   <span data-ttu-id="d8c69-122">**Haupttyp:** Der Haupttyp ist eine GUID, die die Gesamtkategorie der Daten definiert.</span><span class="sxs-lookup"><span data-stu-id="d8c69-122">**Major type**: The major type is a GUID that defines the overall category of the data.</span></span> <span data-ttu-id="d8c69-123">Zu den Haupttypen zählen Video, Audio, nicht geparster Bytestream, DANN-Daten usw.</span><span class="sxs-lookup"><span data-stu-id="d8c69-123">Major types include video, audio, unparsed byte stream, MIDI data, and so forth.</span></span>
-   <span data-ttu-id="d8c69-124">**Untertyp:** Der Untertyp ist eine weitere GUID, die das Format weiter definiert.</span><span class="sxs-lookup"><span data-stu-id="d8c69-124">**Subtype**: The subtype is another GUID, which further defines the format.</span></span> <span data-ttu-id="d8c69-125">Innerhalb des Haupttyps des Videos gibt es beispielsweise Untertypen für RGB-24, RGB-32, UY RGB usw.</span><span class="sxs-lookup"><span data-stu-id="d8c69-125">For example, within the video major type, there are subtypes for RGB-24, RGB-32, UYVY, and so forth.</span></span> <span data-ttu-id="d8c69-126">In audio gibt es PCM-Audio, MPEG-1-Nutzlast und andere.</span><span class="sxs-lookup"><span data-stu-id="d8c69-126">Within audio, there is PCM audio, MPEG-1 payload, and others.</span></span> <span data-ttu-id="d8c69-127">Der Untertyp stellt mehr Informationen als der Haupttyp zur Verfügung, definiert jedoch nicht alles über das Format.</span><span class="sxs-lookup"><span data-stu-id="d8c69-127">The subtype provides more information than the major type, but it does not define everything about the format.</span></span> <span data-ttu-id="d8c69-128">Videountertypen definieren z. B. weder die Bildgröße noch die Bildfrequenz.</span><span class="sxs-lookup"><span data-stu-id="d8c69-128">For example, video subtypes do not define the image size or the frame rate.</span></span> <span data-ttu-id="d8c69-129">Diese werden durch den Formatblock definiert, der unten beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="d8c69-129">These are defined by the format block, described below.</span></span>
-   <span data-ttu-id="d8c69-130">**Formatblock:** Der Formatblock ist ein Datenblock, der das Format im Detail beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d8c69-130">**Format block**: The format block is a block of data that describes the format in detail.</span></span> <span data-ttu-id="d8c69-131">Der Formatblock wird getrennt von der [**AM \_ MEDIA \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d8c69-131">The format block is allocated separately from the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="d8c69-132">Der **pbFormat-Member** der **AM MEDIA \_ \_ TYPE-Struktur** zeigt auf den Formatblock.</span><span class="sxs-lookup"><span data-stu-id="d8c69-132">The **pbFormat** member of the **AM\_MEDIA\_TYPE** structure points to the format block.</span></span>

    <span data-ttu-id="d8c69-133">Der **pbFormat-Member** ist vom Typ \**void \** _ , da sich das Layout des Formatblocks je nach Medientyp ändert.</span><span class="sxs-lookup"><span data-stu-id="d8c69-133">The **pbFormat** member is typed \**void\** _ because the layout of the format block changes depending on the media type.</span></span> <span data-ttu-id="d8c69-134">PCM-Audio verwendet beispielsweise eine [*_WAVEFORMATEX-Struktur.* \*](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d8c69-134">For example, PCM audio uses a [_ *WAVEFORMATEX*\*](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="d8c69-135">Video verwendet verschiedene Strukturen, einschließlich [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) und [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="d8c69-135">Video uses various structures, including [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span> <span data-ttu-id="d8c69-136">Der **formattype-Member** der [**AM MEDIA \_ \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) ist eine GUID, die angibt, welche Struktur im Formatblock enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d8c69-136">The **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure is a GUID that specifies which structure is contained in the format block.</span></span> <span data-ttu-id="d8c69-137">Jeder Formatstruktur wird eine GUID zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d8c69-137">Each format structure is assigned a GUID.</span></span> <span data-ttu-id="d8c69-138">Der **cbFormat-Member** gibt die Größe des Formatblocks an.</span><span class="sxs-lookup"><span data-stu-id="d8c69-138">The **cbFormat** member specifies the size of the format block.</span></span> <span data-ttu-id="d8c69-139">Überprüfen Sie diese Werte immer, bevor Sie den **pbFormat-Zeiger** deferencieren.</span><span class="sxs-lookup"><span data-stu-id="d8c69-139">Always check these values before dereferencing the **pbFormat** pointer.</span></span>

<span data-ttu-id="d8c69-140">Wenn der Formatblock ausgefüllt ist, enthalten Haupttyp und Untertyp redundante Informationen.</span><span class="sxs-lookup"><span data-stu-id="d8c69-140">If the format block is filled in, then the major type and subtype contain redundant information.</span></span> <span data-ttu-id="d8c69-141">Der Haupttyp und Untertyp bieten jedoch eine bequeme Möglichkeit, Formate ohne einen vollständigen Formatblock zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d8c69-141">The major type and subtype, however, provide a convenient way to identify formats without a complete format block.</span></span> <span data-ttu-id="d8c69-142">Beispielsweise können Sie ein generisches 24-Bit-RGB-Format (MEDIASUBTYPE RGB24) angeben, ohne alle Informationen zu kennen, die für die \_ [**VIDEOINFOHEADER-Struktur**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) erforderlich sind, z. B. Bildgröße und Bildfrequenz.</span><span class="sxs-lookup"><span data-stu-id="d8c69-142">For example, you can specify a generic 24-bit RGB format (MEDIASUBTYPE\_RGB24), without knowing all of the information required by the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, such as image size and frame rate.</span></span>

<span data-ttu-id="d8c69-143">Beispielsweise kann ein Filter den folgenden Code verwenden, um einen Medientyp zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="d8c69-143">For example, a filter might use the following code to check a media type:</span></span>


```C++
HRESULT CheckMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt == NULL) return E_POINTER;

    // Check the major type. We're looking for video.
    if (pmt->majortype != MEDIATYPE_Video)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the subtype. We're looking for 24-bit RGB.
    if (pmt->subtype != MEDIASUBTYPE_RGB24)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the format type and the size of the format block.
    if ((pmt->formattype == FORMAT_VideoInfo) &&
         (pmt->cbFormat >= sizeof(VIDEOINFOHEADER) &&
         (pmt->pbFormat != NULL))
    {
        // Now it's safe to coerce the format block pointer to the
        // correct structure, as defined by the formattype GUID.
        VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    
        // Examine pVIH (not shown). If it looks OK, return S_OK.
        return S_OK;
    }

    return VFW_E_INVALIDMEDIATYPE;
}
```



<span data-ttu-id="d8c69-144">Die [**AM \_ MEDIA \_ TYPE-Struktur**](/windows/win32/api/strmif/ns-strmif-am_media_type) enthält auch einige optionale Felder.</span><span class="sxs-lookup"><span data-stu-id="d8c69-144">The [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure also contains some optional fields.</span></span> <span data-ttu-id="d8c69-145">Diese können verwendet werden, um zusätzliche Informationen zur Verfügung zu stellen, aber Filter sind nicht erforderlich, um sie zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="d8c69-145">These can be used to provide additional information, but filters are not required to use them:</span></span>

-   <span data-ttu-id="d8c69-146">**lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="d8c69-146">**lSampleSize**.</span></span> <span data-ttu-id="d8c69-147">Wenn dieses Feld nicht 0 (null) ist, wird die Größe der einzelnen Stichproben definiert.</span><span class="sxs-lookup"><span data-stu-id="d8c69-147">If this field is non-zero, it defines the size of each sample.</span></span> <span data-ttu-id="d8c69-148">Wenn der Wert 0 (null) ist, bedeutet dies, dass sich die Stichprobengröße von Stichproben in Stichproben ändern kann.</span><span class="sxs-lookup"><span data-stu-id="d8c69-148">If it is zero, it indicates that the sample size may change from sample to sample.</span></span>
-   <span data-ttu-id="d8c69-149">**bFixedSizeSamples**.</span><span class="sxs-lookup"><span data-stu-id="d8c69-149">**bFixedSizeSamples**.</span></span> <span data-ttu-id="d8c69-150">Wenn dieses boolesche Flag **TRUE ist,** bedeutet dies, dass der Wert in **lSampleSize** gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d8c69-150">If this Boolean flag is **TRUE**, it means the value in **lSampleSize** is valid.</span></span> <span data-ttu-id="d8c69-151">Andernfalls sollten Sie **lSampleSize ignorieren.**</span><span class="sxs-lookup"><span data-stu-id="d8c69-151">Otherwise, you should ignore **lSampleSize**.</span></span>
-   <span data-ttu-id="d8c69-152">**bTemporalCompression**.</span><span class="sxs-lookup"><span data-stu-id="d8c69-152">**bTemporalCompression**.</span></span> <span data-ttu-id="d8c69-153">Wenn dieses boolesche Flag **FALSE ist,** bedeutet dies, dass alle Frames Keyframes sind.</span><span class="sxs-lookup"><span data-stu-id="d8c69-153">If this Boolean flag is **FALSE**, it means that all frames are key frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8c69-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8c69-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8c69-155">Das Filterdiagramm und seine Komponenten</span><span class="sxs-lookup"><span data-stu-id="d8c69-155">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
