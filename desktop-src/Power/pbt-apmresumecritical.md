---
description: Benachrichtigt Anwendungen, dass das System den Vorgang fortgesetzt hat.
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: PBT_APMRESUMECRITICAL-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4a76e163f2e61e723f4df6572254e8ef89b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353457"
---
# <a name="pbt_apmresumecritical-event"></a>PBT \_ apmresumecritical-Ereignis

\[PBT \_ apmresumecritical ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Die Unterstützung für dieses Ereignis wurde in Windows Vista entfernt. Verwenden Sie stattdessen [PBT \_ apmresumeautomatic](pbt-apmresumeautomatic.md) .\]

Benachrichtigt Anwendungen, dass das System den Vorgang fortgesetzt hat. Dieses Ereignis kann darauf hinweisen, dass einige oder alle Anwendungen kein [PBT \_ apmsuspend](pbt-apmsuspend.md) -Ereignis empfangen haben. Beispielsweise kann dieses Ereignis nach einer kritischen Unterbrechung gesendet werden, die durch einen fehlerhaften Akku verursacht wird.

Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht. Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMECRITICAL
            LPARAM lParam); // zero
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

| Wert                                                                                                                                                                                                                                              | Bedeutung                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <dt>**PBT \_ Apmresumecritical**</dt> <dt>6 (0x6)</dt> </dl> | Ereignis Bezeichner.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Bleiben muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Da eine Notabschaltung ohne vorherige Benachrichtigung aufgetreten ist, sind zuvor verfügbare Ressourcen und Daten möglicherweise nicht vorhanden, wenn die Anwendung dieses Ereignis empfängt. Die Anwendung sollte versuchen, ihren Status im Rahmen ihrer Möglichkeiten optimal wiederherzustellen. Während einer kritischen Unterbrechung behält das System den Status des DRAM und der lokalen Festplatten bei, behält aber möglicherweise keine Netzwerkverbindungen bei. Eine Anwendung muss möglicherweise in Bezug auf Dateien, die im Netzwerk geöffnet waren, vor kritischer Unterbrechung Maßnahmen ergreifen.

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

[**WM- \_ powerbroadcast**](wm-powerbroadcast.md)
</dt> </dl>

 

 




