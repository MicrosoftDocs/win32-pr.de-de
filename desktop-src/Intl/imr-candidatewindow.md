---
description: Keine Anwendung, wenn ein ausgewählter IME Informationen zum Kandidatenfenster benötigt. Die Anwendung empfängt diesen Befehl über die WM \_ IME \_ REQUEST-Nachricht mit Parametereinstellungen, wie unten dargestellt.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: IMR_CANDIDATEWINDOW Benachrichtigungscode (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9376ff08e0406ff5505107ea1a04cf4e62898660065a8c7fdd54a1b8606850c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810114"
---
# <a name="imr_candidatewindow-notification-code"></a>IMR \_ CANDIDATEWINDOW-Benachrichtigungscode

Keine Anwendung, wenn ein ausgewählter IME Informationen zum Kandidatenfenster benötigt. Die Anwendung empfängt diesen Befehl über die [**WM \_ IME \_ REQUEST-Nachricht**](wm-ime-request.md) mit Parametereinstellungen, wie unten dargestellt.


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Legen Sie auf IMR \_ CANDIDATEWINDOW fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Zeiger auf einen Puffer, der eine [**CANDIDATEFORM-Struktur**](/windows/win32/api/imm/ns-imm-candidateform) enthält. Das **dwIndex-Member** enthält den Index des Kandidatenfensters, auf das verwiesen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn die Anwendung die [**CANDIDATEFORM-Struktur ausfüllt.**](/windows/win32/api/imm/ns-imm-candidateform) Andernfalls gibt der Befehl 0 zurück.

## <a name="remarks"></a>Hinweise

Dieser Befehl kann vom IME an ein Fenster gesendet werden, das das ISC \_ SHOWUICKATDATEWINDOW-Flag im [**WM \_ IME \_ SETCONTEXT-Meldungshandler**](wm-ime-setcontext.md) entfernt hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Eingabemethode-Manager](input-method-manager.md)
</dt> <dt>

[Befehle des Eingabemethode-Managers](input-method-manager-commands.md)
</dt> <dt>

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**WM \_ \_ IME-ANFORDERUNG**](wm-ime-request.md)
</dt> <dt>

[**WM \_ IME \_ SETCONTEXT**](wm-ime-setcontext.md)
</dt> </dl>

 

 




