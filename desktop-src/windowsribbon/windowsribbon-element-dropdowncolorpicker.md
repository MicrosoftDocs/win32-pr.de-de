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
# <a name="dropdowncolorpicker-element"></a>Dropdowncolorpicker-Element

Stellt ein [Dropdown-Farbauswahl](windowsribbon-controls-dropdowncolorpicker.md)Steuerelement dar, das beim Klicken auf eine Palette von farbsuhren zeigt.

## <a name="usage"></a>Verbrauch

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
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>type</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Chipgröße</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Die Größe jedes Farbchips oder eines Musters. <br/> Beschränkt auf einen der folgenden Werte:<br/> <br/>
<dt><span></span><span></span><strong></strong> Zuletzt<br/> </dt> <dd> Jeder farbchip ist ein 11x11-Pixel Quadrat. <br/> </dd> <dt><span></span><span></span><strong></strong> Mittelalter<br/> </dt> <dd> Jeder farbchip ist ein 16x16-Pixel Quadrat. <br/> </dd> <dt><span></span><span></span><strong></strong> Viele<br/> </dt> <dd> Jeder farbchip ist ein rund um die Uhr großes Pixel Quadrat. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Colortemplate</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Layoutvorlagen, die den Typ der <a href="windowsribbon-controls-dropdowncolorpicker.md">Dropdown-Farbauswahl</a>angeben. <br/> Auf einen der folgenden Werte beschränkt (wenn keine optionalen Attribute, die sich auf eine <em>colortemplate</em> beziehen, deklariert sind, wird die Standardansicht angezeigt):<br/> <br/>
<dt><span></span><span></span><strong></strong> (Mecolors)<br/> </dt> <dd> Standard. <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> Durch Festlegen des <em>colortemplate</em> -Attributs auf werden <code>ThemeColors</code> die folgenden Funktionen aktiviert:<br/>
<ul>
<li>SplitButton-Anker.</li>
<li>Standardmäßig wird die <strong>Automatische</strong> Farb Schaltfläche angezeigt.</li>
<li>Fensterdesign <strong>Farben</strong> -Muster Raster.</li>
<li>Muster Raster für <strong>Standard Farben</strong> .</li>
<li><strong>Aktuelles Farb</strong> Muster Raster ist optional.</li>
<li>Dialogfeld " <strong>Weitere Farben</strong> ".</li>
<li>Standardmäßig wird <strong>keine Farb</strong> Farb Schaltfläche angezeigt.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (Standardcolors)<br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> Durch Festlegen des <em>colortemplate</em> -Attributs auf werden <code>StandardColors</code> die folgenden Funktionen aktiviert:<br/>
<ul>
<li>SplitButton-Anker.</li>
<li>Standardmäßig wird die <strong>Automatische</strong> Farb Schaltfläche angezeigt.</li>
<li>Muster Raster für <strong>Standard Farben</strong> .</li>
<li>Dialogfeld " <strong>Weitere Farben</strong> ".</li>
<li>Standardmäßig wird <strong>keine Farb</strong> Farb Schaltfläche angezeigt.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (Highlightcolors)<br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> Durch Festlegen des <em>colortemplate</em> -Attributs auf werden <code>HighlightColors</code> die folgenden Funktionen aktiviert:<br/>
<ul>
<li>SplitButton-Anker.</li>
<li>Muster Raster mit <strong>Standard Farben</strong> ohne Header.</li>
<li>Standardmäßig wird <strong>keine Farb</strong> Farb Schaltfläche angezeigt.</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Spalten</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td>Die Anzahl der farbchipspalten (oder Muster Spalten).<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positivin teger)<br/> </dt> <dd> Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 (einschließlich).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveingeteger oder xs: String<br/></td>
<td>Nein<br/></td>
<td>Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich). <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Isautomaticcolorbuttonvisible</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Zeigt die <strong>Automatische</strong> Farb Schaltfläche an oder blendet sie aus. <br/> Nur gültig, wenn <code>StandardColors</code> oder <code>ThemeColors</code> für das <em>colortemplate</em> -Attribut angegeben ist. <br/> Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Isnocolorbuttonvisible</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Zeigt die Schaltfläche <strong>keine Farbe</strong> an (oder blendet sie aus). <br/> Gültig für alle <em>colortemplate</em> -Werte.<br/> Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Recentcolorgridrows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td>Die Anzahl der farbchipzeilen (oder Muster Zeilen) im Bereich " <strong>Letzte Farben</strong> ". <br/> Nur gültig, wenn <code>ThemeColors</code> für das <em>colortemplate</em> -Attribut angegeben ist.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positivin teger)<br/> </dt> <dd> Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 (einschließlich).<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Standardcolorgridrows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td>Die Anzahl der farbchipzeilen (oder Muster Zeilen) im <strong>Standard Farben</strong> Bereich.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positivin teger)<br/> </dt> <dd> Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 (einschließlich).<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>"Mecolorgridrows"</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td>Die Anzahl der farbchipzeilen (oder Muster Zeilen) im Design <strong>Farben</strong> Bereich.<br/> Nur gültig, wenn <code>ThemeColors</code> für das <em>colortemplate</em> -Attribut angegeben ist.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positivin teger)<br/> </dt> <dd> Ein beliebiger positiver ganzzahliger Wert zwischen 1 und 256 (einschließlich).<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                           |
|-----------------------------------------------------------------------------------|
| [**Controlgroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>         |
| [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Gruppe**](windowsribbon-element-group.md)<br/>                           |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, [**DropDownButton**](windowsribbon-element-dropdownbutton.md)-, [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)-, [**Group**](windowsribbon-element-group.md)-, [**MenuGroup**](windowsribbon-element-menugroup.md)-, [**SplitButton**](windowsribbon-element-splitbutton.md)-oder [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Element einmal oder mehrmals vorkommen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für alle drei Typen der [Dropdown-Farbauswahl](windowsribbon-controls-dropdowncolorpicker.md)veranschaulicht.

Dieser Code Abschnitt zeigt die Befehls Deklarationen für drei **dropdowncolorpicker** -Elemente.


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



In diesem Code Abschnitt werden die drei Typen von **dropdowncolorpicker** -Steuerelement Deklarationen veranschaulicht.


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



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Ja       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Dropdown-Farbauswahl-Steuerelement](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[Dropdowncolorpicker-Beispiel](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





