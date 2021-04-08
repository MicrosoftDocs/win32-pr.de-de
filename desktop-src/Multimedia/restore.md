---
title: Restore-Befehl
description: Der Restore-Befehl kopiert ein Bild aus einer Datei in den Frame Puffer. Dies ist das Gegenteil des Aufzeichnungs Befehls. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: e84a478a-3e0f-4767-94d7-eb3c79c31b8b
keywords:
- Restore-Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2d7f0f236b26e3e73807b32485442d597e93d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949442"
---
# <a name="restore-command"></a>Restore-Befehl

Der Restore-Befehl kopiert ein Bild aus einer Datei in den Frame Puffer. Dies ist das Gegenteil des [Aufzeichnungs](capture.md) Befehls. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszrestore*
</dt> <dd>

Mindestens eines der folgenden Flags.



| Wert           | Bedeutung                                                                                                                                                                                                                                                                                                                         |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at- *Rechteck*  | Gibt ein Rechteck relativ zum Frame Puffer Ursprung an. Das *Rechteck* wird als *x1 y1 x2 Y2* angegeben. Die Koordinaten *x1 y1* geben die linke obere Ecke an, und die Koordinaten *x2 Y2* geben die Breite und Höhe an. Wenn dieses Flag nicht verwendet wird, wird das Bild in die linke obere Ecke des Frame Puffers kopiert.<br/> |
| *Dateiname* | Gibt den Namen des zu Rückruf Bilds an. Dieses Flag ist erforderlich.                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify", "Test" oder eine Kombination daraus sein. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Geräte können eine Vielzahl von Bildformaten erkennen. eine Windows-geräteunabhängige Bitmap wird immer erkannt.

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

[einver](capture.md)
</dt> </dl>

 

