---
description: Erstellt eine Quaternion mit dem angegebenen Yaw, der angegebenen Tonhöhe und dem angegebenen Rollover.
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: D3DXQuaternionRotationYawPitchRoll-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4d0df60149643db0d9243afe57e394320f81d08c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353360"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="dc42f-103">D3DXQuaternionRotationYawPitchRoll-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="dc42f-103">D3DXQuaternionRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="dc42f-104">Erstellt eine Quaternion mit dem angegebenen Yaw, der angegebenen Tonhöhe und dem angegebenen Rollover.</span><span class="sxs-lookup"><span data-stu-id="dc42f-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc42f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc42f-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="dc42f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc42f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc42f-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dc42f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc42f-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc42f-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="dc42f-109">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="dc42f-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="dc42f-110">Nicht im  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc42f-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc42f-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc42f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc42f-112">Um die y-Achse im Bogenmaße herum.</span><span class="sxs-lookup"><span data-stu-id="dc42f-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="dc42f-113">*Tonhöhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc42f-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc42f-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc42f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc42f-115">Die Höhe um die x-Achse im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="dc42f-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="dc42f-116">*Rollout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc42f-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc42f-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc42f-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc42f-118">Führen Sie ein Rollback für die z-Achse im Bogenmaße durch.</span><span class="sxs-lookup"><span data-stu-id="dc42f-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc42f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc42f-119">Return value</span></span>

<span data-ttu-id="dc42f-120">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc42f-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="dc42f-121">Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur mit dem angegebenen "Yaw", "Pitch" und "Roll".</span><span class="sxs-lookup"><span data-stu-id="dc42f-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc42f-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc42f-122">Remarks</span></span>

<span data-ttu-id="dc42f-123">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dc42f-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="dc42f-124">Auf diese Weise kann die **D3DXQuaternionRotationYawPitchRoll** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc42f-124">In this way, the **D3DXQuaternionRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="dc42f-125">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="dc42f-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc42f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc42f-126">Requirements</span></span>



| <span data-ttu-id="dc42f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc42f-127">Requirement</span></span> | <span data-ttu-id="dc42f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="dc42f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc42f-129">Header</span><span class="sxs-lookup"><span data-stu-id="dc42f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="dc42f-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc42f-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="dc42f-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc42f-131">Library</span></span><br/> | <dl> <span data-ttu-id="dc42f-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc42f-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dc42f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc42f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc42f-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="dc42f-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="dc42f-135">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="dc42f-135">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="dc42f-136">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="dc42f-136">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 
