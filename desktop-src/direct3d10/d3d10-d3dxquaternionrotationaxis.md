---
description: Dreht eine Quaternion über eine beliebige Achse.
ms.assetid: 9673ef89-458f-4a25-960e-8f03179e78ba
title: D3DXQuaternionRotationAxis-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 739f128ca1a56eed15ebc2528036875eaf2bb9b8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370455"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx10mathh"></a><span data-ttu-id="67fe5-103">D3DXQuaternionRotationAxis-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="67fe5-103">D3DXQuaternionRotationAxis function (D3DX10Math.h)</span></span>

<span data-ttu-id="67fe5-104">Dreht eine Quaternion über eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="67fe5-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="67fe5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="67fe5-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="67fe5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="67fe5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67fe5-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="67fe5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="67fe5-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="67fe5-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="67fe5-109">Zeiger auf das [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="67fe5-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="67fe5-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67fe5-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67fe5-111">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="67fe5-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="67fe5-112">Ein Zeiger auf den [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , der die Achse identifiziert, für die die Quaternion gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="67fe5-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="67fe5-113">*Winkel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67fe5-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67fe5-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="67fe5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="67fe5-115">Winkel der Drehung im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="67fe5-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="67fe5-116">Winkel werden im Uhrzeigersinn gemessen, wenn Sie entlang der Drehungs Achse zum Ursprung suchen.</span><span class="sxs-lookup"><span data-stu-id="67fe5-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67fe5-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67fe5-117">Return value</span></span>

<span data-ttu-id="67fe5-118">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="67fe5-118">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="67fe5-119">Ein Zeiger auf eine D3DXQUATERNION-Struktur, gedreht um die angegebene Achse.</span><span class="sxs-lookup"><span data-stu-id="67fe5-119">Pointer to a D3DXQUATERNION structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="67fe5-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67fe5-120">Remarks</span></span>

<span data-ttu-id="67fe5-121">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="67fe5-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="67fe5-122">Auf diese Weise kann die D3DXQuaternionRotationAxis-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67fe5-122">In this way, the D3DXQuaternionRotationAxis function can be used as a parameter for another function.</span></span>

<span data-ttu-id="67fe5-123">Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="67fe5-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="67fe5-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67fe5-124">Requirements</span></span>



| <span data-ttu-id="67fe5-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67fe5-125">Requirement</span></span> | <span data-ttu-id="67fe5-126">Wert</span><span class="sxs-lookup"><span data-stu-id="67fe5-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67fe5-127">Header</span><span class="sxs-lookup"><span data-stu-id="67fe5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="67fe5-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="67fe5-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="67fe5-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="67fe5-129">Library</span></span><br/> | <dl> <span data-ttu-id="67fe5-130"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67fe5-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="67fe5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67fe5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67fe5-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="67fe5-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
