---
description: 'D3DXQuaternionRotationYawPitchRoll-Funktion (D3DX10Math.h): Erstellt eine Quaternion mit dem angegebenen Yaw, Pitch und Roll.'
ms.assetid: c929d9d4-b9cb-4de6-86c1-26fec3617846
title: D3DXQuaternionRotationYawPitchRoll-Funktion (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cefcf9a927cee0d8f7c83ff42ae6ca4fc699bb09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108748"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx10mathh"></a><span data-ttu-id="bf1e3-103">D3DXQuaternionRotationYawPitchRoll-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="bf1e3-103">D3DXQuaternionRotationYawPitchRoll function (D3DX10Math.h)</span></span>

<span data-ttu-id="bf1e3-104">Erstellt eine Quaternion mit dem angegebenen Yaw, Pitch und Roll.</span><span class="sxs-lookup"><span data-stu-id="bf1e3-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf1e3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf1e3-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="bf1e3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf1e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf1e3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bf1e3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1e3-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf1e3-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bf1e3-109">Zeiger auf [**D3DXQUATERNION,**](d3d10-d3dxquaternion.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="bf1e3-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bf1e3-110">*Yaw* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bf1e3-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1e3-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf1e3-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf1e3-112">Gischen Sie um die y-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="bf1e3-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="bf1e3-113">*Tonhöhe* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bf1e3-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1e3-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf1e3-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf1e3-115">Tonhöhe um die x-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="bf1e3-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="bf1e3-116">*Roll* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bf1e3-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1e3-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf1e3-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf1e3-118">Rolling um die Z-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="bf1e3-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf1e3-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf1e3-119">Return value</span></span>

<span data-ttu-id="bf1e3-120">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf1e3-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bf1e3-121">Zeiger auf eine D3DXQUATERNION-Struktur mit dem angegebenen Yaw, Pitch und Roll.</span><span class="sxs-lookup"><span data-stu-id="bf1e3-121">Pointer to a D3DXQUATERNION structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf1e3-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf1e3-122">Remarks</span></span>

<span data-ttu-id="bf1e3-123">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bf1e3-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="bf1e3-124">Auf diese Weise kann die D3DXQuaternionRotationYawPitchRoll-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf1e3-124">In this way, the D3DXQuaternionRotationYawPitchRoll function can be used as a parameter for another function.</span></span>

<span data-ttu-id="bf1e3-125">Verwenden [**Sie D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="bf1e3-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf1e3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf1e3-126">Requirements</span></span>



| <span data-ttu-id="bf1e3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf1e3-127">Requirement</span></span> | <span data-ttu-id="bf1e3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="bf1e3-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf1e3-129">Header</span><span class="sxs-lookup"><span data-stu-id="bf1e3-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bf1e3-130"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="bf1e3-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bf1e3-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bf1e3-131">Library</span></span><br/> | <dl> <span data-ttu-id="bf1e3-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf1e3-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bf1e3-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bf1e3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf1e3-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="bf1e3-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
