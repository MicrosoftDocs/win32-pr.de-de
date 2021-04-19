---
description: Erstellt eine Ebene von einem Punkt und einem normalen.
ms.assetid: 93c644d2-ab8c-47a1-9a3b-8b9c6a13178b
title: D3DXPlaneFromPointNormal-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9900a9f6838e253bd195374d00f90ee31fae07a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106369326"
---
# <a name="d3dxplanefrompointnormal-function-d3dx10mathh"></a><span data-ttu-id="5873a-103">D3DXPlaneFromPointNormal-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="5873a-103">D3DXPlaneFromPointNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="5873a-104">Erstellt eine Ebene von einem Punkt und einem normalen.</span><span class="sxs-lookup"><span data-stu-id="5873a-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="5873a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5873a-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="5873a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5873a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5873a-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5873a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5873a-108">Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="5873a-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="5873a-109">Zeiger auf das [**D3DXPLANE**](d3d10-d3dxplane.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="5873a-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5873a-110">*PPoint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5873a-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5873a-111">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5873a-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5873a-112">Zeiger auf ein [**D3DXVECTOR3**](d3d10-d3dxvector3.md)-Wert, der den zum Erstellen der Ebene verwendeten Punkt definiert.</span><span class="sxs-lookup"><span data-stu-id="5873a-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="5873a-113">*pnormal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5873a-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5873a-114">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5873a-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="5873a-115">Zeiger auf eine D3DXVECTOR3-Struktur, die das normale definiert, das zum Erstellen der Ebene verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5873a-115">Pointer to a D3DXVECTOR3 structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5873a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5873a-116">Return value</span></span>

<span data-ttu-id="5873a-117">Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="5873a-117">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="5873a-118">Ein Zeiger auf die D3DXPLANE-Struktur, die aus dem Punkt und der normalen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5873a-118">Pointer to the D3DXPLANE structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="5873a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5873a-119">Remarks</span></span>

<span data-ttu-id="5873a-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5873a-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="5873a-121">Auf diese Weise kann die D3DXPlaneFromPointNormal-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5873a-121">In this way, the D3DXPlaneFromPointNormal function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5873a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5873a-122">Requirements</span></span>



| <span data-ttu-id="5873a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5873a-123">Requirement</span></span> | <span data-ttu-id="5873a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5873a-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5873a-125">Header</span><span class="sxs-lookup"><span data-stu-id="5873a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5873a-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5873a-126"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5873a-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5873a-127">Library</span></span><br/> | <dl> <span data-ttu-id="5873a-128"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5873a-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5873a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5873a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5873a-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="5873a-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
