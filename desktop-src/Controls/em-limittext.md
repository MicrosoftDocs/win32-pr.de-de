---
title: EM_LIMITTEXT Meldung (Winuser. h)
description: Legt den Text Grenzwert eines Bearbeitungs Steuer Elements fest.
ms.assetid: 5a605de7-8dc7-4c54-8f18-e0b08c720856
keywords:
- Windows-Steuerelemente für EM_LIMITTEXT Meldung
topic_type:
- apiref
api_name:
- EM_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf45f7ee9cfd88a25b78f0bd58911e516c146096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476107"
---
# <a name="em_limittext-message"></a><span data-ttu-id="483b4-104">EM- \_ Limit-Textnachricht</span><span class="sxs-lookup"><span data-stu-id="483b4-104">EM\_LIMITTEXT message</span></span>

<span data-ttu-id="483b4-105">Legt den Text Grenzwert eines Bearbeitungs Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="483b4-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="483b4-106">Das Text Limit ist die maximale Text Menge in **TCHAR** s, die der Benutzer in das Bearbeitungs Steuerelement eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="483b4-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="483b4-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="483b4-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="483b4-108">Für Bearbeitungs Steuerelemente und Microsoft Rich Edit 1,0 werden Bytes verwendet.</span><span class="sxs-lookup"><span data-stu-id="483b4-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="483b4-109">Für Microsoft Rich Edit 2,0 und höher werden Zeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="483b4-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

## <a name="parameters"></a><span data-ttu-id="483b4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="483b4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="483b4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="483b4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="483b4-112">Die maximale Anzahl von **TCHAR**-s, die der Benutzer eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="483b4-112">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="483b4-113">Bei ANSI-Text ist dies die Anzahl der Bytes. bei Unicode-Text ist dies die Anzahl der Zeichen.</span><span class="sxs-lookup"><span data-stu-id="483b4-113">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="483b4-114">Diese Zahl umfasst nicht das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="483b4-114">This number does not include the terminating null character.</span></span>

<span data-ttu-id="483b4-115">**Rich Edit-Steuerelemente:** Wenn dieser Parameter 0 (null) ist, wird die Textlänge auf 64.000 Zeichen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="483b4-115">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="483b4-116">Wenn dieser Parameter NULL ist, wird die Textlänge für einzeilige Bearbeitungs Steuerelemente auf 0x7ffffffe-Zeichen oder-1 für mehrzeilige Bearbeitungs Steuerelemente festgelegt.</span><span class="sxs-lookup"><span data-stu-id="483b4-116">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or -1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="483b4-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="483b4-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="483b4-118">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="483b4-118">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="483b4-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="483b4-119">Return value</span></span>

<span data-ttu-id="483b4-120">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="483b4-120">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="483b4-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="483b4-121">Remarks</span></span>

<span data-ttu-id="483b4-122">Die **EM- \_ limittext** -Nachricht schränkt nur den Text ein, den der Benutzer eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="483b4-122">The **EM\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="483b4-123">Er wirkt sich nicht auf Text aus, der sich bereits im Bearbeitungs Steuerelement befindet, wenn die Nachricht gesendet wird, und wirkt sich nicht auf die Länge des Texts aus, der durch die [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext) -Nachricht in das Bearbeitungs Steuerelement kopiert wird</span><span class="sxs-lookup"><span data-stu-id="483b4-123">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="483b4-124">Wenn eine Anwendung die **WM- \_ SetText** -Nachricht verwendet, um mehr Text in ein Bearbeitungs Steuerelement zu platzieren, als in der **EM- \_ limittext** Meldung angegeben ist, kann der Benutzer den gesamten Inhalt des Bearbeitungs Steuer Elements bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="483b4-124">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_LIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="483b4-125">Vor dem Aufrufen von **EM- \_ Begrenzungs Text** beträgt der Standard Grenzwert für die Text Menge, die ein Benutzer in einem Bearbeitungs Steuerelement eingeben kann, 32.767 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="483b4-125">Before **EM\_LIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="483b4-126">Für einzeilige Bearbeitungs Steuerelemente ist das Text Limit entweder 0x7ffffffe Bytes oder der Wert des *wParam* -Parameters, je nachdem, welcher Wert kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="483b4-126">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="483b4-127">Für mehrzeilige Bearbeitungs Steuerelemente ist dieser Wert entweder-1 Byte oder der Wert des *wParam* -Parameters, je nachdem, welcher Wert kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="483b4-127">For multiline edit controls, this value is either -1 byte or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="483b4-128">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="483b4-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="483b4-129">Verwenden Sie den [**\_ exlimittext**](em-exlimittext.md) der Nachricht EM für Textlängen Werte größer als 64.000.</span><span class="sxs-lookup"><span data-stu-id="483b4-129">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="483b4-130">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="483b4-130">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="483b4-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="483b4-131">Requirements</span></span>



| <span data-ttu-id="483b4-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="483b4-132">Requirement</span></span> | <span data-ttu-id="483b4-133">Wert</span><span class="sxs-lookup"><span data-stu-id="483b4-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="483b4-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="483b4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="483b4-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="483b4-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="483b4-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="483b4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="483b4-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="483b4-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="483b4-138">Header</span><span class="sxs-lookup"><span data-stu-id="483b4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="483b4-139"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="483b4-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="483b4-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="483b4-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="483b4-141">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="483b4-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="483b4-142">**EM- \_ exlimittext**</span><span class="sxs-lookup"><span data-stu-id="483b4-142">**EM\_EXLIMITTEXT**</span></span>](em-exlimittext.md)
</dt> <dt>

[<span data-ttu-id="483b4-143">**\_Limittext bearbeiten**</span><span class="sxs-lookup"><span data-stu-id="483b4-143">**Edit\_LimitText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
</dt> <dt>

<span data-ttu-id="483b4-144">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="483b4-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="483b4-145">**WM- \_ SetText**</span><span class="sxs-lookup"><span data-stu-id="483b4-145">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

