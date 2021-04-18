---
title: Qualitäts Befehl
description: Der Qualitäts Befehl definiert eine benutzerdefinierte Qualitätsstufe für Audiodaten, Video-oder Bild Datenkomprimierung. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- Qualitäts Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de9cc61d72db541b5f06d8903d7c9dcf153ce07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344493"
---
# <a name="quality-command"></a>Qualitäts Befehl

Der Qualitäts Befehl definiert eine benutzerdefinierte Qualitätsstufe für Audiodaten, Video-oder Bild Datenkomprimierung. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszquality*
</dt> <dd>

Mindestens eines der folgenden Flags. (Eines der drei Flags "Audio", "immer noch" und "Video" muss vorhanden sein.)



| Wert                 | Bedeutung                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *algorithmusalgorithmus* | Ordnet die Qualitätsstufe dem angegebenen *Algorithmus* zu. Dieser *Algorithmus* muss vom Gerät unterstützt werden und mit dem verwendeten Flag "Audiodatei", "immer noch" oder "Video" kompatibel sein. Wenn der Wert nicht weggelassen wird, wird der aktuelle Algorithmus verwendet. |
| *audioname*          | Gibt an, dass dieser Befehl eine Audioqualität angibt, die mit dem *Namen* identifiziert wird.                                                                                                                                                   |
| Dialog (dialog)                | Fordert an, dass das Gerät ein Dialogfeld anzeigt. Dieses Dialogfeld enthält algorithmusspezifische Felder, die intern vom Gerät verwendet werden, um die Struktur zu erstellen, die eine bestimmte Qualitätsstufe beschreibt.                                    |
| Handle *handle*       | Gibt ein *handle* für eine-Struktur an, die algorithmische spezifische Daten enthält, die eine bestimmte Qualitätsstufe beschreiben. Die Strukturen für die Daten, auf die von diesem Handle verwiesen wird, sind gerätespezifisch.                                         |
| immer noch *Name*          | Gibt an, dass der Befehl eine "immer noch"-Qualitätsstufe angibt, die mit dem *Namen*                                                                                                                                                     |
| *videoname*          | Gibt an, dass der Befehl eine mit dem *Namen* identifizierte "Video"-Qualitätsstufe angibt.                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify", "Test" oder eine Kombination daraus sein. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Dieser Befehl definiert einen Zeichen folgen Namen für den Qualitätsgrad, der dann im [setvideo](setvideo.md) -"Quality"-, setvideo-"immer Qualität"-oder [SetAudio"](setaudio.md) Quality"-Befehl verwendet werden kann, um ihn als Aktuelles Video, noch immer oder als audiokomprimierungsqualitätsstufe festzulegen.

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

[setaudiodatei](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 

