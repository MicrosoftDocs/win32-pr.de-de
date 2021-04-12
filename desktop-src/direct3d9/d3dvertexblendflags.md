---
description: Definiert Flags, die verwendet werden, um die Anzahl oder Matrizen zu steuern, die das System beim Ausführen von multimatrix-Vertex-Blending anwendet
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: D3DVERTEXBLENDFLAGS-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBLENDFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0b4d22740a9ad06a9848dc7649d62ac06d37a056
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354736"
---
# <a name="d3dvertexblendflags-enumeration"></a><span data-ttu-id="353f8-103">D3DVERTEXBLENDFLAGS-Enumeration</span><span class="sxs-lookup"><span data-stu-id="353f8-103">D3DVERTEXBLENDFLAGS enumeration</span></span>

<span data-ttu-id="353f8-104">Definiert Flags, die verwendet werden, um die Anzahl oder Matrizen zu steuern, die das System beim Ausführen von multimatrix-Vertex-Blending anwendet</span><span class="sxs-lookup"><span data-stu-id="353f8-104">Defines flags used to control the number or matrices that the system applies when performing multimatrix vertex blending.</span></span>

## <a name="syntax"></a><span data-ttu-id="353f8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="353f8-105">Syntax</span></span>


```C++
typedef enum D3DVERTEXBLENDFLAGS { 
  D3DVBF_DISABLE   = 0,
  D3DVBF_1WEIGHTS  = 1,
  D3DVBF_2WEIGHTS  = 2,
  D3DVBF_3WEIGHTS  = 3,
  D3DVBF_TWEENING  = 255,
  D3DVBF_0WEIGHTS  = 256
} D3DVERTEXBLENDFLAGS, *LPD3DVERTEXBLENDFLAGS;
```



## <a name="constants"></a><span data-ttu-id="353f8-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="353f8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="353f8-107"><span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF \_ Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="353f8-107"><span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="353f8-108">Vertex-Blending deaktivieren; wenden Sie nur die Weltmatrix an, die vom [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md) -Makro festgelegt wird, wobei der Indexwert für den Transformations Status 0 ist.</span><span class="sxs-lookup"><span data-stu-id="353f8-108">Disable vertex blending; apply only the world matrix set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation state is 0.</span></span>

</dd> <dt>

<span data-ttu-id="353f8-109"><span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1 Gewichtungen**</span><span class="sxs-lookup"><span data-stu-id="353f8-109"><span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF\_1WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="353f8-110">Aktivieren Sie die Vertex-Mischung zwischen den beiden Matrizen, die durch das [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md) -Makro festgelegt wurden, wobei der Indexwert für die Transformations Zustände 0 und 1 ist.</span><span class="sxs-lookup"><span data-stu-id="353f8-110">Enable vertex blending between the two matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="353f8-111"><span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2 Gewichtungen**</span><span class="sxs-lookup"><span data-stu-id="353f8-111"><span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF\_2WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="353f8-112">Aktivieren Sie die Vertex-Vermischung zwischen den drei Matrizen, die durch das [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md) -Makro festgelegt sind, wobei der Indexwert für die Transformations Zustände 0, 1 und 2 ist.</span><span class="sxs-lookup"><span data-stu-id="353f8-112">Enable vertex blending between the three matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0, 1, and 2.</span></span>

</dd> <dt>

<span data-ttu-id="353f8-113"><span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3gewichtungen**</span><span class="sxs-lookup"><span data-stu-id="353f8-113"><span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF\_3WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="353f8-114">Aktivieren Sie die vertexmischung zwischen den vier Matrizen, die durch das [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md) -Makro festgelegt werden, wobei der Indexwert für die Transformations Zustände 0, 1, 2 und 3 ist.</span><span class="sxs-lookup"><span data-stu-id="353f8-114">Enable vertex blending between the four matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0, 1, 2, and 3.</span></span>

</dd> <dt>

<span data-ttu-id="353f8-115"><span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**D3DVBF- \_ twiening**</span><span class="sxs-lookup"><span data-stu-id="353f8-115"><span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**D3DVBF\_TWEENING**</span></span>
</dt> <dd>

<span data-ttu-id="353f8-116">Die Vertex-Mischung erfolgt mithilfe des Werts, der D3DRS \_ tweumfactor zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="353f8-116">Vertex blending is done by using the value assigned to D3DRS\_TWEENFACTOR.</span></span>

</dd> <dt>

<span data-ttu-id="353f8-117"><span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0gewichtungen**</span><span class="sxs-lookup"><span data-stu-id="353f8-117"><span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF\_0WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="353f8-118">Verwenden Sie eine einzelne Matrix mit einer Gewichtung von 1,0.</span><span class="sxs-lookup"><span data-stu-id="353f8-118">Use a single matrix with a weight of 1.0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="353f8-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="353f8-119">Remarks</span></span>

<span data-ttu-id="353f8-120">Member dieses Typs werden mit dem D3DRS \_ vertexblend-Rendering-Zustand verwendet.</span><span class="sxs-lookup"><span data-stu-id="353f8-120">Members of this type are used with the D3DRS\_VERTEXBLEND render state.</span></span>

<span data-ttu-id="353f8-121">Geometrie Mischung (multimatrix-Vertex-Blending) erfordert, dass Ihre Anwendung ein Scheitelpunkt Format verwendet, das für jeden Scheitelpunkt über Mischungs-Gewichtungen (Beta) verfügt.</span><span class="sxs-lookup"><span data-stu-id="353f8-121">Geometry blending (multimatrix vertex blending) requires that your application use a vertex format that has blending (beta) weights for each vertex.</span></span>

## <a name="requirements"></a><span data-ttu-id="353f8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="353f8-122">Requirements</span></span>



| <span data-ttu-id="353f8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="353f8-123">Requirement</span></span> | <span data-ttu-id="353f8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="353f8-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="353f8-125">Header</span><span class="sxs-lookup"><span data-stu-id="353f8-125">Header</span></span><br/> | <dl> <span data-ttu-id="353f8-126"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="353f8-126"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="353f8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="353f8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="353f8-128">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="353f8-128">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="353f8-129">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="353f8-129">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> <dt>

[<span data-ttu-id="353f8-130">**D3DTS \_ Welt**</span><span class="sxs-lookup"><span data-stu-id="353f8-130">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="353f8-131">**D3DTS \_ worldn**</span><span class="sxs-lookup"><span data-stu-id="353f8-131">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="353f8-132">**D3DTS \_ worldmatrix**</span><span class="sxs-lookup"><span data-stu-id="353f8-132">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
