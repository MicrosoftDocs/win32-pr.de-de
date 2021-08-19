---
description: Benachrichtigt eine Anwendung, wenn die Schriftart des Eingabekontexts aktualisiert wird. Die Anwendung empfängt diesen Befehl über die WM \_ IME \_ NOTIFY-Nachricht mit Parametereinstellungen, wie unten dargestellt.
ms.assetid: 946bee83-91af-4647-9b22-96d42466352c
title: IMN_SETCOMPOSITIONFONT Benachrichtigungscode (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a5ec4fd5ba8237a1fbba9be3878037c37dc74c2e07f29026ca89ead91512f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949190"
---
# <a name="imn_setcompositionfont-notification-code"></a>IMN \_ SETCOMPOSITIONFONT-Benachrichtigungscode

Benachrichtigt eine Anwendung, wenn die Schriftart des Eingabekontexts aktualisiert wird. Die Anwendung empfängt diesen Befehl über die [**WM \_ IME \_ NOTIFY-Nachricht**](wm-ime-notify.md) mit Parametereinstellungen, wie unten dargestellt.


```C++
IMN_SETCOMPOSITIONFONT
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMN \_ SETCOMPOSITIONFONT fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Befehl hat keinen Rückgabewert.

## <a name="remarks"></a>Hinweise

Die Anwendung kann Mithilfe der [**ImmGetCompositionFont-Funktion**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) Informationen zur Schriftart abrufen. Das IME-Fenster verwendet anschließend die Schriftart, um die Kompositionszeichenfolge zu zeichnen.

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

[**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)
</dt> <dt>

[**WM \_ IME \_ NOTIFY**](wm-ime-notify.md)
</dt> </dl>

 

 




