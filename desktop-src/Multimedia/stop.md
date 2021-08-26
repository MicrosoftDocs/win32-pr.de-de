---
title: Befehl "stop"
description: Der Befehl stop beendet die Wiedergabe oder Aufzeichnung. CD-Audio-, Digital-Video-, SINUS Sequencer-, Videodisc-, VCR- und Waveform-Audio-Geräte erkennen diesen Befehl.
ms.assetid: 82b2da63-f1ac-48f3-a206-6c5cfe00f5be
keywords:
- Befehl "stop" Windows Multimedia
topic_type:
- apiref
api_name:
- stop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3091fcf3c58dc015450a9d585af48cc8347d4167bdd487c37dd3f7c6cd4f04e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037110"
---
# <a name="stop-command"></a>Befehl "stop"

Der Befehl stop beendet die Wiedergabe oder Aufzeichnung. CD-Audio-, Digital-Video-, SINUS Sequencer-, Videodisc-, VCR- und Waveform-Audio-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszStopFlags"></span><span id="lpszstopflags"></span><span id="LPSZSTOPFLAGS"></span>*lpszStopFlags*
</dt> <dd>

Bei Geräten mit digitalem Video kann dies das folgende Flag sein.



| Wert | Bedeutung                                                                                                                                                                                      |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Halten  | Verhindert die Freigabe von Ressourcen, die erforderlich sind, um ein Standbild auf dem Bildschirm neu zu zeichnen. Der Framepuffer bleibt für die Aktualisierung der Anzeige verfügbar, wenn z. B. das Fenster verschoben wird. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für DigitalVideo- und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Bei CD-Audiogeräten beendet der Befehl stop die Wiedergabe und setzt die aktuelle Titelposition auf 0 (null) zurück.

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

[Mci](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> </dl>

 

