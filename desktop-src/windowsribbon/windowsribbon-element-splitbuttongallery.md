---
title: SplitButtonGallery-Element
description: Stellt ein Split Button Gallery-Steuerelement mit einem katalogbasierten Dropdownmenü dar.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- SplitButtonGallery-Element Windows-Menüband
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5f8767135b9472acba333b1cdfa6ab102e9b7f4
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444831"
---
# <a name="splitbuttongallery-element"></a><span data-ttu-id="d3edd-104">SplitButtonGallery-Element</span><span class="sxs-lookup"><span data-stu-id="d3edd-104">SplitButtonGallery element</span></span>

<span data-ttu-id="d3edd-105">Stellt ein Split [Button Gallery-Steuerelement](windowsribbon-controls-splitbuttongallery.md) mit einem katalogbasierten Dropdownmenü dar.</span><span class="sxs-lookup"><span data-stu-id="d3edd-105">Represents a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control with a gallery-based, drop-down menu.</span></span>

## <a name="usage"></a><span data-ttu-id="d3edd-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="d3edd-106">Usage</span></span>

``` syntax
<SplitButtonGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</SplitButtonGallery>
```

## <a name="attributes"></a><span data-ttu-id="d3edd-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="d3edd-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3edd-108">attribute</span><span class="sxs-lookup"><span data-stu-id="d3edd-108">Attribute</span></span></th>
<th><span data-ttu-id="d3edd-109">Typ</span><span class="sxs-lookup"><span data-stu-id="d3edd-109">Type</span></span></th>
<th><span data-ttu-id="d3edd-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d3edd-110">Required</span></span></th>
<th><span data-ttu-id="d3edd-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3edd-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3edd-112"><strong>ApplicationModes</strong></span><span class="sxs-lookup"><span data-stu-id="d3edd-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="d3edd-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="d3edd-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="d3edd-114">Nein</span><span class="sxs-lookup"><span data-stu-id="d3edd-114">No</span></span><br/></td>
<td><span data-ttu-id="d3edd-115">Nur gültig, wenn <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> das übergeordnete Element ist.</span><span class="sxs-lookup"><span data-stu-id="d3edd-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="d3edd-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="d3edd-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d3edd-117">Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste von ganzen Zahlen zwischen 0 und 31 enthält.</span><span class="sxs-lookup"><span data-stu-id="d3edd-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="d3edd-118">Leerraum ist gültig und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d3edd-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="d3edd-119">Maximale Länge: 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d3edd-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3edd-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="d3edd-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="d3edd-121">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="d3edd-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="d3edd-122">Nein</span><span class="sxs-lookup"><span data-stu-id="d3edd-122">No</span></span><br/></td>
<td><span data-ttu-id="d3edd-123">Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3edd-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="d3edd-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="d3edd-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d3edd-125">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999( einschließlich) oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="d3edd-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="d3edd-126">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d3edd-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="d3edd-127">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d3edd-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3edd-128"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="d3edd-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="d3edd-129">Boolesch</span><span class="sxs-lookup"><span data-stu-id="d3edd-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="d3edd-130">Nein</span><span class="sxs-lookup"><span data-stu-id="d3edd-130">No</span></span><br/></td>
<td><span data-ttu-id="d3edd-131">Bestimmt, ob die große oder kleine Imageressource des Befehls im Katalogsteuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d3edd-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d3edd-132">Gilt nur für Kataloge, in denen der Wert des <em>Type-Attributs</em> gleich <code>Command</code> ist.</span><span class="sxs-lookup"><span data-stu-id="d3edd-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="d3edd-133">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="d3edd-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="d3edd-134">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="d3edd-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="d3edd-135">Standard.</span><span class="sxs-lookup"><span data-stu-id="d3edd-135">Default.</span></span> <br/> </dd> <span data-ttu-id="d3edd-136"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="d3edd-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3edd-137"><strong>Itemheight</strong></span><span class="sxs-lookup"><span data-stu-id="d3edd-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="d3edd-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d3edd-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="d3edd-139">Nein</span><span class="sxs-lookup"><span data-stu-id="d3edd-139">No</span></span><br/></td>
<td><span data-ttu-id="d3edd-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="d3edd-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="d3edd-141">Der Standard ist -1.</span><span class="sxs-lookup"><span data-stu-id="d3edd-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3edd-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="d3edd-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="d3edd-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d3edd-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="d3edd-144">Nein</span><span class="sxs-lookup"><span data-stu-id="d3edd-144">No</span></span><br/></td>
<td><span data-ttu-id="d3edd-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="d3edd-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="d3edd-146">Der Standard ist -1.</span><span class="sxs-lookup"><span data-stu-id="d3edd-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3edd-147"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="d3edd-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="d3edd-148">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="d3edd-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="d3edd-149">Nein</span><span class="sxs-lookup"><span data-stu-id="d3edd-149">No</span></span><br/></td>
<td><span data-ttu-id="d3edd-150">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="d3edd-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="d3edd-151">
<dt><span></span><span></span><strong></strong> (Unten)</span><span class="sxs-lookup"><span data-stu-id="d3edd-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d3edd-152"><dt><span></span><span></span><strong></strong> (Ausblenden)</span><span class="sxs-lookup"><span data-stu-id="d3edd-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d3edd-153"><dt><span></span><span></span><strong></strong> (Links)</span><span class="sxs-lookup"><span data-stu-id="d3edd-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d3edd-154"><dt><span></span><span></span><strong></strong> (Überlappung)</span><span class="sxs-lookup"><span data-stu-id="d3edd-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d3edd-155"><dt><span></span><span></span><strong></strong> (Rechts)</span><span class="sxs-lookup"><span data-stu-id="d3edd-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d3edd-156"><dt><span></span><span></span><strong></strong> (Oben)</span><span class="sxs-lookup"><span data-stu-id="d3edd-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3edd-157"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="d3edd-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="d3edd-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="d3edd-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="d3edd-159">Nein</span><span class="sxs-lookup"><span data-stu-id="d3edd-159">No</span></span><br/></td>
<td><span data-ttu-id="d3edd-160">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="d3edd-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="d3edd-161">
<dt><span></span><span></span><strong></strong> (Elemente)</span><span class="sxs-lookup"><span data-stu-id="d3edd-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d3edd-162"><dt><span></span><span></span><strong></strong> (Befehle)</span><span class="sxs-lookup"><span data-stu-id="d3edd-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d3edd-163">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3edd-163">Child elements</span></span>



| <span data-ttu-id="d3edd-164">Element</span><span class="sxs-lookup"><span data-stu-id="d3edd-164">Element</span></span>                                                                                                 | <span data-ttu-id="d3edd-165">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3edd-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="d3edd-166">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="d3edd-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                               | <span data-ttu-id="d3edd-167">Kann ein oder mehrere Male auftreten</span><span class="sxs-lookup"><span data-stu-id="d3edd-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d3edd-168">**Checkbox**</span><span class="sxs-lookup"><span data-stu-id="d3edd-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                           | <span data-ttu-id="d3edd-169">Kann ein oder mehrere Male auftreten</span><span class="sxs-lookup"><span data-stu-id="d3edd-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d3edd-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="d3edd-170">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                     | <span data-ttu-id="d3edd-171">Kann ein oder mehrere Male auftreten</span><span class="sxs-lookup"><span data-stu-id="d3edd-171">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="d3edd-172">**SplitButtonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="d3edd-172">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | <span data-ttu-id="d3edd-173">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="d3edd-173">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="d3edd-174">**SplitButtonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="d3edd-174">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | <span data-ttu-id="d3edd-175">Kann höchstens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="d3edd-175">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="d3edd-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="d3edd-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                                   | <span data-ttu-id="d3edd-177">Kann ein oder mehrere Male auftreten</span><span class="sxs-lookup"><span data-stu-id="d3edd-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="d3edd-178">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d3edd-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3edd-179">Element</span><span class="sxs-lookup"><span data-stu-id="d3edd-179">Element</span></span></th>
<th><span data-ttu-id="d3edd-180">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3edd-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3edd-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3edd-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="d3edd-182"><a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3edd-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="d3edd-183"><a href="windowsribbon-element-menugroup.md"><strong>Menugroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3edd-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="d3edd-184">Wenn sie in einem <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d3edd-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="d3edd-185">Dieses Element wird nur auf der ersten Ebene unterstützt und darf keine untergeordneten Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="d3edd-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3edd-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3edd-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="d3edd-187">Windows 8 und neuer.</span><span class="sxs-lookup"><span data-stu-id="d3edd-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3edd-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3edd-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="d3edd-189">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d3edd-189">Remarks</span></span>

<span data-ttu-id="d3edd-190">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d3edd-190">Optional.</span></span>

<span data-ttu-id="d3edd-191">Kann ein oder mehrere Male für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) [**Group-, MenuGroup-**](windowsribbon-element-menugroup.md)oder [**SplitButton-Element**](windowsribbon-element-splitbutton.md) auftreten. [](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="d3edd-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="d3edd-192">**SplitButtonGallery** unterstützt [Anwendungsmodi.](ribbon-applicationmodes.md)</span><span class="sxs-lookup"><span data-stu-id="d3edd-192">**SplitButtonGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="d3edd-193">[Benutzeroberfläche \_ PKEY \_ BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) wird von einer Anwendung verwendet, um den Umschaltzustand für das Schaltflächensteuerelement eines **SplitButtonGallery** abzufragen.</span><span class="sxs-lookup"><span data-stu-id="d3edd-193">[UI\_PKEY\_BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) is used by an application to query the toggle-state for the button control of a **SplitButtonGallery**.</span></span>

<span data-ttu-id="d3edd-194">Der folgende Screenshot veranschaulicht das Menüband-Steuerelement "Katalog mit [geteilten Schaltflächen"](windowsribbon-controls-splitbuttongallery.md) in Microsoft Paint für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d3edd-194">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot eines Katalogsteuerelements für geteilte Schaltflächen in Microsoft Paint für Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a><span data-ttu-id="d3edd-196">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3edd-196">Examples</span></span>

<span data-ttu-id="d3edd-197">Im folgenden Beispiel wird das grundlegende Markup für den Katalog mit geteilten [Schaltflächen](windowsribbon-controls-splitbuttongallery.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d3edd-197">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="d3edd-198">Dieser Codeabschnitt zeigt die **SplitButtonGallery** Command-Deklarationen mit einer zugeordneten [**Gruppe,**](windowsribbon-element-group.md) die als übergeordneter Container für das **SplitButtonGallery-Element** fungiert.</span><span class="sxs-lookup"><span data-stu-id="d3edd-198">This section of code shows the **SplitButtonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButtonGallery** element.</span></span>


```XML
<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"/>
```



<span data-ttu-id="d3edd-199">Dieser Codeabschnitt zeigt die **SplitButtonGallery-Steuerelementdeklarationen.**</span><span class="sxs-lookup"><span data-stu-id="d3edd-199">This section of code shows the **SplitButtonGallery** control declarations.</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="d3edd-200">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d3edd-200">Element information</span></span>


- <span data-ttu-id="d3edd-201">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3edd-201">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="d3edd-202">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="d3edd-202">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="d3edd-203">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3edd-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3edd-204">Split Button Gallery-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d3edd-204">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="d3edd-205">Arbeiten mit Katalogen</span><span class="sxs-lookup"><span data-stu-id="d3edd-205">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="d3edd-206">**SetModes**</span><span class="sxs-lookup"><span data-stu-id="d3edd-206">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="d3edd-207">Katalogbeispiel</span><span class="sxs-lookup"><span data-stu-id="d3edd-207">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

