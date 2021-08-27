---
title: LVN_MARQUEEBEGIN Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuerelements, dass die Auswahl eines Begrenzungsfelds (Festzelt) begonnen hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- LVN_MARQUEEBEGIN Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8012981883564450603d11d0eb243375f48b46cdb14a14984a19415c84dab3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109530"
---
# <a name="lvn_marqueebegin-notification-code"></a>LVN \_ MARQUEEBEGIN-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuerelements, dass die Auswahl eines Begrenzungsfelds (Festzelt) begonnen hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMHDR-Struktur.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Um den Benachrichtigungscode zu akzeptieren, geben Sie 0 (null) zurück. Um die Auswahl des Begrenzungsfelds zu beenden, geben Sie ungleich 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Eine *Begrenzungsfeldauswahl ist* der Vorgang, bei dem auf den Clientbereich des Listenansichtsfensters geklickt und gezogen wird, um mehrere Elemente gleichzeitig auszuwählen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





