---
Description: Wird an ein Fenster gesendet, nachdem seine Größe geändert wurde.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: WM_SIZE (Winuser.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 473e4e63523c7b97968e54349e5882b7e589fc7238d717ccf96563b5ce93388e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548220"
---
# <a name="wm_size-message"></a>WM \_ SIZE-Meldung

Wird an ein Fenster gesendet, nachdem seine Größe geändert wurde.

Ein Fenster empfängt diese Nachricht über seine [**WindowProc-Funktion.**](/windows/win32/api/winuser/nf-winuser-defwindowproca)


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ der angeforderten Größenver ändern. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                   | Bedeutung                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <dt>**SIZE \_ MAXHIDE**</dt> <dt>4</dt> </dl>       | Die Meldung wird an alle Popupfenster gesendet, wenn ein anderes Fenster maximiert ist.<br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <dt>**SIZE \_ MAXIMIERT**</dt> <dt>2</dt> </dl> | Das Fenster wurde maximiert.<br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <dt>**SIZE \_ MAXSHOW**</dt> <dt>3</dt> </dl>       | Die Meldung wird an alle Popupfenster gesendet, wenn ein anderes Fenster auf seine frühere Größe wiederhergestellt wurde.<br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <dt>**SIZE \_ MINIMIERT 1**</dt> <dt></dt> </dl> | Das Fenster wurde minimiert.<br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <dt>**SIZE \_ RESTORED**</dt> <dt>0</dt> </dl>    | Die Größe des Fensters wurde geändert, aber weder der **Wert SIZE \_ MINIMIZED** noch **SIZE \_ MAXIMIZED gilt.**<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Das niedrige Wort *lParam* gibt die neue Breite des Clientbereichs an.

Das obere Wort *lParam* gibt die neue Höhe des Clientbereichs an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte sie 0 (null) zurückgeben.

## <a name="example"></a>Beispiel

```cpp
/******************************************************************
*                                                                 *
*  SimpleText::OnResize                                           *
*                                                                 *
*  If the application receives a WM_SIZE message, this method     *
*  resize the render target appropriately.                        *
*                                                                 *
******************************************************************/

void SimpleText::OnResize(UINT width, UINT height)
{
    if (pRT_)
    {
        D2D1_SIZE_U size;
        size.width = width;
        size.height = height;
        pRT_->Resize(size);
    }
}

LRESULT CALLBACK SimpleText::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
   
    SimpleText *pSimpleText = reinterpret_cast<SimpleText *>(
                ::GetWindowLongPtr(hwnd, GWLP_USERDATA));

    if (pSimpleText)
    {
        switch(message)
        {
        case WM_SIZE:
            {
                UINT width = LOWORD(lParam);
                UINT height = HIWORD(lParam);
                pSimpleText->OnResize(width, height);
            }
            return 0;

// ...

```

Beispiel aus [Windows klassischen Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) auf GitHub.

## <a name="remarks"></a>Hinweise

Wenn die [**Funktion SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) oder [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) als Ergebnis der **WM \_ SIZE-Meldung** für ein untergeordnetes Fenster aufgerufen wird, sollte der *Parameter bRedraw* oder *bRepaint* ungleich 0 (null) sein, damit das Fenster neu gepaint wird.

Obwohl die Breite und Höhe eines Fensters 32-Bit-Werte sind, enthält der *lParam-Parameter* nur die niedrigen 16 Bits von jedem.

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sendet die **NACHRICHTEN WM \_ SIZE** und **WM \_ MOVE,** wenn sie die [**WM \_ WINDOWPOSCHANGED-Nachricht**](wm-windowposchanged.md) verarbeitet.
Die **NACHRICHTEN WM \_ SIZE** und **WM \_ MOVE** werden nicht gesendet, wenn eine Anwendung die **WM \_ WINDOWPOSCHANGED-Nachricht** ohne Aufruf von **DefWindowProc verarbeitet.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**\_WM-FENSTERPOSCHANGED**](wm-windowposchanged.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)
</dt> </dl>

 

 
