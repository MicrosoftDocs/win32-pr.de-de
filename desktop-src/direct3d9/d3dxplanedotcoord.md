---
description: Berechnet das Punktprodukt einer Ebene und einen 3D-Vektor. Der w-Parameter des Vektors wird als 1 angenommen.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: D3DXPlaneDotCoord-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 99ee9db7df541dcf74867b828a73ede80f11e22b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219434"
---
# <a name="d3dxplanedotcoord-function"></a><span data-ttu-id="b2878-104">D3DXPlaneDotCoord-Funktion</span><span class="sxs-lookup"><span data-stu-id="b2878-104">D3DXPlaneDotCoord function</span></span>

<span data-ttu-id="b2878-105">Berechnet das Punktprodukt einer Ebene und einen 3D-Vektor.</span><span class="sxs-lookup"><span data-stu-id="b2878-105">Computes the dot product of a plane and a 3D vector.</span></span> <span data-ttu-id="b2878-106">Der w-Parameter des Vektors wird als 1 angenommen.</span><span class="sxs-lookup"><span data-stu-id="b2878-106">The w parameter of the vector is assumed to be 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2878-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2878-107">Syntax</span></span>


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="b2878-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2878-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2878-109">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2878-109">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2878-110">Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="b2878-110">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="b2878-111">Zeiger auf eine Quell- [**D3DXPLANE**](d3dxplane.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b2878-111">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b2878-112">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2878-112">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2878-113">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b2878-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b2878-114">Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b2878-114">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2878-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2878-115">Return value</span></span>

<span data-ttu-id="b2878-116">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b2878-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b2878-117">Das Punktprodukt der Ebene und des 3D-Vektors.</span><span class="sxs-lookup"><span data-stu-id="b2878-117">The dot product of the plane and 3D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2878-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2878-118">Remarks</span></span>

<span data-ttu-id="b2878-119">Bei einer Ebene (a, b, c, d) und einem 3D-Vektor (x, y, z) ist der Rückgabewert dieser Funktion ein \* x + b \* y + c \* z + d \* 1.</span><span class="sxs-lookup"><span data-stu-id="b2878-119">Given a plane (a, b, c, d) and a 3D vector (x, y, z) the return value of this function is a\*x + b\*y + c\*z + d\*1.</span></span> <span data-ttu-id="b2878-120">Die **D3DXPlaneDotCoord** -Funktion ist nützlich, um die Beziehung der Ebene mit einer Koordinate im 3D-Raum zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b2878-120">The **D3DXPlaneDotCoord** function is useful for determining the plane's relationship with a coordinate in 3D space.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2878-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2878-121">Requirements</span></span>



| <span data-ttu-id="b2878-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2878-122">Requirement</span></span> | <span data-ttu-id="b2878-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b2878-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2878-124">Header</span><span class="sxs-lookup"><span data-stu-id="b2878-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b2878-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2878-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b2878-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b2878-126">Library</span></span><br/> | <dl> <span data-ttu-id="b2878-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2878-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b2878-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2878-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2878-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="b2878-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b2878-130">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="b2878-130">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
</dt> <dt>

[<span data-ttu-id="b2878-131">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="b2878-131">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
</dt> </dl>

 

 
