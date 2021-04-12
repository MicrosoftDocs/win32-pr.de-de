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
# <a name="how-to-create-a-list-view-control"></a><span data-ttu-id="26211-104">Erstellen eines List-View-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="26211-104">How to Create a List-View Control</span></span>

<span data-ttu-id="26211-105">In diesem Thema wird veranschaulicht, wie ein Listenansicht-Steuerelement erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="26211-105">This topic demonstrates how to create a list-view control.</span></span> <span data-ttu-id="26211-106">Um ein Listenansicht-Steuerelement zu erstellen, verwenden Sie die Funktion "up- [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**deatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " und geben die [**WC- \_ ListView**](common-control-window-classes.md) -Fenster Klasse an.</span><span class="sxs-lookup"><span data-stu-id="26211-106">To create a list-view control, you use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specify the [**WC\_LISTVIEW**](common-control-window-classes.md) window class.</span></span>

<span data-ttu-id="26211-107">Ein Listenansicht-Steuerelement kann auch als Teil einer Dialogfeld Vorlage erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="26211-107">A list-view control can also be created as part of a dialog box template.</span></span> <span data-ttu-id="26211-108">Sie müssen " [**WC \_ ListView**](common-control-window-classes.md) " als Klassennamen angeben.</span><span class="sxs-lookup"><span data-stu-id="26211-108">You must specify [**WC\_LISTVIEW**](common-control-window-classes.md) as the class name.</span></span> <span data-ttu-id="26211-109">Wenn Sie ein Listenansicht-Steuerelement als Teil einer Dialogfeld Vorlage verwenden möchten, müssen Sie [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) oder [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) aufzurufen, bevor Sie eine Instanz des Dialog Felds erstellen.</span><span class="sxs-lookup"><span data-stu-id="26211-109">To use a list-view control as part of a dialog box template, you must call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) or [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) before you create an instance of the dialog box.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="26211-110">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="26211-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="26211-111">Technologien</span><span class="sxs-lookup"><span data-stu-id="26211-111">Technologies</span></span>

-   [<span data-ttu-id="26211-112">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="26211-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="26211-113">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="26211-113">Prerequisites</span></span>

-   <span data-ttu-id="26211-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="26211-114">C/C++</span></span>
-   <span data-ttu-id="26211-115">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="26211-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="26211-116">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="26211-116">Instructions</span></span>


<span data-ttu-id="26211-117">Registrieren Sie zuerst die Fenster Klasse, indem Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion aufrufen und die Klassen des Verzeichnisses [**\_ ListView- \_ Klassen**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) in der zugehörigen **InitCommonControlsEx** -Struktur angeben.</span><span class="sxs-lookup"><span data-stu-id="26211-117">First register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function and specifying the [**ICC\_LISTVIEW\_CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) bit in the accompanying **INITCOMMONCONTROLSEX** structure.</span></span> <span data-ttu-id="26211-118">Dadurch wird sichergestellt, dass die DLL für allgemeine Steuerelemente geladen wird.</span><span class="sxs-lookup"><span data-stu-id="26211-118">This ensures that the common controls DLL is loaded.</span></span> <span data-ttu-id="26211-119">Verwenden Sie als nächstes die Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ", und geben Sie die [**WC- \_ ListView**](common-control-window-classes.md) -Fenster Klasse an.</span><span class="sxs-lookup"><span data-stu-id="26211-119">Next, use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specify the [**WC\_LISTVIEW**](common-control-window-classes.md) window class.</span></span>

> [!Note]  
> <span data-ttu-id="26211-120">Standardmäßig verwendet ein Listenansicht-Steuerelement die Schriftart des Symbol Titels.</span><span class="sxs-lookup"><span data-stu-id="26211-120">By default, a list-view control uses the icon title font.</span></span> <span data-ttu-id="26211-121">Sie können jedoch eine WM- [**\_ setFont**](/windows/desktop/winmsg/wm-setfont) -Nachricht verwenden, um die Schriftart anzugeben, die für den Text verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="26211-121">However, you can use a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to specify the font to be used for the text.</span></span> <span data-ttu-id="26211-122">Sie sollten diese Nachricht vor dem Einfügen von Elementen senden.</span><span class="sxs-lookup"><span data-stu-id="26211-122">You should send this message before inserting any items.</span></span> <span data-ttu-id="26211-123">Das-Steuerelement verwendet die Dimensionen der Schriftart, die von der **WM- \_ setFont** -Nachricht angegeben wird, um den Abstand und das Layout zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="26211-123">The control uses the dimensions of the font that is specified by the **WM\_SETFONT** message to determine spacing and layout.</span></span> <span data-ttu-id="26211-124">Sie können auch die Schriftart für jedes Element anpassen.</span><span class="sxs-lookup"><span data-stu-id="26211-124">You can also customize the font for each item.</span></span> <span data-ttu-id="26211-125">Weitere Informationen finden Sie unter [benutzerdefiniertes Zeichnen](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="26211-125">For more information, see [Custom Draw](custom-draw.md).</span></span>

 

<span data-ttu-id="26211-126">Im folgenden C++-Codebeispiel wird ein Listenansicht-Steuerelement in der Berichtsansicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="26211-126">The following C++ code example creates a list-view control in report view.</span></span>


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




<span data-ttu-id="26211-127">In der Regel ermöglichen Listen Ansichts Anwendungen dem Benutzer das Wechseln von einer Ansicht zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="26211-127">Typically, list-view applications enable the user to change from one view to another.</span></span>

<span data-ttu-id="26211-128">Im folgenden C++-Codebeispiel wird der Fenster Stil der Listenansicht geändert, der wiederum die Ansicht ändert.</span><span class="sxs-lookup"><span data-stu-id="26211-128">The following C++ code example changes the list-view's window style, which in turn changes the view.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="26211-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26211-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26211-130">Listenansicht-Steuerelement Verweis</span><span class="sxs-lookup"><span data-stu-id="26211-130">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="26211-131">Informationen zu List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="26211-131">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="26211-132">Verwenden von List-View Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="26211-132">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 