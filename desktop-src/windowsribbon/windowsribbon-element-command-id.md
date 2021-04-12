---
title: Command.ID-Eigenschaft
description: Stellt eine eindeutige ID für einen Befehl dar.
ms.assetid: 937ca9d6-6910-4133-9cfa-d7e3f895f876
keywords:
- Command.ID-Eigenschaften Fenster (Menü)
topic_type:
- apiref
api_name:
- Command.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13e259e5fd74e3037afde3d4c001000b5a17a9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478639"
---
# <a name="commandid-property"></a>Command.ID-Eigenschaft

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
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jeden [**Befehl**](windowsribbon-element-command.md)auftreten.

Die ID ist einer Befehls Definition in der Menüband-Header Datei zugeordnet, z `#define cmdSave 25003 /* Save */` . b..

Dieses Element enthält einen Wert aus der Vereinigung der Typen *xs: positiveInteger* und *xs: String* , die auf einen ganzzahligen Wert zwischen 2 und 59999 (einschließlich) oder 0x2 und 0xea5f in Hexadezimal (einschließlich) beschränkt sind.

Die maximale Länge beträgt 10 Zeichen, einschließlich optionaler führender Nullen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command**](windowsribbon-element-command.md) -Element mit einer **Command.ID** -Deklaration veranschaulicht.


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



 

 





