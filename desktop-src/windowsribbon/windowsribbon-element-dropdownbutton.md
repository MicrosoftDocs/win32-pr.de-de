---
title: DropDownButton-Element
description: Stellt ein standardmäßiges Drop-Down Button-Steuerelement dar.
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- DropDownButton-Element Windows-Menüband
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a42b8ffb6d39c1da8993972c0b25995f778bdaca
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442961"
---
# <a name="dropdownbutton-element"></a><span data-ttu-id="fe4a5-104">DropDownButton-Element</span><span class="sxs-lookup"><span data-stu-id="fe4a5-104">DropDownButton element</span></span>

<span data-ttu-id="fe4a5-105">Stellt ein standardmäßiges [Dropdown-Schaltflächen-Steuerelement](windowsribbon-controls-dropdownbutton.md) dar.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-105">Represents a standard [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="fe4a5-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="fe4a5-106">Usage</span></span>

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
```

## <a name="attributes"></a><span data-ttu-id="fe4a5-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="fe4a5-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe4a5-108">attribute</span><span class="sxs-lookup"><span data-stu-id="fe4a5-108">Attribute</span></span></th>
<th><span data-ttu-id="fe4a5-109">Typ</span><span class="sxs-lookup"><span data-stu-id="fe4a5-109">Type</span></span></th>
<th><span data-ttu-id="fe4a5-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fe4a5-110">Required</span></span></th>
<th><span data-ttu-id="fe4a5-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe4a5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe4a5-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="fe4a5-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="fe4a5-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="fe4a5-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="fe4a5-114">Nein</span><span class="sxs-lookup"><span data-stu-id="fe4a5-114">No</span></span><br/></td>
<td><span data-ttu-id="fe4a5-115">Nur gültig, wenn <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> das übergeordnete Element ist.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="fe4a5-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="fe4a5-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fe4a5-117">Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste von ganzen Zahlen zwischen 0 und 31 enthält.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="fe4a5-118">Leerraum ist gültig und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="fe4a5-119">Maximale Länge: 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe4a5-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="fe4a5-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="fe4a5-121">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="fe4a5-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="fe4a5-122">Nein</span><span class="sxs-lookup"><span data-stu-id="fe4a5-122">No</span></span><br/></td>
<td><span data-ttu-id="fe4a5-123">Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="fe4a5-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="fe4a5-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="fe4a5-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fe4a5-125">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999 einschließlich oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="fe4a5-126">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="fe4a5-127">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="fe4a5-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fe4a5-128">Child elements</span></span>



| <span data-ttu-id="fe4a5-129">Element</span><span class="sxs-lookup"><span data-stu-id="fe4a5-129">Element</span></span>                                                                             | <span data-ttu-id="fe4a5-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe4a5-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="fe4a5-131">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="fe4a5-132">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe4a5-133">**Checkbox**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="fe4a5-134">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe4a5-135">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-135">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="fe4a5-136">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-136">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="fe4a5-137">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-137">**DropDownButton**</span></span><br/>                                                       | <span data-ttu-id="fe4a5-138">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe4a5-139">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-139">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="fe4a5-140">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe4a5-141">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-141">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="fe4a5-142">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe4a5-143">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-143">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                     | <span data-ttu-id="fe4a5-144">Muss mindestens einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="fe4a5-144">Must occur at least once</span></span><br/> <br/>    |
| [<span data-ttu-id="fe4a5-145">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-145">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="fe4a5-146">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe4a5-147">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="fe4a5-148">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe4a5-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="fe4a5-150">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="fe4a5-151">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fe4a5-151">Parent elements</span></span>



| <span data-ttu-id="fe4a5-152">Element</span><span class="sxs-lookup"><span data-stu-id="fe4a5-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="fe4a5-153">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| <span data-ttu-id="fe4a5-154">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-154">**DropDownButton**</span></span><br/>                                                     |
| [<span data-ttu-id="fe4a5-155">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-155">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="fe4a5-156">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-156">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="fe4a5-157">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-157">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="fe4a5-158">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-158">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="fe4a5-159">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-159">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fe4a5-160">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fe4a5-160">Remarks</span></span>

<span data-ttu-id="fe4a5-161">Optional oder erforderlich, je nach übergeordnetem Element.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-161">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="fe4a5-162">Kann ein oder mehrere Male für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) **DropDownButton-,** [**DropDownGallery-,**](windowsribbon-element-dropdowngallery.md) [**Group-, MenuGroup-,**](windowsribbon-element-menugroup.md) [**SplitButton-**](windowsribbon-element-splitbutton.md)oder [**SplitButtonGallery-Element**](windowsribbon-element-splitbuttongallery.md) auftreten. [](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="fe4a5-162">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="fe4a5-163">**DropDownButton** unterstützt [Anwendungsmodi,](ribbon-applicationmodes.md) wenn es in der linken Spalte des Anwendungsmenüs gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-163">**DropDownButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="fe4a5-164">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) und [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) sind keine gültigen untergeordneten Elemente von **DropDownButton,** wenn **DropDownButton** ein Nachfolger von [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)ist.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-164">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of **DropDownButton** when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fe4a5-165">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe4a5-165">Examples</span></span>

<span data-ttu-id="fe4a5-166">Im folgenden Beispiel wird das grundlegende Markup für **dropDownButton** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-166">The following example demonstrates the basic markup for the **DropDownButton**.</span></span>

<span data-ttu-id="fe4a5-167">Dieser Codeabschnitt zeigt die **DropDownButton-Befehlsdeklarationen** mit einer zugeordneten [**Gruppe,**](windowsribbon-element-group.md) die als übergeordneter Container für das **DropDownButton-Element** fungiert.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-167">This section of code shows the **DropDownButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **DropDownButton** element.</span></span>


```XML
<!-- DropDownButton -->
<Command Name="cmdDropDownButtonGroup"
         Symbol="cmdDropDownButtonGroup"
         Comment="DropDownButton Group"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDropDownButton"
         Symbol="cmdDropDownButton"
         Comment="DropDownButton"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDDBButton1"
         Symbol="cmdDDBButton1"
         Comment="DDBButton1"
         LabelTitle="DDB Button"/>
<Command Name="cmdDDBColorPicker"
         Symbol="cmdDDBColorPicker"
         Comment="DDBColorPicker"
         LabelTitle="DDB ColorPicker"/>
```



<span data-ttu-id="fe4a5-168">Dieser Codeabschnitt zeigt die **DropDownButton-Steuerelementdeklarationen.**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-168">This section of code shows the **DropDownButton** control declarations.</span></span>


```XML
<Group CommandName="cmdDropDownButtonGroup">
  <DropDownButton CommandName="cmdDropDownButton">
    <MenuGroup>
      <Button CommandName="cmdDDBButton1"/>
      <DropDownColorPicker CommandName="cmdDDBColorPicker"/>
    </MenuGroup>
  </DropDownButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="fe4a5-169">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fe4a5-169">Element information</span></span>

* <span data-ttu-id="fe4a5-170">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="fe4a5-170">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="fe4a5-171">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="fe4a5-171">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="fe4a5-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe4a5-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe4a5-173">Dropdown-Schaltflächen-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="fe4a5-173">Drop-Down Button control</span></span>](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[<span data-ttu-id="fe4a5-174">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-174">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

