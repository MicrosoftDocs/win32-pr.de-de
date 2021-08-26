---
title: WM_RASDIALEVENT Meldung (Ras.h)
description: Das Betriebssystem sendet eine WM \_ RASDIALEVENT-Nachricht an eine Fensterprozedur, wenn während eines RAS-Verbindungsprozesses ein Zustandsänderungsereignis auftritt.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- WM_RASDIALEVENT Nachricht RAS
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
ms.openlocfilehash: 093591ffe07ecbe662ca85306b74c34c670e1adbe51e2605b1f21faa20696c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024770"
---
# <a name="wm_rasdialevent-message"></a>WM \_ RASDIALEVENT-Nachricht

Das Betriebssystem sendet eine **\_ WM-RASDIALEVENT-Nachricht** an eine Fensterprozedur, wenn während eines RAS-Verbindungsprozesses ein Zustandsänderungsereignis auftritt. Dies geschieht, wenn ein Fenster angegeben wurde, um Benachrichtigungen solcher Ereignisse mithilfe des *Notifier-Parameters* von [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)zu behandeln.

Die beiden Nachrichtenparameter entsprechen den Parametern der gleichen Namen, die mit den Rückruffunktionen [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) und [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) verwendet werden.


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rasconnstate* 
</dt> <dd>

Der Wert von *wParam.* Entspricht dem *rasconnstate-Parameter* der Rückruffunktionen [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) und [**RasDialFunc1.**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) Gibt einen RASCONNSTATE-Enumeratorwert an, der den Zustand angibt, in den der RasDial-Remotezugriffsverbindungsprozess eingegeben werden soll. [](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))

</dd> <dt>

*dwError* 
</dt> <dd>

Der Wert von *lParam.* Entspricht dem *dwError-Parameter* der Rückruffunktionen [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) und [**RasDialFunc1.**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) Ein Wert ungleich 0 (null) gibt den aufgetretenen Fehler oder 0 (null) an, wenn kein Fehler aufgetreten ist.

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) sendet diese Nachricht, wobei *dwError* beim Eintrag in jeden Verbindungszustand auf 0 (null) festgelegt ist. Wenn ein Fehler innerhalb eines Zustands auftritt, wird die Nachricht für den Zustand erneut gesendet, dieses Mal mit einem dwError-Wert ungleich *0 (null).*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie **TRUE** zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Ras.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotezugriffsdienst (RAS) – Übersicht](about-remote-access-service.md)
</dt> <dt>

[Remotezugriffsdienst-Nachrichten](remote-access-service-messages.md)
</dt> <dt>

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))
</dt> </dl>

 

