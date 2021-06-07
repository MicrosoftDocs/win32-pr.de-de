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
# <a name="drop-down-color-picker"></a>Drop-Down Farbwähler

Das Windows-Menübandframework bietet ein spezielles Drop-Down Farbwähler,das eine Vielzahl von Farbeinstellungen über eine Teilungsschaltfläche und einen anpassbaren Dropdownfarbwähler verfügbar macht.

-   [Introduction (Einführung)](#introduction)
-   [Markup](#markup)
-   [Code](#code)
    -   [Eigenschaften](#properties)
    -   [Befehlshandler](#command-handlers)
-   [Verwandte Themen](#related-topics)

## <a name="introduction"></a>Einführung

Durch emulieren der Darstellung und Funktionalität der Microsoft Office-Farbauswahl kann das Menübandframework sowohl von Konsistenz und Vertrautheit in einer Vielzahl von Anwendungen profitieren als auch zu dieser beitragen.

## <a name="markup"></a>Markup

Wie alle Menübandsteuerelemente kann die Drop-Down Farbwähler einfach implementiert und über Markup angepasst werden. Das Framework stellt eine Reihe von Elementattributen für die Drop-Down Farbwähler, um verschiedene Funktionalitätsebenen verfügbar zu machen. In der folgenden Tabelle sind die Drop-Down Farbwähler aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ColorTemplate</td>
<td>Layoutvorlagen, die den Typ der Drop-Down Farbwähler.<br/> Es gibt drei Vorlagen, von denen jede ein Steuerelementlayout und Standardwerte für zugeordnete Attribute und Eigenschaftsschlüssel angibt. <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td>ChipSize</td>
<td>Die Größe der einzelnen Farbchips (oder Farbmuster).<br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td>Spalten</td>
<td>Die Anzahl der Farbchipspalten (oder Farbmusterspalten).<br/></td>
</tr>
<tr class="even">
<td>CommandName</td>
<td>Der Name der zugeordneten Befehlsdeklaration. <br/></td>
</tr>
<tr class="odd">
<td>IsAutomaticColorButtonVisible</td>
<td>Zeigt die Schaltfläche Automatisch an (oder <strong>blendet</strong> sie aus).<br/> Nur gültig, <em>wenn ColorTemplate</em> über den Wert <code>ThemeColors</code> oder <code>StandardColors</code> verfügt.<br/></td>
</tr>
<tr class="even">
<td>IsNoColorButtonVisible</td>
<td>Zeigt die Schaltfläche Keine Farbe an <strong>(oder blendet sie</strong> aus).<br/> Gültig für alle <em>ColorTemplate-Werte.</em><br/></td>
</tr>
<tr class="odd">
<td>RecentColorGridRows</td>
<td>Die Anzahl der Farbchipzeilen (oder Farbmuster) im <strong>Bereich Zuletzt verwendete</strong> Farben.<br/> Nur gültig, <em>wenn ColorTemplate</em> über den Wert <code>ThemeColors</code> verfügt.<br/></td>
</tr>
<tr class="even">
<td>StandardColorGridRows</td>
<td>Die Anzahl der Farbchipzeilen (oder Farbmuster) im <strong>Bereich Standardfarben.</strong><br/></td>
</tr>
<tr class="odd">
<td>ThemeColorGridRows</td>
<td>Die Anzahl der Farbchipzeilen (oder Farbmuster) im <strong>Bereich Designfarben.</strong><br/> Nur gültig, <em>wenn ColorTemplate</em> über den Wert <code>ThemeColors</code> verfügt.<br/></td>
</tr>
</tbody>
</table>



 

Die folgenden Screenshots veranschaulichen die Drop-Down Farbwähler Layouts für die drei Farbvorlagen.



|     &nbsp;     |  &nbsp;   | &nbsp;  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ThemeColors`: Screenshot des Dropdowncolorpicker-Elements mit dem Colortemplate-Attribut, das auf \[ \] ![ "themecolors" festgelegt ist. ](images/markup/colortemplate.themedcolors.1.png) \[ Zeilenumbruch\] | `standardcolors`: \[ Screenshot des \] ![ Dropdowncolorpicker-Elements mit dem colortemplate-Attribut, das auf "standardcolors" festgelegt ist. ](images/markup/colortemplate.standardcolors.3.png) \[ Zeilenumbruch\] | `highlightcolors`: Screenshot des Dropdowncolorpicker-Elements mit dem Colortemplate-Attribut, das auf \[ \] ![ "highlightcolors" festgelegt ist.](images/markup/colortemplate.highlightcolors.2.png)<br/> |



 

Das grundlegende Markup, das für jeden Drop-Down Farbwähler erforderlich ist, wird in den folgenden Beispielen gezeigt:

> [!Note]  
> Der Drop-Down Farbwähler ist ein gültiges [Button-Steuerelement](windowsribbon-controls-button.md) in einer [**SizeDefinition-Vorlage.**](windowsribbon-element-sizedefinition.md)

 


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





## <a name="code"></a>Code

Als spezialisiertes Steuerelement, das Anpassungen unterstützt, erfordert jede Implementierung der Drop-Down Farbwähler, die diese Funktionen nutzt, speziellen Anwendungscode, um Eigenschaften zu verwalten und alle vom Steuerelement ausgegebenen Befehle zu verarbeiten.

### <a name="properties"></a>Eigenschaften

Das Menübandframework definiert eine Auflistung von [Eigenschaftsschlüsseln für](windowsribbon-reference-properties.md) das Drop-Down Farbwähler Steuerelement.

In der Regel wird eine Drop-Down Farbwähler-Eigenschaft in der Menübandbenutzeroberfläche aktualisiert, indem der befehl, der dem Steuerelement zugeordnet ist, durch einen Aufruf der [**IUIFramework::InvalidateUICommand-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig wird. Das Invalidierungsereignis wird von der [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) behandelt und die Eigenschaft aktualisiert.

Die [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird nicht ausgeführt, und die Anwendung fragt einen aktualisierten Eigenschaftswert ab, bis die Eigenschaft vom Framework benötigt wird. Beispielsweise, wenn eine Registerkarte aktiviert und ein Steuerelement auf der Menübandbenutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft über die [**IUIFramework::GetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) abgerufen und mit der [**IUIFramework::SetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschaftenschlüssel aufgeführt, die dem Steuerelement Drop-Down Farbwähler sind.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschaftsschlüssel</th>
<th>BESCHREIBUNG</th>
<th>Hinweise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></td>
<td>Definiert die Bezeichnung für die Schaltfläche <strong>Automatische</strong> Farbe.<br/> Nur gültig, <em>wenn ColorTemplate</em> über den Wert oder <code>ThemeColors</code> <code>StandardColors</code> verfügt.<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></td>
<td>Definiert den ausgewählten Farbwert als <a href="/windows/win32/gdi/colorref">COLORREF.</a><br/> Nur gültig, <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> den Wert <code>UI_SWATCHCOLORTYPE_RGB</code> hat.<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></td>
<td>Definiert den ausgewählten Farbtyp.<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Definiert die Fähigkeit eines Steuerelements, auf Benutzerinteraktion zu reagieren.<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>

<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Definiert die Zeichenfolge für eine Steuerelementbezeichnung.<br/></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Definiert das große Bild mit hohem Kontrast, das für ein Steuerelement angezeigt werden soll.<br/></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.<br/> Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menübandbildressourcen.</a><br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Definiert das große Bild, das für ein Steuerelement angezeigt werden soll.<br/></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.<br/> Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menübandbildressourcen.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></td>
<td>Definiert die Bezeichnung für die <strong>Schaltfläche Weitere Farben...</strong> .<br/> Nur gültig, <em>wenn ColorTemplate</em> über den Wert oder <code>ThemeColors</code> <code>StandardColors</code> verfügt.<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></td>
<td>Definiert die Bezeichnung für die <strong>Schaltfläche Keine</strong> Farbe.<br/> Gültig für alle <em>ColorTemplate-Werte.</em><br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></td>
<td>Definiert die Bezeichnung für die <strong>Kategorie Zuletzt verwendete</strong> Farben.<br/> Nur gültig, <em>wenn ColorTemplate</em> über den Wert <code>ThemeColors</code> verfügt. Dies ist die einzige Vorlage, die bezeichnete Kategorien enthält.<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Definiert das kleine Bild mit hohem Kontrast, das für ein Steuerelement angezeigt werden soll.<br/></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.<br/> Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menübandbildressourcen.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Definiert das kleine Bild, das für ein Steuerelement angezeigt werden soll.<br/></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.<br/> Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menübandbildressourcen.</a><br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></td>
<td>Definiert ein Array von <a href="/windows/win32/gdi/colorref">COLORREF-Werten</a> für die Muster eines Drop-Down Farbwähler.<br/> Jede Drop-Down Farbwähler <em>ColorTemplate</em> enthält ein <code>StandardColors</code> Raster. <br/>
<blockquote>
[!Note]<br />
Die <a href="/windows/win32/gdi/colorref">COLORREF-Werte</a> aus den <em>anfänglichen StandardColorGridRows</em> <em>x-Spalten</em> des Arrays werden angezeigt. Wenn das Array weniger Farben als die Anzahl der <code>StandardColors</code> im Markup deklarierten Farbfelder definiert, werden leere Leerzeichen für die fehlenden Chips angezeigt.
</blockquote>
<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></td>
<td>Definiert die Bezeichnung für die Kategorie <strong>Standardfarben.</strong><br/> Nur gültig, wenn <em>ColorTemplate</em> über den Wert <code>ThemeColors</code> verfügt. Dies ist die einzige Vorlage, die bezeichnete Kategorien enthält.<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></td>
<td>Definiert ein Zeichenfolgenarray mit Farbwatch-QuickInfos für das <code>StandardColors</code> Raster.<br/> Jede Drop-Down Farbwähler <em>ColorTemplate</em> enthält ein <code>StandardColors</code> Raster. <br/>
<blockquote>
[!Note]<br />
Es werden nur die QuickInfos verwendet, die zum Bezeichnen der im Raster angezeigten Farbwatches erforderlich <code>StandardColors</code> sind. Wenn weniger Bezeichnungen bereitgestellt werden als die Anzahl von Mustern im <code>StandardColors</code> Raster, wird ein Standardwert für die beibehaltenen Muster bereitgestellt.
</blockquote>
<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></td>
<td>Definiert ein Array von <a href="/windows/win32/gdi/colorref">COLORREF-Werten</a> für die Muster eines Drop-Down Farbwähler.<br/> Nur gültig, wenn <em>ColorTemplate</em> über den Wert <code>ThemeColors</code> verfügt. <br/>
<blockquote>
[!Note]<br />
Die <a href="/windows/win32/gdi/colorref">COLORREF-Werte</a> aus den <em>anfänglichen ThemeColorGridRows</em> <em>x-Spalten</em> des Arrays werden angezeigt. Wenn das Array weniger Farben als die Anzahl der <code>ThemeColors</code> im Markup deklarierten Farbfelder definiert, werden leere Leerzeichen für die fehlenden Chips angezeigt.
</blockquote>
<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></td>
<td>Definiert das Zeichenfolgenarray der Farbwatch-QuickInfos für das <code>ThemeColors</code> Raster.<br/> Nur gültig, wenn <em>ColorTemplate</em> über den Wert <code>ThemeColors</code> verfügt. <br/>
<blockquote>
[!Note]<br />
Es werden nur die QuickInfos verwendet, die zum Bezeichnen der im Raster angezeigten Farbwatches erforderlich <code>ThemeColors</code> sind. Wenn weniger Bezeichnungen bereitgestellt werden als die Anzahl von Mustern im <code>ThemeColors</code> Raster, wird ein Standardwert für die beibehaltenen Muster bereitgestellt.
</blockquote>
<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></td>
<td>Definiert die Bezeichnung für die Kategorie <strong>Designfarben.</strong><br/> Nur gültig, wenn <em>ColorTemplate</em> über den Wert <code>ThemeColors</code> verfügt. Dies ist die einzige Vorlage, die bezeichnete Kategorien enthält.<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Definiert die Zeichenfolge für eine QuickInfo-Beschreibung, die einem <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>zugeordnet ist.<br/></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Definiert die Zeichenfolge für eine Befehls-QuickInfo.<br/></td>
<td>Kann nur durch Ungültigkeit aktualisiert werden.</td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a>Befehlshandler

Die [**IUICommandHandler::UpdateProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird verwendet, um einen Drop-Down Farbwähler über die oben aufgeführten Eigenschaftsschlüssel anzupassen. Im folgenden Beispiel wird veranschaulicht, wie die Farbwatches eines Drop-Down Farbwähler basierend auf einer benutzerdefinierten Stilpräferenz oder einem im Markup deklarierten benutzerdefinierten Farbmusterraster festgelegt werden.


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



Im folgenden Beispiel wird eine Implementierung der [**IUICommandHandler::Execute-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) veranschaulicht, die die Drop-Down Farbwähler Farbmuster für die Menübandanwendung verfügbar macht.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Framework-Steuerelementbibliothek für Windows-Menüband](windowsribbon-controls-entry.md)
</dt> <dt>

[**DropDownColorPicker-Markupelement**](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[Farbwähler-Eigenschaften](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[Anpassen eines Menübands durch Größendefinitionen und Skalierungsrichtlinien](windowsribbon-templates.md)
</dt> <dt>

[DropDownColorPicker-Beispiel](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

