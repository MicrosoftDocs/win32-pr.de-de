---
title: Description-Attribut (WMP SDK)
description: Das Beschreibungs Attribut ist eine Beschreibung des Inhalts.
ms.assetid: 8bf76bf5-2bba-4ceb-bc98-f8b8ab2c8b6f
keywords:
- Description-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- Description
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4bc3562e7b807dc0e333c887aad1550d05b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357581"
---
# <a name="description-attribute"></a>Description-Attribut

Das **Beschreibungs** Attribut ist eine Beschreibung des Inhalts.

## <a name="applies-to"></a>Gilt für

-   [Musikdateien](music-file-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird in Musikdateien, nicht in der Bibliothek gespeichert.

Dieses Attribut kann mehrere Werte aufweisen. Wenn Sie alle Werte für ein mehr wertiges Attribut abrufen möchten, müssen Sie die *Medien* verwenden. **getItemInfoByType** -Methode, nicht die *Media*. getiteminfo-Methode.

Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszwmdescription.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





