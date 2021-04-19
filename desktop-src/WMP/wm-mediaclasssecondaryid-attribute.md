---
title: WM/MediaClassSecondaryID-Attribut
description: Das WM/MediaClassSecondaryID-Attribut ist eine GUID, die die sekundäre Medienklasse angibt, bei der es sich um eine Unterklasse der primären Medienklasse handelt.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- WM/MediaClassSecondaryID-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb88ea03e565df649088366e13b20332256b374d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367646"
---
# <a name="wmmediaclasssecondaryid-attribute"></a>WM/MediaClassSecondaryID-Attribut

Das **WM/MediaClassSecondaryID-** Attribut ist eine GUID, die die sekundäre Medienklasse angibt, bei der es sich um eine Unterklasse der primären Medienklasse handelt.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Media-Dateiattribute](commonly-used-windows-media-file-attributes.md)
-   [Andere Elemente](other-item-attributes.md)
-   [Foto Elemente](photo-item-attributes.md)
-   [Wiedergabelisten](playlist-attributes-ref.md)
-   [Options Felder](radio-item-attributes.md)
-   [Video Elemente](video-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.

In der folgenden Tabelle sind die unterstützten GUIDs und ihre Beschreibungen aufgeführt.



| GUID                                 | Beschreibung                                    |
|--------------------------------------|------------------------------------------------|
| D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC | Das Medienobjekt stellt eine statische Wiedergabeliste dar. |
| EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D | Das Medienobjekt stellt eine automatische Wiedergabeliste dar.  |



 

**MediaClassSecondaryID** ist ein Alias für dieses Attribut.

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmmediaclasssecondaryid.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Das Foto Element wird nur in Windows Media Player 10 oder höher unterstützt. das Optionsfeld wird nur in Windows Media Player 9-Reihe unterstützt. alle anderen Elemente werden in Windows Media Player 9 und höher unterstützt.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





