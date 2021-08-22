---
title: SplitButtonGallery-Element
description: Stellt ein Split Button Gallery-Steuerelement mit einem katalogbasierten Dropdownmenü dar.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- SplitButtonGallery-Element Windows Menüband
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c2f954d7b96d3ec2304cd63cd689241a46384fda
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626736"
---
# <a name="splitbuttongallery-element"></a>SplitButtonGallery-Element

Stellt ein [Split Button Gallery-Steuerelement](windowsribbon-controls-splitbuttongallery.md) mit einem katalogbasierten Dropdownmenü dar.

## <a name="usage"></a>Verwendung

``` syntax
<SplitButtonGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</SplitButtonGallery>
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
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Nur gültig, <a href="windowsribbon-element-menugroup.md"><strong>wenn MenuGroup</strong></a> das übergeordnete Element ist.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die eine durch Komma getrennte Liste von ganzen Zahlen zwischen 0 und 31 enthält.<br/> Leerzeichen sind gültig und werden ignoriert.<br/> Maximale Länge: 250 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger oder xs:string<br/></td>
<td>Nein<br/></td>
<td>Ordnet das Element einem Befehl <a href="windowsribbon-element-command.md"><strong>zu.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich. <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>HasLargeItems</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Bestimmt, ob die große oder kleine Bildressource des Befehls im Katalog-Steuerelement angezeigt wird. <br/>
<blockquote>
[!Note]<br />
Gilt nur für Kataloge, in denen der Wert des <em>Type-Attributs</em> gleich <code>Command</code> ist.
</blockquote>
<br/> Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Itemheight</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Der Standard ist -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ItemWidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Der Standard ist -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>TextPositionType<br/></td>
<td>Nein<br/></td>
<td>Auf einen der folgenden Werte beschränkt:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Unten)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Ausblenden)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Links)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Überlappung)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Rechts)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Oben)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Typ</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Auf einen der folgenden Werte beschränkt:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Elemente)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Befehle)<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                 | Beschreibung                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Schaltfläche**](windowsribbon-element-button.md)<br/>                                               | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**CheckBox**](windowsribbon-element-checkbox.md)<br/>                                           | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                     | Kann ein oder mehrere Male auftreten.<br/> <br/> |
| [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | Muss genau einmal auftreten<br/> <br/>     |
| [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | Kann nur einmal auftreten.<br/> <br/>      |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                                   | Kann ein oder mehrere Male auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Gruppe</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-menugroup.md"><strong>Menugroup</strong></a><br/></td>
<td>Wenn in einem <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu enthalten ist.</strong></a> Dieses Element wird nur auf der ersten Ebene unterstützt und darf keine untergeordneten Elemente enthalten.<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 und neuer.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a>Hinweise

Optional.

Kann ein oder mehrere Male für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) [**Group-,**](windowsribbon-element-group.md) [**MenuGroup-**](windowsribbon-element-menugroup.md)oder [**SplitButton-Element**](windowsribbon-element-splitbutton.md) auftreten.

**SplitButtonGallery unterstützt** [anwendungsmodi](ribbon-applicationmodes.md).

[Benutzeroberfläche \_ PKEY \_ BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) wird von einer Anwendung verwendet, um den Umschaltzustand für das Schaltflächen-Steuerelement einer **SplitButtonGallery abzufragen.**

Der folgende Screenshot veranschaulicht das Steuerelement Ribbon [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) in Microsoft Paint für Windows 7.

![Screenshot eines Katalogsteuerfelds mit geteilter Schaltfläche in Microsoft Paint für Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für den [Split Button Gallery veranschaulicht.](windowsribbon-controls-splitbuttongallery.md)

Dieser Codeabschnitt zeigt die **Deklarationen des SplitButtonGallery-Befehls** mit einer zugeordneten [**Gruppe,**](windowsribbon-element-group.md) die als übergeordneter Container für das **SplitButtonGallery-Element** fungiert.


```XML
<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"/>
```



Dieser Codeabschnitt zeigt die **SplitButtonGallery-Steuerelementdeklarationen.**


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="element-information"></a>Elementinformationen


- **Unterstütztes Mindestsystem:** Windows 7 
- **Kann leer sein:** Nein



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Steuerelement "Katalog mit geteilten Schaltflächen"](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Arbeiten mit Katalogen](ribbon-controls-galleries.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[Katalogbeispiel](windowsribbon-gallerysample.md)
</dt> </dl>

 

