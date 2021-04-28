---
description: 'D3DXMatrixReflect-Funktion (D3dx9math.h): Erstellt eine Matrix, die das Koordinatensystem einer Ebene widerspiegelt.'
ms.assetid: f6dc3834-42f2-4ad0-8098-8c5e25e10d58
title: D3DXMatrixReflect-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4118a5f0a1cd997d5fab5fecebae449d4c30b09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118218"
---
# <a name="d3dxmatrixreflect-function-d3dx9mathh"></a><span data-ttu-id="76b22-103">D3DXMatrixReflect-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="76b22-103">D3DXMatrixReflect function (D3dx9math.h)</span></span>

<span data-ttu-id="76b22-104">Erstellt eine Matrix, die das Koordinatensystem über eine Ebene widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="76b22-104">Builds a matrix that reflects the coordinate system about a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="76b22-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76b22-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="76b22-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76b22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76b22-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="76b22-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76b22-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="76b22-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="76b22-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="76b22-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="76b22-110">*pPlane* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="76b22-110">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76b22-111">Typ: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="76b22-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="76b22-112">Zeiger auf die [**D3DXPLANE-Quellstruktur.**](d3dxplane.md)</span><span class="sxs-lookup"><span data-stu-id="76b22-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76b22-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76b22-113">Return value</span></span>

<span data-ttu-id="76b22-114">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="76b22-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="76b22-115">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Koordinatensystem über die Quellebene widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="76b22-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that reflects the coordinate system about the source plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="76b22-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76b22-116">Remarks</span></span>

<span data-ttu-id="76b22-117">Diese Funktion normalisiert die Ebenengleichung, bevor sie die reflektierte Matrix erstellt.</span><span class="sxs-lookup"><span data-stu-id="76b22-117">This function normalizes the plane equation before it creates the reflected matrix.</span></span>

<span data-ttu-id="76b22-118">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="76b22-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="76b22-119">Auf diese Weise kann die **D3DXMatrixReflect-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76b22-119">In this way, the **D3DXMatrixReflect** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="76b22-120">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="76b22-120">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a><span data-ttu-id="76b22-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76b22-121">Requirements</span></span>



| <span data-ttu-id="76b22-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76b22-122">Requirement</span></span> | <span data-ttu-id="76b22-123">Wert</span><span class="sxs-lookup"><span data-stu-id="76b22-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76b22-124">Header</span><span class="sxs-lookup"><span data-stu-id="76b22-124">Header</span></span><br/>  | <dl> <span data-ttu-id="76b22-125"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="76b22-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="76b22-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="76b22-126">Library</span></span><br/> | <dl> <span data-ttu-id="76b22-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="76b22-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="76b22-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="76b22-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76b22-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="76b22-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




