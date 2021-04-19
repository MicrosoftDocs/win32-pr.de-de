---
title: Userrating-Attribut
description: Das userrating-Attribut ist die vom Benutzer in der Bibliothek angegebene Bewertung.
ms.assetid: 33df5316-1506-4ecb-b729-c2d66b878825
keywords:
- Userrating-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- UserRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a25dd7b4e55195deaecf5228b9ad5bad9195c2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355865"
---
# <a name="userrating-attribute"></a>Userrating-Attribut

Das **userrating** -Attribut ist die vom Benutzer in der Bibliothek angegebene Bewertung.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Andere Elemente](other-item-attributes.md)
-   [Foto Elemente](photo-item-attributes.md)
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
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher (das Foto Element wird nur in Windows Media Player 10 oder höher unterstützt)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





