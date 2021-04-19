---
description: Erstellt eine Matrix, die um die x-Achse rotiert.
ms.assetid: 895079bf-b807-4bfd-9222-a7c1251d7d1e
title: D3DXMatrixRotationX-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 5eade695a3b410877665557bd42d61d1d89b18e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370456"
---
# <a name="d3dxmatrixrotationx-function-d3dx10mathh"></a><span data-ttu-id="1fdb2-103">D3DXMatrixRotationX-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="1fdb2-103">D3DXMatrixRotationX function (D3DX10Math.h)</span></span>

<span data-ttu-id="1fdb2-104">Erstellt eine Matrix, die um die x-Achse rotiert.</span><span class="sxs-lookup"><span data-stu-id="1fdb2-104">Builds a matrix that rotates around the x-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fdb2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fdb2-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationX(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="1fdb2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fdb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fdb2-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1fdb2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fdb2-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1fdb2-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1fdb2-109">Ein Zeiger auf die [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="1fdb2-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1fdb2-110">*Winkel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1fdb2-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fdb2-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fdb2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fdb2-112">Winkel der Drehung im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="1fdb2-112">Angle of rotation in radians.</span></span> <span data-ttu-id="1fdb2-113">Winkel werden im Uhrzeigersinn gemessen, wenn Sie entlang der Drehungs Achse zum Ursprung suchen.</span><span class="sxs-lookup"><span data-stu-id="1fdb2-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fdb2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1fdb2-114">Return value</span></span>

<span data-ttu-id="1fdb2-115">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1fdb2-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1fdb2-116">Zeiger auf eine D3DXMATRIX-Struktur, gedreht um die x-Achse.</span><span class="sxs-lookup"><span data-stu-id="1fdb2-116">Pointer to a D3DXMATRIX structure rotated around the x-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fdb2-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1fdb2-117">Remarks</span></span>

<span data-ttu-id="1fdb2-118">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1fdb2-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1fdb2-119">Auf diese Weise kann die D3DXMatrixRotationX-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1fdb2-119">In this way, the D3DXMatrixRotationX function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fdb2-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fdb2-120">Requirements</span></span>



| <span data-ttu-id="1fdb2-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fdb2-121">Requirement</span></span> | <span data-ttu-id="1fdb2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1fdb2-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fdb2-123">Header</span><span class="sxs-lookup"><span data-stu-id="1fdb2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1fdb2-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fdb2-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1fdb2-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1fdb2-125">Library</span></span><br/> | <dl> <span data-ttu-id="1fdb2-126"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fdb2-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1fdb2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fdb2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fdb2-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1fdb2-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
