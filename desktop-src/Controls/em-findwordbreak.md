---
title: EM_FINDWORDBREAK Meldung (RichEdit. h)
description: Sucht das nächste Wort Umbruch vor oder nach der angegebenen Zeichenposition oder ruft Informationen über das Zeichen an dieser Position ab.
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- Windows-Steuerelemente für EM_FINDWORDBREAK Meldung
topic_type:
- apiref
api_name:
- EM_FINDWORDBREAK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6533358c0f4f521bc7021e290dfe11d66d4499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477121"
---
# <a name="em_findwordbreak-message"></a><span data-ttu-id="d2b1e-104">EM \_ findwordbreak-Meldung</span><span class="sxs-lookup"><span data-stu-id="d2b1e-104">EM\_FINDWORDBREAK message</span></span>

<span data-ttu-id="d2b1e-105">Sucht das nächste Wort Umbruch vor oder nach der angegebenen Zeichenposition oder ruft Informationen über das Zeichen an dieser Position ab.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-105">Finds the next word break before or after the specified character position or retrieves information about the character at that position.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2b1e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2b1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2b1e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2b1e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2b1e-108">Gibt den Suchvorgang an.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-108">Specifies the find operation.</span></span> <span data-ttu-id="d2b1e-109">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d2b1e-110">Wert</span><span class="sxs-lookup"><span data-stu-id="d2b1e-110">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="d2b1e-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d2b1e-111">Meaning</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <span data-ttu-id="d2b1e-112"><dt>**WB- \_ Klassifizierung**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1e-112"><dt>**WB\_CLASSIFY**</dt></span></span> </dl>                | <span data-ttu-id="d2b1e-113">Gibt die Zeichenklasse und die Wort Umbruch Flags des Zeichens an der angegebenen Position zurück.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-113">Returns the character class and word-break flags of the character at the specified position.</span></span><br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <span data-ttu-id="d2b1e-114"><dt>**WB- \_ isdelimiter**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1e-114"><dt>**WB\_ISDELIMITER**</dt></span></span> </dl>       | <span data-ttu-id="d2b1e-115">Gibt **true** zurück, wenn das Zeichen an der angegebenen Position ein Trennzeichen ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="d2b1e-115">Returns **TRUE** if the character at the specified position is a delimiter, or **FALSE** otherwise.</span></span><br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <span data-ttu-id="d2b1e-116"><dt>**WB \_ Links**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1e-116"><dt>**WB\_LEFT**</dt></span></span> </dl>                            | <span data-ttu-id="d2b1e-117">Sucht das nächste Zeichen vor der angegebenen Position, die ein Wort beginnt.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-117">Finds the nearest character before the specified position that begins a word.</span></span><br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <span data-ttu-id="d2b1e-118"><dt>**WB \_ leftbreak**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1e-118"><dt>**WB\_LEFTBREAK**</dt></span></span> </dl>             | <span data-ttu-id="d2b1e-119">Sucht das nächste Wort Ende vor der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-119">Finds the next word end before the specified position.</span></span> <span data-ttu-id="d2b1e-120">Dieser Wert entspricht dem Wert von WB \_ prevbreak.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-120">This value is the same as WB\_PREVBREAK.</span></span><br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <span data-ttu-id="d2b1e-121"><dt>**WB-" \_ muvewordleft"**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1e-121"><dt>**WB\_MOVEWORDLEFT**</dt></span></span> </dl>    | <span data-ttu-id="d2b1e-122">Sucht das nächste Zeichen, das ein Wort vor der angegebenen Position beginnt.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-122">Finds the next character that begins a word before the specified position.</span></span> <span data-ttu-id="d2b1e-123">Dieser Wert wird bei der Verarbeitung von STRG + nach-links-Pfeiltaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-123">This value is used during CTRL+LEFT ARROW key processing.</span></span> <span data-ttu-id="d2b1e-124">Dieser Wert ähnelt dem Wert von "WB" \_ .</span><span class="sxs-lookup"><span data-stu-id="d2b1e-124">This value is the similar to WB\_MOVEWORDPREV.</span></span> <span data-ttu-id="d2b1e-125">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-125">See Remarks for more information.</span></span><br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <span data-ttu-id="d2b1e-126"><dt>**WB-" \_ muvewordright"**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1e-126"><dt>**WB\_MOVEWORDRIGHT**</dt></span></span> </dl> | <span data-ttu-id="d2b1e-127">Sucht das nächste Zeichen, das ein Wort nach der angegebenen Position beginnt.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-127">Finds the next character that begins a word after the specified position.</span></span> <span data-ttu-id="d2b1e-128">Dieser Wert wird bei der STRG + right Key-Verarbeitung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-128">This value is used during CTRL+right key processing.</span></span> <span data-ttu-id="d2b1e-129">Dieser Wert ähnelt dem Wert von WB " \_ muvewordnext".</span><span class="sxs-lookup"><span data-stu-id="d2b1e-129">This value is similar to WB\_MOVEWORDNEXT.</span></span> <span data-ttu-id="d2b1e-130">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-130">See Remarks for more information.</span></span><br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <span data-ttu-id="d2b1e-131"><dt>**WB \_ Rechts**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1e-131"><dt>**WB\_RIGHT**</dt></span></span> </dl>                         | <span data-ttu-id="d2b1e-132">Sucht das nächste Zeichen, das ein Wort nach der angegebenen Position beginnt.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-132">Finds the next character that begins a word after the specified position.</span></span><br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <span data-ttu-id="d2b1e-133"><dt>**WB- \_ rightbreak**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1e-133"><dt>**WB\_RIGHTBREAK**</dt></span></span> </dl>          | <span data-ttu-id="d2b1e-134">Sucht das nächste Wort Ende-Trennzeichen nach der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-134">Finds the next end-of-word delimiter after the specified position.</span></span> <span data-ttu-id="d2b1e-135">Dieser Wert entspricht dem Wert von WB \_ nextbreak.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-135">This value is the same as WB\_NEXTBREAK.</span></span><br/>                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="d2b1e-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2b1e-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2b1e-137">Anfangsposition des NULL basierten Zeichens.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-137">Zero-based character starting position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2b1e-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2b1e-138">Return value</span></span>

<span data-ttu-id="d2b1e-139">Die Meldung gibt einen Wert zurück, der auf dem *wParam* -Parameter basiert.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-139">The message returns a value based on the *wParam* parameter.</span></span>



| <span data-ttu-id="d2b1e-140">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d2b1e-140">Return code</span></span>                                                                                    | <span data-ttu-id="d2b1e-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2b1e-141">Description</span></span>                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d2b1e-142"><dt>**wParam**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1e-142"><dt>**wParam**</dt></span></span> </dl>          | <span data-ttu-id="d2b1e-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2b1e-143">Return Value</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="d2b1e-144"><dt>**WB- \_ Klassifizierung**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1e-144"><dt>**WB\_CLASSIFY**</dt></span></span> </dl>    | <span data-ttu-id="d2b1e-145">Gibt die Zeichenklasse und die Wort Umbruch Flags des Zeichens an der angegebenen Position zurück.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-145">Returns the character class and word-break flags of the character at the specified position.</span></span><br/>                |
| <dl> <span data-ttu-id="d2b1e-146"><dt>**WB- \_ isdelimiter**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1e-146"><dt>**WB\_ISDELIMITER**</dt></span></span> </dl> | <span data-ttu-id="d2b1e-147">Gibt **true** zurück, wenn das Zeichen an der angegebenen Position ein Trennzeichen ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-147">Returns **TRUE** if the character at the specified position is a delimiter; otherwise it returns **FALSE**.</span></span><br/> |
| <dl> <span data-ttu-id="d2b1e-148"><dt>**Andere**</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1e-148"><dt>**Others**</dt></span></span> </dl>          | <span data-ttu-id="d2b1e-149">Gibt den Zeichen Index des Wort Bruchs zurück.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-149">Returns the character index of the word break.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="d2b1e-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2b1e-150">Remarks</span></span>

<span data-ttu-id="d2b1e-151">Wenn *wParam* den Wert "WB \_ left" und "WB \_ right" hat, sucht die Prozedur "Wort Umbruch" nach Wort Umbrüchen nur nach Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-151">If *wParam* is WB\_LEFT and WB\_RIGHT, the word-break procedure finds word breaks only after delimiters.</span></span> <span data-ttu-id="d2b1e-152">Dies entspricht der Funktionalität eines Bearbeitungs Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-152">This matches the functionality of an edit control.</span></span> <span data-ttu-id="d2b1e-153">Wenn *wParam* den Wert "WB" \_ , "muvewordleft" oder "WB" ist \_ , vergleicht die Prozedur "Wort Umbruch" auch Zeichenklassen und Wörter Trennungs Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="d2b1e-153">If *wParam* is WB\_MOVEWORDLEFT or WB\_MOVEWORDRIGHT, the word-break procedure also compares character classes and word-break flags.</span></span>

<span data-ttu-id="d2b1e-154">Weitere Informationen zu Zeichenklassen und Flags für das Wort Umbruch finden Sie unter [Wort-und Zeilenumbrüche](using-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="d2b1e-154">For information about character classes and word-break flags, see [Word and Line Breaks](using-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2b1e-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2b1e-155">Requirements</span></span>



| <span data-ttu-id="d2b1e-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2b1e-156">Requirement</span></span> | <span data-ttu-id="d2b1e-157">Wert</span><span class="sxs-lookup"><span data-stu-id="d2b1e-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b1e-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2b1e-158">Minimum supported client</span></span><br/> | <span data-ttu-id="d2b1e-159">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2b1e-159">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2b1e-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2b1e-160">Minimum supported server</span></span><br/> | <span data-ttu-id="d2b1e-161">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2b1e-161">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2b1e-162">Header</span><span class="sxs-lookup"><span data-stu-id="d2b1e-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2b1e-163"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2b1e-163"><dt>Richedit.h</dt></span></span> </dl> |



 

 





