---
description: Benachrichtigt eine Anwendung, wenn ein IME das Statusfenster schließen wird. Die Anwendung empfängt diesen Befehl über die WM \_ IME \_ NOTIFY-Nachricht mit Parametereinstellungen, wie unten dargestellt.
ms.assetid: d59fdf76-50e7-4a59-b1bd-a12cdb0026f6
title: IMN_CLOSESTATUSWINDOW Benachrichtigungscode (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56093e5dac9c5b9b236c6819a627c1d8c1fc05aa8350824577f29f64c007e71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107160"
---
# <a name="imn_closestatuswindow-notification-code"></a>IMN \_ CLOSESTATUSWINDOW-Benachrichtigungscode

Benachrichtigt eine Anwendung, wenn ein IME das Statusfenster schließen wird. Die Anwendung empfängt diesen Befehl über die [**WM \_ IME \_ NOTIFY-Nachricht**](wm-ime-notify.md) mit Parametereinstellungen, wie unten dargestellt.


```C++
IMN_CLOSESTATUSWINDOW
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMN \_ CLOSESTATUSWINDOW fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Befehl hat keinen Rückgabewert.

## <a name="remarks"></a>Hinweise

Eine Anwendung sollte diesen Befehl verarbeiten, wenn sie das Statusfenster für den IME anzeigt.

Das IME-Fenster schließt das Statusfenster, wenn es diesen Befehl verarbeitet.

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

 

 




