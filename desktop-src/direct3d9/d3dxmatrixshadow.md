---
description: 'D3DXMatrixShadow-Funktion (D3dx9math.h): Erstellt eine Matrix, die die Geometrie in eine Ebene flach macht.'
ms.assetid: 8f283ff9-c879-476c-8057-f4fe77a7a9e7
title: D3DXMatrixShadow-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixShadow
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 111a1448f62cae3f782917de76d92e88aa5a3356
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118058"
---
# <a name="d3dxmatrixshadow-function-d3dx9mathh"></a><span data-ttu-id="cacce-103">D3DXMatrixShadow-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="cacce-103">D3DXMatrixShadow function (D3dx9math.h)</span></span>

<span data-ttu-id="cacce-104">Erstellt eine Matrix, die die Geometrie in eine Ebene flach macht.</span><span class="sxs-lookup"><span data-stu-id="cacce-104">Builds a matrix that flattens geometry into a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="cacce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cacce-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="cacce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cacce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cacce-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cacce-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cacce-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="cacce-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cacce-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="cacce-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="cacce-110">*pLight* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cacce-110">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cacce-111">Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="cacce-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="cacce-112">Zeiger auf eine [**D3DXVECTOR4-Struktur,**](d3dxvector4.md) die die Position des Lichts beschreibt.</span><span class="sxs-lookup"><span data-stu-id="cacce-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure describing the light's position.</span></span>

</dd> <dt>

<span data-ttu-id="cacce-113">*pPlane* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cacce-113">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cacce-114">Typ: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="cacce-114">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="cacce-115">Zeiger auf die [**D3DXPLANE-Quellstruktur.**](d3dxplane.md)</span><span class="sxs-lookup"><span data-stu-id="cacce-115">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cacce-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cacce-116">Return value</span></span>

<span data-ttu-id="cacce-117">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="cacce-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="cacce-118">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Geometrie in eine Ebene flacht.</span><span class="sxs-lookup"><span data-stu-id="cacce-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that flattens geometry into a plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="cacce-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cacce-119">Remarks</span></span>

<span data-ttu-id="cacce-120">Die **D3DXMatrixShadow-Funktion** flacht die Geometrie in eine Ebene, als würde sie einen Schatten von einem Licht werfen.</span><span class="sxs-lookup"><span data-stu-id="cacce-120">The **D3DXMatrixShadow** function flattens geometry into a plane, as if casting a shadow from a light.</span></span>

<span data-ttu-id="cacce-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="cacce-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="cacce-122">Auf diese Weise kann die **D3DXMatrixShadow-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cacce-122">In this way, the **D3DXMatrixShadow** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="cacce-123">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="cacce-123">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
L = Light;
d = -dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



<span data-ttu-id="cacce-124">Wenn die w-Komponente des Lichts 0 ist, stellt der Strahl vom Ursprung zum Licht ein direktionales Licht dar.</span><span class="sxs-lookup"><span data-stu-id="cacce-124">If the light's w-component is 0, the ray from the origin to the light represents a directional light.</span></span> <span data-ttu-id="cacce-125">Wenn es 1 ist, ist das Licht ein Punktlicht.</span><span class="sxs-lookup"><span data-stu-id="cacce-125">If it is 1, the light is a point light.</span></span>

## <a name="requirements"></a><span data-ttu-id="cacce-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cacce-126">Requirements</span></span>



| <span data-ttu-id="cacce-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cacce-127">Requirement</span></span> | <span data-ttu-id="cacce-128">Wert</span><span class="sxs-lookup"><span data-stu-id="cacce-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cacce-129">Header</span><span class="sxs-lookup"><span data-stu-id="cacce-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cacce-130"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="cacce-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="cacce-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cacce-131">Library</span></span><br/> | <dl> <span data-ttu-id="cacce-132"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="cacce-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cacce-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cacce-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cacce-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="cacce-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




