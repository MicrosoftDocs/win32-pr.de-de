---
description: In diesem Abschnitt wird erläutert, wie die folgenden Aufgaben für Fenster Prozeduren ausgeführt werden.
ms.assetid: acc68991-4689-44dc-8547-a7b6153b0f62
title: Verwenden von Window
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e0508119a2ba62c813c32e8fd0c00bd3dd1e85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867991"
---
# <a name="using-window-procedures"></a><span data-ttu-id="b73d3-103">Verwenden von Window</span><span class="sxs-lookup"><span data-stu-id="b73d3-103">Using Window Procedures</span></span>

<span data-ttu-id="b73d3-104">In diesem Abschnitt wird erläutert, wie die folgenden Aufgaben für Fenster Prozeduren ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b73d3-104">This section explains how to perform the following tasks associated with window procedures.</span></span>

-   [<span data-ttu-id="b73d3-105">Entwerfen einer Fenster Prozedur</span><span class="sxs-lookup"><span data-stu-id="b73d3-105">Designing a Window Procedure</span></span>](#designing-a-window-procedure)
-   [<span data-ttu-id="b73d3-106">Zuordnen einer Fenster Prozedur zu einer Fenster Klasse</span><span class="sxs-lookup"><span data-stu-id="b73d3-106">Associating a Window Procedure with a Window Class</span></span>](#associating-a-window-procedure-with-a-window-class)
-   [<span data-ttu-id="b73d3-107">Unterklassen eines Fensters</span><span class="sxs-lookup"><span data-stu-id="b73d3-107">Subclassing a Window</span></span>](#subclassing-a-window)

## <a name="designing-a-window-procedure"></a><span data-ttu-id="b73d3-108">Entwerfen einer Fenster Prozedur</span><span class="sxs-lookup"><span data-stu-id="b73d3-108">Designing a Window Procedure</span></span>

<span data-ttu-id="b73d3-109">Das folgende Beispiel zeigt die Struktur einer typischen Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="b73d3-109">The following example shows the structure of a typical window procedure.</span></span> <span data-ttu-id="b73d3-110">Die Fenster Prozedur verwendet das Message-Argument in einer **Switch** -Anweisung mit einzelnen Nachrichten, die von separaten **Case** -Anweisungen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="b73d3-110">The window procedure uses the message argument in a **switch** statement with individual messages handled by separate **case** statements.</span></span> <span data-ttu-id="b73d3-111">Beachten Sie, dass jeder Fall einen bestimmten Wert für jede Nachricht zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b73d3-111">Notice that each case returns a specific value for each message.</span></span> <span data-ttu-id="b73d3-112">Bei Nachrichten, die nicht verarbeitet werden, ruft die Fenster Prozedur die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="b73d3-112">For messages that it does not process, the window procedure calls the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>


```
LRESULT CALLBACK MainWndProc(
    HWND hwnd,        // handle to window
    UINT uMsg,        // message identifier
    WPARAM wParam,    // first message parameter
    LPARAM lParam)    // second message parameter
{ 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            // Initialize the window. 
            return 0; 
 
        case WM_PAINT: 
            // Paint the window's client area. 
            return 0; 
 
        case WM_SIZE: 
            // Set the size and position of the window. 
            return 0; 
 
        case WM_DESTROY: 
            // Clean up window-specific data objects. 
            return 0; 
 
        // 
        // Process other messages. 
        // 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
```



<span data-ttu-id="b73d3-113">Die [**WM- \_ nccreate**](wm-nccreate.md) -Nachricht wird gesendet, nachdem das Fenster erstellt wurde. Wenn jedoch eine Anwendung auf diese Meldung antwortet, indem Sie **false** zurückgibt, schlägt die Funktion " [**deatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " fehl.</span><span class="sxs-lookup"><span data-stu-id="b73d3-113">The [**WM\_NCCREATE**](wm-nccreate.md) message is sent just after your window is created, but if an application responds to this message by returning **FALSE**, [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function fails.</span></span> <span data-ttu-id="b73d3-114">Die [**WM \_ Create**](wm-create.md) -Nachricht wird gesendet, nachdem das Fenster bereits erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b73d3-114">The [**WM\_CREATE**](wm-create.md) message is sent after your window is already created.</span></span>

<span data-ttu-id="b73d3-115">Die [**WM- \_ zerstörungsmeldung**](wm-destroy.md) wird gesendet, wenn das Fenster zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="b73d3-115">The [**WM\_DESTROY**](wm-destroy.md) message is sent when your window is about to be destroyed.</span></span> <span data-ttu-id="b73d3-116">Mit der [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) -Funktion werden alle untergeordneten Fenster des Fensters zerstört, das zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="b73d3-116">The [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function takes care of destroying any child windows of the window being destroyed.</span></span> <span data-ttu-id="b73d3-117">Die [**WM \_ ncdestroy**](wm-ncdestroy.md) -Nachricht wird gesendet, kurz bevor ein Fenster zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="b73d3-117">The [**WM\_NCDESTROY**](wm-ncdestroy.md) message is sent just before a window is destroyed.</span></span>

<span data-ttu-id="b73d3-118">Eine Fenster Prozedur sollte mindestens die WM-Zeichnungs Nachricht verarbeiten [**, \_**](../gdi/wm-paint.md) um sich selbst zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="b73d3-118">At the very least, a window procedure should process the [**WM\_PAINT**](../gdi/wm-paint.md) message to draw itself.</span></span> <span data-ttu-id="b73d3-119">In der Regel sollten auch Maus-und Tastatur Meldungen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="b73d3-119">Typically, it should handle mouse and keyboard messages as well.</span></span> <span data-ttu-id="b73d3-120">Überprüfen Sie die Beschreibungen einzelner Nachrichten, um zu bestimmen, ob Sie von ihrer Fenster Prozedur behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b73d3-120">Consult the descriptions of individual messages to determine whether your window procedure should handle them.</span></span>

<span data-ttu-id="b73d3-121">Die Anwendung kann die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion als Teil der Verarbeitung einer Nachricht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b73d3-121">Your application can call the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as part of the processing of a message.</span></span> <span data-ttu-id="b73d3-122">In einem solchen Fall kann die Anwendung die Nachrichten Parameter ändern, bevor Sie die Nachricht an **defwindowproc** übergibt, oder Sie kann mit der Standard Verarbeitung fortfahren, nachdem Sie Ihre eigenen Vorgänge ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="b73d3-122">In such a case, the application can modify the message parameters before passing the message to **DefWindowProc**, or it can continue with the default processing after performing its own operations.</span></span>

<span data-ttu-id="b73d3-123">Eine Dialogfeld Prozedur empfängt eine [**WM- \_ InitDialog**](../dlgbox/wm-initdialog.md) -Nachricht anstelle einer [**WM \_ Create**](wm-create.md) -Meldung und übergibt keine nicht verarbeiteten Nachrichten an die [**defdlgproc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b73d3-123">A dialog box procedure receives a [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message instead of a [**WM\_CREATE**](wm-create.md) message and does not pass unprocessed messages to the [**DefDlgProc**](/windows/win32/api/winuser/nf-winuser-defdlgprocw) function.</span></span> <span data-ttu-id="b73d3-124">Andernfalls ist eine Dialogfeld Prozedur genauso wie eine Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="b73d3-124">Otherwise, a dialog box procedure is exactly the same as a window procedure.</span></span>

## <a name="associating-a-window-procedure-with-a-window-class"></a><span data-ttu-id="b73d3-125">Zuordnen einer Fenster Prozedur zu einer Fenster Klasse</span><span class="sxs-lookup"><span data-stu-id="b73d3-125">Associating a Window Procedure with a Window Class</span></span>

<span data-ttu-id="b73d3-126">Beim Registrieren der Klasse wird eine Fenster Prozedur mit einer Fenster Klasse verknüpft.</span><span class="sxs-lookup"><span data-stu-id="b73d3-126">You associate a window procedure with a window class when registering the class.</span></span> <span data-ttu-id="b73d3-127">Sie müssen eine [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur mit Informationen über die-Klasse ausfüllen, und das **lpfnwndproc** -Element muss die Adresse der Fenster Prozedur angeben.</span><span class="sxs-lookup"><span data-stu-id="b73d3-127">You must fill a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure with information about the class, and the **lpfnWndProc** member must specify the address of the window procedure.</span></span> <span data-ttu-id="b73d3-128">Übergeben Sie die Adresse der **WNDCLASS** -Struktur an die [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) -Funktion, um die Klasse zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="b73d3-128">To register the class, pass the address of **WNDCLASS** structure to the [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) function.</span></span> <span data-ttu-id="b73d3-129">Nachdem die Fenster Klasse registriert wurde, wird die Fenster Prozedur automatisch jedem neuen Fenster zugeordnet, das mit dieser Klasse erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b73d3-129">After the window class has been registered, the window procedure is automatically associated with each new window created with that class.</span></span>

<span data-ttu-id="b73d3-130">Im folgenden Beispiel wird gezeigt, wie Sie die Fenster Prozedur im vorherigen Beispiel einer Fenster Klasse zuordnen.</span><span class="sxs-lookup"><span data-stu-id="b73d3-130">The following example shows how to associate the window procedure in the previous example with a window class.</span></span>


```
int APIENTRY WinMain( 
    HINSTANCE hinstance,  // handle to current instance 
    HINSTANCE hinstPrev,  // handle to previous instance 
    LPSTR lpCmdLine,      // address of command-line string 
    int nCmdShow)         // show-window type 
{ 
    WNDCLASS wc; 
 
    // Register the main window class. 
    wc.style = CS_HREDRAW | CS_VREDRAW; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  "MainMenu"; 
    wc.lpszClassName = "MainWindowClass"; 
 
    if (!RegisterClass(&wc)) 
       return FALSE; 
 
    // 
    // Process other messages. 
    // 
 
} 
```



## <a name="subclassing-a-window"></a><span data-ttu-id="b73d3-131">Unterklassen eines Fensters</span><span class="sxs-lookup"><span data-stu-id="b73d3-131">Subclassing a Window</span></span>

<span data-ttu-id="b73d3-132">Um eine Unterklasse einer Instanz eines Fensters zu unterteilen, müssen Sie die Funktion [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) aufrufen und das Handle für das Fenster angeben, um das GWL \_ -WndProc-Flag zu unterteilen, und einen Zeiger auf die Unterklassen Prozedur.</span><span class="sxs-lookup"><span data-stu-id="b73d3-132">To subclass an instance of a window, call the [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) function and specify the handle to the window to subclass the GWL\_WNDPROC flag and a pointer to the subclass procedure.</span></span> <span data-ttu-id="b73d3-133">**SetWindowLong** gibt einen Zeiger auf die ursprüngliche Fenster Prozedur zurück. Verwenden Sie diesen Zeiger, um Meldungen an die ursprüngliche Prozedur zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="b73d3-133">**SetWindowLong** returns a pointer to the original window procedure; use this pointer to pass messages to the original procedure.</span></span> <span data-ttu-id="b73d3-134">Die Unterklassen Fenster-Prozedur muss die [**callwindowproc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) -Funktion verwenden, um die ursprüngliche Fenster Prozedur aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b73d3-134">The subclass window procedure must use the [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) function to call the original window procedure.</span></span>

> [!Note]  
> <span data-ttu-id="b73d3-135">Verwenden Sie die [**setwindowlongptr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) -Funktion, um Code zu schreiben, der sowohl mit der 32-Bit-als auch mit der 64-Bit-Version von Windows kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="b73d3-135">To write code that is compatible with both 32-bit and 64-bit versions of Windows, use the [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) function.</span></span>

 

<span data-ttu-id="b73d3-136">Im folgenden Beispiel wird gezeigt, wie eine Instanz eines Bearbeitungs Steuer Elements in einem Dialogfeld unterteilt wird.</span><span class="sxs-lookup"><span data-stu-id="b73d3-136">The following example shows how to subclass an instance of an edit control in a dialog box.</span></span> <span data-ttu-id="b73d3-137">Mithilfe der Prozedur des untergeordneten Klassen Fensters kann das Bearbeitungs Steuerelement alle Tastatureingaben einschließlich der Eingabe-und Tab-Taste empfangen, wenn das Steuerelement den Eingabefokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="b73d3-137">The subclass window procedure enables the edit control to receive all keyboard input, including the ENTER and TAB keys, whenever the control has the input focus.</span></span>


```
WNDPROC wpOrigEditProc; 
 
LRESULT APIENTRY EditBoxProc(
    HWND hwndDlg, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    HWND hwndEdit; 
 
    switch(uMsg) 
    { 
        case WM_INITDIALOG: 
            // Retrieve the handle to the edit control. 
            hwndEdit = GetDlgItem(hwndDlg, ID_EDIT); 
 
            // Subclass the edit control. 
            wpOrigEditProc = (WNDPROC) SetWindowLong(hwndEdit, 
                GWL_WNDPROC, (LONG) EditSubclassProc); 
            // 
            // Continue the initialization procedure. 
            // 
            return TRUE; 
 
        case WM_DESTROY: 
            // Remove the subclass from the edit control. 
            SetWindowLong(hwndEdit, GWL_WNDPROC, 
                (LONG) wpOrigEditProc); 
            // 
            // Continue the cleanup procedure. 
            // 
            break; 
    } 
    return FALSE; 
        UNREFERENCED_PARAMETER(lParam); 
} 
 
// Subclass procedure 
LRESULT APIENTRY EditSubclassProc(
    HWND hwnd, 
    UINT uMsg, 
    WPARAM wParam, 
    LPARAM lParam) 
{ 
    if (uMsg == WM_GETDLGCODE) 
        return DLGC_WANTALLKEYS; 
 
    return CallWindowProc(wpOrigEditProc, hwnd, uMsg, 
        wParam, lParam); 
} 
```



 

 
