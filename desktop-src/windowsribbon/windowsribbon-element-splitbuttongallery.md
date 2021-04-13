---
title: Splitbuttongallery-Element
description: Stellt ein Steuerelement für eine unterteilte Schaltflächen Galerie mit einem Katalog basierten Dropdown Menü dar.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- Windows-Menüband des splitbuttongallery-Elements
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 68e90137325c16af6942f9f3929f8abfdf795660
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473781"
---
# <a name="splitbuttongallery-element"></a><span data-ttu-id="8b245-104">Splitbuttongallery-Element</span><span class="sxs-lookup"><span data-stu-id="8b245-104">SplitButtonGallery element</span></span>

<span data-ttu-id="8b245-105">Stellt ein Steuerelement für eine unter [teilte Schaltflächen Galerie](windowsribbon-controls-splitbuttongallery.md) mit einem Katalog basierten Dropdown Menü dar.</span><span class="sxs-lookup"><span data-stu-id="8b245-105">Represents a [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control with a gallery-based, drop-down menu.</span></span>

## <a name="usage"></a><span data-ttu-id="8b245-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="8b245-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="8b245-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="8b245-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b245-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="8b245-108">Attribute</span></span></th>
<th><span data-ttu-id="8b245-109">type</span><span class="sxs-lookup"><span data-stu-id="8b245-109">Type</span></span></th>
<th><span data-ttu-id="8b245-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8b245-110">Required</span></span></th>
<th><span data-ttu-id="8b245-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b245-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8b245-112"><strong>Applicationmodes</strong></span><span class="sxs-lookup"><span data-stu-id="8b245-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="8b245-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="8b245-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="8b245-114">Nein</span><span class="sxs-lookup"><span data-stu-id="8b245-114">No</span></span><br/></td>
<td><span data-ttu-id="8b245-115">Nur gültig, wenn <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> das übergeordnete Element ist.</span><span class="sxs-lookup"><span data-stu-id="8b245-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="8b245-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="8b245-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="8b245-117">Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste mit ganzen Zahlen zwischen 0 und 31 enthält.</span><span class="sxs-lookup"><span data-stu-id="8b245-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="8b245-118">Leerraum ist gültig und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8b245-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="8b245-119">Maximale Länge: 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8b245-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b245-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="8b245-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="8b245-121">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="8b245-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="8b245-122">Nein</span><span class="sxs-lookup"><span data-stu-id="8b245-122">No</span></span><br/></td>
<td><span data-ttu-id="8b245-123">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="8b245-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="8b245-124">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="8b245-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="8b245-125">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="8b245-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="8b245-126">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="8b245-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="8b245-127">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8b245-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b245-128"><strong>Haslargeitems</strong></span><span class="sxs-lookup"><span data-stu-id="8b245-128"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="8b245-129">Boolesch</span><span class="sxs-lookup"><span data-stu-id="8b245-129">Boolean</span></span><br/></td>
<td><span data-ttu-id="8b245-130">Nein</span><span class="sxs-lookup"><span data-stu-id="8b245-130">No</span></span><br/></td>
<td><span data-ttu-id="8b245-131">Bestimmt, ob die große oder kleine Bildressource des Befehls im Katalog-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8b245-131">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8b245-132">Gilt nur für Galerien, bei denen der Wert des <em>Type</em> -Attributs gleich ist <code>Command</code> .</span><span class="sxs-lookup"><span data-stu-id="8b245-132">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="8b245-133">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="8b245-133">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="8b245-134">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="8b245-134">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="8b245-135">Standard.</span><span class="sxs-lookup"><span data-stu-id="8b245-135">Default.</span></span> <br/> </dd> <span data-ttu-id="8b245-136"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="8b245-136"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b245-137"><strong>ItemHeight</strong></span><span class="sxs-lookup"><span data-stu-id="8b245-137"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="8b245-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8b245-138">xs:integer</span></span><br/></td>
<td><span data-ttu-id="8b245-139">Nein</span><span class="sxs-lookup"><span data-stu-id="8b245-139">No</span></span><br/></td>
<td><span data-ttu-id="8b245-140"><dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="8b245-140"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="8b245-141">Der Standard ist -1.</span><span class="sxs-lookup"><span data-stu-id="8b245-141">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b245-142"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="8b245-142"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="8b245-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8b245-143">xs:integer</span></span><br/></td>
<td><span data-ttu-id="8b245-144">Nein</span><span class="sxs-lookup"><span data-stu-id="8b245-144">No</span></span><br/></td>
<td><span data-ttu-id="8b245-145"><dt><span></span><span></span><strong></strong> (xs: Integer)</span><span class="sxs-lookup"><span data-stu-id="8b245-145"><dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="8b245-146">Der Standard ist -1.</span><span class="sxs-lookup"><span data-stu-id="8b245-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b245-147"><strong>Textposition</strong></span><span class="sxs-lookup"><span data-stu-id="8b245-147"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="8b245-148">Textpositiontype</span><span class="sxs-lookup"><span data-stu-id="8b245-148">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="8b245-149">Nein</span><span class="sxs-lookup"><span data-stu-id="8b245-149">No</span></span><br/></td>
<td><span data-ttu-id="8b245-150">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="8b245-150">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="8b245-151">
<dt><span></span><span></span><strong></strong> Unten</span><span class="sxs-lookup"><span data-stu-id="8b245-151">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="8b245-152"><dt><span></span><span></span><strong></strong> Barg</span><span class="sxs-lookup"><span data-stu-id="8b245-152"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="8b245-153"><dt><span></span><span></span><strong></strong> Linken</span><span class="sxs-lookup"><span data-stu-id="8b245-153"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="8b245-154"><dt><span></span><span></span><strong></strong> Überlappen</span><span class="sxs-lookup"><span data-stu-id="8b245-154"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="8b245-155"><dt><span></span><span></span><strong></strong> Rechten</span><span class="sxs-lookup"><span data-stu-id="8b245-155"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="8b245-156"><dt><span></span><span></span><strong></strong> Oben</span><span class="sxs-lookup"><span data-stu-id="8b245-156"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b245-157"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="8b245-157"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="8b245-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="8b245-158">xs:string</span></span><br/></td>
<td><span data-ttu-id="8b245-159">Nein</span><span class="sxs-lookup"><span data-stu-id="8b245-159">No</span></span><br/></td>
<td><span data-ttu-id="8b245-160">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="8b245-160">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="8b245-161">
<dt><span></span><span></span><strong></strong> Punkte</span><span class="sxs-lookup"><span data-stu-id="8b245-161">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="8b245-162"><dt><span></span><span></span><strong></strong> Respekt</span><span class="sxs-lookup"><span data-stu-id="8b245-162"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="8b245-163">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8b245-163">Child elements</span></span>



| <span data-ttu-id="8b245-164">Element</span><span class="sxs-lookup"><span data-stu-id="8b245-164">Element</span></span>                                                                                                 | <span data-ttu-id="8b245-165">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b245-165">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="8b245-166">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="8b245-166">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                               | <span data-ttu-id="8b245-167">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="8b245-167">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="8b245-168">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="8b245-168">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                           | <span data-ttu-id="8b245-169">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="8b245-169">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="8b245-170">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="8b245-170">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                     | <span data-ttu-id="8b245-171">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="8b245-171">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="8b245-172">**Splitbuttongallery. menugroups**</span><span class="sxs-lookup"><span data-stu-id="8b245-172">**SplitButtonGallery.MenuGroups**</span></span>](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | <span data-ttu-id="8b245-173">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="8b245-173">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="8b245-174">**Splitbuttongallery. menulayout**</span><span class="sxs-lookup"><span data-stu-id="8b245-174">**SplitButtonGallery.MenuLayout**</span></span>](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | <span data-ttu-id="8b245-175">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="8b245-175">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="8b245-176">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="8b245-176">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                                   | <span data-ttu-id="8b245-177">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="8b245-177">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="8b245-178">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8b245-178">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b245-179">Element</span><span class="sxs-lookup"><span data-stu-id="8b245-179">Element</span></span></th>
<th><span data-ttu-id="8b245-180">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b245-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8b245-181"><a href="windowsribbon-element-controlgroup.md"><strong>Controlgroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b245-181"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="8b245-182"><a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b245-182"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="8b245-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b245-183"><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a></span></span><br/></td>
<td><span data-ttu-id="8b245-184">, Wenn Sie in einem <a href="windowsribbon-element-applicationmenu.md"><strong>applicationmenu</strong></a>enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="8b245-184">When contained in an <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>.</span></span> <span data-ttu-id="8b245-185">Dieses Element wird nur auf der ersten Ebene unterstützt und darf keine untergeordneten Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8b245-185">This element is only supported on the first level and must have no child elements.</span></span><br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b245-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>Quickaccesstoolbar. ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b245-186"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="8b245-187">Windows 8 und höher.</span><span class="sxs-lookup"><span data-stu-id="8b245-187">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b245-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="8b245-188"><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a></span></span><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="8b245-189">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b245-189">Remarks</span></span>

<span data-ttu-id="8b245-190">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8b245-190">Optional.</span></span>

<span data-ttu-id="8b245-191">Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, [**Group**](windowsribbon-element-group.md)-, [**MenuGroup**](windowsribbon-element-menugroup.md)-oder [**SplitButton**](windowsribbon-element-splitbutton.md) -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="8b245-191">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), or [**SplitButton**](windowsribbon-element-splitbutton.md) element.</span></span>

<span data-ttu-id="8b245-192">**Splitbuttongallery** unterstützt [Anwendungsmodi](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="8b245-192">**SplitButtonGallery** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="8b245-193">[Benutzeroberfläche \_ Pkey \_ BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) wird von einer Anwendung verwendet, um den UMSCHALT Zustand für das Schaltflächen-Steuerelement eines **splitbuttongallery** abzufragen.</span><span class="sxs-lookup"><span data-stu-id="8b245-193">[UI\_PKEY\_BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) is used by an application to query the toggle-state for the button control of a **SplitButtonGallery**.</span></span>

<span data-ttu-id="8b245-194">Der folgende Screenshot veranschaulicht das Steuerelement für den [Menüband-unterteilte Schalt](windowsribbon-controls-splitbuttongallery.md) Flächen Katalog in Microsoft Paint für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8b245-194">The following screen shot illustrates the Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot eines Steuer Elements für eine unterteilte Schaltflächen Galerie in Microsoft Paint für Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a><span data-ttu-id="8b245-196">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b245-196">Examples</span></span>

<span data-ttu-id="8b245-197">Im folgenden Beispiel wird das grundlegende Markup für den Katalog mit unter [teilten Schalt](windowsribbon-controls-splitbuttongallery.md)Flächen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="8b245-197">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="8b245-198">Dieser Code Abschnitt zeigt die **splitbuttongallery** -Befehls Deklarationen mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **splitbuttongallery** -Element fungiert.</span><span class="sxs-lookup"><span data-stu-id="8b245-198">This section of code shows the **SplitButtonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButtonGallery** element.</span></span>


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



<span data-ttu-id="8b245-199">In diesem Code Abschnitt werden die Deklarationen des **splitbuttongallery** -Steuer Elements veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="8b245-199">This section of code shows the **SplitButtonGallery** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="8b245-200">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8b245-200">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="8b245-201">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="8b245-201">Minimum supported system</span></span><br/> | <span data-ttu-id="8b245-202">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8b245-202">Windows 7</span></span> |
| <span data-ttu-id="8b245-203">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="8b245-203">Can be empty</span></span>                        | <span data-ttu-id="8b245-204">Nein</span><span class="sxs-lookup"><span data-stu-id="8b245-204">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="8b245-205">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8b245-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b245-206">Steuerelement "Split Button Gallery"</span><span class="sxs-lookup"><span data-stu-id="8b245-206">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="8b245-207">Arbeiten mit Galerien</span><span class="sxs-lookup"><span data-stu-id="8b245-207">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="8b245-208">**Setmodes**</span><span class="sxs-lookup"><span data-stu-id="8b245-208">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[<span data-ttu-id="8b245-209">Galerie Beispiel</span><span class="sxs-lookup"><span data-stu-id="8b245-209">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

