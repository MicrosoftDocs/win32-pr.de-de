---
title: Close-Befehl (Corecrt \_ io.h)
description: Der Befehl close schließt das Gerät oder die Datei und alle zugehörigen Ressourcen. MCI entlädt ein Gerät, wenn alle Instanzen des Geräts oder alle Dateien geschlossen sind. Dieser Befehl wird von allen MCI-Geräten erkannt.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- Befehl "close" Windows Multimedia
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
ms.openlocfilehash: b02acd3ebe3d45a402ae565c6fcac121f712df4374924bcb0e02c3dcadf9ceeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807959"
---
# <a name="close-command"></a>Befehl "close"

Der Befehl close schließt das Gerät oder die Datei und alle zugehörigen Ressourcen. MCI entlädt ein Gerät, wenn alle Instanzen des Geräts oder alle Dateien geschlossen sind. Dieser Befehl wird von allen MCI-Geräten erkannt.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Um alle von Ihrer Anwendung geöffneten Geräte zu schließen, geben Sie den Gerätebezeichner "all" für den *LpszDeviceID-Parameter* an.

Wenn Sie das **Cdaudio-Gerät** schließen, wird die Audiowiedergabe beendet.

**Windows 2000/XP:** Wenn das **Cdaudio-Gerät** wiedergegeben wird, führt das Schließen des **cdaudio-Geräts** nicht dazu, dass die Audiowiedergabe beendet wird. Senden Sie zuerst den [Befehl stop.](stop.md)

## <a name="examples"></a>Beispiele

Der folgende Befehl schließt das Gerät "mysound".

``` syntax
close mysound
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Corecrt \_ io.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> </dl>

 

