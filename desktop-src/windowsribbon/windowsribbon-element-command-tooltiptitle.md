---
title: Command.TooltipTitle-Eigenschaft
description: Stellt einen QuickInfo-Titel dar.
ms.assetid: b06a7a6a-fbdd-464b-b804-e62912d6e176
keywords:
- Command.TooltipTitle-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- Command.TooltipTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f9050c97980b0ffa2c2c4828a8ac1d85dfbd1a40ed8330d144db2c0d3802524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710550"
---
# <a name="commandtooltiptitle-property"></a>Command.TooltipTitle-Eigenschaft

Stellt einen QuickInfo-Titel dar.

## <a name="usage"></a>Verwendung

``` syntax
<Command.TooltipTitle>
  child elements
</Command.TooltipTitle>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                   | Beschreibung                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**String**](windowsribbon-element-string.md)<br/> | Kann höchstens einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                     |
|-------------------------------------------------------------|
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.

**Command.TooltipTitle** kann einen Wert vom Typ *xs:string* enthalten, der auf eine beliebige Zeichensequenz beschränkt ist, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.

> [!Note]  
> Verwenden Sie den UCS-XML-Zeichenverweis (Universal Character Set), `&#xA;` um einen Zeilenbreak anzugeben.

 

Die maximale Länge ist ungebunden.

Wenn für **Command.TooltipTitle** kein Wert angegeben wird, ist das untergeordnete [**String-Element**](windowsribbon-element-string.md) erforderlich.

> [!Note]  
> Wenn **Command.TooltipTitle** sowohl einen Wert als auch ein untergeordnetes [**String-Element**](windowsribbon-element-string.md) enthält, hat **String** Vorrang.

 

**Command.TooltipTitle** unterstützt nur die linke Ausrichtung.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command-Element**](windowsribbon-element-command.md) mit einer **Command.TooltipTitle-Deklaration** veranschaulicht.


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
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 





