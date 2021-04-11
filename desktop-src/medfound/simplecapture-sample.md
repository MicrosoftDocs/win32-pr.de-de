---
description: Zeigt, wie Sie mithilfe der mfplay-API ein Video von einem Video Erfassungsgerät in der Vorschau anzeigen.
ms.assetid: 6e2b1636-9d24-40e6-9ed4-e17d1af6a044
title: Simplecapture-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da6fd255ad4c69254eb6ff64bdb99731e0c5ba9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215006"
---
# <a name="simplecapture-sample"></a><span data-ttu-id="88480-103">Simplecapture-Beispiel</span><span class="sxs-lookup"><span data-stu-id="88480-103">SimpleCapture Sample</span></span>

<span data-ttu-id="88480-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="88480-104">\[Deprecated.</span></span> <span data-ttu-id="88480-105">Die MF Play-API kann aus zukünftigen Versionen von Windows entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="88480-105">The MFPlay API may be removed from future releases of Windows.</span></span> <span data-ttu-id="88480-106">Anwendungen sollten den [Quell Reader](source-reader.md) für die Video Erfassung verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="88480-106">Applications should use the [Source Reader](source-reader.md) for video capture.\]</span></span>

<span data-ttu-id="88480-107">Zeigt, wie Sie mithilfe der mfplay-API ein Video von einem Video Erfassungsgerät in der Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="88480-107">Shows how to preview video from a video capture device, using the MFPlay API.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="88480-108">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="88480-108">APIs Demonstrated</span></span>

<span data-ttu-id="88480-109">In diesem Beispiel werden die folgenden Microsoft Media Foundation Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="88480-109">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="88480-110">**Imfmediasource**</span><span class="sxs-lookup"><span data-stu-id="88480-110">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="88480-111">**Imfpmediaitem**</span><span class="sxs-lookup"><span data-stu-id="88480-111">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="88480-112">**Imfpmediaplayer**</span><span class="sxs-lookup"><span data-stu-id="88480-112">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="88480-113">**Imfpmediaplayercallback**</span><span class="sxs-lookup"><span data-stu-id="88480-113">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)

## <a name="requirements"></a><span data-ttu-id="88480-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88480-114">Requirements</span></span>



| <span data-ttu-id="88480-115">Produkt</span><span class="sxs-lookup"><span data-stu-id="88480-115">Product</span></span>                                                        | <span data-ttu-id="88480-116">Version</span><span class="sxs-lookup"><span data-stu-id="88480-116">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="88480-117">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="88480-117">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="88480-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="88480-118">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="88480-119">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="88480-119">Downloading the Sample</span></span>

<span data-ttu-id="88480-120">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimpleCapture)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="88480-120">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/SimpleCapture).</span></span>

## <a name="related-topics"></a><span data-ttu-id="88480-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="88480-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88480-122">Audio-/Videoaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="88480-122">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="88480-123">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="88480-123">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



