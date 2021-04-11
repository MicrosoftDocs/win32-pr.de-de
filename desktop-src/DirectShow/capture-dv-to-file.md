---
description: DV in Datei erfassen
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: DV in Datei erfassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341918"
---
# <a name="capture-dv-to-file"></a><span data-ttu-id="6fbc4-103">DV in Datei erfassen</span><span class="sxs-lookup"><span data-stu-id="6fbc4-103">Capture DV to File</span></span>

<span data-ttu-id="6fbc4-104">In diesem Abschnitt wird beschrieben, wie Sie ein digitales Video (DV) von einer DV-Kamera oder einem VTR-Band erfassen.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-104">This section describes how to capture digital video (DV) from a DV camera or from a VTR tape.</span></span>

1.  <span data-ttu-id="6fbc4-105">Erstellen Sie eine Instanz des [msdv-Treiber](msdv-driver.md) Filters.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-105">Create an instance of the [MSDV Driver](msdv-driver.md) filter.</span></span> <span data-ttu-id="6fbc4-106">Weitere Informationen finden Sie unter [Auswählen eines Erfassungs Geräts](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="6fbc4-106">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>
2.  <span data-ttu-id="6fbc4-107">Initialisieren Sie den Erfassungs Diagramm-Generator, wie unter [Informationen zum Erfassungs Diagramm](about-the-capture-graph-builder.md)-Generator beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-107">Initialize the Capture Graph Builder, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
3.  <span data-ttu-id="6fbc4-108">Erstellen Sie das Erfassungs Diagramm, abhängig vom Ziel Dateityp:</span><span class="sxs-lookup"><span data-stu-id="6fbc4-108">Build the capture graph, depending on the target file type:</span></span>
    -   [<span data-ttu-id="6fbc4-109">Erfassen einer DV-Datei vom Typ "1"</span><span class="sxs-lookup"><span data-stu-id="6fbc4-109">Capture a Type-1 DV File</span></span>](capture-a-type-1-dv-file.md)
    -   [<span data-ttu-id="6fbc4-110">Erfassung einer Type-2-DV-Datei</span><span class="sxs-lookup"><span data-stu-id="6fbc4-110">Capture a Type-2 DV File</span></span>](capture-a-type-2-dv-file.md)
    -   [<span data-ttu-id="6fbc4-111">DV in nicht komprimiertem RGB erfassen</span><span class="sxs-lookup"><span data-stu-id="6fbc4-111">Capture DV to Uncompressed RGB</span></span>](capture-dv-to-uncompressed-rgb.md)
4.  <span data-ttu-id="6fbc4-112">Führen Sie das Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-112">Run the graph.</span></span>

<span data-ttu-id="6fbc4-113">Die Erfassung von einem VTR-Band funktioniert genauso wie das Aufzeichnen von Livevideos von der Kamera, mit dem Unterschied, dass Sie das Band wie unter [Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)beschrieben abspielen müssen.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-113">Capturing from a VTR tape works just like capturing live video from the camera, except that you must play the tape, as described in [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span> <span data-ttu-id="6fbc4-114">Um den Verlust von Frames zu vermeiden, führen Sie zuerst das Diagramm aus, und geben Sie dann das Band wieder.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-114">To avoid losing any frames, run the graph first, and then play the tape.</span></span> <span data-ttu-id="6fbc4-115">Wenn Sie die Übertragung abgeschlossen haben, beenden Sie das Band zuerst, und beenden Sie dann das Diagramm.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-115">When you are done transmitting, stop the tape first and then stop the graph.</span></span>

> [!Note]  
> <span data-ttu-id="6fbc4-116">Der Camcorder muss sich im VTR-Modus befinden.</span><span class="sxs-lookup"><span data-stu-id="6fbc4-116">The camcorder must be in VTR mode.</span></span> <span data-ttu-id="6fbc4-117">Siehe [Geräte Modus](device-mode.md).</span><span class="sxs-lookup"><span data-stu-id="6fbc4-117">See [Device Mode](device-mode.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6fbc4-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6fbc4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fbc4-119">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6fbc4-119">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="6fbc4-120">Type-1 im Vergleich zu Type-2 DV AVI-Dateien</span><span class="sxs-lookup"><span data-stu-id="6fbc4-120">Type-1 vs. Type-2 DV AVI Files</span></span>](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[<span data-ttu-id="6fbc4-121">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="6fbc4-121">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



