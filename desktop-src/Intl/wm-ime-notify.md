---
description: Wird an eine Anwendung gesendet, um sie über Änderungen am IME-Fenster zu benachrichtigen. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 20e064b8-2baf-4b4c-8341-36c3e4643eff
title: WM_IME_NOTIFY Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a072ff41b5731662afa94e387ec48de7d14bc245906e581303fe976dcf455708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014218"
---
# <a name="wm_ime_notify-message"></a>WM_IME_NOTIFY Meldung

Wird an eine Anwendung gesendet, um sie über Änderungen am IME-Fenster zu benachrichtigen. Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_NOTIFY,   
  WPARAM wParam,   
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Hwnd* 
</dt> <dd>

Ein Handle für fenster.

</dd> <dt>

*wParam* 
</dt> <dd>

Der Befehl. Dieser Parameter kann einen der folgenden Werte aufweisen.

<dl>
<dd><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></dd> 
<dd><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></dd> 
<dd><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></dd> 
<dd><a href="imn-guideline.md">IMN_GUIDELINE</a></dd> 
<dd><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></dd> 
<dd><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></dd> 
<dd><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></dd> 
<dd><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></dd> 
<dd><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></dd> 
<dd><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></dd> 
<dd><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></dd> 
<dd><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></dd> 
<dd><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></dd> 
</dl> 
</dd> 
<dt>

*lParam* 
</dt> <dd>

Befehlsspezifische Daten, wobei das Format vom Wert des *wParam-Parameters* abhängig ist. Weitere Informationen finden Sie in der Dokumentation zu den einzelnen Befehlen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert hängt vom gesendeten Befehl ab.

## <a name="remarks"></a>Hinweise

Eine Anwendung verarbeitet diese Nachricht, wenn sie für die Verwaltung des IME-Fensters zuständig ist.

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

[IMN_CHANGECANDIDATE](imn-changecandidate.md)
</dt> <dt>

[IMN_CLOSECANDIDATE](imn-closecandidate.md)
</dt> <dt>

[IMN_CLOSESTATUSWINDOW](imn-closestatuswindow.md)
</dt> <dt>

[IMN_GUIDELINE](imn-guideline.md)
</dt> <dt>

[IMN_OPENCANDIDATE](imn-opencandidate.md)
</dt> <dt>

[IMN_OPENSTATUSWINDOW](imn-openstatuswindow.md)
</dt> <dt>

[IMN_SETCANDIDATEPOS](imn-setcandidatepos.md)
</dt> <dt>

[IMN_SETCOMPOSITIONFONT](imn-setcompositionfont.md)
</dt> <dt>

[IMN_SETCOMPOSITIONWINDOW](imn-setcompositionwindow.md)
</dt> <dt>

[IMN_SETCONVERSIONMODE](imn-setconversionmode.md)
</dt> <dt>

[IMN_SETOPENSTATUS](imn-setopenstatus.md)
</dt> <dt>

[IMN_SETSENTENCEMODE](imn-setsentencemode.md)
</dt> <dt>

[IMN_SETSTATUSWINDOWPOS](imn-setstatuswindowpos.md)
</dt> </dl>

 

 
