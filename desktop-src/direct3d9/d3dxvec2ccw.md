---
description: Gibt die z-Komponente zurück, indem das Kreuz Produkt zweier 2D-Vektoren übernommen wird.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: D3DXVec2CCW-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71c6e14171a9e7d12d86c30f05885cecf50ce973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355180"
---
# <a name="d3dxvec2ccw-function"></a><span data-ttu-id="2e5af-103">D3DXVec2CCW-Funktion</span><span class="sxs-lookup"><span data-stu-id="2e5af-103">D3DXVec2CCW function</span></span>

<span data-ttu-id="2e5af-104">Gibt die z-Komponente zurück, indem das Kreuz Produkt zweier 2D-Vektoren übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="2e5af-104">Returns the z-component by taking the cross product of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e5af-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e5af-105">Syntax</span></span>


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="2e5af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e5af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e5af-107">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e5af-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e5af-108">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="2e5af-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2e5af-109">Zeiger auf eine Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2e5af-109">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2e5af-110">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e5af-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e5af-111">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="2e5af-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="2e5af-112">Zeiger auf eine Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2e5af-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e5af-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e5af-113">Return value</span></span>

<span data-ttu-id="2e5af-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e5af-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e5af-115">Die z-Komponente.</span><span class="sxs-lookup"><span data-stu-id="2e5af-115">The z-component.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e5af-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e5af-116">Remarks</span></span>

<span data-ttu-id="2e5af-117">Diese Funktion bestimmt die z-Komponente, indem Sie das Kreuz Produkt anhand der folgenden Formel bestimmt: ((x1, Y1, 0) Cross (x2, Y2, 0)).</span><span class="sxs-lookup"><span data-stu-id="2e5af-117">This function determines the z-component by determining the cross-product based on the following formula: ((x1,y1,0) cross (x2,y2,0)).</span></span> <span data-ttu-id="2e5af-118">Oder wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2e5af-118">Or as shown in the following example.</span></span>


```
pV1->x * pV2->y - pV1->y * pV2->x
```



<span data-ttu-id="2e5af-119">Wenn der Wert der z-Komponente positiv ist, wird der Vektor V2 gegen den Uhrzeigersinn vom Vektor v1 gegen den Uhrzeigersinn.</span><span class="sxs-lookup"><span data-stu-id="2e5af-119">If the value of the z-component is positive, the vector V2 is counterclockwise from the vector V1.</span></span> <span data-ttu-id="2e5af-120">Diese Informationen sind nützlich für die gegenseitige Erkennung.</span><span class="sxs-lookup"><span data-stu-id="2e5af-120">This information is useful for back-face culling.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e5af-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e5af-121">Requirements</span></span>



| <span data-ttu-id="2e5af-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e5af-122">Requirement</span></span> | <span data-ttu-id="2e5af-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2e5af-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e5af-124">Header</span><span class="sxs-lookup"><span data-stu-id="2e5af-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2e5af-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e5af-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2e5af-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2e5af-126">Library</span></span><br/> | <dl> <span data-ttu-id="2e5af-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e5af-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2e5af-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e5af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e5af-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2e5af-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2e5af-130">**D3DXVec2Dot**</span><span class="sxs-lookup"><span data-stu-id="2e5af-130">**D3DXVec2Dot**</span></span>](d3dxvec2dot.md)
</dt> </dl>

 

 
