---
description: Erstellt ein Animations Controller Objekt.
ms.assetid: 771e5966-ac1a-43c2-8e81-b6d573343ff0
title: D3DXCreateAnimationController-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateAnimationController
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a61b2c42a1eafa2ed28ac98c753588181a0ccf7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353717"
---
# <a name="d3dxcreateanimationcontroller-function"></a><span data-ttu-id="3ac63-103">D3DXCreateAnimationController-Funktion</span><span class="sxs-lookup"><span data-stu-id="3ac63-103">D3DXCreateAnimationController function</span></span>

<span data-ttu-id="3ac63-104">Erstellt ein Animations Controller Objekt.</span><span class="sxs-lookup"><span data-stu-id="3ac63-104">Creates an animation controller object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ac63-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ac63-105">Syntax</span></span>


```C++
HRESULT D3DXCreateAnimationController(
  _In_  UINT                      MaxNumAnimationOutputs,
  _In_  UINT                      MaxNumAnimationSets,
  _In_  UINT                      MaxNumTracks,
  _In_  UINT                      MaxNumEvents,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="3ac63-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ac63-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ac63-107">*Maxnumanimationoutputs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ac63-107">*MaxNumAnimationOutputs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac63-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ac63-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ac63-109">Maximale Anzahl von Animations Ausgaben, die der Controller unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="3ac63-109">Maximum number of animation outputs the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="3ac63-110">*Maxnumanimationsets* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ac63-110">*MaxNumAnimationSets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac63-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ac63-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ac63-112">Maximale Anzahl der Animations Sätze, die gemischt werden können.</span><span class="sxs-lookup"><span data-stu-id="3ac63-112">Maximum number of animation sets that can be mixed.</span></span>

</dd> <dt>

<span data-ttu-id="3ac63-113">*Maxnumtracks* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ac63-113">*MaxNumTracks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac63-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ac63-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ac63-115">Maximale Anzahl von Animations Sätzen, die gleichzeitig gemischt werden können.</span><span class="sxs-lookup"><span data-stu-id="3ac63-115">Maximum number of animation sets that can be mixed simultaneously.</span></span>

</dd> <dt>

<span data-ttu-id="3ac63-116">*Maxnumevents* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ac63-116">*MaxNumEvents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac63-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3ac63-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3ac63-118">Maximale Anzahl ausstehender Ereignisse, die vom Controller unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3ac63-118">Maximum number of outstanding events that the controller will support.</span></span>

</dd> <dt>

<span data-ttu-id="3ac63-119">*ppanimcontroller* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3ac63-119">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac63-120">Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="3ac63-120">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="3ac63-121">Zeiger auf das erstellte Animations Controller Objekt.</span><span class="sxs-lookup"><span data-stu-id="3ac63-121">Pointer to the animation controller object created.</span></span> <span data-ttu-id="3ac63-122">Siehe [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="3ac63-122">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ac63-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3ac63-123">Return value</span></span>

<span data-ttu-id="3ac63-124">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3ac63-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3ac63-125">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3ac63-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3ac63-126">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="3ac63-126">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ac63-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ac63-127">Remarks</span></span>

<span data-ttu-id="3ac63-128">Ein Animations Controller steuert einen Animations-Mixer.</span><span class="sxs-lookup"><span data-stu-id="3ac63-128">An animation controller controls an animation mixer.</span></span> <span data-ttu-id="3ac63-129">Der Controller fügt Methoden hinzu, um Mischungs Parameter im Zeitverlauf zu ändern, um reibungslose Übergänge zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="3ac63-129">The controller adds methods to modify blending parameters over time to enable smooth transitions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ac63-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ac63-130">Requirements</span></span>



| <span data-ttu-id="3ac63-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ac63-131">Requirement</span></span> | <span data-ttu-id="3ac63-132">Wert</span><span class="sxs-lookup"><span data-stu-id="3ac63-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac63-133">Header</span><span class="sxs-lookup"><span data-stu-id="3ac63-133">Header</span></span><br/>  | <dl> <span data-ttu-id="3ac63-134"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ac63-134"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3ac63-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3ac63-135">Library</span></span><br/> | <dl> <span data-ttu-id="3ac63-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ac63-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3ac63-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ac63-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ac63-138">Animations Funktionen</span><span class="sxs-lookup"><span data-stu-id="3ac63-138">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
