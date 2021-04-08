---
description: Wichtig ist veraltet.
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: MFPlayer2-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1904dcc6e64024dacb76e9109f2e785ec8d5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863431"
---
# <a name="mfplayer2-sample"></a><span data-ttu-id="2f092-103">MFPlayer2-Beispiel</span><span class="sxs-lookup"><span data-stu-id="2f092-103">MFPlayer2 Sample</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f092-104">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="2f092-104">Deprecated.</span></span> <span data-ttu-id="2f092-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="2f092-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="2f092-106">Anwendungen sollten die [Medien Sitzung](media-session.md) für die Wiedergabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f092-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="2f092-107">Veranschaulicht einige der Wiedergabe Features, die im [simpleplay](simpleplay-sample.md) -Beispiel ausgelassen werden, wie z. b.:</span><span class="sxs-lookup"><span data-stu-id="2f092-107">Demonstrates some of the playback features that are omitted from the [SimplePlay](simpleplay-sample.md) sample, such as:</span></span>

-   <span data-ttu-id="2f092-108">Diejenigen</span><span class="sxs-lookup"><span data-stu-id="2f092-108">Seeking</span></span>
-   <span data-ttu-id="2f092-109">Raten Kontrolle (schnelles vorwärts und Zurückspulen)</span><span class="sxs-lookup"><span data-stu-id="2f092-109">Rate control (fast forward and rewind)</span></span>
-   <span data-ttu-id="2f092-110">Audiovolume und stumm Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="2f092-110">Audio volume and mute controls</span></span>
-   <span data-ttu-id="2f092-111">Video Zoom</span><span class="sxs-lookup"><span data-stu-id="2f092-111">Video zoom</span></span>

<span data-ttu-id="2f092-112">Die folgende Abbildung zeigt die Steuerelemente, die für diese Funktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f092-112">The following image shows the controls used for these features.</span></span>

![<span data-ttu-id="2f092-113">Screenshot des MF Player-Beispiels</span><span class="sxs-lookup"><span data-stu-id="2f092-113">screen shot of the mfplayer sample</span></span> ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="2f092-114">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="2f092-114">APIs Demonstrated</span></span>

<span data-ttu-id="2f092-115">In diesem Beispiel werden die folgenden APIs veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2f092-115">This sample demonstrates the following APIs.</span></span>

-   [<span data-ttu-id="2f092-116">**Iaudiosessioncontrol**</span><span class="sxs-lookup"><span data-stu-id="2f092-116">**IAudioSessionControl**</span></span>](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [<span data-ttu-id="2f092-117">**Iaudiosessionmanager**</span><span class="sxs-lookup"><span data-stu-id="2f092-117">**IAudioSessionManager**</span></span>](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [<span data-ttu-id="2f092-118">**Imfpmediaitem**</span><span class="sxs-lookup"><span data-stu-id="2f092-118">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="2f092-119">**Imfpmediaplayer**</span><span class="sxs-lookup"><span data-stu-id="2f092-119">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="2f092-120">**Imfpmediaplayercallback**</span><span class="sxs-lookup"><span data-stu-id="2f092-120">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [<span data-ttu-id="2f092-121">**Immdevice**</span><span class="sxs-lookup"><span data-stu-id="2f092-121">**IMMDevice**</span></span>](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [<span data-ttu-id="2f092-122">**Immdeviceenumerator**</span><span class="sxs-lookup"><span data-stu-id="2f092-122">**IMMDeviceEnumerator**</span></span>](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [<span data-ttu-id="2f092-123">**Isimpleaudiovolume**</span><span class="sxs-lookup"><span data-stu-id="2f092-123">**ISimpleAudioVolume**</span></span>](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a><span data-ttu-id="2f092-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f092-124">Requirements</span></span>



| <span data-ttu-id="2f092-125">Produkt</span><span class="sxs-lookup"><span data-stu-id="2f092-125">Product</span></span>                                                        | <span data-ttu-id="2f092-126">Version</span><span class="sxs-lookup"><span data-stu-id="2f092-126">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="2f092-127">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="2f092-127">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="2f092-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2f092-128">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="2f092-129">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="2f092-129">Downloading the Sample</span></span>

<span data-ttu-id="2f092-130">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2f092-130">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f092-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2f092-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f092-132">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f092-132">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="2f092-133">Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="2f092-133">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
