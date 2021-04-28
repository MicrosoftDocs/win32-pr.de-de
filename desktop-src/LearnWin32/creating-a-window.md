---
title: Erstellen eines Fensters
description: Erstellen eines Fensters
ms.assetid: e036519f-26b5-436c-b909-bb280d758e81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea5ec39187b389405d3c6d8eca475944278a3d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103968"
---
# <a name="creating-a-window"></a><span data-ttu-id="992b2-103">Erstellen eines Fensters</span><span class="sxs-lookup"><span data-stu-id="992b2-103">Creating a Window</span></span>

## <a name="window-classes"></a><span data-ttu-id="992b2-104">Fensterklassen</span><span class="sxs-lookup"><span data-stu-id="992b2-104">Window Classes</span></span>

<span data-ttu-id="992b2-105">Eine *Fensterklasse* definiert eine Reihe von Verhaltensweisen, die mehrere Fenster gemeinsam haben können.</span><span class="sxs-lookup"><span data-stu-id="992b2-105">A *window class* defines a set of behaviors that several windows might have in common.</span></span> <span data-ttu-id="992b2-106">Beispielsweise weist jede Schaltfläche in einer Gruppe von Schaltflächen ein ähnliches Verhalten auf, wenn der Benutzer auf die Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="992b2-106">For example, in a group of buttons, each button has a similar behavior when the user clicks the button.</span></span> <span data-ttu-id="992b2-107">Natürlich sind Schaltflächen nicht vollständig identisch. Jede Schaltfläche zeigt eine eigene Textzeichenfolge an und verfügt über eigene Bildschirmkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="992b2-107">Of course, buttons are not completely identical; each button displays its own text string and has its own screen coordinates.</span></span> <span data-ttu-id="992b2-108">Daten, die für jedes Fenster eindeutig sind, werden als *Instanzdaten* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="992b2-108">Data that is unique for each window is called *instance data*.</span></span>

<span data-ttu-id="992b2-109">Jedes Fenster muss einer Fensterklasse zugeordnet werden, auch wenn das Programm nur eine Instanz dieser Klasse erstellt.</span><span class="sxs-lookup"><span data-stu-id="992b2-109">Every window must be associated with a window class, even if your program only ever creates one instance of that class.</span></span> <span data-ttu-id="992b2-110">Es ist wichtig zu verstehen, dass eine Fensterklasse im C++-Sinn keine "Klasse" ist.</span><span class="sxs-lookup"><span data-stu-id="992b2-110">It is important to understand that a window class is not a "class" in the C++ sense.</span></span> <span data-ttu-id="992b2-111">Stattdessen handelt es sich um eine Datenstruktur, die intern vom Betriebssystem verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="992b2-111">Rather, it is a data structure used internally by the operating system.</span></span> <span data-ttu-id="992b2-112">Fensterklassen werden zur Laufzeit beim System registriert.</span><span class="sxs-lookup"><span data-stu-id="992b2-112">Window classes are registered with the system at run time.</span></span> <span data-ttu-id="992b2-113">Um eine neue Fensterklasse zu registrieren, füllen Sie zunächst eine [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) aus:</span><span class="sxs-lookup"><span data-stu-id="992b2-113">To register a new window class, start by filling in a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure:</span></span>

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

<span data-ttu-id="992b2-114">Sie müssen die folgenden Strukturmember festlegen:</span><span class="sxs-lookup"><span data-stu-id="992b2-114">You must set the following structure members:</span></span>

- <span data-ttu-id="992b2-115">**lpfnWndProc** ist ein Zeiger auf eine anwendungsdefinierte Funktion, die als *Fensterprozedur* oder "Fensterprozedur" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="992b2-115">**lpfnWndProc** is a pointer to an application-defined function called the *window procedure* or "window proc."</span></span> <span data-ttu-id="992b2-116">Die Fensterprozedur definiert den Großteil des Verhaltens des Fensters.</span><span class="sxs-lookup"><span data-stu-id="992b2-116">The window procedure defines most of the behavior of the window.</span></span> <span data-ttu-id="992b2-117">Wir untersuchen die Fensterprozedur später im Detail.</span><span class="sxs-lookup"><span data-stu-id="992b2-117">We'll examine the window procedure in detail later.</span></span> <span data-ttu-id="992b2-118">Behandeln Sie dies vorerst nur als Vorwärtsverweis.</span><span class="sxs-lookup"><span data-stu-id="992b2-118">For now, just treat this as a forward reference.</span></span>
- <span data-ttu-id="992b2-119">**hInstance** ist das Handle für die Anwendungsinstanz.</span><span class="sxs-lookup"><span data-stu-id="992b2-119">**hInstance** is the handle to the application instance.</span></span> <span data-ttu-id="992b2-120">Abrufen dieses Werts aus dem *hInstance-Parameter* von **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="992b2-120">Get this value from the *hInstance* parameter of **wWinMain**.</span></span>
- <span data-ttu-id="992b2-121">**lpszClassName** ist eine Zeichenfolge, die die Fensterklasse identifiziert.</span><span class="sxs-lookup"><span data-stu-id="992b2-121">**lpszClassName** is a string that identifies the window class.</span></span>

<span data-ttu-id="992b2-122">Klassennamen sind lokal für den aktuellen Prozess, sodass der Name nur innerhalb des Prozesses eindeutig sein muss.</span><span class="sxs-lookup"><span data-stu-id="992b2-122">Class names are local to the current process, so the name only needs to be unique within the process.</span></span> <span data-ttu-id="992b2-123">Die Windows-Standardsteuerelemente verfügen jedoch auch über Klassen.</span><span class="sxs-lookup"><span data-stu-id="992b2-123">However, the standard Windows controls also have classes.</span></span> <span data-ttu-id="992b2-124">Wenn Sie eines dieser Steuerelemente verwenden, müssen Sie Klassennamen auswählen, die keinen Konflikt mit den Steuerelementklassennamen verursachen.</span><span class="sxs-lookup"><span data-stu-id="992b2-124">If you use any of those controls, you must pick class names that do not conflict with the control class names.</span></span> <span data-ttu-id="992b2-125">Die Fensterklasse für das Schaltflächensteuerelement heißt z. B. "Button".</span><span class="sxs-lookup"><span data-stu-id="992b2-125">For example, the window class for the button control is named "Button".</span></span>

<span data-ttu-id="992b2-126">Die [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) verfügt über andere Member, die hier nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="992b2-126">The [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure has other members not shown here.</span></span> <span data-ttu-id="992b2-127">Sie können wie in diesem Beispiel gezeigt auf 0 (null) festlegen oder sie ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="992b2-127">You can set them to zero, as shown in this example, or fill them in.</span></span> <span data-ttu-id="992b2-128">In der MSDN-Dokumentation wird die Struktur ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="992b2-128">The MSDN documentation describes the structure in detail.</span></span>

<span data-ttu-id="992b2-129">Übergeben Sie als Nächstes die Adresse der [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) an die [**RegisterClass-Funktion.**](/windows/desktop/api/winuser/nf-winuser-registerclassa)</span><span class="sxs-lookup"><span data-stu-id="992b2-129">Next, pass the address of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span> <span data-ttu-id="992b2-130">Diese Funktion registriert die Fensterklasse beim Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="992b2-130">This function registers the window class with the operating system.</span></span>

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a><span data-ttu-id="992b2-131">Erstellen des Fensters</span><span class="sxs-lookup"><span data-stu-id="992b2-131">Creating the Window</span></span>

<span data-ttu-id="992b2-132">Um eine neue Instanz eines Fensters zu erstellen, rufen Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) auf:</span><span class="sxs-lookup"><span data-stu-id="992b2-132">To create a new instance of a window, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function:</span></span>

```C++
HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}
```

<span data-ttu-id="992b2-133">Ausführliche Parameterbeschreibungen finden Sie auf MSDN, aber hier finden Sie eine kurze Zusammenfassung:</span><span class="sxs-lookup"><span data-stu-id="992b2-133">You can read detailed parameter descriptions on MSDN, but here is a quick summary:</span></span>

- <span data-ttu-id="992b2-134">Mit dem ersten Parameter können Sie einige optionale Verhaltensweisen für das Fenster angeben (z. B. transparente Fenster).</span><span class="sxs-lookup"><span data-stu-id="992b2-134">The first parameter lets you specify some optional behaviors for the window (for example, transparent windows).</span></span> <span data-ttu-id="992b2-135">Legen Sie diesen Parameter für die Standardverhalten auf 0 (null) fest.</span><span class="sxs-lookup"><span data-stu-id="992b2-135">Set this parameter to zero for the default behaviors.</span></span>
- <span data-ttu-id="992b2-136">`CLASS_NAME` ist der Name der Fensterklasse.</span><span class="sxs-lookup"><span data-stu-id="992b2-136">`CLASS_NAME` is the name of the window class.</span></span> <span data-ttu-id="992b2-137">Dadurch wird der Typ des Fensters definiert, das Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="992b2-137">This defines the type of window you are creating.</span></span>
- <span data-ttu-id="992b2-138">Der Fenstertext wird von verschiedenen Fenstertypen auf unterschiedliche Weise verwendet.</span><span class="sxs-lookup"><span data-stu-id="992b2-138">The window text is used in different ways by different types of windows.</span></span> <span data-ttu-id="992b2-139">Wenn das Fenster über eine Titelleiste verfügt, wird der Text in der Titelleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="992b2-139">If the window has a title bar, the text is displayed in the title bar.</span></span>
- <span data-ttu-id="992b2-140">Der Fensterstil ist ein Satz von Flags, die einen Teil des Aussehens und Aussehens eines Fensters definieren.</span><span class="sxs-lookup"><span data-stu-id="992b2-140">The window style is a set of flags that define some of the look and feel of a window.</span></span> <span data-ttu-id="992b2-141">Die Konstante **WS \_ OVERLAPPEDWINDOW** besteht eigentlich aus mehreren Flags, die mit einem bitweisen **OR** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="992b2-141">The constant **WS\_OVERLAPPEDWINDOW** is actually several flags combined with a bitwise **OR**.</span></span> <span data-ttu-id="992b2-142">Zusammen geben diese Flags dem Fenster eine Titelleiste, einen Rahmen, ein Systemmenü und die Schaltflächen **Minimieren** und **Maximieren.**</span><span class="sxs-lookup"><span data-stu-id="992b2-142">Together these flags give the window a title bar, a border, a system menu, and **Minimize** and **Maximize** buttons.</span></span> <span data-ttu-id="992b2-143">Dieser Satz von Flags ist der gängigste Stil für ein Anwendungsfenster der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="992b2-143">This set of flags is the most common style for a top-level application window.</span></span>
- <span data-ttu-id="992b2-144">Für Position und Größe bedeutet die konstante **CW \_ USEDEFAULT** die Verwendung von Standardwerten.</span><span class="sxs-lookup"><span data-stu-id="992b2-144">For position and size, the constant **CW\_USEDEFAULT** means to use default values.</span></span>
- <span data-ttu-id="992b2-145">Der nächste Parameter legt ein übergeordnetes Fenster oder Besitzerfenster für das neue Fenster fest.</span><span class="sxs-lookup"><span data-stu-id="992b2-145">The next parameter sets a parent window or owner window for the new window.</span></span> <span data-ttu-id="992b2-146">Legen Sie das übergeordnete Element fest, wenn Sie ein untergeordnetes Fenster erstellen.</span><span class="sxs-lookup"><span data-stu-id="992b2-146">Set the parent if you are creating a child window.</span></span> <span data-ttu-id="992b2-147">Legen Sie für ein Fenster der obersten Ebene diese auf **NULL** fest.</span><span class="sxs-lookup"><span data-stu-id="992b2-147">For a top-level window, set this to **NULL**.</span></span>
- <span data-ttu-id="992b2-148">Für ein Anwendungsfenster definiert der nächste Parameter das Menü für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="992b2-148">For an application window, the next parameter defines the menu for the window.</span></span> <span data-ttu-id="992b2-149">In diesem Beispiel wird kein Menü verwendet, sodass der Wert **NULL** ist.</span><span class="sxs-lookup"><span data-stu-id="992b2-149">This example does not use a menu, so the value is **NULL**.</span></span>
- <span data-ttu-id="992b2-150">*hInstance* ist das zuvor beschriebene Instanzhandle.</span><span class="sxs-lookup"><span data-stu-id="992b2-150">*hInstance* is the instance handle, described previously.</span></span> <span data-ttu-id="992b2-151">(Siehe [WinMain: Der Anwendungseinstiegspunkt.)](winmain--the-application-entry-point.md)</span><span class="sxs-lookup"><span data-stu-id="992b2-151">(See [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).)</span></span>
- <span data-ttu-id="992b2-152">Der letzte Parameter ist ein Zeiger auf beliebige Daten vom Typ **void \***.</span><span class="sxs-lookup"><span data-stu-id="992b2-152">The last parameter is a pointer to arbitrary data of type **void\***.</span></span> <span data-ttu-id="992b2-153">Sie können diesen Wert verwenden, um eine Datenstruktur an Ihre Fensterprozedur zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="992b2-153">You can use this value to pass a data structure to your window procedure.</span></span> <span data-ttu-id="992b2-154">Im Abschnitt Verwalten des [Anwendungszustands](managing-application-state-.md)wird eine mögliche Möglichkeit zur Verwendung dieses Parameters gezeigt.</span><span class="sxs-lookup"><span data-stu-id="992b2-154">We'll show one possible way to use this parameter in the section [Managing Application State](managing-application-state-.md).</span></span>

<span data-ttu-id="992b2-155">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) gibt ein Handle für das neue Fenster oder 0 (null) zurück, wenn die Funktion fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="992b2-155">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) returns a handle to the new window, or zero if the function fails.</span></span> <span data-ttu-id="992b2-156">Übergeben Sie das Fensterhandle an die [**ShowWindow-Funktion,**](/windows/desktop/api/winuser/nf-winuser-showwindow) um das Fenster anzuzeigen, d. b. das Fenster sichtbar zu machen:</span><span class="sxs-lookup"><span data-stu-id="992b2-156">To show the window—that is, make the window visible —pass the window handle to the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function:</span></span>

```C++
ShowWindow(hwnd, nCmdShow);
```

<span data-ttu-id="992b2-157">Der *hwnd-Parameter* ist das Fensterhandle, das von [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="992b2-157">The *hwnd* parameter is the window handle returned by [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="992b2-158">Der *nCmdShow-Parameter* kann verwendet werden, um ein Fenster zu minimieren oder zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="992b2-158">The *nCmdShow* parameter can be used to minimize or maximize a window.</span></span> <span data-ttu-id="992b2-159">Das Betriebssystem übergibt diesen Wert über die **wWinMain-Funktion** an das Programm.</span><span class="sxs-lookup"><span data-stu-id="992b2-159">The operating system passes this value to the program through the **wWinMain** function.</span></span>

<span data-ttu-id="992b2-160">Hier ist der vollständige Code zum Erstellen des Fensters.</span><span class="sxs-lookup"><span data-stu-id="992b2-160">Here is the complete code to create the window.</span></span> <span data-ttu-id="992b2-161">Denken Sie daran, dass `WindowProc` immer noch nur eine Vorwärtsdeklaration einer Funktion ist.</span><span class="sxs-lookup"><span data-stu-id="992b2-161">Remember that `WindowProc` is still just a forward declaration of a function.</span></span>

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;

RegisterClass(&wc);

// Create the window.

HWND hwnd = CreateWindowEx(
    0,                              // Optional window styles.
    CLASS_NAME,                     // Window class
    L"Learn to Program Windows",    // Window text
    WS_OVERLAPPEDWINDOW,            // Window style

    // Size and position
    CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,

    NULL,       // Parent window    
    NULL,       // Menu
    hInstance,  // Instance handle
    NULL        // Additional application data
    );

if (hwnd == NULL)
{
    return 0;
}

ShowWindow(hwnd, nCmdShow);
```

<span data-ttu-id="992b2-162">Herzlichen Glückwunsch, Sie haben ein Fenster erstellt!</span><span class="sxs-lookup"><span data-stu-id="992b2-162">Congratulations, you've created a window!</span></span> <span data-ttu-id="992b2-163">Derzeit enthält das Fenster keine Inhalte und interagiert nicht mit dem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="992b2-163">Right now, the window does not contain any content or interact with the user.</span></span> <span data-ttu-id="992b2-164">In einer echten GUI-Anwendung würde das Fenster auf Ereignisse des Benutzers und des Betriebssystems reagieren.</span><span class="sxs-lookup"><span data-stu-id="992b2-164">In a real GUI application, the window would respond to events from the user and the operating system.</span></span> <span data-ttu-id="992b2-165">Im nächsten Abschnitt wird beschrieben, wie Fenstermeldungen diese Art von Interaktivität bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="992b2-165">The next section describes how window messages provide this sort of interactivity.</span></span>

### <a name="next"></a><span data-ttu-id="992b2-166">Nächste</span><span class="sxs-lookup"><span data-stu-id="992b2-166">Next</span></span>

[<span data-ttu-id="992b2-167">Fenstermeldungen</span><span class="sxs-lookup"><span data-stu-id="992b2-167">Window Messages</span></span>](window-messages.md)
