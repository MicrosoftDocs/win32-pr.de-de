---
title: "\"Element\"-Element"
description: Stellt ein UMSCHALT Fläche-Steuerelement dar.
ms.assetid: f26a90e6-9e9a-4fde-8753-50b8b1d09f80
keywords:
- Menüband für das Fenster "Element" (Fenster)
topic_type:
- apiref
api_name:
- ToggleButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 652ea7b535f41cc3dbb40f25bbe49ab4fe52f5ff
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104314135"
---
# <a name="togglebutton-element"></a>"Element"-Element

Stellt ein [UMSCHALT Fläche](windowsribbon-controls-togglebutton.md) -Steuerelement dar.

## <a name="usage"></a>Verbrauch

``` syntax
<ToggleButton
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
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
<td><strong>ApplicationDefaults. IsChecked</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Dieses Attribut ist nur gültig, wenn das <strong>ToggleButton</strong> -Element ein untergeordnetes Element von <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>quickaccesstoolbar. ApplicationDefaults</strong></a>ist. <br/> Beschränkt auf einen der folgenden Werte:<br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveingeteger oder xs: String<br/></td>
<td>Nein<br/></td>
<td>Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich). <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [**Controlgroup**](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [**Gruppe**](windowsribbon-element-group.md)<br/>                                                                   |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                                                           |
| [**Quickaccesstoolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [**SplitButton. buttonitem**](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a>Bemerkungen

Optional oder erforderlich, abhängig vom übergeordneten Element.

Kann höchstens einmal für jedes [**SplitButton. buttonitem**](windowsribbon-element-splitbutton-buttonitem.md) -Element auftreten.

Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md)-, [**DropDownButton**](windowsribbon-element-dropdownbutton.md)-, [**Group**](windowsribbon-element-group.md)-, [**dropdowngallery**](windowsribbon-element-dropdowngallery.md)-, [**MenuGroup**](windowsribbon-element-menugroup.md)-, [**quickaccesstoolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)-, [**SplitButton**](windowsribbon-element-splitbutton.md)-oder [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Element einmal oder mehrmals vorkommen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für **das Element "** -Element" veranschaulicht.

Dieser Code Abschnitt zeigt eine **ToggleButton** -Element Deklaration innerhalb des [**quickaccesstoolbar. ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) -Elements.


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a>Elementinformationen



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Ja       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Umschalten des Schaltflächen-Steuer Elements](windowsribbon-controls-togglebutton.md)
</dt> </dl>

 

 





