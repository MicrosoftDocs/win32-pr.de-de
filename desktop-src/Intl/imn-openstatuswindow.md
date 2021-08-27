---
description: Benachrichtigt eine Anwendung, wenn ein IME das Statusfenster erstellen soll. Die Anwendung empfängt diesen Befehl über die WM \_ IME \_ NOTIFY-Nachricht mit Parametereinstellungen, wie unten dargestellt.
ms.assetid: bbd85c72-aa78-4e1d-8a7a-490650b2d782
title: IMN_OPENSTATUSWINDOW Benachrichtigungscode (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1726ca2433f450f92ddf7da4752b1a53b23e4176b8f0c6f14d03f6fa279f9daa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107110"
---
# <a name="imn_openstatuswindow-notification-code"></a>IMN \_ OPENSTATUSWINDOW-Benachrichtigungscode

Benachrichtigt eine Anwendung, wenn ein IME das Statusfenster erstellen soll. Die Anwendung empfängt diesen Befehl über die [**WM \_ IME \_ NOTIFY-Nachricht**](wm-ime-notify.md) mit Parametereinstellungen, wie unten dargestellt.


```C++
IMN_OPENSTATUSWINDOW
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMN \_ OPENSTATUSWINDOW fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Befehl hat keinen Rückgabewert.

## <a name="remarks"></a>Hinweise

Eine Anwendung verarbeitet diesen Befehl, um das Statusfenster für den IME selbst anzuzeigen.

Das IME-Fenster erstellt ein Statusfenster, wenn es diesen Befehl verarbeitet, und legt die Zeichenfolgen fest, die im Fenster im Eingabekontext angezeigt werden. Anwendungen können Mithilfe der [**ImmGetConversionStatus-Funktion Informationen zum Statusfenster**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) abrufen.

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

[**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




