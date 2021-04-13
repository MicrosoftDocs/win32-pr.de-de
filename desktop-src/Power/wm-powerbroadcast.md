---
description: Benachrichtigt Anwendungen, dass ein Energie Verwaltungs Ereignis aufgetreten ist.
ms.assetid: 46452909-ac0e-4c06-8542-0b94d00e6556
title: WM_POWERBROADCAST Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f1b273462d8de27c19d715836d168ab8bf8c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529096"
---
# <a name="wm_powerbroadcast-message"></a>WM- \_ powerbroadcast-Meldung

Benachrichtigt Anwendungen, dass ein Energie Verwaltungs Ereignis aufgetreten ist.

Ein Fenster empfängt diese Meldung über seine **WindowProc** -Funktion.


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

*HWND* 
</dt> <dd>

Ein Handle für Fenster.

</dd> <dt>*Umschlag*</dt> <dd> 

| Wert                                                                                                                                                                                                                                          | Bedeutung                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <dt>* * * * WM \_ Powerbroadcast * *</dt> * * * <dt>536 (0x218)</dt> </dl> | Nachrichten-ID.<br/> |



 

</dd> <dt>

*wParam* 
</dt> <dd>

Das Energie Verwaltungs Ereignis. Dieser Parameter kann einem der folgenden Ereignis Bezeichner entsprechen.



| Ereignis                                                                                                                                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <dt>**[PBT \_ Apmpowerstatuschange](pbt-apmpowerstatuschange.md)**</dt> <dt>10 (0xa)</dt> </dl> | Der Energiestatus hat sich geändert.<br/>                                                                                                                                                                        |
| <span id="PBT_APMRESUMEAUTOMATIC"></span><span id="pbt_apmresumeautomatic"></span><dl> <dt>**[PBT \_ Apmresumeautomatic](pbt-apmresumeautomatic.md)**</dt> <dt>18 (0x12)</dt> </dl>        | Der Vorgang wird automatisch von einem Energiespar Zustand fortgesetzt. Diese Meldung wird jedes Mal gesendet, wenn das System fortgesetzt wird.<br/>                                                                                  |
| <span id="PBT_APMRESUMESUSPEND"></span><span id="pbt_apmresumesuspend"></span><dl> <dt>**[PBT \_ Apmresumesuspend](pbt-apmresumesuspend.md)**</dt> <dt>7 (0x7)</dt> </dl>                  | Der Vorgang wird in einem Energiespar Zustand fortgesetzt. Diese Nachricht wird nach [PBT \_ apmresumeautomatic](pbt-apmresumeautomatic.md) gesendet, wenn die Fortsetzung durch Benutzereingaben ausgelöst wird, z. b. durch Drücken einer Taste.<br/> |
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <dt>**[PBT \_ Apmsuspend](pbt-apmsuspend.md)**</dt> <dt>4 (0x4)</dt> </dl>                                          | Der Vorgang wird vom System angehalten.<br/>                                                                                                                                                                  |
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <dt>**[PBT \_ Powersettingchange](pbt-powersettingchange.md)**</dt> <dt>32787 (0x8013)</dt> </dl>   | Ein Energie Einstellungs Änderungs Ereignis wurde empfangen. <br/>                                                                                                                                                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Die ereignisspezifischen Daten. Bei den meisten Ereignissen ist dieser Parameter reserviert und wird nicht verwendet.

Wenn der *wParam* -Parameter [PBT \_ powersettingchange](pbt-powersettingchange.md)ist, ist der *LPARAM* -Parameter ein Zeiger auf eine [**powerbroadcast- \_ Einstellungs**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte **true** zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Das System sendet immer dann eine [PBT \_ apmresumeautomatic](pbt-apmresumeautomatic.md) -Meldung, wenn das System fortgesetzt wird. Wenn das System als Reaktion auf Benutzereingaben (z. b. Drücken einer Taste) fortgesetzt wird, sendet das System nach dem Senden von PBT apmresumeautomatic auch eine **PBT \_ apmresumesuspend** -Nachricht \_ .

**WM \_ Powerbroadcast** -Nachrichten unterscheiden sich nicht zwischen unterschiedlichen Zuständen mit niedrigem Energiezustand. Eine Anwendung kann nur bestimmen, ob das System in den Energiesparmodus wechselt oder ihn wieder aufgenommen hat. der jeweilige Energiezustand kann nicht ermittelt werden. Das System zeichnet Details zu Energie Zustands Übergängen im Windows-System Ereignisprotokoll auf.

Um zu verhindern, dass das System in Windows Vista in einen Energiespar Zustand übergeht, muss eine Anwendung [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) aufrufen, um das System zu informieren, dass es verwendet wird.

Die folgenden Meldungen werden von keinem der im Abschnitt "Anforderungen" angegebenen Betriebssysteme unterstützt:

- PBT_APMQUERYSTANDBY  
- PBT_APMQUERYSTANDBYFAILED  
- PBT_APMSTANDBY  
- PBT_APMRESUMESTANDBY  

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WM- \_ powerbroadcast-Meldungen](wm-powerbroadcast-messages.md)
</dt> <dt>

[Energie Verwaltungs Meldungen](power-management-messages.md)
</dt> </dl>

 

 




