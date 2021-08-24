---
description: Eine Meldung, die an alle Fenster der obersten Ebene gesendet wird, wenn die SystemParametersInfo-Funktion eine systemweite Einstellung ändert oder wenn die Richtlinieneinstellungen geändert wurden.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: WM_SETTINGCHANGE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302f156da905263ed7f3d1d331d4dbb25af5b3e81d9df6136281c7dbc7b3914c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710040"
---
# <a name="wm_settingchange-message"></a>WM \_ SETTINGCHANGE-Meldung

Eine Meldung, die an alle Fenster der obersten Ebene gesendet wird, wenn die [**SystemParametersInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) eine systemweite Einstellung ändert oder wenn die Richtlinieneinstellungen geändert wurden.

Anwendungen sollten **WM \_ SETTINGCHANGE an** alle Fenster der obersten Ebene senden, wenn sie Änderungen an Systemparametern vornehmen. (Diese Nachricht kann nicht direkt an ein Fenster gesendet werden.) Um die **WM \_ SETTINGCHANGE-Nachricht** an alle Fenster der obersten Ebene zu senden, verwenden Sie die [**SendMessageTimeout-Funktion**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) mit dem *hwnd-Parameter,* der auf **HWND \_ BROADCAST festgelegt ist.**

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wenn das System diese Nachricht als Ergebnis eines [**SystemParametersInfo-Aufrufs**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) sendet, ist der *wParam-Parameter* der Wert des *uiAction-Parameters,* der an die **SystemParametersInfo-Funktion übergeben** wird. Eine Liste der Werte finden Sie unter **SystemParametersInfo**.

Wenn das System diese Nachricht als Ergebnis einer Änderung der Richtlinieneinstellungen sendet, gibt dieser Parameter den Typ der angewendeten Richtlinie an. Dieser Wert ist 1, wenn die Computerrichtlinie angewendet wurde, oder 0 (null), wenn die Benutzerrichtlinie angewendet wurde.

Wenn das System diese Nachricht als Ergebnis einer Änderung der Locale-Einstellungen sendet, ist dieser Parameter 0 (null).

Wenn eine Anwendung diese Nachricht sendet, muss dieser Parameter **NULL sein.**

</dd> <dt>

*lParam* 
</dt> <dd>

Wenn das System diese Nachricht als Ergebnis eines [**SystemParametersInfo-Aufrufs**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) sendet, ist *lParam* ein Zeiger auf eine Zeichenfolge, die den Bereich angibt, der den geänderten Systemparameter enthält. Dieser Parameter gibt in der Regel nicht an, welcher bestimmte Systemparameter geändert wurde. (Beachten Sie, dass einige Anwendungen diese Nachricht senden, bei der *lParam* auf **NULL festgelegt ist.)** Wenn Sie diese Meldung erhalten, sollten Sie im Allgemeinen alle Systemparametereinstellungen überprüfen und erneut laden, die von Ihrer Anwendung verwendet werden.

Diese Zeichenfolge kann der Name eines Registrierungsschlüssels oder der Name eines Abschnitts in der Win.ini sein. Wenn die Zeichenfolge ein Registrierungsname ist, gibt sie in der Regel nur den Blattknoten in der Registrierung an, nicht den vollständigen Pfad.

Wenn das System diese Nachricht als Ergebnis einer Änderung der Richtlinieneinstellungen sendet, zeigt dieser Parameter auf die Zeichenfolge "Policy".

Wenn das System diese Nachricht als Ergebnis einer Änderung der Locale-Einstellungen sendet, zeigt dieser Parameter auf die Zeichenfolge "intl".

Um eine Änderung der Umgebungsvariablen für das System oder den Benutzer zu erzielen, übertragen Sie diese Nachricht mit *lParam,* das auf die Zeichenfolge "Environment" festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn Sie diese Meldung verarbeiten, geben Sie 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Der *lParam-Parameter* gibt an, welche Systemmetrik sich geändert hat, z. B. "ConvertibleSlateMode", wenn der Indikator CONVERTIBLESLATEMODE umschaltet wurde, oder "SystemDockMode", wenn der DOCKED-Indikator umschaltet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Richtlinienereignisse](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[**Systemparametersinfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
