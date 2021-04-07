---
title: Zugriffstasten Tabellen
description: .
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9929445809bee71f273b6bd2334e182de59edbfa
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104039000"
---
# <a name="accelerator-tables"></a><span data-ttu-id="e4303-103">Zugriffstasten Tabellen</span><span class="sxs-lookup"><span data-stu-id="e4303-103">Accelerator Tables</span></span>

<span data-ttu-id="e4303-104">Anwendungen definieren häufig Tastenkombinationen, wie z. b. STRG + O für den Befehl zum Öffnen von Dateien.</span><span class="sxs-lookup"><span data-stu-id="e4303-104">Applications often define keyboard shortcuts, such as CTRL+O for the File Open command.</span></span> <span data-ttu-id="e4303-105">Sie können Tastenkombinationen implementieren, indem Sie einzelne [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Meldungen verarbeiten, aber Zugriffstasten Tabellen bieten eine bessere Lösung:</span><span class="sxs-lookup"><span data-stu-id="e4303-105">You could implement keyboard shortcuts by handling individual [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, but accelerator tables provide a better solution that:</span></span>

-   <span data-ttu-id="e4303-106">Erfordert weniger Codierungen.</span><span class="sxs-lookup"><span data-stu-id="e4303-106">Requires less coding.</span></span>
-   <span data-ttu-id="e4303-107">Konsolidiert all Ihre Verknüpfungen in einer Datendatei.</span><span class="sxs-lookup"><span data-stu-id="e4303-107">Consolidates all of your shortcuts into one data file.</span></span>
-   <span data-ttu-id="e4303-108">Unterstützt die Lokalisierung in andere Sprachen.</span><span class="sxs-lookup"><span data-stu-id="e4303-108">Supports localization into other languages.</span></span>
-   <span data-ttu-id="e4303-109">Ermöglicht es Verknüpfungen und Menübefehlen, dieselbe Anwendungslogik zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4303-109">Enables shortcuts and menu commands to use the same application logic.</span></span>

<span data-ttu-id="e4303-110">Eine Zugriffstasten *Tabelle* ist eine Daten Ressource, die Tastenkombinationen wie STRG + O zu Anwendungs Befehlen zuordnet.</span><span class="sxs-lookup"><span data-stu-id="e4303-110">An *accelerator table* is a data resource that maps keyboard combinations, such as CTRL+O, to application commands.</span></span> <span data-ttu-id="e4303-111">Bevor wir uns mit der Verwendung einer Zugriffstasten Tabelle beschäftigen, benötigen wir eine kurze Einführung in die Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e4303-111">Before we see how to use an accelerator table, we'll need a quick introduction to resources.</span></span> <span data-ttu-id="e4303-112">Eine *Ressource* ist ein Daten-BLOB, das in eine Anwendungs Binärdatei (exe oder dll) integriert ist.</span><span class="sxs-lookup"><span data-stu-id="e4303-112">A *resource* is a data blob that is built into an application binary (EXE or DLL).</span></span> <span data-ttu-id="e4303-113">In Ressourcen werden Daten gespeichert, die von der Anwendung benötigt werden, z. b. Menüs, Cursor, Symbole, Bilder, Text Zeichenfolgen oder beliebige benutzerdefinierte Anwendungsdaten.</span><span class="sxs-lookup"><span data-stu-id="e4303-113">Resources store data that are needed by the application, such as menus, cursors, icons, images, text strings, or any custom application data.</span></span> <span data-ttu-id="e4303-114">Die Anwendung lädt die Ressourcen Daten zur Laufzeit aus der Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="e4303-114">The application loads the resource data from the binary at run time.</span></span> <span data-ttu-id="e4303-115">Gehen Sie folgendermaßen vor, um Ressourcen in eine Binärdatei einzuschließen:</span><span class="sxs-lookup"><span data-stu-id="e4303-115">To include resources in a binary, do the following:</span></span>

1.  <span data-ttu-id="e4303-116">Erstellen Sie eine Ressourcen Definitionsdatei (RC-Datei).</span><span class="sxs-lookup"><span data-stu-id="e4303-116">Create a resource definition (.rc) file.</span></span> <span data-ttu-id="e4303-117">Diese Datei definiert die Typen von Ressourcen und deren Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e4303-117">This file defines the types of resources and their identifiers.</span></span> <span data-ttu-id="e4303-118">Die Ressourcen Definitionsdatei kann Verweise auf andere Dateien enthalten.</span><span class="sxs-lookup"><span data-stu-id="e4303-118">The resource definition file may include references to other files.</span></span> <span data-ttu-id="e4303-119">Beispielsweise wird eine Symbol Ressource in der RC-Datei deklariert, aber das Symbolbild wird in einer separaten Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e4303-119">For example, an icon resource is declared in the .rc file, but the icon image is stored in a separate file.</span></span>
2.  <span data-ttu-id="e4303-120">Verwenden Sie den Microsoft Windows-Ressourcen Compiler (RC), um die Ressourcen Definitionsdatei in eine kompilierte Ressourcen Datei (. res) zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="e4303-120">Use the Microsoft Windows Resource Compiler (RC) to compile the resource definition file into a compiled resource (.res) file.</span></span> <span data-ttu-id="e4303-121">Der RC-Compiler wird mit Visual Studio und dem Windows SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e4303-121">The RC compiler is provided with Visual Studio and also the Windows SDK.</span></span>
3.  <span data-ttu-id="e4303-122">Verknüpfen Sie die kompilierte Ressourcen Datei mit der Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="e4303-122">Link the compiled resource file to the binary file.</span></span>

<span data-ttu-id="e4303-123">Diese Schritte entsprechen ungefähr dem Kompilierungs-/Linkprozess für Code Dateien.</span><span class="sxs-lookup"><span data-stu-id="e4303-123">These steps are roughly equivalent to the compile/link process for code files.</span></span> <span data-ttu-id="e4303-124">Visual Studio bietet eine Reihe von Ressourcen-Editoren, mit denen Sie problemlos Ressourcen erstellen und ändern können.</span><span class="sxs-lookup"><span data-stu-id="e4303-124">Visual Studio provides a set of resource editors that make it easy to create and modify resources.</span></span> <span data-ttu-id="e4303-125">(Diese Tools sind in den Express-Editionen von Visual Studio nicht verfügbar.) Eine RC-Datei ist einfach eine Textdatei, und die Syntax wird auf MSDN dokumentiert. Daher ist es möglich, eine RC-Datei mit einem beliebigen Text-Editor zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4303-125">(These tools are not available in the Express editions of Visual Studio.) But an .rc file is simply a text file, and the syntax is documented on MSDN, so it is possible to create an .rc file using any text editor.</span></span> <span data-ttu-id="e4303-126">Weitere Informationen finden Sie unter Informationen [zu Ressourcen Dateien](/windows/desktop/menurc/about-resource-files).</span><span class="sxs-lookup"><span data-stu-id="e4303-126">For more information, see [About Resource Files](/windows/desktop/menurc/about-resource-files).</span></span>

## <a name="defining-an-accelerator-table"></a><span data-ttu-id="e4303-127">Definieren einer Zugriffstasten Tabelle</span><span class="sxs-lookup"><span data-stu-id="e4303-127">Defining an Accelerator Table</span></span>

<span data-ttu-id="e4303-128">Eine Zugriffstasten Tabelle ist eine Tabelle mit Tastenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="e4303-128">An accelerator table is a table of keyboard shortcuts.</span></span> <span data-ttu-id="e4303-129">Jede Verknüpfung wird definiert durch:</span><span class="sxs-lookup"><span data-stu-id="e4303-129">Each shortcut is defined by:</span></span>

-   <span data-ttu-id="e4303-130">Ein numerischer Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e4303-130">A numeric identifier.</span></span> <span data-ttu-id="e4303-131">Diese Nummer identifiziert den Anwendungs Befehl, der von der Verknüpfung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e4303-131">This number identifies the application command that will be invoked by the shortcut.</span></span>
-   <span data-ttu-id="e4303-132">Das ASCII-Zeichen oder der Code für den virtuellen Schlüssel der Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="e4303-132">The ASCII character or virtual-key code of the shortcut.</span></span>
-   <span data-ttu-id="e4303-133">Optionale Modifizierertasten: alt, UMSCHALT oder STRG.</span><span class="sxs-lookup"><span data-stu-id="e4303-133">Optional modifier keys: ALT, SHIFT, or CTRL.</span></span>

<span data-ttu-id="e4303-134">Die Zugriffstasten Tabelle selbst hat einen numerischen Bezeichner, der die Tabelle in der Liste der Anwendungs Ressourcen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e4303-134">The accelerator table itself has a numeric identifier, which identifies the table in the list of application resources.</span></span> <span data-ttu-id="e4303-135">Erstellen wir eine Zugriffstasten Tabelle für ein einfaches Zeichnungsprogramm.</span><span class="sxs-lookup"><span data-stu-id="e4303-135">Let's create an accelerator table for a simple drawing program.</span></span> <span data-ttu-id="e4303-136">Dieses Programm verfügt über zwei Modi: den Zeichnungsmodus und den Auswahlmodus.</span><span class="sxs-lookup"><span data-stu-id="e4303-136">This program will have two modes, draw mode and selection mode.</span></span> <span data-ttu-id="e4303-137">Im Draw-Modus kann der Benutzer Formen zeichnen.</span><span class="sxs-lookup"><span data-stu-id="e4303-137">In draw mode, the user can draw shapes.</span></span> <span data-ttu-id="e4303-138">Im Auswahlmodus kann der Benutzer Formen auswählen.</span><span class="sxs-lookup"><span data-stu-id="e4303-138">In selection mode, the user can select shapes.</span></span> <span data-ttu-id="e4303-139">Für dieses Programm möchten wir die folgenden Tastenkombinationen definieren.</span><span class="sxs-lookup"><span data-stu-id="e4303-139">For this program, we would like to define the following keyboard shortcuts.</span></span>



| <span data-ttu-id="e4303-140">Abkürzung</span><span class="sxs-lookup"><span data-stu-id="e4303-140">Shortcut</span></span> | <span data-ttu-id="e4303-141">Get-Help</span><span class="sxs-lookup"><span data-stu-id="e4303-141">Command</span></span>                   |
|----------|---------------------------|
| <span data-ttu-id="e4303-142">STRG+M</span><span class="sxs-lookup"><span data-stu-id="e4303-142">CTRL+M</span></span>   | <span data-ttu-id="e4303-143">Umschalten zwischen Modi.</span><span class="sxs-lookup"><span data-stu-id="e4303-143">Toggle between modes.</span></span>     |
| <span data-ttu-id="e4303-144">F1</span><span class="sxs-lookup"><span data-stu-id="e4303-144">F1</span></span>       | <span data-ttu-id="e4303-145">Wechseln Sie in den Zeichnungsmodus.</span><span class="sxs-lookup"><span data-stu-id="e4303-145">Switch to draw mode.</span></span>      |
| <span data-ttu-id="e4303-146">F2</span><span class="sxs-lookup"><span data-stu-id="e4303-146">F2</span></span>       | <span data-ttu-id="e4303-147">Wechseln Sie in den Auswahlmodus.</span><span class="sxs-lookup"><span data-stu-id="e4303-147">Switch to selection mode.</span></span> |



 

<span data-ttu-id="e4303-148">Definieren Sie zunächst numerische Bezeichner für die Tabelle und für die Anwendungs Befehle.</span><span class="sxs-lookup"><span data-stu-id="e4303-148">First, define numeric identifiers for the table and for the application commands.</span></span> <span data-ttu-id="e4303-149">Diese Werte sind willkürlich.</span><span class="sxs-lookup"><span data-stu-id="e4303-149">These values are arbitrary.</span></span> <span data-ttu-id="e4303-150">Sie können symbolische Konstanten für die Bezeichner zuweisen, indem Sie Sie in einer Header Datei definieren.</span><span class="sxs-lookup"><span data-stu-id="e4303-150">You can assign symbolic constants for the identifiers by defining them in a header file.</span></span> <span data-ttu-id="e4303-151">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e4303-151">For example:</span></span>


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



<span data-ttu-id="e4303-152">In diesem Beispiel identifiziert der Wert `IDR_ACCEL1` die Zugriffstasten Tabelle, und die nächsten drei Konstanten definieren die Anwendungs Befehle.</span><span class="sxs-lookup"><span data-stu-id="e4303-152">In this example, the value `IDR_ACCEL1` identifies the accelerator table, and the next three constants define the application commands.</span></span> <span data-ttu-id="e4303-153">Gemäß der Konvention wird eine Header Datei, die Ressourcen Konstanten definiert, häufig als "Resource. h" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e4303-153">By convention, a header file that defines resource constants is often named resource.h.</span></span> <span data-ttu-id="e4303-154">In der nächsten Liste wird die Ressourcen Definitionsdatei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e4303-154">The next listing shows the resource definition file.</span></span>


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



<span data-ttu-id="e4303-155">Die Tastenkombinationen werden innerhalb der geschweiften Klammern definiert.</span><span class="sxs-lookup"><span data-stu-id="e4303-155">The accelerator shortcuts are defined within the curly braces.</span></span> <span data-ttu-id="e4303-156">Jede Verknüpfung enthält die folgenden Einträge.</span><span class="sxs-lookup"><span data-stu-id="e4303-156">Each shortcut contains the following entries.</span></span>

-   <span data-ttu-id="e4303-157">Der Code des virtuellen Schlüssels oder das ASCII-Zeichen, das die Verknüpfung aufruft.</span><span class="sxs-lookup"><span data-stu-id="e4303-157">The virtual-key code or ASCII character that invokes the shortcut.</span></span>
-   <span data-ttu-id="e4303-158">Der Anwendungs Befehl.</span><span class="sxs-lookup"><span data-stu-id="e4303-158">The application command.</span></span> <span data-ttu-id="e4303-159">Beachten Sie, dass im Beispiel symbolische Konstanten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4303-159">Notice that symbolic constants are used in the example.</span></span> <span data-ttu-id="e4303-160">Die Ressourcen Definitionsdatei enthält die Datei "Resource. h", in der diese Konstanten definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e4303-160">The resource definition file includes resource.h, where these constants are defined.</span></span>
-   <span data-ttu-id="e4303-161">Das Schlüsselwort **VIRTKEY** bedeutet, dass der erste Eintrag ein Code für den virtuellen Schlüssel ist.</span><span class="sxs-lookup"><span data-stu-id="e4303-161">The keyword **VIRTKEY** means the first entry is a virtual-key code.</span></span> <span data-ttu-id="e4303-162">Die andere Option ist die Verwendung von ASCII-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e4303-162">The other option is to use ASCII characters.</span></span>
-   <span data-ttu-id="e4303-163">Optionale modifiziererer: alt, Steuerelement oder UMSCHALT.</span><span class="sxs-lookup"><span data-stu-id="e4303-163">Optional modifiers: ALT, CONTROL, or SHIFT.</span></span>

<span data-ttu-id="e4303-164">Wenn Sie ASCII-Zeichen für Verknüpfungen verwenden, ist ein Kleinbuchstabe eine andere Verknüpfung als ein Großbuchstabe.</span><span class="sxs-lookup"><span data-stu-id="e4303-164">If you use ASCII characters for shortcuts, then a lowercase character will be a different shortcut than an uppercase character.</span></span> <span data-ttu-id="e4303-165">(Wenn Sie z. b. "a" eingeben, wird möglicherweise ein anderer Befehl als "a" aufgerufen.) Das mag Benutzer verwirrend sein, daher ist es in der Regel besser, anstelle von ASCII-Zeichen anstelle von ASCII-Zeichencode für Verknüpfungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4303-165">(For example, typing 'a' might invoke a different command than typing 'A'.) That might confuse users, so it is generally better to use virtual-key codes, rather than ASCII characters, for shortcuts.</span></span>

## <a name="loading-the-accelerator-table"></a><span data-ttu-id="e4303-166">Laden der Zugriffstasten Tabelle</span><span class="sxs-lookup"><span data-stu-id="e4303-166">Loading the Accelerator Table</span></span>

<span data-ttu-id="e4303-167">Die Ressource für die Zugriffstasten Tabelle muss geladen werden, bevor Sie vom Programm verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4303-167">The resource for the accelerator table must be loaded before the program can use it.</span></span> <span data-ttu-id="e4303-168">Wenn Sie eine Zugriffstasten Tabelle laden möchten, können Sie die [**loadaccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="e4303-168">To load an accelerator table, call the [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) function.</span></span>


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



<span data-ttu-id="e4303-169">Diese Funktion wird aufgerufen, bevor Sie die Nachrichten Schleife eingeben.</span><span class="sxs-lookup"><span data-stu-id="e4303-169">Call this function before you enter the message loop.</span></span> <span data-ttu-id="e4303-170">Der erste Parameter ist das Handle für das Modul.</span><span class="sxs-lookup"><span data-stu-id="e4303-170">The first parameter is the handle to the module.</span></span> <span data-ttu-id="e4303-171">(Dieser Parameter wird an Ihre [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) -Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="e4303-171">(This parameter is passed to your [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="e4303-172">Weitere Informationen finden Sie unter [WinMain: der Einstiegspunkt der Anwendung](winmain--the-application-entry-point.md).) Der zweite Parameter ist der Ressourcen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e4303-172">For details, see [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).) The second parameter is the resource identifier.</span></span> <span data-ttu-id="e4303-173">Die-Funktion gibt ein Handle für die Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="e4303-173">The function returns a handle to the resource.</span></span> <span data-ttu-id="e4303-174">Denken Sie daran, dass ein Handle ein nicht transparenter Typ ist, der auf ein Objekt verweist, das vom System verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="e4303-174">Recall that a handle is an opaque type that refers to an object managed by the system.</span></span> <span data-ttu-id="e4303-175">Wenn die Funktion fehlschlägt, wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e4303-175">If the function fails, it returns **NULL**.</span></span>

<span data-ttu-id="e4303-176">Sie können eine Zugriffstasten Tabelle freigeben, indem Sie [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e4303-176">You can release an accelerator table by calling [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span></span> <span data-ttu-id="e4303-177">Das System gibt die Tabelle jedoch automatisch frei, wenn das Programm beendet wird. Daher müssen Sie diese Funktion nur dann aufzurufen, wenn Sie eine Tabelle durch eine andere ersetzen.</span><span class="sxs-lookup"><span data-stu-id="e4303-177">However, the system automatically releases the table when the program exits, so you only need to call this function if you are replacing one table with another.</span></span> <span data-ttu-id="e4303-178">Ein interessantes Beispiel hierfür finden Sie im Thema Erstellen von [Benutzer bearbeitbaren Accelerators](/windows/desktop/menurc/using-keyboard-accelerators).</span><span class="sxs-lookup"><span data-stu-id="e4303-178">There is an interesting example of this in the topic [Creating User Editable Accelerators](/windows/desktop/menurc/using-keyboard-accelerators).</span></span>

## <a name="translating-key-strokes-into-commands"></a><span data-ttu-id="e4303-179">Übersetzen von Tastenkombinationen in Befehle</span><span class="sxs-lookup"><span data-stu-id="e4303-179">Translating Key Strokes into Commands</span></span>

<span data-ttu-id="e4303-180">Eine Zugriffstasten Tabelle funktioniert durch Übersetzen von Tastenkombinationen in [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="e4303-180">An accelerator table works by translating key strokes into [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="e4303-181">Der *wParam* -Parameter des **WM- \_ Befehls** enthält den numerischen Bezeichner des Befehls.</span><span class="sxs-lookup"><span data-stu-id="e4303-181">The *wParam* parameter of **WM\_COMMAND** contains the numeric identifier of the command.</span></span> <span data-ttu-id="e4303-182">Beispielsweise wird der Schlüssel Strich STRG + M mithilfe der zuvor gezeigten Tabelle in eine **WM- \_ Befehls** Meldung mit dem Wert übersetzt `ID_TOGGLE_MODE` .</span><span class="sxs-lookup"><span data-stu-id="e4303-182">For example, using the table shown previously, the key stroke CTRL+M is translated into a **WM\_COMMAND** message with the value `ID_TOGGLE_MODE`.</span></span> <span data-ttu-id="e4303-183">Um dies zu erreichen, ändern Sie die Nachrichten Schleife wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e4303-183">To make this happen, change your message loop to the following:</span></span>


```C++
    MSG msg;
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(win.Window(), hAccel, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```



<span data-ttu-id="e4303-184">Dieser Code fügt der [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) -Funktion innerhalb der Nachrichten Schleife einen aufzurufenden Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="e4303-184">This code adds a call to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function inside the message loop.</span></span> <span data-ttu-id="e4303-185">Die **TranslateAccelerator** -Funktion untersucht die einzelnen Fenster Meldungen und sucht nach Schlüsseln nach Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="e4303-185">The **TranslateAccelerator** function examines each window message, looking for key-down messages.</span></span> <span data-ttu-id="e4303-186">Wenn der Benutzer eine der Tastenkombinationen drückt, die in der Zugriffstasten Tabelle aufgeführt sind, sendet **TranslateAccelerator** eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung an das Fenster.</span><span class="sxs-lookup"><span data-stu-id="e4303-186">If the user presses one of the key combinations listed in the accelerator table, **TranslateAccelerator** sends a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message to the window.</span></span> <span data-ttu-id="e4303-187">Die Funktion sendet den **WM- \_ Befehl** durch direktes Aufrufen der Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="e4303-187">The function sends **WM\_COMMAND** by directly invoking the window procedure.</span></span> <span data-ttu-id="e4303-188">Wenn **TranslateAccelerator** einen Schlüssel Strich erfolgreich übersetzt, gibt die Funktion einen Wert ungleich 0 (null) zurück, was bedeutet, dass Sie die normale Verarbeitung der Nachricht überspringen sollten.</span><span class="sxs-lookup"><span data-stu-id="e4303-188">When **TranslateAccelerator** successfully translates a key stroke, the function returns a non-zero value, which means you should skip the normal processing for the message.</span></span> <span data-ttu-id="e4303-189">Andernfalls gibt **TranslateAccelerator** 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="e4303-189">Otherwise, **TranslateAccelerator** returns zero.</span></span> <span data-ttu-id="e4303-190">Übergeben Sie in diesem Fall die Fenster Meldung wie üblich an [**translatemess Age**](/windows/desktop/api/winuser/nf-winuser-translatemessage) und [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage).</span><span class="sxs-lookup"><span data-stu-id="e4303-190">In that case, pass the window message to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), as normal.</span></span>

<span data-ttu-id="e4303-191">Im folgenden wird erläutert, wie das Zeichnungsprogramm die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht verarbeiten kann:</span><span class="sxs-lookup"><span data-stu-id="e4303-191">Here is how the drawing program might handle the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message:</span></span>


```C++
    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case ID_DRAW_MODE:
            SetMode(DrawMode);
            break;

        case ID_SELECT_MODE:
            SetMode(SelectMode);
            break;

        case ID_TOGGLE_MODE:
            if (mode == DrawMode)
            {
                SetMode(SelectMode);
            }
            else
            {
                SetMode(DrawMode);
            }
            break;
        }
        return 0;

```



<span data-ttu-id="e4303-192">Dieser Code setzt voraus, dass `SetMode` eine Funktion ist, die von der Anwendung definiert wird, um zwischen den beiden Modi zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="e4303-192">This code assumes that `SetMode` is a function defined by the application to switch between the two modes.</span></span> <span data-ttu-id="e4303-193">Die Details zur Handhabung der einzelnen Befehle hängen offensichtlich von Ihrem Programm ab.</span><span class="sxs-lookup"><span data-stu-id="e4303-193">The details of how you would handle each command obviously depend on your program.</span></span>

## <a name="next"></a><span data-ttu-id="e4303-194">Nächste</span><span class="sxs-lookup"><span data-stu-id="e4303-194">Next</span></span>

[<span data-ttu-id="e4303-195">Festlegen des Cursor Bilds</span><span class="sxs-lookup"><span data-stu-id="e4303-195">Setting the Cursor Image</span></span>](setting-the-cursor-image.md)

 

 