---
title: ControlGroup-Element
description: Stellt eine Gruppe von Steuerelementen in einer SizeDefinition-Layoutvorlage dar.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- ControlGroup-Element Im Windows-Menüband
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d2b49612102d03003c2f61395a56647aaef4475
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442941"
---
# <a name="controlgroup-element"></a><span data-ttu-id="35dc8-104">ControlGroup-Element</span><span class="sxs-lookup"><span data-stu-id="35dc8-104">ControlGroup element</span></span>

<span data-ttu-id="35dc8-105">Stellt eine Gruppe von Steuerelementen in einer [**SizeDefinition-Layoutvorlage**](windowsribbon-element-sizedefinition.md) dar.</span><span class="sxs-lookup"><span data-stu-id="35dc8-105">Represents a group of controls in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="35dc8-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="35dc8-106">Usage</span></span>

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
```

## <a name="attributes"></a><span data-ttu-id="35dc8-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="35dc8-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35dc8-108">attribute</span><span class="sxs-lookup"><span data-stu-id="35dc8-108">Attribute</span></span></th>
<th><span data-ttu-id="35dc8-109">Typ</span><span class="sxs-lookup"><span data-stu-id="35dc8-109">Type</span></span></th>
<th><span data-ttu-id="35dc8-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="35dc8-110">Required</span></span></th>
<th><span data-ttu-id="35dc8-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35dc8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35dc8-112"><strong>SequenceNumber</strong></span><span class="sxs-lookup"><span data-stu-id="35dc8-112"><strong>SequenceNumber</strong></span></span><br/></td>
<td><span data-ttu-id="35dc8-113">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="35dc8-113">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="35dc8-114">Nein</span><span class="sxs-lookup"><span data-stu-id="35dc8-114">No</span></span><br/></td>
<td><span data-ttu-id="35dc8-115">Nur gültig, <a href="windowsribbon-element-group.md"><strong>wenn Group</strong></a> das übergeordnete Element ist.</span><span class="sxs-lookup"><span data-stu-id="35dc8-115">Valid only when <a href="windowsribbon-element-group.md"><strong>Group</strong></a> is the parent element.</span></span><br/> <span data-ttu-id="35dc8-116">Jede <em>SequenceNumber</em> muss innerhalb eines Group-Elements <a href="windowsribbon-element-group.md"><strong>eindeutig</strong></a> sein.</span><span class="sxs-lookup"><span data-stu-id="35dc8-116">Each <em>SequenceNumber</em> must be unique within a <a href="windowsribbon-element-group.md"><strong>Group</strong></a> element.</span></span> <span data-ttu-id="35dc8-117">Die Werte für <em>SequenceNumber</em> sollten für jedes <strong>Group-Element</strong> erhöht werden, müssen jedoch nicht sequenziell sein.</span><span class="sxs-lookup"><span data-stu-id="35dc8-117">The values for <em>SequenceNumber</em> should increase for each <strong>Group</strong> element, but do not need to be sequential.</span></span> <br/> <br/><span data-ttu-id="35dc8-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="35dc8-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="35dc8-119">Ein positiver ganzzahliger Wert zwischen 1000 und 59999 einschließlich .</span><span class="sxs-lookup"><span data-stu-id="35dc8-119">Any positive integer value between 1000 and 59999, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="35dc8-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35dc8-120">Child elements</span></span>



| <span data-ttu-id="35dc8-121">Element</span><span class="sxs-lookup"><span data-stu-id="35dc8-121">Element</span></span>                                                                                 | <span data-ttu-id="35dc8-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35dc8-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="35dc8-123">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="35dc8-123">**Button**</span></span>](windowsribbon-element-button.md)<br/>                               | <span data-ttu-id="35dc8-124">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="35dc8-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35dc8-125">**Checkbox**</span><span class="sxs-lookup"><span data-stu-id="35dc8-125">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                           | <span data-ttu-id="35dc8-126">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="35dc8-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35dc8-127">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="35dc8-127">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                           | <span data-ttu-id="35dc8-128">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="35dc8-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35dc8-129">**ControlSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="35dc8-129">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="35dc8-130">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="35dc8-130">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35dc8-131">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="35dc8-131">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>               | <span data-ttu-id="35dc8-132">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="35dc8-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35dc8-133">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="35dc8-133">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>     | <span data-ttu-id="35dc8-134">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="35dc8-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35dc8-135">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="35dc8-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>             | <span data-ttu-id="35dc8-136">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="35dc8-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35dc8-137">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="35dc8-137">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                     | <span data-ttu-id="35dc8-138">Kann nur einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="35dc8-138">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="35dc8-139">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="35dc8-139">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>             | <span data-ttu-id="35dc8-140">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="35dc8-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35dc8-141">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="35dc8-141">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                             | <span data-ttu-id="35dc8-142">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="35dc8-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35dc8-143">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="35dc8-143">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                     | <span data-ttu-id="35dc8-144">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="35dc8-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35dc8-145">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="35dc8-145">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>       | <span data-ttu-id="35dc8-146">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="35dc8-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="35dc8-147">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="35dc8-147">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                   | <span data-ttu-id="35dc8-148">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="35dc8-148">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="35dc8-149">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="35dc8-149">Parent elements</span></span>



| <span data-ttu-id="35dc8-150">Element</span><span class="sxs-lookup"><span data-stu-id="35dc8-150">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| <span data-ttu-id="35dc8-151">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="35dc8-151">**ControlGroup**</span></span><br/>                                                         |
| [<span data-ttu-id="35dc8-152">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="35dc8-152">**Group**</span></span>](windowsribbon-element-group.md)<br/>                             |
| [<span data-ttu-id="35dc8-153">**GroupSizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="35dc8-153">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="35dc8-154">**Zeile**</span><span class="sxs-lookup"><span data-stu-id="35dc8-154">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="35dc8-155">Hinweise</span><span class="sxs-lookup"><span data-stu-id="35dc8-155">Remarks</span></span>

<span data-ttu-id="35dc8-156">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="35dc8-156">Optional.</span></span>

<span data-ttu-id="35dc8-157">Kann ein oder mehrere Male für jedes [**Group- oder**](windowsribbon-element-group.md) **ControlGroup-Element** auftreten.</span><span class="sxs-lookup"><span data-stu-id="35dc8-157">May occur one or more times for each [**Group**](windowsribbon-element-group.md) or **ControlGroup** element.</span></span>

<span data-ttu-id="35dc8-158">Wenn keine Sequenznummern angegeben werden, werden Elemente in der im Menübandmarkup angegebenen Reihenfolge gerendert.</span><span class="sxs-lookup"><span data-stu-id="35dc8-158">If no sequence numbers are supplied, elements are rendered in the order specified in the Ribbon markup.</span></span>

<span data-ttu-id="35dc8-159">Wenn [**Group**](windowsribbon-element-group.md) oder **ControlGroup** das übergeordnete Element ist, **ist ControlGroup** auf die folgenden möglichen untergeordneten Elemente beschränkt: [**Button,**](windowsribbon-element-button.md) [**CheckBox,**](windowsribbon-element-checkbox.md) [**ComboBox,**](windowsribbon-element-combobox.md) [**DropDownButton,**](windowsribbon-element-dropdownbutton.md) [**DropDownColorPicker,**](windowsribbon-element-dropdowncolorpicker.md) [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**FontControl,**](windowsribbon-element-fontcontrol.md) [**InRibbonGallery,**](windowsribbon-element-inribbongallery.md) [**Spinner,**](windowsribbon-element-spinner.md) [**SplitButton,**](windowsribbon-element-splitbutton.md) [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)oder [**ToggleButton**](windowsribbon-element-togglebutton.md)</span><span class="sxs-lookup"><span data-stu-id="35dc8-159">If [**Group**](windowsribbon-element-group.md) or **ControlGroup** is the parent element then **ControlGroup** is constrained to the following possible child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md)</span></span>

<span data-ttu-id="35dc8-160">Wenn Row [**oder**](windowsribbon-element-row.md) [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) das übergeordnete Element ist, ist [**Group**](windowsribbon-element-group.md) andernfalls auf das folgende mögliche untergeordnete Element [**beschränkt: ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span><span class="sxs-lookup"><span data-stu-id="35dc8-160">Otherwise, when [**Row**](windowsribbon-element-row.md) or [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) is the parent, [**Group**](windowsribbon-element-group.md) is constrained to the following possible child element: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span></span>

## <a name="examples"></a><span data-ttu-id="35dc8-161">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35dc8-161">Examples</span></span>

<span data-ttu-id="35dc8-162">Im folgenden Codebeispiel wird das grundlegende Markup für eine benutzerdefinierte [**SizeDefinition-Layoutvorlage**](windowsribbon-element-sizedefinition.md) mit vier Schaltflächen mit verschiedenen [**Group-Elementen**](windowsribbon-element-group.md) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="35dc8-162">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various [**Group**](windowsribbon-element-group.md) elements.</span></span>


```XML
<Group CommandName="cmdButtonGroup2">
  <SizeDefinition>
    <ControlNameMap>
      <ControlNameDefinition Name="button1"/>
      <ControlNameDefinition Name="button2"/>
      <ControlNameDefinition Name="button3"/>
      <ControlNameDefinition Name="button4"/>
    </ControlNameMap>
    <GroupSizeDefinition Size="Large">
      <ControlGroup>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Large"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Large"
                               IsLabelVisible="true" />
      </ControlGroup>
      <ColumnBreak ShowSeparator="true"/>
      <ControlGroup>
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Large"
                              IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                              ImageSize="Large"
                              IsLabelVisible="true" />
      </ControlGroup>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="true" />
      </Row>
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <Row>
        <ControlSizeDefinition ControlName="button1"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button3"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
      <Row>
        <ControlSizeDefinition ControlName="button2"
                               ImageSize="Small"
                               IsLabelVisible="true" />
        <ControlSizeDefinition ControlName="button4"
                               ImageSize="Small"
                               IsLabelVisible="false" />
      </Row>
    </GroupSizeDefinition>
  </SizeDefinition>
  <Button CommandName="cmdButtonG21"></Button>
  <Button CommandName="cmdButtonG22"></Button>
  <Button CommandName="cmdButtonG23"></Button>
  <Button CommandName="cmdButtonG24"></Button>
</Group>
<Group CommandName="cmdCheckBoxGroup">
  <CheckBox CommandName="cmdCheckBox"></CheckBox>
</Group>
<Group CommandName="cmdToggleButtonGroup"
       SizeDefinition="OneButton">
  <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
</Group>
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="35dc8-163">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="35dc8-163">Element information</span></span>

* <span data-ttu-id="35dc8-164">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="35dc8-164">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="35dc8-165">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="35dc8-165">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="35dc8-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35dc8-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35dc8-167">Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="35dc8-167">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





