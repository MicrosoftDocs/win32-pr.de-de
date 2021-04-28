---
description: 'D3DXMatrixRotationZ-Funktion (D3dx9math.h): Erstellt eine Matrix, die um die Z-Achse gedreht wird.'
ms.assetid: 73db43e6-3831-4867-8eda-80127b61e169
title: D3DXMatrixRotationZ-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0b109f71052657a5d9c32d9af5cb38b2cbcf1f0e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118108"
---
# <a name="d3dxmatrixrotationz-function-d3dx9mathh"></a><span data-ttu-id="afa48-103">D3DXMatrixRotationZ-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="afa48-103">D3DXMatrixRotationZ function (D3dx9math.h)</span></span>

<span data-ttu-id="afa48-104">Erstellt eine Matrix, die um die Z-Achse gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="afa48-104">Builds a matrix that rotates around the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="afa48-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="afa48-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="afa48-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="afa48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afa48-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="afa48-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="afa48-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="afa48-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="afa48-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="afa48-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="afa48-110">*Winkel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="afa48-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afa48-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="afa48-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="afa48-112">Drehwinkel im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="afa48-112">Angle of rotation, in radians.</span></span> <span data-ttu-id="afa48-113">Winkel werden im Uhrzeigersinn gemessen, wenn sie von der Drehachse (positive Seite) zum Ursprung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="afa48-113">Angles are measured clockwise when viewed from the rotation axis (positive side) toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afa48-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afa48-114">Return value</span></span>

<span data-ttu-id="afa48-115">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="afa48-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="afa48-116">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die um die Z-Achse gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="afa48-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the z-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="afa48-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afa48-117">Remarks</span></span>

<span data-ttu-id="afa48-118">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="afa48-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="afa48-119">Auf diese Weise kann die **D3DXMatrixRotationZ-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="afa48-119">In this way, the **D3DXMatrixRotationZ** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="afa48-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afa48-120">Requirements</span></span>



| <span data-ttu-id="afa48-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afa48-121">Requirement</span></span> | <span data-ttu-id="afa48-122">Wert</span><span class="sxs-lookup"><span data-stu-id="afa48-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="afa48-123">Header</span><span class="sxs-lookup"><span data-stu-id="afa48-123">Header</span></span><br/>  | <dl> <span data-ttu-id="afa48-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="afa48-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="afa48-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="afa48-125">Library</span></span><br/> | <dl> <span data-ttu-id="afa48-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="afa48-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="afa48-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="afa48-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afa48-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="afa48-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="afa48-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="afa48-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="afa48-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="afa48-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="afa48-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="afa48-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="afa48-132">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="afa48-132">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="afa48-133">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="afa48-133">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> </dl>

 

 
