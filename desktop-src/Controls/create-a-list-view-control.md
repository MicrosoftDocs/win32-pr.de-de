---
title: Erstellen eines List-View-Steuerelements
description: In diesem Thema wird veranschaulicht, wie Ein Listenansicht-Steuerelement erstellt wird. Um ein Listenansichtssteuerelement zu erstellen, verwenden Sie die CreateWindow- oder CreateWindowEx-Funktion und geben die WC \_ LISTVIEW-Fensterklasse an.
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71eddfb60a2ea035a5afe62423289da40a47b61841d3ba58c4cafa2824a65b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826610"
---
# <a name="how-to-create-a-list-view-control"></a>Erstellen eines List-View-Steuerelements

In diesem Thema wird veranschaulicht, wie Ein Listenansicht-Steuerelement erstellt wird. Um ein Listenansichtssteuerelement zu erstellen, verwenden Sie die [**CreateWindow-**](/windows/desktop/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) und geben die [**WC \_ LISTVIEW-Fensterklasse**](common-control-window-classes.md) an.

Ein Listenansichtssteuerelement kann auch als Teil einer Dialogfeldvorlage erstellt werden. Sie müssen [**WC \_ LISTVIEW**](common-control-window-classes.md) als Klassennamen angeben. Um ein Listenansichtssteuerelement als Teil einer Dialogfeldvorlage zu verwenden, müssen Sie [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) oder [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) aufrufen, bevor Sie eine Instanz des Dialogfelds erstellen.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Registrieren Sie zunächst die Window-Klasse, indem Sie die [**InitCommonControlsEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) aufrufen und das [**BIT VON \_ LISTVIEW \_ CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) in der zugehörigen **INITCOMMONCONTROLSEX-Struktur** angeben. Dadurch wird sichergestellt, dass die DLL für allgemeine Steuerelemente geladen wird. Verwenden Sie als Nächstes die Funktion [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) und geben Sie die [**WC \_ LISTVIEW-Fensterklasse**](common-control-window-classes.md) an.

> [!Note]  
> Standardmäßig verwendet ein Listenansichts-Steuerelement die Symboltitelschriftart. Sie können jedoch eine [**WM \_ SETFONT-Nachricht**](/windows/desktop/winmsg/wm-setfont) verwenden, um die Schriftart anzugeben, die für den Text verwendet werden soll. Sie sollten diese Nachricht senden, bevor Sie Elemente einfügen. Das Steuerelement verwendet die Abmessungen der Schriftart, die von der **WM \_ SETFONT-Meldung** angegeben wird, um Abstand und Layout zu bestimmen. Sie können auch die Schriftart für jedes Element anpassen. Weitere Informationen finden Sie unter [Custom Draw](custom-draw.md).

 

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




In der Regel ermöglichen Listenansichtsanwendungen dem Benutzer, von einer Ansicht in eine andere zu wechseln.

Im folgenden C++-Codebeispiel wird der Fensterstil der Listenansicht geändert, wodurch wiederum die Ansicht geändert wird.


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

[Referenz zum Listenansicht-Steuerelement](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informationen zu List-View-Steuerelementen](list-view-controls-overview.md)
</dt> <dt>

[Verwenden von List-View-Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

 