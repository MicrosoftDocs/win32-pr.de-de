---
description: Erstellt eine Rotations Matrix aus einer Quaternion.
ms.assetid: dcbf8696-b959-4475-a250-6094dd5fe358
title: D3DXMatrixRotationQuaternion-Funktion (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 44cd4a5982b322c2d207263fb490c898ed9fa76e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355223"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx10mathh"></a><span data-ttu-id="f207f-103">D3DXMatrixRotationQuaternion-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f207f-103">D3DXMatrixRotationQuaternion function (D3DX10Math.h)</span></span>

<span data-ttu-id="f207f-104">Erstellt eine Rotations Matrix aus einer Quaternion.</span><span class="sxs-lookup"><span data-stu-id="f207f-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="f207f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f207f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="f207f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f207f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f207f-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f207f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f207f-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f207f-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f207f-109">Ein Zeiger auf die [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="f207f-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f207f-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f207f-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f207f-111">Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f207f-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f207f-112">Ein Zeiger auf die Quell-D3DXQUATERNION-Struktur.</span><span class="sxs-lookup"><span data-stu-id="f207f-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f207f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f207f-113">Return value</span></span>

<span data-ttu-id="f207f-114">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f207f-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f207f-115">Zeiger auf eine D3DXMATRIX-Struktur, die aus der Quell-Quaternion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f207f-115">Pointer to a D3DXMATRIX structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="f207f-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f207f-116">Remarks</span></span>

<span data-ttu-id="f207f-117">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f207f-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f207f-118">Auf diese Weise kann die D3DXMatrixRotationQuaternion-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f207f-118">In this way, the D3DXMatrixRotationQuaternion function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f207f-119">Informationen dazu, wie Sie Quaternion-Werte aus einem Richtungsvektor (x, y, z) und einem Drehwinkel berechnen, finden Sie unter [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="f207f-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f207f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f207f-120">Requirements</span></span>



| <span data-ttu-id="f207f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f207f-121">Requirement</span></span> | <span data-ttu-id="f207f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f207f-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f207f-123">Header</span><span class="sxs-lookup"><span data-stu-id="f207f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f207f-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f207f-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f207f-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f207f-125">Library</span></span><br/> | <dl> <span data-ttu-id="f207f-126"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f207f-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f207f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f207f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f207f-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="f207f-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
