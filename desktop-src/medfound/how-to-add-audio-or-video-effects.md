---
description: In diesem Thema wird beschrieben, wie Sie Audio-/Videoeffekte mit mfplay verwenden.
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: Hinzufügen von Audio-oder Video Effekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d2b02453ce4561ead7fee0d272a07e694e8388
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349795"
---
# <a name="how-to-add-audio-or-video-effects"></a><span data-ttu-id="e96fb-103">Hinzufügen von Audio-oder Video Effekten</span><span class="sxs-lookup"><span data-stu-id="e96fb-103">How to Add Audio or Video Effects</span></span>

<span data-ttu-id="e96fb-104">\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="e96fb-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e96fb-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e96fb-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e96fb-106">\]</span><span class="sxs-lookup"><span data-stu-id="e96fb-106">\]</span></span>

<span data-ttu-id="e96fb-107">In diesem Thema wird beschrieben, wie Sie Audio-/Videoeffekte mit mfplay verwenden.</span><span class="sxs-lookup"><span data-stu-id="e96fb-107">This topic describes how to use audio/video effects with MFPlay.</span></span>

<span data-ttu-id="e96fb-108">Um einen Effekt mit mfplay zu verwenden, muss der Effekt als Media Foundation Transformation (MFT) implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="e96fb-108">To use an effect with MFPlay, the effect must be implemented as a Media Foundation transform (MFT).</span></span> <span data-ttu-id="e96fb-109">Weitere Informationen finden Sie unter [Media Foundation Transformationen](media-foundation-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="e96fb-109">For more information, see [Media Foundation Transforms](media-foundation-transforms.md).</span></span>

<span data-ttu-id="e96fb-110">**So fügen Sie einen Audio-oder Video Effekt hinzu**</span><span class="sxs-lookup"><span data-stu-id="e96fb-110">**To Add an Audio or Video Effect**</span></span>

1.  <span data-ttu-id="e96fb-111">Erstellen Sie eine Instanz des MFT, die den Effekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="e96fb-111">Create an instance of the MFT that implements the effect.</span></span>
2.  <span data-ttu-id="e96fb-112">[**Imfpmediaplayer:: inserteffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e96fb-112">Call [**IMFPMediaPlayer::InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).</span></span>

<span data-ttu-id="e96fb-113">Geben Sie [**inserteffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) ein, bevor Sie die Mediendatei für die Wiedergabe öffnen.</span><span class="sxs-lookup"><span data-stu-id="e96fb-113">Call [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) before you open the media file for playback.</span></span> <span data-ttu-id="e96fb-114">MF Play bestimmt automatisch, ob der Effekt ein Videoeffekt oder ein Audioeffekt ist.</span><span class="sxs-lookup"><span data-stu-id="e96fb-114">MFPlay automatically determines whether the effect is a video effect or audio effect.</span></span>

<span data-ttu-id="e96fb-115">Die [**inserteffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) -Methode nimmt auch einen booleschen Parameter an, der angibt, ob der Effekt optional oder erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e96fb-115">The [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) method also takes a Boolean parameter that specifies whether the effect is optional or required.</span></span> <span data-ttu-id="e96fb-116">Wenn MF Play keinen erforderlichen Effekt hinzufügen kann (z. b. weil das Streamformat nicht kompatibel ist), tritt ein Wiedergabe Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e96fb-116">If MFPlay cannot add a required effect (for example, because the stream format is incompatible), a playback error occurs.</span></span> <span data-ttu-id="e96fb-117">In den meisten Fällen ist es besser, einen Effekt als optional festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e96fb-117">In most cases, it is better to set an effect as optional.</span></span>

<span data-ttu-id="e96fb-118">Mfplay verwendet weiterhin den Effekt für alle nachfolgenden Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="e96fb-118">MFPlay continues to use the effect for all subsequent playback.</span></span> <span data-ttu-id="e96fb-119">Um den Effekt zu entfernen, wenden Sie [**imfpmediaplayer:: removeeffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) oder [**imfpmediaplayer:: removealleffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects)an.</span><span class="sxs-lookup"><span data-stu-id="e96fb-119">To remove the effect, call [**IMFPMediaPlayer::RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) or [**IMFPMediaPlayer::RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).</span></span>


```C++
HRESULT AddPlaybackEffect(REFGUID clsid, IMFPMediaPlayer *pPlayer)
{
    IMFTransform *pMFT = NULL;

    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pMFT));

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->InsertEffect(pMFT, TRUE); // Set as optional.
    }

    SafeRelease(&pMFT);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="e96fb-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e96fb-120">Requirements</span></span>

<span data-ttu-id="e96fb-121">MF Play erfordert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e96fb-121">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e96fb-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e96fb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e96fb-123">Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="e96fb-123">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



