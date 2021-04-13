---
title: Controlgroup-Element
description: Stellt eine Gruppe von Steuerelementen in einer sizedefinition-Layoutvorlage dar.
ms.assetid: 688f3fa5-f305-4554-b16a-590983cf23b9
keywords:
- Windows-Menüband für controlgroup-Element
topic_type:
- apiref
api_name:
- ControlGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd6df69f788efe01b9eb2c7ffe0aaddd98bd7198
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389784"
---
# <a name="controlgroup-element"></a><span data-ttu-id="d7f93-104">Controlgroup-Element</span><span class="sxs-lookup"><span data-stu-id="d7f93-104">ControlGroup element</span></span>

<span data-ttu-id="d7f93-105">Stellt eine Gruppe von Steuerelementen in einer [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Layoutvorlage dar.</span><span class="sxs-lookup"><span data-stu-id="d7f93-105">Represents a group of controls in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template.</span></span>

## <a name="usage"></a><span data-ttu-id="d7f93-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="d7f93-106">Usage</span></span>

``` syntax
<ControlGroup
  SequenceNumber = "xs:positiveInteger">
  child elements
</ControlGroup>
```

## <a name="attributes"></a><span data-ttu-id="d7f93-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="d7f93-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7f93-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="d7f93-108">Attribute</span></span></th>
<th><span data-ttu-id="d7f93-109">type</span><span class="sxs-lookup"><span data-stu-id="d7f93-109">Type</span></span></th>
<th><span data-ttu-id="d7f93-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d7f93-110">Required</span></span></th>
<th><span data-ttu-id="d7f93-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7f93-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d7f93-112"><strong>SequenceNumber</strong></span><span class="sxs-lookup"><span data-stu-id="d7f93-112"><strong>SequenceNumber</strong></span></span><br/></td>
<td><span data-ttu-id="d7f93-113">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d7f93-113">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d7f93-114">Nein</span><span class="sxs-lookup"><span data-stu-id="d7f93-114">No</span></span><br/></td>
<td><span data-ttu-id="d7f93-115">Nur gültig, wenn die <a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a> das übergeordnete Element ist.</span><span class="sxs-lookup"><span data-stu-id="d7f93-115">Valid only when <a href="windowsribbon-element-group.md"><strong>Group</strong></a> is the parent element.</span></span><br/> <span data-ttu-id="d7f93-116">Jede <em>sequencenumkehr</em> muss innerhalb eines <a href="windowsribbon-element-group.md"><strong>Group</strong></a> -Elements eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d7f93-116">Each <em>SequenceNumber</em> must be unique within a <a href="windowsribbon-element-group.md"><strong>Group</strong></a> element.</span></span> <span data-ttu-id="d7f93-117">Die Werte für <em>sequencenenumber</em> sollten für jedes <strong>Group</strong> -Element erhöht werden, müssen jedoch nicht sequenziell sein.</span><span class="sxs-lookup"><span data-stu-id="d7f93-117">The values for <em>SequenceNumber</em> should increase for each <strong>Group</strong> element, but do not need to be sequential.</span></span> <br/> <br/><span data-ttu-id="d7f93-118">
<dt><span></span><span></span><strong></strong> (xs: positivin teger)</span><span class="sxs-lookup"><span data-stu-id="d7f93-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d7f93-119">Ein beliebiger positiver ganzzahliger Wert zwischen 1000 und 59999 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="d7f93-119">Any positive integer value between 1000 and 59999, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d7f93-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d7f93-120">Child elements</span></span>



| <span data-ttu-id="d7f93-121">Element</span><span class="sxs-lookup"><span data-stu-id="d7f93-121">Element</span></span>                                                                                 | <span data-ttu-id="d7f93-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7f93-122">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="d7f93-123">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="d7f93-123">**Button**</span></span>](windowsribbon-element-button.md)<br/>                               | <span data-ttu-id="d7f93-124">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="d7f93-124">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d7f93-125">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="d7f93-125">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                           | <span data-ttu-id="d7f93-126">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="d7f93-126">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d7f93-127">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="d7f93-127">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                           | <span data-ttu-id="d7f93-128">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="d7f93-128">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d7f93-129">**Controlsizedefinition**</span><span class="sxs-lookup"><span data-stu-id="d7f93-129">**ControlSizeDefinition**</span></span>](windowsribbon-element-controlsizedefinition.md)<br/> | <span data-ttu-id="d7f93-130">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="d7f93-130">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d7f93-131">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="d7f93-131">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>               | <span data-ttu-id="d7f93-132">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="d7f93-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d7f93-133">**Dropdowncolorpicker**</span><span class="sxs-lookup"><span data-stu-id="d7f93-133">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>     | <span data-ttu-id="d7f93-134">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="d7f93-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d7f93-135">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="d7f93-135">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>             | <span data-ttu-id="d7f93-136">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="d7f93-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d7f93-137">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="d7f93-137">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                     | <span data-ttu-id="d7f93-138">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="d7f93-138">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="d7f93-139">**Inribbongallery**</span><span class="sxs-lookup"><span data-stu-id="d7f93-139">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>             | <span data-ttu-id="d7f93-140">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="d7f93-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d7f93-141">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="d7f93-141">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                             | <span data-ttu-id="d7f93-142">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="d7f93-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d7f93-143">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="d7f93-143">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                     | <span data-ttu-id="d7f93-144">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="d7f93-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d7f93-145">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="d7f93-145">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>       | <span data-ttu-id="d7f93-146">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="d7f93-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d7f93-147">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="d7f93-147">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                   | <span data-ttu-id="d7f93-148">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="d7f93-148">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="d7f93-149">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d7f93-149">Parent elements</span></span>



| <span data-ttu-id="d7f93-150">Element</span><span class="sxs-lookup"><span data-stu-id="d7f93-150">Element</span></span>                                                                             |
|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f93-151">**Controlgroup**</span><span class="sxs-lookup"><span data-stu-id="d7f93-151">**ControlGroup**</span></span><br/>                                                         |
| [<span data-ttu-id="d7f93-152">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="d7f93-152">**Group**</span></span>](windowsribbon-element-group.md)<br/>                             |
| [<span data-ttu-id="d7f93-153">**Groupsizedefinition**</span><span class="sxs-lookup"><span data-stu-id="d7f93-153">**GroupSizeDefinition**</span></span>](windowsribbon-element-groupsizedefinition.md)<br/> |
| [<span data-ttu-id="d7f93-154">**Zeile**</span><span class="sxs-lookup"><span data-stu-id="d7f93-154">**Row**</span></span>](windowsribbon-element-row.md)<br/>                                 |



## <a name="remarks"></a><span data-ttu-id="d7f93-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7f93-155">Remarks</span></span>

<span data-ttu-id="d7f93-156">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d7f93-156">Optional.</span></span>

<span data-ttu-id="d7f93-157">Kann für jedes [**Group**](windowsribbon-element-group.md) -oder **controlgroup** -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="d7f93-157">May occur one or more times for each [**Group**](windowsribbon-element-group.md) or **ControlGroup** element.</span></span>

<span data-ttu-id="d7f93-158">Wenn keine Sequenznummern angegeben werden, werden Elemente in der Reihenfolge gerendert, in der das Menüband-Markup angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d7f93-158">If no sequence numbers are supplied, elements are rendered in the order specified in the Ribbon markup.</span></span>

<span data-ttu-id="d7f93-159">Wenn " [**Group**](windowsribbon-element-group.md) " oder " **controlgroup** " das übergeordnete Element ist, wird " **controlgroup** " auf die folgenden möglichen untergeordneten Elemente beschränkt: [**Schaltfläche**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**Dropdown Button**](windowsribbon-element-dropdownbutton.md), [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md), [**dropdowngallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**inribbongallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)oder UMSCHALT [**Fläche**](windowsribbon-element-togglebutton.md)</span><span class="sxs-lookup"><span data-stu-id="d7f93-159">If [**Group**](windowsribbon-element-group.md) or **ControlGroup** is the parent element then **ControlGroup** is constrained to the following possible child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**InRibbonGallery**](windowsribbon-element-inribbongallery.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md)</span></span>

<span data-ttu-id="d7f93-160">Wenn " [**Row**](windowsribbon-element-row.md) " oder " [**groupsizedefinition**](windowsribbon-element-groupsizedefinition.md) " das übergeordnete Element ist, wird die [**Gruppe**](windowsribbon-element-group.md) auf das folgende mögliche untergeordnete Element beschränkt: [**controlsizedefinition**](windowsribbon-element-controlsizedefinition.md).</span><span class="sxs-lookup"><span data-stu-id="d7f93-160">Otherwise, when [**Row**](windowsribbon-element-row.md) or [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) is the parent, [**Group**](windowsribbon-element-group.md) is constrained to the following possible child element: [**ControlSizeDefinition**](windowsribbon-element-controlsizedefinition.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d7f93-161">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7f93-161">Examples</span></span>

<span data-ttu-id="d7f93-162">Im folgenden Codebeispiel wird das grundlegende Markup für eine benutzerdefinierte [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Layoutvorlage mit vier Schaltflächen mit verschiedenen [**Gruppen**](windowsribbon-element-group.md) Elementen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d7f93-162">The following code example demonstrates the basic markup for a custom four-button [**SizeDefinition**](windowsribbon-element-sizedefinition.md) layout template with various [**Group**](windowsribbon-element-group.md) elements.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="d7f93-163">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d7f93-163">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="d7f93-164">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="d7f93-164">Minimum supported system</span></span><br/> | <span data-ttu-id="d7f93-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d7f93-165">Windows 7</span></span> |
| <span data-ttu-id="d7f93-166">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="d7f93-166">Can be empty</span></span>                        | <span data-ttu-id="d7f93-167">Nein</span><span class="sxs-lookup"><span data-stu-id="d7f93-167">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="d7f93-168">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d7f93-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f93-169">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d7f93-169">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





