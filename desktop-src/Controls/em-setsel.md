---
title: EM_SETSEL Meldung (Winuser. h)
description: Wählt einen Bereich von Zeichen in einem Bearbeitungs Steuerelement aus. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- Windows-Steuerelemente für EM_SETSEL Meldung
topic_type:
- apiref
api_name:
- EM_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4981fa179ae4bdd454ab0b0a6d7485185ed31d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476098"
---
# <a name="em_setsel-message"></a><span data-ttu-id="4ad5e-105">EM-Aktivität \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="4ad5e-105">EM\_SETSEL message</span></span>

<span data-ttu-id="4ad5e-106">Wählt einen Bereich von Zeichen in einem Bearbeitungs Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-106">Selects a range of characters in an edit control.</span></span> <span data-ttu-id="4ad5e-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4ad5e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ad5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ad5e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ad5e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ad5e-110">Die Anfangs Zeichenposition der Auswahl.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-110">The starting character position of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="4ad5e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ad5e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ad5e-112">Die Position des Endzeichens der Auswahl.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-112">The ending character position of the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ad5e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4ad5e-113">Return value</span></span>

<span data-ttu-id="4ad5e-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ad5e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ad5e-115">Remarks</span></span>

<span data-ttu-id="4ad5e-116">Der Startwert kann größer als der Endwert sein.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-116">The start value can be greater than the end value.</span></span> <span data-ttu-id="4ad5e-117">Der untere der beiden Werte gibt die Zeichenposition des ersten Zeichens in der Auswahl an.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-117">The lower of the two values specifies the character position of the first character in the selection.</span></span> <span data-ttu-id="4ad5e-118">Der höhere Wert gibt die Position des ersten Zeichens außerhalb der Auswahl an.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-118">The higher value specifies the position of the first character beyond the selection.</span></span>

<span data-ttu-id="4ad5e-119">Der Startwert ist der Ankerpunkt der Auswahl, und der Endwert ist das aktive Ende.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-119">The start value is the anchor point of the selection, and the end value is the active end.</span></span> <span data-ttu-id="4ad5e-120">Wenn der Benutzer die UMSCHALTTASTE verwendet, um die Größe der Auswahl anzupassen, kann das aktive Ende verschoben werden, der Ankerpunkt bleibt jedoch unverändert.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-120">If the user uses the SHIFT key to adjust the size of the selection, the active end can move but the anchor point remains the same.</span></span>

<span data-ttu-id="4ad5e-121">Wenn der Start Wert 0 und das Ende-1 ist, wird der gesamte Text im Bearbeitungs Steuerelement ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-121">If the start is 0 and the end is -1, all the text in the edit control is selected.</span></span> <span data-ttu-id="4ad5e-122">Wenn der Start-1 ist, wird jede aktuelle Auswahl deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-122">If the start is -1, any current selection is deselected.</span></span>

<span data-ttu-id="4ad5e-123">Steuer **Elemente bearbeiten:** Das-Steuerelement zeigt einen blinkenden Caretzeichen an der Endposition an, unabhängig von den relativen Werten von Start und Ende.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-123">**Edit controls:** The control displays a flashing caret at the end position regardless of the relative values of start and end.</span></span>

<span data-ttu-id="4ad5e-124">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-124">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="4ad5e-125">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="4ad5e-126">Wenn das Bearbeitungs Steuerelement den [**es \_ nohidesel**](edit-control-styles.md) -Stil hat, wird der ausgewählte Text unabhängig davon hervorgehoben, ob das Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-126">If the edit control has the [**ES\_NOHIDESEL**](edit-control-styles.md) style, the selected text is highlighted regardless of whether the control has focus.</span></span> <span data-ttu-id="4ad5e-127">Ohne den **es \_ nohidesel** -Stil wird der ausgewählte Text nur hervorgehoben, wenn das Bearbeitungs Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="4ad5e-127">Without the **ES\_NOHIDESEL** style, the selected text is highlighted only when the edit control has the focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ad5e-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ad5e-128">Requirements</span></span>



| <span data-ttu-id="4ad5e-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ad5e-129">Requirement</span></span> | <span data-ttu-id="4ad5e-130">Wert</span><span class="sxs-lookup"><span data-stu-id="4ad5e-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad5e-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ad5e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4ad5e-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ad5e-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4ad5e-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ad5e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4ad5e-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4ad5e-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4ad5e-135">Header</span><span class="sxs-lookup"><span data-stu-id="4ad5e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ad5e-136"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="4ad5e-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ad5e-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ad5e-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="4ad5e-138">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="4ad5e-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4ad5e-139">**EM- \_ GetSEL**</span><span class="sxs-lookup"><span data-stu-id="4ad5e-139">**EM\_GETSEL**</span></span>](em-getsel.md)
</dt> <dt>

[<span data-ttu-id="4ad5e-140">**EM \_ replacesel**</span><span class="sxs-lookup"><span data-stu-id="4ad5e-140">**EM\_REPLACESEL**</span></span>](em-replacesel.md)
</dt> <dt>

[<span data-ttu-id="4ad5e-141">**EM \_ scrollcaret**</span><span class="sxs-lookup"><span data-stu-id="4ad5e-141">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
</dt> <dt>

[<span data-ttu-id="4ad5e-142">**EM- \_ Ex-tsel**</span><span class="sxs-lookup"><span data-stu-id="4ad5e-142">**EM\_EXSETSEL**</span></span>](em-exsetsel.md)
</dt> </dl>

 

 





