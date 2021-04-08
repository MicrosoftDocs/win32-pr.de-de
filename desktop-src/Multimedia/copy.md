---
title: Befehl "Kopieren"
description: Der Kopier Befehl kopiert Daten in die Zwischenablage. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- Kopier Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f08c764cb12b1cdca4c1876e6a22220a5c7522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740497"
---
# <a name="copy-command"></a>Befehl "Kopieren"

Der Kopier Befehl kopiert Daten in die Zwischenablage. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("copy %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszitem*
</dt> <dd>

Eines der folgenden Flags, das das zu kopierende Element identifiziert.



| Wert                 | Bedeutung                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at- *Rechteck*        | Gibt den Teil jedes Frames an, der kopiert wird. Wenn keine Angabe erfolgt, ist die Standardeinstellung der gesamte Frame.                                                                                                                             |
| Audiostream- *Stream* | Gibt den Audiodatenstrom im Arbeitsbereich an, der vom Befehl betroffen ist. Wenn Sie dieses Flag verwenden und Video auch kopieren möchten, müssen Sie auch das Flag "Videostream" verwenden. (Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams kopiert.) |
| von *Position*       | Gibt den Anfang des kopierten Bereichs an. Wenn keine Angabe erfolgt, ist die Standardeinstellung die aktuelle Position.                                                                                                                                         |
| an *Position*         | Gibt das Ende des kopierten Bereichs an. Die kopierten Audiodaten und Videodaten sind an dieser Position exklusiv. Wenn keine Angabe erfolgt, ist die Standardeinstellung das Ende des Arbeitsbereichs.                                                                       |
| *videostreamstream* | Gibt den Videostream im Arbeitsbereich an, der vom Befehl betroffen ist. Wenn Sie dieses Flag verwenden und auch Audiodaten kopieren möchten, müssen Sie auch das Flag "Audiostream" verwenden. (Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams kopiert.) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify", "Test" oder eine Kombination daraus sein. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

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

 

