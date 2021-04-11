---
title: LVM_SETHOVERTIME Meldung (kommstrg. h)
description: Legt den Zeitraum fest, in dem der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird. Sie können diese Nachricht explizit senden oder das ListView- \_ Makro "-Serverzeit" verwenden.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- Windows-Steuerelemente für LVM_SETHOVERTIME Meldung
topic_type:
- apiref
api_name:
- LVM_SETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3aecd3c0d48cddc2cbaae49e7e888f91a985575
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102886"
---
# <a name="lvm_sethovertime-message"></a><span data-ttu-id="512cc-105">LVM- \_ mesvertime-Nachricht</span><span class="sxs-lookup"><span data-stu-id="512cc-105">LVM\_SETHOVERTIME message</span></span>

<span data-ttu-id="512cc-106">Legt den Zeitraum fest, in dem der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="512cc-106">Sets the amount of time which the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="512cc-107">Sie können diese Nachricht explizit senden oder das ListView-Makro "- [**\_ Serverzeit**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="512cc-107">You can send this message explicitly or use the [**ListView\_SetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="512cc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="512cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="512cc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="512cc-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="512cc-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="512cc-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="512cc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="512cc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="512cc-112">Die neue Zeitspanne (in Millisekunden), die der Mauszeiger auf ein Element zeigen muss, bevor es ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="512cc-112">The new amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="512cc-113">Wenn dieser Wert (**DWORD**)-1 ist, wird die Hover-Zeit auf die standardmäßige Hover-Zeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="512cc-113">If this value is (**DWORD**)-1, then the hover time is set to the default hover time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="512cc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="512cc-114">Return value</span></span>

<span data-ttu-id="512cc-115">Gibt die vorherige Hover-Zeit zurück.</span><span class="sxs-lookup"><span data-stu-id="512cc-115">Returns the previous hover time.</span></span>

## <a name="remarks"></a><span data-ttu-id="512cc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="512cc-116">Remarks</span></span>

<span data-ttu-id="512cc-117">Die Hover-Zeit wirkt sich nur auf Listenansicht-Steuerelemente aus, die über die [**LVS \_ Ex \_ trackselect**](extended-list-view-styles.md)-, [**LVS \_ Ex \_ oneclickreaktivierungs**](extended-list-view-styles.md)-oder [**LVS \_ Ex \_ twoclickaktivierungs**](extended-list-view-styles.md) -Stil der erweiterten Listenansicht verfügen.</span><span class="sxs-lookup"><span data-stu-id="512cc-117">The hover time only affects list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md), [**LVS\_EX\_ONECLICKACTIVATE**](extended-list-view-styles.md), or [**LVS\_EX\_TWOCLICKACTIVATE**](extended-list-view-styles.md) extended list-view style.</span></span>

## <a name="requirements"></a><span data-ttu-id="512cc-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="512cc-118">Requirements</span></span>



| <span data-ttu-id="512cc-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="512cc-119">Requirement</span></span> | <span data-ttu-id="512cc-120">Wert</span><span class="sxs-lookup"><span data-stu-id="512cc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="512cc-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="512cc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="512cc-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="512cc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="512cc-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="512cc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="512cc-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="512cc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="512cc-125">Header</span><span class="sxs-lookup"><span data-stu-id="512cc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="512cc-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="512cc-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





