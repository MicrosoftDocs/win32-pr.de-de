---
description: In diesem Thema wird beschrieben, wie eine Sequenz von Audiodateien/Videodateien mit mfplay wiedergegeben wird.
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: Wiedergabe einer Sequenz von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dc4d1523be4cc6cc09416096af260c9eae736c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348331"
---
# <a name="how-to-play-a-sequence-of-files"></a><span data-ttu-id="b5bd5-103">Wiedergabe einer Sequenz von Dateien</span><span class="sxs-lookup"><span data-stu-id="b5bd5-103">How to Play a Sequence of Files</span></span>

<span data-ttu-id="b5bd5-104">\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b5bd5-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b5bd5-106">\]</span><span class="sxs-lookup"><span data-stu-id="b5bd5-106">\]</span></span>

<span data-ttu-id="b5bd5-107">In diesem Thema wird beschrieben, wie eine Sequenz von Audiodateien/Videodateien mit mfplay wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-107">This topic describes how to play a sequence of audio/video files using MFPlay.</span></span>


<span data-ttu-id="b5bd5-108">Das Thema " [Getting Started with mfplay](getting-started-with-mfplay.md) " zeigt, wie Sie eine einzelne Mediendatei abspielen können.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-108">The topic [Getting Started with MFPlay](getting-started-with-mfplay.md) shows how to play a single media file.</span></span> <span data-ttu-id="b5bd5-109">Sie können auch mfplay verwenden, um eine Sequenz von Dateien wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-109">You can also use MFPlay to play a sequence of files.</span></span>

### <a name="synchronous-blocking-method"></a><span data-ttu-id="b5bd5-110">Synchrone (blockierende) Methode</span><span class="sxs-lookup"><span data-stu-id="b5bd5-110">Synchronous (Blocking) Method</span></span>

1.  <span data-ttu-id="b5bd5-111">Aufrufen der [**imfpmediaplayer:: foratemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-111">Call the [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method.</span></span> <span data-ttu-id="b5bd5-112">Mit der-Methode wird ein Medien Element erstellt.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-112">The method creates a media item.</span></span>
2.  <span data-ttu-id="b5bd5-113">[**Imfpmediaplayer:: setmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) aufrufen, um das Medien Element für die Wiedergabe in die Warteschlange zu stellen.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-113">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) to queue the media item for playback.</span></span>
3.  <span data-ttu-id="b5bd5-114">[**Imfpmediaplayer aufzurufen::P Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) , um die Wiedergabe zu starten.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-114">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to start playback.</span></span>

<span data-ttu-id="b5bd5-115">Diese Schritte werden im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-115">These steps are shown in the following code.</span></span>


```C++
HRESULT OpenMediaFile(IMFPMediaPlayer *pPlayer, PCWSTR pwszURL)
{
    HRESULT hr = S_OK;
    
    IMFPMediaItem *pItem = NULL;

    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        TRUE,  // Blocking call
        0,     // User data.
        &pItem
        );

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pPlayer->Play();
    }

    if (pItem)
    {
        pItem->Release();
    }
    return hr;
}
```



<span data-ttu-id="b5bd5-116">Die Methode " [**kreatemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) " übernimmt die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="b5bd5-116">The [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method takes the following parameters:</span></span>

-   <span data-ttu-id="b5bd5-117">Der erste Parameter ist die URL der Datei.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-117">The first parameter is the URL of the file.</span></span>
-   <span data-ttu-id="b5bd5-118">Der zweite Parameter gibt an, ob die-Methode blockiert.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-118">The second parameter specifies whether the method blocks.</span></span> <span data-ttu-id="b5bd5-119">Das Angeben des Werts **true**, wie hier gezeigt, bewirkt, dass die-Methode blockiert wird, bis das Medien Element erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-119">Specifying the value **TRUE**, as shown here, causes the method to block until the media item is created.</span></span>
-   <span data-ttu-id="b5bd5-120">Der dritte Parameter ordnet dem Medien Element einen beliebigen **DWORD- \_ ptr** -Wert zu.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-120">The third parameter associates an arbitrary **DWORD\_PTR** value with the media item.</span></span> <span data-ttu-id="b5bd5-121">Sie können diesen Wert später abrufen, indem Sie [**imfpmediaitem:: getuserdata**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-121">You can get this value later by calling [**IMFPMediaItem::GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).</span></span>
-   <span data-ttu-id="b5bd5-122">Der vierte Parameter erhält einen Zeiger auf die [**imfpmediaitem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) -Schnittstelle des Medien Elements.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-122">The fourth parameter receives a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface of the media item.</span></span>

### <a name="asynchronous-non-blocking-method"></a><span data-ttu-id="b5bd5-123">Asynchrone (nicht blockierende) Methode</span><span class="sxs-lookup"><span data-stu-id="b5bd5-123">Asynchronous (Non-Blocking) Method</span></span>

<span data-ttu-id="b5bd5-124">Vermeiden Sie die Blockierungs Option, wenn Sie " [**foratemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) " aus dem UI-Thread aufrufen, da es eine spürbare Zeit für den Abschluss des Vorgangs dauern kann.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-124">Avoid the blocking option if you call [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) from your UI thread, because it can take a noticeable amount of time to complete.</span></span> <span data-ttu-id="b5bd5-125">Die-Methode öffnet in der Regel eine Datei-oder Netzwerkverbindung und liest genügend Daten, um die Dateiheader zu analysieren, die alle eine Weile dauern können.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-125">The method typically opens a file or network connection and reads enough data to parse the file headers, all of which can take time.</span></span> <span data-ttu-id="b5bd5-126">Daher ist es in der Regel besser, den zweiten Parameter auf **false** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-126">Therefore, it is generally better to set the second parameter to **FALSE**.</span></span> <span data-ttu-id="b5bd5-127">Diese Option bewirkt, dass die-Methode asynchron ausführt.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-127">This option causes the method to perform asynchronously.</span></span> <span data-ttu-id="b5bd5-128">Wenn die asynchrone Option verwendet wird, muss der letzte Parameter **null** sein:</span><span class="sxs-lookup"><span data-stu-id="b5bd5-128">When the asynchronous option is used, the last parameter must be **NULL**:</span></span>


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



<span data-ttu-id="b5bd5-129">Wenn das Medien Element erstellt wird, empfängt Ihre Anwendung einen Ereignis **vom Typ "MFP- \_ \_ Ereignistyp \_ mediaitem \_ erstellt** ".</span><span class="sxs-lookup"><span data-stu-id="b5bd5-129">When the media item is created, your application receives an **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event.</span></span> <span data-ttu-id="b5bd5-130">Die Datenstruktur für dieses Ereignis enthält einen Zeiger auf das Medien Element.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-130">The data structure for this event contains a pointer to the media item.</span></span> <span data-ttu-id="b5bd5-131">Übergeben Sie diesen Zeiger an die [**setmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) -Methode, um das Element in die Warteschlange zu stellen.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-131">Pass this pointer to the [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) method to queue the item for playback.</span></span>


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    HRESULT hr = S_OK;
    if (FAILED(pEvent->header.hrEvent))
    {
        // Handle error. (Not shown.)
    }
    else
    {
        hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
    }
}
```



## <a name="requirements"></a><span data-ttu-id="b5bd5-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5bd5-132">Requirements</span></span>

<span data-ttu-id="b5bd5-133">MF Play erfordert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b5bd5-133">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5bd5-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5bd5-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5bd5-135">Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="b5bd5-135">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



