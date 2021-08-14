---
title: LibraryID-Attribut
description: Das LibraryID-Attribut ist der Bezeichner der Bibliothek, zu der das Element gehört.
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- Windows Media Player des LibraryID-Attributs
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a011db4e18509761c232bcf5439e33445128ef77c50945f84662a7b7956f607f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468220"
---
# <a name="libraryid-attribute"></a>LibraryID-Attribut

Das **LibraryID-Attribut** ist der Bezeichner der Bibliothek, zu der das Element gehört.

## <a name="applies-to"></a>Gilt für

-   [**Audioelemente**](audio-item-attributes.md)
-   [**Fotoelemente**](photo-item-attributes.md)
-   [**Wiedergabelistenelemente**](playlist-attributes-ref.md)
-   [**Videoelemente**](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Ein Medienelement kann zur lokalen Bibliothek des aktuellen Benutzers gehören oder zu einer Bibliothek gehören, die von einem anderen Benutzer im Heimnetzwerk oder im Internet zur Verfügung gestellt wurde.

Der Wert dieses Attributs entspricht dem Wert, der von der [**IWMPLibrary2::getItemInfo-Methode**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) zurückgegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> </dl>

 

 





