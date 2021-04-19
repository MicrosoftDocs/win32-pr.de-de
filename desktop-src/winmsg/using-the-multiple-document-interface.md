---
description: In diesem Abschnitt wird erläutert, wie mit der Multiple Document-Schnittstelle verknüpfte Aufgaben ausgeführt werden.
ms.assetid: 024744d3-362f-4162-8d0a-d4dac61de808
title: Verwenden der Multiple Document-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e24aed7abc3640b441345520203c8a02e025e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362936"
---
# <a name="using-the-multiple-document-interface"></a><span data-ttu-id="40f40-103">Verwenden der Multiple Document-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="40f40-103">Using the Multiple Document Interface</span></span>

<span data-ttu-id="40f40-104">In diesem Abschnitt wird erläutert, wie die folgenden Aufgaben ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="40f40-104">This section explains how to perform the following tasks:</span></span>

-   [<span data-ttu-id="40f40-105">Registrieren von untergeordneten und Rahmen Fenster Klassen</span><span class="sxs-lookup"><span data-stu-id="40f40-105">Registering Child and Frame Window Classes</span></span>](#registering-child-and-frame-window-classes)
-   [<span data-ttu-id="40f40-106">Erstellen von Frame-und untergeordneten Fenstern</span><span class="sxs-lookup"><span data-stu-id="40f40-106">Creating Frame and Child Windows</span></span>](#creating-frame-and-child-windows)
-   [<span data-ttu-id="40f40-107">Schreiben der Hauptnachrichten Schleife</span><span class="sxs-lookup"><span data-stu-id="40f40-107">Writing the Main Message Loop</span></span>](#writing-the-main-message-loop)
-   [<span data-ttu-id="40f40-108">Schreiben der Rahmen Fenster Prozedur</span><span class="sxs-lookup"><span data-stu-id="40f40-108">Writing the Frame Window Procedure</span></span>](#writing-the-frame-window-procedure)
-   [<span data-ttu-id="40f40-109">Schreiben der Prozedur für das untergeordnete Fenster</span><span class="sxs-lookup"><span data-stu-id="40f40-109">Writing the Child Window Procedure</span></span>](#writing-the-child-window-procedure)
-   [<span data-ttu-id="40f40-110">Erstellen eines untergeordneten Fensters</span><span class="sxs-lookup"><span data-stu-id="40f40-110">Creating a Child Window</span></span>](#creating-a-child-window)

<span data-ttu-id="40f40-111">Um diese Aufgaben zu veranschaulichen, enthält dieser Abschnitt Beispiele aus MULTIPAD, einer typischen MDI-Anwendung (Multiple Document Interface).</span><span class="sxs-lookup"><span data-stu-id="40f40-111">To illustrate these tasks, this section includes examples from Multipad, a typical multiple-document interface (MDI) application.</span></span>

## <a name="registering-child-and-frame-window-classes"></a><span data-ttu-id="40f40-112">Registrieren von untergeordneten und Rahmen Fenster Klassen</span><span class="sxs-lookup"><span data-stu-id="40f40-112">Registering Child and Frame Window Classes</span></span>

<span data-ttu-id="40f40-113">Eine typische MDI-Anwendung muss zwei Fenster Klassen registrieren: eine für das Rahmen Fenster und eine für die untergeordneten Fenster.</span><span class="sxs-lookup"><span data-stu-id="40f40-113">A typical MDI application must register two window classes: one for its frame window and one for its child windows.</span></span> <span data-ttu-id="40f40-114">Wenn eine Anwendung mehr als einen Dokumenttyp unterstützt (z. b. eine Kalkulations Tabelle und ein Diagramm), muss für jeden Typ eine Fenster Klasse registriert werden.</span><span class="sxs-lookup"><span data-stu-id="40f40-114">If an application supports more than one type of document (for example, a spreadsheet and a chart), it must register a window class for each type.</span></span>

<span data-ttu-id="40f40-115">Die Klassenstruktur für das Rahmen Fenster ähnelt der-Klassenstruktur für das Hauptfenster von nicht-–-MDI-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="40f40-115">The class structure for the frame window is similar to the class structure for the main window in non–MDI applications.</span></span> <span data-ttu-id="40f40-116">Die Klassenstruktur für die untergeordneten MDI-Fenster unterscheidet sich geringfügig von der Struktur für untergeordnete Fenster in nicht –-MDI-Anwendungen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="40f40-116">The class structure for the MDI child windows differs slightly from the structure for child windows in non–MDI applications as follows:</span></span>

-   <span data-ttu-id="40f40-117">Die Klassenstruktur sollte ein Symbol aufweisen, da der Benutzer ein untergeordnetes MDI-Fenster minimieren kann, als ob es sich um ein normales Anwendungsfenster handelt.</span><span class="sxs-lookup"><span data-stu-id="40f40-117">The class structure should have an icon, because the user can minimize an MDI child window as if it were a normal application window.</span></span>
-   <span data-ttu-id="40f40-118">Der Menüname sollte **null** sein, da ein untergeordnetes MDI-Fenster nicht über ein eigenes Menü verfügen kann.</span><span class="sxs-lookup"><span data-stu-id="40f40-118">The menu name should be **NULL**, because an MDI child window cannot have its own menu.</span></span>
-   <span data-ttu-id="40f40-119">Die Klassenstruktur sollte zusätzlichen Platz in der Fenster Struktur reservieren.</span><span class="sxs-lookup"><span data-stu-id="40f40-119">The class structure should reserve extra space in the window structure.</span></span> <span data-ttu-id="40f40-120">Bei diesem Bereich kann die Anwendung Daten, z. b. einen Dateinamen, einem bestimmten untergeordneten Fenster zuordnen.</span><span class="sxs-lookup"><span data-stu-id="40f40-120">With this space, the application can associate data, such as a filename, with a particular child window.</span></span>

<span data-ttu-id="40f40-121">Das folgende Beispiel zeigt, wie das MULTIPAD seine Frame-und untergeordneten Fenster Klassen registriert.</span><span class="sxs-lookup"><span data-stu-id="40f40-121">The following example shows how Multipad registers its frame and child window classes.</span></span>


```
BOOL WINAPI InitializeApplication() 
{ 
    WNDCLASS wc; 
 
    // Register the frame window class. 
 
    wc.style         = 0; 
    wc.lpfnWndProc   = (WNDPROC) MPFrameWndProc; 
    wc.cbClsExtra    = 0; 
    wc.cbWndExtra    = 0; 
    wc.hInstance     = hInst; 
    wc.hIcon         = LoadIcon(hInst, IDMULTIPAD); 
    wc.hCursor       = LoadCursor((HANDLE) NULL, IDC_ARROW); 
    wc.hbrBackground = (HBRUSH) (COLOR_APPWORKSPACE + 1); 
    wc.lpszMenuName  = IDMULTIPAD; 
    wc.lpszClassName = szFrame; 
 
    if (!RegisterClass (&wc) ) 
        return FALSE; 
 
    // Register the MDI child window class. 
 
    wc.lpfnWndProc   = (WNDPROC) MPMDIChildWndProc; 
    wc.hIcon         = LoadIcon(hInst, IDNOTE); 
    wc.lpszMenuName  = (LPCTSTR) NULL; 
    wc.cbWndExtra    = CBWNDEXTRA; 
    wc.lpszClassName = szChild; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    return TRUE; 
} 
```



## <a name="creating-frame-and-child-windows"></a><span data-ttu-id="40f40-122">Erstellen von Frame-und untergeordneten Fenstern</span><span class="sxs-lookup"><span data-stu-id="40f40-122">Creating Frame and Child Windows</span></span>

<span data-ttu-id="40f40-123">Nachdem die Fenster Klassen registriert wurden, kann eine MDI-Anwendung Ihre Fenster erstellen.</span><span class="sxs-lookup"><span data-stu-id="40f40-123">After registering its window classes, an MDI application can create its windows.</span></span> <span data-ttu-id="40f40-124">Zuerst wird das Rahmen Fenster mithilfe der Funktion "up [**Window**](/windows/win32/api/winuser/nf-winuser-createwindowa) " oder der Funktion " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " erstellt.</span><span class="sxs-lookup"><span data-stu-id="40f40-124">First, it creates its frame window by using the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="40f40-125">Nachdem das Rahmen Fenster erstellt wurde, erstellt die Anwendung das Client Fenster, und zwar mithilfe von " **kreatewindow** " oder " **kreatewindowex**".</span><span class="sxs-lookup"><span data-stu-id="40f40-125">After creating its frame window, the application creates its client window, again by using **CreateWindow** or **CreateWindowEx**.</span></span> <span data-ttu-id="40f40-126">Die Anwendung sollte MdiClient als Klassennamen für den Client Fenster angeben. **MdiClient** ist eine vorab übergeordnete Fenster Klasse, die vom System definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="40f40-126">The application should specify MDICLIENT as the client window's class name; **MDICLIENT** is a preregistered window class defined by the system.</span></span> <span data-ttu-id="40f40-127">Der *lpvparam* -Parameter von " **foratewindow** " oder " **foratewindowex** " sollte auf eine [**clientkreatestruct**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="40f40-127">The *lpvParam* parameter of **CreateWindow** or **CreateWindowEx** should point to a [**CLIENTCREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-clientcreatestruct) structure.</span></span> <span data-ttu-id="40f40-128">Diese Struktur enthält die in der folgenden Tabelle beschriebenen Elemente:</span><span class="sxs-lookup"><span data-stu-id="40f40-128">This structure contains the members described in the following table:</span></span>



| <span data-ttu-id="40f40-129">Member</span><span class="sxs-lookup"><span data-stu-id="40f40-129">Member</span></span>           | <span data-ttu-id="40f40-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40f40-130">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40f40-131">**hwindowmenu**</span><span class="sxs-lookup"><span data-stu-id="40f40-131">**hWindowMenu**</span></span>  | <span data-ttu-id="40f40-132">Handle für das Fenstermenü, das zum Steuern untergeordneter MDI-Fenster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="40f40-132">Handle to the window menu used for controlling MDI child windows.</span></span> <span data-ttu-id="40f40-133">Wenn untergeordnete Fenster erstellt werden, fügt die Anwendung ihre Titel im Menü Fenster als Menü Elemente hinzu.</span><span class="sxs-lookup"><span data-stu-id="40f40-133">As child windows are created, the application adds their titles to the window menu as menu items.</span></span> <span data-ttu-id="40f40-134">Der Benutzer kann dann ein untergeordnetes Fenster aktivieren, indem er im Menü Fenster auf seinen Titel klickt.</span><span class="sxs-lookup"><span data-stu-id="40f40-134">The user can then activate a child window by clicking its title on the window menu.</span></span>                                                               |
| <span data-ttu-id="40f40-135">**idfirstchild**</span><span class="sxs-lookup"><span data-stu-id="40f40-135">**idFirstChild**</span></span> | <span data-ttu-id="40f40-136">Gibt den Bezeichner des ersten untergeordneten MDI-Fensters an.</span><span class="sxs-lookup"><span data-stu-id="40f40-136">Specifies the identifier of the first MDI child window.</span></span> <span data-ttu-id="40f40-137">Das erste erstellte untergeordnete MDI-Fenster wird diesem Bezeichner zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="40f40-137">The first MDI child window created is assigned this identifier.</span></span> <span data-ttu-id="40f40-138">Mit inkrementierten Fenster Bezeichner werden weitere Fenster erstellt.</span><span class="sxs-lookup"><span data-stu-id="40f40-138">Additional windows are created with incremented window identifiers.</span></span> <span data-ttu-id="40f40-139">Wenn ein untergeordnetes Fenster zerstört wird, werden die Fenster Bezeichner sofort von dem System neu zugewiesen, um den Bereich zusammenhängend zu halten.</span><span class="sxs-lookup"><span data-stu-id="40f40-139">When a child window is destroyed, the system immediately reassigns the window identifiers to keep their range contiguous.</span></span> |



 

<span data-ttu-id="40f40-140">Wenn der Titel eines untergeordneten Fensters dem Menü Fenster hinzugefügt wird, weist das System dem untergeordneten Fenster einen Bezeichner zu.</span><span class="sxs-lookup"><span data-stu-id="40f40-140">When a child window's title is added to the window menu, the system assigns an identifier to the child window.</span></span> <span data-ttu-id="40f40-141">Wenn der Benutzer auf den Titel eines untergeordneten Fensters klickt, empfängt das Rahmen Fenster eine [**WM- \_ Befehls**](../menurc/wm-command.md) Meldung mit dem Bezeichner im *wParam* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="40f40-141">When the user clicks a child window's title, the frame window receives a [**WM\_COMMAND**](../menurc/wm-command.md) message with the identifier in the *wParam* parameter.</span></span> <span data-ttu-id="40f40-142">Sie sollten einen Wert für das **idfirstchild** -Element angeben, das nicht mit Menü Element bezeichaten im Menü des Rahmen Fensters in Konflikt steht.</span><span class="sxs-lookup"><span data-stu-id="40f40-142">You should specify a value for the **idFirstChild** member that does not conflict with menu-item identifiers in the frame window's menu.</span></span>

<span data-ttu-id="40f40-143">Die Rahmen Fenster Prozedur von MULTIPAD erstellt bei der Verarbeitung der [**WM \_ Create**](wm-create.md) -Meldung das MDI-Client Fenster.</span><span class="sxs-lookup"><span data-stu-id="40f40-143">Multipad's frame window procedure creates the MDI client window while processing the [**WM\_CREATE**](wm-create.md) message.</span></span> <span data-ttu-id="40f40-144">Im folgenden Beispiel wird gezeigt, wie das Client Fenster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="40f40-144">The following example shows how the client window is created.</span></span>


```
case WM_CREATE: 
    { 
        CLIENTCREATESTRUCT ccs; 
 
        // Retrieve the handle to the window menu and assign the 
        // first child window identifier. 
 
        ccs.hWindowMenu = GetSubMenu(GetMenu(hwnd), WINDOWMENU); 
        ccs.idFirstChild = IDM_WINDOWCHILD; 
 
        // Create the MDI client window. 
 
        hwndMDIClient = CreateWindow( "MDICLIENT", (LPCTSTR) NULL, 
            WS_CHILD | WS_CLIPCHILDREN | WS_VSCROLL | WS_HSCROLL, 
            0, 0, 0, 0, hwnd, (HMENU) 0xCAC, hInst, (LPSTR) &ccs); 
 
        ShowWindow(hwndMDIClient, SW_SHOW); 
    } 
    break; 
```



<span data-ttu-id="40f40-145">Am unteren Rand des Menü Fensters werden Titel von untergeordneten Fenstern hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="40f40-145">Titles of child windows are added to the bottom of the window menu.</span></span> <span data-ttu-id="40f40-146">Wenn die Anwendung dem Menü Fenster mithilfe der [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) -Funktion Zeichen folgen hinzufügt, können diese Zeichen folgen durch die Titel der untergeordneten Fenster überschrieben werden, wenn das Fenstermenü neu gezeichnet wird (wenn ein untergeordnetes Fenster erstellt oder zerstört wird).</span><span class="sxs-lookup"><span data-stu-id="40f40-146">If the application adds strings to the window menu by using the [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) function, these strings can be overwritten by the titles of the child windows when the window menu is repainted (whenever a child window is created or destroyed).</span></span> <span data-ttu-id="40f40-147">Eine MDI-Anwendung, die Ihrem Fenstermenü Zeichen folgen hinzufügt, sollte die [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) -Funktion verwenden und sicherstellen, dass die Titel der untergeordneten Fenster diese neuen Zeichen folgen nicht überschrieben haben.</span><span class="sxs-lookup"><span data-stu-id="40f40-147">An MDI application that adds strings to its window menu should use the [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) function and verify that the titles of child windows have not overwritten these new strings.</span></span>

<span data-ttu-id="40f40-148">Verwenden Sie das Format **WS \_ clipchildren** , um das MDI-Client Fenster zu erstellen, um zu verhindern, dass das Fenster über seine untergeordneten Fenster gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="40f40-148">Use the **WS\_CLIPCHILDREN** style to create the MDI client window to prevent the window from painting over its child windows.</span></span>

## <a name="writing-the-main-message-loop"></a><span data-ttu-id="40f40-149">Schreiben der Hauptnachrichten Schleife</span><span class="sxs-lookup"><span data-stu-id="40f40-149">Writing the Main Message Loop</span></span>

<span data-ttu-id="40f40-150">Die Hauptnachrichten Schleife einer MDI-Anwendung ähnelt der Verwendung einer Zugriffstaste für nicht-MDI-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="40f40-150">The main message loop of an MDI application is similar to that of a non-MDI application handling accelerator keys.</span></span> <span data-ttu-id="40f40-151">Der Unterschied besteht darin, dass die MDI-Nachrichten Schleife die [**translatemdisysaccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) -Funktion aufruft, bevor Sie auf Anwendungs definierte Zugriffstasten oder vor der Übermittlung der Nachricht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="40f40-151">The difference is that the MDI message loop calls the [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) function before checking for application-defined accelerator keys or before dispatching the message.</span></span>

<span data-ttu-id="40f40-152">Das folgende Beispiel zeigt die Nachrichten Schleife einer typischen MDI-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="40f40-152">The following example shows the message loop of a typical MDI application.</span></span> <span data-ttu-id="40f40-153">Beachten Sie, dass [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -1 zurückgeben kann, wenn ein Fehler vorliegt.</span><span class="sxs-lookup"><span data-stu-id="40f40-153">Note that [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) can return -1 if there is an error.</span></span>


```
MSG msg;
BOOL bRet;

while ((bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1)
    {
        // handle the error and possibly exit
    }
    else 
    { 
        if (!TranslateMDISysAccel(hwndMDIClient, &msg) && 
                !TranslateAccelerator(hwndFrame, hAccel, &msg))
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



<span data-ttu-id="40f40-154">Die [**translatemdisysaccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) -Funktion übersetzt [**WM- \_ KeyDown**](../inputdev/wm-keydown.md) -Nachrichten in [**WM- \_ syscommand**](../menurc/wm-syscommand.md) -Nachrichten und sendet Sie an das aktive untergeordnete MDI-Fenster.</span><span class="sxs-lookup"><span data-stu-id="40f40-154">The [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) function translates [**WM\_KEYDOWN**](../inputdev/wm-keydown.md) messages into [**WM\_SYSCOMMAND**](../menurc/wm-syscommand.md) messages and sends them to the active MDI child window.</span></span> <span data-ttu-id="40f40-155">Wenn es sich bei der Nachricht nicht um eine MDI-Zugriffstaste handelt, gibt die Funktion **false** zurück. in diesem Fall verwendet die Anwendung die [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) -Funktion, um zu bestimmen, ob eine der Anwendungs definierten Zugriffstasten gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="40f40-155">If the message is not an MDI accelerator message, the function returns **FALSE**, in which case the application uses the [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) function to determine whether any of the application-defined accelerator keys were pressed.</span></span> <span data-ttu-id="40f40-156">Wenn dies nicht der gibt, sendet die-Schleife die Meldung an die entsprechende Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="40f40-156">If not, the loop dispatches the message to the appropriate window procedure.</span></span>

## <a name="writing-the-frame-window-procedure"></a><span data-ttu-id="40f40-157">Schreiben der Rahmen Fenster Prozedur</span><span class="sxs-lookup"><span data-stu-id="40f40-157">Writing the Frame Window Procedure</span></span>

<span data-ttu-id="40f40-158">Die Fenster Prozedur für ein MDI-Rahmen Fenster ähnelt dem Hauptfenster einer MDI-Anwendung (Non – MDI).</span><span class="sxs-lookup"><span data-stu-id="40f40-158">The window procedure for an MDI frame window is similar to that of a non–MDI application's main window.</span></span> <span data-ttu-id="40f40-159">Der Unterschied besteht darin, dass eine Rahmen Fenster Prozedur alle Nachrichten, die nicht verarbeitet werden, an die [**defframeproc**](/windows/win32/api/winuser/nf-winuser-defframeproca) -Funktion und nicht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt.</span><span class="sxs-lookup"><span data-stu-id="40f40-159">The difference is that a frame window procedure passes all messages it does not handle to the [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) function rather than to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="40f40-160">Außerdem muss die Rahmen Fenster Prozedur auch einige Nachrichten übergeben, die Sie verarbeitet, einschließlich der in der folgenden Tabelle aufgeführten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="40f40-160">In addition, the frame window procedure must also pass some messages that it does handle, including those listed in the following table.</span></span>



| <span data-ttu-id="40f40-161">`Message`</span><span class="sxs-lookup"><span data-stu-id="40f40-161">Message</span></span>                                  | <span data-ttu-id="40f40-162">Antwort</span><span class="sxs-lookup"><span data-stu-id="40f40-162">Response</span></span>                                                                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40f40-163">**WM- \_ Befehl**</span><span class="sxs-lookup"><span data-stu-id="40f40-163">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)     | <span data-ttu-id="40f40-164">Aktiviert das untergeordnete MDI-Fenster, das der Benutzer auswählt.</span><span class="sxs-lookup"><span data-stu-id="40f40-164">Activates the MDI child window that the user chooses.</span></span> <span data-ttu-id="40f40-165">Diese Meldung wird gesendet, wenn der Benutzer ein untergeordnetes MDI-Fenster im Menü Fenster des MDI-Frame Fensters auswählt.</span><span class="sxs-lookup"><span data-stu-id="40f40-165">This message is sent when the user chooses an MDI child window from the window menu of the MDI frame window.</span></span> <span data-ttu-id="40f40-166">Die Fenster Kennung, die diese Meldung begleitet, identifiziert das untergeordnete MDI-Fenster, das aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="40f40-166">The window identifier accompanying this message identifies the MDI child window to be activated.</span></span> |
| [<span data-ttu-id="40f40-167">**WM- \_ menuchar**</span><span class="sxs-lookup"><span data-stu-id="40f40-167">**WM\_MENUCHAR**</span></span>](../menurc/wm-menuchar.md)   | <span data-ttu-id="40f40-168">Öffnet das Fenstermenü des aktiven untergeordneten MDI-Fensters, wenn der Benutzer die Tastenkombination Alt + – (minus) drückt.</span><span class="sxs-lookup"><span data-stu-id="40f40-168">Opens the window menu of the active MDI child window when the user presses the ALT+ – (minus) key combination.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="40f40-169">**WM- \_ SetFocus**</span><span class="sxs-lookup"><span data-stu-id="40f40-169">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md) | <span data-ttu-id="40f40-170">Übergibt den Tastaturfokus an das MDI-Client Fenster, das wiederum an das aktive untergeordnete MDI-Fenster übergibt.</span><span class="sxs-lookup"><span data-stu-id="40f40-170">Passes the keyboard focus to the MDI client window, which in turn passes it to the active MDI child window.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="40f40-171">**WM- \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="40f40-171">**WM\_SIZE**</span></span>](wm-size.md)              | <span data-ttu-id="40f40-172">Ändert die Größe des MDI-Client Fensters an den Client Bereich des neuen Rahmen Fensters.</span><span class="sxs-lookup"><span data-stu-id="40f40-172">Resizes the MDI client window to fit in the new frame window's client area.</span></span> <span data-ttu-id="40f40-173">Wenn die Rahmen Fenster Prozedur das MDI-Client Fenster auf eine andere Größe anpasst, sollte die Nachricht nicht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="40f40-173">If the frame window procedure sizes the MDI client window to a different size, it should not pass the message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>                   |



 

<span data-ttu-id="40f40-174">Die Rahmen Fenster Prozedur im MULTIPAD heißt mpframewndproc.</span><span class="sxs-lookup"><span data-stu-id="40f40-174">The frame window procedure in Multipad is called MPFrameWndProc.</span></span> <span data-ttu-id="40f40-175">Die Verarbeitung anderer Nachrichten durch mpframewndproc ähnelt der von nicht-–-MDI-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="40f40-175">The handling of other messages by MPFrameWndProc is similar to that of non–MDI applications.</span></span> <span data-ttu-id="40f40-176">[**WM \_ Befehls**](../menurc/wm-command.md) Meldungen im MULTIPAD werden von der lokal definierten CommandHandler-Funktion verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="40f40-176">[**WM\_COMMAND**](../menurc/wm-command.md) messages in Multipad are handled by the locally defined CommandHandler function.</span></span> <span data-ttu-id="40f40-177">Für Befehls Meldungen, die von MULTIPAD nicht verarbeitet werden, ruft CommandHandler die [**defframeproc**](/windows/win32/api/winuser/nf-winuser-defframeproca) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="40f40-177">For command messages Multipad does not handle, CommandHandler calls the [**DefFrameProc**](/windows/win32/api/winuser/nf-winuser-defframeproca) function.</span></span> <span data-ttu-id="40f40-178">Wenn MULTIPAD standardmäßig **defframeproc** nicht verwendet, kann der Benutzer ein untergeordnetes Fenster nicht über das Fenstermenü aktivieren, da die durch Klicken auf das Menü Element des Fensters gesendete **WM- \_ Befehls** Nachricht verloren gehen würde.</span><span class="sxs-lookup"><span data-stu-id="40f40-178">If Multipad does not use **DefFrameProc** by default, the user can't activate a child window from the window menu, because the **WM\_COMMAND** message sent by clicking the window's menu item would be lost.</span></span>

## <a name="writing-the-child-window-procedure"></a><span data-ttu-id="40f40-179">Schreiben der Prozedur für das untergeordnete Fenster</span><span class="sxs-lookup"><span data-stu-id="40f40-179">Writing the Child Window Procedure</span></span>

<span data-ttu-id="40f40-180">Wie bei der Rahmen Fenster Prozedur verwendet eine untergeordnete MDI-Fenster Prozedur eine spezielle Funktion für die Verarbeitung von Nachrichten standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="40f40-180">Like the frame window procedure, an MDI child window procedure uses a special function for processing messages by default.</span></span> <span data-ttu-id="40f40-181">Alle Nachrichten, die von der untergeordneten Fenster Prozedur nicht behandelt werden, müssen an die [**defmdichildproc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) -Funktion und nicht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="40f40-181">All messages that the child window procedure does not handle must be passed to the [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) function rather than to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="40f40-182">Außerdem müssen einige Fenster Verwaltungs Meldungen an **defmdichildproc** übergeben werden, selbst wenn die Anwendung die Nachricht verarbeitet, damit MDI ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="40f40-182">In addition, some window-management messages must be passed to **DefMDIChildProc**, even if the application handles the message, in order for MDI to function correctly.</span></span> <span data-ttu-id="40f40-183">Im folgenden finden Sie die Nachrichten, die von der Anwendung an **defmdichildproc** übergeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="40f40-183">Following are the messages the application must pass to **DefMDIChildProc**.</span></span>



| <span data-ttu-id="40f40-184">`Message`</span><span class="sxs-lookup"><span data-stu-id="40f40-184">Message</span></span>                                       | <span data-ttu-id="40f40-185">Antwort</span><span class="sxs-lookup"><span data-stu-id="40f40-185">Response</span></span>                                                                                                                                                                                                                                                  |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40f40-186">**WM- \_ childaktivierungs**</span><span class="sxs-lookup"><span data-stu-id="40f40-186">**WM\_CHILDACTIVATE**</span></span>](wm-childactivate.md) | <span data-ttu-id="40f40-187">Führt die Aktivierungs Verarbeitung aus, wenn untergeordnete MDI-Fenster verkleinert, verschoben oder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="40f40-187">Performs activation processing when MDI child windows are sized, moved, or displayed.</span></span> <span data-ttu-id="40f40-188">Diese Nachricht muss übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="40f40-188">This message must be passed.</span></span>                                                                                                                                        |
| [<span data-ttu-id="40f40-189">**WM \_ getminmaxinfo**</span><span class="sxs-lookup"><span data-stu-id="40f40-189">**WM\_GETMINMAXINFO**</span></span>](wm-getminmaxinfo.md) | <span data-ttu-id="40f40-190">Berechnet die Größe eines untergeordneten MDI-Fensters basierend auf der aktuellen Größe des MDI-Client Fensters.</span><span class="sxs-lookup"><span data-stu-id="40f40-190">Calculates the size of a maximized MDI child window, based on the current size of the MDI client window.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="40f40-191">**WM- \_ menuchar**</span><span class="sxs-lookup"><span data-stu-id="40f40-191">**WM\_MENUCHAR**</span></span>](../menurc/wm-menuchar.md)        | <span data-ttu-id="40f40-192">Übergibt die Nachricht an das MDI-Rahmen Fenster.</span><span class="sxs-lookup"><span data-stu-id="40f40-192">Passes the message to the MDI frame window.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="40f40-193">**WM \_ verschieben**</span><span class="sxs-lookup"><span data-stu-id="40f40-193">**WM\_MOVE**</span></span>](wm-move.md)                   | <span data-ttu-id="40f40-194">Berechnet die MDI-Client Scrollleisten neu, wenn Sie vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="40f40-194">Recalculates MDI client scroll bars, if they are present.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="40f40-195">**WM- \_ SetFocus**</span><span class="sxs-lookup"><span data-stu-id="40f40-195">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md)      | <span data-ttu-id="40f40-196">Aktiviert das untergeordnete Fenster, wenn es sich nicht um das aktive untergeordnete MDI-Fenster handelt.</span><span class="sxs-lookup"><span data-stu-id="40f40-196">Activates the child window, if it is not the active MDI child window.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="40f40-197">**WM- \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="40f40-197">**WM\_SIZE**</span></span>](wm-size.md)                   | <span data-ttu-id="40f40-198">Führt Vorgänge aus, die zum Ändern der Größe eines Fensters erforderlich sind, insbesondere zum Maximieren oder Wiederherstellen eines untergeordneten MDI-Fensters.</span><span class="sxs-lookup"><span data-stu-id="40f40-198">Performs operations necessary for changing the size of a window, especially for maximizing or restoring an MDI child window.</span></span> <span data-ttu-id="40f40-199">Wenn diese Nachricht nicht an die [**defmdichildproc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) -Funktion übergeben wird, entstehen sehr unerwünschte Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="40f40-199">Failing to pass this message to the [**DefMDIChildProc**](/windows/win32/api/winuser/nf-winuser-defmdichildproca) function produces highly undesirable results.</span></span> |
| [<span data-ttu-id="40f40-200">**WM ( \_ syscommand)**</span><span class="sxs-lookup"><span data-stu-id="40f40-200">**WM\_SYSCOMMAND**</span></span>](../menurc/wm-syscommand.md)    | <span data-ttu-id="40f40-201">Handles (früher als System bezeichnet) Menübefehle: **SC \_ NextWindow**, **SC \_ prevwindow**, **SC \_ Move**, **SC \_ size** und **SC \_ maximi.**</span><span class="sxs-lookup"><span data-stu-id="40f40-201">Handles window (formerly known as system) menu commands: **SC\_NEXTWINDOW**, **SC\_PREVWINDOW**, **SC\_MOVE**, **SC\_SIZE**, and **SC\_MAXIMIZE**.</span></span>                                                                                                        |



 

## <a name="creating-a-child-window"></a><span data-ttu-id="40f40-202">Erstellen eines untergeordneten Fensters</span><span class="sxs-lookup"><span data-stu-id="40f40-202">Creating a Child Window</span></span>

<span data-ttu-id="40f40-203">Zum Erstellen eines untergeordneten MDI-Fensters kann eine Anwendung entweder die Funktion " [**anatemdiwindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) " aufrufen oder eine " [**WM \_ mdicreate**](wm-mdicreate.md) "-Meldung an das MDI-Client Fenster senden.</span><span class="sxs-lookup"><span data-stu-id="40f40-203">To create an MDI child window, an application can either call the [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) function or send an [**WM\_MDICREATE**](wm-mdicreate.md) message to the MDI client window.</span></span> <span data-ttu-id="40f40-204">(Die Anwendung kann die Funktion "- [**Editor**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " mit dem " **WS \_ Ex \_ MDIChild** "-Stil verwenden, um untergeordnete MDI-Fenster zu erstellen.) In einer MDI-Anwendung mit einem Thread kann eine der beiden Methoden zum Erstellen eines untergeordneten Fensters verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40f40-204">(The application can use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function with the **WS\_EX\_MDICHILD** style to create MDI child windows.) A single-threaded MDI application can use either method to create a child window.</span></span> <span data-ttu-id="40f40-205">Ein Thread in einer Multithread-MDI-Anwendung muss die Funktion " **anatemdiwindow** " oder " **kreatewindowex** " verwenden, um ein untergeordnetes Fenster in einem anderen Thread zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="40f40-205">A thread in a multithreaded MDI application must use the **CreateMDIWindow** or **CreateWindowEx** function to create a child window in a different thread.</span></span>

<span data-ttu-id="40f40-206">Der *LPARAM* -Parameter einer [**WM- \_ mdicreate**](wm-mdicreate.md) -Meldung ist ein weitaus Zeiger auf eine [**mdikreatestruct**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="40f40-206">The *lParam* parameter of a [**WM\_MDICREATE**](wm-mdicreate.md) message is a far pointer to an [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure.</span></span> <span data-ttu-id="40f40-207">Die Struktur enthält vier Dimensions Elemente: **x** und **y**, die die horizontale und vertikale Position des Fensters angeben, sowie **CX** und **CY**, die die horizontalen und vertikalen Blöcke des Fensters angeben.</span><span class="sxs-lookup"><span data-stu-id="40f40-207">The structure includes four dimension members: **x** and **y**, which indicate the horizontal and vertical positions of the window, and **cx** and **cy**, which indicate the horizontal and vertical extents of the window.</span></span> <span data-ttu-id="40f40-208">Diese Member können explizit von der Anwendung zugewiesen werden, oder Sie können auf **CW \_ usedefault** festgelegt werden. in diesem Fall wählt das System eine Position, Größe oder beides gemäß einem kaskadierenden Algorithmus aus.</span><span class="sxs-lookup"><span data-stu-id="40f40-208">Any of these members may be assigned explicitly by the application, or they may be set to **CW\_USEDEFAULT**, in which case the system selects a position, size, or both, according to a cascading algorithm.</span></span> <span data-ttu-id="40f40-209">In jedem Fall müssen alle vier Member initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="40f40-209">In any case, all four members must be initialized.</span></span> <span data-ttu-id="40f40-210">MULTIPAD verwendet **CW \_ usedefault** für alle Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="40f40-210">Multipad uses **CW\_USEDEFAULT** for all dimensions.</span></span>

<span data-ttu-id="40f40-211">Das letzte Element der [**mdikreatestruct**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) -Struktur ist der **stilmember** , der möglicherweise stilbits für das Fenster enthält.</span><span class="sxs-lookup"><span data-stu-id="40f40-211">The last member of the [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure is the **style** member, which may contain style bits for the window.</span></span> <span data-ttu-id="40f40-212">Zum Erstellen eines untergeordneten MDI-Fensters, das eine beliebige Kombination von Fenster Stilen aufweisen kann, geben Sie den Fenster Stil " **MDIS \_ allchildstyles** " an.</span><span class="sxs-lookup"><span data-stu-id="40f40-212">To create an MDI child window that can have any combination of window styles, specify the **MDIS\_ALLCHILDSTYLES** window style.</span></span> <span data-ttu-id="40f40-213">Wenn dieses Format nicht angegeben wird, hat ein untergeordnetes MDI-Fenster die Stile " **WS- \_ minimieren**", " **WS \_ maximieren**", " **WS \_ HScroll**" und " **WS \_ VScroll** " als Standardeinstellungen</span><span class="sxs-lookup"><span data-stu-id="40f40-213">When this style is not specified, an MDI child window has the **WS\_MINIMIZE**, **WS\_MAXIMIZE**, **WS\_HSCROLL**, and **WS\_VSCROLL** styles as default settings.</span></span>

<span data-ttu-id="40f40-214">MULTIPAD erstellt mithilfe der lokal definierten AddFile-Funktion (in der Quelldatei mpfile) die untergeordneten MDI-Fenster. C).</span><span class="sxs-lookup"><span data-stu-id="40f40-214">Multipad creates its MDI child windows by using its locally defined AddFile function (located in the source file MPFILE.C).</span></span> <span data-ttu-id="40f40-215">Die AddFile-Funktion legt den Titel des untergeordneten Fensters fest, indem der **sztitle** -Member der [**mdikreatestruct**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) -Struktur des Fensters entweder dem Namen der bearbeiteten Datei oder der "unbenannten"-Struktur zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="40f40-215">The AddFile function sets the title of the child window by assigning the **szTitle** member of the window's [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) structure to either the name of the file being edited or to "Untitled."</span></span> <span data-ttu-id="40f40-216">Der **szclass** -Member wird auf den Namen der untergeordneten MDI-Fenster Klasse festgelegt, die in der initializeapplication-Funktion von MULTIPAD registriert ist.</span><span class="sxs-lookup"><span data-stu-id="40f40-216">The **szClass** member is set to the name of the MDI child window class registered in Multipad's InitializeApplication function.</span></span> <span data-ttu-id="40f40-217">Das **howner** -Element wird auf das Instanzhandle der Anwendung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="40f40-217">The **hOwner** member is set to the application's instance handle.</span></span>

<span data-ttu-id="40f40-218">Das folgende Beispiel zeigt die AddFile-Funktion im MULTIPAD.</span><span class="sxs-lookup"><span data-stu-id="40f40-218">The following example shows the AddFile function in Multipad.</span></span>


```
HWND APIENTRY AddFile(pName) 
TCHAR * pName; 
{ 
    HWND hwnd; 
    TCHAR sz[160]; 
    MDICREATESTRUCT mcs; 
 
    if (!pName) 
    { 
 
        // If the pName parameter is NULL, load the "Untitled" 
        // string from the STRINGTABLE resource and set the szTitle 
        // member of MDICREATESTRUCT. 
 
        LoadString(hInst, IDS_UNTITLED, sz, sizeof(sz)/sizeof(TCHAR)); 
        mcs.szTitle = (LPCTSTR) sz; 
    } 
    else 
 
        // Title the window with the full path and filename, 
        // obtained by calling the OpenFile function with the 
        // OF_PARSE flag, which is called before AddFile(). 
 
        mcs.szTitle = of.szPathName; 
 
    mcs.szClass = szChild; 
    mcs.hOwner  = hInst; 
 
    // Use the default size for the child window. 
 
    mcs.x = mcs.cx = CW_USEDEFAULT; 
    mcs.y = mcs.cy = CW_USEDEFAULT; 
 
    // Give the child window the default style. The styleDefault 
    // variable is defined in MULTIPAD.C. 
 
    mcs.style = styleDefault; 
 
    // Tell the MDI client window to create the child window. 
 
    hwnd = (HWND) SendMessage (hwndMDIClient, WM_MDICREATE, 0, 
        (LONG) (LPMDICREATESTRUCT) &mcs); 
 
    // If the file is found, read its contents into the child 
    // window's client area. 
 
    if (pName) 
    { 
        if (!LoadFile(hwnd, pName)) 
        { 
 
            // Cannot load the file; close the window. 
 
            SendMessage(hwndMDIClient, WM_MDIDESTROY, 
                (DWORD) hwnd, 0L); 
        } 
    } 
    return hwnd; 
} 
```



<span data-ttu-id="40f40-219">Der Zeiger, der im *LPARAM* -Parameter der [**WM- \_ mdicreate**](wm-mdicreate.md) -Nachricht übergeben wird, wird an die Funktion " [**foratewindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) " übergeben und als erstes Element in der Struktur "Struktur erstellen" angezeigt, das [**in der "**](/windows/win32/api/winuser/ns-winuser-createstructa) [**WM \_ Create**](wm-create.md) "-Nachricht übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="40f40-219">The pointer passed in the *lParam* parameter of the [**WM\_MDICREATE**](wm-mdicreate.md) message is passed to the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) function and appears as the first member in the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure, passed in the [**WM\_CREATE**](wm-create.md) message.</span></span> <span data-ttu-id="40f40-220">Im MULTIPAD initialisiert das untergeordnete Fenster während der **WM \_** die Nachrichtenverarbeitung, indem Dokument Variablen in den zusätzlichen Daten initialisiert werden und das untergeordnete Fenster des Bearbeitungs Steuer Elements erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="40f40-220">In Multipad, the child window initializes itself during **WM\_CREATE** message processing by initializing document variables in its extra data and by creating the edit control's child window.</span></span>

 

 
