---
title: MCM_GETFIRSTDAYOFWEEK Meldung (kommstrg. h)
description: Ruft den ersten Tag der Woche für ein Monatskalender-Steuerelement ab. Sie können diese Nachricht explizit oder mit dem monthcal \_ getfirstdayof Week-Makro senden.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- Windows-Steuerelemente für MCM_GETFIRSTDAYOFWEEK Meldung
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
ms.openlocfilehash: b625e470e13c111b0274bfef422963e48c9cc7c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339345"
---
# <a name="mcm_getfirstdayofweek-message"></a>MCM \_ getfirstdayof Week-Meldung

Ruft den ersten Tag der Woche für ein Monatskalender-Steuerelement ab. Sie können diese Nachricht explizit oder mit dem [**monthcal \_ getfirstdayof Week**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD** -Wert zurück, der zwei Werte enthält. Das hohe Wort ist ein **boolescher** Wert, der ungleich 0 (null) ist, wenn der erste Tag der Woche auf einen anderen Wert als "locale \_ ifirstdayofweek" festgelegt ist, andernfalls "Null". Das niedrige Wort ist ein int-Wert, der den ersten Tag der Woche darstellt, wobei 0 für Montag, 1 für Dienstag usw. steht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





