---
description: 'D3DXMatrixReflect-Funktion (D3DX10Math.h): Erstellt eine Matrix, die das Koordinatensystem einer Ebene widerspiegelt.'
ms.assetid: bd2c5905-780e-4fac-a848-d7dbcfc390c6
title: D3DXMatrixReflect-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixReflect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f96224c881dcd5db2cc1c356003ab96e8a626900
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103408"
---
# <a name="d3dxmatrixreflect-function-d3dx10mathh"></a><span data-ttu-id="1845e-103">D3DXMatrixReflect-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="1845e-103">D3DXMatrixReflect function (D3DX10Math.h)</span></span>

<span data-ttu-id="1845e-104">Erstellt eine Matrix, die das Koordinatensystem einer Ebene widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="1845e-104">Builds a matrix that reflects the coordinate system about a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="1845e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1845e-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="1845e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1845e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1845e-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1845e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1845e-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1845e-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1845e-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="1845e-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1845e-110">*pPlane* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1845e-110">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1845e-111">Typ: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="1845e-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="1845e-112">Zeiger auf die [**D3DXPLANE-Quelldatei.**](d3d10-d3dxplane.md)</span><span class="sxs-lookup"><span data-stu-id="1845e-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1845e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1845e-113">Return value</span></span>

<span data-ttu-id="1845e-114">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1845e-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1845e-115">Zeiger auf eine D3DXMATRIX-Struktur, die das Koordinatensystem der Quellebene widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="1845e-115">Pointer to a D3DXMATRIX structure that reflects the coordinate system about the source plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="1845e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1845e-116">Remarks</span></span>

<span data-ttu-id="1845e-117">Diese Funktion normalisiert die Ebenengleichung, bevor sie die reflektierte Matrix erstellt.</span><span class="sxs-lookup"><span data-stu-id="1845e-117">This function normalizes the plane equation before it creates the reflected matrix.</span></span>

<span data-ttu-id="1845e-118">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1845e-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1845e-119">Auf diese Weise kann die D3DXMatrixReflect-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1845e-119">In this way, the D3DXMatrixReflect function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1845e-120">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="1845e-120">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a><span data-ttu-id="1845e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1845e-121">Requirements</span></span>



| <span data-ttu-id="1845e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1845e-122">Requirement</span></span> | <span data-ttu-id="1845e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1845e-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1845e-124">Header</span><span class="sxs-lookup"><span data-stu-id="1845e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1845e-125"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1845e-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1845e-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1845e-126">Library</span></span><br/> | <dl> <span data-ttu-id="1845e-127"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1845e-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1845e-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1845e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1845e-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1845e-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
