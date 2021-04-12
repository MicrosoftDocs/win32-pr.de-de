---
description: Benachrichtigt eine Anwendung über eine Änderung an der Hardwarekonfiguration eines Geräts oder Computers.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: WM_DEVICECHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f631d75f89f306adc0594a3df6c63d63753e163
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393029"
---
# <a name="wm_devicechange-message"></a>WM- \_ devicechange-Meldung

Benachrichtigt eine Anwendung über eine Änderung an der Hardwarekonfiguration eines Geräts oder Computers.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Ein Handle für das Fenster.

</dd> <dt>

*Umschlag* 
</dt> <dd>

Der **WM- \_ devicechange** -Bezeichner.

</dd> <dt>

*wParam* 
</dt> <dd>

Das Ereignis, das aufgetreten ist. Bei diesem Parameter kann es sich um einen der folgenden Werte aus der DBT. h-Header Datei handeln.



| Wert                                                                                                                                                                                                                                                                                                  | Bedeutung                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span><dl> <dt>**[DBT \_ Configchangeabgeb Rochen](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt> </dl>             | Eine Anforderung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) wurde abgebrochen.<br/>                                           |
| <span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span><dl> <dt>**[DBT \_ ConfigChanged](dbt-configchanged.md)**</dt> <dt>0x0018</dt> </dl>                                         | Die aktuelle Konfiguration wurde aufgrund eines Andocken oder Abdocken geändert.<br/>                                                             |
| <span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span><dl> <dt>**[DBT \_ CustomEvent](dbt-customevent.md)**</dt> <dt>0x8006</dt> </dl>                                                 | Ein benutzerdefiniertes Ereignis ist aufgetreten.<br/>                                                                                                |
| <span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span><dl> <dt>**[DBT \_ Devicearrival](dbt-devicearrival.md)**</dt> <dt>0X8000</dt> </dl>                                         | Ein Gerät oder ein Teil des Mediums wurde eingefügt und ist jetzt verfügbar.<br/>                                                          |
| <span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span><dl> <dt>**[DBT \_ DeviceQueryRemove](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt> </dl>                         | Die Berechtigung zum Entfernen eines Geräts oder eines Mediums wird angefordert. Jede Anwendung kann diese Anforderung verweigern und das Entfernen abbrechen.<br/> |
| <span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span><dl> <dt>**[DBT \_ Devicequeryremovefailed](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt> </dl> | Eine Anforderung zum Entfernen eines Geräts oder eines Mediums wurde abgebrochen.<br/>                                                           |
| <span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span><dl> <dt>**[DBT \_ Deviceremovecomplete](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt> </dl>             | Ein Gerät oder ein Medium wurde entfernt.<br/>                                                                                |
| <span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span><dl> <dt>**[DBT \_ Deviceremovepending](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt> </dl>                 | Ein Gerät oder ein Teil des Mediums wird entfernt. Kann nicht verweigert werden.<br/>                                                        |
| <span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span><dl> <dt>**[DBT \_ Geräte-/linientypespecific](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt> </dl>                     | Ein Geräte spezifisches Ereignis ist aufgetreten.<br/>                                                                                       |
| <span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span><dl> <dt>**[DBT \_ Devnodes \_ geändert](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt> </dl>                            | Ein Gerät wurde dem System hinzugefügt oder daraus entfernt.<br/>                                                                      |
| <span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span><dl> <dt>**[DBT \_ Querychangeconfig](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt> </dl>                         | Die Berechtigung zum Ändern der aktuellen Konfiguration (Andocken oder Abdocken) wird angefordert.<br/>                                               |
| <span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span><dl> <dt>**[DBT \_ Benutzerdefinierter](dbt-userdefined.md)**</dt> <dt>0xFFFF</dt> </dl>                                                 | Die Bedeutung dieser Meldung ist Benutzer definiert.<br/>                                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine-Struktur, die ereignisspezifische Daten enthält. Das Format hängt vom Wert des *wParam* -Parameters ab. Weitere Informationen finden Sie in der Dokumentation zu den einzelnen Ereignissen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, um die Anforderung zu erteilen.

Rückgabe der **Übertragungs \_ Abfrage \_ ablehnen** , um die Anforderung zu verweigern.

## <a name="remarks"></a>Bemerkungen

Bei Geräten, die softwaregesteuerte Features anbieten (z. b. auswerfen und Sperren), sendet das System in der Regel eine [DBT \_ deviceremovepend](dbt-deviceremovepending.md) -Nachricht, damit Anwendungen und Gerätetreiber ihre Verwendung des Geräts ordnungsgemäß beenden können. Wenn das System zwangsweise ein Gerät entfernt, sendet es möglicherweise keine [DBT \_ DeviceQueryRemove](dbt-devicequeryremove.md) -Nachricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                                                    |
| Header<br/>                   | <dl> <dt>Winuser. h (Include Windows. h oder DBT. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DBT \_ configchangeabgeb Rochen](dbt-configchangecanceled.md)
</dt> <dt>

[DBT- \_ ConfigChanged](dbt-configchanged.md)
</dt> <dt>

[DBT \_ CustomEvent](dbt-customevent.md)
</dt> <dt>

[DBT \_ devicearrival](dbt-devicearrival.md)
</dt> <dt>

[DBT \_ DeviceQueryRemove](dbt-devicequeryremove.md)
</dt> <dt>

[DBT \_ devicequeryremovefailed](dbt-devicequeryremovefailed.md)
</dt> <dt>

[DBT \_ deviceremovecomplete](dbt-deviceremovecomplete.md)
</dt> <dt>

[DBT \_ deviceremovepending](dbt-deviceremovepending.md)
</dt> <dt>

[DBT-Geräte- \_ /richtlinientypespecific](dbt-devicetypespecific.md)
</dt> <dt>

[DBT- \_ Devnodes \_ geändert](dbt-devnodes-changed.md)
</dt> <dt>

[DBT \_ querychangeconfig](dbt-querychangeconfig.md)
</dt> <dt>

[DBT \_ UserDefined](dbt-userdefined.md)
</dt> </dl>

 

