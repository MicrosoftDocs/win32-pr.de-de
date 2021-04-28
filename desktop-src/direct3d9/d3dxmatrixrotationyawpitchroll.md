---
description: 'D3DXMatrixRotationYawPitchRoll-Funktion (D3dx9math.h): Erstellt eine Matrix mit einem angegebenen Yaw, Pitch und Roll.'
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: D3DXMatrixRotationYawPitchRoll-Funktion (D3dx9math.h)
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
ms.openlocfilehash: 789812b6e94efd40ff71209348f0c9727088c253
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118148"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="808c5-103">D3DXMatrixRotationYawPitchRoll-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="808c5-103">D3DXMatrixRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="808c5-104">Erstellt eine Matrix mit einem angegebenen Yaw, einer angegebenen Tonhöhe und einem angegebenen Roll.</span><span class="sxs-lookup"><span data-stu-id="808c5-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="808c5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="808c5-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="808c5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="808c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="808c5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="808c5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="808c5-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="808c5-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="808c5-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="808c5-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="808c5-110">*Yaw* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="808c5-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808c5-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="808c5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="808c5-112">Gieren Sie um die y-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="808c5-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="808c5-113">*Pitch* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="808c5-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808c5-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="808c5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="808c5-115">Tonhöhe um die X-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="808c5-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="808c5-116">*Roll* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="808c5-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="808c5-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="808c5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="808c5-118">Rollieren Sie um die Z-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="808c5-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="808c5-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="808c5-119">Return value</span></span>

<span data-ttu-id="808c5-120">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="808c5-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="808c5-121">Zeiger auf eine [**D3DXMATRIX-Struktur**](d3dxmatrix.md) mit dem angegebenen Yaw, Pitch und Roll.</span><span class="sxs-lookup"><span data-stu-id="808c5-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="808c5-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="808c5-122">Remarks</span></span>

<span data-ttu-id="808c5-123">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="808c5-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="808c5-124">Auf diese Weise kann die **D3DXMatrixRotationYawPitchRoll-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="808c5-124">In this way, the **D3DXMatrixRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="808c5-125">Die Reihenfolge der Transformationen ist zuerst roll, dann pitch und yaw.</span><span class="sxs-lookup"><span data-stu-id="808c5-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="808c5-126">Relativ zur lokalen Koordinatenachse des Objekts entspricht dies der Drehung um die Z-Achse, gefolgt von der Drehung um die x-Achse und der Drehung um die y-Achse, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="808c5-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![Abbildung von Roll, Pitch und YAW als Drehungen um die drei Achsen](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="808c5-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="808c5-128">Requirements</span></span>



| <span data-ttu-id="808c5-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="808c5-129">Requirement</span></span> | <span data-ttu-id="808c5-130">Wert</span><span class="sxs-lookup"><span data-stu-id="808c5-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="808c5-131">Header</span><span class="sxs-lookup"><span data-stu-id="808c5-131">Header</span></span><br/>  | <dl> <span data-ttu-id="808c5-132"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="808c5-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="808c5-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="808c5-133">Library</span></span><br/> | <dl> <span data-ttu-id="808c5-134"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="808c5-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="808c5-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="808c5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="808c5-136">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="808c5-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="808c5-137">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="808c5-137">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="808c5-138">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="808c5-138">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="808c5-139">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="808c5-139">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="808c5-140">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="808c5-140">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="808c5-141">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="808c5-141">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
