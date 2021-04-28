---
title: Zugriffstastentabellen
description: Zugriffstastentabellen
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2951ee99a31a977e0909de5639fa3110cea10e0b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090818"
---
# <a name="accelerator-tables"></a><span data-ttu-id="7571c-103">Zugriffstastentabellen</span><span class="sxs-lookup"><span data-stu-id="7571c-103">Accelerator Tables</span></span>

<span data-ttu-id="7571c-104">Anwendungen definieren häufig Tastenkombinationen, z. B. STRG+O für den Befehl Datei öffnen.</span><span class="sxs-lookup"><span data-stu-id="7571c-104">Applications often define keyboard shortcuts, such as CTRL+O for the File Open command.</span></span> <span data-ttu-id="7571c-105">Sie können Tastenkombinationen implementieren, indem Sie einzelne [**WM \_ KEYDOWN-Nachrichten**](/windows/desktop/inputdev/wm-keydown) behandeln, aber Zugriffstastentabellen bieten eine bessere Lösung für:</span><span class="sxs-lookup"><span data-stu-id="7571c-105">You could implement keyboard shortcuts by handling individual [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, but accelerator tables provide a better solution that:</span></span>

-   <span data-ttu-id="7571c-106">Erfordert weniger Codierung.</span><span class="sxs-lookup"><span data-stu-id="7571c-106">Requires less coding.</span></span>
-   <span data-ttu-id="7571c-107">Konsolidiert alle Tastenkombinationen in einer Datendatei.</span><span class="sxs-lookup"><span data-stu-id="7571c-107">Consolidates all of your shortcuts into one data file.</span></span>
-   <span data-ttu-id="7571c-108">Unterstützt die Lokalisierung in anderen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="7571c-108">Supports localization into other languages.</span></span>
-   <span data-ttu-id="7571c-109">Aktiviert Verknüpfungen und Menübefehle, um dieselbe Anwendungslogik zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7571c-109">Enables shortcuts and menu commands to use the same application logic.</span></span>

<span data-ttu-id="7571c-110">Eine *Zugriffstastentabelle* ist eine Datenressource, die Tastenkombinationen wie STRG+O Anwendungsbefehlen zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="7571c-110">An *accelerator table* is a data resource that maps keyboard combinations, such as CTRL+O, to application commands.</span></span> <span data-ttu-id="7571c-111">Bevor wir sehen, wie sie eine Zugriffstastentabelle verwenden, benötigen wir eine kurze Einführung in Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="7571c-111">Before we see how to use an accelerator table, we'll need a quick introduction to resources.</span></span> <span data-ttu-id="7571c-112">Eine *Ressource* ist ein Datenblob, das in eine Anwendungsbin binär (EXE oder DLL) integriert ist.</span><span class="sxs-lookup"><span data-stu-id="7571c-112">A *resource* is a data blob that is built into an application binary (EXE or DLL).</span></span> <span data-ttu-id="7571c-113">Ressourcen speichern Daten, die von der Anwendung benötigt werden, z. B. Menüs, Cursor, Symbole, Bilder, Textzeichenfolgen oder benutzerdefinierte Anwendungsdaten.</span><span class="sxs-lookup"><span data-stu-id="7571c-113">Resources store data that are needed by the application, such as menus, cursors, icons, images, text strings, or any custom application data.</span></span> <span data-ttu-id="7571c-114">Die Anwendung lädt die Ressourcendaten zur Laufzeit aus der Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="7571c-114">The application loads the resource data from the binary at run time.</span></span> <span data-ttu-id="7571c-115">Gehen Sie wie folgt vor, um Ressourcen in eine Binärdatei ein-/aus zu schließen:</span><span class="sxs-lookup"><span data-stu-id="7571c-115">To include resources in a binary, do the following:</span></span>

1.  <span data-ttu-id="7571c-116">Erstellen Sie eine Ressourcendefinitionsdatei (RC).</span><span class="sxs-lookup"><span data-stu-id="7571c-116">Create a resource definition (.rc) file.</span></span> <span data-ttu-id="7571c-117">Diese Datei definiert die Ressourcentypen und deren Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7571c-117">This file defines the types of resources and their identifiers.</span></span> <span data-ttu-id="7571c-118">Die Ressourcendefinitionsdatei kann Verweise auf andere Dateien enthalten.</span><span class="sxs-lookup"><span data-stu-id="7571c-118">The resource definition file may include references to other files.</span></span> <span data-ttu-id="7571c-119">Beispielsweise wird eine Symbolressource in der RC-Datei deklariert, aber das Symbolbild wird in einer separaten Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7571c-119">For example, an icon resource is declared in the .rc file, but the icon image is stored in a separate file.</span></span>
2.  <span data-ttu-id="7571c-120">Verwenden Sie den Microsoft Windows-Ressourcencompiler (RC), um die Ressourcendefinitionsdatei in eine kompilierte Ressourcendatei (.res) zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="7571c-120">Use the Microsoft Windows Resource Compiler (RC) to compile the resource definition file into a compiled resource (.res) file.</span></span> <span data-ttu-id="7571c-121">Der RC-Compiler wird mit Visual Studio und auch dem Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7571c-121">The RC compiler is provided with Visual Studio and also the Windows SDK.</span></span>
3.  <span data-ttu-id="7571c-122">Verknüpfen Sie die kompilierte Ressourcendatei mit der Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="7571c-122">Link the compiled resource file to the binary file.</span></span>

<span data-ttu-id="7571c-123">Diese Schritte entsprechen in etwa dem Kompilierungs-/Linkprozess für Codedateien.</span><span class="sxs-lookup"><span data-stu-id="7571c-123">These steps are roughly equivalent to the compile/link process for code files.</span></span> <span data-ttu-id="7571c-124">Visual Studio stellt eine Reihe von Ressourcen-Editoren zur Verfügung, die das Erstellen und Ändern von Ressourcen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7571c-124">Visual Studio provides a set of resource editors that make it easy to create and modify resources.</span></span> <span data-ttu-id="7571c-125">(Diese Tools sind in den Express-Editionen von Visual Studio.) Eine RC-Datei ist jedoch einfach eine Textdatei, und die Syntax ist auf MSDN dokumentiert, sodass es möglich ist, eine RC-Datei mit einem beliebigen Text-Editor zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7571c-125">(These tools are not available in the Express editions of Visual Studio.) But an .rc file is simply a text file, and the syntax is documented on MSDN, so it is possible to create an .rc file using any text editor.</span></span> <span data-ttu-id="7571c-126">Weitere Informationen finden Sie unter [Informationen zu Ressourcendateien.](/windows/desktop/menurc/about-resource-files)</span><span class="sxs-lookup"><span data-stu-id="7571c-126">For more information, see [About Resource Files](/windows/desktop/menurc/about-resource-files).</span></span>

## <a name="defining-an-accelerator-table"></a><span data-ttu-id="7571c-127">Definieren einer Zugriffstastentabelle</span><span class="sxs-lookup"><span data-stu-id="7571c-127">Defining an Accelerator Table</span></span>

<span data-ttu-id="7571c-128">Eine Zugriffstastentabelle ist eine Tabelle mit Tastenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="7571c-128">An accelerator table is a table of keyboard shortcuts.</span></span> <span data-ttu-id="7571c-129">Jede Verknüpfung wird definiert durch:</span><span class="sxs-lookup"><span data-stu-id="7571c-129">Each shortcut is defined by:</span></span>

-   <span data-ttu-id="7571c-130">Ein numerischer Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7571c-130">A numeric identifier.</span></span> <span data-ttu-id="7571c-131">Diese Zahl gibt den Anwendungsbefehl an, der von der Verknüpfung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7571c-131">This number identifies the application command that will be invoked by the shortcut.</span></span>
-   <span data-ttu-id="7571c-132">Das ASCII-Zeichen oder der Virtuelle Schlüsselcode der Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="7571c-132">The ASCII character or virtual-key code of the shortcut.</span></span>
-   <span data-ttu-id="7571c-133">Optionale Modifizierertasten: ALT, UMSCHALT ODER STRG.</span><span class="sxs-lookup"><span data-stu-id="7571c-133">Optional modifier keys: ALT, SHIFT, or CTRL.</span></span>

<span data-ttu-id="7571c-134">Die Zugriffstastentabelle selbst verfügt über einen numerischen Bezeichner, der die Tabelle in der Liste der Anwendungsressourcen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7571c-134">The accelerator table itself has a numeric identifier, which identifies the table in the list of application resources.</span></span> <span data-ttu-id="7571c-135">Erstellen Sie eine Zugriffstastentabelle für ein einfaches Zeichenprogramm.</span><span class="sxs-lookup"><span data-stu-id="7571c-135">Let's create an accelerator table for a simple drawing program.</span></span> <span data-ttu-id="7571c-136">Dieses Programm hat zwei Modi: den Draw-Modus und den Auswahlmodus.</span><span class="sxs-lookup"><span data-stu-id="7571c-136">This program will have two modes, draw mode and selection mode.</span></span> <span data-ttu-id="7571c-137">Im Draw-Modus kann der Benutzer Formen zeichnen.</span><span class="sxs-lookup"><span data-stu-id="7571c-137">In draw mode, the user can draw shapes.</span></span> <span data-ttu-id="7571c-138">Im Auswahlmodus kann der Benutzer Formen auswählen.</span><span class="sxs-lookup"><span data-stu-id="7571c-138">In selection mode, the user can select shapes.</span></span> <span data-ttu-id="7571c-139">Für dieses Programm möchten wir die folgenden Tastenkombinationen definieren.</span><span class="sxs-lookup"><span data-stu-id="7571c-139">For this program, we would like to define the following keyboard shortcuts.</span></span>



| <span data-ttu-id="7571c-140">Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="7571c-140">Shortcut</span></span> | <span data-ttu-id="7571c-141">Get-Help</span><span class="sxs-lookup"><span data-stu-id="7571c-141">Command</span></span>                   |
|----------|---------------------------|
| <span data-ttu-id="7571c-142">STRG+M</span><span class="sxs-lookup"><span data-stu-id="7571c-142">CTRL+M</span></span>   | <span data-ttu-id="7571c-143">Umschalten zwischen Modi.</span><span class="sxs-lookup"><span data-stu-id="7571c-143">Toggle between modes.</span></span>     |
| <span data-ttu-id="7571c-144">F1</span><span class="sxs-lookup"><span data-stu-id="7571c-144">F1</span></span>       | <span data-ttu-id="7571c-145">Wechseln Sie in den Zeichnen-Modus.</span><span class="sxs-lookup"><span data-stu-id="7571c-145">Switch to draw mode.</span></span>      |
| <span data-ttu-id="7571c-146">F2</span><span class="sxs-lookup"><span data-stu-id="7571c-146">F2</span></span>       | <span data-ttu-id="7571c-147">Wechseln Sie in den Auswahlmodus.</span><span class="sxs-lookup"><span data-stu-id="7571c-147">Switch to selection mode.</span></span> |



 

<span data-ttu-id="7571c-148">Definieren Sie zunächst numerische Bezeichner für die Tabelle und für die Anwendungsbefehle.</span><span class="sxs-lookup"><span data-stu-id="7571c-148">First, define numeric identifiers for the table and for the application commands.</span></span> <span data-ttu-id="7571c-149">Diese Werte sind willkürlich.</span><span class="sxs-lookup"><span data-stu-id="7571c-149">These values are arbitrary.</span></span> <span data-ttu-id="7571c-150">Sie können symbolische Konstanten für die Bezeichner zuweisen, indem Sie sie in einer Headerdatei definieren.</span><span class="sxs-lookup"><span data-stu-id="7571c-150">You can assign symbolic constants for the identifiers by defining them in a header file.</span></span> <span data-ttu-id="7571c-151">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7571c-151">For example:</span></span>


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



<span data-ttu-id="7571c-152">In diesem Beispiel identifiziert der Wert `IDR_ACCEL1` die Zugriffstastentabelle, und die nächsten drei Konstanten definieren die Anwendungsbefehle.</span><span class="sxs-lookup"><span data-stu-id="7571c-152">In this example, the value `IDR_ACCEL1` identifies the accelerator table, and the next three constants define the application commands.</span></span> <span data-ttu-id="7571c-153">Standardmäßig wird eine Headerdatei, die Ressourcenkonstanten definiert, häufig resource.h genannt.</span><span class="sxs-lookup"><span data-stu-id="7571c-153">By convention, a header file that defines resource constants is often named resource.h.</span></span> <span data-ttu-id="7571c-154">In der nächsten Auflistung wird die Ressourcendefinitionsdatei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7571c-154">The next listing shows the resource definition file.</span></span>


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



<span data-ttu-id="7571c-155">Die Tastenkombinationen werden innerhalb der geschweiften Klammern definiert.</span><span class="sxs-lookup"><span data-stu-id="7571c-155">The accelerator shortcuts are defined within the curly braces.</span></span> <span data-ttu-id="7571c-156">Jede Verknüpfung enthält die folgenden Einträge.</span><span class="sxs-lookup"><span data-stu-id="7571c-156">Each shortcut contains the following entries.</span></span>

-   <span data-ttu-id="7571c-157">Der Code mit virtuellem Schlüssel oder ASCII-Zeichen, das die Verknüpfung aufruft.</span><span class="sxs-lookup"><span data-stu-id="7571c-157">The virtual-key code or ASCII character that invokes the shortcut.</span></span>
-   <span data-ttu-id="7571c-158">Der Anwendungsbefehl.</span><span class="sxs-lookup"><span data-stu-id="7571c-158">The application command.</span></span> <span data-ttu-id="7571c-159">Beachten Sie, dass im Beispiel symbolische Konstanten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7571c-159">Notice that symbolic constants are used in the example.</span></span> <span data-ttu-id="7571c-160">Die Ressourcendefinitionsdatei enthält resource.h, wobei diese Konstanten definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7571c-160">The resource definition file includes resource.h, where these constants are defined.</span></span>
-   <span data-ttu-id="7571c-161">Das Schlüsselwort **VIRTKEY** bedeutet, dass der erste Eintrag ein Virtueller Schlüsselcode ist.</span><span class="sxs-lookup"><span data-stu-id="7571c-161">The keyword **VIRTKEY** means the first entry is a virtual-key code.</span></span> <span data-ttu-id="7571c-162">Die andere Option ist die Verwendung von ASCII-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="7571c-162">The other option is to use ASCII characters.</span></span>
-   <span data-ttu-id="7571c-163">Optionale Modifizierer: ALT, CONTROL oder SHIFT.</span><span class="sxs-lookup"><span data-stu-id="7571c-163">Optional modifiers: ALT, CONTROL, or SHIFT.</span></span>

<span data-ttu-id="7571c-164">Wenn Sie ASCII-Zeichen für Tastenkombinationen verwenden, ist ein Kleinbuchstaben eine andere Verknüpfung als ein Großbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="7571c-164">If you use ASCII characters for shortcuts, then a lowercase character will be a different shortcut than an uppercase character.</span></span> <span data-ttu-id="7571c-165">(Wenn Sie z. B. "a" eingeben, kann ein anderer Befehl als die Eingabe von "A" aufgerufen werden.) Das kann benutzerverwendigend sein. Daher ist es im Allgemeinen besser, Codes mit virtuellen Schlüsseln anstelle von ASCII-Zeichen für Tastenkombinationen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7571c-165">(For example, typing 'a' might invoke a different command than typing 'A'.) That might confuse users, so it is generally better to use virtual-key codes, rather than ASCII characters, for shortcuts.</span></span>

## <a name="loading-the-accelerator-table"></a><span data-ttu-id="7571c-166">Laden der Zugriffstastentabelle</span><span class="sxs-lookup"><span data-stu-id="7571c-166">Loading the Accelerator Table</span></span>

<span data-ttu-id="7571c-167">Die Ressource für die Zugriffstastentabelle muss geladen werden, bevor das Programm sie verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="7571c-167">The resource for the accelerator table must be loaded before the program can use it.</span></span> <span data-ttu-id="7571c-168">Um eine Zugriffstastentabelle zu laden, rufen Sie die [**LoadAccelerators-Funktion**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) auf.</span><span class="sxs-lookup"><span data-stu-id="7571c-168">To load an accelerator table, call the [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) function.</span></span>


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



<span data-ttu-id="7571c-169">Rufen Sie diese Funktion auf, bevor Sie die Meldungsschleife eingeben.</span><span class="sxs-lookup"><span data-stu-id="7571c-169">Call this function before you enter the message loop.</span></span> <span data-ttu-id="7571c-170">Der erste Parameter ist das Handle für das Modul.</span><span class="sxs-lookup"><span data-stu-id="7571c-170">The first parameter is the handle to the module.</span></span> <span data-ttu-id="7571c-171">(Dieser Parameter wird an Ihre [**WinMain-Funktion**](/windows/desktop/api/winbase/nf-winbase-winmain) übergeben.</span><span class="sxs-lookup"><span data-stu-id="7571c-171">(This parameter is passed to your [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="7571c-172">Weitere Informationen finden Sie unter [WinMain: Der Anwendungseinstiegspunkt](winmain--the-application-entry-point.md).) Der zweite Parameter ist der Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="7571c-172">For details, see [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).) The second parameter is the resource identifier.</span></span> <span data-ttu-id="7571c-173">Die Funktion gibt ein Handle an die Ressource zurück.</span><span class="sxs-lookup"><span data-stu-id="7571c-173">The function returns a handle to the resource.</span></span> <span data-ttu-id="7571c-174">Denken Sie daran, dass ein Handle ein nicht transparenter Typ ist, der auf ein vom System verwaltetes Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="7571c-174">Recall that a handle is an opaque type that refers to an object managed by the system.</span></span> <span data-ttu-id="7571c-175">Wenn die Funktion fehlschlägt, gibt sie **NULL zurück.**</span><span class="sxs-lookup"><span data-stu-id="7571c-175">If the function fails, it returns **NULL**.</span></span>

<span data-ttu-id="7571c-176">Sie können eine Zugriffstastentabelle durch Aufrufen [**von DestroyAcceleratorTable veröffentlichen.**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable)</span><span class="sxs-lookup"><span data-stu-id="7571c-176">You can release an accelerator table by calling [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span></span> <span data-ttu-id="7571c-177">Allerdings gibt das System die Tabelle automatisch frei, wenn das Programm beendet wird. Daher müssen Sie diese Funktion nur aufrufen, wenn Sie eine Tabelle durch eine andere ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7571c-177">However, the system automatically releases the table when the program exits, so you only need to call this function if you are replacing one table with another.</span></span> <span data-ttu-id="7571c-178">Ein interessantes Beispiel hierfür finden Sie im Thema Creating User Editable Accelerators (Erstellen von [bearbeitbaren Beschleunigern für Benutzer).](/windows/desktop/menurc/using-keyboard-accelerators)</span><span class="sxs-lookup"><span data-stu-id="7571c-178">There is an interesting example of this in the topic [Creating User Editable Accelerators](/windows/desktop/menurc/using-keyboard-accelerators).</span></span>

## <a name="translating-key-strokes-into-commands"></a><span data-ttu-id="7571c-179">Übersetzen von Tastenstrichen in Befehle</span><span class="sxs-lookup"><span data-stu-id="7571c-179">Translating Key Strokes into Commands</span></span>

<span data-ttu-id="7571c-180">Eine Zugriffstastentabelle übersetzt Schlüsselstriche in [**WM \_ COMMAND-Meldungen.**](/windows/desktop/menurc/wm-command)</span><span class="sxs-lookup"><span data-stu-id="7571c-180">An accelerator table works by translating key strokes into [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="7571c-181">Der *wParam-Parameter* von **WM \_ COMMAND** enthält den numerischen Bezeichner des Befehls.</span><span class="sxs-lookup"><span data-stu-id="7571c-181">The *wParam* parameter of **WM\_COMMAND** contains the numeric identifier of the command.</span></span> <span data-ttu-id="7571c-182">Wenn Sie beispielsweise die zuvor gezeigte Tabelle verwenden, wird der Tastenstrich STRG+M in eine **WM \_ COMMAND-Meldung** mit dem Wert `ID_TOGGLE_MODE` übersetzt.</span><span class="sxs-lookup"><span data-stu-id="7571c-182">For example, using the table shown previously, the key stroke CTRL+M is translated into a **WM\_COMMAND** message with the value `ID_TOGGLE_MODE`.</span></span> <span data-ttu-id="7571c-183">Um dies zu ermöglichen, ändern Sie die Nachrichtenschleife wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7571c-183">To make this happen, change your message loop to the following:</span></span>


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



<span data-ttu-id="7571c-184">Dieser Code fügt einen Aufruf der [**TranslateAccelerator-Funktion**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) innerhalb der Nachrichtenschleife hinzu.</span><span class="sxs-lookup"><span data-stu-id="7571c-184">This code adds a call to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function inside the message loop.</span></span> <span data-ttu-id="7571c-185">Die **TranslateAccelerator-Funktion** untersucht jede Fenstermeldung und sucht nach Key-Down-Meldungen.</span><span class="sxs-lookup"><span data-stu-id="7571c-185">The **TranslateAccelerator** function examines each window message, looking for key-down messages.</span></span> <span data-ttu-id="7571c-186">Wenn der Benutzer eine der in der Zugriffstastentabelle aufgeführten Tastenkombinationen drückt, sendet **TranslateAccelerator** eine [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) an das Fenster.</span><span class="sxs-lookup"><span data-stu-id="7571c-186">If the user presses one of the key combinations listed in the accelerator table, **TranslateAccelerator** sends a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message to the window.</span></span> <span data-ttu-id="7571c-187">Die Funktion sendet **WM \_ COMMAND,** indem sie die Fensterprozedur direkt aufruft.</span><span class="sxs-lookup"><span data-stu-id="7571c-187">The function sends **WM\_COMMAND** by directly invoking the window procedure.</span></span> <span data-ttu-id="7571c-188">Wenn **TranslateAccelerator** einen Schlüsselstrich erfolgreich übersetzt, gibt die Funktion einen Wert ungleich 0 (null) zurück. Das bedeutet, dass Sie die normale Verarbeitung für die Nachricht überspringen sollten.</span><span class="sxs-lookup"><span data-stu-id="7571c-188">When **TranslateAccelerator** successfully translates a key stroke, the function returns a non-zero value, which means you should skip the normal processing for the message.</span></span> <span data-ttu-id="7571c-189">Andernfalls gibt **TranslateAccelerator** 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="7571c-189">Otherwise, **TranslateAccelerator** returns zero.</span></span> <span data-ttu-id="7571c-190">Übergeben Sie in diesem Fall die Fenstermeldung wie gewohnt an [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) und [**DispatchMessage.**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)</span><span class="sxs-lookup"><span data-stu-id="7571c-190">In that case, pass the window message to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), as normal.</span></span>

<span data-ttu-id="7571c-191">Im Folgenden wird erläutert, wie das Zeichnungsprogramm die [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) behandeln kann:</span><span class="sxs-lookup"><span data-stu-id="7571c-191">Here is how the drawing program might handle the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message:</span></span>


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



<span data-ttu-id="7571c-192">In diesem Code wird davon ausgegangen, dass `SetMode` eine funktion ist, die von der Anwendung definiert wird, um zwischen den beiden Modi zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="7571c-192">This code assumes that `SetMode` is a function defined by the application to switch between the two modes.</span></span> <span data-ttu-id="7571c-193">Die Details dazu, wie Sie jeden Befehl behandeln würden, hängen natürlich von Ihrem Programm ab.</span><span class="sxs-lookup"><span data-stu-id="7571c-193">The details of how you would handle each command obviously depend on your program.</span></span>

## <a name="next"></a><span data-ttu-id="7571c-194">Nächste</span><span class="sxs-lookup"><span data-stu-id="7571c-194">Next</span></span>

[<span data-ttu-id="7571c-195">Festlegen des Cursorbilds</span><span class="sxs-lookup"><span data-stu-id="7571c-195">Setting the Cursor Image</span></span>](setting-the-cursor-image.md)

 

 
