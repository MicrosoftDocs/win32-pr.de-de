---
title: Befehl "speichern"
description: Mit dem Befehl save wird eine MCI-Datei gespeichert. Videoüberlagerungs- und Waveform-Audiogeräte erkennen diesen Befehl. Obwohl digital-video-Geräte und DANN-Sequencer diesen Befehl ebenfalls erkennen, unterstützen die MCIAVI- und MCISEQ-Treiber ihn nicht.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- Save-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c7b4fb75f78f8468a204217f5a4fa1593a1c50d5db541a83070a7faed41cc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037480"
---
# <a name="save-command"></a>Befehl "speichern"

Mit dem Befehl save wird eine MCI-Datei gespeichert. Videoüberlagerungs- und Waveform-Audiogeräte erkennen diesen Befehl. Obwohl digital-video-Geräte und DANN-Sequencer diesen Befehl ebenfalls erkennen, unterstützen die MCIAVI- und MCISEQ-Treiber ihn nicht.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) mit dem *lpszCommand-Parameter* auf, der wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("save %s %s %s"), 
  lpszDeviceID, 
  lpszFilename, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*
</dt> <dd>

Flag, das den Namen der zu speichernden Datei an und optional zusätzliche Flags an, die den Speichervorgang ändern. In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den **Speicherbefehl** und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung              | Bedeutung               |
|--------------|----------------------|-----------------------|
| digitalvideo | Abbruch beim *Rechteck* | *filename* keepreserve |
| overlay      | am *Rechteck*       | *filename*            |
| sequencer    | *filename*           |                       |
| Waveaudio    | *filename*           |                       |



 

In der folgenden Tabelle sind die Flags, die im **lpszFilename-Parameter angegeben** werden können, und ihre Bedeutungen aufgeführt.



| Wert          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abort          | Beendet einen **speichervorgang,** der in Bearbeitung ist. Bei Verwendung muss dies das einzige Element sein, das vorhanden ist.                                                                                                                                                                                                                                                                                                                                                                                                                 |
| am *Rechteck* | Gibt ein Rechteck relativ zum Framepuffer-Ursprung an. Das *Rechteck* wird als *X1 Y1 X2 Y2 angegeben.* Die Koordinaten *X1 Y1 geben* die obere linke Ecke und die *Koordinaten X2 Y2* die Breite und Höhe an. Bei Digitalvideogeräten wird der [Erfassungsbefehl](capture.md) verwendet, um den Inhalt des Framepuffers zu erfassen.<br/>                                                                                                                                               |
| *filename*     | Gibt den Dateinamen an, der der Datendatei zugewiesen werden soll. Wenn kein Pfad angegeben wird, wird die Datei auf dem Datenträger und im Verzeichnis platziert, das zuvor für den expliziten oder impliziten Reservebefehl [angegeben](reserve.md) wurde. Wenn **die** Reserve nicht ausgestellt wurde, sind das Standardlaufwerk und das Standardverzeichnis diejenigen, die der Aufgabe der Anwendung zugeordnet sind. Wenn ein Pfad angegeben wird, kann es für das Gerät erforderlich sein, dass er sich auf dem Laufwerk befindet, das durch die explizite oder implizite Reserve **angegeben wird.** Dieses Flag ist erforderlich. |
| keepreserve    | Gibt an, dass nicht verwendeter  Speicherplatz, der vom ursprünglichen Reservebefehl übrig bleibt, nicht entfernt wird.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für digital-video- und VCR-Geräte kann auch "test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die *Dateinamenvariable* ist erforderlich, wenn das Gerät mit der Geräte-ID "new" geöffnet wurde.

## <a name="examples"></a>Beispiele

Der folgende Befehl speichert den gesamten Videopuffer in einer Datei mit dem Namen VCAPFILE. Tga.

``` syntax
save vboard c:\vcap\vcapfile.tga
```

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

[Erfassen](capture.md)
</dt> <dt>

[Reserve](reserve.md)
</dt> </dl>

 

