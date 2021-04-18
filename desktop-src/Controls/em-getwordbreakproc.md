---
title: EM_GETWORDBREAKPROC Meldung (Winuser. h)
description: Ruft die Adresse der aktuellen WordWrap-Funktion ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- Windows-Steuerelemente für EM_GETWORDBREAKPROC Meldung
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb9499492668abac24774b66304ae8a87a2d739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478108"
---
# <a name="em_getwordbreakproc-message"></a><span data-ttu-id="89cd0-105">EM \_ getwordbreakproc-Meldung</span><span class="sxs-lookup"><span data-stu-id="89cd0-105">EM\_GETWORDBREAKPROC message</span></span>

<span data-ttu-id="89cd0-106">Ruft die Adresse der aktuellen WordWrap-Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="89cd0-106">Gets the address of the current Wordwrap function.</span></span> <span data-ttu-id="89cd0-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="89cd0-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="89cd0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="89cd0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89cd0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89cd0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89cd0-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="89cd0-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="89cd0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89cd0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89cd0-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="89cd0-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89cd0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89cd0-113">Return value</span></span>

<span data-ttu-id="89cd0-114">Der Rückgabewert gibt die Adresse der Anwendungs definierten WordWrap-Funktion an.</span><span class="sxs-lookup"><span data-stu-id="89cd0-114">The return value specifies the address of the application-defined Wordwrap function.</span></span> <span data-ttu-id="89cd0-115">Der Rückgabewert ist **null** , wenn keine WordWrap-Funktion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="89cd0-115">The return value is **NULL** if no Wordwrap function exists.</span></span>

## <a name="remarks"></a><span data-ttu-id="89cd0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89cd0-116">Remarks</span></span>

<span data-ttu-id="89cd0-117">Eine WordWrap-Funktion scannt einen Text Puffer, der Text enthält, der an die Anzeige gesendet werden soll, und sucht nach dem ersten Wort, das nicht in die aktuelle Anzeige Zeile passt.</span><span class="sxs-lookup"><span data-stu-id="89cd0-117">A Wordwrap function scans a text buffer that contains text to be sent to the display, looking for the first word that does not fit on the current display line.</span></span> <span data-ttu-id="89cd0-118">Die WordWrap-Funktion platziert dieses Wort am Anfang der nächsten Zeile auf der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="89cd0-118">The wordwrap function places this word at the beginning of the next line on the display.</span></span> <span data-ttu-id="89cd0-119">Eine WordWrap-Funktion definiert den Punkt, an dem das System eine Textzeile für mehrzeilige Bearbeitungs Steuerelemente unterbrechen soll, in der Regel bei einem Leerzeichen, das zwei Wörter trennt.</span><span class="sxs-lookup"><span data-stu-id="89cd0-119">A Wordwrap function defines the point at which the system should break a line of text for multiline edit controls, usually at a space character that separates two words.</span></span>

<span data-ttu-id="89cd0-120">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89cd0-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="89cd0-121">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="89cd0-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89cd0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89cd0-122">Requirements</span></span>



| <span data-ttu-id="89cd0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89cd0-123">Requirement</span></span> | <span data-ttu-id="89cd0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="89cd0-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89cd0-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89cd0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="89cd0-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89cd0-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="89cd0-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89cd0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="89cd0-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89cd0-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="89cd0-129">Header</span><span class="sxs-lookup"><span data-stu-id="89cd0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="89cd0-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="89cd0-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89cd0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89cd0-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="89cd0-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="89cd0-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="89cd0-133">*Editwordbreakproc*</span><span class="sxs-lookup"><span data-stu-id="89cd0-133">*EditWordBreakProc*</span></span>](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[<span data-ttu-id="89cd0-134">**EM- \_ Zeilen Trennlinien**</span><span class="sxs-lookup"><span data-stu-id="89cd0-134">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
</dt> <dt>

[<span data-ttu-id="89cd0-135">**EM \_ setwordbreakproc**</span><span class="sxs-lookup"><span data-stu-id="89cd0-135">**EM\_SETWORDBREAKPROC**</span></span>](em-setwordbreakproc.md)
</dt> </dl>

 

