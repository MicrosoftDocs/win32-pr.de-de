---
description: In diesem Thema wird beschrieben, wie Sie ein Segment einer Mediendatei in mfplay abspielen, indem Sie die Start-und Endzeit für die Wiedergabe festlegen.
ms.assetid: cd761a4a-42ad-4994-b1b8-0946d29c3d8b
title: Wiedergeben eines Datei Clips
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744db96c6dc384f2473f6c6d3361b24950a8881d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863291"
---
# <a name="how-to-play-a-file-clip"></a><span data-ttu-id="a1a7f-103">Wiedergeben eines Datei Clips</span><span class="sxs-lookup"><span data-stu-id="a1a7f-103">How to Play a File Clip</span></span>

<span data-ttu-id="a1a7f-104">\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a1a7f-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a1a7f-106">\]</span><span class="sxs-lookup"><span data-stu-id="a1a7f-106">\]</span></span>

<span data-ttu-id="a1a7f-107">In diesem Thema wird beschrieben, wie Sie ein Segment einer Mediendatei in mfplay abspielen, indem Sie die Start-und Endzeit für die Wiedergabe festlegen.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-107">This topic describes how to play a segment of a media file in MFPlay, by setting the start and stop times for playback.</span></span>

<span data-ttu-id="a1a7f-108">**So spielen Sie einen dateiclip wieder**</span><span class="sxs-lookup"><span data-stu-id="a1a7f-108">**To Play a File Clip**</span></span>

1.  <span data-ttu-id="a1a7f-109">Rufen Sie [**imfpmediaplayer:: foratemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) oder [**imfpmediaplayer:: foratemediaitemfromubject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) auf, um ein Medien Element für die Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-109">Call [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) or [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) to create a media item for the file.</span></span>
2.  <span data-ttu-id="a1a7f-110">Optional können Sie die gesamte Dauer der Datei erhalten, wie unter [How to Get the Wiedergabe Duration](how-to-get-the-playback-duration.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-110">Optionally, get the total duration of the file, as described in [How to Get the Playback Duration](how-to-get-the-playback-duration.md).</span></span>
3.  <span data-ttu-id="a1a7f-111">Aufrufen von [**imfpmediaitem:: setstartstopposition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) zum Festlegen der Start-und Endzeiten.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-111">Call [**IMFPMediaItem::SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) to set the start and stop times.</span></span> <span data-ttu-id="a1a7f-112">Die Endzeit darf die Datei Dauer nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-112">The stop time must not exceed the file duration.</span></span>
4.  <span data-ttu-id="a1a7f-113">Aufrufen von [**imfpmediaplayer:: setmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) zum Starten der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-113">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) to start playback.</span></span>

<span data-ttu-id="a1a7f-114">Im folgenden Beispiel wird die blockierende Version von " [**kreatemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-114">The following example uses the blocking version of [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span></span> <span data-ttu-id="a1a7f-115">Wenn die nicht blockierende Version verwendet wird, sollte der Code, der nach dem Erstellen von " **kreatemediaitemfromurl** " angezeigt wird, im Handler für das Ereignis " **\_ \_ \_ mediaitem \_** -Ereignis" des MFP-Ereignis Typs eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-115">If the non-blocking version is used, the code that appears after **CreateMediaItemFromURL** should be placed in the handler for the **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event.</span></span> <span data-ttu-id="a1a7f-116">Weitere Informationen zu Ereignissen in MF Play finden Sie unter [empfangen von Ereignissen vom Player](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="a1a7f-116">For more information about events in MFPlay, see [Receiving Events From the Player](getting-started-with-mfplay.md).</span></span>

<span data-ttu-id="a1a7f-117">Um die Datei Dauer zu erhalten, wird in diesem Beispiel die-Funktion aufgerufen, die `GetPlaybackDuration` im Thema Gewusst [wie: erhalten der Wiedergabedauer](how-to-get-the-playback-duration.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-117">To get the file duration, this example calls the `GetPlaybackDuration` function shown in the topic [How to Get the Playback Duration](how-to-get-the-playback-duration.md).</span></span>


```C++
HRESULT PlayMediaClip(
    IMFPMediaPlayer *pPlayer,
    PCWSTR pszURL,
    LONGLONG    hnsStart,
    LONGLONG    hnsEnd
    )
{
    IMFPMediaItem *pItem = NULL;
    PROPVARIANT varStart, varEnd;

    ULONGLONG hnsDuration = 0;

    HRESULT hr = pPlayer->CreateMediaItemFromURL(pszURL, TRUE, 0, &pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetPlaybackDuration(pItem, &hnsDuration);
    if (FAILED(hr))
    {
        goto done;
    }

    if ((ULONGLONG)hnsEnd > hnsDuration)
    {
        hnsEnd = hnsDuration;
    }

    hr = InitPropVariantFromInt64(hnsStart, &varStart);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitPropVariantFromInt64(hnsEnd, &varEnd);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pItem->SetStartStopPosition(
        &MFP_POSITIONTYPE_100NS,
        &varStart,
        &MFP_POSITIONTYPE_100NS,
        &varEnd
        );
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPlayer->SetMediaItem(pItem);

done:
    SafeRelease(&pItem);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="a1a7f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1a7f-118">Requirements</span></span>

<span data-ttu-id="a1a7f-119">MF Play erfordert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a1a7f-119">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1a7f-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1a7f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1a7f-121">Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="a1a7f-121">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



