---
title: Userservicerating-Attribut
description: Das userservicerating-Attribut ist für die zukünftige Verwendung reserviert.
ms.assetid: e6113474-725d-4eb1-9c05-cff7749f2010
keywords:
- Userservicerating-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- UserServiceRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690a090aaa9d07ee850caee004242272368129f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367418"
---
# <a name="userservicerating-attribute"></a>Userservicerating-Attribut

Das **userservicerating** -Attribut ist für die zukünftige Verwendung reserviert.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Wiedergabelisten](playlist-attributes-ref.md)
-   [Video Elemente](video-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Benutzerbewertungen werden durch ganzzahlige Werte dargestellt, wie in der folgenden Tabelle beschrieben. Wenn Sie einen Wert angeben, verwenden Sie einen der Werte aus der Spalte zum Schreiben von Werten. Beim Abrufen von Werten können Sie die Bereiche in der Spalte Lesewerte verwenden, um die Anzahl der Sterne zu bestimmen.



| Rating  | Wert wird geschrieben | Lesen von Werten |
|---------|---------------|----------------|
| Unbewertete | 0             | 0              |
| 1 Stern  | 1             | 1 bis 12        |
| 2 Sterne | 25            | 13 bis 37       |
| 3 Sterne | 50            | 38 bis 62       |
| 4 Sterne | 75            | 63 bis 86       |
| 5 Sterne | 99            | 87 bis 99       |



 

Dieses Attribut ist nur in der-Bibliothek gespeichert.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





