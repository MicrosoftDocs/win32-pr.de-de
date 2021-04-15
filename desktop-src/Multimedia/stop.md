---
title: Befehl "Befehl"
description: Der Befehl "beenden" beendet die Wiedergabe oder Aufzeichnung. CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.
ms.assetid: 82b2da63-f1ac-48f3-a206-6c5cfe00f5be
keywords:
- Befehl "Befehl" für Windows Multimedia
topic_type:
- apiref
api_name:
- stop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79d70aa150c01bd4c0ceab10332b4eca8b15d041
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391903"
---
# <a name="stop-command"></a>Befehl "Befehl"

Der Befehl "beenden" beendet die Wiedergabe oder Aufzeichnung. CD-Audiodateien, Digital Video, MIDI Sequencer, Videodisk, VCR und Waveform-Audiogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("stop %s %s %s"), 
  lpszDeviceID, 
  lpszStopFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszstopflags*
</dt> <dd>

Bei Digital-Video-Geräten kann es sich um das folgende Flag handeln:



| Wert | Bedeutung                                                                                                                                                                                      |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| verfügen  | Verhindert das Freigeben von Ressourcen, die erforderlich sind, um ein Bild auf dem Bildschirm neu zu zeichnen. Der Frame Puffer bleibt für die Aktualisierung der Anzeige verfügbar, wenn beispielsweise das Fenster verschoben wird. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Bei CD-Audiogeräten beendet der Befehl "beenden" die Wiedergabe und setzt die aktuelle Position des Titels auf NULL zurück.

## <a name="examples"></a>Beispiele

Der folgende Befehl beendet die Wiedergabe oder Aufzeichnung auf dem Gerät "mysound".

``` syntax
stop mysound
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
</dt> </dl>

 

