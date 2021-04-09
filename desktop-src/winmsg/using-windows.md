---
description: In den Beispielen in diesem Abschnitt wird beschrieben, wie mit Windows verbundene Aufgaben ausgeführt werden.
ms.assetid: 7695fb64-3918-4d9a-8cd8-01d20edd9c55
title: Verwenden von Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54bebe537f82de65efddc086ee457e1abe47a617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867988"
---
# <a name="using-windows"></a><span data-ttu-id="aafc2-103">Verwenden von Windows</span><span class="sxs-lookup"><span data-stu-id="aafc2-103">Using Windows</span></span>

<span data-ttu-id="aafc2-104">In den Beispielen in diesem Abschnitt wird beschrieben, wie die folgenden Aufgaben ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="aafc2-104">The examples in this section describe how to perform the following tasks:</span></span>

-   [<span data-ttu-id="aafc2-105">Erstellen eines Hauptfensters</span><span class="sxs-lookup"><span data-stu-id="aafc2-105">Creating a Main Window</span></span>](#creating-a-main-window)
-   [<span data-ttu-id="aafc2-106">Erstellen, auflisten und Größenanpassung von untergeordneten Fenstern</span><span class="sxs-lookup"><span data-stu-id="aafc2-106">Creating, Enumerating, and Sizing Child Windows</span></span>](#creating-enumerating-and-sizing-child-windows)
-   [<span data-ttu-id="aafc2-107">Zerstören eines Fensters</span><span class="sxs-lookup"><span data-stu-id="aafc2-107">Destroying a Window</span></span>](#destroying-a-window)
-   [<span data-ttu-id="aafc2-108">Verwenden von geschichteten Fenstern</span><span class="sxs-lookup"><span data-stu-id="aafc2-108">Using Layered Windows</span></span>](#using-layered-windows)

## <a name="creating-a-main-window"></a><span data-ttu-id="aafc2-109">Erstellen eines Hauptfensters</span><span class="sxs-lookup"><span data-stu-id="aafc2-109">Creating a Main Window</span></span>

<span data-ttu-id="aafc2-110">Das erste Fenster, das eine Anwendung erstellt, ist in der Regel das Hauptfenster.</span><span class="sxs-lookup"><span data-stu-id="aafc2-110">The first window an application creates is typically the main window.</span></span> <span data-ttu-id="aafc2-111">Sie erstellen das Hauptfenster mithilfe der Funktion "up- [**windowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " und geben die Fenster Klasse, den Fensternamen, die Fenster Stile, die Größe, die Position, das Menü handle, das Instanzhandle und die Erstellungs Daten an.</span><span class="sxs-lookup"><span data-stu-id="aafc2-111">You create the main window by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function, specifying the window class, window name, window styles, size, position, menu handle, instance handle, and creation data.</span></span> <span data-ttu-id="aafc2-112">Ein Hauptfenster gehört zu einer von der Anwendung definierten Fenster Klasse, sodass Sie die Fenster Klasse registrieren und eine Fenster Prozedur für die Klasse bereitstellen müssen, bevor Sie das Hauptfenster erstellen.</span><span class="sxs-lookup"><span data-stu-id="aafc2-112">A main window belongs to an application-defined window class, so you must register the window class and provide a window procedure for the class before creating the main window.</span></span>

<span data-ttu-id="aafc2-113">Die meisten Anwendungen verwenden normalerweise den [**WS \_ overlappedwindow**](window-styles.md) -Stil, um das Hauptfenster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="aafc2-113">Most applications typically use the [**WS\_OVERLAPPEDWINDOW**](window-styles.md) style to create the main window.</span></span> <span data-ttu-id="aafc2-114">Dieser Stil gibt dem Fenster eine Titelleiste, ein Fenstermenü, einen Größen Anpassungsrahmen und Schaltflächen zum minimieren und maximieren.</span><span class="sxs-lookup"><span data-stu-id="aafc2-114">This style gives the window a title bar, a window menu, a sizing border, and minimize and maximize buttons.</span></span> <span data-ttu-id="aafc2-115">Die Funktion " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " gibt ein Handle zurück, das das Fenster eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="aafc2-115">The [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function returns a handle that uniquely identifies the window.</span></span>

<span data-ttu-id="aafc2-116">Im folgenden Beispiel wird ein Hauptfenster erstellt, das zu einer Anwendungs definierten Fenster Klasse gehört.</span><span class="sxs-lookup"><span data-stu-id="aafc2-116">The following example creates a main window belonging to an application-defined window class.</span></span> <span data-ttu-id="aafc2-117">Der Fenster Name, das **Hauptfenster**, wird in der Titelleiste des Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aafc2-117">The window name, **Main Window**, will appear in the window's title bar.</span></span> <span data-ttu-id="aafc2-118">Durch die Kombination der [**WS- \_ VScroll**](window-styles.md) -und **WS \_ HScroll** -Stile mit dem **WS \_ overlappedwindow** -Stil erstellt die Anwendung ein Hauptfenster mit horizontalen und vertikalen Schiebe leisten zusätzlich zu den Komponenten, die vom **WS \_ overlappedwindow** -Stil bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="aafc2-118">By combining the [**WS\_VSCROLL**](window-styles.md) and **WS\_HSCROLL** styles with the **WS\_OVERLAPPEDWINDOW** style, the application creates a main window with horizontal and vertical scroll bars in addition to the components provided by the **WS\_OVERLAPPEDWINDOW** style.</span></span> <span data-ttu-id="aafc2-119">Die vier Vorkommen der **CW \_ usedefault** -Konstante legen die anfängliche Größe und Position des Fensters auf die vom System definierten Standardwerte fest.</span><span class="sxs-lookup"><span data-stu-id="aafc2-119">The four occurrences of the **CW\_USEDEFAULT** constant set the initial size and position of the window to the system-defined default values.</span></span> <span data-ttu-id="aafc2-120">Wenn Sie anstelle eines Menü Handles **null** angeben, wird im Fenster das Menü für die Fenster Klasse definiert.</span><span class="sxs-lookup"><span data-stu-id="aafc2-120">By specifying **NULL** instead of a menu handle, the window will have the menu defined for the window class.</span></span>


```
HINSTANCE hinst; 
HWND hwndMain; 
 
// Create the main window. 
 
hwndMain = CreateWindowEx( 
    0,                      // no extended styles           
    "MainWClass",           // class name                   
    "Main Window",          // window name                  
    WS_OVERLAPPEDWINDOW |   // overlapped window            
             WS_HSCROLL |   // horizontal scroll bar        
             WS_VSCROLL,    // vertical scroll bar          
    CW_USEDEFAULT,          // default horizontal position  
    CW_USEDEFAULT,          // default vertical position    
    CW_USEDEFAULT,          // default width                
    CW_USEDEFAULT,          // default height               
    (HWND) NULL,            // no parent or owner window    
    (HMENU) NULL,           // class menu used              
    hinst,                  // instance handle              
    NULL);                  // no window creation data      
 
if (!hwndMain) 
    return FALSE; 
 
// Show the window using the flag specified by the program 
// that started the application, and send the application 
// a WM_PAINT message. 
 
ShowWindow(hwndMain, SW_SHOWDEFAULT); 
UpdateWindow(hwndMain); 
```



<span data-ttu-id="aafc2-121">Beachten Sie, dass im vorherigen Beispiel die [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) -Funktion aufgerufen wird, nachdem das Hauptfenster erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="aafc2-121">Notice that the preceding example calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function after creating the main window.</span></span> <span data-ttu-id="aafc2-122">Dies geschieht, da das System nach dem Erstellen nicht automatisch das Hauptfenster anzeigt.</span><span class="sxs-lookup"><span data-stu-id="aafc2-122">This is done because the system does not automatically display the main window after creating it.</span></span> <span data-ttu-id="aafc2-123">Durch die Übergabe des " **SW \_ showdefault** "-Flags an **ShowWindow** ermöglicht die Anwendung dem Programm, das die Anwendung gestartet hat, den anfänglichen Anzeige Zustand des Hauptfensters festzulegen.</span><span class="sxs-lookup"><span data-stu-id="aafc2-123">By passing the **SW\_SHOWDEFAULT** flag to **ShowWindow**, the application allows the program that started the application to set the initial show state of the main window.</span></span> <span data-ttu-id="aafc2-124">Die [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) -Funktion sendet das Fenster als erste WM-Zeichnungs Nachricht. [**\_**](../gdi/wm-paint.md)</span><span class="sxs-lookup"><span data-stu-id="aafc2-124">The [**UpdateWindow**](/windows/win32/api/winuser/nf-winuser-updatewindow) function sends the window its first [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span>

## <a name="creating-enumerating-and-sizing-child-windows"></a><span data-ttu-id="aafc2-125">Erstellen, auflisten und Größenanpassung von untergeordneten Fenstern</span><span class="sxs-lookup"><span data-stu-id="aafc2-125">Creating, Enumerating, and Sizing Child Windows</span></span>

<span data-ttu-id="aafc2-126">Mithilfe von untergeordneten Fenstern können Sie den Client Bereich eines Fensters in andere Funktionsbereiche aufteilen.</span><span class="sxs-lookup"><span data-stu-id="aafc2-126">You can divide a window's client area into different functional areas by using child windows.</span></span> <span data-ttu-id="aafc2-127">Das Erstellen eines untergeordneten Fensters ähnelt dem Erstellen eines Hauptfensters – Sie verwenden die Funktion "up- [**windowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ".</span><span class="sxs-lookup"><span data-stu-id="aafc2-127">Creating a child window is like creating a main window—you use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="aafc2-128">Wenn Sie ein Fenster einer Anwendungs definierten Fenster Klasse erstellen möchten, müssen Sie die Fenster Klasse registrieren und eine Fenster Prozedur bereitstellen, bevor Sie das untergeordnete Fenster erstellen.</span><span class="sxs-lookup"><span data-stu-id="aafc2-128">To create a window of an application-defined window class, you must register the window class and provide a window procedure before creating the child window.</span></span> <span data-ttu-id="aafc2-129">Sie müssen dem untergeordneten Fenster den untergeordneten [**WS \_**](window-styles.md) -Stil geben und ein übergeordnetes Fenster für das untergeordnete Fenster angeben, wenn Sie es erstellen.</span><span class="sxs-lookup"><span data-stu-id="aafc2-129">You must give the child window the [**WS\_CHILD**](window-styles.md) style and specify a parent window for the child window when you create it.</span></span>

<span data-ttu-id="aafc2-130">Im folgenden Beispiel wird der Client Bereich des Hauptfensters einer Anwendung in drei Funktionsbereiche aufgeteilt, indem drei untergeordnete Fenster der gleichen Größe erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="aafc2-130">The following example divides the client area of an application's main window into three functional areas by creating three child windows of equal size.</span></span> <span data-ttu-id="aafc2-131">Jedes untergeordnete Fenster hat dieselbe Höhe wie der Client Bereich des Hauptfensters, jede Breite ist jedoch ein Drittel.</span><span class="sxs-lookup"><span data-stu-id="aafc2-131">Each child window is the same height as the main window's client area, but each is one-third its width.</span></span> <span data-ttu-id="aafc2-132">Im Hauptfenster werden die untergeordneten Fenster als Antwort auf die [**WM \_ Create**](wm-create.md) -Nachricht erstellt, die das Hauptfenster während des eigenen Fenster Erstellungs Prozesses empfängt.</span><span class="sxs-lookup"><span data-stu-id="aafc2-132">The main window creates the child windows in response to the [**WM\_CREATE**](wm-create.md) message, which the main window receives during its own window-creation process.</span></span> <span data-ttu-id="aafc2-133">Da jedes untergeordnete Fenster die [**WS \_**](window-styles.md) -Rahmenart hat, weist jedes untergeordnete Fenster einen schmalen Linien Rahmen auf.</span><span class="sxs-lookup"><span data-stu-id="aafc2-133">Because each child window has the [**WS\_BORDER**](window-styles.md) style, each has a thin line border.</span></span> <span data-ttu-id="aafc2-134">Da der nicht **\_ sichtbare WS** -Stil nicht angegeben ist, wird jedes untergeordnete Fenster anfänglich ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="aafc2-134">Also, because the **WS\_VISIBLE** style is not specified, each child window is initially hidden.</span></span> <span data-ttu-id="aafc2-135">Beachten Sie auch, dass jedes untergeordnete Fenster einem untergeordneten Fenster Bezeichner zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="aafc2-135">Notice also that each child window is assigned a child-window identifier.</span></span>

<span data-ttu-id="aafc2-136">Im Hauptfenster werden die untergeordneten Fenster als Antwort auf die [**WM- \_ Größen**](wm-size.md) Nachricht angezeigt, die das Hauptfenster empfängt, wenn sich die Größe ändert.</span><span class="sxs-lookup"><span data-stu-id="aafc2-136">The main window sizes and positions the child windows in response to the [**WM\_SIZE**](wm-size.md) message, which the main window receives when its size changes.</span></span> <span data-ttu-id="aafc2-137">Als Antwort auf die **WM- \_ Größe** Ruft das Hauptfenster die Dimensionen seines Client Bereichs mithilfe der [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) -Funktion ab und übergibt dann die Dimensionen an die [**enumchildwindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="aafc2-137">In response to **WM\_SIZE**, the main window retrieves the dimensions of its client area by using the [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) function and then passes the dimensions to the [**EnumChildWindows**](/windows/win32/api/winuser/nf-winuser-enumchildwindows) function.</span></span> <span data-ttu-id="aafc2-138">**Enumchildwindows** übergibt das Handle wiederum an jedes untergeordnete Fenster an die Anwendungs definierte [**enumchildproc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) -Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="aafc2-138">**EnumChildWindows** passes the handle to each child window, in turn, to the application-defined [**EnumChildProc**](/previous-versions/windows/desktop/legacy/ms633493(v=vs.85)) callback function.</span></span> <span data-ttu-id="aafc2-139">Mit dieser Funktion wird jedes untergeordnete Fenster durch Aufrufen der Funktion " [**vwindow**](/windows/win32/api/winuser/nf-winuser-movewindow) " Größe und Position positioniert. Größe und Position basieren auf den Abmessungen des Client Bereichs des Hauptfensters und dem Bezeichner des untergeordneten Fensters.</span><span class="sxs-lookup"><span data-stu-id="aafc2-139">This function sizes and positions each child window by calling the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function; the size and position are based on the dimensions of the main window's client area and the identifier of the child window.</span></span> <span data-ttu-id="aafc2-140">Danach ruft **enumchildproc** die [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) -Funktion auf, um das Fenster sichtbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="aafc2-140">Afterward, **EnumChildProc** calls the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function to make the window visible.</span></span>


```
#define ID_FIRSTCHILD  100 
#define ID_SECONDCHILD 101 
#define ID_THIRDCHILD  102 
 
LONG APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rcClient; 
    int i; 
 
    switch(uMsg) 
    { 
        case WM_CREATE: // creating main window  
 
            // Create three invisible child windows. 

            for (i = 0; i < 3; i++) 
            { 
                CreateWindowEx(0, 
                               "ChildWClass", 
                               (LPCTSTR) NULL, 
                               WS_CHILD | WS_BORDER, 
                               0,0,0,0, 
                               hwnd, 
                               (HMENU) (int) (ID_FIRSTCHILD + i), 
                               hinst, 
                               NULL); 
            }
 
            return 0; 
 
        case WM_SIZE:   // main window changed size 
 
            // Get the dimensions of the main window's client 
            // area, and enumerate the child windows. Pass the 
            // dimensions to the child windows during enumeration. 
 
            GetClientRect(hwnd, &rcClient); 
            EnumChildWindows(hwnd, EnumChildProc, (LPARAM) &rcClient); 
            return 0; 

        // Process other messages. 
    } 
    return DefWindowProc(hwnd, uMsg, wParam, lParam); 
} 
 
BOOL CALLBACK EnumChildProc(HWND hwndChild, LPARAM lParam) 
{ 
    LPRECT rcParent; 
    int i, idChild; 
 
    // Retrieve the child-window identifier. Use it to set the 
    // position of the child window. 
 
    idChild = GetWindowLong(hwndChild, GWL_ID); 
 
    if (idChild == ID_FIRSTCHILD) 
        i = 0; 
    else if (idChild == ID_SECONDCHILD) 
        i = 1; 
    else 
        i = 2; 
 
    // Size and position the child window.  
 
    rcParent = (LPRECT) lParam; 
    MoveWindow(hwndChild, 
               (rcParent->right / 3) * i, 
               0, 
               rcParent->right / 3, 
               rcParent->bottom, 
               TRUE); 
 
    // Make sure the child window is visible. 
 
    ShowWindow(hwndChild, SW_SHOW); 
 
    return TRUE;
}
```



## <a name="destroying-a-window"></a><span data-ttu-id="aafc2-141">Zerstören eines Fensters</span><span class="sxs-lookup"><span data-stu-id="aafc2-141">Destroying a Window</span></span>

<span data-ttu-id="aafc2-142">Sie können die [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) -Funktion verwenden, um ein Fenster zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="aafc2-142">You can use the [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function to destroy a window.</span></span> <span data-ttu-id="aafc2-143">Normalerweise sendet eine Anwendung die " [**WM \_ Close**](wm-close.md) "-Nachricht, bevor ein Fenster zerstört wird, sodass dem Fenster die Möglichkeit gegeben wird, den Benutzer zur Bestätigung aufzufordern, bevor das Fenster zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="aafc2-143">Typically, an application sends the [**WM\_CLOSE**](wm-close.md) message before destroying a window, giving the window the opportunity to prompt the user for confirmation before the window is destroyed.</span></span> <span data-ttu-id="aafc2-144">Ein Fenster, in dem ein Fenstermenü enthalten ist, erhält automatisch die Meldung zum **\_ Schließen der WM** , wenn der Benutzer im Menü Fenster auf **Schließen** klickt.</span><span class="sxs-lookup"><span data-stu-id="aafc2-144">A window that includes a window menu automatically receives the **WM\_CLOSE** message when the user clicks **Close** from the window menu.</span></span> <span data-ttu-id="aafc2-145">Wenn der Benutzer bestätigt, dass das Fenster zerstört werden soll, ruft die Anwendung **DestroyWindow** auf.</span><span class="sxs-lookup"><span data-stu-id="aafc2-145">If the user confirms that the window should be destroyed, the application calls **DestroyWindow**.</span></span> <span data-ttu-id="aafc2-146">Das System sendet die [**WM- \_ zerstörungsmeldung**](wm-destroy.md) an das Fenster, nachdem es vom Bildschirm entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="aafc2-146">The system sends the [**WM\_DESTROY**](wm-destroy.md) message to the window after removing it from the screen.</span></span> <span data-ttu-id="aafc2-147">Als Antwort auf **WM \_ Destroy** speichert das Fenster seine Daten und gibt alle zugeordneten Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="aafc2-147">In response to **WM\_DESTROY**, the window saves its data and frees any resources it allocated.</span></span> <span data-ttu-id="aafc2-148">Ein Hauptfenster beendet die Verarbeitung von **WM- \_ Zerstörung** durch Aufrufen der [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) -Funktion, um die Anwendung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="aafc2-148">A main window concludes its processing of **WM\_DESTROY** by calling the [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) function to quit the application.</span></span>

<span data-ttu-id="aafc2-149">Im folgenden Beispiel wird gezeigt, wie Sie vor dem Zerstören eines Fensters zur Bestätigung des Benutzers aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="aafc2-149">The following example shows how to prompt for user confirmation before destroying a window.</span></span> <span data-ttu-id="aafc2-150">Als Antwort auf [**" \_ WM close**](wm-close.md)" zeigt das Beispiel ein Dialogfeld an, das die Schaltflächen **Ja**, **Nein** und **Abbrechen** enthält.</span><span class="sxs-lookup"><span data-stu-id="aafc2-150">In response to [**WM\_CLOSE**](wm-close.md), the example displays a dialog box that contains **Yes**, **No**, and **Cancel** buttons.</span></span> <span data-ttu-id="aafc2-151">Wenn der Benutzer auf **Ja** klickt, wird [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) aufgerufen. Andernfalls wird das Fenster nicht zerstört.</span><span class="sxs-lookup"><span data-stu-id="aafc2-151">If the user clicks **Yes**, [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) is called; otherwise, the window is not destroyed.</span></span> <span data-ttu-id="aafc2-152">Da das Fenster, das zerstört wird, ein Hauptfenster ist, wird [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) im Beispiel als Antwort auf [**WM \_ Destroy**](wm-destroy.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="aafc2-152">Because the window being destroyed is a main window, the example calls [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) in response to [**WM\_DESTROY**](wm-destroy.md).</span></span>


```
case WM_CLOSE: 
 
    // Create the message box. If the user clicks 
    // the Yes button, destroy the main window. 
 
    if (MessageBox(hwnd, szConfirm, szAppName, MB_YESNOCANCEL) == IDYES) 
        DestroyWindow(hwndMain); 
    else 
        return 0; 
 
case WM_DESTROY: 
 
    // Post the WM_QUIT message to 
    // quit the application terminate. 
 
    PostQuitMessage(0); 
    return 0;
```



## <a name="using-layered-windows"></a><span data-ttu-id="aafc2-153">Verwenden von geschichteten Fenstern</span><span class="sxs-lookup"><span data-stu-id="aafc2-153">Using Layered Windows</span></span>

<span data-ttu-id="aafc2-154">Wenn ein Dialogfeld als durchlässiges Fenster angezeigt werden soll, erstellen Sie zuerst das Dialogfeld wie üblich.</span><span class="sxs-lookup"><span data-stu-id="aafc2-154">To have a dialog box come up as a translucent window, first create the dialog as usual.</span></span> <span data-ttu-id="aafc2-155">Legen Sie dann bei [**WM \_ InitDialog**](../dlgbox/wm-initdialog.md)das geschichtete Bit des erweiterten Stils des Fensters fest, und nennen Sie [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) mit dem gewünschten Alpha-Wert.</span><span class="sxs-lookup"><span data-stu-id="aafc2-155">Then, on [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md), set the layered bit of the window's extended style and call [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) with the desired alpha value.</span></span> <span data-ttu-id="aafc2-156">Der Code könnte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="aafc2-156">The code might look like this:</span></span>


```
// Set WS_EX_LAYERED on this window 
SetWindowLong(hwnd, 
              GWL_EXSTYLE, 
              GetWindowLong(hwnd, GWL_EXSTYLE) | WS_EX_LAYERED);

// Make this window 70% alpha
SetLayeredWindowAttributes(hwnd, 0, (255 * 70) / 100, LWA_ALPHA);
```



<span data-ttu-id="aafc2-157">Beachten Sie, dass der dritte Parameter von [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) ein Wert zwischen 0 und 255 ist, wobei 0 das Fenster vollständig transparent ist und 255 vollständig deckend ist.</span><span class="sxs-lookup"><span data-stu-id="aafc2-157">Note that the third parameter of [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) is a value that ranges from 0 to 255, with 0 making the window completely transparent and 255 making it completely opaque.</span></span> <span data-ttu-id="aafc2-158">Dieser Parameter imitiert die vielseitigere [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) der [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="aafc2-158">This parameter mimics the more versatile [**BLENDFUNCTION**](/windows/win32/api/wingdi/ns-wingdi-blendfunction) of the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function.</span></span>

<span data-ttu-id="aafc2-159">Um dieses Fenster wieder vollständig zu deinstallieren, entfernen Sie das überlappende **WS \_ Ex \_** -Bit, indem Sie [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) aufrufen und dann das Fenster zum Umzeichnen auffordern.</span><span class="sxs-lookup"><span data-stu-id="aafc2-159">To make this window completely opaque again, remove the **WS\_EX\_LAYERED** bit by calling [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) and then ask the window to repaint.</span></span> <span data-ttu-id="aafc2-160">Das Entfernen des Bits ist erwünscht, damit das System weiß, dass es Arbeitsspeicher freigeben kann, der mit der Schichtung und Umleitung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="aafc2-160">Removing the bit is desired to let the system know that it can free up some memory associated with layering and redirection.</span></span> <span data-ttu-id="aafc2-161">Der Code könnte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="aafc2-161">The code might look like this:</span></span>


```
// Remove WS_EX_LAYERED from this window styles
SetWindowLong(hwnd, 
              GWL_EXSTYLE,
              GetWindowLong(hwnd, GWL_EXSTYLE) & ~WS_EX_LAYERED);

// Ask the window and its children to repaint
RedrawWindow(hwnd, 
             NULL, 
             NULL, 
             RDW_ERASE | RDW_INVALIDATE | RDW_FRAME | RDW_ALLCHILDREN);
```



<span data-ttu-id="aafc2-162">Um untergeordnete Fenster mit Ebenen zu verwenden, muss die Anwendung Windows 8-fähig im Manifest deklarieren.</span><span class="sxs-lookup"><span data-stu-id="aafc2-162">In order to use layered child windows, the application has to declare itself Windows 8-aware in the manifest.</span></span>

 

 
