---
description: Identifiziert nachfolgende Transformations Matrizen, die verwendet werden können, um Vertices mit der entsprechenden Matrix und einem im Vertex-Format angegebenen Mischungs Gewichtungswert (Beta) zu kombinieren.
ms.assetid: cab444c2-b245-4d1a-a90c-745c92a2ea89
title: D3DTS_WORLDn (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDn
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 004435d278538c788e21ed7dc3482fd5e248895b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351936"
---
# <a name="d3dts_worldn"></a><span data-ttu-id="0d421-103">D3DTS \_ worldn</span><span class="sxs-lookup"><span data-stu-id="0d421-103">D3DTS\_WORLDn</span></span>

<span data-ttu-id="0d421-104">Identifiziert nachfolgende Transformations Matrizen, die verwendet werden können, um Vertices mit der entsprechenden Matrix und einem im Vertex-Format angegebenen Mischungs Gewichtungswert (Beta) zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="0d421-104">Identifies subsequent transformation matrices that can be used to blend vertices by using the corresponding matrix and a blending (beta) weight value specified in the vertex format.</span></span>

``` syntax
#define D3DTS_WORLDn 
#define D3DTS_WORLD1 D3DTS_WORLDMATRIX(1)
#define D3DTS_WORLD2 D3DTS_WORLDMATRIX(2)
#define D3DTS_WORLD3 D3DTS_WORLDMATRIX(3)
```

## <a name="remarks"></a><span data-ttu-id="0d421-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d421-105">Remarks</span></span>

<span data-ttu-id="0d421-106">Diese Makros werden bereitgestellt, um das Portieren vorhandener Anwendungen auf Direct3D 9 zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="0d421-106">These macros are provided to facilitate porting existing applications to Direct3D 9.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d421-107">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d421-107">Requirements</span></span>



| <span data-ttu-id="0d421-108">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d421-108">Requirement</span></span> | <span data-ttu-id="0d421-109">Wert</span><span class="sxs-lookup"><span data-stu-id="0d421-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d421-110">Header</span><span class="sxs-lookup"><span data-stu-id="0d421-110">Header</span></span><br/> | <dl> <span data-ttu-id="0d421-111"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d421-111"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d421-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d421-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d421-113">Makros</span><span class="sxs-lookup"><span data-stu-id="0d421-113">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="0d421-114">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="0d421-114">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="0d421-115">**D3DTS \_ worldmatrix**</span><span class="sxs-lookup"><span data-stu-id="0d421-115">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
