---
title: Bildstreams
description: Bildstreams
ms.assetid: 17a945aa-463a-4aac-82cc-68b49c720c0a
keywords:
- Windows Media-Format-SDK, bildstreams
- Advanced Systems Format (ASF), bildstreams
- ASF (Advanced Systems Format), bildstreams
- Windows Media-Format-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- bildstreams, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d029715a3c722d05ee335a3a88ae4632cabbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310844"
---
# <a name="image-streams"></a><span data-ttu-id="e3ecd-110">Bildstreams</span><span class="sxs-lookup"><span data-stu-id="e3ecd-110">Image Streams</span></span>

<span data-ttu-id="e3ecd-111">Ein Bildstream ist ein spezieller Typ von Datenstrom, der weiterhin Bilder enthält, die Präsentations Zeiten zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-111">An image stream is a special type of stream that contains still images assigned to presentation times.</span></span> <span data-ttu-id="e3ecd-112">Eine Anwendung kann die Bilder wie gewünscht in einem Bildstream anzeigen, aber die typische Implementierung besteht darin, jedes Bild anzuzeigen, bis das nächste Bild übermittelt wird, wie z. b. eine Folien Anzeige.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-112">An application can display the pictures in an image stream as desired, but the typical implementation is to display each picture until the next picture is delivered, like a slide show.</span></span> <span data-ttu-id="e3ecd-113">In der Regel wird ein Bildstream in einer Datei mit einem Audiostream codiert, um eine einfache Präsentation von Bildern zu schaffen, die mit Musik oder Sprache synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-113">Usually, an image stream is encoded in a file with an audio stream to produce a simple presentation of images synchronized with music or speech.</span></span>

<span data-ttu-id="e3ecd-114">Bildstreams ähneln den Videostreams darin, dass Sie aus nicht komprimierten Beispielen erstellt werden, die im Rahmen des Datei Schreibvorgangs komprimiert werden, aber Sie sind auch beliebige Streams, da Sie dem Inhalt eine Bitrate und ein Puffer Fenster zuweisen müssen, ohne dass die vom Codec zugewiesenen Eigenschaften abhängig sind.</span><span class="sxs-lookup"><span data-stu-id="e3ecd-114">Image streams are like video streams in that they are created from uncompressed samples that are compressed as part of the file writing process, but they are also like arbitrary streams because you must assign a bit rate and buffer window appropriate to the content without relying on codec-assigned properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3ecd-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e3ecd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3ecd-116">**Beliebige Streams**</span><span class="sxs-lookup"><span data-stu-id="e3ecd-116">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="e3ecd-117">**Funktionen der ASF-Datei**</span><span class="sxs-lookup"><span data-stu-id="e3ecd-117">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="e3ecd-118">**Audiodaten und Videostreams**</span><span class="sxs-lookup"><span data-stu-id="e3ecd-118">**Audio and Video Streams**</span></span>](audio-and-video-streams.md)
</dt> <dt>

[<span data-ttu-id="e3ecd-119">**Schreiben von bildstreams**</span><span class="sxs-lookup"><span data-stu-id="e3ecd-119">**Writing Image Streams**</span></span>](writing-image-streams.md)
</dt> </dl>

 

 




