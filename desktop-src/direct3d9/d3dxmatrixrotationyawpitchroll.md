---
description: Erstellt eine Matrix mit einem angegebenen Yaw, einer angegebenen Tonhöhe und einem angegebenen Rollout.
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: D3DXMatrixRotationYawPitchRoll-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2a8d6a531592ce49342dae0d0ecd6b3ace995bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219439"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="ba7d2-103">D3DXMatrixRotationYawPitchRoll-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ba7d2-103">D3DXMatrixRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="ba7d2-104">Erstellt eine Matrix mit einem angegebenen Yaw, einer angegebenen Tonhöhe und einem angegebenen Rollout.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba7d2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba7d2-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="ba7d2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba7d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba7d2-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ba7d2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba7d2-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba7d2-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ba7d2-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ba7d2-110">Nicht im  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba7d2-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba7d2-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba7d2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba7d2-112">Um die y-Achse im Bogenmaße herum.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="ba7d2-113">*Tonhöhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba7d2-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba7d2-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba7d2-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba7d2-115">Die Höhe um die x-Achse im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="ba7d2-116">*Rollout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba7d2-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba7d2-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba7d2-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba7d2-118">Führen Sie ein Rollback für die z-Achse im Bogenmaße durch.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba7d2-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba7d2-119">Return value</span></span>

<span data-ttu-id="ba7d2-120">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba7d2-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ba7d2-121">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur mit dem angegebenen "Yaw", "Pitch" und "Roll".</span><span class="sxs-lookup"><span data-stu-id="ba7d2-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba7d2-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba7d2-122">Remarks</span></span>

<span data-ttu-id="ba7d2-123">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ba7d2-124">Auf diese Weise kann die **D3DXMatrixRotationYawPitchRoll** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-124">In this way, the **D3DXMatrixRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ba7d2-125">Die Reihenfolge der Transformationen lautet zuerst "Roll First", dann "Pitch" und "Yaw".</span><span class="sxs-lookup"><span data-stu-id="ba7d2-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="ba7d2-126">Relativ zur lokalen Koordinatenachse des Objekts entspricht dies der Drehung um die z-Achse, gefolgt von der Drehung um die x-Achse, gefolgt von der Drehung um die y-Achse, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ba7d2-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![Abbildung von "Roll", "Pitch" und "Yaw" als Drehung um die drei Achsen](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="ba7d2-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba7d2-128">Requirements</span></span>



| <span data-ttu-id="ba7d2-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba7d2-129">Requirement</span></span> | <span data-ttu-id="ba7d2-130">Wert</span><span class="sxs-lookup"><span data-stu-id="ba7d2-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7d2-131">Header</span><span class="sxs-lookup"><span data-stu-id="ba7d2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ba7d2-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba7d2-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ba7d2-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ba7d2-133">Library</span></span><br/> | <dl> <span data-ttu-id="ba7d2-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba7d2-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ba7d2-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba7d2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba7d2-136">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ba7d2-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ba7d2-137">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="ba7d2-137">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="ba7d2-138">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="ba7d2-138">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="ba7d2-139">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="ba7d2-139">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="ba7d2-140">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="ba7d2-140">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="ba7d2-141">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="ba7d2-141">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
