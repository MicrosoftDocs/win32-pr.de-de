---
title: MCM_GETFIRSTDAYOFWEEK Meldung (Commctrl.h)
description: Ruft den ersten Tag der Woche für ein Monatskalender-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des \_ MonthCal GetFirstDayOfWeek-Makros senden.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- MCM_GETFIRSTDAYOFWEEK Windows-Steuerelementen
topic_type:
- apiref
api_name:
- MCM_GETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc0ddcd36da0b993f3a05092c878319a6749d9eb5a3043ce910eba1462beef9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319650"
---
# <a name="mcm_getfirstdayofweek-message"></a>MCM \_ GETFIRSTDAYOFWEEK-Nachricht

Ruft den ersten Tag der Woche für ein Monatskalender-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**MonthCal \_ GetFirstDayOfWeek-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD-Wert** zurück, der zwei Werte enthält. Das obere Wort ist ein **BOOL-Wert,** der ungleich 0 (null) ist, wenn der erste Tag der Woche auf einen anderen Wert als LOCALE \_ IFIRSTDAYOFWEEK oder andernfalls auf 0 (null) festgelegt ist. Das niedrige Wort ist ein INT-Wert, der den ersten Tag der Woche darstellt, wobei 0 Montag, 1 Dienstag usw. ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





