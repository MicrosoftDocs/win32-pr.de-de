---
title: Command.Name-Eigenschaft
description: Stellt den Namen eines Befehls dar.
ms.assetid: 36fb0b93-143f-4706-8c32-e6c818cce16f
keywords:
- Command.Name-Eigenschaften Fenster (Menü)
topic_type:
- apiref
api_name:
- Command.Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d93b830e29ca271052a4693b00ba64eee94309f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040902"
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
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.

Auf **Command.Name** wird im Markup verwiesen, um einen Befehl mit einem-Steuerelement über das *CommandName* -Attribut des-Steuer Elements zu verknüpfen.

Dieses Element enthält einen Wert vom Typ *xs: String*.

Der Wert ist auf eine Zeichenfolge beschränkt, die aus einem Buchstaben oder Unterstrich besteht, gefolgt von einer beliebigen Folge von Buchstaben, Ziffern und unterstrichen.

Die maximale Länge beträgt 100 Zeichen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command**](windowsribbon-element-command.md) -Element mit einer **Command.Name** -Deklaration veranschaulicht.


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



 

 





