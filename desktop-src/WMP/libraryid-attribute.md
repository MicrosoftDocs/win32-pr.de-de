---
title: LIBRARYID-Attribut
description: Das LIBRARYID-Attribut ist der Bezeichner der Bibliothek, zu der das Element gehört.
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- LIBRARYID-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ae9e5ad097bc188b8de1e76a09448c57aa9b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368418"
---
# <a name="libraryid-attribute"></a>LIBRARYID-Attribut

Das **LIBRARYID** -Attribut ist der Bezeichner der Bibliothek, zu der das Element gehört.

## <a name="applies-to"></a>Gilt für

-   [**Audioelemente**](audio-item-attributes.md)
-   [**Foto Elemente**](photo-item-attributes.md)
-   [**Wiedergabelisten Elemente**](playlist-attributes-ref.md)
-   [**Video Elemente**](video-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Ein Medien Element kann der lokalen Bibliothek des aktuellen Benutzers angehören, oder es kann einer Bibliothek angehören, die von einem anderen Benutzer im Heimnetzwerk oder im Internet zur Verfügung gestellt wurde.

Der Wert dieses Attributs entspricht dem Wert, der von der [**IWMPLibrary2:: getiteminfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) -Methode zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





