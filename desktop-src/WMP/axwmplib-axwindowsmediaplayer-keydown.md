---
title: KeyDown-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das KeyDown-Ereignis tritt auf, wenn eine Taste gedrückt wird. | KeyDown-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: e67b9628-6c53-4893-921a-9487ebfc1cd5
keywords:
- Das KeyDown-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- KeyDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc89814063e1a43badd22e658b5f19ece7abb074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359747"
---
# <a name="keydown-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="2f3c6-105">KeyDown-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="2f3c6-105">KeyDown Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="2f3c6-106">Das KeyDown-Ereignis tritt auf, wenn eine Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="2f3c6-106">The KeyDown event occurs when a key is pressed.</span></span>

``` syntax
[C#]
private void player_KeyDownEvent(
  object sender,
  _WMPOCXEvents_KeyDownEvent e
)

[Visual Basic]
Private Sub player_KeyDownEvent(  
  sender As Object, 
  e As _WMPOCXEvents_KeyDownEvent
) Handles player.KeyDownEvent
```

## <a name="event-data"></a><span data-ttu-id="2f3c6-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="2f3c6-107">Event Data</span></span>

<span data-ttu-id="2f3c6-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ keydownetventhandler**.</span><span class="sxs-lookup"><span data-stu-id="2f3c6-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyDownEventHandler**.</span></span> <span data-ttu-id="2f3c6-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ keydownvent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="2f3c6-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyDownEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="2f3c6-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2f3c6-110">Property</span></span>    | <span data-ttu-id="2f3c6-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f3c6-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c6-112">nKeyCode</span><span class="sxs-lookup"><span data-stu-id="2f3c6-112">nKeyCode</span></span>    | <span data-ttu-id="2f3c6-113">System. Int16Specifies der physische Schlüssel, auf den geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="2f3c6-113">System.Int16Specifies which physical key is pressed.</span></span> <span data-ttu-id="2f3c6-114">Mögliche Werte finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="2f3c6-114">For possible values, see Remarks.</span></span><br/>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="2f3c6-115">nshiftstate</span><span class="sxs-lookup"><span data-stu-id="2f3c6-115">nShiftState</span></span> | <span data-ttu-id="2f3c6-116">System. Int16A Bitfeld mit den geringsten signifikanten Bits, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2f3c6-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="2f3c6-117">Diese Bits entsprechen den Werten 1, 2 und 4.</span><span class="sxs-lookup"><span data-stu-id="2f3c6-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="2f3c6-118">Das Shift-Argument gibt den Zustand dieser Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="2f3c6-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="2f3c6-119">Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="2f3c6-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f3c6-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f3c6-120">Remarks</span></span>

<span data-ttu-id="2f3c6-121">Die **nKeyCode** -Eigenschaft gibt einen physischen Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="2f3c6-121">The **nKeyCode** property specifies a physical key.</span></span> <span data-ttu-id="2f3c6-122">In den folgenden Tabellen sind die möglichen Werte für die Hauptschlüssel auf einer Standardtastatur aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f3c6-122">The following tables show the possible values for the major keys on a standard keyboard.</span></span>

<span data-ttu-id="2f3c6-123">Werte für die Hauptschlüssel.</span><span class="sxs-lookup"><span data-stu-id="2f3c6-123">Values for the main keys.</span></span>



| <span data-ttu-id="2f3c6-124">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2f3c6-124">Key</span></span>                     | <span data-ttu-id="2f3c6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2f3c6-125">Value</span></span>   |
|-------------------------|---------|
| <span data-ttu-id="2f3c6-126">A-Z</span><span class="sxs-lookup"><span data-stu-id="2f3c6-126">A-Z</span></span>                     | <span data-ttu-id="2f3c6-127">65-90</span><span class="sxs-lookup"><span data-stu-id="2f3c6-127">65-90</span></span>   |
| <span data-ttu-id="2f3c6-128">0-9</span><span class="sxs-lookup"><span data-stu-id="2f3c6-128">0-9</span></span>                     | <span data-ttu-id="2f3c6-129">48-56</span><span class="sxs-lookup"><span data-stu-id="2f3c6-129">48-56</span></span>   |
| <span data-ttu-id="2f3c6-130">F1-F12</span><span class="sxs-lookup"><span data-stu-id="2f3c6-130">F1-F12</span></span>                  | <span data-ttu-id="2f3c6-131">112-123</span><span class="sxs-lookup"><span data-stu-id="2f3c6-131">112-123</span></span> |
| <span data-ttu-id="2f3c6-132">ESC</span><span class="sxs-lookup"><span data-stu-id="2f3c6-132">ESC</span></span>                     | <span data-ttu-id="2f3c6-133">27</span><span class="sxs-lookup"><span data-stu-id="2f3c6-133">27</span></span>      |
| <span data-ttu-id="2f3c6-134">TAB</span><span class="sxs-lookup"><span data-stu-id="2f3c6-134">TAB</span></span>                     | <span data-ttu-id="2f3c6-135">9</span><span class="sxs-lookup"><span data-stu-id="2f3c6-135">9</span></span>       |
| <span data-ttu-id="2f3c6-136">Feststelltaste</span><span class="sxs-lookup"><span data-stu-id="2f3c6-136">CAPS LOCK</span></span>               | <span data-ttu-id="2f3c6-137">20</span><span class="sxs-lookup"><span data-stu-id="2f3c6-137">20</span></span>      |
| <span data-ttu-id="2f3c6-138">Shift (links oder rechts)</span><span class="sxs-lookup"><span data-stu-id="2f3c6-138">SHIFT (left or right)</span></span>   | <span data-ttu-id="2f3c6-139">16</span><span class="sxs-lookup"><span data-stu-id="2f3c6-139">16</span></span>      |
| <span data-ttu-id="2f3c6-140">STRG (links oder rechts)</span><span class="sxs-lookup"><span data-stu-id="2f3c6-140">CTRL (left or right)</span></span>    | <span data-ttu-id="2f3c6-141">17</span><span class="sxs-lookup"><span data-stu-id="2f3c6-141">17</span></span>      |
| <span data-ttu-id="2f3c6-142">ALT (links oder rechts)</span><span class="sxs-lookup"><span data-stu-id="2f3c6-142">ALT (left or right)</span></span>     | <span data-ttu-id="2f3c6-143">18</span><span class="sxs-lookup"><span data-stu-id="2f3c6-143">18</span></span>      |
| <span data-ttu-id="2f3c6-144">SPACE</span><span class="sxs-lookup"><span data-stu-id="2f3c6-144">SPACE</span></span>                   | <span data-ttu-id="2f3c6-145">32</span><span class="sxs-lookup"><span data-stu-id="2f3c6-145">32</span></span>      |
| <span data-ttu-id="2f3c6-146">RÜCKTASTE</span><span class="sxs-lookup"><span data-stu-id="2f3c6-146">BACKSPACE</span></span>               | <span data-ttu-id="2f3c6-147">8</span><span class="sxs-lookup"><span data-stu-id="2f3c6-147">8</span></span>       |
| <span data-ttu-id="2f3c6-148">EINGABETASTE</span><span class="sxs-lookup"><span data-stu-id="2f3c6-148">ENTER</span></span>                   | <span data-ttu-id="2f3c6-149">13</span><span class="sxs-lookup"><span data-stu-id="2f3c6-149">13</span></span>      |
| <span data-ttu-id="2f3c6-150">Windows-Taste, Links</span><span class="sxs-lookup"><span data-stu-id="2f3c6-150">Windows logo key, left</span></span>  | <span data-ttu-id="2f3c6-151">91</span><span class="sxs-lookup"><span data-stu-id="2f3c6-151">91</span></span>      |
| <span data-ttu-id="2f3c6-152">Windows-Taste, rechts</span><span class="sxs-lookup"><span data-stu-id="2f3c6-152">Windows logo key, right</span></span> | <span data-ttu-id="2f3c6-153">92</span><span class="sxs-lookup"><span data-stu-id="2f3c6-153">92</span></span>      |
| <span data-ttu-id="2f3c6-154">Anwendungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="2f3c6-154">Application key</span></span>         | <span data-ttu-id="2f3c6-155">93</span><span class="sxs-lookup"><span data-stu-id="2f3c6-155">93</span></span>      |



 

<span data-ttu-id="2f3c6-156">Werte für die Zahlen Füll Tasten.</span><span class="sxs-lookup"><span data-stu-id="2f3c6-156">Values for the number pad keys.</span></span>



| <span data-ttu-id="2f3c6-157">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2f3c6-157">Key</span></span>               | <span data-ttu-id="2f3c6-158">Wert</span><span class="sxs-lookup"><span data-stu-id="2f3c6-158">Value</span></span>  |
|-------------------|--------|
| <span data-ttu-id="2f3c6-159">0-9</span><span class="sxs-lookup"><span data-stu-id="2f3c6-159">0-9</span></span>               | <span data-ttu-id="2f3c6-160">96-105</span><span class="sxs-lookup"><span data-stu-id="2f3c6-160">96-105</span></span> |
| <span data-ttu-id="2f3c6-161">NUM-Sperre</span><span class="sxs-lookup"><span data-stu-id="2f3c6-161">NUM LOCK</span></span>          | <span data-ttu-id="2f3c6-162">144</span><span class="sxs-lookup"><span data-stu-id="2f3c6-162">144</span></span>    |
| <span data-ttu-id="2f3c6-163">Dividieren (/)</span><span class="sxs-lookup"><span data-stu-id="2f3c6-163">DIVIDE (/)</span></span>        | <span data-ttu-id="2f3c6-164">111</span><span class="sxs-lookup"><span data-stu-id="2f3c6-164">111</span></span>    |
| <span data-ttu-id="2f3c6-165">Multiplizieren ( \* )</span><span class="sxs-lookup"><span data-stu-id="2f3c6-165">MULTIPLY (\*)</span></span>     | <span data-ttu-id="2f3c6-166">106</span><span class="sxs-lookup"><span data-stu-id="2f3c6-166">106</span></span>    |
| <span data-ttu-id="2f3c6-167">Subtraktion (-)</span><span class="sxs-lookup"><span data-stu-id="2f3c6-167">SUBTRACT (-)</span></span>      | <span data-ttu-id="2f3c6-168">109</span><span class="sxs-lookup"><span data-stu-id="2f3c6-168">109</span></span>    |
| <span data-ttu-id="2f3c6-169">Hinzufügen (+)</span><span class="sxs-lookup"><span data-stu-id="2f3c6-169">ADD (+)</span></span>           | <span data-ttu-id="2f3c6-170">107</span><span class="sxs-lookup"><span data-stu-id="2f3c6-170">107</span></span>    |
| <span data-ttu-id="2f3c6-171">Trennzeichen (EINGABETASTE)</span><span class="sxs-lookup"><span data-stu-id="2f3c6-171">SEPARATOR (Enter)</span></span> | <span data-ttu-id="2f3c6-172">108</span><span class="sxs-lookup"><span data-stu-id="2f3c6-172">108</span></span>    |
| <span data-ttu-id="2f3c6-173">Dezimalzahl (.)</span><span class="sxs-lookup"><span data-stu-id="2f3c6-173">DECIMAL (.)</span></span>       | <span data-ttu-id="2f3c6-174">110</span><span class="sxs-lookup"><span data-stu-id="2f3c6-174">110</span></span>    |



 

<span data-ttu-id="2f3c6-175">Werte für die Navigationstasten.</span><span class="sxs-lookup"><span data-stu-id="2f3c6-175">Values for the navigation keys.</span></span>



| <span data-ttu-id="2f3c6-176">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2f3c6-176">Key</span></span>         | <span data-ttu-id="2f3c6-177">Wert</span><span class="sxs-lookup"><span data-stu-id="2f3c6-177">Value</span></span> |
|-------------|-------|
| <span data-ttu-id="2f3c6-178">INSERT</span><span class="sxs-lookup"><span data-stu-id="2f3c6-178">INSERT</span></span>      | <span data-ttu-id="2f3c6-179">45</span><span class="sxs-lookup"><span data-stu-id="2f3c6-179">45</span></span>    |
| <span data-ttu-id="2f3c6-180">Delete</span><span class="sxs-lookup"><span data-stu-id="2f3c6-180">DELETE</span></span>      | <span data-ttu-id="2f3c6-181">46</span><span class="sxs-lookup"><span data-stu-id="2f3c6-181">46</span></span>    |
| <span data-ttu-id="2f3c6-182">POS1</span><span class="sxs-lookup"><span data-stu-id="2f3c6-182">HOME</span></span>        | <span data-ttu-id="2f3c6-183">36</span><span class="sxs-lookup"><span data-stu-id="2f3c6-183">36</span></span>    |
| <span data-ttu-id="2f3c6-184">ENDE</span><span class="sxs-lookup"><span data-stu-id="2f3c6-184">END</span></span>         | <span data-ttu-id="2f3c6-185">35</span><span class="sxs-lookup"><span data-stu-id="2f3c6-185">35</span></span>    |
| <span data-ttu-id="2f3c6-186">BILD-AUF</span><span class="sxs-lookup"><span data-stu-id="2f3c6-186">PAGE UP</span></span>     | <span data-ttu-id="2f3c6-187">33</span><span class="sxs-lookup"><span data-stu-id="2f3c6-187">33</span></span>    |
| <span data-ttu-id="2f3c6-188">BILD-AB</span><span class="sxs-lookup"><span data-stu-id="2f3c6-188">PAGE DOWN</span></span>   | <span data-ttu-id="2f3c6-189">34</span><span class="sxs-lookup"><span data-stu-id="2f3c6-189">34</span></span>    |
| <span data-ttu-id="2f3c6-190">NACH-OBEN-TASTE</span><span class="sxs-lookup"><span data-stu-id="2f3c6-190">UP ARROW</span></span>    | <span data-ttu-id="2f3c6-191">38</span><span class="sxs-lookup"><span data-stu-id="2f3c6-191">38</span></span>    |
| <span data-ttu-id="2f3c6-192">NACH-UNTEN-TASTE</span><span class="sxs-lookup"><span data-stu-id="2f3c6-192">DOWN ARROW</span></span>  | <span data-ttu-id="2f3c6-193">40</span><span class="sxs-lookup"><span data-stu-id="2f3c6-193">40</span></span>    |
| <span data-ttu-id="2f3c6-194">NACH-LINKS-TASTE</span><span class="sxs-lookup"><span data-stu-id="2f3c6-194">LEFT ARROW</span></span>  | <span data-ttu-id="2f3c6-195">37</span><span class="sxs-lookup"><span data-stu-id="2f3c6-195">37</span></span>    |
| <span data-ttu-id="2f3c6-196">NACH-RECHTS-TASTE</span><span class="sxs-lookup"><span data-stu-id="2f3c6-196">RIGHT ARROW</span></span> | <span data-ttu-id="2f3c6-197">39</span><span class="sxs-lookup"><span data-stu-id="2f3c6-197">39</span></span>    |



 

## <a name="requirements"></a><span data-ttu-id="2f3c6-198">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f3c6-198">Requirements</span></span>



| <span data-ttu-id="2f3c6-199">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f3c6-199">Requirement</span></span> | <span data-ttu-id="2f3c6-200">Wert</span><span class="sxs-lookup"><span data-stu-id="2f3c6-200">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c6-201">Version</span><span class="sxs-lookup"><span data-stu-id="2f3c6-201">Version</span></span><br/>   | <span data-ttu-id="2f3c6-202">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="2f3c6-202">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="2f3c6-203">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f3c6-203">Namespace</span></span><br/> | <span data-ttu-id="2f3c6-204">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="2f3c6-204">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="2f3c6-205">Assembly</span><span class="sxs-lookup"><span data-stu-id="2f3c6-205">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2f3c6-206"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2f3c6-206"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f3c6-207">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f3c6-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f3c6-208">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2f3c6-208">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





