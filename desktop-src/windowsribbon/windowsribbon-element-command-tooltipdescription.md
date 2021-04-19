---
title: Command. tooltipdescription (Eigenschaft)
description: Stellt eine QuickInfo-Beschreibung dar.
ms.assetid: 2d3ea497-2d96-4420-8fcf-39ac2c472bf1
keywords:
- Command. tooltipdescription-Eigenschaft, Windows-Menüband
topic_type:
- apiref
api_name:
- Command.TooltipDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 288578e74420912b7454be5037c4b2651918ac6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345920"
---
# <a name="commandtooltipdescription-property"></a>Command. tooltipdescription (Eigenschaft)

Stellt eine QuickInfo-Beschreibung dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Command.TooltipDescription>
  child elements
</Command.TooltipDescription>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                   | BESCHREIBUNG                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**Schnür**](windowsribbon-element-string.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                     |
|-------------------------------------------------------------|
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.

**Command. tooltipdescription** kann einen Wert vom Typ *xs: String* enthalten, der auf eine beliebige Sequenz von Zeichen beschränkt ist, einschließlich Leerzeichen und Zeilenumbruch Zeichen.

> [!Note]  
> Verwenden Sie den XML-Zeichen Verweis Universal Character Set (UCS) `&#xA;` , um einen Zeilenumbruch anzugeben.

 

Die maximale Länge ist unbegrenzt.

Wenn für **Command. tooltipdescription** kein Wert angegeben wird, ist das untergeordnete [**Zeichen**](windowsribbon-element-string.md) folgen Element erforderlich.

> [!Note]  
> Wenn **Command. tooltipdescription** sowohl einen Wert als auch ein untergeordnetes [**Zeichen**](windowsribbon-element-string.md) folgen Element enthält, hat die **Zeichenfolge** Vorrang.

 

" **Command. tooltipdescription** " unterstützt nur die linke Ausrichtung.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command**](windowsribbon-element-command.md) -Element mit der **Command. tooltipdescription** -Deklaration veranschaulicht.


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[UI- \_ pkey- \_ tooltipdescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 





