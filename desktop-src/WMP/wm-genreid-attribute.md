---
title: WM/GenreID-Attribut
description: Das WM/GenreID-Attribut ist ein Genre Bezeichner, der mit dem TCON-Tag in "ID3v2" kompatibel ist.
ms.assetid: 9b68f9be-1f02-4b14-b052-90657b8800e3
keywords:
- WM/GenreID-Attribut Fenster Media Player
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d31e54805f778a51f345c84654056391ec4052e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358042"
---
# <a name="wmgenreid-attribute"></a>WM/GenreID-Attribut

Das **WM/GenreID-** Attribut ist ein Genre Bezeichner, der mit dem TCON-Tag in "ID3v2" kompatibel ist.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Media-Dateiattribute](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird nur in der digitalen Mediendatei gespeichert.

ID3 Version 2 ist eine Tagging-Konvention, die ursprünglich für MP3 entworfen wurde. Weitere Informationen finden Sie auf der [Website der ID3-Organisation](https://id3.org/).

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszgenreid.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie Windows Media Player 10 oder höher unterstützt dieses Attribut nicht.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





