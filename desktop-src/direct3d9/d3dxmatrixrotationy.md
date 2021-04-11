---
description: Erstellt eine Matrix, die um die y-Achse rotiert.
ms.assetid: 80449e5d-f9bb-48c0-a787-a5e5a9d1c9a3
title: D3DXMatrixRotationY-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81e233f3d643e99c829c7d567721e52b9b5d3e82
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355407"
---
# <a name="d3dxmatrixrotationy-function-d3dx9mathh"></a><span data-ttu-id="8c5cf-103">D3DXMatrixRotationY-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8c5cf-103">D3DXMatrixRotationY function (D3dx9math.h)</span></span>

<span data-ttu-id="8c5cf-104">Erstellt eine Matrix, die um die y-Achse rotiert.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-104">Builds a matrix that rotates around the y-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c5cf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c5cf-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationY(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="8c5cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c5cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c5cf-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8c5cf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c5cf-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c5cf-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8c5cf-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8c5cf-110">*Winkel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c5cf-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c5cf-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8c5cf-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8c5cf-112">Winkel der Drehung im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-112">Angle of rotation in radians.</span></span> <span data-ttu-id="8c5cf-113">Winkel werden im Uhrzeigersinn gemessen, wenn Sie entlang der Drehungs Achse zum Ursprung suchen.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-113">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c5cf-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c5cf-114">Return value</span></span>

<span data-ttu-id="8c5cf-115">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8c5cf-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8c5cf-116">Ein Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die um die y-Achse gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the y-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c5cf-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c5cf-117">Remarks</span></span>

<span data-ttu-id="8c5cf-118">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8c5cf-119">Auf diese Weise kann die **D3DXMatrixRotationY** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c5cf-119">In this way, the **D3DXMatrixRotationY** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c5cf-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c5cf-120">Requirements</span></span>



| <span data-ttu-id="8c5cf-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c5cf-121">Requirement</span></span> | <span data-ttu-id="8c5cf-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8c5cf-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c5cf-123">Header</span><span class="sxs-lookup"><span data-stu-id="8c5cf-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8c5cf-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c5cf-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8c5cf-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8c5cf-125">Library</span></span><br/> | <dl> <span data-ttu-id="8c5cf-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c5cf-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8c5cf-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c5cf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c5cf-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="8c5cf-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8c5cf-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="8c5cf-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="8c5cf-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="8c5cf-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="8c5cf-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="8c5cf-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="8c5cf-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="8c5cf-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="8c5cf-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="8c5cf-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
