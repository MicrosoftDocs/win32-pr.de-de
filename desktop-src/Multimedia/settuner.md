---
title: settuner-Befehl
description: Der Befehl settuner ändert den aktuellen Tuner oder die Kanaleinstellung des aktuellen Tuners. VCR-Geräte erkennen diesen Befehl.
ms.assetid: 76d05210-3c2a-4d00-b3eb-c912c1deabf7
keywords:
- settuner-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- settuner
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7075de6ed50c49773a502ba77e093d84e85b079a6b17c462ea8ee65ad1330aa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688799"
---
# <a name="settuner-command"></a>settuner-Befehl

Der Befehl settuner ändert den aktuellen Tuner oder die Kanaleinstellung des aktuellen Tuners. VCR-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszTuner"></span><span id="lpsztuner"></span><span id="LPSZTUNER"></span>*lpszTuner*
</dt> <dd>

Eines der folgenden Flags.



| Wert                            | Bedeutung                                                                                                                                                                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Kanalkanal*                | Legt den Tuner auf *channel* fest. Je nach VCR können Sie den Kanal während der Aufzeichnung möglicherweise nicht ändern. Ein Kanal, der größer als das Maximum ist, legt den Tuner auf den maximalen Kanal fest.                                                                                                                    |
| Channel seek upchannel seek down | Sucht den nächsten Kanal mit einem gültigen Signal. "Suchen nach" erhöht die Kanalnummer in seiner Suche. "Suchen nach unten" dekrementiert die Kanalnummer in der Suche. Der Tuner umschließt den Kanal 1, wenn die maximale Kanalnummer überschritten wird. Auf ähnliche Weise umschließt der Tuner bei der Suche nach unten den maximalen Kanal. |
| Kanal upchannel down           | Erhöht oder dekrementiert den Tunerkanal. Je nach VCR können Sie den Kanal während der Aufzeichnung möglicherweise nicht ändern. Der Tuner umschließt den Kanal 1, wenn die maximale Kanalnummer überschritten wird. Auf ähnliche Weise umschließt der Tuner bei der Suche nach unten den maximalen Kanal.                              |
| number *number*                  | Gibt den Tuner an, der vom settuner-Befehl betroffen sein soll. Wenn *number* nicht angegeben wird, wird der Standardwert 1 angenommen.                                                                                                                                                                                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify", "test" oder eine Kombination dieser sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

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

 

