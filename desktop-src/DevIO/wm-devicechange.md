---
description: Benachrichtigt eine Anwendung über eine Änderung an der Hardwarekonfiguration eines Geräts oder Computers.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: WM_DEVICECHANGE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cc45d7a7978d5501e51cc1355c43afcf12b956
ms.sourcegitcommit: 8c1942ac6731488abbeae46a7dbe3da166fee2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2021
ms.locfileid: "107581502"
---
# <a name="wm_devicechange-message"></a>WM \_ DEVICECHANGE-Nachricht

Benachrichtigt eine Anwendung über eine Änderung an der Hardwarekonfiguration eines Geräts oder Computers.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

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

Das aufgetretene Ereignis. Dieser Parameter kann einer der folgenden Werte aus der Dbt.h-Headerdatei sein.

| Wert | Bedeutung |
|-------|---------|
| **[DBT \_ DEVNODES \_ GEÄNDERT](dbt-devnodes-changed.md)**</br>0x0007 | Ein Gerät wurde dem System hinzugefügt oder daraus entfernt. |
| **[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</br>0x0017 | Die Berechtigung zum Ändern der aktuellen Konfiguration (Dock oder Abdocken) wird angefordert. |
| **[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</br>0x0018 | Die aktuelle Konfiguration wurde aufgrund eines Andocks oder Abdockens geändert. |
| **[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</br>0x0019 | Eine Anforderung zum Ändern der aktuellen Konfiguration (Dock oder Abdocken) wurde abgebrochen. |
| **[DBT \_ DEVICEARRARRARR](dbt-devicearrival.md)**</br>0x8000 | Ein Gerät oder Medienteil wurde eingefügt und ist jetzt verfügbar. |
| **[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</br>0x8001 | Die Berechtigung zum Entfernen eines Geräts oder Medienstücks wird angefordert. Jede Anwendung kann diese Anforderung verweigern und die Entfernung abbrechen. |
| **[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</br>0x8002 | Eine Anforderung zum Entfernen eines Geräts oder Medienstücks wurde abgebrochen. |
| **[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</br>0x8003 | Ein Gerät oder Medienteil wird entfernt. Kann nicht verweigert werden. |
| **[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</br>0x8004 | Ein Gerät oder Medienteil wurde entfernt. |
| **[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</br>0x8005 | Ein gerätespezifisches Ereignis ist aufgetreten. |
| **[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</br>0x8006 | Ein benutzerdefiniertes Ereignis ist aufgetreten. |
| **[DBT \_ USERDEFINED](dbt-userdefined.md)**</br>0xffff | Die Bedeutung dieser Nachricht ist benutzerdefiniert. |

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine -Struktur, die ereignisspezifische Daten enthält. Das Format hängt vom Wert des *wParam-Parameters* ab. Weitere Informationen finden Sie in der Dokumentation für jedes Ereignis.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, um die Anforderung zu gewähren.

Geben Sie **BROADCAST \_ QUERY \_ DENY** zurück, um die Anforderung zu verweigern.

## <a name="remarks"></a>Bemerkungen

Für Geräte, die softwarekontrollierbare Features wie z. B. Einschleien und Sperren bieten, sendet das System in der Regel eine [DBT \_ DEVICEREMOVEPENDING-Nachricht,](dbt-deviceremovepending.md) damit Anwendungen und Gerätetreiber die Verwendung des Geräts ordnungsgemäß beenden können. Wenn das System ein Gerät entfernt, sendet es möglicherweise keine [DBT \_ DEVICEQUERYREMOVE-Nachricht,](dbt-devicequeryremove.md) bevor dies der Fall ist.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows XP |
| Unterstützte Mindestversion (Server) | Windows Server 2003|
| Header | <dl> <dt>Winuser.h (einschließlich Windows.h oder Dbt.h)</dt> </dl> |

## <a name="see-also"></a>Weitere Informationen

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
