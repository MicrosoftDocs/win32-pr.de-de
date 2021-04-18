---
title: LVN_MARQUEEBEGIN Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass eine Begrenzungsfeld Auswahl (Marquee) begonnen hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- Windows-Steuerelemente für LVN_MARQUEEBEGIN Benachrichtigungs
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
ms.openlocfilehash: 8d46d399b8355bea0ddb2054340d52db59c3ad27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340020"
---
# <a name="lvn_marqueebegin-notification-code"></a>LVN- \_ marqueebegin-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass eine Begrenzungsfeld Auswahl (Marquee) begonnen hat. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Um den Benachrichtigungs Code zu akzeptieren, wird NULL zurückgegeben. Um die Begrenzungsfeld Auswahl zu beenden, geben Sie einen Wert ungleich 0 (null)

## <a name="remarks"></a>Bemerkungen

Bei der *Auswahl eines Begrenzungs* Rahmens handelt es sich um den Prozess, bei dem auf den Client Bereich der Listenansicht geklickt und mehrere Elemente gleichzeitig ausgewählt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





