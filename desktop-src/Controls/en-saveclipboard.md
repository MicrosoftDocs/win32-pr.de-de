---
title: EN_SAVECLIPBOARD Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster des Rich-Edit-Steuer Elements, dass das-Steuerelement geschlossen wird und die Zwischenablage Informationen enthält. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: e8b95e80-6494-4153-8e78-ede9ed17c66f
keywords:
- Windows-Steuerelemente für EN_SAVECLIPBOARD Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_SAVECLIPBOARD
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1fd7c6e11ed82a7f77483c692dd68f860395c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858826"
---
# <a name="en_saveclipboard-notification-code"></a>EN \_ saveclipboard-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster des Rich-Edit-Steuer Elements, dass das-Steuerelement geschlossen wird und die Zwischenablage Informationen enthält. Ein Rich Edit-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)


```C++
EN_SAVECLIPBOARD

    penSaveClipboard = (ENSAVECLIPBOARD *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) eingefüchende-Struktur, die Informationen zu Zwischenablage Informationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn die Zwischenablage anderen Anwendungen zur Verfügung gestellt werden soll.

Gibt einen Wert ungleich 0 (null) zurück, wenn die Zwischenablage nicht gespeichert werden soll.

## <a name="remarks"></a>Bemerkungen

Das übergeordnete Fenster ruft immer eine [**WM \_**](wm-notify.md) -Benachrichtigungs Meldung für dieses Ereignis ab. es ist keine Benachrichtigungs Maske erforderlich, die mit der "em-Einstellungs [**\_ Maske**](em-seteventmask.md)" gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**""**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
</dt> </dl>

 

 





