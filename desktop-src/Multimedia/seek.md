---
title: Seek-Befehl
description: Der Seek-Befehl wechselt an die angegebene Position und wird beendet. CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: e9e8ca14-d181-4f29-b4d3-c7f5b0301164
keywords:
- Seek-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- seek
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40f3467d328e161245e77217b4ce6edfa9665ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391545"
---
# <a name="seek-command"></a>Seek-Befehl

Der Seek-Befehl wechselt an die angegebene Position und wird beendet. CD-Audiodateien, Digital Video, MIDI Sequencer, VCR, Videodisk und Waveform-Audiogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("seek %s %s %s"), 
  lpszDeviceID, 
  lpszSeekFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszSeekFlags"></span><span id="lpszseekflags"></span><span id="LPSZSEEKFLAGS"></span>*lpszseekflags*
</dt> <dd>

Flag zum Verschieben an eine angegebene Position. In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den **Seek** -Befehl und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung                          | Bedeutung                      |
|--------------|----------------------------------|------------------------------|
| CDAudio      | bis zum Ende der *Position*             | zum Starten                     |
| Digitalvideo | bis zum Ende der *Position*             | zum Starten                     |
| sequencer    | bis zum Ende der *Position*             | zum Starten                     |
| VCR          | zum *Zeitpunkt* der Markierung von *\_ NUM* | So beenden Sie die *Position* zum Starten |
| Videodisk    | zum Ende umkehren                   | so *Positionieren* Sie den Start        |
| waveaudiodatei    | bis zum Ende der *Position*             | zum Starten                     |



 

In der folgenden Tabelle werden die Flags aufgelistet, die im **lpszseekflags** -Parameter und deren Bedeutung angegeben werden können.



| Wert            | Bedeutung                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| zum *Zeitpunkt*        | Gibt an, wann das Gerät mit der Ausführung dieses Befehls beginnen soll, oder ob das Gerät beim Start des Geräts gecuht wurde. Weitere Informationen finden Sie [unter dem Hinweis](cue.md) Befehl.                             |
| Markierung Nr. *\_ NUM* | Sucht die relative Markierung, die von *Mark \_ NUM* angegeben wird. Dies muss ein positiver ganzzahliger Wert sein. Markierungen sind Signale, die mithilfe des Befehls [Markieren](mark.md) auf das VCR-Band geschrieben werden und für die schnelle Suche verwendet werden. |
| reverse          | Gibt an, dass die Suchrichtung auf VCRs-und CAV-Videodisks rückwärts verläuft. Dieses Flag ist ungültig, wenn das Flag "to" angegeben wird. Für VCRs muss dieses Flag mit dem Flag "Mark" verwendet werden.                             |
| zum Ende           | Sucht am Ende des Inhalts.                                                                                                                                                                                 |
| an *Position*    | Gibt die Position an, an der die Suche beendet wird. Bei **CDAudio** -Geräten gibt MCI einen Fehler außerhalb des gültigen Bereichs zurück, wenn die angegebene Position größer als die Länge der Festplatte ist.                                            |
| zum Starten         | Versucht, den Inhalt zu starten.                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Vor dem Ausgeben von Befehlen, die Positionswerte verwenden, sollten Sie das gewünschte Zeitformat mithilfe des [Set](set.md) -Befehls festlegen.

Digital Video-Geräte unterstützen zwei Suchmodi, die Sie mit dem [Set](set.md) -Befehl ändern können. Der "Seek genau on"-Modus bewirkt, dass der Seek-Befehl in den angegebenen Frame verschoben wird. Der Modus "suchen genau aus" bewirkt, dass der Seek-Befehl in den nächstgelegenen Keyframe vor dem angegebenen Frame verschoben wird.

Wenn ein CD-Audiogerät abgespielt wird, wenn der Seek-Befehl ausgegeben wird, wird die Wiedergabe angehalten. Wenn der Befehl "Seek" mit einem Video Disk-Gerät ausgegeben wird, sucht das Gerät mithilfe von "schneller vorwärts" oder "schneller umkehren" mit Video-und Audiodaten.

Wenn der Seek-Befehl mit einem Waveform-Audiogerät ausgegeben wird, hängt das Verhalten von der Stichprobengröße ab. Wenn die Stichprobengröße 16 Bits oder größer ist, wird die Suche bis zum Anfang des nächsten Beispiels fortgesetzt, wenn eine angegebene Position nicht mit dem Anfang eines Beispiels übereinstimmt.

## <a name="examples"></a>Beispiele

Der folgende Befehl sucht am Anfang der Mediendatei, die dem "mysound"-Gerät zugeordnet ist.

``` syntax
seek mysound to start
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

[mark](mark.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

