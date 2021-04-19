---
title: Befehl "Escape"
description: Der Befehl "Escape" sendet gerätespezifische Informationen an ein Gerät. Videodisk-Geräte erkennen diesen Befehl.
ms.assetid: 16e0e2b6-6d98-440a-86c1-eca8201ad61a
keywords:
- escapebefehl Windows Multimedia
topic_type:
- apiref
api_name:
- escape
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b04f7a2ef6c2e91adc9b24a044d0a7e941843f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339535"
---
# <a name="escape-command"></a>Befehl "Escape"

Der Befehl "Escape" sendet gerätespezifische Informationen an ein Gerät. Videodisk-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, wenden Sie die [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion mit dem festgelegten *lpszcommand* -Parameter wie folgt an.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("escape %s %s %s"), 
  lpszDeviceID, 
  lpszEscape, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszde viceid*
</dt> <dd>

Der Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

</dd> <dt>

<span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszescape*
</dt> <dd>

Benutzerdefinierte Informationen, die an das Gerät gesendet werden sollen.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszflags*
</dt> <dd>

Kann "wait", "notify" oder beides sein. Weitere Informationen zu diesen Flags finden Sie [unter warte-, Benachrichtigungs-und testflags](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="examples"></a>Beispiele

Mit dem folgenden Befehl wird die Escapezeichenfolge "SA" an das Videodisk-Gerät gesendet.

``` syntax
escape videodisc SA
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

 

