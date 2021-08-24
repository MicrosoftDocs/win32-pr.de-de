---
description: Eine Anwendung sendet die \_ WM-WININICHANGE-Nachricht an alle Fenster der obersten Ebene, nachdem sie eine Änderung an der WIN.INI-Datei vornehmen. Die SystemParametersInfo-Funktion sendet diese Nachricht, nachdem eine Anwendung die -Funktion verwendet, um eine Einstellung in WIN.INI zu ändern.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: WM_WININICHANGE Meldung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cfdfeff65c1580f0bd8373fdc5ef1eec409233a9624934ea67ba835ddf805e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810460"
---
# <a name="wm_wininichange-message"></a>WM \_ WININICHANGE-Nachricht

Eine Anwendung sendet die **\_ WM-WININICHANGE-Nachricht** an alle Fenster der obersten Ebene, nachdem sie eine Änderung an der WIN.INI-Datei vornehmen. Die [**SystemParametersInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) sendet diese Nachricht, nachdem eine Anwendung die -Funktion verwendet, um eine Einstellung in WIN.INI zu ändern.

> [!Note]  
> Die **WM \_ WININICHANGE-Nachricht** wird nur aus Gründen der Kompatibilität mit früheren Versionen des Systems bereitgestellt. Anwendungen sollten die [**WM \_ SETTINGCHANGE-Nachricht**](wm-settingchange.md) verwenden.

 

Ein Fenster empfängt diese Meldung über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_WININICHANGE                 0x001A
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des geänderten Systemparameters enthält. Diese Zeichenfolge kann beispielsweise der Name eines Registrierungsschlüssels oder der Name eines Abschnitts in der datei Win.ini sein. Dieser Parameter ist nicht besonders nützlich, um zu bestimmen, welcher Systemparameter geändert wurde. Wenn die Zeichenfolge beispielsweise ein Registrierungsname ist, gibt sie in der Regel nur den Blattknoten in der Registrierung und nicht den gesamten Pfad an. Darüber hinaus senden einige Anwendungen diese Nachricht, wobei *lParam* auf **NULL** festgelegt ist. Wenn Sie diese Meldung erhalten, sollten Sie im Allgemeinen alle Systemparametereinstellungen überprüfen und neu laden, die von Ihrer Anwendung verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn Sie diese Nachricht verarbeiten, geben Sie 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Um die **WM \_ WININICHANGE-Nachricht** an alle Fenster der obersten Ebene zu senden, verwenden Sie die [**SendMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-sendmessage) mit dem *hWnd-Parameter,* der auf **HWND \_ BROADCAST** festgelegt ist.

Aufrufe von Funktionen, die WIN.INI ändern, können stattdessen der Registrierung zugeordnet werden. Diese Zuordnung tritt auf, wenn WIN.INI und der geänderte Abschnitt in der Registrierung unter dem folgenden Schlüssel angegeben werden:

**HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ IniFileMapping**

Die Änderung am Speicherort hat keine Auswirkungen auf das Verhalten dieser Nachricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systemparametersinfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
