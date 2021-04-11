---
description: Die WM- \_ spoolerstatus-Nachricht wird vom Druck-Manager gesendet, wenn ein Auftrag der Druck-Manager-Warteschlange hinzugefügt oder daraus entfernt wird.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: WM_SPOOLERSTATUS Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 460e36e44f219bcbe6f514d7d368accddae46b83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131801"
---
# <a name="wm_spoolerstatus-message"></a>WM- \_ spoolerstatus-Meldung

Die **WM- \_ spoolerstatus** -Nachricht wird vom Druck-Manager gesendet, wenn ein Auftrag der Druck-Manager-Warteschlange hinzugefügt oder daraus entfernt wird.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das PR- \_ Jobstatus-Flag.

</dd> <dt>

*lParam* 
</dt> <dd>

Mit dem nieder wertigen Wort wird die Anzahl der verbleibenden Aufträge in der Druck-Manager-Warteschlange angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Diese Meldung dient nur zu Informationszwecken. Diese Meldung ist eine Empfehlung und weist keine garantierte Übermittlungs Semantik auf. Anwendungen sollten nicht davon ausgehen, dass Sie eine WM- \_ spoolerstatus-Meldung für jede Änderung des spoolerstatus erhalten.

Die WM- \_ spoolerstatus-Nachricht wird nach Windows XP nicht unterstützt. Wenn Sie über Änderungen am Status der Druck Warteschlange benachrichtigt werden möchten, können Sie [**findfirstprinterchangenotifizierung**](findfirstprinterchangenotification.md) und [**findnextprinterchangenotifiken**](findnextprinterchangenotification.md)verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Meldungen](printing-and-print-spooler-messages.md)
</dt> <dt>

[**Findfirstprinterchangenotifizierung**](findfirstprinterchangenotification.md)
</dt> <dt>

[**Findnextprinterchangenotifizierung**](findnextprinterchangenotification.md)
</dt> </dl>

 

