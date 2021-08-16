---
description: Änderungsereignis der Energieeinstellung, das mit einer WM \_ POWERBROADCAST-Fenstermeldung oder in einem HandlerEx-Benachrichtigungsrückruf für Dienste gesendet wird.
ms.assetid: 0bcadb85-47c5-48a9-b3f9-f0a1ca60b503
title: PBT_POWERSETTINGCHANGE -Ereignis (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e50a793e22cce7b0720fa7a020fb3d2d1b6e464ef619a0cf5c43ca256748d69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961690"
---
# <a name="pbt_powersettingchange-event"></a>PBT \_ POWERSETTINGCHANGE-Ereignis

Änderungsereignis der Energieeinstellung, das mit einer [**WM \_ POWERBROADCAST-Fenstermeldung**](wm-powerbroadcast.md) oder in einem [**HandlerEx-Benachrichtigungsrückruf**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) für Dienste gesendet wird.


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

*Hwnd* 
</dt> <dd>

Ein Handle für fenster.

</dd> <dt>*uMsg*</dt> <dd> 

| Wert                                                                                                                                                                                                                                                                   | Bedeutung                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt> </dl> | Nachrichtenbezeichner.<br/> |



 

</dd> <dt>*wParam*</dt> <dd> 

| Wert                                                                                                                                                                                                                                                        | Bedeutung                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**PBT \_ POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt> </dl> | Ereignisbezeichner.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**POWERBROADCAST \_ SETTING-Struktur.**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>WinUser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Energieverwaltungsereignisse](power-management-events.md)
</dt> <dt>

[**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> <dt>

[**\_POWERBROADCAST-EINSTELLUNG**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
</dt> </dl>

 

