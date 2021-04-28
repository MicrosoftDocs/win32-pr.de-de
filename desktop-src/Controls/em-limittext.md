---
title: EM_LIMITTEXT (Winuser.h)
description: 'EM_LIMITTEXT Meldung: Legt die Textgrenze eines Bearbeitungssteuerfelds fest.'
ms.assetid: 5a605de7-8dc7-4c54-8f18-e0b08c720856
keywords:
- EM_LIMITTEXT Meldung Windows-Steuerelemente
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
ms.openlocfilehash: a80ce29d4ee5155f6b3c5c32609366982655a078
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109788"
---
# <a name="em_limittext-message"></a><span data-ttu-id="d5fae-104">EM \_ LIMITTEXT-Meldung</span><span class="sxs-lookup"><span data-stu-id="d5fae-104">EM\_LIMITTEXT message</span></span>

<span data-ttu-id="d5fae-105">Legt die Textgrenze eines Bearbeitungssteuerfelds fest.</span><span class="sxs-lookup"><span data-stu-id="d5fae-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="d5fae-106">Die Textgrenze ist die maximale Textmenge in **TCHAR** s, die der Benutzer in das Bearbeitungssteuerfeld eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="d5fae-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="d5fae-107">Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="d5fae-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="d5fae-108">Für Bearbeitungssteuerelemente und Microsoft Rich Edit 1.0 werden Bytes verwendet.</span><span class="sxs-lookup"><span data-stu-id="d5fae-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="d5fae-109">Für Microsoft Rich Edit 2.0 und höher werden Zeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d5fae-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

## <a name="parameters"></a><span data-ttu-id="d5fae-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5fae-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5fae-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d5fae-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5fae-112">Die maximale Anzahl von **TCHAR-S,** die der Benutzer eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="d5fae-112">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="d5fae-113">Für ANSI-Text ist dies die Anzahl von Bytes. für Unicode-Text ist dies die Anzahl von Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d5fae-113">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="d5fae-114">Diese Zahl schließt das beendende NULL-Zeichen nicht ein.</span><span class="sxs-lookup"><span data-stu-id="d5fae-114">This number does not include the terminating null character.</span></span>

<span data-ttu-id="d5fae-115">**Umfangreiche Bearbeitungssteuerelemente:** Wenn dieser Parameter null ist, wird die Textlänge auf 64.000 Zeichen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d5fae-115">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="d5fae-116">Wenn dieser Parameter 0 (null) ist, wird die Textlänge auf 0x7FFFFFFE Zeichen für einzeilenbasierte Bearbeitungssteuerelemente oder -1 für mehrzeilenbasierte Bearbeitungssteuerelemente festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d5fae-116">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or -1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="d5fae-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5fae-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5fae-118">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d5fae-118">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5fae-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5fae-119">Return value</span></span>

<span data-ttu-id="d5fae-120">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d5fae-120">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5fae-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5fae-121">Remarks</span></span>

<span data-ttu-id="d5fae-122">Die **EM \_ LIMITTEXT-Meldung** schränkt nur den Text ein, den der Benutzer eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="d5fae-122">The **EM\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="d5fae-123">Sie wirkt sich weder auf Text aus, der bereits im Bearbeitungssteuerfeld enthalten ist, wenn die Nachricht gesendet wird, noch auf die Länge des Texts, der von der [**WM \_ SETTEXT-Nachricht**](/windows/desktop/winmsg/wm-settext) in das Bearbeitungssteuerfeld kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="d5fae-123">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="d5fae-124">Wenn eine Anwendung die **WM \_ SETTEXT-Nachricht** verwendet, um mehr Text in ein Bearbeitungssteuerfeld zu platzieren, als in der **EM \_ LIMITTEXT-Meldung** angegeben ist, kann der Benutzer den gesamten Inhalt des Bearbeitungssteuerfelds bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d5fae-124">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_LIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="d5fae-125">Bevor **EM \_ LIMITTEXT** aufgerufen wird, beträgt der Standardgrenzwert für die Textmenge, die ein Benutzer in ein Bearbeitungssteuerfeld eingeben kann, 32.767 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d5fae-125">Before **EM\_LIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="d5fae-126">Bei einzeilenbasierten Bearbeitungssteuerelementen beträgt der Textgrenzwert 0x7FFFFFFE Bytes oder den Wert des *wParam-Parameters,* je nach Kleinerem.</span><span class="sxs-lookup"><span data-stu-id="d5fae-126">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="d5fae-127">Bei mehrzeiligen Bearbeitungssteuerelementen ist dieser Wert entweder -1 Byte oder der Wert des *wParam-Parameters,* je nachdem, welcher Wert kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="d5fae-127">For multiline edit controls, this value is either -1 byte or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="d5fae-128">**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d5fae-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="d5fae-129">Verwenden Sie die Meldung [**EM \_ EXLIMITTEXT**](em-exlimittext.md) für Textlängenwerte, die größer als 64.000 sind.</span><span class="sxs-lookup"><span data-stu-id="d5fae-129">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="d5fae-130">Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)</span><span class="sxs-lookup"><span data-stu-id="d5fae-130">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5fae-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5fae-131">Requirements</span></span>



| <span data-ttu-id="d5fae-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5fae-132">Requirement</span></span> | <span data-ttu-id="d5fae-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d5fae-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5fae-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5fae-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d5fae-135">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5fae-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d5fae-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5fae-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d5fae-137">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5fae-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d5fae-138">Header</span><span class="sxs-lookup"><span data-stu-id="d5fae-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5fae-139"><dt>Winuser.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d5fae-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5fae-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d5fae-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5fae-141">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d5fae-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d5fae-142">**EM \_ EXLIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="d5fae-142">**EM\_EXLIMITTEXT**</span></span>](em-exlimittext.md)
</dt> <dt>

[<span data-ttu-id="d5fae-143">**Bearbeiten von \_ LimitText**</span><span class="sxs-lookup"><span data-stu-id="d5fae-143">**Edit\_LimitText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
</dt> <dt>

<span data-ttu-id="d5fae-144">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="d5fae-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d5fae-145">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="d5fae-145">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

