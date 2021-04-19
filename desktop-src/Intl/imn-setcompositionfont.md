---
description: Benachrichtigt eine Anwendung, wenn die Schriftart des Eingabe Kontexts aktualisiert wird. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 946bee83-91af-4647-9b22-96d42466352c
title: IMN_SETCOMPOSITIONFONT Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8373954e80e420004b347bf1b40021c86ddbb876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359490"
---
# <a name="imn_setcompositionfont-notification-code"></a>IMN \_ setcompositionfont-Benachrichtigungs Code

Benachrichtigt eine Anwendung, wenn die Schriftart des Eingabe Kontexts aktualisiert wird. Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.


```C++
IMN_SETCOMPOSITIONFONT
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf IMN \_ setcompositionfont fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Befehl weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Die Anwendung kann Informationen über die Schriftart mithilfe der [**immgetcompositionfont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) -Funktion erhalten. Das IME-Fenster verwendet anschließend die Schriftart zum Zeichnen der Kompositions Zeichenfolge.

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

[**Immgetcompositionfont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)
</dt> <dt>

[**WM- \_ IME \_ Benachrichtigen**](wm-ime-notify.md)
</dt> </dl>

 

 




