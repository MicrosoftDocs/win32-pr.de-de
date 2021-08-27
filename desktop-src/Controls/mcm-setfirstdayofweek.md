---
title: MCM_SETFIRSTDAYOFWEEK (Commctrl.h)
description: Legt den ersten Tag der Woche für ein Monatskalender-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des \_ MonthCal-Makros SetFirstDayOfWeek senden.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- MCM_SETFIRSTDAYOFWEEK von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- MCM_SETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e34732257c18acceec3fd7db9807753e9a930e106198b33a0dd61dc27a33eef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077110"
---
# <a name="mcm_setfirstdayofweek-message"></a>MCM \_ SETFIRSTDAYOFWEEK-Nachricht

Legt den ersten Tag der Woche für ein Monatskalender-Steuerelement fest. Sie können diese Nachricht explizit oder mithilfe des [**\_ MonthCal-Makros SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Der Wert vom Typ **int,** der darstellt, welcher Tag als erster Tag der Woche festgelegt werden soll, wobei 0 für Montag, 1 für Dienstag und so weiter ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD-Wert** zurück, der zwei Werte enthält. Das hohe Wort ist ein **BOOL-Wert** ungleich null, wenn der vorherige erste Tag der Woche nicht LOCALE \_ IFIRSTDAYOFWEEK oder 0 (null) war. Das niedrige Wort ist ein INT-Wert, der den vorherigen ersten Tag der Woche darstellt.

## <a name="remarks"></a>Hinweise

Wenn der erste Tag der Woche auf einen anderen Als den Standardwert (LOCALE IFIRSTDAYOFWEEK) festgelegt ist, aktualisiert das Steuerelement änderungen am ersten Wochentag nicht automatisch auf Grundlage von Änderungen am Ersten Tag der \_ Woche.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





