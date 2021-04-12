---
description: Benachrichtigt eine Anwendung, wenn eine IME im Begriff ist, eine Fehlermeldung oder andere Informationen anzuzeigen. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Benachrichtigungs Meldung mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: b898283a-af1a-484f-bfb8-e5d5c0ac8ee1
title: IMN_GUIDELINE Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4efc222f7bfceadecce0f14573cab66471b119d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345768"
---
# <a name="imn_guideline-notification-code"></a>\_Benachrichtigungs Code für IMN

Benachrichtigt eine Anwendung, wenn eine IME im Begriff ist, eine Fehlermeldung oder andere Informationen anzuzeigen. Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Benachrichtigungs**](wm-ime-notify.md) Meldung mit den Parametereinstellungen, wie unten gezeigt.


```C++
IMN_GUIDELINE
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf IMN- \_ Richtlinie fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Befehl weist keinen Rückgabewert auf.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung verarbeitet diesen Befehl durch Aufrufen der Funktion " [**immgetguideline**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) ", um die Fehlermeldung oder Informationen aus dem IME abzurufen.

Das IME-Fenster zeigt die Fehlermeldung oder die Informations Zeichenfolge in einem Informationsfenster an.

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

[**Immgetrichtrichtwert**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)
</dt> <dt>

[**WM- \_ IME \_ Benachrichtigen**](wm-ime-notify.md)
</dt> </dl>

 

 




