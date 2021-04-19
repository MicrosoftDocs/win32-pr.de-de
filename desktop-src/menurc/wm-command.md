---
title: WM_COMMAND Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer ein Befehls Element aus einem Menü auswählt, wenn ein Steuerelement eine Benachrichtigungs Meldung an das übergeordnete Fenster sendet oder wenn eine Tastenkombination für die Zugriffstaste übersetzt wird.
ms.assetid: 5516098e-fd90-49c8-afb0-78164b028376
keywords:
- WM_COMMAND von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_COMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1826c4668f3be8a2991c914e60320b55de867e33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369158"
---
# <a name="wm_command-message"></a>WM- \_ Befehls Meldung

Wird gesendet, wenn der Benutzer ein Befehls Element aus einem Menü auswählt, wenn ein Steuerelement eine Benachrichtigungs Meldung an das übergeordnete Fenster sendet oder wenn eine Tastenkombination für die Zugriffstaste übersetzt wird.


```C++
#define WM_COMMAND                      0x0111
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Eine Beschreibung dieses Parameters finden Sie unter "Hinweise".

</dd> <dt>

*lParam* 
</dt> <dd>

Eine Beschreibung dieses Parameters finden Sie unter "Hinweise".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.

## <a name="example"></a>Beispiel

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
Beispiel für [klassische Windows-Beispiele](https://github.com/microsoft/Windows-classic-samples) auf GitHub.


## <a name="remarks"></a>Bemerkungen

Die Verwendung der Parameter *wParam* und *LPARAM* wird hier zusammengefasst.



| Nachrichtenquelle | wParam (hohes Wort)                | wParam (niedriges Wort)                | lParam                       |
|----------------|-----------------------------------|----------------------------------|------------------------------|
| Menü           | 0                                 | Menü Bezeichner (IDM \_ \* )        | 0                            |
| Accelerator    | 1                                 | Zugriffstasten-ID (IDM \_ \* ) | 0                            |
| Control        | Steuerelement definierter Benachrichtigungs Code | Steuerelement Bezeichner               | Handle für das Steuerelement Fenster |



 

### <a name="menus"></a>Menüs

Wenn eine Anwendung ein Menü Trennzeichen aktiviert, sendet das System eine **WM- \_ Befehls** Nachricht, bei der das niedrige Wort des *wParam* -Parameters auf NULL festgelegt ist, wenn der Benutzer das Trennzeichen auswählt.

Wenn ein Menü mit einem [**menuinfo. dwstyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) -Wert von **MNS \_ notifybypos** definiert ist, wird [**WM \_ MenuCommand**](wm-menucommand.md) anstelle des **WM- \_ Befehls** gesendet.

### <a name="accelerators"></a>Zugriffstasten

Tastenkombinationen, die Elemente aus dem Menü Fenster auswählen, werden in die [**WM- \_ syscommand**](wm-syscommand.md) -Meldungen übersetzt.

Wenn eine Zugriffstasten-Tastatureingabe auftritt, die einem Menü Element entspricht, wenn das Fenster, das das Menü besitzt, minimiert ist, wird keine **WM- \_ Befehls** Nachricht gesendet. Wenn jedoch eine Tastenkombination angezeigt wird, die nicht mit den Elementen im Menü des Fensters oder im Menü Fenster identisch ist, wird eine WM- **\_ Befehls** Nachricht gesendet, auch wenn das Fenster minimiert wird.

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

**Licher**
</dt> <dt>

[Menüs](menus.md)
</dt> </dl>

 

