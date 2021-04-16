---
title: EM_SETFONTSIZE Meldung (RichEdit. h)
description: Legt den Schrift Grad für den ausgewählten Text in einem Rich-Edit-Steuerelement fest.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- Windows-Steuerelemente für EM_SETFONTSIZE Meldung
topic_type:
- apiref
api_name:
- EM_SETFONTSIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb75276acbb86cbd452a8ad97698f1cd7382bd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476830"
---
# <a name="em_setfontsize-message"></a><span data-ttu-id="16675-104">EM \_ SetFontSize-Meldung</span><span class="sxs-lookup"><span data-stu-id="16675-104">EM\_SETFONTSIZE message</span></span>

<span data-ttu-id="16675-105">Legt den Schrift Grad für den ausgewählten Text in einem Rich-Edit-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="16675-105">Sets the font size for the selected text in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="16675-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="16675-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16675-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16675-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16675-108">Ändern der Punktgröße des ausgewählten Texts.</span><span class="sxs-lookup"><span data-stu-id="16675-108">Change in point size of the selected text.</span></span> <span data-ttu-id="16675-109">Das Ergebnis wird entsprechend den in der folgenden Tabelle gezeigten Werten gerundet.</span><span class="sxs-lookup"><span data-stu-id="16675-109">The result will be rounded according to values shown in the following table.</span></span> <span data-ttu-id="16675-110">Dieser Parameter sollte im Bereich von-1637 bis 1638 liegen.</span><span class="sxs-lookup"><span data-stu-id="16675-110">This parameter should be in the range of -1637 to 1638.</span></span> <span data-ttu-id="16675-111">Die resultierende Schriftgröße liegt im Bereich von 1 bis 1638.</span><span class="sxs-lookup"><span data-stu-id="16675-111">The resulting font size will be within the range of 1 to 1638.</span></span>

</dd> <dt>

<span data-ttu-id="16675-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16675-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16675-113">Dieser Parameter wird nicht verwendet. Er muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="16675-113">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16675-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16675-114">Return value</span></span>

<span data-ttu-id="16675-115">Wenn kein Fehler aufgetreten ist, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="16675-115">If no error occurred, the return value is **TRUE**.</span></span>

<span data-ttu-id="16675-116">Wenn ein Fehler aufgetreten ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="16675-116">If an error occurred, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="16675-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16675-117">Remarks</span></span>

<span data-ttu-id="16675-118">Sie können den Schrift Grad auf einfache Weise durch Senden der [**EM \_ getcharformat**](em-getcharformat.md) -Meldung erhalten.</span><span class="sxs-lookup"><span data-stu-id="16675-118">You can easily get the font size by sending the [**EM\_GETCHARFORMAT**](em-getcharformat.md) message.</span></span>

<span data-ttu-id="16675-119">Rich Edit fügt zuerst dem aktuellen Schrift Grad *wParam* hinzu und verwendet dann die resultierende Größe und die folgende Tabelle, um den Rundungs Wert zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="16675-119">Rich Edit first adds *wParam* to the current font size and then uses the resulting size and the following table to determine the rounding value.</span></span>



| <span data-ttu-id="16675-120">Kreuz</span><span class="sxs-lookup"><span data-stu-id="16675-120">Band</span></span>    | <span data-ttu-id="16675-121">Rundungs Wert</span><span class="sxs-lookup"><span data-stu-id="16675-121">Rounding value</span></span> |
|---------|----------------|
| <span data-ttu-id="16675-122"><= 12</span><span class="sxs-lookup"><span data-stu-id="16675-122"><=12</span></span> | <span data-ttu-id="16675-123">1</span><span class="sxs-lookup"><span data-stu-id="16675-123">1</span></span>              |
| <span data-ttu-id="16675-124">28</span><span class="sxs-lookup"><span data-stu-id="16675-124">28</span></span>      | <span data-ttu-id="16675-125">2</span><span class="sxs-lookup"><span data-stu-id="16675-125">2</span></span>              |
| <span data-ttu-id="16675-126">36</span><span class="sxs-lookup"><span data-stu-id="16675-126">36</span></span>      | <span data-ttu-id="16675-127">0</span><span class="sxs-lookup"><span data-stu-id="16675-127">0</span></span>              |
| <span data-ttu-id="16675-128">48</span><span class="sxs-lookup"><span data-stu-id="16675-128">48</span></span>      | <span data-ttu-id="16675-129">0</span><span class="sxs-lookup"><span data-stu-id="16675-129">0</span></span>              |
| <span data-ttu-id="16675-130">72</span><span class="sxs-lookup"><span data-stu-id="16675-130">72</span></span>      | <span data-ttu-id="16675-131">0</span><span class="sxs-lookup"><span data-stu-id="16675-131">0</span></span>              |
| <span data-ttu-id="16675-132">80</span><span class="sxs-lookup"><span data-stu-id="16675-132">80</span></span>      | <span data-ttu-id="16675-133">0</span><span class="sxs-lookup"><span data-stu-id="16675-133">0</span></span>              |
| <span data-ttu-id="16675-134">> 80</span><span class="sxs-lookup"><span data-stu-id="16675-134">> 80</span></span> | <span data-ttu-id="16675-135">10</span><span class="sxs-lookup"><span data-stu-id="16675-135">10</span></span>             |



 

<span data-ttu-id="16675-136">Wenn die resultierende Schriftgröße durch den Rundungs Wert nicht gleichmäßig teilbar ist, wird der Schrift Grad auf eine Zahl gerundet, die durch den Rundungs Wert gleichmäßig erkennbar ist.</span><span class="sxs-lookup"><span data-stu-id="16675-136">If the resulting font size is not evenly divisible by the rounding value, the font size is then rounded to a number evenly divisible by the rounding value.</span></span> <span data-ttu-id="16675-137">Wenn die Schriftgröße also kleiner oder gleich 12 ist, lautet der Rundungs Wert 1.</span><span class="sxs-lookup"><span data-stu-id="16675-137">So if the font size is less than or equal to 12, the rounding value will be 1.</span></span> <span data-ttu-id="16675-138">Ebenso ist der Rundungs Wert 2, wenn der Schrift Grad kleiner oder gleich 28 ist.</span><span class="sxs-lookup"><span data-stu-id="16675-138">Similarly, if the font size is less than or equal to 28, the rounding value is 2.</span></span> <span data-ttu-id="16675-139">Bei Werten, die größer als 28 sind, werden die Schriftgrößen auf das nächste Band gerundet.</span><span class="sxs-lookup"><span data-stu-id="16675-139">For values greater than 28, font sizes are rounded to the next band.</span></span> <span data-ttu-id="16675-140">Daher springt die Schriftgröße zu 36, 48, 72, 80.</span><span class="sxs-lookup"><span data-stu-id="16675-140">So, the font size jumps to 36, 48, 72, 80.</span></span> <span data-ttu-id="16675-141">Nach 80 werden alle Rundungen in Schritten von zehn Punkten durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="16675-141">After 80, all rounding is done in increments of ten points.</span></span>

<span data-ttu-id="16675-142">Der Schrift Grad ist abhängig vom Vorzeichen von *wParam* nach oben oder unten aufgerundet.</span><span class="sxs-lookup"><span data-stu-id="16675-142">The font size is rounded up or down depending on the sign of *wParam*.</span></span> <span data-ttu-id="16675-143">Wenn *wParam* positiv ist, ist die Rundung immer auf dem neuesten Stand.</span><span class="sxs-lookup"><span data-stu-id="16675-143">If *wParam* is positive, the rounding is always up.</span></span> <span data-ttu-id="16675-144">Andernfalls ist die Rundung immer herunter.</span><span class="sxs-lookup"><span data-stu-id="16675-144">Otherwise, rounding is always down.</span></span> <span data-ttu-id="16675-145">Wenn die aktuelle Schriftgröße den Wert 10 hat und *wParam* den Wert 3 hat, beträgt die resultierende Schriftgröße 14 (10 + 3 = 13, die nicht durch 2 teilbar ist, sodass die Größe auf 14 aufgerundet wird).</span><span class="sxs-lookup"><span data-stu-id="16675-145">So, if the current font size is 10 and *wParam* is 3, the resulting font size would be 14 (10 + 3 = 13, which is not divisible by 2, so the size rounds up to 14).</span></span> <span data-ttu-id="16675-146">Wenn die aktuelle Schriftgröße den Wert 14 hat und *wParam* den Wert-3 hat, ist die resultierende Schriftgröße 10 (14-3 = 11, der nicht durch 2 teilbar ist, sodass die Größe auf 10 gerundet).</span><span class="sxs-lookup"><span data-stu-id="16675-146">Conversely, if the current font size is 14 and *wParam* is -3, the resulting font size would be 10 (14 - 3 = 11, which is not divisible by 2, so the size rounds down to 10).</span></span>

<span data-ttu-id="16675-147">Die Änderung wird auf jeden Teil der Auswahl angewendet.</span><span class="sxs-lookup"><span data-stu-id="16675-147">The change is applied to each part of the selection.</span></span> <span data-ttu-id="16675-148">Wenn ein Teil des Texts 10 pt und 20 PT ist, werden die Schriftgrößen nach einem *wParam* -Aufrufsatz auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="16675-148">So, if some of the text is 10pt and some 20pt, after a call with *wParam* set to 1, the font sizes become 11pt and 22pt, respectively.</span></span>

<span data-ttu-id="16675-149">Weitere Beispiele sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="16675-149">Additional examples are shown in the following table.</span></span>



| <span data-ttu-id="16675-150">Ursprünglicher Schrift Grad</span><span class="sxs-lookup"><span data-stu-id="16675-150">Original font size</span></span> | <span data-ttu-id="16675-151">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16675-151">*wParam*</span></span> | <span data-ttu-id="16675-152">Resultierende Schriftgröße</span><span class="sxs-lookup"><span data-stu-id="16675-152">Resulting font size</span></span> |
|--------------------|----------|---------------------|
| <span data-ttu-id="16675-153">7</span><span class="sxs-lookup"><span data-stu-id="16675-153">7</span></span>                  | <span data-ttu-id="16675-154">1</span><span class="sxs-lookup"><span data-stu-id="16675-154">1</span></span>        | <span data-ttu-id="16675-155">8</span><span class="sxs-lookup"><span data-stu-id="16675-155">8</span></span>                   |
| <span data-ttu-id="16675-156">7</span><span class="sxs-lookup"><span data-stu-id="16675-156">7</span></span>                  | <span data-ttu-id="16675-157">3</span><span class="sxs-lookup"><span data-stu-id="16675-157">3</span></span>        | <span data-ttu-id="16675-158">10</span><span class="sxs-lookup"><span data-stu-id="16675-158">10</span></span>                  |
| <span data-ttu-id="16675-159">10</span><span class="sxs-lookup"><span data-stu-id="16675-159">10</span></span>                 | <span data-ttu-id="16675-160">3</span><span class="sxs-lookup"><span data-stu-id="16675-160">3</span></span>        | <span data-ttu-id="16675-161">14</span><span class="sxs-lookup"><span data-stu-id="16675-161">14</span></span>                  |
| <span data-ttu-id="16675-162">14</span><span class="sxs-lookup"><span data-stu-id="16675-162">14</span></span>                 | <span data-ttu-id="16675-163">-3</span><span class="sxs-lookup"><span data-stu-id="16675-163">-3</span></span>       | <span data-ttu-id="16675-164">10</span><span class="sxs-lookup"><span data-stu-id="16675-164">10</span></span>                  |
| <span data-ttu-id="16675-165">28</span><span class="sxs-lookup"><span data-stu-id="16675-165">28</span></span>                 | <span data-ttu-id="16675-166">1</span><span class="sxs-lookup"><span data-stu-id="16675-166">1</span></span>        | <span data-ttu-id="16675-167">36</span><span class="sxs-lookup"><span data-stu-id="16675-167">36</span></span>                  |
| <span data-ttu-id="16675-168">28</span><span class="sxs-lookup"><span data-stu-id="16675-168">28</span></span>                 | <span data-ttu-id="16675-169">3</span><span class="sxs-lookup"><span data-stu-id="16675-169">3</span></span>        | <span data-ttu-id="16675-170">36</span><span class="sxs-lookup"><span data-stu-id="16675-170">36</span></span>                  |
| <span data-ttu-id="16675-171">80</span><span class="sxs-lookup"><span data-stu-id="16675-171">80</span></span>                 | <span data-ttu-id="16675-172">1</span><span class="sxs-lookup"><span data-stu-id="16675-172">1</span></span>        | <span data-ttu-id="16675-173">90</span><span class="sxs-lookup"><span data-stu-id="16675-173">90</span></span>                  |
| <span data-ttu-id="16675-174">80</span><span class="sxs-lookup"><span data-stu-id="16675-174">80</span></span>                 | <span data-ttu-id="16675-175">-1</span><span class="sxs-lookup"><span data-stu-id="16675-175">-1</span></span>       | <span data-ttu-id="16675-176">72</span><span class="sxs-lookup"><span data-stu-id="16675-176">72</span></span>                  |



 

## <a name="requirements"></a><span data-ttu-id="16675-177">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16675-177">Requirements</span></span>



| <span data-ttu-id="16675-178">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16675-178">Requirement</span></span> | <span data-ttu-id="16675-179">Wert</span><span class="sxs-lookup"><span data-stu-id="16675-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="16675-180">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16675-180">Minimum supported client</span></span><br/> | <span data-ttu-id="16675-181">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16675-181">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="16675-182">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16675-182">Minimum supported server</span></span><br/> | <span data-ttu-id="16675-183">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16675-183">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="16675-184">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="16675-184">Redistributable</span></span><br/>          | <span data-ttu-id="16675-185">Rich Edit 3,0</span><span class="sxs-lookup"><span data-stu-id="16675-185">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="16675-186">Header</span><span class="sxs-lookup"><span data-stu-id="16675-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="16675-187"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="16675-187"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16675-188">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16675-188">See also</span></span>

<dl> <dt>

<span data-ttu-id="16675-189">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="16675-189">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="16675-190">**EM \_ getcharformat**</span><span class="sxs-lookup"><span data-stu-id="16675-190">**EM\_GETCHARFORMAT**</span></span>](em-getcharformat.md)
</dt> <dt>

[<span data-ttu-id="16675-191">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="16675-191">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

<span data-ttu-id="16675-192">**Licher**</span><span class="sxs-lookup"><span data-stu-id="16675-192">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="16675-193">Informationen zu Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="16675-193">About Rich Edit Controls</span></span>](about-rich-edit-controls.md)
</dt> </dl>

 

 





