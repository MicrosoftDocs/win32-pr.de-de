---
title: WM/MediaClassSecondaryID-Attribut
description: Das WM/MediaClassSecondaryID-Attribut ist eine GUID, die die sekundäre Medienklasse an gibt, die eine Unterklasse der primären Medienklasse ist.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- WM/MediaClassSecondaryID-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9582fc3db713b8db945ec17534f1dc9c951402eea88489285526d6a3cfbdf147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000990"
---
# <a name="wmmediaclasssecondaryid-attribute"></a>WM/MediaClassSecondaryID-Attribut

Das **WM/MediaClassSecondaryID-Attribut** ist eine GUID, die die sekundäre Medienklasse an gibt, die eine Unterklasse der primären Medienklasse ist.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Mediendateiattribute](commonly-used-windows-media-file-attributes.md)
-   [Andere Elemente](other-item-attributes.md)
-   [Fotoelemente](photo-item-attributes.md)
-   [Wiedergabelisten](playlist-attributes-ref.md)
-   [Optionselemente](radio-item-attributes.md)
-   [Videoelemente](video-item-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.

In der folgenden Tabelle sind die unterstützten GUIDs und ihre Beschreibungen aufgeführt.



| GUID                                 | Beschreibung                                    |
|--------------------------------------|------------------------------------------------|
| D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC | Das Medienobjekt stellt eine statische Wiedergabeliste dar. |
| EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D | Das Medienobjekt stellt eine automatische Wiedergabeliste dar.  |



 

**MediaClassSecondaryID ist** ein Alias für dieses Attribut.

Die Windows Media Format SDK-Konstante für dieses Attribut ist g \_ wszWMMediaClassSecondaryID.

Um zu bestimmen, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media.isReadOnlyItem-Methode.](media-isreadonlyitem.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Das Fotoelement wird nur in Windows Media Player 10 oder höher unterstützt. Das Optionselement wird nur in der Windows Media Player 9-Serie unterstützt. Alle anderen Elemente werden in Windows Media Player 9-Serie und höher unterstützt.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributreferenz**](attribute-reference.md)
</dt> </dl>

 

 





