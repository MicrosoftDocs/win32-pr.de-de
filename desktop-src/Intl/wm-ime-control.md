---
description: Wird von einer Anwendung gesendet, um das IME-Fenster an den angeforderten Befehl weiterzuleiten.
ms.assetid: 5d3b7f8a-57c9-41e3-8022-9a3f515fc32e
title: WM_IME_CONTROL Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd0adc534883bc0b31984c8d3e9b57a04b555987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862651"
---
# <a name="wm_ime_control-message"></a>WM_IME_CONTROL Meldung

Wird von einer Anwendung gesendet, um das IME-Fenster an den angeforderten Befehl weiterzuleiten. Die Anwendung verwendet diese Nachricht, um das von ihr erstellte IME-Fenster zu steuern. Um diese Nachricht zu senden, ruft die Anwendung die [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion mit den folgenden Parametern auf.


```C++
SendMessage(
  HWND   hwnd,
  WM_IME_CONTROL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* 
</dt> <dd>

Handle für das Fenster.

</dd> <dt>

*wParam* 
</dt> <dd>

Der Befehl. Dieser Parameter kann einen der folgenden Werte aufweisen:

<dl>
<dd><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></dd> 
<dd><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></dd> 
<dd><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></dd> 
<dd><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></dd> 
<dd><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></dd> 
<dd><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></dd> 
<dd><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></dd> 
<dd><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></dd> 
<dd><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></dd> 
<dd><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></dd> 
</dl>
</dd>

<dt>

*lParam* 
</dt> <dd>

Befehls spezifische Daten, wobei das Format vom Wert des Parameters " *wParam* " abhängig ist. Weitere Informationen finden Sie in der Dokumentation zu den einzelnen Befehlen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Meldung gibt einen Befehls spezifischen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                                                      |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen); </dt> <dt>Imm. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Eingabemethoden-Manager-Meldungen](input-method-manager-messages.md)
</dt> <dt>

[IMC_CLOSESTATUSWINDOW](imc-closestatuswindow.md)
</dt> <dt>

[IMC_GETCANDIDATEPOS](imc-getcandidatepos.md)
</dt> <dt>

[IMC_GETCOMPOSITIONFONT](imc-getcompositionfont.md)
</dt> <dt>

[IMC_GETCOMPOSITIONWINDOW](imc-getcompositionwindow.md)
</dt> <dt>

[IMC_GETSTATUSWINDOWPOS](imc-getstatuswindowpos.md)
</dt> <dt>

[IMC_OPENSTATUSWINDOW](imc-openstatuswindow.md)
</dt> <dt>

[IMC_SETCANDIDATEPOS](imc-setcandidatepos.md)
</dt> <dt>

[IMC_SETCOMPOSITIONFONT](imc-setcompositionfont.md)
</dt> <dt>

[IMC_SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md)
</dt> <dt>

[IMC_SETSTATUSWINDOWPOS](imc-setstatuswindowpos.md)
</dt> </dl>

 

 
