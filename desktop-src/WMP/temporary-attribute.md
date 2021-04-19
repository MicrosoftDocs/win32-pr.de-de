---
title: Temporäres Attribut
description: Das temporäre Attribut gibt an, ob eine Wiedergabeliste temporär ist.
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- Temporäres Attribut Fenster Media Player
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70ae8f3ae06ae44077cce3d8fa3fdf67dc853eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354056"
---
# <a name="temporary-attribute"></a>Temporäres Attribut

Das **temporäre** Attribut gibt an, ob eine Wiedergabeliste temporär ist.

**Anmerkungen**

Wenn Sie eine Wiedergabeliste aus der Bibliothek abgerufen haben, werden die Änderungen, die Sie an der Wiedergabeliste vornehmen, in der Bibliothek des Benutzers widergespiegelt. Um dies zu vermeiden, nennen Sie [iwmpwiedergabe:: Set Items MINFO](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) , und übergeben Sie den Attributnamen "temporär" und den Wert "true". Dadurch wird die Wiedergabelisten Instanz in eine temporäre Wiedergabeliste konvertiert, die ohne Änderung der ursprünglichen Wiedergabeliste sicher bearbeitet werden kann.

**Gilt für**

-   [Wiedergabelisten](playlist-attributes-ref.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





