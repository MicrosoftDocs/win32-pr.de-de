---
description: Erstellt eine Matrix mit einem angegebenen Yaw, einer angegebenen Tonhöhe und einem angegebenen Rollout.
ms.assetid: a3ef2b57-275f-484a-88fc-aaa5e470717c
title: D3DXMatrixRotationYawPitchRoll-Funktion (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d65242f49ee94394337f43555c3e154141e3b642
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961730"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="2b748-103">D3DXMatrixRotationYawPitchRoll-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="2b748-103">D3DXMatrixRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="2b748-104">Erstellt eine Matrix mit einem angegebenen Yaw, einer angegebenen Tonhöhe und einem angegebenen Rollout.</span><span class="sxs-lookup"><span data-stu-id="2b748-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b748-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b748-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="2b748-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b748-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b748-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2b748-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b748-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b748-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2b748-109">Ein Zeiger auf die [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="2b748-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2b748-110">Nicht im  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b748-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b748-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b748-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b748-112">Um die y-Achse im Bogenmaße herum.</span><span class="sxs-lookup"><span data-stu-id="2b748-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="2b748-113">*Tonhöhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b748-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b748-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b748-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b748-115">Die Höhe um die x-Achse im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="2b748-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="2b748-116">*Rollout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b748-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b748-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b748-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b748-118">Führen Sie ein Rollback für die z-Achse im Bogenmaße durch.</span><span class="sxs-lookup"><span data-stu-id="2b748-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b748-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b748-119">Return value</span></span>

<span data-ttu-id="2b748-120">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b748-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2b748-121">Zeiger auf eine D3DXMATRIX-Struktur mit dem angegebenen "Yaw", "Pitch" und "Roll".</span><span class="sxs-lookup"><span data-stu-id="2b748-121">Pointer to a D3DXMATRIX structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b748-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b748-122">Remarks</span></span>

<span data-ttu-id="2b748-123">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2b748-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2b748-124">Auf diese Weise kann die D3DXMatrixRotationYawPitchRoll-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b748-124">In this way, the D3DXMatrixRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2b748-125">Die Reihenfolge der Transformationen lautet zuerst "Roll First", dann "Pitch" und "Yaw".</span><span class="sxs-lookup"><span data-stu-id="2b748-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="2b748-126">Relativ zur lokalen Koordinatenachse des Objekts entspricht dies der Drehung um die z-Achse, gefolgt von der Drehung um die x-Achse, gefolgt von der Drehung um die y-Achse, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2b748-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![Abbildung von "Roll", "Pitch" und "Yaw" als Drehung um die drei Achsen](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="2b748-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b748-128">Requirements</span></span>



| <span data-ttu-id="2b748-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b748-129">Requirement</span></span> | <span data-ttu-id="2b748-130">Wert</span><span class="sxs-lookup"><span data-stu-id="2b748-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b748-131">Header</span><span class="sxs-lookup"><span data-stu-id="2b748-131">Header</span></span><br/>  | <dl> <span data-ttu-id="2b748-132"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b748-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2b748-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2b748-133">Library</span></span><br/> | <dl> <span data-ttu-id="2b748-134"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b748-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2b748-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b748-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b748-136">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2b748-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
