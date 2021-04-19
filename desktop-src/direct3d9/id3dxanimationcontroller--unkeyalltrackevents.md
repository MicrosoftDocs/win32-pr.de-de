---
description: Entfernt alle Ereignisse aus einer angegebenen Animations Spur.
ms.assetid: 25c4d04a-0d75-4113-ad90-db84aa937098
title: 'ID3DXAnimationController:: unkeyalltrackevents-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyAllTrackEvents
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5904e9e09c8a821cdc532f9046217ae64bbf3de5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353773"
---
# <a name="id3dxanimationcontrollerunkeyalltrackevents-method"></a><span data-ttu-id="63fa3-103">ID3DXAnimationController:: unkeyalltrackevents-Methode</span><span class="sxs-lookup"><span data-stu-id="63fa3-103">ID3DXAnimationController::UnkeyAllTrackEvents method</span></span>

<span data-ttu-id="63fa3-104">Entfernt alle Ereignisse aus einer angegebenen Animations Spur.</span><span class="sxs-lookup"><span data-stu-id="63fa3-104">Removes all events from a specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="63fa3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="63fa3-105">Syntax</span></span>


```C++
HRESULT UnkeyAllTrackEvents(
  [in] UINT Track
);
```



## <a name="parameters"></a><span data-ttu-id="63fa3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="63fa3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63fa3-107">Nach *verfolgen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63fa3-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63fa3-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="63fa3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="63fa3-109">Der Bezeichner der Spur, auf der alle Ereignisse entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="63fa3-109">Identifier of the track on which all events should be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63fa3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63fa3-110">Return value</span></span>

<span data-ttu-id="63fa3-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="63fa3-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="63fa3-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="63fa3-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="63fa3-113">Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="63fa3-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="63fa3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63fa3-114">Remarks</span></span>

<span data-ttu-id="63fa3-115">Diese Methode verhindert die Ausführung aller Ereignisse, die zuvor für die Nachverfolgung geplant wurden, und verwirft alle Daten, die diesen Ereignissen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="63fa3-115">This method prevents the execution of all events previously scheduled on the track, and discards all data associated with those events.</span></span>

## <a name="requirements"></a><span data-ttu-id="63fa3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63fa3-116">Requirements</span></span>



| <span data-ttu-id="63fa3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63fa3-117">Requirement</span></span> | <span data-ttu-id="63fa3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="63fa3-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63fa3-119">Header</span><span class="sxs-lookup"><span data-stu-id="63fa3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="63fa3-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="63fa3-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="63fa3-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="63fa3-121">Library</span></span><br/> | <dl> <span data-ttu-id="63fa3-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63fa3-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="63fa3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63fa3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63fa3-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="63fa3-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
