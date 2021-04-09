---
description: Eine Anwendung sendet die WM- \_ wininichange-Nachricht an alle Fenster der obersten Ebene, nachdem eine Änderung an der WIN.INI Datei vorgenommen wurde. Die SystemParametersInfo-Funktion sendet diese Nachricht, nachdem eine Anwendung die-Funktion verwendet hat, um eine Einstellung in WIN.INI zu ändern.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: WM_WININICHANGE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b8db6c4794a8c1a572f61028d32eaeaf578d0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958893"
---
# <a name="wm_wininichange-message"></a>WM- \_ wininichange-Meldung

Eine Anwendung sendet die **WM- \_ wininichange** -Nachricht an alle Fenster der obersten Ebene, nachdem eine Änderung an der WIN.INI Datei vorgenommen wurde. Die [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion sendet diese Nachricht, nachdem eine Anwendung die-Funktion verwendet hat, um eine Einstellung in WIN.INI zu ändern.

> [!Note]  
> Die **WM- \_ wininichange** -Nachricht wird nur aus Gründen der Kompatibilität mit früheren Versionen des Systems bereitgestellt. Anwendungen sollten die " [**WM \_ settingchange**](wm-settingchange.md) "-Meldung verwenden.

 

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.


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

Ein Zeiger auf eine Zeichenfolge, die den Namen des geänderten System Parameters enthält. Diese Zeichenfolge kann z. b. der Name eines Registrierungsschlüssels oder der Name eines Abschnitts in der Win.ini-Datei sein. Dieser Parameter ist nicht besonders nützlich, um zu bestimmen, welcher Systemparameter geändert wurde. Wenn die Zeichenfolge z. b. ein Registrierungs Name ist, gibt Sie in der Regel nur den Endknoten in der Registrierung und nicht den gesamten Pfad an. Außerdem senden einige Anwendungen diese Nachricht, wobei *LPARAM* auf **null** festgelegt ist. Wenn Sie diese Meldung erhalten, sollten Sie im Allgemeinen alle Systemparameter Einstellungen überprüfen und erneut laden, die von der Anwendung verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn Sie diese Meldung verarbeiten, wird NULL zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Um die **WM- \_ wininichange** -Nachricht an alle Fenster der obersten Ebene zu senden, verwenden Sie die [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion mit dem *HWND* -Parameter, der auf **HWND- \_ Broadcast** festgelegt ist.

Aufrufe von Funktionen, die WIN.INI ändern, können stattdessen der Registrierung zugeordnet werden. Diese Zuordnung tritt auf, wenn WIN.INI und der Abschnitt, der geändert wird, in der Registrierung unter dem folgenden Schlüssel angegeben werden:

**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ IniFileMapping**

Die Änderung am Speicherort hat keine Auswirkung auf das Verhalten dieser Nachricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
