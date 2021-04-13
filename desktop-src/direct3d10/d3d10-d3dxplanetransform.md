---
description: Transformiert eine Ebene um eine Matrix. Die Eingabe Matrix ist die umgekehrte Umwandlung der eigentlichen Transformation.
ms.assetid: ded06eac-4086-47e8-bc55-c37959afc22d
title: D3DXPlaneTransform-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 1b3c3390d84cd0d9c876afac6243ab90ca515e11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355596"
---
# <a name="d3dxplanetransform-function-d3dx10mathh"></a><span data-ttu-id="2e99b-104">D3DXPlaneTransform-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="2e99b-104">D3DXPlaneTransform function (D3DX10Math.h)</span></span>

<span data-ttu-id="2e99b-105">Transformiert eine Ebene um eine Matrix.</span><span class="sxs-lookup"><span data-stu-id="2e99b-105">Transforms a plane by a matrix.</span></span> <span data-ttu-id="2e99b-106">Die Eingabe Matrix ist die umgekehrte Umwandlung der eigentlichen Transformation.</span><span class="sxs-lookup"><span data-stu-id="2e99b-106">The input matrix is the inverse transpose of the actual transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e99b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e99b-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="2e99b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e99b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e99b-109">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2e99b-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e99b-110">Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e99b-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="2e99b-111">Zeiger auf den [**D3DXPLANE**](d3d10-d3dxplane.md) , der die resultierende transformierte Ebene enthält.</span><span class="sxs-lookup"><span data-stu-id="2e99b-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that contains the resulting transformed plane.</span></span> <span data-ttu-id="2e99b-112">Weitere Informationen sind im Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="2e99b-112">See example.</span></span>

</dd> <dt>

<span data-ttu-id="2e99b-113">*PP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e99b-113">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e99b-114">Typ: **Konstanten [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="2e99b-114">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="2e99b-115">Ein Zeiger auf die Eingabe D3DXPLANE-Struktur, die die zu transformierende Ebene enthält.</span><span class="sxs-lookup"><span data-stu-id="2e99b-115">Pointer to the input D3DXPLANE structure, which contains the plane that will be transformed.</span></span> <span data-ttu-id="2e99b-116">Der Vektor (a, b, c), der die Ebene beschreibt, muss normalisiert werden, bevor diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2e99b-116">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="2e99b-117">Weitere Informationen sind im Beispiel enthalten.</span><span class="sxs-lookup"><span data-stu-id="2e99b-117">See example.</span></span>

</dd> <dt>

<span data-ttu-id="2e99b-118">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e99b-118">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e99b-119">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2e99b-119">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2e99b-120">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die die Transformations Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="2e99b-120">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the transformation values.</span></span> <span data-ttu-id="2e99b-121">Diese Matrix muss die umgekehrte Umwandlung der Transformations Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="2e99b-121">This matrix must contain the inverse transpose of the transformation values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e99b-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e99b-122">Return value</span></span>

<span data-ttu-id="2e99b-123">Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e99b-123">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="2e99b-124">Zeiger auf eine D3DXPLANE-Struktur, die die transformierte Ebene darstellt.</span><span class="sxs-lookup"><span data-stu-id="2e99b-124">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="2e99b-125">Dabei handelt es sich um denselben Wert, der im Pout-Parameter zurückgegeben wird, sodass diese Funktion als Parameter für eine andere Funktion verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2e99b-125">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e99b-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e99b-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="2e99b-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e99b-127">Examples</span></span>

<span data-ttu-id="2e99b-128">In diesem Beispiel wird eine Ebene durch Anwenden einer nicht einheitlichen Skala transformiert.</span><span class="sxs-lookup"><span data-stu-id="2e99b-128">This example transforms a plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="2e99b-129">Eine Ebene wird von AX + by + CZ + DW = 0 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2e99b-129">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="2e99b-130">Die erste Ebene wird mit (a, b, c, d) = (0, 1, 1, 0) erstellt. Dies ist eine Ebene, die von y + z = 0 beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="2e99b-130">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="2e99b-131">Nach dem Skalieren enthält die neue Ebene (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), die die neue Ebene anzeigt, die von 0.353 y + 0.235 z = 0 beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="2e99b-131">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="2e99b-132">Der-Parameter pm enthält die umgekehrte Umwandlung der Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="2e99b-132">The parameter pM contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="2e99b-133">Die umgekehrte Umwandlung ist für diese Methode erforderlich, damit der normale Vektor der transformierten Ebene ebenfalls ordnungsgemäß transformiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2e99b-133">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e99b-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e99b-134">Requirements</span></span>



| <span data-ttu-id="2e99b-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e99b-135">Requirement</span></span> | <span data-ttu-id="2e99b-136">Wert</span><span class="sxs-lookup"><span data-stu-id="2e99b-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e99b-137">Header</span><span class="sxs-lookup"><span data-stu-id="2e99b-137">Header</span></span><br/>  | <dl> <span data-ttu-id="2e99b-138"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e99b-138"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2e99b-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2e99b-139">Library</span></span><br/> | <dl> <span data-ttu-id="2e99b-140"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e99b-140"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2e99b-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e99b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e99b-142">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2e99b-142">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
