---
title: Reserve Befehl
description: Der Reserve Befehl ordnet dem Arbeitsbereich der Geräte Instanz zusammenhängenden Speicherplatz zu. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- Reserve Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f71889af552b9040777394047a0facfc6c81366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949441"
---
# <a name="reserve-command"></a>Reserve Befehl

Der Reserve Befehl ordnet dem Arbeitsbereich der Geräte Instanz zusammenhängenden Speicherplatz zu. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("reserve %s %s %s"), 
  lpszDeviceID, 
  lpszReserve, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszreserve*
</dt> <dd>

Mindestens eines der folgenden Flags.



| Wert           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| in *Pfad*       | Gibt das Laufwerk und den Verzeichnispfad (aber nicht den Namen) einer temporären Datei an, die zum Speichern der aufgezeichneten Daten verwendet wird. Der Name dieser Datei wird vom Gerät angegeben. Die temporäre Datei wird gelöscht, wenn das Gerät geschlossen wird. Wenn dieses Flag weggelassen wird, gibt das Gerät den Speicherort des Speicherplatzes an.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Größen *Dauer* | Gibt die ungefähre Menge an Speicherplatz an, die im Arbeitsbereich reserviert werden soll. Der *Duration* -Wert wird im aktuellen Zeitformat angegeben. Das Gerät basiert auf der Schätzung des erforderlichen Speicherplatzes auf den folgenden Parametern: der angeforderten Zeit, dem Dateiformat, dem Video-und Audiokomprimierungs Algorithmus und den gültigen Komprimierungs Qualitätswerten. Wenn [setvideo](setvideo.md) "Record" den Wert "Off" hat, ist der Speicherplatz nur für Audiodaten reserviert. Wenn [setaudiodaten](setaudio.md) "Record" den Wert "Off" hat, ist der Speicherplatz nur für Videos reserviert. Wenn beide "Off" oder " *Duration* " gleich 0 (null) sind, ist kein Speicherplatz reserviert, und der vorhandene reservierte Speicherplatz wird aufgehoben. Wenn dieses Flag ausgelassen wird, verwendet das Gerät einen Geräte definierten Standardwert. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify", "Test" oder eine Kombination daraus sein. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Bei Bedarf verwenden nachfolgende [Daten Satz](record.md) -oder [Speicher](save.md) Befehle den von diesem Befehl reservierten Speicherplatz. Wenn der Arbeitsbereich nicht gespeicherte Daten enthält, gehen die Daten verloren. Einige Geräte erfordern keine Reservierung und ignorieren Sie. Wenn der Speicherplatz vor dem Aufzeichnen nicht reserviert ist, führt der Datensatz-Befehl eine implizite Reserve mit gerätespezifischen Standardflags aus. Verwenden Sie einen expliziten Reserve Befehl, wenn Sie eine bessere Kontrolle darüber haben möchten, wann die Verzögerung für die Datenträger Zuordnung auftritt, und Steuern Sie, wie viel Speicherplatz zugewiesen ist, und Steuern Sie den Speicherort des Speicherplatzes. Die Anwendung kann die Menge und den Speicherort des zuvor reservierten Speicherplatzes mit nachfolgenden Reserve Befehlen ändern. Der zugeordnete und noch nicht verwendete Speicherplatz wird nicht aufgehoben, bis alle aufgezeichneten Daten gespeichert oder die Geräte Instanz geschlossen wird.

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

[record](record.md)
</dt> <dt>

[Speichern](save.md)
</dt> <dt>

[setaudiodatei](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 

