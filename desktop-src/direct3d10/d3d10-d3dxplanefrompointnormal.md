---
description: 'D3DXPlaneFromPointNormal-Funktion (D3DX10Math.h): Erstellt eine Ebene aus einem Punkt und einer Normalen.'
ms.assetid: 93c644d2-ab8c-47a1-9a3b-8b9c6a13178b
title: D3DXPlaneFromPointNormal-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 519ce82a8d5a8c6adaf22b69047a8d365bd777ac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108838"
---
# <a name="d3dxplanefrompointnormal-function-d3dx10mathh"></a><span data-ttu-id="2f3f3-103">D3DXPlaneFromPointNormal-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="2f3f3-103">D3DXPlaneFromPointNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="2f3f3-104">Erstellt eine Ebene aus einem Punkt und einem Normalwert.</span><span class="sxs-lookup"><span data-stu-id="2f3f3-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f3f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f3f3-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="2f3f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f3f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f3f3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2f3f3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f3f3-108">Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f3f3-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="2f3f3-109">Zeiger auf die [**D3DXPLANE,**](d3d10-d3dxplane.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="2f3f3-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2f3f3-110">*pPoint* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2f3f3-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f3f3-111">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f3f3-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f3f3-112">Zeiger auf einen [**D3DXVECTOR3,**](d3d10-d3dxvector3.md)der den Punkt definiert, der zum Erstellen der Ebene verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f3f3-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="2f3f3-113">*pNormal* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2f3f3-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f3f3-114">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f3f3-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2f3f3-115">Zeiger auf eine D3DXVECTOR3-Struktur, die den zum Erstellen der Ebene verwendeten Normalwert definiert.</span><span class="sxs-lookup"><span data-stu-id="2f3f3-115">Pointer to a D3DXVECTOR3 structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f3f3-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f3f3-116">Return value</span></span>

<span data-ttu-id="2f3f3-117">Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f3f3-117">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="2f3f3-118">Zeiger auf die D3DXPLANE-Struktur, die aus dem Punkt und dem Normalwert erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2f3f3-118">Pointer to the D3DXPLANE structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f3f3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f3f3-119">Remarks</span></span>

<span data-ttu-id="2f3f3-120">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2f3f3-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2f3f3-121">Auf diese Weise kann die D3DXPlaneFromPointNormal-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f3f3-121">In this way, the D3DXPlaneFromPointNormal function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f3f3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f3f3-122">Requirements</span></span>



| <span data-ttu-id="2f3f3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f3f3-123">Requirement</span></span> | <span data-ttu-id="2f3f3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2f3f3-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3f3-125">Header</span><span class="sxs-lookup"><span data-stu-id="2f3f3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2f3f3-126"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="2f3f3-126"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2f3f3-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2f3f3-127">Library</span></span><br/> | <dl> <span data-ttu-id="2f3f3-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f3f3-128"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f3f3-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2f3f3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f3f3-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2f3f3-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
