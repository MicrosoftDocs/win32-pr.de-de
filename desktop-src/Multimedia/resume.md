---
title: Resume-Befehl
description: Der Resume-Befehl setzt die Wiedergabe oder Aufzeichnung auf einem Gerät fort, das mithilfe des Pause-Befehls angehalten wurde.
ms.assetid: 0a2cdd23-8c1d-4d9e-9b63-3fdcbb13e3a2
keywords:
- Befehl "fortsetzen" Windows Multimedia
topic_type:
- apiref
api_name:
- resume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f01fd96e2b25e191608c7c6abf70bfd842158d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338116"
---
# <a name="resume-command"></a>Resume-Befehl

Der Resume-Befehl setzt die Wiedergabe oder Aufzeichnung auf einem Gerät fort, das mithilfe des [Pause](pause.md) -Befehls angehalten wurde. Mit Digital Video-, VCR-und Waveform-Audiogeräten wird dieser Befehl erkannt. Obwohl die Geräte von CD-Audiodaten, MIDI-Sequencer und Videodisc diesen Befehl ebenfalls erkennen, unterstützen die Gerätetreiber mcicda, mcitarq und mcipionr Sie nicht.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="examples"></a>Beispiele

Mit dem folgenden Befehl wird die Wiedergabe oder Aufzeichnung des "Newsound"-Geräts fortgesetzt.

``` syntax
resume newsound
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

[pause](pause.md)
</dt> </dl>

 

