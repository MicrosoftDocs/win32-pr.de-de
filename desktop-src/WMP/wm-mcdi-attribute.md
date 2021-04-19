---
title: WM/MCDI-Attribut
description: Das WM/MCDI-Attribut ist der Musik-CD-Bezeichner der CD, von der die Datei oder der Titel kopiert wurde.
ms.assetid: f0bec14d-416c-477f-98df-dece0bf85ea4
keywords:
- WM/MCDI-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aec51c306f94e25acb94155c4d87f1f1a8b95866
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369487"
---
# <a name="wmmcdi-attribute"></a>WM/MCDI-Attribut

Das **WM/MCDI-** Attribut ist der Musik-CD-Bezeichner der CD, von der die Datei oder der Titel kopiert wurde.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [CD-Spuren](cd-track-attributes.md)
-   [Häufig verwendete Windows Media-Dateiattribute](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist sowohl in der Bibliothek (oder im Cache) als auch in der digitalen Mediendatei gespeichert.

"Inhaltsverzeichnis **" ist ein** Alias für dieses Attribut.

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmmcdi.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





