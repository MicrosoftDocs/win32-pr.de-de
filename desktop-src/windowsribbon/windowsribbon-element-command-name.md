---
title: Command.Name-Eigenschaft
description: Stellt den Namen eines Befehls dar.
ms.assetid: 36fb0b93-143f-4706-8c32-e6c818cce16f
keywords:
- Command.Name-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- Command.Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48162c5edda2dd8787518ce7042a8ae8eeb349ff332488cd834d10b377d96a0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587750"
---
# <a name="commandname-property"></a>Command.Name-Eigenschaft

Stellt den Namen eines Befehls dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Command.Name/>
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

Kann für jeden Befehl mindestens einmal [**auftreten.**](windowsribbon-element-command.md)

**Command.Name** wird im Markup referenziert, um einen Befehl über das *CommandName-Attribut* des Steuerelements einem -Steuerelement zu zuordnen.

Dieses Element enthält einen Wert vom Typ *xs:string.*

Der Wert ist auf eine Zeichenfolge beschränkt, die aus einem Buchstaben oder Unterstrich gefolgt von einer beliebigen Sequenz von Buchstaben, Ziffern und Unterstrichen besteht.

Die maximale Länge beträgt 100 Zeichen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command-Element**](windowsribbon-element-command.md) mit einer Command.Name **veranschaulicht.**


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



 

 





