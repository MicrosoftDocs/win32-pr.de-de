---
description: Markiert eine Anwendung, wenn eine ausgewählte IME Informationen zum Kandidaten Fenster benötigt. Die Anwendung empfängt diesen Befehl über die WM- \_ IME- \_ Anforderungs Nachricht mit den Parametereinstellungen, wie unten gezeigt.
ms.assetid: 35849290-a5be-406f-82f5-4a7e2af48586
title: IMR_CANDIDATEWINDOW Benachrichtigungs Code (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edb905acace27cc9bb04ce2b14dc6a685b7c4f8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362210"
---
# <a name="imr_candidatewindow-notification-code"></a>IMR \_ candidatewindow-Benachrichtigungs Code

Markiert eine Anwendung, wenn eine ausgewählte IME Informationen zum Kandidaten Fenster benötigt. Die Anwendung empfängt diesen Befehl über die [**WM- \_ IME- \_ Anforderungs**](wm-ime-request.md) Nachricht mit den Parametereinstellungen, wie unten gezeigt.


```C++
LRESULT IMR_CANDIDATEWINDOW
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Legen Sie auf IMR \_ candidatewindow fest.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Zeiger auf einen Puffer, der eine [**candidateform**](/windows/win32/api/imm/ns-imm-candidateform) -Struktur enthält. Der zugehörige **dwIndex** -Member enthält den Index des Kandidaten Fensters, auf das verwiesen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn die Anwendung die [**candidateform**](/windows/win32/api/imm/ns-imm-candidateform) -Struktur füllt. Andernfalls gibt der Befehl 0 zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Befehl kann vom IME an ein Fenster gesendet werden, das das ISC \_ showuicandidatewindow-Flag im [**WM \_ IME \_ SetContext**](wm-ime-setcontext.md) -Nachrichten Handler gelöscht hat.

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

[**Candidateform**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> <dt>

[**WM- \_ IME- \_ Anforderung**](wm-ime-request.md)
</dt> <dt>

[**WM \_ IME \_ SetContext**](wm-ime-setcontext.md)
</dt> </dl>

 

 




