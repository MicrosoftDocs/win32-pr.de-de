---
description: 'D3DXMatrixRotationZ-Funktion (D3DX10Math.h): Erstellt eine Matrix, die um die Z-Achse gedreht wird.'
ms.assetid: a168ea24-0cec-4e1b-a128-e9dadedf190b
title: D3DXMatrixRotationZ-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationZ
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b952e310dd463d07a35fb294c4a50168361658a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108938"
---
# <a name="d3dxmatrixrotationz-function-d3dx10mathh"></a><span data-ttu-id="fcd29-103">D3DXMatrixRotationZ-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="fcd29-103">D3DXMatrixRotationZ function (D3DX10Math.h)</span></span>

<span data-ttu-id="fcd29-104">Erstellt eine Matrix, die um die Z-Achse gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="fcd29-104">Builds a matrix that rotates around the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcd29-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcd29-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="fcd29-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcd29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcd29-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fcd29-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcd29-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fcd29-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fcd29-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="fcd29-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fcd29-110">*Winkel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fcd29-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcd29-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcd29-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcd29-112">Drehwinkel im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="fcd29-112">Angle of rotation, in radians.</span></span> <span data-ttu-id="fcd29-113">Winkel werden im Uhrzeigersinn gemessen, wenn sie von der Drehachse (positive Seite) zum Ursprung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fcd29-113">Angles are measured clockwise when viewed from the rotation axis (positive side) toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcd29-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fcd29-114">Return value</span></span>

<span data-ttu-id="fcd29-115">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fcd29-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fcd29-116">Zeiger auf eine D3DXMATRIX-Struktur, die um die Z-Achse gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="fcd29-116">Pointer to a D3DXMATRIX structure rotated around the z-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcd29-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcd29-117">Remarks</span></span>

<span data-ttu-id="fcd29-118">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fcd29-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="fcd29-119">Auf diese Weise kann die D3DXMatrixRotationZ-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcd29-119">In this way, the D3DXMatrixRotationZ function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcd29-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fcd29-120">Requirements</span></span>



| <span data-ttu-id="fcd29-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fcd29-121">Requirement</span></span> | <span data-ttu-id="fcd29-122">Wert</span><span class="sxs-lookup"><span data-stu-id="fcd29-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd29-123">Header</span><span class="sxs-lookup"><span data-stu-id="fcd29-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fcd29-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="fcd29-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="fcd29-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fcd29-125">Library</span></span><br/> | <dl> <span data-ttu-id="fcd29-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcd29-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fcd29-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fcd29-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcd29-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="fcd29-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
