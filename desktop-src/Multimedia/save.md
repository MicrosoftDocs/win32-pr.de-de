---
title: Befehl "Speichern"
description: Mit dem Befehl "Speichern" wird eine MCI-Datei gespeichert. Video-Overlay-und Waveform-Audiogeräte erkennen diesen Befehl. Obwohl Digital-Video-Geräte und MIDI-Sequencer diesen Befehl ebenfalls erkennen, unterstützen die MCIAVI-und mciseq-Treiber dies nicht.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- Befehl "Speichern" Windows Multimedia
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0029ad03c1b7fe855e8485b2719b11628fac1103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339537"
---
# <a name="save-command"></a>Befehl "Speichern"

Mit dem Befehl "Speichern" wird eine MCI-Datei gespeichert. Video-Overlay-und Waveform-Audiogeräte erkennen diesen Befehl. Obwohl Digital-Video-Geräte und MIDI-Sequencer diesen Befehl ebenfalls erkennen, unterstützen die MCIAVI-und mciseq-Treiber dies nicht.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszfilename*
</dt> <dd>

Flag, das den Namen der zu speichernden Datei und optional zusätzliche Flags angibt, die den Speichervorgang verändern. In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Save** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung              | Bedeutung               |
|--------------|----------------------|-----------------------|
| Digitalvideo | beim *Rechteck* Abbrechen | *Dateiname* keepreserve |
| overlay      | at- *Rechteck*       | *filename*            |
| sequencer    | *filename*           |                       |
| waveaudiodatei    | *filename*           |                       |



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszfilename** -Parameter und deren Bedeutung angegeben werden können.



| Wert          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abort          | Beendet einen aktuell ausgeführten **Speicher** Vorgang. Wenn diese Option verwendet wird, muss dies das einzige vorhandene Element sein.                                                                                                                                                                                                                                                                                                                                                                                                                 |
| at- *Rechteck* | Gibt ein Rechteck relativ zum Frame Puffer Ursprung an. Das *Rechteck* wird als *x1 y1 x2 Y2* angegeben. Die Koordinaten *x1 y1* geben die linke obere Ecke an, und die Koordinaten *x2 Y2* geben die Breite und Höhe an. Für Digital Video-Geräte wird der [Erfassungs](capture.md) Befehl verwendet, um den Inhalt des Frame Puffers aufzuzeichnen.<br/>                                                                                                                                               |
| *filename*     | Gibt den Dateinamen an, der der Datendatei zugewiesen werden soll. Wenn kein Pfad angegeben ist, wird die Datei auf dem Datenträger und im Verzeichnis abgelegt, das zuvor im expliziten oder impliziten [Reserve](reserve.md) Befehl angegeben wurde. Wenn **Reserve** nicht ausgestellt wurde, sind das Standard Laufwerk und das Standardverzeichnis diejenigen, die der Aufgabe der Anwendung zugeordnet sind. Wenn ein Pfad angegeben ist, muss sich das Gerät möglicherweise auf dem Laufwerk befinden, das von der expliziten oder impliziten **Reserve** angegeben wird. Dieses Flag ist erforderlich. |
| keepreserve    | Gibt an, dass nicht verwendeter Speicherplatz, der vom ursprünglichen **Reserve** Befehl übrig geblieben ist, nicht aufgehoben wird.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die *filename* -Variable ist erforderlich, wenn das Gerät mithilfe des "neuen" Geräte Bezeichners geöffnet wurde.

## <a name="examples"></a>Beispiele

Der folgende Befehl speichert den gesamten Video Puffer in einer Datei namens vcapfile. TGA.

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

[MCI](mci.md)
</dt> <dt>

[MCI-Befehls Zeichenfolgen](mci-command-strings.md)
</dt> <dt>

[einver](capture.md)
</dt> <dt>

[Reserve](reserve.md)
</dt> </dl>

 

