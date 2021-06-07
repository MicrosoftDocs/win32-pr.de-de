---
title: MenuGroup-Element
description: Stellt einen Container von Steuerelementen dar, die in einem Katalog, einem Menü oder einer Symbolleiste angezeigt werden sollen.
ms.assetid: 75da63fe-dd9e-46af-8f13-a8d8e7575641
keywords:
- MenuGroup-Element Windows-Menüband
topic_type:
- apiref
api_name:
- MenuGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95cbda43fe2f652888a7b84539752b5d671868c3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442851"
---
# <a name="menugroup-element"></a><span data-ttu-id="f197d-104">MenuGroup-Element</span><span class="sxs-lookup"><span data-stu-id="f197d-104">MenuGroup element</span></span>

<span data-ttu-id="f197d-105">Stellt einen Container von Steuerelementen dar, die in einem Katalog, einem Menü oder einer Symbolleiste angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f197d-105">Represents a container of controls to display in a gallery, menu, or toolbar.</span></span>

## <a name="usage"></a><span data-ttu-id="f197d-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="f197d-106">Usage</span></span>

``` syntax
<MenuGroup
  Class = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</MenuGroup>
```

## <a name="attributes"></a><span data-ttu-id="f197d-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="f197d-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f197d-108">attribute</span><span class="sxs-lookup"><span data-stu-id="f197d-108">Attribute</span></span></th>
<th><span data-ttu-id="f197d-109">Typ</span><span class="sxs-lookup"><span data-stu-id="f197d-109">Type</span></span></th>
<th><span data-ttu-id="f197d-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f197d-110">Required</span></span></th>
<th><span data-ttu-id="f197d-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f197d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f197d-112"><strong>Klasse</strong></span><span class="sxs-lookup"><span data-stu-id="f197d-112"><strong>Class</strong></span></span><br/></td>
<td><span data-ttu-id="f197d-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="f197d-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="f197d-114">Nein</span><span class="sxs-lookup"><span data-stu-id="f197d-114">No</span></span><br/></td>
<td><span data-ttu-id="f197d-115">Gibt die Größe und den Layoutstil für Elemente in der Menübenutzeroberfläche an.</span><span class="sxs-lookup"><span data-stu-id="f197d-115">Specifies the size and layout style for elements in the menu UI.</span></span><br/> <span data-ttu-id="f197d-116">Eine Imageressource kann in zwei Größen (groß und klein) bereitgestellt und dem -Element im Markup mithilfe der <a href="windowsribbon-element-command-largeimages.md"><strong>Command.LargeImages-</strong></a> und <a href="windowsribbon-element-command-smallimages.md"><strong>Command.SmallImages-Eigenschaftselemente</strong></a> zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f197d-116">An image resource can be supplied in two sizes (large and small) and associated with the element in markup using the <a href="windowsribbon-element-command-largeimages.md"><strong>Command.LargeImages</strong></a> and <a href="windowsribbon-element-command-smallimages.md"><strong>Command.SmallImages</strong></a> property elements.</span></span> <span data-ttu-id="f197d-117">Wenn nur ein Image bereitgestellt wird, wird die Größe des Images nach Bedarf vom Framework geändert.</span><span class="sxs-lookup"><span data-stu-id="f197d-117">If only one image is supplied, the framework resizes it as necessary.</span></span><br/> <span data-ttu-id="f197d-118">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="f197d-118">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="f197d-119">
<dt><span></span><span></span><strong></strong> (StandardItems)</span><span class="sxs-lookup"><span data-stu-id="f197d-119">
<dt><span></span><span></span><strong></strong> (StandardItems)</span></span><br/> </dt> <dd> <span data-ttu-id="f197d-120">Standard.</span><span class="sxs-lookup"><span data-stu-id="f197d-120">Default.</span></span> <br/> <span data-ttu-id="f197d-121">Stil: kleines Bild und textfreies Format.</span><span class="sxs-lookup"><span data-stu-id="f197d-121">Style: small image and de-emphasized text.</span></span><br/><img src="images/markup/menugroup-standarditems.png" alt="Screen shot of a StandardItems button." /></dd> <span data-ttu-id="f197d-122"><dt><span></span><span></span><strong></strong> (MajorItems)</span><span class="sxs-lookup"><span data-stu-id="f197d-122"><dt><span></span><span></span><strong></strong> (MajorItems)</span></span><br/> </dt> <dd> <span data-ttu-id="f197d-123">Stil: großes Bild und fetter Text.</span><span class="sxs-lookup"><span data-stu-id="f197d-123">Style: large image and bold text.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f197d-124">Wenn <strong>MenuGroup</strong> ein untergeordnetes Element von <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>ist, wird das <em>Class-Attribut</em> ignoriert, und ein Stil von <code>MajorItems</code> wird vom Framework erzwungen.</span><span class="sxs-lookup"><span data-stu-id="f197d-124">If <strong>MenuGroup</strong> is a child of <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>, the <em>Class</em> attribute is ignored and a style of <code>MajorItems</code> is enforced by the framework.</span></span>
</blockquote>
<br/> <img src="images/markup/menugroup-majoritems.png" alt="Screen shot of a MajorItems button." /></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f197d-125"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="f197d-125"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="f197d-126">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="f197d-126">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="f197d-127">Nein</span><span class="sxs-lookup"><span data-stu-id="f197d-127">No</span></span><br/></td>
<td><span data-ttu-id="f197d-128">Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="f197d-128">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="f197d-129">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="f197d-129">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="f197d-130">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999 einschließlich oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="f197d-130">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="f197d-131">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="f197d-131">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="f197d-132">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="f197d-132">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="f197d-133">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f197d-133">Child elements</span></span>



| <span data-ttu-id="f197d-134">Element</span><span class="sxs-lookup"><span data-stu-id="f197d-134">Element</span></span>                                                                             | <span data-ttu-id="f197d-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f197d-135">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="f197d-136">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="f197d-136">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="f197d-137">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="f197d-137">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f197d-138">**Checkbox**</span><span class="sxs-lookup"><span data-stu-id="f197d-138">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="f197d-139">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="f197d-139">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f197d-140">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="f197d-140">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="f197d-141">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="f197d-141">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f197d-142">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="f197d-142">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="f197d-143">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="f197d-143">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f197d-144">**DropDownColorPicker**</span><span class="sxs-lookup"><span data-stu-id="f197d-144">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="f197d-145">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="f197d-145">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f197d-146">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="f197d-146">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="f197d-147">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="f197d-147">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f197d-148">**FontControl**</span><span class="sxs-lookup"><span data-stu-id="f197d-148">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="f197d-149">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="f197d-149">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="f197d-150">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="f197d-150">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="f197d-151">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="f197d-151">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f197d-152">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="f197d-152">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="f197d-153">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="f197d-153">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="f197d-154">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="f197d-154">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="f197d-155">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="f197d-155">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="f197d-156">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f197d-156">Parent elements</span></span>



| <span data-ttu-id="f197d-157">Element</span><span class="sxs-lookup"><span data-stu-id="f197d-157">Element</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f197d-158">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="f197d-158">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/>                             |
| [<span data-ttu-id="f197d-159">**ContextMenu**</span><span class="sxs-lookup"><span data-stu-id="f197d-159">**ContextMenu**</span></span>](windowsribbon-element-contextmenu.md)<br/>                                     |
| [<span data-ttu-id="f197d-160">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="f197d-160">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                               |
| [<span data-ttu-id="f197d-161">**DropDownGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="f197d-161">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/>       |
| [<span data-ttu-id="f197d-162">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="f197d-162">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/>       |
| [<span data-ttu-id="f197d-163">**MiniToolbar**</span><span class="sxs-lookup"><span data-stu-id="f197d-163">**MiniToolbar**</span></span>](windowsribbon-element-minitoolbar.md)<br/>                                     |
| [<span data-ttu-id="f197d-164">**SplitButton.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="f197d-164">**SplitButton.MenuGroups**</span></span>](windowsribbon-element-splitbutton-menugroups.md)<br/>               |
| [<span data-ttu-id="f197d-165">**SplitButtonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="f197d-165">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="f197d-166">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f197d-166">Remarks</span></span>

<span data-ttu-id="f197d-167">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f197d-167">Required.</span></span>

<span data-ttu-id="f197d-168">Muss mindestens einmal für jedes [**ApplicationMenu-,**](windowsribbon-element-applicationmenu.md) [**ContextMenu-,**](windowsribbon-element-contextmenu.md) [**DropDownButton-,**](windowsribbon-element-dropdownbutton.md) [**DropDownGallery.MenuGroups-,**](windowsribbon-element-dropdowngallery-menugroups.md) [**InRibbonGallery.MenuGroups-,**](windowsribbon-element-inribbongallery-menugroups.md) [**SplitButton.MenuGroups-,**](windowsribbon-element-splitbutton-menugroups.md) [**MiniToolbar-**](windowsribbon-element-minitoolbar.md)oder [**SplitButtonGallery.MenuGroups-Element**](windowsribbon-element-splitbuttongallery-menugroups.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="f197d-168">Must occur at least once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md), [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), [**MiniToolbar**](windowsribbon-element-minitoolbar.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) element.</span></span>

<span data-ttu-id="f197d-169">Wenn [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) das übergeordnete Element ist, ist **MenuGroup** auf die folgenden untergeordneten Elemente beschränkt: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md)oder [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="f197d-169">If [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).</span></span>

<span data-ttu-id="f197d-170">Wenn [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups,**](windowsribbon-element-inribbongallery-menugroups.md) [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md)oder [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) das übergeordnete Element ist, ist **MenuGroup** auf die folgenden untergeordneten Elemente beschränkt: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)oder [**ToggleButton**](windowsribbon-element-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="f197d-170">If [**ContextMenu**](windowsribbon-element-contextmenu.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md), [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md), [**SplitButton.MenuGroups**](windowsribbon-element-splitbutton-menugroups.md), or [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), **DropDownButton**, [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="f197d-171">Wenn [**MiniToolbar**](windowsribbon-element-minitoolbar.md) das übergeordnete Element ist, wird **MenuGroup** auf die folgenden untergeordneten Elemente beschränkt: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)oder [**ToggleButton**](windowsribbon-element-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="f197d-171">If [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is the parent element then **MenuGroup** is constrained to the following child elements: [**Button**](windowsribbon-element-button.md), [**CheckBox**](windowsribbon-element-checkbox.md), [**ComboBox**](windowsribbon-element-combobox.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**FontControl**](windowsribbon-element-fontcontrol.md), [**Spinner**](windowsribbon-element-spinner.md), [**SplitButton**](windowsribbon-element-splitbutton.md), [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md), or [**ToggleButton**](windowsribbon-element-togglebutton.md).</span></span>

<span data-ttu-id="f197d-172">Das Class-Attribut ist nicht erforderlich, wenn [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) das übergeordnete Element ist.</span><span class="sxs-lookup"><span data-stu-id="f197d-172">The Class attribute is not required when [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element.</span></span> <span data-ttu-id="f197d-173">Das Framework erzwingt den Wert MajorItems für das Class-Attribut.</span><span class="sxs-lookup"><span data-stu-id="f197d-173">The framework enforces a value of MajorItems for the Class attribute.</span></span>

<span data-ttu-id="f197d-174">Wenn [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) das übergeordnete Element ist, ist das Class-Attribut nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f197d-174">When [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) is the parent element the Class attribute is not required.</span></span>

## <a name="examples"></a><span data-ttu-id="f197d-175">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f197d-175">Examples</span></span>

<span data-ttu-id="f197d-176">Im folgenden Beispiel wird das grundlegende Markup für [**SplitButton**](windowsribbon-element-splitbutton.md) mit einem **MenuGroup-Element** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f197d-176">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a **MenuGroup** element.</span></span>

<span data-ttu-id="f197d-177">Dieser Codeabschnitt zeigt die [**Deklarationen SplitButton**](windowsribbon-element-splitbutton.md) und **MenuGroup** Command mit einer großen und einer kleinen Imageressource.</span><span class="sxs-lookup"><span data-stu-id="f197d-177">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="f197d-178">Eine zugeordnete [**Gruppe,**](windowsribbon-element-group.md) die als übergeordneter Container für das **SplitButton-Element** fungiert, wird ebenfalls deklariert.</span><span class="sxs-lookup"><span data-stu-id="f197d-178">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


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



<span data-ttu-id="f197d-179">Dieser Codeabschnitt zeigt die [**Steuerelementdeklarationen SplitButton**](windowsribbon-element-splitbutton.md) und **MenuGroup** mit `StandardItems` und `MajorItems` .</span><span class="sxs-lookup"><span data-stu-id="f197d-179">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **MenuGroup** control declarations with both `StandardItems` and `MajorItems`.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="f197d-180">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f197d-180">Element information</span></span>

* <span data-ttu-id="f197d-181">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="f197d-181">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="f197d-182">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="f197d-182">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="f197d-183">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f197d-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f197d-184">Angeben von Menübandbildressourcen</span><span class="sxs-lookup"><span data-stu-id="f197d-184">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="f197d-185">Menügruppe</span><span class="sxs-lookup"><span data-stu-id="f197d-185">Menu Group</span></span>](windowsribbon-controls-menugroup.md)
</dt> </dl>

 

 





