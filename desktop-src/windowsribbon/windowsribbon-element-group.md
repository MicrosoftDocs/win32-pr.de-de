---
title: Group-Element
description: Stellt ein Gruppen Steuerelement dar, das als Container für eine Gruppe von Elementen fungiert.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Windows-Menüband für Gruppenelement
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a42e9efb30397862037426041420d96be8fd387
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390642"
---
# <a name="group-element"></a><span data-ttu-id="e2c03-104">Group-Element</span><span class="sxs-lookup"><span data-stu-id="e2c03-104">Group element</span></span>

<span data-ttu-id="e2c03-105">Stellt ein [Gruppen](windowsribbon-controls-group.md) Steuerelement dar, das als Container für eine Gruppe von Elementen fungiert.</span><span class="sxs-lookup"><span data-stu-id="e2c03-105">Represents a [Group](windowsribbon-controls-group.md) control that functions as a container for a group of elements.</span></span>

## <a name="usage"></a><span data-ttu-id="e2c03-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="e2c03-106">Usage</span></span>

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
```

## <a name="attributes"></a><span data-ttu-id="e2c03-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="e2c03-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e2c03-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="e2c03-108">Attribute</span></span></th>
<th><span data-ttu-id="e2c03-109">type</span><span class="sxs-lookup"><span data-stu-id="e2c03-109">Type</span></span></th>
<th><span data-ttu-id="e2c03-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e2c03-110">Required</span></span></th>
<th><span data-ttu-id="e2c03-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2c03-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e2c03-112"><strong>Applicationmodes</strong></span><span class="sxs-lookup"><span data-stu-id="e2c03-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="e2c03-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="e2c03-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="e2c03-114">Nein</span><span class="sxs-lookup"><span data-stu-id="e2c03-114">No</span></span><br/></td>
<td><span data-ttu-id="e2c03-115"><dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="e2c03-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e2c03-116">Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste mit ganzen Zahlen zwischen 0 und 31 enthält.</span><span class="sxs-lookup"><span data-stu-id="e2c03-116">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="e2c03-117">Leerraum ist gültig und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e2c03-117">White space is valid and ignored.</span></span><br/> <span data-ttu-id="e2c03-118">Maximale Länge: 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e2c03-118">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2c03-119"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="e2c03-119"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="e2c03-120">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="e2c03-120">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="e2c03-121">Nein</span><span class="sxs-lookup"><span data-stu-id="e2c03-121">No</span></span><br/></td>
<td><span data-ttu-id="e2c03-122">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="e2c03-122">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="e2c03-123">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="e2c03-123">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e2c03-124">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="e2c03-124">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="e2c03-125">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="e2c03-125">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="e2c03-126">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e2c03-126">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e2c03-127"><strong>Sizedefinition</strong></span><span class="sxs-lookup"><span data-stu-id="e2c03-127"><strong>SizeDefinition</strong></span></span><br/></td>
<td><span data-ttu-id="e2c03-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="e2c03-128">xs:string</span></span><br/></td>
<td><span data-ttu-id="e2c03-129">Nein</span><span class="sxs-lookup"><span data-stu-id="e2c03-129">No</span></span><br/></td>
<td><span data-ttu-id="e2c03-130">Wenn angegeben, wird der Wert von <em>sizedefinition</em> auf eine der <a href="windowsribbon-templates.md">Layoutvorlagen</a> beschränkt, die im Menüband-Framework definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e2c03-130">When specified, the value of <em>SizeDefinition</em> is constrained to one of the <a href="windowsribbon-templates.md">layout templates</a> defined by the Ribbon framework.</span></span> <br/> <br/><span data-ttu-id="e2c03-131">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="e2c03-131">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="e2c03-132">Eine beliebige Sequenz von NULL oder mehr Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e2c03-132">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="e2c03-133">Die maximale Länge ist unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="e2c03-133">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="e2c03-134">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2c03-134">Child elements</span></span>



| <span data-ttu-id="e2c03-135">Element</span><span class="sxs-lookup"><span data-stu-id="e2c03-135">Element</span></span>                                                                             | <span data-ttu-id="e2c03-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2c03-136">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="e2c03-137">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="e2c03-137">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="e2c03-138">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="e2c03-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e2c03-139">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="e2c03-139">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="e2c03-140">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="e2c03-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e2c03-141">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="e2c03-141">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="e2c03-142">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="e2c03-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e2c03-143">**Controlgroup**</span><span class="sxs-lookup"><span data-stu-id="e2c03-143">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               | <span data-ttu-id="e2c03-144">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="e2c03-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e2c03-145">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="e2c03-145">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="e2c03-146">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="e2c03-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e2c03-147">**Dropdowncolorpicker**</span><span class="sxs-lookup"><span data-stu-id="e2c03-147">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="e2c03-148">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="e2c03-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e2c03-149">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="e2c03-149">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="e2c03-150">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="e2c03-150">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e2c03-151">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="e2c03-151">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="e2c03-152">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="e2c03-152">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="e2c03-153">**Inribbongallery**</span><span class="sxs-lookup"><span data-stu-id="e2c03-153">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>         | <span data-ttu-id="e2c03-154">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="e2c03-154">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e2c03-155">**Sizedefinition**</span><span class="sxs-lookup"><span data-stu-id="e2c03-155">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/>           | <span data-ttu-id="e2c03-156">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="e2c03-156">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="e2c03-157">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="e2c03-157">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                         | <span data-ttu-id="e2c03-158">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="e2c03-158">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e2c03-159">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="e2c03-159">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="e2c03-160">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="e2c03-160">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e2c03-161">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="e2c03-161">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="e2c03-162">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="e2c03-162">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="e2c03-163">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="e2c03-163">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="e2c03-164">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="e2c03-164">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="e2c03-165">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2c03-165">Parent elements</span></span>



| <span data-ttu-id="e2c03-166">Element</span><span class="sxs-lookup"><span data-stu-id="e2c03-166">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="e2c03-167">**Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="e2c03-167">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="e2c03-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2c03-168">Remarks</span></span>

<span data-ttu-id="e2c03-169">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e2c03-169">Optional.</span></span>

<span data-ttu-id="e2c03-170">Kann für jedes [**Register**](windowsribbon-element-tab.md) Kartenelement einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="e2c03-170">May occur one or more times for each [**Tab**](windowsribbon-element-tab.md) element.</span></span>

<span data-ttu-id="e2c03-171">[**Registerkarte**](windowsribbon-element-tab.md) unterstützt [Anwendungsmodi](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="e2c03-171">[**Tab**](windowsribbon-element-tab.md) supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="e2c03-172">Das Menü Band Markup ist nur gültig, wenn die untergeordneten Elemente der **Gruppe** der für *sizedefinition* angegebenen Vorlage entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e2c03-172">The Ribbon markup is valid only when the child elements of **Group** correspond to the template specified for *SizeDefinition*.</span></span>

## <a name="examples"></a><span data-ttu-id="e2c03-173">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2c03-173">Examples</span></span>

<span data-ttu-id="e2c03-174">Das folgende Codebeispiel veranschaulicht die Verwendung einer benutzerdefinierten Vorlage in einer **Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="e2c03-174">The following code example illustrates the use of a custom template in a **Group**.</span></span>


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="e2c03-175">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e2c03-175">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="e2c03-176">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="e2c03-176">Minimum supported system</span></span><br/> | <span data-ttu-id="e2c03-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2c03-177">Windows 7</span></span> |
| <span data-ttu-id="e2c03-178">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="e2c03-178">Can be empty</span></span>                        | <span data-ttu-id="e2c03-179">Nein</span><span class="sxs-lookup"><span data-stu-id="e2c03-179">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="e2c03-180">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e2c03-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2c03-181">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="e2c03-181">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="e2c03-182">Gruppen Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e2c03-182">Group control</span></span>](windowsribbon-controls-group.md)
</dt> <dt>

[<span data-ttu-id="e2c03-183">**Setmodes**</span><span class="sxs-lookup"><span data-stu-id="e2c03-183">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

