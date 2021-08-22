---
title: Restore-Befehl
description: Der Wiederherstellungsbefehl kopiert ein Standbild aus einer Datei in den Framepuffer. Dies ist die Umkehrung des Aufzeichnungsbefehls. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: e84a478a-3e0f-4767-94d7-eb3c79c31b8b
keywords:
- Restore-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e82fdec2480cfe2fc1b41901872aef7e41ee468d1adc3924df17a27e40031e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689190"
---
# <a name="restore-command"></a>Restore-Befehl

Der Wiederherstellungsbefehl kopiert ein Standbild aus einer Datei in den Framepuffer. Dies ist die [](capture.md) Umkehrung des Aufzeichnungsbefehls. Digitalvideogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("restore %s %s %s"), 
  lpszDeviceID, 
  lpszRestore, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*
</dt> <dd>

Mindestens eines der folgenden Flags.



| Wert           | Bedeutung                                                                                                                                                                                                                                                                                                                         |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| am *Rechteck*  | Gibt ein Rechteck relativ zum Framepufferursprung an. Das *Rechteck* wird als *X1 Y1 X2 Y2* angegeben. Die Koordinaten *X1 Y1* geben die obere linke Ecke und die Koordinaten *X2 Y2* die Breite und Höhe an. Wenn dieses Flag nicht verwendet wird, wird das Bild in die obere linke Ecke des Rahmenpuffers kopiert.<br/> |
| aus *Dateiname* | Gibt den Imagedateinamen an, der abgerufen werden soll. Dieses Flag ist erforderlich.                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify", "test" oder eine Kombination dieser sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Geräte können eine Vielzahl von Bildformaten erkennen. eine Windows geräteunabhängige Bitmap wird immer erkannt.

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

[Erfassen](capture.md)
</dt> </dl>

 

