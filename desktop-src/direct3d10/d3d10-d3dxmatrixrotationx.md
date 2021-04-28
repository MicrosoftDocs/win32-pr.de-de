---
description: 'D3DXMatrixRotationX-Funktion (D3DX10Math.h): Erstellt eine Matrix, die um die x-Achse gedreht wird.'
ms.assetid: 895079bf-b807-4bfd-9222-a7c1251d7d1e
title: D3DXMatrixRotationX-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationX
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 53c4bf27a359bd6d131f8d6d9c685e929d1a9ec1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108988"
---
# <a name="d3dxmatrixrotationx-function-d3dx10mathh"></a><span data-ttu-id="1c05d-103">D3DXMatrixRotationX-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="1c05d-103">D3DXMatrixRotationX function (D3DX10Math.h)</span></span>

<span data-ttu-id="1c05d-104">Erstellt eine Matrix, die um die X-Achse gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="1c05d-104">Builds a matrix that rotates around the x-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c05d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c05d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="1c05d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c05d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c05d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1c05d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c05d-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c05d-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1c05d-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="1c05d-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1c05d-110">*Winkel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1c05d-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c05d-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c05d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c05d-112">Drehwinkel im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="1c05d-112">Angle of rotation in radians.</span></span> <span data-ttu-id="1c05d-113">Winkel werden im Uhrzeigersinn gemessen, wenn sie entlang der Drehachse zum Ursprung hin betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="1c05d-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c05d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c05d-114">Return value</span></span>

<span data-ttu-id="1c05d-115">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c05d-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1c05d-116">Zeiger auf eine D3DXMATRIX-Struktur, die um die X-Achse gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="1c05d-116">Pointer to a D3DXMATRIX structure rotated around the x-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c05d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c05d-117">Remarks</span></span>

<span data-ttu-id="1c05d-118">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1c05d-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1c05d-119">Auf diese Weise kann die D3DXMatrixRotationX-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c05d-119">In this way, the D3DXMatrixRotationX function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c05d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c05d-120">Requirements</span></span>



| <span data-ttu-id="1c05d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c05d-121">Requirement</span></span> | <span data-ttu-id="1c05d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1c05d-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c05d-123">Header</span><span class="sxs-lookup"><span data-stu-id="1c05d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1c05d-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1c05d-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1c05d-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1c05d-125">Library</span></span><br/> | <dl> <span data-ttu-id="1c05d-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c05d-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1c05d-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1c05d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c05d-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1c05d-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
