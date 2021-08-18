---
title: Record-Befehl
description: Der Datensatzbefehl beginnt mit der Aufzeichnung von Daten. VCR- und Waveform-Audiogeräte erkennen diesen Befehl. Obwohl digital-video-Geräte und GIGABYTE-Sequencer diesen Befehl ebenfalls erkennen, implementieren die MCIAVI- und MCISEQ-Treiber ihn nicht.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- Befehl "record" Windows Multimedia
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f326b13d86f073074ef2c1119d449e297e65e7d3accb22d9858e5c1579493c01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037560"
---
# <a name="record-command"></a>Record-Befehl

Der Datensatzbefehl beginnt mit der Aufzeichnung von Daten. VCR- und Waveform-Audiogeräte erkennen diesen Befehl. Obwohl digital-video-Geräte und GIGABYTE-Sequencer diesen Befehl ebenfalls erkennen, implementieren die MCIAVI- und MCISEQ-Treiber ihn nicht.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("record %s %s %s"), 
  lpszDeviceID, 
  lpszRecordFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszRecordFlags*
</dt> <dd>

Flag für die Aufzeichnung von Daten. In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den **Datensatzbefehl** und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                | Bedeutung                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| digitalvideo | beim *Rechteckaudiostreamstream* aus Position *halten*  | Einfügen des Überschreibens zum *Positionieren* des *Videostreamstreams* |
| sequencer    | from *position* insert                                  | Überschreiben zur *Position*                             |
| Vcr          | *zum Zeitpunkt* der *Positionsinitialisierung*                     | Insert overwrite to *position*                      |
| Waveaudio    | from *position* insert                                  | Überschreiben zur *Position*                             |



 

Die folgende Tabelle enthält die Flags, die im **lpszRecordFlags-Parameter** angegeben werden können, und ihre Bedeutungen.



| Wert                 | Bedeutung                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| am *Rechteck*        | Gibt einen rechteckigen Bereich der externen Eingabe an, der als Quelle für die komprimierten und gespeicherten Pixel verwendet wird. Wenn keine Angabe erfolgt, wird das Rechteck standardmäßig auf das Rechteck festgelegt, das für [put](put.md) "video" angegeben ist. Wenn es anders als das Rechteck "Video" festgelegt ist, wird das angezeigte Bild nicht aufgezeichnet. |
| *zur zeit*             | Gibt an, wann das Gerät mit der Ausführung dieses Befehls beginnen soll, oder , wenn das Gerät angekuppelt wurde, wenn der Cued-Befehl beginnt. Weitere Informationen finden Sie im [Befehl cue.](cue.md)                                                                                                                             |
| *Audiostreamstream* | Gibt den für die Aufzeichnung verwendeten Audiostream an. Wenn dieses Flag nicht angegeben ist und das Dateiformat keinen Standardwert definiert, wird es in dem Datenstrom aufgezeichnet, der zuerst physisch ist.                                                                                                                             |
| from *position*       | Gibt eine Anfangsposition für die Aufzeichnung an. Wenn das Flag "from" nicht angegeben ist, beginnt das Gerät mit der Aufzeichnung an der aktuellen Position.                                                                                                                                                                       |
| Halten                  | Friert das Bild ein, wenn die Aufzeichnung abgeschlossen ist, anstatt Livevideos zu zeigen. Wenn die Aufzeichnung beendet wird, wird ein automatischer [Monitorbefehl](monitor.md) "file" ausgeführt. Um zum Livevideo zurückzukehren, geben Sie den **Befehl "input"** für den Monitor aus.                                                                              |
| initialisieren            | Initialisieren Sie das Band (Medien), das die Aufzeichnung des Zeitcodes (falls möglich) für leeres Video und Audio umfasst. Dieser Befehl kann mehrere Stunden dauern, wenn das gesamte Band initialisiert werden muss.                                                                                                                            |
| insert                | Gibt an, dass der Datei an der aktuellen Position neue Daten hinzugefügt werden.                                                                                                                                                                                                                                            |
| overwrite             | Gibt an, dass neue Daten Daten in der Datei ersetzen.                                                                                                                                                                                                                                                           |
| , um *zu positionieren*         | Gibt eine Endposition für die Aufzeichnung an. Wenn das Flag "to" nicht angegeben ist, zeichnet das Gerät auf, bis es einen [Befehl zum Beenden](stop.md) oder [Anhalten](pause.md) empfängt.                                                                                                                                        |
| Videostream  | Gibt den Videostream an, der für die Aufzeichnung verwendet wird. Wenn dies nicht angegeben ist und das Dateiformat keinen Standardwert definiert, wird er in dem Datenstrom aufgezeichnet, der physisch zuerst ist.                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für DigitalVideo- und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die Aufzeichnung wird beendet, wenn ein [Befehl zum Beenden](stop.md) oder [Anhalten](pause.md) ausgegeben wird. Für den MCIWAVE-Treiber werden alle Nach dem Öffnen einer Datei aufgezeichneten Daten verworfen, wenn die Datei geschlossen wird, ohne sie zu speichern.

Bevor Sie Befehle ausgeben, die Positionswerte verwenden, sollten Sie das gewünschte Zeitformat mit dem Befehl [set](set.md) festlegen. Die aufgezeichneten Spuren werden durch die Befehle [settimecode](settimecode.md) "record", set "assemble record", [setvideo](setvideo.md) "record" und [setaudio](setaudio.md) "record" angegeben.

## <a name="examples"></a>Beispiele

Mit dem folgenden Befehl wird die Aufzeichnung an der aktuellen Position gestartet.

``` syntax
record mysound
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> <dt>

[Hinweis](cue.md)
</dt> <dt>

[Monitor](monitor.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[put](put.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[Setaudio](setaudio.md)
</dt> <dt>

[settimecode](settimecode.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

