---
description: Wenn Sie nicht mit einem Vertex-Shader oder einem Pixelshader Leuchten, können Sie die Beleuchtungs-Engine in der Laufzeit verwenden.
ms.assetid: vs|directx_sdk|~\lighting_state.htm
title: Beleuchtungs Zustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74f0e7b7ec4a8bcf0ee27c9bc1e643536819d8fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339646"
---
# <a name="lighting-state-direct3d-9"></a><span data-ttu-id="50452-103">Beleuchtungs Zustand (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="50452-103">Lighting State (Direct3D 9)</span></span>

<span data-ttu-id="50452-104">Wenn Sie nicht mit einem Vertex-Shader oder einem Pixelshader Leuchten, können Sie die Beleuchtungs-Engine in der Laufzeit verwenden.</span><span class="sxs-lookup"><span data-stu-id="50452-104">If you do not light with a vertex shader or a pixel shader, you may choose to use the lighting engine in the runtime.</span></span> <span data-ttu-id="50452-105">Die Beleuchtungs-Engine erfordert, dass die Vertex-Daten pro-vertexnormale enthalten. Vertices ohne normale Daten generieren in allen Beleuchtungsberechnungen ein Punktprodukt von NULL.</span><span class="sxs-lookup"><span data-stu-id="50452-105">The lighting engine requires that the vertex data contains per-vertex normals; vertices without normal data will generate a dot product of zero in all lighting computations.</span></span> <span data-ttu-id="50452-106">Die Beleuchtungsberechnungen werden in der [Mathematik der Beleuchtung ausführlicher behandelt (Direct3D 9)](mathematics-of-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="50452-106">The lighting calculations are covered in more detail in [Mathematics of Lighting (Direct3D 9)](mathematics-of-lighting.md).</span></span>

<span data-ttu-id="50452-107">Verwenden Sie zum Aktivieren der Beleuchtungs-Engine Folgendes:</span><span class="sxs-lookup"><span data-stu-id="50452-107">To enable the lighting engine, use:</span></span>


```
SetRenderState(D3DRS_LIGHTING, TRUE); 
```



## <a name="related-topics"></a><span data-ttu-id="50452-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="50452-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50452-109">Rendering-Zustände</span><span class="sxs-lookup"><span data-stu-id="50452-109">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



