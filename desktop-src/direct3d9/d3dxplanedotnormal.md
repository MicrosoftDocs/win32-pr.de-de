---
description: Berechnet das Punktprodukt einer Ebene und einen 3D-Vektor. Der w-Parameter des Vektors wird als 0 angenommen.
ms.assetid: 7aba1e94-6531-4c07-83b0-6100805e8bbd
title: D3DXPlaneDotNormal-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28903fc8ce0073e4014ae6ce75df636222ce32f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353333"
---
# <a name="d3dxplanedotnormal-function"></a><span data-ttu-id="b1cda-104">D3DXPlaneDotNormal-Funktion</span><span class="sxs-lookup"><span data-stu-id="b1cda-104">D3DXPlaneDotNormal function</span></span>

<span data-ttu-id="b1cda-105">Berechnet das Punktprodukt einer Ebene und einen 3D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="b1cda-105">Computes the dot product of a plane and a 3D vector.</span></span> <span data-ttu-id="b1cda-106">Der w-Parameter des Vektors wird als 0 angenommen.</span><span class="sxs-lookup"><span data-stu-id="b1cda-106">The w parameter of the vector is assumed to be 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1cda-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1cda-107">Syntax</span></span>


```C++
FLOAT D3DXPlaneDotNormal(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="b1cda-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1cda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1cda-109">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1cda-109">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1cda-110">Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="b1cda-110">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="b1cda-111">Zeiger auf eine Quell- [**D3DXPLANE**](d3dxplane.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b1cda-111">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b1cda-112">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1cda-112">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1cda-113">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b1cda-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b1cda-114">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b1cda-114">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1cda-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1cda-115">Return value</span></span>

<span data-ttu-id="b1cda-116">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1cda-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1cda-117">Das Punktprodukt der Ebene und des 3D-Vektors.</span><span class="sxs-lookup"><span data-stu-id="b1cda-117">The dot product of the plane and 3D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1cda-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1cda-118">Remarks</span></span>

<span data-ttu-id="b1cda-119">Bei einer Ebene (a, b, c, d) und einem 3D-Vektor (x, y, z) ist der Rückgabewert dieser Funktion ein \* x + b \* y + c \* z + d \* 0.</span><span class="sxs-lookup"><span data-stu-id="b1cda-119">Given a plane (a, b, c, d) and a 3D vector (x, y, z) the return value of this function is a\*x + b\*y + c\*z + d\*0.</span></span> <span data-ttu-id="b1cda-120">Die **D3DXPlaneDotNormal** -Funktion ist nützlich, um den Winkel zwischen der normalen Ebene der Ebene und einer anderen normal zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="b1cda-120">The **D3DXPlaneDotNormal** function is useful for calculating the angle between the normal of the plane, and another normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1cda-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1cda-121">Requirements</span></span>



| <span data-ttu-id="b1cda-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1cda-122">Requirement</span></span> | <span data-ttu-id="b1cda-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b1cda-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1cda-124">Header</span><span class="sxs-lookup"><span data-stu-id="b1cda-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b1cda-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1cda-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b1cda-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b1cda-126">Library</span></span><br/> | <dl> <span data-ttu-id="b1cda-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1cda-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b1cda-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1cda-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1cda-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="b1cda-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b1cda-130">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="b1cda-130">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
</dt> <dt>

[<span data-ttu-id="b1cda-131">**D3DXPlaneDotCoord**</span><span class="sxs-lookup"><span data-stu-id="b1cda-131">**D3DXPlaneDotCoord**</span></span>](d3dxplanedotcoord.md)
</dt> </dl>

 

 
