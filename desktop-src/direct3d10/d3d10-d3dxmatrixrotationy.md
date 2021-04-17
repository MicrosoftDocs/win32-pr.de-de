---
description: Erstellt eine Matrix, die um die y-Achse rotiert.
ms.assetid: b58def9b-29dc-4c7d-89a3-188ef9b9f94f
title: D3DXMatrixRotationY-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationY
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1ae6c0be4e9e53b62a0504997bfd4687fa3fcab5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531034"
---
# <a name="d3dxmatrixrotationy-function-d3dx10mathh"></a><span data-ttu-id="792be-103">D3DXMatrixRotationY-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="792be-103">D3DXMatrixRotationY function (D3DX10Math.h)</span></span>

<span data-ttu-id="792be-104">Erstellt eine Matrix, die um die y-Achse rotiert.</span><span class="sxs-lookup"><span data-stu-id="792be-104">Builds a matrix that rotates around the y-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="792be-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="792be-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationY(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="792be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="792be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="792be-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="792be-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="792be-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="792be-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="792be-109">Ein Zeiger auf die [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="792be-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="792be-110">*Winkel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="792be-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="792be-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="792be-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="792be-112">Winkel der Drehung im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="792be-112">Angle of rotation in radians.</span></span> <span data-ttu-id="792be-113">Winkel werden im Uhrzeigersinn gemessen, wenn Sie entlang der Drehungs Achse zum Ursprung suchen.</span><span class="sxs-lookup"><span data-stu-id="792be-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="792be-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="792be-114">Return value</span></span>

<span data-ttu-id="792be-115">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="792be-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="792be-116">Ein Zeiger auf eine D3DXMATRIX-Struktur, die um die y-Achse gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="792be-116">Pointer to a D3DXMATRIX structure rotated around the y-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="792be-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="792be-117">Remarks</span></span>

<span data-ttu-id="792be-118">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="792be-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="792be-119">Auf diese Weise kann die D3DXMatrixRotationY-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="792be-119">In this way, the D3DXMatrixRotationY function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="792be-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="792be-120">Requirements</span></span>



| <span data-ttu-id="792be-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="792be-121">Requirement</span></span> | <span data-ttu-id="792be-122">Wert</span><span class="sxs-lookup"><span data-stu-id="792be-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="792be-123">Header</span><span class="sxs-lookup"><span data-stu-id="792be-123">Header</span></span><br/>  | <dl> <span data-ttu-id="792be-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="792be-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="792be-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="792be-125">Library</span></span><br/> | <dl> <span data-ttu-id="792be-126"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="792be-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="792be-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="792be-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="792be-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="792be-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
