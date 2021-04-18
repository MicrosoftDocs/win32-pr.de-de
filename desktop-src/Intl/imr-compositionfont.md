---
description: Benachrichtigt eine Anwendung, wenn eine ausgewählte IME Informationen über die Schriftart benötigt, die vom Kompositionsfenster verwendet wird. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Anforderungs Nachricht mit Parametern, wie unten gezeigt.
ms.assetid: 46bb71ee-8dc9-4ef0-bc4e-59866c122bf7
title: IMR_COMPOSITIONFONT Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2751944e451475fd0bde9a34d8902dcaf30e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358877"
---
# <a name="imr_compositionfont-notification-code"></a>IMR \_ compositionfont-Benachrichtigungs Code

Benachrichtigt eine Anwendung, wenn eine ausgewählte IME Informationen über die Schriftart benötigt, die vom Kompositionsfenster verwendet wird. Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Anforderungs**](wm-ime-request.md) Nachricht mit Parametern, wie unten gezeigt.


```C++
LRESULT IMR_COMPOSITIONFONT
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf IMR \_ compositionfont fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Zeiger auf einen Puffer, der eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur enthält. Die Anwendung füllt die Werte für das aktuelle Kompositionsfenster aus.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn die Anwendung die [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur füllt. Andernfalls gibt der Befehl 0 zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Befehl kann vom IME an ein Fenster gesendet werden, das das ISC \_ showuicompositionwindow-Flag im [**WM \_ IME \_ SetContext**](wm-ime-setcontext.md) -Nachrichten Handler gelöscht hat.

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

[**WM- \_ IME- \_ Anforderung**](wm-ime-request.md)
</dt> <dt>

[**WM \_ IME \_ SetContext**](wm-ime-setcontext.md)
</dt> </dl>

 

 
