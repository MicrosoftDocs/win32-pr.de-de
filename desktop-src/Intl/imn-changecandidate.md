---
description: Benachrichtigt die Anwendung, wenn ein IME im Begriff ist, den Inhalt des Kandidaten Fensters zu ändern. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 0a276f9c-cece-4fa6-b71a-ba0daad5ca05
title: IMN_CHANGECANDIDATE Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197380c3cf6369e0dbfd7dbca76bb3b84334eb6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131740"
---
# <a name="imn_changecandidate-notification-code"></a>IMN \_ changecandidate-Benachrichtigungs Code

Benachrichtigt die Anwendung, wenn ein IME im Begriff ist, den Inhalt des Kandidaten Fensters zu ändern. Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.


```C++
IMN_CHANGECANDIDATE
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf IMN \_ changecandidate fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Flag der Kandidatenliste. Jedes Bit entspricht einer Kandidatenliste: Bit 0 bis zur ersten Liste, Bit 1 zur zweiten Liste usw. Wenn ein angegebenes Bit 1 ist, wird das entsprechende Kandidaten Fenster geändert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Befehl weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung sollte diesen Befehl verarbeiten, wenn Sie Kandidaten selbst anzeigt.

Das IME-Fenster ändert die Darstellung des Kandidaten Fensters, wenn es diesen Befehl verarbeitet. Eine Anwendung kann Informationen über das System Fenster mit " [**immgetcandidatelistcount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) " und " [**immgetcandidatelist**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista) " erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Imm. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Eingabemethoden-Manager-Befehle](input-method-manager-commands.md)
</dt> <dt>

[**Immgetcandidatelist**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[**Immgetcandidatelistcount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)
</dt> <dt>

[**WM- \_ IME \_ Benachrichtigen**](wm-ime-notify.md)
</dt> </dl>

 

 




