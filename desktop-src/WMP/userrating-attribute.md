---
title: UserRating-Attribut
description: Das UserRating-Attribut ist die Bewertung, die vom Benutzer in der Bibliothek angegeben wird.
ms.assetid: 33df5316-1506-4ecb-b729-c2d66b878825
keywords:
- UserRating-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- UserRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41725119f97e0609931a3c9b7789e86d16a20507523e76a3f5642a0955998d6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001650"
---
# <a name="userrating-attribute"></a>UserRating-Attribut

Das **UserRating-Attribut** ist die Bewertung, die vom Benutzer in der Bibliothek angegeben wird.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Andere Elemente](other-item-attributes.md)
-   [Fotoelemente](photo-item-attributes.md)
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
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher (Das Fotoelement wird nur in Windows Media Player 10 oder höher unterstützt)<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> </dl>

 

 





