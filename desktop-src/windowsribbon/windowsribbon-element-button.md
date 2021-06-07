---
title: Button-Element (Windows Ribbon Framework)
description: Stellt ein Schaltflächen-Steuerelement dar.
ms.assetid: a17d4dd8-9b0d-4b4a-93f4-f2a8c008fc58
keywords:
- Schaltflächenelement Windows-Menüband
topic_type:
- apiref
api_name:
- Button
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40236b60a9fe9c72dd35d67fcf7c98bc188938af
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443571"
---
# <a name="button-element"></a><span data-ttu-id="ed814-104">Button-Element</span><span class="sxs-lookup"><span data-stu-id="ed814-104">Button element</span></span>

<span data-ttu-id="ed814-105">Stellt ein [Schaltflächen-Steuerelement](windowsribbon-controls-button.md) dar.</span><span class="sxs-lookup"><span data-stu-id="ed814-105">Represents a [Button](windowsribbon-controls-button.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="ed814-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="ed814-106">Usage</span></span>

``` syntax
<Button
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="ed814-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="ed814-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed814-108">attribute</span><span class="sxs-lookup"><span data-stu-id="ed814-108">Attribute</span></span></th>
<th><span data-ttu-id="ed814-109">Typ</span><span class="sxs-lookup"><span data-stu-id="ed814-109">Type</span></span></th>
<th><span data-ttu-id="ed814-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ed814-110">Required</span></span></th>
<th><span data-ttu-id="ed814-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed814-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ed814-112"><strong>ApplicationDefaults.IsChecked</strong></span><span class="sxs-lookup"><span data-stu-id="ed814-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="ed814-113">Boolesch</span><span class="sxs-lookup"><span data-stu-id="ed814-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="ed814-114">Nein</span><span class="sxs-lookup"><span data-stu-id="ed814-114">No</span></span><br/></td>
<td><span data-ttu-id="ed814-115">Dieses Attribut ist nur gültig, wenn <strong>das Button-Element</strong> ein untergeordnetes Element von <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults ist.</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed814-115">This attribute is valid only when the <strong>Button</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="ed814-116">Auf einen der folgenden Werte beschränkt:</span><span class="sxs-lookup"><span data-stu-id="ed814-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="ed814-117">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="ed814-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="ed814-118">Standard.</span><span class="sxs-lookup"><span data-stu-id="ed814-118">Default.</span></span> <br/> </dd> <span data-ttu-id="ed814-119"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="ed814-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed814-120"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="ed814-120"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="ed814-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="ed814-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="ed814-122">Nein</span><span class="sxs-lookup"><span data-stu-id="ed814-122">No</span></span><br/></td>
<td><span data-ttu-id="ed814-123">Nur gültig, <a href="windowsribbon-element-menugroup.md"><strong>wenn MenuGroup</strong></a> das übergeordnete Element ist.</span><span class="sxs-lookup"><span data-stu-id="ed814-123">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="ed814-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="ed814-124">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ed814-125">Eine Zeichenfolge, die eine durch Komma getrennte Liste von ganzen Zahlen zwischen 0 und 31 enthält.</span><span class="sxs-lookup"><span data-stu-id="ed814-125">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="ed814-126">Leerzeichen sind gültig und werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="ed814-126">White space is valid and ignored.</span></span><br/> <span data-ttu-id="ed814-127">Maximale Länge: 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ed814-127">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ed814-128"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="ed814-128"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="ed814-129">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="ed814-129">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="ed814-130">Nein</span><span class="sxs-lookup"><span data-stu-id="ed814-130">No</span></span><br/></td>
<td><span data-ttu-id="ed814-131">Ordnet das Element einem Befehl <a href="windowsribbon-element-command.md"><strong>zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed814-131">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="ed814-132">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="ed814-132">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ed814-133">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="ed814-133">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="ed814-134">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ed814-134">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="ed814-135">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ed814-135">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="ed814-136">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ed814-136">Child elements</span></span>

<span data-ttu-id="ed814-137">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="ed814-137">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ed814-138">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ed814-138">Parent elements</span></span>



| <span data-ttu-id="ed814-139">Element</span><span class="sxs-lookup"><span data-stu-id="ed814-139">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed814-140">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="ed814-140">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="ed814-141">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="ed814-141">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="ed814-142">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="ed814-142">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="ed814-143">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="ed814-143">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="ed814-144">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="ed814-144">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="ed814-145">**QuickAccessToolbar.ApplicationDefaults**</span><span class="sxs-lookup"><span data-stu-id="ed814-145">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="ed814-146">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="ed814-146">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="ed814-147">**SplitButton.ButtonItem**</span><span class="sxs-lookup"><span data-stu-id="ed814-147">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="ed814-148">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="ed814-148">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="ed814-149">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ed814-149">Remarks</span></span>

<span data-ttu-id="ed814-150">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ed814-150">Optional.</span></span>

<span data-ttu-id="ed814-151">Kann für jedes [**SplitButton.ButtonItem-Element nur einmal auftreten.**](windowsribbon-element-splitbutton-buttonitem.md)</span><span class="sxs-lookup"><span data-stu-id="ed814-151">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="ed814-152">Kann ein oder mehrere Male für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) [**DropDownButton-,**](windowsribbon-element-dropdownbutton.md) [**DropDownGallery-,**](windowsribbon-element-dropdowngallery.md) [**Group-,**](windowsribbon-element-group.md) [**MenuGroup-,**](windowsribbon-element-menugroup.md) [**QuickAccessToolbar.ApplicationDefaults-,**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) [**SplitButton-**](windowsribbon-element-splitbutton.md)oder [**SplitButtonGallery-Element**](windowsribbon-element-splitbuttongallery.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="ed814-152">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="ed814-153">**Die** Schaltfläche [unterstützt Anwendungsmodi,](ribbon-applicationmodes.md) wenn sie in der linken Spalte des Anwendungsmenüs gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="ed814-153">**Button** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

## <a name="examples"></a><span data-ttu-id="ed814-154">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed814-154">Examples</span></span>

<span data-ttu-id="ed814-155">Im folgenden Beispiel wird das grundlegende Markup für die **Schaltfläche veranschaulicht.**</span><span class="sxs-lookup"><span data-stu-id="ed814-155">The following example demonstrates the basic markup for the **Button**.</span></span>

<span data-ttu-id="ed814-156">In diesem Codeabschnitt werden die **Button** Command-Deklarationen mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) angezeigt, die als übergeordneter Container für das **Button-Element** fungiert.</span><span class="sxs-lookup"><span data-stu-id="ed814-156">This section of code shows the **Button** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **Button** element.</span></span>


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



<span data-ttu-id="ed814-157">In diesem Codeabschnitt werden die **Button-Steuerelementdeklarationen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed814-157">This section of code shows the **Button** control declarations.</span></span>


```XML
<Group CommandName="cmdButtonGroup"
       SizeDefinition="ThreeButtons">
  <Button CommandName="cmdButton1"></Button>
  <Button CommandName="cmdButton2"></Button>
  <Button CommandName="cmdButton3"></Button>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="ed814-158">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ed814-158">Element information</span></span>

* <span data-ttu-id="ed814-159">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="ed814-159">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="ed814-160">**Kann leer sein:** Ja</span><span class="sxs-lookup"><span data-stu-id="ed814-160">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="ed814-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed814-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed814-162">Schaltflächen-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ed814-162">Button control</span></span>](windowsribbon-controls-button.md)
</dt> <dt>

[<span data-ttu-id="ed814-163">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="ed814-163">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

