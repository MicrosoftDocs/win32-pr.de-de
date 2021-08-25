---
title: Reservebefehl
description: Der Reservebefehl ordnet zusammenhängenden Speicherplatz für den Arbeitsbereich der Geräteinstanz zu. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: ac4fc75e-82d0-4817-a5cf-a77996bc69e2
keywords:
- Reservebefehl Windows Multimedia
topic_type:
- apiref
api_name:
- reserve
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83f4573f5a630bbf1243b7126867c2d6c6beef61810210624fe87958e12b02ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892920"
---
# <a name="reserve-command"></a>Reservebefehl

Der Reservebefehl ordnet zusammenhängenden Speicherplatz für den Arbeitsbereich der Geräteinstanz zu. Digitalvideogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszReserve"></span><span id="lpszreserve"></span><span id="LPSZRESERVE"></span>*lpszReserve*
</dt> <dd>

Mindestens eines der folgenden Flags.



| Wert           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| im *Pfad*       | Gibt das Laufwerk und den Verzeichnispfad (aber nicht den Namen) einer temporären Datei an, die zum Speichern aufgezeichneter Daten verwendet wird. Der Name dieser Datei wird vom Gerät angegeben. Die temporäre Datei wird gelöscht, wenn das Gerät geschlossen wird. Wenn dieses Flag ausgelassen wird, gibt das Gerät den Speicherort des Speicherplatzes an.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Dauer  der Größe | Gibt den ungefähren Speicherplatz an, der im Arbeitsbereich reserviert werden soll. Der *wert duration* wird im aktuellen Zeitformat angegeben. Das Gerät basiert seine Schätzung des erforderlichen Speicherplatzes auf den folgenden Parametern: der angeforderten Zeit, dem Dateiformat, dem Algorithmus für die Video- und Audiokomprimierung und den tatsächlichen Komprimierungsqualitätswerten. Wenn [setvideo](setvideo.md) "record" "off" ist, ist der Speicherplatz nur für Audio reserviert. Wenn [setaudio](setaudio.md) "record" "off" ist, ist Speicherplatz nur für Videos reserviert. Wenn beide "off" sind oder die *Dauer* 0 (null) ist, wird kein Speicherplatz reserviert, und die Zuordnung eines vorhandenen reservierten Speicherplatzes wird freigegeben. Wenn dieses Flag ausgelassen wird, verwendet das Gerät einen gerätedefinierten Standardwert. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify", "test" oder eine Kombination dieser sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Bei Bedarf verwenden nachfolgende [Aufzeichnungs-](record.md) oder [Speicherbefehle](save.md) den durch diesen Befehl reservierten Speicherplatz. Wenn der Arbeitsbereich nicht gespeicherte Daten enthält, geht der Datenverlust verloren. Einige Geräte erfordern keine Reservierung und ignorieren sie. Wenn vor der Aufzeichnung kein Speicherplatz reserviert wird, führt der Aufzeichnungsbefehl eine implizite Reserve mit gerätespezifischen Standardflags aus. Verwenden Sie einen expliziten Reservebefehl, wenn Sie besser steuern möchten, wann die Verzögerung bei der Datenträgerzuordnung auftritt, wie viel Speicherplatz zugeordnet wird und wo der Speicherplatz zugeordnet wird. Ihre Anwendung kann die Menge und den Speicherort des zuvor reservierten Speicherplatzes mit nachfolgenden Reservebefehlen ändern. Der zugeordnete und noch nicht belegte Speicherplatz wird erst freigegeben, wenn aufgezeichnete Daten gespeichert oder die Geräteinstanz geschlossen wurde.

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

[record](record.md)
</dt> <dt>

[Speichern](save.md)
</dt> <dt>

[Setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 

