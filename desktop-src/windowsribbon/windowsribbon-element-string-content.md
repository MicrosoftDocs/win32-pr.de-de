---
title: String.Content-Eigenschaft
description: Stellt den Inhalt einer Zeichenfolgenressource dar.
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- String.Content-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526062956c6ab7498caac8712ba932d6e7ac1f2dd6307359183d2529e35fc8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439505"
---
# <a name="stringcontent-property"></a>String.Content-Eigenschaft

Stellt den Inhalt einer Zeichenfolgenressource dar.

## <a name="usage"></a>Verbrauch

``` syntax
<String.Content/>
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

Dieses Element enthält einen Wert vom Typ *xs:string*. Der Wert ist auf eine Zeichenfolge beschränkt, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.

Die maximale Länge ist ungebunden.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das Markup für ein [**Command.LabelTitle-Element**](windowsribbon-element-command-labeltitle.md) mit einer **String.Content-Deklaration** veranschaulicht.


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



 

 





