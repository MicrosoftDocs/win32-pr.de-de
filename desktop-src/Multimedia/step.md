---
title: Schrittbefehl
description: Mit dem Schrittbefehl wird die Wiedergabe mindestens eines Frames vorwärts oder umgekehrt ausgeführt. Die Standardaktion besteht im Schrittweisen Vorwärtsschritt eines Frames. Videodisc-Geräte im Digital-Video-, VCR- und CAV-Format erkennen diesen Befehl.
ms.assetid: 6017ace5-cde9-42a0-bb2f-f85d7847adc5
keywords:
- Step-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b804ac64c2641ba1eb43ba7019ae2668c04a7d8b07fbfd20ab7b8cb570d8fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370830"
---
# <a name="step-command"></a>Schrittbefehl

Mit dem Schrittbefehl wird die Wiedergabe mindestens eines Frames vorwärts oder umgekehrt ausgeführt. Die Standardaktion besteht im Schrittweisen Vorwärtsschritt eines Frames. Videodisc-Geräte im Digital-Video-, VCR- und CAV-Format erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) mit dem *lpszCommand-Parameter* auf, der wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszStepFlags"></span><span id="lpszstepflags"></span><span id="LPSZSTEPFLAGS"></span>*lpszStepFlags*
</dt> <dd>

Eines oder beide der folgenden Flags.



| Wert       | Bedeutung                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------|
| nach *Frames* | Gibt die Anzahl der frames an, für die ein Schrittschritt verwendet werden soll. Wenn Sie einen negativen *Frameswert angeben,* können Sie das Flag "umgekehrt" nicht angeben. |
| reverse     | Einzelschritt für die Frames in umgekehrter Reihenfolge.                                                                                              |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für digital-video- und VCR-Geräte kann auch "test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

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
</dt> </dl>

 

