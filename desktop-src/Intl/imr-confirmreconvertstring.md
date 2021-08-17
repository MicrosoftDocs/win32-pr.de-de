---
description: Benachrichtigt eine Anwendung, wenn die IME die RECONVERTSTRING-Struktur ändern muss. Die Anwendung empfängt diesen Befehl über die WM \_ IME \_ REQUEST-Nachricht mit Parametereinstellungen, wie unten dargestellt.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: IMR_CONFIRMRECONVERTSTRING Benachrichtigungscode (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a0fd1c38c7552d09489c51b9acc897f679aa3a218e86bbba222225fcff57e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948797"
---
# <a name="imr_confirmreconvertstring-notification-code"></a>IMR \_ CONFIRMRECONVERTSTRING-Benachrichtigungscode

Benachrichtigt eine Anwendung, wenn die IME die [**RECONVERTSTRING-Struktur**](/windows/win32/api/imm/ns-imm-reconvertstring) ändern muss. Die Anwendung empfängt diesen Befehl über die [**WM \_ IME \_ REQUEST-Nachricht**](wm-ime-request.md) mit Parametereinstellungen, wie unten dargestellt.


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMR \_ CONFIRMRECONVERTSTRING fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Zeiger auf eine [**RECONVERTSTRING-Struktur**](/windows/win32/api/imm/ns-imm-reconvertstring) aus dem IME. Weitere Informationen finden Sie im Abschnitt "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn die Anwendung die geänderte [**RECONVERTSTRING-Struktur**](/windows/win32/api/imm/ns-imm-reconvertstring) akzeptiert. Andernfalls gibt der Befehl 0 zurück, und die IME verwendet die ursprüngliche **RECONVERTSTRING-Struktur.**

## <a name="remarks"></a>Hinweise

Die Anwendung füllt die [**RECONVERTSTRING-Struktur**](/windows/win32/api/imm/ns-imm-reconvertstring) nach dem Empfang des [IMR \_ RECONVERTSTRING-Befehls](imr-reconvertstring.md) aus.

Nachdem die Anwendung [IMR \_ RECONVERTSTRING](imr-reconvertstring.md)verarbeitet hat, kann die IME die [**RECONVERTSTRING-Struktur**](/windows/win32/api/imm/ns-imm-reconvertstring) anpassen oder nicht. Die IME sendet WM \_ IME \_ REQUEST mit **IMR \_ CONFIRMRECONVERTSTRING,** um die Änderungen an der **RECONVERTSTRING-Struktur** zu bestätigen. Wenn die Anwendung **TRUE** für **IMR \_ CONFIRMRECONVERTSTRING** zurückgibt, generiert die IME eine neue Kompositionszeichenfolge basierend auf der **RECONVERTSTRING-Struktur** für den **BEFEHL IMR \_ CONFIRMRECONVERTSTRING.** Wenn die Anwendung **FALSE** für **IMR \_ CONFIRMRECONVERTSTRING** zurückgibt, generiert die IME eine neue Kompositionszeichenfolge basierend auf der ursprünglichen **RECONVERTSTRING-Struktur,** die von der Anwendung im IMR \_ RECONVERTSTRING-Befehl angegeben wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Befehle des Eingabemethoden-Managers](input-method-manager-commands.md)
</dt> <dt>

[IMR \_ RECONVERTSTRING](imr-reconvertstring.md)
</dt> <dt>

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**WM \_ IME \_ REQUEST**](wm-ime-request.md)
</dt> </dl>

 

 




