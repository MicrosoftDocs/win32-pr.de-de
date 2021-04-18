---
description: ICE34 überprüft, ob jedes Optionsfeld für jedes RadioButton Group-Steuerelement über eine Eigenschaft in der Eigenschafts Spalte der RadioButton-Tabelle verfügt, die die Optionsfeld Gruppe angibt.
ms.assetid: 23a88a5a-89e9-47bc-9c0a-6101ce03123c
title: ICE34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7723cb530397eae66374b0f218db9ad8505195a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358567"
---
# <a name="ice34"></a><span data-ttu-id="0d296-103">ICE34</span><span class="sxs-lookup"><span data-stu-id="0d296-103">ICE34</span></span>

<span data-ttu-id="0d296-104">ICE34 überprüft, ob jedes Optionsfeld für jedes RadioButton [Group-Steuer](radiobuttongroup-control.md) Element über eine Eigenschaft in der Eigenschafts Spalte der Radio [Button-Tabelle](radiobutton-table.md) verfügt, die die Optionsfeld Gruppe angibt.</span><span class="sxs-lookup"><span data-stu-id="0d296-104">ICE34 validates that each radio button on every [RadioButtonGroup Control](radiobuttongroup-control.md) has a property in the Property column of the [RadioButton table](radiobutton-table.md) that specifies its radio button group.</span></span> <span data-ttu-id="0d296-105">ICE34 überprüft, ob diese Eigenschaft vorhanden und auf einen Standardwert in der [Eigenschaften Tabelle](property-table.md) festgelegt ist, der einem der Optionsfeld Werte der Gruppe in der Spalte Wert der Tabelle RadioButton entspricht.</span><span class="sxs-lookup"><span data-stu-id="0d296-105">ICE34 validates that this property exists and is set to a default value in the [Property table](property-table.md) which is equal to one of the group's radio button values in the Value column of the RadioButton table.</span></span>

<span data-ttu-id="0d296-106">Eine Optionsfeld Gruppe muss über einen Standardwert verfügen, damit Benutzer mithilfe der Tab-Taste eine Auswahl treffen können.</span><span class="sxs-lookup"><span data-stu-id="0d296-106">A radio button group must have a default for users to be able to select a choice using the TAB key.</span></span> <span data-ttu-id="0d296-107">Dies ist für die richtige Benutzer Barrierefreiheit erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0d296-107">This is required for proper user accessibility.</span></span>

<span data-ttu-id="0d296-108">ICE34 meldet fehlende Tabellen.</span><span class="sxs-lookup"><span data-stu-id="0d296-108">ICE34 reports missing tables.</span></span>

## <a name="result"></a><span data-ttu-id="0d296-109">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="0d296-109">Result</span></span>

<span data-ttu-id="0d296-110">ICE34 senden Sie eine Fehlermeldung, wenn ein Optionsfeld vorhanden ist, das eine ungültige Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="0d296-110">ICE34 post an error message if there is a radio button that specifies an invalid property.</span></span>

## <a name="example"></a><span data-ttu-id="0d296-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0d296-111">Example</span></span>

<span data-ttu-id="0d296-112">ICE34 meldet die folgenden Fehler für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="0d296-112">ICE34 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="0d296-113">ICE34-Fehler</span><span class="sxs-lookup"><span data-stu-id="0d296-113">ICE34 error</span></span>                                                                                                                                                                | <span data-ttu-id="0d296-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0d296-114">Description</span></span>                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d296-115">Das Steuerelement dialoga. Control2 muss über eine-Eigenschaft verfügen, da es vom Typ RadioButtonGroup ist.</span><span class="sxs-lookup"><span data-stu-id="0d296-115">Control DialogA.Control2 must have a property because it is of type RadioButtonGroup.</span></span>                                                                                      | <span data-ttu-id="0d296-116">Es gibt ein [RadioButton Group-Steuer](radiobuttongroup-control.md)Element, ohne dass das [indirekte Steuerungs](indirect-control-attribute.md) Bit in der Spalte Attribute der [Steuerelement Tabelle](control-table.md)festgelegt ist, die in der Spalte Eigenschaft nicht über eine Eigenschaft verfügt.</span><span class="sxs-lookup"><span data-stu-id="0d296-116">There is a [RadioButtonGroup control](radiobuttongroup-control.md), without the [Indirect control](indirect-control-attribute.md) bit set in the Attributes column of the [Control table](control-table.md), that does not have a property listed in the Property column.</span></span> |
| <span data-ttu-id="0d296-117">Möglicherweise ist kein gültiger Standardwert für die RadioButtonGroup mithilfe der Property3-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0d296-117">Maybe is not a valid default value for the RadioButtonGroup using property Property3.</span></span> <span data-ttu-id="0d296-118">Der Wert muss als Option in der Tabelle RadioButton Group aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0d296-118">The value must be listed as an option in the RadioButtonGroup table.</span></span>                 | <span data-ttu-id="0d296-119">Es gibt einen Standardwert für eine Eigenschaft, die in der Spalte Wert der [Eigenschaften Tabelle](property-table.md) angegeben ist, die nicht einer der Werte für die Optionsfeld Gruppe ist, die in der Spalte Wert der [RadioButton-Tabelle](radiobutton-table.md)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0d296-119">There is a default value for a property specified in the Value column of the [Property table](property-table.md) that is not one of the values for the radio button group specified in the Value column of the [RadioButton table](radiobutton-table.md).</span></span>                  |
| <span data-ttu-id="0d296-120">Property propertyb muss definiert werden, da es sich um eine indirekte Eigenschaft eines RadioButton Group-Steuer Elements dialoga. Control4</span><span class="sxs-lookup"><span data-stu-id="0d296-120">Property PropertyB must be defined because it is an indirect property of a RadioButtonGroup control DialogA.Control4</span></span>                                                       | <span data-ttu-id="0d296-121">Die Eigenschaft, auf die diese RadioButton-Gruppe verweist, ist eine indirekte Eigenschaft, und der Wert der indirekten Eigenschaft ist nicht eine der Optionen für die RadioButton-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="0d296-121">The property referenced by this RadioButton group is an indirect property, and the value of the indirect property is not one of the choices for the RadioButton group.</span></span>                                                                                                       |
| <span data-ttu-id="0d296-122">Möglicherweise ist kein gültiger Standardwert für die PropertyA-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0d296-122">Maybe is not a valid default value for the property PropertyA.</span></span> <span data-ttu-id="0d296-123">Die-Eigenschaft ist eine indirekte RadioButtonGroup-Eigenschaft des Steuer Elements dialoga. Control5 (über die Property5-Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="0d296-123">The property is an indirect RadioButtonGroup property of control DialogA.Control5 (via property Property5).</span></span> | <span data-ttu-id="0d296-124">Der Wert der indirekten Eigenschaft, auf die über das-Steuerelement verwiesen wird, ist keiner der Standardwerte für diese RadioButtonGroup.</span><span class="sxs-lookup"><span data-stu-id="0d296-124">The value of the indirect property referenced via the control is not one of the default values for that RadioButtonGroup.</span></span>                                                                                                                                                    |



 

<span data-ttu-id="0d296-125">[Control-Tabelle](control-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="0d296-125">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="0d296-126">Dialog</span><span class="sxs-lookup"><span data-stu-id="0d296-126">Dialog</span></span>  | <span data-ttu-id="0d296-127">Control</span><span class="sxs-lookup"><span data-stu-id="0d296-127">Control</span></span>  | <span data-ttu-id="0d296-128">type</span><span class="sxs-lookup"><span data-stu-id="0d296-128">Type</span></span>             | <span data-ttu-id="0d296-129">Attribute</span><span class="sxs-lookup"><span data-stu-id="0d296-129">Attributes</span></span> | <span data-ttu-id="0d296-130">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0d296-130">Property</span></span>  |
|---------|----------|------------------|------------|-----------|
| <span data-ttu-id="0d296-131">Dialoga</span><span class="sxs-lookup"><span data-stu-id="0d296-131">DialogA</span></span> | <span data-ttu-id="0d296-132">Control1</span><span class="sxs-lookup"><span data-stu-id="0d296-132">Control1</span></span> | <span data-ttu-id="0d296-133">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="0d296-133">RadioButtonGroup</span></span> | <span data-ttu-id="0d296-134">0</span><span class="sxs-lookup"><span data-stu-id="0d296-134">0</span></span>          | <span data-ttu-id="0d296-135">Property1</span><span class="sxs-lookup"><span data-stu-id="0d296-135">Property1</span></span> |
| <span data-ttu-id="0d296-136">Dialoga</span><span class="sxs-lookup"><span data-stu-id="0d296-136">DialogA</span></span> | <span data-ttu-id="0d296-137">Control2</span><span class="sxs-lookup"><span data-stu-id="0d296-137">Control2</span></span> | <span data-ttu-id="0d296-138">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="0d296-138">RadioButtonGroup</span></span> | <span data-ttu-id="0d296-139">0</span><span class="sxs-lookup"><span data-stu-id="0d296-139">0</span></span>          |           |
| <span data-ttu-id="0d296-140">Dialoga</span><span class="sxs-lookup"><span data-stu-id="0d296-140">DialogA</span></span> | <span data-ttu-id="0d296-141">Control3</span><span class="sxs-lookup"><span data-stu-id="0d296-141">Control3</span></span> | <span data-ttu-id="0d296-142">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="0d296-142">RadioButtonGroup</span></span> | <span data-ttu-id="0d296-143">0</span><span class="sxs-lookup"><span data-stu-id="0d296-143">0</span></span>          | <span data-ttu-id="0d296-144">Property3</span><span class="sxs-lookup"><span data-stu-id="0d296-144">Property3</span></span> |
| <span data-ttu-id="0d296-145">Dialoga</span><span class="sxs-lookup"><span data-stu-id="0d296-145">DialogA</span></span> | <span data-ttu-id="0d296-146">Control4</span><span class="sxs-lookup"><span data-stu-id="0d296-146">Control4</span></span> | <span data-ttu-id="0d296-147">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="0d296-147">RadioButtonGroup</span></span> | <span data-ttu-id="0d296-148">8</span><span class="sxs-lookup"><span data-stu-id="0d296-148">8</span></span>          | <span data-ttu-id="0d296-149">Property4</span><span class="sxs-lookup"><span data-stu-id="0d296-149">Property4</span></span> |
| <span data-ttu-id="0d296-150">Dialoga</span><span class="sxs-lookup"><span data-stu-id="0d296-150">DialogA</span></span> | <span data-ttu-id="0d296-151">Control5</span><span class="sxs-lookup"><span data-stu-id="0d296-151">Control5</span></span> | <span data-ttu-id="0d296-152">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="0d296-152">RadioButtonGroup</span></span> | <span data-ttu-id="0d296-153">8</span><span class="sxs-lookup"><span data-stu-id="0d296-153">8</span></span>          | <span data-ttu-id="0d296-154">Property5</span><span class="sxs-lookup"><span data-stu-id="0d296-154">Property5</span></span> |



 

<span data-ttu-id="0d296-155">[Eigenschaften Tabelle](property-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="0d296-155">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="0d296-156">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0d296-156">Property</span></span>  | <span data-ttu-id="0d296-157">Wert</span><span class="sxs-lookup"><span data-stu-id="0d296-157">Value</span></span>     |
|-----------|-----------|
| <span data-ttu-id="0d296-158">Property1</span><span class="sxs-lookup"><span data-stu-id="0d296-158">Property1</span></span> | <span data-ttu-id="0d296-159">Ja</span><span class="sxs-lookup"><span data-stu-id="0d296-159">Yes</span></span>       |
| <span data-ttu-id="0d296-160">Property3</span><span class="sxs-lookup"><span data-stu-id="0d296-160">Property3</span></span> | <span data-ttu-id="0d296-161">Vielleicht</span><span class="sxs-lookup"><span data-stu-id="0d296-161">Maybe</span></span>     |
| <span data-ttu-id="0d296-162">Property4</span><span class="sxs-lookup"><span data-stu-id="0d296-162">Property4</span></span> | <span data-ttu-id="0d296-163">Propertyb</span><span class="sxs-lookup"><span data-stu-id="0d296-163">PropertyB</span></span> |
| <span data-ttu-id="0d296-164">Property5</span><span class="sxs-lookup"><span data-stu-id="0d296-164">Property5</span></span> | <span data-ttu-id="0d296-165">PropertyA</span><span class="sxs-lookup"><span data-stu-id="0d296-165">PropertyA</span></span> |
| <span data-ttu-id="0d296-166">PropertyA</span><span class="sxs-lookup"><span data-stu-id="0d296-166">PropertyA</span></span> | <span data-ttu-id="0d296-167">Vielleicht</span><span class="sxs-lookup"><span data-stu-id="0d296-167">Maybe</span></span>     |



 

<span data-ttu-id="0d296-168">[RadioButton-Tabelle](radiobutton-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="0d296-168">[RadioButton Table](radiobutton-table.md) (partial)</span></span>



| <span data-ttu-id="0d296-169">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0d296-169">Property</span></span>  | <span data-ttu-id="0d296-170">Auftrag</span><span class="sxs-lookup"><span data-stu-id="0d296-170">Order</span></span> | <span data-ttu-id="0d296-171">Wert</span><span class="sxs-lookup"><span data-stu-id="0d296-171">Value</span></span> |
|-----------|-------|-------|
| <span data-ttu-id="0d296-172">Property1</span><span class="sxs-lookup"><span data-stu-id="0d296-172">Property1</span></span> | <span data-ttu-id="0d296-173">1</span><span class="sxs-lookup"><span data-stu-id="0d296-173">1</span></span>     | <span data-ttu-id="0d296-174">Ja</span><span class="sxs-lookup"><span data-stu-id="0d296-174">Yes</span></span>   |
| <span data-ttu-id="0d296-175">Property1</span><span class="sxs-lookup"><span data-stu-id="0d296-175">Property1</span></span> | <span data-ttu-id="0d296-176">2</span><span class="sxs-lookup"><span data-stu-id="0d296-176">2</span></span>     | <span data-ttu-id="0d296-177">jetzt</span><span class="sxs-lookup"><span data-stu-id="0d296-177">Now</span></span>   |
| <span data-ttu-id="0d296-178">Eigenschaft2</span><span class="sxs-lookup"><span data-stu-id="0d296-178">Property2</span></span> | <span data-ttu-id="0d296-179">1</span><span class="sxs-lookup"><span data-stu-id="0d296-179">1</span></span>     | <span data-ttu-id="0d296-180">Ja</span><span class="sxs-lookup"><span data-stu-id="0d296-180">Yes</span></span>   |
| <span data-ttu-id="0d296-181">Eigenschaft2</span><span class="sxs-lookup"><span data-stu-id="0d296-181">Property2</span></span> | <span data-ttu-id="0d296-182">2</span><span class="sxs-lookup"><span data-stu-id="0d296-182">2</span></span>     | <span data-ttu-id="0d296-183">Nein</span><span class="sxs-lookup"><span data-stu-id="0d296-183">No</span></span>    |
| <span data-ttu-id="0d296-184">Property3</span><span class="sxs-lookup"><span data-stu-id="0d296-184">Property3</span></span> | <span data-ttu-id="0d296-185">1</span><span class="sxs-lookup"><span data-stu-id="0d296-185">1</span></span>     | <span data-ttu-id="0d296-186">Ja</span><span class="sxs-lookup"><span data-stu-id="0d296-186">Yes</span></span>   |
| <span data-ttu-id="0d296-187">Property3</span><span class="sxs-lookup"><span data-stu-id="0d296-187">Property3</span></span> | <span data-ttu-id="0d296-188">2</span><span class="sxs-lookup"><span data-stu-id="0d296-188">2</span></span>     | <span data-ttu-id="0d296-189">Nein</span><span class="sxs-lookup"><span data-stu-id="0d296-189">No</span></span>    |
| <span data-ttu-id="0d296-190">Property4</span><span class="sxs-lookup"><span data-stu-id="0d296-190">Property4</span></span> | <span data-ttu-id="0d296-191">1</span><span class="sxs-lookup"><span data-stu-id="0d296-191">1</span></span>     | <span data-ttu-id="0d296-192">Ja</span><span class="sxs-lookup"><span data-stu-id="0d296-192">Yes</span></span>   |
| <span data-ttu-id="0d296-193">Property4</span><span class="sxs-lookup"><span data-stu-id="0d296-193">Property4</span></span> | <span data-ttu-id="0d296-194">2</span><span class="sxs-lookup"><span data-stu-id="0d296-194">2</span></span>     | <span data-ttu-id="0d296-195">Nein</span><span class="sxs-lookup"><span data-stu-id="0d296-195">No</span></span>    |
| <span data-ttu-id="0d296-196">PropertyA</span><span class="sxs-lookup"><span data-stu-id="0d296-196">PropertyA</span></span> | <span data-ttu-id="0d296-197">1</span><span class="sxs-lookup"><span data-stu-id="0d296-197">1</span></span>     | <span data-ttu-id="0d296-198">Ja</span><span class="sxs-lookup"><span data-stu-id="0d296-198">Yes</span></span>   |
| <span data-ttu-id="0d296-199">PropertyA</span><span class="sxs-lookup"><span data-stu-id="0d296-199">PropertyA</span></span> | <span data-ttu-id="0d296-200">2</span><span class="sxs-lookup"><span data-stu-id="0d296-200">2</span></span>     | <span data-ttu-id="0d296-201">Nein</span><span class="sxs-lookup"><span data-stu-id="0d296-201">No</span></span>    |
| <span data-ttu-id="0d296-202">Propertyb</span><span class="sxs-lookup"><span data-stu-id="0d296-202">PropertyB</span></span> | <span data-ttu-id="0d296-203">1</span><span class="sxs-lookup"><span data-stu-id="0d296-203">1</span></span>     | <span data-ttu-id="0d296-204">Ja</span><span class="sxs-lookup"><span data-stu-id="0d296-204">Yes</span></span>   |
| <span data-ttu-id="0d296-205">Propertyb</span><span class="sxs-lookup"><span data-stu-id="0d296-205">PropertyB</span></span> | <span data-ttu-id="0d296-206">2</span><span class="sxs-lookup"><span data-stu-id="0d296-206">2</span></span>     | <span data-ttu-id="0d296-207">Nein</span><span class="sxs-lookup"><span data-stu-id="0d296-207">No</span></span>    |



 

<span data-ttu-id="0d296-208">Um die von diesem Ice gemeldeten Fehler zu beheben, überprüfen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0d296-208">To fix the errors reported by this ICE, check the following:</span></span>

-   <span data-ttu-id="0d296-209">Jeder RadioButton-Steuerelement Eintrag ohne den indirekten Attribut Satz verfügt über eine Eigenschaft, die in der Eigenschafts Spalte aufgeführt ist:</span><span class="sxs-lookup"><span data-stu-id="0d296-209">That every RadioButton control entry without the indirect attribute set has a property listed in the Property column:</span></span>
-   <span data-ttu-id="0d296-210">Jede dieser Eigenschaften hat mindestens einen entsprechenden Eintrag in der RadioButton-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0d296-210">That every such property has at least one corresponding entry in the RadioButton table.</span></span>
-   <span data-ttu-id="0d296-211">Jede dieser Eigenschaften wird in der Eigenschaften Tabelle mit einem Wert definiert, der eine der Optionen aus der RadioButton-Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="0d296-211">That every such property is defined in the Property table, with a value that is one of the choices from the RadioButton table.</span></span>
-   <span data-ttu-id="0d296-212">Jede Eigenschaft, auf die in der Eigenschafts Spalte eines RadioButton-Steuer Elements mit dem indirekten Attribut Satz verwiesen wird, wird in der Eigenschaften Tabelle definiert.</span><span class="sxs-lookup"><span data-stu-id="0d296-212">That every property referenced in the Property column of a RadioButton control with the indirect attribute set is defined in the Property table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d296-213">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d296-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d296-214">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="0d296-214">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



