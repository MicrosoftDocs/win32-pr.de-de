---
description: 'D3DXMatrixRotationY-Funktion (D3DX10Math.h): Erstellt eine Matrix, die um die y-Achse gedreht wird.'
ms.assetid: b58def9b-29dc-4c7d-89a3-188ef9b9f94f
title: D3DXMatrixRotationY-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 570179fadc9008c5f919acf657541e53ab399ac8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108968"
---
# <a name="d3dxmatrixrotationy-function-d3dx10mathh"></a><span data-ttu-id="70dbc-103">D3DXMatrixRotationY-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="70dbc-103">D3DXMatrixRotationY function (D3DX10Math.h)</span></span>

<span data-ttu-id="70dbc-104">Erstellt eine Matrix, die um die y-Achse gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="70dbc-104">Builds a matrix that rotates around the y-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="70dbc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="70dbc-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationY(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="70dbc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="70dbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70dbc-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="70dbc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="70dbc-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="70dbc-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="70dbc-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="70dbc-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="70dbc-110">*Winkel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="70dbc-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70dbc-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="70dbc-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="70dbc-112">Drehwinkel im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="70dbc-112">Angle of rotation in radians.</span></span> <span data-ttu-id="70dbc-113">Winkel werden im Uhrzeigersinn gemessen, wenn sie entlang der Drehachse zum Ursprung hin betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="70dbc-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70dbc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70dbc-114">Return value</span></span>

<span data-ttu-id="70dbc-115">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="70dbc-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="70dbc-116">Zeiger auf eine D3DXMATRIX-Struktur, die um die y-Achse gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="70dbc-116">Pointer to a D3DXMATRIX structure rotated around the y-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="70dbc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70dbc-117">Remarks</span></span>

<span data-ttu-id="70dbc-118">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="70dbc-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="70dbc-119">Auf diese Weise kann die D3DXMatrixRotationY-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="70dbc-119">In this way, the D3DXMatrixRotationY function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="70dbc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70dbc-120">Requirements</span></span>



| <span data-ttu-id="70dbc-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70dbc-121">Requirement</span></span> | <span data-ttu-id="70dbc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="70dbc-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70dbc-123">Header</span><span class="sxs-lookup"><span data-stu-id="70dbc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="70dbc-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="70dbc-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="70dbc-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="70dbc-125">Library</span></span><br/> | <dl> <span data-ttu-id="70dbc-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="70dbc-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="70dbc-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="70dbc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70dbc-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="70dbc-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
