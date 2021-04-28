---
description: 'D3DXPlaneFromPoints-Funktion (D3DX10Math.h): Erstellt eine Ebene aus drei Punkten.'
ms.assetid: 0e77af1b-cedf-482c-8398-10becb398a2c
title: D3DXPlaneFromPoints-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPoints
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a3af01df7d1ce66029994226d040544b733a75df
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103318"
---
# <a name="d3dxplanefrompoints-function-d3dx10mathh"></a><span data-ttu-id="ad04b-103">D3DXPlaneFromPoints-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="ad04b-103">D3DXPlaneFromPoints function (D3DX10Math.h)</span></span>

<span data-ttu-id="ad04b-104">Erstellt eine Ebene aus drei Punkten.</span><span class="sxs-lookup"><span data-stu-id="ad04b-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad04b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad04b-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="ad04b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad04b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad04b-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ad04b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-108">Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad04b-108">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="ad04b-109">Zeiger auf die [**D3DXPLANE,**](d3d10-d3dxplane.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="ad04b-109">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ad04b-110">*pV1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ad04b-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-111">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad04b-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad04b-112">Zeiger auf einen [**D3DXVECTOR3,**](d3d10-d3dxvector3.md)der einen der Punkte definiert, die zum Erstellen der Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad04b-112">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="ad04b-113">*pV2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ad04b-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-114">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad04b-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad04b-115">Zeiger auf eine D3DXVECTOR3-Struktur, die einen der Punkte definiert, die zum Erstellen der Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad04b-115">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="ad04b-116">*pV3* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ad04b-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-117">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad04b-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad04b-118">Zeiger auf eine D3DXVECTOR3-Struktur, die einen der Punkte definiert, die zum Erstellen der Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad04b-118">Pointer to a D3DXVECTOR3 structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad04b-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad04b-119">Return value</span></span>

<span data-ttu-id="ad04b-120">Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad04b-120">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="ad04b-121">Zeiger auf die D3DXPLANE-Struktur, die aus den angegebenen Punkten erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad04b-121">Pointer to the D3DXPLANE structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad04b-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad04b-122">Remarks</span></span>

<span data-ttu-id="ad04b-123">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ad04b-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ad04b-124">Auf diese Weise kann die D3DXPlaneFromPoints-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad04b-124">In this way, the D3DXPlaneFromPoints function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad04b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad04b-125">Requirements</span></span>



| <span data-ttu-id="ad04b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad04b-126">Requirement</span></span> | <span data-ttu-id="ad04b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ad04b-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad04b-128">Header</span><span class="sxs-lookup"><span data-stu-id="ad04b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="ad04b-129"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ad04b-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="ad04b-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ad04b-130">Library</span></span><br/> | <dl> <span data-ttu-id="ad04b-131"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad04b-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ad04b-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ad04b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad04b-133">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad04b-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
