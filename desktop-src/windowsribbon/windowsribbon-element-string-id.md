---
title: String.Id-Eigenschaft
description: Stellt die eindeutige ID einer Zeichenfolgenressource dar.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- String.Id-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f9c1af4ba32982ce52ba470f6b3d1996abe11c81bdd520a4e50203adb56093
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441650"
---
# <a name="stringid-property"></a>String.Id-Eigenschaft

Stellt die eindeutige ID einer Zeichenfolgenressource dar.

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
| [**Schnur**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jedes [**String-Element**](windowsribbon-element-string.md) auftreten.

Der Wert für **String.Id** muss eindeutig sein.

Die ID ist einer Zeichenfolgendefinition in der Menübandheaderdatei zugeordnet, z. `#define strSave 59999` B. .

Dieses Element enthält einen Wert aus der Vereinigung der Typen *xs:positiveInteger* und *xs:string*. Der Wert ist auf einen ganzzahligen Wert zwischen 2 und 59999 beschränkt, einschließlich oder 0x2 und 0xea5f hexadezimal, einschließlich.

Die maximale Länge beträgt 10 Zeichen mit optionalen führenden Nullen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command.LabelTitle-Element**](windowsribbon-element-command-labeltitle.md) mit einer **String.Id-Deklaration** veranschaulicht.


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
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



 

 





