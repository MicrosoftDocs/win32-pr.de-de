---
title: Verwenden von Tastatur Accelerators
description: In diesem Abschnitt werden Aufgaben beschrieben, die mit Tastatur Accelerators verknüpft sind.
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- Benutzereingabe, Tastaturbeschleuniger
- Erfassen von Benutzereingaben, Tastatur Accelerators
- Tastaturbeschleuniger
- Accelerators
- Zugriffstasten Tabellen
- Zugriffstasten-Tabellen Ressourcen
- Übersetzen der Beschleunigungs Funktion
- WM_COMMAND Meldung
- WM_SYS Befehls Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2241ba828ea9e6be5e4bb0b7471adcc3130940ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038977"
---
# <a name="using-keyboard-accelerators"></a><span data-ttu-id="1f473-112">Verwenden von Tastatur Accelerators</span><span class="sxs-lookup"><span data-stu-id="1f473-112">Using Keyboard Accelerators</span></span>

<span data-ttu-id="1f473-113">In diesem Abschnitt werden Aufgaben beschrieben, die mit Tastatur Accelerators verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1f473-113">This section covers tasks that are associated with keyboard accelerators.</span></span>

-   [<span data-ttu-id="1f473-114">Verwenden einer Zugriffstasten-Tabellen Ressource</span><span class="sxs-lookup"><span data-stu-id="1f473-114">Using an Accelerator Table Resource</span></span>](#using-an-accelerator-table-resource)
    -   [<span data-ttu-id="1f473-115">Erstellen der Zugriffstasten-Tabellen Ressource</span><span class="sxs-lookup"><span data-stu-id="1f473-115">Creating the Accelerator Table Resource</span></span>](#creating-the-accelerator-table-resource)
    -   [<span data-ttu-id="1f473-116">Laden der Zugriffstasten-Tabellen Ressource</span><span class="sxs-lookup"><span data-stu-id="1f473-116">Loading the Accelerator Table Resource</span></span>](#loading-the-accelerator-table-resource)
    -   [<span data-ttu-id="1f473-117">Aufrufen der Translation Accelerator-Funktion</span><span class="sxs-lookup"><span data-stu-id="1f473-117">Calling the Translate Accelerator Function</span></span>](#calling-the-translate-accelerator-function)
    -   [<span data-ttu-id="1f473-118">Verarbeiten von WM- \_ Befehls Meldungen</span><span class="sxs-lookup"><span data-stu-id="1f473-118">Processing WM\_COMMAND Messages</span></span>](/windows)
    -   [<span data-ttu-id="1f473-119">Zerstören der Zugriffstasten-Tabellen Ressource</span><span class="sxs-lookup"><span data-stu-id="1f473-119">Destroying the Accelerator Table Resource</span></span>](#destroying-the-accelerator-table-resource)
    -   [<span data-ttu-id="1f473-120">Erstellen von Accelerators für Schriftart Attribute</span><span class="sxs-lookup"><span data-stu-id="1f473-120">Creating Accelerators for Font Attributes</span></span>](#creating-accelerators-for-font-attributes)
-   [<span data-ttu-id="1f473-121">Verwenden einer Zugriffstasten Tabelle, die zur Laufzeit erstellt wird</span><span class="sxs-lookup"><span data-stu-id="1f473-121">Using an Accelerator Table Created at Run Time</span></span>](#using-an-accelerator-table-created-at-run-time)
    -   [<span data-ttu-id="1f473-122">Erstellen einer Run-Time Accelerator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="1f473-122">Creating a Run-Time Accelerator Table</span></span>](#creating-a-run-time-accelerator-table)
    -   [<span data-ttu-id="1f473-123">Verarbeiten von Accelerators</span><span class="sxs-lookup"><span data-stu-id="1f473-123">Processing Accelerators</span></span>](#processing-accelerators)
    -   [<span data-ttu-id="1f473-124">Zerstören einer Run-Time Accelerator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="1f473-124">Destroying a Run-Time Accelerator Table</span></span>](#destroying-a-run-time-accelerator-table)
    -   [<span data-ttu-id="1f473-125">Erstellen von Benutzer bearbeitbaren Acceleratoren</span><span class="sxs-lookup"><span data-stu-id="1f473-125">Creating User Editable Accelerators</span></span>](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a><span data-ttu-id="1f473-126">Verwenden einer Zugriffstasten-Tabellen Ressource</span><span class="sxs-lookup"><span data-stu-id="1f473-126">Using an Accelerator Table Resource</span></span>

<span data-ttu-id="1f473-127">Die gängigste Methode zum Hinzufügen von Zugriffstasten für eine Anwendung ist das Einschließen einer Zugriffstasten-Tabellen Ressource mit der ausführbaren Datei der Anwendung und das anschließende Laden der Ressource zur Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="1f473-127">The most common way to add accelerator support to an application is to include an accelerator-table resource with the application's executable file and then load the resource at run time.</span></span>

<span data-ttu-id="1f473-128">In diesem Abschnitt werden die folgenden Themen behandelt.</span><span class="sxs-lookup"><span data-stu-id="1f473-128">This section covers the following topics.</span></span>

-   [<span data-ttu-id="1f473-129">Erstellen der Zugriffstasten-Tabellen Ressource</span><span class="sxs-lookup"><span data-stu-id="1f473-129">Creating the Accelerator Table Resource</span></span>](#creating-the-accelerator-table-resource)
-   [<span data-ttu-id="1f473-130">Laden der Zugriffstasten-Tabellen Ressource</span><span class="sxs-lookup"><span data-stu-id="1f473-130">Loading the Accelerator Table Resource</span></span>](#loading-the-accelerator-table-resource)
-   [<span data-ttu-id="1f473-131">Aufrufen der Translation Accelerator-Funktion</span><span class="sxs-lookup"><span data-stu-id="1f473-131">Calling the Translate Accelerator Function</span></span>](#calling-the-translate-accelerator-function)
-   [<span data-ttu-id="1f473-132">Verarbeiten von WM- \_ Befehls Meldungen</span><span class="sxs-lookup"><span data-stu-id="1f473-132">Processing WM\_COMMAND Messages</span></span>](/windows)
-   [<span data-ttu-id="1f473-133">Zerstören der Zugriffstasten-Tabellen Ressource</span><span class="sxs-lookup"><span data-stu-id="1f473-133">Destroying the Accelerator Table Resource</span></span>](#destroying-the-accelerator-table-resource)
-   [<span data-ttu-id="1f473-134">Erstellen von Accelerators für Schriftart Attribute</span><span class="sxs-lookup"><span data-stu-id="1f473-134">Creating Accelerators for Font Attributes</span></span>](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a><span data-ttu-id="1f473-135">Erstellen der Zugriffstasten-Tabellen Ressource</span><span class="sxs-lookup"><span data-stu-id="1f473-135">Creating the Accelerator Table Resource</span></span>

<span data-ttu-id="1f473-136">Sie erstellen eine Accelerator-Table-Ressource, indem Sie die [Accelerators](./accelerators-resource.md) -Anweisung in der Ressourcen Definitionsdatei Ihrer Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f473-136">You create an accelerator-table resource by using the [ACCELERATORS](./accelerators-resource.md) statement in your application's resource-definition file.</span></span> <span data-ttu-id="1f473-137">Sie müssen der Zugriffstasten Tabelle einen Namen oder Ressourcen Bezeichner zuweisen, vorzugsweise im Gegensatz zu allen anderen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="1f473-137">You must assign a name or resource identifier to the accelerator table, preferably unlike that of any other resource.</span></span> <span data-ttu-id="1f473-138">Das System verwendet diesen Bezeichner, um die Ressource zur Laufzeit zu laden.</span><span class="sxs-lookup"><span data-stu-id="1f473-138">The system uses this identifier to load the resource at run time.</span></span>

<span data-ttu-id="1f473-139">Jede Zugriffstaste, die Sie definieren, erfordert einen separaten Eintrag in der Zugriffstasten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1f473-139">Each accelerator you define requires a separate entry in the accelerator table.</span></span> <span data-ttu-id="1f473-140">In jedem Eintrag definieren Sie den Tastatur Schlag (entweder einen ASCII-Zeichencode oder einen Code für den virtuellen Schlüssel), der die Zugriffstaste und den Bezeichner der Zugriffstaste generiert.</span><span class="sxs-lookup"><span data-stu-id="1f473-140">In each entry, you define the keystroke (either an ASCII character code or virtual-key code) that generates the accelerator and the accelerator's identifier.</span></span> <span data-ttu-id="1f473-141">Außerdem müssen Sie angeben, ob der Tastatur Strich in einer Kombination mit der alt-, UMSCHALT-oder STRG-Taste verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="1f473-141">You must also specify whether the keystroke must be used in some combination with the ALT, SHIFT, or CTRL keys.</span></span> <span data-ttu-id="1f473-142">Weitere Informationen zu virtuellen Schlüsseln finden Sie unter [Tastatureingabe](/windows/desktop/inputdev/keyboard-input).</span><span class="sxs-lookup"><span data-stu-id="1f473-142">For more information about virtual keys, see [Keyboard Input](/windows/desktop/inputdev/keyboard-input).</span></span>

<span data-ttu-id="1f473-143">Ein ASCII-Tastatur Strich wird entweder durch Einschließen des ASCII-Zeichens in doppelte Anführungszeichen oder durch Verwendung des ganzzahligen Werts des Zeichens in Kombination mit dem ASCII-Flag angegeben.</span><span class="sxs-lookup"><span data-stu-id="1f473-143">An ASCII keystroke is specified either by enclosing the ASCII character in double quotation marks or by using the integer value of the character in combination with the ASCII flag.</span></span> <span data-ttu-id="1f473-144">In den folgenden Beispielen wird gezeigt, wie Sie ASCII-Beschleuniger definieren.</span><span class="sxs-lookup"><span data-stu-id="1f473-144">The following examples show how to define ASCII accelerators.</span></span>

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

<span data-ttu-id="1f473-145">Eine Tastenkombination für den Code eines virtuellen Schlüssels wird unterschiedlich angegeben, je nachdem, ob es sich bei der Tastatureingabe um einen alphanumerischen Schlüssel oder um einen nicht alphanumerischen Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="1f473-145">A virtual-key code keystroke is specified differently depending on whether the keystroke is an alphanumeric key or a non-alphanumeric key.</span></span> <span data-ttu-id="1f473-146">Bei einem alphanumerischen Schlüssel wird der Buchstabe oder die Zahl des Schlüssels, der in doppelte Anführungszeichen eingeschlossen ist, mit dem **VIRTKEY** -Flag kombiniert.</span><span class="sxs-lookup"><span data-stu-id="1f473-146">For an alphanumeric key, the key's letter or number, enclosed in double quotation marks, is combined with the **VIRTKEY** flag.</span></span> <span data-ttu-id="1f473-147">Bei einem nicht alphanumerischen Schlüssel wird der Code für den virtuellen Schlüssel für den jeweiligen Schlüssel mit dem **VIRTKEY** -Flag kombiniert.</span><span class="sxs-lookup"><span data-stu-id="1f473-147">For a non-alphanumeric key, the virtual-key code for the specific key is combined with the **VIRTKEY** flag.</span></span> <span data-ttu-id="1f473-148">In den folgenden Beispielen wird veranschaulicht, wie Sie Code Accelerators für virtuelle Schlüssel definieren.</span><span class="sxs-lookup"><span data-stu-id="1f473-148">The following examples show how to define virtual-key code accelerators.</span></span>

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

<span data-ttu-id="1f473-149">Das folgende Beispiel zeigt eine Zugriffstaste für eine Ressource, die Accelerators für Datei Vorgänge definiert.</span><span class="sxs-lookup"><span data-stu-id="1f473-149">The following example shows an accelerator-table resource that defines accelerators for file operations.</span></span> <span data-ttu-id="1f473-150">Der Name der Ressource ist " *fileaccel*".</span><span class="sxs-lookup"><span data-stu-id="1f473-150">The name of the resource is *FileAccel*.</span></span>

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

<span data-ttu-id="1f473-151">Wenn Sie möchten, dass der Benutzer die Alt-Taste, die UMSCHALTTASTE oder die STRG-Taste in einer Kombination mit der Zugriffstaste drücken, geben Sie die alt-, UMSCHALT-und steuerungflags in der Zugriffstasten Definition an.</span><span class="sxs-lookup"><span data-stu-id="1f473-151">If you want the user to press the ALT, SHIFT, or CTRL keys in some combination with the accelerator keystroke, specify the ALT, SHIFT, and CONTROL flags in the accelerator's definition.</span></span> <span data-ttu-id="1f473-152">Hier einige Beispiele.</span><span class="sxs-lookup"><span data-stu-id="1f473-152">Following are some examples.</span></span>

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

<span data-ttu-id="1f473-153">Wenn eine Zugriffstaste einem Menü Element entspricht, hebt das System standardmäßig das Menü Element hervor.</span><span class="sxs-lookup"><span data-stu-id="1f473-153">By default, when an accelerator key corresponds to a menu item, the system highlights the menu item.</span></span> <span data-ttu-id="1f473-154">Sie können das **noinvert** -Flag verwenden, um die Hervorhebung für eine einzelne Zugriffstaste zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="1f473-154">You can use the **NOINVERT** flag to prevent highlighting for an individual accelerator.</span></span> <span data-ttu-id="1f473-155">Im folgenden Beispiel wird gezeigt, wie das **noinvert** -Flag verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="1f473-155">The following example shows how to use the **NOINVERT** flag:</span></span>

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

<span data-ttu-id="1f473-156">Zum Definieren von Accelerators, die Menü Elementen in der Anwendung entsprechen, fügen Sie die Zugriffstasten in den Text der Menü Elemente ein.</span><span class="sxs-lookup"><span data-stu-id="1f473-156">To define accelerators that correspond to menu items in your application, include the accelerators in the text of the menu items.</span></span> <span data-ttu-id="1f473-157">Im folgenden Beispiel wird gezeigt, wie Acceleratoren in Menü Element Text in eine Ressourcen Definitionsdatei eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="1f473-157">The following example shows how to include accelerators in menu-item text in a resource-definition file.</span></span>

``` syntax
FilePopup MENU 
BEGIN 
    POPUP   "&File" 
    BEGIN 
        MENUITEM    "&New..",           IDM_NEW 
        MENUITEM    "&Open\tCtrl+F12",  IDM_OPEN 
        MENUITEM    "&Close\tAlt+F4"    IDM_CLOSE 
        MENUITEM    "&Save\tShift+F12", IDM_SAVE 
        MENUITEM    "Save &As...\tF12", IDM_SAVEAS 
    END 
END 
```

### <a name="loading-the-accelerator-table-resource"></a><span data-ttu-id="1f473-158">Laden der Zugriffstasten-Tabellen Ressource</span><span class="sxs-lookup"><span data-stu-id="1f473-158">Loading the Accelerator Table Resource</span></span>

<span data-ttu-id="1f473-159">Eine Anwendung lädt eine Accelerator-Table-Ressource, indem Sie die [**loadaccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) -Funktion aufruft und den Instanzhandle für die Anwendung angibt, deren ausführbare Datei die Ressource und den Namen oder Bezeichner der Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="1f473-159">An application loads an accelerator-table resource by calling the [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) function and specifying the instance handle to the application whose executable file contains the resource and the name or identifier of the resource.</span></span> <span data-ttu-id="1f473-160">**Loadaccelerators** lädt die angegebene Zugriffstasten Tabelle in den Arbeitsspeicher und gibt das Handle an die Zugriffstasten Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="1f473-160">**LoadAccelerators** loads the specified accelerator table into memory and returns the handle to the accelerator table.</span></span>

<span data-ttu-id="1f473-161">Eine Anwendung kann jederzeit eine Accelerator-Table-Ressource laden.</span><span class="sxs-lookup"><span data-stu-id="1f473-161">An application can load an accelerator-table resource at any time.</span></span> <span data-ttu-id="1f473-162">Normalerweise lädt eine Single Thread-Anwendung die Zugriffstasten Tabelle, bevor Sie die Hauptnachrichten Schleife eingibt.</span><span class="sxs-lookup"><span data-stu-id="1f473-162">Usually, a single-threaded application loads its accelerator table before entering its main message loop.</span></span> <span data-ttu-id="1f473-163">Eine Anwendung, die mehrere Threads verwendet, lädt in der Regel die Zugriffstasten-Tabellen Ressource für einen Thread, bevor die Nachrichten Schleife für den Thread eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1f473-163">An application that uses multiple threads typically loads the accelerator-table resource for a thread before entering the message loop for the thread.</span></span> <span data-ttu-id="1f473-164">Eine Anwendung oder ein Thread kann auch mehrere Zugriffstasten Tabellen verwenden, die jeweils einem bestimmten Fenster in der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1f473-164">An application or thread might also use multiple accelerator tables, each associated with a particular window in the application.</span></span> <span data-ttu-id="1f473-165">Eine solche Anwendung lädt die Zugriffstasten Tabelle für das Fenster jedes Mal, wenn der Benutzer das Fenster aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="1f473-165">Such an application would load the accelerator table for the window each time the user activated the window.</span></span> <span data-ttu-id="1f473-166">Weitere Informationen zu Threads finden Sie unter [Prozesse und Threads](/windows/desktop/ProcThread/processes-and-threads).</span><span class="sxs-lookup"><span data-stu-id="1f473-166">For more information about threads, see [Processes and Threads](/windows/desktop/ProcThread/processes-and-threads).</span></span>

### <a name="calling-the-translate-accelerator-function"></a><span data-ttu-id="1f473-167">Aufrufen der Translation Accelerator-Funktion</span><span class="sxs-lookup"><span data-stu-id="1f473-167">Calling the Translate Accelerator Function</span></span>

<span data-ttu-id="1f473-168">Zum Verarbeiten von Accelerators muss die Nachrichten Schleife einer Anwendung (oder des Threads) einen aufrufsvorgang der [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) -Funktion enthalten.</span><span class="sxs-lookup"><span data-stu-id="1f473-168">To process accelerators, an application's (or thread's) message loop must contain a call to the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function.</span></span> <span data-ttu-id="1f473-169">**TranslateAccelerator** vergleicht Tastatureingaben mit einer Zugriffstasten Tabelle und übersetzt die Tastatureingaben in eine [**WM- \_ Befehls**](wm-command.md) Meldung (oder eine [**WM- \_ syscommand**](wm-syscommand.md)-Meldung), wenn eine Entsprechung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="1f473-169">**TranslateAccelerator** compares keystrokes to an accelerator table and, if it finds a match, translates the keystrokes into a [**WM\_COMMAND**](wm-command.md) (or [**WM\_SYSCOMMAND**](wm-syscommand.md)) message.</span></span> <span data-ttu-id="1f473-170">Die-Funktion sendet die Nachricht dann an eine Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="1f473-170">The function then sends the message to a window procedure.</span></span> <span data-ttu-id="1f473-171">Die Parameter der **TranslateAccelerator** -Funktion enthalten das Handle für das Fenster, das die WM- **\_ Befehls** Meldungen empfängt, das Handle für die Zugriffstasten Tabelle, die zum Übersetzen von Acceleratoren verwendet wird, und einen Zeiger auf eine [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur, die eine Nachricht aus der Warteschlange enthält.</span><span class="sxs-lookup"><span data-stu-id="1f473-171">The parameters of the **TranslateAccelerator** function include the handle to the window that is to receive the **WM\_COMMAND** messages, the handle to the accelerator table used to translate accelerators, and a pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure containing a message from the queue.</span></span> <span data-ttu-id="1f473-172">Im folgenden Beispiel wird gezeigt, wie Sie **TranslateAccelerator** aus einer Nachrichten Schleife heraus abrufen können.</span><span class="sxs-lookup"><span data-stu-id="1f473-172">The following example shows how to call **TranslateAccelerator** from within a message loop.</span></span>


```
MSG msg;
BOOL bRet;

while ( (bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1) 
    {
        // handle the error and possibly exit
    }
    else
    { 
        // Check for accelerator keystrokes. 
     
        if (!TranslateAccelerator( 
                hwndMain,      // handle to receiving window 
                haccel,        // handle to active accelerator table 
                &msg))         // message data 
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



### <a name="processing-wm_command-messages"></a><span data-ttu-id="1f473-173">Verarbeiten von WM- \_ Befehls Meldungen</span><span class="sxs-lookup"><span data-stu-id="1f473-173">Processing WM\_COMMAND Messages</span></span>

<span data-ttu-id="1f473-174">Wenn eine Zugriffstaste verwendet wird, empfängt das in der [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) -Funktion angegebene Fenster einen [**WM- \_ Befehl**](wm-command.md) oder eine [**WM- \_ syscommand**](wm-syscommand.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1f473-174">When an accelerator is used, the window specified in the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function receives a [**WM\_COMMAND**](wm-command.md) or [**WM\_SYSCOMMAND**](wm-syscommand.md) message.</span></span> <span data-ttu-id="1f473-175">Das nieder wertige Wort des *wParam* -Parameters enthält den Bezeichner der Zugriffstaste.</span><span class="sxs-lookup"><span data-stu-id="1f473-175">The low-order word of the *wParam* parameter contains the identifier of the accelerator.</span></span> <span data-ttu-id="1f473-176">Die Fenster Prozedur überprüft den Bezeichner, um die Quelle der **WM- \_ Befehls** Nachricht zu bestimmen und die Nachricht entsprechend zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1f473-176">The window procedure examines the identifier to determine the source of the **WM\_COMMAND** message and process the message accordingly.</span></span>

<span data-ttu-id="1f473-177">Wenn eine Zugriffstaste einem Menü Element in der Anwendung entspricht, wird in der Regel die Zugriffstaste und das Menü Element dem gleichen Bezeichner zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1f473-177">Typically, if an accelerator corresponds to a menu item in the application, the accelerator and menu item are assigned the same identifier.</span></span> <span data-ttu-id="1f473-178">Wenn Sie wissen möchten, ob eine [**WM- \_ Befehls**](wm-command.md) Nachricht von einer Zugriffstaste oder einem Menü Element generiert wurde, können Sie das höchst wertige Wort des *wParam* -Parameters überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1f473-178">If you need to know whether a [**WM\_COMMAND**](wm-command.md) message was generated by an accelerator or by a menu item, you can examine the high-order word of the *wParam* parameter.</span></span> <span data-ttu-id="1f473-179">Wenn eine Zugriffstaste die Meldung generiert hat, ist das höchst wertige Wort 1. Wenn ein Menü Element die Meldung generiert hat, ist das höchst wertige Wort 0.</span><span class="sxs-lookup"><span data-stu-id="1f473-179">If an accelerator generated the message, the high-order word is 1; if a menu item generated the message, the high-order word is 0.</span></span>

### <a name="destroying-the-accelerator-table-resource"></a><span data-ttu-id="1f473-180">Zerstören der Zugriffstasten-Tabellen Ressource</span><span class="sxs-lookup"><span data-stu-id="1f473-180">Destroying the Accelerator Table Resource</span></span>

<span data-ttu-id="1f473-181">Das System zerstört die von der [**loadaccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) -Funktion geladenen acceleratortabellenressourcen automatisch und entfernt die Ressource nach dem Schließen der Anwendung aus dem Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1f473-181">The system automatically destroys accelerator-table resources loaded by the [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) function, removing the resource from memory after the application closes.</span></span>

### <a name="creating-accelerators-for-font-attributes"></a><span data-ttu-id="1f473-182">Erstellen von Accelerators für Schriftart Attribute</span><span class="sxs-lookup"><span data-stu-id="1f473-182">Creating Accelerators for Font Attributes</span></span>

<span data-ttu-id="1f473-183">Das Beispiel in diesem Abschnitt zeigt, wie die folgenden Aufgaben ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="1f473-183">The example in this section shows how to perform the following tasks:</span></span>

-   <span data-ttu-id="1f473-184">Erstellen Sie eine Zugriffstaste für eine Ressource.</span><span class="sxs-lookup"><span data-stu-id="1f473-184">Create an accelerator-table resource.</span></span>
-   <span data-ttu-id="1f473-185">Lädt die Zugriffstasten Tabelle zur Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="1f473-185">Load the accelerator table at run time.</span></span>
-   <span data-ttu-id="1f473-186">Übersetzen Sie Accelerators in einer Nachrichten Schleife.</span><span class="sxs-lookup"><span data-stu-id="1f473-186">Translate accelerators in a message loop.</span></span>
-   <span data-ttu-id="1f473-187">Prozess [**WM- \_ Befehls**](wm-command.md) Meldungen, die von den Accelerators generiert werden.</span><span class="sxs-lookup"><span data-stu-id="1f473-187">Process [**WM\_COMMAND**](wm-command.md) messages generated by the accelerators.</span></span>

<span data-ttu-id="1f473-188">Diese Aufgaben werden im Kontext einer Anwendung veranschaulicht, die ein **Zeichen** Menü und entsprechende Acceleratoren enthält, mit denen der Benutzerattribute der aktuellen Schriftart auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="1f473-188">These tasks are demonstrated in the context of an application that includes a **Character** menu and corresponding accelerators that allow the user to select attributes of the current font.</span></span>

<span data-ttu-id="1f473-189">Der folgende Teil einer Ressourcen Definitionsdatei definiert das **Zeichen** Menü und die zugehörige Zugriffstasten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1f473-189">The following portion of a resource-definition file defines the **Character** menu and the associated accelerator table.</span></span> <span data-ttu-id="1f473-190">Beachten Sie, dass die Menü Elemente die Tastenkombinationen anzeigen und dass jede Zugriffstaste denselben Bezeichner wie das zugehörige Menü Element aufweist.</span><span class="sxs-lookup"><span data-stu-id="1f473-190">Note that the menu items show the accelerator keystrokes and that each accelerator has the same identifier as its associated menu item.</span></span>


```
#include <windows.h> 
#include "acc.h" 
 
MainMenu MENU 
{ 
    POPUP   "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```



<span data-ttu-id="1f473-191">Die folgenden Abschnitte aus der Quelldatei der Anwendung veranschaulichen, wie die Accelerators implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="1f473-191">The following sections from the application's source file show how to implement the accelerators.</span></span>


```
HWND hwndMain;      // handle to main window 
HANDLE hinstAcc;    // handle to application instance 
int WINAPI WinMain(HINSTANCE hinst, HINSTANCE hinstPrev, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg;            // application messages 
    BOOL bRet;          // for return value of GetMessage
    HACCEL haccel;      // handle to accelerator table 
 
    // Perform the initialization procedure. 
 
    // Create a main window for this application instance. 
 
    hwndMain = CreateWindowEx(0L, "MainWindowClass", 
        "Sample Application", WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, 
        hinst, NULL ); 
 
    // If a window cannot be created, return "failure." 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Make the window visible and update its client area. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Load the accelerator table. 
 
    haccel = LoadAccelerators(hinstAcc, "FontAccel"); 
    if (haccel == NULL) 
        HandleAccelErr(ERR_LOADING);     // application defined 
 
    // Get and dispatch messages until a WM_QUIT message is 
    // received. 
 
    while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        { 
            // Check for accelerator keystrokes. 
     
            if (!TranslateAccelerator( 
                    hwndMain,  // handle to receiving window 
                    haccel,    // handle to active accelerator table 
                    &msg))         // message data 
            {
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
        } 
    }
    return msg.wParam; 
} 
 
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    BYTE fbFontAttrib;        // array of font-attribute flags 
    static HMENU hmenu;       // handle to main menu 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Add a check mark to the Regular menu item to 
            // indicate that it is the default. 
 
            hmenu = GetMenu(hwndMain); 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the accelerator and menu commands. 
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // GetFontAttributes is an application-defined 
                    // function that sets the menu-item check marks 
                    // and returns the user-selected font attributes. 
 
                    fbFontAttrib = GetFontAttributes( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // SetFontAttributes is an application-defined 
                    // function that creates a font with the 
                    // user-specified attributes the font with 
                    // the main window's device context. 
 
                    SetFontAttributes(fbFontAttrib); 
                    break; 
 
                default: 
                    break; 
            } 
            break; 
 
            // Process other messages. 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="using-an-accelerator-table-created-at-run-time"></a><span data-ttu-id="1f473-192">Verwenden einer Zugriffstasten Tabelle, die zur Laufzeit erstellt wird</span><span class="sxs-lookup"><span data-stu-id="1f473-192">Using an Accelerator Table Created at Run Time</span></span>

<span data-ttu-id="1f473-193">In diesem Thema wird die Verwendung von Zugriffstasten Tabellen erläutert, die zur Laufzeit erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1f473-193">This topic discusses how to use accelerator tables created at run time.</span></span>

-   [<span data-ttu-id="1f473-194">Erstellen einer Run-Time Accelerator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="1f473-194">Creating a Run-Time Accelerator Table</span></span>](#creating-a-run-time-accelerator-table)
-   [<span data-ttu-id="1f473-195">Verarbeiten von Accelerators</span><span class="sxs-lookup"><span data-stu-id="1f473-195">Processing Accelerators</span></span>](#processing-accelerators)
-   [<span data-ttu-id="1f473-196">Zerstören einer Run-Time Accelerator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="1f473-196">Destroying a Run-Time Accelerator Table</span></span>](#destroying-a-run-time-accelerator-table)
-   [<span data-ttu-id="1f473-197">Erstellen von Benutzer bearbeitbaren Acceleratoren</span><span class="sxs-lookup"><span data-stu-id="1f473-197">Creating User Editable Accelerators</span></span>](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a><span data-ttu-id="1f473-198">Erstellen einer Run-Time Accelerator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="1f473-198">Creating a Run-Time Accelerator Table</span></span>

<span data-ttu-id="1f473-199">Der erste Schritt beim Erstellen einer Zugriffstasten Tabelle zur Laufzeit ist das Auffüllen eines Arrays von [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="1f473-199">The first step in creating an accelerator table at run time is filling an array of [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structures.</span></span> <span data-ttu-id="1f473-200">Jede Struktur im Array definiert eine Zugriffstaste in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1f473-200">Each structure in the array defines an accelerator in the table.</span></span> <span data-ttu-id="1f473-201">Die Definition eines Zugriffstasten enthält die Flags, den Schlüssel und den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1f473-201">An accelerator's definition includes its flags, its key, and its identifier.</span></span> <span data-ttu-id="1f473-202">Die **Accel** -Struktur hat die folgende Form.</span><span class="sxs-lookup"><span data-stu-id="1f473-202">The **ACCEL** structure has the following form.</span></span>

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

<span data-ttu-id="1f473-203">Sie definieren eine Tastenkombination einer Zugriffstaste, indem Sie einen ASCII-Zeichencode oder einen Code für den virtuellen Schlüssel im **Schlüssel** Element der [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) -Struktur angeben.</span><span class="sxs-lookup"><span data-stu-id="1f473-203">You define an accelerator's keystroke by specifying an ASCII character code or a virtual-key code in the **key** member of the [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structure.</span></span> <span data-ttu-id="1f473-204">Wenn Sie einen Code für den virtuellen Schlüssel angeben, müssen Sie zunächst das **fvirtkey** -Flag in das **fvirt** -Member einschließen. Andernfalls interpretiert das System den Code als ASCII-Zeichencode.</span><span class="sxs-lookup"><span data-stu-id="1f473-204">If you specify a virtual-key code, you must first include the **FVIRTKEY** flag in the **fVirt** member; otherwise, the system interprets the code as an ASCII character code.</span></span> <span data-ttu-id="1f473-205">Sie können das **Fcontrol** **-, das**-oder das **fshift** -Flag oder alle drei einschließen, um die STRG-Taste, die Alt-Taste oder die UMSCHALTTASTE mit dem Tastatur Strich zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="1f473-205">You can include the **FCONTROL**, **FALT**, or **FSHIFT** flag, or all three, to combine the CTRL, ALT, or SHIFT key with the keystroke.</span></span>

<span data-ttu-id="1f473-206">Um die Zugriffstasten Tabelle zu erstellen, übergeben Sie einen Zeiger auf das Array von [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) -Strukturen an [**die Funktion "**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) -Funktion".</span><span class="sxs-lookup"><span data-stu-id="1f473-206">To create the accelerator table, pass a pointer to the array of [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structures to the [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) function.</span></span> <span data-ttu-id="1f473-207">" **Kreateacceleratortable** " erstellt die Zugriffstasten Tabelle und gibt das Handle für die Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="1f473-207">**CreateAcceleratorTable** creates the accelerator table and returns the handle to the table.</span></span>

### <a name="processing-accelerators"></a><span data-ttu-id="1f473-208">Verarbeiten von Accelerators</span><span class="sxs-lookup"><span data-stu-id="1f473-208">Processing Accelerators</span></span>

<span data-ttu-id="1f473-209">Das Laden und Aufrufen von Acceleratoren, die von einer zur Laufzeit erstellten Zugriffstasten-Tabelle bereitgestellt werden, ist identisch mit der Verarbeitung von Zugriffstasten, die von einer Zugriffstasten-Tabelle bereitgestellt werden</span><span class="sxs-lookup"><span data-stu-id="1f473-209">The process of loading and calling accelerators provided by an accelerator table created at run time is the same as processing those provided by an accelerator-table resource.</span></span> <span data-ttu-id="1f473-210">Weitere Informationen finden Sie unter [Laden der](#loading-the-accelerator-table-resource) Zugriffstasten-Tabellen Ressource durch [Verarbeitung von WM- \_ befehlsnachrichten](/windows).</span><span class="sxs-lookup"><span data-stu-id="1f473-210">For more information, see [Loading the Accelerator Table Resource](#loading-the-accelerator-table-resource) through [Processing WM\_COMMAND Messages](/windows).</span></span>

### <a name="destroying-a-run-time-accelerator-table"></a><span data-ttu-id="1f473-211">Zerstören einer Run-Time Accelerator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="1f473-211">Destroying a Run-Time Accelerator Table</span></span>

<span data-ttu-id="1f473-212">Das System zerstört schnell Zugriffs Tabellen, die zur Laufzeit erstellt werden, und entfernt die Ressourcen nach dem Schließen der Anwendung aus dem Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1f473-212">The system automatically destroys accelerator tables created at run time, removing the resources from memory after the application closes.</span></span> <span data-ttu-id="1f473-213">Sie können eine Zugriffstasten Tabelle zerstören und Sie zuvor aus dem Arbeitsspeicher entfernen, indem Sie das Handle der Tabelle an die [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="1f473-213">You can destroy an accelerator table and remove it from memory earlier by passing the table's handle to the [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) function.</span></span>

### <a name="creating-user-editable-accelerators"></a><span data-ttu-id="1f473-214">Erstellen von Benutzer bearbeitbaren Acceleratoren</span><span class="sxs-lookup"><span data-stu-id="1f473-214">Creating User Editable Accelerators</span></span>

<span data-ttu-id="1f473-215">In diesem Beispiel wird gezeigt, wie ein Dialogfeld erstellt wird, das es dem Benutzer ermöglicht, die einem Menü Element zugeordnete Zugriffstaste zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1f473-215">This example shows how to construct a dialog box that allows the user to change the accelerator associated with a menu item.</span></span> <span data-ttu-id="1f473-216">Das Dialogfeld besteht aus einem Kombinations Feld mit Menü Elementen, einem Kombinations Feld mit den Namen der Schlüssel und Kontrollkästchen zum Auswählen der Tasten STRG, alt und UMSCHALT.</span><span class="sxs-lookup"><span data-stu-id="1f473-216">The dialog box consists of a combo box containing menu items, a combo box containing the names of keys, and check boxes for selecting the CTRL, ALT, and SHIFT keys.</span></span> <span data-ttu-id="1f473-217">Die folgende Abbildung zeigt das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="1f473-217">The following illustration shows the dialog box.</span></span>

![Dialogfeld mit Kombinations Feldern und Kontrollkästchen](images/useredit.gif)

<span data-ttu-id="1f473-219">Im folgenden Beispiel wird gezeigt, wie das Dialogfeld in der Ressourcen Definitionsdatei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1f473-219">The following example shows how the dialog box is defined in the resource-definition file.</span></span>

``` syntax
EdAccelBox DIALOG 5, 17, 193, 114 
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Edit Accelerators" 
BEGIN 
    COMBOBOX        IDD_MENUITEMS, 10, 22, 52, 53, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    CONTROL         "Control", IDD_CNTRL, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 35, 40, 10 
    CONTROL         "Alt", IDD_ALT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 48, 40, 10 
    CONTROL         "Shift", IDD_SHIFT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 61, 40, 10 
    COMBOBOX        IDD_KEYSTROKES, 124, 22, 58, 58, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    PUSHBUTTON      "Ok", IDOK, 43, 92, 40, 14 
    PUSHBUTTON      "Cancel", IDCANCEL, 103, 92, 40, 14 
    LTEXT           "Select Item:", 101, 10, 12, 43, 8 
    LTEXT           "Select Keystroke:", 102, 123, 12, 60, 8 
END
```

<span data-ttu-id="1f473-220">Die Menüleiste der Anwendung enthält ein Untermenü des **Zeichens** , dessen Elemente mit Zugriffstasten verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1f473-220">The application's menu bar contains a **Character** submenu whose items have accelerators associated with them.</span></span>

``` syntax
MainMenu MENU 
{ 
    POPUP "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```

<span data-ttu-id="1f473-221">Die Menü Element Werte für die Menüvorlage sind Konstanten, die wie folgt in der Header Datei der Anwendung definiert sind.</span><span class="sxs-lookup"><span data-stu-id="1f473-221">The menu item values for the menu template are constants defined as follows in the application's header file.</span></span>

``` syntax
#define IDM_REGULAR    1100
#define IDM_BOLD       1200
#define IDM_ITALIC     1300
#define IDM_ULINE      1400
```

<span data-ttu-id="1f473-222">Im Dialogfeld wird ein Array von Anwendungs definierten VKey-Strukturen verwendet, von denen jedes eine Keystroke-Text Zeichenfolge und eine Zugriffs Text Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="1f473-222">The dialog box uses an array of application-defined VKEY structures, each containing a keystroke-text string and an accelerator-text string.</span></span> <span data-ttu-id="1f473-223">Wenn das Dialogfeld erstellt wird, wird das Array analysiert, und jede Keystroke-Text Zeichenfolge wird dem Kombinations Feld **KeyStroke auswählen** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1f473-223">When the dialog box is created, it parses the array and adds each keystroke-text string to the **Select Keystroke** combo box.</span></span> <span data-ttu-id="1f473-224">Wenn der Benutzer auf die Schaltfläche **OK** klickt, wird das Dialogfeld die ausgewählte Keystroke-Text Zeichenfolge nachschlagen und die entsprechende Zugriffstasten-Text Zeichenfolge abrufen.</span><span class="sxs-lookup"><span data-stu-id="1f473-224">When the user clicks the **OK** button, the dialog box looks up the selected keystroke-text string and retrieves the corresponding accelerator-text string.</span></span> <span data-ttu-id="1f473-225">Das Dialogfeld fügt die Zugriffstasten-Text Zeichenfolge an den Text des Menü Elements an, das der Benutzer ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="1f473-225">The dialog box appends the accelerator-text string to the text of the menu item that the user selected.</span></span> <span data-ttu-id="1f473-226">Das folgende Beispiel zeigt das Array von VKey-Strukturen:</span><span class="sxs-lookup"><span data-stu-id="1f473-226">The following example shows the array of VKEY structures:</span></span>


```
// VKey Lookup Support 
 
#define MAXKEYS 25 
 
typedef struct _VKEYS { 
    char *pKeyName; 
    char *pKeyString; 
} VKEYS; 
 
VKEYS vkeys[MAXKEYS] = { 
    "BkSp",     "Back Space", 
    "PgUp",     "Page Up", 
    "PgDn",     "Page Down", 
    "End",      "End", 
    "Home",     "Home", 
    "Lft",      "Left", 
    "Up",       "Up", 
    "Rgt",      "Right", 
    "Dn",       "Down", 
    "Ins",      "Insert", 
    "Del",      "Delete", 
    "Mult",     "Multiply", 
    "Add",      "Add", 
    "Sub",      "Subtract", 
    "DecPt",    "Decimal Point", 
    "Div",      "Divide", 
    "F2",       "F2", 
    "F3",       "F3", 
    "F5",       "F5", 
    "F6",       "F6", 
    "F7",       "F7", 
    "F8",       "F8", 
    "F9",       "F9", 
    "F11",      "F11", 
    "F12",      "F12" 
};
```



<span data-ttu-id="1f473-227">Die Initialisierungs Prozedur des Dialog Felds füllt die Kombinations Felder **Select Item** und **KeyStroke** aus.</span><span class="sxs-lookup"><span data-stu-id="1f473-227">The dialog box's initialization procedure fills the **Select Item** and **Select Keystroke** combo boxes.</span></span> <span data-ttu-id="1f473-228">Nachdem der Benutzer ein Menü Element und eine zugeordnete Zugriffstaste ausgewählt hat, überprüft das Dialogfeld die Steuerelemente im Dialogfeld, um die Benutzer Auswahl zu erhalten, aktualisiert den Text des Menü Elements und erstellt dann eine neue Zugriffstasten Tabelle, die die benutzerdefinierte neue Zugriffstaste enthält.</span><span class="sxs-lookup"><span data-stu-id="1f473-228">After the user selects a menu item and associated accelerator, the dialog box examines the controls in the dialog box to get the user's selection, updates the text of the menu item, and then creates a new accelerator table that contains the user-defined new accelerator.</span></span> <span data-ttu-id="1f473-229">Das folgende Beispiel zeigt die-Dialogfeld Prozedur.</span><span class="sxs-lookup"><span data-stu-id="1f473-229">The following example shows the dialog-box procedure.</span></span> <span data-ttu-id="1f473-230">Beachten Sie, dass Sie in der Fenster Prozedur initialisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="1f473-230">Note that you must initialize in your window procedure.</span></span>


```
// Global variables 
 
HWND hwndMain;      // handle to main window 
HACCEL haccel;      // handle to accelerator table 
 
// Dialog-box procedure 
 
BOOL CALLBACK EdAccelProc(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    int nCurSel;            // index of list box item 
    UINT idItem;            // menu-item identifier 
    UINT uItemPos;          // menu-item position 
    UINT i, j = 0;          // loop counters 
    static UINT cItems;     // count of items in menu 
    char szTemp[32];        // temporary buffer 
    char szAccelText[32];   // buffer for accelerator text 
    char szKeyStroke[16];   // buffer for keystroke text 
    static char szItem[32]; // buffer for menu-item text 
    HWND hwndCtl;           // handle to control window 
    static HMENU hmenu;     // handle to "Character" menu 
    PCHAR pch, pch2;        // pointers for string copying 
    WORD wVKCode;           // accelerator virtual-key code 
    BYTE fAccelFlags;       // fVirt flags for ACCEL structure 
    LPACCEL lpaccelNew;     // pointer to new accelerator table 
    HACCEL haccelOld;       // handle to old accelerator table 
    int cAccelerators;      // number of accelerators in table 
    static BOOL fItemSelected = FALSE; // item selection flag 
    static BOOL fKeySelected = FALSE;  // key selection flag 
    HRESULT hr;
    INT numTCHAR;           // TCHARs in listbox text
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
 
            // Get the handle to the menu-item combo box. 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_MENUITEMS); 
 
            // Get the handle to the Character submenu and
            // count the number of items it has. In this example, 
            // the menu has position 0. You must alter this value 
            // if you add additional menus. 
            hmenu = GetSubMenu(GetMenu(hwndMain), 0); 
            cItems = GetMenuItemCount(hmenu); 
 
            // Get the text of each item, strip out the '&' and 
            // the accelerator text, and add the text to the 
            // menu-item combo box. 
 
            for (i = 0; i < cItems; i++) 
            { 
                if (!(GetMenuString(hmenu, i, szTemp, 
                        sizeof(szTemp)/sizeof(TCHAR), MF_BYPOSITION))) 
                    continue; 
                for (pch = szTemp, pch2 = szItem; *pch != '\0'; ) 
                { 
                    if (*pch != '&') 
                    { 
                        if (*pch == '\t') 
                        { 
                            *pch = '\0'; 
                            *pch2 = '\0'; 
                        } 
                        else *pch2++ = *pch++; 
                    } 
                    else pch++; 
                } 
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) szItem); 
            } 
 
            // Now fill the keystroke combo box with the list of 
            // keystrokes that will be allowed for accelerators. 
            // The list of keystrokes is in the application-defined 
            // structure called "vkeys". 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
            for (i = 0; i < MAXKEYS; i++) 
            {
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) vkeys[i].pKeyString); 
            }
 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDD_MENUITEMS: 
 
                    // The user must select an item from the combo 
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fItemSelected = TRUE; 
                    return 0; 
 
                case IDD_KEYSTROKES: 
 
                    // The user must select an item from the combo
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fKeySelected = TRUE; 
 
                    return 0; 
 
                case IDOK: 
 
                    // If the user has not selected a menu item 
                    // and a keystroke, display a reminder in a 
                    // message box. 
 
                    if (!fItemSelected || !fKeySelected) 
                    { 
                        MessageBox(hwndDlg, 
                            "Item or key not selected.", NULL, 
                            MB_OK); 
                        return 0; 
                    } 
 
                    // Determine whether the CTRL, ALT, and SHIFT 
                    // keys are selected. Concatenate the 
                    // appropriate strings to the accelerator- 
                    // text buffer, and set the appropriate 
                    // accelerator flags. 
 
                    szAccelText[0] = '\0'; 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_CNTRL); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Ctl+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FCONTROL; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_ALT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Alt+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FALT; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_SHIFT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    {
                        hr = StringCchCat(szAccelText, 32, "Shft+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FSHIFT; 
                    } 
 
                    // Get the selected keystroke, and look up the 
                    // accelerator text and the virtual-key code 
                    // for the keystroke in the vkeys structure. 
 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
                    nCurSel = (int) SendMessage(hwndCtl, 
                        CB_GETCURSEL, 0, 0);
                    numTCHAR = SendMessage(hwndCtl, CB_GETLBTEXTLEN, 
                        nCursel, 0); 
                    if (numTCHAR <= 15)
                        {                   
                        SendMessage(hwndCtl, CB_GETLBTEXT, 
                            nCurSel, (LONG) (LPSTR) szKeyStroke);
                        }
                    else
                        {
                        // TODO: writer error handler
                        }
                         
                    for (i = 0; i < MAXKEYS; i++) 
                    {
                    //
                    // lstrcmp requires that both parameters are
                    // null-terminated.
                    //
                        if(lstrcmp(vkeys[i].pKeyString, szKeyStroke) 
                            == 0) 
                        { 
                            hr = StringCchCopy(szKeyStroke, 16, vkeys[i].pKeyName);
                            if (FAILED(hr))
                            {
                            // TODO: write error handler
                            }
                            break; 
                        } 
                    } 
 
                    // Concatenate the keystroke text to the 
                    // "Ctl+","Alt+", or "Shft+" string. 
 
                        hr = StringCchCat(szAccelText, 32, szKeyStroke);
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
 
                    // Determine the position in the menu of the 
                    // selected menu item. Menu items in the 
                    // "Character" menu have positions 0,2,3, and 4.
                    // Note: the lstrcmp parameters must be
                    // null-terminated. 
 
                    if (lstrcmp(szItem, "Regular") == 0) 
                        uItemPos = 0; 
                    else if (lstrcmp(szItem, "Bold") == 0) 
                        uItemPos = 2; 
                    else if (lstrcmp(szItem, "Italic") == 0) 
                        uItemPos = 3; 
                    else if (lstrcmp(szItem, "Underline") == 0) 
                        uItemPos = 4; 
 
                    // Get the string that corresponds to the 
                    // selected item. 
 
                    GetMenuString(hmenu, uItemPos, szItem, 
                        sizeof(szItem)/sizeof(TCHAR), MF_BYPOSITION); 
 
                    // Append the new accelerator text to the 
                    // menu-item text. 
 
                    for (pch = szItem; *pch != '\t'; pch++); 
                        ++pch; 
 
                    for (pch2 = szAccelText; *pch2 != '\0'; pch2++) 
                        *pch++ = *pch2; 
                    *pch = '\0'; 
 
                    // Modify the menu item to reflect the new 
                    // accelerator text. 
 
                    idItem = GetMenuItemID(hmenu, uItemPos); 
                    ModifyMenu(hmenu, idItem, MF_BYCOMMAND | 
                        MF_STRING, idItem, szItem); 
 
                    // Reset the selection flags. 
 
                    fItemSelected = FALSE; 
                    fKeySelected = FALSE; 
 
                    // Save the current accelerator table. 
 
                    haccelOld = haccel; 
 
                    // Count the number of entries in the current 
                    // table, allocate a buffer for the table, and 
                    // then copy the table into the buffer. 
 
                    cAccelerators = CopyAcceleratorTable( 
                        haccelOld, NULL, 0); 
                    lpaccelNew = (LPACCEL) LocalAlloc(LPTR, 
                        cAccelerators * sizeof(ACCEL)); 
 
                    if (lpaccelNew != NULL) 
                    {
                        CopyAcceleratorTable(haccel, lpaccelNew, 
                            cAccelerators); 
                    }
 
                    // Find the accelerator that the user modified 
                    // and change its flags and virtual-key code 
                    // as appropriate. 
 
                    for (i = 0; i < (UINT) cAccelerators; i++) 
                    { 
                           if (lpaccelNew[i].cmd == (WORD) idItem)
                        {
                            lpaccelNew[i].fVirt = fAccelFlags; 
                            lpaccelNew[i].key = wVKCode; 
                        }
                    } 
 
                    // Create the new accelerator table, and 
                    // destroy the old one. 
 
                    DestroyAcceleratorTable(haccelOld); 
                    haccel = CreateAcceleratorTable(lpaccelNew, 
                        cAccelerators); 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hwndDlg, TRUE); 
                    return 0; 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    break; 
            } 
        default: 
            break; 
    } 
    return FALSE; 
}
```



 

 