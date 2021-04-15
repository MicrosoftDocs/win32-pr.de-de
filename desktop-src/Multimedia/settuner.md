---
title: settuner-Befehl
description: Der settuner-Befehl ändert den aktuellen Tuner oder die channeleinstellung des aktuellen Tuners. VCR-Geräte erkennen diesen Befehl.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- settuner-Befehl, Windows Multimedia
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51150043a68f3cd34525eb74a64237fc4dc150e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479368"
---
# <a name="settuner-command"></a>settuner-Befehl

Der settuner-Befehl ändert den aktuellen Tuner oder die channeleinstellung des aktuellen Tuners. VCR-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settuner %s %s %s"), 
  lpszDeviceID, 
  lpszTuner, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpsztuner*
</dt> <dd>

Eines der folgenden Flags.



| Wert                            | Bedeutung                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *kanalchannel*                | Legt den Tuner auf *Channel* fest. Abhängig vom VCR ist es möglicherweise nicht möglich, den Kanal während der Aufzeichnung zu ändern. Ein Kanal, der größer als der Höchstwert ist, legt den Tuner auf den maximalen Kanal fest.                                                                                                                    |
| Channel Seek-upchannel-Suche nach unten | Sucht den nächsten Kanal mit einem gültigen Signal. "Suchen" erhöht die Kanalnummer in der Suche. "Suchen" Dekremente die Kanalnummer in der Suche. Der Tuner wird mit Channel 1 umschlossen, wenn die maximale Kanalnummer überschritten wird. Entsprechend umschließt der Tuner bei der Suche den maximalen Kanal. |
| Kanal-upchannel nach unten           | Inkrement oder Dekrement für den tunkanchannel. Abhängig vom VCR ist es möglicherweise nicht möglich, den Kanal während der Aufzeichnung zu ändern. Der Tuner wird mit Channel 1 umschlossen, wenn die maximale Kanalnummer überschritten wird. Entsprechend umschließt der Tuner bei der Suche den maximalen Kanal.                              |
| Zahlen *Nummer*                  | Gibt den Tuner an, der vom settuner-Befehl beeinflusst werden soll. Wenn *Number* nicht angegeben wird, wird der Standardwert 1 angenommen.                                                                                                                                                                                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify", "Test" oder eine Kombination daraus sein. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

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

 

