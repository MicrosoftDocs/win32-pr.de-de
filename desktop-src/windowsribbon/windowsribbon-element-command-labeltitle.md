---
title: Command.LabelTitle-Eigenschaft
description: Stellt einen Bezeichnungstitel dar.
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- Command.LabelTitle-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44995d3f17b165c38f9fe7490a33e5d140c8d2b375d5d6b625bb00e3228b21e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810790"
---
# <a name="commandlabeltitle-property"></a>Command.LabelTitle-Eigenschaft

Stellt einen Bezeichnungstitel dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Command.LabelTitle>
  child elements
</Command.LabelTitle>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                   | Beschreibung                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**String**](windowsribbon-element-string.md)<br/> | Kann nur einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                     |
|-------------------------------------------------------------|
| [**Befehl**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann für jeden Befehl mindestens einmal [**auftreten.**](windowsribbon-element-command.md)

**Command.LabelTitle kann** einen Wert vom Typ *xs:string* enthalten, der auf eine beliebige Folge von Zeichen beschränkt ist, einschließlich Leerzeichen und Zeilenumbruchzeichen.

> [!Note]  
> Verwenden Sie den UCS-XML-Zeichenverweis (Universal Character Set), `&#xA;` um einen Zeilenumbruch anzugeben.

 

Die maximale Länge ist ungebunden.

Wenn kein Wert für **Command.LabelTitle angegeben wird,** ist das [**untergeordnete String-Element**](windowsribbon-element-string.md) erforderlich.

> [!Note]  
> Wenn **Command.LabelTitle** sowohl einen Wert als auch ein untergeordnetes [**String-Element**](windowsribbon-element-string.md) enthält, hat **String** Vorrang.

 

**Command.LabelTitle unterstützt** nur die linke Ausrichtung.

Wenn ein Befehl über ein Menüelement verfügbar gemacht wird und der Wert von **Command.LabelTitle** oder [ \_ UI PKEY \_ Label](windowsribbon-reference-properties-uipkey-label.md) einen Buchstaben enthält, dem ein ampersand vorangestellt ist, wie im folgenden Beispiel gezeigt, wird dieser Buchstabe sowohl als Tastenkombination als auch als Tastenkombination für diesen Befehl vom Menübandframework behandelt.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Um ein ampersand-Zeichen in einer Bezeichnung anzuzeigen, versehen Sie die Sonderzeichenbezeichnung mit einem doppelten Ampersand ( ), wie `&&` im folgenden Beispiel gezeigt.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command-Element**](windowsribbon-element-command.md) mit einer **Command.LabelTitle-Deklaration** veranschaulicht.


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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[\_PKEY-Bezeichnung der \_ Benutzeroberfläche](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





