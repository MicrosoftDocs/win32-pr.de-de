---
description: Festlegen des Medientyps "Gruppe"
ms.assetid: 05f0fdcb-74a4-441e-ac3c-d3d2c1dfee80
title: Festlegen des Medientyps "Gruppe"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365bd2171100a9d4bcfc48d70dbeb94d8a6639dd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106373420"
---
# <a name="setting-the-group-media-type"></a><span data-ttu-id="db424-103">Festlegen des Medientyps "Gruppe"</span><span class="sxs-lookup"><span data-stu-id="db424-103">Setting the Group Media Type</span></span>

<span data-ttu-id="db424-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="db424-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="db424-105">Alle Gruppen müssen einen unkomprimierten Medientyp definieren, entweder Audiodaten oder Videos.</span><span class="sxs-lookup"><span data-stu-id="db424-105">All groups must define an uncompressed media type, either audio or video.</span></span> <span data-ttu-id="db424-106">Der unkomprimierte Medientyp ist das Format, das Viewer während der Wiedergabe sehen oder hören.</span><span class="sxs-lookup"><span data-stu-id="db424-106">The uncompressed media type is the format that viewers see or hear during playback.</span></span> <span data-ttu-id="db424-107">In der Regel wird die endgültige Ausgabe in einem komprimierten Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="db424-107">Typically, the final output will be in a compressed format.</span></span> <span data-ttu-id="db424-108">Weitere Informationen finden Sie unter [Rendern eines Projekts](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="db424-108">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="db424-109">Um das unkomprimierte Format festzulegen, erstellen Sie eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, und füllen Sie Sie mit dem entsprechenden Haupttyp, Untertyp und Format Header.</span><span class="sxs-lookup"><span data-stu-id="db424-109">To set the uncompressed format, create an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure and fill it with the appropriate major type, subtype, and format header.</span></span> <span data-ttu-id="db424-110">Weisen Sie für Video eine [**videinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur für den Format Block zu, und legen Sie die Breite, Höhe und Bittiefe fest.</span><span class="sxs-lookup"><span data-stu-id="db424-110">For video, allocate a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure for the format block, and set the width, height, and bit depth.</span></span> <span data-ttu-id="db424-111">Weisen Sie für Audiodaten eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur für den Format Block zu, und legen Sie die Samplingrate, die Bittiefe und die Anzahl der Kanäle fest.</span><span class="sxs-lookup"><span data-stu-id="db424-111">For audio, allocate a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure for the format block, and set the sample rate, bit depth, and number of channels.</span></span> <span data-ttu-id="db424-112">Wenn Sie nur den Haupttyp festlegen, stellt der von dem geeignete Standardwerte für die anderen Werte bereit.</span><span class="sxs-lookup"><span data-stu-id="db424-112">If you set just the major type, DES provides reasonable defaults for the other values.</span></span> <span data-ttu-id="db424-113">In der Praxis sollten Sie die Werte explizit festlegen, um die Ausgabe zu steuern.</span><span class="sxs-lookup"><span data-stu-id="db424-113">In practice, you should set the values explicitly to control the output.</span></span>

<span data-ttu-id="db424-114">Nachdem Sie die Medientyp Struktur initialisiert haben, können Sie die [**iamtimelinegroup:: setmediatype**](iamtimelinegroup-setmediatype.md) -Methode aufrufen, um den Medientyp für die Gruppe festzulegen.</span><span class="sxs-lookup"><span data-stu-id="db424-114">After you initialize the media type structure, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method to set the media type for the group.</span></span>

<span data-ttu-id="db424-115">Im folgenden Beispiel wird ein 16-Bit-RGB-Video mit 320 Pixel breit und 240 Pixel hoch angegeben:</span><span class="sxs-lookup"><span data-stu-id="db424-115">The following example specifies 16-bit RGB video, 320 pixels wide by 240 pixels high:</span></span>


```C++
AM_MEDIA_TYPE mtGroup;  
mtGroup.majortype = MEDIATYPE_Video;
mtGroup.subtype = MEDIASUBTYPE_RGB555;

// Set format headers.
mtGroup.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(VIDEOINFOHEADER));
if (mtGroup.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}

VIDEOINFOHEADER *pVideoHeader = (VIDEOINFOHEADER*)mtGroup.pbFormat;
ZeroMemory(pVideoHeader, sizeof(VIDEOINFOHEADER));
pVideoHeader->bmiHeader.biBitCount = 16;
pVideoHeader->bmiHeader.biWidth = 320;
pVideoHeader->bmiHeader.biHeight = 240;
pVideoHeader->bmiHeader.biPlanes = 1;
pVideoHeader->bmiHeader.biSize = sizeof(BITMAPINFOHEADER);
pVideoHeader->bmiHeader.biSizeImage = DIBSIZE(pVideoHeader->bmiHeader);

// Set the format type and size.
mtGroup.formattype = FORMAT_VideoInfo;
mtGroup.cbFormat = sizeof(VIDEOINFOHEADER);

// Set the sample size.
mtGroup.bFixedSizeSamples = TRUE;
mtGroup.lSampleSize = DIBSIZE(pVideoHeader->bmiHeader);

// Now use this media type for the group.
pGroup->SetMediaType(&mtGroup);

// Clean up.
CoTaskMemFree(mtGroup.pbFormat);
```



<span data-ttu-id="db424-116">Im nächsten Beispiel wird eine Audiogruppe angegeben, indem der Gruppen Medientyp auf einen 16-Bit-Stereo, 44100 Samples pro Sekunde festgelegt wird:</span><span class="sxs-lookup"><span data-stu-id="db424-116">The next example specifies an audio group, by setting the group media type to 16-bit stereo, 44100 samples per second:</span></span>


```C++
AM_MEDIA_TYPE mt;  
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));

mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.formattype = FORMAT_WaveFormatEx;

// Set format block.
mt.pbFormat = (BYTE*)CoTaskMemAlloc(sizeof(WAVEFORMATEX));
if (mt.pbFormat == NULL)
{
    return E_OUTOFMEMORY;
}
mt.cbFormat = sizeof(WAVEFORMATEX);

// Fill in the WAVEFORMATEX structure.
WAVEFORMATEX *wave = (WAVEFORMATEX*) mt.pbFormat;
wave->wFormatTag = WAVE_FORMAT_PCM;
wave->nChannels = 2;  // Stereo
wave->nSamplesPerSec = 44100;
wave->wBitsPerSample = 16;
wave->nBlockAlign = wave->nChannels * wave->wBitsPerSample/8;
wave->nAvgBytesPerSec = wave->nSamplesPerSec * wave->nBlockAlign; 
wave->cbSize = 0;

hr = pGroup->SetMediaType(&mt);
CoTaskMemFree(mt.pbFormat);
```



<span data-ttu-id="db424-117">Sie können auch die [**cmediatype**](cmediatype.md) -Klasse in den [DirectShow-Basisklassen](directshow-base-classes.md) zum Verwalten von Medientypen verwenden.</span><span class="sxs-lookup"><span data-stu-id="db424-117">You can also use the [**CMediaType**](cmediatype.md) class in the [DirectShow Base Classes](directshow-base-classes.md) to manage media types.</span></span> <span data-ttu-id="db424-118">Sie enthält einige nützliche Hilfsmethoden und gibt den Format Block automatisch frei.</span><span class="sxs-lookup"><span data-stu-id="db424-118">It contains some useful helper methods, and automatically releases the format block.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db424-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db424-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db424-120">Informationen zu Medientypen</span><span class="sxs-lookup"><span data-stu-id="db424-120">About Media Types</span></span>](about-media-types.md)
</dt> <dt>

[<span data-ttu-id="db424-121">Erstellen einer Zeitachse</span><span class="sxs-lookup"><span data-stu-id="db424-121">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 
