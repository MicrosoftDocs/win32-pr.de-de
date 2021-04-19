---
title: SplitButton-Element
description: Stellt ein Standard Steuerelement für unterteilte Schaltflächen dar.
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- Fensterleiste des SplitButton-Elements
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3235d58d6499d7d57c54e33e1049f40c50dd189a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337237"
---
# <a name="splitbutton-element"></a><span data-ttu-id="fd45b-104">SplitButton-Element</span><span class="sxs-lookup"><span data-stu-id="fd45b-104">SplitButton element</span></span>

<span data-ttu-id="fd45b-105">Stellt ein Standard Steuerelement für unter [teilte Schalt](windowsribbon-controls-splitbutton.md) Flächen dar.</span><span class="sxs-lookup"><span data-stu-id="fd45b-105">Represents a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="fd45b-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="fd45b-106">Usage</span></span>

``` syntax
<SplitButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</SplitButton>
```

## <a name="attributes"></a><span data-ttu-id="fd45b-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="fd45b-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fd45b-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="fd45b-108">Attribute</span></span></th>
<th><span data-ttu-id="fd45b-109">type</span><span class="sxs-lookup"><span data-stu-id="fd45b-109">Type</span></span></th>
<th><span data-ttu-id="fd45b-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fd45b-110">Required</span></span></th>
<th><span data-ttu-id="fd45b-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd45b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fd45b-112"><strong>Applicationmodes</strong></span><span class="sxs-lookup"><span data-stu-id="fd45b-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="fd45b-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="fd45b-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="fd45b-114">Nein</span><span class="sxs-lookup"><span data-stu-id="fd45b-114">No</span></span><br/></td>
<td><span data-ttu-id="fd45b-115">Nur gültig, wenn <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> das übergeordnete Element ist.</span><span class="sxs-lookup"><span data-stu-id="fd45b-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="fd45b-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="fd45b-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fd45b-117">Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste mit ganzen Zahlen zwischen 0 und 31 enthält.</span><span class="sxs-lookup"><span data-stu-id="fd45b-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="fd45b-118">Leerraum ist gültig und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fd45b-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="fd45b-119">Maximale Länge: 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fd45b-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fd45b-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="fd45b-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="fd45b-121">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="fd45b-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="fd45b-122">Nein</span><span class="sxs-lookup"><span data-stu-id="fd45b-122">No</span></span><br/></td>
<td><span data-ttu-id="fd45b-123">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="fd45b-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="fd45b-124">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="fd45b-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fd45b-125">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="fd45b-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="fd45b-126">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="fd45b-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="fd45b-127">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fd45b-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="fd45b-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd45b-128">Child elements</span></span>



| <span data-ttu-id="fd45b-129">Element</span><span class="sxs-lookup"><span data-stu-id="fd45b-129">Element</span></span>                                                                                   | <span data-ttu-id="fd45b-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd45b-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="fd45b-131">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="fd45b-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                 | <span data-ttu-id="fd45b-132">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="fd45b-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fd45b-133">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="fd45b-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                             | <span data-ttu-id="fd45b-134">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="fd45b-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fd45b-135">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="fd45b-135">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                 | <span data-ttu-id="fd45b-136">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="fd45b-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fd45b-137">**Dropdowncolorpicker**</span><span class="sxs-lookup"><span data-stu-id="fd45b-137">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>       | <span data-ttu-id="fd45b-138">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="fd45b-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fd45b-139">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="fd45b-139">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>               | <span data-ttu-id="fd45b-140">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="fd45b-140">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="fd45b-141">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="fd45b-141">**SplitButton**</span></span><br/>                                                                | <span data-ttu-id="fd45b-142">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="fd45b-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fd45b-143">**SplitButton. buttonitem**</span><span class="sxs-lookup"><span data-stu-id="fd45b-143">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/> | <span data-ttu-id="fd45b-144">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="fd45b-144">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="fd45b-145">**SplitButton. menugroups**</span><span class="sxs-lookup"><span data-stu-id="fd45b-145">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/> | <span data-ttu-id="fd45b-146">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="fd45b-146">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="fd45b-147">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="fd45b-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>         | <span data-ttu-id="fd45b-148">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="fd45b-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fd45b-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="fd45b-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                     | <span data-ttu-id="fd45b-150">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="fd45b-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="fd45b-151">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd45b-151">Parent elements</span></span>



| <span data-ttu-id="fd45b-152">Element</span><span class="sxs-lookup"><span data-stu-id="fd45b-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="fd45b-153">**Controlgroup**</span><span class="sxs-lookup"><span data-stu-id="fd45b-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="fd45b-154">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="fd45b-154">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="fd45b-155">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="fd45b-155">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="fd45b-156">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="fd45b-156">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| <span data-ttu-id="fd45b-157">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="fd45b-157">**SplitButton**</span></span><br/>                                                        |
| [<span data-ttu-id="fd45b-158">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="fd45b-158">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fd45b-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd45b-159">Remarks</span></span>

<span data-ttu-id="fd45b-160">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="fd45b-160">Optional.</span></span>

<span data-ttu-id="fd45b-161">Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)-, [**Group**](windowsribbon-element-group.md)-, [**MenuGroup**](windowsribbon-element-menugroup.md)-, **SplitButton**-oder [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="fd45b-161">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton**, or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="fd45b-162">**SplitButton** unterstützt [Anwendungsmodi](ribbon-applicationmodes.md) , wenn es in der linken Spalte des Anwendungs Menüs gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="fd45b-162">**SplitButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="fd45b-163">[**Dropdowngallery**](windowsribbon-element-dropdowngallery.md) und [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) sind keine gültigen untergeordneten Elemente von [**DropDownButton**](windowsribbon-element-dropdownbutton.md) , wenn **DropDownButton** ein Nachfolger von [**applicationmenu**](windowsribbon-element-applicationmenu.md)ist.</span><span class="sxs-lookup"><span data-stu-id="fd45b-163">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of [**DropDownButton**](windowsribbon-element-dropdownbutton.md) when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

<span data-ttu-id="fd45b-164">[**SplitButton. menugroups**](windowsribbon-element-splitbutton-menugroups.md) muss einmal auftreten, wenn Folgendes nicht als untergeordnete Elemente von **SplitButton** vorhanden ist:</span><span class="sxs-lookup"><span data-stu-id="fd45b-164">[**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) must occur once if the following are not present as child elements of **SplitButton**:</span></span>

-   [<span data-ttu-id="fd45b-165">**Gedrückt**</span><span class="sxs-lookup"><span data-stu-id="fd45b-165">**Button**</span></span>](windowsribbon-element-button.md)
-   [<span data-ttu-id="fd45b-166">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="fd45b-166">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)
-   [<span data-ttu-id="fd45b-167">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="fd45b-167">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)
-   [<span data-ttu-id="fd45b-168">**Dropdowncolorpicker**</span><span class="sxs-lookup"><span data-stu-id="fd45b-168">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
-   [<span data-ttu-id="fd45b-169">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="fd45b-169">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)
-   <span data-ttu-id="fd45b-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="fd45b-170">**SplitButton**</span></span>
-   [<span data-ttu-id="fd45b-171">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="fd45b-171">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)
-   [<span data-ttu-id="fd45b-172">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="fd45b-172">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)

<span data-ttu-id="fd45b-173">Diese Steuerelemente werden als untergeordnete Elemente eines einzelnen standardmäßigen [**SplitButton. menugroups**](windowsribbon-element-splitbutton-menugroups.md) -Elements behandelt.</span><span class="sxs-lookup"><span data-stu-id="fd45b-173">These controls are treated as child elements of a single default [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="fd45b-174">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd45b-174">Examples</span></span>

<span data-ttu-id="fd45b-175">Im folgenden Beispiel wird das grundlegende Markup für die [Trenn Schaltfläche](windowsribbon-controls-splitbutton.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fd45b-175">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="fd45b-176">Dieser Code Abschnitt zeigt die **SplitButton** -Befehls Deklarationen mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **SplitButton** -Element fungiert.</span><span class="sxs-lookup"><span data-stu-id="fd45b-176">This section of code shows the **SplitButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="fd45b-177">In diesem Code Abschnitt werden die Deklarationen des **SplitButton** -Steuer Elements angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fd45b-177">This section of code shows the **SplitButton** control declarations.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="fd45b-178">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fd45b-178">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="fd45b-179">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="fd45b-179">Minimum supported system</span></span><br/> | <span data-ttu-id="fd45b-180">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fd45b-180">Windows 7</span></span> |
| <span data-ttu-id="fd45b-181">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="fd45b-181">Can be empty</span></span>                        | <span data-ttu-id="fd45b-182">Nein</span><span class="sxs-lookup"><span data-stu-id="fd45b-182">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="fd45b-183">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fd45b-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd45b-184">Steuerelement "Split Button</span><span class="sxs-lookup"><span data-stu-id="fd45b-184">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[<span data-ttu-id="fd45b-185">**Setmodes**</span><span class="sxs-lookup"><span data-stu-id="fd45b-185">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

