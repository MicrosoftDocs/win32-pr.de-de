---
title: DropDownColorPicker-Element
description: Stellt ein Drop-Down Farbauswahlsteuerfeld dar, das eine Palette von Farbmustern anzeigt, wenn darauf geklickt wird.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- DropDownColorPicker-Element Windows Menüband
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31525ee1b7233f0bf49668856d917ef14bc034b6
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622886"
---
# <a name="dropdowncolorpicker-element"></a>DropDownColorPicker-Element

Stellt ein [Dropdown-Farbwähler-Steuerelement](windowsribbon-controls-dropdowncolorpicker.md)dar, das beim Klicken eine Palette von Farbüberwachungen anzeigt.

## <a name="usage"></a>Verwendung

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

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Typ</th>
<th>Erforderlich</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ChipSize</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Die Größe der einzelnen Farbchips oder Farbwatches. <br/> Beschränkt auf einen der folgenden Werte:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Klein)<br/> </dt> <dd> Jeder Farbchip ist ein Quadrat mit 11 x 11 Pixeln. <br/> </dd> <dt><span></span><span></span><strong></strong> (Mittel)<br/> </dt> <dd> Jeder Farbchip ist ein Quadrat mit 16 x 16 Pixeln. <br/> </dd> <dt><span></span><span></span><strong></strong> (Groß)<br/> </dt> <dd> Jeder Farbchip ist ein Quadrat mit 24 x 24 Pixeln. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ColorTemplate</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Layoutvorlagen, die den Typ der <a href="windowsribbon-controls-dropdowncolorpicker.md">Dropdown-Farbwähler</a>angeben. <br/> Beschränkt auf einen der folgenden Werte (wenn keine optionalen Attribute im Zusammenhang mit einer <em>ColorTemplate</em> deklariert werden, wird die Standardansicht angezeigt):<br/> <br/>
<dt><span></span><span></span><strong></strong> (ThemeColors)<br/> </dt> <dd> Standard. <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> Das Festlegen des <em>ColorTemplate-Attributs</em> auf <code>ThemeColors</code> ermöglicht die folgende Funktionalität:<br/>
<ul>
<li>SplitButton-Anker.</li>
<li>Die <strong>automatische</strong> Farbschaltfläche wird standardmäßig angezeigt.</li>
<li>Windows Farbmusterraster <strong>für Designfarben.</strong></li>
<li><strong>Standardfarben–</strong> Musterraster.</li>
<li>Das Farbmusterraster <strong>"Zuletzt verwendet"</strong> ist optional.</li>
<li><strong>Startfeld</strong> für weitere Farben.</li>
<li>Standardmäßig wird <strong>keine Farbfarbe</strong> angezeigt.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (StandardColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> Das Festlegen des <em>ColorTemplate-Attributs</em> auf <code>StandardColors</code> ermöglicht die folgende Funktionalität:<br/>
<ul>
<li>SplitButton-Anker.</li>
<li>Die <strong>automatische</strong> Farbschaltfläche wird standardmäßig angezeigt.</li>
<li><strong>Standardfarben–</strong> Musterraster.</li>
<li><strong>Startfeld</strong> für weitere Farben.</li>
<li>Standardmäßig wird <strong>keine Farbfarbe</strong> angezeigt.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (HighlightColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> Das Festlegen des <em>ColorTemplate-Attributs</em> auf <code>HighlightColors</code> ermöglicht die folgende Funktionalität:<br/>
<ul>
<li>SplitButton-Anker.</li>
<li>Musterraster für <strong>Standardfarben</strong> ohne Kopfzeile.</li>
<li>Standardmäßig wird <strong>keine Farbfarbe</strong> angezeigt.</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Spalten</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td>Die Anzahl der Farbchipspalten (oder Farbmusterspalten).<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 einschließlich.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger oder xs:string<br/></td>
<td>Nein<br/></td>
<td>Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999( einschließlich) oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich. <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsAutomaticColorButtonVisible</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Zeigt die Schaltfläche <strong>Automatische</strong> Farbe an (oder blendet sie aus). <br/> Nur gültig, wenn <code>StandardColors</code> oder <code>ThemeColors</code> für das <em>ColorTemplate-Attribut</em> angegeben ist. <br/> Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsNoColorButtonVisible</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Zeigt die Schaltfläche <strong>Keine Farbe</strong> an (oder blendet sie aus). <br/> Gültig für alle <em>ColorTemplate-Werte.</em><br/> Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>RecentColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td>Die Anzahl von Farbchipzeilen (oder Farbmusterzeilen) im Bereich <strong>Zuletzt verwendeten Farben.</strong> <br/> Nur gültig, wenn <code>ThemeColors</code> für das <em>ColorTemplate-Attribut</em> angegeben ist.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 einschließlich.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>StandardColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td>Die Anzahl von Farbchipzeilen (oder Farbmusterzeilen) im <strong>Bereich Standardfarben.</strong><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 einschließlich.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ThemeColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td>Die Anzahl von Farbchipzeilen (oder Farbmusterzeilen) im Bereich <strong>Designfarben.</strong><br/> Nur gültig, wenn <code>ThemeColors</code> für das <em>ColorTemplate-Attribut</em> angegeben ist.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 einschließlich.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>         |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Gruppe**](windowsribbon-element-group.md)<br/>                           |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann ein oder mehrere Male für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) [**DropDownButton-,**](windowsribbon-element-dropdownbutton.md) [**DropDownGallery-,**](windowsribbon-element-dropdowngallery.md) [**Group-,**](windowsribbon-element-group.md) [**MenuGroup-,**](windowsribbon-element-menugroup.md) [**SplitButton-**](windowsribbon-element-splitbutton.md)oder [**SplitButtonGallery-Element**](windowsribbon-element-splitbuttongallery.md) auftreten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für alle drei Typen von [Dropdown-Farbwähler.](windowsribbon-controls-dropdowncolorpicker.md)

Dieser Codeabschnitt zeigt die Befehlsdeklarationen für drei **DropDownColorPicker-Elemente.**


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



In diesem Codeabschnitt werden die drei Typen von **DropDownColorPicker-Steuerelementdeklarationen** veranschaulicht.


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



## <a name="element-information"></a>Elementinformationen

* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Ja



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Dropdown-Farbwähler Steuerelement](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[DropDownColorPicker-Beispiel](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





