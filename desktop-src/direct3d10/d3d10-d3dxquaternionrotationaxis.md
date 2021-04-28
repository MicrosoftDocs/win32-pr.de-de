---
description: 'D3DXQuaternionRotationAxis-Funktion (D3DX10Math.h): Rotiert eine Quaternion um eine beliebige Achse.'
ms.assetid: 9673ef89-458f-4a25-960e-8f03179e78ba
title: D3DXQuaternionRotationAxis-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationAxis
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 509df80023427a20125e1b5603e85424851a640e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108768"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="b66dc-103">D3DXQuaternionRotationAxis-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="b66dc-103">D3DXQuaternionRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="b66dc-104">Dreht eine Quaternion um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="b66dc-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="b66dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b66dc-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="b66dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b66dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b66dc-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b66dc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b66dc-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="b66dc-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b66dc-109">Zeiger auf das [**D3DXQUATERNION-Steuerelement,**](d3d10-d3dxquaternion.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="b66dc-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b66dc-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b66dc-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b66dc-111">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b66dc-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b66dc-112">Zeiger auf [**D3DXVECTOR3,**](d3d10-d3dxvector3.md) der die Achse identifiziert, um die die Quaternion gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b66dc-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="b66dc-113">*Winkel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b66dc-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b66dc-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b66dc-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b66dc-115">Drehwinkel im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="b66dc-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="b66dc-116">Winkel werden im Uhrzeigersinn gemessen, wenn sie entlang der Drehachse zum Ursprung hin betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="b66dc-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b66dc-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b66dc-117">Return value</span></span>

<span data-ttu-id="b66dc-118">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="b66dc-118">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b66dc-119">Zeiger auf eine D3DXQUATERNION-Struktur, die um die angegebene Achse gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="b66dc-119">Pointer to a D3DXQUATERNION structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="b66dc-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b66dc-120">Remarks</span></span>

<span data-ttu-id="b66dc-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b66dc-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b66dc-122">Auf diese Weise kann die D3DXQuaternionRotationAxis-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b66dc-122">In this way, the D3DXQuaternionRotationAxis function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b66dc-123">Verwenden [**Sie D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="b66dc-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="b66dc-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b66dc-124">Requirements</span></span>



| <span data-ttu-id="b66dc-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b66dc-125">Requirement</span></span> | <span data-ttu-id="b66dc-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b66dc-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b66dc-127">Header</span><span class="sxs-lookup"><span data-stu-id="b66dc-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b66dc-128"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="b66dc-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b66dc-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b66dc-129">Library</span></span><br/> | <dl> <span data-ttu-id="b66dc-130"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b66dc-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b66dc-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b66dc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b66dc-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="b66dc-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
