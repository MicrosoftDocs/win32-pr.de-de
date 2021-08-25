---
description: Benachrichtigt Anwendungen, dass der Computer in einen angehaltenen Zustand übergehen soll.
ms.assetid: 61b177a0-4cff-4740-bed8-a46c06c43be8
title: PBT_APMSUSPEND -Ereignis (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb3634765e6c0f863beb0c7a1c16af29cadae18ef14796e9ef01a0c8edec36a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961670"
---
# <a name="pbt_apmsuspend-event"></a>\_PBT-APMSUSPEND-Ereignis

Benachrichtigt Anwendungen, dass der Computer in einen angehaltenen Zustand übergehen soll. Dieses Ereignis wird in der Regel übertragen, wenn alle Anwendungen und installierbaren Treiber **TRUE** an ein früheres [ \_ PBT-APMQUERYSUSPEND-Ereignis](pbt-apmquerysuspend.md) zurückgegeben haben.

Ein Fenster empfängt dieses Ereignis über die [**WM \_ POWERBROADCAST-Nachricht.**](wm-powerbroadcast.md) Die *Parameter wParam* und *lParam* werden wie folgt festgelegt.


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

*Hwnd* 
</dt> <dd>

Ein Handle für fenster.

</dd> <dt>*uMsg*</dt> <dd> 

| Wert                                                                                                                                                                                                                                                                   | Bedeutung                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Nachrichtenbezeichner.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Wert                                                                                                                                                                                                                         | Bedeutung                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <dt>**PBT \_ APMSUSPEND**</dt> <dt>4 (0x4)</dt> </dl> | Ereignisbezeichner.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reserviert; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Eine Anwendung sollte dieses Ereignis verarbeiten, indem alle Aufgaben abgeschlossen werden, die zum Speichern von Daten erforderlich sind.

Das System lässt ca. zwei Sekunden zu, damit eine Anwendung diese Benachrichtigung verarbeitet. Wenn eine Anwendung weiterhin Vorgänge ausführt, nachdem die Zuteilung abgelaufen ist, kann das System die Anwendung unterbrechen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>WinUser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Kriterien für den Systemmodus](system-sleep-criteria.md)
</dt> <dt>

[Systemreaktivierungsereignisse](system-wake-up-events.md)
</dt> <dt>

[Energieverwaltungsereignisse](power-management-events.md)
</dt> <dt>

[PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md)
</dt> <dt>

[**SetSystemPowerState**](/windows/desktop/api/WinBase/nf-winbase-setsystempowerstate)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




