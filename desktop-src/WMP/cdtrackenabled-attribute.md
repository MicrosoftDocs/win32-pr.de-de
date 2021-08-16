---
title: CDTrackEnabled-Attribut
description: Das CDTrackEnabled-Attribut gibt an, ob die Spur für die Wiedergabe aktiviert ist.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- CDTrackEnabled-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a86c94c2c1b44327cdbfb35544c3e0b5b34d25885215d78dbec0ec084d056e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342683"
---
# <a name="cdtrackenabled-attribute"></a>CDTrackEnabled-Attribut

Das **CDTrackEnabled-Attribut** gibt an, ob die Spur für die Wiedergabe aktiviert ist.

## <a name="applies-to"></a>Gilt für

-   [CD-Spuren](cd-track-attributes.md)

## <a name="remarks"></a>Hinweise

Dieses Attribut wird nur im Bibliothekscache gespeichert.

Beim Wiedergeben einer CD in Windows Media Player kann der Benutzer einen Titel auswählen und angeben, dass er nicht wiedergegeben werden soll. Dieser Wert dieses Attributs ist True, wenn die Spur wiedergegeben werden kann, oder False, wenn der Benutzer angegeben hat, dass die Spur nicht wiedergegeben werden soll.

Verwenden Sie die [Media.isReadOnlyItem-Methode,](media-isreadonlyitem.md) um zu bestimmen, ob Sie den Wert dieses Attributs ändern können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> </dl>

 

 





