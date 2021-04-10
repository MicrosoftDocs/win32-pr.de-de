---
title: MCN_SELCHANGE Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Monatskalender-Steuerelement gesendet, wenn das aktuell ausgewählte Datum oder der Datumsbereich geändert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- Windows-Steuerelemente für MCN_SELCHANGE Benachrichtigungs
topic_type:
- apiref
api_name:
- MCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffa328ca0173afd3a577f6cf14e0204cd5c0f7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040240"
---
# <a name="mcn_selchange-notification-code"></a>MCN \_ selChange-Benachrichtigungs Code

Wird von einem Monatskalender-Steuerelement gesendet, wenn das aktuell ausgewählte Datum oder der Datumsbereich geändert wird. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmselchange**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) -Struktur, die Informationen über den aktuell ausgewählten Datumsbereich enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Beispielsweise sendet das Steuerelement MCN \_ selChange, wenn der Benutzer die Auswahl innerhalb des aktuellen Monats explizit ändert oder wenn die Auswahl in Reaktion auf die nächste/vorherige Monats Navigation implizit geändert wird. Dieser Benachrichtigungs Code wird auch in regelmäßigen Abständen vom System gesendet, sodass das Steuerelement auf Datumsänderungen reagieren kann.

Dieser Benachrichtigungs Code ähnelt [MCN \_ Select](mcn-select.md), aber er wird als Reaktion auf eine beliebige Auswahl Änderung gesendet. \_Die Auswahl von MCN wird nur für eine explizite Datumsauswahl gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





