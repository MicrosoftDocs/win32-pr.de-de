---
title: Verwenden von Menüs
description: Dieser Abschnitt enthält Codebeispiele für Aufgaben im Zusammenhang mit Menüs.
ms.assetid: b1391e37-a146-46ec-a329-aa57cfcfd351
keywords:
- Ressourcen, Menüs
- Menüs, erstellen
- Menü Vorlagen Ressourcen
- Ressourcen, Menüvorlage
- Erweitertes Menü-Vorlagen Format
- Format der alten Menüvorlage
- Menü Vorlagen Ressourcen werden geladen.
- Menüs, Klasse
- Menüs, Verknüpfung
- Erstellen von Menüs
- Klassen Menüs
- Kontextmenüs
- Bitmaps für Menü Elemente
- Menüs, gezeichnete Besitzer
- vom Besitzer gezeichnete Menüs
- Bitmaps für benutzerdefinierte Prüfzeichen
- Menüs, Kontrollkästchen
- Menüs, Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d216b5fe5e6c25a98b5bdf3abe9d55b4bb0b34f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726752"
---
# <a name="using-menus"></a><span data-ttu-id="44b7f-121">Verwenden von Menüs</span><span class="sxs-lookup"><span data-stu-id="44b7f-121">Using Menus</span></span>

<span data-ttu-id="44b7f-122">In diesem Abschnitt werden die folgenden Aufgaben beschrieben:</span><span class="sxs-lookup"><span data-stu-id="44b7f-122">This section describes the following tasks:</span></span>

-   [<span data-ttu-id="44b7f-123">Verwenden einer Menu-Template-Ressource</span><span class="sxs-lookup"><span data-stu-id="44b7f-123">Using a Menu-Template Resource</span></span>](#using-a-menu-template-resource)
    -   [<span data-ttu-id="44b7f-124">Erweitertes Menu-Template Format</span><span class="sxs-lookup"><span data-stu-id="44b7f-124">Extended Menu-Template Format</span></span>](#extended-menu-template-format)
    -   [<span data-ttu-id="44b7f-125">Altes Menu-Template Format</span><span class="sxs-lookup"><span data-stu-id="44b7f-125">Old Menu-Template Format</span></span>](#old-menu-template-format)
    -   [<span data-ttu-id="44b7f-126">Laden einer Menu-Template Ressource</span><span class="sxs-lookup"><span data-stu-id="44b7f-126">Loading a Menu-Template Resource</span></span>](#loading-a-menu-template-resource)
    -   [<span data-ttu-id="44b7f-127">Erstellen eines Klassen Menüs</span><span class="sxs-lookup"><span data-stu-id="44b7f-127">Creating a Class Menu</span></span>](#creating-a-class-menu)
-   [<span data-ttu-id="44b7f-128">Erstellen eines Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="44b7f-128">Creating a Shortcut Menu</span></span>](#creating-a-shortcut-menu)
    -   [<span data-ttu-id="44b7f-129">Verarbeiten der WM- \_ ContextMenu-Meldung</span><span class="sxs-lookup"><span data-stu-id="44b7f-129">Processing the WM\_CONTEXTMENU Message</span></span>](/windows)
    -   [<span data-ttu-id="44b7f-130">Erstellen einer Verknüpfung Font-Attributes Menü</span><span class="sxs-lookup"><span data-stu-id="44b7f-130">Creating a Shortcut Font-Attributes Menu</span></span>](#creating-a-shortcut-font-attributes-menu)
    -   [<span data-ttu-id="44b7f-131">Anzeigen eines Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="44b7f-131">Displaying a Shortcut Menu</span></span>](#displaying-a-shortcut-menu)
-   [<span data-ttu-id="44b7f-132">Verwenden von Menu-Item Bitmaps</span><span class="sxs-lookup"><span data-stu-id="44b7f-132">Using Menu-Item Bitmaps</span></span>](#using-menu-item-bitmaps)
    -   [<span data-ttu-id="44b7f-133">Festlegen des Bitmap-Typflags</span><span class="sxs-lookup"><span data-stu-id="44b7f-133">Setting the Bitmap Type Flag</span></span>](#setting-the-bitmap-type-flag)
    -   [<span data-ttu-id="44b7f-134">Erstellen der Bitmap</span><span class="sxs-lookup"><span data-stu-id="44b7f-134">Creating the Bitmap</span></span>](#creating-the-bitmap)
    -   [<span data-ttu-id="44b7f-135">Hinzufügen von Linien und Diagrammen zu einem Menü</span><span class="sxs-lookup"><span data-stu-id="44b7f-135">Adding Lines and Graphs to a Menu</span></span>](#adding-lines-and-graphs-to-a-menu)
    -   [<span data-ttu-id="44b7f-136">Beispiel für Menu-Item Bitmaps</span><span class="sxs-lookup"><span data-stu-id="44b7f-136">Example of Menu-Item Bitmaps</span></span>](#example-of-menu-item-bitmaps)
-   [<span data-ttu-id="44b7f-137">Erstellen von Owner-Drawn Menü Elementen</span><span class="sxs-lookup"><span data-stu-id="44b7f-137">Creating Owner-Drawn Menu Items</span></span>](#creating-owner-drawn-menu-items)
    -   [<span data-ttu-id="44b7f-138">Festlegen des Owner-Drawn Flags</span><span class="sxs-lookup"><span data-stu-id="44b7f-138">Setting the Owner-Drawn Flag</span></span>](#setting-the-owner-drawn-flag)
    -   [<span data-ttu-id="44b7f-139">Vom Besitzer gezeichnete Menüs und die WM- \_ MeasureItem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="44b7f-139">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>](/windows)
    -   [<span data-ttu-id="44b7f-140">Von einem Besitzer gezeichnete Menüs und die WM- \_ DrawItem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="44b7f-140">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>](/windows)
    -   [<span data-ttu-id="44b7f-141">Von einem Besitzer gezeichnete Menüs und die WM- \_ menuchar-Meldung</span><span class="sxs-lookup"><span data-stu-id="44b7f-141">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>](/windows)
    -   [<span data-ttu-id="44b7f-142">Festlegen von Schriftarten für Menu-Item Text Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="44b7f-142">Setting Fonts for Menu-Item Text Strings</span></span>](#setting-fonts-for-menu-item-text-strings)
    -   [<span data-ttu-id="44b7f-143">Beispiel für Owner-Drawn Menü Elemente</span><span class="sxs-lookup"><span data-stu-id="44b7f-143">Example of Owner-Drawn Menu Items</span></span>](#example-of-owner-drawn-menu-items)
-   [<span data-ttu-id="44b7f-144">Verwenden von benutzerdefinierten Häkchen-Bitmaps</span><span class="sxs-lookup"><span data-stu-id="44b7f-144">Using Custom Check Mark Bitmaps</span></span>](#using-custom-check-mark-bitmaps)
    -   [<span data-ttu-id="44b7f-145">Erstellen von benutzerdefinierten Häkchen Bitmaps</span><span class="sxs-lookup"><span data-stu-id="44b7f-145">Creating Custom Check Mark Bitmaps</span></span>](#creating-custom-check-mark-bitmaps)
    -   [<span data-ttu-id="44b7f-146">Zuordnen von Bitmaps zu einem Menü Element</span><span class="sxs-lookup"><span data-stu-id="44b7f-146">Associating Bitmaps with a Menu Item</span></span>](#associating-bitmaps-with-a-menu-item)
    -   [<span data-ttu-id="44b7f-147">Festlegen des Häkchen Attributs</span><span class="sxs-lookup"><span data-stu-id="44b7f-147">Setting the Check-mark Attribute</span></span>](#setting-the-check-mark-attribute)
    -   [<span data-ttu-id="44b7f-148">Simulieren von Kontrollkästchen in einem Menü</span><span class="sxs-lookup"><span data-stu-id="44b7f-148">Simulating Check Boxes in a Menu</span></span>](#simulating-check-boxes-in-a-menu)
    -   [<span data-ttu-id="44b7f-149">Beispiel für die Verwendung von benutzerdefinierten Bitmaps für das Häkchen</span><span class="sxs-lookup"><span data-stu-id="44b7f-149">Example of Using Custom Check-mark Bitmaps</span></span>](#example-of-using-custom-check-mark-bitmaps)

## <a name="using-a-menu-template-resource"></a><span data-ttu-id="44b7f-150">Verwenden einer Menu-Template-Ressource</span><span class="sxs-lookup"><span data-stu-id="44b7f-150">Using a Menu-Template Resource</span></span>

<span data-ttu-id="44b7f-151">In der Regel fügen Sie ein Menü in eine Anwendung ein, indem Sie eine Menü Vorlagen Ressource erstellen und das Menü dann zur Laufzeit laden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-151">You typically include a menu in an application by creating a menu-template resource and then loading the menu at run time.</span></span> <span data-ttu-id="44b7f-152">In diesem Abschnitt wird das Format einer Menüvorlage beschrieben. Außerdem wird erläutert, wie Sie eine Menü Vorlagen Ressource laden und in Ihrer Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-152">This section describes the format of a menu template, and explains how to load a menu-template resource and use it in your application.</span></span> <span data-ttu-id="44b7f-153">Weitere Informationen zum Erstellen einer Menü Vorlagen Ressource finden Sie in der Dokumentation, die in ihren Entwicklungs Tools enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-153">For information about creating a menu-template resource, see the documentation included with your development tools.</span></span>

-   [<span data-ttu-id="44b7f-154">Erweitertes Menu-Template Format</span><span class="sxs-lookup"><span data-stu-id="44b7f-154">Extended Menu-Template Format</span></span>](#extended-menu-template-format)
-   [<span data-ttu-id="44b7f-155">Altes Menu-Template Format</span><span class="sxs-lookup"><span data-stu-id="44b7f-155">Old Menu-Template Format</span></span>](#old-menu-template-format)
-   [<span data-ttu-id="44b7f-156">Laden einer Menu-Template Ressource</span><span class="sxs-lookup"><span data-stu-id="44b7f-156">Loading a Menu-Template Resource</span></span>](#loading-a-menu-template-resource)
-   [<span data-ttu-id="44b7f-157">Erstellen eines Klassen Menüs</span><span class="sxs-lookup"><span data-stu-id="44b7f-157">Creating a Class Menu</span></span>](#creating-a-class-menu)

### <a name="extended-menu-template-format"></a><span data-ttu-id="44b7f-158">Erweitertes Menu-Template Format</span><span class="sxs-lookup"><span data-stu-id="44b7f-158">Extended Menu-Template Format</span></span>

<span data-ttu-id="44b7f-159">Das erweiterte Menü Vorlagen Format unterstützt zusätzliche Menüfunktionen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-159">The extended menu-template format supports additional menu functionality.</span></span> <span data-ttu-id="44b7f-160">Ebenso wie Standardmenü Vorlagen Ressourcen haben erweiterte Menü Vorlagen Ressourcen den **\_ Menü** Ressourcentyp RT.</span><span class="sxs-lookup"><span data-stu-id="44b7f-160">Like standard menu-template resources, extended menu-template resources have the **RT\_MENU** resource type.</span></span> <span data-ttu-id="44b7f-161">Das System unterscheidet die beiden Ressourcen Formate durch die Versionsnummer, die der erste Member des Ressourcen Headers ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-161">The system distinguishes the two resource formats by the version number, which is the first member of the resource header.</span></span>

<span data-ttu-id="44b7f-162">Eine erweiterte Menüvorlage besteht aus einer [**menuex- \_ Vorlagen \_ Header**](menuex-template-header.md) Struktur, gefolgt von einer weiteren [**menuex- \_ Vorlagen \_ Element**](menuex-template-item.md) -Element Definitions Struktur.</span><span class="sxs-lookup"><span data-stu-id="44b7f-162">An extended menu template consists of a [**MENUEX\_TEMPLATE\_HEADER**](menuex-template-header.md) structure followed by one more [**MENUEX\_TEMPLATE\_ITEM**](menuex-template-item.md) item definition structures.</span></span>

### <a name="old-menu-template-format"></a><span data-ttu-id="44b7f-163">Altes Menu-Template Format</span><span class="sxs-lookup"><span data-stu-id="44b7f-163">Old Menu-Template Format</span></span>

<span data-ttu-id="44b7f-164">In einer alten Menüvorlage (Microsoft Windows NT 3,51 und früher) ist ein Menü definiert, aber die neue Menü Funktionalität wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="44b7f-164">An old menu template (Microsoft Windows NT 3.51 and earlier) defines a menu, but does not support the new menu functionality.</span></span> <span data-ttu-id="44b7f-165">Eine alte Menü Vorlagen Ressource verfügt über den **RT- \_ Menü** Ressourcentyp.</span><span class="sxs-lookup"><span data-stu-id="44b7f-165">An old menu-template resource has the **RT\_MENU** resource type.</span></span>

<span data-ttu-id="44b7f-166">Eine alte Menüvorlage besteht aus einer [**menuitemtemplateheader**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) -Struktur, gefolgt von einer oder mehreren [**menuitemtemplate**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-166">An old menu template consists of a [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) structure followed by one or more [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) structures.</span></span>

### <a name="loading-a-menu-template-resource"></a><span data-ttu-id="44b7f-167">Laden einer Menu-Template Ressource</span><span class="sxs-lookup"><span data-stu-id="44b7f-167">Loading a Menu-Template Resource</span></span>

<span data-ttu-id="44b7f-168">Verwenden Sie zum Laden einer Menü Vorlagen Ressource die [**loadmenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) -Funktion, und geben Sie ein Handle für das Modul an, das die Ressource und den Bezeichner der Menüvorlage enthält.</span><span class="sxs-lookup"><span data-stu-id="44b7f-168">To load a menu-template resource, use the [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) function, specifying a handle to the module that contains the resource and the menu template's identifier.</span></span> <span data-ttu-id="44b7f-169">Die **loadmenu** -Funktion gibt ein Menü Handle zurück, das Sie verwenden können, um das Menü einem Fenster zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-169">The **LoadMenu** function returns a menu handle that you can use to assign the menu to a window.</span></span> <span data-ttu-id="44b7f-170">Dieses Fenster wird zum Besitzer Fenster des Menüs, das alle vom Menü generierten Meldungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="44b7f-170">This window becomes the menu's owner window, receiving all the messages generated by the menu.</span></span>

<span data-ttu-id="44b7f-171">Verwenden Sie die [**loadmenuindirekte**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) -Funktion, um ein Menü aus einer Menüvorlage zu erstellen, die sich bereits im Arbeitsspeicher befindet.</span><span class="sxs-lookup"><span data-stu-id="44b7f-171">To create a menu from a menu template that is already in memory, use the [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) function.</span></span> <span data-ttu-id="44b7f-172">Dies ist nützlich, wenn Ihre Anwendung Menü Vorlagen dynamisch generiert.</span><span class="sxs-lookup"><span data-stu-id="44b7f-172">This is useful if your application generates menu templates dynamically.</span></span>

<span data-ttu-id="44b7f-173">Wenn Sie ein Menü einem Fenster zuweisen möchten, verwenden Sie die [**setMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) -Funktion, oder geben Sie beim Erstellen eines Fensters das Handle des Menüs im *HMENU* -Parameter der Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " an.</span><span class="sxs-lookup"><span data-stu-id="44b7f-173">To assign a menu to a window, use the [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) function or specify the menu's handle in the *hMenu* parameter of the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function when creating a window.</span></span> <span data-ttu-id="44b7f-174">Eine andere Möglichkeit, einem Fenster ein Menü zuzuweisen, besteht darin, eine Menüvorlage anzugeben, wenn Sie eine Fenster Klasse registrieren. die Vorlage identifiziert das angegebene Menü als Klassen Menü für diese Fenster Klasse.</span><span class="sxs-lookup"><span data-stu-id="44b7f-174">Another way you can assign a menu to a window is to specify a menu template when you register a window class; the template identifies the specified menu as the class menu for that window class.</span></span>

<span data-ttu-id="44b7f-175">Wenn das System ein bestimmtes Menü automatisch einem Fenster zuweisen soll, geben Sie die Menüvorlage an, wenn Sie die Klasse des Fensters registrieren.</span><span class="sxs-lookup"><span data-stu-id="44b7f-175">To have the system automatically assign a specific menu to a window, specify the menu's template when you register the window's class.</span></span> <span data-ttu-id="44b7f-176">Die Vorlage identifiziert das angegebene Menü als Klassen Menü für diese Fenster Klasse.</span><span class="sxs-lookup"><span data-stu-id="44b7f-176">The template identifies the specified menu as the class menu for that window class.</span></span> <span data-ttu-id="44b7f-177">Wenn Sie dann ein Fenster der angegebenen Klasse erstellen, weist das System das angegebene Menü automatisch dem Fenster zu.</span><span class="sxs-lookup"><span data-stu-id="44b7f-177">Then, when you create a window of the specified class, the system automatically assigns the specified menu to the window.</span></span>

<span data-ttu-id="44b7f-178">Einem Fenster, das ein untergeordnetes Fenster ist, kann kein Menü zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-178">You cannot assign a menu to a window that is a child window.</span></span>

<span data-ttu-id="44b7f-179">Um ein Klassen Menü zu erstellen, schließen Sie den Bezeichner der Menü Vorlagen Ressource als **lpszmenuname** -Member einer [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur ein, und übergeben Sie dann einen Zeiger auf die-Struktur an die [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="44b7f-179">To create a class menu, include the identifier of the menu-template resource as the **lpszMenuName** member of a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure and then pass a pointer to the structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span>

### <a name="creating-a-class-menu"></a><span data-ttu-id="44b7f-180">Erstellen eines Klassen Menüs</span><span class="sxs-lookup"><span data-stu-id="44b7f-180">Creating a Class Menu</span></span>

<span data-ttu-id="44b7f-181">Im folgenden Beispiel wird gezeigt, wie ein Klassen Menü für eine Anwendung erstellt wird, ein Fenster erstellt wird, in dem das Klassen Menü und Menübefehle verarbeiten in der Fenster Prozedur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-181">The following example shows how to create a class menu for an application, create a window that uses the class menu, and process menu commands in the window procedure.</span></span>

<span data-ttu-id="44b7f-182">Im folgenden ist der relevante Teil der Header Datei der Anwendung aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="44b7f-182">Following is the relevant portion of the application's header file:</span></span>


```
// Menu-template resource identifier 
 
#define IDM_MYMENURESOURCE   3
```



<span data-ttu-id="44b7f-183">Im folgenden sind die relevanten Teile der Anwendung selbst aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="44b7f-183">Following are the relevant portions of the application itself:</span></span>


```
HINSTANCE hinst; 
 
int APIENTRY WinMain(HINSTANCE hinstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg = { };  // message 
    WNDCLASS wc;    // windowclass data 
    HWND hwnd;      // handle to the main window 
 
    // Create the window class for the main window. Specify 
    // the identifier of the menu-template resource as the 
    // lpszMenuName member of the WNDCLASS structure to create 
    // the class menu. 
 
    wc.style = 0; 
    wc.lpfnWndProc = (WNDPROC) MainWndProc; 
    wc.cbClsExtra = 0; 
    wc.cbWndExtra = 0; 
    wc.hInstance = hinstance; 
    wc.hIcon = LoadIcon(NULL, IDI_APPLICATION); 
    wc.hCursor = LoadCursor(NULL, IDC_ARROW); 
    wc.hbrBackground = GetStockObject(WHITE_BRUSH); 
    wc.lpszMenuName =  MAKEINTRESOURCE(IDM_MYMENURESOURCE); 
    wc.lpszClassName = "MainWClass"; 
 
    if (!RegisterClass(&wc)) 
        return FALSE; 
 
    hinst = hinstance; 
 
    // Create the main window. Set the hmenu parameter to NULL so 
    // that the system uses the class menu for the window. 
 
    hwnd = CreateWindow("MainWClass", "Sample Application", 
        WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, hinstance, 
        NULL); 
 
    if (hwnd == NULL) 
        return FALSE; 
 
    // Make the window visible and send a WM_PAINT message to the 
    // window procedure. 
 
    ShowWindow(hwnd, nCmdShow); 
    UpdateWindow(hwnd); 
 
    // Start the main message loop. 
 
    while (GetMessage(&msg, NULL, 0, 0)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
    return msg.wParam; 
        UNREFERENCED_PARAMETER(hPrevInstance); 
} 
 
 
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    switch (uMsg) 
    { 
        // Process other window messages. 
 
        case WM_COMMAND: 
 
            // Test for the identifier of a command item. 
 
            switch(LOWORD(wParam)) 
            { 
                case IDM_FI_OPEN: 
                    DoFileOpen();   // application-defined 
                    break; 
 
                case IDM_FI_CLOSE: 
                    DoFileClose();  // application-defined 
                    break; 
                // Process other menu commands. 
 
                default: 
                    break; 
 
            } 
            return 0; 
 
        // Process other window messages. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



## <a name="creating-a-shortcut-menu"></a><span data-ttu-id="44b7f-184">Erstellen eines Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="44b7f-184">Creating a Shortcut Menu</span></span>

<span data-ttu-id="44b7f-185">Wenn Sie ein Kontextmenü in einer Anwendung verwenden möchten, übergeben Sie das zugehörige Handle an die [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="44b7f-185">To use a shortcut menu in an application, pass its handle to the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function.</span></span> <span data-ttu-id="44b7f-186">Eine Anwendung ruft in der Regel **TrackPopupMenuEx** in einer Fenster Prozedur als Reaktion auf eine benutzergenerierte Meldung auf, z. b. [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) oder [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown).</span><span class="sxs-lookup"><span data-stu-id="44b7f-186">An application typically calls **TrackPopupMenuEx** in a window procedure in response to a user-generated message, such as [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) or [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown).</span></span>

<span data-ttu-id="44b7f-187">Zusätzlich zum Popup-Menü handle erfordert [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) , dass Sie ein Handle für das Besitzer Fenster, die Position des Kontextmenüs (in Bildschirm Koordinaten) und die Maustaste angeben, mit der der Benutzer ein Element auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="44b7f-187">In addition to the pop-up menu handle, [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) requires that you specify a handle to the owner window, the position of the shortcut menu (in screen coordinates), and the mouse button that the user can use to choose an item.</span></span>

<span data-ttu-id="44b7f-188">Die ältere [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) -Funktion wird weiterhin unterstützt, aber neue Anwendungen sollten die [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-188">The older [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function is still supported, but new applications should use the [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) function.</span></span> <span data-ttu-id="44b7f-189">Die **TrackPopupMenuEx** -Funktion erfordert dieselben Parameter wie **TrackPopupMenu**, aber Sie können auch einen Teil des Bildschirms angeben, der vom Menü nicht verdeckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="44b7f-189">The **TrackPopupMenuEx** function requires the same parameters as **TrackPopupMenu**, but also lets you specify a portion of the screen that the menu should not obscure.</span></span> <span data-ttu-id="44b7f-190">Eine Anwendung ruft diese Funktionen in der Regel in einer Fenster Prozedur auf, wenn die [**WM- \_ ContextMenu**](wm-contextmenu.md) -Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="44b7f-190">An application typically calls these functions in a window procedure when processing the [**WM\_CONTEXTMENU**](wm-contextmenu.md) message.</span></span>

<span data-ttu-id="44b7f-191">Sie können die Position eines Kontextmenüs angeben, indem Sie x-und y-Koordinaten zusammen mit dem **TPM \_ centeralign**, **TPM \_ leftalign** oder dem **TPM \_ RightAlign** -Flag bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-191">You can specify the position of a shortcut menu by providing x- and y-coordinates along with the **TPM\_CENTERALIGN**, **TPM\_LEFTALIGN**, or **TPM\_RIGHTALIGN** flag.</span></span> <span data-ttu-id="44b7f-192">Das-Flag gibt die Position des Kontextmenüs in Bezug auf die x-und y-Koordinaten an.</span><span class="sxs-lookup"><span data-stu-id="44b7f-192">The flag specifies the position of the shortcut menu relative to the x- and y-coordinates.</span></span>

<span data-ttu-id="44b7f-193">Sie sollten zulassen, dass der Benutzer ein Element aus einem Kontextmenü mithilfe derselben Maustaste zum Anzeigen des Menüs auswählen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-193">You should permit the user to choose an item from a shortcut menu by using the same mouse button used to display the menu.</span></span> <span data-ttu-id="44b7f-194">Geben Sie hierzu entweder **TPM \_ LeftButton** oder **TPM \_ RightButton** -Flag an, um anzugeben, welche Maustaste der Benutzer zum Auswählen eines Menü Elements verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="44b7f-194">To do this, specify either **TPM\_LEFTBUTTON** or **TPM\_RIGHTBUTTON** flag to indicate which mouse button the user can use to choose a menu item.</span></span>

-   [<span data-ttu-id="44b7f-195">Verarbeiten der WM- \_ ContextMenu-Meldung</span><span class="sxs-lookup"><span data-stu-id="44b7f-195">Processing the WM\_CONTEXTMENU Message</span></span>](/windows)
-   [<span data-ttu-id="44b7f-196">Erstellen einer Verknüpfung Font-Attributes Menü</span><span class="sxs-lookup"><span data-stu-id="44b7f-196">Creating a Shortcut Font-Attributes Menu</span></span>](#creating-a-shortcut-font-attributes-menu)
-   [<span data-ttu-id="44b7f-197">Anzeigen eines Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="44b7f-197">Displaying a Shortcut Menu</span></span>](#displaying-a-shortcut-menu)

### <a name="processing-the-wm_contextmenu-message"></a><span data-ttu-id="44b7f-198">Verarbeiten der WM- \_ ContextMenu-Meldung</span><span class="sxs-lookup"><span data-stu-id="44b7f-198">Processing the WM\_CONTEXTMENU Message</span></span>

<span data-ttu-id="44b7f-199">Die [**"WM \_ ContextMenu**](wm-contextmenu.md) "-Meldung wird generiert, wenn die Fenster Prozedur einer Anwendung die [**WM- \_ rbuttonup**](/windows/desktop/inputdev/wm-rbuttonup) -oder [**WM \_ ncrbuttonup**](/windows/desktop/inputdev/wm-ncrbuttonup) -Meldung an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt.</span><span class="sxs-lookup"><span data-stu-id="44b7f-199">The [**WM\_CONTEXTMENU**](wm-contextmenu.md) message is generated when an application's window procedure passes the [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) or [**WM\_NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) message to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="44b7f-200">Die Anwendung kann diese Nachricht verarbeiten, um ein Kontextmenü anzuzeigen, das für einen bestimmten Teil des Bildschirms geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-200">The application can process this message to display a shortcut menu appropriate to a specific portion of its screen.</span></span> <span data-ttu-id="44b7f-201">Wenn in der Anwendung kein Kontextmenü angezeigt wird, sollte die Nachricht zur Standardbehandlung an **defwindowproc** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-201">If the application does not display a shortcut menu, it should pass the message to **DefWindowProc** for default handling.</span></span>

<span data-ttu-id="44b7f-202">Im folgenden finden Sie ein Beispiel der WM-Verarbeitung von [**\_ ContextMenu**](wm-contextmenu.md) , wie Sie in der Fenster Prozedur einer Anwendung angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="44b7f-202">Following is an example of [**WM\_CONTEXTMENU**](wm-contextmenu.md) message processing as it might appear in an application's window procedure.</span></span> <span data-ttu-id="44b7f-203">Die nieder wertigen und höherwertigen Wörter des *LPARAM* -Parameters geben die Bildschirm Koordinaten der Maus an, wenn die Rechte Maustaste losgelassen wird (Beachten Sie, dass diese Koordinaten für Systeme mit mehreren Monitoren negative Werte annehmen können).</span><span class="sxs-lookup"><span data-stu-id="44b7f-203">The low-order and high-order words of the *lParam* parameter specify the screen coordinates of the mouse when the right mouse button is released (note that these coordinates can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="44b7f-204">Die von der Anwendung definierte **oncontextmenu** -Funktion gibt **true** zurück, wenn ein Kontextmenü angezeigt wird, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="44b7f-204">The application-defined **OnContextMenu** function returns **TRUE** if it displays a context menu, or **FALSE** if it does not.</span></span>


```
case WM_CONTEXTMENU: 
    if (!OnContextMenu(hwnd, GET_X_LPARAM(lParam),
              GET_Y_LPARAM(lParam))) 
        return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    break; 
```



<span data-ttu-id="44b7f-205">Die folgende Anwendungs definierte oncontextmenu-Funktion zeigt ein Kontextmenü an, wenn sich die angegebene Mausposition im Client Bereich des Fensters befindet.</span><span class="sxs-lookup"><span data-stu-id="44b7f-205">The following application-defined OnContextMenu function displays a shortcut menu if the specified mouse position is within the window's client area.</span></span> <span data-ttu-id="44b7f-206">Je nachdem, welcher Teil des Client Bereichs angegeben ist, kann eine anspruchsvollere Funktion eine von mehreren unterschiedlichen Menüs anzeigen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-206">A more sophisticated function might display one of several different menus, depending on which portion of the client area is specified.</span></span> <span data-ttu-id="44b7f-207">Um das Kontextmenü tatsächlich anzuzeigen, wird in diesem Beispiel eine Anwendungs definierte Funktion namens "displaycontextmenu" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-207">To actually display the shortcut menu, this example calls an application-defined function called DisplayContextMenu.</span></span> <span data-ttu-id="44b7f-208">Eine Beschreibung dieser Funktion finden Sie unter [Anzeigen eines Kontextmenüs](#displaying-a-shortcut-menu).</span><span class="sxs-lookup"><span data-stu-id="44b7f-208">For a description of this function, see [Displaying a Shortcut Menu](#displaying-a-shortcut-menu).</span></span>


```
BOOL WINAPI OnContextMenu(HWND hwnd, int x, int y) 
{ 
    RECT rc;                    // client area of window 
    POINT pt = { x, y };        // location of mouse click 
 
    // Get the bounding rectangle of the client area. 
 
    GetClientRect(hwnd, &rc); 
 
    // Convert the mouse position to client coordinates. 
 
    ScreenToClient(hwnd, &pt); 
 
    // If the position is in the client area, display a  
    // shortcut menu. 
 
    if (PtInRect(&rc, pt)) 
    { 
        ClientToScreen(hwnd, &pt); 
        DisplayContextMenu(hwnd, pt); 
        return TRUE; 
    } 
 
    // Return FALSE if no menu is displayed. 
 
    return FALSE; 
} 
```



### <a name="creating-a-shortcut-font-attributes-menu"></a><span data-ttu-id="44b7f-209">Erstellen einer Verknüpfung Font-Attributes Menü</span><span class="sxs-lookup"><span data-stu-id="44b7f-209">Creating a Shortcut Font-Attributes Menu</span></span>

<span data-ttu-id="44b7f-210">Das Beispiel in diesem Abschnitt enthält Teile von Code aus einer Anwendung, die ein Kontextmenü erstellt und anzeigt, das es dem Benutzer ermöglicht, Schriftarten und Schriftart Attribute festzulegen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-210">The example in this section contains portions of code from an application that creates and displays a shortcut menu that enables the user to set fonts and font attributes.</span></span> <span data-ttu-id="44b7f-211">Die Anwendung zeigt das Menü im Client Bereich des Hauptfensters an, wenn der Benutzer mit der linken Maustaste klickt.</span><span class="sxs-lookup"><span data-stu-id="44b7f-211">The application displays the menu in the client area of its main window whenever the user clicks the left mouse button.</span></span>

<span data-ttu-id="44b7f-212">Hier ist die Menüvorlage für das Kontextmenü, das in der Ressourcen Definitionsdatei der Anwendung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="44b7f-212">Here is the menu template for the shortcut menu that is provided in the application's resource-definition file.</span></span>


```
PopupMenu MENU 
BEGIN 
  POPUP "Dummy Popup" 
    BEGIN 
      POPUP "Fonts" 
        BEGIN 
          MENUITEM "Courier",     IDM_FONT_COURIER 
          MENUITEM "Times Roman", IDM_FONT_TMSRMN 
          MENUITEM "Swiss",       IDM_FONT_SWISS 
          MENUITEM "Helvetica",   IDM_FONT_HELV 
          MENUITEM "Old English", IDM_FONT_OLDENG 
        END 
      POPUP "Sizes" 
        BEGIN 
          MENUITEM "7",  IDM_SIZE_7 
          MENUITEM "8",  IDM_SIZE_8 
          MENUITEM "9",  IDM_SIZE_9 
          MENUITEM "10", IDM_SIZE_10 
          MENUITEM "11", IDM_SIZE_11 
          MENUITEM "12", IDM_SIZE_12 
          MENUITEM "14", IDM_SIZE_14 
        END 
      POPUP "Styles" 
        BEGIN 
          MENUITEM "Bold",        IDM_STYLE_BOLD 
          MENUITEM "Italic",      IDM_STYLE_ITALIC 
          MENUITEM "Strike Out",  IDM_STYLE_SO 
          MENUITEM "Superscript", IDM_STYLE_SUPER 
          MENUITEM "Subscript",   IDM_STYLE_SUB 
        END 
    END 
 
END 
```



<span data-ttu-id="44b7f-213">Im folgenden Beispiel werden die Fenster Prozedur und die unterstützenden Funktionen verwendet, mit denen das Kontextmenü erstellt und angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="44b7f-213">The following example gives the window procedure and supporting functions used to create and display the shortcut menu.</span></span>


```
LRESULT APIENTRY MenuWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    RECT rc;    // client area             
    POINT pt;   // location of mouse click  
 
    switch (uMsg) 
    { 
        case WM_LBUTTONDOWN: 
 
            // Get the bounding rectangle of the client area. 
 
            GetClientRect(hwnd, (LPRECT) &rc); 
 
            // Get the client coordinates for the mouse click.  
 
            pt.x = GET_X_LPARAM(lParam); 
            pt.y = GET_Y_LPARAM(lParam); 
 
            // If the mouse click took place inside the client 
            // area, execute the application-defined function 
            // that displays the shortcut menu. 
 
            if (PtInRect((LPRECT) &rc, pt)) 
                HandlePopupMenu(hwnd, pt); 
            break; 
        // Process other window messages.  
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
 
VOID APIENTRY HandlePopupMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // menu template          
    HMENU hmenuTrackPopup;  // shortcut menu   
 
    //  Load the menu template containing the shortcut menu from the 
    //  application's resources. 
 
    hmenu = LoadMenu(hinst, "PopupMenu"); 
    if (hmenu == NULL) 
        return; 
 
    // Get the first shortcut menu in the menu template. This is the 
    // menu that TrackPopupMenu displays. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // TrackPopup uses screen coordinates, so convert the 
    // coordinates of the mouse click to screen coordinates. 
 
    ClientToScreen(hwnd, (LPPOINT) &pt); 
 
    // Draw and track the shortcut menu.  
 
    TrackPopupMenu(hmenuTrackPopup, TPM_LEFTALIGN | TPM_LEFTBUTTON, 
        pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



### <a name="displaying-a-shortcut-menu"></a><span data-ttu-id="44b7f-214">Anzeigen eines Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="44b7f-214">Displaying a Shortcut Menu</span></span>

<span data-ttu-id="44b7f-215">Die im folgenden Beispiel gezeigte Funktion zeigt ein Kontextmenü an.</span><span class="sxs-lookup"><span data-stu-id="44b7f-215">The function shown in the following example displays a shortcut menu.</span></span>

<span data-ttu-id="44b7f-216">Die Anwendung enthält eine Menü Ressource, die durch die Zeichenfolge "shortcutexample" identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="44b7f-216">The application includes a menu resource identified by the string "ShortcutExample."</span></span> <span data-ttu-id="44b7f-217">Die Menüleiste enthält einfach einen Menünamen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-217">The menu bar simply contains a menu name.</span></span> <span data-ttu-id="44b7f-218">Die Anwendung verwendet die [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) -Funktion, um das Menü anzuzeigen, das diesem Menü Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-218">The application uses the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function to display the menu associated with this menu item.</span></span> <span data-ttu-id="44b7f-219">(Die Menüleiste selbst wird nicht angezeigt, da **TrackPopupMenu** ein Handle für ein Menü, ein Untermenü oder ein Kontextmenü erfordert.)</span><span class="sxs-lookup"><span data-stu-id="44b7f-219">(The menu bar itself is not displayed because **TrackPopupMenu** requires a handle to a menu, submenu, or shortcut menu.)</span></span>


```
VOID APIENTRY DisplayContextMenu(HWND hwnd, POINT pt) 
{ 
    HMENU hmenu;            // top-level menu 
    HMENU hmenuTrackPopup;  // shortcut menu 
 
    // Load the menu resource. 
 
    if ((hmenu = LoadMenu(hinst, "ShortcutExample")) == NULL) 
        return; 
 
    // TrackPopupMenu cannot display the menu bar so get 
    // a handle to the first shortcut menu. 
 
    hmenuTrackPopup = GetSubMenu(hmenu, 0); 
 
    // Display the shortcut menu. Track the right mouse 
    // button. 
 
    TrackPopupMenu(hmenuTrackPopup, 
            TPM_LEFTALIGN | TPM_RIGHTBUTTON, 
            pt.x, pt.y, 0, hwnd, NULL); 
 
    // Destroy the menu. 
 
    DestroyMenu(hmenu); 
} 
```



## <a name="using-menu-item-bitmaps"></a><span data-ttu-id="44b7f-220">Verwenden von Menu-Item Bitmaps</span><span class="sxs-lookup"><span data-stu-id="44b7f-220">Using Menu-Item Bitmaps</span></span>

<span data-ttu-id="44b7f-221">Das System kann eine Bitmap anstelle einer Text Zeichenfolge verwenden, um ein Menü Element anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-221">The system can use a bitmap instead of a text string to display a menu item.</span></span> <span data-ttu-id="44b7f-222">Um eine Bitmap zu verwenden, müssen Sie das **miim- \_ Bitmap** -Flag für das Menü Element festlegen und ein Handle für die Bitmap angeben, das das System für das Menü Element im **hbmpitem** -Member der [**menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="44b7f-222">To use a bitmap, you must set the **MIIM\_BITMAP** flag for the menu item and specify a handle to the bitmap that the system should display for the menu item in the **hbmpItem** member of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure.</span></span> <span data-ttu-id="44b7f-223">In diesem Abschnitt wird beschrieben, wie Bitmaps für Menü Elemente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-223">This section describes how to use bitmaps for menu items.</span></span>

-   [<span data-ttu-id="44b7f-224">Festlegen des Bitmap-Typflags</span><span class="sxs-lookup"><span data-stu-id="44b7f-224">Setting the Bitmap Type Flag</span></span>](#setting-the-bitmap-type-flag)
-   [<span data-ttu-id="44b7f-225">Erstellen der Bitmap</span><span class="sxs-lookup"><span data-stu-id="44b7f-225">Creating the Bitmap</span></span>](#creating-the-bitmap)
-   [<span data-ttu-id="44b7f-226">Hinzufügen von Linien und Diagrammen zu einem Menü</span><span class="sxs-lookup"><span data-stu-id="44b7f-226">Adding Lines and Graphs to a Menu</span></span>](#adding-lines-and-graphs-to-a-menu)
-   [<span data-ttu-id="44b7f-227">Beispiel für Menu-Item Bitmaps</span><span class="sxs-lookup"><span data-stu-id="44b7f-227">Example of Menu-Item Bitmaps</span></span>](#example-of-menu-item-bitmaps)

### <a name="setting-the-bitmap-type-flag"></a><span data-ttu-id="44b7f-228">Festlegen des Bitmap-Typflags</span><span class="sxs-lookup"><span data-stu-id="44b7f-228">Setting the Bitmap Type Flag</span></span>

<span data-ttu-id="44b7f-229">Das **miim \_ Bitmap** -oder **MF- \_ bitmapflag** weist das System an, anstelle einer Text Zeichenfolge eine Bitmap zu verwenden, um ein Menü Element anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-229">The **MIIM\_BITMAP** or **MF\_BITMAP** flag tells the system to use a bitmap rather than a text string to display a menu item.</span></span> <span data-ttu-id="44b7f-230">Das **miim \_ Bitmap** -oder MF- **\_ bitmapflag** eines Menü Elements muss zur Laufzeit festgelegt werden. es ist nicht möglich, es in der Ressourcen Definitionsdatei festzulegen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-230">A menu item's **MIIM\_BITMAP** or **MF\_BITMAP** flag must be set at run time; you cannot set it in the resource-definition file.</span></span>

<span data-ttu-id="44b7f-231">Bei neuen Anwendungen können Sie die [**setmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) -oder [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) -Funktion verwenden, um das **miim- \_ Bitmap** -Typflag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-231">For new applications, you can use the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) or [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) function to set the **MIIM\_BITMAP** type flag.</span></span> <span data-ttu-id="44b7f-232">Verwenden Sie **setmenuiteminfo**, um ein Menü Element von einem Textelement in ein bitmapelement zu ändern.</span><span class="sxs-lookup"><span data-stu-id="44b7f-232">To change a menu item from a text item to a bitmap item, use **SetMenuItemInfo**.</span></span> <span data-ttu-id="44b7f-233">Verwenden Sie die **InsertMenuItem** -Funktion, um einem Menü ein neues Bitmap-Element hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-233">To add a new bitmap item to a menu, use the **InsertMenuItem** function.</span></span>

<span data-ttu-id="44b7f-234">Anwendungen, die für frühere Versionen des Systems geschrieben wurden, können weiterhin die [**modifymenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)-, [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)-oder [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) -Funktion verwenden, um das **MF- \_ bitmapflag** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-234">Applications written for earlier versions of the system can continue to use the [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), or [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) functions to set the **MF\_BITMAP** flag.</span></span> <span data-ttu-id="44b7f-235">Wenn Sie ein Menü Element von einem Textzeichen folgen Element in ein bitmapelement ändern möchten, verwenden Sie **modifymenu**.</span><span class="sxs-lookup"><span data-stu-id="44b7f-235">To change a menu item from a text string item to a bitmap item, use **ModifyMenu**.</span></span> <span data-ttu-id="44b7f-236">Um einem Menü ein neues bitmapelement hinzuzufügen, verwenden Sie das **MF- \_ Bitmap** -Flag mit der **InsertMenu** -Funktion oder der **AppendMenu** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="44b7f-236">To add a new bitmap item to a menu, use the **MF\_BITMAP** flag with the **InsertMenu** or **AppendMenu** function.</span></span>

### <a name="creating-the-bitmap"></a><span data-ttu-id="44b7f-237">Erstellen der Bitmap</span><span class="sxs-lookup"><span data-stu-id="44b7f-237">Creating the Bitmap</span></span>

<span data-ttu-id="44b7f-238">Wenn Sie das Flag **miim \_ Bitmap** -oder **MF- \_ Bitmaptyp** für ein Menü Element festlegen, müssen Sie auch ein Handle für die Bitmap angeben, das das System für das Menü Element anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="44b7f-238">When you set the **MIIM\_BITMAP** or **MF\_BITMAP** type flag for a menu item, you must also specify a handle to the bitmap that the system should display for the menu item.</span></span> <span data-ttu-id="44b7f-239">Sie können die Bitmap als Bitmap-Ressource bereitstellen oder die Bitmap zur Laufzeit erstellen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-239">You can provide the bitmap as a bitmap resource or create the bitmap at run time.</span></span> <span data-ttu-id="44b7f-240">Wenn Sie eine Bitmap-Ressource verwenden, können Sie die [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) -Funktion verwenden, um die Bitmap zu laden und Ihr Handle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-240">If you use a bitmap resource, you can use the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function to load the bitmap and obtain its handle.</span></span>

<span data-ttu-id="44b7f-241">Um die Bitmap zur Laufzeit zu erstellen, verwenden Sie die Funktionen von Windows Graphics Device Interface (GDI).</span><span class="sxs-lookup"><span data-stu-id="44b7f-241">To create the bitmap at run time, use Windows Graphics Device Interface (GDI) functions.</span></span> <span data-ttu-id="44b7f-242">GDI bietet mehrere Möglichkeiten zum Erstellen einer Bitmap zur Laufzeit, aber Entwickler verwenden normalerweise die folgende Methode:</span><span class="sxs-lookup"><span data-stu-id="44b7f-242">GDI provides several ways to create a bitmap at run time, but developers typically use the following method:</span></span>

1.  <span data-ttu-id="44b7f-243">Verwenden Sie [**die Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) "Funktion", um einen Gerätekontext zu erstellen, der mit dem vom Hauptfenster der Anwendung verwendeten Gerätekontext kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-243">Use the [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) function to create a device context compatible with the device context used by the application's main window.</span></span>
2.  <span data-ttu-id="44b7f-244">Verwenden Sie [**die Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) "-Funktion", um eine Bitmap zu erstellen, die mit dem Hauptfenster der Anwendung kompatibel ist, oder verwenden [**Sie die Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) "die Funktion", um eine monochrome Bitmap zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-244">Use the [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) function to create a bitmap compatible with the application's main window or use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) function to create a monochrome bitmap.</span></span>
3.  <span data-ttu-id="44b7f-245">Verwenden Sie die [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) -Funktion, um die Bitmap in den kompatiblen Gerätekontext auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-245">Use the [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) function to select the bitmap into the compatible device context.</span></span>
4.  <span data-ttu-id="44b7f-246">Verwenden Sie GDI-Zeichnungsfunktionen, z. b. [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) und [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), um ein Bild in die Bitmap zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-246">Use GDI drawing functions, such as [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) and [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), to draw an image into the bitmap.</span></span>

<span data-ttu-id="44b7f-247">Weitere Informationen finden Sie unter [Bitmaps](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="44b7f-247">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

### <a name="adding-lines-and-graphs-to-a-menu"></a><span data-ttu-id="44b7f-248">Hinzufügen von Linien und Diagrammen zu einem Menü</span><span class="sxs-lookup"><span data-stu-id="44b7f-248">Adding Lines and Graphs to a Menu</span></span>

<span data-ttu-id="44b7f-249">Im folgenden Codebeispiel wird gezeigt, wie ein Menü erstellt wird, das Menü Element Bitmaps enthält.</span><span class="sxs-lookup"><span data-stu-id="44b7f-249">The following code sample shows how to create a menu that contains menu-item bitmaps.</span></span> <span data-ttu-id="44b7f-250">Es werden zwei Menüs erstellt.</span><span class="sxs-lookup"><span data-stu-id="44b7f-250">It creates two menus.</span></span> <span data-ttu-id="44b7f-251">Das erste ist ein Diagramm Menü, das drei Menü Element Bitmaps enthält: ein Kreis Diagramm, ein Liniendiagramm und ein Balkendiagramm.</span><span class="sxs-lookup"><span data-stu-id="44b7f-251">The first is a Chart menu that contains three menu-item bitmaps: a pie chart, a line chart, and a bar chart.</span></span> <span data-ttu-id="44b7f-252">Im Beispiel wird veranschaulicht, wie diese Bitmaps aus der Ressourcen Datei der Anwendung geladen werden, und anschließend werden die Menü-und Menü Elemente mithilfe der Funktionen " [**anatepopupmenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) " und " [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) " erstellt.</span><span class="sxs-lookup"><span data-stu-id="44b7f-252">The example demonstrates how to load these bitmaps from the application's resource file, and then use the [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) and [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) functions to create the menu and menu items.</span></span>

<span data-ttu-id="44b7f-253">Das zweite Menü ist ein Zeilen Menü.</span><span class="sxs-lookup"><span data-stu-id="44b7f-253">The second menu is a Lines menu.</span></span> <span data-ttu-id="44b7f-254">Sie enthält Bitmaps, die die vom vordefinierten Stift im System bereitgestellten Linienstile darstellen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-254">It contains bitmaps showing the line styles provided by the predefined pen in the system.</span></span> <span data-ttu-id="44b7f-255">Die zeilenweise Bitmaps werden zur Laufzeit mithilfe von GDI-Funktionen erstellt.</span><span class="sxs-lookup"><span data-stu-id="44b7f-255">The line-style bitmaps are created at run time by using GDI functions.</span></span>

<span data-ttu-id="44b7f-256">Im folgenden finden Sie die Definitionen der Bitmapressourcen in der Ressourcen Definitionsdatei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="44b7f-256">Here are the definitions of the bitmap resources in the application's resource-definition file.</span></span>


```
PIE BITMAP pie.bmp 
LINE BITMAP line.bmp 
BAR BITMAP bar.bmp 
 
```



<span data-ttu-id="44b7f-257">Im folgenden finden Sie die relevanten Teile der Header Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="44b7f-257">Here are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers 
 
#define IDM_SOLID       PS_SOLID 
#define IDM_DASH        PS_DASH 
#define IDM_DASHDOT     PS_DASHDOT 
#define IDM_DASHDOTDOT  PS_DASHDOTDOT 
 
#define IDM_PIE  1 
#define IDM_LINE 2 
#define IDM_BAR  3 
 
// Line-type flags  
 
#define SOLID       0 
#define DOT         1 
#define DASH        2 
#define DASHDOT     3 
#define DASHDOTDOT  4 
 
// Count of pens  
 
#define CPENS 5 
 
// Chart-type flags  
 
#define PIE  1 
#define LINE 2 
#define BAR  3 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
VOID MakeChartMenu(HWND); 
VOID MakeLineMenu(HWND, HPEN, HBITMAP); 
```



<span data-ttu-id="44b7f-258">Im folgenden Beispiel wird gezeigt, wie Menüs und Menü Element Bitmaps in einer Anwendung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-258">The following example shows how menus and menu-item bitmaps are created in an application.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HPEN hpen[CPENS]; 
    static HBITMAP hbmp[CPENS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Create the Chart and Line menus.  
 
            MakeChartMenu(hwnd); 
            MakeLineMenu(hwnd, hpen, hbmp); 
            return 0; 
 
        // Process other window messages. 
 
        case WM_DESTROY: 
 
            for (i = 0; i < CPENS; i++) 
            { 
                DeleteObject(hbmp[i]); 
                DeleteObject(hpen[i]); 
            } 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
VOID MakeChartMenu(HWND hwnd) 
{ 
    HBITMAP hbmpPie;    // handle to pie chart bitmap   
    HBITMAP hbmpLine;   // handle to line chart bitmap  
    HBITMAP hbmpBar;    // handle to bar chart bitmap   
    HMENU hmenuMain;    // handle to main menu          
    HMENU hmenuChart;   // handle to Chart menu  
 
    // Load the pie, line, and bar chart bitmaps from the 
    // resource-definition file. 
 
    hbmpPie = LoadBitmap(hinst, MAKEINTRESOURCE(PIE)); 
    hbmpLine = LoadBitmap(hinst, MAKEINTRESOURCE(LINE)); 
    hbmpBar = LoadBitmap(hinst, MAKEINTRESOURCE(BAR)); 
 
    // Create the Chart menu and add it to the menu bar. 
    // Append the Pie, Line, and Bar menu items to the Chart 
    // menu. 
 
    hmenuMain = GetMenu(hwnd); 
    hmenuChart = CreatePopupMenu(); 
    AppendMenu(hmenuMain, MF_STRING | MF_POPUP, (UINT) hmenuChart, 
        "Chart"); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_PIE, (LPCTSTR) hbmpPie); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_LINE, 
        (LPCTSTR) hbmpLine); 
    AppendMenu(hmenuChart, MF_BITMAP, IDM_BAR, (LPCTSTR) hbmpBar); 
 
    return; 
} 
 
VOID MakeLineMenu(HWND hwnd, HPEN phpen, HBITMAP phbmp) 
{ 
    HMENU hmenuLines;       // handle to Lines menu      
    HMENU hmenu;            // handle to main menu              
    COLORREF crMenuClr;     // menu-item background color       
    HBRUSH hbrBackground;   // handle to background brush       
    HBRUSH hbrOld;          // handle to previous brush         
    WORD wLineX;            // width of line bitmaps            
    WORD wLineY;            // height of line bitmaps           
    HDC hdcMain;            // handle to main window's DC       
    HDC hdcLines;           // handle to compatible DC          
    HBITMAP hbmpOld;        // handle to previous bitmap        
    int i;                  // loop counter                     
 
    // Create the Lines menu. Add it to the menu bar.  
 
    hmenu = GetMenu(hwnd); 
    hmenuLines = CreatePopupMenu(); 
    AppendMenu(hmenu, MF_STRING | MF_POPUP, 
        (UINT) hmenuLines, "&Lines"); 
 
    // Create a brush for the menu-item background color.  
 
    crMenuClr = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crMenuClr); 
 
    // Create a compatible device context for the line bitmaps, 
    // and then select the background brush into it. 
 
    hdcMain = GetDC(hwnd); 
    hdcLines = CreateCompatibleDC(hdcMain); 
    hbrOld = SelectObject(hdcLines, hbrBackground); 
 
    // Get the dimensions of the check-mark bitmap. The width of 
    // the line bitmaps will be five times the width of the 
    // check-mark bitmap. 
 
    wLineX = GetSystemMetrics(SM_CXMENUCHECK) * (WORD) 5; 
    wLineY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    // Create the bitmaps and select them, one at a time, into the 
    // compatible device context. Initialize each bitmap by 
    // filling it with the menu-item background color. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        phbmp[i] = CreateCompatibleBitmap(hdcMain, wLineX, wLineY); 
        if (i == 0) 
            hbmpOld = SelectObject(hdcLines, phbmp[i]); 
        else 
            SelectObject(hdcLines, phbmp[i]); 
        ExtFloodFill(hdcLines, 0, 0, crMenuClr, FLOODFILLBORDER); 
    } 
 
    // Create the pens.  
 
    phpen[0] = CreatePen(PS_SOLID, 1, RGB(0, 0, 0)); 
    phpen[1] = CreatePen(PS_DOT, 1, RGB(0, 0, 0)); 
    phpen[2] = CreatePen(PS_DASH, 1, RGB(0, 0, 0)); 
    phpen[3] = CreatePen(PS_DASHDOT, 1, RGB(0, 0, 0)); 
    phpen[4] = CreatePen(PS_DASHDOTDOT, 1, RGB(0, 0, 0)); 
 
    // Select a pen and a bitmap into the compatible device 
    // context, draw a line into the bitmap, and then append 
    // the bitmap as an item in the Lines menu. 
 
    for (i = 0; i < CPENS; i++) 
    { 
        SelectObject(hdcLines, phbmp[i]); 
        SelectObject(hdcLines, phpen[i]); 
        MoveToEx(hdcLines, 0, wLineY / 2, NULL); 
        LineTo(hdcLines, wLineX, wLineY / 2); 
        AppendMenu(hmenuLines, MF_BITMAP, i + 1, 
            (LPCTSTR) phbmp[i]); 
    } 
 
    // Release the main window's device context and destroy the 
    // compatible device context. Also, destroy the background 
    // brush. 
 
    ReleaseDC(hwnd, hdcMain); 
    SelectObject(hdcLines, hbrOld); 
    DeleteObject(hbrBackground); 
    SelectObject(hdcLines, hbmpOld); 
    DeleteDC(hdcLines); 
 
    return; 
} 
```



### <a name="example-of-menu-item-bitmaps"></a><span data-ttu-id="44b7f-259">Beispiel für Menu-Item Bitmaps</span><span class="sxs-lookup"><span data-stu-id="44b7f-259">Example of Menu-Item Bitmaps</span></span>

<span data-ttu-id="44b7f-260">Im Beispiel in diesem Thema werden zwei Menüs erstellt, die jeweils mehrere Bitmap-Menü Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="44b7f-260">The example in this topic creates two menus, each containing several bitmap menu items.</span></span> <span data-ttu-id="44b7f-261">Die Anwendung fügt der Menüleiste des Hauptfensters für jedes Menü einen entsprechenden Menünamen hinzu.</span><span class="sxs-lookup"><span data-stu-id="44b7f-261">For each menu, the application adds a corresponding menu name to the main window's menu bar.</span></span>

<span data-ttu-id="44b7f-262">Das erste Menü enthält Menü Elemente, die jeden der drei Diagrammtypen anzeigen: Kreis, Linie und Balken.</span><span class="sxs-lookup"><span data-stu-id="44b7f-262">The first menu contains menu items showing each of three chart types: pie, line, and bar.</span></span> <span data-ttu-id="44b7f-263">Die Bitmaps für diese Menü Elemente werden als Ressourcen definiert und mithilfe der [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) -Funktion geladen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-263">The bitmaps for these menu items are defined as resources and are loaded by using the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function.</span></span> <span data-ttu-id="44b7f-264">Diesem Menü ist der Menü Name "Diagramm" in der Menüleiste zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="44b7f-264">Associated with this menu is a "Chart" menu name on the menu bar.</span></span>

<span data-ttu-id="44b7f-265">Das zweite Menü enthält Menü Elemente, die jeden der fünf Zeilen Formate mit der Funktion " [**kreatepen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) " angezeigt werden: **PS \_ Solid**, **PS \_ Dash**, **PS- \_ Punkt**, **PS- \_ DashDot** und **PS- \_ DashDotDot**.</span><span class="sxs-lookup"><span data-stu-id="44b7f-265">The second menu contains menu items showing each of the five line styles used with the [**CreatePen**](/windows/desktop/api/wingdi/nf-wingdi-createpen) function: **PS\_SOLID**, **PS\_DASH**, **PS\_DOT**, **PS\_DASHDOT**, and **PS\_DASHDOTDOT**.</span></span> <span data-ttu-id="44b7f-266">Die Anwendung erstellt die Bitmaps für diese Menü Elemente zur Laufzeit mithilfe von GDI-Zeichnungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-266">The application creates the bitmaps for these menu items at run time using GDI drawing functions.</span></span> <span data-ttu-id="44b7f-267">Diesem Menü ist ein **Zeilen** Menü Name in der Menüleiste zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="44b7f-267">Associated with this menu is a **Lines** menu name on the menu bar.</span></span>

<span data-ttu-id="44b7f-268">In der Fenster Prozedur der Anwendung sind zwei statische Arrays von bitmaphandles definiert.</span><span class="sxs-lookup"><span data-stu-id="44b7f-268">Defined in the application's window procedure are two static arrays of bitmap handles.</span></span> <span data-ttu-id="44b7f-269">Ein Array enthält die Handles der drei Bitmaps, die für das **Diagramm** Menü verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-269">One array contains the handles of the three bitmaps used for the **Chart** menu.</span></span> <span data-ttu-id="44b7f-270">Der andere enthält die Handles der fünf Bitmaps, die für das Menü " **Linien** " verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-270">The other contains the handles of the five bitmaps used for the **Lines** menu.</span></span> <span data-ttu-id="44b7f-271">Bei der Verarbeitung der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht lädt die Fenster Prozedur die Diagramm Bitmaps, erstellt die Zeilen Bitmaps und fügt dann die entsprechenden Menü Elemente hinzu.</span><span class="sxs-lookup"><span data-stu-id="44b7f-271">When processing the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, the window procedure loads the chart bitmaps, creates the line bitmaps, and then adds the corresponding menu items.</span></span> <span data-ttu-id="44b7f-272">Bei der Verarbeitung [**der \_ WM**](/windows/desktop/winmsg/wm-destroy) -Lösch Nachricht löscht die Fenster Prozedur alle Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="44b7f-272">When processing the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, the window procedure deletes all of the bitmaps.</span></span>

<span data-ttu-id="44b7f-273">Im folgenden finden Sie die relevanten Teile der Header Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="44b7f-273">Following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers 
 
#define IDM_PIE         1 
#define IDM_LINE        2 
#define IDM_BAR         3 
 
#define IDM_SOLID       4 
#define IDM_DASH        5 
#define IDM_DASHDOT     6 
#define IDM_DASHDOTDOT  7 
 
// Number of items on the Chart and Lines menus 
 
#define C_LINES         5 
#define C_CHARTS        3 
 
// Bitmap resource identifiers 
 
#define IDB_PIE         1 
#define IDB_LINE        2 
#define IDB_BAR         3 
 
// Dimensions of the line bitmaps 
 
#define CX_LINEBMP      40 
#define CY_LINEBMP      10 
```



<span data-ttu-id="44b7f-274">Im folgenden sind die relevanten Teile der Fenster Prozedur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="44b7f-274">Following are the relevant portions of the window procedure.</span></span> <span data-ttu-id="44b7f-275">Die Fenster Prozedur führt den größten Teil ihrer Initialisierung durch Aufrufen der Anwendungs definierten loadchartbitmaps-, createlinebitmaps-und addbitmapmenu-Funktionen aus, die weiter unten in diesem Thema beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-275">The window procedure performs most of its initialization by calling the application-defined LoadChartBitmaps, CreateLineBitmaps, and AddBitmapMenu functions, described later in this topic.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    static HBITMAP aHbmLines[C_LINES]; 
    static HBITMAP aHbmChart[C_CHARTS]; 
    int i; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
             // Call application-defined functions to load the 
             // bitmaps for the Chart menu and create those for 
             // the Lines menu. 
 
            LoadChartBitmaps(aHbmChart); 
            CreateLineBitmaps(aHbmLines); 
 
             // Call an application-defined function to create 
             // menus containing the bitmap menu items. The function 
             // also adds a menu name to the window's menu bar. 
 
            AddBitmapMenu( 
                    hwnd,      // menu bar's owner window 
                    "&Chart",  // text of menu name on menu bar 
                    IDM_PIE,   // ID of first item on menu 
                    aHbmChart, // array of bitmap handles 
                    C_CHARTS   // number of items on menu 
                    ); 
            AddBitmapMenu(hwnd, "&Lines", IDM_SOLID, 
                    aHbmLines, C_LINES); 
            break; 
 
        case WM_DESTROY: 
            for (i = 0; i < C_LINES; i++) 
                DeleteObject(aHbmLines[i]); 
            for (i = 0; i < C_CHARTS; i++) 
                DeleteObject(aHbmChart[i]); 
            PostQuitMessage(0); 
            break; 
 
        // Process additional messages here. 
 
        default: 
            return (DefWindowProc(hwnd, uMsg, wParam, lParam)); 
    } 
    return 0; 
} 
```



<span data-ttu-id="44b7f-276">Die Anwendungs definierte loadchartbitmaps-Funktion lädt die Bitmapressourcen für das Diagramm Menü, indem die [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) -Funktion wie folgt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="44b7f-276">The application-defined LoadChartBitmaps function loads the bitmap resources for the chart menu by calling the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function, as follows.</span></span>


```
VOID WINAPI LoadChartBitmaps(HBITMAP *paHbm) 
{ 
    paHbm[0] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_PIE)); 
    paHbm[1] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_LINE)); 
    paHbm[2] = LoadBitmap(g_hinst, MAKEINTRESOURCE(IDB_BAR)); 
} 
```



<span data-ttu-id="44b7f-277">Die von der Anwendung definierte Funktion "-Funktion" erstellt die Bitmaps für das Menü "Zeilen" mithilfe von GDI-Zeichnungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-277">The application-defined CreateLineBitmaps function creates the bitmaps for the Lines menu by using GDI drawing functions.</span></span> <span data-ttu-id="44b7f-278">Die-Funktion erstellt einen Arbeitsspeicher-Gerätekontext (DC) mit denselben Eigenschaften wie der DC des Desktop Fensters.</span><span class="sxs-lookup"><span data-stu-id="44b7f-278">The function creates a memory device context (DC) with the same properties as the desktop window's DC.</span></span> <span data-ttu-id="44b7f-279">Für jede Linienart erstellt die Funktion eine Bitmap, wählt Sie in den Speicher-DC aus und zeichnet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="44b7f-279">For each line style, the function creates a bitmap, selects it into the memory DC, and draws in it.</span></span>


```
VOID WINAPI CreateLineBitmaps(HBITMAP *paHbm) 
{ 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
    COLORREF clrMenu = GetSysColor(COLOR_MENU); 
    HBRUSH hbrOld; 
    HPEN hpenOld; 
    HBITMAP hbmOld; 
    int fnDrawMode; 
    int i; 
 
     // Create a brush using the menu background color, 
     // and select it into the memory DC. 
 
    hbrOld = SelectObject(hdcMem, CreateSolidBrush(clrMenu)); 
 
     // Create the bitmaps. Select each one into the memory 
     // DC that was created and draw in it. 
 
    for (i = 0; i < C_LINES; i++) 
    { 
        // Create the bitmap and select it into the DC. 
 
        paHbm[i] = CreateCompatibleBitmap(hdcDesktop, 
                CX_LINEBMP, CY_LINEBMP); 
        hbmOld = SelectObject(hdcMem, paHbm[i]); 
 
        // Fill the background using the brush. 
 
        PatBlt(hdcMem, 0, 0, CX_LINEBMP, CY_LINEBMP, PATCOPY); 
 
        // Create the pen and select it into the DC. 
 
        hpenOld = SelectObject(hdcMem, 
                CreatePen(PS_SOLID + i, 1, RGB(0, 0, 0))); 
 
         // Draw the line. To preserve the background color where 
         // the pen is white, use the R2_MASKPEN drawing mode. 
 
        fnDrawMode = SetROP2(hdcMem, R2_MASKPEN); 
        MoveToEx(hdcMem, 0, CY_LINEBMP / 2, NULL); 
        LineTo(hdcMem, CX_LINEBMP, CY_LINEBMP / 2); 
        SetROP2(hdcMem, fnDrawMode); 
 
        // Delete the pen, and select the old pen and bitmap. 
 
        DeleteObject(SelectObject(hdcMem, hpenOld)); 
        SelectObject(hdcMem, hbmOld); 
    } 
 
    // Delete the brush and select the original brush. 
 
    DeleteObject(SelectObject(hdcMem, hbrOld)); 
 
    // Delete the memory DC and release the desktop DC. 
 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
} 
```



<span data-ttu-id="44b7f-280">Die Anwendungs definierte addbitmapmenu-Funktion erstellt ein Menü und fügt dieser die angegebene Anzahl von Bitmap-Menü Elementen hinzu.</span><span class="sxs-lookup"><span data-stu-id="44b7f-280">The application-defined AddBitmapMenu function creates a menu and adds the specified number of bitmap menu items to it.</span></span> <span data-ttu-id="44b7f-281">Anschließend wird der Menüleiste des angegebenen Fensters ein entsprechender Menü Name hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="44b7f-281">Then it adds a corresponding menu name to the specified window's menu bar.</span></span>


```
VOID WINAPI AddBitmapMenu( 
        HWND hwnd,          // window that owned the menu bar 
        LPSTR lpszText,     // text of menu name on menu bar 
        UINT uID,           // ID of first bitmap menu item 
        HBITMAP *paHbm,     // bitmaps for the menu items 
        int cItems)         // number bitmap menu items 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup = CreatePopupMenu(); 
    MENUITEMINFO mii; 
    int i; 
 
    // Add the bitmap menu items to the menu. 
 
    for (i = 0; i < cItems; i++) 
    { 
        mii.fMask = MIIM_ID | MIIM_BITMAP | MIIM_DATA; 
        mii.wID = uID + i; 
        mii.hbmpItem = &paHbm[i]; 
        InsertMenuItem(hmenuPopup, i, TRUE, &mii); 
    } 
 
    // Add a menu name to the menu bar. 
 
    mii.fMask = MIIM_STRING | MIIM_DATA | MIIM_SUBMENU; 
    mii.fType = MFT_STRING; 
    mii.hSubMenu = hmenuPopup; 
    mii.dwTypeData = lpszText; 
    InsertMenuItem(hmenuBar, 
        GetMenuItemCount(hmenuBar), TRUE, &mii); 
} 
```



## <a name="creating-owner-drawn-menu-items"></a><span data-ttu-id="44b7f-282">Erstellen von Owner-Drawn Menü Elementen</span><span class="sxs-lookup"><span data-stu-id="44b7f-282">Creating Owner-Drawn Menu Items</span></span>

<span data-ttu-id="44b7f-283">Wenn Sie die gesamte Kontrolle über die Darstellung eines Menü Elements benötigen, können Sie ein von einem Besitzer gezeichnetes Menü Element in der Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-283">If you need complete control over the appearance of a menu item, you can use an owner-drawn menu item in your application.</span></span> <span data-ttu-id="44b7f-284">In diesem Abschnitt werden die Schritte beschrieben, die zum Erstellen und Verwenden eines von einem Besitzer gezeichneten Menü Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="44b7f-284">This section describes the steps involved in creating and using an owner-drawn menu item.</span></span>

-   [<span data-ttu-id="44b7f-285">Festlegen des Owner-Drawn Flags</span><span class="sxs-lookup"><span data-stu-id="44b7f-285">Setting the Owner-Drawn Flag</span></span>](#setting-the-owner-drawn-flag)
-   [<span data-ttu-id="44b7f-286">Vom Besitzer gezeichnete Menüs und die WM- \_ MeasureItem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="44b7f-286">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>](/windows)
-   [<span data-ttu-id="44b7f-287">Von einem Besitzer gezeichnete Menüs und die WM- \_ DrawItem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="44b7f-287">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>](/windows)
-   [<span data-ttu-id="44b7f-288">Von einem Besitzer gezeichnete Menüs und die WM- \_ menuchar-Meldung</span><span class="sxs-lookup"><span data-stu-id="44b7f-288">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>](/windows)
-   [<span data-ttu-id="44b7f-289">Festlegen von Schriftarten für Menu-Item Text Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="44b7f-289">Setting Fonts for Menu-Item Text Strings</span></span>](#setting-fonts-for-menu-item-text-strings)
-   [<span data-ttu-id="44b7f-290">Beispiel für Owner-Drawn Menü Elemente</span><span class="sxs-lookup"><span data-stu-id="44b7f-290">Example of Owner-Drawn Menu Items</span></span>](#example-of-owner-drawn-menu-items)

### <a name="setting-the-owner-drawn-flag"></a><span data-ttu-id="44b7f-291">Festlegen des Owner-Drawn Flags</span><span class="sxs-lookup"><span data-stu-id="44b7f-291">Setting the Owner-Drawn Flag</span></span>

<span data-ttu-id="44b7f-292">Sie können kein vom Besitzer gezeichnetes Menü Element in der Ressourcen Definitionsdatei Ihrer Anwendung definieren.</span><span class="sxs-lookup"><span data-stu-id="44b7f-292">You cannot define an owner-drawn menu item in your application's resource-definition file.</span></span> <span data-ttu-id="44b7f-293">Stattdessen müssen Sie ein neues Menü Element erstellen oder ein vorhandenes Menü Element ändern, indem Sie das MFT-Menü Kennzeichen für Besitzer **\_ Zeichnen** verwenden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-293">Instead, you must create a new menu item or modify an existing one by using the **MFT\_OWNERDRAW** menu flag.</span></span>

<span data-ttu-id="44b7f-294">Mit der [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) -oder der [**setmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) -Funktion können Sie ein vom Besitzer gezeichnetes Menü Element angeben.</span><span class="sxs-lookup"><span data-stu-id="44b7f-294">You can use the [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) or [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function to specify an owner-drawn menu item.</span></span> <span data-ttu-id="44b7f-295">Verwenden Sie **InsertMenuItem** , um ein neues Menü Element an der angegebenen Position in einer Menüleiste oder einem Menü einzufügen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-295">Use **InsertMenuItem** to insert a new menu item at the specified position in a menu bar or menu.</span></span> <span data-ttu-id="44b7f-296">Verwenden Sie **setmenuiteminfo** , um den Inhalt eines Menüs zu ändern.</span><span class="sxs-lookup"><span data-stu-id="44b7f-296">Use **SetMenuItemInfo** to change the contents of a menu.</span></span>

<span data-ttu-id="44b7f-297">Wenn Sie diese beiden Funktionen aufrufen, müssen Sie einen Zeiger auf eine [**menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur angeben, die die Eigenschaften des neuen Menü Elements oder die Eigenschaften angibt, die Sie für ein vorhandenes Menü Element ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="44b7f-297">When calling these two functions, you must specify a pointer to a [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure, which specifies the properties of the new menu item or the properties you want to change for an existing menu item.</span></span> <span data-ttu-id="44b7f-298">Um ein Element als vom Besitzer gezeichnetes Element festzulegen, geben Sie den **miim \_ ftype** -Wert für das **fmask** -Element und den **MFT-Besitzer \_ Zeichnungs** Wert für das **ftype** -Element an.</span><span class="sxs-lookup"><span data-stu-id="44b7f-298">To make an item an owner-drawn item, specify the **MIIM\_FTYPE** value for the **fMask** member and the **MFT\_OWNERDRAW** value for the **fType** member.</span></span>

<span data-ttu-id="44b7f-299">Durch Festlegen der entsprechenden Member der [**menuiteminfo**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) -Struktur können Sie jedem Menü Element einen Anwendungs definierten Wert, der als **Elementdaten** bezeichnet wird, zuordnen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-299">By setting the appropriate members of the [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) structure, you can associate an application-defined value, which is called **item data**, with each menu item.</span></span> <span data-ttu-id="44b7f-300">Geben Sie hierzu den **miim- \_ Datenwert** für das **fmask** -Element und den von der Anwendung definierten Wert für das **dwitemdata** -Element an.</span><span class="sxs-lookup"><span data-stu-id="44b7f-300">To do so, specify the **MIIM\_DATA** value for the **fMask** member and the application-defined value for the **dwItemData** member.</span></span>

<span data-ttu-id="44b7f-301">Sie können Elementdaten mit jedem beliebigen Menü Elementtyp verwenden, aber dies ist besonders nützlich für Elemente, die vom Besitzer gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-301">You can use item data with any type of menu item, but it is particularly useful for owner-drawn items.</span></span> <span data-ttu-id="44b7f-302">Angenommen, eine-Struktur enthält Informationen, die zum Zeichnen eines Menü Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-302">For example, suppose a structure contains information used to draw a menu item.</span></span> <span data-ttu-id="44b7f-303">Eine Anwendung kann die Elementdaten für ein Menü Element verwenden, um einen Zeiger auf die Struktur zu speichern.</span><span class="sxs-lookup"><span data-stu-id="44b7f-303">An application might use the item data for a menu item to store a pointer to the structure.</span></span> <span data-ttu-id="44b7f-304">Die Elementdaten werden mit den Nachrichten " [**WM \_ MeasureItem**](../controls/wm-measureitem.md) " und " [**WM \_ DrawItem**](../controls/wm-drawitem.md) " an das Besitzer Fenster des Menüs gesendet.</span><span class="sxs-lookup"><span data-stu-id="44b7f-304">The item data is sent to the menu's owner window with the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) and [**WM\_DRAWITEM**](../controls/wm-drawitem.md) messages.</span></span> <span data-ttu-id="44b7f-305">Um die Elementdaten für ein Menü zu einem beliebigen Zeitpunkt abzurufen, verwenden Sie die [**getmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="44b7f-305">To retrieve the item data for a menu at any time, use the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function.</span></span>

<span data-ttu-id="44b7f-306">Anwendungen, die für frühere Versionen des Systems geschrieben wurden, können weiterhin [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)oder [**modifymenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) aufrufen, um das MF-Besitzer **\_ Zeichnungs** Flag einem von einem Besitzer gezeichneten Menü Element zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-306">Applications written for earlier versions of the system can continue to call [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), or [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) to assign the **MF\_OWNERDRAW** flag to an owner-drawn menu item.</span></span>

<span data-ttu-id="44b7f-307">Wenn Sie eine dieser drei Funktionen aufrufen, können Sie einen Wert als *lpnetwitem* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="44b7f-307">When you call any of these three functions, you can pass a value as the *lpNewItem* parameter.</span></span> <span data-ttu-id="44b7f-308">Dieser Wert kann alle Informationen darstellen, die für Ihre Anwendung von Bedeutung sind, und die der Anwendung zur Verfügung stehen, wenn das Element angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="44b7f-308">This value can represent any information that is meaningful to your application, and that will be available to your application when the item is to be displayed.</span></span> <span data-ttu-id="44b7f-309">Der Wert kann z. b. einen Zeiger auf eine-Struktur enthalten. die-Struktur kann wiederum eine Text Zeichenfolge und ein Handle für die logische Schriftart enthalten, die Ihre Anwendung zum Zeichnen der Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="44b7f-309">For example, the value could contain a pointer to a structure; the structure, in turn, might contain a text string and a handle to the logical font your application will use to draw the string.</span></span>

### <a name="owner-drawn-menus-and-the-wm_measureitem-message"></a><span data-ttu-id="44b7f-310">Owner-Drawn Menüs und die "WM \_ MeasureItem"-Meldung</span><span class="sxs-lookup"><span data-stu-id="44b7f-310">Owner-Drawn Menus and the WM\_MEASUREITEM Message</span></span>

<span data-ttu-id="44b7f-311">Bevor das System zum ersten Mal ein vom Besitzer gezeichnetes Menü Element anzeigt, sendet es die " [**WM \_ MeasureItem**](../controls/wm-measureitem.md) "-Meldung an die Fenster Prozedur des Fensters, das das Menü des Elements besitzt.</span><span class="sxs-lookup"><span data-stu-id="44b7f-311">Before the system displays an owner-drawn menu item for the first time, it sends the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message to the window procedure of the window that owns the item's menu.</span></span> <span data-ttu-id="44b7f-312">Diese Meldung enthält einen Zeiger auf eine [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur, die das Element identifiziert und die Elementdaten enthält, die einer Anwendung möglicherweise zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-312">This message contains a pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that identifies the item and contains the item data that an application may have assigned to it.</span></span> <span data-ttu-id="44b7f-313">Die Fenster Prozedur muss die Elemente **ItemWidth** und **ItemHeight** der Struktur ausfüllen, bevor Sie von der Verarbeitung der Nachricht zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="44b7f-313">The window procedure must fill the **itemWidth** and **itemHeight** members of the structure before returning from processing the message.</span></span> <span data-ttu-id="44b7f-314">Das System verwendet die Informationen in diesen Membern beim Erstellen des umgebenden Rechtecks, in dem eine Anwendung das Menü Element zeichnet.</span><span class="sxs-lookup"><span data-stu-id="44b7f-314">The system uses the information in these members when creating the bounding rectangle in which an application draws the menu item.</span></span> <span data-ttu-id="44b7f-315">Außerdem werden die Informationen verwendet, um zu erkennen, wann der Benutzer das Element auswählt.</span><span class="sxs-lookup"><span data-stu-id="44b7f-315">It also uses the information to detect when the user chooses the item.</span></span>

### <a name="owner-drawn-menus-and-the-wm_drawitem-message"></a><span data-ttu-id="44b7f-316">Owner-Drawn Menüs und die WM- \_ DrawItem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="44b7f-316">Owner-Drawn Menus and the WM\_DRAWITEM Message</span></span>

<span data-ttu-id="44b7f-317">Wenn das Element gezeichnet werden muss (z. b. wenn es zum ersten Mal angezeigt wird oder wenn der Benutzer es auswählt), sendet das System die [**WM \_ DrawItem**](../controls/wm-drawitem.md) -Nachricht an die Fenster Prozedur des Besitzer Fensters des Menüs.</span><span class="sxs-lookup"><span data-stu-id="44b7f-317">Whenever the item must be drawn (for example, when it is first displayed or when the user selects it), the system sends the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message to the window procedure of the menu's owner window.</span></span> <span data-ttu-id="44b7f-318">Diese Meldung enthält einen Zeiger auf eine [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur, die Informationen über das Element enthält, einschließlich der Elementdaten, die einer Anwendung möglicherweise zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-318">This message contains a pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure, which contains information about the item, including the item data that an application may have assigned to it.</span></span> <span data-ttu-id="44b7f-319">Außerdem enthält **drawitemstruct** Flags, die den Zustand des Elements angeben (z. b. ob es abgeblendet oder ausgewählt ist), sowie ein umgebenden Rechteck und einen Gerätekontext, den die Anwendung zum Zeichnen des Elements verwendet.</span><span class="sxs-lookup"><span data-stu-id="44b7f-319">In addition, **DRAWITEMSTRUCT** contains flags that indicate the state of the item (such as whether it is grayed or selected) as well as a bounding rectangle and a device context that the application uses to draw the item.</span></span>

<span data-ttu-id="44b7f-320">Eine Anwendung muss beim Verarbeiten der [**WM- \_ DrawItem**](../controls/wm-drawitem.md) -Nachricht folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="44b7f-320">An application must do the following while processing the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message:</span></span>

-   <span data-ttu-id="44b7f-321">Bestimmen Sie den Typ der Zeichnung, der erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-321">Determine the type of drawing that is necessary.</span></span> <span data-ttu-id="44b7f-322">Überprüfen Sie hierzu den **itemaction** -Member der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="44b7f-322">To do so, check the **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span>
-   <span data-ttu-id="44b7f-323">Zeichnen Sie das Menü Element entsprechend, indem Sie das umgebende Rechteck und den Gerätekontext verwenden, die aus der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-323">Draw the menu item appropriately, using the bounding rectangle and device context obtained from the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span> <span data-ttu-id="44b7f-324">Die Anwendung muss nur innerhalb des umgebenden Rechtecks gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-324">The application must draw only within the bounding rectangle.</span></span> <span data-ttu-id="44b7f-325">Aus Leistungsgründen gibt das System keine Teile des Bilds aus, die außerhalb des Rechtecks gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-325">For performance reasons, the system does not clip portions of the image that are drawn outside the rectangle.</span></span>
-   <span data-ttu-id="44b7f-326">Stellt alle GDI-Objekte wieder her, die für den Gerätekontext des Menü Elements ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-326">Restore all GDI objects selected for the menu item's device context.</span></span>

<span data-ttu-id="44b7f-327">Wenn der Benutzer das Menü Element auswählt, legt das System den **itemaction** -Member [**der drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur auf den Wert für die **ODA- \_ Auswahl** fest und legt den **\_ ausgewählten ODS** -Wert im **ItemState** -Member fest.</span><span class="sxs-lookup"><span data-stu-id="44b7f-327">If the user selects the menu item, the system sets the **itemAction** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure to the **ODA\_SELECT** value and sets the **ODS\_SELECTED** value in the **itemState** member.</span></span> <span data-ttu-id="44b7f-328">Dies ist der Hinweis einer Anwendung, um das Menü Element neu zu zeichnen, um anzugeben, dass es ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-328">This is an application's cue to redraw the menu item to indicate that it is selected.</span></span>

### <a name="owner-drawn-menus-and-the-wm_menuchar-message"></a><span data-ttu-id="44b7f-329">Owner-Drawn Menüs und die WM- \_ menuchar-Meldung</span><span class="sxs-lookup"><span data-stu-id="44b7f-329">Owner-Drawn Menus and the WM\_MENUCHAR Message</span></span>

<span data-ttu-id="44b7f-330">Menüs, die keine von einem Besitzer gezeichneten Menüs sind, können ein mnetmonisches Menü angeben, indem Sie einen Unterstrich neben einem Zeichen in der Menü Zeichenfolge einfügen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-330">Menus other than owner-drawn menus can specify a menu mnemonic by inserting an underscore next to a character in the menu string.</span></span> <span data-ttu-id="44b7f-331">Dies ermöglicht dem Benutzer das Auswählen des Menüs durch Drücken von alt und drücken des Menüs mnetmonisches Zeichen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-331">This allows the user to select the menu by pressing ALT and pressing the menu mnemonic character.</span></span> <span data-ttu-id="44b7f-332">In den von einem Besitzer gezeichneten Menüs können Sie jedoch kein mnetmonisches Menü auf diese Weise angeben.</span><span class="sxs-lookup"><span data-stu-id="44b7f-332">In owner-drawn menus, however, you cannot specify a menu mnemonic in this manner.</span></span> <span data-ttu-id="44b7f-333">Stattdessen muss Ihre Anwendung die [**WM \_ menuchar**](wm-menuchar.md) -Nachricht verarbeiten, um von einem Besitzer gezeichnete Menüs mit Menü-mnetmonics bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-333">Instead, your application must process the [**WM\_MENUCHAR**](wm-menuchar.md) message to provide owner-drawn menus with menu mnemonics.</span></span>

<span data-ttu-id="44b7f-334">Die " [**WM \_ menuchar**](wm-menuchar.md) "-Meldung wird gesendet, wenn der Benutzer ein Menü "mnetmonic" eingibt, das mit keinem der vordefinierten mmaics des aktuellen Menüs identisch ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-334">The [**WM\_MENUCHAR**](wm-menuchar.md) message is sent when the user types a menu mnemonic that does not match any of the predefined mnemonics of the current menu.</span></span> <span data-ttu-id="44b7f-335">Der in *wParam* enthaltene Wert gibt das ASCII-Zeichen an, das dem Schlüssel entspricht, den der Benutzer mit der Alt-Taste gedrückt hat.</span><span class="sxs-lookup"><span data-stu-id="44b7f-335">The value contained in *wParam* specifies the ASCII character that corresponds to the key the user pressed with the ALT key.</span></span> <span data-ttu-id="44b7f-336">Das nieder wertige Wort von *wParam* gibt den Typ des ausgewählten Menüs an und kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="44b7f-336">The low-order word of *wParam* specifies the type of the selected menu and can be one of the following values:</span></span>

-   <span data-ttu-id="44b7f-337">**MF \_ Popup** , wenn das aktuelle Menü ein Untermenü ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-337">**MF\_POPUP** if the current menu is a submenu.</span></span>
-   <span data-ttu-id="44b7f-338">**MF \_ Sysmenu** , wenn das Menü das Systemmenü ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-338">**MF\_SYSMENU** if the menu is the system menu.</span></span>

<span data-ttu-id="44b7f-339">Das hochwertige Wort von *wParam* enthält das Menü Handle für das aktuelle Menü.</span><span class="sxs-lookup"><span data-stu-id="44b7f-339">The high-order word of *wParam* contains the menu handle to the current menu.</span></span> <span data-ttu-id="44b7f-340">Das Fenster mit den von einem Besitzer gezeichneten Menüs kann [**WM \_ menuchar**](wm-menuchar.md) wie folgt verarbeiten:</span><span class="sxs-lookup"><span data-stu-id="44b7f-340">The window with the owner-drawn menus can process [**WM\_MENUCHAR**](wm-menuchar.md) as follows:</span></span>


```
   case WM_MENUCHAR:
      nIndex = Determine index of menu item to be selected from
               character that was typed and handle to the current
               menu.
      return MAKELRESULT(nIndex, 2);
```



<span data-ttu-id="44b7f-341">Mit den beiden im höherwertigen Wort des Rückgabewerts wird dem System mitgeteilt, dass das nieder wertige Wort des Rückgabewerts den NULL basierten Index des auszuwählenden Menü Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="44b7f-341">The two in the high-order word of the return value informs the system that the low-order word of the return value contains the zero-based index of the menu item to be selected.</span></span>

<span data-ttu-id="44b7f-342">Die folgenden Konstanten entsprechen den möglichen Rückgabe Werten der WM- [**\_ menuchar**](wm-menuchar.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="44b7f-342">The following constants correspond to the possible return values from the [**WM\_MENUCHAR**](wm-menuchar.md) message.</span></span>



| <span data-ttu-id="44b7f-343">Konstante</span><span class="sxs-lookup"><span data-stu-id="44b7f-343">Constant</span></span>         | <span data-ttu-id="44b7f-344">Wert</span><span class="sxs-lookup"><span data-stu-id="44b7f-344">Value</span></span> | <span data-ttu-id="44b7f-345">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="44b7f-345">Meaning</span></span>                                                                                                                                                       |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44b7f-346">**MNC \_ ignorieren**</span><span class="sxs-lookup"><span data-stu-id="44b7f-346">**MNC\_IGNORE**</span></span>  | <span data-ttu-id="44b7f-347">0</span><span class="sxs-lookup"><span data-stu-id="44b7f-347">0</span></span>     | <span data-ttu-id="44b7f-348">Das System sollte das vom Benutzer gedrückte Zeichen verwerfen und auf dem System Sprecher ein kurzes Signal erstellen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-348">The system should discard the character the user pressed and create a short beep on the system speaker.</span></span>                                                       |
| <span data-ttu-id="44b7f-349">**MNC- \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="44b7f-349">**MNC\_CLOSE**</span></span>   | <span data-ttu-id="44b7f-350">1</span><span class="sxs-lookup"><span data-stu-id="44b7f-350">1</span></span>     | <span data-ttu-id="44b7f-351">Das System sollte das aktive Menü schließen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-351">The system should close the active menu.</span></span>                                                                                                                      |
| <span data-ttu-id="44b7f-352">**MNC- \_ Ausführung**</span><span class="sxs-lookup"><span data-stu-id="44b7f-352">**MNC\_EXECUTE**</span></span> | <span data-ttu-id="44b7f-353">2</span><span class="sxs-lookup"><span data-stu-id="44b7f-353">2</span></span>     | <span data-ttu-id="44b7f-354">Das System sollte das im nieder wertigen Wort des Rückgabewerts angegebene Element auswählen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-354">The system should choose the item specified in the low-order word of the return value.</span></span> <span data-ttu-id="44b7f-355">Das Besitzer Fenster empfängt eine [**WM- \_ Befehls**](wm-command.md) Meldung.</span><span class="sxs-lookup"><span data-stu-id="44b7f-355">The owner window receives a [**WM\_COMMAND**](wm-command.md) message.</span></span> |
| <span data-ttu-id="44b7f-356">**MNC \_ SELECT**</span><span class="sxs-lookup"><span data-stu-id="44b7f-356">**MNC\_SELECT**</span></span>  | <span data-ttu-id="44b7f-357">3</span><span class="sxs-lookup"><span data-stu-id="44b7f-357">3</span></span>     | <span data-ttu-id="44b7f-358">Das System sollte das im nieder wertigen Wort des Rückgabewerts angegebene Element auswählen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-358">The system should select the item specified in the low-order word of the return value.</span></span>                                                                        |



 

### <a name="setting-fonts-for-menu-item-text-strings"></a><span data-ttu-id="44b7f-359">Festlegen von Schriftarten für Menu-Item Text Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="44b7f-359">Setting Fonts for Menu-Item Text Strings</span></span>

<span data-ttu-id="44b7f-360">Dieses Thema enthält ein Beispiel für eine Anwendung, die in einem Menü von einem Besitzer gezeichnete Menü Elemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="44b7f-360">This topic contains an example from an application that uses owner-drawn menu items in a menu.</span></span> <span data-ttu-id="44b7f-361">Das Menü enthält Elemente, die die Attribute der aktuellen Schriftart festlegen, und die Elemente werden mit dem entsprechenden Font-Attribut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="44b7f-361">The menu contains items that set the attributes of the current font, and the items are displayed using the appropriate font attribute.</span></span>

<span data-ttu-id="44b7f-362">Hier sehen Sie, wie das Menü in der Ressourcen Definitionsdatei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-362">Here is how the menu is defined in the resource-definition file.</span></span> <span data-ttu-id="44b7f-363">Beachten Sie, dass die Zeichen folgen für die Menü Elemente "regulär", "Fett", "Kursiv" und "Unterstreichung" zur Laufzeit zugewiesen werden, sodass Ihre Zeichen folgen in der Ressourcen Definitionsdatei leer sind.</span><span class="sxs-lookup"><span data-stu-id="44b7f-363">Note that the strings for the Regular, Bold, Italic, and Underline menu items are assigned at run time, so their strings are empty in the resource-definition file.</span></span>


```
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "",    IDM_REGULAR 
        MENUITEM SEPARATOR 
        MENUITEM    "",    IDM_BOLD 
        MENUITEM    "",    IDM_ITALIC 
        MENUITEM    "",    IDM_ULINE 
    END 
END 
```



<span data-ttu-id="44b7f-364">Die Fenster Prozedur der Anwendung verarbeitet die Nachrichten, die an der Verwendung von vom Besitzer gezeichneten Menü Elementen beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="44b7f-364">The application's window procedure processes the messages involved in using owner-drawn menu items.</span></span> <span data-ttu-id="44b7f-365">Die Anwendung verwendet die [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht, um Folgendes durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="44b7f-365">The application uses the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to do the following:</span></span>

-   <span data-ttu-id="44b7f-366">Legen Sie für die Menü Elemente das-Flag für den **MF \_** -Besitzer fest.</span><span class="sxs-lookup"><span data-stu-id="44b7f-366">Set the **MF\_OWNERDRAW** flag for the menu items.</span></span>
-   <span data-ttu-id="44b7f-367">Legen Sie die Text Zeichenfolgen für die Menü Elemente fest.</span><span class="sxs-lookup"><span data-stu-id="44b7f-367">Set the text strings for the menu items.</span></span>
-   <span data-ttu-id="44b7f-368">Ruft Handles der Schriftarten ab, die zum Zeichnen der Elemente verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-368">Obtain handles of the fonts used to draw the items.</span></span>
-   <span data-ttu-id="44b7f-369">Ruft die Text-und Hintergrund Farbwerte für ausgewählte Menü Elemente ab.</span><span class="sxs-lookup"><span data-stu-id="44b7f-369">Obtain the text and background color values for selected menu items.</span></span>

<span data-ttu-id="44b7f-370">Die Text Zeichenfolgen und Schriftart Handles werden in einem Array von Anwendungs definierten myItem-Strukturen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="44b7f-370">The text strings and font handles are stored in an array of application-defined MYITEM structures.</span></span> <span data-ttu-id="44b7f-371">Die Anwendungs definierte getafont-Funktion erstellt eine Schriftart, die dem angegebenen Schriftart Attribut entspricht, und gibt ein Handle für die Schriftart zurück.</span><span class="sxs-lookup"><span data-stu-id="44b7f-371">The application-defined GetAFont function creates a font that corresponds to the specified font attribute and returns a handle to the font.</span></span> <span data-ttu-id="44b7f-372">Die Handles werden während der Verarbeitung der WM- [**\_ zerstörungsnachricht**](/windows/desktop/winmsg/wm-destroy) zerstört.</span><span class="sxs-lookup"><span data-stu-id="44b7f-372">The handles are destroyed during the processing of the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span>

<span data-ttu-id="44b7f-373">Während der Verarbeitung der " [**WM \_ MeasureItem**](../controls/wm-measureitem.md) "-Nachricht Ruft das Beispiel die Breite und Höhe einer Menü Element Zeichenfolge ab und kopiert diese Werte in die [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="44b7f-373">During the processing of the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message, the example gets the width and height of a menu-item string and copies these values into the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure.</span></span> <span data-ttu-id="44b7f-374">Das System verwendet die Width-und Height-Werte, um die Größe des Menüs zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-374">The system uses the width and height values to calculate the size of the menu.</span></span>

<span data-ttu-id="44b7f-375">Während der Verarbeitung der [**WM- \_ DrawItem**](../controls/wm-drawitem.md) -Nachricht wird die Zeichenfolge des Menü Elements mit Raum links neben der Zeichenfolge für das Häkchen-Bitmap gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="44b7f-375">During the processing of the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message, the menu item's string is drawn with room left next to the string for the check-mark bitmap.</span></span> <span data-ttu-id="44b7f-376">Wenn der Benutzer das Element auswählt, werden die ausgewählten Text-und Hintergrundfarben verwendet, um das Element zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-376">If the user selects the item, the selected text and background colors are used to draw the item.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    typedef struct _MYITEM 
    { 
        HFONT hfont; 
        LPSTR psz; 
    } MYITEM;             // structure for item font and string  
 
    MYITEM *pmyitem;      // pointer to item's font and string        
    static MYITEM myitem[CITEMS];   // array of MYITEMS               
    static HMENU hmenu;             // handle to main menu            
    static COLORREF crSelText;  // text color of selected item        
    static COLORREF crSelBkgnd; // background color of selected item  
    COLORREF crText;            // text color of unselected item      
    COLORREF crBkgnd;           // background color unselected item   
    LPMEASUREITEMSTRUCT lpmis;  // pointer to item of data             
    LPDRAWITEMSTRUCT lpdis;     // pointer to item drawing data        
    HDC hdc;                    // handle to screen DC                
    SIZE size;                  // menu-item text extents             
    WORD wCheckX;               // check-mark width                   
    int nTextX;                 // width of menu item                 
    int nTextY;                 // height of menu item                
    int i;                      // loop counter                       
    HFONT hfontOld;             // handle to old font                 
    BOOL fSelected = FALSE;     // menu-item selection flag
    size_t * pcch;
    HRESULT hResult;           
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Modify the Regular, Bold, Italic, and Underline 
            // menu items to make them owner-drawn items. Associate 
            // a MYITEM structure with each item to contain the 
            // string for and font handle to each item. 
 
            hmenu = GetMenu(hwnd); 
            ModifyMenu(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED | MF_OWNERDRAW, IDM_REGULAR, 
                (LPTSTR) &myitem[REGULAR]); 
            ModifyMenu(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_BOLD, (LPTSTR) &myitem[BOLD]); 
            ModifyMenu(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ITALIC, 
                (LPTSTR) &myitem[ITALIC]); 
            ModifyMenu(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                MF_OWNERDRAW, IDM_ULINE, (LPTSTR) &myitem[ULINE]); 
 
            // Retrieve each item's font handle and copy it into 
            // the hfont member of each item's MYITEM structure. 
            // Also, copy each item's string into the structures. 
 
            myitem[REGULAR].hfont = GetAFont(REGULAR); 
            myitem[REGULAR].psz = "Regular"; 
            myitem[BOLD].hfont = GetAFont(BOLD); 
            myitem[BOLD].psz = "Bold"; 
            myitem[ITALIC].hfont = GetAFont(ITALIC); 
            myitem[ITALIC].psz = "Italic"; 
            myitem[ULINE].hfont = GetAFont(ULINE); 
            myitem[ULINE].psz = "Underline"; 
 
            // Retrieve the text and background colors of the 
            // selected menu text. 
 
            crSelText = GetSysColor(COLOR_HIGHLIGHTTEXT); 
            crSelBkgnd = GetSysColor(COLOR_HIGHLIGHT); 
 
            return 0; 
 
        case WM_MEASUREITEM: 
 
            // Retrieve a device context for the main window.  
 
            hdc = GetDC(hwnd); 
 
            // Retrieve pointers to the menu item's 
            // MEASUREITEMSTRUCT structure and MYITEM structure. 
 
            lpmis = (LPMEASUREITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpmis->itemData; 
 
            // Select the font associated with the item into 
            // the main window's device context. 
 
            hfontOld = SelectObject(hdc, pmyitem->hfont); 
 
            // Retrieve the width and height of the item's string, 
            // and then copy the width and height into the 
            // MEASUREITEMSTRUCT structure's itemWidth and 
            // itemHeight members.
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            GetTextExtentPoint32(hdc, pmyitem->psz, 
                *pcch, &size); 
            lpmis->itemWidth = size.cx; 
            lpmis->itemHeight = size.cy; 
 
            // Select the old font back into the device context, 
            // and then release the device context. 
 
            SelectObject(hdc, hfontOld); 
            ReleaseDC(hwnd, hdc); 
 
            return TRUE; 
 
            break; 
 
        case WM_DRAWITEM: 
 
            // Get pointers to the menu item's DRAWITEMSTRUCT 
            // structure and MYITEM structure. 
 
            lpdis = (LPDRAWITEMSTRUCT) lParam; 
            pmyitem = (MYITEM *) lpdis->itemData; 
 
            // If the user has selected the item, use the selected 
            // text and background colors to display the item. 
 
            if (lpdis->itemState & ODS_SELECTED) 
            { 
                crText = SetTextColor(lpdis->hDC, crSelText); 
                crBkgnd = SetBkColor(lpdis->hDC, crSelBkgnd); 
                fSelected = TRUE; 
            } 
 
            // Remember to leave space in the menu item for the 
            // check-mark bitmap. Retrieve the width of the bitmap 
            // and add it to the width of the menu item. 
 
            wCheckX = GetSystemMetrics(SM_CXMENUCHECK); 
            nTextX = wCheckX + lpdis->rcItem.left; 
            nTextY = lpdis->rcItem.top; 
 
            // Select the font associated with the item into the 
            // item's device context, and then draw the string. 
 
            hfontOld = SelectObject(lpdis->hDC, pmyitem->hfont);
            
            hResult = StringCchLength(pmyitem->psz,STRSAFE_MAX_CCH, pcch);
            if (FAILED(hResult))
            {
            // Add code to fail as securely as possible.
                return;
            } 
 
            ExtTextOut(lpdis->hDC, nTextX, nTextY, ETO_OPAQUE, 
                &lpdis->rcItem, pmyitem->psz, 
                *pcch, NULL); 
 
            // Select the previous font back into the device 
            // context. 
 
            SelectObject(lpdis->hDC, hfontOld); 
 
            // Return the text and background colors to their 
            // normal state (not selected). 
 
            if (fSelected) 
            { 
                SetTextColor(lpdis->hDC, crText); 
                SetBkColor(lpdis->hDC, crBkgnd); 
            } 
 
            return TRUE; 
 
        // Process other messages.  
 
        case WM_DESTROY: 
 
            // Destroy the menu items' font handles.  
 
            for (i = 0; i < CITEMS; i++) 
                DeleteObject(myitem[i].hfont); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HFONT GetAFont(int fnFont) 
{ 
    static LOGFONT lf;  // structure for font information  
 
    // Get a handle to the ANSI fixed-pitch font, and copy 
    // information about the font to a LOGFONT structure. 
 
    GetObject(GetStockObject(ANSI_FIXED_FONT), sizeof(LOGFONT), 
        &lf); 
 
    // Set the font attributes, as appropriate.  
 
    if (fnFont == BOLD) 
        lf.lfWeight = FW_BOLD; 
    else 
        lf.lfWeight = FW_NORMAL; 
 
    lf.lfItalic = (fnFont == ITALIC); 
    lf.lfItalic = (fnFont == ULINE); 
 
    // Create the font, and then return its handle.  
 
    return CreateFont(lf.lfHeight, lf.lfWidth, 
        lf.lfEscapement, lf.lfOrientation, lf.lfWeight, 
        lf.lfItalic, lf.lfUnderline, lf.lfStrikeOut, lf.lfCharSet, 
        lf.lfOutPrecision, lf.lfClipPrecision, lf.lfQuality, 
        lf.lfPitchAndFamily, lf.lfFaceName); 
} 
```



### <a name="example-of-owner-drawn-menu-items"></a><span data-ttu-id="44b7f-377">Beispiel für Owner-Drawn Menü Elemente</span><span class="sxs-lookup"><span data-stu-id="44b7f-377">Example of Owner-Drawn Menu Items</span></span>

<span data-ttu-id="44b7f-378">Im Beispiel in diesem Thema werden vom Besitzer gezeichnete Menü Elemente in einem Menü verwendet.</span><span class="sxs-lookup"><span data-stu-id="44b7f-378">The example in this topic uses owner-drawn menu items in a menu.</span></span> <span data-ttu-id="44b7f-379">Die Menü Elemente wählen bestimmte Schriftart Attribute aus, und die Anwendung zeigt jedes Menü Element mit einer Schriftart an, die das entsprechende-Attribut aufweist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-379">The menu items select specific font attributes, and the application displays each menu item using a font that has the corresponding attribute.</span></span> <span data-ttu-id="44b7f-380">Beispielsweise wird das Menü Element **kursiv** formatiert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="44b7f-380">For example, the **Italic** menu item is displayed in an italic font.</span></span> <span data-ttu-id="44b7f-381">Der Name des **Zeichen** Menüs in der Menüleiste öffnet das Menü.</span><span class="sxs-lookup"><span data-stu-id="44b7f-381">The **Character** menu name on the menu bar opens the menu.</span></span>

<span data-ttu-id="44b7f-382">Die Menüleiste und das Dropdown Menü werden anfänglich durch eine erweiterte Menü Vorlagen Ressource definiert.</span><span class="sxs-lookup"><span data-stu-id="44b7f-382">The menu bar and drop-down menu are defined initially by an extended menu-template resource.</span></span> <span data-ttu-id="44b7f-383">Da eine Menüvorlage keine von einem Besitzer gezeichneten Elemente angeben kann, enthält das Menü anfänglich vier Text Menü Elemente mit den folgenden Zeichen folgen: "Regular", "Bold", "Kursiv" und "unterstrichen".</span><span class="sxs-lookup"><span data-stu-id="44b7f-383">Because a menu template cannot specify owner-drawn items, the menu initially contains four text menu items with the following strings: "Regular," "Bold," "Italic," and "Underline."</span></span> <span data-ttu-id="44b7f-384">Die Fenster Prozedur der Anwendung ändert diese in vom Besitzer gezeichnete Elemente, wenn die [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="44b7f-384">The application's window procedure changes these to owner-drawn items when it processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span> <span data-ttu-id="44b7f-385">Beim Empfang der **WM \_ Create** -Nachricht Ruft die Fenster Prozedur die Anwendungs definierte OnCreate-Funktion auf, die die folgenden Schritte für jedes Menü Element ausführt:</span><span class="sxs-lookup"><span data-stu-id="44b7f-385">When it receives the **WM\_CREATE** message, the window procedure calls the application-defined OnCreate function, which performs the following steps for each menu item:</span></span>

-   <span data-ttu-id="44b7f-386">Ordnet eine von der Anwendung definierte myItem-Struktur zu.</span><span class="sxs-lookup"><span data-stu-id="44b7f-386">Allocates an application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="44b7f-387">Ruft den Text des Menü Elements ab und speichert ihn in der von der Anwendung definierten myItem-Struktur.</span><span class="sxs-lookup"><span data-stu-id="44b7f-387">Gets the text of the menu item and saves it in the application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="44b7f-388">Erstellt die Schriftart, die zum Anzeigen des Menü Elements verwendet wird, und speichert das Handle in der von der Anwendung definierten myItem-Struktur.</span><span class="sxs-lookup"><span data-stu-id="44b7f-388">Creates the font used to display the menu item and saves its handle in the application-defined MYITEM structure.</span></span>
-   <span data-ttu-id="44b7f-389">Ändert den Menü Elementtyp in **MFT \_** -Besitzer zeichnen und speichert einen Zeiger auf die Anwendungs definierte myItem-Struktur als Elementdaten.</span><span class="sxs-lookup"><span data-stu-id="44b7f-389">Changes the menu item type to **MFT\_OWNERDRAW** and saves a pointer to the application-defined MYITEM structure as item data.</span></span>

<span data-ttu-id="44b7f-390">Da ein Zeiger auf jede Anwendungs definierte myItem-Struktur als Elementdaten gespeichert wird, wird Sie in Verbindung mit den Nachrichten " [**WM \_ MeasureItem**](../controls/wm-measureitem.md) " und " [**WM \_ DrawItem**](../controls/wm-drawitem.md) " für das entsprechende Menü Element an die Fenster Prozedur übergeben.</span><span class="sxs-lookup"><span data-stu-id="44b7f-390">Because a pointer to each application-defined MYITEM structure is saved as item data, it is passed to the window procedure in conjunction with the [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) and [**WM\_DRAWITEM**](../controls/wm-drawitem.md) messages for the corresponding menu item.</span></span> <span data-ttu-id="44b7f-391">Der-Zeiger ist im **ItemData** -Member der [**measureitemstruct**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) -Struktur und der [**drawitemstruct**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="44b7f-391">The pointer is contained in the **itemData** member of both the [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) and [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structures.</span></span>

<span data-ttu-id="44b7f-392">Bei der ersten Anzeige wird eine [**WM \_ MeasureItem**](../controls/wm-measureitem.md) -Meldung für jedes Menü Element gesendet, das vom Besitzer gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="44b7f-392">A [**WM\_MEASUREITEM**](../controls/wm-measureitem.md) message is sent for each owner-drawn menu item the first time it is displayed.</span></span> <span data-ttu-id="44b7f-393">Die Anwendung verarbeitet diese Nachricht, indem die Schriftart für das Menü Element in einen Gerätekontext ausgewählt und dann der erforderliche Speicherplatz für die Anzeige des Menü Element Texts in dieser Schriftart festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="44b7f-393">The application processes this message by selecting the font for the menu item into a device context and then determining the space required to display the menu item text in that font.</span></span> <span data-ttu-id="44b7f-394">Der Text für Schriftart und Menü Element wird durch die Struktur des Menü Elements `MYITEM` (die von der Anwendung definierte Struktur) angegeben.</span><span class="sxs-lookup"><span data-stu-id="44b7f-394">The font and menu item text are both specified by the menu item's `MYITEM` structure (the structure defined by the application).</span></span> <span data-ttu-id="44b7f-395">Die Anwendung bestimmt die Größe des Texts mithilfe der [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="44b7f-395">The application determines the size of the text by using the [**GetTextExtentPoint32**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpoint32a) function.</span></span>

<span data-ttu-id="44b7f-396">Die Fenster Prozedur verarbeitet die [**WM- \_ DrawItem**](../controls/wm-drawitem.md) -Nachricht, indem der Menü Element Text in der entsprechenden Schriftart angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="44b7f-396">The window procedure processes the [**WM\_DRAWITEM**](../controls/wm-drawitem.md) message by displaying the menu item text in the appropriate font.</span></span> <span data-ttu-id="44b7f-397">Der Schriftart-und Menü Element Text wird durch die Struktur des Menü Elements angegeben `MYITEM` .</span><span class="sxs-lookup"><span data-stu-id="44b7f-397">The font and menu item text are both specified by the menu item's `MYITEM` structure.</span></span> <span data-ttu-id="44b7f-398">Die Anwendung wählt Text und Hintergrundfarben aus, die für den Zustand des Menü Elements geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="44b7f-398">The application selects text and background colors appropriate to the menu item's state.</span></span>

<span data-ttu-id="44b7f-399">Die Fenster Prozedur verarbeitet die [**WM- \_ zerstörungsnachricht**](/windows/desktop/winmsg/wm-destroy) , um Schriftarten zu zerstören und Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="44b7f-399">The window procedure processes the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message to destroy fonts and free memory.</span></span> <span data-ttu-id="44b7f-400">Die Anwendung löscht die Schriftart und gibt die von der Anwendung definierte myItem-Struktur für jedes Menü Element frei.</span><span class="sxs-lookup"><span data-stu-id="44b7f-400">The application deletes the font and frees the application-defined MYITEM structure for each menu item.</span></span>

<span data-ttu-id="44b7f-401">Im folgenden finden Sie die relevanten Teile der Header Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="44b7f-401">The following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_REGULAR   11 
#define IDM_BOLD      12 
#define IDM_ITALIC    13 
#define IDM_UNDERLINE 14 
 
// Structure associated with menu items 
 
typedef struct tagMYITEM 
{ 
    HFONT hfont; 
    int   cchItemText; 
    char  szItemText[1]; 
} MYITEM; 
 
#define CCH_MAXITEMTEXT 256 
 
```



<span data-ttu-id="44b7f-402">Im folgenden sind die relevanten Teile der Fenster Prozedur der Anwendung und die zugehörigen Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="44b7f-402">The following are the relevant portions of the application's window procedure and its associated functions.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_MEASUREITEM: 
            OnMeasureItem(hwnd, (LPMEASUREITEMSTRUCT) lParam); 
            return TRUE; 
 
        case WM_DRAWITEM: 
            OnDrawItem(hwnd, (LPDRAWITEMSTRUCT) lParam); 
            return TRUE; 
 
        // Additional message processing goes here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Modify each menu item. Assume that the IDs IDM_REGULAR 
    // through IDM_UNDERLINE are consecutive numbers. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
         // Allocate an item structure, leaving space for a 
         // string of up to CCH_MAXITEMTEXT characters. 
 
        pMyItem = (MYITEM *) LocalAlloc(LMEM_FIXED, 
                sizeof(MYITEM) + CCH_MAXITEMTEXT); 
 
        // Save the item text in the item structure. 
 
        mii.fMask = MIIM_STRING; 
        mii.dwTypeData = pMyItem->szItemText; 
        mii.cch = CCH_MAXITEMTEXT; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem->cchItemText = mii.cch; 
 
        // Reallocate the structure to the minimum required size. 
 
        pMyItem = (MYITEM *) LocalReAlloc(pMyItem, 
                sizeof(MYITEM) + mii.cch, LMEM_MOVEABLE); 
 
        // Create the font used to draw the item. 
 
        pMyItem->hfont = CreateMenuItemFont(uID); 
 
        // Change the item to an owner-drawn item, and save 
        // the address of the item structure as item data. 
 
        mii.fMask = MIIM_FTYPE | MIIM_DATA; 
        mii.fType = MFT_OWNERDRAW; 
        mii.dwItemData = (ULONG_PTR) pMyItem; 
        SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
    } 
    return TRUE; 
} 
 
HFONT CreateMenuItemFont(UINT uID) 
{ 
    LOGFONT lf;
    HRESULT hr; 
 
    ZeroMemory(&lf, sizeof(lf)); 
    lf.lfHeight = 20; 
    hr = StringCchCopy(lf.lfFaceName, 32, "Times New Roman");
    if (FAILED(hr))
    {
    // TODO: writer error handler
    } 
 
    switch (uID) 
    { 
        case IDM_BOLD: 
            lf.lfWeight = FW_HEAVY; 
            break; 
 
        case IDM_ITALIC: 
            lf.lfItalic = TRUE; 
            break; 
 
        case IDM_UNDERLINE: 
            lf.lfUnderline = TRUE; 
            break; 
    } 
    return CreateFontIndirect(&lf); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    MYITEM *pMyItem; 
 
    // Get a handle to the menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get  
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Free resources associated with each menu item. 
 
    for (uID = IDM_REGULAR; uID <= IDM_UNDERLINE; uID++) 
    { 
        // Get the item data. 
 
        mii.fMask = MIIM_DATA; 
        GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
        pMyItem = (MYITEM *) mii.dwItemData; 
 
        // Destroy the font and free the item structure. 
 
        DeleteObject(pMyItem->hfont); 
        LocalFree(pMyItem); 
    } 
} 
 
VOID WINAPI OnMeasureItem(HWND hwnd, LPMEASUREITEMSTRUCT lpmis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpmis->itemData; 
    HDC hdc = GetDC(hwnd); 
    HFONT hfntOld = (HFONT)SelectObject(hdc, pMyItem->hfont); 
    SIZE size; 
 
    GetTextExtentPoint32(hdc, pMyItem->szItemText, 
            pMyItem->cchItemText, &size); 
 
    lpmis->itemWidth = size.cx; 
    lpmis->itemHeight = size.cy; 
 
    SelectObject(hdc, hfntOld); 
    ReleaseDC(hwnd, hdc); 
} 
 
VOID WINAPI OnDrawItem(HWND hwnd, LPDRAWITEMSTRUCT lpdis) 
{ 
    MYITEM *pMyItem = (MYITEM *) lpdis->itemData; 
    COLORREF clrPrevText, clrPrevBkgnd; 
    HFONT hfntPrev; 
    int x, y; 
 
    // Set the appropriate foreground and background colors. 
 
    if (lpdis->itemState & ODS_SELECTED) 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHTTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_HIGHLIGHT)); 
    } 
    else 
    { 
        clrPrevText = SetTextColor(lpdis->hDC, 
                GetSysColor(COLOR_MENUTEXT)); 
        clrPrevBkgnd = SetBkColor(lpdis->hDC, 
                GetSysColor(COLOR_MENU)); 
    } 
 
    // Determine where to draw and leave space for a check mark. 
 
    x = lpdis->rcItem.left; 
    y = lpdis->rcItem.top; 
    x += GetSystemMetrics(SM_CXMENUCHECK); 
 
    // Select the font and draw the text. 
 
    hfntPrev = (HFONT)SelectObject(lpdis->hDC, pMyItem->hfont); 
    ExtTextOut(lpdis->hDC, x, y, ETO_OPAQUE, 
            &lpdis->rcItem, pMyItem->szItemText, 
            pMyItem->cchItemText, NULL); 
 
    // Restore the original font and colors. 
 
    SelectObject(lpdis->hDC, hfntPrev); 
    SetTextColor(lpdis->hDC, clrPrevText); 
    SetBkColor(lpdis->hDC, clrPrevBkgnd); 
} 
```



## <a name="using-custom-check-mark-bitmaps"></a><span data-ttu-id="44b7f-403">Verwenden von benutzerdefinierten Häkchen-Bitmaps</span><span class="sxs-lookup"><span data-stu-id="44b7f-403">Using Custom Check Mark Bitmaps</span></span>

<span data-ttu-id="44b7f-404">Das System stellt eine Standard Bitmap für das Häkchen bereit, die neben einem ausgewählten Menü Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="44b7f-404">The system provides a default check-mark bitmap for displaying next to a menu item that is selected.</span></span> <span data-ttu-id="44b7f-405">Sie können ein einzelnes Menü Element anpassen, indem Sie ein Bitmappaar bereitstellen, um die Standard Bitmap für das Häkchen zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-405">You can customize an individual menu item by providing a pair of bitmaps to replace the default check-mark bitmap.</span></span> <span data-ttu-id="44b7f-406">Das System zeigt eine Bitmap an, wenn das Element ausgewählt wird, und das andere, wenn es klar ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-406">The system displays one bitmap when the item is selected and the other when it is clear.</span></span> <span data-ttu-id="44b7f-407">In diesem Abschnitt werden die Schritte zum Erstellen und Verwenden von benutzerdefinierten Prüfzeichen-Bitmaps beschrieben.</span><span class="sxs-lookup"><span data-stu-id="44b7f-407">This section describes the steps involved in creating and using custom check-mark bitmaps.</span></span>

-   [<span data-ttu-id="44b7f-408">Erstellen von benutzerdefinierten Häkchen Bitmaps</span><span class="sxs-lookup"><span data-stu-id="44b7f-408">Creating Custom Check Mark Bitmaps</span></span>](#creating-custom-check-mark-bitmaps)
-   [<span data-ttu-id="44b7f-409">Zuordnen von Bitmaps zu einem Menü Element</span><span class="sxs-lookup"><span data-stu-id="44b7f-409">Associating Bitmaps with a Menu Item</span></span>](#associating-bitmaps-with-a-menu-item)
-   [<span data-ttu-id="44b7f-410">Festlegen des Häkchen Attributs</span><span class="sxs-lookup"><span data-stu-id="44b7f-410">Setting the Check-mark Attribute</span></span>](#setting-the-check-mark-attribute)
-   [<span data-ttu-id="44b7f-411">Simulieren von Kontrollkästchen in einem Menü</span><span class="sxs-lookup"><span data-stu-id="44b7f-411">Simulating Check Boxes in a Menu</span></span>](#simulating-check-boxes-in-a-menu)
-   [<span data-ttu-id="44b7f-412">Beispiel für die Verwendung von benutzerdefinierten Bitmaps für das Häkchen</span><span class="sxs-lookup"><span data-stu-id="44b7f-412">Example of Using Custom Check-mark Bitmaps</span></span>](#example-of-using-custom-check-mark-bitmaps)

### <a name="creating-custom-check-mark-bitmaps"></a><span data-ttu-id="44b7f-413">Erstellen von benutzerdefinierten Häkchen Bitmaps</span><span class="sxs-lookup"><span data-stu-id="44b7f-413">Creating Custom Check Mark Bitmaps</span></span>

<span data-ttu-id="44b7f-414">Eine benutzerdefinierte Bitmap für das Häkchen muss dieselbe Größe aufweisen wie die Standard Bitmap für das Häkchen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-414">A custom check-mark bitmap must be the same size as the default check-mark bitmap.</span></span> <span data-ttu-id="44b7f-415">Sie können die standardmäßige Häkchen Größe der Bitmap abrufen, indem Sie die [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-415">You can retrieve the default check-mark size of the bitmap by calling the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="44b7f-416">Das nieder wertige Wort des Rückgabewerts dieser Funktion gibt die Breite an. das höchst wertige Wort gibt die Höhe an.</span><span class="sxs-lookup"><span data-stu-id="44b7f-416">The low-order word of this function's return value specifies the width; the high-order word specifies the height.</span></span>

<span data-ttu-id="44b7f-417">Sie können Bitmapressourcen verwenden, um Bitmaps für das Häkchen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-417">You can use bitmap resources to provide check-mark bitmaps.</span></span> <span data-ttu-id="44b7f-418">Da die erforderliche Bitmapgröße je nach Anzeigetyp variiert, müssen Sie möglicherweise die Größe der Bitmap zur Laufzeit ändern, indem Sie die [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-418">However, because the required bitmap size varies depending on the display type, you may need to resize the bitmap at run time by using the [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) function.</span></span> <span data-ttu-id="44b7f-419">Abhängig von der Bitmap kann die durch die Größenänderung verursachte Verzerrung zu nicht akzeptablen Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-419">Depending on the bitmap, the distortion caused by sizing could produce unacceptable results.</span></span>

<span data-ttu-id="44b7f-420">Anstatt eine Bitmap-Ressource zu verwenden, können Sie mithilfe von GDI-Funktionen zur Laufzeit eine Bitmap erstellen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-420">Instead of using a bitmap resource, you can create a bitmap at run time by using GDI functions.</span></span>

<span data-ttu-id="44b7f-421">**So erstellen Sie eine Bitmap zur Laufzeit**</span><span class="sxs-lookup"><span data-stu-id="44b7f-421">**To create a bitmap at run time**</span></span>

1.  <span data-ttu-id="44b7f-422">Verwenden Sie [**die Funktion**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) "Funktion", um einen Gerätekontext zu erstellen, der mit dem vom Hauptfenster der Anwendung verwendeten kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-422">Use the [**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) function to create a device context compatible with the one used by the application's main window.</span></span>

    <span data-ttu-id="44b7f-423">Der *hdc* -Parameter der Funktion kann entweder **null** oder den Rückgabewert der Funktion angeben.</span><span class="sxs-lookup"><span data-stu-id="44b7f-423">The function's *hdc* parameter can specify either **NULL** or the return value from the function.</span></span> <span data-ttu-id="44b7f-424">" [**Kreatecompatibledc**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) " gibt ein Handle an den kompatiblen Gerätekontext zurück.</span><span class="sxs-lookup"><span data-stu-id="44b7f-424">[**CreateCompatibleDC**](/windows/desktop/api/wingdi/nf-wingdi-createcompatibledc) returns a handle to the compatible device context.</span></span>

2.  <span data-ttu-id="44b7f-425">Verwenden Sie [**die Funktion "**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) -Funktion", um eine Bitmap zu erstellen, die mit dem Hauptfenster der Anwendung kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-425">Use the [**CreateCompatibleBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap) function to create a bitmap compatible with the application's main window.</span></span>

    <span data-ttu-id="44b7f-426">Mit den Parametern " *nwidth* " und " *nheight* " der Funktion wird die Größe der Bitmap festgelegt. Sie sollten die von der [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion zurückgegebenen Width-und Height-Informationen angeben.</span><span class="sxs-lookup"><span data-stu-id="44b7f-426">This function's *nWidth* and *nHeight* parameters set the size of the bitmap; they should specify the width and height information returned by the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span>

    > [!Note]  
    > <span data-ttu-id="44b7f-427">Sie können auch die Funktion " [**kreatebitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) " verwenden, um eine monochrome Bitmap zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-427">You can also use the [**CreateBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createbitmap) function to create a monochrome bitmap.</span></span>

     

3.  <span data-ttu-id="44b7f-428">Verwenden Sie die [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) -Funktion, um die Bitmap in den kompatiblen Gerätekontext auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-428">Use the [**SelectObject**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) function to select the bitmap into the compatible device context.</span></span>
4.  <span data-ttu-id="44b7f-429">Verwenden Sie GDI-Zeichnungsfunktionen, z. b. [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) und [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), um ein Bild in die Bitmap zu zeichnen, oder verwenden Sie Funktionen wie [**BitBLT**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) und [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) zum Kopieren eines Bilds in die Bitmap.</span><span class="sxs-lookup"><span data-stu-id="44b7f-429">Use GDI drawing functions, such as [**Ellipse**](/windows/desktop/api/wingdi/nf-wingdi-ellipse) and [**LineTo**](/windows/desktop/api/wingdi/nf-wingdi-lineto), to draw an image into the bitmap, or use functions such as [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) and [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) to copy an image into the bitmap.</span></span>

<span data-ttu-id="44b7f-430">Weitere Informationen finden Sie unter [Bitmaps](/windows/desktop/gdi/bitmaps).</span><span class="sxs-lookup"><span data-stu-id="44b7f-430">For more information, see [Bitmaps](/windows/desktop/gdi/bitmaps).</span></span>

### <a name="associating-bitmaps-with-a-menu-item"></a><span data-ttu-id="44b7f-431">Zuordnen von Bitmaps zu einem Menü Element</span><span class="sxs-lookup"><span data-stu-id="44b7f-431">Associating Bitmaps with a Menu Item</span></span>

<span data-ttu-id="44b7f-432">Sie ordnen ein paar von Check-Mark-Bitmaps einem Menü Element zu, indem Sie die Handles der Bitmaps an die [**setmenuitembitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="44b7f-432">You associate a pair of check-mark bitmaps with a menu item by passing the handles of the bitmaps to the [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) function.</span></span> <span data-ttu-id="44b7f-433">Der *hbitmapuncheck* -Parameter identifiziert die Clear-Bitmap, und der *hbitmapcheck* -Parameter identifiziert die ausgewählte Bitmap.</span><span class="sxs-lookup"><span data-stu-id="44b7f-433">The *hBitmapUnchecked* parameter identifies the clear bitmap, and the *hBitmapChecked* parameter identifies the selected bitmap.</span></span> <span data-ttu-id="44b7f-434">Wenn Sie ein oder beide Häkchen aus einem Menü Element entfernen möchten, können Sie den Parameter *hbitmapuncheck* oder *hbitmapcheck* oder beides auf **null** festlegen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-434">If you want to remove one or both check marks from a menu item, you can set the *hBitmapUnchecked* or *hBitmapChecked* parameter, or both, to **NULL**.</span></span>

### <a name="setting-the-check-mark-attribute"></a><span data-ttu-id="44b7f-435">Festlegen des Häkchen Attributs</span><span class="sxs-lookup"><span data-stu-id="44b7f-435">Setting the Check-mark Attribute</span></span>

<span data-ttu-id="44b7f-436">Die [**checkmenuitem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) -Funktion legt das Häkchen Attribut eines Menü Elements auf "ausgewählt" oder "deaktiviert" fest.</span><span class="sxs-lookup"><span data-stu-id="44b7f-436">The [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) function sets a menu item's check-mark attribute to either selected or cleared.</span></span> <span data-ttu-id="44b7f-437">Sie können den von **MF \_** aktivierten Wert angeben, um das Häkchen Attribut auf "ausgewählt" festzulegen, und den Wert " **MF \_** deaktiviert", um ihn zu löschen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-437">You can specify the **MF\_CHECKED** value to set the check-mark attribute to selected and the **MF\_UNCHECKED** value to set it to clear.</span></span>

<span data-ttu-id="44b7f-438">Mithilfe der [**setmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) -Funktion können Sie auch den Status der Überprüfung eines Menü Elements festlegen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-438">You can also set the check state of a menu item by using the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function.</span></span>

<span data-ttu-id="44b7f-439">Manchmal stellt eine Gruppe von Menü Elementen einen Satz von sich gegenseitig ausschließenden Optionen dar.</span><span class="sxs-lookup"><span data-stu-id="44b7f-439">Sometimes a group of menu items represents a set of mutually exclusive options.</span></span> <span data-ttu-id="44b7f-440">Mithilfe der [**checkmenuradioitem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) -Funktion können Sie ein Menü Element aktivieren und gleichzeitig das Häkchen aus allen anderen Menü Elementen in der Gruppe entfernen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-440">By using the [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) function, you can check one menu item while simultaneously removing the check mark from all other menu items in the group.</span></span>

### <a name="simulating-check-boxes-in-a-menu"></a><span data-ttu-id="44b7f-441">Simulieren von Kontrollkästchen in einem Menü</span><span class="sxs-lookup"><span data-stu-id="44b7f-441">Simulating Check Boxes in a Menu</span></span>

<span data-ttu-id="44b7f-442">Dieses Thema enthält ein Beispiel, das zeigt, wie Kontrollkästchen in einem Menü simuliert werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-442">This topic contains an example that shows how to simulate check boxes in a menu.</span></span> <span data-ttu-id="44b7f-443">Das Beispiel enthält ein Zeichen Menü, dessen Elemente es dem Benutzer ermöglichen, die Attribute "Bold", "Kursiv" und "unterstreichen" der aktuellen Schriftart festzulegen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-443">The example contains a Character menu whose items allow the user to set the bold, italic, and underline attributes of the current font.</span></span> <span data-ttu-id="44b7f-444">Wenn ein Schriftart Attribut in Kraft ist, wird im Kontrollkästchen neben dem entsprechenden Menü Element ein Häkchen angezeigt. Andernfalls wird neben dem Element ein leeres Kontrollkästchen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="44b7f-444">When a font attribute is in effect, a check mark is displayed in the check box next to the corresponding menu item; otherwise, an empty check box is displayed next to the item.</span></span>

<span data-ttu-id="44b7f-445">Im Beispiel wird die Standard Bitmap für das Häkchen durch zwei Bitmaps ersetzt: eine Bitmap mit einem aktivierten Kontrollkästchen und die Bitmap mit einem leeren Feld.</span><span class="sxs-lookup"><span data-stu-id="44b7f-445">The example replaces the default check-mark bitmap with two bitmaps: a bitmap with a selected check box and the bitmap with an empty box.</span></span> <span data-ttu-id="44b7f-446">Das aktivierte Kontrollkästchen Bitmap wird neben dem Menü Element Fett, kursiv oder unterstrichen angezeigt, wenn das Häkchen-Attribut des Elements auf **MF \_ aktiviert** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-446">The selected check box bitmap is displayed next to the Bold, Italic, or Underline menu item when the item's check-mark attribute is set to **MF\_CHECKED**.</span></span> <span data-ttu-id="44b7f-447">Das Kontrollkästchen Bitmap löschen oder leer wird angezeigt, wenn das Häkchen-Attribut auf **MF \_** deaktiviert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-447">The clear or empty check box bitmap is displayed when the check-mark attribute is set to **MF\_UNCHECKED**.</span></span>

<span data-ttu-id="44b7f-448">Das System stellt eine vordefinierte Bitmap bereit, die die für Kontrollkästchen und Options Felder verwendeten Bilder enthält.</span><span class="sxs-lookup"><span data-stu-id="44b7f-448">The system provides a predefined bitmap that contains the images used for check boxes and radio buttons.</span></span> <span data-ttu-id="44b7f-449">Im Beispiel werden die Kontrollkästchen aktiviert und leer isoliert, in zwei separate Bitmaps kopiert und dann als ausgewählte und gelöschte Bitmaps für Elemente im Menü **Zeichen** verwendet.</span><span class="sxs-lookup"><span data-stu-id="44b7f-449">The example isolates the selected and empty check boxes, copies them to two separate bitmaps, and then uses them as the selected and cleared bitmaps for items in the **Character** menu.</span></span>

<span data-ttu-id="44b7f-450">Zum Abrufen eines Handles für das System definierte Kontrollkästchen Bitmap Ruft das Beispiel die [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) -Funktion auf, wobei **null** als *HINSTANCE* -Parameter und **obm- \_ Kontrollkästchen** als *lpbitmapname* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="44b7f-450">To retrieve a handle to the system-defined check box bitmap, the example calls the [**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa) function, specifying **NULL** as the *hInstance* parameter and **OBM\_CHECKBOXES** as the *lpBitmapName* parameter.</span></span> <span data-ttu-id="44b7f-451">Da die Bilder in der Bitmap die gleiche Größe haben, kann das Beispiel diese isolieren, indem Sie die Breite und Höhe der Bitmap durch die Anzahl der Bilder in den Zeilen und Spalten dividiert.</span><span class="sxs-lookup"><span data-stu-id="44b7f-451">Because the images in the bitmap are all the same size, the example can isolate them by dividing the bitmap width and height by the number of images in its rows and columns.</span></span>

<span data-ttu-id="44b7f-452">Der folgende Teil einer Ressourcen Definitionsdatei zeigt, wie die Menü Elemente im Menü **Zeichen** definiert werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-452">The following portion of a resource-definition file shows how the menu items in the **Character** menu are defined.</span></span> <span data-ttu-id="44b7f-453">Beachten Sie, dass keine Schriftart Attribute anfänglich sind, sodass das Häkchen-Attribut für das **reguläre** Element auf ausgewählt festgelegt ist und das Häkchen-Attribut der restlichen Elemente standardmäßig auf Clear festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="44b7f-453">Note that no font attributes are in effect initially, so the check-mark attribute for the **Regular** item is set to selected and, by default, the check-mark attribute of the remaining items is set to clear.</span></span>


```
#include "men3.h" 
 
MainMenu MENU 
BEGIN 
    POPUP   "&Character" 
    BEGIN 
        MENUITEM    "&Regular",     IDM_REGULAR, CHECKED 
        MENUITEM SEPARATOR 
        MENUITEM    "&Bold",        IDM_BOLD 
        MENUITEM    "&Italic",      IDM_ITALIC 
        MENUITEM    "&Underline",   IDM_ULINE 
    END 
END
```



<span data-ttu-id="44b7f-454">Dies sind die relevanten Inhalte der Header Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="44b7f-454">Here are the relevant contents of the application's header file.</span></span>


```
// Menu-item identifiers  
 
#define IDM_REGULAR 0x1 
#define IDM_BOLD    0x2 
#define IDM_ITALIC  0x4 
#define IDM_ULINE   0x8 
 
// Check-mark flags  
 
#define CHECK   1 
#define UNCHECK 2 
 
// Font-attribute mask  
 
#define ATTRIBMASK 0xe 
 
// Function prototypes  
 
LRESULT APIENTRY MainWndProc(HWND, UINT, WPARAM, LPARAM); 
HBITMAP GetMyCheckBitmaps(UINT); 
BYTE CheckOrUncheckMenuItem(BYTE, HMENU); 
```



<span data-ttu-id="44b7f-455">Im folgenden Beispiel werden die Teile der Fenster Prozedur gezeigt, die die Prüfzeichen-Bitmaps erstellen. Legen Sie das Häkchen Attribut der Menü Elemente **Fett**, **kursiv** und unter **Streichung** fest. und zerstören Kontrollkästchen-Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="44b7f-455">The following example shows the portions of the window procedure that create the check-mark bitmaps; set the check-mark attribute of the **Bold**, **Italic**, and **Underline** menu items; and destroy check-mark bitmaps.</span></span>


```
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
 
    static HBITMAP hbmpCheck;   // handle to checked bitmap    
    static HBITMAP hbmpUncheck; // handle to unchecked bitmap  
    static HMENU hmenu;         // handle to main menu         
    BYTE fbFontAttrib;          // font-attribute flags        
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Call the application-defined GetMyCheckBitmaps 
            // function to get the predefined checked and 
            // unchecked check box bitmaps. 
 
            hbmpCheck = GetMyCheckBitmaps(CHECK); 
            hbmpUncheck = GetMyCheckBitmaps(UNCHECK); 
 
            // Set the checked and unchecked bitmaps for the menu 
            // items. 
 
            hmenu = GetMenu(hwndMain); 
            SetMenuItemBitmaps(hmenu, IDM_BOLD, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ITALIC, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
            SetMenuItemBitmaps(hmenu, IDM_ULINE, MF_BYCOMMAND, 
                hbmpUncheck, hbmpCheck); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the menu commands.  
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // CheckOrUncheckMenuItem is an application- 
                    // defined function that sets the menu item 
                    // checkmarks and returns the user-selected 
                    // font attributes. 
 
                    fbFontAttrib = CheckOrUncheckMenuItem( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // Set the font attributes.  
 
                    return 0; 
 
                // Process other command messages.  
 
                default: 
                    break; 
            } 
 
            break; 
 
        // Process other window messages.  
 
        case WM_DESTROY: 
 
            // Destroy the checked and unchecked bitmaps.  
 
            DeleteObject(hbmpCheck); 
            DeleteObject(hbmpUncheck); 
 
            PostQuitMessage(0); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
 
HBITMAP GetMyCheckBitmaps(UINT fuCheck) 
{ 
    COLORREF crBackground;  // background color                  
    HBRUSH hbrBackground;   // background brush                  
    HBRUSH hbrTargetOld;    // original background brush         
    HDC hdcSource;          // source device context             
    HDC hdcTarget;          // target device context             
    HBITMAP hbmpCheckboxes; // handle to check-box bitmap        
    BITMAP bmCheckbox;      // structure for bitmap data         
    HBITMAP hbmpSourceOld;  // handle to original source bitmap  
    HBITMAP hbmpTargetOld;  // handle to original target bitmap  
    HBITMAP hbmpCheck;      // handle to check-mark bitmap       
    RECT rc;                // rectangle for check-box bitmap    
    WORD wBitmapX;          // width of check-mark bitmap        
    WORD wBitmapY;          // height of check-mark bitmap       
 
    // Get the menu background color and create a solid brush 
    // with that color. 
 
    crBackground = GetSysColor(COLOR_MENU); 
    hbrBackground = CreateSolidBrush(crBackground); 
 
    // Create memory device contexts for the source and 
    // destination bitmaps. 
 
    hdcSource = CreateCompatibleDC((HDC) NULL); 
    hdcTarget = CreateCompatibleDC(hdcSource); 
 
    // Get the size of the system default check-mark bitmap and 
    // create a compatible bitmap of the same size. 
 
    wBitmapX = GetSystemMetrics(SM_CXMENUCHECK); 
    wBitmapY = GetSystemMetrics(SM_CYMENUCHECK); 
 
    hbmpCheck = CreateCompatibleBitmap(hdcSource, wBitmapX, 
        wBitmapY); 
 
    // Select the background brush and bitmap into the target DC. 
 
    hbrTargetOld = SelectObject(hdcTarget, hbrBackground); 
    hbmpTargetOld = SelectObject(hdcTarget, hbmpCheck); 
 
    // Use the selected brush to initialize the background color 
    // of the bitmap in the target device context. 
 
    PatBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, PATCOPY); 
 
    // Load the predefined check box bitmaps and select it 
    // into the source DC. 
 
    hbmpCheckboxes = LoadBitmap((HINSTANCE) NULL, 
        (LPTSTR) OBM_CHECKBOXES); 
 
    hbmpSourceOld = SelectObject(hdcSource, hbmpCheckboxes); 
 
    // Fill a BITMAP structure with information about the 
    // check box bitmaps, and then find the upper-left corner of 
    // the unchecked check box or the checked check box. 
 
    GetObject(hbmpCheckboxes, sizeof(BITMAP), &bmCheckbox); 
 
    if (fuCheck == UNCHECK) 
    { 
        rc.left = 0; 
        rc.right = (bmCheckbox.bmWidth / 4); 
    } 
    else 
    { 
        rc.left = (bmCheckbox.bmWidth / 4); 
        rc.right = (bmCheckbox.bmWidth / 4) * 2; 
    } 
 
    rc.top = 0; 
    rc.bottom = (bmCheckbox.bmHeight / 3); 
 
    // Copy the appropriate bitmap into the target DC. If the 
    // check-box bitmap is larger than the default check-mark 
    // bitmap, use StretchBlt to make it fit; otherwise, just 
    // copy it. 
 
    if (((rc.right - rc.left) > (int) wBitmapX) || 
            ((rc.bottom - rc.top) > (int) wBitmapY)) 
    {
        StretchBlt(hdcTarget, 0, 0, wBitmapX, wBitmapY, 
            hdcSource, rc.left, rc.top, rc.right - rc.left, 
            rc.bottom - rc.top, SRCCOPY); 
    }
 
    else 
    {
        BitBlt(hdcTarget, 0, 0, rc.right - rc.left, 
            rc.bottom - rc.top, 
            hdcSource, rc.left, rc.top, SRCCOPY); 
    }
 
    // Select the old source and destination bitmaps into the 
    // source and destination DCs, and then delete the DCs and 
    // the background brush. 
 
    SelectObject(hdcSource, hbmpSourceOld); 
    SelectObject(hdcTarget, hbrTargetOld); 
    hbmpCheck = SelectObject(hdcTarget, hbmpTargetOld); 
 
    DeleteObject(hbrBackground); 
    DeleteObject(hdcSource); 
    DeleteObject(hdcTarget); 
 
    // Return a handle to the new check-mark bitmap.  
 
    return hbmpCheck; 
} 
 
 
BYTE CheckOrUncheckMenuItem(BYTE bMenuItemID, HMENU hmenu) 
{ 
    DWORD fdwMenu; 
    static BYTE fbAttributes; 
 
    switch (bMenuItemID) 
    { 
        case IDM_REGULAR: 
 
            // Whenever the Regular menu item is selected, add a 
            // check mark to it and then remove checkmarks from 
            // any font-attribute menu items. 
 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_BOLD, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ITALIC, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
                CheckMenuItem(hmenu, IDM_ULINE, MF_BYCOMMAND | 
                    MF_UNCHECKED); 
            } 
            fbAttributes = IDM_REGULAR; 
            return fbAttributes; 
 
        case IDM_BOLD: 
        case IDM_ITALIC: 
        case IDM_ULINE: 
 
            // Toggle the check mark for the selected menu item and 
            // set the font attribute flags appropriately. 
 
            fdwMenu = GetMenuState(hmenu, (UINT) bMenuItemID, 
                MF_BYCOMMAND); 
            if (!(fdwMenu & MF_CHECKED)) 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes |= bMenuItemID; 
            }
            else 
            { 
                CheckMenuItem(hmenu, (UINT) bMenuItemID, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes ^= bMenuItemID; 
            } 
 
            // If any font attributes are currently selected, 
            // remove the check mark from the Regular menu item; 
            // if no attributes are selected, add a check mark 
            // to the Regular menu item. 
 
            if (fbAttributes & ATTRIBMASK) 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_UNCHECKED); 
                fbAttributes &= (BYTE) ~IDM_REGULAR; 
            }
            else 
            { 
                CheckMenuItem(hmenu, IDM_REGULAR, 
                    MF_BYCOMMAND | MF_CHECKED); 
                fbAttributes = IDM_REGULAR; 
            } 
 
            return fbAttributes; 
    } 
} 
```



### <a name="example-of-using-custom-check-mark-bitmaps"></a><span data-ttu-id="44b7f-456">Beispiel für die Verwendung von benutzerdefinierten Bitmaps für das Häkchen</span><span class="sxs-lookup"><span data-stu-id="44b7f-456">Example of Using Custom Check-mark Bitmaps</span></span>

<span data-ttu-id="44b7f-457">Im Beispiel in diesem Thema werden Menü Elementen benutzerdefinierte Bitmaps für das Häkchen in zwei Menüs zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-457">The example in this topic assigns custom check-mark bitmaps to menu items in two menus.</span></span> <span data-ttu-id="44b7f-458">Die Menü Elemente im ersten Menü geben Zeichen Attribute an: Fett, kursiv und unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-458">The menu items in the first menu specify character attributes: bold, italic, and underline.</span></span> <span data-ttu-id="44b7f-459">Jedes Menü Element kann entweder aktiviert oder deaktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="44b7f-459">Each menu item can be either selected or cleared.</span></span> <span data-ttu-id="44b7f-460">In diesem Beispiel werden für diese Menü Elemente Kontrollkästchen-Bitmaps verwendet, die den ausgewählten und gelöschten Zuständen eines Kontrollkästchen-Steuer Elements ähneln.</span><span class="sxs-lookup"><span data-stu-id="44b7f-460">For these menu items, the example uses check-mark bitmaps that resemble the selected and cleared states of a check box control.</span></span>

<span data-ttu-id="44b7f-461">Die Menü Elemente im zweiten Menü geben die Einstellungen für die Absatz Ausrichtung an: Links, zentriert und rechts.</span><span class="sxs-lookup"><span data-stu-id="44b7f-461">The menu items in the second menu specify paragraph alignment settings: left, centered, and right.</span></span> <span data-ttu-id="44b7f-462">Es wird immer nur eines dieser Menü Elemente ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="44b7f-462">Only one of these menu items is selected at any time.</span></span> <span data-ttu-id="44b7f-463">In diesem Beispiel werden für diese Menü Elemente Kontrollkästchen-Bitmaps verwendet, die den ausgewählten und unklaren Zuständen eines Optionsfeld-Steuer Elements ähneln.</span><span class="sxs-lookup"><span data-stu-id="44b7f-463">For these menu items, the example uses check-mark bitmaps that resemble the selected and clear states of a radio button control.</span></span>

<span data-ttu-id="44b7f-464">Die Fenster Prozedur verarbeitet die [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht, indem Sie die Anwendungs definierte OnCreate-Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-464">The window procedure processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message by calling the application-defined OnCreate function.</span></span> <span data-ttu-id="44b7f-465">`OnCreate` erstellt die vier Bitmaps für das Häkchen und weist diese dann den entsprechenden Menü Elementen mithilfe der [**setmenuitembitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) -Funktion zu.</span><span class="sxs-lookup"><span data-stu-id="44b7f-465">`OnCreate` creates the four check-mark bitmaps and then assigns them to their appropriate menu items by using the [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) function.</span></span>

<span data-ttu-id="44b7f-466">Um jede Bitmap zu erstellen, ruft OnCreate die Anwendungs definierte Funktion "roatemenubitmaps" auf und gibt einen Zeiger auf eine bitmapspezifische Zeichnungs Funktion an.</span><span class="sxs-lookup"><span data-stu-id="44b7f-466">To create each bitmap, OnCreate calls the application-defined CreateMenuBitmaps function, specifying a pointer to a bitmap-specific drawing function.</span></span> <span data-ttu-id="44b7f-467">"Anatemenubitmaps" erstellt eine monochrome Bitmap der erforderlichen Größe, wählt Sie in einen Speichergeräte Kontext aus und löscht den Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="44b7f-467">CreateMenuBitmaps creates a monochrome bitmap of the required size, selects it into a memory device context, and erases the background.</span></span> <span data-ttu-id="44b7f-468">Anschließend wird die angegebene Zeichnungs Funktion aufgerufen, um in den Vordergrund zu füllen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-468">Then it calls the specified drawing function to fill in the foreground.</span></span>

<span data-ttu-id="44b7f-469">Die vier Anwendungs definierten Zeichnungsfunktionen sind "drawcheck", "drawuncheck", " **drawradiocheck**" und "drawradiouncheck".</span><span class="sxs-lookup"><span data-stu-id="44b7f-469">The four application-defined drawing functions are DrawCheck, DrawUncheck, **DrawRadioCheck**, and DrawRadioUncheck.</span></span> <span data-ttu-id="44b7f-470">Sie zeichnen ein Rechteck mit einem X, einem leeren Rechteck, einer Ellipse, die eine kleinere Gefüllte Ellipse enthält, bzw. einer leeren Ellipse.</span><span class="sxs-lookup"><span data-stu-id="44b7f-470">They draw a rectangle with an X, an empty rectangle, an ellipse containing a smaller filled ellipse, and an empty ellipse, respectively.</span></span>

<span data-ttu-id="44b7f-471">Die Fenster Prozedur verarbeitet die [**WM \_**](/windows/desktop/winmsg/wm-destroy) -Lösch Nachricht, indem die Prüfzeichen-Bitmaps gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-471">The window procedure processes the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message by deleting the check-mark bitmaps.</span></span> <span data-ttu-id="44b7f-472">Alle bitmaphandles werden mithilfe der [**getmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) -Funktion abgerufen und dann ein Handle an die Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="44b7f-472">It retrieves each bitmap handle by using the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function and then passes a handle to the function.</span></span>

<span data-ttu-id="44b7f-473">Wenn der Benutzer ein Menü Element auswählt, wird eine [**WM- \_ Befehls**](wm-command.md) Meldung an das Besitzer Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="44b7f-473">When the user chooses a menu item, a [**WM\_COMMAND**](wm-command.md) message is sent to the owner window.</span></span> <span data-ttu-id="44b7f-474">Für Menü Elemente im Menü **Zeichen** Ruft die Fenster Prozedur die Anwendungs definierte checkcharakteritem-Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="44b7f-474">For menu items on the **Character** menu, the window procedure calls the application-defined CheckCharacterItem function.</span></span> <span data-ttu-id="44b7f-475">Für Elemente im **Absatz** Menü Ruft die Fenster Prozedur die Anwendungs definierte checkparagraphitem-Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="44b7f-475">For items on the **Paragraph** menu, the window procedure calls the application-defined CheckParagraphItem function.</span></span>

<span data-ttu-id="44b7f-476">Jedes Element im Menü " **Zeichen** " kann unabhängig voneinander ausgewählt und gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-476">Each item on the **Character** menu can be selected and cleared independently.</span></span> <span data-ttu-id="44b7f-477">Daher schaltet checkcharakteritem einfach den Überprüfungs Zustand des angegebenen Menü Elements.</span><span class="sxs-lookup"><span data-stu-id="44b7f-477">Therefore, CheckCharacterItem simply switches the specified menu item's check state.</span></span> <span data-ttu-id="44b7f-478">Zuerst Ruft die Funktion die [**getmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) -Funktion auf, um den aktuellen Menü Element Zustand zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="44b7f-478">First, the function calls the [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) function to get the current menu item state.</span></span> <span data-ttu-id="44b7f-479">Anschließend schaltet er das Flag für aktivierte **MFS \_** -Zustände um und legt den neuen Status durch Aufrufen der Funktion [**setmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) fest.</span><span class="sxs-lookup"><span data-stu-id="44b7f-479">Then it switches the **MFS\_CHECKED** state flag and sets the new state by calling the [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) function.</span></span>

<span data-ttu-id="44b7f-480">Im Gegensatz zu Zeichen Attributen kann jeweils nur eine Absatz Ausrichtung ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="44b7f-480">Unlike character attributes, only one paragraph alignment can be selected at a time.</span></span> <span data-ttu-id="44b7f-481">Daher prüft checkparagphitem das angegebene Menü Element und entfernt das Häkchen aus allen anderen Elementen im Menü.</span><span class="sxs-lookup"><span data-stu-id="44b7f-481">Therefore, CheckParagraphItem checks the specified menu item and removes the check mark from all other items on the menu.</span></span> <span data-ttu-id="44b7f-482">Zu diesem Zweck wird die [**checkmenuradioitem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) -Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="44b7f-482">To do so, it calls the [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) function.</span></span>

<span data-ttu-id="44b7f-483">Im folgenden finden Sie die relevanten Teile der Header Datei der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="44b7f-483">Following are the relevant portions of the application's header file.</span></span>


```
// Menu-item identifiers for the Character menu 
 
#define IDM_CHARACTER 10 
#define IDM_BOLD      11 
#define IDM_ITALIC    12 
#define IDM_UNDERLINE 13 
 
// Menu-item identifiers for the Paragraph menu 
 
#define IDM_PARAGRAPH 20 
#define IDM_LEFT      21 
#define IDM_CENTER    22 
#define IDM_RIGHT     23 
 
// Function-pointer type for drawing functions 
 
typedef VOID (WINAPI * DRAWFUNC)(HDC hdc, SIZE size); 
 
```



<span data-ttu-id="44b7f-484">Im folgenden sind die relevanten Teile der Fenster Prozedur der Anwendung und zugehöriger Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="44b7f-484">The following are the relevant portions of the application's window procedure and related functions.</span></span>


```
LRESULT CALLBACK MainWindowProc( 
        HWND hwnd, 
        UINT uMsg, 
        WPARAM wParam, 
        LPARAM lParam 
        ) 
{ 
    switch (uMsg) 
    { 
        case WM_CREATE: 
            if (!OnCreate(hwnd)) 
                return -1; 
            break; 
 
        case WM_DESTROY: 
            OnDestroy(hwnd); 
            PostQuitMessage(0); 
            break; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_UNDERLINE: 
                    CheckCharacterItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                case IDM_LEFT: 
                case IDM_CENTER: 
                case IDM_RIGHT: 
                    CheckParagraphItem(hwnd, LOWORD(wParam)); 
                    break; 
 
                // Process other commands here. 
 
            } 
            break; 
 
        // Process other messages here. 
 
        default: 
            return DefWindowProc(hwnd, uMsg, wParam, lParam); 
    } 
    return 0; 
} 
 
VOID WINAPI CheckCharacterItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the state of the specified menu item. 
 
    mii.fMask = MIIM_STATE;    // information to get 
    GetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
 
    // Toggle the checked state. 
 
    mii.fState ^= MFS_CHECKED; 
    SetMenuItemInfo(hmenuPopup, uID, FALSE, &mii); 
} 
 
VOID WINAPI CheckParagraphItem(HWND hwnd, UINT uID) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;  // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Check the specified item and uncheck all the others. 
 
    CheckMenuRadioItem( 
            hmenuPopup,         // handle to menu 
            IDM_LEFT,           // first item in range 
            IDM_RIGHT,          // last item in range 
            uID,                // item to check 
            MF_BYCOMMAND        // IDs, not positions 
            ); 
} 
 
BOOL WINAPI OnCreate(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
    UINT uID; 
    HBITMAP hbmChecked; 
    HBITMAP hbmUnchecked; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_BOLD; uID <= IDM_UNDERLINE; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Get a handle to the Paragraph pop-up menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Create the checked and unchecked bitmaps. 
 
    hbmChecked = CreateMenuBitmap(DrawRadioCheck); 
    hbmUnchecked = CreateMenuBitmap(DrawRadioUncheck); 
 
    // Set the check-mark bitmaps for each menu item. 
 
    for (uID = IDM_LEFT; uID <= IDM_RIGHT; uID++) 
    { 
        SetMenuItemBitmaps(hmenuPopup, uID, MF_BYCOMMAND, 
                hbmUnchecked, hbmChecked); 
    } 
 
    // Initially check the IDM_LEFT paragraph item. 
 
    CheckMenuRadioItem(hmenuPopup, IDM_LEFT, IDM_RIGHT, 
            IDM_LEFT, MF_BYCOMMAND); 
    return TRUE; 
} 
 
HBITMAP WINAPI CreateMenuBitmap(DRAWFUNC lpfnDraw) 
{ 
    // Create a DC compatible with the desktop window's DC. 
 
    HWND hwndDesktop = GetDesktopWindow(); 
    HDC hdcDesktop = GetDC(hwndDesktop); 
    HDC hdcMem = CreateCompatibleDC(hdcDesktop); 
 
    // Determine the required bitmap size. 
 
    SIZE size = { GetSystemMetrics(SM_CXMENUCHECK), 
                  GetSystemMetrics(SM_CYMENUCHECK) }; 
 
    // Create a monochrome bitmap and select it. 
 
    HBITMAP hbm = CreateBitmap(size.cx, size.cy, 1, 1, NULL); 
    HBITMAP hbmOld = SelectObject(hdcMem, hbm); 
 
    // Erase the background and call the drawing function. 
 
    PatBlt(hdcMem, 0, 0, size.cx, size.cy, WHITENESS); 
    (*lpfnDraw)(hdcMem, size); 
 
    // Clean up. 
 
    SelectObject(hdcMem, hbmOld); 
    DeleteDC(hdcMem); 
    ReleaseDC(hwndDesktop, hdcDesktop); 
    return hbm; 
} 
 
VOID WINAPI DrawCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    MoveToEx(hdc, 0, 0, NULL); 
    LineTo(hdc, size.cx, size.cy); 
    MoveToEx(hdc, 0, size.cy - 1, NULL); 
    LineTo(hdc, size.cx - 1, 0); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Rectangle(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioCheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, GetStockObject(BLACK_BRUSH)); 
    Ellipse(hdc, 2, 2, size.cx - 2, size.cy - 2); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI DrawRadioUncheck(HDC hdc, SIZE size) 
{ 
    HBRUSH hbrOld; 
    hbrOld = SelectObject(hdc, GetStockObject(NULL_BRUSH)); 
    Ellipse(hdc, 0, 0, size.cx, size.cy); 
    SelectObject(hdc, hbrOld); 
} 
 
VOID WINAPI OnDestroy(HWND hwnd) 
{ 
    HMENU hmenuBar = GetMenu(hwnd); 
    HMENU hmenuPopup; 
    MENUITEMINFO mii; 
 
    // Get a handle to the Character menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_CHARACTER, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_BOLD, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
 
    // Get a handle to the Paragraph menu. 
 
    mii.fMask = MIIM_SUBMENU;     // information to get 
    GetMenuItemInfo(hmenuBar, IDM_PARAGRAPH, FALSE, &mii); 
    hmenuPopup = mii.hSubMenu; 
 
    // Get the check-mark bitmaps and delete them. 
 
    mii.fMask = MIIM_CHECKMARKS; 
    GetMenuItemInfo(hmenuPopup, IDM_LEFT, FALSE, &mii); 
    DeleteObject(mii.hbmpChecked); 
    DeleteObject(mii.hbmpUnchecked); 
} 
```



 

 