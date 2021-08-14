---
title: Unfreeze-Befehl
description: Der Befehl unfreeze aktiviert die Videoerfassung erneut in den Framepuffer, nachdem er durch den Freeze-Befehl deaktiviert wurde. Digitalvideo-, VCR- und Videoüberlagerungsgeräte erkennen diesen Befehl.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- Befehl "unfreeze" Windows Multimedia
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88fe45b1346872483a4012c5f5d161dcd61020c64349fee254ae4bf337b4be8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370810"
---
# <a name="unfreeze-command"></a>Unfreeze-Befehl

Der Befehl unfreeze aktiviert die Videoerfassung erneut in den Framepuffer, nachdem er durch den [Freeze-Befehl](freeze.md) deaktiviert wurde. Digitalvideo-, VCR- und Videoüberlagerungsgeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("unfreeze %s %s %s"), 
  lpszDeviceID, 
  lpszUnfreeze, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*
</dt> <dd>

Flag für die erneute Videoerfassung in den Framepuffer. In der folgenden Tabelle sind die Gerätetypen aufgeführt, die den Befehl **unfreeze** und die von den einzelnen Typen verwendeten Flags erkennen.



| Wert        | Bedeutung        |
|--------------|----------------|
| digitalvideo | am *Rechteck* |
| overlay      | am *Rechteck* |
| Vcr          | Eingabeausgabe   |



 

Die folgende Tabelle enthält die Flags, die im **lpszUnfreeze-Parameter** angegeben werden können, und ihre Bedeutungen.



| Wert          | Bedeutung                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| am *Rechteck* | Gibt die Region an, in der die Videoerfassung wieder einseniert werden soll. Das Rechteck ist relativ zum Ursprung des Videopuffers und wird als *X1 Y1 X2 Y2* angegeben. Die Koordinaten *X1 Y1* geben die obere linke Ecke des Rechtecks und die Koordinaten *X2 Y2* die Breite und Höhe an. |
| input          | Aufheben des Fixierens des Eingabebilds.                                                                                                                                                                                                                                                                  |
| output         | Aufheben der Freigabe des Ausgabebilds. Wenn weder "input" noch "output" angegeben ist, wird "output" angenommen.                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für DigitalVideo- und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="examples"></a>Beispiele

Der folgende Befehl entpackt einen Bereich des Videopuffers.

``` syntax
unfreeze vboard at 10 20 90 165
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

[Einfrieren](freeze.md)
</dt> </dl>

 

