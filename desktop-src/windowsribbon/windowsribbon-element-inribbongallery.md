---
title: InRibbonGallery-Element
description: Stellt den In-Ribbon Katalog dar, ein katalogbasiertes Steuerelement, das eine Standardteilmenge von Elementen direkt im Menüband verfügbar macht. Alle verbleibenden Elemente werden angezeigt, wenn auf eine Dropdownmenüschaltfläche geklickt wird.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- InRibbonGallery-Element Im Windows-Menüband
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a25b2ebb937d954adce58231fd8c6b3347a031a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443371"
---
# <a name="inribbongallery-element"></a><span data-ttu-id="96716-105">InRibbonGallery-Element</span><span class="sxs-lookup"><span data-stu-id="96716-105">InRibbonGallery element</span></span>

<span data-ttu-id="96716-106">Stellt den [Katalog im Menüband dar,](windowsribbon-controls-inribbongallery.md)ein katalogbasiertes Steuerelement, das eine Standardteilmenge von Elementen direkt im Menüband verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="96716-106">Represents the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md), a gallery-based control that exposes a default subset of items directly in the Ribbon.</span></span> <span data-ttu-id="96716-107">Alle verbleibenden Elemente werden angezeigt, wenn auf eine Dropdownmenüschaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="96716-107">Any remaining items are displayed when a drop-down menu button is clicked.</span></span>

## <a name="usage"></a><span data-ttu-id="96716-108">Verwendung</span><span class="sxs-lookup"><span data-stu-id="96716-108">Usage</span></span>

``` syntax
<InRibbonGallery
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  MinColumnsLarge = "xs:integer"
  MaxColumnsMedium = "xs:integer"
  MinColumnsMedium = "xs:integer"
  MaxColumns = "xs:integer"
  MaxRows = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</InRibbonGallery>
```

## <a name="attributes"></a><span data-ttu-id="96716-109">Attribute</span><span class="sxs-lookup"><span data-stu-id="96716-109">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96716-110">attribute</span><span class="sxs-lookup"><span data-stu-id="96716-110">Attribute</span></span></th>
<th><span data-ttu-id="96716-111">Typ</span><span class="sxs-lookup"><span data-stu-id="96716-111">Type</span></span></th>
<th><span data-ttu-id="96716-112">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="96716-112">Required</span></span></th>
<th><span data-ttu-id="96716-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96716-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96716-114"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="96716-114"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="96716-115">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="96716-115">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="96716-116">Nein</span><span class="sxs-lookup"><span data-stu-id="96716-116">No</span></span><br/></td>
<td><span data-ttu-id="96716-117">Ordnet das Element einem Befehl <a href="windowsribbon-element-command.md"><strong>zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="96716-117">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="96716-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="96716-118">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="96716-119">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="96716-119">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="96716-120">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="96716-120">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="96716-121">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="96716-121">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96716-122"><strong>HasLargeItems</strong></span><span class="sxs-lookup"><span data-stu-id="96716-122"><strong>HasLargeItems</strong></span></span><br/></td>
<td><span data-ttu-id="96716-123">Boolesch</span><span class="sxs-lookup"><span data-stu-id="96716-123">Boolean</span></span><br/></td>
<td><span data-ttu-id="96716-124">Nein</span><span class="sxs-lookup"><span data-stu-id="96716-124">No</span></span><br/></td>
<td><span data-ttu-id="96716-125">Bestimmt, ob die große oder kleine Bildressource des Befehls im Katalog-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="96716-125">Determines whether the large or small image resource of the Command is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="96716-126">Gilt nur für Kataloge, in denen der Wert des <em>Type-Attributs</em> gleich <code>Command</code> ist.</span><span class="sxs-lookup"><span data-stu-id="96716-126">Applies only to galleries where the value of the <em>Type</em> attribute is equal to <code>Command</code>.</span></span>
</blockquote>
<br/> <span data-ttu-id="96716-127">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="96716-127">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="96716-128">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="96716-128">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="96716-129">Standard.</span><span class="sxs-lookup"><span data-stu-id="96716-129">Default.</span></span> <br/> </dd> <span data-ttu-id="96716-130"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="96716-130"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96716-131"><strong>Itemheight</strong></span><span class="sxs-lookup"><span data-stu-id="96716-131"><strong>ItemHeight</strong></span></span><br/></td>
<td><span data-ttu-id="96716-132">xs:integer</span><span class="sxs-lookup"><span data-stu-id="96716-132">xs:integer</span></span><br/></td>
<td><span data-ttu-id="96716-133">Nein</span><span class="sxs-lookup"><span data-stu-id="96716-133">No</span></span><br/></td>
<td><span data-ttu-id="96716-134">Bestimmt zusammen <em>mit ItemWidth</em>die Größe des Elementbilds, das im Katalogsteuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="96716-134">Together with <em>ItemWidth</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="96716-135">Gilt nur für Kataloge, in denen der Wert des <em>Type-Attributs</em> gleich ist.</span><span class="sxs-lookup"><span data-stu-id="96716-135">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="96716-136">.</span><span class="sxs-lookup"><span data-stu-id="96716-136">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="96716-137">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="96716-137">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="96716-138">Der Standard ist -1.</span><span class="sxs-lookup"><span data-stu-id="96716-138">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96716-139"><strong>ItemWidth</strong></span><span class="sxs-lookup"><span data-stu-id="96716-139"><strong>ItemWidth</strong></span></span><br/></td>
<td><span data-ttu-id="96716-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="96716-140">xs:integer</span></span><br/></td>
<td><span data-ttu-id="96716-141">Nein</span><span class="sxs-lookup"><span data-stu-id="96716-141">No</span></span><br/></td>
<td><span data-ttu-id="96716-142">Bestimmt zusammen <em>mit ItemHeight</em>die Größe des Elementbilds, das im Katalogsteuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="96716-142">Together with <em>ItemHeight</em>, determines the size of the item image that is displayed in the gallery control.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="96716-143">Gilt nur für Kataloge, in denen der Wert des <em>Type-Attributs</em> gleich ist.</span><span class="sxs-lookup"><span data-stu-id="96716-143">Applies only to galleries where the value of the <em>Type</em> attribute is equal to</span></span> <code>Item</code><span data-ttu-id="96716-144">.</span><span class="sxs-lookup"><span data-stu-id="96716-144">.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="96716-145">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="96716-145">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="96716-146">Der Standard ist -1.</span><span class="sxs-lookup"><span data-stu-id="96716-146">The default is -1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96716-147"><strong>MaxColumns</strong></span><span class="sxs-lookup"><span data-stu-id="96716-147"><strong>MaxColumns</strong></span></span><br/></td>
<td><span data-ttu-id="96716-148">xs:integer</span><span class="sxs-lookup"><span data-stu-id="96716-148">xs:integer</span></span><br/></td>
<td><span data-ttu-id="96716-149">Nein</span><span class="sxs-lookup"><span data-stu-id="96716-149">No</span></span><br/></td>
<td><span data-ttu-id="96716-150">Gibt die maximale Anzahl von Spalten an, die <strong>in InRibbonGallery</strong> angezeigt werden, z. B. in der Dropdownliste Großes Gruppenlayout. <em></em></span><span class="sxs-lookup"><span data-stu-id="96716-150">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays, for example, in the <em>Large</em> group layout drop-down.</span></span><br/> <br/><span data-ttu-id="96716-151">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="96716-151">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96716-152"><strong>MaxColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="96716-152"><strong>MaxColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="96716-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="96716-153">xs:integer</span></span><br/></td>
<td><span data-ttu-id="96716-154">Nein</span><span class="sxs-lookup"><span data-stu-id="96716-154">No</span></span><br/></td>
<td><span data-ttu-id="96716-155">Gibt die maximale Anzahl von Spalten an, die <strong>die InRibbonGallery</strong> im <em>Gruppenlayout</em> Mittel anzeigt, bevor sie zu <em>Großes Layout</em> wechselt.</span><span class="sxs-lookup"><span data-stu-id="96716-155">Specifies the maximum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Large</em> layout.</span></span> <br/> <br/><span data-ttu-id="96716-156">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="96716-156">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96716-157"><strong>MaxRows</strong></span><span class="sxs-lookup"><span data-stu-id="96716-157"><strong>MaxRows</strong></span></span><br/></td>
<td><span data-ttu-id="96716-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="96716-158">xs:integer</span></span><br/></td>
<td><span data-ttu-id="96716-159">Nein</span><span class="sxs-lookup"><span data-stu-id="96716-159">No</span></span><br/></td>
<td><span data-ttu-id="96716-160">Gibt die maximale Anzahl von Zeilen für das Layout von <strong>InRibbonGallery-Elementen</strong> an.</span><span class="sxs-lookup"><span data-stu-id="96716-160">Specifies the maximum number of rows for the layout of <strong>InRibbonGallery</strong> items.</span></span> <br/> <br/><span data-ttu-id="96716-161">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="96716-161">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd> <span data-ttu-id="96716-162">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="96716-162">The default is 1.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96716-163"><strong>MinColumnsLarge</strong></span><span class="sxs-lookup"><span data-stu-id="96716-163"><strong>MinColumnsLarge</strong></span></span><br/></td>
<td><span data-ttu-id="96716-164">xs:integer</span><span class="sxs-lookup"><span data-stu-id="96716-164">xs:integer</span></span><br/></td>
<td><span data-ttu-id="96716-165">Nein</span><span class="sxs-lookup"><span data-stu-id="96716-165">No</span></span><br/></td>
<td><span data-ttu-id="96716-166">Gibt die Mindestanzahl von Spalten an, die die <em></em> <strong>InRibbonGallery</strong> im Layout der großen Gruppe anzeigt, bevor sie zu <em>Medium wechselt.</em></span><span class="sxs-lookup"><span data-stu-id="96716-166">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Large</em> group layout, before switching to <em>Medium</em>.</span></span><br/> <br/><span data-ttu-id="96716-167">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="96716-167">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96716-168"><strong>MinColumnsMedium</strong></span><span class="sxs-lookup"><span data-stu-id="96716-168"><strong>MinColumnsMedium</strong></span></span><br/></td>
<td><span data-ttu-id="96716-169">xs:integer</span><span class="sxs-lookup"><span data-stu-id="96716-169">xs:integer</span></span><br/></td>
<td><span data-ttu-id="96716-170">Nein</span><span class="sxs-lookup"><span data-stu-id="96716-170">No</span></span><br/></td>
<td><span data-ttu-id="96716-171">Gibt die Mindestanzahl von Spalten an, die <strong>in DerRibbonGallery</strong> im <em>Gruppenlayout</em> Mittel angezeigt wird, bevor zu <em>Small</em>wechselt.</span><span class="sxs-lookup"><span data-stu-id="96716-171">Specifies the minimum number of columns that the <strong>InRibbonGallery</strong> displays in the <em>Medium</em> group layout, before switching to <em>Small</em>.</span></span><br/> <br/><span data-ttu-id="96716-172">
<dt><span></span><span></span><strong></strong> (xs:integer)</span><span class="sxs-lookup"><span data-stu-id="96716-172">
<dt><span></span><span></span><strong></strong> (xs:integer)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96716-173"><strong>TextPosition</strong></span><span class="sxs-lookup"><span data-stu-id="96716-173"><strong>TextPosition</strong></span></span><br/></td>
<td><span data-ttu-id="96716-174">TextPositionType</span><span class="sxs-lookup"><span data-stu-id="96716-174">TextPositionType</span></span><br/></td>
<td><span data-ttu-id="96716-175">Nein</span><span class="sxs-lookup"><span data-stu-id="96716-175">No</span></span><br/></td>
<td><span data-ttu-id="96716-176">Gibt an, wo die Elementbezeichnung relativ zum Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="96716-176">Specifies where the item label is displayed, relative to the image.</span></span> <br/> <span data-ttu-id="96716-177">Auf einen der folgenden Werte beschränkt:</span><span class="sxs-lookup"><span data-stu-id="96716-177">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="96716-178">
<dt><span></span><span></span><strong></strong> (Unten)</span><span class="sxs-lookup"><span data-stu-id="96716-178">
<dt><span></span><span></span><strong></strong> (Bottom)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="96716-179"><dt><span></span><span></span><strong></strong> (Ausblenden)</span><span class="sxs-lookup"><span data-stu-id="96716-179"><dt><span></span><span></span><strong></strong> (Hide)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="96716-180"><dt><span></span><span></span><strong></strong> (Links)</span><span class="sxs-lookup"><span data-stu-id="96716-180"><dt><span></span><span></span><strong></strong> (Left)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="96716-181"><dt><span></span><span></span><strong></strong> (Überlappung)</span><span class="sxs-lookup"><span data-stu-id="96716-181"><dt><span></span><span></span><strong></strong> (Overlap)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="96716-182"><dt><span></span><span></span><strong></strong> (Rechts)</span><span class="sxs-lookup"><span data-stu-id="96716-182"><dt><span></span><span></span><strong></strong> (Right)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="96716-183"><dt><span></span><span></span><strong></strong> (Oben)</span><span class="sxs-lookup"><span data-stu-id="96716-183"><dt><span></span><span></span><strong></strong> (Top)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96716-184"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="96716-184"><strong>Type</strong></span></span><br/></td>
<td><span data-ttu-id="96716-185">xs:string</span><span class="sxs-lookup"><span data-stu-id="96716-185">xs:string</span></span><br/></td>
<td><span data-ttu-id="96716-186">Nein</span><span class="sxs-lookup"><span data-stu-id="96716-186">No</span></span><br/></td>
<td><span data-ttu-id="96716-187">Auf einen der folgenden Werte beschränkt:</span><span class="sxs-lookup"><span data-stu-id="96716-187">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="96716-188">
<dt><span></span><span></span><strong></strong> (Elemente)</span><span class="sxs-lookup"><span data-stu-id="96716-188">
<dt><span></span><span></span><strong></strong> (Items)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="96716-189"><dt><span></span><span></span><strong></strong> (Befehle)</span><span class="sxs-lookup"><span data-stu-id="96716-189"><dt><span></span><span></span><strong></strong> (Commands)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="96716-190">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="96716-190">Child elements</span></span>



| <span data-ttu-id="96716-191">Element</span><span class="sxs-lookup"><span data-stu-id="96716-191">Element</span></span>                                                                                           | <span data-ttu-id="96716-192">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96716-192">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="96716-193">**Checkbox**</span><span class="sxs-lookup"><span data-stu-id="96716-193">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                                     | <span data-ttu-id="96716-194">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="96716-194">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="96716-195">**InRibbonGallery.MenuGroups**</span><span class="sxs-lookup"><span data-stu-id="96716-195">**InRibbonGallery.MenuGroups**</span></span>](windowsribbon-element-inribbongallery-menugroups.md)<br/> | <span data-ttu-id="96716-196">Muss genau einmal auftreten</span><span class="sxs-lookup"><span data-stu-id="96716-196">Must occur exactly once</span></span><br/> <br/>     |
| [<span data-ttu-id="96716-197">**InRibbonGallery.MenuLayout**</span><span class="sxs-lookup"><span data-stu-id="96716-197">**InRibbonGallery.MenuLayout**</span></span>](windowsribbon-element-inribbongallery-menulayout.md)<br/> | <span data-ttu-id="96716-198">Kann nur einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="96716-198">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="96716-199">**Schaltfläche**</span><span class="sxs-lookup"><span data-stu-id="96716-199">**Button**</span></span>](windowsribbon-element-button.md)<br/>                                       | <span data-ttu-id="96716-200">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="96716-200">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="96716-201">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="96716-201">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                               | <span data-ttu-id="96716-202">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="96716-202">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="96716-203">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="96716-203">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>                             | <span data-ttu-id="96716-204">Kann ein oder mehrere Male auftreten.</span><span class="sxs-lookup"><span data-stu-id="96716-204">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="96716-205">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="96716-205">Parent elements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="96716-206">Element</span><span class="sxs-lookup"><span data-stu-id="96716-206">Element</span></span></th>
<th><span data-ttu-id="96716-207">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96716-207">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96716-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span><span class="sxs-lookup"><span data-stu-id="96716-208"><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="96716-209"><a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a></span><span class="sxs-lookup"><span data-stu-id="96716-209"><a href="windowsribbon-element-group.md"><strong>Group</strong></a></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="96716-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span><span class="sxs-lookup"><span data-stu-id="96716-210"><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="96716-211">Windows 8 und neuer.</span><span class="sxs-lookup"><span data-stu-id="96716-211">Windows 8 and newer.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="96716-212">Hinweise</span><span class="sxs-lookup"><span data-stu-id="96716-212">Remarks</span></span>

<span data-ttu-id="96716-213">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="96716-213">Optional.</span></span>

<span data-ttu-id="96716-214">Kann höchstens einmal für jedes [**ControlGroup-**](windowsribbon-element-controlgroup.md) oder [**Group-Element**](windowsribbon-element-group.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="96716-214">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

<span data-ttu-id="96716-215">Der folgende Screenshot veranschaulicht das [Menüband-In-Ribbon Gallery-Steuerelement](windowsribbon-controls-inribbongallery.md) in Microsoft Paint für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="96716-215">The following screen shot illustrates the Ribbon [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control in Microsoft Paint for Windows 7.</span></span>

![Screenshot eines Katalog-Steuerelements im Menüband im Microsoft-Farbband.](images/controls/inribbongallery.png)

## <a name="examples"></a><span data-ttu-id="96716-217">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96716-217">Examples</span></span>

<span data-ttu-id="96716-218">Im folgenden Beispiel wird das grundlegende Markup für einen [Katalog im Menüband](windowsribbon-controls-inribbongallery.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="96716-218">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="96716-219">Dieser Codeabschnitt zeigt die **InRibbonGallery-Befehlsdeklarationen** mit einer zugeordneten [**Gruppe,**](windowsribbon-element-group.md) die als übergeordneter Container für das **InRibbonGallery-Element** fungiert.</span><span class="sxs-lookup"><span data-stu-id="96716-219">This section of code shows the **InRibbonGallery** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **InRibbonGallery** element.</span></span>


```XML
<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"/>
```



<span data-ttu-id="96716-220">Dieser Codeabschnitt zeigt die **InRibbonGallery-Steuerelementdeklarationen.**</span><span class="sxs-lookup"><span data-stu-id="96716-220">This section of code shows the **InRibbonGallery** control declarations.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="96716-221">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="96716-221">Element information</span></span>


* <span data-ttu-id="96716-222">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="96716-222">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="96716-223">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="96716-223">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="96716-224">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96716-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96716-225">Katalogsteuerelement im Menüband</span><span class="sxs-lookup"><span data-stu-id="96716-225">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="96716-226">Arbeiten mit Katalogen</span><span class="sxs-lookup"><span data-stu-id="96716-226">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="96716-227">Katalogbeispiel</span><span class="sxs-lookup"><span data-stu-id="96716-227">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





