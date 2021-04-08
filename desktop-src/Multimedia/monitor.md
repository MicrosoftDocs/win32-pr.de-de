---
title: Monitor Befehl
description: Der Monitor-Befehl gibt die Präsentations Quelle an. (Die Standard Präsentations Quelle ist der Arbeitsbereich.) Wenn Sie die Präsentations Quelle wechseln, werden alle Audio-und Videostreams in der Quelle gewechselt. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 5cacbe88-b94e-4101-badf-2bb4796b19cf
keywords:
- Monitor Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- monitor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ccbe1d8919c232ab88d04081dad242944868893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741425"
---
# <a name="monitor-command"></a>Monitor Befehl

Der Monitor-Befehl gibt die Präsentations Quelle an. (Die Standard Präsentations Quelle ist der Arbeitsbereich.) Wenn Sie die Präsentations Quelle wechseln, werden alle Audio-und Videostreams in der Quelle gewechselt. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszMonitor"></span><span id="lpszmonitor"></span><span id="LPSZMONITOR"></span>*lpszmonitor*
</dt> <dd>

Mindestens eines der folgenden Flags.



| Wert           | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| file            | Gibt an, dass der Arbeitsbereich die Präsentations Quelle ist. Dies ist die Standard Quelle.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| input           | Gibt an, dass die externe Eingabe die Präsentations Quelle ist. Wenn ein [Wiedergabe](play.md) Befehl ausgeführt wird, wird er zuerst angehalten. Wenn [setvideo](setvideo.md) "on" ist, zeigt dieses Flag ein standardmäßiges ausgeblendetes Fenster an. Geräte können beim Überwachen von Eingaben möglicherweise die Vorgänge anderer Geräte Instanzen einschränken.                                                                                                                                                                                                                                                                                                                                                                    |
| method- *Methode* | Bei Verwendung mit dem **Monitor** "Input" wählt dieses Flag die Methode für die Überwachung aus. Die *Methode* ist entweder "Pre", "Post" oder "Direct". Die direkte Überwachung verlangt, dass das Gerät während der Überwachung für die optimale Anzeigequalität konfiguriert wird. Die direkte Überwachungsmethode ist möglicherweise nicht mit der Motion-Videoaufzeichnung kompatibel. Videoaufzeichnung vor und nach der Überwachung zulassen Vor der Überwachung wird die externe Eingabe vor der Komprimierung angezeigt, während nach der Überwachung die externe Eingabe nach der Komprimierung angezeigt wird. In der Regel haben unterschiedliche Überwachungsmethoden andere Auswirkungen auf die Hardware. Die Standard Überwachungsmethode wird vom Gerät ausgewählt.<br/> |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify", "Test" oder eine Kombination daraus sein. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die Präsentations Quelle wechselt automatisch zum Arbeitsbereich, nachdem eine [Wiedergabe](play.md), ein [Schritt](step.md), eine [Pause](pause.md), ein Hinweis "Output" oder ein [Such](seek.md) Befehl [angezeigt wurde.](cue.md) Der [Datensatz](record.md) -Befehl wechselt nicht automatisch in die Präsentations Quellen, was Ihrer Anwendung die Möglichkeit bietet, während der Aufzeichnung keine Videos anzuzeigen.

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

[STI](cue.md)
</dt> <dt>

[pause](pause.md)
</dt> <dt>

[Theater](play.md)
</dt> <dt>

[record](record.md)
</dt> <dt>

[einzuholen](seek.md)
</dt> <dt>

[Schritt](step.md)
</dt> </dl>

 

