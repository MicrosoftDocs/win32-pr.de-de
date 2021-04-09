---
description: Fordert die Berechtigung zum Aussetzen des Computers an. Eine Anwendung, die die Erlaubnis erteilt, muss vor dem Beenden Vorbereitungen für den Standbymodus treffen.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: PBT_APMQUERYSUSPEND-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277e4faf7617037b917dedab3193e421a381166a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865072"
---
# <a name="pbt_apmquerysuspend-event"></a>PBT \_ apmquerysuspend-Ereignis

\[PBT \_ apmquerysuspend ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Die Unterstützung für dieses Ereignis wurde in Windows Vista entfernt. Verwenden Sie stattdessen [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) .\]

Fordert die Berechtigung zum Aussetzen des Computers an. Eine Anwendung, die die Erlaubnis erteilt, muss vor dem Beenden Vorbereitungen für den Standbymodus treffen.

Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht. Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPEND
            LPARAM lParam); // action flags
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Ein Handle für Fenster.

</dd> <dt>*Umschlag*</dt> <dd> 

| Wert                                                                                                                                                                                                                                                                   | Bedeutung                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ Powerbroadcast**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Nachrichten-ID.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Wert                                                                                                                                                                                                                                        | Bedeutung                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <dt>**PBT \_ Apmquerysuspend**</dt> <dt>0 (0x0)</dt> </dl> | Ereignis Bezeichner.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Die Aktionsflags. Wenn Bit 0 1 ist, kann die Anwendung den Benutzer zur Eingabe von Anweisungen auffordern, wie die Unterbrechung vorbereitet werden soll. Andernfalls muss die Anwendung ohne Benutzerinteraktion vorbereitet werden. Alle anderen Bitwerte sind reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, um die Anforderung zum aussetzen zu erteilen. Um die Anforderung zu verweigern, geben Sie **Broadcast \_ Query \_ Deny** zurück.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung sollte dieses Ereignis so schnell wie möglich verarbeiten. Die Anwendung kann den Benutzer zur Eingabe von Anweisungen auffordern, wie die Unterbrechung vorbereitet werden soll, wenn Bit 0 im *Flags* -Parameter festgelegt ist. Wenn diese Meldung jedoch ausgegeben wird, weil der Benutzer die Laptop-Lid schließt, ist es nicht möglich, den Benutzer zur Eingabe aufzufordern. Anwendungen sollten beachten, dass der Benutzer ein bestimmtes Verhalten erwartet, wenn er die Laptop-Taste schließt oder den Netzschalter drückt und den Übergang zulässt.

Das System lässt zu, dass eine Anwendung ungefähr 20 Sekunden die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht entfernt, die das PBT \_ apmquerysuspend-Ereignis aus der Nachrichten Warteschlange der Anwendung sendet. Wenn eine Anwendung die Nachricht nicht in weniger als 20 Sekunden aus der Warteschlange entfernt, geht das System davon aus, dass sich die Anwendung in einem nicht reagierenden Zustand befindet und dass die Anwendung der standbyanforderung zustimmt. Anwendungen, die Ihre Nachrichten Warteschlangen nicht verarbeiten, werden möglicherweise unterbrochen. Nachdem die Nachricht aus der Nachrichten Warteschlange entfernt wurde, kann es so lange dauern, bis alle erforderlichen Vorgänge ausgeführt werden, bevor Sie in den Ruhezustand wechseln. Alle Vorgänge, die länger als 20 Sekunden dauern könnten, sollten zu diesem Zeitpunkt ausgeführt werden, da das System während der [PBT- \_ apmsuspend](pbt-apmsuspend.md) -Verarbeitung nur 20 Sekunden für den Abschluss von Vorgängen zulässt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                                    |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                                           |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[System Aktivierungs Ereignisse](system-wake-up-events.md)
</dt> <dt>

[Energie Verwaltungs Ereignisse](power-management-events.md)
</dt> <dt>

[PBT \_ apmsuspend](pbt-apmsuspend.md)
</dt> <dt>

[**WM- \_ powerbroadcast**](wm-powerbroadcast.md)
</dt> </dl>

 

 




