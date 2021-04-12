---
description: VMR-System Anforderungen
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: VMR-System Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d54d6d1604c3e514f3ceef379eaba4a8fa1ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216775"
---
# <a name="vmr-system-requirements"></a><span data-ttu-id="9c1b6-103">VMR-System Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c1b6-103">VMR System Requirements</span></span>

<span data-ttu-id="9c1b6-104">VMR verwendet die Grafik Verarbeitungsfunktionen der Anzeigekarte des Computers exklusiv. VMR führt keine Vermischung oder das Rendering von Videos mithilfe des Host Prozessors durch, da dies die Frame Rate und die Qualität des angezeigten Videos erheblich beeinträchtigen würde.</span><span class="sxs-lookup"><span data-stu-id="9c1b6-104">The VMR uses the graphics-processing capabilities of the computer's display card exclusively; the VMR does not perform any blending or rendering of video using the host processor, because to do so would greatly impact the frame rate and quality of the video being displayed.</span></span> <span data-ttu-id="9c1b6-105">Wenn Sie die neuen Features von VMR nutzen, insbesondere die Mischung mehrerer Videostreams und/oder Anwendungs Images, ist die Gesamtleistung stark von den Funktionen der Grafikkarte abhängig, die auf dem Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c1b6-105">When taking advantage of the new features offered by the VMR, particularly blending of multiple video streams and/or application images, the overall performance obtained is highly dependent on the capabilities of the graphics card being used on the computer.</span></span> <span data-ttu-id="9c1b6-106">Grafikkarten, die sich gut mit VMR ausführen lassen, haben folgende Hardwareunterstützung:</span><span class="sxs-lookup"><span data-stu-id="9c1b6-106">Graphics cards that perform well with the VMR have the following hardware support built into them:</span></span>

-   <span data-ttu-id="9c1b6-107">Unterstützung für YUV und "Non-Power von 2" Direct3D Textur Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="9c1b6-107">Support for YUV and "non-power of 2" Direct3D texture surfaces.</span></span>
-   <span data-ttu-id="9c1b6-108">Die Möglichkeit der Stretchblt von YUV zu RGB DirectDraw-Oberflächen.</span><span class="sxs-lookup"><span data-stu-id="9c1b6-108">The ability to StretchBlt from YUV to RGB DirectDraw surfaces.</span></span>
-   <span data-ttu-id="9c1b6-109">Mindestens 16MB Videospeicher, wenn mehrere Videostreams kombiniert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9c1b6-109">At least 16MB of video memory if multiple video streams are to be blended together.</span></span> <span data-ttu-id="9c1b6-110">Die tatsächliche erforderliche Arbeitsspeicher Menge hängt von der Bildgröße der Videostreams und der Auflösung des verwendeten Anzeigemodus ab.</span><span class="sxs-lookup"><span data-stu-id="9c1b6-110">The actual amount of memory required is dependent on the image size of the video streams and resolution of the display mode being used.</span></span>
-   <span data-ttu-id="9c1b6-111">Unterstützung für eine RGB-Überlagerung oder die Möglichkeit, mit einer YUV-über Lagerungs Oberfläche zu mischen.</span><span class="sxs-lookup"><span data-stu-id="9c1b6-111">Support for an RGB overlay or the ability to blend to a YUV overlay surface.</span></span>
-   <span data-ttu-id="9c1b6-112">Hardware beschleunigtes Video (Unterstützung für die DirectX-Videobeschleunigung) Decodierung.</span><span class="sxs-lookup"><span data-stu-id="9c1b6-112">Hardware-accelerated video (support for DirectX Video Acceleration) decoding.</span></span>
-   <span data-ttu-id="9c1b6-113">Hohe Pixel Füll Raten.</span><span class="sxs-lookup"><span data-stu-id="9c1b6-113">High pixel fill rates.</span></span>

> [!Note]  
> <span data-ttu-id="9c1b6-114">Der VMR erfordert, dass der System Monitor für eine Farbtiefe von mindestens 16 Bits festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="9c1b6-114">The VMR requires that the system monitor be set for a color depth of at least 16 bits.</span></span> <span data-ttu-id="9c1b6-115">Der VMR kann nicht in den Zustand "ausführen" versetzt werden, wenn der Monitor für 256 Farben festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9c1b6-115">The VMR cannot be put into a run state if the monitor is set for 256 colors.</span></span> <span data-ttu-id="9c1b6-116">Außerdem können von einigen Videokarten keine Direct3D-Vorgänge durchgeführt werden, wenn die Anzeige auf 24 Bits pro Pixel festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9c1b6-116">Also, some video cards cannot perform Direct3D operations when the display is set to 24 bits per pixel.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9c1b6-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c1b6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c1b6-118">Informationen zum Video Mischungs Rendering</span><span class="sxs-lookup"><span data-stu-id="9c1b6-118">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



