---
description: Benachrichtigt Anwendungen, dass der Computer im Begriff ist, in einen angehaltenen Zustand zu wechseln.
ms.assetid: 61b177a0-4cff-4740-bed8-a46c06c43be8
title: PBT_APMSUSPEND-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6982e00565329c85e06765879b9b72b07fe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216025"
---
# <a name="pbt_apmsuspend-event"></a>PBT \_ apmsuspend-Ereignis

Benachrichtigt Anwendungen, dass der Computer im Begriff ist, in einen angehaltenen Zustand zu wechseln. Dieses Ereignis wird in der Regel übertragen, wenn alle Anwendungen und installierbaren Treiber **true** für ein vorheriges [PBT \_ apmquerysuspend](pbt-apmquerysuspend.md) -Ereignis zurückgegeben haben.

Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht. Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMSUSPEND
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

| Wert                                                                                                                                                                                                                         | Bedeutung                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <dt>**PBT \_ Apmsuspend**</dt> <dt>4 (0x4)</dt> </dl> | Ereignis Bezeichner.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Bleiben muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung sollte dieses Ereignis verarbeiten, indem alle Aufgaben abgeschlossen werden, die zum Speichern der Daten erforderlich sind.

Das System lässt zu, dass eine Anwendung diese Benachrichtigung in ungefähr zwei Sekunden verarbeitet. Wenn eine Anwendung nach Ablauf der Zeitzuweisung noch Vorgänge ausführt, kann das System die Anwendung unterbrechen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[System Energiespar Kriterien](system-sleep-criteria.md)
</dt> <dt>

[System Aktivierungs Ereignisse](system-wake-up-events.md)
</dt> <dt>

[Energie Verwaltungs Ereignisse](power-management-events.md)
</dt> <dt>

[PBT \_ apmquerysuspend](pbt-apmquerysuspend.md)
</dt> <dt>

[**SetSystemPowerState**](/windows/desktop/api/WinBase/nf-winbase-setsystempowerstate)
</dt> <dt>

[**WM- \_ powerbroadcast**](wm-powerbroadcast.md)
</dt> </dl>

 

 




