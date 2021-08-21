---
title: String.Symbol-Eigenschaft
description: Stellt den Namen einer Zeichenfolgenressource dar.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- String.Symbol-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe6c071461fcdeb5f2bbbdbb15fce0f3f6e6031edddf4bd18e034416ba8c49e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706861"
---
# <a name="stringsymbol-property"></a>String.Symbol-Eigenschaft

Stellt den Namen einer Zeichenfolgenressource dar.

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
| [**String**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jedes [**String-Element**](windowsribbon-element-string.md) auftreten.

Das Symbol ist einer Zeichenfolgendefinition in der Menübandheaderdatei zugeordnet, z. `#define strSave 59999` B. .

Dieses Element enthält einen Wert vom Typ *xs:string*. Der Wert ist auf eine Zeichenfolge beschränkt, die aus einem Buchstaben oder Unterstrich besteht, gefolgt von einer beliebigen Sequenz von Buchstaben, Ziffern oder Unterstrichen.

Die maximale Länge beträgt 100 Zeichen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command.LabelTitle-Element**](windowsribbon-element-command-labeltitle.md) mit einer **String.Symbol-Deklaration** veranschaulicht.


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



 

 





