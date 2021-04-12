---
description: Erstellt eine Matrix, die um die z-Achse rotiert.
ms.assetid: a168ea24-0cec-4e1b-a128-e9dadedf190b
title: D3DXMatrixRotationZ-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 3dfe1d3d43e4110c4e7554c75fba3ac89a69ccb3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219654"
---
# <a name="d3dxmatrixrotationz-function-d3dx10mathh"></a><span data-ttu-id="ae774-103">D3DXMatrixRotationZ-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="ae774-103">D3DXMatrixRotationZ function (D3DX10Math.h)</span></span>

<span data-ttu-id="ae774-104">Erstellt eine Matrix, die um die z-Achse rotiert.</span><span class="sxs-lookup"><span data-stu-id="ae774-104">Builds a matrix that rotates around the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae774-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae774-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="ae774-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae774-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae774-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ae774-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae774-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ae774-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ae774-109">Ein Zeiger auf die [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="ae774-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ae774-110">*Winkel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae774-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae774-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae774-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae774-112">Winkel der Drehung im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="ae774-112">Angle of rotation, in radians.</span></span> <span data-ttu-id="ae774-113">Winkel werden im Uhrzeigersinn gemessen, wenn Sie von der Drehungs Achse (positive Seite) bis zum Ursprung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ae774-113">Angles are measured clockwise when viewed from the rotation axis (positive side) toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae774-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae774-114">Return value</span></span>

<span data-ttu-id="ae774-115">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ae774-115">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ae774-116">Ein Zeiger auf eine D3DXMATRIX-Struktur, gedreht um die z-Achse.</span><span class="sxs-lookup"><span data-stu-id="ae774-116">Pointer to a D3DXMATRIX structure rotated around the z-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae774-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae774-117">Remarks</span></span>

<span data-ttu-id="ae774-118">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ae774-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ae774-119">Auf diese Weise kann die D3DXMatrixRotationZ-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae774-119">In this way, the D3DXMatrixRotationZ function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae774-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae774-120">Requirements</span></span>



| <span data-ttu-id="ae774-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae774-121">Requirement</span></span> | <span data-ttu-id="ae774-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ae774-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae774-123">Header</span><span class="sxs-lookup"><span data-stu-id="ae774-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ae774-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae774-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="ae774-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ae774-125">Library</span></span><br/> | <dl> <span data-ttu-id="ae774-126"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae774-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ae774-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae774-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae774-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ae774-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
