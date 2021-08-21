---
title: Befehl "rückgängig"
description: Mit dem Befehl "Rückgängig" wird die Aktion rückgängig gemacht, die mit dem letzten erfolgreichen Befehl zum Kopieren, Ausschneiden, Löschen, Rückgängigmachen oder Einfügen ausgeführt wurde. Digitalvideogeräte erkennen diesen Befehl.
ms.assetid: 81d696a9-5288-4efd-bc76-8416dd63e694
keywords:
- Rückgängig-Befehl Windows Multimedia
topic_type:
- apiref
api_name:
- undo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec088f893b221a80cb3fe84c191a52874a8c29f5163ad3bcdaa8e68a9a4d4d2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804730"
---
# <a name="undo-command"></a>Befehl "rückgängig"

Der Befehl "rückgängig" kehrt die Aktion des letzten erfolgreichen [Kopier-,](copy.md) [Ausschneide-,](cut.md) [Lösch-,](delete.md)Rückgängig- oder [Einfügebefehls](paste.md) um. Digitalvideogeräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendString-Funktion**](/previous-versions//dd757161(v=vs.85)) auf, wobei der *lpszCommand-Parameter* wie folgt festgelegt ist.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("undo %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Bezeichner eines MCI-Geräts. Dieser Bezeichner oder Alias wird zugewiesen, wenn das Gerät geöffnet wird.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehlszeichenfolgen](mci-command-strings.md)
</dt> <dt>

[copy](copy.md)
</dt> <dt>

[Schneiden](cut.md)
</dt> <dt>

[delete](delete.md)
</dt> <dt>

[Einfügen](paste.md)
</dt> </dl>

 

