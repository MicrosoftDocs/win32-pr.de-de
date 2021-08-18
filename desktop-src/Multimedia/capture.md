---
title: Capture-Befehl
description: Der Capture-Befehl kopiert den Inhalt des Framepuffers und speichert ihn in der angegebenen Datei. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- Capture-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68bc32fd247cbe3519fbffad778b33679e3b71c652b476f557db5a910e87721c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941518"
---
# <a name="capture-command"></a>Capture-Befehl

Der Capture-Befehl kopiert den Inhalt des Framepuffers und speichert ihn in der angegebenen Datei. Digitalvideogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) mit dem *lpszCommand-Parameter* auf, der wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capture %s %s %s"), 
  lpszDeviceID, 
  lpszCapture, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*
</dt> <dd>

Mindestens eines der folgenden Flags:



| Wert          | Bedeutung                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| als *Pfadname*  | Gibt den Zielpfad und dateinamen für das erfasste Bild an. Dieses Flag ist erforderlich.                                                                                                                                                                |
| am *Rechteck* | Gibt den rechteckigen Bereich innerhalb des Framepuffers an, der vom Gerät eniert und auf dem Datenträger gespeichert wird. Wenn nicht angegeben, wird der zugeschnittene Bereich standardmäßig auf das Rechteck festgelegt, das für einen vorherigen [Put-Befehl](put.md) "source" für diese Geräteinstanz angegeben oder standardmäßig festgelegt wurde. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify", "test" oder eine Kombination aus diesen sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Dieser Befehl kann fehlschlagen, wenn das Gerät gerade Bewegungsvideos abspielt oder einen anderen ressourcenintensiven Vorgang ausgeführt. Wenn der Framepuffer in Echtzeit aktualisiert wird, wird die Aktualisierung kurzzeitig angehalten, sodass ein vollständiges Bild erfasst wird. Wenn das Gerät die Aktualisierung anzuhalten, kann es einen visuellen oder akustischen Effekt geben. Wenn das Dateiformat, der Komprimierungsalgorithmus und die Qualitätsstufen nicht festgelegt wurden, werden ihre Standardwerte verwendet.

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

[put](put.md)
</dt> </dl>

 

