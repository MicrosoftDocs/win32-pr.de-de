---
title: Dropdowncolorpicker-Element
description: Stellt ein Drop-Down Color pickercontrol dar, das beim Klicken auf eine Palette von farbsuhren zeigt.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- Windows-Menüband für dropdowncolorpicker-Element
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 00185d14d9066b2cb85da4b23959e84df1827007
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "103720489"
---
# <a name="dropdowncolorpicker-element"></a><span data-ttu-id="d6639-104">Dropdowncolorpicker-Element</span><span class="sxs-lookup"><span data-stu-id="d6639-104">DropDownColorPicker element</span></span>

<span data-ttu-id="d6639-105">Stellt ein [Dropdown-Farbauswahl](windowsribbon-controls-dropdowncolorpicker.md)Steuerelement dar, das beim Klicken auf eine Palette von farbsuhren zeigt.</span><span class="sxs-lookup"><span data-stu-id="d6639-105">Represents a [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md)control that when clicked displays a palette of color swatches.</span></span>

## <a name="usage"></a><span data-ttu-id="d6639-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="d6639-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="d6639-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="d6639-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6639-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="d6639-108">Attribute</span></span></th>
<th><span data-ttu-id="d6639-109">type</span><span class="sxs-lookup"><span data-stu-id="d6639-109">Type</span></span></th>
<th><span data-ttu-id="d6639-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d6639-110">Required</span></span></th>
<th><span data-ttu-id="d6639-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6639-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d6639-112"><strong>Chipgröße</strong></span><span class="sxs-lookup"><span data-stu-id="d6639-112"><strong>ChipSize</strong></span></span><br/></td>
<td><span data-ttu-id="d6639-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="d6639-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="d6639-114">Nein</span><span class="sxs-lookup"><span data-stu-id="d6639-114">No</span></span><br/></td>
<td><span data-ttu-id="d6639-115">Die Größe jedes Farbchips oder eines Musters.</span><span class="sxs-lookup"><span data-stu-id="d6639-115">The size of each color chip or swatch.</span></span> <br/> <span data-ttu-id="d6639-116">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="d6639-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="d6639-117">
<dt><span></span><span></span><strong></strong> Zuletzt</span><span class="sxs-lookup"><span data-stu-id="d6639-117">
<dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="d6639-118">Jeder farbchip ist ein 11x11-Pixel Quadrat.</span><span class="sxs-lookup"><span data-stu-id="d6639-118">Each color chip is an 11x11 pixel square.</span></span> <br/> </dd> <span data-ttu-id="d6639-119"><dt><span></span><span></span><strong></strong> Mittelalter</span><span class="sxs-lookup"><span data-stu-id="d6639-119"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd> <span data-ttu-id="d6639-120">Jeder farbchip ist ein 16x16-Pixel Quadrat.</span><span class="sxs-lookup"><span data-stu-id="d6639-120">Each color chip is a 16x16 pixel square.</span></span> <br/> </dd> <span data-ttu-id="d6639-121"><dt><span></span><span></span><strong></strong> Viele</span><span class="sxs-lookup"><span data-stu-id="d6639-121"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd> <span data-ttu-id="d6639-122">Jeder farbchip ist ein rund um die Uhr großes Pixel Quadrat.</span><span class="sxs-lookup"><span data-stu-id="d6639-122">Each color chip is a 24x24 pixel square.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6639-123"><strong>Colortemplate</strong></span><span class="sxs-lookup"><span data-stu-id="d6639-123"><strong>ColorTemplate</strong></span></span><br/></td>
<td><span data-ttu-id="d6639-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="d6639-124">xs:string</span></span><br/></td>
<td><span data-ttu-id="d6639-125">Nein</span><span class="sxs-lookup"><span data-stu-id="d6639-125">No</span></span><br/></td>
<td><span data-ttu-id="d6639-126">Layoutvorlagen, die den Typ der <a href="windowsribbon-controls-dropdowncolorpicker.md">Dropdown-Farbauswahl</a>angeben.</span><span class="sxs-lookup"><span data-stu-id="d6639-126">Layout templates that specify the type of <a href="windowsribbon-controls-dropdowncolorpicker.md">Drop-Down Color Picker</a>.</span></span> <br/> <span data-ttu-id="d6639-127">Auf einen der folgenden Werte beschränkt (wenn keine optionalen Attribute, die sich auf eine <em>colortemplate</em> beziehen, deklariert sind, wird die Standardansicht angezeigt):</span><span class="sxs-lookup"><span data-stu-id="d6639-127">Restricted to one of the following values (if no optional attributes related to a <em>ColorTemplate</em> are declared, the default view is shown):</span></span><br/> <br/><span data-ttu-id="d6639-128">
<dt><span></span><span></span><strong></strong> (Mecolors)</span><span class="sxs-lookup"><span data-stu-id="d6639-128">
<dt><span></span><span></span><strong></strong> (ThemeColors)</span></span><br/> </dt> <dd> <span data-ttu-id="d6639-129">Standard.</span><span class="sxs-lookup"><span data-stu-id="d6639-129">Default.</span></span> <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> <span data-ttu-id="d6639-130">Durch Festlegen des <em>colortemplate</em> -Attributs auf werden <code>ThemeColors</code> die folgenden Funktionen aktiviert:</span><span class="sxs-lookup"><span data-stu-id="d6639-130">Setting the <em>ColorTemplate</em> attribute to <code>ThemeColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="d6639-131">SplitButton-Anker.</span><span class="sxs-lookup"><span data-stu-id="d6639-131">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="d6639-132">Standardmäßig wird die <strong>Automatische</strong> Farb Schaltfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6639-132"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="d6639-133">Fensterdesign <strong>Farben</strong> -Muster Raster.</span><span class="sxs-lookup"><span data-stu-id="d6639-133">Windows <strong>Theme colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="d6639-134">Muster Raster für <strong>Standard Farben</strong> .</span><span class="sxs-lookup"><span data-stu-id="d6639-134"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="d6639-135"><strong>Aktuelles Farb</strong> Muster Raster ist optional.</span><span class="sxs-lookup"><span data-stu-id="d6639-135"><strong>Recent Colors</strong> swatch grid is optional.</span></span></li>
<li><span data-ttu-id="d6639-136">Dialogfeld " <strong>Weitere Farben</strong> ".</span><span class="sxs-lookup"><span data-stu-id="d6639-136"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="d6639-137">Standardmäßig wird <strong>keine Farb</strong> Farb Schaltfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6639-137"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="d6639-138"><dt><span></span><span></span><strong></strong> (Standardcolors)</span><span class="sxs-lookup"><span data-stu-id="d6639-138"><dt><span></span><span></span><strong></strong> (StandardColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> <span data-ttu-id="d6639-139">Durch Festlegen des <em>colortemplate</em> -Attributs auf werden <code>StandardColors</code> die folgenden Funktionen aktiviert:</span><span class="sxs-lookup"><span data-stu-id="d6639-139">Setting the <em>ColorTemplate</em> attribute to <code>StandardColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="d6639-140">SplitButton-Anker.</span><span class="sxs-lookup"><span data-stu-id="d6639-140">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="d6639-141">Standardmäßig wird die <strong>Automatische</strong> Farb Schaltfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6639-141"><strong>Automatic</strong> color button is displayed by default.</span></span></li>
<li><span data-ttu-id="d6639-142">Muster Raster für <strong>Standard Farben</strong> .</span><span class="sxs-lookup"><span data-stu-id="d6639-142"><strong>Standard colors</strong> swatch grid.</span></span></li>
<li><span data-ttu-id="d6639-143">Dialogfeld " <strong>Weitere Farben</strong> ".</span><span class="sxs-lookup"><span data-stu-id="d6639-143"><strong>More colors</strong> dialog box launcher.</span></span></li>
<li><span data-ttu-id="d6639-144">Standardmäßig wird <strong>keine Farb</strong> Farb Schaltfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6639-144"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> <span data-ttu-id="d6639-145"><dt><span></span><span></span><strong></strong> (Highlightcolors)</span><span class="sxs-lookup"><span data-stu-id="d6639-145"><dt><span></span><span></span><strong></strong> (HighlightColors)</span></span><br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> <span data-ttu-id="d6639-146">Durch Festlegen des <em>colortemplate</em> -Attributs auf werden <code>HighlightColors</code> die folgenden Funktionen aktiviert:</span><span class="sxs-lookup"><span data-stu-id="d6639-146">Setting the <em>ColorTemplate</em> attribute to <code>HighlightColors</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="d6639-147">SplitButton-Anker.</span><span class="sxs-lookup"><span data-stu-id="d6639-147">SplitButton anchor.</span></span></li>
<li><span data-ttu-id="d6639-148">Muster Raster mit <strong>Standard Farben</strong> ohne Header.</span><span class="sxs-lookup"><span data-stu-id="d6639-148"><strong>Standard colors</strong> swatch grid with no header.</span></span></li>
<li><span data-ttu-id="d6639-149">Standardmäßig wird <strong>keine Farb</strong> Farb Schaltfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d6639-149"><strong>No color</strong> color button is displayed by default.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6639-150"><strong>Spalten</strong></span><span class="sxs-lookup"><span data-stu-id="d6639-150"><strong>Columns</strong></span></span><br/></td>
<td><span data-ttu-id="d6639-151">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d6639-151">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d6639-152">Nein</span><span class="sxs-lookup"><span data-stu-id="d6639-152">No</span></span><br/></td>
<td><span data-ttu-id="d6639-153">Die Anzahl der farbchipspalten (oder Muster Spalten).</span><span class="sxs-lookup"><span data-stu-id="d6639-153">The number of color chip (or swatch) columns.</span></span><br/> <br/><span data-ttu-id="d6639-154">
<dt><span></span><span></span><strong></strong> (xs: positivin teger)</span><span class="sxs-lookup"><span data-stu-id="d6639-154">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d6639-155">Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="d6639-155">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6639-156"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="d6639-156"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="d6639-157">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="d6639-157">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="d6639-158">Nein</span><span class="sxs-lookup"><span data-stu-id="d6639-158">No</span></span><br/></td>
<td><span data-ttu-id="d6639-159">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="d6639-159">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="d6639-160">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="d6639-160">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="d6639-161">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="d6639-161">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="d6639-162">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d6639-162">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="d6639-163">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d6639-163">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6639-164"><strong>Isautomaticcolorbuttonvisible</strong></span><span class="sxs-lookup"><span data-stu-id="d6639-164"><strong>IsAutomaticColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="d6639-165">Boolesch</span><span class="sxs-lookup"><span data-stu-id="d6639-165">Boolean</span></span><br/></td>
<td><span data-ttu-id="d6639-166">Nein</span><span class="sxs-lookup"><span data-stu-id="d6639-166">No</span></span><br/></td>
<td><span data-ttu-id="d6639-167">Zeigt die <strong>Automatische</strong> Farb Schaltfläche an oder blendet sie aus.</span><span class="sxs-lookup"><span data-stu-id="d6639-167">Displays (or hides) the <strong>Automatic</strong> color button.</span></span> <br/> <span data-ttu-id="d6639-168">Nur gültig, wenn <code>StandardColors</code> oder <code>ThemeColors</code> für das <em>colortemplate</em> -Attribut angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d6639-168">Valid only when <code>StandardColors</code> or <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span> <br/> <span data-ttu-id="d6639-169">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="d6639-169">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="d6639-170">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="d6639-170">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d6639-171"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="d6639-171"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6639-172"><strong>Isnocolorbuttonvisible</strong></span><span class="sxs-lookup"><span data-stu-id="d6639-172"><strong>IsNoColorButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="d6639-173">Boolesch</span><span class="sxs-lookup"><span data-stu-id="d6639-173">Boolean</span></span><br/></td>
<td><span data-ttu-id="d6639-174">Nein</span><span class="sxs-lookup"><span data-stu-id="d6639-174">No</span></span><br/></td>
<td><span data-ttu-id="d6639-175">Zeigt die Schaltfläche <strong>keine Farbe</strong> an (oder blendet sie aus).</span><span class="sxs-lookup"><span data-stu-id="d6639-175">Displays (or hides) the <strong>No color</strong> button.</span></span> <br/> <span data-ttu-id="d6639-176">Gültig für alle <em>colortemplate</em> -Werte.</span><span class="sxs-lookup"><span data-stu-id="d6639-176">Valid for all <em>ColorTemplate</em> values.</span></span><br/> <span data-ttu-id="d6639-177">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="d6639-177">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="d6639-178">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="d6639-178">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="d6639-179"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="d6639-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6639-180"><strong>Recentcolorgridrows</strong></span><span class="sxs-lookup"><span data-stu-id="d6639-180"><strong>RecentColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="d6639-181">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d6639-181">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d6639-182">Nein</span><span class="sxs-lookup"><span data-stu-id="d6639-182">No</span></span><br/></td>
<td><span data-ttu-id="d6639-183">Die Anzahl der farbchipzeilen (oder Muster Zeilen) im Bereich " <strong>Letzte Farben</strong> ".</span><span class="sxs-lookup"><span data-stu-id="d6639-183">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span> <br/> <span data-ttu-id="d6639-184">Nur gültig, wenn <code>ThemeColors</code> für das <em>colortemplate</em> -Attribut angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d6639-184">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="d6639-185">
<dt><span></span><span></span><strong></strong> (xs: positivin teger)</span><span class="sxs-lookup"><span data-stu-id="d6639-185">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d6639-186">Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="d6639-186">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d6639-187"><strong>Standardcolorgridrows</strong></span><span class="sxs-lookup"><span data-stu-id="d6639-187"><strong>StandardColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="d6639-188">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d6639-188">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d6639-189">Nein</span><span class="sxs-lookup"><span data-stu-id="d6639-189">No</span></span><br/></td>
<td><span data-ttu-id="d6639-190">Die Anzahl der farbchipzeilen (oder Muster Zeilen) im <strong>Standard Farben</strong> Bereich.</span><span class="sxs-lookup"><span data-stu-id="d6639-190">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/> <br/><span data-ttu-id="d6639-191">
<dt><span></span><span></span><strong></strong> (xs: positivin teger)</span><span class="sxs-lookup"><span data-stu-id="d6639-191">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d6639-192">Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="d6639-192">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d6639-193"><strong>"Mecolorgridrows"</strong></span><span class="sxs-lookup"><span data-stu-id="d6639-193"><strong>ThemeColorGridRows</strong></span></span><br/></td>
<td><span data-ttu-id="d6639-194">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="d6639-194">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="d6639-195">Nein</span><span class="sxs-lookup"><span data-stu-id="d6639-195">No</span></span><br/></td>
<td><span data-ttu-id="d6639-196">Die Anzahl der farbchipzeilen (oder Muster Zeilen) im Design <strong>Farben</strong> Bereich.</span><span class="sxs-lookup"><span data-stu-id="d6639-196">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="d6639-197">Nur gültig, wenn <code>ThemeColors</code> für das <em>colortemplate</em> -Attribut angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="d6639-197">Valid only when <code>ThemeColors</code> is specified for the <em>ColorTemplate</em> attribute.</span></span><br/> <br/><span data-ttu-id="d6639-198">
<dt><span></span><span></span><strong></strong> (xs: positivin teger)</span><span class="sxs-lookup"><span data-stu-id="d6639-198">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="d6639-199">Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="d6639-199">Any positive integer value between 1 and 256, inclusive.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="d6639-200">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6639-200">Child elements</span></span>

<span data-ttu-id="d6639-201">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="d6639-201">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d6639-202">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6639-202">Parent elements</span></span>



| <span data-ttu-id="d6639-203">Element</span><span class="sxs-lookup"><span data-stu-id="d6639-203">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="d6639-204">**Controlgroup**</span><span class="sxs-lookup"><span data-stu-id="d6639-204">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="d6639-205">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="d6639-205">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>         |
| [<span data-ttu-id="d6639-206">**Dropdown Gallery**</span><span class="sxs-lookup"><span data-stu-id="d6639-206">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="d6639-207">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="d6639-207">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="d6639-208">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="d6639-208">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="d6639-209">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="d6639-209">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="d6639-210">**Splitbuttongallery**</span><span class="sxs-lookup"><span data-stu-id="d6639-210">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d6639-211">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6639-211">Remarks</span></span>

<span data-ttu-id="d6639-212">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d6639-212">Optional.</span></span>

<span data-ttu-id="d6639-213">Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, [**DropDownButton**](windowsribbon-element-dropdownbutton.md)-, [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)-, [**Group**](windowsribbon-element-group.md)-, [**MenuGroup**](windowsribbon-element-menugroup.md)-, [**SplitButton**](windowsribbon-element-splitbutton.md)-oder [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Element einmal oder mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="d6639-213">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="d6639-214">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6639-214">Examples</span></span>

<span data-ttu-id="d6639-215">Im folgenden Beispiel wird das grundlegende Markup für alle drei Typen der [Dropdown-Farbauswahl](windowsribbon-controls-dropdowncolorpicker.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d6639-215">The following example demonstrates the basic markup for all three types of [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="d6639-216">Dieser Code Abschnitt zeigt die Befehls Deklarationen für drei **dropdowncolorpicker** -Elemente.</span><span class="sxs-lookup"><span data-stu-id="d6639-216">This section of code shows the Command declarations for three **DropDownColorPicker** elements.</span></span>


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



<span data-ttu-id="d6639-217">In diesem Code Abschnitt werden die drei Typen von **dropdowncolorpicker** -Steuerelement Deklarationen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d6639-217">This section of code shows the three types of **DropDownColorPicker** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="d6639-218">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d6639-218">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="d6639-219">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="d6639-219">Minimum supported system</span></span><br/> | <span data-ttu-id="d6639-220">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d6639-220">Windows 7</span></span> |
| <span data-ttu-id="d6639-221">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="d6639-221">Can be empty</span></span>                        | <span data-ttu-id="d6639-222">Ja</span><span class="sxs-lookup"><span data-stu-id="d6639-222">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="d6639-223">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6639-223">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6639-224">Dropdown-Farbauswahl-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d6639-224">Drop-Down Color Picker control</span></span>](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="d6639-225">Dropdowncolorpicker-Beispiel</span><span class="sxs-lookup"><span data-stu-id="d6639-225">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





