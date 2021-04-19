---
title: Signal Befehl
description: Der Signal-Befehl identifiziert eine angegebene Position im Arbeitsbereich, indem die Anwendung eine mm \_ mcisignal-Nachricht sendet. Dieser Befehl wird von Digital-Video-Geräten erkannt. MCIAVI unterstützt jeweils nur ein aktives Signal.
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- Signal Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd96b8970ebbb6502306c6d2d5fd8c49f172cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339977"
---
# <a name="signal-command"></a>Signal Befehl

Der Signal-Befehl identifiziert eine angegebene Position im Arbeitsbereich, indem die Anwendung eine [mm \_ mcisignal](mm-mcisignal.md) -Nachricht sendet. Dieser Befehl wird von Digital-Video-Geräten erkannt. MCIAVI unterstützt jeweils nur ein aktives Signal.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("signal %s %s %s"), 
  lpszDeviceID, 
  lpszSignalFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszsignalflags*
</dt> <dd>

Eines der folgenden Flags.



| Wert            | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| an Position      | Gibt den Frame zum Aufrufen eines Signals an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| cancel           | Entfernt Signale aus dem Arbeitsbereich. Ein einzelnes Signal wird mit dem Flag "uservalue" angegeben. Wenn das Flag "uservalue" nicht mit "Abbrechen" angegeben wird, bricht das Gerät alle Signale ab. Das Flag "Abbrechen" ist nicht mit den Flags "at", "All" und "Return Position" kompatibel.                                                                                                                                                                                                                                                                                          |
| Jedes *Intervall* | Gibt den Zeitraum der Signale an. Der *Intervall* Wert wird im aktuellen Zeitformat angegeben. Bei Verwendung mit der *Position*"an" werden Signale im gesamten Arbeitsbereich platziert, wobei eine Signal Markierung an der *Position* platziert wird.<br/> Ohne das Flag "at" werden Signale im gesamten Arbeitsbereich mit einem Signal an der aktuellen Position platziert.<br/> Wenn dieses Flag weggelassen wird, wird nur die durch das Flag "at" bezeichnete Position als markiert.<br/> Wenn der *Intervall* Wert niedriger als die von einem Gerät unterstützte Mindestfrequenz ist, wird der Mindestwert verwendet.<br/> |
| Rückgabe Position  | Gibt an, dass das Gerät den Positionswert anstelle des Bezeichners "uservalue" in der Signalisierungs Nachricht senden soll. Der Bezeichner "uservalue" kann weiterhin verwendet werden, um die Signal Markierungen abzubrechen oder neu zu definieren.                                                                                                                                                                                                                                                                                                                                                                      |
| *ID* des Benutzer Werts   | Gibt einen Bezeichner an, der mit der Signal Meldung zurückgemeldet wird. Dieser Bezeichner fungiert als Bezeichner, der mit anderen **Signal** Befehlen verwendet werden kann, um auf diese **Signal** Einstellung zu verweisen. Wenn keine Angabe erfolgt, ist der Standardwert 0 (null).                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify", "Test" oder eine Kombination daraus sein. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Das Fenster Handle, das für die Benachrichtigung über Befehls Vervollständigungs Meldungen verwendet wird, wird auch zur Signalisierung verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Befehls Zeichenfolgen](mci-command-strings.md)
</dt> <dt>

[MM- \_ mcisignal](mm-mcisignal.md)
</dt> </dl>

 

