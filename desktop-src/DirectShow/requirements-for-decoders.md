---
description: Anforderungen für Decoders
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: Anforderungen für Decoders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461120bec88636e4c015c2e319d855571e8ac1b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481451"
---
# <a name="requirements-for-decoders"></a><span data-ttu-id="aeb2a-103">Anforderungen für Decoders</span><span class="sxs-lookup"><span data-stu-id="aeb2a-103">Requirements for Decoders</span></span>

<span data-ttu-id="aeb2a-104">Decoderer, die Beispiele für den VMR bereitstellen, müssen die folgenden Regeln beachten:</span><span class="sxs-lookup"><span data-stu-id="aeb2a-104">Decoders that deliver samples to the VMR must observe the following rules:</span></span>

-   <span data-ttu-id="aeb2a-105">Für jeden Videoframe sollte ein Teil Bild Rahmen an den VMR übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="aeb2a-105">There should be one subpicture frame delivered to the VMR for each video frame.</span></span> <span data-ttu-id="aeb2a-106">Die beiden Frames sollten die gleichen Zeitstempel aufweisen.</span><span class="sxs-lookup"><span data-stu-id="aeb2a-106">The two frames should have the same time stamps.</span></span>
-   <span data-ttu-id="aeb2a-107">Wenn das Teilbild nicht geändert wurde, verwenden Sie das am \_ GBF \_ notasyncpoint-Flag in der [**imemzuzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) -Methode, um zu erzwingen, dass die Zuweisung einen Puffer mit dem letzten Frame zurückgibt, der an die VMR übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="aeb2a-107">If the subpicture has not changed, use the AM\_GBF\_NOTASYNCPOINT flag in the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method to force the allocator to return a buffer containing the last frame delivered to the VMR.</span></span> <span data-ttu-id="aeb2a-108">Legen Sie einfach einen neuen Zeitstempel für das Beispiel fest, und übermitteln Sie ihn erneut an den VMR.</span><span class="sxs-lookup"><span data-stu-id="aeb2a-108">Just put a new time stamp on the sample and deliver it to the VMR again.</span></span> <span data-ttu-id="aeb2a-109">Wenn das Bild des unter Bilds leer ist, sollten Sie es trotzdem übermitteln.</span><span class="sxs-lookup"><span data-stu-id="aeb2a-109">If the subpicture fame is blank, you should still deliver it.</span></span> <span data-ttu-id="aeb2a-110">VMR erkennt den leeren Frame und nicht mit dem Video.</span><span class="sxs-lookup"><span data-stu-id="aeb2a-110">The VMR will detect the empty frame and not blend it with the video.</span></span> <span data-ttu-id="aeb2a-111">Dieser Test wird vom VGA-Chip durchgeführt und wirkt sich nicht auf die Wiedergabe Leistung aus.</span><span class="sxs-lookup"><span data-stu-id="aeb2a-111">This test is performed by the VGA chip and does not affect the playback performance.</span></span>
-   <span data-ttu-id="aeb2a-112">Allen Beispielen, mit Ausnahme von Livestreams, müssen gültige Start-und Endzeit Stempel angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="aeb2a-112">All samples, except for live streams, must have valid start and stop time stamps attached.</span></span> <span data-ttu-id="aeb2a-113">(Die DVD ist kein Livestream.)</span><span class="sxs-lookup"><span data-stu-id="aeb2a-113">(DVD is not a live stream.)</span></span>
-   <span data-ttu-id="aeb2a-114">Die Zeitstempel für das Medien Beispiel müssen zusammenhängend sein.</span><span class="sxs-lookup"><span data-stu-id="aeb2a-114">The media sample time stamps must be contiguous</span></span>
-   <span data-ttu-id="aeb2a-115">Der Decoder muss sich selbst als VMR-fähig für die Verwendung durch Graph-Generatoren identifizieren.</span><span class="sxs-lookup"><span data-stu-id="aeb2a-115">The decoder must identify itself as VMR-capable for use by graph builders.</span></span>
-   <span data-ttu-id="aeb2a-116">Der unterbildstream sollte nun eingebettete Alpha Werte pro Pixel enthalten.</span><span class="sxs-lookup"><span data-stu-id="aeb2a-116">The subpicture stream should now contain embedded per-pixel alpha values.</span></span> <span data-ttu-id="aeb2a-117">Der ARGB4444-Oberflächen Typ ist ideal für unter Bilder.</span><span class="sxs-lookup"><span data-stu-id="aeb2a-117">The ARGB4444 surface type is ideal for subpictures.</span></span>
-   <span data-ttu-id="aeb2a-118">Gehen Sie nicht davon aus, dass der Stride-Wert des Teil Bilds mit der Oberflächen Breite identisch ist.</span><span class="sxs-lookup"><span data-stu-id="aeb2a-118">Do not assume that the stride of the subpicture is the same as the surface width.</span></span> <span data-ttu-id="aeb2a-119">Dies ist bei VMR nicht immer der Fall.</span><span class="sxs-lookup"><span data-stu-id="aeb2a-119">This is not always the case with the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aeb2a-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aeb2a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aeb2a-121">Informationen zur DirectX-Video Beschleunigung</span><span class="sxs-lookup"><span data-stu-id="aeb2a-121">About DirectX Video Acceleration</span></span>](about-directx-video-acceleration.md)
</dt> </dl>

 

 



