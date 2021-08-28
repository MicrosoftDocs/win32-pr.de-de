---
title: Spinner-Element
description: Stellt ein Spinner-Steuerelement dar.
ms.assetid: 6a174ec9-0fde-4171-a363-0e330ac31a8b
keywords:
- Spinner-Element Windows Menüband
topic_type:
- apiref
api_name:
- Spinner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3ea9c7ff4710837b859003b617c92ed288e261
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631658"
---
# <a name="spinner-element"></a>Spinner-Element

Stellt ein [Spinner-Steuerelement](windowsribbon-controls-spinner.md) dar.

## <a name="usage"></a>Verwendung

``` syntax
<Spinner
  CommandName = "xs:positiveInteger or xs:string"/>
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
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger oder xs:string<br/></td>
<td>Nein<br/></td>
<td>Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999( einschließlich) oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich. <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Gruppe**](windowsribbon-element-group.md)<br/>                           |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann ein oder mehrere Male für jedes [**ControlGroup-**](windowsribbon-element-controlgroup.md) oder [**Group-Element**](windowsribbon-element-group.md) auftreten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für den [Spinner](windowsribbon-controls-spinner.md)veranschaulicht.

Dieser Codeabschnitt zeigt die **Spinner** Command-Deklarationen mit einem [**Group-Element,**](windowsribbon-element-group.md) das als übergeordneter Container für das **Spinner-Element** fungiert.


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



Dieser Codeabschnitt zeigt die Spinner-Steuerelementdeklarationen. 


```XML
<Group CommandName="GroupSpinner1">
  <Spinner CommandName="Spinner_Size" />
</Group>
```



## <a name="element-information"></a>Elementinformationen

- **Unterstütztes Mindestsystem:** Windows 7 
- **Kann leer sein:** Ja



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Drehungssteuerelement](windowsribbon-controls-spinner.md)
</dt> </dl>

 

 





