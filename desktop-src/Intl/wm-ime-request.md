---
description: Wird an eine Anwendung gesendet, um Befehle bereitzustellen und Informationen anzufordern. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: c5e9f256-eed2-46cb-bb33-0e640a975f1f
title: WM_IME_REQUEST Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d73f1f920efb2908104304fcbc08fd19d648e52fdb737f12027b47436531eb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927630"
---
# <a name="wm_ime_request-message"></a>WM_IME_REQUEST Meldung

Wird an eine Anwendung gesendet, um Befehle bereitzustellen und Informationen anzufordern. Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_REQUEST,  
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

Befehl. Dieser Parameter kann einen der folgenden Werte aufweisen:

<dl> 
<dd><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></dd> 
<dd><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></dd> 
<dd><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></dd> 
<dd><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></dd> 
<dd><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></dd> 
<dd><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></dd> 
<dd><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></dd> 
</dl> 
</dd> 
<dt>

*lParam* 
</dt> <dd>

Befehlsspezifische Daten. Weitere Informationen finden Sie in der Beschreibung der einzelnen Befehle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen befehlsspezifischen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                                                      |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h);</dt> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eingabemethoden-Manager](input-method-manager.md)
</dt> <dt>

[Eingabemethoden-Manager-Nachrichten](input-method-manager-messages.md)
</dt> <dt>

[IMR_CANDIDATEWINDOW](imr-candidatewindow.md)
</dt> <dt>

[IMR_COMPOSITIONFONT](imr-compositionfont.md)
</dt> <dt>

[IMR_COMPOSITIONWINDOW](imr-compositionwindow.md)
</dt> <dt>

[IMR_CONFIRMRECONVERTSTRING](imr-confirmreconvertstring.md)
</dt> <dt>

[IMR_DOCUMENTFEED](imr-documentfeed.md)
</dt> <dt>

[IMR_QUERYCHARPOSITION](imr-querycharposition.md)
</dt> <dt>

[IMR_RECONVERTSTRING](imr-reconvertstring.md)
</dt> </dl>

 

 
