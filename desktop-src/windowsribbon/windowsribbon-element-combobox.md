---
title: ComboBox-Element
description: Stellt ein Kombinationsfeld-Steuerelement dar.
ms.assetid: d796e26b-44c2-4e11-b1a5-2ede5bcff676
keywords:
- ComboBox-Element Windows-Menüband
topic_type:
- apiref
api_name:
- ComboBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60ad8866b655be587e0c3d0f123d8bc59b6b8a21
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443581"
---
# <a name="combobox-element"></a><span data-ttu-id="46b5d-104">ComboBox-Element</span><span class="sxs-lookup"><span data-stu-id="46b5d-104">ComboBox element</span></span>

<span data-ttu-id="46b5d-105">Stellt ein [Kombinationsfeld-Steuerelement](windowsribbon-controls-combobox.md) dar.</span><span class="sxs-lookup"><span data-stu-id="46b5d-105">Represents a [Combo Box](windowsribbon-controls-combobox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="46b5d-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="46b5d-106">Usage</span></span>

``` syntax
<ComboBox
  CommandName = "xs:positiveInteger or xs:string"
  IsEditable = "Boolean"
  ResizeType = "ComboBoxResizeType"
  IsAutoCompleteEnabled = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="46b5d-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="46b5d-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="46b5d-108">attribute</span><span class="sxs-lookup"><span data-stu-id="46b5d-108">Attribute</span></span></th>
<th><span data-ttu-id="46b5d-109">Typ</span><span class="sxs-lookup"><span data-stu-id="46b5d-109">Type</span></span></th>
<th><span data-ttu-id="46b5d-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="46b5d-110">Required</span></span></th>
<th><span data-ttu-id="46b5d-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46b5d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46b5d-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="46b5d-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="46b5d-113">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="46b5d-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="46b5d-114">Nein</span><span class="sxs-lookup"><span data-stu-id="46b5d-114">No</span></span><br/></td>
<td><span data-ttu-id="46b5d-115">Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="46b5d-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="46b5d-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="46b5d-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="46b5d-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999 einschließlich oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="46b5d-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="46b5d-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="46b5d-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="46b5d-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="46b5d-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46b5d-120"><strong>IsAutoCompleteEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="46b5d-120"><strong>IsAutoCompleteEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="46b5d-121">Boolesch</span><span class="sxs-lookup"><span data-stu-id="46b5d-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="46b5d-122">Nein</span><span class="sxs-lookup"><span data-stu-id="46b5d-122">No</span></span><br/></td>
<td><span data-ttu-id="46b5d-123">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="46b5d-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="46b5d-124">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="46b5d-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="46b5d-125">Standard.</span><span class="sxs-lookup"><span data-stu-id="46b5d-125">Default.</span></span> <br/> </dd> <span data-ttu-id="46b5d-126"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="46b5d-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46b5d-127"><strong>Iseditable</strong></span><span class="sxs-lookup"><span data-stu-id="46b5d-127"><strong>IsEditable</strong></span></span><br/></td>
<td><span data-ttu-id="46b5d-128">Boolesch</span><span class="sxs-lookup"><span data-stu-id="46b5d-128">Boolean</span></span><br/></td>
<td><span data-ttu-id="46b5d-129">Nein</span><span class="sxs-lookup"><span data-stu-id="46b5d-129">No</span></span><br/></td>
<td><span data-ttu-id="46b5d-130">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="46b5d-130">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="46b5d-131">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="46b5d-131">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="46b5d-132">Standard.</span><span class="sxs-lookup"><span data-stu-id="46b5d-132">Default.</span></span> <br/> </dd> <span data-ttu-id="46b5d-133"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="46b5d-133"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="46b5d-134"><strong>ResizeType</strong></span><span class="sxs-lookup"><span data-stu-id="46b5d-134"><strong>ResizeType</strong></span></span><br/></td>
<td><span data-ttu-id="46b5d-135">ComboBoxResizeType</span><span class="sxs-lookup"><span data-stu-id="46b5d-135">ComboBoxResizeType</span></span><br/></td>
<td><span data-ttu-id="46b5d-136">Nein</span><span class="sxs-lookup"><span data-stu-id="46b5d-136">No</span></span><br/></td>
<td><span data-ttu-id="46b5d-137"><dt><span></span><span></span><strong></strong> (NoResize)</span><span class="sxs-lookup"><span data-stu-id="46b5d-137"><dt><span></span><span></span><strong></strong> (NoResize)</span></span><br/> </dt> <dd> <span data-ttu-id="46b5d-138">Standard.</span><span class="sxs-lookup"><span data-stu-id="46b5d-138">Default.</span></span> <br/> </dd> <span data-ttu-id="46b5d-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span><span class="sxs-lookup"><span data-stu-id="46b5d-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="46b5d-140">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46b5d-140">Child elements</span></span>

<span data-ttu-id="46b5d-141">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="46b5d-141">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="46b5d-142">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46b5d-142">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="46b5d-143">Element</span><span class="sxs-lookup"><span data-stu-id="46b5d-143">Element</span></span></th>
<th><span data-ttu-id="46b5d-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="46b5d-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="46b5d-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="46b5d-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="46b5d-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="46b5d-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46b5d-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="46b5d-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="46b5d-148"><a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a></span><span class="sxs-lookup"><span data-stu-id="46b5d-148"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="46b5d-149"><a href="windowsribbon-element-menugroup.md"><strong>Menugroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="46b5d-149"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="46b5d-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="46b5d-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="46b5d-151">Windows 8 und neuer.</span><span class="sxs-lookup"><span data-stu-id="46b5d-151">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="46b5d-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="46b5d-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="46b5d-153">Hinweise</span><span class="sxs-lookup"><span data-stu-id="46b5d-153">Remarks</span></span>

<span data-ttu-id="46b5d-154">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="46b5d-154">Optional.</span></span>

<span data-ttu-id="46b5d-155">Kann ein oder mehrere Male für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) [**DropDownButton-,**](windowsribbon-element-dropdownbutton.md) [**DropDownGallery-,**](windowsribbon-element-dropdowngallery.md) [**Group-, MenuGroup-**](windowsribbon-element-menugroup.md)oder [**SplitButtonGallery-Element**](windowsribbon-element-splitbuttongallery.md) auftreten. [](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="46b5d-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="46b5d-156">Da es sich bei **ComboBox** ausschließlich um einen Elementkatalog handelt, werden keine Befehlselemente unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46b5d-156">Because the **ComboBox** is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="46b5d-157">Es ist auch das einzige Katalogsteuerelement, das keinen Befehlsbereich unterstützt (eine Sammlung von Befehlen, die im Markup deklariert und am unteren Rand eines Elementkatalogs oder Befehlskatalogs aufgeführt sind).</span><span class="sxs-lookup"><span data-stu-id="46b5d-157">It is also the only gallery control that does not support a Command Space (a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery).</span></span> <span data-ttu-id="46b5d-158">Weitere Informationen finden Sie unter [Arbeiten mit Katalogen.](ribbon-controls-galleries.md)</span><span class="sxs-lookup"><span data-stu-id="46b5d-158">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="46b5d-159">Der folgende Screenshot veranschaulicht ein [Menüband-Kombinationsfeld-Steuerelement](windowsribbon-controls-combobox.md) von Windows Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="46b5d-159">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![Screenshot eines Combobox-Steuerelements im Microsoft Paint-Menüband.](images/controls/combobox.png)

## <a name="examples"></a><span data-ttu-id="46b5d-161">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46b5d-161">Examples</span></span>

<span data-ttu-id="46b5d-162">In den folgenden Beispielen wird das grundlegende Markup für **comboBox** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="46b5d-162">The following examples demonstrate the basic markup for the **ComboBox**.</span></span>

<span data-ttu-id="46b5d-163">Dieser Codeabschnitt zeigt die **ComboBox-Befehlsdeklarationen** mit einer zugeordneten [**Gruppe,**](windowsribbon-element-group.md) die als übergeordneter Container für das **ComboBox-Element** fungiert.</span><span class="sxs-lookup"><span data-stu-id="46b5d-163">This section of code shows the **ComboBox** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **ComboBox** element.</span></span>


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```



<span data-ttu-id="46b5d-164">Dieser Codeabschnitt zeigt die **ComboBox-Steuerelementdeklarationen.**</span><span class="sxs-lookup"><span data-stu-id="46b5d-164">This section of code shows the **ComboBox** control declarations.</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="46b5d-165">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="46b5d-165">Element information</span></span>

* <span data-ttu-id="46b5d-166">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="46b5d-166">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="46b5d-167">**Kann leer sein:** Ja</span><span class="sxs-lookup"><span data-stu-id="46b5d-167">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="46b5d-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46b5d-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46b5d-169">Kombinationsfeld-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="46b5d-169">Combo Box control</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="46b5d-170">Katalogbeispiel</span><span class="sxs-lookup"><span data-stu-id="46b5d-170">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





