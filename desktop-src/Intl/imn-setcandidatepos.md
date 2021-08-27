---
description: Benachrichtigt eine Anwendung, wenn die Kandidatenverarbeitung abgeschlossen ist und die IME das Kandidatenfenster verschieben wird. Die Anwendung empfängt diesen Befehl über die WM \_ IME \_ NOTIFY-Nachricht mit Parametereinstellungen, wie unten dargestellt.
ms.assetid: 64252d88-130b-44c3-854a-78b01def7a13
title: IMN_SETCANDIDATEPOS Benachrichtigungscode (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 689dfe0c38f5508c853af94e271bb1f333bfbad0df18b3fab09450d73497e7fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107060"
---
# <a name="imn_setcandidatepos-notification-code"></a>IMN \_ SETCANDIDATEPOS-Benachrichtigungscode

Benachrichtigt eine Anwendung, wenn die Kandidatenverarbeitung abgeschlossen ist und die IME das Kandidatenfenster verschieben wird. Die Anwendung empfängt diesen Befehl über die [**WM \_ IME \_ NOTIFY-Nachricht**](wm-ime-notify.md) mit Parametereinstellungen, wie unten dargestellt.


```C++
IMN_SETCANDIDATEPOS
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMN \_ SETCANDIDATEPOS fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Kandidatenlistenflag. Jedes Bit entspricht einer Kandidatenliste: Bit 0 zur ersten Liste, Bit 1 für die zweite usw. Wenn ein angegebenes Bit 1 ist, wird das entsprechende Kandidatenfenster verschoben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Befehl hat keinen Rückgabewert.

## <a name="remarks"></a>Hinweise

Eine Anwendung sollte diesen Befehl verarbeiten, wenn das Kandidatenfenster selbst angezeigt wird.

Das IME-Fenster verschiebt das Kandidatenfenster, wenn dieser Befehl verarbeitet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Befehle des Eingabemethoden-Managers](input-method-manager-commands.md)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




