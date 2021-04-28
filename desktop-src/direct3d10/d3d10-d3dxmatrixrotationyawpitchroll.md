---
description: 'D3DXMatrixRotationYawPitchRoll-Funktion (D3DX10Math.h): Erstellt eine Matrix mit einem angegebenen Yaw, Pitch und Roll.'
ms.assetid: a3ef2b57-275f-484a-88fc-aaa5e470717c
title: D3DXMatrixRotationYawPitchRoll-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: ae00865c45878159dbf86a6f829e9d1cf50337e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108948"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="ce06f-103">D3DXMatrixRotationYawPitchRoll-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="ce06f-103">D3DXMatrixRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="ce06f-104">Erstellt eine Matrix mit einem angegebenen Yaw, einer angegebenen Tonhöhe und einem angegebenen Roll.</span><span class="sxs-lookup"><span data-stu-id="ce06f-104">Builds a matrix with a specified yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce06f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce06f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a><span data-ttu-id="ce06f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce06f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce06f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ce06f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce06f-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce06f-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ce06f-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="ce06f-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ce06f-110">*Yaw* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ce06f-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce06f-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce06f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce06f-112">Gieren Sie um die y-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="ce06f-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="ce06f-113">*Pitch* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ce06f-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce06f-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce06f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce06f-115">Tonhöhe um die X-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="ce06f-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="ce06f-116">*Roll* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ce06f-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce06f-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce06f-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce06f-118">Rollieren Sie um die Z-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="ce06f-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce06f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce06f-119">Return value</span></span>

<span data-ttu-id="ce06f-120">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce06f-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ce06f-121">Zeiger auf eine D3DXMATRIX-Struktur mit dem angegebenen Yaw, Pitch und Roll.</span><span class="sxs-lookup"><span data-stu-id="ce06f-121">Pointer to a D3DXMATRIX structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce06f-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce06f-122">Remarks</span></span>

<span data-ttu-id="ce06f-123">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ce06f-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ce06f-124">Auf diese Weise kann die D3DXMatrixRotationYawPitchRoll-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce06f-124">In this way, the D3DXMatrixRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ce06f-125">Die Reihenfolge der Transformationen ist zuerst roll, dann pitch und yaw.</span><span class="sxs-lookup"><span data-stu-id="ce06f-125">The order of transformations is roll first, then pitch, then yaw.</span></span> <span data-ttu-id="ce06f-126">Relativ zur lokalen Koordinatenachse des Objekts entspricht dies der Drehung um die Z-Achse, gefolgt von der Drehung um die x-Achse und der Drehung um die y-Achse, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ce06f-126">Relative to the object's local coordinate axis, this is equivalent to rotation around the z-axis, followed by rotation around the x-axis, followed by rotation around the y-axis, as shown in the following illustration.</span></span>

![Abbildung von Roll, Pitch und YAW als Drehungen um die drei Achsen](images/pitchyawroll.png)

## <a name="requirements"></a><span data-ttu-id="ce06f-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce06f-128">Requirements</span></span>



| <span data-ttu-id="ce06f-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce06f-129">Requirement</span></span> | <span data-ttu-id="ce06f-130">Wert</span><span class="sxs-lookup"><span data-stu-id="ce06f-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce06f-131">Header</span><span class="sxs-lookup"><span data-stu-id="ce06f-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ce06f-132"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ce06f-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="ce06f-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce06f-133">Library</span></span><br/> | <dl> <span data-ttu-id="ce06f-134"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce06f-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ce06f-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ce06f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce06f-136">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ce06f-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
