---
title: Freeze-Befehl
description: Der Befehl freeze friert video input or video output on a VCR (Videoeingabe oder Videoausgabe auf einem VCR) ein oder deaktiviert die Videoerfassung für den Framepuffer. Digital-Video-, Video-Overlay- und VCR-Geräte erkennen diesen Befehl.
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- Freeze-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1261cc75575a5b59d200ff965a5325caef9fa966
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481556"
---
# <a name="freeze-command"></a>Freeze-Befehl

Der Befehl freeze friert video input or video output on a VCR (Videoeingabe oder Videoausgabe auf einem VCR) ein oder deaktiviert die Videoerfassung für den Framepuffer. Digital-Video-, Video-Overlay- und VCR-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*
</dt> <dd>

Flag, das angibt, was fixiert werden soll. Die folgende Tabelle enthält Gerätetypen, die den **Freeze-Befehl** und die von den einzelnen Typen verwendeten Flags erkennen.




| Wert | Bedeutung | Bedeutung | 
|-------|---------|---------|
| digitalvideo | am <em>Rechteck</em> | Außerhalb | 
| overlay | am <em>Rechteck</em> | 
| Vcr | <ul><li>Feld</li><li>frame</li></ul> | <ul><li>input</li><li>output</li></ul> | 




 

Die folgende Tabelle enthält die Flags, die im *lpszFreezeFlags-Parameter* angegeben werden können, und ihre Bedeutungen.



| Wert          | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| am *Rechteck* | Gibt den Bereich an, der eingefroren wird. Für Videoüberlagerungsgeräte ist die Videoerfassung in dieser Region deaktiviert. Bei Digitalvideogeräten ist das Sperrmaskenbit in den Pixeln innerhalb des Rechtecks aktiviert (es sei denn, das Flag "outside" ist angegeben). Das Rechteck ist relativ zum Ursprung des Videopuffers und wird als *X1 Y1 X2 Y2* angegeben. Die Koordinaten *X1 Y1* geben die obere linke Ecke des Rechtecks an, und die Koordinaten *X2 Y2* geben die Breite und Höhe an. |
| Feld          | Friert das erste Feld ein. Das Feld wird standardmäßig angenommen (wenn weder Frame noch Feld angegeben ist).                                                                                                                                                                                                                                                                                                                                                                                               |
| frame          | Friert den gesamten Frame ein und zeigt beide Felder an.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| input          | Friert den aktuellen Frame des Eingabebilds ein, unabhängig davon, ob es angehalten ist oder ausgeführt wird.                                                                                                                                                                                                                                                                                                                                                                                                                |
| output         | Friert den aktuellen Frame der Ausgabe des VCR ein. Wenn der VCR beim Einfrieren wiedergegeben wird, wird der aktuelle Frame fixiert, und der VCR wird angehalten. Wenn der VCR angehalten wird, wenn dieser Befehl ausgegeben wird, wird der aktuelle Frame fixiert. Das fixierte Bild verbleibt auf dem Ausgabegerät, bis ein Befehl zum Aufheben der [Freigabe](unfreeze.md) ausgegeben wird. Wenn weder "input" noch "output" angegeben ist, wird "output" angenommen.                                                                                    |
| Außerhalb        | Gibt an, dass der Bereich außerhalb des mit dem Flag "at" angegebenen Bereichs fixiert ist.                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für DigitalVideo- und VCR-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Bei Verwendung mit VCR-Geräten ist dieser Befehl für Frame-Grabb-Karten vorgesehen.

Um unregelmäßige Erfassungsregionen mit dem Flag "at" anzugeben, verwenden Sie eine Reihe von Befehlen zum Einfrieren und Aufheben der [Fixierung.](unfreeze.md) Einige Videoüberlagerungsgeräte beschränken die Komplexität der Kaufregion.

Dieser Befehl wird nur unterstützt, wenn ein Aufruf des [Funktionsbefehls](capability.md) mit dem Flag "can freeze" **TRUE** zurückgibt.

## <a name="examples"></a>Beispiele

Der folgende Befehl deaktiviert die Videoerfassung in einem Quadrat mit 100 Pixeln in der oberen linken Ecke des Videopuffers.

``` syntax
freeze vboard at 0 0 100 100
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

[capability](capability.md)
</dt> <dt>

[Auftauen](unfreeze.md)
</dt> </dl>

 

