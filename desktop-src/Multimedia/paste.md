---
title: Befehl "paste"
description: Der Befehl paste kopiert den Inhalt der Zwischenablage in den Arbeitsbereich. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- Befehl "paste" Windows Multimedia
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b93f042193c50a810ac23285224ddd234a23b2070f8db2d56d216fee037c37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373215"
---
# <a name="paste-command"></a>Befehl "paste"

Der Befehl paste kopiert den Inhalt der Zwischenablage in den Arbeitsbereich. Digitalvideogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*
</dt> <dd>

Mindestens eines der folgenden Flags.



| Wert                 | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| am *Rechteck*        | Gibt die Position innerhalb des Rahmens an, in den die Daten eingefügt werden. Die obere linke Ecke des *Rechtecks* entspricht der oberen linken Ecke der hinzugefügten Daten. Wenn das Rechteck eine Größe ungleich 0 (null) in X oder Y aufweist, wird der Inhalt der Zwischenablage in diesen Dimensionen skaliert, wenn sie in den Rahmen eingefügt werden. Wenn dies nicht angegeben wird, wird das *Rechteck* standardmäßig auf den gesamten Frame eingestellt. Wenn dieses Flag im Einfügemodus (Standard) angegeben ist, wird jeder Bereich außerhalb des Rechtecks in eine Volltonfarbe gezeichnet.                       |
| *Audiostreamstream* | Gibt den Audiodatenstrom im Arbeitsbereich an, der vom Befehl betroffen ist. Wenn nur ein Audiostream in der Zwischenablage vorhanden ist, werden die Audiodaten in den angegebenen *Stream* eingefügt. Wenn mehr als ein Audiostream in der Zwischenablage vorhanden ist, gibt der *Stream* die Startnummer für die Streamsequenzen an. Wenn Sie dieses Flag verwenden und auch Videos einfügen möchten, müssen Sie auch das Flag "Videostream" verwenden. (Wenn kein Flag angegeben ist, werden alle Audio- und Videostreams eingefügt und behalten ihre ursprünglichen Datenstromnummern bei.) |
| insert                | Gibt an, dass die Daten in den Arbeitsbereich eingefügt werden. Alle Daten nach der Einfügemarke werden im Arbeitsbereich vorwärts verschoben, um Platz zu schaffen. Dies ist der Standardwert.                                                                                                                                                                                                                                                                                                                                                    |
| overwrite             | Gibt an, dass die Daten in den Arbeitsbereich kopiert werden, indem vorhandene Daten nach der Einfügemarke geschrieben werden. Die Flags "insert" und "overwrite" beeinflussen, ob Frames während des Einfügevorgangs zerstört oder verschoben werden, nicht wie die Daten in die einzelnen Frames eingefügt werden.                                                                                                                                                                                                                                              |
| , um *zu positionieren*         | Gibt die Position im Arbeitsbereich an, an der die Daten eingefügt werden. Wenn sie nicht angegeben wird, wird standardmäßig die aktuelle Position verwendet.                                                                                                                                                                                                                                                                                                                                                                                                    |
| Videostream  | Gibt den Videostream im Arbeitsbereich an, der vom Befehl betroffen ist. Wenn nur ein Videostream in der Zwischenablage vorhanden ist, werden die Videodaten in den angegebenen *Stream* eingefügt. Wenn mehr als ein Videostream in der Zwischenablage vorhanden ist, gibt der *Stream* die Startnummer für die Streamsequenzen an. Wenn Sie dieses Flag verwenden und auch Audio einfügen möchten, müssen Sie auch das Flag "Audiostream" verwenden. (Wenn kein Flag angegeben ist, werden alle Audio- und Videostreams eingefügt und behalten ihre ursprünglichen Datenstromnummern bei.) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify", "test" oder eine Kombination dieser sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

In den aus der Zwischenablage kopierten Daten sind keine Signale vorhanden. Die Änderung wird nur dann dauerhaft, wenn die Daten explizit gespeichert werden. Die Wiedergabe verhält sich jedoch so, als ob die Daten hinzugefügt wurden.

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

 

