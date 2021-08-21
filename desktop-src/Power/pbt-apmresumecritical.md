---
description: Benachrichtigt Anwendungen, dass der Vorgang vom System fortgesetzt wurde.
ms.assetid: f2997905-26c9-4884-ae79-64df5ce6bc55
title: PBT_APMRESUMECRITICAL-Ereignis (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13214a97e99954d0649df0647bdf6ee3823b91926c0f2f2dc1212fa780a7b6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961707"
---
# <a name="pbt_apmresumecritical-event"></a>\_PBT-APMRESUMECRITICAL-Ereignis

\[PBT \_ APMRESUMECRITICAL ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Die Unterstützung für dieses Ereignis wurde in Windows Vista entfernt. Verwenden Sie stattdessen [PBT \_ APMRESUMEAUTOMATIC.](pbt-apmresumeautomatic.md)\]

Benachrichtigt Anwendungen, dass der Vorgang vom System fortgesetzt wurde. Dieses Ereignis kann angeben, dass einige oder alle Anwendungen kein [ \_ PBT-APMSUSPEND-Ereignis](pbt-apmsuspend.md) empfangen haben. Dieses Ereignis kann z. B. nach einer kritischen Unterbrechung übertragen werden, die durch einen ausfallbedingten Akku verursacht wird.

Ein Fenster empfängt dieses Ereignis über die [**WM \_ POWERBROADCAST-Nachricht.**](wm-powerbroadcast.md) Die *Parameter wParam* und *lParam* werden wie folgt festgelegt.


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

*Hwnd* 
</dt> <dd>

Ein Handle für fenster.

</dd> <dt>*uMsg*</dt> <dd> 

| Wert                                                                                                                                                                                                                                                                   | Bedeutung                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Nachrichtenbezeichner.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Wert                                                                                                                                                                                                                                              | Bedeutung                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMECRITICAL"></span><span id="pbt_apmresumecritical"></span><dl> <dt>**PBT \_ APMRESUMECRITICAL**</dt> <dt>6 (0x6)</dt> </dl> | Ereignisbezeichner.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reserviert; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Da eine Notabschaltung ohne vorherige Benachrichtigung aufgetreten ist, sind zuvor verfügbare Ressourcen und Daten möglicherweise nicht vorhanden, wenn die Anwendung dieses Ereignis empfängt. Die Anwendung sollte versuchen, ihren Status im Rahmen ihrer Möglichkeiten optimal wiederherzustellen. Während einer kritischen Unterbrechung behält das System den Zustand des DRAM und der lokalen Festplatten bei, behält jedoch möglicherweise keine Nettoverbindungen bei. Eine Anwendung muss möglicherweise Maßnahmen in Bezug auf Dateien ergreifen, die vor dem kritischen Stopp im Netzwerk geöffnet waren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                                    |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                                           |
| Header<br/>                   | <dl> <dt>WinUser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Systemreaktivierungsereignisse](system-wake-up-events.md)
</dt> <dt>

[Energieverwaltungsereignisse](power-management-events.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




