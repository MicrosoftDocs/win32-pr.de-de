---
title: Dropdowngallery-Element
description: Stellt ein Drop-Down Katalog-Steuerelement mit einem Galerie basierten Menü dar.
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- Dropdowngallery-Element Windows-Menüband
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6dfc2890e33fa7f5d93919e7361465e163dadcb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516841"
---
# <a name="dropdowngallery-element"></a><span data-ttu-id="56217-104">Dropdowngallery-Element</span><span class="sxs-lookup"><span data-stu-id="56217-104">DropDownGallery element</span></span>

<span data-ttu-id="56217-105">Stellt ein [Dropdown-](windowsribbon-controls-dropdowngallery.md) Katalog Steuerelement mit einem Galerie basierten Menü dar.</span><span class="sxs-lookup"><span data-stu-id="56217-105">Represents a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control with a gallery-based menu.</span></span>

## <a name="usage"></a><span data-ttu-id="56217-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="56217-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="56217-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="56217-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56217-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="56217-108">Attribute</span></span></th>
<th><span data-ttu-id="56217-109">type</span><span class="sxs-lookup"><span data-stu-id="56217-109">Type</span></span></th>
<th><span data-ttu-id="56217-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="56217-110">Required</span></span></th>
<th><span data-ttu-id="56217-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56217-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56217-112"><strong>Applicationmodes</strong></span><span class="sxs-lookup"><span data-stu-id="56217-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="56217-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="56217-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="56217-114">Nein</span><span class="sxs-lookup"><span data-stu-id="56217-114">No</span></span><br/></td>
<td><span data-ttu-id="56217-115">Nur gültig, wenn <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> das übergeordnete Element ist.</span><span class="sxs-lookup"><span data-stu-id="56217-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="56217-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="56217-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="56217-117">Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste mit ganzen Zahlen zwischen 0 und 31 enthält.</span><span class="sxs-lookup"><span data-stu-id="56217-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="56217-118">Leerraum ist gültig und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="56217-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="56217-119">Maximale Länge: 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="56217-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56217-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="56217-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="56217-121">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="56217-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="56217-122">Nein</span><span class="sxs-lookup"><span data-stu-id="56217-122">No</span></span><br/></td>
<td><span data-ttu-id="56217-123">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="56217-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="56217-124">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="56217-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="56217-125">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="56217-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="56217-126">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="56217-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="56217-127">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="56217-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56217-128"><strong>Haslargeitems</strong></span><span class="sxs-lookup"><span data-stu-id="56217-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="56217-129">Boolesch</span><span class="sxs-lookup"><span data-stu-id="56217-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="56217-130">Nein</span><span class="sxs-lookup"><span data-stu-id="56217-130">No</span></span><br/></td>
<td><span data-ttu-id="56217-131">Bestimmt, ob die große oder kleine Bildressource des Befehls im Katalog-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="56217-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="56217-132">Gilt nur für Galerien, bei denen der Wert des <em>Type</em> -Attributs gleich ist <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="56217-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="56217-133">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="56217-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="56217-134">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="56217-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="56217-135">Standard.</span><span class="sxs-lookup"><span data-stu-id="56217-135">Default.</span></span> <br/> </dd> <span data-ttu-id="56217-136"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="56217-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56217-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="56217-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="56217-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="56217-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="56217-139">Nein</span><span class="sxs-lookup"><span data-stu-id="56217-139">No</span></span><br/></td>
<td><span data-ttu-id="56217-140"><dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="56217-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="56217-141">Der Standard ist -1.</span><span class="sxs-lookup"><span data-stu-id="56217-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56217-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="56217-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="56217-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="56217-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="56217-144">Nein</span><span class="sxs-lookup"><span data-stu-id="56217-144">No</span></span><br/></td>
<td><span data-ttu-id="56217-145"><dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="56217-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="56217-146">Der Standard ist -1.</span><span class="sxs-lookup"><span data-stu-id="56217-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56217-147"><strong>Textposition</strong></span><span class="sxs-lookup"><span data-stu-id="56217-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="56217-148">Textpositiontype</span><span class="sxs-lookup"><span data-stu-id="56217-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="56217-149">Nein</span><span class="sxs-lookup"><span data-stu-id="56217-149">No</span></span><br/></td>
<td><span data-ttu-id="56217-150">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="56217-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="56217-151">
<dt><span></span><span></span><strong></strong> Unten</span><span class="sxs-lookup"><span data-stu-id="56217-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="56217-152"><dt><span></span><span></span><strong></strong> Barg</span><span class="sxs-lookup"><span data-stu-id="56217-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="56217-153"><dt><span></span><span></span><strong></strong> Linken</span><span class="sxs-lookup"><span data-stu-id="56217-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="56217-154"><dt><span></span><span></span><strong></strong> Überlappen</span><span class="sxs-lookup"><span data-stu-id="56217-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="56217-155"><dt><span></span><span></span><strong></strong> Rechten</span><span class="sxs-lookup"><span data-stu-id="56217-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="56217-156"><dt><span></span><span></span><strong></strong> Oben</span><span class="sxs-lookup"><span data-stu-id="56217-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56217-157"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="56217-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="56217-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="56217-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="56217-159">Nein</span><span class="sxs-lookup"><span data-stu-id="56217-159">No</span></span><br/></td>
<td><span data-ttu-id="56217-160">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="56217-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="56217-161">
<dt><span></span><span></span><strong></strong> Punkte</span><span class="sxs-lookup"><span data-stu-id="56217-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="56217-162"><dt><span></span><span></span><strong></strong> Respekt</span><span class="sxs-lookup"><span data-stu-id="56217-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="56217-163">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="56217-163">Child elements</span></span>



| <span data-ttu-id="56217-164">Element</span><span class="sxs-lookup"><span data-stu-id="56217-164">Element</span></span>                                                                                           | <span data-ttu-id="56217-165">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56217-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="56217-166">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="56217-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                         | <span data-ttu-id="56217-167">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="56217-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="56217-168">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="56217-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="56217-169">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="56217-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="56217-170">**Dropdowngallery. menugroups**</span><span class="sxs-lookup"><span data-stu-id="56217-170">**DropDownGallery.MenuGroups**</span></span>](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | <span data-ttu-id="56217-171">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="56217-171">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="56217-172">**Dropdowngallery. menulayout**</span><span class="sxs-lookup"><span data-stu-id="56217-172">**DropDownGallery.MenuLayout**</span></span>](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | <span data-ttu-id="56217-173">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="56217-173">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="56217-174">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="56217-174">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="56217-175">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="56217-175">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="56217-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="56217-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="56217-177">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="56217-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="56217-178">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="56217-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56217-179">Element</span><span class="sxs-lookup"><span data-stu-id="56217-179">Element</span></span></th>
<th><span data-ttu-id="56217-180">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56217-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56217-181"><a href="windowsribbon-element-controlgroup.md"><strong>Controlgroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="56217-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="56217-182"><a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a></span><span class="sxs-lookup"><span data-stu-id="56217-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="56217-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="56217-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="56217-184">, Wenn Sie in einem <a href="windowsribbon-element-applicationmenu.md"><strong>applicationmenu</strong></a>enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="56217-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="56217-185">Dieses Element wird nur auf der ersten Ebene unterstützt und darf keine untergeordneten Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="56217-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56217-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>Quickaccesstoolbar. ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="56217-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="56217-187">Windows 8 und höher.</span><span class="sxs-lookup"><span data-stu-id="56217-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="56217-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="56217-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="56217-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56217-189">Remarks</span></span>

<span data-ttu-id="56217-190">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="56217-190">Optional.</span></span>

<span data-ttu-id="56217-191">Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, [**DropDownButton**](windowsribbon-element-dropdownbutton.md)-, [**Group**](windowsribbon-element-group.md)-, [**MenuGroup**](windowsribbon-element-menugroup.md)-oder [**SplitButton**](windowsribbon-element-splitbutton.md) -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="56217-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="56217-192">**Dropdowngallery** unterstützt [Anwendungsmodi](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="56217-192">**DropDownGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="56217-193">Der folgende Screenshot veranschaulicht das Menüband [-Dropdown-](windowsribbon-controls-dropdowngallery.md) Katalog Steuerelement in Microsoft Paint für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="56217-193">The following screen shot illustrates the Ribbon [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot eines Dropdown Galerie-Steuer Elements in Microsoft Paint für Windows 7.](images/controls/dropdowngallery.png)

## <a name="examples"></a><span data-ttu-id="56217-195">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56217-195">Examples</span></span>

<span data-ttu-id="56217-196">Im folgenden Beispiel wird das grundlegende Markup für **dropdowngallery** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="56217-196">The following example demonstrates the basic markup for the **DropDownGallery**.</span></span>

<span data-ttu-id="56217-197">Dieser Code Abschnitt zeigt die **dropdowngallery** -Befehls Deklarationen mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **dropdowngallery** -Element fungiert.</span><span class="sxs-lookup"><span data-stu-id="56217-197">This section of code shows the **DropDownGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **DropDownGallery** element.</span></span>


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



<span data-ttu-id="56217-198">In diesem Code Abschnitt werden die Deklarationen des **dropdowngallery** -Steuer Elements veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="56217-198">This section of code shows the **DropDownGallery** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="56217-199">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="56217-199">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="56217-200">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="56217-200">Minimum supported system</span></span><br/> | <span data-ttu-id="56217-201">Windows 7</span><span class="sxs-lookup"><span data-stu-id="56217-201">Windows 7</span></span> |
| <span data-ttu-id="56217-202">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="56217-202">Can be empty</span></span>                        | <span data-ttu-id="56217-203">Nein</span><span class="sxs-lookup"><span data-stu-id="56217-203">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="56217-204">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="56217-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56217-205">**Dropdown-Katalog-Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="56217-205">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="56217-206">Arbeiten mit Galerien</span><span class="sxs-lookup"><span data-stu-id="56217-206">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="56217-207">**Setmodes**</span><span class="sxs-lookup"><span data-stu-id="56217-207">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="56217-208">Galerie Beispiel</span><span class="sxs-lookup"><span data-stu-id="56217-208">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

