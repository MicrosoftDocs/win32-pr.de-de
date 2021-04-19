---
title: Buttontip-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Buttontip-Element
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- Buttontip-Element Fenster Media Player
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ab94794232ade6f924b87fd3f4d73d4452d544
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353823"
---
# <a name="buttontip-element"></a>Buttontip-Element

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **buttontip** -Element gibt die Text Zeichenfolge an, die angezeigt wird, wenn der Benutzer auf eine Schaltfläche des Aufgabenbereichs zeigt.

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Element                                              |
|-----------------|------------------------------------------------------|
| Übergeordnete Elemente | **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |
| Untergeordnete Elemente  | Keine                                                 |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element ist für jede Instanz von **ServiceTask1**, **ServiceTask2** oder **ServiceTask3** optional. Wenn dieses Element nicht angegeben wird, verwendet Windows Media Player den Schaltflächen Text als Standardwert.

> [!Note]  
> Windows Media Player 10 umfasst drei Aufgabenbereiche, in denen ein Online Shop seine Webseiten anzeigen kann. Der Online Shop kann einen, zwei oder alle drei Aufgabenbereiche verwenden. Windows Media Player 11 verfügt nur über einen Aufgabenbereich, den der Benutzer durch Klicken auf die Registerkarte " **Online Stores** " anzeigen kann. die **ServiceTask2** -und **ServiceTask3** -Elemente werden von Windows Media Player 11 ignoriert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





