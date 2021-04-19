---
title: WM/Writer-Attribut
description: Das WM/Writer-Attribut ist der Name des Writers, der die Wörter des Inhalts geschrieben hat.
ms.assetid: e2035cf7-29f4-4642-9388-4cd7cb08149e
keywords:
- WM/Writer-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/Writer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29aabf353fc742370ac5d01f084544be8143d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359630"
---
# <a name="wmwriter-attribute"></a>WM/Writer-Attribut

Das **WM/Writer-** Attribut ist der Name des Writers, der die Wörter des Inhalts geschrieben hat.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [Häufig verwendete Windows Media-Dateiattribute](commonly-used-windows-media-file-attributes.md)
-   [Video Elemente](video-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.

Dieses Attribut kann mehrere Werte aufweisen. Wenn Sie alle Werte für ein mehr wertiges Attribut abrufen möchten, müssen Sie die Media. **getItemInfoByType** -Methode und nicht die **Media. getiteminfo** -Methode verwenden.

**Writer** ist ein Alias für dieses Attribut.

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmwriter.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





