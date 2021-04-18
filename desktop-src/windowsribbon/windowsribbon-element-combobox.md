---
title: ComboBox-Element
description: Stellt ein Kombinations Feld-Steuerelement dar.
ms.assetid: d796e26b-44c2-4e11-b1a5-2ede5bcff676
keywords:
- Windows-Menüband für ComboBox-Element
topic_type:
- apiref
api_name:
- ComboBox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5bdcc95c64c2bd60df4f2f53d3bd3699c0a7ee65
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "106340680"
---
# <a name="combobox-element"></a>ComboBox-Element

Stellt ein Kombinations [Feld](windowsribbon-controls-combobox.md) -Steuerelement dar.

## <a name="usage"></a>Verbrauch

``` syntax
<ComboBox
  CommandName = "xs:positiveInteger or xs:string"
  IsEditable = "Boolean"
  ResizeType = "ComboBoxResizeType"
  IsAutoCompleteEnabled = "Boolean"/>
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
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveingeteger oder xs: String<br/></td>
<td>Nein<br/></td>
<td>Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich). <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Isautocompleteaktivierte</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsEditable</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Resizetype</strong><br/></td>
<td>Comboboxresizetype<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (NORESIZE)<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> (Verticalresize)<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-controlgroup.md"><strong>Controlgroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-dropdownbutton.md"><strong>DropDownButton</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-dropdowngallery.md"><strong>Dropdown Gallery</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>Quickaccesstoolbar. ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 und höher.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-splitbuttongallery.md"><strong>Splitbuttongallery</strong></a><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, [**DropDownButton**](windowsribbon-element-dropdownbutton.md)-, [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)-, [**Group**](windowsribbon-element-group.md)-, [**MenuGroup**](windowsribbon-element-menugroup.md)-oder [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Element einmal oder mehrmals vorkommen.

Da es sich bei der **ComboBox** ausschließlich um einen Element Katalog handelt, werden Befehls Elemente nicht unterstützt. Es ist auch das einzige Katalog Steuerelement, das keinen Befehlsbereich unterstützt (eine Auflistung von Befehlen, die im Markup deklariert und im unteren Bereich eines Element Katalogs oder einer Befehls Galerie aufgelistet sind). Weitere Informationen finden Sie unter [Arbeiten mit Galerien](ribbon-controls-galleries.md).

Der folgende Screenshot veranschaulicht ein Menüband-Kombinations [Feld](windowsribbon-controls-combobox.md) -Steuerelement von Windows Live Movie Maker.

![Screenshot eines ComboBox-Steuer Elements im Microsoft Paint-Menüband.](images/controls/combobox.png)

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird das grundlegende Markup für das Kombinations **Feld** veranschaulicht.

Dieser Code Abschnitt zeigt die **ComboBox** -Befehls Deklarationen mit einer zugeordneten [**Gruppe**](windowsribbon-element-group.md) , die als übergeordneter Container für das **ComboBox** -Element fungiert.


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```



Dieser Code Abschnitt zeigt die **ComboBox** -Steuerelement Deklarationen.


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



## <a name="element-information"></a>Elementinformationen



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Ja       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kombinationsfeld-Steuerelement](windowsribbon-controls-combobox.md)
</dt> <dt>

[Galerie Beispiel](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





