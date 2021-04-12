---
description: Erstellt eine Quaternion aus einer Rotations Matrix.
ms.assetid: 316bf3e0-32ff-4e5e-b771-99f7eea2e27c
title: D3DXQuaternionRotationMatrix-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1caccf47e03388ffb85f2e12a5d0203f3fe839bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219652"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx10mathh"></a><span data-ttu-id="c8c66-103">D3DXQuaternionRotationMatrix-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="c8c66-103">D3DXQuaternionRotationMatrix function (D3DX10Math.h)</span></span>

<span data-ttu-id="c8c66-104">Erstellt eine Quaternion aus einer Rotations Matrix.</span><span class="sxs-lookup"><span data-stu-id="c8c66-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8c66-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8c66-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c8c66-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8c66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8c66-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c8c66-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c66-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8c66-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c8c66-109">Zeiger auf das [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="c8c66-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c8c66-110">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8c66-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c66-111">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8c66-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c8c66-112">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c8c66-112">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8c66-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8c66-113">Return value</span></span>

<span data-ttu-id="c8c66-114">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8c66-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c8c66-115">Ein Zeiger auf die D3DXQUATERNION-Struktur, die aus einer Rotations Matrix erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c8c66-115">Pointer to the D3DXQUATERNION structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8c66-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8c66-116">Remarks</span></span>

<span data-ttu-id="c8c66-117">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c8c66-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c8c66-118">Auf diese Weise kann die D3DXQuaternionRotationMatrix-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8c66-118">In this way, the D3DXQuaternionRotationMatrix function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c8c66-119">Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="c8c66-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8c66-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8c66-120">Requirements</span></span>



| <span data-ttu-id="c8c66-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8c66-121">Requirement</span></span> | <span data-ttu-id="c8c66-122">Wert</span><span class="sxs-lookup"><span data-stu-id="c8c66-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8c66-123">Header</span><span class="sxs-lookup"><span data-stu-id="c8c66-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c8c66-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8c66-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c8c66-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c8c66-125">Library</span></span><br/> | <dl> <span data-ttu-id="c8c66-126"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8c66-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c8c66-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8c66-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8c66-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c8c66-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
