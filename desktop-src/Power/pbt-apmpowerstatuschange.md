---
description: Benachrichtigt Anwendungen über eine Änderung des Energiestatus des Computers, z. b. einen Wechsel von Akkuleistung zu a/C.
ms.assetid: dc56fee3-e0df-4f8e-8a41-92460279280a
title: PBT_APMPOWERSTATUSCHANGE-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ed67f7ba064d44614196da4190ce18a996bd5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216026"
---
# <a name="pbt_apmpowerstatuschange-event"></a>PBT \_ apmpowerstatuschange-Ereignis

Benachrichtigt Anwendungen über eine Änderung des Energiestatus des Computers, z. b. einen Wechsel von Akkuleistung zu a/C. Das System leitet dieses Ereignis auch dann weiter, wenn die verbleibende Akkuleistung unter einen vom Benutzer festgelegten Wert sinkt oder sich um einen angegebenen Prozentsatz ändert.

Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht. Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMPOWERSTATUSCHANGE
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

| Wert                                                                                                                                                                                                                                                        | Bedeutung                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <dt>**PBT \_ Apmpowerstatuschange**</dt> <dt>10 (0xa)</dt> </dl> | Ereignis Bezeichner.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Bleiben muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung sollte dieses Ereignis verarbeiten, indem Sie die [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) -Funktion aufrufen, um den aktuellen Energiestatus des Computers abzurufen. Insbesondere sollte die Anwendung die Elemente " **ACLineStatus**", " **BatteryFlag**", " **batterylifetime**" und " **batterylifeprozent** " der [**System \_ Energie \_ Status**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) -Struktur auf Änderungen überprüfen. Dieses Ereignis kann auftreten, wenn die Akku Lebensdauer weniger als 5 Minuten sinkt oder wenn der Prozentsatz der Akku Lebensdauer unter 10 Prozent sinkt oder wenn sich die Akku Lebensdauer um 3 Prozent ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[System Energie Status](system-power-status.md)
</dt> <dt>

[Energie Verwaltungs Ereignisse](power-management-events.md)
</dt> <dt>

[**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus)
</dt> <dt>

[**System \_ Energie \_ Status**](/windows/desktop/api/Winbase/ns-winbase-system_power_status)
</dt> <dt>

[**WM- \_ powerbroadcast**](wm-powerbroadcast.md)
</dt> </dl>

 

 




