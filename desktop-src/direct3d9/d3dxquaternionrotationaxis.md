---
description: 'D3DXQuaternionRotationAxis-Funktion (D3dx9math.h): Rotiert eine Quaternion um eine beliebige Achse.'
ms.assetid: 9ff0fe2c-54d6-482c-84e1-f38e3c57d8dd
title: D3DXQuaternionRotationAxis-Funktion (D3dx9math.h)
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
ms.openlocfilehash: a5cbbdc3603b5e2eb7a03f592d44fa88f07ef015
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118018"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx9mathh"></a><span data-ttu-id="8ff8c-103">D3DXQuaternionRotationAxis-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="8ff8c-103">D3DXQuaternionRotationAxis function (D3dx9math.h)</span></span>

<span data-ttu-id="8ff8c-104">Rotiert eine Quaternion um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="8ff8c-104">Rotates a quaternion about an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ff8c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ff8c-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a><span data-ttu-id="8ff8c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ff8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ff8c-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8ff8c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff8c-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ff8c-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8ff8c-109">Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="8ff8c-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8ff8c-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8ff8c-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff8c-111">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ff8c-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="8ff8c-112">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die Achse identifiziert, um die die Quaternion gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ff8c-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the axis about which to rotate the quaternion.</span></span>

</dd> <dt>

<span data-ttu-id="8ff8c-113">*Winkel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8ff8c-113">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff8c-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ff8c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ff8c-115">Drehwinkel im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="8ff8c-115">Angle of rotation, in radians.</span></span> <span data-ttu-id="8ff8c-116">Winkel werden im Uhrzeigersinn gemessen, wenn entlang der Drehachse zum Ursprung gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="8ff8c-116">Angles are measured clockwise when looking along the rotation axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ff8c-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ff8c-117">Return value</span></span>

<span data-ttu-id="8ff8c-118">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ff8c-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8ff8c-119">Zeiger auf eine um die angegebene Achse gedrehte [**D3DXQUATERNION-Struktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="8ff8c-119">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure rotated around the specified axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ff8c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ff8c-120">Remarks</span></span>

<span data-ttu-id="8ff8c-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8ff8c-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8ff8c-122">Auf diese Weise kann die **D3DXQuaternionRotationAxis-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8ff8c-122">In this way, the **D3DXQuaternionRotationAxis** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8ff8c-123">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die nicht bereits normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="8ff8c-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ff8c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ff8c-124">Requirements</span></span>



| <span data-ttu-id="8ff8c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ff8c-125">Requirement</span></span> | <span data-ttu-id="8ff8c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8ff8c-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff8c-127">Header</span><span class="sxs-lookup"><span data-stu-id="8ff8c-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8ff8c-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8ff8c-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8ff8c-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ff8c-129">Library</span></span><br/> | <dl> <span data-ttu-id="8ff8c-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ff8c-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8ff8c-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8ff8c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ff8c-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="8ff8c-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8ff8c-133">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="8ff8c-133">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> <dt>

[<span data-ttu-id="8ff8c-134">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="8ff8c-134">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 
