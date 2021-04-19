---
Description: Wird an ein Fenster gesendet, nachdem sich die Größe geändert hat.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: WM_SIZE Meldung (Winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 04afafd3faafc4ea8c400472254dcf4ec4afa050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362173"
---
# <a name="wm_size-message"></a>WM- \_ Größen Meldung

Wird an ein Fenster gesendet, nachdem sich die Größe geändert hat.

Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) -Funktion.


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ der angeforderten Größe der Größe. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                   | Bedeutung                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <dt>**Größe \_ Maxhide**</dt> <dt>4</dt> </dl>       | Die Nachricht wird an alle Popup Fenster gesendet, wenn ein anderes Fenster maximiert ist.<br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <dt>**Größe \_ Maximiert**</dt> <dt>2</dt> </dl> | Das Fenster wurde maximiert.<br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <dt>**Größe \_ Maxshow**</dt> <dt>3</dt> </dl>       | Die Nachricht wird an alle Popup Fenster gesendet, wenn ein anderes Fenster auf die frühere Größe wieder hergestellt wurde.<br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <dt>**Größe \_ Minimiert**</dt> <dt>1</dt> </dl> | Das Fenster wurde minimiert.<br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <dt>**Größe \_ Wieder hergestellt**</dt> <dt>0</dt> </dl>    | Die Größe des Fensters wurde geändert, aber weder die **\_ minimierte Größe** noch die **Größe des \_ maximierten** Werts.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort von *LPARAM* gibt die neue Breite des Client Bereichs an.

Das hochwertige Wort von *LPARAM* gibt die neue Höhe des Client Bereichs an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **LRESULT**

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

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

Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) auf GitHub.

## <a name="remarks"></a>Bemerkungen

Wenn die Funktion " [**setscrollpos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) " oder " [**muvewindow**](/windows/win32/api/winuser/nf-winuser-movewindow) " als Ergebnis der **WM- \_ Größen** Meldung für ein untergeordnetes Fenster aufgerufen wird, sollte der *bredraw* -Parameter oder der *brepaint* -Parameter nicht NULL sein, damit das Fenster neu gezeichnet wird.

Obwohl die Breite und Höhe eines Fensters 32-Bit-Werte ist, enthält der *LPARAM* -Parameter nur die nieder wertigen 16 Bits der einzelnen Werte.

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion sendet die **WM- \_ Größe** und die WM-Verschiebungs Nachricht, wenn Sie die [**WM- \_ windowposchge**](wm-windowposchanged.md) -Nachricht verarbeitet. **\_**
Die **WM- \_ Größe** und die WM-Verschiebungs Nachricht werden nicht gesendet, wenn eine Anwendung die **WM- \_ windowposchangsnachricht** verarbeitet, ohne **defwindowproc** Aufrufs. **\_**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**Fenster**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**WM-Windows-Server \_**](wm-windowposchanged.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Setscrollpos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)
</dt> </dl>

 

 
