---
title: String.ID-Eigenschaft
description: Stellt die eindeutige ID einer Zeichen folgen Ressource dar.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- String.ID-Eigenschaften Fenster (Menü)
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3ab87327ed4f11a901fb8a201e72137ab62c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105621"
---
# <a name="stringid-property"></a>String.ID-Eigenschaft

Stellt die eindeutige ID einer Zeichen folgen Ressource dar.

## <a name="usage"></a>Verbrauch

``` syntax
<String.Id/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                   |
|-----------------------------------------------------------|
| [**Schnür**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jedes [**Zeichen**](windowsribbon-element-string.md) folgen Element auftreten.

Der Wert für **String.ID** muss eindeutig sein.

Die ID ist einer Zeichen folgen Definition in der Menüband-Header Datei zugeordnet, z `#define strSave 59999` . b..

Dieses Element enthält einen Wert aus der Vereinigung der Typen " *xs: positiveInteger* " und " *xs: String*". Der Wert wird auf einen ganzzahligen Wert zwischen 2 und 59999, einschließlich, oder 0x2 und 0xea5f in Hexadezimal (einschließlich) beschränkt.

Die maximale Länge beträgt 10 Zeichen mit optionalen führenden Nullen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) -Element mit einer **String.ID** -Deklaration veranschaulicht.


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

 





