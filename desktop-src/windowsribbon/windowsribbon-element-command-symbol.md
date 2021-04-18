---
title: Command. Symbol-Eigenschaft
description: Stellt den Namen eines Befehls dar, auf den extern verwiesen werden kann.
ms.assetid: affa5f3f-f641-4bec-9165-6102509cf355
keywords:
- Command. Symbol-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Command.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b88dccb71a90feca7348ca9731ca5966b012c9c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341020"
---
# <a name="commandsymbol-property"></a>Command. Symbol-Eigenschaft

Stellt den Namen eines [**Befehls**](windowsribbon-element-command.md) dar, auf den extern verwiesen werden kann.

## <a name="usage"></a>Verbrauch

``` syntax
<Command.Symbol/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                     |
|-------------------------------------------------------------|
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.

Das Symbol ist einer Befehls Definition in der Menüband-Header Datei zugeordnet, z `#define cmdSave 25003 /* Save */` . b..

Dieses Element enthält einen Wert vom Typ *xs: String*.

Der Wert ist auf eine Zeichenfolge beschränkt, die aus einem Buchstaben oder Unterstrich besteht, gefolgt von einer beliebigen Folge von Buchstaben, Ziffern und unterstrichen.

Die maximale Länge beträgt 100 Zeichen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command**](windowsribbon-element-command.md) -Element mit der **Command. Symbol** -Deklaration veranschaulicht.


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



 

 





