---
title: ComboBox-Element
description: Stellt ein Kombinations Feld-Steuerelement dar.
ms.assetid: d796e26b-44c2-4e11-b1a5-2ede5bcff676
keywords:
- Windows-Menüband für ComboBox-Element
topic_type:
- apiref
api_name:
- ComboBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5bdcc95c64c2bd60df4f2f53d3bd3699c0a7ee65
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "106340680"
---
# <a name="combobox-element"></a><span data-ttu-id="48350-104">ComboBox-Element</span><span class="sxs-lookup"><span data-stu-id="48350-104">ComboBox element</span></span>

<span data-ttu-id="48350-105">Stellt ein Kombinations [Feld](windowsribbon-controls-combobox.md) -Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="48350-105">Represents a [Combo Box](windowsribbon-controls-combobox.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="48350-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="48350-106">Usage</span></span>

``` syntax
<ComboBox
  CommandName = "xs:positiveInteger or xs:string"
  IsEditable = "Boolean"
  ResizeType = "ComboBoxResizeType"
  IsAutoCompleteEnabled = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="48350-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="48350-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48350-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="48350-108">Attribute</span></span></th>
<th><span data-ttu-id="48350-109">type</span><span class="sxs-lookup"><span data-stu-id="48350-109">Type</span></span></th>
<th><span data-ttu-id="48350-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="48350-110">Required</span></span></th>
<th><span data-ttu-id="48350-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48350-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48350-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="48350-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="48350-113">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="48350-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="48350-114">Nein</span><span class="sxs-lookup"><span data-stu-id="48350-114">No</span></span><br/></td>
<td><span data-ttu-id="48350-115">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="48350-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="48350-116">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="48350-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="48350-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="48350-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="48350-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="48350-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="48350-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="48350-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48350-120"><strong>Isautocompleteaktivierte</strong></span><span class="sxs-lookup"><span data-stu-id="48350-120"><strong>IsAutoCompleteEnabled</strong></span></span><br/></td>
<td><span data-ttu-id="48350-121">Boolesch</span><span class="sxs-lookup"><span data-stu-id="48350-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="48350-122">Nein</span><span class="sxs-lookup"><span data-stu-id="48350-122">No</span></span><br/></td>
<td><span data-ttu-id="48350-123">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="48350-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="48350-124">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="48350-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="48350-125">Standard.</span><span class="sxs-lookup"><span data-stu-id="48350-125">Default.</span></span> <br/> </dd> <span data-ttu-id="48350-126"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="48350-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48350-127"><strong>IsEditable</strong></span><span class="sxs-lookup"><span data-stu-id="48350-127"><strong>IsEditable</strong></span></span><br/></td>
<td><span data-ttu-id="48350-128">Boolesch</span><span class="sxs-lookup"><span data-stu-id="48350-128">Boolean</span></span><br/></td>
<td><span data-ttu-id="48350-129">Nein</span><span class="sxs-lookup"><span data-stu-id="48350-129">No</span></span><br/></td>
<td><span data-ttu-id="48350-130">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="48350-130">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="48350-131">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="48350-131">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="48350-132">Standard.</span><span class="sxs-lookup"><span data-stu-id="48350-132">Default.</span></span> <br/> </dd> <span data-ttu-id="48350-133"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="48350-133"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48350-134"><strong>Resizetype</strong></span><span class="sxs-lookup"><span data-stu-id="48350-134"><strong>ResizeType</strong></span></span><br/></td>
<td><span data-ttu-id="48350-135">Comboboxresizetype</span><span class="sxs-lookup"><span data-stu-id="48350-135">ComboBoxResizeType</span></span><br/></td>
<td><span data-ttu-id="48350-136">Nein</span><span class="sxs-lookup"><span data-stu-id="48350-136">No</span></span><br/></td>
<td><span data-ttu-id="48350-137"><dt><span></span><span></span><strong></strong> (NORESIZE)</span><span class="sxs-lookup"><span data-stu-id="48350-137"><dt><span></span><span></span><strong></strong> (NoResize)</span></span><br/> </dt> <dd> <span data-ttu-id="48350-138">Standard.</span><span class="sxs-lookup"><span data-stu-id="48350-138">Default.</span></span> <br/> </dd> <span data-ttu-id="48350-139"><dt><span></span><span></span><strong></strong> (Verticalresize)</span><span class="sxs-lookup"><span data-stu-id="48350-139"><dt><span></span><span></span><strong></strong> (VerticalResize)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="48350-140">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48350-140">Child elements</span></span>

<span data-ttu-id="48350-141">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="48350-141">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="48350-142">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="48350-142">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48350-143">Element</span><span class="sxs-lookup"><span data-stu-id="48350-143">Element</span></span></th>
<th><span data-ttu-id="48350-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48350-144">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48350-145"><a href="windowsribbon-element-controlgroup.md"><strong>Controlgroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="48350-145"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="48350-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="48350-146"><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="48350-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>Dropdown Gallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="48350-147"><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="48350-148"><a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a></span><span class="sxs-lookup"><span data-stu-id="48350-148"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="48350-149"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="48350-149"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="48350-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>Quickaccesstoolbar. ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="48350-150"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="48350-151">Windows 8 und höher.</span><span class="sxs-lookup"><span data-stu-id="48350-151">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48350-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>Splitbuttongallery</strong></a></span><span class="sxs-lookup"><span data-stu-id="48350-152"><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="48350-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48350-153">Remarks</span></span>

<span data-ttu-id="48350-154">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="48350-154">Optional.</span></span>

<span data-ttu-id="48350-155">Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, [**DropDownButton**](windowsribbon-element-dropdownbutton.md)-, [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)-, [**Group**](windowsribbon-element-group.md)-, [**MenuGroup**](windowsribbon-element-menugroup.md)-oder [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="48350-155">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="48350-156">Da es sich bei der **ComboBox** ausschließlich um einen Element Katalog handelt, werden Befehls Elemente nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="48350-156">Because the **ComboBox** is exclusively an item gallery, it does not support Command items.</span></span> <span data-ttu-id="48350-157">Es ist auch das einzige Katalog Steuerelement, das keinen Befehlsbereich unterstützt (eine Auflistung von Befehlen, die im Markup deklariert und im unteren Bereich eines Element Katalogs oder einer Befehls Galerie aufgelistet sind).</span><span class="sxs-lookup"><span data-stu-id="48350-157">It is also the only gallery control that does not support a Command Space (a collection of Commands that are declared in markup and listed at the bottom of an item gallery or Command gallery).</span></span> <span data-ttu-id="48350-158">Weitere Informationen finden Sie unter [Arbeiten mit Galerien](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="48350-158">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="48350-159">Der folgende Screenshot veranschaulicht ein Menüband-Kombinations [Feld](windowsribbon-controls-combobox.md) -Steuerelement von Windows Live Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="48350-159">The following screen shot illustrates a Ribbon [Combo Box](windowsribbon-controls-combobox.md) control from Windows Live Movie Maker.</span></span>

![Screenshot eines ComboBox-Steuer Elements im Microsoft Paint-Menüband.](images/controls/combobox.png)

## <a name="examples"></a><span data-ttu-id="48350-161">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48350-161">Examples</span></span>

<span data-ttu-id="48350-162">In den folgenden Beispielen wird das grundlegende Markup für das Kombinations **Feld** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="48350-162">The following examples demonstrate the basic markup for the **ComboBox**.</span></span>

<span data-ttu-id="48350-163">Dieser Code Abschnitt zeigt die **ComboBox** -Befehls Deklarationen mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **ComboBox** -Element fungiert.</span><span class="sxs-lookup"><span data-stu-id="48350-163">This section of code shows the **ComboBox** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **ComboBox** element.</span></span>


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



<span data-ttu-id="48350-164">Dieser Code Abschnitt zeigt die **ComboBox** -Steuerelement Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="48350-164">This section of code shows the **ComboBox** control declarations.</span></span>


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="48350-165">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="48350-165">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="48350-166">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="48350-166">Minimum supported system</span></span><br/> | <span data-ttu-id="48350-167">Windows 7</span><span class="sxs-lookup"><span data-stu-id="48350-167">Windows 7</span></span> |
| <span data-ttu-id="48350-168">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="48350-168">Can be empty</span></span>                        | <span data-ttu-id="48350-169">Ja</span><span class="sxs-lookup"><span data-stu-id="48350-169">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="48350-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48350-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48350-171">Kombinationsfeld-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="48350-171">Combo Box control</span></span>](windowsribbon-controls-combobox.md)
</dt> <dt>

[<span data-ttu-id="48350-172">Galerie Beispiel</span><span class="sxs-lookup"><span data-stu-id="48350-172">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





