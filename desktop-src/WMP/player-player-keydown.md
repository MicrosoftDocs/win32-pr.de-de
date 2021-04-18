---
title: Player. KeyDown-Ereignis
description: Das KeyDown-Ereignis tritt auf, wenn eine Taste gedrückt wird. | Player. KeyDown-Ereignis
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- KeyDown-Ereignisfenster Media Player
- KeyDown-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, KeyDown-Ereignis
topic_type:
- apiref
api_name:
- Player.KeyDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226430421977a58eca02b7a42cf0349f2a5ff520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372691"
---
# <a name="playerkeydown-event"></a><span data-ttu-id="5e35f-107">Player. KeyDown-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5e35f-107">Player.KeyDown event</span></span>

<span data-ttu-id="5e35f-108">Das **KeyDown** -Ereignis tritt auf, wenn eine Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="5e35f-108">The **KeyDown** event occurs when a key is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e35f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e35f-109">Syntax</span></span>


```JScript
Player.KeyDown(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a><span data-ttu-id="5e35f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e35f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e35f-111">*nKeyCode*</span><span class="sxs-lookup"><span data-stu-id="5e35f-111">*nKeyCode*</span></span> 
</dt> <dd>

<span data-ttu-id="5e35f-112">**Number** (**int**), der angibt, welcher physische Schlüssel gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="5e35f-112">**Number** (**int**) specifying which physical key is pressed.</span></span> <span data-ttu-id="5e35f-113">Mögliche Werte finden Sie im Abschnitt „Hinweise“.</span><span class="sxs-lookup"><span data-stu-id="5e35f-113">For possible values, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="5e35f-114">*nshiftstate*</span><span class="sxs-lookup"><span data-stu-id="5e35f-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="5e35f-115">**Number** (**int**): gibt ein Bitfeld mit den geringsten signifikanten Bits an, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5e35f-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="5e35f-116">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="5e35f-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="5e35f-117">Das Shift-Argument gibt den Zustand dieser Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="5e35f-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="5e35f-118">Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="5e35f-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e35f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e35f-119">Return value</span></span>

<span data-ttu-id="5e35f-120">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5e35f-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e35f-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e35f-121">Remarks</span></span>

<span data-ttu-id="5e35f-122">Das *nKeyCode* -Argument gibt einen physischen Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="5e35f-122">The *nKeyCode* argument specifies a physical key.</span></span> <span data-ttu-id="5e35f-123">In den folgenden Tabellen sind die möglichen Werte für die Hauptschlüssel auf einer Standardtastatur aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e35f-123">The following tables show the possible values for the major keys on a standard keyboard.</span></span>

<span data-ttu-id="5e35f-124">Werte für die Hauptschlüssel.</span><span class="sxs-lookup"><span data-stu-id="5e35f-124">Values for the main keys.</span></span>



| <span data-ttu-id="5e35f-125">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="5e35f-125">Key</span></span>                     | <span data-ttu-id="5e35f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5e35f-126">Value</span></span>   |
|-------------------------|---------|
| <span data-ttu-id="5e35f-127">A-Z</span><span class="sxs-lookup"><span data-stu-id="5e35f-127">A-Z</span></span>                     | <span data-ttu-id="5e35f-128">65-90</span><span class="sxs-lookup"><span data-stu-id="5e35f-128">65-90</span></span>   |
| <span data-ttu-id="5e35f-129">0-9</span><span class="sxs-lookup"><span data-stu-id="5e35f-129">0-9</span></span>                     | <span data-ttu-id="5e35f-130">48-56</span><span class="sxs-lookup"><span data-stu-id="5e35f-130">48-56</span></span>   |
| <span data-ttu-id="5e35f-131">F1-F12</span><span class="sxs-lookup"><span data-stu-id="5e35f-131">F1-F12</span></span>                  | <span data-ttu-id="5e35f-132">112-123</span><span class="sxs-lookup"><span data-stu-id="5e35f-132">112-123</span></span> |
| <span data-ttu-id="5e35f-133">ESC</span><span class="sxs-lookup"><span data-stu-id="5e35f-133">ESC</span></span>                     | <span data-ttu-id="5e35f-134">27</span><span class="sxs-lookup"><span data-stu-id="5e35f-134">27</span></span>      |
| <span data-ttu-id="5e35f-135">TAB</span><span class="sxs-lookup"><span data-stu-id="5e35f-135">TAB</span></span>                     | <span data-ttu-id="5e35f-136">9</span><span class="sxs-lookup"><span data-stu-id="5e35f-136">9</span></span>       |
| <span data-ttu-id="5e35f-137">Feststelltaste</span><span class="sxs-lookup"><span data-stu-id="5e35f-137">CAPS LOCK</span></span>               | <span data-ttu-id="5e35f-138">20</span><span class="sxs-lookup"><span data-stu-id="5e35f-138">20</span></span>      |
| <span data-ttu-id="5e35f-139">Shift (links oder rechts)</span><span class="sxs-lookup"><span data-stu-id="5e35f-139">SHIFT (left or right)</span></span>   | <span data-ttu-id="5e35f-140">16</span><span class="sxs-lookup"><span data-stu-id="5e35f-140">16</span></span>      |
| <span data-ttu-id="5e35f-141">STRG (links oder rechts)</span><span class="sxs-lookup"><span data-stu-id="5e35f-141">CTRL (left or right)</span></span>    | <span data-ttu-id="5e35f-142">17</span><span class="sxs-lookup"><span data-stu-id="5e35f-142">17</span></span>      |
| <span data-ttu-id="5e35f-143">ALT (links oder rechts)</span><span class="sxs-lookup"><span data-stu-id="5e35f-143">ALT (left or right)</span></span>     | <span data-ttu-id="5e35f-144">18</span><span class="sxs-lookup"><span data-stu-id="5e35f-144">18</span></span>      |
| <span data-ttu-id="5e35f-145">SPACE</span><span class="sxs-lookup"><span data-stu-id="5e35f-145">SPACE</span></span>                   | <span data-ttu-id="5e35f-146">32</span><span class="sxs-lookup"><span data-stu-id="5e35f-146">32</span></span>      |
| <span data-ttu-id="5e35f-147">RÜCKTASTE</span><span class="sxs-lookup"><span data-stu-id="5e35f-147">BACKSPACE</span></span>               | <span data-ttu-id="5e35f-148">8</span><span class="sxs-lookup"><span data-stu-id="5e35f-148">8</span></span>       |
| <span data-ttu-id="5e35f-149">EINGABETASTE</span><span class="sxs-lookup"><span data-stu-id="5e35f-149">ENTER</span></span>                   | <span data-ttu-id="5e35f-150">13</span><span class="sxs-lookup"><span data-stu-id="5e35f-150">13</span></span>      |
| <span data-ttu-id="5e35f-151">Windows-Taste, Links</span><span class="sxs-lookup"><span data-stu-id="5e35f-151">Windows logo key, left</span></span>  | <span data-ttu-id="5e35f-152">91</span><span class="sxs-lookup"><span data-stu-id="5e35f-152">91</span></span>      |
| <span data-ttu-id="5e35f-153">Windows-Taste, rechts</span><span class="sxs-lookup"><span data-stu-id="5e35f-153">Windows logo key, right</span></span> | <span data-ttu-id="5e35f-154">92</span><span class="sxs-lookup"><span data-stu-id="5e35f-154">92</span></span>      |
| <span data-ttu-id="5e35f-155">Anwendungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="5e35f-155">Application key</span></span>         | <span data-ttu-id="5e35f-156">93</span><span class="sxs-lookup"><span data-stu-id="5e35f-156">93</span></span>      |



 

<span data-ttu-id="5e35f-157">Werte für die Zahlen Füll Tasten.</span><span class="sxs-lookup"><span data-stu-id="5e35f-157">Values for the number pad keys.</span></span>



| <span data-ttu-id="5e35f-158">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="5e35f-158">Key</span></span>               | <span data-ttu-id="5e35f-159">Wert</span><span class="sxs-lookup"><span data-stu-id="5e35f-159">Value</span></span>  |
|-------------------|--------|
| <span data-ttu-id="5e35f-160">0-9</span><span class="sxs-lookup"><span data-stu-id="5e35f-160">0-9</span></span>               | <span data-ttu-id="5e35f-161">96-105</span><span class="sxs-lookup"><span data-stu-id="5e35f-161">96-105</span></span> |
| <span data-ttu-id="5e35f-162">NUM-Sperre</span><span class="sxs-lookup"><span data-stu-id="5e35f-162">NUM LOCK</span></span>          | <span data-ttu-id="5e35f-163">144</span><span class="sxs-lookup"><span data-stu-id="5e35f-163">144</span></span>    |
| <span data-ttu-id="5e35f-164">Dividieren (/)</span><span class="sxs-lookup"><span data-stu-id="5e35f-164">DIVIDE (/)</span></span>        | <span data-ttu-id="5e35f-165">111</span><span class="sxs-lookup"><span data-stu-id="5e35f-165">111</span></span>    |
| <span data-ttu-id="5e35f-166">Multiplizieren ( \* )</span><span class="sxs-lookup"><span data-stu-id="5e35f-166">MULTIPLY (\*)</span></span>     | <span data-ttu-id="5e35f-167">106</span><span class="sxs-lookup"><span data-stu-id="5e35f-167">106</span></span>    |
| <span data-ttu-id="5e35f-168">Subtraktion (-)</span><span class="sxs-lookup"><span data-stu-id="5e35f-168">SUBTRACT (-)</span></span>      | <span data-ttu-id="5e35f-169">109</span><span class="sxs-lookup"><span data-stu-id="5e35f-169">109</span></span>    |
| <span data-ttu-id="5e35f-170">Hinzufügen (+)</span><span class="sxs-lookup"><span data-stu-id="5e35f-170">ADD (+)</span></span>           | <span data-ttu-id="5e35f-171">107</span><span class="sxs-lookup"><span data-stu-id="5e35f-171">107</span></span>    |
| <span data-ttu-id="5e35f-172">Trennzeichen (EINGABETASTE)</span><span class="sxs-lookup"><span data-stu-id="5e35f-172">SEPARATOR (Enter)</span></span> | <span data-ttu-id="5e35f-173">108</span><span class="sxs-lookup"><span data-stu-id="5e35f-173">108</span></span>    |
| <span data-ttu-id="5e35f-174">Dezimalzahl (.)</span><span class="sxs-lookup"><span data-stu-id="5e35f-174">DECIMAL (.)</span></span>       | <span data-ttu-id="5e35f-175">110</span><span class="sxs-lookup"><span data-stu-id="5e35f-175">110</span></span>    |



 

<span data-ttu-id="5e35f-176">Werte für die Navigationstasten.</span><span class="sxs-lookup"><span data-stu-id="5e35f-176">Values for the navigation keys.</span></span>



| <span data-ttu-id="5e35f-177">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="5e35f-177">Key</span></span>         | <span data-ttu-id="5e35f-178">Wert</span><span class="sxs-lookup"><span data-stu-id="5e35f-178">Value</span></span> |
|-------------|-------|
| <span data-ttu-id="5e35f-179">INSERT</span><span class="sxs-lookup"><span data-stu-id="5e35f-179">INSERT</span></span>      | <span data-ttu-id="5e35f-180">45</span><span class="sxs-lookup"><span data-stu-id="5e35f-180">45</span></span>    |
| <span data-ttu-id="5e35f-181">Delete</span><span class="sxs-lookup"><span data-stu-id="5e35f-181">DELETE</span></span>      | <span data-ttu-id="5e35f-182">46</span><span class="sxs-lookup"><span data-stu-id="5e35f-182">46</span></span>    |
| <span data-ttu-id="5e35f-183">POS1</span><span class="sxs-lookup"><span data-stu-id="5e35f-183">HOME</span></span>        | <span data-ttu-id="5e35f-184">36</span><span class="sxs-lookup"><span data-stu-id="5e35f-184">36</span></span>    |
| <span data-ttu-id="5e35f-185">ENDE</span><span class="sxs-lookup"><span data-stu-id="5e35f-185">END</span></span>         | <span data-ttu-id="5e35f-186">35</span><span class="sxs-lookup"><span data-stu-id="5e35f-186">35</span></span>    |
| <span data-ttu-id="5e35f-187">BILD-AUF</span><span class="sxs-lookup"><span data-stu-id="5e35f-187">PAGE UP</span></span>     | <span data-ttu-id="5e35f-188">33</span><span class="sxs-lookup"><span data-stu-id="5e35f-188">33</span></span>    |
| <span data-ttu-id="5e35f-189">BILD-AB</span><span class="sxs-lookup"><span data-stu-id="5e35f-189">PAGE DOWN</span></span>   | <span data-ttu-id="5e35f-190">34</span><span class="sxs-lookup"><span data-stu-id="5e35f-190">34</span></span>    |
| <span data-ttu-id="5e35f-191">NACH-OBEN-TASTE</span><span class="sxs-lookup"><span data-stu-id="5e35f-191">UP ARROW</span></span>    | <span data-ttu-id="5e35f-192">38</span><span class="sxs-lookup"><span data-stu-id="5e35f-192">38</span></span>    |
| <span data-ttu-id="5e35f-193">NACH-UNTEN-TASTE</span><span class="sxs-lookup"><span data-stu-id="5e35f-193">DOWN ARROW</span></span>  | <span data-ttu-id="5e35f-194">40</span><span class="sxs-lookup"><span data-stu-id="5e35f-194">40</span></span>    |
| <span data-ttu-id="5e35f-195">NACH-LINKS-TASTE</span><span class="sxs-lookup"><span data-stu-id="5e35f-195">LEFT ARROW</span></span>  | <span data-ttu-id="5e35f-196">37</span><span class="sxs-lookup"><span data-stu-id="5e35f-196">37</span></span>    |
| <span data-ttu-id="5e35f-197">NACH-RECHTS-TASTE</span><span class="sxs-lookup"><span data-stu-id="5e35f-197">RIGHT ARROW</span></span> | <span data-ttu-id="5e35f-198">39</span><span class="sxs-lookup"><span data-stu-id="5e35f-198">39</span></span>    |



 

<span data-ttu-id="5e35f-199">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="5e35f-199">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="5e35f-200">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="5e35f-200">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="5e35f-201">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e35f-201">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e35f-202">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e35f-202">Requirements</span></span>



| <span data-ttu-id="5e35f-203">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e35f-203">Requirement</span></span> | <span data-ttu-id="5e35f-204">Wert</span><span class="sxs-lookup"><span data-stu-id="5e35f-204">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5e35f-205">Version</span><span class="sxs-lookup"><span data-stu-id="5e35f-205">Version</span></span><br/> | <span data-ttu-id="5e35f-206">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="5e35f-206">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="5e35f-207">DLL</span><span class="sxs-lookup"><span data-stu-id="5e35f-207">DLL</span></span><br/>     | <dl> <span data-ttu-id="5e35f-208"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e35f-208"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e35f-209">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e35f-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e35f-210">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="5e35f-210">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





