---
description: Wird von einer Anwendung gesendet, um das IME-Fenster anweisen, den angeforderten Befehl auszuführen.
ms.assetid: 5d3b7f8a-57c9-41e3-8022-9a3f515fc32e
title: WM_IME_CONTROL Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104ef8eb2a90c7c55eb0d4bca2fcdb1744dd9433f131b753e962fcfec571f43d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822470"
---
# <a name="wm_ime_control-message"></a>WM_IME_CONTROL Meldung

Wird von einer Anwendung gesendet, um das IME-Fenster anweisen, den angeforderten Befehl auszuführen. Die Anwendung verwendet diese Meldung, um das erstellte IME-Fenster zu steuern. Um diese Nachricht zu senden, ruft die Anwendung die [**SendMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-sendmessage) mit den folgenden Parametern auf.


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

*Hwnd* 
</dt> <dd>

Handle zum Fenster.

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

Befehlsspezifische Daten, wobei das Format vom Wert des *wParam-Parameters abhängt.* Weitere Informationen finden Sie in der Dokumentation zu den einzelnen Befehlen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Meldung gibt einen befehlsspezifischen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                                                      |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h);</dt> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Eingabemethoden-Manager-Nachrichten](input-method-manager-messages.md)
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

 

 
