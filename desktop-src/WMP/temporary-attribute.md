---
title: Temporäres Attribut
description: Das Temporary-Attribut gibt an, ob eine Wiedergabeliste temporär ist.
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- Temporäre Windows Media Player
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8f6101d6b41a7a66bbc29d2a30f3166427f4db7cb583508165cc28639fc6f58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933498"
---
# <a name="temporary-attribute"></a>Temporäres Attribut

Das **Temporary-Attribut** gibt an, ob eine Wiedergabeliste temporär ist.

**Anmerkungen**

Wenn Sie eine Wiedergabeliste aus der Bibliothek abgerufen haben, werden Änderungen, die Sie an der Wiedergabeliste vornehmen, in der Bibliothek des Benutzers widergespiegelt. Um dies zu vermeiden, rufen [Sie IWMPPlaylist::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) auf, und übergeben Sie dabei den Attributnamen "Temporary" und den Wert "true". Dadurch wird Ihre Wiedergabelisteninstanz in eine temporäre Wiedergabeliste konvertiert, die problemlos bearbeitet werden kann, ohne die ursprüngliche Wiedergabeliste zu ändern.

**Gilt für**

-   [Wiedergabelisten](playlist-attributes-ref.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributreferenz**](attribute-reference.md)
</dt> </dl>

 

 





