---
title: EM_SETMODIFY Meldung (Winuser. h)
description: Legt das Änderungsflag für ein Bearbeitungs Steuerelement fest oder löscht dieses. Das Änderungsflag gibt an, ob der Text im Bearbeitungs Steuerelement geändert wurde. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Windows-Steuerelemente für EM_SETMODIFY Meldung
topic_type:
- apiref
api_name:
- EM_SETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 591b57dbc5441e96c1c6d3963172864713ed939f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859012"
---
# <a name="em_setmodify-message"></a><span data-ttu-id="9f103-106">EM- \_ setmodify-Meldung</span><span class="sxs-lookup"><span data-stu-id="9f103-106">EM\_SETMODIFY message</span></span>

<span data-ttu-id="9f103-107">Legt das Änderungsflag für ein Bearbeitungs Steuerelement fest oder löscht dieses.</span><span class="sxs-lookup"><span data-stu-id="9f103-107">Sets or clears the modification flag for an edit control.</span></span> <span data-ttu-id="9f103-108">Das Änderungsflag gibt an, ob der Text im Bearbeitungs Steuerelement geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="9f103-108">The modification flag indicates whether the text within the edit control has been modified.</span></span> <span data-ttu-id="9f103-109">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="9f103-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f103-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f103-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f103-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f103-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f103-112">Der neue Wert für das Änderungsflag.</span><span class="sxs-lookup"><span data-stu-id="9f103-112">The new value for the modification flag.</span></span> <span data-ttu-id="9f103-113">Der Wert **true** gibt an, dass der Text geändert wurde, und der Wert **false** gibt an, dass er nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="9f103-113">A value of **TRUE** indicates the text has been modified, and a value of **FALSE** indicates it has not been modified.</span></span>

</dd> <dt>

<span data-ttu-id="9f103-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f103-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f103-115">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f103-115">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f103-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f103-116">Return value</span></span>

<span data-ttu-id="9f103-117">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9f103-117">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f103-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f103-118">Remarks</span></span>

<span data-ttu-id="9f103-119">Wenn das Steuerelement erstellt wird, löscht das System das Änderungsflag automatisch auf 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9f103-119">The system automatically clears the modification flag to zero when the control is created.</span></span> <span data-ttu-id="9f103-120">Wenn der Benutzer den Text des Steuer Elements ändert, legt das System das Flag auf einen Wert ungleich 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="9f103-120">If the user changes the control's text, the system sets the flag to nonzero.</span></span> <span data-ttu-id="9f103-121">Sie können die [**EM \_ getmodify**](em-getmodify.md) -Nachricht an das Bearbeitungs Steuerelement senden, um den aktuellen Status des Flags abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9f103-121">You can send the [**EM\_GETMODIFY**](em-getmodify.md) message to the edit control to retrieve the current state of the flag.</span></span>

<span data-ttu-id="9f103-122">**Rich Edit 1,0:** Objekte, die ohne das **REO \_ dynamicsize** -Flag erstellt werden, Sperren Ihre Blöcke, wenn das Modify-Flag auf " **false**" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9f103-122">**Rich Edit 1.0:** Objects created without the **REO\_DYNAMICSIZE** flag will lock in their extents when the modify flag is set to **FALSE**.</span></span>

<span data-ttu-id="9f103-123">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f103-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="9f103-124">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="9f103-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f103-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f103-125">Requirements</span></span>



| <span data-ttu-id="9f103-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f103-126">Requirement</span></span> | <span data-ttu-id="9f103-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9f103-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f103-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f103-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9f103-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f103-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9f103-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f103-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9f103-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f103-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9f103-132">Header</span><span class="sxs-lookup"><span data-stu-id="9f103-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f103-133"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9f103-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f103-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f103-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="9f103-135">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9f103-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9f103-136">**EM \_ getmodify**</span><span class="sxs-lookup"><span data-stu-id="9f103-136">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
</dt> <dt>

[<span data-ttu-id="9f103-137">**Reobject**</span><span class="sxs-lookup"><span data-stu-id="9f103-137">**REOBJECT**</span></span>](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





