---
title: EM_STREAMOUT Meldung (RichEdit. h)
description: Bewirkt, dass ein Rich Edit-Steuerelement seinen Inhalt an eine Application \ 8211; defined editstreamcallback-Rückruffunktion übergibt. Die Rückruffunktion kann dann den Datenstrom in eine Datei oder an einen beliebigen anderen Speicherort schreiben, den Sie auswählt.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- Windows-Steuerelemente für EM_STREAMOUT Meldung
topic_type:
- apiref
api_name:
- EM_STREAMOUT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbdef51348593f8dbcfdb1ef579aca7dba6f96e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956509"
---
# <a name="em_streamout-message"></a><span data-ttu-id="e2e3b-105">EM- \_ StreamOut-Meldung</span><span class="sxs-lookup"><span data-stu-id="e2e3b-105">EM\_STREAMOUT message</span></span>

<span data-ttu-id="e2e3b-106">Bewirkt, dass ein Rich Edit-Steuerelement seinen Inhalt an eine von der Anwendung definierte [*editstreamcallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) -Rückruffunktion übergibt.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-106">Causes a rich edit control to pass its contents to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) callback function.</span></span> <span data-ttu-id="e2e3b-107">Die Rückruffunktion kann dann den Datenstrom in eine Datei oder an einen beliebigen anderen Speicherort schreiben, den Sie auswählt.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-107">The callback function can then write the stream of data to a file or any other location that it chooses.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2e3b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2e3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2e3b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2e3b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2e3b-110">Gibt die Datenformat-und Ersetzungs Optionen an.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-110">Specifies the data format and replacement options.</span></span>

<span data-ttu-id="e2e3b-111">Dieser Wert muss einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-111">This value must be one of the following values.</span></span>



| <span data-ttu-id="e2e3b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="e2e3b-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="e2e3b-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e2e3b-113">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <span data-ttu-id="e2e3b-114"><dt>**SF \_ RTF**</dt></span><span class="sxs-lookup"><span data-stu-id="e2e3b-114"><dt>**SF\_RTF**</dt></span></span> </dl>                   | <span data-ttu-id="e2e3b-115">RTF.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-115">RTF.</span></span><br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <span data-ttu-id="e2e3b-116"><dt>**SF \_ RTF noobjs**</dt></span><span class="sxs-lookup"><span data-stu-id="e2e3b-116"><dt>**SF\_RTFNOOBJS**</dt></span></span> </dl> | <span data-ttu-id="e2e3b-117">RTF mit Leerzeichen anstelle von COM-Objekten.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-117">RTF with spaces in place of COM objects.</span></span><br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <span data-ttu-id="e2e3b-118"><dt>**SF- \_ Text**</dt></span><span class="sxs-lookup"><span data-stu-id="e2e3b-118"><dt>**SF\_TEXT**</dt></span></span> </dl>                | <span data-ttu-id="e2e3b-119">Text mit Leerzeichen anstelle von COM-Objekten.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-119">Text with spaces in place of COM objects.</span></span><br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <span data-ttu-id="e2e3b-120"><dt>**SF \_ textisiert**</dt></span><span class="sxs-lookup"><span data-stu-id="e2e3b-120"><dt>**SF\_TEXTIZED**</dt></span></span> </dl>    | <span data-ttu-id="e2e3b-121">Text mit einer Textdarstellung von COM-Objekten.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-121">Text with a text representation of COM objects.</span></span><br/> |



 

<span data-ttu-id="e2e3b-122">Die Option " **SF \_ RTF noobjs** " ist nützlich, wenn eine Anwendung com-Objekte selbst speichert, da die RTF-Darstellung von COM-Objekten nicht sehr kompakt ist.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-122">The **SF\_RTFNOOBJS** option is useful if an application stores COM objects itself, as RTF representation of COM objects is not very compact.</span></span> <span data-ttu-id="e2e3b-123">Das Steuerwort \\ objattph, gefolgt von einem Leerzeichen, deutet auf die Objektposition hin.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-123">The control word, \\objattph, followed by a space denotes the object position.</span></span>

<span data-ttu-id="e2e3b-124">Außerdem können Sie die folgenden Flags angeben.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-124">In addition, you can specify the following flags.</span></span>



| <span data-ttu-id="e2e3b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e2e3b-125">Value</span></span>                                                                                                                                                            | <span data-ttu-id="e2e3b-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e2e3b-126">Meaning</span></span>                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <span data-ttu-id="e2e3b-127"><dt>**SFF- \_ plainrtf**</dt></span><span class="sxs-lookup"><span data-stu-id="e2e3b-127"><dt>**SFF\_PLAINRTF**</dt></span></span> </dl>       | <span data-ttu-id="e2e3b-128">Wenn angegeben, werden durch das Rich Edit-Steuerelement nur die Schlüsselwörter gestreamt, die für alle Sprachen gelten, wobei sprachspezifische Schlüsselwörter ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-128">If specified, the rich edit control streams out only the keywords common to all languages, ignoring language-specific keywords.</span></span> <span data-ttu-id="e2e3b-129">Wenn nicht angegeben, werden durch das Rich Edit-Steuerelement alle Schlüsselwörter gestreamt.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-129">If not specified, the rich edit control streams out all keywords.</span></span> <span data-ttu-id="e2e3b-130">Sie können dieses Flag mit dem **SF \_ RTF** -oder **SF \_ RTF** -Flag kombinieren.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-130">You can combine this flag with the **SF\_RTF** or **SF\_RTFNOOBJS** flag.</span></span><br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <span data-ttu-id="e2e3b-131"><dt>**SFF- \_ Auswahl**</dt></span><span class="sxs-lookup"><span data-stu-id="e2e3b-131"><dt>**SFF\_SELECTION**</dt></span></span> </dl>    | <span data-ttu-id="e2e3b-132">Wenn diese Option angegeben ist, wird das Rich Edit-Steuerelement nur den Inhalt der aktuellen Auswahl auslagern.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-132">If specified, the rich edit control streams out only the contents of the current selection.</span></span> <span data-ttu-id="e2e3b-133">Wenn nichts angegeben ist, streamt das Steuerelement den gesamten Inhalt.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-133">If not specified, the control streams out the entire contents.</span></span> <span data-ttu-id="e2e3b-134">Sie können dieses Flag mit einem beliebigen Datenformat Wert kombinieren.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-134">You can combine this flag with any of data format values.</span></span><br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <span data-ttu-id="e2e3b-135"><dt>**SF ( \_ Unicode)**</dt></span><span class="sxs-lookup"><span data-stu-id="e2e3b-135"><dt>**SF\_UNICODE**</dt></span></span> </dl>             | <span data-ttu-id="e2e3b-136">**Microsoft Rich Edit 2,0 und höher:** Gibt Unicode-Text an.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-136">**Microsoft Rich Edit 2.0 and later:** Indicates Unicode text.</span></span> <span data-ttu-id="e2e3b-137">Sie können dieses Flag mit dem **SF- \_ textflag** kombinieren.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-137">You can combine this flag with the **SF\_TEXT** flag.</span></span><br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <span data-ttu-id="e2e3b-138"><dt>**SF \_ useCodepage**</dt></span><span class="sxs-lookup"><span data-stu-id="e2e3b-138"><dt>**SF\_USECODEPAGE**</dt></span></span> </dl> | <span data-ttu-id="e2e3b-139">**Rich Edit 3,0 und höher:** Generiert UTF-8 RTF sowie Text, der andere Codepages verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-139">**Rich Edit 3.0 and later:** Generates UTF-8 RTF as well as text using other code pages.</span></span> <span data-ttu-id="e2e3b-140">Die Codepage wird im großen Wort von *wParam* festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-140">The code page is set in the high word of *wParam*.</span></span> <span data-ttu-id="e2e3b-141">Legen Sie z. b. für UTF-8 RTF *wParam* auf (CP \_ UTF8 << 16) \| SF \_ useCodepage \| SF \_ RTF fest.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-141">For example, for UTF-8 RTF, set *wParam* to (CP\_UTF8 << 16) \| SF\_USECODEPAGE \| SF\_RTF.</span></span><br/>                               |



 

</dd> <dt>

<span data-ttu-id="e2e3b-142">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2e3b-142">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2e3b-143">Zeiger auf eine [**editstream**](/windows/desktop/api/Richedit/ns-richedit-editstream) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-143">Pointer to an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="e2e3b-144">Bei der Eingabe muss der **pfncallback** -Member dieser Struktur auf eine von der Anwendung definierte [*editstreamcallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) -Funktion verweisen.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-144">On input, the **pfnCallback** member of this structure must point to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function.</span></span> <span data-ttu-id="e2e3b-145">Bei der Ausgabe kann der **dwError** -Member einen Fehlercode ungleich 0 (null) enthalten, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-145">On output, the **dwError** member can contain a nonzero error code if an error occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2e3b-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2e3b-146">Return value</span></span>

<span data-ttu-id="e2e3b-147">Diese Meldung gibt die Anzahl der Zeichen zurück, die in den Datenstrom geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-147">This message returns the number of characters written to the data stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2e3b-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2e3b-148">Remarks</span></span>

<span data-ttu-id="e2e3b-149">Wenn Sie eine **EM- \_ StreamOut** -Nachricht senden, führt das Rich Edit-Steuerelement wiederholte Aufrufe an die [*editstreamcallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) -Funktion aus, die vom **pfncallback** -Member der [**editstream**](/windows/desktop/api/Richedit/ns-richedit-editstream) -Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-149">When you send an **EM\_STREAMOUT** message, the rich edit control makes repeated calls to the [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function specified by the **pfnCallback** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="e2e3b-150">Jedes Mal, wenn die Rückruffunktion aufgerufen wird, übergibt das Steuerelement einen Puffer, der einen Teil des Inhalts des Steuer Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-150">Each time it calls the callback function, the control passes a buffer containing a portion of the contents of the control.</span></span> <span data-ttu-id="e2e3b-151">Dieser Prozess wird fortgesetzt, bis das Steuerelement seinen gesamten Inhalt an die Rückruffunktion weitergegeben hat oder bis ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="e2e3b-151">This process continues until the control has passed all its contents to the callback function, or until an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e3b-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2e3b-152">Requirements</span></span>



| <span data-ttu-id="e2e3b-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2e3b-153">Requirement</span></span> | <span data-ttu-id="e2e3b-154">Wert</span><span class="sxs-lookup"><span data-stu-id="e2e3b-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e3b-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e2e3b-155">Minimum supported client</span></span><br/> | <span data-ttu-id="e2e3b-156">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2e3b-156">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2e3b-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e2e3b-157">Minimum supported server</span></span><br/> | <span data-ttu-id="e2e3b-158">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e2e3b-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e2e3b-159">Header</span><span class="sxs-lookup"><span data-stu-id="e2e3b-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2e3b-160"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2e3b-160"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2e3b-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2e3b-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="e2e3b-162">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e2e3b-162">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e2e3b-163">**Editstream**</span><span class="sxs-lookup"><span data-stu-id="e2e3b-163">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[<span data-ttu-id="e2e3b-164">*Editstreamcallback*</span><span class="sxs-lookup"><span data-stu-id="e2e3b-164">*EditStreamCallback*</span></span>](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[<span data-ttu-id="e2e3b-165">**EM- \_ StreamIn**</span><span class="sxs-lookup"><span data-stu-id="e2e3b-165">**EM\_STREAMIN**</span></span>](em-streamin.md)
</dt> </dl>

 

 





