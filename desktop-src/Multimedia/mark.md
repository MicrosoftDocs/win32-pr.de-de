---
title: Befehl "markieren"
description: Der Mark-Befehl steuert das Aufzeichnen und Löschen von Markierungen auf dem Videotape. VCR-Geräte erkennen diesen Befehl.
ms.assetid: d5f7a546-dc46-459c-b5dc-0651bca842cb
keywords:
- Mark-Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- mark
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570968af05424597a7fe2b59e86e0364694e0e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339960"
---
# <a name="mark-command"></a>Befehl "markieren"

Der Mark-Befehl steuert das Aufzeichnen und Löschen von Markierungen auf dem Videotape. VCR-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszmark*
</dt> <dd>

Eines der folgenden Flags.



| Wert | Bedeutung                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| erase | Löscht eine Markierung an der aktuellen Position, sofern vorhanden. Um eine Markierung zu löschen, suchen Sie zuerst nach der Markierung, und geben Sie dann den Befehl "Löschen" der Markierung aus. |
| Schreiben | Schreibt eine Markierung an der aktuellen Position. Der VCR muss sich möglicherweise im Wiedergabe-oder Aufzeichnungsmodus befinden, damit dieser Befehl erfolgreich ausgeführt wird.                    |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder "Test" lauten. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Markierungen sind spezielle Signale, die in den Inhalt geschrieben werden, der von VCR bei hoch Geschwindigkeits suchen erkannt werden kann. Marken sind VCR-spezifisch.

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

 

