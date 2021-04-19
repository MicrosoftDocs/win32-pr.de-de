---
description: Wendet den Animations Satz auf den angegebenen Titel an.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: 'ID3DXAnimationController:: settrackanimationset-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dce979e48ed118dc257c147b27615f7bbc89231
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361234"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a><span data-ttu-id="ed92b-103">ID3DXAnimationController:: settrackanimationset-Methode</span><span class="sxs-lookup"><span data-stu-id="ed92b-103">ID3DXAnimationController::SetTrackAnimationSet method</span></span>

<span data-ttu-id="ed92b-104">Wendet den Animations Satz auf den angegebenen Titel an.</span><span class="sxs-lookup"><span data-stu-id="ed92b-104">Applies the animation set to the specified track.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed92b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed92b-105">Syntax</span></span>


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="ed92b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed92b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed92b-107">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed92b-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed92b-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed92b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed92b-109">Der Bezeichner des Titels, auf den der Animations Satz angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed92b-109">Identifier of the track to which the animation set is applied.</span></span>

</dd> <dt>

<span data-ttu-id="ed92b-110">*panimset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed92b-110">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed92b-111">Typ: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="ed92b-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="ed92b-112">Zeiger auf den [**ID3DXAnimationSet**](id3dxanimationset.md) -Animations Satz, der der Spur hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed92b-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to be added to the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed92b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed92b-113">Return value</span></span>

<span data-ttu-id="ed92b-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed92b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed92b-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed92b-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ed92b-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="ed92b-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed92b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed92b-117">Remarks</span></span>

<span data-ttu-id="ed92b-118">Diese Methode legt den Animations Satz auf den angegebenen Titel für die Mischung fest.</span><span class="sxs-lookup"><span data-stu-id="ed92b-118">This method sets the animation set to the specified track for mixing.</span></span> <span data-ttu-id="ed92b-119">Der Animations Satz für jede Spur wird entsprechend der Last und Geschwindigkeit des Titels gemischt, wenn [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ed92b-119">The animation set for each track is blended according to the track weight and speed when [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed92b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed92b-120">Requirements</span></span>



| <span data-ttu-id="ed92b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed92b-121">Requirement</span></span> | <span data-ttu-id="ed92b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ed92b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed92b-123">Header</span><span class="sxs-lookup"><span data-stu-id="ed92b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ed92b-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed92b-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ed92b-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ed92b-125">Library</span></span><br/> | <dl> <span data-ttu-id="ed92b-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed92b-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ed92b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed92b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed92b-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ed92b-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
