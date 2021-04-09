---
description: Erstellt eine Matrix, die um eine beliebige Achse rotiert.
ms.assetid: dc4b8b3f-e1d2-475f-9dcb-622ada9fae6b
title: D3DXMatrixRotationAxis-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: bba74aa7258b39b8fdbbb8cab09684a14bfbda91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050916"
---
# <a name="d3dxmatrixrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="26e23-103">D3DXMatrixRotationAxis-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="26e23-103">D3DXMatrixRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="26e23-104">Erstellt eine Matrix, die um eine beliebige Achse rotiert.</span><span class="sxs-lookup"><span data-stu-id="26e23-104">Builds a matrix that rotates around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="26e23-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="26e23-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationAxis(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="26e23-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="26e23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26e23-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="26e23-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="26e23-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="26e23-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="26e23-109">Ein Zeiger auf die [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="26e23-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="26e23-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26e23-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26e23-111">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="26e23-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="26e23-112">Zeiger auf die beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="26e23-112">Pointer to the arbitrary axis.</span></span> <span data-ttu-id="26e23-113">Siehe [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="26e23-113">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="26e23-114">*Winkel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26e23-114">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26e23-115">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26e23-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26e23-116">Winkel der Drehung im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="26e23-116">Angle of rotation in radians.</span></span> <span data-ttu-id="26e23-117">Winkel werden im Uhrzeigersinn gemessen, wenn Sie entlang der Drehungs Achse zum Ursprung suchen.</span><span class="sxs-lookup"><span data-stu-id="26e23-117">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26e23-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26e23-118">Return value</span></span>

<span data-ttu-id="26e23-119">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="26e23-119">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="26e23-120">Ein Zeiger auf eine D3DXMATRIX-Struktur, gedreht um die angegebene Achse.</span><span class="sxs-lookup"><span data-stu-id="26e23-120">Pointer to a D3DXMATRIX structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="26e23-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26e23-121">Remarks</span></span>

<span data-ttu-id="26e23-122">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="26e23-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="26e23-123">Auf diese Weise kann die D3DXMatrixRotationAxis-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26e23-123">In this way, the D3DXMatrixRotationAxis function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="26e23-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26e23-124">Requirements</span></span>



| <span data-ttu-id="26e23-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26e23-125">Requirement</span></span> | <span data-ttu-id="26e23-126">Wert</span><span class="sxs-lookup"><span data-stu-id="26e23-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26e23-127">Header</span><span class="sxs-lookup"><span data-stu-id="26e23-127">Header</span></span><br/>  | <dl> <span data-ttu-id="26e23-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="26e23-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="26e23-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="26e23-129">Library</span></span><br/> | <dl> <span data-ttu-id="26e23-130"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26e23-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="26e23-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26e23-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e23-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="26e23-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
