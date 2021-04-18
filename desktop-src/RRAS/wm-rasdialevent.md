---
title: WM_RASDIALEVENT Meldung (RAS. h)
description: Das Betriebssystem sendet eine WM- \_ rasdialereignisnachricht an eine Fenster Prozedur, wenn während eines RAS-Verbindungsprozesses eine Änderung des Zustands Ereignisses auftritt.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- WM_RASDIALEVENT-Message-RAS
topic_type:
- apiref
api_name:
- WM_RASDIALEVENT
api_location:
- Ras.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 470fe3915c9f672c4663971159386e529ea60db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339119"
---
# <a name="wm_rasdialevent-message"></a>WM- \_ rasdialereignismeldung

Das Betriebssystem sendet eine **WM- \_ rasdialereignisnachricht** an eine Fenster Prozedur, wenn während eines RAS-Verbindungsprozesses eine Änderung des Zustands Ereignisses auftritt. Dies ist der Fall, wenn ein Fenster angegeben wurde, das Benachrichtigungen über solche Ereignisse mithilfe des *Benachrichtigung* -Parameters von [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala)behandelt.

Die beiden Nachrichten Parameter entsprechen den Parametern mit denselben Namen, die mit den Rückruf Funktionen von " [**rasdialfunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) " und " [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) " verwendet werden.


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rasrestate* 
</dt> <dd>

Der Wert von *wParam*. Entspricht dem " *rasconfiguration State* "-Parameter der " [**rasdialfunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) "-und " [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) "-Rückruffunktion. Gibt einen " [**rasnetwork State**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) "-Enumeratorwert an, der den Zustand angibt, in den der RAS-RAS-Verbindungsprozess eintritt.

</dd> <dt>

*dwError* 
</dt> <dd>

Der Wert von *LPARAM*. Entspricht dem *dwError* -Parameter der " [**rasdialfunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) "-und " [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) "-Rückruffunktion. Ein Wert ungleich NULL gibt den Fehler an, der aufgetreten ist, oder 0 (null), wenn kein Fehler aufgetreten ist.

Der [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) sendet diese Nachricht mit *dwError* auf NULL festgelegt, wenn für den jeweiligen Verbindungsstatus ein Eintrag festgelegt ist. Wenn ein Fehler innerhalb eines Zustands auftritt, wird die Nachricht erneut für den Zustand gesendet, dieses Mal mit einem *dwError* -Wert ungleich 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>RAS. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remote Zugriffs Dienst (RAS) (Übersicht)](about-remote-access-service.md)
</dt> <dt>

[Remote Zugriffs Dienst-Meldungen](remote-access-service-messages.md)
</dt> <dt>

[**Rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[**Rasdialfunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

[**Rasrestate**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))
</dt> </dl>

 

