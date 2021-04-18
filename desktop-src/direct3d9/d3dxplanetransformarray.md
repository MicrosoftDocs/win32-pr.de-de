---
description: Transformiert ein Array von Ebenen durch eine Matrix. Die Vektoren, die die einzelnen Ebenen beschreiben, müssen normalisiert werden.
ms.assetid: e82e830b-efbb-4bdc-b370-7bfa4326a669
title: D3DXPlaneTransformArray-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a9a213b17aca9999ef0028fdceb4bb4321d47660
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354346"
---
# <a name="d3dxplanetransformarray-function-d3dx9mathh"></a><span data-ttu-id="79775-104">D3DXPlaneTransformArray-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="79775-104">D3DXPlaneTransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="79775-105">Transformiert ein Array von Ebenen durch eine Matrix.</span><span class="sxs-lookup"><span data-stu-id="79775-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="79775-106">Die Vektoren, die die einzelnen Ebenen beschreiben, müssen normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="79775-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="79775-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="79775-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _Out_         UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a><span data-ttu-id="79775-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="79775-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79775-109">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="79775-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="79775-110">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="79775-110">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="79775-111">Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Struktur, die die resultierende transformierte Ebene enthält.</span><span class="sxs-lookup"><span data-stu-id="79775-111">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="79775-112">Siehe Beispiel.</span><span class="sxs-lookup"><span data-stu-id="79775-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="79775-113">*Outstride* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="79775-113">*OutStride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79775-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79775-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79775-115">Der Schritt der einzelnen transformierten Ebenen.</span><span class="sxs-lookup"><span data-stu-id="79775-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="79775-116">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79775-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79775-117">Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="79775-117">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="79775-118">Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Eingabe Struktur, die das zu transformierenden Array von Ebenen enthält.</span><span class="sxs-lookup"><span data-stu-id="79775-118">Pointer to the input [**D3DXPLANE**](d3dxplane.md) structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="79775-119">Der Vektor (a, b, c), der die Ebene beschreibt, muss normalisiert werden, bevor diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="79775-119">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="79775-120">Siehe Beispiel.</span><span class="sxs-lookup"><span data-stu-id="79775-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="79775-121">*Pstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79775-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79775-122">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79775-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79775-123">Der Stride der einzelnen nicht transformierten Ebenen.</span><span class="sxs-lookup"><span data-stu-id="79775-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="79775-124">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79775-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79775-125">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="79775-125">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="79775-126">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die umgekehrte Umwandlung der Transformations Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="79775-126">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="79775-127">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79775-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79775-128">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79775-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79775-129">Die Anzahl der zu transformierenden Ebenen.</span><span class="sxs-lookup"><span data-stu-id="79775-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79775-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79775-130">Return value</span></span>

<span data-ttu-id="79775-131">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="79775-131">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="79775-132">Zeiger auf eine [**D3DXPLANE**](d3dxplane.md) -Struktur, die die transformierte Ebene darstellt.</span><span class="sxs-lookup"><span data-stu-id="79775-132">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure, representing the transformed plane.</span></span> <span data-ttu-id="79775-133">Dabei handelt es sich um denselben Wert, der im *Pout* -Parameter zurückgegeben wird, sodass diese Funktion als Parameter für eine andere Funktion verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="79775-133">This is the same value returned in the *pOut* parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="79775-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79775-134">Remarks</span></span>

<span data-ttu-id="79775-135">In diesem Beispiel wird eine Ebene durch Anwenden einer nicht einheitlichen Skala transformiert.</span><span class="sxs-lookup"><span data-stu-id="79775-135">This example transforms one plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="79775-136">Eine Ebene wird von AX + by + CZ + DW = 0 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="79775-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="79775-137">Die erste Ebene wird mit (a, b, c, d) = (0, 1, 1, 0) erstellt. Dies ist eine Ebene, die von y + z = 0 beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="79775-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="79775-138">Nach dem Skalieren enthält die neue Ebene (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), die die neue Ebene anzeigt, die von 0.353 y + 0.235 z = 0 beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="79775-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="79775-139">Der-Parameter *pm* enthält die umgekehrte Umwandlung der Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="79775-139">The parameter *pM* contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="79775-140">Die umgekehrte Umwandlung ist für diese Methode erforderlich, damit der normale Vektor der transformierten Ebene ebenfalls ordnungsgemäß transformiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="79775-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="79775-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79775-141">Requirements</span></span>



| <span data-ttu-id="79775-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79775-142">Requirement</span></span> | <span data-ttu-id="79775-143">Wert</span><span class="sxs-lookup"><span data-stu-id="79775-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79775-144">Header</span><span class="sxs-lookup"><span data-stu-id="79775-144">Header</span></span><br/>  | <dl> <span data-ttu-id="79775-145"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="79775-145"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="79775-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="79775-146">Library</span></span><br/> | <dl> <span data-ttu-id="79775-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79775-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="79775-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79775-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79775-149">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="79775-149">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="79775-150">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="79775-150">**D3DXPlaneNormalize**</span></span>](d3dxplanenormalize.md)
</dt> <dt>

[<span data-ttu-id="79775-151">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="79775-151">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="79775-152">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="79775-152">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="79775-153">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="79775-153">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> <dt>

[<span data-ttu-id="79775-154">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="79775-154">**D3DXMatrixInverse**</span></span>](d3dxmatrixinverse.md)
</dt> <dt>

[<span data-ttu-id="79775-155">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="79775-155">**D3DXMatrixTranspose**</span></span>](d3dxmatrixtranspose.md)
</dt> </dl>

 

 
