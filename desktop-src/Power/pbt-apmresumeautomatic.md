---
description: Benachrichtigt Anwendungen, dass das System aus dem Ruhezustand oder Ruhezustand wieder besteht. Dieses Ereignis wird jedes Mal übermittelt, wenn das System fortgesetzt wird, und gibt nicht an, ob ein Benutzer vorhanden ist.
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: PBT_APMRESUMEAUTOMATIC -Ereignis (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e66fcd2201e9fb3c4feeb135843e92a350303b89a5c5045836428b9a326a30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143343"
---
# <a name="pbt_apmresumeautomatic-event"></a>PBT \_ APMRESUMEAUTOMATIC-Ereignis

Benachrichtigt Anwendungen, dass das System aus dem Ruhezustand oder Ruhezustand wieder besteht. Dieses Ereignis wird jedes Mal übermittelt, wenn das System fortgesetzt wird, und gibt nicht an, ob ein Benutzer vorhanden ist.

Ein Fenster empfängt dieses Ereignis über die [**WM \_ POWERBROADCAST-Nachricht.**](wm-powerbroadcast.md) Die *Parameter wParam* *und lParam* werden wie folgt festgelegt.

> [!Note]  
> In Windows 10 Systemen der Version 1507 oder höher wird dieses Ereignis nicht übermittelt, wenn das System nur aus dem Ruhezustand wieder in den Ruhezustand überträgt. In [**diesem Fall wird keine WM \_ POWERBROADCAST-Nachricht**](wm-powerbroadcast.md) gesendet.

 


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMRESUMEAUTOMATIC
            LPARAM lParam); // zero
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Ein Handle für ein Fenster.

</dd> <dt>*uMsg*</dt> <dd> 

| Wert                                                                                                                                                                                                                                                                   | Bedeutung                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Nachrichtenbezeichner.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Wert                                                                                                                                                                                                                                                   | Bedeutung                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**PBT \_ APMRESUMEAUTOMATIC**</dt> <dt>18 (0x12)</dt> </dl> | Ereignisbezeichner.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Reserviert; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Wenn das System nach der Übertragung von PBT APMRESUMEAUTOMATIC eine Benutzeraktivität erkennt, sendet es ein \_ [PBT \_ APMRESUMESUSPEND-Ereignis,](pbt-apmresumesuspend.md) um Anwendungen darüber zu informieren, dass sie die vollständige Interaktion mit dem Benutzer fortsetzen können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>WinUser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systemreaktivingsereignisse](system-wake-up-events.md)
</dt> <dt>

[Energieverwaltungsereignisse](power-management-events.md)
</dt> <dt>

[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




