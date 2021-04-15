---
title: EM_EMPTYUNDOBUFFER Meldung (Winuser. h)
description: Setzt das rückgängig-Flag eines Bearbeitungs Steuer Elements zurück. Das rückgängigflag wird festgelegt, wenn ein Vorgang innerhalb des Bearbeitungs Steuer Elements rückgängig gemacht werden kann. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- Windows-Steuerelemente für EM_EMPTYUNDOBUFFER Meldung
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abbdc067b603a032b8d311ddd7930a8ca6de01c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477604"
---
# <a name="em_emptyundobuffer-message"></a><span data-ttu-id="e171d-106">Nachricht "em \_ emptyundobuffer"</span><span class="sxs-lookup"><span data-stu-id="e171d-106">EM\_EMPTYUNDOBUFFER message</span></span>

<span data-ttu-id="e171d-107">Setzt das rückgängig-Flag eines Bearbeitungs Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="e171d-107">Resets the undo flag of an edit control.</span></span> <span data-ttu-id="e171d-108">Das rückgängigflag wird festgelegt, wenn ein Vorgang innerhalb des Bearbeitungs Steuer Elements rückgängig gemacht werden kann.</span><span class="sxs-lookup"><span data-stu-id="e171d-108">The undo flag is set whenever an operation within the edit control can be undone.</span></span> <span data-ttu-id="e171d-109">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="e171d-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e171d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e171d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e171d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e171d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e171d-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="e171d-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e171d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e171d-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e171d-114">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="e171d-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e171d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e171d-115">Return value</span></span>

<span data-ttu-id="e171d-116">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e171d-116">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e171d-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e171d-117">Remarks</span></span>

<span data-ttu-id="e171d-118">Das rückgängig-Flag wird automatisch zurückgesetzt, wenn das Bearbeitungs Steuerelement eine [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext) -oder [**EM \_ SetHandle**](em-sethandle.md) -Meldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="e171d-118">The undo flag is automatically reset whenever the edit control receives a [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) or [**EM\_SETHANDLE**](em-sethandle.md) message.</span></span>

<span data-ttu-id="e171d-119">**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 1,0:** Das Steuerelement kann nur den letzten Vorgang rückgängig machen oder wiederholen.</span><span class="sxs-lookup"><span data-stu-id="e171d-119">**Edit controls and Rich Edit 1.0:** The control can only undo or redo the most recent operation.</span></span>

<span data-ttu-id="e171d-120">**Rich Edit 2,0 und höher:** Die Nachricht " **EM \_ emptyundobuffer** " Leert alle rückgängig-und Wiederholungs Puffer.</span><span class="sxs-lookup"><span data-stu-id="e171d-120">**Rich Edit 2.0 and later:** The **EM\_EMPTYUNDOBUFFER** message empties all undo and redo buffers.</span></span> <span data-ttu-id="e171d-121">Rich Edit-Steuerelemente ermöglichen dem Benutzer das Rückgängigmachen oder wiederholen mehrerer Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e171d-121">Rich edit controls enable the user to undo or redo multiple operations.</span></span>

<span data-ttu-id="e171d-122">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e171d-122">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="e171d-123">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="e171d-123">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e171d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e171d-124">Requirements</span></span>



| <span data-ttu-id="e171d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e171d-125">Requirement</span></span> | <span data-ttu-id="e171d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e171d-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e171d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e171d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e171d-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e171d-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e171d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e171d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e171d-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e171d-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e171d-131">Header</span><span class="sxs-lookup"><span data-stu-id="e171d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e171d-132"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="e171d-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e171d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e171d-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="e171d-134">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e171d-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e171d-135">**EM \_ CanUndo**</span><span class="sxs-lookup"><span data-stu-id="e171d-135">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> <dt>

[<span data-ttu-id="e171d-136">**EM- \_ andle**</span><span class="sxs-lookup"><span data-stu-id="e171d-136">**EM\_SETHANDLE**</span></span>](em-sethandle.md)
</dt> <dt>

[<span data-ttu-id="e171d-137">**EM \_ rückgängig machen**</span><span class="sxs-lookup"><span data-stu-id="e171d-137">**EM\_UNDO**</span></span>](em-undo.md)
</dt> <dt>

<span data-ttu-id="e171d-138">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="e171d-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e171d-139">**WM- \_ SetText**</span><span class="sxs-lookup"><span data-stu-id="e171d-139">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

