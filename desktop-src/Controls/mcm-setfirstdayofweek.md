---
title: MCM_SETFIRSTDAYOFWEEK Meldung (kommstrg. h)
description: Legt den ersten Tag der Woche für ein Monatskalender-Steuerelement fest. Sie können diese Nachricht explizit oder mit dem monthcal \_ setfirstdayof Week-Makro senden.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- Windows-Steuerelemente für MCM_SETFIRSTDAYOFWEEK Meldung
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
ms.openlocfilehash: a32452c9043bbd7c3bbcf96f9dc32e67714eacce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343059"
---
# <a name="mcm_setfirstdayofweek-message"></a>MCM \_ setfirstdayof Week-Meldung

Legt den ersten Tag der Woche für ein Monatskalender-Steuerelement fest. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ setfirstdayof Week**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Wert vom Typ **int** , der angibt, welcher Tag als erster Wochentag festgelegt werden soll, wobei 0 für Montag, 1 für Dienstag usw. steht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD** -Wert zurück, der zwei Werte enthält. Das hohe Wort ist ein **boolescher** Wert, der ungleich 0 (null) ist, wenn der vorherige erste Tag der Woche nicht dem Gebiets Schema \_ ifirstdayosweek entspricht, andernfalls NULL. Das niedrige Wort ist ein int-Wert, der den vorherigen ersten Tag der Woche darstellt.

## <a name="remarks"></a>Bemerkungen

Wenn der erste Tag der Woche auf einen anderen Wert als den Standardwert festgelegt ist (Gebiets Schema \_ ifirstdayofweek), aktualisiert das Steuerelement die Änderungen am Wochentag nicht automatisch basierend auf Gebiets Schema Änderungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





