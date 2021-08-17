---
description: Fordert die Berechtigung zum Aussetzen des Computers an. Eine Anwendung, die die Erlaubnis erteilt, muss vor dem Beenden Vorbereitungen für den Standbymodus treffen.
ms.assetid: 83cb0fdc-437e-4d03-87f0-6a416281c0d5
title: PBT_APMQUERYSUSPEND (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e8063ce68a88c8a39cb6f9ab8a4f559aed41242eaae25fab616ace8793b16ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143383"
---
# <a name="pbt_apmquerysuspend-event"></a>PBT \_ APMQUERYSUSPEND-Ereignis

\[PBT APMQUERYSUSPEND steht für die Verwendung in den im Abschnitt Anforderungen \_ angegebenen Betriebssystemen zur Verfügung. Die Unterstützung für dieses Ereignis wurde in Windows Vista entfernt. Verwenden [**Sie stattdessen SetThreadExecutionState.**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate)\]

Fordert die Berechtigung zum Aussetzen des Computers an. Eine Anwendung, die die Erlaubnis erteilt, muss vor dem Beenden Vorbereitungen für den Standbymodus treffen.

Ein Fenster empfängt dieses Ereignis über die [**WM \_ POWERBROADCAST-Nachricht.**](wm-powerbroadcast.md) Die *Parameter wParam* *und lParam* werden wie folgt festgelegt.


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPEND
            LPARAM lParam); // action flags
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

| Wert                                                                                                                                                                                                                                        | Bedeutung                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPEND"></span><span id="pbt_apmquerysuspend"></span><dl> <dt>**PBT \_ APMQUERYSUSPEND**</dt> <dt>0 (0x0)</dt> </dl> | Ereignisbezeichner.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Die Aktionsflags. Wenn Bit 0 1 ist, kann die Anwendung den Benutzer auffordern, anweisungen zur Vorbereitung auf das Aussetzen zu erhalten. Andernfalls muss die Anwendung ohne Benutzerinteraktion vorbereitet werden. Alle anderen Bitwerte sind reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie **TRUE zurück,** um der Anforderung das Aussetzen zu gewähren. Um die Anforderung zu verweigern, geben Sie **BROADCAST \_ QUERY \_ DENY zurück.**

## <a name="remarks"></a>Hinweise

Eine Anwendung sollte dieses Ereignis so schnell wie möglich verarbeiten. Die Anwendung kann den Benutzer nur dann zur Eingabe von Anweisungen zur Vorbereitung auf die Unterbrechung auffordern, wenn Bit 0 im *Flags-Parameter* festgelegt ist. Wenn diese Meldung jedoch ausgegeben wird, weil der Benutzer den Laptop schließt, kann der Benutzer nicht dazu aufgefordert werden. Anwendungen sollten darauf achten, dass der Benutzer ein bestimmtes Verhalten erwartet, wenn er den Laptop schließt oder den Netzschalter drückt und den Übergang erfolgreich ermöglicht.

Das System erlaubt einer Anwendung ungefähr 20 Sekunden, die [**WM \_ POWERBROADCAST-Nachricht**](wm-powerbroadcast.md) zu entfernen, die das PBT APMQUERYSUSPEND-Ereignis aus der Nachrichtenwarteschlange der Anwendung \_ sendet. Wenn eine Anwendung die Nachricht nicht in weniger als 20 Sekunden aus der Warteschlange entfernt, geht das System davon aus, dass sich die Anwendung in einem nicht reaktionsschnellen Zustand befindet und dass die Anwendung der Sleepanforderung zu stimmt. Bei Anwendungen, die ihre Nachrichtenwarteschlangen nicht verarbeiten, werden ihre Vorgänge möglicherweise unterbrochen. Nachdem die Nachricht aus der Nachrichtenwarteschlange entfernt wurde, kann eine Anwendung so viel Zeit wie nötig benötigen, um alle erforderlichen Vorgänge durchzuführen, bevor sie in den Ruhezustand eintritt. Alle Vorgänge, die länger als 20 Sekunden dauern können, sollten zu diesem Zeitpunkt ausgeführt werden, da das System nur 20 Sekunden für Vorgänge während der [PBT \_ APMSUSPEND-Verarbeitung](pbt-apmsuspend.md) zulässt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                                    |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                                           |
| Header<br/>                   | <dl> <dt>WinUser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systemreaktivingsereignisse](system-wake-up-events.md)
</dt> <dt>

[Energieverwaltungsereignisse](power-management-events.md)
</dt> <dt>

[PBT \_ APMSUSPEND](pbt-apmsuspend.md)
</dt> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




