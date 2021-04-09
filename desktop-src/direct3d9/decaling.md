---
description: Direct3D-Anwendungen verwenden die-Verwendung, um zu steuern, welche Pixel von einem bestimmten primitiven Bild auf die Renderingzieloberfläche gezeichnet werden. Anwendungen wenden die Abbilder von primitiven an, damit Coplanar-Polygone ordnungsgemäß wieder hergestellt werden können.
ms.assetid: 0d57983c-c8f3-4095-9495-a3ec5d280bda
title: Wird abgebrochen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5606bdbc798d8b1e834aff53b04984f659af650
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123877"
---
# <a name="decaling-direct3d-9"></a><span data-ttu-id="91748-104">Wird abgebrochen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="91748-104">Decaling (Direct3D 9)</span></span>

<span data-ttu-id="91748-105">Direct3D-Anwendungen verwenden die-Verwendung, um zu steuern, welche Pixel von einem bestimmten primitiven Bild auf die Renderingzieloberfläche gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="91748-105">Direct3D applications use decaling to control which pixels from a particular primitive image are drawn to the rendering target surface.</span></span> <span data-ttu-id="91748-106">Anwendungen wenden die Abbilder von primitiven an, damit Coplanar-Polygone ordnungsgemäß wieder hergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="91748-106">Applications apply decals to the images of primitives to enable coplanar polygons to render correctly.</span></span>

<span data-ttu-id="91748-107">Wenn beispielsweise Reifen Markierungen und gelbe Linien auf eine Straßenebene angewendet werden, sollten die Markierungen direkt auf der Straße angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="91748-107">For instance, when applying tire marks and yellow lines to a roadway, the markings should appear directly on top of the road.</span></span> <span data-ttu-id="91748-108">Die z-Werte der Markierungen und der Straße sind jedoch identisch.</span><span class="sxs-lookup"><span data-stu-id="91748-108">However, the z values of the markings and the road are the same.</span></span> <span data-ttu-id="91748-109">Daher erzeugt der tiefen Puffer möglicherweise keine saubere Trennung zwischen den beiden.</span><span class="sxs-lookup"><span data-stu-id="91748-109">Therefore, the depth buffer might not produce a clean separation between the two.</span></span> <span data-ttu-id="91748-110">Einige Pixel im Hintergrundtyp können über dem Front-primitiv und umgekehrt gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="91748-110">Some pixels in the back primitive may be rendered on top of the front primitive and vice versa.</span></span> <span data-ttu-id="91748-111">Das resultierende Bild wird angezeigt, um von Frame zu Rahmen zu vershicheln.</span><span class="sxs-lookup"><span data-stu-id="91748-111">The resulting image appears to shimmer from frame to frame.</span></span> <span data-ttu-id="91748-112">Dieser Effekt heißt *z-Fighting* oder *Flimmern*.</span><span class="sxs-lookup"><span data-stu-id="91748-112">This effect is called *z-fighting* or *flimmering*.</span></span>

<span data-ttu-id="91748-113">Um dieses Problem zu beheben, verwenden Sie eine Schablone, um den Abschnitt des hintergrundprimitivs zu maskieren, in dem die Client Zugriffslizenz angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="91748-113">To solve this problem, use a stencil to mask the section of the back primitive where the decal will appear.</span></span> <span data-ttu-id="91748-114">Deaktivieren Sie die z-Pufferung, und Renderern Sie das Bild des Front-Primitivs in den maskierten Bereich der Renderziel-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="91748-114">Turn off z-buffering and render the image of the front primitive into the masked-off area of the render-target surface.</span></span>

<span data-ttu-id="91748-115">Obwohl mehrere Textur Mischungs Möglichkeiten verwendet werden können, um dieses Problem zu lösen, schränkt dies die Anzahl anderer spezieller Effekte ein, die Ihre Anwendung erzeugen kann.</span><span class="sxs-lookup"><span data-stu-id="91748-115">Although multiple texture blending can be used to solve this problem, doing so limits the number of other special effects that your application can produce.</span></span> <span data-ttu-id="91748-116">Wenn Sie den Schablonen Puffer zum Anwenden von Decals verwenden, werden Textur Mischungs Phasen für andere Effekte freigegeben.</span><span class="sxs-lookup"><span data-stu-id="91748-116">Using the stencil buffer to apply decals frees up texture blending stages for other effects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91748-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="91748-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91748-118">Techniken für Schablonen Puffer</span><span class="sxs-lookup"><span data-stu-id="91748-118">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



