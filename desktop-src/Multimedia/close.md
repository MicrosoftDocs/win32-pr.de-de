---
title: Befehl "Schließen" (corecrt \_ IO. h)
description: Der Close-Befehl schließt das Gerät oder die Datei und alle zugehörigen Ressourcen. MCI entlädt ein Gerät, wenn alle Instanzen des Geräts oder alle Dateien geschlossen sind. Dieser Befehl wird von allen MCI-Geräten erkannt.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- Befehl "Schließen" Windows Multimedia
topic_type:
- apiref
api_name:
- close
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28c255e518553c022dfc833c857b792f43fdbe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949758"
---
# <a name="close-command"></a>Befehl "Schließen"

Der Close-Befehl schließt das Gerät oder die Datei und alle zugehörigen Ressourcen. MCI entlädt ein Gerät, wenn alle Instanzen des Geräts oder alle Dateien geschlossen sind. Dieser Befehl wird von allen MCI-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("close %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Wenn Sie alle von Ihrer Anwendung geöffneten Geräte schließen möchten, geben Sie den "All"-Geräte Bezeichner für den *lpszdebug* -Parameter an.

Durch das Schließen des **CDAudio** -Geräts wird die Audiowiedergabe beendet.

**Windows 2000/XP:** Wenn das **CDAudio** -Gerät abgespielt wird, führt das Schließen des **CDAudio** -Geräts nicht dazu, dass die Audiowiedergabe beendet wird. Senden Sie zuerst den Befehl " [Abbrechen](stop.md) ".

## <a name="examples"></a>Beispiele

Mit dem folgenden Befehl wird das Gerät "mysound" geschlossen.

``` syntax
close mysound
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Corecrt \_ IO. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Befehls Zeichenfolgen](mci-command-strings.md)
</dt> </dl>

 

