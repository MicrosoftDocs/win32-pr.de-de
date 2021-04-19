---
description: Legt die Gewichtung für die Prioritäts Mischung für den angegebenen Animations Titel fest.
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: 'ID3DXAnimationController:: settrackpriority-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPriority
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 32f1f8cce4641203782b0a84840d2986780da26a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353774"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a><span data-ttu-id="bf142-103">ID3DXAnimationController:: settrackpriority-Methode</span><span class="sxs-lookup"><span data-stu-id="bf142-103">ID3DXAnimationController::SetTrackPriority method</span></span>

<span data-ttu-id="bf142-104">Legt die Gewichtung für die Prioritäts Mischung für den angegebenen Animations Titel fest.</span><span class="sxs-lookup"><span data-stu-id="bf142-104">Sets the priority blending weight for the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf142-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf142-105">Syntax</span></span>


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a><span data-ttu-id="bf142-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf142-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf142-107">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf142-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf142-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf142-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf142-109">Bezeichner nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="bf142-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bf142-110">*Priorität* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf142-110">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf142-111">Type: **[ **D3DXPRIORITY- \_ Typ**](./d3dxpriority-type.md)**</span><span class="sxs-lookup"><span data-stu-id="bf142-111">Type: **[**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md)**</span></span>

<span data-ttu-id="bf142-112">Priorität nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="bf142-112">Track priority.</span></span> <span data-ttu-id="bf142-113">Dieser Parameter sollte auf eine der Konstanten vom [**D3DXPRIORITY- \_ Typ**](./d3dxpriority-type.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bf142-113">This parameter should be set to one of the constants from [**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf142-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf142-114">Return value</span></span>

<span data-ttu-id="bf142-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bf142-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bf142-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bf142-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bf142-117">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="bf142-117">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf142-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf142-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bf142-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bf142-119">Requirements</span></span>



| <span data-ttu-id="bf142-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf142-120">Requirement</span></span> | <span data-ttu-id="bf142-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bf142-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf142-122">Header</span><span class="sxs-lookup"><span data-stu-id="bf142-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bf142-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf142-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="bf142-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bf142-124">Library</span></span><br/> | <dl> <span data-ttu-id="bf142-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf142-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bf142-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf142-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf142-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="bf142-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
