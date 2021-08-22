---
description: Benachrichtigt die Anwendung, wenn ein IME den Inhalt des Kandidatenfensters ändern wird. Die Anwendung empfängt diesen Befehl über die WM \_ IME \_ NOTIFY-Nachricht mit Parametereinstellungen, wie unten dargestellt.
ms.assetid: 0a276f9c-cece-4fa6-b71a-ba0daad5ca05
title: IMN_CHANGECANDIDATE Benachrichtigungscode (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 599f064b05f4fa0bda205825d623d13eec39334683fbe2b69f1c8b7b2997026b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949251"
---
# <a name="imn_changecandidate-notification-code"></a>IMN \_ CHANGECANDIDATE-Benachrichtigungscode

Benachrichtigt die Anwendung, wenn ein IME den Inhalt des Kandidatenfensters ändern wird. Die Anwendung empfängt diesen Befehl über die [**WM \_ IME \_ NOTIFY-Nachricht**](wm-ime-notify.md) mit Parametereinstellungen, wie unten dargestellt.


```C++
IMN_CHANGECANDIDATE
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMN \_ CHANGECANDIDATE fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Kandidatenlistenflag. Jedes Bit entspricht einer Kandidatenliste: Bit 0 für die erste Liste, Bit 1 bis zur zweiten Liste und so weiter. Wenn ein angegebenes Bit 1 ist, wird das entsprechende Kandidatenfenster geändert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Befehl hat keinen Rückgabewert.

## <a name="remarks"></a>Hinweise

Eine Anwendung sollte diesen Befehl verarbeiten, wenn sie Kandidaten selbst anzeigt.

Das IME-Fenster ändert die Darstellung des Kandidatenfensters, wenn es diesen Befehl verarbeitet. Eine Anwendung kann Mit [**immGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) und [**ImmGetCandidateList Informationen zum Systemfenster erhalten.**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Eingabemethode-Manager](input-method-manager.md)
</dt> <dt>

[Befehle des Eingabemethode-Managers](input-method-manager-commands.md)
</dt> <dt>

[**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




