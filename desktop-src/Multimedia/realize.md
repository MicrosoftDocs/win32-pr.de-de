---
title: realize-Befehl
description: Der Befehl realize weist ein Gerät an, seine Palette im Anzeigekontext des angezeigten Fensters auszuwählen und zu realisieren. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- realize-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0aba1e610f4636c7dbfb71fbc959d9b4b8496cc23e91a97100ef6edce133b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371435"
---
# <a name="realize-command"></a>realize-Befehl

Der Befehl realize weist ein Gerät an, seine Palette im Anzeigekontext des angezeigten Fensters auszuwählen und zu realisieren. Digitalvideogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) mit dem *lpszCommand-Parameter* auf, der wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("realize %s %s %s"), 
  lpszDeviceID, 
  lpszPalette, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*
</dt> <dd>

Eines der folgenden Flags.



| Wert      | Bedeutung                                                                   |
|------------|---------------------------------------------------------------------------|
| background | Realisiert die Palette als Hintergrundpalette.                             |
| normal     | Realisiert die Palette für ein Fenster der obersten Ebene. Dies ist die Standardeinstellung. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digitalvideogeräte kann auch "test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Verwenden Sie diesen Befehl nur, wenn Ihre Anwendung ein Fensterhandle verwendet und eine **WM \_ QUERYNEWPALTONE-** oder **WM \_ PALETTECHANGED-Meldung empfängt.**

## <a name="examples"></a>Beispiele

Der folgende Befehl weist das Gerät "myvideo" an, seine Palette zu realisieren.

``` syntax
realize myvideo normal
```

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
</dt> </dl>

 

