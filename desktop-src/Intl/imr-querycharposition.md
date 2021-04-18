---
description: Benachrichtigt eine Anwendung, wenn der ausgewählte IME Informationen zu den Koordinaten eines Zeichens in der Kompositions Zeichenfolge benötigt. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Anforderungs Nachricht mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: cae7e5b3-8aaf-452d-80df-fb0ae04a342c
title: IMR_QUERYCHARPOSITION Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947eec9b3dd1f678d9266bb795214cf392629193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358434"
---
# <a name="imr_querycharposition-notification-code"></a>IMR \_ querycharposition-Benachrichtigungs Code

Benachrichtigt eine Anwendung, wenn der ausgewählte IME Informationen zu den Koordinaten eines Zeichens in der Kompositions Zeichenfolge benötigt. Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Anforderungs**](wm-ime-request.md) Nachricht mit den Parametereinstellungen, wie unten gezeigt.


```C++
LRESULT IMR_QUERYCHARPOSITION
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf IMR \_ querycharposition fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Zeiger auf eine [**imecharposition**](/windows/win32/api/imm/ns-imm-imecharposition) -Struktur, die die Position des Zeichens im Kompositionsfenster enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn die Anwendung die [**imecharposition**](/windows/win32/api/imm/ns-imm-imecharposition) -Struktur füllt. Andernfalls gibt der Befehl 0 zurück.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung, die die Kompositions Zeichenfolge selbst zeichnet, anstatt sich auf den IME zu verlassen, ist für das Ausfüllen aller Member der [**imecharposition**](/windows/win32/api/imm/ns-imm-imecharposition) -Struktur verantwortlich. Andernfalls sollte die Anwendung den Befehl an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) oder [**immisuimess**](/windows/desktop/api/Imm/nf-imm-immisuimessagea) übergeben, wenn Sie über ein eigenes IME-Benutzeroberflächen Fenster verfügt.

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

[**Imecharposition**](/windows/win32/api/imm/ns-imm-imecharposition)
</dt> <dt>

[**Immisuimess Age**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> <dt>

[**WM- \_ IME- \_ Anforderung**](wm-ime-request.md)
</dt> </dl>

 

 
