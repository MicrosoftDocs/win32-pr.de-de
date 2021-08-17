---
title: UserEffectiveRating-Attribut
description: Das UserEffectiveRating-Attribut ist die Bewertung, die von Windows Media Player basierend darauf berechnet wird, wie oft das Element wiedergegeben wurde.
ms.assetid: 6a420e20-f61d-4e15-84f8-a738caabd1d7
keywords:
- UserEffectiveRating-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- UserEffectiveRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e3244d793288fe1535c7e7cb4d44c05a3b71404531cf2ae344eb77528dd4a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134443"
---
# <a name="usereffectiverating-attribute"></a>UserEffectiveRating-Attribut

Das **UserEffectiveRating-Attribut** ist die Bewertung, die von Windows Media Player basierend darauf berechnet wird, wie oft das Element wiedergegeben wurde.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Andere Elemente](other-item-attributes.md)
-   [Wiedergabelisten](playlist-attributes-ref.md)
-   [Videoelemente](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Benutzerbewertungen werden durch ganzzahlige Werte dargestellt, wie in der folgenden Tabelle beschrieben. Verwenden Sie beim Angeben eines Werts einen der Werte aus der Spalte Schreibwert. Beim Abrufen von Werten können Sie die Bereiche in der Spalte Lesewerte verwenden, um die Anzahl der Sterne zu bestimmen.



| Rating  | Schreiben eines Werts | Lesen von Werten |
|---------|---------------|----------------|
| Unrated | 0             | 0              |
| 1 Stern  | 1             | 1 bis 12        |
| 2 Sterne | 25            | 13 bis 37       |
| 3 Sterne | 50            | 38 bis 62       |
| 4 Sterne | 75            | 63 bis 86       |
| 5 Sterne | 99            | 87 bis 99       |



 

Dieses Attribut wird nur in der Bibliothek gespeichert.

Verwenden Sie die [Media.isReadOnlyItem-Methode,](media-isreadonlyitem.md) um zu bestimmen, ob Sie den Wert dieses Attributs ändern können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> </dl>

 

 





