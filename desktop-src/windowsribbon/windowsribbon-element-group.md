---
title: Group-Element
description: Stellt ein Group-Steuerelement dar, das als Container für eine Gruppe von Elementen fungiert.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Gruppenelement Windows-Menüband
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1162055491f61ae6feffa385bbc5015e4f1b66f0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442871"
---
# <a name="group-element"></a><span data-ttu-id="71ca9-104">Group-Element</span><span class="sxs-lookup"><span data-stu-id="71ca9-104">Group element</span></span>

<span data-ttu-id="71ca9-105">Stellt ein [Group-Steuerelement](windowsribbon-controls-group.md) dar, das als Container für eine Gruppe von Elementen fungiert.</span><span class="sxs-lookup"><span data-stu-id="71ca9-105">Represents a [Group](windowsribbon-controls-group.md) control that functions as a container for a group of elements.</span></span>

## <a name="usage"></a><span data-ttu-id="71ca9-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="71ca9-106">Usage</span></span>

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
```

## <a name="attributes"></a><span data-ttu-id="71ca9-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="71ca9-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71ca9-108">attribute</span><span class="sxs-lookup"><span data-stu-id="71ca9-108">Attribute</span></span></th>
<th><span data-ttu-id="71ca9-109">Typ</span><span class="sxs-lookup"><span data-stu-id="71ca9-109">Type</span></span></th>
<th><span data-ttu-id="71ca9-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="71ca9-110">Required</span></span></th>
<th><span data-ttu-id="71ca9-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71ca9-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="71ca9-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="71ca9-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="71ca9-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="71ca9-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="71ca9-114">Nein</span><span class="sxs-lookup"><span data-stu-id="71ca9-114">No</span></span><br/></td>
<td><span data-ttu-id="71ca9-115"><dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="71ca9-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="71ca9-116">Eine Zeichenfolge, die eine durch Komma getrennte Liste von ganzen Zahlen zwischen 0 und 31 enthält.</span><span class="sxs-lookup"><span data-stu-id="71ca9-116">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="71ca9-117">Leerzeichen sind gültig und werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="71ca9-117">White space is valid and ignored.</span></span><br/> <span data-ttu-id="71ca9-118">Maximale Länge: 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="71ca9-118">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="71ca9-119"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="71ca9-119"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="71ca9-120">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="71ca9-120">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="71ca9-121">Nein</span><span class="sxs-lookup"><span data-stu-id="71ca9-121">No</span></span><br/></td>
<td><span data-ttu-id="71ca9-122">Ordnet das Element einem Befehl <a href="windowsribbon-element-command.md"><strong>zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="71ca9-122">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="71ca9-123">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="71ca9-123">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="71ca9-124">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="71ca9-124">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="71ca9-125">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="71ca9-125">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="71ca9-126">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="71ca9-126">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="71ca9-127"><strong>SizeDefinition</strong></span><span class="sxs-lookup"><span data-stu-id="71ca9-127"><strong>SizeDefinition</strong></span></span><br/></td>
<td><span data-ttu-id="71ca9-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="71ca9-128">xs:string</span></span><br/></td>
<td><span data-ttu-id="71ca9-129">Nein</span><span class="sxs-lookup"><span data-stu-id="71ca9-129">No</span></span><br/></td>
<td><span data-ttu-id="71ca9-130">Wenn angegeben, ist der Wert von <em>SizeDefinition</em> auf eine der Layoutvorlagen beschränkt, <a href="windowsribbon-templates.md">die</a> vom Menübandframework definiert werden.</span><span class="sxs-lookup"><span data-stu-id="71ca9-130">When specified, the value of <em>SizeDefinition</em> is constrained to one of the <a href="windowsribbon-templates.md">layout templates</a> defined by the Ribbon framework.</span></span> <br/> <br/><span data-ttu-id="71ca9-131">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="71ca9-131">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="71ca9-132">Eine beliebige Sequenz von null oder mehr Zeichen.</span><span class="sxs-lookup"><span data-stu-id="71ca9-132">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="71ca9-133">Die maximale Länge ist ungebunden.</span><span class="sxs-lookup"><span data-stu-id="71ca9-133">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="71ca9-134">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="71ca9-134">Child elements</span></span>



| <span data-ttu-id="71ca9-135">Element</span><span class="sxs-lookup"><span data-stu-id="71ca9-135">Element</span></span>                                                                             | <span data-ttu-id="71ca9-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71ca9-136">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="71ca9-137">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="71ca9-137">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="71ca9-138">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="71ca9-139">**Checkbox**</span><span class="sxs-lookup"><span data-stu-id="71ca9-139">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="71ca9-140">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="71ca9-141">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="71ca9-141">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="71ca9-142">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="71ca9-143">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="71ca9-143">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               | <span data-ttu-id="71ca9-144">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="71ca9-145">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="71ca9-145">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="71ca9-146">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="71ca9-147">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="71ca9-147">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="71ca9-148">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="71ca9-149">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="71ca9-149">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="71ca9-150">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-150">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="71ca9-151">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="71ca9-151">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="71ca9-152">Kann nur einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-152">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="71ca9-153">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="71ca9-153">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>         | <span data-ttu-id="71ca9-154">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-154">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="71ca9-155">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="71ca9-155">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/>           | <span data-ttu-id="71ca9-156">Kann nur einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-156">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="71ca9-157">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="71ca9-157">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                         | <span data-ttu-id="71ca9-158">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-158">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="71ca9-159">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="71ca9-159">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="71ca9-160">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-160">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="71ca9-161">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="71ca9-161">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="71ca9-162">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-162">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="71ca9-163">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="71ca9-163">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="71ca9-164">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-164">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="71ca9-165">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="71ca9-165">Parent elements</span></span>



| <span data-ttu-id="71ca9-166">Element</span><span class="sxs-lookup"><span data-stu-id="71ca9-166">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="71ca9-167">**Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="71ca9-167">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="71ca9-168">Hinweise</span><span class="sxs-lookup"><span data-stu-id="71ca9-168">Remarks</span></span>

<span data-ttu-id="71ca9-169">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="71ca9-169">Optional.</span></span>

<span data-ttu-id="71ca9-170">Kann ein oder mehrere Male für jedes [**Tab-Element**](windowsribbon-element-tab.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="71ca9-170">May occur one or more times for each [**Tab**](windowsribbon-element-tab.md) element.</span></span>

<span data-ttu-id="71ca9-171">[**Die Registerkarte**](windowsribbon-element-tab.md) unterstützt [die Anwendungsmodi](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="71ca9-171">[**Tab**](windowsribbon-element-tab.md) supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="71ca9-172">Das Menübandmarkup ist nur gültig, wenn die untergeordneten Elemente von **Group** der für *SizeDefinition angegebenen Vorlage entsprechen.*</span><span class="sxs-lookup"><span data-stu-id="71ca9-172">The Ribbon markup is valid only when the child elements of **Group** correspond to the template specified for *SizeDefinition*.</span></span>

## <a name="examples"></a><span data-ttu-id="71ca9-173">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71ca9-173">Examples</span></span>

<span data-ttu-id="71ca9-174">Im folgenden Codebeispiel wird die Verwendung einer benutzerdefinierten Vorlage in einer **Gruppe veranschaulicht.**</span><span class="sxs-lookup"><span data-stu-id="71ca9-174">The following code example illustrates the use of a custom template in a **Group**.</span></span>


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="71ca9-175">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="71ca9-175">Element information</span></span>

* <span data-ttu-id="71ca9-176">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="71ca9-176">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="71ca9-177">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="71ca9-177">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="71ca9-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71ca9-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ca9-179">Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="71ca9-179">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="71ca9-180">Gruppensteuerung</span><span class="sxs-lookup"><span data-stu-id="71ca9-180">Group control</span></span>](windowsribbon-controls-group.md)
</dt> <dt>

[<span data-ttu-id="71ca9-181">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="71ca9-181">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

