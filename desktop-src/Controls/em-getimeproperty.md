---
title: EM_GETIMEPROPERTY Meldung (RichEdit. h)
description: Ruft die Eigenschaft und die Funktionen des Eingabemethoden-Editors (IME) ab, die dem aktuellen Eingabe Gebiets Schema zugeordnet sind.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- Windows-Steuerelemente für EM_GETIMEPROPERTY Meldung
topic_type:
- apiref
api_name:
- EM_GETIMEPROPERTY
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c081aa99c99f4cd0995c0f9d2f5256e2958dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105123"
---
# <a name="em_getimeproperty-message"></a><span data-ttu-id="495fd-104">EM \_ getimeproperty-Nachricht</span><span class="sxs-lookup"><span data-stu-id="495fd-104">EM\_GETIMEPROPERTY message</span></span>

<span data-ttu-id="495fd-105">Ruft die Eigenschaft und die Funktionen des Eingabemethoden-Editors (IME) ab, die dem aktuellen Eingabe Gebiets Schema zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="495fd-105">Retrieves the property and capabilities of the Input Method Editor (IME) associated with the current input locale.</span></span>

## <a name="parameters"></a><span data-ttu-id="495fd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="495fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="495fd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="495fd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="495fd-108">Gibt den Typ der abzurufenden Eigenschafts Informationen an.</span><span class="sxs-lookup"><span data-stu-id="495fd-108">Specifies the type of property information to retrieve.</span></span> <span data-ttu-id="495fd-109">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="495fd-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="495fd-110">Wert</span><span class="sxs-lookup"><span data-stu-id="495fd-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="495fd-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="495fd-111">Meaning</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <span data-ttu-id="495fd-112"><dt>**IGP- \_ Eigenschaft**</dt></span><span class="sxs-lookup"><span data-stu-id="495fd-112"><dt>**IGP\_PROPERTY**</dt></span></span> </dl>                | <span data-ttu-id="495fd-113">Eigenschafts Informationen.</span><span class="sxs-lookup"><span data-stu-id="495fd-113">Property information.</span></span><br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <span data-ttu-id="495fd-114"><dt>**IGP- \_ Konvertierung**</dt></span><span class="sxs-lookup"><span data-stu-id="495fd-114"><dt>**IGP\_CONVERSION**</dt></span></span> </dl>          | <span data-ttu-id="495fd-115">Konvertierungs Funktionen.</span><span class="sxs-lookup"><span data-stu-id="495fd-115">Conversion capabilities.</span></span> <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <span data-ttu-id="495fd-116"><dt>**IGP- \_ Satz**</dt></span><span class="sxs-lookup"><span data-stu-id="495fd-116"><dt>**IGP\_SENTENCE**</dt></span></span> </dl>                | <span data-ttu-id="495fd-117">Satzmodusfunktionen.</span><span class="sxs-lookup"><span data-stu-id="495fd-117">Sentence mode capabilities.</span></span> <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <span data-ttu-id="495fd-118"><dt>**IGP- \_ Benutzeroberfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="495fd-118"><dt>**IGP\_UI**</dt></span></span> </dl>                                  | <span data-ttu-id="495fd-119">Benutzeroberflächen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="495fd-119">User interface capabilities.</span></span> <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <span data-ttu-id="495fd-120"><dt>**IGP \_ setcompstr**</dt></span><span class="sxs-lookup"><span data-stu-id="495fd-120"><dt>**IGP\_SETCOMPSTR**</dt></span></span> </dl>          | <span data-ttu-id="495fd-121">Kompositions Zeichen folgen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="495fd-121">Composition string capabilities.</span></span> <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <span data-ttu-id="495fd-122"><dt>**IGP- \_ Auswahl**</dt></span><span class="sxs-lookup"><span data-stu-id="495fd-122"><dt>**IGP\_SELECT**</dt></span></span> </dl>                      | <span data-ttu-id="495fd-123">Auswahl Vererbungs Funktionen.</span><span class="sxs-lookup"><span data-stu-id="495fd-123">Selection inheritance capabilities.</span></span> <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <span data-ttu-id="495fd-124"><dt>**IGP- \_ getimeversion**</dt></span><span class="sxs-lookup"><span data-stu-id="495fd-124"><dt>**IGP\_GETIMEVERSION**</dt></span></span> </dl> | <span data-ttu-id="495fd-125">Ruft die System Versionsnummer ab, für die der angegebene IME erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="495fd-125">Retrieves the system version number for which the specified IME was created.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="495fd-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="495fd-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="495fd-127">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="495fd-127">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="495fd-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="495fd-128">Return value</span></span>

<span data-ttu-id="495fd-129">Gibt den Eigenschafts-oder Funktionswert zurück, abhängig vom Wert des *LPARAM* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="495fd-129">Returns the property or capability value, depending on the value of the *lParam* parameter.</span></span> <span data-ttu-id="495fd-130">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="495fd-130">For more information, see the Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="495fd-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="495fd-131">Remarks</span></span>

<span data-ttu-id="495fd-132">Wenn *wParam* eine IGP- \_ Eigenschaft ist, gibt Sie einen oder mehrere der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="495fd-132">If *wParam* is IGP\_PROPERTY, it returns one or more of the following values.</span></span>



| <span data-ttu-id="495fd-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="495fd-133">Requirement</span></span> | <span data-ttu-id="495fd-134">Wert</span><span class="sxs-lookup"><span data-stu-id="495fd-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="495fd-135">IME- \_ Prop \_ bei \_ Caretzeichen</span><span class="sxs-lookup"><span data-stu-id="495fd-135">IME\_PROP\_AT\_CARET</span></span>                | <span data-ttu-id="495fd-136">Wenn festgelegt, befindet sich das Konvertierungs Fenster an der Einfügemarke.</span><span class="sxs-lookup"><span data-stu-id="495fd-136">If set, conversion window is at the caret position.</span></span> <span data-ttu-id="495fd-137">Wenn diese Option deaktiviert ist, befindet sich das Fenster in der Nähe der Position der</span><span class="sxs-lookup"><span data-stu-id="495fd-137">If clear, the window is near caret position.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="495fd-138">spezielle IME- \_ Prop- \_ \_ Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="495fd-138">IME\_PROP\_SPECIAL\_UI</span></span>              | <span data-ttu-id="495fd-139">Wenn festgelegt, verfügt IME über eine nicht standardmäßige Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="495fd-139">If set, IME has a nonstandard user interface.</span></span> <span data-ttu-id="495fd-140">Die Anwendung sollte nicht im IME-Fenster gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="495fd-140">The application should not draw in the IME window.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="495fd-141">Start Seite der IME- \_ Prop-Kerze mit \_ \_ \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="495fd-141">IME\_PROP\_CANDLIST\_START\_FROM\_1</span></span> | <span data-ttu-id="495fd-142">Wenn festgelegt, werden Zeichen folgen in der Kandidatenliste beginnend mit 1 nummeriert.</span><span class="sxs-lookup"><span data-stu-id="495fd-142">If set, strings in the candidate list are numbered starting at 1.</span></span> <span data-ttu-id="495fd-143">Wenn Clear, beginnen Zeichen folgen bei Null.</span><span class="sxs-lookup"><span data-stu-id="495fd-143">If clear, strings start at zero.</span></span>                                                                                                                                                                |
| <span data-ttu-id="495fd-144">IME- \_ Prop- \_ Unicode</span><span class="sxs-lookup"><span data-stu-id="495fd-144">IME\_PROP\_UNICODE</span></span>                  | <span data-ttu-id="495fd-145">Wenn festgelegt, wird der IME als unicodeime angezeigt.</span><span class="sxs-lookup"><span data-stu-id="495fd-145">If set, the IME is viewed as a UnicodeIME.</span></span> <span data-ttu-id="495fd-146">Das System und der IME kommunizieren über die unicodeime-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="495fd-146">The system and the IME will communicate through the UnicodeIME interface.</span></span> <span data-ttu-id="495fd-147">Wenn Clear, verwendet IME die ANSI-Schnittstelle für die Kommunikation mit dem System.</span><span class="sxs-lookup"><span data-stu-id="495fd-147">If clear, IME will use the ANSI interface to communicate with the system.</span></span>                                                                    |
| <span data-ttu-id="495fd-148">IME \_ - \_ Prop \_ bei \_ Auswahl beenden</span><span class="sxs-lookup"><span data-stu-id="495fd-148">IME\_PROP\_COMPLETE\_ON\_UNSELECT</span></span>   | <span data-ttu-id="495fd-149">Wenn festgelegt, befindet sich das Konvertierungs Fenster an der Einfügemarke.</span><span class="sxs-lookup"><span data-stu-id="495fd-149">If set, conversion window is at the caret position.</span></span> <span data-ttu-id="495fd-150">Wenn diese Option deaktiviert ist, befindet sich das Fenster in der Nähe der Position der</span><span class="sxs-lookup"><span data-stu-id="495fd-150">If clear, the window is near caret position.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="495fd-151">IME-unter \_ Stützung für \_ \_ Wide \_ VKey</span><span class="sxs-lookup"><span data-stu-id="495fd-151">IME\_PROP\_ACCEPT\_WIDE\_VKEY</span></span>       | <span data-ttu-id="495fd-152">Wenn festgelegt, verarbeitet der IME den eingefügten Unicode, der aus der [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) -Funktion stammt, mithilfe des VK- \_ Pakets.</span><span class="sxs-lookup"><span data-stu-id="495fd-152">If set, the IME processes the injected Unicode that came from the [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) function by using VK\_PACKET.</span></span> <span data-ttu-id="495fd-153">Wenn Clear, verarbeitet der IME möglicherweise nicht den eingefügten Unicode-Code, und der eingefügte Unicode kann direkt an die Anwendung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="495fd-153">If clear, the IME might not process the injected Unicode, and the injected Unicode might be sent to the application directly.</span></span> |



 

<span data-ttu-id="495fd-154">Wenn *wParam* die IGP- \_ Benutzeroberfläche ist, gibt Sie einen oder mehrere der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="495fd-154">If *wParam* is IGP\_UI, it returns one or more of the following values.</span></span>



| <span data-ttu-id="495fd-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="495fd-155">Requirement</span></span> | <span data-ttu-id="495fd-156">Wert</span><span class="sxs-lookup"><span data-stu-id="495fd-156">Value</span></span> |
|-----------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="495fd-157">\_Oberfläche \_ 2700</span><span class="sxs-lookup"><span data-stu-id="495fd-157">UI\_CAP\_2700</span></span>   | <span data-ttu-id="495fd-158">Unterstützt Text escapeswerte von 0 oder 2700.</span><span class="sxs-lookup"><span data-stu-id="495fd-158">Supports text escapement values of 0 or 2700.</span></span> <span data-ttu-id="495fd-159">Weitere Informationen finden Sie unter **LF escapements**.</span><span class="sxs-lookup"><span data-stu-id="495fd-159">For more information, see **lfEscapement**.</span></span>             |
| <span data-ttu-id="495fd-160">UI- \_ Obergrenze \_ ROT90</span><span class="sxs-lookup"><span data-stu-id="495fd-160">UI\_CAP\_ROT90</span></span>  | <span data-ttu-id="495fd-161">Unterstützt Text escapeswerte von 0, 900, 1800 oder 2700.</span><span class="sxs-lookup"><span data-stu-id="495fd-161">Supports text escapement values of 0, 900, 1800, or 2700.</span></span> <span data-ttu-id="495fd-162">Weitere Informationen finden Sie unter **LF escapements**.</span><span class="sxs-lookup"><span data-stu-id="495fd-162">For more information, see **lfEscapement**.</span></span> |
| <span data-ttu-id="495fd-163">Oberfläche für die Benutzeroberflächen Abdeckung \_ \_</span><span class="sxs-lookup"><span data-stu-id="495fd-163">UI\_CAP\_ROTANY</span></span> | <span data-ttu-id="495fd-164">Unterstützt jeden Text escapeswert.</span><span class="sxs-lookup"><span data-stu-id="495fd-164">Supports any text escapement value.</span></span> <span data-ttu-id="495fd-165">Weitere Informationen finden Sie unter **LF escapements**.</span><span class="sxs-lookup"><span data-stu-id="495fd-165">For more information, see **lfEscapement**.</span></span>                       |



 

<span data-ttu-id="495fd-166">Wenn *wParam* \_ den Wert IGP setcompstr hat, gibt er einen oder mehrere der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="495fd-166">If *wParam* is IGP\_SETCOMPSTR, it returns one or more of the following values.</span></span>



| <span data-ttu-id="495fd-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="495fd-167">Requirement</span></span> | <span data-ttu-id="495fd-168">Wert</span><span class="sxs-lookup"><span data-stu-id="495fd-168">Value</span></span> |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="495fd-169">SCS- \_ Cap- \_ compstr</span><span class="sxs-lookup"><span data-stu-id="495fd-169">SCS\_CAP\_COMPSTR</span></span>            | <span data-ttu-id="495fd-170">Kann die Kompositions Zeichenfolge durch Aufrufen der [**immsetcompositionstring**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) -Funktion mit dem SCS \_ setstr-Wert erstellen.</span><span class="sxs-lookup"><span data-stu-id="495fd-170">Can create the composition string by calling the [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) function with the SCS\_SETSTR value.</span></span>                                                      |
| <span data-ttu-id="495fd-171">SCS- \_ Cap- \_ makeread</span><span class="sxs-lookup"><span data-stu-id="495fd-171">SCS\_CAP\_MAKEREAD</span></span>           | <span data-ttu-id="495fd-172">Kann die Lese Zeichenfolge aus der entsprechenden Kompositions Zeichenfolge erstellen, wenn die [**immsetcompositionstring**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) -Funktion mit SCS \_ setstr und ohne Festlegen von *lpread* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="495fd-172">Can create the reading string from corresponding composition string when using the [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) function with SCS\_SETSTR and without setting *lpRead*.</span></span> |
| <span data-ttu-id="495fd-173">SCS- \_ Cap-abdeckungszeichenfolge \_</span><span class="sxs-lookup"><span data-stu-id="495fd-173">SCS\_CAP\_SETRECONVERTSTRING</span></span> | <span data-ttu-id="495fd-174">Dieser IME kann eine erneute Konvertierung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="495fd-174">This IME can support reconversion.</span></span> <span data-ttu-id="495fd-175">Verwenden Sie [**immsetcompositionstring**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) , um die erneute Konvertierung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="495fd-175">Use [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) to do the reconversion.</span></span>                                                                             |



 

<span data-ttu-id="495fd-176">Wenn für *wParam* die Option IGP ausgewählt ist, wird mindestens \_ einer der folgenden Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="495fd-176">If *wParam* is IGP\_SELECT, it returns one or more of the following values.</span></span>



| <span data-ttu-id="495fd-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="495fd-177">Requirement</span></span> | <span data-ttu-id="495fd-178">Wert</span><span class="sxs-lookup"><span data-stu-id="495fd-178">Value</span></span> |
|-----------------------|------------------------------------------------------|
| <span data-ttu-id="495fd-179">Wählen Sie Cap-Verbindungs Modus aus. \_ \_</span><span class="sxs-lookup"><span data-stu-id="495fd-179">SELECT\_CAP\_CONVMODE</span></span> | <span data-ttu-id="495fd-180">Erbt den Konvertierungsmodus, wenn ein neuer IME ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="495fd-180">Inherits conversion mode when a new IME is selected.</span></span> |
| <span data-ttu-id="495fd-181">\_Cap- \_ Satz auswählen</span><span class="sxs-lookup"><span data-stu-id="495fd-181">SELECT\_CAP\_SENTENCE</span></span> | <span data-ttu-id="495fd-182">Erbt den Satz Modus, wenn ein neuer IME ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="495fd-182">Inherits sentence mode when a new IME is selected.</span></span>   |



 

<span data-ttu-id="495fd-183">Wenn *wParam* eine IGP- \_ getimeversion ist, gibt Sie einen oder mehrere der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="495fd-183">If *wParam* is IGP\_GETIMEVERSION, it returns one or more of the following values.</span></span>



| <span data-ttu-id="495fd-184">Anforderung</span><span class="sxs-lookup"><span data-stu-id="495fd-184">Requirement</span></span> | <span data-ttu-id="495fd-185">Wert</span><span class="sxs-lookup"><span data-stu-id="495fd-185">Value</span></span> |
|--------------|---------------------------------------------|
| <span data-ttu-id="495fd-186">Imever \_ 0310</span><span class="sxs-lookup"><span data-stu-id="495fd-186">IMEVER\_0310</span></span> | <span data-ttu-id="495fd-187">Der IME wurde für Windows 3,1 erstellt.</span><span class="sxs-lookup"><span data-stu-id="495fd-187">The IME was created for Windows 3.1.</span></span>        |
| <span data-ttu-id="495fd-188">Imever \_ 0400</span><span class="sxs-lookup"><span data-stu-id="495fd-188">IMEVER\_0400</span></span> | <span data-ttu-id="495fd-189">Der IME wurde für Windows 95 oder höher erstellt.</span><span class="sxs-lookup"><span data-stu-id="495fd-189">The IME was created for Windows 95 or later</span></span> |



 

<span data-ttu-id="495fd-190">Diese Meldung ähnelt " [**immgetproperty**](/windows/desktop/api/imm/nf-imm-immgetproperty)", mit dem Unterschied, dass Sie das aktuelle Eingabe Gebiets Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="495fd-190">This message is similar to [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty), except that it uses the current input locale.</span></span> <span data-ttu-id="495fd-191">Die Anwendung sollte [**EM- \_ isime**](em-isime.md) aufrufen, bevor diese Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="495fd-191">The application should call [**EM\_ISIME**](em-isime.md) before calling this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="495fd-192">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="495fd-192">Requirements</span></span>



| <span data-ttu-id="495fd-193">Anforderung</span><span class="sxs-lookup"><span data-stu-id="495fd-193">Requirement</span></span> | <span data-ttu-id="495fd-194">Wert</span><span class="sxs-lookup"><span data-stu-id="495fd-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="495fd-195">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="495fd-195">Minimum supported client</span></span><br/> | <span data-ttu-id="495fd-196">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="495fd-196">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="495fd-197">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="495fd-197">Minimum supported server</span></span><br/> | <span data-ttu-id="495fd-198">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="495fd-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="495fd-199">Header</span><span class="sxs-lookup"><span data-stu-id="495fd-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="495fd-200"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="495fd-200"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="495fd-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="495fd-201">See also</span></span>

<dl> <dt>

<span data-ttu-id="495fd-202">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="495fd-202">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="495fd-203">**EM- \_ isime**</span><span class="sxs-lookup"><span data-stu-id="495fd-203">**EM\_ISIME**</span></span>](em-isime.md)
</dt> <dt>

<span data-ttu-id="495fd-204">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="495fd-204">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="495fd-205">**Immgetproperty**</span><span class="sxs-lookup"><span data-stu-id="495fd-205">**ImmGetProperty**</span></span>](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

