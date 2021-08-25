---
title: Command.Id-Eigenschaft
description: Stellt eine eindeutige ID für einen Befehl dar.
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- Command.Id-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c542cbf4103c6063a177990d454a45e5f937745720c7c0a7bc5c60c4c1047e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931614"
---
# <a name="commandid-property"></a>Command.Id-Eigenschaft

Stellt eine eindeutige ID für einen Befehl dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Command.Id/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                     |
|-------------------------------------------------------------|
| [**Befehl**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.

Die ID ist einer Befehlsdefinition in der Menübandheaderdatei zugeordnet, z. `#define cmdSave 25003 /* Save */` B. .

Dieses Element enthält einen Wert aus der Vereinigung der Typen *xs:positiveInteger* und *xs:string,* die auf einen ganzzahligen Wert zwischen 2 und 59999 beschränkt sind, einschließlich oder 0x2 und 0xea5f in Hexadezimal, einschließlich.

Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command-Element**](windowsribbon-element-command.md) mit einer **Command.Id-Deklaration** veranschaulicht.


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



 

 





