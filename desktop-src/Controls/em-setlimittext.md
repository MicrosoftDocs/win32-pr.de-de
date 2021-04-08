---
title: EM_SETLIMITTEXT Meldung (Winuser. h)
description: Legt den Text Grenzwert eines Bearbeitungs Steuer Elements fest.
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- Windows-Steuerelemente für EM_SETLIMITTEXT Meldung
topic_type:
- apiref
api_name:
- EM_SETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c138e6d7fed75fa8da2e7a6b93308632c250e7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742008"
---
# <a name="em_setlimittext-message"></a><span data-ttu-id="bdff6-104">EM \_ SetLimitText-Nachricht</span><span class="sxs-lookup"><span data-stu-id="bdff6-104">EM\_SETLIMITTEXT message</span></span>

<span data-ttu-id="bdff6-105">Legt den Text Grenzwert eines Bearbeitungs Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="bdff6-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="bdff6-106">Das Text Limit ist die maximale Text Menge in **TCHAR** s, die der Benutzer in das Bearbeitungs Steuerelement eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="bdff6-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="bdff6-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="bdff6-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="bdff6-108">Für Bearbeitungs Steuerelemente und Microsoft Rich Edit 1,0 werden Bytes verwendet.</span><span class="sxs-lookup"><span data-stu-id="bdff6-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="bdff6-109">Für Microsoft Rich Edit 2,0 und höher werden Zeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="bdff6-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

<span data-ttu-id="bdff6-110">Die **EM- \_ SetLimitText** -Nachricht ist mit der [**EM- \_ limittext**](em-limittext.md) Nachricht identisch.</span><span class="sxs-lookup"><span data-stu-id="bdff6-110">The **EM\_SETLIMITTEXT** message is identical to the [**EM\_LIMITTEXT**](em-limittext.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="bdff6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdff6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdff6-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bdff6-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdff6-113">Die maximale Anzahl von **TCHAR**-s, die der Benutzer eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="bdff6-113">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="bdff6-114">Bei ANSI-Text ist dies die Anzahl der Bytes. bei Unicode-Text ist dies die Anzahl der Zeichen.</span><span class="sxs-lookup"><span data-stu-id="bdff6-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="bdff6-115">Diese Zahl umfasst nicht das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="bdff6-115">This number does not include the terminating null character.</span></span>

<span data-ttu-id="bdff6-116">**Rich Edit-Steuerelemente:** Wenn dieser Parameter 0 (null) ist, wird die Textlänge auf 64.000 Zeichen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bdff6-116">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="bdff6-117">Wenn dieser Parameter 0 (null) ist, wird die Textlänge für einzeilige Bearbeitungs Steuerelemente auf 0x7ffffffe-Zeichen oder für mehrzeilige Bearbeitungs Steuerelemente auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bdff6-117">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or  1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="bdff6-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bdff6-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bdff6-119">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bdff6-119">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdff6-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdff6-120">Return value</span></span>

<span data-ttu-id="bdff6-121">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bdff6-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdff6-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bdff6-122">Remarks</span></span>

<span data-ttu-id="bdff6-123">Die " **EM \_ SetLimitText** "-Nachricht schränkt nur den Text ein, den der Benutzer eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="bdff6-123">The **EM\_SETLIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="bdff6-124">Er wirkt sich nicht auf Text aus, der sich bereits im Bearbeitungs Steuerelement befindet, wenn die Nachricht gesendet wird, und wirkt sich nicht auf die Länge des Texts aus, der durch die [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext) -Nachricht in das Bearbeitungs Steuerelement kopiert wird</span><span class="sxs-lookup"><span data-stu-id="bdff6-124">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="bdff6-125">Wenn eine Anwendung die **WM- \_ SetText** -Nachricht verwendet, um mehr Text in ein Bearbeitungs Steuerelement zu platzieren, als in der **EM- \_ SetLimitText** -Meldung angegeben ist, kann der Benutzer den gesamten Inhalt des Bearbeitungs Steuer Elements bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="bdff6-125">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_SETLIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="bdff6-126">Bevor **EM \_ SetLimitText** aufgerufen wird, ist der Standard Grenzwert für die Textmenge, die ein Benutzer in einem Bearbeitungs Steuerelement eingeben kann, 32.767 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="bdff6-126">Before **EM\_SETLIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="bdff6-127">Für einzeilige Bearbeitungs Steuerelemente ist das Text Limit entweder 0x7ffffffe Bytes oder der Wert des *wParam* -Parameters, je nachdem, welcher Wert kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="bdff6-127">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="bdff6-128">Für mehrzeilige Bearbeitungs Steuerelemente ist dieser Wert entweder 1 Byte oder der Wert des *wParam* -Parameters, je nachdem, welcher Wert kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="bdff6-128">For multiline edit controls, this value is either  1 bytes or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="bdff6-129">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bdff6-129">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="bdff6-130">Verwenden Sie den [**\_ exlimittext**](em-exlimittext.md) der Nachricht EM für Textlängen Werte größer als 64.000.</span><span class="sxs-lookup"><span data-stu-id="bdff6-130">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="bdff6-131">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="bdff6-131">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdff6-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdff6-132">Requirements</span></span>



| <span data-ttu-id="bdff6-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdff6-133">Requirement</span></span> | <span data-ttu-id="bdff6-134">Wert</span><span class="sxs-lookup"><span data-stu-id="bdff6-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdff6-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdff6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bdff6-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdff6-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bdff6-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdff6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bdff6-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdff6-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bdff6-139">Header</span><span class="sxs-lookup"><span data-stu-id="bdff6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdff6-140"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="bdff6-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdff6-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdff6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdff6-142">**EM \_ getlimittext**</span><span class="sxs-lookup"><span data-stu-id="bdff6-142">**EM\_GETLIMITTEXT**</span></span>](em-getlimittext.md)
</dt> </dl>

 

