---
description: 'D3DXQuaternionToAxisAngle-Funktion (D3DX10Math.h): Berechnet die Achse und den Drehwinkel einer Quaternion.'
ms.assetid: 1e81b88b-071d-46f1-b640-c70d063a14d1
title: D3DXQuaternionToAxisAngle-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 51f704aa839ff210b3c2de57767cb32ec609232f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108698"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx10mathh"></a><span data-ttu-id="7f611-103">D3DXQuaternionToAxisAngle-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="7f611-103">D3DXQuaternionToAxisAngle function (D3DX10Math.h)</span></span>

<span data-ttu-id="7f611-104">Berechnet die Achse und den Drehwinkel einer Quaternion.</span><span class="sxs-lookup"><span data-stu-id="7f611-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f611-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f611-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="7f611-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f611-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f611-107">*pQ* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7f611-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f611-108">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="7f611-108">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7f611-109">Zeiger auf die Quelle [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="7f611-109">Pointer to the source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f611-110">*pAxis* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7f611-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f611-111">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f611-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7f611-112">Diese Funktion gibt einen Zeiger auf einen [**D3DXVECTOR3**](d3d10-d3dxvector3.md) zurück, der die Drehachse der Quaternion identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7f611-112">This function returns a pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="7f611-113">*pAngle* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7f611-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f611-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7f611-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7f611-115">Diese Funktion gibt einen Zeiger auf einen FLOAT-Wert zurück, der den Drehwinkel der Quaternion im Bogenmaß identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7f611-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f611-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f611-116">Return value</span></span>

<span data-ttu-id="7f611-117">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="7f611-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f611-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f611-118">Remarks</span></span>

<span data-ttu-id="7f611-119">Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die nicht bereits normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="7f611-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f611-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f611-120">Requirements</span></span>



| <span data-ttu-id="7f611-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f611-121">Requirement</span></span> | <span data-ttu-id="7f611-122">Wert</span><span class="sxs-lookup"><span data-stu-id="7f611-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f611-123">Header</span><span class="sxs-lookup"><span data-stu-id="7f611-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7f611-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="7f611-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="7f611-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7f611-125">Library</span></span><br/> | <dl> <span data-ttu-id="7f611-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f611-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7f611-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7f611-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f611-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="7f611-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
