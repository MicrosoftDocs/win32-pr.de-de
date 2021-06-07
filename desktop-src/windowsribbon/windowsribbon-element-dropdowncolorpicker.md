---
title: DropDownColorPicker-Element
description: Stellt ein Drop-Down Farbauswahlsteuerfeld dar, das beim Klicken eine Palette von Farbmustern anzeigt.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- DropDownColorPicker-Element Windows-Menüband
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce2fd1d9ff12b56d87955304fad24af23209ff91
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442901"
---
# <a name="dropdowncolorpicker-element"></a><span data-ttu-id="d2f32-104">DropDownColorPicker-Element</span><span class="sxs-lookup"><span data-stu-id="d2f32-104">DropDownColorPicker element</span></span>

<span data-ttu-id="d2f32-105">Stellt ein [Dropdown-Farbwähler-Steuerelement](windowsribbon-controls-dropdowncolorpicker.md)dar, das beim Klicken eine Palette von Farbüberwachungen anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d2f32-105">Represents a [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md)control that when clicked displays a palette of color swatches.</span></span>

## <a name="usage"></a><span data-ttu-id="d2f32-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="d2f32-106">Usage</span></span>

``` syntax
<DropDownColorPicker
  CommandName = "xs:positiveInteger or xs:string"
  Columns = "xs:positiveInteger"
  ThemeColorGridRows = "xs:positiveInteger"
  StandardColorGridRows = "xs:positiveInteger"
  RecentColorGridRows = "xs:positiveInteger"
  IsAutomaticColorButtonVisible = "Boolean"
  IsNoColorButtonVisible = "Boolean"
  ColorTemplate = "xs:string"
  ChipSize = "xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="d2f32-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="d2f32-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d2f32-108">attribute</span><span class="sxs-lookup"><span data-stu-id="d2f32-108">Attribute</span></span></th>
<th><span data-ttu-id="d2f32-109">Typ</span><span class="sxs-lookup"><span data-stu-id="d2f32-109">Type</span></span></th>
<th><span data-ttu-id="d2f32-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d2f32-110">Required</span></span></th>
<th><span data-ttu-id="d2f32-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2f32-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d2f32-112"><strong>ChipSize</strong></span><span class="sxs-lookup"><span data-stu-id="d2f32-112"><strong>ChipSize</strong></span></span><br/></td>
<td><span data-ttu-id="d2f32-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="d2f32-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="d2f32-114">Nein</span><span class="sxs-lookup"><span data-stu-id="d2f32-114">No</span></span><br/></td>
<td><span data-ttu-id="d2f32-115">Die Größe der einzelnen Farbchips oder Farbwatches.</span><span class="sxs-lookup"><span data-stu-id="d2f32-115">The size of each color chip or swatch.</span></span> <br/> <span data-ttu-id="d2f32-116">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="d2f32-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="d2f32-117">
<dt><span></span><span></span><strong></strong> (Klein)</span><span class="sxs-lookup"><span data-stu-id="d2f32-117">
<dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="d2f32-118">Jeder Farbchip ist ein Quadrat mit 11 x 11 Pixeln.</span><span class="sxs-lookup"><span data-stu-id="d2f32-118">Each color chip is an 11x11 pixel square.</span></span> <br/> </dd> <span data-ttu-id="d2f32-119"><dt><span></span><span></span><strong></strong> (Mittel)</span><span class="sxs-lookup"><span data-stu-id="d2f32-119"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="d2f32-120">Jeder Farbchip ist ein Quadrat mit 16 x 16 Pixeln.</span><span class="sxs-lookup"><span data-stu-id="d2f32-120">Each color chip is a 16x16 pixel square.</span></span> <br/> </dd> <span data-ttu-id="d2f32-121"><dt><span></span><span></span><strong></strong> (Groß)</span><span class="sxs-lookup"><span data-stu-id="d2f32-121"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="d2f32-122">Jeder Farbchip ist ein Quadrat mit 24 x 24 Pixeln.</span><span class="sxs-lookup"><span data-stu-id="d2f32-122">Each color chip is a 24x24 pixel square.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2f32-123"><strong>ColorTemplate</strong></span><span class="sxs-lookup"><span data-stu-id="d2f32-123"><strong>ColorTemplate</strong></span></span><br/></td>
<td><span data-ttu-id="d2f32-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="d2f32-124">xs:string</span></span><br/></td>
<td><span data-ttu-id="d2f32-125">Nein</span><span class="sxs-lookup"><span data-stu-id="d2f32-125">No</span></span><br/></td>
<td><span data-ttu-id="d2f32-126">Layoutvorlagen, die den Typ der <a href="windowsribbon-controls-dropdowncolorpicker.md">Dropdown-Farbwähler</a>angeben.</span><span class="sxs-lookup"><span data-stu-id="d2f32-126">Layout templates that specify the type of <a href="windowsribbon-controls-dropdowncolorpicker.md">Drop-Down Color Picker</a>.</span></span> <br/> <span data-ttu-id="d2f32-127">Beschränkt auf einen der folgenden Werte (wenn keine optionalen Attribute im Zusammenhang mit einer <em>ColorTemplate</em> deklariert werden, wird die Standardansicht angezeigt):</span><span class="sxs-lookup"><span data-stu-id="d2f32-127">Restricted to one of the following values (if no optional attributes related to a <em>ColorTemplate</em> are declared, the default view is shown):</span></span><br/> <br/><span data-ttu-id="d2f32-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span><span class="sxs-lookup"><span data-stu-id="d2f32-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span></span><br/> </dt> <dd> <span data-ttu-id="d2f32-129">Standard.</span><span class="sxs-lookup"><span data-stu-id="d2f32-129">Default.</span></span> <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> <span data-ttu-id="d2f32-130">Das Festlegen des <em>ColorTemplate-Attributs</em> auf <code>ThemeColors</code> ermöglicht die folgende Funktionalität:</span><span class="sxs-lookup"><span data-stu-id="d2f32-130">Setting the <em>ColorTemplate</em> attribute to <code>ThemeColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="d2f32-131">SplitButton-Anker.</span><span class="sxs-lookup"><span data-stu-id="d2f32-131">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="d2f32-132">Die <strong>automatische</strong> Farbschaltfläche wird standardmäßig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2f32-132"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="d2f32-133"><strong>Fensterdesignfarben–</strong> Farbmusterraster.</span><span class="sxs-lookup"><span data-stu-id="d2f32-133">Windows <strong>Theme colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="d2f32-134"><strong>Standardfarben–</strong> Musterraster.</span><span class="sxs-lookup"><span data-stu-id="d2f32-134"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="d2f32-135">Das Farbmusterraster <strong>"Zuletzt verwendet"</strong> ist optional.</span><span class="sxs-lookup"><span data-stu-id="d2f32-135"><strong>Recent Colors</strong> swatch grid is optional.</span></span></li>
<li><span data-ttu-id="d2f32-136"><strong>Dialogfeldstartfeld "Weitere Farben".</strong></span><span class="sxs-lookup"><span data-stu-id="d2f32-136"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="d2f32-137">Standardmäßig wird <strong>keine Farbfarbe</strong> angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2f32-137"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="d2f32-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span><span class="sxs-lookup"><span data-stu-id="d2f32-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> <span data-ttu-id="d2f32-139">Das Festlegen des <em>ColorTemplate-Attributs</em> auf <code>StandardColors</code> ermöglicht die folgende Funktionalität:</span><span class="sxs-lookup"><span data-stu-id="d2f32-139">Setting the <em>ColorTemplate</em> attribute to <code>StandardColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="d2f32-140">SplitButton-Anker.</span><span class="sxs-lookup"><span data-stu-id="d2f32-140">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="d2f32-141">Die <strong>automatische</strong> Farbschaltfläche wird standardmäßig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2f32-141"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="d2f32-142"><strong>Standardfarben–</strong> Musterraster.</span><span class="sxs-lookup"><span data-stu-id="d2f32-142"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="d2f32-143"><strong>Dialogfeldstartfeld "Weitere Farben".</strong></span><span class="sxs-lookup"><span data-stu-id="d2f32-143"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="d2f32-144">Standardmäßig wird <strong>keine Farbfarbe</strong> angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2f32-144"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="d2f32-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span><span class="sxs-lookup"><span data-stu-id="d2f32-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> <span data-ttu-id="d2f32-146">Das Festlegen des <em>ColorTemplate-Attributs</em> auf <code>HighlightColors</code> ermöglicht die folgende Funktionalität:</span><span class="sxs-lookup"><span data-stu-id="d2f32-146">Setting the <em>ColorTemplate</em> attribute to <code>HighlightColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="d2f32-147">SplitButton-Anker.</span><span class="sxs-lookup"><span data-stu-id="d2f32-147">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="d2f32-148">Musterraster für <strong>Standardfarben</strong> ohne Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="d2f32-148"><strong>Standard colors</strong> swatch grid with no header.</span></span></li>
<li><span data-ttu-id="d2f32-149">Standardmäßig wird <strong>keine Farbfarbe</strong> angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d2f32-149"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2f32-150"><strong>Spalten</strong></span><span class="sxs-lookup"><span data-stu-id="d2f32-150"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="d2f32-151">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d2f32-151">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d2f32-152">Nein</span><span class="sxs-lookup"><span data-stu-id="d2f32-152">No</span></span><br/></td>
<td><span data-ttu-id="d2f32-153">Die Anzahl der Farbchipspalten (oder Farbmusterspalten).</span><span class="sxs-lookup"><span data-stu-id="d2f32-153">The number of color chip (or swatch) columns.</span></span><br/> <br/><span data-ttu-id="d2f32-154">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="d2f32-154">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d2f32-155">Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 einschließlich.</span><span class="sxs-lookup"><span data-stu-id="d2f32-155">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2f32-156"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="d2f32-156"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="d2f32-157">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="d2f32-157">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="d2f32-158">Nein</span><span class="sxs-lookup"><span data-stu-id="d2f32-158">No</span></span><br/></td>
<td><span data-ttu-id="d2f32-159">Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="d2f32-159">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="d2f32-160">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="d2f32-160">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d2f32-161">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999 einschließlich oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="d2f32-161">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="d2f32-162">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d2f32-162">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="d2f32-163">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d2f32-163">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2f32-164"><strong>IsAutomaticColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="d2f32-164"><strong>IsAutomaticColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="d2f32-165">Boolesch</span><span class="sxs-lookup"><span data-stu-id="d2f32-165">Boolean</span></span><br/></td>
<td><span data-ttu-id="d2f32-166">Nein</span><span class="sxs-lookup"><span data-stu-id="d2f32-166">No</span></span><br/></td>
<td><span data-ttu-id="d2f32-167">Zeigt die Schaltfläche <strong>Automatische</strong> Farbe an (oder blendet sie aus).</span><span class="sxs-lookup"><span data-stu-id="d2f32-167">Displays (or hides) the <strong>Automatic</strong> color button.</span></span> <br/> <span data-ttu-id="d2f32-168">Nur gültig, wenn <code>StandardColors</code> oder <code>ThemeColors</code> für das <em>ColorTemplate-Attribut</em> angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d2f32-168">Valid only when <code>StandardColors</code> or <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span> <br/> <span data-ttu-id="d2f32-169">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="d2f32-169">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="d2f32-170">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="d2f32-170">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d2f32-171"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="d2f32-171"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2f32-172"><strong>IsNoColorButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="d2f32-172"><strong>IsNoColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="d2f32-173">Boolesch</span><span class="sxs-lookup"><span data-stu-id="d2f32-173">Boolean</span></span><br/></td>
<td><span data-ttu-id="d2f32-174">Nein</span><span class="sxs-lookup"><span data-stu-id="d2f32-174">No</span></span><br/></td>
<td><span data-ttu-id="d2f32-175">Zeigt die Schaltfläche <strong>Keine Farbe</strong> an (oder blendet sie aus).</span><span class="sxs-lookup"><span data-stu-id="d2f32-175">Displays (or hides) the <strong>No color</strong> button.</span></span> <br/> <span data-ttu-id="d2f32-176">Gültig für alle <em>ColorTemplate-Werte.</em></span><span class="sxs-lookup"><span data-stu-id="d2f32-176">Valid for all <em>ColorTemplate</em> values.</span></span><br/> <span data-ttu-id="d2f32-177">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="d2f32-177">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="d2f32-178">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="d2f32-178">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d2f32-179"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="d2f32-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2f32-180"><strong>RecentColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="d2f32-180"><strong>RecentColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="d2f32-181">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d2f32-181">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d2f32-182">Nein</span><span class="sxs-lookup"><span data-stu-id="d2f32-182">No</span></span><br/></td>
<td><span data-ttu-id="d2f32-183">Die Anzahl von Farbchipzeilen (oder Farbmusterzeilen) im Bereich <strong>Zuletzt verwendeter Farben.</strong></span><span class="sxs-lookup"><span data-stu-id="d2f32-183">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span> <br/> <span data-ttu-id="d2f32-184">Nur gültig, wenn <code>ThemeColors</code> für das <em>ColorTemplate-Attribut</em> angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d2f32-184">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="d2f32-185">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="d2f32-185">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d2f32-186">Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 einschließlich.</span><span class="sxs-lookup"><span data-stu-id="d2f32-186">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2f32-187"><strong>StandardColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="d2f32-187"><strong>StandardColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="d2f32-188">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d2f32-188">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d2f32-189">Nein</span><span class="sxs-lookup"><span data-stu-id="d2f32-189">No</span></span><br/></td>
<td><span data-ttu-id="d2f32-190">Die Anzahl von Farbchipzeilen (oder Farbmusterzeilen) im <strong>Bereich Standardfarben.</strong></span><span class="sxs-lookup"><span data-stu-id="d2f32-190">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/> <br/><span data-ttu-id="d2f32-191">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="d2f32-191">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d2f32-192">Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 einschließlich.</span><span class="sxs-lookup"><span data-stu-id="d2f32-192">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2f32-193"><strong>ThemeColorGridRows</strong></span><span class="sxs-lookup"><span data-stu-id="d2f32-193"><strong>ThemeColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="d2f32-194">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d2f32-194">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d2f32-195">Nein</span><span class="sxs-lookup"><span data-stu-id="d2f32-195">No</span></span><br/></td>
<td><span data-ttu-id="d2f32-196">Die Anzahl von Farbchipzeilen (oder Farbmusterzeilen) im Bereich <strong>Designfarben.</strong></span><span class="sxs-lookup"><span data-stu-id="d2f32-196">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="d2f32-197">Nur gültig, wenn <code>ThemeColors</code> für das <em>ColorTemplate-Attribut</em> angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d2f32-197">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="d2f32-198">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="d2f32-198">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d2f32-199">Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 einschließlich.</span><span class="sxs-lookup"><span data-stu-id="d2f32-199">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d2f32-200">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d2f32-200">Child elements</span></span>

<span data-ttu-id="d2f32-201">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="d2f32-201">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d2f32-202">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d2f32-202">Parent elements</span></span>



| <span data-ttu-id="d2f32-203">Element</span><span class="sxs-lookup"><span data-stu-id="d2f32-203">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="d2f32-204">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="d2f32-204">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="d2f32-205">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="d2f32-205">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>         |
| [<span data-ttu-id="d2f32-206">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="d2f32-206">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="d2f32-207">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="d2f32-207">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="d2f32-208">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="d2f32-208">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="d2f32-209">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="d2f32-209">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="d2f32-210">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="d2f32-210">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d2f32-211">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d2f32-211">Remarks</span></span>

<span data-ttu-id="d2f32-212">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d2f32-212">Optional.</span></span>

<span data-ttu-id="d2f32-213">Kann ein oder mehrere Male für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) [**DropDownButton-,**](windowsribbon-element-dropdownbutton.md) [**DropDownGallery-,**](windowsribbon-element-dropdowngallery.md) [**Group-,**](windowsribbon-element-group.md) [**MenuGroup-,**](windowsribbon-element-menugroup.md) [**SplitButton-**](windowsribbon-element-splitbutton.md)oder [**SplitButtonGallery-Element**](windowsribbon-element-splitbuttongallery.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="d2f32-213">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="d2f32-214">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2f32-214">Examples</span></span>

<span data-ttu-id="d2f32-215">Im folgenden Beispiel wird das grundlegende Markup für alle drei Typen von [Dropdown-Farbwähler.](windowsribbon-controls-dropdowncolorpicker.md)</span><span class="sxs-lookup"><span data-stu-id="d2f32-215">The following example demonstrates the basic markup for all three types of [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="d2f32-216">Dieser Codeabschnitt zeigt die Befehlsdeklarationen für drei **DropDownColorPicker-Elemente.**</span><span class="sxs-lookup"><span data-stu-id="d2f32-216">This section of code shows the Command declarations for three **DropDownColorPicker** elements.</span></span>


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```



<span data-ttu-id="d2f32-217">Dieser Codeabschnitt zeigt die drei Typen von **DropDownColorPicker-Steuerelementdeklarationen.**</span><span class="sxs-lookup"><span data-stu-id="d2f32-217">This section of code shows the three types of **DropDownColorPicker** control declarations.</span></span>


```XML
<Group CommandName="cmdDropDownColorPickerGroup"
       SizeDefinition="ThreeButtons">
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerThemeColors"
    ColorTemplate="ThemeColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerStandardColors"
    ColorTemplate="StandardColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerHighlightColors"
    ColorTemplate="HighlightColors"
    StandardColorGridRows="1"/>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="d2f32-218">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d2f32-218">Element information</span></span>

* <span data-ttu-id="d2f32-219">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="d2f32-219">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="d2f32-220">**Kann leer sein:** Ja</span><span class="sxs-lookup"><span data-stu-id="d2f32-220">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="d2f32-221">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2f32-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f32-222">Dropdown-Farbwähler Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d2f32-222">Drop-Down Color Picker control</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="d2f32-223">DropDownColorPicker-Beispiel</span><span class="sxs-lookup"><span data-stu-id="d2f32-223">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





