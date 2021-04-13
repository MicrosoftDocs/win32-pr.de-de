---
title: EM_SETEVENTMASK Meldung (RichEdit. h)
description: Legt die Ereignis Maske für ein Rich-Edit-Steuerelement fest. Die Ereignis Maske gibt an, welche Benachrichtigungs Codes das Steuerelement an das übergeordnete Fenster sendet.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- Windows-Steuerelemente für EM_SETEVENTMASK Meldung
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4d79d23f7b56a29bc4f5142ed03b23e8081687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478567"
---
# <a name="em_seteventmask-message"></a><span data-ttu-id="dcadd-105">EM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="dcadd-105">EM\_SETEVENTMASK message</span></span>

<span data-ttu-id="dcadd-106">Legt die Ereignis Maske für ein Rich-Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="dcadd-106">Sets the event mask for a rich edit control.</span></span> <span data-ttu-id="dcadd-107">Die Ereignis Maske gibt an, welche Benachrichtigungs Codes das Steuerelement an das übergeordnete Fenster sendet.</span><span class="sxs-lookup"><span data-stu-id="dcadd-107">The event mask specifies which notification codes the control sends to its parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="dcadd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcadd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcadd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dcadd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dcadd-110">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="dcadd-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dcadd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dcadd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dcadd-112">Neue Ereignis Maske für das Rich Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="dcadd-112">New event mask for the rich edit control.</span></span> <span data-ttu-id="dcadd-113">Eine Liste der Ereignis Masken finden Sie unter [**Rich Edit Control Event Mask Flags**](rich-edit-control-event-mask-flags.md).</span><span class="sxs-lookup"><span data-stu-id="dcadd-113">For a list of event masks, see [**Rich Edit Control Event Mask Flags**](rich-edit-control-event-mask-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcadd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dcadd-114">Return value</span></span>

<span data-ttu-id="dcadd-115">Diese Meldung gibt die vorherige Ereignis Maske zurück.</span><span class="sxs-lookup"><span data-stu-id="dcadd-115">This message returns the previous event mask.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcadd-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dcadd-116">Remarks</span></span>

<span data-ttu-id="dcadd-117">Die Standard Ereignis Maske (bevor Any festgelegt ist) ist "ENM \_ None".</span><span class="sxs-lookup"><span data-stu-id="dcadd-117">The default event mask (before any is set) is ENM\_NONE.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcadd-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dcadd-118">Requirements</span></span>



| <span data-ttu-id="dcadd-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcadd-119">Requirement</span></span> | <span data-ttu-id="dcadd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="dcadd-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dcadd-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dcadd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dcadd-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dcadd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dcadd-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dcadd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dcadd-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dcadd-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dcadd-125">Header</span><span class="sxs-lookup"><span data-stu-id="dcadd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcadd-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcadd-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcadd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcadd-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="dcadd-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="dcadd-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dcadd-129">**EM \_ GetEventMask**</span><span class="sxs-lookup"><span data-stu-id="dcadd-129">**EM\_GETEVENTMASK**</span></span>](em-geteventmask.md)
</dt> <dt>

[<span data-ttu-id="dcadd-130">**Rich-Flags für Bearbeitungs Steuerelemente-Ereignis Maske**</span><span class="sxs-lookup"><span data-stu-id="dcadd-130">**Rich Edit Control Event Mask Flags**</span></span>](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





