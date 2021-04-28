---
description: 'D3DXPlaneTransformArray-Funktion (D3DX10Math.h): Transformiert ein Array von Ebenen durch eine Matrix. Die Vektoren, die die einzelnen Ebenen beschreiben, müssen normalisiert werden.'
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: D3DXPlaneTransformArray-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d8b02b64fd13e7466980340056fceccc1da784cf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103258"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a><span data-ttu-id="5a6b0-104">D3DXPlaneTransformArray-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="5a6b0-104">D3DXPlaneTransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="5a6b0-105">Transformiert ein Array von Ebenen durch eine Matrix.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="5a6b0-106">Die Vektoren, die die einzelnen Ebenen beschreiben, müssen normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a6b0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a6b0-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _In_          UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a><span data-ttu-id="5a6b0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a6b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a6b0-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5a6b0-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6b0-110">Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a6b0-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="5a6b0-111">Zeiger auf die [**D3DXPLANE-Struktur,**](d3d10-d3dxplane.md) die die resultierende transformierte Ebene enthält.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="5a6b0-112">Siehe Beispiel.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="5a6b0-113">*OutStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5a6b0-113">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6b0-114">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a6b0-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a6b0-115">Der Schritt jeder transformierten Ebene.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="5a6b0-116">*pP* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5a6b0-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6b0-117">Typ: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="5a6b0-117">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="5a6b0-118">Zeiger auf die D3DXPLANE-Eingabestruktur, die das Array der zu transformierten Ebenen enthält.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-118">Pointer to the input D3DXPLANE structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="5a6b0-119">Der Vektor (a, b, c), der die Ebene beschreibt, muss normalisiert werden, bevor diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-119">The vector (a, b, c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="5a6b0-120">Siehe Beispiel.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="5a6b0-121">*PStride* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5a6b0-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6b0-122">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a6b0-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a6b0-123">Der Schritt jeder nicht transformierten Ebene.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="5a6b0-124">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5a6b0-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6b0-125">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5a6b0-125">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5a6b0-126">Zeiger auf die [**D3DXMATRIX-Quellstruktur,**](d3d10-d3dxmatrix.md) die die umgekehrte Transponierung der Transformationswerte enthält.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-126">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="5a6b0-127">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a6b0-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6b0-128">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a6b0-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a6b0-129">Die Anzahl der zu transformierenden Ebenen.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a6b0-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a6b0-130">Return value</span></span>

<span data-ttu-id="5a6b0-131">Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a6b0-131">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="5a6b0-132">Zeiger auf eine D3DXPLANE-Struktur, die die transformierte Ebene darstellt.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-132">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="5a6b0-133">Dies ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird, sodass diese Funktion als Parameter für eine andere Funktion verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-133">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a6b0-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a6b0-134">Remarks</span></span>

<span data-ttu-id="5a6b0-135">In diesem Beispiel wird eine Ebene transformiert, indem eine nicht einheitliche Skala angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-135">This example transforms one plane by applying a non-uniform scale.</span></span>


```
#define ARRAYSIZE 4
D3DXPLANE planeNew[ARRAYSIZE];
D3DXPLANE plane[ARRAYSIZE];

for(int i = 0; i < ARRAYSIZE; i++)
{
    plane = D3DXPLANE( 0.0f, 1.0f, 1.0f, 0.0f );
    D3DXPlaneNormalize( &plane[i], &plane[i] );
}

D3DXMATRIX  matrix;
D3DXMatrixScaling( &matrix, 1.0f, 2.0f, 3.0f ); 
D3DXMatrixInverse( &matrix, NULL, &matrix );
D3DXMatrixTranspose( &matrix, &matrix );
D3DXPlaneTransformArray( &planeNew, sizeof (D3DXPLANE), &plane, 
                         sizeof (D3DXPLANE), &matrix, ARRAYSIZE );
```



<span data-ttu-id="5a6b0-136">Eine Ebene wird durch ax + by + soll + dw = 0 beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="5a6b0-137">Die erste Ebene wird mit (a,b,c,d) = (0,1,1,0) erstellt. Dabei handelt es sich um eine Ebene, die durch y + z = 0 beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="5a6b0-138">Nach der Skalierung enthält die neue Ebene (a,b,c,d) = (0, 0,353f, 0,235f, 0), die die neue Ebene anzeigt, die durch 0,353y + 0,235z = 0 beschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="5a6b0-139">Der Parameter pM enthält die umgekehrte Transponierung der Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-139">The parameter pM, contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="5a6b0-140">Die umgekehrte Transponieren ist für diese Methode erforderlich, damit auch der normale Vektor der transformierten Ebene ordnungsgemäß transformiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="5a6b0-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a6b0-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a6b0-141">Requirements</span></span>



| <span data-ttu-id="5a6b0-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a6b0-142">Requirement</span></span> | <span data-ttu-id="5a6b0-143">Wert</span><span class="sxs-lookup"><span data-stu-id="5a6b0-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a6b0-144">Header</span><span class="sxs-lookup"><span data-stu-id="5a6b0-144">Header</span></span><br/>  | <dl> <span data-ttu-id="5a6b0-145"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5a6b0-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="5a6b0-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5a6b0-146">Library</span></span><br/> | <dl> <span data-ttu-id="5a6b0-147"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a6b0-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a6b0-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5a6b0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a6b0-149">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="5a6b0-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
