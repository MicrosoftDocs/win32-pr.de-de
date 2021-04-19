---
title: WM/Dirigent-Attribut
description: Das WM/Conductor-Attribut ist der Name des Dirigenten der Musik.
ms.assetid: 31c7d310-da6a-4c30-86b0-15defaee1743
keywords:
- WM/Dirigent-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- WM/Conductor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1ae08dfee807d130f04dd258c6af81a8d68057
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359322"
---
# <a name="wmconductor-attribute"></a>WM/Dirigent-Attribut

Das **WM/Conductor-** Attribut ist der Name des Dirigenten der Musik.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)
-   [CD-Spuren](cd-track-attributes.md)
-   [Häufig verwendete Windows Media-Dateiattribute](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist sowohl in der Bibliothek (oder im Cache) als auch in der digitalen Mediendatei gespeichert.

Dieses Attribut kann mehrere Werte aufweisen. Wenn Sie alle Werte für ein mehr wertiges Attribut abrufen möchten, müssen Sie die Media. **getItemInfoByType** -Methode und nicht die **Media. getiteminfo** -Methode verwenden.

Der- **Dirigent** ist ein Alias für dieses Attribut.

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmconductor.

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

 

 





