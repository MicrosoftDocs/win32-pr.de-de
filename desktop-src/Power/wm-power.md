---
description: Benachrichtigt Anwendungen, dass das System, üblicherweise ein Akku gesteuerter PC, im Begriff ist, in einen angehaltenen Modus zu wechseln.
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: WM_POWER Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53fd165ee1cefe8970f85daea04b931a673b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359036"
---
# <a name="wm_power-message"></a>\_Power Message-WM

Benachrichtigt Anwendungen, dass das System, üblicherweise ein Akku gesteuerter PC, im Begriff ist, in einen angehaltenen Modus zu wechseln.

> [!Note]  
> Die **WM- \_ Strom** Meldung ist veraltet. Sie wird nur für die Kompatibilität mit 16-Bit-Windows-basierten Anwendungen bereitgestellt. Anwendungen sollten die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht verwenden.

 

Ein Fenster empfängt diese Meldung über seine **WindowProc** -Funktion.


```C++
LRESULT CALLBACK WindowProc
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWER
  WPARAM wParam,  // power-event notification
  LPARAM lParam   // not used
); 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Ein Handle für Fenster.

</dd> <dt>

*Umschlag* 
</dt> <dd>

Der **WM- \_ Strom** Nachrichten Bezeichner.

</dd> <dt>

*wParam* 
</dt> <dd>

Die Strom Ereignis Benachrichtigung. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <dt>**PWR \_ criticalresume**</dt> </dl> | Gibt an, dass das System den Vorgang nach dem Wechsel in den Modus "angehalten" fortsetzt, ohne zuerst eine **PWR \_ suspendrequest** -Benachrichtigungs Meldung an die Anwendung zu senden Eine Anwendung sollte alle notwendigen Wiederherstellungs Aktionen ausführen.<br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <dt>**PWR \_ suspendrequest**</dt> </dl> | Gibt an, dass das System in den Modus "angehalten" versetzt wird.<br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <dt>**PWR \_ suspendresume**</dt> </dl>    | Gibt an, dass das System den Vorgang fortsetzt, nachdem der angehaltene Modus in den normalen Zustand versetzt wurde. das System überträgt eine **PWR \_ suspendrequest** -Benachrichtigungs Meldung an die Anwendung, bevor das System angehalten wurde. Eine Anwendung sollte alle notwendigen Wiederherstellungs Aktionen ausführen.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Wert, der von einer Anwendung zurückgegeben wird, hängt vom Wert des *wParam* -Parameters ab. Wenn " *wParam* " **PWR \_ suspendrequest** ist, kann der Rückgabewert **PWR \_ nicht** verhindern, dass das System in den Zustand "angehalten" wechselt; andernfalls ist es **PWR \_ OK**. Wenn " *wParam* " **PWR \_ suspendresume** oder **PWR \_ criticalresume** ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Diese Meldung wird nur an eine Anwendung übertragen, die auf einem System ausgeführt wird, das der Spezifikation "Basic Input/Output System (FIM) für die erweiterte Energie Verwaltung (Basic Input/Output System)" entspricht. Die Meldung wird vom Energie Verwaltungs Treiber an jedes Fenster gesendet, das von der **EnumWindows** -Funktion zurückgegeben wird.

Der angehaltene Modus ist der Status, in dem die größte Menge an Energieeinsparungen auftritt, aber alle operativen Daten und Parameter bleiben erhalten. RAM-Inhalte (Random Access Memory) werden beibehalten, aber viele Geräte sind wahrscheinlich ausgeschaltet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WM- \_ powerbroadcast**](wm-powerbroadcast.md)
</dt> </dl>

 

 




