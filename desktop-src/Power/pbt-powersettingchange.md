---
description: Das Energie Einstellungs Änderungs Ereignis wurde mit einer WM- \_ powerbroadcast-Fenster Meldung oder in einem handlerex-Benachrichtigungs Rückruf für Dienste gesendet.
ms.assetid: 0bcadb85-47c5-48a9-b3f9-f0a1ca60b503
title: PBT_POWERSETTINGCHANGE-Ereignis (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f38486d2e5cce1cfe541468e548e92353c9837
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865068"
---
# <a name="pbt_powersettingchange-event"></a>PBT- \_ powersettingchange-Ereignis

Das Energie Einstellungs Änderungs Ereignis wurde mit einer [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Fenster Meldung oder in einem [**handlerex**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) -Benachrichtigungs Rückruf für Dienste gesendet.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_POWERSETTINGCHANGE
            LPARAM lParam); // Pointer to POWERBROADCAST_SETTING
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
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**PBT \_ Powersettingchange**</dt> <dt>32787 (0x8013)</dt> </dl> | Ereignis Bezeichner.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**powerbroadcast- \_ Einstellungs**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Energie Verwaltungs Ereignisse](power-management-events.md)
</dt> <dt>

[**Handlerex**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)
</dt> <dt>

[**WM- \_ powerbroadcast**](wm-powerbroadcast.md)
</dt> <dt>

[**powerbroadcast- \_ Einstellung**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
</dt> </dl>

 

