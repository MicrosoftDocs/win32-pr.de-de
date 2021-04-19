---
description: Video Codierung mit Temporaler Komprimierung
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Video Codierung mit Temporaler Komprimierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee107d8bf6b1ef6b1700abff105b0bdb79f72f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360181"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a><span data-ttu-id="20b9b-103">Video Codierung mit Temporaler Komprimierung (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="20b9b-103">Video Encoding with Temporal Compression (Microsoft Media Foundation)</span></span>

<span data-ttu-id="20b9b-104">Um möglichst hohe Komprimierungs Verhältnisse zu erzielen, verwenden die Windows Media Video Codecs die *zeitliche Komprimierung*.</span><span class="sxs-lookup"><span data-stu-id="20b9b-104">To achieve the highest compression ratios possible, the Windows Media Video codecs use *temporal compression*.</span></span> <span data-ttu-id="20b9b-105">Mit der temporalen Komprimierung wird die komprimierte Videogröße reduziert, indem die einzelnen Frames nicht als Ganzes Bild codiert werden</span><span class="sxs-lookup"><span data-stu-id="20b9b-105">Temporal compression is a technique of reducing compressed video size by not encoding each frame as a complete image.</span></span> <span data-ttu-id="20b9b-106">Die Frames, die vollständig codiert werden (wie ein statisches Bild), werden als *Keyframes* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="20b9b-106">The frames that are encoded completely (like a static image) are called *key frames*.</span></span> <span data-ttu-id="20b9b-107">Alle anderen Frames im Video werden durch Daten dargestellt, die die Änderung seit dem letzten Frame angeben.</span><span class="sxs-lookup"><span data-stu-id="20b9b-107">All other frames in the video are represented by data specifying the change since the last frame.</span></span> <span data-ttu-id="20b9b-108">Diese Frames werden als *Delta Frames* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="20b9b-108">These frames are called *delta frames*.</span></span>

<span data-ttu-id="20b9b-109">Der Umfang der Komprimierung, die mithilfe der temporalen Komprimierung erreicht werden kann, hängt vom Inhalt ab.</span><span class="sxs-lookup"><span data-stu-id="20b9b-109">The amount of compression that can be achieved using temporal compression depends upon the content.</span></span> <span data-ttu-id="20b9b-110">Wenn das Video ohne großen Bewegungs Aufwand oder anderen Änderungen im Bild statisch ist, können für jeden Keyframe viele Delta Rahmen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="20b9b-110">If the video is static, without a lot of motion or other changes in image, many delta frames can be created for each key frame.</span></span> <span data-ttu-id="20b9b-111">Welche weiteren Delta Rahmen verwendet werden, desto kleiner ist der codierte Videostream.</span><span class="sxs-lookup"><span data-stu-id="20b9b-111">The more delta frames that are used, the smaller the encoded video stream.</span></span> <span data-ttu-id="20b9b-112">Wenn das Video jedoch dynamisch ist, aber viel Bewegung oder Farben hat, ist der Vorteil der Verwendung der temporalen Komprimierung geringer.</span><span class="sxs-lookup"><span data-stu-id="20b9b-112">However, if the video is dynamic, with lots of motion or changing colors, the benefit of using temporal compression is smaller.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20b9b-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20b9b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20b9b-114">Arbeiten mit Videos</span><span class="sxs-lookup"><span data-stu-id="20b9b-114">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



