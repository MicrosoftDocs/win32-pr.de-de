---
title: WM/GenreID-Attribut
description: Das WM/GenreID-Attribut ist ein Genrebezeichner, der mit dem TCON-Tag in ID3v2 kompatibel ist.
ms.assetid: 9b68f9be-1f02-4b14-b052-90657b8800e3
keywords:
- WM/GenreID-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fdb409453bbdc6a30026b5d36cb35bbaeb2a21264e5049c9e5fff520aea08b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332326"
---
# <a name="wmgenreid-attribute"></a>WM/GenreID-Attribut

Das **WM/GenreID-Attribut** ist ein Genrebezeichner, der mit dem TCON-Tag in ID3v2 kompatibel ist.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Mediendateiattribute](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird nur in der digitalen Mediendatei gespeichert.

ID3 Version 2 ist eine Markierungskonvention, die ursprünglich für MP3 entwickelt wurde. Weitere Informationen finden Sie auf der Website der [ID3-Organisation.](https://id3.org/)

Die Windows Media Format SDK-Konstante für dieses Attribut ist g \_ wszGenreID.

Verwenden Sie die [Media.isReadOnlyItem-Methode,](media-isreadonlyitem.md) um zu bestimmen, ob Sie den Wert dieses Attributs ändern können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie Windows Media Player 10 oder höher unterstützt dieses Attribut nicht.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> </dl>

 

 





