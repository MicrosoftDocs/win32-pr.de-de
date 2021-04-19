---
description: Zeigt, wie Sie eine Mediendatei mit der mfplay-API abspielen können.
ms.assetid: 1acd6f98-af59-47fd-9a3e-38a668fb6acf
title: Simpleplay-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02fee507ffed7bd91664f67ffb725565f47c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356844"
---
# <a name="simpleplay-sample"></a><span data-ttu-id="cf1a8-103">Simpleplay-Beispiel</span><span class="sxs-lookup"><span data-stu-id="cf1a8-103">SimplePlay Sample</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf1a8-104">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-104">Deprecated.</span></span> <span data-ttu-id="cf1a8-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="cf1a8-106">Anwendungen sollten die [Medien Sitzung](media-session.md) für die Wiedergabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="cf1a8-107">Zeigt, wie Sie eine Mediendatei mit der mfplay-API abspielen können.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-107">Shows how to play a media file using the MFPlay API.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="cf1a8-108">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="cf1a8-108">APIs Demonstrated</span></span>

<span data-ttu-id="cf1a8-109">In diesem Beispiel werden die folgenden Microsoft Media Foundation Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="cf1a8-109">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="cf1a8-110">**Imfpmediaitem**</span><span class="sxs-lookup"><span data-stu-id="cf1a8-110">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="cf1a8-111">**Imfpmediaplayer**</span><span class="sxs-lookup"><span data-stu-id="cf1a8-111">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="cf1a8-112">**Imfpmediaplayercallback**</span><span class="sxs-lookup"><span data-stu-id="cf1a8-112">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)

## <a name="requirements"></a><span data-ttu-id="cf1a8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf1a8-113">Requirements</span></span>



| <span data-ttu-id="cf1a8-114">Produkt</span><span class="sxs-lookup"><span data-stu-id="cf1a8-114">Product</span></span>                                                        | <span data-ttu-id="cf1a8-115">Version</span><span class="sxs-lookup"><span data-stu-id="cf1a8-115">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="cf1a8-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="cf1a8-116">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="cf1a8-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cf1a8-117">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="cf1a8-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="cf1a8-118">Downloading the Sample</span></span>

<span data-ttu-id="cf1a8-119">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimplePlay)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-119">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimplePlay).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf1a8-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cf1a8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf1a8-121">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf1a8-121">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="cf1a8-122">Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="cf1a8-122">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



