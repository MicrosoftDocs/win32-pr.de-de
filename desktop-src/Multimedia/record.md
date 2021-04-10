---
title: Datensatz-Befehl
description: Der Datensatz-Befehl beginnt mit dem Aufzeichnen von Daten. VCR-und Waveform-Audiogeräte erkennen diesen Befehl. Obwohl Digital-Video-Geräte und MIDI-Sequencer diesen Befehl ebenfalls erkennen, implementieren die MCIAVI-und mciseq-Treiber Sie nicht.
ms.assetid: a0838153-5ac2-437f-ae1e-0c4f950fcac5
keywords:
- Datensatz-Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- record
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39d3659d4577517726260f948563cd31ecc07bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858668"
---
# <a name="record-command"></a>Datensatz-Befehl

Der Datensatz-Befehl beginnt mit dem Aufzeichnen von Daten. VCR-und Waveform-Audiogeräte erkennen diesen Befehl. Obwohl Digital-Video-Geräte und MIDI-Sequencer diesen Befehl ebenfalls erkennen, implementieren die MCIAVI-und mciseq-Treiber Sie nicht.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszRecordFlags"></span><span id="lpszrecordflags"></span><span id="LPSZRECORDFLAGS"></span>*lpszrecordflags*
</dt> <dd>

Flag zum Aufzeichnen von Daten. In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den **Datensatz** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                                                | Bedeutung                                             |
|--------------|--------------------------------------------------------|-----------------------------------------------------|
| Digitalvideo | bei *Rechteck*-Audiostream von *Position* halten  | INSERT-Vorgang zum *Positionieren* von *videostreamstream* einfügen |
| sequencer    | aus *Position* einfügen                                  | an *Position* überschreiben                             |
| VCR          | zum *Zeitpunkt* von der *Positions* Initialisierung                     | Überschreiben an *Position* einfügen                      |
| waveaudiodatei    | aus *Position* einfügen                                  | an *Position* überschreiben                             |



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszrecordflags** -Parameter und deren Bedeutung angegeben werden können.



| Wert                 | Bedeutung                                                                                                                                                                                                                                                                                                          |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at- *Rechteck*        | Gibt einen rechteckigen Bereich der externen Eingabe an, der als Quelle für die komprimierten und gespeicherten Pixel verwendet wird. Wenn nicht angegeben, wird das Rechteck standardmäßig auf das Rechteck festgelegt, das für [Put](put.md) "Video" angegeben wird. Wenn Sie anders als das Rechteck "Video" festgelegt wird, wird das angezeigte Bild nicht so aufgezeichnet. |
| zum *Zeitpunkt*             | Gibt an, wann das Gerät mit der Ausführung dieses Befehls beginnen soll, oder ob das Gerät beim Start des Geräts gecuht wurde. Weitere Informationen finden Sie [unter dem Hinweis](cue.md) Befehl.                                                                                                                             |
| Audiostream- *Stream* | Gibt den für die Aufzeichnung verwendeten Audiodatenstrom an. Wenn dieses Flag nicht angegeben wird und das Dateiformat keinen Standardwert definiert, wird es in den physisch ersten Datenstrom aufgezeichnet.                                                                                                                             |
| von *Position*       | Gibt eine Startposition für die Aufzeichnung an. Wenn das Flag "from" nicht angegeben wird, beginnt das Gerät mit der Aufzeichnung an der aktuellen Position.                                                                                                                                                                       |
| verfügen                  | Friert das Bild, wenn die Aufzeichnung abgeschlossen ist, anstatt Livevideos anzuzeigen. Wenn die Aufzeichnung angehalten wird, wird der Befehl "file" des automatischen [Monitors](monitor.md) ausgeführt. Um zu Live Videos zurückzukehren, geben Sie den Befehl "Input" für den **Monitor** aus.                                                                              |
| initialisieren            | Initialisieren Sie das Band (Medium), das das Aufzeichnen von Zeitcode (sofern möglich) für leeres Video und Audiodaten umfasst. Dieser Befehl kann mehrere Stunden in Anspruch nehmen, wenn das gesamte Band initialisiert werden muss.                                                                                                                            |
| insert                | Gibt an, dass der Datei an der aktuellen Position neue Daten hinzugefügt werden.                                                                                                                                                                                                                                            |
| overwrite             | Gibt an, dass neue Daten Daten in der Datei ersetzen.                                                                                                                                                                                                                                                           |
| an *Position*         | Gibt eine Endposition für die Aufzeichnung an. Wenn das Flag "to" nicht angegeben ist, wird das Gerät so lange aufgezeichnet, bis es [einen Befehl zum](pause.md) [Anhalten oder anhalten](stop.md) empfängt.                                                                                                                                        |
| *videostreamstream* | Gibt den für die Aufzeichnung verwendeten Videostream an. Wenn dies nicht angegeben wird und das Dateiformat keinen Standardwert definiert, wird es im Stream aufgezeichnet, der physisch zuerst vorliegt.                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die Aufzeichnung wird beendet, wenn ein [Befehl zum](pause.md) [Beenden oder anhalten](stop.md) ausgegeben wird. Für den MCIWave-Treiber werden alle Daten, die nach dem Öffnen einer Datei aufgezeichnet werden, verworfen, wenn die Datei geschlossen wird, ohne Sie zu speichern.

Vor dem Ausgeben von Befehlen, die Positionswerte verwenden, sollten Sie das gewünschte Zeitformat mithilfe des [Set](set.md) -Befehls festlegen. Die aufzuzeichnenden Spuren werden durch die Befehle [settimecode](settimecode.md) "Record", Set "assemblierungsdatensatz", " [setvideo](setvideo.md) " und [setaudiodatensatz](setaudio.md) "Record" angegeben.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Befehls Zeichenfolgen](mci-command-strings.md)
</dt> <dt>

[STI](cue.md)
</dt> <dt>

[über](monitor.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[stellte](put.md)
</dt> <dt>

[set](set.md)
</dt> <dt>

[setaudiodatei](setaudio.md)
</dt> <dt>

[settimecode](settimecode.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> <dt>

[stop](stop.md)
</dt> </dl>

 

