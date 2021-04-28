---
description: 'D3DXMatrixRotationAxis-Funktion (D3DX10Math.h): Erstellt eine Matrix, die um eine beliebige Achse gedreht wird.'
ms.assetid: dc4b8b3f-e1d2-475f-9dcb-622ada9fae6b
title: D3DXMatrixRotationAxis-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationAxis
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8ea5b8b0a40e876af454daa8915c0e455d691d08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108998"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="05559-103">D3DXMatrixRotationAxis-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="05559-103">D3DXMatrixRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="05559-104">Erstellt eine Matrix, die um eine beliebige Achse gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="05559-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="05559-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="05559-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="05559-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="05559-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05559-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="05559-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="05559-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="05559-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="05559-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="05559-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="05559-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="05559-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05559-111">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="05559-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="05559-112">Zeiger auf die beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="05559-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="05559-113">Siehe [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="05559-113">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="05559-114">*Winkel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="05559-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05559-115">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="05559-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="05559-116">Drehwinkel im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="05559-116">Angle of rotation in radians.</span></span> <span data-ttu-id="05559-117">Winkel werden im Uhrzeigersinn gemessen, wenn sie entlang der Drehachse zum Ursprung hin betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="05559-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05559-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05559-118">Return value</span></span>

<span data-ttu-id="05559-119">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="05559-119">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="05559-120">Zeiger auf eine D3DXMATRIX-Struktur, die um die angegebene Achse gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="05559-120">Pointer to a D3DXMATRIX structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="05559-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05559-121">Remarks</span></span>

<span data-ttu-id="05559-122">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="05559-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="05559-123">Auf diese Weise kann die D3DXMatrixRotationAxis-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05559-123">In this way, the D3DXMatrixRotationAxis function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="05559-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05559-124">Requirements</span></span>



| <span data-ttu-id="05559-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05559-125">Requirement</span></span> | <span data-ttu-id="05559-126">Wert</span><span class="sxs-lookup"><span data-stu-id="05559-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05559-127">Header</span><span class="sxs-lookup"><span data-stu-id="05559-127">Header</span></span><br/>  | <dl> <span data-ttu-id="05559-128"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="05559-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="05559-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="05559-129">Library</span></span><br/> | <dl> <span data-ttu-id="05559-130"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="05559-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="05559-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="05559-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05559-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="05559-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
