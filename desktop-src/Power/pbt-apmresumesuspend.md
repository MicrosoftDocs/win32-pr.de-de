---
description: Benachrichtigt Anwendungen, dass das System den Vorgang fortgesetzt hat, nachdem es angehalten wurde.
ms.assetid: 9058a2ff-9b8e-48e5-accb-4810c8598294
title: PBT_APMRESUMESUSPEND-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d26357215853e0989851b6a9e731340a8dc2e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363466"
---
# <a name="pbt_apmresumesuspend-event"></a>PBT \_ apmresumesuspend-Ereignis

Benachrichtigt Anwendungen, dass das System den Vorgang fortgesetzt hat, nachdem es angehalten wurde.

Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht. Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMESUSPEND
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

| Wert                                                                                                                                                                                                                                           | Bedeutung                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**PBT \_ Apmresumesuspend**</dt> <dt>7 (0x7)</dt> </dl> | Ereignis Bezeichner.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Bleiben muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung kann dieses Ereignis nur empfangen, wenn Sie das [PBT \_ apmsuspend](pbt-apmsuspend.md) -Ereignis empfangen hat, bevor der Computer angehalten wurde. Andernfalls empfängt die Anwendung ein [PBT \_ apmresumecritical](pbt-apmresumecritical.md) -Ereignis.

Wenn das System aufgrund der Benutzeraktivität reaktiviert wird (z. b. durch Drücken der Schaltfläche "einschalten") oder wenn das System eine Benutzerinteraktion in der physischen Konsole (z. b. Maus-oder Tastatureingabe) erkennt, nachdem das unbeaufsichtigte Einschalten erfolgt ist, überträgt das System zunächst das [PBT \_ apmresumeautomatic](pbt-apmresumeautomatic.md) -Ereignis und überträgt es dann übermittelt \_ Außerdem schaltet das System die Anzeige ein. Die Anwendung sollte die Dateien erneut öffnen, die Sie geschlossen haben, als das System in den Standbymodus gewechselt und die Benutzereingaben vorbereitet

Wenn das System aufgrund eines externen Aktivierungs Signals (Remote Wake) aktiviert wird, überträgt das System nur das [PBT \_ apmresumeautomatic](pbt-apmresumeautomatic.md) -Ereignis. Das PBT \_ apmresumesuspend-Ereignis wird nicht gesendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[System Aktivierungs Ereignisse](system-wake-up-events.md)
</dt> <dt>

[Energie Verwaltungs Ereignisse](power-management-events.md)
</dt> <dt>

[PBT \_ apmsuspend](pbt-apmsuspend.md)
</dt> <dt>

[PBT \_ apmresumecritical](pbt-apmresumecritical.md)
</dt> <dt>

[**WM- \_ powerbroadcast**](wm-powerbroadcast.md)
</dt> </dl>

 

 




