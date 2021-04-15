---
title: LVM_GETHOVERTIME Meldung (kommstrg. h)
description: Ruft die Zeitspanne ab, die der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird. Sie können diese Nachricht explizit senden oder das ListView \_ gethovertime-Makro verwenden.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- Windows-Steuerelemente für LVM_GETHOVERTIME Meldung
topic_type:
- apiref
api_name:
- LVM_GETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e243ece42f06ffe35eb31954d9ca0dd44957be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477574"
---
# <a name="lvm_gethovertime-message"></a><span data-ttu-id="2e50e-105">LVM- \_ gethovertime-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2e50e-105">LVM\_GETHOVERTIME message</span></span>

<span data-ttu-id="2e50e-106">Ruft die Zeitspanne ab, die der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="2e50e-106">Retrieves the amount of time that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="2e50e-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ gethovertime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="2e50e-107">You can send this message explicitly or use the [**ListView\_GetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2e50e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e50e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e50e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e50e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2e50e-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2e50e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2e50e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e50e-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2e50e-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2e50e-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e50e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e50e-113">Return value</span></span>

<span data-ttu-id="2e50e-114">Gibt die Zeitspanne in Millisekunden zurück, die der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="2e50e-114">Returns the amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="2e50e-115">Wenn der Rückgabewert (**DWORD**)-1 ist, ist die Hover-Zeit die standardmäßige Hover-Zeit.</span><span class="sxs-lookup"><span data-stu-id="2e50e-115">If the return value is (**DWORD**)-1, then the hover time is the default hover time.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e50e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e50e-116">Remarks</span></span>

<span data-ttu-id="2e50e-117">Die Hover-Zeit wirkt sich nur auf Listenansicht-Steuerelemente aus, die über die [**LVS \_ Ex \_ trackselect**](extended-list-view-styles.md)-, [**LVS \_ Ex \_ oneclickreaktivierungs**](extended-list-view-styles.md)-oder [**LVS \_ Ex \_ twoclickaktivierungs**](extended-list-view-styles.md) -Stil der erweiterten Listenansicht verfügen.</span><span class="sxs-lookup"><span data-stu-id="2e50e-117">The hover time only affects list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md), [**LVS\_EX\_ONECLICKACTIVATE**](extended-list-view-styles.md), or [**LVS\_EX\_TWOCLICKACTIVATE**](extended-list-view-styles.md) extended list-view style.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e50e-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e50e-118">Requirements</span></span>



| <span data-ttu-id="2e50e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e50e-119">Requirement</span></span> | <span data-ttu-id="2e50e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2e50e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2e50e-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2e50e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2e50e-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e50e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2e50e-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2e50e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2e50e-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2e50e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2e50e-125">Header</span><span class="sxs-lookup"><span data-stu-id="2e50e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e50e-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e50e-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





