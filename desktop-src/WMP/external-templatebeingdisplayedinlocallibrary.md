---
title: External.templateBeingDisplayedInLocalLibrary
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | External.templateBeingDisplayedInLocalLibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- External.templateBeingDisplayedInLocalLibrary Windows Media Player
topic_type:
- apiref
api_name:
- External.templateBeingDisplayedInLocalLibrary
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8292e2527fe14ec00a2bf7169b4e2ea2ca4c8229672625712ed3ad3a10e421e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648270"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a>External.templateBeingDisplayedInLocalLibrary

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **templateBeingDisplayedInLocalLibrary-Eigenschaft** gibt an, ob der von der aktuellen Ermittlungsseite dargestellte Feed im Strukturansichtssteuerelement der lokalen Bibliothek angezeigt wird.

## <a name="syntax"></a>Syntax

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist ein **schreibgeschützter boolescher** Wert. **TRUE** gibt an, dass der Feed im Strukturansichtssteuerelement der lokalen Bibliothek angezeigt wird.

## <a name="remarks"></a>Hinweise

Eine Ermittlungsseite, die einen Feed für eine dynamische Wiedergabeliste darstellt, kann eine Schaltfläche anzeigen, mit der der Benutzer den Feed in seiner lokalen Bibliothek "speichern" kann. Das Speichern des Feeds bedeutet in diesem Kontext, dass einige Metadaten auf dem Computer des Benutzers gespeichert werden und der Feed unter dem Knoten **Wiedergabelisten** im Strukturansichtssteuerelement der lokalen Bibliothek aufgeführt wird. Das Skript auf der Ermittlungsseite kann die **TemplateBeingDisplayedInLocalLibrary-Eigenschaft** überprüfen, um zu ermitteln, ob der Benutzer den Feed bereits in der lokalen Bibliothek gespeichert hat. Wenn der Benutzer den Feed bereits gespeichert hat, sollte auf der Ermittlungsseite nicht die Schaltfläche "Speichern" angezeigt werden.

Eine Ermittlungsseite, die einen Funkfeed darstellt, sollte die **TemplateBeingDisplayedInLocalLibrary-Eigenschaft** aus dem gleichen Grund überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlineshops vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





