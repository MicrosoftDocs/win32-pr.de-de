---
title: EM_SETLIMITTEXT (Winuser.h)
description: 'EM_SETLIMITTEXT Meldung: Legt die Textgrenze eines Bearbeitungssteuerfelds fest.'
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- EM_SETLIMITTEXT Meldung Windows-Steuerelemente
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
ms.openlocfilehash: b66d4e03b5c1824ab501226482fcf51fb9121cba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109748"
---
# <a name="em_setlimittext-message"></a><span data-ttu-id="8d05a-104">EM \_ SETLIMITTEXT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8d05a-104">EM\_SETLIMITTEXT message</span></span>

<span data-ttu-id="8d05a-105">Legt die Textgrenze eines Bearbeitungssteuerfelds fest.</span><span class="sxs-lookup"><span data-stu-id="8d05a-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="8d05a-106">Die Textgrenze ist die maximale Textmenge in **TCHAR** s, die der Benutzer in das Bearbeitungssteuerfeld eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="8d05a-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="8d05a-107">Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="8d05a-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="8d05a-108">Für Bearbeitungssteuerelemente und Microsoft Rich Edit 1.0 werden Bytes verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d05a-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="8d05a-109">Für Microsoft Rich Edit 2.0 und höher werden Zeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d05a-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

<span data-ttu-id="8d05a-110">Die **EM \_ SETLIMITTEXT-Nachricht** ist mit der [**EM \_ LIMITTEXT-Nachricht**](em-limittext.md) identisch.</span><span class="sxs-lookup"><span data-stu-id="8d05a-110">The **EM\_SETLIMITTEXT** message is identical to the [**EM\_LIMITTEXT**](em-limittext.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d05a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d05a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d05a-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d05a-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d05a-113">Die maximale Anzahl von **TCHAR-S,** die der Benutzer eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="8d05a-113">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="8d05a-114">Für ANSI-Text ist dies die Anzahl von Bytes. für Unicode-Text ist dies die Anzahl von Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8d05a-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="8d05a-115">Diese Zahl schließt das beendende NULL-Zeichen nicht ein.</span><span class="sxs-lookup"><span data-stu-id="8d05a-115">This number does not include the terminating null character.</span></span>

<span data-ttu-id="8d05a-116">**Umfangreiche Bearbeitungssteuerelemente:** Wenn dieser Parameter null ist, wird die Textlänge auf 64.000 Zeichen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8d05a-116">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="8d05a-117">Wenn dieser Parameter null ist, wird die Textlänge auf 0x7FFFFFFE Zeichen für einzeilenbasierte Bearbeitungssteuerelemente oder 1 für mehrzeilenbasierte Bearbeitungssteuerelemente festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8d05a-117">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or  1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="8d05a-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d05a-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d05a-119">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d05a-119">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d05a-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d05a-120">Return value</span></span>

<span data-ttu-id="8d05a-121">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8d05a-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d05a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d05a-122">Remarks</span></span>

<span data-ttu-id="8d05a-123">Die **EM \_ SETLIMITTEXT-Meldung** schränkt nur den Text ein, den der Benutzer eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="8d05a-123">The **EM\_SETLIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="8d05a-124">Sie wirkt sich weder auf Text aus, der bereits im Bearbeitungssteuerfeld enthalten ist, wenn die Nachricht gesendet wird, noch auf die Länge des Texts, der von der [**WM \_ SETTEXT-Nachricht**](/windows/desktop/winmsg/wm-settext) in das Bearbeitungssteuerfeld kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="8d05a-124">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="8d05a-125">Wenn eine Anwendung die **WM \_ SETTEXT-Nachricht** verwendet, um mehr Text in ein Bearbeitungssteuerfeld zu platzieren, als in der **EM \_ SETLIMITTEXT-Nachricht** angegeben ist, kann der Benutzer den gesamten Inhalt des Bearbeitungssteuerfelds bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8d05a-125">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_SETLIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="8d05a-126">Bevor **EM \_ SETLIMITTEXT** aufgerufen wird, beträgt der Standardgrenzwert für die Textmenge, die ein Benutzer in ein Bearbeitungssteuerfeld eingeben kann, 32.767 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8d05a-126">Before **EM\_SETLIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="8d05a-127">Bei einzeiligen Bearbeitungssteuerelementen ist der Textgrenzwert entweder 0x7FFFFFFE Bytes oder der Wert des *wParam-Parameters,* je nachdem, welcher Wert kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="8d05a-127">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="8d05a-128">Bei mehrzeiligen Bearbeitungssteuerelementen beträgt dieser Wert entweder 1 Byte oder der Wert des *wParam-Parameters,* je nachdem, welcher Wert kleiner ist.</span><span class="sxs-lookup"><span data-stu-id="8d05a-128">For multiline edit controls, this value is either  1 bytes or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="8d05a-129">**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8d05a-129">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="8d05a-130">Verwenden Sie die Meldung [**EM \_ EXLIMITTEXT**](em-exlimittext.md) für Textlängenwerte, die größer als 64.000 sind.</span><span class="sxs-lookup"><span data-stu-id="8d05a-130">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="8d05a-131">Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)</span><span class="sxs-lookup"><span data-stu-id="8d05a-131">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d05a-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d05a-132">Requirements</span></span>



| <span data-ttu-id="8d05a-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d05a-133">Requirement</span></span> | <span data-ttu-id="8d05a-134">Wert</span><span class="sxs-lookup"><span data-stu-id="8d05a-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d05a-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d05a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8d05a-136">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d05a-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8d05a-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d05a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8d05a-138">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d05a-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8d05a-139">Header</span><span class="sxs-lookup"><span data-stu-id="8d05a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d05a-140"><dt>Winuser.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="8d05a-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d05a-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8d05a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d05a-142">**EM \_ GETLIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="8d05a-142">**EM\_GETLIMITTEXT**</span></span>](em-getlimittext.md)
</dt> </dl>

 

