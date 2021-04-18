---
description: Streamformat
ms.assetid: 7ed095f2-b541-4b99-8afc-9acba58081cd
title: Streamformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75413c28f0871db0168e27685de49fd35b682224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350821"
---
# <a name="stream-format"></a><span data-ttu-id="8fc94-103">Streamformat</span><span class="sxs-lookup"><span data-stu-id="8fc94-103">Stream Format</span></span>

<span data-ttu-id="8fc94-104">Sowohl der msdv-als auch der UVC-Treiber können zwei DV-Formate ausgeben: überlappende Audiovideo oder nur Video.</span><span class="sxs-lookup"><span data-stu-id="8fc94-104">Both the MSDV and the UVC driver can output two DV formats: interleaved audio-video, or video only.</span></span> <span data-ttu-id="8fc94-105">Interleaved Audiovideo ist das ursprüngliche Format des Geräts.</span><span class="sxs-lookup"><span data-stu-id="8fc94-105">Interleaved audio-video is the original format from the device.</span></span> <span data-ttu-id="8fc94-106">Das nur-Text-Format enthält dieselben Daten, die Beispiele sind jedoch so gekennzeichnet, dass Sie keine Audiodaten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8fc94-106">The video-only format contains the same data, but the samples are marked as having no audio data.</span></span> <span data-ttu-id="8fc94-107">Das nur-Video-Format besteht hauptsächlich aus der Kompatibilität mit Anwendungen, die Video für Windows verwenden.</span><span class="sxs-lookup"><span data-stu-id="8fc94-107">The video-only format exists mainly for compatibility with applications that use Video for Windows.</span></span> <span data-ttu-id="8fc94-108">Weitere Informationen finden Sie unter [Type-1 vs. Type-2 DV AVI files](type-1-vs--type-2-dv-avi-files.md).</span><span class="sxs-lookup"><span data-stu-id="8fc94-108">For more information, see [Type-1 vs. Type-2 DV AVI Files](type-1-vs--type-2-dv-avi-files.md).</span></span>

<span data-ttu-id="8fc94-109">**Msdv-Treiber**</span><span class="sxs-lookup"><span data-stu-id="8fc94-109">**MSDV Driver**</span></span>

<span data-ttu-id="8fc94-110">Der msdv-Treiber verfügt über zwei Ausgabe Pins.</span><span class="sxs-lookup"><span data-stu-id="8fc94-110">The MSDV driver has two output pins.</span></span> <span data-ttu-id="8fc94-111">Mit dem ersten Ausgabepin werden überlappende Daten gesendet, und mit dem zweiten Ausgabepin werden nur Videodaten gesendet.</span><span class="sxs-lookup"><span data-stu-id="8fc94-111">The first output pin sends interleaved data, and the second output pin sends video-only data.</span></span> <span data-ttu-id="8fc94-112">Es kann jeweils nur eine Ausgabe-PIN verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="8fc94-112">Only one output pin can be connected at a time.</span></span> <span data-ttu-id="8fc94-113">Um ein Format auszuwählen, verbinden Sie die entsprechende Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="8fc94-113">To select a format, connect the appropriate output pin.</span></span> <span data-ttu-id="8fc94-114">Sie können die [**iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) -Schnittstelle in der Ausgabe-PIN verwenden, um das Format zu suchen.</span><span class="sxs-lookup"><span data-stu-id="8fc94-114">You can use the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface on the output pin to find the format.</span></span>

<span data-ttu-id="8fc94-115">**UVC-Treiber**</span><span class="sxs-lookup"><span data-stu-id="8fc94-115">**UVC Driver**</span></span>

<span data-ttu-id="8fc94-116">Im Gegensatz zum msdv-Treiber liefert der UVC-Treiber beide Formate von derselben PIN.</span><span class="sxs-lookup"><span data-stu-id="8fc94-116">Unlike the MSDV driver, the UVC driver delivers both formats from the same pin.</span></span> <span data-ttu-id="8fc94-117">Das Standardformat ist nur Video.</span><span class="sxs-lookup"><span data-stu-id="8fc94-117">The default format is video-only.</span></span> <span data-ttu-id="8fc94-118">Um das Format auszuwählen, verwenden Sie die **iamstreamconfig** -Schnittstelle in der Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="8fc94-118">To select the format, use the **IAMStreamConfig** interface on the output pin.</span></span> <span data-ttu-id="8fc94-119">Ruft die **getstreamcaps** -Methode auf, um die Medientypen in der Ausgabe-PIN aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="8fc94-119">Call the **GetStreamCaps** method to enumerate the media types on the output pin.</span></span> <span data-ttu-id="8fc94-120">Wenn der Haupttyp mit dem gewünschten Format übereinstimmt, müssen Sie für jeden Medientyp **SetFormat** aufrufen und diesen Medientyp übergeben.</span><span class="sxs-lookup"><span data-stu-id="8fc94-120">For each media type, if the major type matches the desired format, call **SetFormat** and pass in that media type.</span></span>



| <span data-ttu-id="8fc94-121">Format</span><span class="sxs-lookup"><span data-stu-id="8fc94-121">Format</span></span>                      | <span data-ttu-id="8fc94-122">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="8fc94-122">Major type</span></span>             |
|-----------------------------|------------------------|
| <span data-ttu-id="8fc94-123">Verschachtelte Audiodaten und Videos</span><span class="sxs-lookup"><span data-stu-id="8fc94-123">Interleaved audio and video</span></span> | <span data-ttu-id="8fc94-124">Überlappende \_ mediaType</span><span class="sxs-lookup"><span data-stu-id="8fc94-124">MEDIATYPE\_Interleaved</span></span> |
| <span data-ttu-id="8fc94-125">Nur Video</span><span class="sxs-lookup"><span data-stu-id="8fc94-125">Video only</span></span>                  | <span data-ttu-id="8fc94-126">MediaType- \_ Video</span><span class="sxs-lookup"><span data-stu-id="8fc94-126">MEDIATYPE\_Video</span></span>       |



 

<span data-ttu-id="8fc94-127">Mit der folgenden Funktion wird das Format basierend auf der GUID des Haupt Typs festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8fc94-127">The following function sets the format based on the major type GUID.</span></span>


```C++
HRESULT SetStreamFormat(IAMStreamConfig *pConfig, const GUID& majorType)
{
    if (pConfig == NULL)
    {
        return E_POINTER;
    }

    // Get the number of stream capabilities.
    int count = 0, size = 0;
    HRESULT hr = pConfig->GetNumberOfCapabilities(&count, &size);
    if (FAILED(hr))
    {
        return hr;
    }

    // Allocate memory for the stream capabilities structure.
    BYTE *pCaps = new BYTE[size];
    if (pCaps == NULL)
    {
        return E_OUTOFMEMORY;
    }
    
    // Enumerate the stream capabilities.
    bool bFoundType = false;
    for (int ix = 0; ix < count; ix++)
    {
        AM_MEDIA_TYPE *pmt;
        hr = pConfig->GetStreamCaps(ix, &pmt, pCaps);
        if (FAILED(hr))
        {
            break;
        }
        else if (pmt->majortype == majorType)
        {
            // This is the media type we want.
            bFoundType = true;
            hr = pConfig->SetFormat(pmt);
            DeleteMediaType(pmt);
            break;
        }
        DeleteMediaType(pmt);
    }
    delete [] pCaps;
    if (FAILED(hr))
    {
        return hr;
    }
    return bFoundType ? S_OK : E_FAIL;
}
```



<span data-ttu-id="8fc94-128">Der msdv-Treiber unterstützt auch **iamstreamconfig**, sodass Sie Code schreiben können, der für beide Gerätetypen funktioniert.</span><span class="sxs-lookup"><span data-stu-id="8fc94-128">The MSDV driver also supports **IAMStreamConfig**, so you can write code that works for both device types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fc94-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8fc94-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fc94-130">Steuern eines DV-Camcorder</span><span class="sxs-lookup"><span data-stu-id="8fc94-130">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



