---
description: Dreht eine Quaternion über eine beliebige Achse.
ms.assetid: 9ff0fe2c-54d6-482c-84e1-f38e3c57d8dd
title: D3DXQuaternionRotationAxis-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7974a1199c468ac762042ae41af59f5a3b66bafd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373506"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="36ff5-103">D3DXQuaternionRotationAxis-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="36ff5-103">D3DXQuaternionRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="36ff5-104">Dreht eine Quaternion über eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="36ff5-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="36ff5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="36ff5-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="36ff5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="36ff5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36ff5-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="36ff5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="36ff5-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="36ff5-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="36ff5-109">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="36ff5-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="36ff5-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36ff5-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36ff5-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="36ff5-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="36ff5-112">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Achse identifiziert, für die die Quaternion gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="36ff5-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="36ff5-113">*Winkel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36ff5-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36ff5-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36ff5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36ff5-115">Winkel der Drehung im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="36ff5-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="36ff5-116">Winkel werden im Uhrzeigersinn gemessen, wenn Sie entlang der Drehungs Achse zum Ursprung suchen.</span><span class="sxs-lookup"><span data-stu-id="36ff5-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36ff5-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36ff5-117">Return value</span></span>

<span data-ttu-id="36ff5-118">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="36ff5-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="36ff5-119">Ein Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, gedreht um die angegebene Achse.</span><span class="sxs-lookup"><span data-stu-id="36ff5-119">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="36ff5-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36ff5-120">Remarks</span></span>

<span data-ttu-id="36ff5-121">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="36ff5-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="36ff5-122">Auf diese Weise kann die **D3DXQuaternionRotationAxis** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36ff5-122">In this way, the **D3DXQuaternionRotationAxis** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="36ff5-123">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="36ff5-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="36ff5-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36ff5-124">Requirements</span></span>



| <span data-ttu-id="36ff5-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36ff5-125">Requirement</span></span> | <span data-ttu-id="36ff5-126">Wert</span><span class="sxs-lookup"><span data-stu-id="36ff5-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36ff5-127">Header</span><span class="sxs-lookup"><span data-stu-id="36ff5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="36ff5-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="36ff5-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="36ff5-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="36ff5-129">Library</span></span><br/> | <dl> <span data-ttu-id="36ff5-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36ff5-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="36ff5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36ff5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36ff5-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="36ff5-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="36ff5-133">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="36ff5-133">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> <dt>

[<span data-ttu-id="36ff5-134">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="36ff5-134">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 
