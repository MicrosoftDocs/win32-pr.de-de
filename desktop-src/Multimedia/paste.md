---
title: Befehl Einfügen
description: Mit dem Befehl Einfügen wird der Inhalt der Zwischenablage in den Arbeitsbereich kopiert. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- Befehl zum Einfügen von Windows Multimedia
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482fd744d7e6e163059330148b6e3f081d435880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040294"
---
# <a name="paste-command"></a>Befehl Einfügen

Mit dem Befehl Einfügen wird der Inhalt der Zwischenablage in den Arbeitsbereich kopiert. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("paste %s %s %s"), 
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

Mindestens eines der folgenden Flags.



| Wert                 | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at- *Rechteck*        | Gibt den Speicherort innerhalb des Frames an, in den die Daten eingefügt werden. Die linke obere Ecke des *Rechtecks* entspricht der oberen linken Ecke der hinzugefügten Daten. Wenn das Rechteck eine Größe ungleich 0 (null) aufweist, wird der Inhalt der Zwischenablage in diesen Dimensionen skaliert, wenn Sie in den Frame eingefügt werden. Wenn der Wert nicht weggelassen wird, wird das *Rechteck* standardmäßig auf den gesamten Frame Wenn dieses Flag im Einfügemodus (Standardeinstellung) angegeben wird, wird jede Region außerhalb des Rechtecks mit einer voll Tonfarbe gezeichnet.                       |
| Audiostream- *Stream* | Gibt den Audiodatenstrom im Arbeitsbereich an, der vom Befehl betroffen ist. Wenn nur ein Audiostream in der Zwischenablage vorhanden ist, werden die Audiodaten in den vorgesehenen *Stream* eingefügt. Wenn mehr als ein Audiostream in der Zwischenablage vorhanden ist, gibt der *Stream* die Startnummer für die Datenstrom Sequenzen an. Wenn Sie dieses Flag verwenden und auch Videos einfügen möchten, müssen Sie auch das Flag "Videostream" verwenden. (Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams eingefügt, und ihre ursprünglichen streamnummern werden beibehalten.) |
| insert                | Gibt an, dass die Daten in den Arbeitsbereich eingefügt werden. Alle Daten nach der Einfügemarke werden im Arbeitsbereich vorwärts verschoben, um Platz zu schaffen. Dies ist der Standardwert.                                                                                                                                                                                                                                                                                                                                                    |
| overwrite             | Gibt an, dass die Daten in den Arbeitsbereich kopiert werden, indem alle vorhandenen Daten nach der Einfügemarke geschrieben werden. Die Flags "Insert" und "Überschreibung" beeinflussen, ob Frames während des Einfügevorgangs zerstört oder verschoben werden, und nicht, wie die Daten in jedem Frame eingefügt werden.                                                                                                                                                                                                                                              |
| an *Position*         | Gibt die Position im Arbeitsbereich an, an der die Daten eingefügt werden. Wenn der Wert nicht weggelassen wird, wird standardmäßig die aktuelle Position verwendet.                                                                                                                                                                                                                                                                                                                                                                                                    |
| *videostreamstream* | Gibt den Videostream im Arbeitsbereich an, der vom Befehl betroffen ist. Wenn nur ein Videostream in der Zwischenablage vorhanden ist, werden die Videodaten in den vorgesehenen *Stream* eingefügt. Wenn mehr als ein Videostream in der Zwischenablage vorhanden ist, gibt der *Stream* die Startnummer für die Datenstrom Sequenzen an. Wenn Sie dieses Flag verwenden und auch Audiodaten einfügen möchten, müssen Sie auch das Flag "Audiostream" verwenden. (Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams eingefügt, und ihre ursprünglichen streamnummern werden beibehalten.) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify", "Test" oder eine Kombination daraus sein. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

In den Daten, die aus der Zwischenablage kopiert wurden, sind keine Signale vorhanden. Die Änderung wird nur dann permanent, wenn die Daten explizit gespeichert werden. die Wiedergabe verhält sich jedoch so, als ob die Daten hinzugefügt wurden.

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

 

