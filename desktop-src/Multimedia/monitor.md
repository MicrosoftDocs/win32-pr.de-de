---
title: Befehl "monitor"
description: Der Monitorbefehl gibt die Präsentationsquelle an. (Die Standardpräsentationsquelle ist der Arbeitsbereich.) Wenn Sie die Präsentationsquelle wechseln, werden alle Audio- und Videostreams in der Quelle gewechselt. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- Monitorbefehl Windows Multimedia
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef9a47db68856196dc84aefb3c5f110941189dec80f62b369eae13c60932d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038810"
---
# <a name="monitor-command"></a>Befehl "monitor"

Der Monitorbefehl gibt die Präsentationsquelle an. (Die Standardpräsentationsquelle ist der Arbeitsbereich.) Wenn Sie die Präsentationsquelle wechseln, werden alle Audio- und Videostreams in der Quelle gewechselt. Digitalvideogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("monitor %s %s %s"), 
  lpszDeviceID, 
  lpszMonitor, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszMonitor*
</dt> <dd>

Mindestens eines der folgenden Flags.



| Wert           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| file            | Gibt an, dass der Arbeitsbereich die Präsentationsquelle ist. Dies ist die Standardquelle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| input           | Gibt an, dass die externe Eingabe die Präsentationsquelle ist. Wenn ein [Wiedergabebefehl](play.md) ausgeführt wird, wird er zunächst angehalten. Wenn [setvideo](setvideo.md) auf "on" festgelegt ist, zeigt dieses Flag ein ausgeblendetes Standardfenster an. Geräte können die Möglichkeiten anderer Geräteinstanzen beim Überwachen von Eingaben einschränken.                                                                                                                                                                                                                                                                                                                                                                    |
| *-Methode* | Bei Verwendung mit **monitor** "input" wählt dieses Flag die Überwachungsmethode aus. Die *Methode* ist entweder "pre", "post" oder "direct". Die direkte Überwachung fordert an, dass das Gerät während der Überwachung für eine optimale Anzeigequalität konfiguriert wird. Die direkte Überwachungsmethode ist möglicherweise nicht mit der Aufzeichnung von Bewegungsvideos kompatibel. Die Vor- und Nachüberwachung ermöglicht die Aufzeichnung von Bewegungsvideos. Bei der Vorabüberwachung wird die externe Eingabe vor der Komprimierung angezeigt, während nach der Überwachung die externe Eingabe nach der Komprimierung angezeigt wird. In der Regel haben unterschiedliche Überwachungsmethoden unterschiedliche Auswirkungen auf die Hardware. Die Standardüberwachungsmethode wird vom Gerät ausgewählt.<br/> |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify", "test" oder eine Kombination dieser sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die Präsentationsquelle wechselt automatisch zum Arbeitsbereich, nachdem ein [Wiedergabe-, Schritt-,](step.md) [Pausen-,](pause.md) [Cue-Befehl](cue.md) "output" oder [seek](seek.md) ausgeführt wurde. [](play.md) Der [Datensatzbefehl](record.md) wechselt nicht automatisch die Präsentationsquellen, was Ihrer Anwendung die Möglichkeit gibt, während der Aufzeichnung kein Video zu zeigen.

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
</dt> <dt>

[Hinweis](cue.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Spielen](play.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[Suchen](seek.md)
</dt> <dt>

[Schritt](step.md)
</dt> </dl>

 

