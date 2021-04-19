---
description: Erstellt eine Rotations Matrix aus einer Quaternion.
ms.assetid: e590058c-772b-4eef-aab0-a12bb04c299a
title: D3DXMatrixRotationQuaternion-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationQuaternion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275a369da106e9f114ce47286f0f6ea9ce381ecb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367473"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx9mathh"></a><span data-ttu-id="25c16-103">D3DXMatrixRotationQuaternion-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="25c16-103">D3DXMatrixRotationQuaternion function (D3dx9math.h)</span></span>

<span data-ttu-id="25c16-104">Erstellt eine Rotations Matrix aus einer Quaternion.</span><span class="sxs-lookup"><span data-stu-id="25c16-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="25c16-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="25c16-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="25c16-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="25c16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25c16-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="25c16-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="25c16-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="25c16-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="25c16-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="25c16-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="25c16-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25c16-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25c16-111">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="25c16-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="25c16-112">Ein Zeiger auf die Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="25c16-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25c16-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25c16-113">Return value</span></span>

<span data-ttu-id="25c16-114">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="25c16-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="25c16-115">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die aus der Quell-Quaternion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="25c16-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="25c16-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25c16-116">Remarks</span></span>

<span data-ttu-id="25c16-117">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="25c16-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="25c16-118">Auf diese Weise kann die **D3DXMatrixRotationQuaternion** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25c16-118">In this way, the **D3DXMatrixRotationQuaternion** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="25c16-119">Informationen dazu, wie Sie Quaternion-Werte aus einem Richtungsvektor (x, y, z) und einem Drehwinkel berechnen, finden Sie unter [**D3DXQUATERNION**](d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="25c16-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25c16-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25c16-120">Requirements</span></span>



| <span data-ttu-id="25c16-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25c16-121">Requirement</span></span> | <span data-ttu-id="25c16-122">Wert</span><span class="sxs-lookup"><span data-stu-id="25c16-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25c16-123">Header</span><span class="sxs-lookup"><span data-stu-id="25c16-123">Header</span></span><br/>  | <dl> <span data-ttu-id="25c16-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="25c16-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="25c16-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="25c16-125">Library</span></span><br/> | <dl> <span data-ttu-id="25c16-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25c16-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="25c16-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25c16-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25c16-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="25c16-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="25c16-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="25c16-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="25c16-130">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="25c16-130">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="25c16-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="25c16-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="25c16-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="25c16-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="25c16-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="25c16-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 




