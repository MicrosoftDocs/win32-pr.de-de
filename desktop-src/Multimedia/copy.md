---
title: Befehl "copy"
description: Der Befehl copy kopiert Daten in die Zwischenablage. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- Befehl "copy" Windows Multimedia
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3d103aae14b9dc13bb0d7d210d0412db993210bc788fa7fedd1a48a7216d59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144783"
---
# <a name="copy-command"></a>Befehl "copy"

Der Befehl copy kopiert Daten in die Zwischenablage. Digitalvideogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

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

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*
</dt> <dd>

Eines der folgenden Flags, das das zu kopierende Element identifiziert.



| Wert                 | Bedeutung                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| am *Rechteck*        | Gibt den Teil jedes Frames an, der kopiert wird. Wenn sie nicht angegeben wird, ist die Standardeinstellung der gesamte Frame.                                                                                                                             |
| *Audiostreamstream* | Gibt den Audiodatenstrom im Arbeitsbereich an, der vom Befehl betroffen ist. Wenn Sie dieses Flag verwenden und auch Videos kopieren möchten, müssen Sie auch das Flag "Videostream" verwenden. (Wenn kein Flag angegeben ist, werden alle Audio- und Videostreams kopiert.) |
| from *position*       | Gibt den Anfang des kopierten Bereichs an. Wenn keine Angabe erfolgt, ist die Standardeinstellung die aktuelle Position.                                                                                                                                         |
| , um *zu positionieren*         | Gibt das Ende des kopierten Bereichs an. Die kopierten Audio- und Videodaten gelten ausschließlich für diese Position. Wenn diese Einstellung nicht angegeben wird, ist die Standardeinstellung das Ende des Arbeitsbereichs.                                                                       |
| Videostream  | Gibt den Videostream im Arbeitsbereich an, der vom Befehl betroffen ist. Wenn Sie dieses Flag verwenden und auch Audio kopieren möchten, müssen Sie auch das Flag "Audiostream" verwenden. (Wenn kein Flag angegeben ist, werden alle Audio- und Videostreams kopiert.) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Kann "wait", "notify", "test" oder eine Kombination dieser sein. Weitere Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn der Fehler erfolgreich war, oder andernfalls ein Fehler.

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

 

