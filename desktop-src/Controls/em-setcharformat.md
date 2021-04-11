---
title: EM_SETCHARFORMAT Meldung (RichEdit. h)
description: Legt die Zeichen Formatierung in einem Rich-Edit-Steuerelement fest.
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- Windows-Steuerelemente für EM_SETCHARFORMAT Meldung
topic_type:
- apiref
api_name:
- EM_SETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba8f37960659f29dd33d5b8f27f0b5a2e3d35eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105585"
---
# <a name="em_setcharformat-message"></a><span data-ttu-id="e6983-104">EM \_ setcharformat-Meldung</span><span class="sxs-lookup"><span data-stu-id="e6983-104">EM\_SETCHARFORMAT message</span></span>

<span data-ttu-id="e6983-105">Legt die Zeichen Formatierung in einem Rich-Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="e6983-105">Sets character formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6983-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6983-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6983-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6983-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6983-108">Zeichen Formatierung, die auf das-Steuerelement angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6983-108">Character formatting that applies to the control.</span></span> <span data-ttu-id="e6983-109">Wenn dieser Parameter 0 (null) ist, wird das Standard Zeichenformat festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e6983-109">If this parameter is zero, the default character format is set.</span></span> <span data-ttu-id="e6983-110">Andernfalls kann es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="e6983-110">Otherwise, it can be one of the following values.</span></span>



| <span data-ttu-id="e6983-111">Wert</span><span class="sxs-lookup"><span data-stu-id="e6983-111">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="e6983-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e6983-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <span data-ttu-id="e6983-113"><dt>**SCF \_ alle**</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-113"><dt>**SCF\_ALL**</dt></span></span> </dl>                                     | <span data-ttu-id="e6983-114">Wendet die Formatierung auf den gesamten Text im-Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="e6983-114">Applies the formatting to all text in the control.</span></span> <span data-ttu-id="e6983-115">Ungültig bei der **SCF- \_ Auswahl** oder dem **SCF- \_ Wort**.</span><span class="sxs-lookup"><span data-stu-id="e6983-115">Not valid with **SCF\_SELECTION** or **SCF\_WORD**.</span></span><br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <span data-ttu-id="e6983-116"><dt>**SCF- \_ associatefont**</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-116"><dt>**SCF\_ASSOCIATEFONT**</dt></span></span> </dl>       | <span data-ttu-id="e6983-117">**RichEdit 4,1:** Ordnet einem angegebenen Skript eine Schriftart zu und ändert somit die Standard Schriftart für dieses Skript.</span><span class="sxs-lookup"><span data-stu-id="e6983-117">**RichEdit 4.1:** Associates a font to a given script, thus changing the default font for that script.</span></span> <span data-ttu-id="e6983-118">Um die Schriftart anzugeben, verwenden Sie die folgenden Member von [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bcharset**, **bpitchandfamily**, **szfakename** und **LCID**.</span><span class="sxs-lookup"><span data-stu-id="e6983-118">To specify the font, use the following members of [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid**.</span></span><br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <span data-ttu-id="e6983-119"><dt>**SCF \_ ASSOCIATEFONT2**</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-119"><dt>**SCF\_ASSOCIATEFONT2**</dt></span></span> </dl>    | <span data-ttu-id="e6983-120">**RichEdit 4,1:** Ordnet einem angegebenen Skript eine Ersatz Zeichen Schriftart (Plane-2) zu, sodass die Standard Schriftart für dieses Skript geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e6983-120">**RichEdit 4.1:** Associates a surrogate (plane-2) font to a given script, thus changing the default font for that script.</span></span> <span data-ttu-id="e6983-121">Um die Schriftart anzugeben, verwenden Sie die folgenden Member von [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bcharset**, **bpitchandfamily**, **szfakename** und **LCID**.</span><span class="sxs-lookup"><span data-stu-id="e6983-121">To specify the font, use the following members of [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid**.</span></span><br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <span data-ttu-id="e6983-122"><dt>**SCF \_ charrepfromlcid**</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-122"><dt>**SCF\_CHARREPFROMLCID**</dt></span></span> </dl> | <span data-ttu-id="e6983-123">Ruft das Zeichen Repertoire aus der LCID ab.</span><span class="sxs-lookup"><span data-stu-id="e6983-123">Gets the character repertoire from the LCID.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <span data-ttu-id="e6983-124"><dt>**SCF- \_ Standard**</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-124"><dt>**SCF\_DEFAULT**</dt></span></span> </dl>                         | <span data-ttu-id="e6983-125">**RichEdit 4,1:** Legt die Standard Schriftart für das-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="e6983-125">**RichEdit 4.1:** Sets the default font for the control.</span></span> <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <span data-ttu-id="e6983-126"><dt>**SPF- \_ dontsetdefault**</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-126"><dt>**SPF\_DONTSETDEFAULT**</dt></span></span> </dl>    | <span data-ttu-id="e6983-127">Verhindert das Festlegen des Standard Absatz Formats, wenn das Rich Edit-Steuerelement leer ist.</span><span class="sxs-lookup"><span data-stu-id="e6983-127">Prevents setting the default paragraph format when the rich edit control is empty.</span></span><br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <span data-ttu-id="e6983-128"><dt>**SCF- \_ nokbupdate**</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-128"><dt>**SCF\_NOKBUPDATE**</dt></span></span> </dl>                | <span data-ttu-id="e6983-129">**RichEdit 4,1:** Verhindert, dass der Tastatur Wechsel der Schriftart entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6983-129">**RichEdit 4.1:** Prevents keyboard switching to match the font.</span></span> <span data-ttu-id="e6983-130">Wenn z. b. eine arabische Schriftart festgelegt ist, ändert die automatische Tastatur Funktion für Bidi-Sprachen die Tastatur in eine arabische Tastatur.</span><span class="sxs-lookup"><span data-stu-id="e6983-130">For example, if an Arabic font is set, normally the automatic keyboard feature for Bidi languages changes the keyboard to an Arabic keyboard.</span></span><br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <span data-ttu-id="e6983-131"><dt>**SCF- \_ Auswahl**</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-131"><dt>**SCF\_SELECTION**</dt></span></span> </dl>                   | <span data-ttu-id="e6983-132">Wendet die Formatierung auf die aktuelle Auswahl an.</span><span class="sxs-lookup"><span data-stu-id="e6983-132">Applies the formatting to the current selection.</span></span> <span data-ttu-id="e6983-133">Wenn die Auswahl leer ist, wird die Zeichen Formatierung auf die Einfügemarke angewendet, und das neue Zeichenformat ist nur bis zur Änderung der Einfügemarke wirksam.</span><span class="sxs-lookup"><span data-stu-id="e6983-133">If the selection is empty, the character formatting is applied to the insertion point, and the new character format is in effect only until the insertion point changes.</span></span><br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <span data-ttu-id="e6983-134"><dt>**SPF ( \_ SetDefault)**</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-134"><dt>**SPF\_SETDEFAULT**</dt></span></span> </dl>                | <span data-ttu-id="e6983-135">Legt die standardmäßigen Absatz Formatierungs Attribute fest.</span><span class="sxs-lookup"><span data-stu-id="e6983-135">Sets the default paragraph formatting attributes.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <span data-ttu-id="e6983-136"><dt>**SCF- \_ smartfont**</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-136"><dt>**SCF\_SMARTFONT**</dt></span></span> </dl>                   | <span data-ttu-id="e6983-137">Wenden Sie die Schriftart nur an, wenn Sie das Skript behandeln kann.</span><span class="sxs-lookup"><span data-stu-id="e6983-137">Apply the font only if it can handle script.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <span data-ttu-id="e6983-138"><dt>**SCF- \_ useuirules**</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-138"><dt>**SCF\_USEUIRULES**</dt></span></span> </dl>                | <span data-ttu-id="e6983-139">**RichEdit 4,1:** Wird bei der **SCF- \_ Auswahl** verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6983-139">**RichEdit 4.1:** Used with **SCF\_SELECTION**.</span></span> <span data-ttu-id="e6983-140">Gibt an, dass das Format von einer Symbolleiste oder einem anderen UI-Tool stammt, sodass anstelle der literalen Formatierung UI-Formatierungs Regeln verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e6983-140">Indicates that format came from a toolbar or other UI tool, so UI formatting rules should be used instead of literal formatting.</span></span><br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <span data-ttu-id="e6983-141"><dt>**SCF- \_ Wort**</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-141"><dt>**SCF\_WORD**</dt></span></span> </dl>                                  | <span data-ttu-id="e6983-142">Wendet die Formatierung auf das ausgewählte Wort oder die Wörter an.</span><span class="sxs-lookup"><span data-stu-id="e6983-142">Applies the formatting to the selected word or words.</span></span> <span data-ttu-id="e6983-143">Wenn die Auswahl leer ist, die Einfügemarke aber in einem Wort liegt, wird die Formatierung auf das Wort angewendet.</span><span class="sxs-lookup"><span data-stu-id="e6983-143">If the selection is empty but the insertion point is inside a word, the formatting is applied to the word.</span></span> <span data-ttu-id="e6983-144">Der **SCF- \_ Wort** Wert muss in Verbindung mit dem **SCF- \_ Auswahl** Wert verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6983-144">The **SCF\_WORD** value must be used in conjunction with the **SCF\_SELECTION** value.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="e6983-145">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6983-145">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6983-146">Zeiger auf eine [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) -Struktur, die die zu verwendende Zeichen Formatierung angibt.</span><span class="sxs-lookup"><span data-stu-id="e6983-146">Pointer to a [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure specifying the character formatting to use.</span></span> <span data-ttu-id="e6983-147">Nur die Formatierungs Attribute, die vom **dwMask** -Member angegeben werden, werden geändert.</span><span class="sxs-lookup"><span data-stu-id="e6983-147">Only the formatting attributes specified by the **dwMask** member are changed.</span></span>

<span data-ttu-id="e6983-148">Microsoft Rich Edit 2,0 und höher: dieser Parameter kann ein Zeiger auf eine [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) -Struktur sein, die eine Erweiterung der [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) -Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="e6983-148">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure, which is an extension of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span> <span data-ttu-id="e6983-149">Vor dem Senden der **EM- \_ setcharformat** -Meldung legen Sie den **CBSIZE** -Member der Struktur auf fest, `sizeof(CHARFORMAT)` oder geben Sie an, `sizeof(CHARFORMAT2)` welche Version der Struktur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6983-149">Before sending the **EM\_SETCHARFORMAT** message, set the structure's **cbSize** member to `sizeof(CHARFORMAT)` or `sizeof(CHARFORMAT2)` indicate which version of the structure is being used.</span></span>

<span data-ttu-id="e6983-150">Die Elemente **szfakename** und **bcharset** können überschrieben werden, wenn Sie für Zeichen ungültig sind, z. b. Arial für Kanji-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e6983-150">The **szFaceName** and **bCharSet** members may be overruled when invalid for characters, for example: Arial on kanji characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6983-151">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6983-151">Return value</span></span>

<span data-ttu-id="e6983-152">Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e6983-152">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e6983-153">Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e6983-153">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6983-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6983-154">Remarks</span></span>

<span data-ttu-id="e6983-155">Wenn diese Nachricht mehrmals mit denselben Parametern gesendet wird, wird die Auswirkung auf den Text ein-und ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="e6983-155">If this message is sent more than once with the same parameters, the effect on the text is toggled.</span></span> <span data-ttu-id="e6983-156">Das bedeutet, dass das Senden der Nachricht einmal den Effekt erzeugt, dass das Senden der Nachricht zweimal den Effekt abbricht usw.</span><span class="sxs-lookup"><span data-stu-id="e6983-156">That is, sending the message once produces the effect, sending the message twice cancels the effect, and so forth.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6983-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6983-157">Requirements</span></span>



| <span data-ttu-id="e6983-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6983-158">Requirement</span></span> | <span data-ttu-id="e6983-159">Wert</span><span class="sxs-lookup"><span data-stu-id="e6983-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6983-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6983-160">Minimum supported client</span></span><br/> | <span data-ttu-id="e6983-161">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6983-161">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6983-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6983-162">Minimum supported server</span></span><br/> | <span data-ttu-id="e6983-163">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6983-163">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6983-164">Header</span><span class="sxs-lookup"><span data-stu-id="e6983-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6983-165"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6983-165"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6983-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6983-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6983-167">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="e6983-167">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e6983-168">**Charformat**</span><span class="sxs-lookup"><span data-stu-id="e6983-168">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[<span data-ttu-id="e6983-169">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="e6983-169">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





