---
title: Quality-Befehl
description: Der Qualitätsbefehl definiert eine benutzerdefinierte Qualitätsstufe für die Komprimierung von Audio-, Video- oder Standbilddaten. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- Quality-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f50f019b0e89f21d792f75c13e6c8e755486009d38d242878fec3121333fb9af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372325"
---
# <a name="quality-command"></a>Quality-Befehl

Der Qualitätsbefehl definiert eine benutzerdefinierte Qualitätsstufe für die Komprimierung von Audio-, Video- oder Standbilddaten. Digitalvideogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("quality %s %s %s"), 
  lpszDeviceID, 
  lpszQuality, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*
</dt> <dd>

Mindestens eines der folgenden Flags. (Eines der drei Flags "audio", "still" und "video" muss vorhanden sein.)



| Wert                 | Bedeutung                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Algorithmusalgorithmus* | Ordnet die Qualitätsebene dem angegebenen *Algorithmus* zu. Dieser *Algorithmus* muss vom Gerät unterstützt werden und mit dem verwendeten Flag "audio", "still" oder "video" kompatibel sein. Wenn dieser Wert ausgelassen wird, wird der aktuelle Algorithmus verwendet. |
| *Audioname*          | Gibt an, dass dieser Befehl eine "Audio"-Qualitätsstufe angibt, die mit *dem Namen* identifiziert wird.                                                                                                                                                   |
| Dialog (dialog)                | Fordert an, dass das Gerät ein Dialogfeld anzeigt. Dieses Dialogfeld enthält algorithmusspezifische Felder, die intern vom Gerät verwendet werden, um die Struktur zu erstellen, die eine bestimmte Qualitätsstufe beschreibt.                                    |
| *Handlehandle*       | Gibt ein *Handle* für eine Struktur an, die algorithmisch-spezifische Daten enthält, die eine bestimmte Qualitätsstufe beschreiben. Die Strukturen für die Daten, auf die von diesem Handle verwiesen wird, sind gerätespezifisch.                                         |
| still *name*          | Gibt an, dass der Befehl eine mit dem Namen identifizierte Qualitätsstufe "still" *angibt.*                                                                                                                                                     |
| *Videoname*          | Gibt an, dass der Befehl eine "Video"-Qualitätsstufe angibt, die mit *dem Namen* identifiziert wird.                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify", "test" oder eine Kombination dieser sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Dieser Befehl definiert einen Zeichenfolgennamen für die Qualitätsstufe, der dann in einem [setvideo-Befehl](setvideo.md) "quality", setvideo "still quality" oder [setaudio](setaudio.md) "quality" verwendet werden kann, um ihn als die aktuelle Qualitätsstufe "Video", "Still" oder "Audiokomprimierung" festzulegen.

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

[Setaudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 

