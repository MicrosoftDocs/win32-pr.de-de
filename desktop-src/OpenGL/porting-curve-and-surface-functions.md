---
title: Portieren von Kurven-und Oberflächen Funktionen
description: Portieren von Kurven-und Oberflächen Funktionen
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- IRIS GL portieren, Kurven
- Portieren von IRIS GL, Kurven
- Portieren auf OpenGL von IRIS GL, Kurven
- OpenGL-Portierung von IRIS GL, Kurven
- IRIS GL portieren, Surface-Patches
- Portieren von IRIS GL, Surface-Patches
- Portieren auf OpenGL von IRIS GL, Surface-Patches
- OpenGL-Portierung von IRIS GL, Surface-Patches
- Kurven
- Surface-Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3caedc89697d1c83325a00b3dc1cb55c34612e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309455"
---
# <a name="porting-curve-and-surface-functions"></a><span data-ttu-id="e58c0-113">Portieren von Kurven-und Oberflächen Funktionen</span><span class="sxs-lookup"><span data-stu-id="e58c0-113">Porting Curve and Surface Functions</span></span>

<span data-ttu-id="e58c0-114">OpenGL unterstützt keine Entsprechungen der Iris GL-Funktionen für Kurven und Oberflächen Patches.</span><span class="sxs-lookup"><span data-stu-id="e58c0-114">OpenGL doesn't support equivalents to the IRIS GL functions for curves and surface patches.</span></span> <span data-ttu-id="e58c0-115">Sie müssen Ihren Code neu schreiben, wenn er einen der folgenden Aufrufe umfasst:</span><span class="sxs-lookup"><span data-stu-id="e58c0-115">You'll need to rewrite your code if it includes any of the following calls:</span></span>

-   <span data-ttu-id="e58c0-116">**mit defbasis**</span><span class="sxs-lookup"><span data-stu-id="e58c0-116">**defbasis**</span></span>
-   <span data-ttu-id="e58c0-117">**"Cursor**", " **Cursor Genauigkeit**", " **CRV**", " **crvN**", " **rcrv**", " **rcrvn**" und " **Cursor** "</span><span class="sxs-lookup"><span data-stu-id="e58c0-117">**curvebasis**, **curveprecision**, **crv**, **crvn**, **rcrv**, **rcrvn**, and **curveit**</span></span>
-   <span data-ttu-id="e58c0-118">**Patchbasis**, **patchkurven**, **patchgenauigkeit**, **Patch** und **rpatch**</span><span class="sxs-lookup"><span data-stu-id="e58c0-118">**patchbasis**, **patchcurves**, **patchprecision**, **patch**, and **rpatch**</span></span>

<span data-ttu-id="e58c0-119">Dieses Thema enthält Informationen zu den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="e58c0-119">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="e58c0-120">Portieren von nursb-Objekten</span><span class="sxs-lookup"><span data-stu-id="e58c0-120">Porting NURBS Objects</span></span>](porting-nurbs-objects.md)
-   [<span data-ttu-id="e58c0-121">Portieren von nursb-Kurven</span><span class="sxs-lookup"><span data-stu-id="e58c0-121">Porting NURBS Curves</span></span>](porting-nurbs-curves.md)
-   [<span data-ttu-id="e58c0-122">Portieren von Kürzungs Kurven</span><span class="sxs-lookup"><span data-stu-id="e58c0-122">Porting Trimming Curves</span></span>](porting-trimming-curves.md)
-   [<span data-ttu-id="e58c0-123">Portieren von nursb-Oberflächen</span><span class="sxs-lookup"><span data-stu-id="e58c0-123">Porting NURBS Surfaces</span></span>](porting-nurbs-surfaces.md)

 

 




