---
title: DropDownGallery-Element
description: Stellt ein Drop-Down Gallery-Steuerelement mit einem katalogbasierten Menü dar.
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- DropDownGallery-Element Windows-Menüband
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befe0624dfef5910625a0aa067f3ad8cd9882ca2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443421"
---
# <a name="dropdowngallery-element"></a><span data-ttu-id="89ca5-104">DropDownGallery-Element</span><span class="sxs-lookup"><span data-stu-id="89ca5-104">DropDownGallery element</span></span>

<span data-ttu-id="89ca5-105">Stellt ein [Dropdownkatalog-Steuerelement](windowsribbon-controls-dropdowngallery.md) mit einem katalogbasierten Menü dar.</span><span class="sxs-lookup"><span data-stu-id="89ca5-105">Represents a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control with a gallery-based menu.</span></span>

## <a name="usage"></a><span data-ttu-id="89ca5-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="89ca5-106">Usage</span></span>

``` syntax
<DropDownGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</DropDownGallery>
```

## <a name="attributes"></a><span data-ttu-id="89ca5-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="89ca5-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="89ca5-108">attribute</span><span class="sxs-lookup"><span data-stu-id="89ca5-108">Attribute</span></span></th>
<th><span data-ttu-id="89ca5-109">Typ</span><span class="sxs-lookup"><span data-stu-id="89ca5-109">Type</span></span></th>
<th><span data-ttu-id="89ca5-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="89ca5-110">Required</span></span></th>
<th><span data-ttu-id="89ca5-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89ca5-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89ca5-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="89ca5-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="89ca5-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="89ca5-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="89ca5-114">Nein</span><span class="sxs-lookup"><span data-stu-id="89ca5-114">No</span></span><br/></td>
<td><span data-ttu-id="89ca5-115">Nur gültig, wenn <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> das übergeordnete Element ist.</span><span class="sxs-lookup"><span data-stu-id="89ca5-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="89ca5-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="89ca5-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="89ca5-117">Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste von ganzen Zahlen zwischen 0 und 31 enthält.</span><span class="sxs-lookup"><span data-stu-id="89ca5-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="89ca5-118">Leerraum ist gültig und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="89ca5-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="89ca5-119">Maximale Länge: 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="89ca5-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89ca5-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="89ca5-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="89ca5-121">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="89ca5-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="89ca5-122">Nein</span><span class="sxs-lookup"><span data-stu-id="89ca5-122">No</span></span><br/></td>
<td><span data-ttu-id="89ca5-123">Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="89ca5-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="89ca5-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="89ca5-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="89ca5-125">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999 einschließlich oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="89ca5-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="89ca5-126">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="89ca5-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="89ca5-127">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="89ca5-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89ca5-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="89ca5-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="89ca5-129">Boolesch</span><span class="sxs-lookup"><span data-stu-id="89ca5-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="89ca5-130">Nein</span><span class="sxs-lookup"><span data-stu-id="89ca5-130">No</span></span><br/></td>
<td><span data-ttu-id="89ca5-131">Bestimmt, ob die große oder kleine Bildressource des Befehls im Katalogsteuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="89ca5-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="89ca5-132">Gilt nur für Kataloge, in denen der Wert des <em>Type-Attributs</em> gleich <code>Command</code> ist.</span><span class="sxs-lookup"><span data-stu-id="89ca5-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="89ca5-133">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="89ca5-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="89ca5-134">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="89ca5-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="89ca5-135">Standard.</span><span class="sxs-lookup"><span data-stu-id="89ca5-135">Default.</span></span> <br/> </dd> <span data-ttu-id="89ca5-136"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="89ca5-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89ca5-137"><strong>Itemheight</strong></span><span class="sxs-lookup"><span data-stu-id="89ca5-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="89ca5-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="89ca5-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="89ca5-139">Nein</span><span class="sxs-lookup"><span data-stu-id="89ca5-139">No</span></span><br/></td>
<td><span data-ttu-id="89ca5-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="89ca5-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="89ca5-141">Der Standard ist -1.</span><span class="sxs-lookup"><span data-stu-id="89ca5-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89ca5-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="89ca5-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="89ca5-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="89ca5-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="89ca5-144">Nein</span><span class="sxs-lookup"><span data-stu-id="89ca5-144">No</span></span><br/></td>
<td><span data-ttu-id="89ca5-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="89ca5-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="89ca5-146">Der Standard ist -1.</span><span class="sxs-lookup"><span data-stu-id="89ca5-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89ca5-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="89ca5-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="89ca5-148">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="89ca5-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="89ca5-149">Nein</span><span class="sxs-lookup"><span data-stu-id="89ca5-149">No</span></span><br/></td>
<td><span data-ttu-id="89ca5-150">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="89ca5-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="89ca5-151">
<dt><span></span><span></span><strong></strong> (Unten)</span><span class="sxs-lookup"><span data-stu-id="89ca5-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="89ca5-152"><dt><span></span><span></span><strong></strong> (Ausblenden)</span><span class="sxs-lookup"><span data-stu-id="89ca5-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="89ca5-153"><dt><span></span><span></span><strong></strong> (Links)</span><span class="sxs-lookup"><span data-stu-id="89ca5-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="89ca5-154"><dt><span></span><span></span><strong></strong> (Überlappung)</span><span class="sxs-lookup"><span data-stu-id="89ca5-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="89ca5-155"><dt><span></span><span></span><strong></strong> (Rechts)</span><span class="sxs-lookup"><span data-stu-id="89ca5-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="89ca5-156"><dt><span></span><span></span><strong></strong> (Oben)</span><span class="sxs-lookup"><span data-stu-id="89ca5-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89ca5-157"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="89ca5-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="89ca5-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="89ca5-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="89ca5-159">Nein</span><span class="sxs-lookup"><span data-stu-id="89ca5-159">No</span></span><br/></td>
<td><span data-ttu-id="89ca5-160">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="89ca5-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="89ca5-161">
<dt><span></span><span></span><strong></strong> (Elemente)</span><span class="sxs-lookup"><span data-stu-id="89ca5-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="89ca5-162"><dt><span></span><span></span><strong></strong> (Befehle)</span><span class="sxs-lookup"><span data-stu-id="89ca5-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="89ca5-163">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="89ca5-163">Child elements</span></span>



| <span data-ttu-id="89ca5-164">Element</span><span class="sxs-lookup"><span data-stu-id="89ca5-164">Element</span></span>                                                                                           | <span data-ttu-id="89ca5-165">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89ca5-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="89ca5-166">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="89ca5-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                         | <span data-ttu-id="89ca5-167">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="89ca5-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="89ca5-168">**Checkbox**</span><span class="sxs-lookup"><span data-stu-id="89ca5-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="89ca5-169">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="89ca5-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="89ca5-170">**DropDownGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="89ca5-170">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | <span data-ttu-id="89ca5-171">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="89ca5-171">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="89ca5-172">**DropDownGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="89ca5-172">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | <span data-ttu-id="89ca5-173">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="89ca5-173">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="89ca5-174">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="89ca5-174">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="89ca5-175">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="89ca5-175">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="89ca5-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="89ca5-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="89ca5-177">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="89ca5-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="89ca5-178">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="89ca5-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="89ca5-179">Element</span><span class="sxs-lookup"><span data-stu-id="89ca5-179">Element</span></span></th>
<th><span data-ttu-id="89ca5-180">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89ca5-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89ca5-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="89ca5-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="89ca5-182"><a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a></span><span class="sxs-lookup"><span data-stu-id="89ca5-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="89ca5-183"><a href="windowsribbon-element-menugroup.md"><strong>Menugroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="89ca5-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="89ca5-184">Wenn sie in einem <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="89ca5-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="89ca5-185">Dieses Element wird nur auf der ersten Ebene unterstützt und darf keine untergeordneten Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="89ca5-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89ca5-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="89ca5-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="89ca5-187">Windows 8 und neuer.</span><span class="sxs-lookup"><span data-stu-id="89ca5-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89ca5-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="89ca5-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="89ca5-189">Hinweise</span><span class="sxs-lookup"><span data-stu-id="89ca5-189">Remarks</span></span>

<span data-ttu-id="89ca5-190">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="89ca5-190">Optional.</span></span>

<span data-ttu-id="89ca5-191">Kann ein oder mehrere Male für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) [**DropDownButton-,**](windowsribbon-element-dropdownbutton.md) [**Group-, MenuGroup-**](windowsribbon-element-menugroup.md)oder [**SplitButton-Element**](windowsribbon-element-splitbutton.md) auftreten. [](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="89ca5-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="89ca5-192">**DropDownGallery** unterstützt [Anwendungsmodi.](ribbon-applicationmodes.md)</span><span class="sxs-lookup"><span data-stu-id="89ca5-192">**DropDownGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="89ca5-193">Der folgende Screenshot veranschaulicht das [Menüband-Dropdownkatalog-Steuerelement](windowsribbon-controls-dropdowngallery.md) in Microsoft Paint für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="89ca5-193">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot eines Dropdownkatalog-Steuerelements in Microsoft Paint für Windows 7.](images/controls/dropdowngallery.png)

## <a name="examples"></a><span data-ttu-id="89ca5-195">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89ca5-195">Examples</span></span>

<span data-ttu-id="89ca5-196">Im folgenden Beispiel wird das grundlegende Markup für **dropDownGallery** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="89ca5-196">The following example demonstrates the basic markup for the **DropDownGallery**.</span></span>

<span data-ttu-id="89ca5-197">Dieser Codeabschnitt zeigt die **DropDownGallery** Command-Deklarationen mit einer zugeordneten [**Gruppe,**](windowsribbon-element-group.md) die als übergeordneter Container für das **DropDownGallery-Element** fungiert.</span><span class="sxs-lookup"><span data-stu-id="89ca5-197">This section of code shows the **DropDownGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **DropDownGallery** element.</span></span>


```XML
<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```



<span data-ttu-id="89ca5-198">Dieser Codeabschnitt zeigt die **DropDownGallery-Steuerelementdeklarationen.**</span><span class="sxs-lookup"><span data-stu-id="89ca5-198">This section of code shows the **DropDownGallery** control declarations.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="89ca5-199">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="89ca5-199">Element information</span></span>

* <span data-ttu-id="89ca5-200">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="89ca5-200">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="89ca5-201">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="89ca5-201">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="89ca5-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89ca5-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89ca5-203">**Dropdownkatalog-Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="89ca5-203">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="89ca5-204">Arbeiten mit Katalogen</span><span class="sxs-lookup"><span data-stu-id="89ca5-204">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="89ca5-205">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="89ca5-205">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="89ca5-206">Katalogbeispiel</span><span class="sxs-lookup"><span data-stu-id="89ca5-206">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

