---
description: 'D3DXQuaternionRotationYawPitchRoll-Funktion (D3dx9math.h): Erstellt eine Quaternion mit dem angegebenen Yaw, Pitch und Roll.'
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: D3DXQuaternionRotationYawPitchRoll-Funktion (D3dx9math.h)
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
ms.openlocfilehash: 541e181425782662c6d40affc22c829b4ba343ab
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117998"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a><span data-ttu-id="0c0a0-103">D3DXQuaternionRotationYawPitchRoll-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="0c0a0-103">D3DXQuaternionRotationYawPitchRoll function (D3dx9math.h)</span></span>

<span data-ttu-id="0c0a0-104">Erstellt eine Quaternion mit dem angegebenen Yaw, Pitch und Roll.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-104">Builds a quaternion with the given yaw, pitch, and roll.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c0a0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c0a0-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a><span data-ttu-id="0c0a0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c0a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c0a0-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0c0a0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c0a0-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c0a0-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0c0a0-109">Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0c0a0-110">*Yaw* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0c0a0-110">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c0a0-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c0a0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c0a0-112">Gischen Sie um die y-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-112">Yaw around the y-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="0c0a0-113">*Tonhöhe* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0c0a0-113">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c0a0-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c0a0-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c0a0-115">Tonhöhe um die x-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-115">Pitch around the x-axis, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="0c0a0-116">*Roll* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0c0a0-116">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c0a0-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c0a0-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c0a0-118">Rolling um die Z-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-118">Roll around the z-axis, in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c0a0-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c0a0-119">Return value</span></span>

<span data-ttu-id="0c0a0-120">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="0c0a0-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0c0a0-121">Zeiger auf eine [**D3DXQUATERNION-Struktur**](d3dxquaternion.md) mit dem angegebenen Yaw, Pitch und Roll.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure with the specified yaw, pitch, and roll.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c0a0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c0a0-122">Remarks</span></span>

<span data-ttu-id="0c0a0-123">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0c0a0-124">Auf diese Weise kann die **D3DXQuaternionRotationYawPitchRoll-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-124">In this way, the **D3DXQuaternionRotationYawPitchRoll** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="0c0a0-125">Verwenden [**Sie D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="0c0a0-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c0a0-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c0a0-126">Requirements</span></span>



| <span data-ttu-id="0c0a0-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c0a0-127">Requirement</span></span> | <span data-ttu-id="0c0a0-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0c0a0-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c0a0-129">Header</span><span class="sxs-lookup"><span data-stu-id="0c0a0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0c0a0-130"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0c0a0-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0c0a0-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c0a0-131">Library</span></span><br/> | <dl> <span data-ttu-id="0c0a0-132"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c0a0-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0c0a0-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0c0a0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c0a0-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="0c0a0-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0c0a0-135">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="0c0a0-135">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="0c0a0-136">**D3DXQuaternionRotationMatrix**</span><span class="sxs-lookup"><span data-stu-id="0c0a0-136">**D3DXQuaternionRotationMatrix**</span></span>](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 
