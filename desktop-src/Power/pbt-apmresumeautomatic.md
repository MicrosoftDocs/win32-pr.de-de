---
description: Benachrichtigt Anwendungen, dass das System aus dem Standbymodus oder Ruhezustand wieder aufgenommen wird. Dieses Ereignis wird jedes Mal übermittelt, wenn das System fortgesetzt wird, und gibt nicht an, ob ein Benutzer vorhanden ist.
ms.assetid: cd331f79-b64d-479e-aea8-5118ccc87224
title: PBT_APMRESUMEAUTOMATIC-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a481dee356c85b3831fcace0c1ff127b0b276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865071"
---
# <a name="pbt_apmresumeautomatic-event"></a>PBT \_ apmresumeautomatic-Ereignis

Benachrichtigt Anwendungen, dass das System aus dem Standbymodus oder Ruhezustand wieder aufgenommen wird. Dieses Ereignis wird jedes Mal übermittelt, wenn das System fortgesetzt wird, und gibt nicht an, ob ein Benutzer vorhanden ist.

Ein Fenster empfängt dieses Ereignis über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht. Die *wParam* -Parameter und die *LPARAM* -Parameter werden wie folgt festgelegt.

> [!Note]  
> Wenn das System in Windows 10, Version 1507, oder höher, nur wieder aus dem Standbymodus wechselt, um sofort in den Ruhezustand zu wechseln, wird dieses Ereignis nicht übermittelt. In diesem Fall wird keine [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht gesendet.

 


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

*HWND* 
</dt> <dd>

Ein Handle für Fenster.

</dd> <dt>*Umschlag*</dt> <dd> 

| Wert                                                                                                                                                                                                                                                                   | Bedeutung                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ Powerbroadcast**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Nachrichten-ID.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Wert                                                                                                                                                                                                                                                   | Bedeutung                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**PBT \_ Apmresumeautomatic**</dt> <dt>18 (0x12)</dt> </dl> | Ereignis Bezeichner.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Bleiben muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn das System nach der Übertragung von PBT \_ apmresumeautomatic eine Benutzeraktivität erkennt, sendet es ein [PBT \_ apmresumesuspend](pbt-apmresumesuspend.md) -Ereignis, um Anwendungen mitzuteilen, dass die vollständige Interaktion mit dem Benutzer fortgesetzt werden kann.

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

[PBT \_ apmresumesuspend](pbt-apmresumesuspend.md)
</dt> <dt>

[**WM- \_ powerbroadcast**](wm-powerbroadcast.md)
</dt> </dl>

 

 




