---
title: Drop-Down Farbwähler
description: Das Windows-Menübandframework bietet ein spezielles Drop-Down Farbwähler,das eine Vielzahl von Farbeinstellungen über eine Teilungsschaltfläche und einen anpassbaren Dropdownfarbwähler verfügbar macht.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366cc7eadaca23271d5b2afa43ec66235839694a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443661"
---
# <a name="drop-down-color-picker"></a><span data-ttu-id="3be00-103">Drop-Down Farbwähler</span><span class="sxs-lookup"><span data-stu-id="3be00-103">Drop-Down Color Picker</span></span>

<span data-ttu-id="3be00-104">Das Windows-Menübandframework bietet ein spezielles Drop-Down Farbwähler,das eine Vielzahl von Farbeinstellungen über eine Teilungsschaltfläche und einen anpassbaren Dropdownfarbwähler verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="3be00-104">The Windows Ribbon framework provides a specialized Drop-Down Color Picker control that exposes a variety of color settings through a split button and customizable drop-down color selector.</span></span>

-   [<span data-ttu-id="3be00-105">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="3be00-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="3be00-106">Markup</span><span class="sxs-lookup"><span data-stu-id="3be00-106">Markup</span></span>](#markup)
-   [<span data-ttu-id="3be00-107">Code</span><span class="sxs-lookup"><span data-stu-id="3be00-107">Code</span></span>](#code)
    -   [<span data-ttu-id="3be00-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3be00-108">Properties</span></span>](#properties)
    -   [<span data-ttu-id="3be00-109">Befehlshandler</span><span class="sxs-lookup"><span data-stu-id="3be00-109">Command handlers</span></span>](#command-handlers)
-   [<span data-ttu-id="3be00-110">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="3be00-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="3be00-111">Einführung</span><span class="sxs-lookup"><span data-stu-id="3be00-111">Introduction</span></span>

<span data-ttu-id="3be00-112">Durch emulieren der Darstellung und Funktionalität der Microsoft Office-Farbauswahl kann das Menübandframework sowohl von Konsistenz und Vertrautheit in einer Vielzahl von Anwendungen profitieren als auch zu dieser beitragen.</span><span class="sxs-lookup"><span data-stu-id="3be00-112">By emulating the appearance and functionality of the Microsoft Office color picker, the Ribbon framework is able to both benefit from, and contribute to, consistency and familiarity across a wide range of applications.</span></span>

## <a name="markup"></a><span data-ttu-id="3be00-113">Markup</span><span class="sxs-lookup"><span data-stu-id="3be00-113">Markup</span></span>

<span data-ttu-id="3be00-114">Wie alle Menübandsteuerelemente kann die Drop-Down Farbwähler einfach implementiert und über Markup angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="3be00-114">Like all Ribbon controls, the Drop-Down Color Picker is easily implemented and customized through markup.</span></span> <span data-ttu-id="3be00-115">Das Framework stellt eine Reihe von Elementattributen für die Drop-Down Farbwähler, um verschiedene Funktionalitätsebenen verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="3be00-115">The framework provides a number of element attributes for the Drop-Down Color Picker to expose various levels of functionality.</span></span> <span data-ttu-id="3be00-116">In der folgenden Tabelle sind die Drop-Down Farbwähler aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3be00-116">The following table lists the Drop-Down Color Picker attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3be00-117">attribute</span><span class="sxs-lookup"><span data-stu-id="3be00-117">Attribute</span></span></th>
<th><span data-ttu-id="3be00-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3be00-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3be00-119">ColorTemplate</span><span class="sxs-lookup"><span data-stu-id="3be00-119">ColorTemplate</span></span></td>
<td><span data-ttu-id="3be00-120">Layoutvorlagen, die den Typ der Drop-Down Farbwähler.</span><span class="sxs-lookup"><span data-stu-id="3be00-120">Layout templates that specify the type of Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="3be00-121">Es gibt drei Vorlagen, von denen jede ein Steuerelementlayout und Standardwerte für zugeordnete Attribute und Eigenschaftsschlüssel angibt.</span><span class="sxs-lookup"><span data-stu-id="3be00-121">There are three templates, each of which specifies a control layout and default values for associated attributes and property keys.</span></span> <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be00-122">ChipSize</span><span class="sxs-lookup"><span data-stu-id="3be00-122">ChipSize</span></span></td>
<td><span data-ttu-id="3be00-123">Die Größe der einzelnen Farbchips (oder Farbmuster).</span><span class="sxs-lookup"><span data-stu-id="3be00-123">The size of each color chip (or swatch).</span></span><br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be00-124">Spalten</span><span class="sxs-lookup"><span data-stu-id="3be00-124">Columns</span></span></td>
<td><span data-ttu-id="3be00-125">Die Anzahl der Farbchipspalten (oder Farbmusterspalten).</span><span class="sxs-lookup"><span data-stu-id="3be00-125">The number of color chip (or swatch) columns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be00-126">CommandName</span><span class="sxs-lookup"><span data-stu-id="3be00-126">CommandName</span></span></td>
<td><span data-ttu-id="3be00-127">Der Name der zugeordneten Befehlsdeklaration.</span><span class="sxs-lookup"><span data-stu-id="3be00-127">The name of the associated Command declaration.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be00-128">IsAutomaticColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="3be00-128">IsAutomaticColorButtonVisible</span></span></td>
<td><span data-ttu-id="3be00-129">Zeigt die Schaltfläche Automatisch an (oder <strong>blendet</strong> sie aus).</span><span class="sxs-lookup"><span data-stu-id="3be00-129">Displays (or hides) the <strong>Automatic</strong> button.</span></span><br/> <span data-ttu-id="3be00-130">Nur gültig, <em>wenn ColorTemplate</em> über den Wert <code>ThemeColors</code> oder <code>StandardColors</code> verfügt.</span><span class="sxs-lookup"><span data-stu-id="3be00-130">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be00-131">IsNoColorButtonVisible</span><span class="sxs-lookup"><span data-stu-id="3be00-131">IsNoColorButtonVisible</span></span></td>
<td><span data-ttu-id="3be00-132">Zeigt die Schaltfläche Keine Farbe an <strong>(oder blendet sie</strong> aus).</span><span class="sxs-lookup"><span data-stu-id="3be00-132">Displays (or hides) the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="3be00-133">Gültig für alle <em>ColorTemplate-Werte.</em></span><span class="sxs-lookup"><span data-stu-id="3be00-133">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be00-134">RecentColorGridRows</span><span class="sxs-lookup"><span data-stu-id="3be00-134">RecentColorGridRows</span></span></td>
<td><span data-ttu-id="3be00-135">Die Anzahl der Farbchipzeilen (oder Farbmuster) im <strong>Bereich Zuletzt verwendete</strong> Farben.</span><span class="sxs-lookup"><span data-stu-id="3be00-135">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span><br/> <span data-ttu-id="3be00-136">Nur gültig, <em>wenn ColorTemplate</em> über den Wert <code>ThemeColors</code> verfügt.</span><span class="sxs-lookup"><span data-stu-id="3be00-136">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be00-137">StandardColorGridRows</span><span class="sxs-lookup"><span data-stu-id="3be00-137">StandardColorGridRows</span></span></td>
<td><span data-ttu-id="3be00-138">Die Anzahl der Farbchipzeilen (oder Farbmuster) im <strong>Bereich Standardfarben.</strong></span><span class="sxs-lookup"><span data-stu-id="3be00-138">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be00-139">ThemeColorGridRows</span><span class="sxs-lookup"><span data-stu-id="3be00-139">ThemeColorGridRows</span></span></td>
<td><span data-ttu-id="3be00-140">Die Anzahl der Farbchipzeilen (oder Farbmuster) im <strong>Bereich Designfarben.</strong></span><span class="sxs-lookup"><span data-stu-id="3be00-140">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="3be00-141">Nur gültig, <em>wenn ColorTemplate</em> über den Wert <code>ThemeColors</code> verfügt.</span><span class="sxs-lookup"><span data-stu-id="3be00-141">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3be00-142">Die folgenden Screenshots veranschaulichen die Drop-Down Farbwähler Layouts für die drei Farbvorlagen.</span><span class="sxs-lookup"><span data-stu-id="3be00-142">The following screen shots illustrate the default Drop-Down Color Picker layouts for the three color templates.</span></span>



|     &nbsp;     |  &nbsp;   | &nbsp;  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3be00-143">`ThemeColors`: Screenshot des Dropdowncolorpicker-Elements mit dem Colortemplate-Attribut, das auf \[ \] ![ "themecolors" festgelegt ist. ](images/markup/colortemplate.themedcolors.1.png) \[ Zeilenumbruch\]</span><span class="sxs-lookup"><span data-stu-id="3be00-143">`ThemeColors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'themecolors'.](images/markup/colortemplate.themedcolors.1.png)\[newline\]</span></span> | <span data-ttu-id="3be00-144">`standardcolors`: \[ Screenshot des \] ![ Dropdowncolorpicker-Elements mit dem colortemplate-Attribut, das auf "standardcolors" festgelegt ist. ](images/markup/colortemplate.standardcolors.3.png) \[ Zeilenumbruch\]</span><span class="sxs-lookup"><span data-stu-id="3be00-144">`standardcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'standardcolors'.](images/markup/colortemplate.standardcolors.3.png)\[newline\]</span></span> | <span data-ttu-id="3be00-145">`highlightcolors`: Screenshot des Dropdowncolorpicker-Elements mit dem Colortemplate-Attribut, das auf \[ \] ![ "highlightcolors" festgelegt ist.](images/markup/colortemplate.highlightcolors.2.png)</span><span class="sxs-lookup"><span data-stu-id="3be00-145">`highlightcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)</span></span><br/> |



 

<span data-ttu-id="3be00-146">Das grundlegende Markup, das für jeden Drop-Down Farbwähler erforderlich ist, wird in den folgenden Beispielen gezeigt:</span><span class="sxs-lookup"><span data-stu-id="3be00-146">The basic markup required for each Drop-Down Color Picker type is demonstrated in the following examples:</span></span>

> [!Note]  
> <span data-ttu-id="3be00-147">Der Drop-Down Farbwähler ist ein gültiges [Button-Steuerelement](windowsribbon-controls-button.md) in einer [**SizeDefinition-Vorlage.**](windowsribbon-element-sizedefinition.md)</span><span class="sxs-lookup"><span data-stu-id="3be00-147">The Drop-Down Color Picker is a valid [Button](windowsribbon-controls-button.md) control in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

 


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


```XML

<Group CommandName=&quot;cmdDropDownColorPickerGroup&quot;
       SizeDefinition=&quot;ThreeButtons&quot;>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerThemeColors&quot;
    ColorTemplate=&quot;ThemeColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerStandardColors&quot;
    ColorTemplate=&quot;StandardColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerHighlightColors&quot;
    ColorTemplate=&quot;HighlightColors&quot;
    StandardColorGridRows=&quot;1&quot;/>
</Group>
```





## <a name="code"></a><span data-ttu-id="3be00-148">Code</span><span class="sxs-lookup"><span data-stu-id="3be00-148">Code</span></span>

<span data-ttu-id="3be00-149">Als spezialisiertes Steuerelement, das Anpassungen unterstützt, erfordert jede Implementierung der Drop-Down Farbwähler, die diese Funktionen nutzt, speziellen Anwendungscode, um Eigenschaften zu verwalten und alle vom Steuerelement ausgegebenen Befehle zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="3be00-149">As a specialized control that supports customization, any implemention of the Drop-Down Color Picker that takes advantage of these capabilities requires specialized application code to manage properties and handle any Commands issued by the control.</span></span>

### <a name="properties"></a><span data-ttu-id="3be00-150">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3be00-150">Properties</span></span>

<span data-ttu-id="3be00-151">Das Menübandframework definiert eine Auflistung von [Eigenschaftsschlüsseln für](windowsribbon-reference-properties.md) das Drop-Down Farbwähler Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="3be00-151">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Color Picker control.</span></span>

<span data-ttu-id="3be00-152">In der Regel wird eine Drop-Down Farbwähler-Eigenschaft in der Menübandbenutzeroberfläche aktualisiert, indem der befehl, der dem Steuerelement zugeordnet ist, durch einen Aufruf der [**IUIFramework::InvalidateUICommand-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="3be00-152">Typically, a Drop-Down Color Picker property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="3be00-153">Das Invalidierungsereignis wird von der [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) behandelt und die Eigenschaft aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3be00-153">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="3be00-154">Die [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird nicht ausgeführt, und die Anwendung fragt einen aktualisierten Eigenschaftswert ab, bis die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="3be00-154">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="3be00-155">Beispielsweise, wenn eine Registerkarte aktiviert und ein Steuerelement auf der Menübandbenutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3be00-155">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="3be00-156">In einigen Fällen kann eine Eigenschaft über die [**IUIFramework::GetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) abgerufen und mit der [**IUIFramework::SetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3be00-156">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="3be00-157">In der folgenden Tabelle sind die Eigenschaftenschlüssel aufgeführt, die dem Steuerelement Drop-Down Farbwähler sind.</span><span class="sxs-lookup"><span data-stu-id="3be00-157">The following table lists the property keys that are associated with the Drop-Down Color Picker control.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3be00-158">Eigenschaftsschlüssel</span><span class="sxs-lookup"><span data-stu-id="3be00-158">Property Key</span></span></th>
<th><span data-ttu-id="3be00-159">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3be00-159">Description</span></span></th>
<th><span data-ttu-id="3be00-160">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3be00-160">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3be00-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="3be00-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span></span></td>
<td><span data-ttu-id="3be00-162">Definiert die Bezeichnung für die Schaltfläche <strong>Automatische</strong> Farbe.</span><span class="sxs-lookup"><span data-stu-id="3be00-162">Defines the label for the <strong>Automatic</strong> color button.</span></span><br/> <span data-ttu-id="3be00-163">Nur gültig, <em>wenn ColorTemplate</em> über den Wert oder <code>ThemeColors</code> <code>StandardColors</code> verfügt.</span><span class="sxs-lookup"><span data-stu-id="3be00-163">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="3be00-164">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3be00-164">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be00-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span><span class="sxs-lookup"><span data-stu-id="3be00-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span></span></td>
<td><span data-ttu-id="3be00-166">Definiert den ausgewählten Farbwert als <a href="/windows/win32/gdi/colorref">COLORREF.</a></span><span class="sxs-lookup"><span data-stu-id="3be00-166">Defines the selected color value as a <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span></span><br/> <span data-ttu-id="3be00-167">Nur gültig, <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> den Wert <code>UI_SWATCHCOLORTYPE_RGB</code> hat.</span><span class="sxs-lookup"><span data-stu-id="3be00-167">Only valid when <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> has a value of <code>UI_SWATCHCOLORTYPE_RGB</code>.</span></span><br/></td>
<td><span data-ttu-id="3be00-168">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3be00-168">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be00-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span><span class="sxs-lookup"><span data-stu-id="3be00-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span></span></td>
<td><span data-ttu-id="3be00-170">Definiert den ausgewählten Farbtyp.</span><span class="sxs-lookup"><span data-stu-id="3be00-170">Defines the selected color type.</span></span><br/></td>
<td><span data-ttu-id="3be00-171">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3be00-171">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be00-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="3be00-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="3be00-173">Definiert die Fähigkeit eines Steuerelements, auf Benutzerinteraktion zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="3be00-173">Defines the ability for a control to respond to user interaction.</span></span><br/></td>
<td><span data-ttu-id="3be00-174">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3be00-174">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be00-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="3be00-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>

<td><span data-ttu-id="3be00-176">Kann nur durch Ungültigkeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3be00-176">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be00-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="3be00-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="3be00-178">Definiert die Zeichenfolge für eine Steuerelementbezeichnung.</span><span class="sxs-lookup"><span data-stu-id="3be00-178">Defines the character string for a control label.</span></span><br/></td>
<td><span data-ttu-id="3be00-179">Kann nur durch Ungültigkeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3be00-179">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be00-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="3be00-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="3be00-181">Definiert das große Bild mit hohem Kontrast, das für ein Steuerelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3be00-181">Defines the large high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="3be00-182">Kann nur durch Ungültigkeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3be00-182">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="3be00-183">Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menübandbildressourcen.</a></span><span class="sxs-lookup"><span data-stu-id="3be00-183">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be00-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="3be00-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="3be00-185">Definiert das große Bild, das für ein Steuerelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3be00-185">Defines the large image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="3be00-186">Kann nur durch Ungültigkeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3be00-186">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="3be00-187">Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menübandbildressourcen.</a></span><span class="sxs-lookup"><span data-stu-id="3be00-187">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be00-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span><span class="sxs-lookup"><span data-stu-id="3be00-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span></span></td>
<td><span data-ttu-id="3be00-189">Definiert die Bezeichnung für die <strong>Schaltfläche Weitere Farben...</strong> .</span><span class="sxs-lookup"><span data-stu-id="3be00-189">Defines the label for the <strong>More colors...</strong> button.</span></span><br/> <span data-ttu-id="3be00-190">Nur gültig, <em>wenn ColorTemplate</em> über den Wert oder <code>ThemeColors</code> <code>StandardColors</code> verfügt.</span><span class="sxs-lookup"><span data-stu-id="3be00-190">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="3be00-191">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3be00-191">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be00-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="3be00-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span></span></td>
<td><span data-ttu-id="3be00-193">Definiert die Bezeichnung für die <strong>Schaltfläche Keine</strong> Farbe.</span><span class="sxs-lookup"><span data-stu-id="3be00-193">Defines the label for the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="3be00-194">Gültig für alle <em>ColorTemplate-Werte.</em></span><span class="sxs-lookup"><span data-stu-id="3be00-194">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
<td><span data-ttu-id="3be00-195">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3be00-195">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be00-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="3be00-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="3be00-197">Definiert die Bezeichnung für die <strong>Kategorie Zuletzt verwendete</strong> Farben.</span><span class="sxs-lookup"><span data-stu-id="3be00-197">Defines the label for the <strong>Recent colors</strong> category.</span></span><br/> <span data-ttu-id="3be00-198">Nur gültig, <em>wenn ColorTemplate</em> über den Wert <code>ThemeColors</code> verfügt.</span><span class="sxs-lookup"><span data-stu-id="3be00-198">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="3be00-199">Dies ist die einzige Vorlage, die bezeichnete Kategorien enthält.</span><span class="sxs-lookup"><span data-stu-id="3be00-199">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="3be00-200">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3be00-200">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be00-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="3be00-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="3be00-202">Definiert das kleine Bild mit hohem Kontrast, das für ein Steuerelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3be00-202">Defines the small high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="3be00-203">Kann nur durch Ungültigkeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3be00-203">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="3be00-204">Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menübandbildressourcen.</a></span><span class="sxs-lookup"><span data-stu-id="3be00-204">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be00-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="3be00-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="3be00-206">Definiert das kleine Bild, das für ein Steuerelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3be00-206">Defines the small image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="3be00-207">Kann nur durch Ungültigkeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3be00-207">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="3be00-208">Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menübandbildressourcen.</a></span><span class="sxs-lookup"><span data-stu-id="3be00-208">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be00-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span><span class="sxs-lookup"><span data-stu-id="3be00-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span></span></td>
<td><span data-ttu-id="3be00-210">Definiert ein Array von <a href="/windows/win32/gdi/colorref">COLORREF-Werten</a> für die Muster eines Drop-Down Farbwähler.</span><span class="sxs-lookup"><span data-stu-id="3be00-210">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="3be00-211">Jede Drop-Down Farbwähler <em>ColorTemplate</em> enthält ein <code>StandardColors</code> Raster.</span><span class="sxs-lookup"><span data-stu-id="3be00-211">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3be00-212">Die <a href="/windows/win32/gdi/colorref">COLORREF-Werte</a> aus den <em>anfänglichen StandardColorGridRows</em> <em>x-Spalten</em> des Arrays werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3be00-212">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>StandardColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="3be00-213">Wenn das Array weniger Farben als die Anzahl der <code>StandardColors</code> im Markup deklarierten Farbfelder definiert, werden leere Leerzeichen für die fehlenden Chips angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3be00-213">If the array defines fewer colors than the number of <code>StandardColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="3be00-214">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3be00-214">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be00-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="3be00-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="3be00-216">Definiert die Bezeichnung für die Kategorie <strong>Standardfarben.</strong></span><span class="sxs-lookup"><span data-stu-id="3be00-216">Defines the label for the <strong>Standard colors</strong> category.</span></span><br/> <span data-ttu-id="3be00-217">Nur gültig, wenn <em>ColorTemplate</em> über den Wert <code>ThemeColors</code> verfügt.</span><span class="sxs-lookup"><span data-stu-id="3be00-217">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="3be00-218">Dies ist die einzige Vorlage, die bezeichnete Kategorien enthält.</span><span class="sxs-lookup"><span data-stu-id="3be00-218">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="3be00-219">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3be00-219">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be00-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="3be00-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span></span></td>
<td><span data-ttu-id="3be00-221">Definiert ein Zeichenfolgenarray mit Farbwatch-QuickInfos für das <code>StandardColors</code> Raster.</span><span class="sxs-lookup"><span data-stu-id="3be00-221">Defines a string array of color swatch tooltips for the <code>StandardColors</code> grid.</span></span><br/> <span data-ttu-id="3be00-222">Jede Drop-Down Farbwähler <em>ColorTemplate</em> enthält ein <code>StandardColors</code> Raster.</span><span class="sxs-lookup"><span data-stu-id="3be00-222">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3be00-223">Es werden nur die QuickInfos verwendet, die zum Bezeichnen der im Raster angezeigten Farbwatches erforderlich <code>StandardColors</code> sind.</span><span class="sxs-lookup"><span data-stu-id="3be00-223">Only those tool tips required to label the color swatches displayed in the <code>StandardColors</code> grid are used.</span></span> <span data-ttu-id="3be00-224">Wenn weniger Bezeichnungen bereitgestellt werden als die Anzahl von Mustern im <code>StandardColors</code> Raster, wird ein Standardwert für die beibehaltenen Muster bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3be00-224">If fewer labels are supplied than the number of swatches in the <code>StandardColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="3be00-225">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3be00-225">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be00-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span><span class="sxs-lookup"><span data-stu-id="3be00-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span></span></td>
<td><span data-ttu-id="3be00-227">Definiert ein Array von <a href="/windows/win32/gdi/colorref">COLORREF-Werten</a> für die Muster eines Drop-Down Farbwähler.</span><span class="sxs-lookup"><span data-stu-id="3be00-227">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="3be00-228">Nur gültig, wenn <em>ColorTemplate</em> über den Wert <code>ThemeColors</code> verfügt.</span><span class="sxs-lookup"><span data-stu-id="3be00-228">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3be00-229">Die <a href="/windows/win32/gdi/colorref">COLORREF-Werte</a> aus den <em>anfänglichen ThemeColorGridRows</em> <em>x-Spalten</em> des Arrays werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3be00-229">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>ThemeColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="3be00-230">Wenn das Array weniger Farben als die Anzahl der <code>ThemeColors</code> im Markup deklarierten Farbfelder definiert, werden leere Leerzeichen für die fehlenden Chips angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3be00-230">If the array defines fewer colors than the number of <code>ThemeColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="3be00-231">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3be00-231">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be00-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="3be00-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span></span></td>
<td><span data-ttu-id="3be00-233">Definiert das Zeichenfolgenarray der Farbwatch-QuickInfos für das <code>ThemeColors</code> Raster.</span><span class="sxs-lookup"><span data-stu-id="3be00-233">Defines the string array of color swatch tooltips for the <code>ThemeColors</code> grid.</span></span><br/> <span data-ttu-id="3be00-234">Nur gültig, wenn <em>ColorTemplate</em> über den Wert <code>ThemeColors</code> verfügt.</span><span class="sxs-lookup"><span data-stu-id="3be00-234">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3be00-235">Es werden nur die QuickInfos verwendet, die zum Bezeichnen der im Raster angezeigten Farbwatches erforderlich <code>ThemeColors</code> sind.</span><span class="sxs-lookup"><span data-stu-id="3be00-235">Only those tool tips required to label the color swatches displayed in the <code>ThemeColors</code> grid are used.</span></span> <span data-ttu-id="3be00-236">Wenn weniger Bezeichnungen bereitgestellt werden als die Anzahl von Mustern im <code>ThemeColors</code> Raster, wird ein Standardwert für die beibehaltenen Muster bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3be00-236">If fewer labels are supplied than the number of swatches in the <code>ThemeColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="3be00-237">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3be00-237">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be00-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="3be00-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="3be00-239">Definiert die Bezeichnung für die Kategorie <strong>Designfarben.</strong></span><span class="sxs-lookup"><span data-stu-id="3be00-239">Defines the label for the <strong>Theme colors</strong> category.</span></span><br/> <span data-ttu-id="3be00-240">Nur gültig, wenn <em>ColorTemplate</em> über den Wert <code>ThemeColors</code> verfügt.</span><span class="sxs-lookup"><span data-stu-id="3be00-240">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="3be00-241">Dies ist die einzige Vorlage, die bezeichnete Kategorien enthält.</span><span class="sxs-lookup"><span data-stu-id="3be00-241">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="3be00-242">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></span><span class="sxs-lookup"><span data-stu-id="3be00-242">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3be00-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="3be00-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="3be00-244">Definiert die Zeichenfolge für eine QuickInfo-Beschreibung, die einem <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3be00-244">Defines the character string for a tooltip description associated with a <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span></span><br/></td>
<td><span data-ttu-id="3be00-245">Kann nur durch Ungültigkeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3be00-245">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3be00-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="3be00-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="3be00-247">Definiert die Zeichenfolge für eine Befehls-QuickInfo.</span><span class="sxs-lookup"><span data-stu-id="3be00-247">Defines the character string for a Command tooltip.</span></span><br/></td>
<td><span data-ttu-id="3be00-248">Kann nur durch Ungültigkeit aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3be00-248">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a><span data-ttu-id="3be00-249">Befehlshandler</span><span class="sxs-lookup"><span data-stu-id="3be00-249">Command handlers</span></span>

<span data-ttu-id="3be00-250">Die [**IUICommandHandler::UpdateProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird verwendet, um einen Drop-Down Farbwähler über die oben aufgeführten Eigenschaftsschlüssel anzupassen.</span><span class="sxs-lookup"><span data-stu-id="3be00-250">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method is used to customize a Drop-Down Color Picker through the property keys listed above.</span></span> <span data-ttu-id="3be00-251">Im folgenden Beispiel wird veranschaulicht, wie die Farbwatches eines Drop-Down Farbwähler basierend auf einer benutzerdefinierten Stilpräferenz oder einem im Markup deklarierten benutzerdefinierten Farbmusterraster festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3be00-251">The following example demonstrates how to set the color swatches of a Drop-Down Color Picker, based on a custom style preference or a custom swatch grid that is declared in markup.</span></span>


```C++
STDMETHODIMP DropDownColorPickerHandler::UpdateProperty(
              UINT nCmdID,
              __in REFPROPERTYKEY key,
              __in_opt const PROPVARIANT* ppropvarCurrentValue,
              __out PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_ThemeColors)
  {
    COLORREF rThemeColors[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeColors); i++)
    {
      // any COLORREF
      rThemeColors[i] = RGB(0, 255, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rThemeColors, ARRAYSIZE(rThemeColors), ppropvarNewValue);
  }

  else if (key == UI_PKEY_StandardColors)
  {
    ULONG rStandardColors[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rStandardColors); i++)
    {
      // any COLORREF
      rStandardColors[i] = RGB(255, 0, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rStandardColors, ARRAYSIZE(rStandardColors),ppropvarNewValue);
  }

  else if (key == UI_PKEY_ThemeColorsTooltips)
  {
    BSTR rThemeTooltips[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeTooltips); i++)
    {
      // any constant character string
      rThemeTooltips[i] = L"Green"; 
    }
    hr = InitPropVariantFromStringVector((PCWSTR *)&rThemeTooltips, 50, ppropvarNewValue);
  }
  else if (key == UI_PKEY_StandardColorsTooltips)
  {
    static BSTR rStandardTooltips[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSize(rStandardTooltips); i++)
    {
      // any constant character string
      rStandardTooltips[i] = L"Red"; 
    }
    hr = InitPropVariantFromStringVector(
           (PCWSTR *)&rStandardTooltips, 20, ppropvarNewValue);
  }
  return hr;
}
```



<span data-ttu-id="3be00-252">Im folgenden Beispiel wird eine Implementierung der [**IUICommandHandler::Execute-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) veranschaulicht, die die Drop-Down Farbwähler Farbmuster für die Menübandanwendung verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="3be00-252">The following example demonstrates an implementation of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method that exposes the Drop-Down Color Picker swatch colors to the Ribbon application.</span></span>


```C++
STDMETHODIMP DropDownColorPickerHandler::Execute(
                 UINT nCmdID,
                 UI_EXECUTIONVERB verb,
                 __in_opt const PROPERTYKEY* key,
                 __in_opt const PROPVARIANT* ppropvarValue,
                 __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  HRESULT hr = E_NOTIMPL;
  if (*key == UI_PKEY_ColorType)
  {
    UI_SWATCHCOLORTYPE uType = 
      (UI_SWATCHCOLORTYPE)PropVariantToUInt32WithDefault(
        *ppropvarValue, 
        UI_SWATCHCOLORTYPE_NOCOLOR);

    COLORREF color;
    switch(uType)
    {
      case UI_SWATCHCOLORTYPE_RGB:
        PROPVARIANT var;
        pCommandExecutionProperties->GetValue(UI_PKEY_Color, &var);
        color = PropVariantToUInt32WithDefault(var, 0);
        break;
      case UI_SWATCHCOLORTYPE_AUTOMATIC:
        color = COLOR_WINDOWTEXT;
        break;
      case UI_SWATCHCOLORTYPE_NOCOLOR:
        color = MSONoFill;
        break;
    }

    // do with your color what you will...
    gInternalColor = color;
    hr = S_OK;
  }
  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3be00-253">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3be00-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3be00-254">Framework-Steuerelementbibliothek für Windows-Menüband</span><span class="sxs-lookup"><span data-stu-id="3be00-254">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="3be00-255">**DropDownColorPicker-Markupelement**</span><span class="sxs-lookup"><span data-stu-id="3be00-255">**DropDownColorPicker markup element**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="3be00-256">Farbwähler-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3be00-256">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[<span data-ttu-id="3be00-257">Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="3be00-257">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="3be00-258">DropDownColorPicker-Beispiel</span><span class="sxs-lookup"><span data-stu-id="3be00-258">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

