---
title: EM_SETCTFMODEBIAS Meldung (RichEdit. h)
description: Legt den TSF-Modus (Text Services Framework) für ein Rich-Edit-Steuerelement fest.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- Windows-Steuerelemente für EM_SETCTFMODEBIAS Meldung
topic_type:
- apiref
api_name:
- EM_SETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b872fa5489c898ec4482ecdc094de7df6e3180be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518674"
---
# <a name="em_setctfmodebias-message"></a><span data-ttu-id="9cdbe-104">EM \_ setctf modebias-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9cdbe-104">EM\_SETCTFMODEBIAS message</span></span>

<span data-ttu-id="9cdbe-105">Legt den TSF-Modus (Text Services Framework) für ein Rich-Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-105">Sets the Text Services Framework (TSF) mode bias for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9cdbe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9cdbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cdbe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9cdbe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9cdbe-108">Moduswert.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-108">Mode bias value.</span></span> <span data-ttu-id="9cdbe-109">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="9cdbe-109">This can be one of the following values.</span></span>



| <span data-ttu-id="9cdbe-110">Wert</span><span class="sxs-lookup"><span data-stu-id="9cdbe-110">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="9cdbe-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9cdbe-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <span data-ttu-id="9cdbe-112"><dt>**CTF modebias ( \_ Standard)**</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbe-112"><dt>**CTFMODEBIAS\_DEFAULT**</dt></span></span> </dl>                                           | <span data-ttu-id="9cdbe-113">Es gibt keine Modus-Abweichung.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-113">There is no mode bias.</span></span><br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <span data-ttu-id="9cdbe-114"><dt>**CTF modebias- \_ Dateiname**</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbe-114"><dt>**CTFMODEBIAS\_FILENAME**</dt></span></span> </dl>                                        | <span data-ttu-id="9cdbe-115">Die Verschiebung ist ein Dateiname.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-115">The bias is to a filename.</span></span><br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <span data-ttu-id="9cdbe-116"><dt>**Name des CTF modebias \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbe-116"><dt>**CTFMODEBIAS\_NAME**</dt></span></span> </dl>                                                    | <span data-ttu-id="9cdbe-117">Die Verschiebung ist ein Name.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-117">The bias is to a name.</span></span><br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <span data-ttu-id="9cdbe-118"><dt>**CTF modebias- \_ Lesevorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbe-118"><dt>**CTFMODEBIAS\_READING**</dt></span></span> </dl>                                           | <span data-ttu-id="9cdbe-119">Die Verschiebung ist das lesen.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-119">The bias is to the reading.</span></span><br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <span data-ttu-id="9cdbe-120"><dt>**CTF modebias \_ DateTime**</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbe-120"><dt>**CTFMODEBIAS\_DATETIME**</dt></span></span> </dl>                                        | <span data-ttu-id="9cdbe-121">Der Bias ist ein Datum oder eine Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-121">The bias is to a date or time.</span></span><br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <span data-ttu-id="9cdbe-122"><dt>**CTF modebias- \_ Konversation**</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbe-122"><dt>**CTFMODEBIAS\_CONVERSATION**</dt></span></span> </dl>                            | <span data-ttu-id="9cdbe-123">Der Bias ist eine Konversation.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-123">The bias is to a conversation.</span></span><br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <span data-ttu-id="9cdbe-124"><dt>**CTF modebias \_ numerisch**</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbe-124"><dt>**CTFMODEBIAS\_NUMERIC**</dt></span></span> </dl>                                           | <span data-ttu-id="9cdbe-125">Der Bias ist eine Zahl.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-125">The bias is to a number.</span></span><br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <span data-ttu-id="9cdbe-126"><dt>**CTF modebias \_ Hiragana**</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbe-126"><dt>**CTFMODEBIAS\_HIRAGANA**</dt></span></span> </dl>                                        | <span data-ttu-id="9cdbe-127">Die Verschiebung erfolgt auf Hiragana-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-127">The bias is to hiragana strings.</span></span><br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <span data-ttu-id="9cdbe-128"><dt>**CTF modebias \_ Katakana**</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbe-128"><dt>**CTFMODEBIAS\_KATAKANA**</dt></span></span> </dl>                                        | <span data-ttu-id="9cdbe-129">Die Verschiebung erfolgt auf Katakana-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-129">The bias is to katakana strings.</span></span><br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <span data-ttu-id="9cdbe-130"><dt>**CTF modebias \_ Hangul**</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbe-130"><dt>**CTFMODEBIAS\_HANGUL**</dt></span></span> </dl>                                              | <span data-ttu-id="9cdbe-131">Die Verschiebung erfolgt auf Hangul-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-131">The bias is to Hangul characters.</span></span><br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <span data-ttu-id="9cdbe-132"><dt>**CTF modebias \_ halfwidthkatakana**</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbe-132"><dt>**CTFMODEBIAS\_HALFWIDTHKATAKANA**</dt></span></span> </dl>             | <span data-ttu-id="9cdbe-133">Die Verschiebung erfolgt auf Katakana-Zeichen folgen der Hälfte Breite.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-133">The bias is to half-width katakana strings.</span></span><br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <span data-ttu-id="9cdbe-134"><dt>**ctfmodebias \_ fullwidthalpha numerisch**</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbe-134"><dt>**CTFMODEBIAS\_FULLWIDTHALPHANUMERIC**</dt></span></span> </dl> | <span data-ttu-id="9cdbe-135">Der Bias besteht aus alphanumerischen Zeichen mit voller Breite.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-135">The bias is to full-width alphanumeric characters.</span></span><br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <span data-ttu-id="9cdbe-136"><dt>**ctfmodebias \_ halfwidthalpha numerisch**</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbe-136"><dt>**CTFMODEBIAS\_HALFWIDTHALPHANUMERIC**</dt></span></span> </dl> | <span data-ttu-id="9cdbe-137">Die Verschiebung erfolgt auf alphanumerische Zeichen mit halber Breite.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-137">The bias is to half-width alphanumeric characters.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9cdbe-138">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9cdbe-138">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9cdbe-139">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-139">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cdbe-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9cdbe-140">Return value</span></span>

<span data-ttu-id="9cdbe-141">Bei erfolgreicher Ausführung ist der Rückgabewert der neue Wert des TSF-Modus-Bias.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-141">If successful, the return value is the new TSF mode bias value.</span></span> <span data-ttu-id="9cdbe-142">Wenn nicht erfolgreich, ist der Rückgabewert der alte Wert des TSF-Modus-Bias.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-142">If unsuccessful, the return value is the old TSF mode bias value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cdbe-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9cdbe-143">Remarks</span></span>

<span data-ttu-id="9cdbe-144">Wenn eine Microsoft Rich Edit-Anwendung TSF verwendet, kann Sie den TSF-Modus "Bias" auswählen.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-144">When a Microsoft Rich Edit application uses TSF, it can select the TSF mode bias.</span></span> <span data-ttu-id="9cdbe-145">In dieser Meldung werden die Kriterien festgelegt, mit denen eine Alternative Auswahl am oberen Rand der Liste zur Auswahl angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9cdbe-145">This message sets the criteria by which an alternative choice appears at the top of the list for selection.</span></span>

<span data-ttu-id="9cdbe-146">Um die modusabweichung für den Eingabemethoden-Editor (Input Method Editor, IME) festzulegen, verwenden Sie [**EM \_ setimemodebias**](em-setimemodebias.md).</span><span class="sxs-lookup"><span data-stu-id="9cdbe-146">To set the mode bias for the Input Method Editor (IME), use [**EM\_SETIMEMODEBIAS**](em-setimemodebias.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cdbe-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cdbe-147">Requirements</span></span>



| <span data-ttu-id="9cdbe-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cdbe-148">Requirement</span></span> | <span data-ttu-id="9cdbe-149">Wert</span><span class="sxs-lookup"><span data-stu-id="9cdbe-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9cdbe-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9cdbe-150">Minimum supported client</span></span><br/> | <span data-ttu-id="9cdbe-151">Nur Windows XP mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9cdbe-151">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9cdbe-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9cdbe-152">Minimum supported server</span></span><br/> | <span data-ttu-id="9cdbe-153">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9cdbe-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9cdbe-154">Header</span><span class="sxs-lookup"><span data-stu-id="9cdbe-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cdbe-155"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cdbe-155"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cdbe-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cdbe-156">See also</span></span>

<dl> <dt>

<span data-ttu-id="9cdbe-157">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9cdbe-157">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9cdbe-158">**EM \_ getctf modebias**</span><span class="sxs-lookup"><span data-stu-id="9cdbe-158">**EM\_GETCTFMODEBIAS**</span></span>](em-getctfmodebias.md)
</dt> <dt>

[<span data-ttu-id="9cdbe-159">**EM- \_ Zeit modebias**</span><span class="sxs-lookup"><span data-stu-id="9cdbe-159">**EM\_SETIMEMODEBIAS**</span></span>](em-setimemodebias.md)
</dt> </dl>

 

 





