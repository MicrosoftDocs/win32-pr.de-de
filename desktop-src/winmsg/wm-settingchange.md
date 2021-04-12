---
description: Eine Meldung, die an alle Fenster der obersten Ebene gesendet wird, wenn die SystemParametersInfo-Funktion eine systemweite Einstellung ändert oder wenn sich die Richtlinien Einstellungen geändert haben.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: WM_SETTINGCHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c3d1360b5e4cc5de2dbd23b09b8f2ad034948f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218211"
---
# <a name="wm_settingchange-message"></a>WM- \_ settingchange-Meldung

Eine Meldung, die an alle Fenster der obersten Ebene gesendet wird, wenn die [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion eine systemweite Einstellung ändert oder wenn sich die Richtlinien Einstellungen geändert haben.

Anwendungen sollten **WM \_ settingchange** an alle Fenster der obersten Ebene senden, wenn Sie Änderungen an den Systemparametern vornehmen. (Diese Nachricht kann nicht direkt an ein Fenster gesendet werden.) Um die **WM- \_ settingchange** -Nachricht an alle Fenster der obersten Ebene zu senden, verwenden Sie die [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) -Funktion mit dem *HWND* -Parameter, der auf **HWND- \_ Broadcast** festgelegt ist.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wenn das System diese Nachricht als Ergebnis eines [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Aufrufes sendet, ist der *wParam* -Parameter der Wert des *uiaction* -Parameters, der an die **SystemParametersInfo** -Funktion übergeben wird. Eine Liste der Werte finden Sie unter **SystemParametersInfo**.

Wenn das System diese Nachricht aufgrund einer Änderung der Richtlinien Einstellungen sendet, gibt dieser Parameter den Typ der angewendeten Richtlinie an. Dieser Wert ist 1, wenn die Computer Richtlinie angewendet wurde, oder NULL, wenn die Benutzer Richtlinie angewendet wurde.

Wenn das System diese Nachricht aufgrund einer Änderung der Gebiets Schema Einstellungen sendet, ist dieser Parameter 0 (null).

Wenn eine Anwendung diese Nachricht sendet, muss dieser Parameter **null** sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Wenn das System diese Nachricht als Ergebnis eines [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Aufrufes sendet, ist *LPARAM* ein Zeiger auf eine Zeichenfolge, die den Bereich angibt, der den geänderten Systemparameter enthält. Dieser Parameter gibt in der Regel nicht an, welcher spezifische Systemparameter geändert wurde. (Beachten Sie, dass einige Anwendungen diese Nachricht senden, wobei *LPARAM* auf **null** festgelegt ist.) Wenn Sie diese Meldung erhalten, sollten Sie im Allgemeinen alle Systemparameter Einstellungen überprüfen und erneut laden, die von der Anwendung verwendet werden.

Diese Zeichenfolge kann der Name eines Registrierungsschlüssels oder der Name eines Abschnitts in der Win.ini-Datei sein. Wenn die Zeichenfolge ein Registrierungs Name ist, gibt Sie in der Regel nur den Endknoten in der Registrierung an, nicht den vollständigen Pfad.

Wenn das System diese Nachricht aufgrund einer Änderung der Richtlinien Einstellungen sendet, verweist dieser Parameter auf die Zeichenfolge "Policy".

Wenn das System diese Nachricht aufgrund einer Änderung der Gebiets Schema Einstellungen sendet, verweist dieser Parameter auf die Zeichenfolge "Intl".

Um eine Änderung in den Umgebungsvariablen für das System oder den Benutzer zu beeinflussen, senden Sie diese Meldung mit *LPARAM* , die auf die Zeichenfolge "Environment" festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn Sie diese Meldung verarbeiten, wird NULL zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Der *LPARAM* -Parameter gibt an, welche Systemmetrik sich geändert hat, z. b. "cabriblelockemode", wenn der "konvertierte Indikator" geändert wurde, oder "systemdockmode", wenn der angedockte Indikator umgeschaltet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Richtlinien Ereignisse](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[**Von SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
