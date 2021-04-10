---
title: EM_SETTEXTMODE Meldung (RichEdit. h)
description: Legt den Textmodus oder die rückgängig-Ebene eines Rich-Edit-Steuer Elements fest. Die Meldung schlägt fehl, wenn das Steuerelement Text enthält.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- Windows-Steuerelemente für EM_SETTEXTMODE Meldung
topic_type:
- apiref
api_name:
- EM_SETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74ec5378213bdd32721ff95ae3f4505437973256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956635"
---
# <a name="em_settextmode-message"></a><span data-ttu-id="9eae2-105">EM \_ settextmode-Meldung</span><span class="sxs-lookup"><span data-stu-id="9eae2-105">EM\_SETTEXTMODE message</span></span>

<span data-ttu-id="9eae2-106">Legt den Textmodus oder die rückgängig-Ebene eines Rich-Edit-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="9eae2-106">Sets the text mode or undo level of a rich edit control.</span></span> <span data-ttu-id="9eae2-107">Die Meldung schlägt fehl, wenn das Steuerelement Text enthält.</span><span class="sxs-lookup"><span data-stu-id="9eae2-107">The message fails if the control contains any text.</span></span>

## <a name="parameters"></a><span data-ttu-id="9eae2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9eae2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eae2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9eae2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9eae2-110">Mindestens ein Wert aus dem [**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="9eae2-110">One or more values from the [**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode) enumeration type.</span></span> <span data-ttu-id="9eae2-111">Die Werte geben die neuen Einstellungen für die Parameter für den Textmodus und den rückgängiggrad des Steuer Elements an.</span><span class="sxs-lookup"><span data-stu-id="9eae2-111">The values specify the new settings for the control's text mode and undo level parameters.</span></span>

<span data-ttu-id="9eae2-112">Geben Sie einen der folgenden Werte an, um den textmodusparameter festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9eae2-112">Specify one of the following values to set the text mode parameter.</span></span> <span data-ttu-id="9eae2-113">Wenn Sie keinen textmoduswert angeben, bleibt der Textmodus bei der aktuellen Einstellung erhalten.</span><span class="sxs-lookup"><span data-stu-id="9eae2-113">If you do not specify a text mode value, the text mode remains at its current setting.</span></span> 

| <span data-ttu-id="9eae2-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9eae2-114">Value</span></span>                                          | <span data-ttu-id="9eae2-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9eae2-115">Meaning</span></span>                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9eae2-116">**TM \_ -Klartext**</span><span class="sxs-lookup"><span data-stu-id="9eae2-116">**TM\_PLAINTEXT**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="9eae2-117">Gibt den nur-Text-Modus an, in dem das Steuerelement einem Standard Bearbeitungs Steuerelement ähnelt.</span><span class="sxs-lookup"><span data-stu-id="9eae2-117">Indicates plain text mode, in which the control is similar to a standard edit control.</span></span> <span data-ttu-id="9eae2-118">Weitere Informationen zum nur-Text-Modus finden Sie im folgenden Abschnitt mit hinweisen.</span><span class="sxs-lookup"><span data-stu-id="9eae2-118">For more information about plain text mode, see the following Remarks section.</span></span> |
| [<span data-ttu-id="9eae2-119">**TM \_ RichText**</span><span class="sxs-lookup"><span data-stu-id="9eae2-119">**TM\_RICHTEXT**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="9eae2-120">Gibt den Rich-Text-Modus an, in dem das Steuerelement über eine standardmäßige Funktionalität zur Bearbeitung verfügt</span><span class="sxs-lookup"><span data-stu-id="9eae2-120">Indicates rich text mode, in which the control has standard rich edit functionality.</span></span> <span data-ttu-id="9eae2-121">Der Rich-Text-Modus ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="9eae2-121">Rich text mode is the default setting.</span></span>                                           |



 

<span data-ttu-id="9eae2-122">Geben Sie einen der folgenden Werte zum Festlegen des Parameters für die rückgängig-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="9eae2-122">Specify one of the following values to set the undo level parameter.</span></span> <span data-ttu-id="9eae2-123">Wenn Sie keinen Wert für die rückgängig-Stufe angeben, bleibt die rückgängig-Ebene bei der aktuellen Einstellung erhalten.</span><span class="sxs-lookup"><span data-stu-id="9eae2-123">If you do not specify an undo level value, the undo level remains at its current setting.</span></span> 

| <span data-ttu-id="9eae2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9eae2-124">Value</span></span>                                                      | <span data-ttu-id="9eae2-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9eae2-125">Meaning</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9eae2-126">**TM \_ singlelevelundo**</span><span class="sxs-lookup"><span data-stu-id="9eae2-126">**TM\_SINGLELEVELUNDO**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="9eae2-127">Das-Steuerelement ermöglicht dem Benutzer, nur die letzte Aktion rückgängig zu machen, die rückgängig gemacht werden kann.</span><span class="sxs-lookup"><span data-stu-id="9eae2-127">The control allows the user to undo only the last action that can be undone.</span></span>                                                                                                       |
| [<span data-ttu-id="9eae2-128">**TM \_ MultiLevelUndo**</span><span class="sxs-lookup"><span data-stu-id="9eae2-128">**TM\_MULTILEVELUNDO**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="9eae2-129">Das-Steuerelement unterstützt mehrere rückgängig-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="9eae2-129">The control supports multiple undo operations.</span></span> <span data-ttu-id="9eae2-130">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="9eae2-130">This is the default setting.</span></span> <span data-ttu-id="9eae2-131">Verwenden Sie die Nachricht [**EM \_ setundolimit**](em-setundolimit.md) , um die maximale Anzahl von Rückgängig-Aktionen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9eae2-131">Use the [**EM\_SETUNDOLIMIT**](em-setundolimit.md) message to set the maximum number of undo actions.</span></span> |



 

<span data-ttu-id="9eae2-132">Geben Sie einen der folgenden Werte an, um den Code Page Parameter festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9eae2-132">Specify one of the following values to set the code page parameter.</span></span> <span data-ttu-id="9eae2-133">Wenn Sie keinen Code Page Wert angeben, bleibt die Codepage bei der aktuellen Einstellung erhalten.</span><span class="sxs-lookup"><span data-stu-id="9eae2-133">If you do not specify an code page value, the code page remains at its current setting.</span></span> 

| <span data-ttu-id="9eae2-134">Wert</span><span class="sxs-lookup"><span data-stu-id="9eae2-134">Value</span></span>                                                    | <span data-ttu-id="9eae2-135">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9eae2-135">Meaning</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9eae2-136">**TM- \_ singlecodepage**</span><span class="sxs-lookup"><span data-stu-id="9eae2-136">**TM\_SINGLECODEPAGE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode) | <span data-ttu-id="9eae2-137">Das-Steuerelement lässt nur die englische Tastatur und eine Tastatur zu, die dem Standardzeichensatz entspricht.</span><span class="sxs-lookup"><span data-stu-id="9eae2-137">The control only allows the English keyboard and a keyboard corresponding to the default character set.</span></span> <span data-ttu-id="9eae2-138">Beispielsweise können Sie Griechisch und Englisch haben.</span><span class="sxs-lookup"><span data-stu-id="9eae2-138">For example, you could have Greek and English.</span></span> <span data-ttu-id="9eae2-139">Beachten Sie, dass dadurch der Unicode-Text nicht in das Steuerelement eingegeben werden</span><span class="sxs-lookup"><span data-stu-id="9eae2-139">Note that this prevents Unicode text from entering the control.</span></span> <span data-ttu-id="9eae2-140">Verwenden Sie diesen Wert z. b., wenn ein Rich-Edit-Steuerelement auf ANSI-Text beschränkt werden muss.</span><span class="sxs-lookup"><span data-stu-id="9eae2-140">For example, use this value if a Rich Edit control must be restricted to ANSI text.</span></span> |
| [<span data-ttu-id="9eae2-141">**TM \_ multicodepage**</span><span class="sxs-lookup"><span data-stu-id="9eae2-141">**TM\_MULTICODEPAGE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)   | <span data-ttu-id="9eae2-142">Das-Steuerelement lässt mehrere Codepages und Unicode-Text im-Steuerelement zu.</span><span class="sxs-lookup"><span data-stu-id="9eae2-142">The control allows multiple code pages and Unicode text into the control.</span></span> <span data-ttu-id="9eae2-143">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="9eae2-143">This is the default setting.</span></span>                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="9eae2-144">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9eae2-144">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9eae2-145">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="9eae2-145">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eae2-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9eae2-146">Return value</span></span>

<span data-ttu-id="9eae2-147">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9eae2-147">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="9eae2-148">Wenn die Meldung fehlschlägt, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9eae2-148">If the message fails, the return value is a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eae2-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9eae2-149">Remarks</span></span>

<span data-ttu-id="9eae2-150">Im Rich-Text-Modus verfügt ein Rich-Edit-Steuerelement über eine standardmäßige Funktionalität zur Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="9eae2-150">In rich text mode, a rich edit control has standard rich edit functionality.</span></span> <span data-ttu-id="9eae2-151">Im nur-Text-Modus ist das Steuerelement jedoch mit einem Standard Bearbeitungs Steuerelement vergleichbar:</span><span class="sxs-lookup"><span data-stu-id="9eae2-151">However, in plain text mode, the control is similar to a standard edit control:</span></span>

-   <span data-ttu-id="9eae2-152">Der Text in einem nur-Text-Steuerelement kann nur ein Format aufweisen (z. b. Fett, 10 pt Arial).</span><span class="sxs-lookup"><span data-stu-id="9eae2-152">The text in a plain text control can have only one format (such as Bold, 10pt Arial).</span></span>
-   <span data-ttu-id="9eae2-153">Der Benutzer kann keine Rich-Text-Formate wie das Rich-Text-Format (RTF) oder eingebettete Objekte in ein nur-Text-Steuerelement einfügen.</span><span class="sxs-lookup"><span data-stu-id="9eae2-153">The user cannot paste rich text formats, such as Rich Text Format (RTF) or embedded objects into a plain text control.</span></span>
-   <span data-ttu-id="9eae2-154">Rich-Text-Modus-Steuerelemente verfügen immer über einen standardendeendemarker oder Wagen Rücklauf, um Absätze zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="9eae2-154">Rich text mode controls always have a default end-of-document marker or carriage return, to format paragraphs.</span></span> <span data-ttu-id="9eae2-155">Nur-Text-Steuerelemente benötigen nicht den Standard Marker für das Ende des Dokuments, sodass Sie ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="9eae2-155">Plain text controls, on the other hand, do not need the default, end-of-document marker, so it is omitted.</span></span>

<span data-ttu-id="9eae2-156">Das Steuerelement muss beim Empfang der **EM \_ settextmode** -Meldung keinen Text enthalten.</span><span class="sxs-lookup"><span data-stu-id="9eae2-156">The control must contain no text when it receives the **EM\_SETTEXTMODE** message.</span></span> <span data-ttu-id="9eae2-157">Um sicherzustellen, dass kein Text vorhanden ist, senden Sie eine [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext) -Nachricht mit einer leeren Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="9eae2-157">To ensure there is no text, send a [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message with an empty string ("").</span></span>

## <a name="requirements"></a><span data-ttu-id="9eae2-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9eae2-158">Requirements</span></span>



| <span data-ttu-id="9eae2-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9eae2-159">Requirement</span></span> | <span data-ttu-id="9eae2-160">Wert</span><span class="sxs-lookup"><span data-stu-id="9eae2-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9eae2-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9eae2-161">Minimum supported client</span></span><br/> | <span data-ttu-id="9eae2-162">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9eae2-162">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9eae2-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9eae2-163">Minimum supported server</span></span><br/> | <span data-ttu-id="9eae2-164">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9eae2-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9eae2-165">Header</span><span class="sxs-lookup"><span data-stu-id="9eae2-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eae2-166"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eae2-166"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eae2-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9eae2-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eae2-168">**EM \_ gettextmode**</span><span class="sxs-lookup"><span data-stu-id="9eae2-168">**EM\_GETTEXTMODE**</span></span>](em-gettextmode.md)
</dt> <dt>

[<span data-ttu-id="9eae2-169">**EM- \_ tundolimit**</span><span class="sxs-lookup"><span data-stu-id="9eae2-169">**EM\_SETUNDOLIMIT**</span></span>](em-setundolimit.md)
</dt> <dt>

[<span data-ttu-id="9eae2-170">**TextMode**</span><span class="sxs-lookup"><span data-stu-id="9eae2-170">**TEXTMODE**</span></span>](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[<span data-ttu-id="9eae2-171">**WM- \_ SetText**</span><span class="sxs-lookup"><span data-stu-id="9eae2-171">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

