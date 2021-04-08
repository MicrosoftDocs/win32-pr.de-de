---
title: Rendern von Inhalten
description: Rendern von Inhalten
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- Windows Media-Format-SDK, Rendern von Inhalten
- Advanced Systems Format (ASF), Rendern von Inhalten
- ASF (Advanced Systems Format), Rendern von Inhalten
- Advanced Systems Format (ASF), Inhalts Rendering
- ASF (Advanced Systems Format), Inhalts Rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a171ce9b404c4cc16862ffd64b53ada5821b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856848"
---
# <a name="rendering-content"></a><span data-ttu-id="d1e9e-108">Rendern von Inhalten</span><span class="sxs-lookup"><span data-stu-id="d1e9e-108">Rendering Content</span></span>

<span data-ttu-id="d1e9e-109">Das Windows Media-Format-SDK stellt keine Routinen zum Rendern von Inhalten bereit, die vom Reader-Objekt bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d1e9e-109">The Windows Media Format SDK does not provide any routines for rendering content delivered by the reader object.</span></span> <span data-ttu-id="d1e9e-110">Wenn Sie Anwendungen schreiben, um die Inhalte in ASF-Dateien wiederzugeben, müssen Sie Ihre eigenen renderingroutinen implementieren.</span><span class="sxs-lookup"><span data-stu-id="d1e9e-110">If you write applications to play back the content in ASF files, you must implement your own rendering routines.</span></span>

<span data-ttu-id="d1e9e-111">Beim Rendern von Inhalten müssen Sie vorsichtig sein, um sicherzustellen, dass Beispiele in der Reihenfolge der Präsentationszeit gerendert werden und dass beim Rendern Beispiele aus unterschiedlichen Streams synchronisiert werden</span><span class="sxs-lookup"><span data-stu-id="d1e9e-111">You must be careful when rendering content to ensure that samples are rendered in order of presentation time and that samples from different streams are synchronized when rendering.</span></span> <span data-ttu-id="d1e9e-112">Die Methode, die Sie verwenden, um die streamsynchronisierung sicherzustellen, hängt von der für Ihre Anwendung verwendeten renderingtechnik ab.</span><span class="sxs-lookup"><span data-stu-id="d1e9e-112">The method you employ to ensure stream synchronization will depend upon the rendering technique you use for your application.</span></span> <span data-ttu-id="d1e9e-113">Im Allgemeinen sollten Sie, wenn Sie über Audiodaten und Videostreams verfügen, eine Synchronisierung mit dem Audiostream durchzuführen, da die Inkonsistenz im Audiostream merkbarer ist als einige wenige gelöschte Frames in einem Videostream.</span><span class="sxs-lookup"><span data-stu-id="d1e9e-113">In general, if you have audio and video streams, you should synchronize to the audio stream, because inconsistency in the audio stream is more noticeable than a few dropped frames in a video stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1e9e-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d1e9e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1e9e-115">**Lesen von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="d1e9e-115">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="d1e9e-116">**So rufen Sie Medien Beispiele mit dem asynchronen Reader ab**</span><span class="sxs-lookup"><span data-stu-id="d1e9e-116">**To Retrieve Media Samples with the Asynchronous Reader**</span></span>](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="d1e9e-117">**So rufen Sie Medien Beispiele mit dem synchronen Reader ab**</span><span class="sxs-lookup"><span data-stu-id="d1e9e-117">**To Retrieve Media Samples with the Synchronous Reader**</span></span>](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




