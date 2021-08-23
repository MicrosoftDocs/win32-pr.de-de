---
title: Befehl "cut"
description: Der Ausschneidebefehl entfernt Daten aus dem Arbeitsbereich und kopiert sie in die Zwischenablage. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- Befehl "cut" Windows Multimedia
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5a39010ad7dd07ccff38291441bb0aa05a54ee65da1b865d7ac82ed77fbfdd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144563"
---
# <a name="cut-command"></a>Befehl "cut"

Der Ausschneidebefehl entfernt Daten aus dem Arbeitsbereich und kopiert sie in die Zwischenablage. Digitalvideogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*
</dt> <dd>

Eines der folgenden Flags, das das zuschneidende Element identifiziert.



| Wert                 | Bedeutung                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| am *Rechteck*        | Gibt den Teil jedes Rahmenschnitts an. Wenn sie nicht angegeben wird, wird standardmäßig der gesamte Frame verwendet. Wenn dieses Element angegeben wird, werden Frames nicht gelöscht. Stattdessen wird der Bereich innerhalb des Rechtecks schwarz.                                       |
| *Audiostreamstream* | Gibt den Audiodatenstrom im Arbeitsbereich an, der vom Befehl betroffen ist. Wenn Sie dieses Flag verwenden und auch Videos ausschneiden möchten, müssen Sie auch das Flag "Videostream" verwenden. (Wenn kein Flag angegeben ist, werden alle Audio- und Videostreams ausgeschnitten.) |
| from *position*       | Gibt den Anfang des Bereichsschnitts an. Wenn sie nicht angegeben wird, wird standardmäßig die aktuelle Position verwendet.                                                                                                                                                |
| , um *zu positionieren*         | Gibt das Ende des Bereichsschnitts an. Der Audio- und Videodatenschnitt ist von dieser Position exklusiv. Wenn sie nicht angegeben wird, wird standardmäßig das Ende des Arbeitsbereichs verwendet.                                                                                  |
| Videostream  | Gibt den Videostream im Arbeitsbereich an, der vom Befehl betroffen ist. Wenn Sie dieses Flag verwenden und auch Audio ausschneiden möchten, müssen Sie auch das Flag "Audiostream" verwenden. (Wenn kein Flag angegeben ist, werden alle Audio- und Videostreams ausgeschnitten.) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify", "test" oder eine Kombination dieser sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die Änderung wird nur dann dauerhaft, wenn die Daten explizit gespeichert werden. Die Wiedergabe verhält sich jedoch so, als ob die Daten entfernt wurden.

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

 

