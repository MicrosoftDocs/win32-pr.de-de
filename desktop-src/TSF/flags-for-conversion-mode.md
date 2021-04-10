---
title: Flags für den Konvertierungsmodus (ctffunc. h)
description: Die folgenden Flags werden als Wert von "GUID Depot \_ - \_ Tastatur \_ Eingabe im InputMode" verwendet \_ . Dies entspricht den IME- \_ cmode-Werten für imm32.
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- Flags für den Konvertierungsmodus-Text Dienst-Framework
topic_type:
- apiref
api_name:
- Flags for Conversion Mode
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022712ff45f213992bf3d40bd0149959e4864faa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104121"
---
# <a name="flags-for-conversion-mode"></a><span data-ttu-id="ed0ab-105">Flags für den Konvertierungsmodus</span><span class="sxs-lookup"><span data-stu-id="ed0ab-105">Flags for Conversion Mode</span></span>

<span data-ttu-id="ed0ab-106">Die folgenden Flags werden als Wert von " [GUID Depot \_ - \_ Tastatur \_ Eingabe im InputMode \_ ](predefined-compartments.md)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-106">The following flags are used as a value of [GUID\_COMPARTMENT\_KEYBOARD\_INPUTMODE\_CONVERSION](predefined-compartments.md).</span></span> <span data-ttu-id="ed0ab-107">Dies entspricht den [IME- \_ cmode](../intl/ime-conversion-mode-values.md) -Werten für imm32.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-107">This is equivalent with [IME\_CMODE](../intl/ime-conversion-mode-values.md) values for IMM32.</span></span>



| <span data-ttu-id="ed0ab-108">Flag</span><span class="sxs-lookup"><span data-stu-id="ed0ab-108">Flag</span></span>                             | <span data-ttu-id="ed0ab-109">Wert</span><span class="sxs-lookup"><span data-stu-id="ed0ab-109">Value</span></span>  | <span data-ttu-id="ed0ab-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed0ab-110">Description</span></span>                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| <span data-ttu-id="ed0ab-111">TF in der \_ alphanumerischen Version des TF-Modus \_</span><span class="sxs-lookup"><span data-stu-id="ed0ab-111">TF\_CONVERSIONMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="ed0ab-112">0x0000</span><span class="sxs-lookup"><span data-stu-id="ed0ab-112">0x0000</span></span> | <span data-ttu-id="ed0ab-113">Auf 1 festgelegt, wenn alphanumerischer Modus.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-113">Set to 1 if ALPHANUMERIC mode.</span></span>                                  |
| <span data-ttu-id="ed0ab-114">TF- \_ Konfigurations Modus ( \_ nativ)</span><span class="sxs-lookup"><span data-stu-id="ed0ab-114">TF\_CONVERSIONMODE\_NATIVE</span></span>       | <span data-ttu-id="ed0ab-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="ed0ab-115">0x0001</span></span> | <span data-ttu-id="ed0ab-116">Auf 1 festgelegt, wenn der einheitliche Modus ist; 0 (null), wenn der alphanumerische Modus ist.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-116">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                |
| <span data-ttu-id="ed0ab-117">TF- \_ systemversionmoduskatakana \_</span><span class="sxs-lookup"><span data-stu-id="ed0ab-117">TF\_CONVERSIONMODE\_KATAKANA</span></span>     | <span data-ttu-id="ed0ab-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="ed0ab-118">0x0002</span></span> | <span data-ttu-id="ed0ab-119">Auf 1 festgelegt, wenn Katakana-Modus; 0, wenn der Hiragana-Modus ist.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-119">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                  |
| <span data-ttu-id="ed0ab-120">TF-Konstante für den Verbindungs \_ Modus \_</span><span class="sxs-lookup"><span data-stu-id="ed0ab-120">TF\_CONVERSIONMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="ed0ab-121">0x0008</span><span class="sxs-lookup"><span data-stu-id="ed0ab-121">0x0008</span></span> | <span data-ttu-id="ed0ab-122">Auf 1 festgelegt, wenn vollständiger Shape-Modus; 0 (null), wenn Halbform Modus.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-122">Set to 1 if full shape mode; 0 if half shape mode.</span></span>              |
| <span data-ttu-id="ed0ab-123">TF-Verbindungs \_ Modus \_</span><span class="sxs-lookup"><span data-stu-id="ed0ab-123">TF\_CONVERSIONMODE\_ROMAN</span></span>        | <span data-ttu-id="ed0ab-124">0x0010</span><span class="sxs-lookup"><span data-stu-id="ed0ab-124">0x0010</span></span> | <span data-ttu-id="ed0ab-125">Auf 1 festgelegt, um die Verarbeitung von Konvertierungen durch IME zu verhindern. 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-125">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span> |
| <span data-ttu-id="ed0ab-126">TF- \_ konforme \_ CharCode</span><span class="sxs-lookup"><span data-stu-id="ed0ab-126">TF\_CONVERSIONMODE\_CHARCODE</span></span>     | <span data-ttu-id="ed0ab-127">0x0020</span><span class="sxs-lookup"><span data-stu-id="ed0ab-127">0x0020</span></span> | <span data-ttu-id="ed0ab-128">Auf 1 festgelegt, wenn Zeichencode Eingabemodus; 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-128">Set to 1 if character code input mode; 0 if not.</span></span>                |
| <span data-ttu-id="ed0ab-129">TF-Verbindungs \_ Modus-Bildschirm \_ Tastatur</span><span class="sxs-lookup"><span data-stu-id="ed0ab-129">TF\_CONVERSIONMODE\_SOFTKEYBOARD</span></span> | <span data-ttu-id="ed0ab-130">0x0080</span><span class="sxs-lookup"><span data-stu-id="ed0ab-130">0x0080</span></span> | <span data-ttu-id="ed0ab-131">Auf 1 festgelegt, wenn weicher Tastaturmodus 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-131">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                       |
| <span data-ttu-id="ed0ab-132">TF- \_ Konversions Modus- \_ noconversion</span><span class="sxs-lookup"><span data-stu-id="ed0ab-132">TF\_CONVERSIONMODE\_NOCONVERSION</span></span> | <span data-ttu-id="ed0ab-133">0x0100</span><span class="sxs-lookup"><span data-stu-id="ed0ab-133">0x0100</span></span> | <span data-ttu-id="ed0ab-134">Auf 1 festgelegt, um die Verarbeitung von Konvertierungen durch IME zu verhindern. 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-134">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span> |
| <span data-ttu-id="ed0ab-135">TF-Symbol für " \_ deversionmode" \_</span><span class="sxs-lookup"><span data-stu-id="ed0ab-135">TF\_CONVERSIONMODE\_SYMBOL</span></span>       | <span data-ttu-id="ed0ab-136">0x0400</span><span class="sxs-lookup"><span data-stu-id="ed0ab-136">0x0400</span></span> | <span data-ttu-id="ed0ab-137">Auf 1 festgelegt, wenn der Modus für die Symbol Konvertierung 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-137">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                   |
| <span data-ttu-id="ed0ab-138">TF-Verbindungs \_ Modus \_ korrigiert</span><span class="sxs-lookup"><span data-stu-id="ed0ab-138">TF\_CONVERSIONMODE\_FIXED</span></span>        | <span data-ttu-id="ed0ab-139">0x0800</span><span class="sxs-lookup"><span data-stu-id="ed0ab-139">0x0800</span></span> | <span data-ttu-id="ed0ab-140">Auf 1 festgelegt, wenn fester Konvertierungsmodus; 0, wenn nicht.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-140">Set to 1 if fixed conversion mode; 0 if not.</span></span>                    |



 

<span data-ttu-id="ed0ab-141">Die folgenden Werte werden als Wert von " [GUID Depot \_ \_ Tastatur \_ InputMode- \_ Satz](predefined-compartments.md)" verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-141">The following values are used as a value of [GUID\_COMPARTMENT\_KEYBOARD\_INPUTMODE\_SENTENCE](predefined-compartments.md).</span></span> <span data-ttu-id="ed0ab-142">Dies entspricht den [IME- \_ smode](../intl/ime-composition-string-values.md) -Werten für imm32.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-142">This is equivalent with [IME\_SMODE](../intl/ime-composition-string-values.md) values for IMM32.</span></span>



| <span data-ttu-id="ed0ab-143">Flag</span><span class="sxs-lookup"><span data-stu-id="ed0ab-143">Flag</span></span>                            | <span data-ttu-id="ed0ab-144">Wert</span><span class="sxs-lookup"><span data-stu-id="ed0ab-144">Value</span></span>  | <span data-ttu-id="ed0ab-145">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed0ab-145">Description</span></span>                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| <span data-ttu-id="ed0ab-146">TF \_ sentencemode \_ None</span><span class="sxs-lookup"><span data-stu-id="ed0ab-146">TF\_SENTENCEMODE\_NONE</span></span>          | <span data-ttu-id="ed0ab-147">0x0000</span><span class="sxs-lookup"><span data-stu-id="ed0ab-147">0x0000</span></span> | <span data-ttu-id="ed0ab-148">Keine Informationen für einen Satz.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-148">No information for sentence.</span></span>                                               |
| <span data-ttu-id="ed0ab-149">TF \_ sentencemode- \_ plauralklausel</span><span class="sxs-lookup"><span data-stu-id="ed0ab-149">TF\_SENTENCEMODE\_PLAURALCLAUSE</span></span> | <span data-ttu-id="ed0ab-150">0x0001</span><span class="sxs-lookup"><span data-stu-id="ed0ab-150">0x0001</span></span> | <span data-ttu-id="ed0ab-151">Der IME verwendet die Plural-klauselinformationen, um die Konvertierungs Verarbeitung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-151">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="ed0ab-152">TF \_ sentencemode \_ singleconvert</span><span class="sxs-lookup"><span data-stu-id="ed0ab-152">TF\_SENTENCEMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="ed0ab-153">0x0002</span><span class="sxs-lookup"><span data-stu-id="ed0ab-153">0x0002</span></span> | <span data-ttu-id="ed0ab-154">Der IME führt die Konvertierungs Verarbeitung im Einzelzeichen Modus aus.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-154">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="ed0ab-155">TF \_ sentencemode \_ automatisch</span><span class="sxs-lookup"><span data-stu-id="ed0ab-155">TF\_SENTENCEMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="ed0ab-156">0x0004</span><span class="sxs-lookup"><span data-stu-id="ed0ab-156">0x0004</span></span> | <span data-ttu-id="ed0ab-157">Der IME führt die Konvertierungs Verarbeitung im automatischen Modus aus.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-157">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="ed0ab-158">TF \_ sentencemode \_ phraervorhersage</span><span class="sxs-lookup"><span data-stu-id="ed0ab-158">TF\_SENTENCEMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="ed0ab-159">0x0008</span><span class="sxs-lookup"><span data-stu-id="ed0ab-159">0x0008</span></span> | <span data-ttu-id="ed0ab-160">Der IME verwendet Ausdrucks Informationen, um das nächste Zeichen vorherzusagen.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-160">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="ed0ab-161">TF \_ sentencemode- \_ Konversation</span><span class="sxs-lookup"><span data-stu-id="ed0ab-161">TF\_SENTENCEMODE\_CONVERSATION</span></span>  | <span data-ttu-id="ed0ab-162">0x0010</span><span class="sxs-lookup"><span data-stu-id="ed0ab-162">0x0010</span></span> | <span data-ttu-id="ed0ab-163">Der IME verwendet den Konversationsmodus.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-163">The IME uses conversation mode.</span></span> <span data-ttu-id="ed0ab-164">Dies ist nützlich für Chat Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="ed0ab-164">This is useful for chat applications.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="ed0ab-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed0ab-165">Requirements</span></span>



| <span data-ttu-id="ed0ab-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed0ab-166">Requirement</span></span> | <span data-ttu-id="ed0ab-167">Wert</span><span class="sxs-lookup"><span data-stu-id="ed0ab-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed0ab-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed0ab-168">Minimum supported client</span></span><br/> | <span data-ttu-id="ed0ab-169">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed0ab-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ed0ab-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed0ab-170">Minimum supported server</span></span><br/> | <span data-ttu-id="ed0ab-171">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed0ab-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ed0ab-172">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ed0ab-172">Redistributable</span></span><br/>          | <span data-ttu-id="ed0ab-173">TSF 1,0 onwindows NT 4.0, Windows 2000 professionalandwindows meWindows 98</span><span class="sxs-lookup"><span data-stu-id="ed0ab-173">TSF 1.0 onWindows NT 4.0,Windows 2000 ProfessionalandWindows MeWindows 98</span></span><br/>   |
| <span data-ttu-id="ed0ab-174">Header</span><span class="sxs-lookup"><span data-stu-id="ed0ab-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed0ab-175"><dt>Ctffunc. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed0ab-175"><dt>Ctffunc.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed0ab-176">IDL</span><span class="sxs-lookup"><span data-stu-id="ed0ab-176">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ed0ab-177"><dt>Ctffunc. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ed0ab-177"><dt>Ctffunc.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed0ab-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed0ab-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed0ab-179">Vordefinierte Depots</span><span class="sxs-lookup"><span data-stu-id="ed0ab-179">Predefined Compartments</span></span>](predefined-compartments.md)
</dt> </dl>

 

