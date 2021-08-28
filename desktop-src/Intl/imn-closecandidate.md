---
description: Benachrichtigt eine Anwendung, wenn ein IME das Kandidatenfenster schließen soll. Die Anwendung empfängt diesen Befehl über die WM \_ IME \_ NOTIFY-Nachricht mit Parametereinstellungen, wie unten dargestellt.
ms.assetid: d96cea0a-1fc4-4ba7-bb96-7e9c0b67ce5b
title: IMN_CLOSECANDIDATE Benachrichtigungscode (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd0a71eac28b2c7dc170724e40c9b4ba6707cd5774145f38efdd791e7ebd8b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107150"
---
# <a name="imn_closecandidate-notification-code"></a>IMN \_ CLOSECANDIDATE-Benachrichtigungscode

Benachrichtigt eine Anwendung, wenn ein IME das Kandidatenfenster schließen soll. Die Anwendung empfängt diesen Befehl über die [**WM \_ IME \_ NOTIFY-Nachricht**](wm-ime-notify.md) mit Parametereinstellungen, wie unten dargestellt.


```C++
IMN_CLOSECANDIDATE
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMN \_ CLOSECANDIDATE fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Kandidatenlistenflag. Jedes Bit entspricht einer Kandidatenliste: Bit 0 für die erste Liste, Bit 1 bis Sekunde und so weiter. Wenn ein angegebenes Bit 1 ist, wird das entsprechende Kandidatenfenster geschlossen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Befehl hat keinen Rückgabewert.

## <a name="remarks"></a>Hinweise

Eine Anwendung sollte diesen Befehl verarbeiten, wenn sie Kandidaten selbst anzeigt.

Standardmäßig zerstört das IME-Fenster ein Kandidatenfenster, wenn es diesen Befehl verarbeitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethode-Manager](input-method-manager.md)
</dt> <dt>

[Befehle des Eingabemethode-Managers](input-method-manager-commands.md)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




