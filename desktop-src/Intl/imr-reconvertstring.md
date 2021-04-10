---
description: Benachrichtigt eine Anwendung, wenn eine ausgewählte IME eine Zeichenfolge für die erneute Konvertierung benötigt. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Anforderungs Nachricht mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: IMR_RECONVERTSTRING Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbb1caeedb729b176f116a15e64879d79d519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864883"
---
# <a name="imr_reconvertstring-notification-code"></a>IMR \_ reconvertstring-Benachrichtigungs Code

Benachrichtigt eine Anwendung, wenn eine ausgewählte IME eine Zeichenfolge für die erneute Konvertierung benötigt. Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Anforderungs**](wm-ime-request.md) Nachricht mit den Parametereinstellungen, wie unten gezeigt.


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf IMR \_ reconvertstring fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Zeiger auf einen Puffer, der die [**reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring) -Struktur und Zeichen folgen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die aktuelle Zeichen folgen Struktur der erneuten Konvertierung zurück. Wenn *LPARAM* auf **null** festgelegt ist, gibt die Anwendung die Größe des Puffers zurück, der zum Speichern der Struktur erforderlich ist. Der Befehl gibt 0 (null) zurück, wenn er nicht erfolgreich ist.

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

[**Reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**WM- \_ IME- \_ Anforderung**](wm-ime-request.md)
</dt> </dl>

 

 




