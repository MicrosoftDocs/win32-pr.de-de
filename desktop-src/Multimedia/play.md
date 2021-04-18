---
title: Wiedergabe Befehl
description: Der Play-Befehl beginnt mit der Wiedergabe eines Geräts. CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- Wiedergabe Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf262db152677ef5a2f29de9526152c1d48d4c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340781"
---
# <a name="play-command"></a>Wiedergabe Befehl

Der Play-Befehl beginnt mit der Wiedergabe eines Geräts. CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("play %s %s %s"), 
  lpszDeviceID, 
  lpszPlayFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszplayflags*
</dt> <dd>

Flag für die Wiedergabe eines Geräts. In der folgenden Tabelle werden die Gerätetypen aufgelistet, die den **Wiedergabe** Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                          | Bedeutung                           |
|--------------|----------------------------------|-----------------------------------|
| CDAudio      | von *Position*                  | an *Position*                     |
| Digitalvideo | von *Position* voll Bildwiederholung | an *Positions* Fenster umkehren       |
| sequencer    | von *Position*                  | an *Position*                     |
| VCR          | zum *Zeitpunkt* von der *Position* umkehren  | an *Position* überprüfen                |
| Videodisk    | schnelle from- *Position*-Reverse-Scan | *ganze* Zahl mit langsamer Geschwindigkeit an *Position* |
| waveaudiodatei    | von *Position*                  | an *Position*                     |



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszplayflags** -Parameter und deren Bedeutung angegeben werden können.



| Wert           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| zum *Zeitpunkt*       | Gibt an, wann das Gerät mit der Ausführung dieses Befehls beginnen soll, oder ob das Gerät beim Start des Geräts gecuht wurde. Weitere Informationen finden Sie [unter dem Hinweis](cue.md) Befehl.                                                                                                                                                                                                                                                                 |
| fast            | Gibt an, dass das Gerät schneller als normal abgespielt werden soll. Um die genaue Geschwindigkeit eines Video Disk Players zu ermitteln, verwenden Sie das Flag "Geschwindigkeit" des [Status](status.md) -Befehls. Um die Geschwindigkeit genauer anzugeben, verwenden Sie das Flag "Geschwindigkeit" dieses Befehls.                                                                                                                                                                                                   |
| von *Position* | Gibt eine Startposition für die Wiedergabe an. Wenn das Flag "from" nicht angegeben wird, beginnt die Wiedergabe an der aktuellen Position. Bei **CDAudio** -Geräten gibt der Treiber einen Fehler zurück, wenn die "von"-Position größer als die Endposition der Festplatte ist oder wenn die "von"-Position größer als die "an"-Position ist. Bei **Videodisk** -Geräten befinden sich die Standardpositionen in Frames für CAV-Festplatten und in Stunden, Minuten und Sekunden für CLV-Festplatten. |
| Vollbild      | Gibt an, dass eine voll Bild Anzeige verwendet werden soll. Verwenden Sie dieses Flag nur, wenn Sie komprimierte Dateien abspielen. (Nicht komprimierte Dateien werden nicht voll Bildschirm abgespielt.)                                                                                                                                                                                                                                                                                                  |
| wiederholen          | Gibt an, dass die Wiedergabe neu gestartet werden soll, wenn das Ende des Inhalts erreicht ist.                                                                                                                                                                                                                                                                                                                                                                       |
| reverse         | Gibt an, dass die Wiedergabe Richtung rückwärts verläuft. Sie können keine Endposition mit dem Flag "Reverse" angeben. Bei Videodisks gilt "Scan" nur für das CAV-Format.                                                                                                                                                                                                                                                                                     |
| fein            | Wird so schnell wie möglich abgespielt, ohne das Video zu deaktivieren (obwohl Audiodaten möglicherweise deaktiviert sind). Bei Videodisks gilt "Scan" nur für das CAV-Format.                                                                                                                                                                                                                                                                                                             |
| langsam            | Wird langsam abgespielt. Um die genaue Geschwindigkeit eines Video Disk Players zu ermitteln, verwenden Sie das Flag "Geschwindigkeit" des [Status](status.md) -Befehls. Um die Geschwindigkeit genauer anzugeben, verwenden Sie das Flag "Geschwindigkeit" dieses Befehls. Bei Videodisks gilt "langsam" nur für das CAV-Format.                                                                                                                                                                                            |
| *ganzzahlige* Geschwindigkeit | Gibt eine Video Disk mit der angegebenen Geschwindigkeit in Frames pro Sekunde wieder. Dieses Flag gilt nur für CAV-CDs.                                                                                                                                                                                                                                                                                                                                                 |
| an *Position*   | Gibt eine Endposition für die Wiedergabe an. Wenn das Flag "to" nicht angegeben wird, wird die Wiedergabe am Ende des Inhalts angehalten. Bei **CDAudio** -Geräten gibt der Treiber einen Fehler zurück, wenn die "an"-Position größer als die Endposition der Festplatte ist. Bei **Videodisk** -Geräten befinden sich die Standardpositionen in Frames für CAV-Festplatten und in Stunden, Minuten und Sekunden für CLV-Festplatten.                                                                  |
| Fenster          | Gibt an, dass die Wiedergabe das Fenster verwenden soll, das der Geräte Instanz zugeordnet ist. Dies ist die Standardeinstellung.                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Vor dem Ausgeben von Befehlen, die Positionswerte verwenden, sollten Sie das gewünschte Zeitformat mithilfe des [Set](set.md) -Befehls festlegen. Dieser Befehl beginnt mit der aktuellen Geschwindigkeit, wie Sie mit dem Befehl "Geschwindigkeit" festlegen festgelegt ist. Die Richtung ist umgekehrt, wenn das Flag "Reverse" angegeben wird, oder wenn das Flag "to" als Wert kleiner als das Flag "from" angegeben wird. Wenn das Flag "from" nicht angegeben wird, beginnt die Wiedergabe an der aktuellen Position. Die Flags "to" und "Reverse" können nicht gleichzeitig verwendet werden.

## <a name="examples"></a>Beispiele

Der folgende Befehl gibt das "mysound"-Gerät von der Position 1000 bis zur Position 2000 wieder und sendet eine Benachrichtigungs Meldung, wenn die Wiedergabe abgeschlossen ist.

``` syntax
play mysound from 1000 to 2000 notify
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

[set](set.md)
</dt> </dl>

 

