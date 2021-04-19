---
title: Mediacontenttypes-Attribut
description: Das mediacontenttypes-Attribut gibt den Typ des Inhalts im Element an.
ms.assetid: b91bab65-d6d2-4e05-9338-c24f28b7c71e
keywords:
- Mediacontenttypes-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- MediaContentTypes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8979864151e029abf2731f6f0b4663e078a2c061
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352945"
---
# <a name="mediacontenttypes-attribute"></a>Mediacontenttypes-Attribut

Das **mediacontenttypes** -Attribut gibt den Typ des Inhalts im Element an.

## <a name="applies-to"></a>Gilt für

-   [Wiedergabelisten](playlist-attributes-ref.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut kann einen der folgenden Werte aufweisen:



| Wert | Bedeutung                                |
|-------|----------------------------------------|
| 1     | Die Wiedergabeliste enthält Audioinhalte.   |
| 2     | , Um bereitgestellt zu werden.                        |
| 3     | Die Wiedergabeliste enthält Audioinhalte.   |
| 4     | Die Wiedergabeliste enthält Videoinhalte.   |
| 5     | Die Wiedergabeliste enthält Bildinhalte. |
| 6     | Die Wiedergabeliste enthält TV-Inhalte.      |



 

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





