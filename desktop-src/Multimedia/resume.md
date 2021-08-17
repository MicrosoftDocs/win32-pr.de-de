---
title: Resume-Befehl
description: Der Befehl resume setzt die Wiedergabe oder Aufzeichnung auf einem Gerät fort, das mit dem Befehl pause angehalten wurde.
ms.assetid: 0a2cdd23-8c1d-4d9e-9b63-3fdcbb13e3a2
keywords:
- Befehl "resume" Windows Multimedia
topic_type:
- apiref
api_name:
- resume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e4a728e3ca89e2b4ddc21809830d5af3be9a2b04e004f99d5a792a9be5da01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801892"
---
# <a name="resume-command"></a>Resume-Befehl

Der Befehl resume setzt die Wiedergabe oder Aufzeichnung auf einem Gerät fort, das mit dem Befehl [pause](pause.md) angehalten wurde. Digital-Video-, VCR- und Waveform-Audio-Geräte erkennen diesen Befehl. Obwohl CD-Audio-, GIGABYTE-Sequencer- und Videodisc-Geräte diesen Befehl ebenfalls erkennen, unterstützen die McICDA-, MCISEQ- und MCIPIONR-Gerätetreiber diesen Befehl nicht.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("resume %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für DigitalVideo- und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="examples"></a>Beispiele

Der folgende Befehl setzt die Wiedergabe oder Aufzeichnung des Geräts "newsound" fort.

``` syntax
resume newsound
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

[pause](pause.md)
</dt> </dl>

 

