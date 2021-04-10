---
description: Um die Renderingleistung zu verbessern, können Sie eine primitive, die von der Kamera entfernt ist, auslagern (oder entfernen).
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: Status der Zertifizierungsstelle (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86e71fd7c6543f0d232e32a630d73e0ebbadae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127125"
---
# <a name="culling-state-direct3d-9"></a><span data-ttu-id="17b22-103">Status der Zertifizierungsstelle (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="17b22-103">Culling State (Direct3D 9)</span></span>

<span data-ttu-id="17b22-104">Um die Renderingleistung zu verbessern, können Sie eine primitive, die von der Kamera entfernt ist, auslagern (oder entfernen).</span><span class="sxs-lookup"><span data-stu-id="17b22-104">To improve rendering performance, you can cull out (or remove) a primitive that faces away from the camera.</span></span> <span data-ttu-id="17b22-105">Bei einseitigen primitiven spart dies die Renderingzeit, da eine Backface nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="17b22-105">For single-sided primitives, this saves rendering time because a back-face is not visible.</span></span> <span data-ttu-id="17b22-106">Um die Daten zu aktivieren, müssen Sie die Sortierreihenfolge der Scheitel Punkte kennen (in der Regel gegen den Uhrzeigersinn).</span><span class="sxs-lookup"><span data-stu-id="17b22-106">To enable culling, you need to know the winding order of the vertices (typically counter-clockwise).</span></span> <span data-ttu-id="17b22-107">In diesem Beispiel werden alle primitiven entfernt, deren Rückseite vorwärts geht (bei einer Sortierreihenfolge gegen den Uhrzeigersinn):</span><span class="sxs-lookup"><span data-stu-id="17b22-107">This example will remove any primitive whose back face is facing forward (given a counter-clockwise winding order):</span></span>


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a><span data-ttu-id="17b22-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="17b22-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17b22-109">Rendering-Zustände</span><span class="sxs-lookup"><span data-stu-id="17b22-109">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



