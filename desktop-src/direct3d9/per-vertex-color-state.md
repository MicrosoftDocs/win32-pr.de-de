---
description: Die Direct3D-Beleuchtungs-Engine kann bei der Durchführung der Beleuchtung Daten pro Scheitelpunkt Farbe verwenden, wenn Sie der Laufzeit mitteilen, dass die Daten vorhanden sind.
ms.assetid: acb43921-f0d4-4151-9371-1b99e5d30c0e
title: Per-Vertex Farben Zustand (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0104b427753fa3d7b7cf5a0a5a10cfeb5d10f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392347"
---
# <a name="per-vertex-color-state-direct3d-9"></a><span data-ttu-id="24b19-103">Per-Vertex Farben Zustand (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="24b19-103">Per-Vertex Color State (Direct3D 9)</span></span>

<span data-ttu-id="24b19-104">Die Direct3D-Beleuchtungs-Engine kann bei der Durchführung der Beleuchtung Daten pro Scheitelpunkt Farbe verwenden, wenn Sie der Laufzeit mitteilen, dass die Daten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="24b19-104">The Direct3D lighting engine can use per-vertex color data when performing lighting if you tell the runtime the data is present.</span></span> <span data-ttu-id="24b19-105">Dies erfolgt durch Aktivieren des folgenden Rendering-Status:</span><span class="sxs-lookup"><span data-stu-id="24b19-105">This is done by turning on the following render state:</span></span>


```
// disable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, FALSE);

// enable per-vertex color
SetRenderState(D3DRS_COLORVERTEX, TRUE);
```



<span data-ttu-id="24b19-106">Wenn die pro-Vertex-Farbe aktiviert ist, können Anwendungen die Quelle konfigurieren, von der das System Farbinformationen für einen Scheitelpunkt abruft.</span><span class="sxs-lookup"><span data-stu-id="24b19-106">If per-vertex color is enabled, applications can configure the source from which the system retrieves color information for a vertex.</span></span> <span data-ttu-id="24b19-107">Die "D3DRS \_ AmbientMaterialSource"-, "D3DRS \_ DiffuseMaterialSource"-, "D3DRS \_ emissivematerialsource"-und "D3DRS \_ SpecularMaterialSource"-Darstellung steuern die Umgebungs-, diffusen, emissive-bzw. Glanz Farben-Komponenten Quellen.</span><span class="sxs-lookup"><span data-stu-id="24b19-107">The D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE render states control the ambient, diffuse, emissive, and specular color component sources, respectively.</span></span> <span data-ttu-id="24b19-108">Jeder Status kann auf Member des [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) -enumerierten Typs festgelegt werden, der Konstanten definiert, die das System anweisen, das aktuelle Material, die diffuse Farbe oder die Glanz Farbe als Quelle für die angegebene Farbkomponente zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="24b19-108">Each state can be set to members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type, which defines constants that instruct the system to use the current material, diffuse color, or specular color as the source for the specified color component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24b19-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24b19-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24b19-110">Rendering-Zustände</span><span class="sxs-lookup"><span data-stu-id="24b19-110">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
