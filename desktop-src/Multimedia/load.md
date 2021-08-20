---
title: Befehl "load"
description: Der Befehl load lädt eine Datei in einem gerätespezifischen Format. Digital-Video- und Videoüberlagerungsgeräte erkennen diesen Befehl.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- Load-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c66822de727ea45e93839c710dae19739cba8adaac8b571846c1fa23ef0083c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139355"
---
# <a name="load-command"></a>Befehl "load"

Der Befehl load lädt eine Datei in einem gerätespezifischen Format. Digital-Video- und Videoüberlagerungsgeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) mit dem *lpszCommand-Parameter* auf, der wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("load %s %s %s"), 
  lpszDeviceID, 
  lpszFilePos, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*
</dt> <dd>

Pfad und Dateiname, der geladen werden soll. Bei Videoüberlagerungsgeräten kann dies auch ein Zielrechteck für die Daten enthalten. Um ein Zielrechteck anzugeben, geben Sie "at" gefolgt von **X1 Y1 X2 Y2** an, wobei **X1 Y1** die obere linke Ecke des Rechtecks und **X2 Y2** die Breite und Höhe angeben. Das Rechteck ist relativ zum Ursprung des Videopuffers.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digitalvideogeräte kann auch "test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Das Gerät "vidboard" sendet eine Benachrichtigung, wenn das Laden abgeschlossen ist.

## <a name="examples"></a>Beispiele

Der folgende Befehl lädt eine Datei in das Gerät "vidboard".

``` syntax
load vidboard c:\vid\fish.vid notify
```

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

 

