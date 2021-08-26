---
title: Befehl "play"
description: Mit dem Befehl play wird die Wiedergabe eines Geräts gestartet. CD-Audio, digital-video, KEYBOARD sequencer, videodisc, VCR und waveform-audio-Geräte erkennen diesen Befehl.
ms.assetid: 3ee707d6-6af4-494d-a887-d91ea5666ac4
keywords:
- Play-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- play
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da0df530f1c7a0166dcbb7c852fe491127a9e187d1cb6cb953ec46b2533ac00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038050"
---
# <a name="play-command"></a>Befehl "play"

Mit dem Befehl play wird die Wiedergabe eines Geräts gestartet. CD-Audio, digital-video, KEYBOARD sequencer, videodisc, VCR und waveform-audio-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) mit dem *lpszCommand-Parameter* auf, der wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszPlayFlags"></span><span id="lpszplayflags"></span><span id="LPSZPLAYFLAGS"></span>*lpszPlayFlags*
</dt> <dd>

Flag für die Wiedergabe eines Geräts. In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den **Play-Befehl** und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                          | Bedeutung                           |
|--------------|----------------------------------|-----------------------------------|
| cdaudio      | von *Position*                  | nach *Position*                     |
| digitalvideo | Von *position fullscreen* repeat | Umgekehrtes *Zum-Position-Fenster*       |
| sequencer    | von *Position*                  | nach *Position*                     |
| Vcr          | zum *Zeitpunkt von* der Position in *umgekehrter* Richtung  | Scan an *Position*                |
| videodisc    | Schneller Umgekehrter *Scan von* Position | slow speed integer to position *(Ganzzahl* für langsame Geschwindigkeit bis *Position)* |
| Waveaudio    | von *Position*                  | nach *Position*                     |



 

In der folgenden Tabelle sind die Flags, die im **lpszPlayFlags-Parameter** angegeben werden können, und ihre Bedeutungen aufgeführt.



| Wert           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| zur *Zeit*       | Gibt an, wann das Gerät mit der Ausführung dieses Befehls beginnen soll, oder, wenn das Gerät mit einem Cuing-Befehl begonnen wurde, wenn der Cued-Befehl beginnt. Weitere Informationen finden Sie im [Cue-Befehl.](cue.md)                                                                                                                                                                                                                                                                 |
| fast            | Gibt an, dass das Gerät schneller als normal wiedergibt. Um die genaue Geschwindigkeit eines videodisc-Players zu bestimmen, verwenden Sie das Flag "speed" des [Statusbefehls.](status.md) Um die Geschwindigkeit genauer anzugeben, verwenden Sie das Flag "speed" dieses Befehls.                                                                                                                                                                                                   |
| von *Position* | Gibt eine Anfangsposition für die Wiedergabe an. Wenn das Flag "from" nicht angegeben ist, beginnt die Wiedergabe an der aktuellen Position. Bei **cdaudio-Geräten** gibt der Treiber einen Fehler zurück, wenn die Position "von" größer als die Endposition des Datenträgers ist oder wenn die Position "von" größer als die Position "to" ist. Bei **Videodisc-Geräten** befinden sich die Standardpositionen in Frames für CAV-Datenträger und in Stunden, Minuten und Sekunden für CLV-Datenträger. |
| Fullscreen      | Gibt an, dass eine Vollbildanzeige verwendet werden soll. Verwenden Sie dieses Flag nur bei der Wiedergabe komprimierter Dateien. (Nicht komprimierte Dateien werden nicht im Vollbildmodus angezeigt.)                                                                                                                                                                                                                                                                                                  |
| wiederholen          | Gibt an, dass die Wiedergabe neu gestartet werden soll, wenn das Ende des Inhalts erreicht ist.                                                                                                                                                                                                                                                                                                                                                                       |
| reverse         | Gibt an, dass die Wiedergaberichtung rückwärts ist. Sie können keine Endposition mit dem Flag "reverse" angeben. Bei videodiscs gilt "scan" nur für das CAV-Format.                                                                                                                                                                                                                                                                                     |
| Scan            | Spielt so schnell wie möglich ab, ohne Video zu deaktivieren (obwohl Audio möglicherweise deaktiviert ist). Bei videodiscs gilt "scan" nur für das CAV-Format.                                                                                                                                                                                                                                                                                                             |
| langsam            | Wird langsam abspielt. Um die genaue Geschwindigkeit eines videodisc-Players zu bestimmen, verwenden Sie das Flag "speed" des [Statusbefehls.](status.md) Um die Geschwindigkeit genauer anzugeben, verwenden Sie das Flag "speed" dieses Befehls. Bei videodiscs gilt "langsam" nur für das CAV-Format.                                                                                                                                                                                            |
| speed *integer* | Gibt eine Videodisc mit der angegebenen Geschwindigkeit in Frames pro Sekunde wieder. Dieses Flag gilt nur für CAV-Datenträger.                                                                                                                                                                                                                                                                                                                                                 |
| nach *Position*   | Gibt eine Endposition für die Wiedergabe an. Wenn das To-Flag nicht angegeben ist, wird die Wiedergabe am Ende des Inhalts beendet. Wenn **bei cdaudio-Geräten** die Position "to" größer als die Endposition des Datenträgers ist, gibt der Treiber einen Fehler zurück. Bei **Videodisc-Geräten** befinden sich die Standardpositionen in Frames für CAV-Datenträger und in Stunden, Minuten und Sekunden für CLV-Datenträger.                                                                  |
| Fenster          | Gibt an, dass bei der Wiedergabe das der Geräteinstanz zugeordnete Fenster verwendet werden soll. Dies ist die Standardeinstellung.                                                                                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für digital-video- und VCR-Geräte kann auch "test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Vor dem Ausführen von Befehlen, die Positionswerte verwenden, sollten Sie das gewünschte Zeitformat mit dem [Set-Befehl](set.md) festlegen. Dieser Befehl beginnt mit der aktuellen Geschwindigkeit, wie mit dem festgelegten Befehl "speed" festgelegt. Die Richtung ist umgekehrt, wenn das Flag "reverse" angegeben ist, oder wenn das "to"-Flag als Wert kleiner als das "from"-Flag angegeben ist. Wenn das Flag "from" nicht angegeben ist, beginnt die Wiedergabe an der aktuellen Position. Die Flags "to" und "reverse" können nicht zusammen verwendet werden.

## <a name="examples"></a>Beispiele

Der folgende Befehl gibt das Gerät "mysound" von Position 1000 bis Position 2000 wieder und sendet eine Benachrichtigung, wenn die Wiedergabe abgeschlossen ist.

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

[Mci](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> <dt>

[Hinweis](cue.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

