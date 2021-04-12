---
description: Klone oder kopiert einen Animations Controller.
ms.assetid: 9836653c-9ea5-4fbc-89ac-0b46054a12d7
title: 'ID3DXAnimationController:: cloneanimationcontroller-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.CloneAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49c4a1c000df469c72a5e5538237e7110ded126f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355797"
---
# <a name="id3dxanimationcontrollercloneanimationcontroller-method"></a><span data-ttu-id="a5483-103">ID3DXAnimationController:: cloneanimationcontroller-Methode</span><span class="sxs-lookup"><span data-stu-id="a5483-103">ID3DXAnimationController::CloneAnimationController method</span></span>

<span data-ttu-id="a5483-104">Klone oder kopiert einen Animations Controller.</span><span class="sxs-lookup"><span data-stu-id="a5483-104">Clones, or copies, an animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5483-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5483-105">Syntax</span></span>


```C++
HRESULT CloneAnimationController(
  [in] UINT                      MaxNumAnimationOutputs,
  [in] UINT                      MaxNumAnimationSets,
  [in] UINT                      MaxNumTracks,
  [in] UINT                      MaxNumEvents,
  [in] LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="a5483-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5483-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5483-107">*Maxnumanimationoutputs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5483-107">*MaxNumAnimationOutputs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5483-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5483-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5483-109">Maximale Anzahl von Animations Ausgaben, die der Controller unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="a5483-109">Maximum number of animation outputs the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="a5483-110">*Maxnumanimationsets* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5483-110">*MaxNumAnimationSets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5483-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5483-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5483-112">Maximale Anzahl von Animations Sätzen, die der Controller unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="a5483-112">Maximum number of animation sets the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="a5483-113">*Maxnumtracks* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5483-113">*MaxNumTracks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5483-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5483-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5483-115">Maximale Anzahl von nach Titeln, die der Controller unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="a5483-115">Maximum number of tracks the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="a5483-116">*Maxnumevents* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5483-116">*MaxNumEvents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5483-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5483-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5483-118">Maximale Anzahl von Ereignissen, die der Controller unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="a5483-118">Maximum number of events the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="a5483-119">*ppanimcontroller* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5483-119">*ppAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5483-120">Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="a5483-120">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="a5483-121">Adresse eines Zeigers auf den geklonten [**ID3DXAnimationController**](id3dxanimationcontroller.md) -Animations Controller.</span><span class="sxs-lookup"><span data-stu-id="a5483-121">Address of a pointer to the cloned [**ID3DXAnimationController**](id3dxanimationcontroller.md) animation controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5483-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5483-122">Return value</span></span>

<span data-ttu-id="a5483-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a5483-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a5483-124">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a5483-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a5483-125">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="a5483-125">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5483-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5483-126">Requirements</span></span>



| <span data-ttu-id="a5483-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5483-127">Requirement</span></span> | <span data-ttu-id="a5483-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a5483-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5483-129">Header</span><span class="sxs-lookup"><span data-stu-id="a5483-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a5483-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5483-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a5483-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a5483-131">Library</span></span><br/> | <dl> <span data-ttu-id="a5483-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5483-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a5483-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5483-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5483-134">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="a5483-134">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
