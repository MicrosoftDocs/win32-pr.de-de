---
description: Benachrichtigt eine Anwendung, wenn der Konvertierungsmodus des Eingabe Kontexts aktualisiert wird. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 62bb9717-cc41-4e34-af1a-ff41324bd3a9
title: IMN_SETCONVERSIONMODE Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c0ba945b9988ddb32d86c2005ec240c16f82ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352664"
---
# <a name="imn_setconversionmode-notification-code"></a>IMN \_ setcoversionmode-Benachrichtigungs Code

Benachrichtigt eine Anwendung, wenn der Konvertierungsmodus des Eingabe Kontexts aktualisiert wird. Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.


```C++
IMN_SETCONVERSIONMODE
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie diese Einstellung auf IMN \_ SetConfiguration-Mode fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Befehl weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Die Anwendung kann Informationen über den Konvertierungsmodus mithilfe der [**immgetkonversionstatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) -Funktion erhalten.

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

[**Immgetsystemversionstatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[**WM- \_ IME \_ Benachrichtigen**](wm-ime-notify.md)
</dt> </dl>

 

 




