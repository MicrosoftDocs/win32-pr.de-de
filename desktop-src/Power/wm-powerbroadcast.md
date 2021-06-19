---
description: Benachrichtigt Anwendungen, dass ein Energieverwaltungsereignis aufgetreten ist.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: WM_POWERBROADCAST-Nachricht (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b205a146b731bdf8cf9adc1563621232c24c10b4
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396505"
---
# <a name="wm_powerbroadcast-message"></a>WM \_ POWERBROADCAST-Nachricht

Benachrichtigt Anwendungen, dass ein Energieverwaltungsereignis aufgetreten ist.

Ein Fenster empfängt diese Meldung über seine **WindowProc-Funktion.**


```C++
LRESULT CALLBACK WindowProc(
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWERBROADCAST
  WPARAM wParam,  // power-management event
  LPARAM lParam   // function-specific data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Ein Handle für fenster.

</dd> <dt>
  
*uMsg*
</dt> <dd> 

| Wert                                                                                                                                                                                                                                          | Bedeutung                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>–WM \_ POWERBROADCAST**</dt> <dt>536 (0x218)</dt> </dl> | Nachrichtenbezeichner.<br/> |



 

</dd> <dt>

*wParam* 
</dt> <dd>

Das Energieverwaltungsereignis. Dieser Parameter kann einer der folgenden Ereignisbezeichner sein.



| Ereignis                                                                                                                                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <dt>**[PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xA)</dt> </dl> | Der Energiestatus wurde geändert.<br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**[PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt> </dl>        | Der Vorgang wird automatisch von einem Energiesparzustand aus fortsetzen. Diese Meldung wird jedes Mal gesendet, wenn das System fortgesetzt wird.<br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**[PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt> </dl>                  | Der Vorgang wird von einem Energiesparzustand aus fortsetzen. Diese Meldung wird nach [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) gesendet, wenn der Fortsetzen durch Benutzereingabe ausgelöst wird, z. B. durch Drücken einer Taste.<br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <dt>**[PBT \_ APMSUSPEND](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt> </dl>                                          | Das System hält den Vorgang an.<br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**[PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt> </dl>   | Ein Energieeinstellungsänderungsereignis wurde empfangen. <br/>                                                                                                                                                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Die ereignisspezifischen Daten. Für die meisten Ereignisse ist dieser Parameter reserviert und wird nicht verwendet.

Wenn der *wParam-Parameter* [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md)ist, ist der *lParam-Parameter* ein Zeiger auf eine [**POWERBROADCAST \_ SETTING-Struktur.**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte **TRUE** zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Das System sendet immer dann eine [PBT-APMRESUMEAUTOMATIC-Nachricht, \_ ](pbt-apmresumeautomatic.md) wenn das System fortgesetzt wird. Wenn das System als Reaktion auf Benutzereingaben wie das Drücken einer Taste fortgesetzt wird, sendet das System nach dem Senden von PBT APMRESUMEAUTOMATIC auch eine **PBT-APMRESUMESUSPEND-Nachricht. \_** \_

**WM \_ POWERBROADCAST-Nachrichten** unterscheiden nicht zwischen verschiedenen Zuständen mit geringer Leistung. Eine Anwendung kann nur feststellen, dass das System in einen Energiesparzustand übergeht oder wieder aufgenommen wurde. der spezifische Energiezustand kann nicht bestimmt werden. Das System zeichnet Details zu Energiezustandsübergängen im Windows-Systemereignisprotokoll auf.

Um zu verhindern, dass das System in Windows Vista in einen Energiesparzustand übergehen kann, muss eine Anwendung [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) aufrufen, um das System darüber zu informieren, dass es verwendet wird.

Die folgenden Meldungen werden auf keinem der im Abschnitt Anforderungen angegebenen Betriebssysteme unterstützt:

- PBT_APMQUERYSTANDBY  
- PBT_APMQUERYSTANDBYFAILED  
- PBT_APMSTANDBY  
- PBT_APMRESUMESTANDBY  

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>WinUser.h (windows.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WM \_ POWERBROADCAST Messages](wm-powerbroadcast-messages.md)
</dt> <dt>

[Energieverwaltungsmeldungen](power-management-messages.md)
</dt> </dl>

 

 




