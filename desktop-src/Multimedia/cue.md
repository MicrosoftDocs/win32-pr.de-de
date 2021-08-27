---
title: cue-Befehl
description: Der Cue-Befehl bereitet die Wiedergabe oder Aufzeichnung vor. Digital-Video-, VCR- und Waveform-Audio-Geräte erkennen diesen Befehl.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- Cue-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6398d4773b6c92332e8a95996e4d81941a073fe
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467857"
---
# <a name="cue-command"></a>cue-Befehl

Der Cue-Befehl bereitet die Wiedergabe oder Aufzeichnung vor. Digital-Video-, VCR- und Waveform-Audio-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*
</dt> <dd>

Flag, das ein Gerät für die Wiedergabe oder Aufzeichnung vorbereitet. Die folgende Tabelle enthält Gerätetypen, die den **Cue-Befehl** und die von den einzelnen Typen verwendeten Flags erkennen.




| Wert | Position (Cue) | Position (Cue) | 
|-------|-----|-----|
| digitalvideo | <ul><li>input</li><li>Noshow</li></ul> | <ul><li>output</li><li>, um <em>zu positionieren</em></li></ul> | 
| Vcr | <ul><li>from <em>position</em></li><li>input</li><li>output</li></ul> | <ul><li>Preroll</li><li>reverse</li><li>, um <em>zu positionieren</em></li></ul> | 
| Waveaudio | input | output | 




 

Die folgende Tabelle enthält die Flags, die im *lpszInOutTo-Parameter* angegeben werden können, und ihre Bedeutungen.



| Wert           | Bedeutung                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| from *position* | Gibt an, wo begonnen werden soll.                                                                                                                                                                                                                                                                                      |
| input           | Bereitet die Aufzeichnung vor. Bei Digitalvideogeräten kann dieses Flag ausgelassen werden, wenn die aktuelle Präsentationsquelle bereits die externe Eingabe ist.                                                                                                                                                                  |
| Noshow          | Bereitet die Wiedergabe eines Frames vor, ohne ihn anzuzeigen. Wenn dieses Flag angegeben wird, zeigt die Anzeige weiterhin das Bild im Framepuffer an, obwohl der entsprechende Frame nicht die aktuelle Position ist. Ein nachfolgender Cue-Befehl ohne dieses Flag und ohne das Flag "to" zeigt den aktuellen Frame an. |
| output          | Bereitet die Wiedergabe vor. Wenn weder "input" noch "output" angegeben ist, ist die Standardeinstellung "output".                                                                                                                                                                                                           |
| Preroll         | Verschiebt den Prerollabstand von der *punktübergreifenden*. Der Punkt ist die aktuelle Position oder die position, die durch das Flag "from" angegeben wird.                                                                                                                                                                            |
| reverse         | Gibt an, dass die Wiedergaberichtung umgekehrt (rückwärts) ist.                                                                                                                                                                                                                                                             |
| , um *zu positionieren*   | Verschiebt den Arbeitsbereich an die angegebene Position. Bei VCR-Geräten gibt dieses Flag an, wo beendet werden soll.                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für DigitalVideo- und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Obwohl dies nicht erforderlich ist, kann das Ausgeben des Cue-Befehls vor der Wiedergabe oder Aufzeichnung auf einigen Geräten die Verzögerung verringern, bevor das Gerät die Aktion startet.

Dieser Befehl schlägt fehl, wenn die Wiedergabe oder Aufzeichnung ausgeführt wird oder das Gerät angehalten wird.

Beim Cueing für die Wiedergabe (mit dem Hinweis "output") wird der Cue-Befehl durch Ausgeben des [Wiedergabebefehls](play.md) mit dem Flag "from", "to" oder "reverse" abgebrochen.

Beim Cueing für die Aufzeichnung (mithilfe von "input") wird der Befehl ["record"](record.md) mit dem Flag "from", "to" oder "initialize" abgebrochen.

## <a name="examples"></a>Beispiele

Mit dem folgenden Befehl wird das Gerät "mysound" für die Aufzeichnung vorbereitet.

``` syntax
cue mysound input
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> <dt>

[Spielen](play.md)
</dt> <dt>

[record](record.md)
</dt> </dl>

 

