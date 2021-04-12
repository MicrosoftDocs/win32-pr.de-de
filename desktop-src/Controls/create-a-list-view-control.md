---
title: Erstellen eines List-View-Steuer Elements
description: In diesem Thema wird veranschaulicht, wie ein Listenansicht-Steuerelement erstellt wird. Um ein Listenansicht-Steuerelement zu erstellen, verwenden Sie die Funktion "up-Window" oder "deatewindowex" und geben die WC- \_ ListView-Fenster Klasse an.
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050498b87aaf701249a06cfe2c3ad18afdc1d84
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474673"
---
# <a name="how-to-create-a-list-view-control"></a>Erstellen eines List-View-Steuer Elements

In diesem Thema wird veranschaulicht, wie ein Listenansicht-Steuerelement erstellt wird. Um ein Listenansicht-Steuerelement zu erstellen, verwenden Sie die Funktion "up- [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**deatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " und geben die [**WC- \_ ListView**](common-control-window-classes.md) -Fenster Klasse an.

Ein Listenansicht-Steuerelement kann auch als Teil einer Dialogfeld Vorlage erstellt werden. Sie müssen " [**WC \_ ListView**](common-control-window-classes.md) " als Klassennamen angeben. Wenn Sie ein Listenansicht-Steuerelement als Teil einer Dialogfeld Vorlage verwenden möchten, müssen Sie [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) oder [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) aufzurufen, bevor Sie eine Instanz des Dialog Felds erstellen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Registrieren Sie zuerst die Fenster Klasse, indem Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion aufrufen und die Klassen des Verzeichnisses [**\_ ListView- \_ Klassen**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) in der zugehörigen **InitCommonControlsEx** -Struktur angeben. Dadurch wird sichergestellt, dass die DLL für allgemeine Steuerelemente geladen wird. Verwenden Sie als nächstes die Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ", und geben Sie die [**WC- \_ ListView**](common-control-window-classes.md) -Fenster Klasse an.

> [!Note]  
> Standardmäßig verwendet ein Listenansicht-Steuerelement die Schriftart des Symbol Titels. Sie können jedoch eine WM- [**\_ setFont**](/windows/desktop/winmsg/wm-setfont) -Nachricht verwenden, um die Schriftart anzugeben, die für den Text verwendet werden soll. Sie sollten diese Nachricht vor dem Einfügen von Elementen senden. Das-Steuerelement verwendet die Dimensionen der Schriftart, die von der **WM- \_ setFont** -Nachricht angegeben wird, um den Abstand und das Layout zu bestimmen. Sie können auch die Schriftart für jedes Element anpassen. Weitere Informationen finden Sie unter [benutzerdefiniertes Zeichnen](custom-draw.md).

 

Im folgenden C++-Codebeispiel wird ein Listenansicht-Steuerelement in der Berichtsansicht erstellt.


```C++
// CreateListView: Creates a list-view control in report view.
// Returns the handle to the new control
// TO DO:  The calling procedure should determine whether the handle is NULL, in case 
// of an error in creation.
//
// HINST hInst: The global handle to the applicadtion instance.
// HWND  hWndParent: The handle to the control's parent window. 
//
HWND CreateListView (HWND hwndParent) 
{
    INITCOMMONCONTROLSEX icex;           // Structure for control initialization.
    icex.dwICC = ICC_LISTVIEW_CLASSES;
    InitCommonControlsEx(&icex);

    RECT rcClient;                       // The parent window's client area.

    GetClientRect (hwndParent, &rcClient); 

    // Create the list-view window in report view with label editing enabled.
    HWND hWndListView = CreateWindow(WC_LISTVIEW, 
                                     L"",
                                     WS_CHILD | LVS_REPORT | LVS_EDITLABELS,
                                     0, 0,
                                     rcClient.right - rcClient.left,
                                     rcClient.bottom - rcClient.top,
                                     hwndParent,
                                     (HMENU)IDM_CODE_SAMPLES,
                                     g_hInst,
                                     NULL); 

    return (hWndListView);
}

```




In der Regel ermöglichen Listen Ansichts Anwendungen dem Benutzer das Wechseln von einer Ansicht zu einem anderen.

Im folgenden C++-Codebeispiel wird der Fenster Stil der Listenansicht geändert, der wiederum die Ansicht ändert.


```C++
// SetView: Sets a list-view's window style to change the view.
// hWndListView: A handle to the list-view control. 
// dwView:       A value specifying the new view style.
//
VOID SetView(HWND hWndListView, DWORD dwView) 
{ 
    // Retrieve the current window style. 
    DWORD dwStyle = GetWindowLong(hWndListView, GWL_STYLE); 
    
    // Set the window style only if the view bits changed.
    if ((dwStyle & LVS_TYPEMASK) != dwView) 
    {
        SetWindowLong(hWndListView,
                      GWL_STYLE,
                      (dwStyle & ~LVS_TYPEMASK) | dwView);
    }               // Logical OR'ing of dwView with the result of 
}                   // a bitwise AND between dwStyle and 
                    // the Unary complenent of LVS_TYPEMASK.

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Listenansicht-Steuerelement Verweis](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informationen zu List-View Steuerelementen](list-view-controls-overview.md)
</dt> <dt>

[Verwenden von List-View Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

 