---
title: ButtonTip-Element
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | ButtonTip-Element
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- ButtonTip-Element Windows Media Player
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7fb4a162a8e77fea7548265825af6c6cbda75dbafadf05fe32cb664c4d563f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764300"
---
# <a name="buttontip-element"></a>ButtonTip-Element

> [!Note]  
> In diesem Abschnitt werden funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **ButtonTip-Element** gibt die Textzeichenfolge an, die angezeigt wird, wenn der Benutzer auf eine Aufgabenbereichsschaltfläche zeigt.

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Element                                              |
|-----------------|------------------------------------------------------|
| Übergeordnete Elemente | **ServiceTask1,** **ServiceTask2,** **ServiceTask3** |
| Untergeordnete Elemente  | Keine                                                 |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element ist für jede Instanz von **ServiceTask1,** **ServiceTask2** oder **ServiceTask3** optional. Wenn dieses Element nicht angegeben wird, verwendet Windows Media Player den Schaltflächentext als Standardwert.

> [!Note]  
> Windows Media Player 10 verfügt über drei Aufgabenbereiche, in denen ein Onlineshop seine Webseiten anzeigen kann. Der Onlineshop kann einen, zwei oder alle drei Aufgabenbereiche verwenden. Windows Media Player 11 verfügt nur über einen Aufgabenbereich, den der Benutzer anzeigen kann, indem er auf die Registerkarte **Onlineshops** klickt. Windows Media Player 11 ignoriert die Elemente **ServiceTask2** und **ServiceTask3.**

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für ein Online-Store vom Typ 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





