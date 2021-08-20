---
title: Befehl "mark"
description: Der Befehl mark steuert das Aufzeichnen und Löschen von Markierungen auf der Videoaufzeichnung. VCR-Geräte erkennen diesen Befehl.
ms.assetid: d5f7a546-dc46-459c-b5dc-0651bca842cb
keywords:
- Befehl "mark" Windows Multimedia
topic_type:
- apiref
api_name:
- mark
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f59f56a6d542120d088d764d1b301329a7f0b167f25952587a9e743878643e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138751"
---
# <a name="mark-command"></a>Befehl "mark"

Der Befehl mark steuert das Aufzeichnen und Löschen von Markierungen auf der Videoaufzeichnung. VCR-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("mark %s %s %s"), 
  lpszDeviceID, 
  lpszMark, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*
</dt> <dd>

Eines der folgenden Flags.



| Wert | Bedeutung                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| erase | Löscht eine Markierung an der aktuellen Position, sofern vorhanden. Um eine Markierung zu löschen, suchen Sie zuerst nach der Markierung und geben dann den Befehl "erase" aus. |
| Schreiben | Schreibt eine Markierung an der aktuellen Position. Der VCR muss sich möglicherweise im Wiedergabe- oder Aufzeichnungsmodus befinden, damit dieser Befehl erfolgreich ausgeführt werden kann.                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder "test" sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Markierungen sind spezielle Signale, die in den Inhalt geschrieben werden, die vom VCR bei schnell durchgeführten Suchvorgängen erkannt werden können. Markierungen sind VCR-spezifisch.

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

 

