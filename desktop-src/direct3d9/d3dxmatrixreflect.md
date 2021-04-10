---
description: Erstellt eine Matrix, die das Koordinatensystem über eine Ebene wieder gibt.
ms.assetid: f6dc3834-42f2-4ad0-8098-8c5e25e10d58
title: D3DXMatrixReflect-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 2e54c5f93164e5fccee0d74199a1843a1476e69a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961548"
---
# <a name="d3dxmatrixreflect-function-d3dx9mathh"></a><span data-ttu-id="82638-103">D3DXMatrixReflect-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="82638-103">D3DXMatrixReflect function (D3dx9math.h)</span></span>

<span data-ttu-id="82638-104">Erstellt eine Matrix, die das Koordinatensystem über eine Ebene wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="82638-104">Builds a matrix that reflects the coordinate system about a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="82638-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="82638-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="82638-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="82638-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82638-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="82638-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="82638-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="82638-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="82638-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="82638-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="82638-110">*pplane* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82638-110">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82638-111">Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="82638-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="82638-112">Ein Zeiger auf die Quell- [**D3DXPLANE**](d3dxplane.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="82638-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82638-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82638-113">Return value</span></span>

<span data-ttu-id="82638-114">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="82638-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="82638-115">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Koordinatensystem über die Quell Ebene wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="82638-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that reflects the coordinate system about the source plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="82638-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82638-116">Remarks</span></span>

<span data-ttu-id="82638-117">Diese Funktion normalisiert die Gleichung der Ebene, bevor die reflektierte Matrix erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="82638-117">This function normalizes the plane equation before it creates the reflected matrix.</span></span>

<span data-ttu-id="82638-118">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="82638-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="82638-119">Auf diese Weise kann die **D3DXMatrixReflect** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82638-119">In this way, the **D3DXMatrixReflect** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="82638-120">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="82638-120">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a><span data-ttu-id="82638-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82638-121">Requirements</span></span>



| <span data-ttu-id="82638-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82638-122">Requirement</span></span> | <span data-ttu-id="82638-123">Wert</span><span class="sxs-lookup"><span data-stu-id="82638-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82638-124">Header</span><span class="sxs-lookup"><span data-stu-id="82638-124">Header</span></span><br/>  | <dl> <span data-ttu-id="82638-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="82638-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="82638-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="82638-126">Library</span></span><br/> | <dl> <span data-ttu-id="82638-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82638-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="82638-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82638-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82638-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="82638-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




