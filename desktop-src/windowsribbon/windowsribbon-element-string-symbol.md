---
title: String. Symbol-Eigenschaft
description: Stellt den Namen einer Zeichen folgen Ressource dar.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- String. Symbol-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7bf7d30ddd8677b1c5ff0a5e55d4b9c119795ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858694"
---
# <a name="stringsymbol-property"></a>String. Symbol-Eigenschaft

Stellt den Namen einer Zeichen folgen Ressource dar.

## <a name="usage"></a>Verbrauch

``` syntax
<String.Symbol/>
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

Das Symbol ist einer Zeichen folgen Definition in der Menüband-Header Datei zugeordnet, z `#define strSave 59999` . b..

Dieses Element enthält einen Wert vom Typ *xs: String*. Der Wert wird auf eine Zeichenfolge beschränkt, die aus einem Buchstaben oder Unterstrich, gefolgt von einer beliebigen Folge von Buchstaben, Ziffern oder unterstrichen, besteht.

Die maximale Länge beträgt 100 Zeichen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) -Element mit einer **String. Symbol** -Deklaration veranschaulicht.


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



 

 





