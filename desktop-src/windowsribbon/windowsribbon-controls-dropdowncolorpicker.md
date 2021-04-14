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
# <a name="drop-down-color-picker"></a>Drop-Down Farbauswahl

Das Windows-Menü Band Framework bietet ein spezielles Steuerelement für die Drop-Down Farbauswahl, das eine Vielzahl von Farbeinstellungen über eine unterteilte Schaltfläche und eine anpassbare Dropdown-Farbauswahl verfügbar macht

-   [Introduction (Einführung)](#introduction)
-   [Markup](#markup)
-   [Code](#code)
    -   [Eigenschaften](#properties)
    -   [Befehls Handler](#command-handlers)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Durch Emulierung des Erscheinungs Bilds und der Funktionalität der Microsoft Office Farbauswahl kann das Menüband-Framework sowohl von profitieren als auch an Konsistenz und Vertrautheit in einer Vielzahl von Anwendungen mitwirken.

## <a name="markup"></a>Markup

Wie alle multifunktionsleistensteuerelemente kann die Drop-Down Farbauswahl problemlos implementiert und durch Markup angepasst werden. Das Framework bietet eine Reihe von Element Attributen für die Drop-Down Farbauswahl, um verschiedene Funktionsebenen verfügbar zu machen. In der folgenden Tabelle sind die Drop-Down Farbauswahl Attribute aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Colortemplate</td>
<td>Layoutvorlagen, die den Typ der Drop-Down Farbauswahl angeben.<br/> Es gibt drei Vorlagen, von denen jedes ein Steuerelement Layout und Standardwerte für zugeordnete Attribute und Eigenschafts Schlüssel angibt. <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td>Chipgröße</td>
<td>Die Größe jedes Farbchips (oder Musters).<br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td>Spalten</td>
<td>Die Anzahl der farbchipspalten (oder Muster Spalten).<br/></td>
</tr>
<tr class="even">
<td>CommandName</td>
<td>Der Name der zugeordneten Befehls Deklaration. <br/></td>
</tr>
<tr class="odd">
<td>Isautomaticcolorbuttonvisible</td>
<td>Zeigt die Schaltfläche <strong>automatisch</strong> an (oder blendet sie aus).<br/> Nur gültig, wenn <em>colortemplate</em> den Wert <code>ThemeColors</code> oder aufweist <code>StandardColors</code> .<br/></td>
</tr>
<tr class="even">
<td>Isnocolorbuttonvisible</td>
<td>Zeigt die Schaltfläche <strong>keine Farbe</strong> an (oder blendet sie aus).<br/> Gültig für alle <em>colortemplate</em> -Werte.<br/></td>
</tr>
<tr class="odd">
<td>Recentcolorgridrows</td>
<td>Die Anzahl der farbchipzeilen (oder Muster Zeilen) im Bereich " <strong>Letzte Farben</strong> ".<br/> Nur gültig, wenn <em>colortemplate</em> den Wert hat <code>ThemeColors</code> .<br/></td>
</tr>
<tr class="even">
<td>Standardcolorgridrows</td>
<td>Die Anzahl der farbchipzeilen (oder Muster Zeilen) im <strong>Standard Farben</strong> Bereich.<br/></td>
</tr>
<tr class="odd">
<td>"Mecolorgridrows"</td>
<td>Die Anzahl der farbchipzeilen (oder Muster Zeilen) im Design <strong>Farben</strong> Bereich.<br/> Nur gültig, wenn <em>colortemplate</em> den Wert hat <code>ThemeColors</code> .<br/></td>
</tr>
</tbody>
</table>



 

Die folgenden Bildschirmfotos veranschaulichen die standardmäßigen Drop-Down Farbauswahl Layouts für die drei Farbvorlagen.



|                                                                                                                                                                                               |                                                                                                                                                                                                       |                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ThemeColors`: \[ Zeilen \] ![ Vorschub für das dropdowncolorpicker-Element, bei dem das colortemplate-Attribut auf "thmecolors" festgelegt ist. ](images/markup/colortemplate.themedcolors.1.png) \[ Zeilenumbruch\] | `standardcolors`: \[ Zeilen \] ![ Vorschub für das dropdowncolorpicker-Element, bei dem das colortemplate-Attribut auf ' standardcolors ' festgelegt ist. ](images/markup/colortemplate.standardcolors.3.png) \[ Zeilenumbruch\] | `highlightcolors`: \[ Zeilen \] ![ Vorschub für das dropdowncolorpicker-Element, bei dem das colortemplate-Attribut auf ' highlightcolors ' festgelegt ist.](images/markup/colortemplate.highlightcolors.2.png)<br/> |



 

Das grundlegende Markup, das für die einzelnen Drop-Down Farbauswahl Typen erforderlich ist, wird in den folgenden Beispielen veranschaulicht:

> [!Note]  
> Die Drop-Down Farbauswahl ist ein gültiges [Schalt](windowsribbon-controls-button.md) Flächen-Steuerelement in einer [**sizedefinition**](windowsribbon-element-sizedefinition.md) -Vorlage.

 


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

Als spezialisiertes Steuerelement, das die Anpassung unterstützt, erfordert jede Implementierung der Drop-Down Farbauswahl, die diese Funktionen nutzt, speziellen Anwendungscode, um Eigenschaften zu verwalten und alle Befehle zu verarbeiten, die vom Steuerelement ausgegeben werden.

### <a name="properties"></a>Eigenschaften

Das Menüband-Framework definiert eine Auflistung von [Eigenschafts Schlüsseln](windowsribbon-reference-properties.md) für das Drop-Down Farbauswahl-Steuerelement.

In der Regel wird eine Drop-Down Color-Auswahl Eigenschaft in der Menüband-Benutzeroberfläche aktualisiert, indem der Befehl, der dem Steuerelement zugeordnet ist, durch einen Rückruf der [**iuiframework:: invalidateuicommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) -Methode ungültig gemacht wird. Das Invalidierung-Ereignis wird durch die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode behandelt und die Eigenschaften Updates definiert.

Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Rückruf Methode wird nicht ausgeführt, und die Anwendung wird nach einem aktualisierten Eigenschafts Wert abgefragt, bis die Eigenschaft vom Framework benötigt wird. Wenn z. b. eine Registerkarte aktiviert ist und ein Steuerelement in der Menüband-Benutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft durch die [**iuiframework:: getuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) -Methode abgerufen und mit der [**iuiframework:: setuicommandproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) -Methode festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschafts Schlüssel aufgelistet, die dem Steuerelement Drop-Down Color Picker zugeordnet sind.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschafts Schlüssel</th>
<th>BESCHREIBUNG</th>
<th>Notizen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></td>
<td>Definiert die Bezeichnung für die <strong>Automatische</strong> Farb Schaltfläche.<br/> Nur gültig, wenn <em>colortemplate</em> den Wert <code>ThemeColors</code> oder aufweist <code>StandardColors</code> .<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></td>
<td>Definiert den ausgewählten Farbwert als <a href="/windows/win32/gdi/colorref">COLORREF</a>.<br/> Nur gültig, wenn <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> den Wert hat <code>UI_SWATCHCOLORTYPE_RGB</code> .<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></td>
<td>Definiert den ausgewählten Farbtyp.<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Definiert die Fähigkeit eines Steuer Elements, auf Benutzerinteraktionen zu reagieren.<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>

<td>Kann nur durch Invalidierung aktualisiert werden.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Definiert die Zeichenfolge für eine Steuerelement Bezeichnung.<br/></td>
<td>Kann nur durch Invalidierung aktualisiert werden.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Definiert das große Bild mit hohem Kontrast, das für ein Steuerelement angezeigt werden soll.<br/></td>
<td>Kann nur durch Invalidierung aktualisiert werden.<br/> Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menüband-Bild Ressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Definiert das große Bild, das für ein Steuerelement angezeigt werden soll.<br/></td>
<td>Kann nur durch Invalidierung aktualisiert werden.<br/> Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menüband-Bild Ressourcen</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></td>
<td>Definiert die Bezeichnung für die Schaltfläche mit den <strong>weiteren Farben...</strong><br/> Nur gültig, wenn <em>colortemplate</em> den Wert <code>ThemeColors</code> oder aufweist <code>StandardColors</code> .<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></td>
<td>Definiert die Bezeichnung für die Schaltfläche <strong>keine Farbe</strong> .<br/> Gültig für alle <em>colortemplate</em> -Werte.<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></td>
<td>Definiert die Bezeichnung für die Kategorie " <strong>zuletzt verwendete Farben</strong> ".<br/> Nur gültig, wenn <em>colortemplate</em> den Wert hat <code>ThemeColors</code> . Dies ist die einzige Vorlage, die bezeichnete Kategorien enthält.<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Definiert das kleine Bild mit hohem Kontrast, das für ein Steuerelement angezeigt werden soll.<br/></td>
<td>Kann nur durch Invalidierung aktualisiert werden.<br/> Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menüband-Bild Ressourcen</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Definiert das kleine Bild, das für ein Steuerelement angezeigt werden soll.<br/></td>
<td>Kann nur durch Invalidierung aktualisiert werden.<br/> Weitere Informationen zu Bildformaten finden Sie unter <a href="windowsribbon-imageformats.md">Angeben von Menüband-Bild Ressourcen</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></td>
<td>Definiert ein Array von <a href="/windows/win32/gdi/colorref">COLORREF</a> -Werten für die Dragquellen einer Drop-Down Farbauswahl.<br/> Jede Drop-Down Farbauswahl <em>colortemplate</em> enthält ein <code>StandardColors</code> Raster. <br/>
<blockquote>
[!Note]<br />
Die <a href="/windows/win32/gdi/colorref">COLORREF</a> -Werte aus den anfänglichen <em>standardcolorgridrows</em> x- <em>Spalten</em> des Arrays werden angezeigt. Wenn das Array weniger Farben als die Anzahl der <code>StandardColors</code> im Markup deklarierten Dragquellen definiert, werden leere Leerzeichen für die fehlenden Chips angezeigt.
</blockquote>
<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></td>
<td>Definiert die Bezeichnung für die Kategorie " <strong>Standard Farben</strong> ".<br/> Nur gültig, wenn <em>colortemplate</em> den Wert hat <code>ThemeColors</code> . Dies ist die einzige Vorlage, die bezeichnete Kategorien enthält.<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></td>
<td>Definiert ein Zeichen folgen Array von Farbmuster-Quick Infos für das <code>StandardColors</code> Raster.<br/> Jede Drop-Down Farbauswahl <em>colortemplate</em> enthält ein <code>StandardColors</code> Raster. <br/>
<blockquote>
[!Note]<br />
Es werden nur die Quick Infos verwendet, die zum bezeichnen der im Raster angezeigten farbsüberwachungen erforderlich <code>StandardColors</code> sind. Wenn weniger Bezeichnungen als die Anzahl der Dragquellen im <code>StandardColors</code> Raster bereitgestellt werden, wird für die restlichen Swatch ein Standardwert bereitgestellt.
</blockquote>
<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></td>
<td>Definiert ein Array von <a href="/windows/win32/gdi/colorref">COLORREF</a> -Werten für die Dragquellen einer Drop-Down Farbauswahl.<br/> Nur gültig, wenn <em>colortemplate</em> den Wert hat <code>ThemeColors</code> . <br/>
<blockquote>
[!Note]<br />
Die <a href="/windows/win32/gdi/colorref">COLORREF</a> -Werte aus den anfänglichen " <em>temecolorgridrows</em> x"- <em>Spalten</em> des Arrays werden angezeigt. Wenn das Array weniger Farben als die Anzahl der <code>ThemeColors</code> im Markup deklarierten Dragquellen definiert, werden leere Leerzeichen für die fehlenden Chips angezeigt.
</blockquote>
<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></td>
<td>Definiert das Zeichen folgen Array von Farbmuster-Quick Infos für das <code>ThemeColors</code> Raster.<br/> Nur gültig, wenn <em>colortemplate</em> den Wert hat <code>ThemeColors</code> . <br/>
<blockquote>
[!Note]<br />
Es werden nur die Quick Infos verwendet, die zum bezeichnen der im Raster angezeigten farbsüberwachungen erforderlich <code>ThemeColors</code> sind. Wenn weniger Bezeichnungen als die Anzahl der Dragquellen im <code>ThemeColors</code> Raster bereitgestellt werden, wird für die restlichen Swatch ein Standardwert bereitgestellt.
</blockquote>
<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></td>
<td>Definiert die Bezeichnung für die Kategorie Design <strong>Farben</strong> .<br/> Nur gültig, wenn <em>colortemplate</em> den Wert hat <code>ThemeColors</code> . Dies ist die einzige Vorlage, die bezeichnete Kategorien enthält.<br/></td>
<td>Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>iuiframework:: getuicommandproperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>iuiframework:: abtuicommandproperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Definiert die Zeichenfolge für eine QuickInfo-Beschreibung, die einem <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>zugeordnet ist.<br/></td>
<td>Kann nur durch Invalidierung aktualisiert werden.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Definiert die Zeichenfolge für eine Befehls-QuickInfo.<br/></td>
<td>Kann nur durch Invalidierung aktualisiert werden.</td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a>Befehls Handler

Die [**iuicommandhandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) -Methode wird zum Anpassen einer Drop-Down Farbauswahl über die oben aufgeführten Eigenschaften Schlüssel verwendet. Im folgenden Beispiel wird veranschaulicht, wie die farbswatch einer Drop-Down Farbauswahl basierend auf einer benutzerdefinierten Formatvorlage oder einem benutzerdefinierten Muster Raster, das im Markup deklariert ist, festgelegt wird.


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



Im folgenden Beispiel wird eine Implementierung der [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Methode veranschaulicht, die die Muster Farben der Drop-Down Farbauswahl für die Menüband-Anwendung verfügbar macht.


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

[Windows-Menüband-Steuerelement Bibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**Dropdowncolorpicker-Markup Element**](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[Farbauswahl Eigenschaften](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md)
</dt> <dt>

[Dropdowncolorpicker-Beispiel](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

