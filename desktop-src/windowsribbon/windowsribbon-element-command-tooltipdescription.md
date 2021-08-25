---
title: Command.TooltipDescription (Eigenschaft)
description: Stellt eine QuickInfo-Beschreibung dar.
ms.assetid: 2d3ea497-2d96-4420-8fcf-39ac2c472bf1
keywords:
- Command.TooltipDescription-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- Command.TooltipDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5dd356ae3bcfa5949e8469240330a3a09a11f01b5a919ed02f4eb55683fbc15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933210"
---
# <a name="commandtooltipdescription-property"></a>Command.TooltipDescription (Eigenschaft)

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
| [**String**](windowsribbon-element-string.md)<br/> | Kann nur einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                     |
|-------------------------------------------------------------|
| [**Befehl**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann für jeden Befehl mindestens einmal [**auftreten.**](windowsribbon-element-command.md)

**Command.TooltipDescription** kann einen Wert vom Typ *xs:string* enthalten, der auf eine beliebige Sequenz von Zeichen beschränkt ist, einschließlich Leerzeichen und Zeilenumbruchzeichen.

> [!Note]  
> Verwenden Sie den UCS-XML-Zeichenverweis (Universal Character Set), `&#xA;` um einen Zeilenumbruch anzugeben.

 

Die maximale Länge ist ungebunden.

Wenn kein Wert für **Command.TooltipDescription** angegeben wird, ist das untergeordnete [**String-Element**](windowsribbon-element-string.md) erforderlich.

> [!Note]  
> Wenn **Command.TooltipDescription** sowohl einen Wert als auch ein untergeordnetes [**String-Element**](windowsribbon-element-string.md) enthält, hat **String** Vorrang.

 

**Command.TooltipDescription unterstützt** nur die linke Ausrichtung.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command-Element**](windowsribbon-element-command.md) mit einer **Command.TooltipDescription-Deklaration** veranschaulicht.


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
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 





