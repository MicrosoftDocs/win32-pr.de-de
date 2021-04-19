---
description: Benachrichtigt eine Anwendung, wenn die Verarbeitung der Kandidaten abgeschlossen ist und der IME im Begriff ist, das Kandidaten Fenster zu verschieben. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 64252d88-130b-44c3-854a-78b01def7a13
title: IMN_SETCANDIDATEPOS Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03171a76ce94572d2425f8e75f1cbe45b7efe4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353504"
---
# <a name="imn_setcandidatepos-notification-code"></a>IMN \_ setcandidatepos-Benachrichtigungs Code

Benachrichtigt eine Anwendung, wenn die Verarbeitung der Kandidaten abgeschlossen ist und der IME im Begriff ist, das Kandidaten Fenster zu verschieben. Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.


```C++
IMN_SETCANDIDATEPOS
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf IMN \_ setcandidatepos fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Flag der Kandidatenliste. Jedes Bit entspricht einer Kandidatenliste: Bit 0 bis zur ersten Liste, Bit 1 bis zum zweiten usw. Wenn ein angegebenes Bit 1 ist, wird das entsprechende Kandidaten Fenster verschoben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Befehl weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung sollte diesen Befehl verarbeiten, wenn Sie das Kandidaten Fenster selbst anzeigt.

Das Fenster IME verschiebt das Kandidaten Fenster, wenn es diesen Befehl verarbeitet.

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

[**WM- \_ IME \_ Benachrichtigen**](wm-ime-notify.md)
</dt> </dl>

 

 




