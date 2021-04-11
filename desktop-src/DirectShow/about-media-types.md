---
description: Informationen zu Medientypen
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Informationen zu Medientypen (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3289a37e95bf5dbd1e5c277b5799a2c7c8c90586
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351229"
---
# <a name="about-media-types-directshow"></a><span data-ttu-id="acd40-103">Informationen zu Medientypen (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="acd40-103">About Media Types (DirectShow)</span></span>

<span data-ttu-id="acd40-104">Da DirectShow modular aufgebaut ist, ist es erforderlich, das Format der Daten an jedem Punkt im Filter Diagramm zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="acd40-104">Because DirectShow is modular, it requires a way to describe the format of the data at each point in the filter graph.</span></span> <span data-ttu-id="acd40-105">Nehmen Sie beispielsweise die AVI-Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="acd40-105">For example, consider AVI playback.</span></span> <span data-ttu-id="acd40-106">Daten werden als Stream von Riff Blöcken in das Diagramm eingegeben.</span><span class="sxs-lookup"><span data-stu-id="acd40-106">Data enters the graph as a stream of RIFF chunks.</span></span> <span data-ttu-id="acd40-107">Diese werden in Video-und Audiodatenströme analysiert.</span><span class="sxs-lookup"><span data-stu-id="acd40-107">These are parsed into video and audio streams.</span></span> <span data-ttu-id="acd40-108">Der Videostream besteht aus Video Frames, die wahrscheinlich komprimiert sind.</span><span class="sxs-lookup"><span data-stu-id="acd40-108">The video stream consists of video frames, which are probably compressed.</span></span> <span data-ttu-id="acd40-109">Nach der Decodierung ist der Videostream eine Reihe von nicht komprimierten Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="acd40-109">After decoding, the video stream is a series of uncompressed bitmaps.</span></span> <span data-ttu-id="acd40-110">Der Audiodatenstrom durchläuft einen ähnlichen Prozess.</span><span class="sxs-lookup"><span data-stu-id="acd40-110">The audio stream goes through a similar process.</span></span>

<span data-ttu-id="acd40-111">Medientypen: Funktionsweise von DirectShow-Formaten</span><span class="sxs-lookup"><span data-stu-id="acd40-111">Media Types: How DirectShow Represents Formats</span></span>

<span data-ttu-id="acd40-112">Der *Medientyp* ist eine universelle und erweiterbare Methode, um digitale Medienformate zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="acd40-112">The *media type* is a universal and extensible way to describe digital media formats.</span></span> <span data-ttu-id="acd40-113">Wenn zwei Filter eine Verbindung herstellen, stimmen Sie einem Medientyp zu.</span><span class="sxs-lookup"><span data-stu-id="acd40-113">When two filters connect, they agree on a media type.</span></span> <span data-ttu-id="acd40-114">Der Medientyp gibt an, welche Art von Daten der Upstream-Filter für den downstreamfilter bereitstellt, und das physische Layout der Daten.</span><span class="sxs-lookup"><span data-stu-id="acd40-114">The media type identifies what kind of data the upstream filter will deliver to the downstream filter, and the physical layout of the data.</span></span> <span data-ttu-id="acd40-115">Wenn zwei Filter einem Medientyp nicht zustimmen können, wird keine Verbindung hergestellt.</span><span class="sxs-lookup"><span data-stu-id="acd40-115">If two filters cannot agree on a media type, they will not connect.</span></span>

<span data-ttu-id="acd40-116">Bei manchen Anwendungen müssen Sie sich keine Gedanken über die Medientypen machen.</span><span class="sxs-lookup"><span data-stu-id="acd40-116">For some applications, you will never have to worry about media types.</span></span> <span data-ttu-id="acd40-117">Bei der Wiedergabe von Dateien verarbeitet DirectShow beispielsweise alle Details.</span><span class="sxs-lookup"><span data-stu-id="acd40-117">In file playback, for example, DirectShow handles all of the details.</span></span> <span data-ttu-id="acd40-118">Andere Arten von Anwendungen müssen möglicherweise direkt mit Medientypen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="acd40-118">Other kinds of applications may need to work directly with media types.</span></span>

<span data-ttu-id="acd40-119">Medientypen werden mithilfe der [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="acd40-119">Media types are defined using the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="acd40-120">Diese Struktur enthält die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="acd40-120">This structure contains the following information:</span></span>

-   <span data-ttu-id="acd40-121">**Haupttyp**: der Haupttyp ist eine GUID, die die Gesamtkategorie der Daten definiert.</span><span class="sxs-lookup"><span data-stu-id="acd40-121">**Major type**: The major type is a GUID that defines the overall category of the data.</span></span> <span data-ttu-id="acd40-122">Zu den Haupttypen zählen Video, Audiodaten, nicht analysierte Bytestream, MIDI-Daten usw.</span><span class="sxs-lookup"><span data-stu-id="acd40-122">Major types include video, audio, unparsed byte stream, MIDI data, and so forth.</span></span>
-   <span data-ttu-id="acd40-123">**Untertyp**: der Untertyp ist eine andere GUID, die das Format weiter definiert.</span><span class="sxs-lookup"><span data-stu-id="acd40-123">**Subtype**: The subtype is another GUID, which further defines the format.</span></span> <span data-ttu-id="acd40-124">Im Video Haupttyp gibt es z. b. Untertypen für RGB-24, RGB-32, UYVY usw.</span><span class="sxs-lookup"><span data-stu-id="acd40-124">For example, within the video major type, there are subtypes for RGB-24, RGB-32, UYVY, and so forth.</span></span> <span data-ttu-id="acd40-125">In Audiodaten gibt es PCM-Audiodaten, MPEG-1-Nutzlast und andere.</span><span class="sxs-lookup"><span data-stu-id="acd40-125">Within audio, there is PCM audio, MPEG-1 payload, and others.</span></span> <span data-ttu-id="acd40-126">Der Untertyp bietet mehr Informationen als der Haupttyp, aber er definiert nicht alles über das Format.</span><span class="sxs-lookup"><span data-stu-id="acd40-126">The subtype provides more information than the major type, but it does not define everything about the format.</span></span> <span data-ttu-id="acd40-127">Beispielsweise definieren Video Untertypen nicht die Bildgröße oder die Framerate.</span><span class="sxs-lookup"><span data-stu-id="acd40-127">For example, video subtypes do not define the image size or the frame rate.</span></span> <span data-ttu-id="acd40-128">Diese werden durch den unten beschriebenen Format Block definiert.</span><span class="sxs-lookup"><span data-stu-id="acd40-128">These are defined by the format block, described below.</span></span>
-   <span data-ttu-id="acd40-129">**Format Block**: der Format Block ist ein Datenblock, der das Format ausführlich beschreibt.</span><span class="sxs-lookup"><span data-stu-id="acd40-129">**Format block**: The format block is a block of data that describes the format in detail.</span></span> <span data-ttu-id="acd40-130">Der Format Block wird getrennt von der [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="acd40-130">The format block is allocated separately from the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="acd40-131">Der **pbformat** -Member der **am \_ \_ Medientyp** -Struktur verweist auf den Format Block.</span><span class="sxs-lookup"><span data-stu-id="acd40-131">The **pbFormat** member of the **AM\_MEDIA\_TYPE** structure points to the format block.</span></span>

    <span data-ttu-id="acd40-132">Der **pbformat** -Member ist typisiert \**void \** _, weil das Layout des Format Blocks abhängig vom Medientyp geändert wird.</span><span class="sxs-lookup"><span data-stu-id="acd40-132">The **pbFormat** member is typed \**void\** _ because the layout of the format block changes depending on the media type.</span></span> <span data-ttu-id="acd40-133">Beispielsweise verwendet PCM-Audiodaten eine [_ *WaveFormatEx* \*](/previous-versions/dd757713(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="acd40-133">For example, PCM audio uses a [_ *WAVEFORMATEX*\*](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="acd40-134">Video verwendet verschiedene Strukturen, einschließlich [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) und [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="acd40-134">Video uses various structures, including [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span> <span data-ttu-id="acd40-135">Der **Format Type** -Member der [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur ist eine GUID, die angibt, welche Struktur im Format Block enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="acd40-135">The **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure is a GUID that specifies which structure is contained in the format block.</span></span> <span data-ttu-id="acd40-136">Jeder Format Struktur wird eine GUID zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="acd40-136">Each format structure is assigned a GUID.</span></span> <span data-ttu-id="acd40-137">Der **cbformat** -Member gibt die Größe des Format Blocks an.</span><span class="sxs-lookup"><span data-stu-id="acd40-137">The **cbFormat** member specifies the size of the format block.</span></span> <span data-ttu-id="acd40-138">Überprüfen Sie diese Werte immer, bevor Sie den **pbformat** -Zeiger dereferenzieren.</span><span class="sxs-lookup"><span data-stu-id="acd40-138">Always check these values before dereferencing the **pbFormat** pointer.</span></span>

<span data-ttu-id="acd40-139">Wenn der Format Block ausgefüllt ist, enthalten der Haupttyp und der Untertyp redundante Informationen.</span><span class="sxs-lookup"><span data-stu-id="acd40-139">If the format block is filled in, then the major type and subtype contain redundant information.</span></span> <span data-ttu-id="acd40-140">Der Haupttyp und der Untertyp stellen jedoch eine bequeme Möglichkeit zum Identifizieren von Formaten ohne einen kompletten Format Block dar.</span><span class="sxs-lookup"><span data-stu-id="acd40-140">The major type and subtype, however, provide a convenient way to identify formats without a complete format block.</span></span> <span data-ttu-id="acd40-141">Sie können z. b. ein generisches 24-Bit-RGB-Format (mediasubtype \_ RGB24) angeben, ohne alle Informationen zu kennen, die für die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur erforderlich sind, wie z. b. die Bildgröße und die Framerate.</span><span class="sxs-lookup"><span data-stu-id="acd40-141">For example, you can specify a generic 24-bit RGB format (MEDIASUBTYPE\_RGB24), without knowing all of the information required by the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, such as image size and frame rate.</span></span>

<span data-ttu-id="acd40-142">Ein Filter kann z. b. den folgenden Code verwenden, um einen Medientyp zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="acd40-142">For example, a filter might use the following code to check a media type:</span></span>


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



<span data-ttu-id="acd40-143">Die [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur enthält auch einige optionale Felder.</span><span class="sxs-lookup"><span data-stu-id="acd40-143">The [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure also contains some optional fields.</span></span> <span data-ttu-id="acd40-144">Diese können verwendet werden, um zusätzliche Informationen bereitzustellen, aber es sind keine Filter erforderlich, um Sie zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="acd40-144">These can be used to provide additional information, but filters are not required to use them:</span></span>

-   <span data-ttu-id="acd40-145">**lsamplesize**.</span><span class="sxs-lookup"><span data-stu-id="acd40-145">**lSampleSize**.</span></span> <span data-ttu-id="acd40-146">Wenn dieses Feld ungleich 0 (null) ist, wird die Größe der einzelnen Stichproben definiert.</span><span class="sxs-lookup"><span data-stu-id="acd40-146">If this field is non-zero, it defines the size of each sample.</span></span> <span data-ttu-id="acd40-147">Wenn Sie 0 (null) ist, gibt Sie an, dass sich die Stichprobengröße von Sample in Sample ändern kann.</span><span class="sxs-lookup"><span data-stu-id="acd40-147">If it is zero, it indicates that the sample size may change from sample to sample.</span></span>
-   <span data-ttu-id="acd40-148">**bfixedsizesamples**.</span><span class="sxs-lookup"><span data-stu-id="acd40-148">**bFixedSizeSamples**.</span></span> <span data-ttu-id="acd40-149">Wenn dieses boolesche Flag " **true**" ist, bedeutet dies, dass der Wert in " **lsamplesize** " gültig ist.</span><span class="sxs-lookup"><span data-stu-id="acd40-149">If this Boolean flag is **TRUE**, it means the value in **lSampleSize** is valid.</span></span> <span data-ttu-id="acd40-150">Andernfalls sollten Sie " **lsamplesize**" ignorieren.</span><span class="sxs-lookup"><span data-stu-id="acd40-150">Otherwise, you should ignore **lSampleSize**.</span></span>
-   <span data-ttu-id="acd40-151">**btemporalcompression**.</span><span class="sxs-lookup"><span data-stu-id="acd40-151">**bTemporalCompression**.</span></span> <span data-ttu-id="acd40-152">Wenn dieses boolesche Flag **false** ist, bedeutet dies, dass es sich bei allen Frames um Keyframes handelt.</span><span class="sxs-lookup"><span data-stu-id="acd40-152">If this Boolean flag is **FALSE**, it means that all frames are key frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acd40-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="acd40-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acd40-154">Das Filter Diagramm und dessen Komponenten</span><span class="sxs-lookup"><span data-stu-id="acd40-154">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
