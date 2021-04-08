---
title: DropDownButton-Element
description: Stellt ein Standard-Drop-Down Schaltflächen-Steuerelement dar.
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- Windows-Menüband für DropDownButton-Element
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 98af363aeb70a61def04eaee0ad13ff60e6e7640
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729224"
---
# <a name="dropdownbutton-element"></a><span data-ttu-id="33d08-104">DropDownButton-Element</span><span class="sxs-lookup"><span data-stu-id="33d08-104">DropDownButton element</span></span>

<span data-ttu-id="33d08-105">Stellt ein Standard [-Dropdown-Schalt](windowsribbon-controls-dropdownbutton.md) Flächen-Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="33d08-105">Represents a standard [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="33d08-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="33d08-106">Usage</span></span>

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
```

## <a name="attributes"></a><span data-ttu-id="33d08-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="33d08-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="33d08-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="33d08-108">Attribute</span></span></th>
<th><span data-ttu-id="33d08-109">type</span><span class="sxs-lookup"><span data-stu-id="33d08-109">Type</span></span></th>
<th><span data-ttu-id="33d08-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="33d08-110">Required</span></span></th>
<th><span data-ttu-id="33d08-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33d08-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33d08-112"><strong>Applicationmodes</strong></span><span class="sxs-lookup"><span data-stu-id="33d08-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="33d08-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="33d08-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="33d08-114">Nein</span><span class="sxs-lookup"><span data-stu-id="33d08-114">No</span></span><br/></td>
<td><span data-ttu-id="33d08-115">Nur gültig, wenn <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> das übergeordnete Element ist.</span><span class="sxs-lookup"><span data-stu-id="33d08-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="33d08-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="33d08-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="33d08-117">Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste mit ganzen Zahlen zwischen 0 und 31 enthält.</span><span class="sxs-lookup"><span data-stu-id="33d08-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="33d08-118">Leerraum ist gültig und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="33d08-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="33d08-119">Maximale Länge: 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="33d08-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33d08-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="33d08-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="33d08-121">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="33d08-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="33d08-122">Nein</span><span class="sxs-lookup"><span data-stu-id="33d08-122">No</span></span><br/></td>
<td><span data-ttu-id="33d08-123">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="33d08-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="33d08-124">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="33d08-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="33d08-125">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="33d08-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="33d08-126">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="33d08-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="33d08-127">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="33d08-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="33d08-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33d08-128">Child elements</span></span>



| <span data-ttu-id="33d08-129">Element</span><span class="sxs-lookup"><span data-stu-id="33d08-129">Element</span></span>                                                                             | <span data-ttu-id="33d08-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33d08-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="33d08-131">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="33d08-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="33d08-132">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="33d08-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="33d08-133">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="33d08-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="33d08-134">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="33d08-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="33d08-135">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="33d08-135">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="33d08-136">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="33d08-136">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="33d08-137">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="33d08-137">**DropDownButton**</span></span><br/>                                                       | <span data-ttu-id="33d08-138">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="33d08-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="33d08-139">**Dropdowncolorpicker**</span><span class="sxs-lookup"><span data-stu-id="33d08-139">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="33d08-140">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="33d08-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="33d08-141">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="33d08-141">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="33d08-142">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="33d08-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="33d08-143">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="33d08-143">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                     | <span data-ttu-id="33d08-144">Muss mindestens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="33d08-144">Must occur at least once</span></span><br/> <br/>    |
| [<span data-ttu-id="33d08-145">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="33d08-145">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="33d08-146">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="33d08-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="33d08-147">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="33d08-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="33d08-148">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="33d08-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="33d08-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="33d08-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="33d08-150">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="33d08-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="33d08-151">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="33d08-151">Parent elements</span></span>



| <span data-ttu-id="33d08-152">Element</span><span class="sxs-lookup"><span data-stu-id="33d08-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="33d08-153">**Controlgroup**</span><span class="sxs-lookup"><span data-stu-id="33d08-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| <span data-ttu-id="33d08-154">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="33d08-154">**DropDownButton**</span></span><br/>                                                     |
| [<span data-ttu-id="33d08-155">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="33d08-155">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="33d08-156">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="33d08-156">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="33d08-157">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="33d08-157">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="33d08-158">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="33d08-158">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="33d08-159">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="33d08-159">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="33d08-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33d08-160">Remarks</span></span>

<span data-ttu-id="33d08-161">Optional oder erforderlich, abhängig vom übergeordneten Element.</span><span class="sxs-lookup"><span data-stu-id="33d08-161">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="33d08-162">Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, **DropDownButton**-, [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)-, [**Group**](windowsribbon-element-group.md)-, [**MenuGroup**](windowsribbon-element-menugroup.md)-, [**SplitButton**](windowsribbon-element-splitbutton.md)-oder [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="33d08-162">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="33d08-163">**DropDownButton** unterstützt [Anwendungsmodi](ribbon-applicationmodes.md) , wenn Sie in der linken Spalte des Anwendungs Menüs gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="33d08-163">**DropDownButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="33d08-164">[**Dropdowngallery**](windowsribbon-element-dropdowngallery.md) und [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) sind keine gültigen untergeordneten Elemente von **DropDownButton** , wenn **DropDownButton** ein Nachfolger von [**applicationmenu**](windowsribbon-element-applicationmenu.md)ist.</span><span class="sxs-lookup"><span data-stu-id="33d08-164">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of **DropDownButton** when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

## <a name="examples"></a><span data-ttu-id="33d08-165">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33d08-165">Examples</span></span>

<span data-ttu-id="33d08-166">Im folgenden Beispiel wird das grundlegende Markup für **DropDownButton** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="33d08-166">The following example demonstrates the basic markup for the **DropDownButton**.</span></span>

<span data-ttu-id="33d08-167">Dieser Code Abschnitt zeigt die **Dropdown Button** -Befehls Deklarationen mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **Dropdown Button** -Element fungiert.</span><span class="sxs-lookup"><span data-stu-id="33d08-167">This section of code shows the **DropDownButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **DropDownButton** element.</span></span>


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



<span data-ttu-id="33d08-168">In diesem Code Abschnitt werden die Deklarationen des **Dropdown Button** -Steuer Elements angezeigt.</span><span class="sxs-lookup"><span data-stu-id="33d08-168">This section of code shows the **DropDownButton** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="33d08-169">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="33d08-169">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="33d08-170">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="33d08-170">Minimum supported system</span></span><br/> | <span data-ttu-id="33d08-171">Windows 7</span><span class="sxs-lookup"><span data-stu-id="33d08-171">Windows 7</span></span> |
| <span data-ttu-id="33d08-172">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="33d08-172">Can be empty</span></span>                        | <span data-ttu-id="33d08-173">Nein</span><span class="sxs-lookup"><span data-stu-id="33d08-173">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="33d08-174">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="33d08-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33d08-175">Dropdown-Schaltflächen-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="33d08-175">Drop-Down Button control</span></span>](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[<span data-ttu-id="33d08-176">**Setmodes**</span><span class="sxs-lookup"><span data-stu-id="33d08-176">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

