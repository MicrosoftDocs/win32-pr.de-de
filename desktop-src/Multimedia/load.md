---
title: Befehl "Laden"
description: Der Load-Befehl lädt eine Datei in einem gerätespezifischen Format. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- Befehl "Laden" Windows Multimedia
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199a6d3aea8a2697217eb75176c24b2b0bc2e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742496"
---
# <a name="load-command"></a>Befehl "Laden"

Der Load-Befehl lädt eine Datei in einem gerätespezifischen Format. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszfilepos*
</dt> <dd>

Der zu ladende Pfad und Dateiname. Bei Video Überlagerungs Geräten kann dies auch ein Ziel Rechteck für die Daten enthalten. Geben Sie zum Angeben eines Ziel Rechtecks "at" gefolgt von **x1 y1 x2 Y2** an, wobei **x1 y1** die obere linke Ecke des Rechtecks angeben und **x2 Y2** die Breite und Höhe angeben. Das Rechteck ist relativ zum Video Puffer Ursprung.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Das "vidboard"-Gerät sendet eine Benachrichtigungs Meldung, wenn der Ladevorgang abgeschlossen ist.

## <a name="examples"></a>Beispiele

Mit dem folgenden Befehl wird eine Datei in das "vidboard"-Gerät geladen.

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

[MCI](mci.md)
</dt> <dt>

[MCI-Befehls Zeichenfolgen](mci-command-strings.md)
</dt> </dl>

 

