---
title: Schritt Befehl
description: Der Schritt Befehl führt Sie durch die Schritte zum Wiedergeben eines oder mehrerer Frames vor oder nach vorne. Die Standardaktion besteht darin, einen Frame vorwärts zu Stufen. Videodisk-Geräte Digital Video, VCR und CAV-Format erkennen diesen Befehl.
ms.assetid: 6017ace5-cde9-42a0-bb2f-f85d7847adc5
keywords:
- Schritt Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6203d0b2d5dea401e8197e1261946955cd28618a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476584"
---
# <a name="step-command"></a>Schritt Befehl

Der Schritt Befehl führt Sie durch die Schritte zum Wiedergeben eines oder mehrerer Frames vor oder nach vorne. Die Standardaktion besteht darin, einen Frame vorwärts zu Stufen. Videodisk-Geräte Digital Video, VCR und CAV-Format erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("step %s %s %s"), 
  lpszDeviceID, 
  lpszStepFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszstepflags*
</dt> <dd>

Eines oder beide der folgenden Flags.



| Wert       | Bedeutung                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| nach *Frames* | Gibt die Anzahl der zu schrifenden Rahmen an. Wenn Sie einen negativen *Rahmen* Wert angeben, können Sie das Flag "Reverse" nicht angeben. |
| reverse     | Ändern Sie die Frames in umgekehrter Reihenfolge.                                                                                              |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

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

 

