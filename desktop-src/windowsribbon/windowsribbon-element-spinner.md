---
title: Spinner-Element
description: Stellt ein Spinner-Steuerelement dar.
ms.assetid: 6a174ec9-0fde-4171-a363-0e330ac31a8b
keywords:
- Fensterleiste des Spinner-Elements
topic_type:
- apiref
api_name:
- Spinner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b1f9727dc7fbad8be24c15f0b1f551b021294dd
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104038493"
---
# <a name="spinner-element"></a>Spinner-Element

Stellt ein [Spinner](windowsribbon-controls-spinner.md) -Steuerelement dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Spinner
  CommandName = "xs:positiveInteger or xs:string"/>
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
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                           |
|-----------------------------------------------------------------------------------|
| [**Controlgroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**Dropdown Gallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Gruppe**](windowsribbon-element-group.md)<br/>                           |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**Splitbuttongallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann für jedes [**controlgroup**](windowsribbon-element-controlgroup.md) -oder [**Group**](windowsribbon-element-group.md) -Element einmal oder mehrmals vorkommen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für den [Spinner](windowsribbon-controls-spinner.md)veranschaulicht.

Dieser Code Abschnitt zeigt die **Spinner** -Befehls Deklarationen mit einem [**Group**](windowsribbon-element-group.md) -Element, das als übergeordneter Container für das **Spinner** -Element fungiert.


```XML
<Command Name="GroupSpinner1" Symbol="IDR_CMD_GROUPSPINNER1" Id="30010">
  <Command.LabelTitle>
    <String Id="210">Resize</String>
  </Command.LabelTitle>
</Command>
<Command Name="Spinner_Size" Symbol="IDR_CMD_SPINNER_RESIZE" Id="30015">
  <Command.LabelTitle>
    <String Id="215">Resize by:</String>
  </Command.LabelTitle>
</Command>
```



Dieser Code Abschnitt zeigt die **Spinner** -Steuerelement Deklarationen.


```XML
<Group CommandName="GroupSpinner1">
  <Spinner CommandName="Spinner_Size" />
</Group>
```



## <a name="element-information"></a>Elementinformationen



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Ja       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Spinner-Steuerelement](windowsribbon-controls-spinner.md)
</dt> </dl>

 

 





