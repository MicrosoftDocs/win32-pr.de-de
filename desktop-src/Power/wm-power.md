---
description: Benachrichtigt Anwendungen darüber, dass das System , in der Regel ein akkugestützter Personalcomputer, in den angehaltenen Modus versetzt wird.
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: WM_POWER-Nachricht (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fd525b4bf229fdb04dac4c1d1492a52dad44317344f58a2f0807ba9afbdc962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143183"
---
# <a name="wm_power-message"></a>WM \_ POWER-Nachricht

Benachrichtigt Anwendungen darüber, dass das System , in der Regel ein akkugestützter Personalcomputer, in den angehaltenen Modus versetzt wird.

> [!Note]  
> Die **WM \_ POWER-Nachricht** ist veraltet. Sie wird nur aus Gründen der Kompatibilität mit 16-Bit-Windows-basierten Anwendungen bereitgestellt. Anwendungen sollten die [**WM \_ POWERBROADCAST-Nachricht**](wm-powerbroadcast.md) verwenden.

 

Ein Fenster empfängt diese Meldung über seine **WindowProc-Funktion.**


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

*Hwnd* 
</dt> <dd>

Ein Handle für fenster.

</dd> <dt>

*uMsg* 
</dt> <dd>

Der **WM POWER-Nachrichtenbezeichner. \_**

</dd> <dt>

*wParam* 
</dt> <dd>

Die Energieereignisbenachrichtigung. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <dt>**PWR \_ CRITICALRESUME**</dt> </dl> | Gibt an, dass das System den Vorgang nach dem Wechseln in den angehaltenen Modus fortsetzen kann, ohne zuvor eine **PWR SUSPENDREQUEST-Benachrichtigungsmeldung \_** an die Anwendung zu senden. Eine Anwendung sollte alle erforderlichen Wiederherstellungsaktionen ausführen.<br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <dt>**PWR \_ SUSPENDREQUEST**</dt> </dl> | Gibt an, dass das System in den angehaltenen Modus wechselt.<br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <dt>**PWR \_ SUSPENDRESUME**</dt> </dl>    | Gibt an, dass das System den Vorgang fortsetzen soll, nachdem es normalerweise in den angehaltenen Modus versetzt wurde, d. h., das System sendet eine **PWR SUSPENDREQUEST-Benachrichtigungsmeldung \_** an die Anwendung, bevor das System angehalten wurde. Eine Anwendung sollte alle erforderlichen Wiederherstellungsaktionen ausführen.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Wert, den eine Anwendung zurückgibt, hängt vom Wert des *wParam-Parameters* ab. Wenn *wParam* **PWR \_ SUSPENDREQUEST** ist, lautet der Rückgabewert **PWR \_ FAIL,** um zu verhindern, dass das System in den angehaltenen Zustand übergeht. Andernfalls ist es **PWR \_ OK.** Wenn *wParam* **PWR \_ SUSPENDRESUME** oder **PWR \_ CRITICALRESUME** ist, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Diese Nachricht wird nur an eine Anwendung übertragen, die auf einem System ausgeführt wird, das der BIOS-Spezifikation (Basic Input/Output System) der Advanced Power Management (APM) entspricht. Die Nachricht wird vom Treiber für die Energieverwaltung an jedes Fenster übertragen, das von der **EnumWindows-Funktion** zurückgegeben wird.

Der angehaltene Modus ist der Zustand, in dem die größten Einsparungen auftreten, aber alle betriebsbereiten Daten und Parameter werden beibehalten. Ram-Inhalte (Random Access Memory) werden beibehalten, aber viele Geräte sind wahrscheinlich deaktiviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>WinUser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




