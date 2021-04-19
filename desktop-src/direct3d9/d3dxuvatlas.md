---
description: Definiert Optionen zum Ausführen von geodäschen Entfernungs Berechnungen, wenn eine Textur an eine gekrümmte Oberfläche angepasst wird. Verwenden Sie dieses Flag, um beim Berechnen eines Textur Atlas zwischen hochwertigen und schnellen Berechnungen zu wählen.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: D3DXUVATLAS-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 64cc116199b688fc9dcd8d6fbf331d85da508948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355799"
---
# <a name="d3dxuvatlas-enumeration"></a><span data-ttu-id="06e50-104">D3DXUVATLAS-Enumeration</span><span class="sxs-lookup"><span data-stu-id="06e50-104">D3DXUVATLAS enumeration</span></span>

<span data-ttu-id="06e50-105">Definiert Optionen zum Ausführen von geodäschen Entfernungs Berechnungen, wenn eine Textur an eine gekrümmte Oberfläche angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="06e50-105">Defines options for performing geodesic distance calculations, when fitting a texture to a curved surface.</span></span> <span data-ttu-id="06e50-106">Verwenden Sie dieses Flag, um beim Berechnen eines Textur Atlas zwischen hochwertigen und schnellen Berechnungen zu wählen.</span><span class="sxs-lookup"><span data-stu-id="06e50-106">Use this flag to choose between high quality versus fast calculations when computing a texture atlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="06e50-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="06e50-107">Syntax</span></span>


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a><span data-ttu-id="06e50-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="06e50-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="06e50-109"><span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="06e50-109"><span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="06e50-110">Für Netzen mit mehr als 25 KB wird die schnelle geodasic-Entfernungs Methode angewendet, während für Netzen mit weniger als 25 KB die Entfernungs Methode für höhere Qualität auf Sie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="06e50-110">Meshes with more than 25k faces will have the fast geodasic distance method applied to them while meshes with fewer than 25k faces will have the higher quality geodesic distance method applied to them instead.</span></span>

</dd> <dt>

<span data-ttu-id="06e50-111"><span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS \_ Geodesic \_ fast**</span><span class="sxs-lookup"><span data-stu-id="06e50-111"><span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS\_GEODESIC\_FAST**</span></span>
</dt> <dd>

<span data-ttu-id="06e50-112">Verwendet Näherungs Werte, um die Diagramm Geschwindigkeit zu verbessern, indem zusätzliche Stretch oder mehr Diagramme für das Mesh ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="06e50-112">Uses approximations to improve charting speed at the cost of added stretch or more charts being output for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="06e50-113"><span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**D3DXUVATLAS \_ Geodesic- \_ Qualität**</span><span class="sxs-lookup"><span data-stu-id="06e50-113"><span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**D3DXUVATLAS\_GEODESIC\_QUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="06e50-114">Bietet bessere Qualitäts Diagramme, erfordert jedoch mehr Zeit und Arbeitsspeicher als schnell.</span><span class="sxs-lookup"><span data-stu-id="06e50-114">Provides better quality charts, but requires more time and memory than fast.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06e50-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06e50-115">Requirements</span></span>



| <span data-ttu-id="06e50-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06e50-116">Requirement</span></span> | <span data-ttu-id="06e50-117">Wert</span><span class="sxs-lookup"><span data-stu-id="06e50-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06e50-118">Header</span><span class="sxs-lookup"><span data-stu-id="06e50-118">Header</span></span><br/> | <dl> <span data-ttu-id="06e50-119"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="06e50-119"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06e50-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06e50-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06e50-121">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="06e50-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




