---
description: In diesem Thema wird beschrieben, wie Sie die Wiedergabedauer einer Mediendatei mithilfe von mfplay erhalten.
ms.assetid: b1ea4f21-55d1-47b0-b6d3-8951dce79f7c
title: So erhalten Sie die Wiedergabedauer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21dd98a916109c8fb3d0ad3311643b1ffdc0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357416"
---
# <a name="how-to-get-the-playback-duration"></a><span data-ttu-id="2a002-103">So erhalten Sie die Wiedergabedauer</span><span class="sxs-lookup"><span data-stu-id="2a002-103">How to Get the Playback Duration</span></span>

<span data-ttu-id="2a002-104">\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2a002-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2a002-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="2a002-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2a002-106">\]</span><span class="sxs-lookup"><span data-stu-id="2a002-106">\]</span></span>

<span data-ttu-id="2a002-107">In diesem Thema wird beschrieben, wie Sie die Wiedergabedauer einer Mediendatei mithilfe von mfplay erhalten.</span><span class="sxs-lookup"><span data-stu-id="2a002-107">This topic describes how to get the playback duration of a media file using MFPlay.</span></span>

<span data-ttu-id="2a002-108">**So erhalten Sie die Wiedergabedauer**</span><span class="sxs-lookup"><span data-stu-id="2a002-108">**To Get the Playback Duration**</span></span>

1.  <span data-ttu-id="2a002-109">Rufen Sie [**imfpmediaplayer:: foratemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) oder [**imfpmediaplayer:: foratemediaitemfromubject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) auf, um ein Medien Element für die Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2a002-109">Call [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) or [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) to create a media item for the file.</span></span>
2.  <span data-ttu-id="2a002-110">[**Imfpmediaitem:: getduration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2a002-110">Call [**IMFPMediaItem::GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration).</span></span> <span data-ttu-id="2a002-111">Geben Sie für den ersten Parameter **MFP \_ PositionType \_ 100 ns** an.</span><span class="sxs-lookup"><span data-stu-id="2a002-111">Specify **MFP\_POSITIONTYPE\_100NS** for the first parameter.</span></span> <span data-ttu-id="2a002-112">Die Dauer wird als **PROPVARIANT** zurückgegeben, das einen **großen \_ ganzzahligen** Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="2a002-112">The duration is returned as a **PROPVARIANT** that contains a **LARGE\_INTEGER** value.</span></span> <span data-ttu-id="2a002-113">Die Dauer wird in 100-Nanosecond-Einheiten angegeben.</span><span class="sxs-lookup"><span data-stu-id="2a002-113">The duration is given in 100-nanosecond units.</span></span>

<span data-ttu-id="2a002-114">Das folgende Beispiel zeigt Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="2a002-114">The following example shows step 2:</span></span>


```C++
#include <propvarutil.h>

HRESULT GetPlaybackDuration(IMFPMediaItem *pItem, ULONGLONG *phnsDuration)
{
    PROPVARIANT var;

    HRESULT hr = pItem->GetDuration(MFP_POSITIONTYPE_100NS, &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt64(var, phnsDuration);
        PropVariantClear(&var);
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="2a002-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a002-115">Requirements</span></span>

<span data-ttu-id="2a002-116">MF Play erfordert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2a002-116">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a002-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2a002-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a002-118">Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="2a002-118">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



