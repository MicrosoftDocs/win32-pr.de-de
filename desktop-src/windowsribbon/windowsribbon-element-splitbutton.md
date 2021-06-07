---
title: SplitButton-Element
description: Stellt ein Standardmäßiges Split Button-Steuerelement dar.
ms.assetid: dece1100-ed04-49a3-a16d-3c5d5e7a2225
keywords:
- SplitButton-Element Im Windows-Menüband
topic_type:
- apiref
api_name:
- SplitButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf03d85dd0402548d02f107dafb209b68c13bb72
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444401"
---
# <a name="splitbutton-element"></a><span data-ttu-id="45ff6-104">SplitButton-Element</span><span class="sxs-lookup"><span data-stu-id="45ff6-104">SplitButton element</span></span>

<span data-ttu-id="45ff6-105">Stellt ein Standardmäßiges [Split Button-Steuerelement](windowsribbon-controls-splitbutton.md) dar.</span><span class="sxs-lookup"><span data-stu-id="45ff6-105">Represents a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="45ff6-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="45ff6-106">Usage</span></span>

``` syntax
<SplitButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</SplitButton>
```

## <a name="attributes"></a><span data-ttu-id="45ff6-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="45ff6-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45ff6-108">attribute</span><span class="sxs-lookup"><span data-stu-id="45ff6-108">Attribute</span></span></th>
<th><span data-ttu-id="45ff6-109">Typ</span><span class="sxs-lookup"><span data-stu-id="45ff6-109">Type</span></span></th>
<th><span data-ttu-id="45ff6-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="45ff6-110">Required</span></span></th>
<th><span data-ttu-id="45ff6-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45ff6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="45ff6-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="45ff6-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="45ff6-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="45ff6-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="45ff6-114">Nein</span><span class="sxs-lookup"><span data-stu-id="45ff6-114">No</span></span><br/></td>
<td><span data-ttu-id="45ff6-115">Nur gültig, <a href="windowsribbon-element-menugroup.md"><strong>wenn MenuGroup</strong></a> das übergeordnete Element ist.</span><span class="sxs-lookup"><span data-stu-id="45ff6-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="45ff6-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="45ff6-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="45ff6-117">Eine Zeichenfolge, die eine durch Komma getrennte Liste von ganzen Zahlen zwischen 0 und 31 enthält.</span><span class="sxs-lookup"><span data-stu-id="45ff6-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="45ff6-118">Leerzeichen sind gültig und werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="45ff6-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="45ff6-119">Maximale Länge: 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="45ff6-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="45ff6-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="45ff6-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="45ff6-121">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="45ff6-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="45ff6-122">Nein</span><span class="sxs-lookup"><span data-stu-id="45ff6-122">No</span></span><br/></td>
<td><span data-ttu-id="45ff6-123">Ordnet das Element einem Befehl <a href="windowsribbon-element-command.md"><strong>zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="45ff6-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="45ff6-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="45ff6-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="45ff6-125">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="45ff6-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="45ff6-126">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="45ff6-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="45ff6-127">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="45ff6-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="45ff6-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45ff6-128">Child elements</span></span>



| <span data-ttu-id="45ff6-129">Element</span><span class="sxs-lookup"><span data-stu-id="45ff6-129">Element</span></span>                                                                                   | <span data-ttu-id="45ff6-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45ff6-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="45ff6-131">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="45ff6-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                 | <span data-ttu-id="45ff6-132">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="45ff6-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="45ff6-133">**Checkbox**</span><span class="sxs-lookup"><span data-stu-id="45ff6-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                             | <span data-ttu-id="45ff6-134">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="45ff6-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="45ff6-135">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="45ff6-135">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                 | <span data-ttu-id="45ff6-136">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="45ff6-136">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="45ff6-137">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="45ff6-137">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/>       | <span data-ttu-id="45ff6-138">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="45ff6-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="45ff6-139">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="45ff6-139">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>               | <span data-ttu-id="45ff6-140">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="45ff6-140">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="45ff6-141">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="45ff6-141">**SplitButton**</span></span><br/>                                                                | <span data-ttu-id="45ff6-142">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="45ff6-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="45ff6-143">**SplitButton.ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="45ff6-143">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/> | <span data-ttu-id="45ff6-144">Kann nur einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="45ff6-144">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="45ff6-145">**SplitButton.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="45ff6-145">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/> | <span data-ttu-id="45ff6-146">Kann nur einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="45ff6-146">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="45ff6-147">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="45ff6-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>         | <span data-ttu-id="45ff6-148">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="45ff6-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="45ff6-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="45ff6-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                     | <span data-ttu-id="45ff6-150">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="45ff6-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="45ff6-151">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="45ff6-151">Parent elements</span></span>



| <span data-ttu-id="45ff6-152">Element</span><span class="sxs-lookup"><span data-stu-id="45ff6-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="45ff6-153">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="45ff6-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="45ff6-154">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="45ff6-154">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="45ff6-155">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="45ff6-155">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="45ff6-156">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="45ff6-156">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| <span data-ttu-id="45ff6-157">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="45ff6-157">**SplitButton**</span></span><br/>                                                        |
| [<span data-ttu-id="45ff6-158">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="45ff6-158">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="45ff6-159">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45ff6-159">Remarks</span></span>

<span data-ttu-id="45ff6-160">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="45ff6-160">Optional.</span></span>

<span data-ttu-id="45ff6-161">Kann ein oder mehrere Male für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) [**DropDownGallery-,**](windowsribbon-element-dropdowngallery.md) [**Group-,**](windowsribbon-element-group.md) [**MenuGroup-,**](windowsribbon-element-menugroup.md) **SplitButton-** oder [**SplitButtonGallery-Element**](windowsribbon-element-splitbuttongallery.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="45ff6-161">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), **SplitButton**, or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="45ff6-162">**SplitButton unterstützt** [Anwendungsmodi,](ribbon-applicationmodes.md) wenn es in der linken Spalte des Anwendungsmenüs gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="45ff6-162">**SplitButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="45ff6-163">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) und [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) sind keine gültigen untergeordneten Elemente von [**DropDownButton,**](windowsribbon-element-dropdownbutton.md) wenn **DropDownButton** ein Nachfolger von [**ApplicationMenu ist.**](windowsribbon-element-applicationmenu.md)</span><span class="sxs-lookup"><span data-stu-id="45ff6-163">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of [**DropDownButton**](windowsribbon-element-dropdownbutton.md) when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

<span data-ttu-id="45ff6-164">[**SplitButton.MenuGroups muss**](windowsribbon-element-splitbutton-menugroups.md) einmal auftreten, wenn folgende Elemente nicht als untergeordnete Elemente von **SplitButton vorhanden sind:**</span><span class="sxs-lookup"><span data-stu-id="45ff6-164">[**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) must occur once if the following are not present as child elements of **SplitButton**:</span></span>

-   [<span data-ttu-id="45ff6-165">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="45ff6-165">**Button**</span></span>](windowsribbon-element-button.md)
-   [<span data-ttu-id="45ff6-166">**Checkbox**</span><span class="sxs-lookup"><span data-stu-id="45ff6-166">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)
-   [<span data-ttu-id="45ff6-167">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="45ff6-167">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)
-   [<span data-ttu-id="45ff6-168">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="45ff6-168">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
-   [<span data-ttu-id="45ff6-169">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="45ff6-169">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)
-   <span data-ttu-id="45ff6-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="45ff6-170">**SplitButton**</span></span>
-   [<span data-ttu-id="45ff6-171">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="45ff6-171">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)
-   [<span data-ttu-id="45ff6-172">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="45ff6-172">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)

<span data-ttu-id="45ff6-173">Diese Steuerelemente werden als untergeordnete Elemente eines einzelnen [**SplitButton.MenuGroups-Standardelements**](windowsribbon-element-splitbutton-menugroups.md) behandelt.</span><span class="sxs-lookup"><span data-stu-id="45ff6-173">These controls are treated as child elements of a single default [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="45ff6-174">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45ff6-174">Examples</span></span>

<span data-ttu-id="45ff6-175">Im folgenden Beispiel wird das grundlegende Markup für die [Split-Schaltfläche veranschaulicht.](windowsribbon-controls-splitbutton.md)</span><span class="sxs-lookup"><span data-stu-id="45ff6-175">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="45ff6-176">In diesem Codeabschnitt werden die **Deklarationen des SplitButton-Befehls** mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) gezeigt, die als übergeordneter Container für das **SplitButton-Element** fungiert.</span><span class="sxs-lookup"><span data-stu-id="45ff6-176">This section of code shows the **SplitButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


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



<span data-ttu-id="45ff6-177">In diesem Codeabschnitt werden die **SplitButton-Steuerelementdeklarationen** gezeigt.</span><span class="sxs-lookup"><span data-stu-id="45ff6-177">This section of code shows the **SplitButton** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="45ff6-178">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="45ff6-178">Element information</span></span>

- <span data-ttu-id="45ff6-179">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="45ff6-179">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="45ff6-180">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="45ff6-180">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="45ff6-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45ff6-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45ff6-182">Steuerelement "Schaltfläche teilen"</span><span class="sxs-lookup"><span data-stu-id="45ff6-182">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> <dt>

[<span data-ttu-id="45ff6-183">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="45ff6-183">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

