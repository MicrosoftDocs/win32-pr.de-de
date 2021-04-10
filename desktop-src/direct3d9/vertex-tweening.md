---
description: Vertex-Tweening kombiniert zwei vom Benutzer bereitgestellte Positionen (oder normale).
ms.assetid: vs|directx_sdk|~\vertex_tweening.htm
title: Vertex-Tweening (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a5458e384fa69b91b1eab1623fb526d514591f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213925"
---
# <a name="vertex-tweening-direct3d-9"></a><span data-ttu-id="55e0c-103">Vertex-Tweening (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="55e0c-103">Vertex Tweening (Direct3D 9)</span></span>

<span data-ttu-id="55e0c-104">Vertex-Tweening kombiniert zwei vom Benutzer bereitgestellte Positionen (oder normale).</span><span class="sxs-lookup"><span data-stu-id="55e0c-104">Vertex tweening blends two user-provided positions (or normals).</span></span> <span data-ttu-id="55e0c-105">Das twiening schließt sich gegenseitig aus der Vertex-Mischung mit Gewichtungen aus.</span><span class="sxs-lookup"><span data-stu-id="55e0c-105">Tweening is mutually exclusive from vertex blending with weights.</span></span> <span data-ttu-id="55e0c-106">Das twipping erfolgt vor Beleuchtung und Clipping und wird durch Festlegen von D3DRS \_ vertexblend auf D3DVBF \_ Tweening ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="55e0c-106">Tweening is performed before lighting and clipping, and is enabled by setting D3DRS\_VERTEXBLEND to D3DVBF\_TWEENING.</span></span> <span data-ttu-id="55e0c-107">Die resultierende Scheitelpunkt Position wird berechnet durch:</span><span class="sxs-lookup"><span data-stu-id="55e0c-107">The resulting vertex position is computed by:</span></span>


```
POSITION = POSITION1 * (1.0 - TWEENFACTOR) + POSITION2 * TWEENFACTOR
```



<span data-ttu-id="55e0c-108">Der gleiche Ansatz wird für die Berechnung von normalen verwendet.</span><span class="sxs-lookup"><span data-stu-id="55e0c-108">The same approach is used for calculating normals.</span></span> <span data-ttu-id="55e0c-109">Weitere Informationen finden Sie unter [Verwenden der Vertex-Tweening (Direct3D 9)](using-vertex-tweening.md).</span><span class="sxs-lookup"><span data-stu-id="55e0c-109">For more information, see [Using Vertex Tweening (Direct3D 9)](using-vertex-tweening.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="55e0c-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55e0c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55e0c-111">Geometrie Mischung</span><span class="sxs-lookup"><span data-stu-id="55e0c-111">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 



