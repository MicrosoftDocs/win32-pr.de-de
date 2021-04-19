---
description: In diesem Thema wird beschrieben, wie Sie mfplay verwenden, um ein Video von einer Videokamera aus anzuzeigen.
ms.assetid: ecf6113f-1d8e-4680-87ab-bfd45a9663e4
title: Video Vorschau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d458568a18f598e5aa4ee7e8fb21059e503362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359932"
---
# <a name="video-preview"></a><span data-ttu-id="64139-103">Video Vorschau</span><span class="sxs-lookup"><span data-stu-id="64139-103">Video Preview</span></span>

<span data-ttu-id="64139-104">\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="64139-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="64139-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="64139-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="64139-106">\]</span><span class="sxs-lookup"><span data-stu-id="64139-106">\]</span></span>

<span data-ttu-id="64139-107">In diesem Thema wird beschrieben, wie Sie mfplay verwenden, um ein Video von einer Videokamera aus anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="64139-107">This topic describes how to use MFPlay to preview video from a video camera.</span></span>

<span data-ttu-id="64139-108">Mfplay bietet die einfachste Möglichkeit, das Video von einem Erfassungsgerät aus Microsoft Media Foundation in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="64139-108">MFPlay provides the simplest way in Microsoft Media Foundation to preview video from a capture device.</span></span> <span data-ttu-id="64139-109">Sie sollten MF Play verwenden, wenn die folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="64139-109">You should use MFPlay if the following conditions are all true:</span></span>

-   <span data-ttu-id="64139-110">Sie müssen das Video nicht in einer Datei erfassen.</span><span class="sxs-lookup"><span data-stu-id="64139-110">You do not need to capture the video to a file.</span></span>
-   <span data-ttu-id="64139-111">Sie benötigen keine fein abgestimmte Kontrolle darüber, wie das Video gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="64139-111">You do not need fine-grained control over how the video is rendered.</span></span> <span data-ttu-id="64139-112">(Sie müssen z. b. die Erstellung des Direct3D-Geräts nicht steuern.)</span><span class="sxs-lookup"><span data-stu-id="64139-112">(For example, you do not need to control the creation of the Direct3D device.)</span></span>
-   <span data-ttu-id="64139-113">Vor dem Rendern müssen die Videodaten nicht von der Kamera verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="64139-113">You do not need to process the video data from the camera prior to rendering.</span></span>

<span data-ttu-id="64139-114">Andernfalls ist der [Quell Leser](source-reader.md) möglicherweise eine bessere Option.</span><span class="sxs-lookup"><span data-stu-id="64139-114">Otherwise, the [Source Reader](source-reader.md) may be a better option.</span></span>

<span data-ttu-id="64139-115">Um mfplay mit einem Video Erfassungsgerät zu verwenden, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="64139-115">To use MFPlay with a video capture device, perform the following steps:</span></span>

1.  <span data-ttu-id="64139-116">Erstellen Sie eine Medienquelle für das Erfassungsgerät.</span><span class="sxs-lookup"><span data-stu-id="64139-116">Create a media source for the capture device.</span></span> <span data-ttu-id="64139-117">Weitere Informationen finden Sie unter Auflisten von [Video Erfassungs Geräten](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="64139-117">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="64139-118">Rufen Sie [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) auf, um eine Instanz des Player-Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="64139-118">Call [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) to create an instance of the player object.</span></span>
3.  <span data-ttu-id="64139-119">Aufrufen der [**imfpmediaplayer:: foratemediaitemfromubject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) -Methode.</span><span class="sxs-lookup"><span data-stu-id="64139-119">Call the [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) method.</span></span> <span data-ttu-id="64139-120">Übergeben Sie einen Zeiger auf die imfmediasource-Schnittstelle der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="64139-120">Pass in a pointer to the IMFMediaSource interface of the media source.</span></span> <span data-ttu-id="64139-121">Die-Methode empfängt einen Zeiger auf die [**imfpmediaitem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="64139-121">The method receives a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface.</span></span>
4.  <span data-ttu-id="64139-122">Aufrufen von [**imfpmediaplayer:: setmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).</span><span class="sxs-lookup"><span data-stu-id="64139-122">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).</span></span>
5.  <span data-ttu-id="64139-123">[**Imfpmediaplayer aufrufen::P Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) , um die Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="64139-123">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to begin previewing.</span></span>

<span data-ttu-id="64139-124">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="64139-124">The following code shows these steps:</span></span>


```C++
    IMFPMediaItem *pItem = NULL;

    if (SUCCEEDED(hr))
    {
        hr = MFPCreateMediaPlayer(
            NULL,       // URL.
            FALSE,      // Do not start playback yet.
            0,          // Option flags.
            NULL,       // Callback interface.
            hwnd,
            &g_pPlayer
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromObject(
            g_pSource,
            TRUE,       // Blocking call.
            0,          // User data.
            &pItem
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->Play();
    }

    SafeRelease(&pItem);
```



<span data-ttu-id="64139-125">In einer typischen Anwendung würden Sie einen Zeiger auf eine Rückruf Schnittstelle in der [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) -Funktion bereitstellen und die Rückruf Schnittstelle verwenden, um Ereignisse vom Player zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="64139-125">In a typical application, you would provide a pointer to a callback interface in the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function, and use the callback interface to get events from the player.</span></span> <span data-ttu-id="64139-126">Der Einfachheit halber überspringt der hier gezeigte Code diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="64139-126">For simplicity, the code shown here skips these steps.</span></span> <span data-ttu-id="64139-127">Weitere Informationen finden Sie unter [Getting Started with MF](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="64139-127">For more information, see [Getting Started with MFPlay](getting-started-with-mfplay.md).</span></span>

### <a name="shutting-down"></a><span data-ttu-id="64139-128">Wird heruntergefahren</span><span class="sxs-lookup"><span data-stu-id="64139-128">Shutting Down</span></span>

<span data-ttu-id="64139-129">Bevor die Anwendung beendet wird, fahren Sie die Medienquelle und das Player-Objekt wie folgt herunter:</span><span class="sxs-lookup"><span data-stu-id="64139-129">Before the application exits, shut down the media source and the player object as follows:</span></span>

1.  <span data-ttu-id="64139-130">Nennen Sie [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) für die Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="64139-130">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span>
2.  <span data-ttu-id="64139-131">Nennen Sie [**imfpmediaplayer:: Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) für das Player-Objekt.</span><span class="sxs-lookup"><span data-stu-id="64139-131">Call [**IMFPMediaPlayer::Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) on the player object.</span></span>


```C++
    if (g_pSource)
    {
        g_pSource->Shutdown();
        g_pSource->Release();
        g_pSource = NULL;
    }

    if (g_pPlayer)
    {
        g_pPlayer->Shutdown();
        g_pPlayer->Release();
        g_pPlayer = NULL;
    }
```



## <a name="requirements"></a><span data-ttu-id="64139-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64139-132">Requirements</span></span>

<span data-ttu-id="64139-133">MF Play erfordert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="64139-133">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64139-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64139-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64139-135">MF Play</span><span class="sxs-lookup"><span data-stu-id="64139-135">MFPlay</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="64139-136">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="64139-136">Video Capture</span></span>](audio-video-capture.md)
</dt> </dl>

 

 



