---
title: DTN_DROPDOWN Benachrichtigungs Code (kommctrl. h)
description: Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer den Dropdown-Monatskalender aktiviert. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 6f20fa87-2223-4876-b77d-2c684685bf10
keywords:
- Windows-Steuerelemente für DTN_DROPDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- DTN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101a25a8e2da09b9f4065a54fcff9896690adbb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859076"
---
# <a name="dtn_dropdown-notification-code"></a>DTN- \_ Dropdown-Benachrichtigungs Code

Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer den Dropdown-Monatskalender aktiviert. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
DTN_DROPDOWN

    lpNmhdr = (LPNMHDR)lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die Informationen zur Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="remarks"></a>Bemerkungen

Eine Aufgabe, die der Benachrichtigungs Handler ausführen muss, besteht darin, das Dropdown-Monatskalender-Steuerelement anzupassen. Wenn Sie beispielsweise "Gehe zu heute" nicht möchten, müssen Sie den [**MCS- \_ notoday**](month-calendar-control-styles.md)  -Stil des Steuer Elements festlegen. Um ein Handle für das Month-Calendar-Steuerelement abzurufen, senden Sie dem DTP-Steuerelement eine [**DTM \_ getmonthcal**](dtm-getmonthcal.md) -Nachricht. Anschließend können Sie dieses Handle und [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) verwenden, um den gewünschten Monat Kalender Stil festzulegen.

DTP-Steuerelemente behalten kein statisches Steuerelement für untergeordnete Monatskalender bei. Das DTP-Steuerelement erstellt vor dem Senden dieses Benachrichtigungs Codes ein neues Monatskalender-Steuerelement. Darüber hinaus zerstört das DTP-Steuerelement das untergeordnete Steuerelement, wenn es nicht aktiv ist (sichtbar). Daher darf Ihre Anwendung nicht auf ein statisches Fenster Handle für den untergeordneten Monatskalender des Steuer Elements zurückgreifen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[DTN- \_ Schließung](dtn-closeup.md)
</dt> <dt>

[**DTM \_ getmonthcal**](dtm-getmonthcal.md)
</dt> </dl>

 

