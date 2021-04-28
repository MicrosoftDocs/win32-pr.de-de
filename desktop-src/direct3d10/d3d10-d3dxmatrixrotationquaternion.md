---
description: 'D3DXMatrixRotationQuaternion-Funktion (D3DX10Math.h): Erstellt eine Rotationsmatrix aus einer Quaternion.'
ms.assetid: dcbf8696-b959-4475-a250-6094dd5fe358
title: D3DXMatrixRotationQuaternion-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 7d95d28b7f7106df9ddfb43a9175f5c19292d52c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103428"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx10mathh"></a><span data-ttu-id="4c8f9-103">D3DXMatrixRotationQuaternion-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="4c8f9-103">D3DXMatrixRotationQuaternion function (D3DX10Math.h)</span></span>

<span data-ttu-id="4c8f9-104">Erstellt eine Rotationsmatrix aus einer Quaternion.</span><span class="sxs-lookup"><span data-stu-id="4c8f9-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c8f9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c8f9-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="4c8f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c8f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c8f9-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4c8f9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c8f9-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c8f9-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4c8f9-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="4c8f9-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4c8f9-110">*pQ* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4c8f9-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c8f9-111">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4c8f9-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4c8f9-112">Zeiger auf die D3DXQUATERNION-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="4c8f9-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c8f9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c8f9-113">Return value</span></span>

<span data-ttu-id="4c8f9-114">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c8f9-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="4c8f9-115">Zeiger auf eine D3DXMATRIX-Struktur, die aus der Quellquaternion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4c8f9-115">Pointer to a D3DXMATRIX structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c8f9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c8f9-116">Remarks</span></span>

<span data-ttu-id="4c8f9-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4c8f9-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="4c8f9-118">Auf diese Weise kann die D3DXMatrixRotationQuaternion-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c8f9-118">In this way, the D3DXMatrixRotationQuaternion function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4c8f9-119">Informationen zum Berechnen von Quaternionwerten aus einem Richtungsvektor ( x, y, z ) und einem Drehwinkel finden Sie unter [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="4c8f9-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c8f9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c8f9-120">Requirements</span></span>



| <span data-ttu-id="4c8f9-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c8f9-121">Requirement</span></span> | <span data-ttu-id="4c8f9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4c8f9-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c8f9-123">Header</span><span class="sxs-lookup"><span data-stu-id="4c8f9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4c8f9-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="4c8f9-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4c8f9-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4c8f9-125">Library</span></span><br/> | <dl> <span data-ttu-id="4c8f9-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c8f9-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4c8f9-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4c8f9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c8f9-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="4c8f9-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
