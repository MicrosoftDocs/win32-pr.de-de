---
description: 'D3DXMatrixRotationAxis-Funktion (D3dx9math.h): Erstellt eine Matrix, die um eine beliebige Achse gedreht wird.'
ms.assetid: 368c8f64-7709-4200-94d3-3dbc92a960c1
title: D3DXMatrixRotationAxis-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 720ac4d3bdae2910cee7913b9c34316d72526688
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118188"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="4d806-103">D3DXMatrixRotationAxis-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="4d806-103">D3DXMatrixRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="4d806-104">Erstellt eine Matrix, die um eine beliebige Achse gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="4d806-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d806-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d806-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="4d806-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d806-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d806-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4d806-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d806-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d806-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4d806-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="4d806-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4d806-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4d806-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d806-111">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d806-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="4d806-112">Zeiger auf die beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="4d806-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="4d806-113">Siehe [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="4d806-113">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d806-114">*Winkel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4d806-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d806-115">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4d806-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4d806-116">Drehwinkel im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="4d806-116">Angle of rotation in radians.</span></span> <span data-ttu-id="4d806-117">Winkel werden im Uhrzeigersinn gemessen, wenn sie entlang der Drehachse zum Ursprung hin betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="4d806-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d806-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d806-118">Return value</span></span>

<span data-ttu-id="4d806-119">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d806-119">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4d806-120">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die um die angegebene Achse gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="4d806-120">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d806-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d806-121">Remarks</span></span>

<span data-ttu-id="4d806-122">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="4d806-122">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4d806-123">Auf diese Weise kann die **D3DXMatrixRotationAxis-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d806-123">In this way, the **D3DXMatrixRotationAxis** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d806-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d806-124">Requirements</span></span>



| <span data-ttu-id="4d806-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d806-125">Requirement</span></span> | <span data-ttu-id="4d806-126">Wert</span><span class="sxs-lookup"><span data-stu-id="4d806-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d806-127">Header</span><span class="sxs-lookup"><span data-stu-id="4d806-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4d806-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="4d806-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4d806-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4d806-129">Library</span></span><br/> | <dl> <span data-ttu-id="4d806-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d806-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4d806-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4d806-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d806-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="4d806-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4d806-133">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="4d806-133">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="4d806-134">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="4d806-134">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="4d806-135">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="4d806-135">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="4d806-136">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="4d806-136">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="4d806-137">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="4d806-137">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
