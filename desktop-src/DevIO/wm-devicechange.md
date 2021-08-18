---
description: Benachrichtigt eine Anwendung über eine Änderung der Hardwarekonfiguration eines Geräts oder Computers.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: WM_DEVICECHANGE-Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32936d36e01a34acc9ace512703db7584768e8b51a9fe06a791b2a285ee2add
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017798"
---
# <a name="wm_devicechange-message"></a>WM \_ DEVICECHANGE-Nachricht

Benachrichtigt eine Anwendung über eine Änderung der Hardwarekonfiguration eines Geräts oder Computers.

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Ein Handle für das Fenster.

</dd> <dt>

*uMsg* 
</dt> <dd>

Der **WM \_ DEVICECHANGE-Bezeichner.**

</dd> <dt>

*wParam* 
</dt> <dd>

Das Ereignis, das aufgetreten ist. Dieser Parameter kann einer der folgenden Werte aus der Dbt.h-Headerdatei sein.

| Wert | Bedeutung |
|-------|---------|
| **[DBT \_ DEVNODES \_ GEÄNDERT](dbt-devnodes-changed.md)**</br>0x0007 | Ein Gerät wurde dem System hinzugefügt oder daraus entfernt. |
| **[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</br>0x0017 | Die Berechtigung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) wird angefordert. |
| **[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</br>0x0018 | Die aktuelle Konfiguration wurde aufgrund eines Andockens oder Abdockens geändert. |
| **[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</br>0x0019 | Eine Anforderung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) wurde abgebrochen. |
| **[DBT \_ DEVICECONTEXTVAL](dbt-devicearrival.md)**</br>0x8000 | Ein Gerät oder ein Medienelement wurde eingefügt und ist jetzt verfügbar. |
| **[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</br>0x8001 | Die Berechtigung zum Entfernen eines Geräts oder Eines Mediums wird angefordert. Jede Anwendung kann diese Anforderung ablehnen und die Entfernung abbrechen. |
| **[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</br>0x8002 | Eine Anforderung zum Entfernen eines Geräts oder Eines Mediums wurde abgebrochen. |
| **[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</br>0x8003 | Ein Gerät oder ein Medienelement wird entfernt. Kann nicht verweigert werden. |
| **[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</br>0x8004 | Ein Gerät oder ein Medienelement wurde entfernt. |
| **[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</br>0x8005 | Ein gerätespezifisches Ereignis ist aufgetreten. |
| **[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</br>0x8006 | Ein benutzerdefiniertes Ereignis ist aufgetreten. |
| **[DBT \_ USERDEFINED](dbt-userdefined.md)**</br>0xFFFF | Die Bedeutung dieser Nachricht ist benutzerdefiniert. |

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine -Struktur, die ereignisspezifische Daten enthält. Das Format hängt vom Wert des *wParam-Parameters* ab. Weitere Informationen finden Sie in der Dokumentation für jedes Ereignis.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, um die Anforderung zu gewähren.

Gibt **BROADCAST \_ QUERY \_ DENY** zurück, um die Anforderung zu verweigern.

## <a name="remarks"></a>Hinweise

Für Geräte, die softwaresteuerbare Features wie Einschleien und Sperren bieten, sendet das System in der Regel eine [DBT \_ DEVICEREMOVEPENDING-Nachricht,](dbt-deviceremovepending.md) damit Anwendungen und Gerätetreiber die Nutzung des Geräts ordnungsgemäß beenden können. Wenn das System ein Gerät entfernt, sendet es möglicherweise keine [DBT \_ DEVICEQUERYREMOVE-Nachricht,](dbt-devicequeryremove.md) bevor dies der Fall ist.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows XP |
| Unterstützte Mindestversion (Server) | Windows Server 2003|
| Header | <dl> <dt>Winuser.h (include Windows.h oder Dbt.h)</dt> </dl> |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)
</dt> <dt>

[DBT \_ CONFIGCHANGED](dbt-configchanged.md)
</dt> <dt>

[DBT \_ CUSTOMEVENT](dbt-customevent.md)
</dt> <dt>

[DBT \_ DEVICECONTEXTVAL](dbt-devicearrival.md)
</dt> <dt>

[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)
</dt> <dt>

[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)
</dt> <dt>

[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)
</dt> <dt>

[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)
</dt> <dt>

[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)
</dt> <dt>

[DBT \_ DEVNODES \_ GEÄNDERT](dbt-devnodes-changed.md)
</dt> <dt>

[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)
</dt> <dt>

[DBT \_ USERDEFINED](dbt-userdefined.md)
</dt> </dl>
