---
title: Befehl Ausschneiden
description: Mit dem Befehl "Ausschneiden" werden Daten aus dem Arbeitsbereich entfernt und in die Zwischenablage kopiert. Dieser Befehl wird von Digital-Video-Geräten erkannt.
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- Befehl "Ausschneiden" Windows Multimedia
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33571309e1dd249f20e577c97b8c6e1b950eda09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956975"
---
# <a name="cut-command"></a>Befehl Ausschneiden

Mit dem Befehl "Ausschneiden" werden Daten aus dem Arbeitsbereich entfernt und in die Zwischenablage kopiert. Dieser Befehl wird von Digital-Video-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cut %s %s %s"), 
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

Eines der folgenden Flags, das das auszuschneide Ende Element identifiziert.



| Wert                 | Bedeutung                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| at- *Rechteck*        | Gibt den Teil jedes Frame Ausschnitts an. Wenn der Wert nicht weggelassen wird, wird standardmäßig der gesamte Frame verwendet. Wenn dieses Element angegeben wird, werden Rahmen nicht gelöscht. Stattdessen wird der Bereich innerhalb des Rechtecks schwarz.                                       |
| Audiostream- *Stream* | Gibt den Audiodatenstrom im Arbeitsbereich an, der vom Befehl betroffen ist. Wenn Sie dieses Flag verwenden und auch Video ausschneiden möchten, müssen Sie auch das Flag "Videostream" verwenden. (Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams ausgeschnitten.) |
| von *Position*       | Gibt den Anfang des Bereichs Ausschnitts an. Wenn der Wert nicht weggelassen wird, wird standardmäßig die aktuelle Position verwendet.                                                                                                                                                |
| an *Position*         | Gibt das Ende des Bereichs Ausschnitts an. Der Ton-und Videodaten Ausschnitt ist an dieser Position exklusiv. Wenn der Wert ausgelassen wird, wird standardmäßig das Ende des Arbeitsbereichs verwendet.                                                                                  |
| *videostreamstream* | Gibt den Videostream im Arbeitsbereich an, der vom Befehl betroffen ist. Wenn Sie dieses Flag verwenden und auch das Audiodaten ausschneiden möchten, müssen Sie auch das Flag "Audiostream" verwenden. (Wenn keines der Flags angegeben ist, werden alle Audio-und Videostreams ausgeschnitten.) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify", "Test" oder eine Kombination daraus sein. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die Änderung wird nur dann permanent, wenn die Daten explizit gespeichert werden. die Wiedergabe verhält sich jedoch so, als ob die Daten entfernt wurden.

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

 

