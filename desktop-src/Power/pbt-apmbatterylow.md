---
description: Benachrichtigt Anwendungen, dass der Akku Strom niedrig ist.
ms.assetid: ef24b8cf-d801-4452-a03c-3f2bdbdd7e5d
title: PBT_APMBATTERYLOW-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64884f9bb01e37883e1be61b2de88862e8b119fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358890"
---
# <a name="pbt_apmbatterylow-event"></a>PBT \_ apmbatterylow-Ereignis

\[PBT \_ apmbatterylow ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Die Unterstützung für dieses Ereignis wurde in Windows Vista entfernt. Verwenden Sie stattdessen [PBT \_ apmpowerstatuschange](pbt-apmpowerstatuschange.md) .\]

Benachrichtigt Anwendungen, dass der Akku Strom niedrig ist.

Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht. Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMBATTERYLOW
            LPARAM lParam); // zero
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Ein Handle für das Fenster.

</dd> <dt>*Umschlag*</dt> <dd> 

| Wert                                                                                                                                                                                                                                                                   | Bedeutung                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ Powerbroadcast**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Nachrichten-ID.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Wert                                                                                                                                                                                                                                  | Bedeutung                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMBATTERYLOW"></span><span id="pbt_apmbatterylow"></span><dl> <dt>**PBT \_ Apmbatterylow**</dt> <dt>9 (0x9)</dt> </dl> | Ereignis Bezeichner.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reserviert, muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird gesendet, wenn das APM-BIOS eines Systems eine apm-Akku Benachrichtigung mit geringer Leistung signalisiert. Da einige APM-BIOS-Implementierungen keine Benachrichtigungen bereitstellen, wenn Akkus niedrig sind, wird dieses Ereignis möglicherweise nie auf einigen Computern übertragen.

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

[Energie Verwaltungs Ereignisse](power-management-events.md)
</dt> <dt>

[**WM- \_ powerbroadcast**](wm-powerbroadcast.md)
</dt> </dl>

 

 




