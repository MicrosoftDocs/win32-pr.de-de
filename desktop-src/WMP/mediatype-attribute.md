---
title: MediaType-Attribut
description: Das MediaType-Attribut ist der Inhaltstyp im Element.
ms.assetid: 0d8a6937-32d8-4a4a-87e5-0002f077fefe
keywords:
- MediaType-Attribut (Windows Media Player)
topic_type:
- apiref
api_name:
- MediaType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5779552f62007aa3dd3da0e2f4253fcf5499a6be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372341"
---
# <a name="mediatype-attribute"></a>MediaType-Attribut

Das **mediaType** -Attribut ist der Inhaltstyp im Element.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Andere Elemente](other-item-attributes.md)
-   [Foto Elemente](photo-item-attributes.md)
-   [Wiedergabelisten](playlist-attributes-ref.md)
-   [Options Felder](radio-item-attributes.md)
-   [Video Elemente](video-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nur in der-Bibliothek gespeichert.

Dieses Attribut weist einen der folgenden Werte auf: "Audiodatei", "Other", "Photo", "Wiedergabeliste", "Radio" oder "Video". Verwenden Sie dieses Attribut mit der *mediacollection*. **getbyattribute** -Methode zum Abrufen einer Wiedergabeliste, die alle Elemente eines bestimmten Typs enthält.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> <dt>

[**Mediacollection. getbyattribute**](mediacollection-getbyattribute.md)
</dt> </dl>

 

 





