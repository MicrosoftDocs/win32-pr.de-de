---
title: HDM_ORDERTOINDEX (Commctrl.h)
description: Ruft einen Indexwert für ein Element basierend auf seiner Reihenfolge im Headersteuerelement ab. Sie können diese Nachricht explizit senden oder das \_ OrderToIndex-Makro Header verwenden.
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- HDM_ORDERTOINDEX meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7afd006c90684137ffc484dac62ab40c04d90c0cdbc87f51102d8e9119e8b14d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576259"
---
# <a name="hdm_ordertoindex-message"></a>HDM \_ ORDERTOINDEX-Nachricht

Ruft einen Indexwert für ein Element basierend auf seiner Reihenfolge im Headersteuerelement ab. Sie können diese Nachricht explizit senden oder das [**\_ OrderToIndex-Makro Header**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Reihenfolge, in der das Element im Headersteuerelement von links nach rechts angezeigt wird. Der Indexwert des Elements in der spalte ganz links wäre z. B. 0. Der Wert für das nächste Element auf der rechten Seite wäre 1, und so weiter.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt INT zurück, das den Elementindex angibt. Wenn *wParam* ungültig (negativ oder zu groß) ist, entspricht die Rückgabe *wParam*.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





