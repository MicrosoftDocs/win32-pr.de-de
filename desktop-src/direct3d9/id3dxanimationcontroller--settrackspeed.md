---
description: Legt die Erfolgs Geschwindigkeit fest. Die Erfolgs Geschwindigkeit ähnelt einem Multiplikator, der verwendet wird, um die Wiedergabe des Titels zu beschleunigen oder zu verlangsamen.
ms.assetid: b3946b61-0676-4690-9844-639fabd8fd7c
title: 'ID3DXAnimationController:: settrackspeed-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6cf57df2db370921c633ab695c9f60b96d2183dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355956"
---
# <a name="id3dxanimationcontrollersettrackspeed-method"></a><span data-ttu-id="d3765-104">ID3DXAnimationController:: settrackspeed-Methode</span><span class="sxs-lookup"><span data-stu-id="d3765-104">ID3DXAnimationController::SetTrackSpeed method</span></span>

<span data-ttu-id="d3765-105">Legt die Erfolgs Geschwindigkeit fest.</span><span class="sxs-lookup"><span data-stu-id="d3765-105">Sets the track speed.</span></span> <span data-ttu-id="d3765-106">Die Erfolgs Geschwindigkeit ähnelt einem Multiplikator, der verwendet wird, um die Wiedergabe des Titels zu beschleunigen oder zu verlangsamen.</span><span class="sxs-lookup"><span data-stu-id="d3765-106">The track speed is similar to a multiplier that is used to speed up or slow down the playback of the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3765-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3765-107">Syntax</span></span>


```C++
HRESULT SetTrackSpeed(
  [in] UINT  Track,
  [in] FLOAT Speed
);
```



## <a name="parameters"></a><span data-ttu-id="d3765-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3765-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3765-109">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3765-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3765-110">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d3765-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d3765-111">Der Bezeichner des Titels, auf den die Geschwindigkeit festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d3765-111">Identifier of the track to set the speed on.</span></span>

</dd> <dt>

<span data-ttu-id="d3765-112">*Geschwindigkeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3765-112">*Speed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3765-113">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d3765-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d3765-114">Neue Geschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="d3765-114">New speed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3765-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3765-115">Return value</span></span>

<span data-ttu-id="d3765-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d3765-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d3765-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d3765-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d3765-118">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="d3765-118">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3765-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3765-119">Requirements</span></span>



| <span data-ttu-id="d3765-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3765-120">Requirement</span></span> | <span data-ttu-id="d3765-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d3765-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3765-122">Header</span><span class="sxs-lookup"><span data-stu-id="d3765-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d3765-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3765-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d3765-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d3765-124">Library</span></span><br/> | <dl> <span data-ttu-id="d3765-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3765-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3765-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3765-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3765-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="d3765-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
