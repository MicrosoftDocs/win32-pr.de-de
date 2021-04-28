---
description: 'D3DXPlaneTransform-Funktion (D3DX10Math.h): Transformiert eine Ebene durch eine Matrix. Die Eingabematrix ist die umgekehrte Transponieren der tatsächlichen Transformation.'
ms.assetid: ded06eac-4086-47e8-bc55-c37959afc22d
title: D3DXPlaneTransform-Funktion (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9b1d16ba2a29d42614c388a6207503ad32dd5e0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108788"
---
# <a name="d3dxplanetransform-function-d3dx10mathh"></a><span data-ttu-id="322fa-104">D3DXPlaneTransform-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="322fa-104">D3DXPlaneTransform function (D3DX10Math.h)</span></span>

<span data-ttu-id="322fa-105">Transformiert eine Ebene durch eine Matrix.</span><span class="sxs-lookup"><span data-stu-id="322fa-105">Transforms a plane by a matrix.</span></span> <span data-ttu-id="322fa-106">Die Eingabematrix ist die umgekehrte Transponieren der tatsächlichen Transformation.</span><span class="sxs-lookup"><span data-stu-id="322fa-106">The input matrix is the inverse transpose of the actual transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="322fa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="322fa-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="322fa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="322fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="322fa-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="322fa-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="322fa-110">Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="322fa-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="322fa-111">Zeiger auf die [**D3DXPLANE,die**](d3d10-d3dxplane.md) die resultierende transformierte Ebene enthält.</span><span class="sxs-lookup"><span data-stu-id="322fa-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that contains the resulting transformed plane.</span></span> <span data-ttu-id="322fa-112">Weitere Informationen sind im Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="322fa-112">See example.</span></span>

</dd> <dt>

<span data-ttu-id="322fa-113">*pP* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="322fa-113">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="322fa-114">Typ: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="322fa-114">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="322fa-115">Zeiger auf die D3DXPLANE-Eingabestruktur, die die ebene enthält, die transformiert wird.</span><span class="sxs-lookup"><span data-stu-id="322fa-115">Pointer to the input D3DXPLANE structure, which contains the plane that will be transformed.</span></span> <span data-ttu-id="322fa-116">Der Vektor (a,b,c), der die Ebene beschreibt, muss normalisiert werden, bevor diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="322fa-116">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="322fa-117">Weitere Informationen sind im Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="322fa-117">See example.</span></span>

</dd> <dt>

<span data-ttu-id="322fa-118">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="322fa-118">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="322fa-119">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="322fa-119">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="322fa-120">Zeiger auf die [**D3DXMATRIX-Quellstruktur,**](d3d10-d3dxmatrix.md) die die Transformationswerte enthält.</span><span class="sxs-lookup"><span data-stu-id="322fa-120">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the transformation values.</span></span> <span data-ttu-id="322fa-121">Diese Matrix muss die umgekehrte Transponieren der Transformationswerte enthalten.</span><span class="sxs-lookup"><span data-stu-id="322fa-121">This matrix must contain the inverse transpose of the transformation values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="322fa-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="322fa-122">Return value</span></span>

<span data-ttu-id="322fa-123">Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="322fa-123">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="322fa-124">Zeiger auf eine D3DXPLANE-Struktur, die die transformierte Ebene darstellt.</span><span class="sxs-lookup"><span data-stu-id="322fa-124">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="322fa-125">Dies ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird, sodass diese Funktion als Parameter für eine andere Funktion verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="322fa-125">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="322fa-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="322fa-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="322fa-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="322fa-127">Examples</span></span>

<span data-ttu-id="322fa-128">In diesem Beispiel wird eine Ebene transformiert, indem eine nicht einheitliche Skala angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="322fa-128">This example transforms a plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="322fa-129">Eine Ebene wird durch ax + by + soll + dw = 0 beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="322fa-129">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="322fa-130">Die erste Ebene wird mit (a,b,c,d) = (0,1,1,0) erstellt. Dabei handelt es sich um eine Ebene, die durch y + z = 0 beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="322fa-130">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="322fa-131">Nach der Skalierung enthält die neue Ebene (a,b,c,d) = (0, 0,353f, 0,235f, 0), die die neue Ebene anzeigt, die durch 0,353y + 0,235z = 0 beschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="322fa-131">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="322fa-132">Der Parameter pM enthält die umgekehrte Transponierung der Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="322fa-132">The parameter pM contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="322fa-133">Die umgekehrte Transponieren ist für diese Methode erforderlich, damit auch der normale Vektor der transformierten Ebene ordnungsgemäß transformiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="322fa-133">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="322fa-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="322fa-134">Requirements</span></span>



| <span data-ttu-id="322fa-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="322fa-135">Requirement</span></span> | <span data-ttu-id="322fa-136">Wert</span><span class="sxs-lookup"><span data-stu-id="322fa-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="322fa-137">Header</span><span class="sxs-lookup"><span data-stu-id="322fa-137">Header</span></span><br/>  | <dl> <span data-ttu-id="322fa-138"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="322fa-138"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="322fa-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="322fa-139">Library</span></span><br/> | <dl> <span data-ttu-id="322fa-140"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="322fa-140"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="322fa-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="322fa-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="322fa-142">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="322fa-142">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
