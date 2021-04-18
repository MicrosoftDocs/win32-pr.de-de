---
title: Albumittelalbumartist-Attribut
description: Das albuminalbumartist-Attribut ist ein eindeutiger Bezeichner für das Album.
ms.assetid: beaa8d01-1722-4545-8705-6b3d130113b1
keywords:
- Albuminalbumartist-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- AlbumIDAlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1925f40a50b15efcd339ad949d5d54ddb915cbe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371695"
---
# <a name="albumidalbumartist-attribute"></a>Albumittelalbumartist-Attribut

Das **albuminalbumartist** -Attribut ist ein eindeutiger Bezeichner für das Album.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nur in der-Bibliothek gespeichert.

Der eindeutige Bezeichner ist eine Kombination aus dem Albumtitel und dem Namen des Album-Künstlers. In diesem Attribut kommt der Name des Album-Künstlers zunächst vor. Wenn Sie die [mediacollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) -Methode verwenden, um ein **StringCollection** -Objekt mithilfe dieses Attributs zu erhalten, werden die Werte nach dem Namen des Album-Künstlers sortiert.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AlbumId-Attribut**](albumid-attribute.md)
</dt> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





