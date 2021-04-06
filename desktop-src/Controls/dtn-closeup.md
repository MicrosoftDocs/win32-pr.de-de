---
title: DTN_CLOSEUP Benachrichtigungs Code (kommctrl. h)
description: Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer den Dropdown-Monatskalender schließt.
ms.assetid: 94ace714-55cc-4c59-8b87-8d0348b15f34
keywords:
- Windows-Steuerelemente für DTN_CLOSEUP Benachrichtigungs
topic_type:
- apiref
api_name:
- DTN_CLOSEUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cfcfb23215aeffe15bec576075fd4d930790e47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742832"
---
# <a name="dtn_closeup-notification-code"></a>DTN- \_ closeup-Benachrichtigungs Code

Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn der Benutzer den Dropdown-Monatskalender schließt. Der Monatskalender wird geschlossen, wenn der Benutzer ein Datum aus dem Monatskalender auswählt oder auf den Dropdown Pfeil klickt, während der Kalender geöffnet ist. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
DTN_CLOSEUP

    lpNmhdr = (LPMNHDR)lParam;
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

DTP-Steuerelemente behalten kein statisches Steuerelement für untergeordnete Monatskalender bei. Das DTP-Steuerelement zerstört das Kalender Steuerelement des untergeordneten Monats vor dem Senden dieses Benachrichtigungs Codes. Daher darf Ihre Anwendung nicht auf ein statisches Fenster Handle für den untergeordneten Monatskalender des Steuer Elements zurückgreifen.

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

[DTN- \_ Dropdown](dtn-dropdown.md)
</dt> <dt>

[**DTM \_ getmonthcal**](dtm-getmonthcal.md)
</dt> </dl>

 

 





