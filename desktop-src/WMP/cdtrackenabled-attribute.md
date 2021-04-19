---
title: Cdtrackaktiviertes Attribut
description: Das cdtrackaktivierte-Attribut gibt an, ob der Titel für die Wiedergabe aktiviert ist.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- Cdtrackaktiviertes Attribut Windows Media Player
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81c231dbdfc432ea7aa510a19b1f85e0826c836
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359813"
---
# <a name="cdtrackenabled-attribute"></a>Cdtrackaktiviertes Attribut

Das **cdtrackaktivierte** -Attribut gibt an, ob der Titel für die Wiedergabe aktiviert ist.

## <a name="applies-to"></a>Gilt für

-   [CD-Spuren](cd-track-attributes.md)

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist nur im Bibliotheks Cache gespeichert.

Bei der Wiedergabe einer CD in Windows Media Player kann der Benutzer eine Spur auswählen und angeben, dass er nicht wiedergegeben werden soll. Dieser Wert dieses Attributs ist true, wenn der Titel wiedergegeben werden kann, oder false, wenn der Benutzer angegeben hat, dass der Titel nicht wiedergegeben werden soll.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





