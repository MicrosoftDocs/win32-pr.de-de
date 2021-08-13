---
Description: Wird als Signal gesendet, dass ein Fenster oder eine Anwendung beendet werden soll.
ms.assetid: 19500baf-e0ad-4dfa-804f-6a6e0652cffb
title: WM_CLOSE (Winuser.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: ebe027935391bc1e8946b8691a17f026b39b398ebefee2ea6f6e3765fcaa0c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436353"
---
# <a name="wm_close-message"></a>WM \_ CLOSE-Meldung

Wird als Signal gesendet, dass ein Fenster oder eine Anwendung beendet werden soll.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_CLOSE                        0x0010
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="example"></a>Beispiel

```cpp
LRESULT CALLBACK WindowProc(
    __in HWND hWindow,
    __in UINT uMsg,
    __in WPARAM wParam,
    __in LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_CLOSE:
        DestroyWindow(hWindow);
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWindow, uMsg, wParam, lParam);
    }

    return 0;
}
```
Beispiel aus [Windows klassischen Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/RadialController/cpp/RadialController.cpp) auf GitHub.


## <a name="remarks"></a>Hinweise

Eine Anwendung kann den Benutzer vor dem Zerstören eines Fensters zur Bestätigung auffordern, indem die **WM \_ CLOSE-Nachricht** verarbeitet und die [**DestroyWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-destroywindow) nur dann aufruft, wenn der Benutzer die Auswahl bestätigt.

Standardmäßig ruft die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) die [**DestroyWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-destroywindow) auf, um das Fenster zu zerstören.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
