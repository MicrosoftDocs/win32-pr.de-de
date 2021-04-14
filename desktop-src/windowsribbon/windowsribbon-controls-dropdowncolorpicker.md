---
title: Drop-Down Farbauswahl
description: Das Windows-Menü Band Framework bietet ein spezielles Steuerelement für die Drop-Down Farbauswahl, das eine Vielzahl von Farbeinstellungen über eine unterteilte Schaltfläche und eine anpassbare Dropdown-Farbauswahl verfügbar macht
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552cd05e619ba71653d0d72e8457f5d4c8c39624
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104391117"
---
# <a name="drop-down-color-picker"></a><span data-ttu-id="d7d8f-103">Drop-Down Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="d7d8f-103">Drop-Down Color Picker</span></span>

<span data-ttu-id="d7d8f-104">Das Windows-Menü Band Framework bietet ein spezielles Steuerelement für die Drop-Down Farbauswahl, das eine Vielzahl von Farbeinstellungen über eine unterteilte Schaltfläche und eine anpassbare Dropdown-Farbauswahl verfügbar macht</span><span class="sxs-lookup"><span data-stu-id="d7d8f-104">The Windows Ribbon framework provides a specialized Drop-Down Color Picker control that exposes a variety of color settings through a split button and customizable drop-down color selector.</span></span>

-   [<span data-ttu-id="d7d8f-105">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="d7d8f-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="d7d8f-106">Markup</span><span class="sxs-lookup"><span data-stu-id="d7d8f-106">Markup</span></span>](#markup)
-   [<span data-ttu-id="d7d8f-107">Code</span><span class="sxs-lookup"><span data-stu-id="d7d8f-107">Code</span></span>](#code)
    -   [<span data-ttu-id="d7d8f-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7d8f-108">Properties</span></span>](#properties)
    -   [<span data-ttu-id="d7d8f-109">Befehls Handler</span><span class="sxs-lookup"><span data-stu-id="d7d8f-109">Command handlers</span></span>](#command-handlers)
-   [<span data-ttu-id="d7d8f-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7d8f-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="d7d8f-111">Einführung</span><span class="sxs-lookup"><span data-stu-id="d7d8f-111">Introduction</span></span>

<span data-ttu-id="d7d8f-112">Durch Emulierung des Erscheinungs Bilds und der Funktionalität der Microsoft Office Farbauswahl kann das Menüband-Framework sowohl von profitieren als auch an Konsistenz und Vertrautheit in einer Vielzahl von Anwendungen mitwirken.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-112">By emulating the appearance and functionality of the Microsoft Office color picker, the Ribbon framework is able to both benefit from, and contribute to, consistency and familiarity across a wide range of applications.</span></span>

## <a name="markup"></a><span data-ttu-id="d7d8f-113">Markup</span><span class="sxs-lookup"><span data-stu-id="d7d8f-113">Markup</span></span>

<span data-ttu-id="d7d8f-114">Wie alle multifunktionsleistensteuerelemente kann die Drop-Down Farbauswahl problemlos implementiert und durch Markup angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-114">Like all Ribbon controls, the Drop-Down Color Picker is easily implemented and customized through markup.</span></span> <span data-ttu-id="d7d8f-115">Das Framework bietet eine Reihe von Element Attributen für die Drop-Down Farbauswahl, um verschiedene Funktionsebenen verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-115">The framework provides a number of element attributes for the Drop-Down Color Picker to expose various levels of functionality.</span></span> <span data-ttu-id="d7d8f-116">In der folgenden Tabelle sind die Drop-Down Farbauswahl Attribute aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-116">The following table lists the Drop-Down Color Picker attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7d8f-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="d7d8f-117">Attribute</span></span></th>
<th><span data-ttu-id="d7d8f-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7d8f-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d7d8f-119">Colortemplate</span><span class="sxs-lookup"><span data-stu-id="d7d8f-119">ColorTemplate</span></span></td>
<td><span data-ttu-id="d7d8f-120">Layoutvorlagen, die den Typ der Drop-Down Farbauswahl angeben.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-120">Layout templates that specify the type of Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="d7d8f-121">Es gibt drei Vorlagen, von denen jedes ein Steuerelement Layout und Standardwerte für zugeordnete Attribute und Eigenschafts Schlüssel angibt.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-121">There are three templates, each of which specifies a control layout and default values for associated attributes and property keys.</span></span> <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7d8f-122">Chipgröße</span><span class="sxs-lookup"><span data-stu-id="d7d8f-122">ChipSize</span></span></td>
<td><span data-ttu-id="d7d8f-123">Die Größe jedes Farbchips (oder Musters).</span><span class="sxs-lookup"><span data-stu-id="d7d8f-123">The size of each color chip (or swatch).</span></span><br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7d8f-124">Spalten</span><span class="sxs-lookup"><span data-stu-id="d7d8f-124">Columns</span></span></td>
<td><span data-ttu-id="d7d8f-125">Die Anzahl der farbchipspalten (oder Muster Spalten).</span><span class="sxs-lookup"><span data-stu-id="d7d8f-125">The number of color chip (or swatch) columns.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7d8f-126">CommandName</span><span class="sxs-lookup"><span data-stu-id="d7d8f-126">CommandName</span></span></td>
<td><span data-ttu-id="d7d8f-127">Der Name der zugeordneten Befehls Deklaration.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-127">The name of the associated Command declaration.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7d8f-128">Isautomaticcolorbuttonvisible</span><span class="sxs-lookup"><span data-stu-id="d7d8f-128">IsAutomaticColorButtonVisible</span></span></td>
<td><span data-ttu-id="d7d8f-129">Zeigt die Schaltfläche <strong>automatisch</strong> an (oder blendet sie aus).</span><span class="sxs-lookup"><span data-stu-id="d7d8f-129">Displays (or hides) the <strong>Automatic</strong> button.</span></span><br/> <span data-ttu-id="d7d8f-130">Nur gültig, wenn <em>colortemplate</em> den Wert <code>ThemeColors</code> oder aufweist <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="d7d8f-130">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7d8f-131">Isnocolorbuttonvisible</span><span class="sxs-lookup"><span data-stu-id="d7d8f-131">IsNoColorButtonVisible</span></span></td>
<td><span data-ttu-id="d7d8f-132">Zeigt die Schaltfläche <strong>keine Farbe</strong> an (oder blendet sie aus).</span><span class="sxs-lookup"><span data-stu-id="d7d8f-132">Displays (or hides) the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="d7d8f-133">Gültig für alle <em>colortemplate</em> -Werte.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-133">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7d8f-134">Recentcolorgridrows</span><span class="sxs-lookup"><span data-stu-id="d7d8f-134">RecentColorGridRows</span></span></td>
<td><span data-ttu-id="d7d8f-135">Die Anzahl der farbchipzeilen (oder Muster Zeilen) im Bereich " <strong>Letzte Farben</strong> ".</span><span class="sxs-lookup"><span data-stu-id="d7d8f-135">The number of color chip (or swatch) rows in the <strong>Recent colors</strong> area.</span></span><br/> <span data-ttu-id="d7d8f-136">Nur gültig, wenn <em>colortemplate</em> den Wert hat <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="d7d8f-136">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7d8f-137">Standardcolorgridrows</span><span class="sxs-lookup"><span data-stu-id="d7d8f-137">StandardColorGridRows</span></span></td>
<td><span data-ttu-id="d7d8f-138">Die Anzahl der farbchipzeilen (oder Muster Zeilen) im <strong>Standard Farben</strong> Bereich.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-138">The number of color chip (or swatch) rows in the <strong>Standard colors</strong> area.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7d8f-139">"Mecolorgridrows"</span><span class="sxs-lookup"><span data-stu-id="d7d8f-139">ThemeColorGridRows</span></span></td>
<td><span data-ttu-id="d7d8f-140">Die Anzahl der farbchipzeilen (oder Muster Zeilen) im Design <strong>Farben</strong> Bereich.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-140">The number of color chip (or swatch) rows in the <strong>Theme colors</strong> area.</span></span><br/> <span data-ttu-id="d7d8f-141">Nur gültig, wenn <em>colortemplate</em> den Wert hat <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="d7d8f-141">Valid only when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d7d8f-142">Die folgenden Bildschirmfotos veranschaulichen die standardmäßigen Drop-Down Farbauswahl Layouts für die drei Farbvorlagen.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-142">The following screen shots illustrate the default Drop-Down Color Picker layouts for the three color templates.</span></span>



|                                                                                                                                                                                               |                                                                                                                                                                                                       |                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d8f-143">`ThemeColors`: \[ Zeilen \] ![ Vorschub für das dropdowncolorpicker-Element, bei dem das colortemplate-Attribut auf "thmecolors" festgelegt ist. ](images/markup/colortemplate.themedcolors.1.png) \[ Zeilenumbruch\]</span><span class="sxs-lookup"><span data-stu-id="d7d8f-143">`ThemeColors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'themecolors'.](images/markup/colortemplate.themedcolors.1.png)\[newline\]</span></span> | <span data-ttu-id="d7d8f-144">`standardcolors`: \[ Zeilen \] ![ Vorschub für das dropdowncolorpicker-Element, bei dem das colortemplate-Attribut auf ' standardcolors ' festgelegt ist. ](images/markup/colortemplate.standardcolors.3.png) \[ Zeilenumbruch\]</span><span class="sxs-lookup"><span data-stu-id="d7d8f-144">`standardcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'standardcolors'.](images/markup/colortemplate.standardcolors.3.png)\[newline\]</span></span> | <span data-ttu-id="d7d8f-145">`highlightcolors`: \[ Zeilen \] ![ Vorschub für das dropdowncolorpicker-Element, bei dem das colortemplate-Attribut auf ' highlightcolors ' festgelegt ist.](images/markup/colortemplate.highlightcolors.2.png)</span><span class="sxs-lookup"><span data-stu-id="d7d8f-145">`highlightcolors`:\[newline\] ![screen shot of the dropdowncolorpicker element with the colortemplate attribute set to 'highlightcolors'.](images/markup/colortemplate.highlightcolors.2.png)</span></span><br/> |



 

<span data-ttu-id="d7d8f-146">Das grundlegende Markup, das für die einzelnen Drop-Down Farbauswahl Typen erforderlich ist, wird in den folgenden Beispielen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="d7d8f-146">The basic markup required for each Drop-Down Color Picker type is demonstrated in the following examples:</span></span>

> [!Note]  
> <span data-ttu-id="d7d8f-147">Die Drop-Down Farbauswahl ist ein gültiges [Schalt](windowsribbon-controls-button.md) Flächen-Steuerelement in einer [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlage.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-147">The Drop-Down Color Picker is a valid [Button](windowsribbon-controls-button.md) control in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

 


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





## <a name="code"></a><span data-ttu-id="d7d8f-148">Code</span><span class="sxs-lookup"><span data-stu-id="d7d8f-148">Code</span></span>

<span data-ttu-id="d7d8f-149">Als spezialisiertes Steuerelement, das die Anpassung unterstützt, erfordert jede Implementierung der Drop-Down Farbauswahl, die diese Funktionen nutzt, speziellen Anwendungscode, um Eigenschaften zu verwalten und alle Befehle zu verarbeiten, die vom Steuerelement ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-149">As a specialized control that supports customization, any implemention of the Drop-Down Color Picker that takes advantage of these capabilities requires specialized application code to manage properties and handle any Commands issued by the control.</span></span>

### <a name="properties"></a><span data-ttu-id="d7d8f-150">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7d8f-150">Properties</span></span>

<span data-ttu-id="d7d8f-151">Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Drop-Down Farbauswahl-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-151">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Color Picker control.</span></span>

<span data-ttu-id="d7d8f-152">In der Regel wird eine Drop-Down Color-Auswahl Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-152">Typically, a Drop-Down Color Picker property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="d7d8f-153">Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-153">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="d7d8f-154">Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-154">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="d7d8f-155">Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-155">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="d7d8f-156">In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-156">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="d7d8f-157">In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die dem Steuerelement Drop-Down Color Picker zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-157">The following table lists the property keys that are associated with the Drop-Down Color Picker control.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7d8f-158">Eigenschafts Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d7d8f-158">Property Key</span></span></th>
<th><span data-ttu-id="d7d8f-159">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7d8f-159">Description</span></span></th>
<th><span data-ttu-id="d7d8f-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7d8f-160">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d7d8f-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-161"><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></span></span></td>
<td><span data-ttu-id="d7d8f-162">Definiert die Bezeichnung für die <strong>Automatische</strong> Farb Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-162">Defines the label for the <strong>Automatic</strong> color button.</span></span><br/> <span data-ttu-id="d7d8f-163">Nur gültig, wenn <em>colortemplate</em> den Wert <code>ThemeColors</code> oder aufweist <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="d7d8f-163">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-164">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-164">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7d8f-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-165"><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></span></span></td>
<td><span data-ttu-id="d7d8f-166">Definiert den ausgewählten Farbwert als <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-166">Defines the selected color value as a <a href="/windows/win32/gdi/colorref">COLORREF</a>.</span></span><br/> <span data-ttu-id="d7d8f-167">Nur gültig, wenn <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> den Wert hat <code>UI_SWATCHCOLORTYPE_RGB</code> .</span><span class="sxs-lookup"><span data-stu-id="d7d8f-167">Only valid when <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> has a value of <code>UI_SWATCHCOLORTYPE_RGB</code>.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-168">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-168">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7d8f-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-169"><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></span></span></td>
<td><span data-ttu-id="d7d8f-170">Definiert den ausgewählten Farbtyp.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-170">Defines the selected color type.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-171">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-171">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7d8f-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-172"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="d7d8f-173">Definiert die Fähigkeit eines Steuer Elements, auf Benutzerinteraktionen zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-173">Defines the ability for a control to respond to user interaction.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-174">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-174">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7d8f-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-175"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>

<td><span data-ttu-id="d7d8f-176">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-176">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7d8f-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-177"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="d7d8f-178">Definiert die Zeichenfolge für eine Steuerelement Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-178">Defines the character string for a control label.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-179">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-179">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7d8f-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-180"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="d7d8f-181">Definiert das große Bild mit hohem Kontrast, das für ein Steuerelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-181">Defines the large high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-182">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-182">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="d7d8f-183">Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menüband-Bild Ressourcen</a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-183">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7d8f-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-184"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="d7d8f-185">Definiert das große Bild, das für ein Steuerelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-185">Defines the large image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-186">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-186">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="d7d8f-187">Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menüband-Bild Ressourcen</a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-187">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7d8f-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-188"><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></span></span></td>
<td><span data-ttu-id="d7d8f-189">Definiert die Bezeichnung für die Schaltfläche mit den <strong>weiteren Farben...</strong></span><span class="sxs-lookup"><span data-stu-id="d7d8f-189">Defines the label for the <strong>More colors...</strong> button.</span></span><br/> <span data-ttu-id="d7d8f-190">Nur gültig, wenn <em>colortemplate</em> den Wert <code>ThemeColors</code> oder aufweist <code>StandardColors</code> .</span><span class="sxs-lookup"><span data-stu-id="d7d8f-190">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code> or <code>StandardColors</code>.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-191">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-191">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7d8f-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-192"><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></span></span></td>
<td><span data-ttu-id="d7d8f-193">Definiert die Bezeichnung für die Schaltfläche <strong>keine Farbe</strong> .</span><span class="sxs-lookup"><span data-stu-id="d7d8f-193">Defines the label for the <strong>No color</strong> button.</span></span><br/> <span data-ttu-id="d7d8f-194">Gültig für alle <em>colortemplate</em> -Werte.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-194">Valid for all <em>ColorTemplate</em> values.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-195">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-195">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7d8f-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-196"><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="d7d8f-197">Definiert die Bezeichnung für die Kategorie " <strong>zuletzt verwendete Farben</strong> ".</span><span class="sxs-lookup"><span data-stu-id="d7d8f-197">Defines the label for the <strong>Recent colors</strong> category.</span></span><br/> <span data-ttu-id="d7d8f-198">Nur gültig, wenn <em>colortemplate</em> den Wert hat <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="d7d8f-198">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="d7d8f-199">Dies ist die einzige Vorlage, die bezeichnete Kategorien enthält.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-199">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-200">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-200">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7d8f-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-201"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="d7d8f-202">Definiert das kleine Bild mit hohem Kontrast, das für ein Steuerelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-202">Defines the small high-contrast image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-203">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-203">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="d7d8f-204">Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menüband-Bild Ressourcen</a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-204">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7d8f-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-205"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="d7d8f-206">Definiert das kleine Bild, das für ein Steuerelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-206">Defines the small image to display for a control.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-207">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-207">Can only be updated through invalidation.</span></span><br/> <span data-ttu-id="d7d8f-208">Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menüband-Bild Ressourcen</a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-208">For more information on image formats, see <a href="windowsribbon-imageformats.md">Specifying Ribbon Image Resources</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7d8f-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-209"><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></span></span></td>
<td><span data-ttu-id="d7d8f-210">Definiert ein Array von <a href="/windows/win32/gdi/colorref">COLORREF</a> -Werten für die Dragquellen einer Drop-Down Farbauswahl.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-210">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="d7d8f-211">Jede Drop-Down Farbauswahl <em>colortemplate</em> enthält ein <code>StandardColors</code> Raster.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-211">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d7d8f-212">Die <a href="/windows/win32/gdi/colorref">COLORREF</a> -Werte aus den anfänglichen <em>standardcolorgridrows</em> x- <em>Spalten</em> des Arrays werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-212">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>StandardColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="d7d8f-213">Wenn das Array weniger Farben als die Anzahl der <code>StandardColors</code> im Markup deklarierten Dragquellen definiert, werden leere Leerzeichen für die fehlenden Chips angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-213">If the array defines fewer colors than the number of <code>StandardColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="d7d8f-214">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-214">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7d8f-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-215"><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="d7d8f-216">Definiert die Bezeichnung für die Kategorie " <strong>Standard Farben</strong> ".</span><span class="sxs-lookup"><span data-stu-id="d7d8f-216">Defines the label for the <strong>Standard colors</strong> category.</span></span><br/> <span data-ttu-id="d7d8f-217">Nur gültig, wenn <em>colortemplate</em> den Wert hat <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="d7d8f-217">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="d7d8f-218">Dies ist die einzige Vorlage, die bezeichnete Kategorien enthält.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-218">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-219">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-219">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7d8f-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-220"><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></span></span></td>
<td><span data-ttu-id="d7d8f-221">Definiert ein Zeichen folgen Array von Farbmuster-Quick Infos für das <code>StandardColors</code> Raster.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-221">Defines a string array of color swatch tooltips for the <code>StandardColors</code> grid.</span></span><br/> <span data-ttu-id="d7d8f-222">Jede Drop-Down Farbauswahl <em>colortemplate</em> enthält ein <code>StandardColors</code> Raster.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-222">Each Drop-Down Color Picker <em>ColorTemplate</em> contains a <code>StandardColors</code> grid.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d7d8f-223">Es werden nur die Quick Infos verwendet, die zum bezeichnen der im Raster angezeigten farbsüberwachungen erforderlich <code>StandardColors</code> sind.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-223">Only those tool tips required to label the color swatches displayed in the <code>StandardColors</code> grid are used.</span></span> <span data-ttu-id="d7d8f-224">Wenn weniger Bezeichnungen als die Anzahl der Dragquellen im <code>StandardColors</code> Raster bereitgestellt werden, wird für die restlichen Swatch ein Standardwert bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-224">If fewer labels are supplied than the number of swatches in the <code>StandardColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="d7d8f-225">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-225">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7d8f-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-226"><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></span></span></td>
<td><span data-ttu-id="d7d8f-227">Definiert ein Array von <a href="/windows/win32/gdi/colorref">COLORREF</a> -Werten für die Dragquellen einer Drop-Down Farbauswahl.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-227">Defines an array of <a href="/windows/win32/gdi/colorref">COLORREF</a> values for the swatches of a Drop-Down Color Picker.</span></span><br/> <span data-ttu-id="d7d8f-228">Nur gültig, wenn <em>colortemplate</em> den Wert hat <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="d7d8f-228">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d7d8f-229">Die <a href="/windows/win32/gdi/colorref">COLORREF</a> -Werte aus den anfänglichen " <em>temecolorgridrows</em> x"- <em>Spalten</em> des Arrays werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-229">The <a href="/windows/win32/gdi/colorref">COLORREF</a> values from the initial <em>ThemeColorGridRows</em> x <em>Columns</em> of the array are displayed.</span></span> <span data-ttu-id="d7d8f-230">Wenn das Array weniger Farben als die Anzahl der <code>ThemeColors</code> im Markup deklarierten Dragquellen definiert, werden leere Leerzeichen für die fehlenden Chips angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-230">If the array defines fewer colors than the number of <code>ThemeColors</code> swatches declared in markup, empty spaces are displayed for the missing chips.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="d7d8f-231">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-231">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7d8f-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-232"><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></span></span></td>
<td><span data-ttu-id="d7d8f-233">Definiert das Zeichen folgen Array von Farbmuster-Quick Infos für das <code>ThemeColors</code> Raster.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-233">Defines the string array of color swatch tooltips for the <code>ThemeColors</code> grid.</span></span><br/> <span data-ttu-id="d7d8f-234">Nur gültig, wenn <em>colortemplate</em> den Wert hat <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="d7d8f-234">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d7d8f-235">Es werden nur die Quick Infos verwendet, die zum bezeichnen der im Raster angezeigten farbsüberwachungen erforderlich <code>ThemeColors</code> sind.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-235">Only those tool tips required to label the color swatches displayed in the <code>ThemeColors</code> grid are used.</span></span> <span data-ttu-id="d7d8f-236">Wenn weniger Bezeichnungen als die Anzahl der Dragquellen im <code>ThemeColors</code> Raster bereitgestellt werden, wird für die restlichen Swatch ein Standardwert bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-236">If fewer labels are supplied than the number of swatches in the <code>ThemeColors</code> grid, a default is provided for the remainining swatches.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="d7d8f-237">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-237">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7d8f-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-238"><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></span></span></td>
<td><span data-ttu-id="d7d8f-239">Definiert die Bezeichnung für die Kategorie Design <strong>Farben</strong> .</span><span class="sxs-lookup"><span data-stu-id="d7d8f-239">Defines the label for the <strong>Theme colors</strong> category.</span></span><br/> <span data-ttu-id="d7d8f-240">Nur gültig, wenn <em>colortemplate</em> den Wert hat <code>ThemeColors</code> .</span><span class="sxs-lookup"><span data-stu-id="d7d8f-240">Only valid when <em>ColorTemplate</em> has a value of <code>ThemeColors</code>.</span></span> <span data-ttu-id="d7d8f-241">Dies ist die einzige Vorlage, die bezeichnete Kategorien enthält.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-241">This is the only template that contains labeled categories.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-242">Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-242">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7d8f-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-243"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="d7d8f-244">Definiert die Zeichenfolge für eine QuickInfo-Beschreibung, die einem <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-244">Defines the character string for a tooltip description associated with a <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-245">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-245">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7d8f-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="d7d8f-246"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="d7d8f-247">Definiert die Zeichenfolge für eine Befehls-QuickInfo.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-247">Defines the character string for a Command tooltip.</span></span><br/></td>
<td><span data-ttu-id="d7d8f-248">Kann nur durch Invalidierung aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-248">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a><span data-ttu-id="d7d8f-249">Befehls Handler</span><span class="sxs-lookup"><span data-stu-id="d7d8f-249">Command handlers</span></span>

<span data-ttu-id="d7d8f-250">Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Methode wird zum Anpassen einer Drop-Down Farbauswahl über die oben aufgeführten Eigenschaften Schlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-250">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method is used to customize a Drop-Down Color Picker through the property keys listed above.</span></span> <span data-ttu-id="d7d8f-251">Im folgenden Beispiel wird veranschaulicht, wie die farbswatch einer Drop-Down Farbauswahl basierend auf einer benutzerdefinierten Formatvorlage oder einem benutzerdefinierten Muster Raster, das im Markup deklariert ist, festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-251">The following example demonstrates how to set the color swatches of a Drop-Down Color Picker, based on a custom style preference or a custom swatch grid that is declared in markup.</span></span>


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



<span data-ttu-id="d7d8f-252">Im folgenden Beispiel wird eine Implementierung der [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Methode veranschaulicht, die die Muster Farben der Drop-Down Farbauswahl für die Menüband-Anwendung verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="d7d8f-252">The following example demonstrates an implementation of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method that exposes the Drop-Down Color Picker swatch colors to the Ribbon application.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d7d8f-253">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7d8f-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7d8f-254">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d7d8f-254">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="d7d8f-255">**Dropdowncolorpicker-Markup Element**</span><span class="sxs-lookup"><span data-stu-id="d7d8f-255">**DropDownColorPicker markup element**</span></span>](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[<span data-ttu-id="d7d8f-256">Farbauswahl Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d7d8f-256">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[<span data-ttu-id="d7d8f-257">Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d7d8f-257">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="d7d8f-258">Dropdowncolorpicker-Beispiel</span><span class="sxs-lookup"><span data-stu-id="d7d8f-258">DropDownColorPicker Sample</span></span>](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

