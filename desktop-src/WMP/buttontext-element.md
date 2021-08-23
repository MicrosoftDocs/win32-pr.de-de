---
title: ButtonText-Element
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | ButtonText-Element
ms.assetid: 1afe1626-769a-40c8-883a-968ebd995a93
keywords:
- ButtonText-Element Windows Media Player
topic_type:
- apiref
api_name:
- ButtonText Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb67d1b6f43d59bc2f177394f1622d2ae4615d44050566cdbb7ec02670d4dcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118840298"
---
# <a name="buttontext-element"></a>ButtonText-Element

> [!Note]  
> In diesem Abschnitt werden funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **ButtonText-Element** gibt die Textzeichenfolge an, die Windows Media Player für eine Aufgabenbereichsschaltfläche angezeigt wird.

``` syntax
<ButtonText>
   text string
</ButtonText>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Element                                              |
|-----------------|------------------------------------------------------|
| Übergeordnete Elemente | **ServiceTask1,** **ServiceTask2,** **ServiceTask3** |
| Untergeordnete Elemente  | Keine                                                 |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element ist für jede Instanz von **ServiceTask1,** **ServiceTask2** oder **ServiceTask3** erforderlich.

> [!Note]  
> Windows Media Player 10 verfügt über drei Aufgabenbereiche, in denen ein Onlineshop seine Webseiten anzeigen kann. Der Onlineshop kann einen, zwei oder alle drei Aufgabenbereiche verwenden. Windows Media Player 11 verfügt nur über einen Aufgabenbereich, den der Benutzer anzeigen kann, indem er auf die Registerkarte **Onlineshops** klickt. Windows Media Player 11 ignoriert die Elemente **ServiceTask2** und **ServiceTask3.**

 

Windows Media Player können Schaltflächentext an den verfügbaren Platz anpassen. Der Player verwendet für diesen Text immer die Schriftart Tahoma bold mit 8 Punkten. Es stehen zwei Zeilen zum Anzeigen von Schaltflächentext zur Verfügung, aber der Player umschließt Text nicht automatisch von der ersten Zeile zur zweiten. Um einen Zeilenwechsel im Schaltflächentext anzugeben, fügen Sie die neue Zeilen-Escapesequenz \\ "n" in die Textzeichenfolge ein.

Die Textzeichenfolge wird auch im **GoTo-Menü** auf der Windows Media Player Benutzeroberfläche angezeigt.

Sie sollten Ihren Onlineshop mithilfe einer Vielzahl von Anzeigeeinstellungen testen, um sicherzustellen, dass Text wie erwartet angezeigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für ein Online-Store vom Typ 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





