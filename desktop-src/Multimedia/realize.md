---
title: Befehl "erkennen"
description: Der Befehl "erkennen" weist ein Gerät an, seine Palette im Anzeige Kontext des angezeigten Fensters auszuwählen und zu erkennen. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- Befehl "Windows Multimedia"
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33accaa9638210adf4385a1776fcd8d2bd2021e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957028"
---
# <a name="realize-command"></a>Befehl "erkennen"

Der Befehl "erkennen" weist ein Gerät an, seine Palette im Anzeige Kontext des angezeigten Fensters auszuwählen und zu erkennen. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszpalette*
</dt> <dd>

Eines der folgenden Flags.



| Wert      | Bedeutung                                                                   |
|------------|---------------------------------------------------------------------------|
| background | Erkennt die Palette als Hintergrund Palette.                             |
| normal     | Erkennt die Palette für ein Fenster der obersten Ebene. Dies ist die Standardeinstellung. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Für Digital Video-Geräte kann auch "Test" angegeben werden. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diesen Befehl nur, wenn Ihre Anwendung ein Fenster Handle verwendet und eine **WM \_ querynewpallette** -oder **WM \_ palettechanged** -Meldung empfängt.

## <a name="examples"></a>Beispiele

Der folgende Befehl weist das Gerät "MyVideo" an, seine Palette zu erkennen.

``` syntax
realize myvideo normal
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

 

