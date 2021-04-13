---
title: EM_SETWORDBREAKPROC Meldung (Winuser. h)
description: Ersetzt die Standard-WordWrap-Funktion eines Bearbeitungs Steuer Elements durch eine Anwendungs definierte WordWrap-Funktion. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- Windows-Steuerelemente für EM_SETWORDBREAKPROC Meldung
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e85335562c9e9881093d89293e7e2ace9cf43b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517975"
---
# <a name="em_setwordbreakproc-message"></a><span data-ttu-id="bc2a5-105">EM \_ setwordbreakproc-Meldung</span><span class="sxs-lookup"><span data-stu-id="bc2a5-105">EM\_SETWORDBREAKPROC message</span></span>

<span data-ttu-id="bc2a5-106">Ersetzt die Standard-WordWrap-Funktion eines Bearbeitungs Steuer Elements durch eine Anwendungs definierte WordWrap-Funktion.</span><span class="sxs-lookup"><span data-stu-id="bc2a5-106">Replaces an edit control's default Wordwrap function with an application-defined Wordwrap function.</span></span> <span data-ttu-id="bc2a5-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="bc2a5-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc2a5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc2a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc2a5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc2a5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc2a5-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bc2a5-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="bc2a5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc2a5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc2a5-112">Die Adresse der Anwendungs definierten WordWrap-Funktion.</span><span class="sxs-lookup"><span data-stu-id="bc2a5-112">The address of the application-defined Wordwrap function.</span></span> <span data-ttu-id="bc2a5-113">Weitere Informationen zu Zeilenumbruch finden Sie in der Beschreibung der [*editwordbreakproc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) -Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="bc2a5-113">For more information about breaking lines, see the description of the [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc2a5-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc2a5-114">Return value</span></span>

<span data-ttu-id="bc2a5-115">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bc2a5-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc2a5-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc2a5-116">Remarks</span></span>

<span data-ttu-id="bc2a5-117">Eine WordWrap-Funktion scannt einen Text Puffer, der Text enthält, der an den Bildschirm gesendet werden soll, und sucht nach dem ersten Wort, das nicht in die aktuelle Bildschirm Zeile passt.</span><span class="sxs-lookup"><span data-stu-id="bc2a5-117">A Wordwrap function scans a text buffer that contains text to be sent to the screen, looking for the first word that does not fit on the current screen line.</span></span> <span data-ttu-id="bc2a5-118">Die WordWrap-Funktion legt dieses Wort am Anfang der nächsten Zeile auf dem Bildschirm ab.</span><span class="sxs-lookup"><span data-stu-id="bc2a5-118">The Wordwrap function places this word at the beginning of the next line on the screen.</span></span>

<span data-ttu-id="bc2a5-119">Eine WordWrap-Funktion definiert den Punkt, an dem das System eine Textzeile für mehrzeilige Bearbeitungs Steuerelemente unterbrechen soll, in der Regel bei einem Leerzeichen, das zwei Wörter trennt.</span><span class="sxs-lookup"><span data-stu-id="bc2a5-119">A Wordwrap function defines the point at which the system should break a line of text for multiline edit controls, usually at a space character that separates two words.</span></span> <span data-ttu-id="bc2a5-120">Diese Funktion kann entweder von einem mehrzeiligen oder einem einzeiligen Bearbeitungs Steuerelement aufgerufen werden, wenn der Benutzer die Pfeiltasten in Kombination mit der STRG-Taste drückt, um die Einfügemarke zum nächsten Wort oder zum vorherigen Wort zu bewegen.</span><span class="sxs-lookup"><span data-stu-id="bc2a5-120">Either a multiline or a single-line edit control might call this function when the user presses arrow keys in combination with the CTRL key to move the caret to the next word or previous word.</span></span> <span data-ttu-id="bc2a5-121">Die standardmäßige WordWrap-Funktion unterbricht eine Textzeile bei einem Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="bc2a5-121">The default Wordwrap function breaks a line of text at a space character.</span></span> <span data-ttu-id="bc2a5-122">Die Anwendungs definierte Funktion definiert möglicherweise, dass der WordWrap-Vorgang bei einem Bindestrich oder einem anderen als dem Leerzeichen auftritt.</span><span class="sxs-lookup"><span data-stu-id="bc2a5-122">The application-defined function may define the Wordwrap to occur at a hyphen or a character other than the space character.</span></span>

<span data-ttu-id="bc2a5-123">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bc2a5-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="bc2a5-124">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="bc2a5-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc2a5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc2a5-125">Requirements</span></span>



| <span data-ttu-id="bc2a5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc2a5-126">Requirement</span></span> | <span data-ttu-id="bc2a5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="bc2a5-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc2a5-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc2a5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bc2a5-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc2a5-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bc2a5-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc2a5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bc2a5-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc2a5-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bc2a5-132">Header</span><span class="sxs-lookup"><span data-stu-id="bc2a5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc2a5-133"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="bc2a5-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc2a5-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc2a5-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc2a5-135">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="bc2a5-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bc2a5-136">*Editwordbreakproc*</span><span class="sxs-lookup"><span data-stu-id="bc2a5-136">*EditWordBreakProc*</span></span>](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[<span data-ttu-id="bc2a5-137">**EM- \_ Zeilen Trennlinien**</span><span class="sxs-lookup"><span data-stu-id="bc2a5-137">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
</dt> <dt>

[<span data-ttu-id="bc2a5-138">**EM \_ getwordbreakproc**</span><span class="sxs-lookup"><span data-stu-id="bc2a5-138">**EM\_GETWORDBREAKPROC**</span></span>](em-getwordbreakproc.md)
</dt> </dl>

 

