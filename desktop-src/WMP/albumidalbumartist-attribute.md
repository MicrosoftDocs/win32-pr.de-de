---
title: AlbumIDWertartist-Attribut
description: Das AlbumIDKatartist-Attribut ist ein eindeutiger Bezeichner für das Album.
ms.assetid: beaa8d01-1722-4545-8705-6b3d130113b1
keywords:
- AlbumIDWertartist-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- AlbumIDAlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4905f0448c7e08abe308a57b1ad08020d47563847db1aa32744c0de3279cdcdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055388"
---
# <a name="albumidalbumartist-attribute"></a>AlbumIDWertartist-Attribut

Das **AlbumIDKatartist-Attribut** ist ein eindeutiger Bezeichner für das Album.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird nur in der Bibliothek gespeichert.

Der eindeutige Bezeichner ist eine Kombination aus dem Titel des Albums und dem Namen des Album-Interpreten. In diesem Attribut steht der Name des Album-Interpreten an erster Stelle. Wenn Sie die [MediaCollection.getAttributeStringCollection-Methode](mediacollection-getattributestringcollection.md) verwenden, um ein **StringCollection-Objekt** mit diesem Attribut zu erhalten, werden die Werte nach dem Namen des Album-Interpreten sortiert.

Um zu bestimmen, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media.isReadOnlyItem-Methode.](media-isreadonlyitem.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AlbumID-Attribut**](albumid-attribute.md)
</dt> <dt>

[**Attributreferenz**](attribute-reference.md)
</dt> </dl>

 

 





