---
description: Die WM SPOOLERSTATUS-Nachricht wird immer dann vom Druck-Manager gesendet, wenn der Druck-Manager-Warteschlange ein Auftrag hinzugefügt \_ oder daraus entfernt wird.
ms.assetid: 6140c9d8-0e5b-49f2-a4a6-cc1f2a0bed0a
title: WM_SPOOLERSTATUS (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2869c468517abf466b348583748e391fc1f2a4226c74b5811fffabdb5eeb89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460340"
---
# <a name="wm_spoolerstatus-message"></a>WM \_ SPOOLERSTATUS-Meldung

Die **WM \_ SPOOLERSTATUS-Nachricht** wird immer dann vom Druck-Manager gesendet, wenn der Druck-Manager-Warteschlange ein Auftrag hinzugefügt oder daraus entfernt wird.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Das PR \_ JOBSTATUS-Flag.

</dd> <dt>

*lParam* 
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt die Anzahl der Aufträge an, die in der Druck-Manager-Warteschlange übrig bleiben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Hinweise

Diese Meldung dient nur zu Informationszwecken. Diese Nachricht ist eine Empfehlung und verfügt nicht über eine garantierte Übermittlungssemantik. Anwendungen sollten nicht davon ausgehen, dass sie für jede Änderung des Spoolerstatus eine WM \_ SPOOLERSTATUS-Meldung erhalten.

Die WM \_ SPOOLERSTATUS-Meldung wird nach der Installation Windows XP nicht mehr unterstützt. Um über Änderungen am Status der Druckwarteschlange benachrichtigt zu werden, können Sie [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) und [**FindNextPrinterChangeNotification verwenden.**](findnextprinterchangenotification.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Nachrichten](printing-and-print-spooler-messages.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> </dl>

 

