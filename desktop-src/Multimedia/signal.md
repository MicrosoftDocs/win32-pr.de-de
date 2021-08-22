---
title: signal-Befehl
description: Der Signalbefehl identifiziert eine angegebene Position im Arbeitsbereich, indem er der Anwendung eine MM \_ MCISIGNAL-Nachricht sendet. Digitalvideogeräte erkennen diesen Befehl. MCIAVI unterstützt jeweils nur ein aktives Signal.
ms.assetid: 3d10eac0-fd1a-41ee-98fa-2518642c7339
keywords:
- Signalbefehl Windows Multimedia
topic_type:
- apiref
api_name:
- signal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db007a03738f13bb9acc0733b67bcd38de4b97f2b194bb16cdfcd85f798cfdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037180"
---
# <a name="signal-command"></a>signal-Befehl

Der Signalbefehl identifiziert eine angegebene Position im Arbeitsbereich, indem er der Anwendung eine [MM \_ MCISIGNAL-Nachricht](mm-mcisignal.md) sendet. Digitalvideogeräte erkennen diesen Befehl. MCIAVI unterstützt jeweils nur ein aktives Signal.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszSignalFlags"></span><span id="lpszsignalflags"></span><span id="LPSZSIGNALFLAGS"></span>*lpszSignalFlags*
</dt> <dd>

Eines der folgenden Flags.



| Wert            | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| an Position      | Gibt den Frame an, um ein Signal aufzurufen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| cancel           | Entfernt Signale aus dem Arbeitsbereich. Ein einzelnes Signal wird mithilfe des Flags "uservalue" angegeben. Wenn das Flag "uservalue" nicht mithilfe von "cancel" angegeben wird, bricht das Gerät alle Signale ab. Das Flag "cancel" ist nicht mit den Flags "at", "every" und "return position" kompatibel.                                                                                                                                                                                                                                                                                          |
| jedes *Intervall* | Gibt den Zeitraum der Signale an. Der *Intervallwert* wird im aktuellen Zeitformat angegeben. Bei Verwendung mit der *Position*"at" werden Signale im gesamten Arbeitsbereich mit einer Signalmarkierung an *position* platziert.<br/> Ohne das Flag "at" werden Signale im gesamten Arbeitsbereich mit einem Signal an der aktuellen Position platziert.<br/> Wenn dieses Flag ausgelassen wird, wird nur die Position markiert, die durch das Flag "at" angegeben wird.<br/> Wenn der *Intervallwert* kleiner als die von einem Gerät unterstützte Mindesthäufigkeit ist, wird der Mindestwert verwendet.<br/> |
| Rückgabeposition  | Gibt an, dass das Gerät den Positionswert anstelle des Bezeichners "uservalue" in der Signalisierungsmeldung senden soll. Der Bezeichner "uservalue" kann weiterhin verwendet werden, um die Signalmarkierungen abzubrechen oder neu zu definieren.                                                                                                                                                                                                                                                                                                                                                                      |
| uservalue *id*   | Gibt einen Bezeichner an, der mit der Signalisierungsmeldung gemeldet wird. Dieser Bezeichner fungiert als Bezeichner, der mit anderen **Signalbefehlen** verwendet werden kann, um auf diese **Signaleinstellung** zu verweisen. Wenn keine Angabe erfolgt, ist der Standardwert 0 (null).                                                                                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify", "test" oder eine Kombination dieser sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Das Fensterhandle, das für die Benachrichtigung von Befehlsabschlussmeldungen verwendet wird, wird auch für die Signalisierung verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> <dt>

[MM \_ MCISIGNAL](mm-mcisignal.md)
</dt> </dl>

 

