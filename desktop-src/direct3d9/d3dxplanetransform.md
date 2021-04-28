---
description: 'D3DXPlaneTransform-Funktion (D3dx9math.h): Transformiert eine Ebene durch eine Matrix. Die Eingabematrix ist die umgekehrte Transponierung der tatsächlichen Transformation.'
ms.assetid: 3581b397-cbd8-4aed-80dd-1841f331a367
title: D3DXPlaneTransform-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1f1f6ffc45098ba8f8b689e6f6212e5bec4fd679
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098018"
---
# <a name="d3dxplanetransform-function-d3dx9mathh"></a><span data-ttu-id="bea03-104">D3DXPlaneTransform-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="bea03-104">D3DXPlaneTransform function (D3dx9math.h)</span></span>

<span data-ttu-id="bea03-105">Transformiert eine Ebene durch eine Matrix.</span><span class="sxs-lookup"><span data-stu-id="bea03-105">Transforms a plane by a matrix.</span></span> <span data-ttu-id="bea03-106">Die Eingabematrix ist die umgekehrte Transponierung der tatsächlichen Transformation.</span><span class="sxs-lookup"><span data-stu-id="bea03-106">The input matrix is the inverse transpose of the actual transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bea03-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bea03-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="bea03-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bea03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bea03-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bea03-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bea03-110">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="bea03-110">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="bea03-111">Zeiger auf die [**D3DXPLANE-Struktur,**](d3dxplane.md) die die resultierende transformierte Ebene enthält.</span><span class="sxs-lookup"><span data-stu-id="bea03-111">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="bea03-112">Weitere Informationen sind im Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="bea03-112">See example.</span></span>

</dd> <dt>

<span data-ttu-id="bea03-113">*pP* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bea03-113">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bea03-114">Typ: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="bea03-114">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="bea03-115">Zeiger auf die [**D3DXPLANE-Eingabestruktur,**](d3dxplane.md) die die ebene enthält, die transformiert wird.</span><span class="sxs-lookup"><span data-stu-id="bea03-115">Pointer to the input [**D3DXPLANE**](d3dxplane.md) structure, which contains the plane that will be transformed.</span></span> <span data-ttu-id="bea03-116">Der Vektor (a,b,c), der die Ebene beschreibt, muss normalisiert werden, bevor diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bea03-116">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="bea03-117">Weitere Informationen sind im Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="bea03-117">See example.</span></span>

</dd> <dt>

<span data-ttu-id="bea03-118">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bea03-118">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bea03-119">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="bea03-119">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bea03-120">Zeiger auf die [**D3DXMATRIX-Quellstruktur,**](d3dxmatrix.md) die die Transformationswerte enthält.</span><span class="sxs-lookup"><span data-stu-id="bea03-120">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure, which contains the transformation values.</span></span> <span data-ttu-id="bea03-121">Diese Matrix muss die umgekehrte Transponierung der Transformationswerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="bea03-121">This matrix must contain the inverse transpose of the transformation values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bea03-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bea03-122">Return value</span></span>

<span data-ttu-id="bea03-123">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="bea03-123">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="bea03-124">Zeiger auf eine [**D3DXPLANE-Struktur,**](d3dxplane.md) die die transformierte Ebene darstellt.</span><span class="sxs-lookup"><span data-stu-id="bea03-124">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure, representing the transformed plane.</span></span> <span data-ttu-id="bea03-125">Dies ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird, sodass diese Funktion als Parameter für eine andere Funktion verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="bea03-125">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="bea03-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bea03-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="bea03-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bea03-127">Examples</span></span>

<span data-ttu-id="bea03-128">In diesem Beispiel wird eine Ebene durch Anwenden einer nicht einheitlichen Skala transformiert.</span><span class="sxs-lookup"><span data-stu-id="bea03-128">This example transforms a plane by applying a non-uniform scale.</span></span>


```
D3DXPLANE   planeNew;
D3DXPLANE   plane(0,1,1,0);
D3DXPlaneNormalize(&plane, &plane);

D3DXMATRIX  matrix;
D3DXMatrixScaling(&matrix, 1.0f,2.0f,3.0f); 
D3DXMatrixInverse(&matrix, NULL, &matrix);
D3DXMatrixTranspose(&matrix, &matrix);
D3DXPlaneTransform(&planeNew, &plane, &matrix);
```



<span data-ttu-id="bea03-129">Eine Ebene wird durch ax + by + dw + dw = 0 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bea03-129">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="bea03-130">Die erste Ebene wird mit (a,b,c,d) = (0,1,1,0) erstellt. Dies ist eine Ebene, die von y + z = 0 beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="bea03-130">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="bea03-131">Nach der Skalierung enthält die neue Ebene (a,b,c,d) = (0, 0,353f, 0,235f, 0), die die neue Ebene zeigt, die von 0,353y + 0,235z = 0 beschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="bea03-131">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="bea03-132">Der Parameter pM enthält die umgekehrte Transponierung der Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="bea03-132">The parameter pM contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="bea03-133">Die umgekehrte Transponierung ist für diese Methode erforderlich, damit auch der normale Vektor der transformierten Ebene ordnungsgemäß transformiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bea03-133">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="bea03-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bea03-134">Requirements</span></span>



| <span data-ttu-id="bea03-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bea03-135">Requirement</span></span> | <span data-ttu-id="bea03-136">Wert</span><span class="sxs-lookup"><span data-stu-id="bea03-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bea03-137">Header</span><span class="sxs-lookup"><span data-stu-id="bea03-137">Header</span></span><br/>  | <dl> <span data-ttu-id="bea03-138"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="bea03-138"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bea03-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bea03-139">Library</span></span><br/> | <dl> <span data-ttu-id="bea03-140"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bea03-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bea03-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bea03-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bea03-142">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="bea03-142">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="bea03-143">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="bea03-143">**D3DXPlaneNormalize**</span></span>](d3dxplanenormalize.md)
</dt> <dt>

[<span data-ttu-id="bea03-144">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="bea03-144">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="bea03-145">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="bea03-145">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="bea03-146">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="bea03-146">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> <dt>

[<span data-ttu-id="bea03-147">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="bea03-147">**D3DXMatrixInverse**</span></span>](d3dxmatrixinverse.md)
</dt> <dt>

[<span data-ttu-id="bea03-148">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="bea03-148">**D3DXMatrixTranspose**</span></span>](d3dxmatrixtranspose.md)
</dt> </dl>

 

 




