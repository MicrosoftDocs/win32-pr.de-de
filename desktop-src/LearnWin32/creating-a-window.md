---
title: Erstellen eines Fensters
description: .
ms.assetid: e036519f-26b5-436c-b909-bb280d758e81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126f040d72fec423ad5b6f3ecb31bc780a3192b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390329"
---
# <a name="creating-a-window"></a><span data-ttu-id="07645-103">Erstellen eines Fensters</span><span class="sxs-lookup"><span data-stu-id="07645-103">Creating a Window</span></span>

## <a name="window-classes"></a><span data-ttu-id="07645-104">Fensterklassen</span><span class="sxs-lookup"><span data-stu-id="07645-104">Window Classes</span></span>

<span data-ttu-id="07645-105">Eine *Fenster Klasse* definiert eine Reihe von Verhaltensweisen, die mehrere Fenster gemeinsam haben können.</span><span class="sxs-lookup"><span data-stu-id="07645-105">A *window class* defines a set of behaviors that several windows might have in common.</span></span> <span data-ttu-id="07645-106">Beispielsweise weist eine Schaltfläche in einer Gruppe von Schaltflächen ein ähnliches Verhalten auf, wenn der Benutzer auf die Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="07645-106">For example, in a group of buttons, each button has a similar behavior when the user clicks the button.</span></span> <span data-ttu-id="07645-107">Natürlich sind die Schaltflächen nicht vollständig identisch. jede Schaltfläche zeigt eine eigene Text Zeichenfolge an und verfügt über eigene Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="07645-107">Of course, buttons are not completely identical; each button displays its own text string and has its own screen coordinates.</span></span> <span data-ttu-id="07645-108">Daten, die für jedes Fenster eindeutig sind, werden als *Instanzdaten* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="07645-108">Data that is unique for each window is called *instance data*.</span></span>

<span data-ttu-id="07645-109">Jedes Fenster muss einer Fenster Klasse zugeordnet werden, auch wenn das Programm immer nur eine Instanz dieser Klasse erstellt.</span><span class="sxs-lookup"><span data-stu-id="07645-109">Every window must be associated with a window class, even if your program only ever creates one instance of that class.</span></span> <span data-ttu-id="07645-110">Es ist wichtig zu verstehen, dass eine Fenster Klasse nicht "Class" in der C++ Sense ist.</span><span class="sxs-lookup"><span data-stu-id="07645-110">It is important to understand that a window class is not a "class" in the C++ sense.</span></span> <span data-ttu-id="07645-111">Vielmehr handelt es sich um eine Datenstruktur, die intern vom Betriebssystem verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="07645-111">Rather, it is a data structure used internally by the operating system.</span></span> <span data-ttu-id="07645-112">Fenster Klassen werden zur Laufzeit beim System registriert.</span><span class="sxs-lookup"><span data-stu-id="07645-112">Window classes are registered with the system at run time.</span></span> <span data-ttu-id="07645-113">Um eine neue Fenster Klasse zu registrieren, müssen Sie zunächst eine [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur ausfüllen:</span><span class="sxs-lookup"><span data-stu-id="07645-113">To register a new window class, start by filling in a [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure:</span></span>

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

<span data-ttu-id="07645-114">Sie müssen die folgenden Strukturmember festlegen:</span><span class="sxs-lookup"><span data-stu-id="07645-114">You must set the following structure members:</span></span>

- <span data-ttu-id="07645-115">**lpfnwndproc** ist ein Zeiger auf eine Anwendungs definierte Funktion, die als *Fenster Prozedur* oder "Fenster proc" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="07645-115">**lpfnWndProc** is a pointer to an application-defined function called the *window procedure* or "window proc."</span></span> <span data-ttu-id="07645-116">Die Fenster Prozedur definiert den größten Teil des Verhaltens des Fensters.</span><span class="sxs-lookup"><span data-stu-id="07645-116">The window procedure defines most of the behavior of the window.</span></span> <span data-ttu-id="07645-117">Die Fenster Prozedur wird später ausführlich untersucht.</span><span class="sxs-lookup"><span data-stu-id="07645-117">We'll examine the window procedure in detail later.</span></span> <span data-ttu-id="07645-118">Behandeln Sie dies vorerst als vorwärts Verweis.</span><span class="sxs-lookup"><span data-stu-id="07645-118">For now, just treat this as a forward reference.</span></span>
- <span data-ttu-id="07645-119">**HINSTANCE** ist das Handle für die Anwendungs Instanz.</span><span class="sxs-lookup"><span data-stu-id="07645-119">**hInstance** is the handle to the application instance.</span></span> <span data-ttu-id="07645-120">Diesen Wert erhalten Sie vom *HINSTANCE* -Parameter von **wWinMain**.</span><span class="sxs-lookup"><span data-stu-id="07645-120">Get this value from the *hInstance* parameter of **wWinMain**.</span></span>
- <span data-ttu-id="07645-121">**lpszClassName** ist eine Zeichenfolge, die die Fenster Klasse identifiziert.</span><span class="sxs-lookup"><span data-stu-id="07645-121">**lpszClassName** is a string that identifies the window class.</span></span>

<span data-ttu-id="07645-122">Klassennamen sind für den aktuellen Prozess lokal, sodass der Name nur innerhalb des Prozesses eindeutig sein muss.</span><span class="sxs-lookup"><span data-stu-id="07645-122">Class names are local to the current process, so the name only needs to be unique within the process.</span></span> <span data-ttu-id="07645-123">Die standardmäßigen Windows-Steuerelemente verfügen jedoch auch über Klassen.</span><span class="sxs-lookup"><span data-stu-id="07645-123">However, the standard Windows controls also have classes.</span></span> <span data-ttu-id="07645-124">Wenn Sie eines dieser Steuerelemente verwenden, müssen Sie Klassennamen auswählen, die nicht mit den Steuerelement Klassennamen in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="07645-124">If you use any of those controls, you must pick class names that do not conflict with the control class names.</span></span> <span data-ttu-id="07645-125">Beispielsweise hat die Fenster Klasse für das Schaltflächen-Steuerelement den Namen "Button".</span><span class="sxs-lookup"><span data-stu-id="07645-125">For example, the window class for the button control is named "Button".</span></span>

<span data-ttu-id="07645-126">Die [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur enthält andere Member, die hier nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="07645-126">The [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure has other members not shown here.</span></span> <span data-ttu-id="07645-127">Sie können Sie auf 0 (null) festlegen, wie im folgenden Beispiel gezeigt, oder Sie können Sie in ausfüllen.</span><span class="sxs-lookup"><span data-stu-id="07645-127">You can set them to zero, as shown in this example, or fill them in.</span></span> <span data-ttu-id="07645-128">In der MSDN-Dokumentation wird die Struktur ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="07645-128">The MSDN documentation describes the structure in detail.</span></span>

<span data-ttu-id="07645-129">Übergeben Sie anschließend die Adresse der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur an die [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="07645-129">Next, pass the address of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure to the [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function.</span></span> <span data-ttu-id="07645-130">Diese Funktion registriert die Fenster Klasse beim Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="07645-130">This function registers the window class with the operating system.</span></span>

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a><span data-ttu-id="07645-131">Erstellen des Fensters</span><span class="sxs-lookup"><span data-stu-id="07645-131">Creating the Window</span></span>

<span data-ttu-id="07645-132">Um eine neue Instanz eines Fensters zu erstellen, rufen Sie die Funktion "up- [**windowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " auf:</span><span class="sxs-lookup"><span data-stu-id="07645-132">To create a new instance of a window, call the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function:</span></span>

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

<span data-ttu-id="07645-133">Sie können ausführliche Parameter Beschreibungen auf MSDN lesen, aber hier finden Sie eine kurze Zusammenfassung:</span><span class="sxs-lookup"><span data-stu-id="07645-133">You can read detailed parameter descriptions on MSDN, but here is a quick summary:</span></span>

- <span data-ttu-id="07645-134">Mit dem ersten Parameter können Sie einige optionale Verhalten für das Fenster angeben (z. b. transparente Fenster).</span><span class="sxs-lookup"><span data-stu-id="07645-134">The first parameter lets you specify some optional behaviors for the window (for example, transparent windows).</span></span> <span data-ttu-id="07645-135">Legen Sie diesen Parameter für das Standardverhalten auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="07645-135">Set this parameter to zero for the default behaviors.</span></span>
- <span data-ttu-id="07645-136">`CLASS_NAME` der Name der Fenster Klasse.</span><span class="sxs-lookup"><span data-stu-id="07645-136">`CLASS_NAME` is the name of the window class.</span></span> <span data-ttu-id="07645-137">Hiermit wird der Typ des Fensters definiert, das Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="07645-137">This defines the type of window you are creating.</span></span>
- <span data-ttu-id="07645-138">Der Fenster Text wird von unterschiedlichen Windows-Typen auf unterschiedliche Weise verwendet.</span><span class="sxs-lookup"><span data-stu-id="07645-138">The window text is used in different ways by different types of windows.</span></span> <span data-ttu-id="07645-139">Wenn das Fenster über eine Titelleiste verfügt, wird der Text in der Titelleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="07645-139">If the window has a title bar, the text is displayed in the title bar.</span></span>
- <span data-ttu-id="07645-140">Der Fenster Stil ist ein Satz von Flags, die ein paar aus dem Aussehen und dem Gefühl eines Fensters definieren.</span><span class="sxs-lookup"><span data-stu-id="07645-140">The window style is a set of flags that define some of the look and feel of a window.</span></span> <span data-ttu-id="07645-141">Die Konstante **WS \_ overlappedwindow** ist tatsächlich mehrere Flags, die mit einem bitweisen **or** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="07645-141">The constant **WS\_OVERLAPPEDWINDOW** is actually several flags combined with a bitwise **OR**.</span></span> <span data-ttu-id="07645-142">Diese Flags versehen das Fenster in einer Titelleiste, einem Rahmen, einem Systemmenü und den Schaltflächen **minimieren** und **Maxi** mieren.</span><span class="sxs-lookup"><span data-stu-id="07645-142">Together these flags give the window a title bar, a border, a system menu, and **Minimize** and **Maximize** buttons.</span></span> <span data-ttu-id="07645-143">Diese Gruppe von Flags ist der gängigste Stil für ein Anwendungsfenster der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="07645-143">This set of flags is the most common style for a top-level application window.</span></span>
- <span data-ttu-id="07645-144">Für Position und Größe bedeutet die Konstante **CW \_ usedefault** , dass Standardwerte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07645-144">For position and size, the constant **CW\_USEDEFAULT** means to use default values.</span></span>
- <span data-ttu-id="07645-145">Mit dem nächsten Parameter wird ein übergeordnetes Fenster oder Besitzer Fenster für das neue Fenster festgelegt.</span><span class="sxs-lookup"><span data-stu-id="07645-145">The next parameter sets a parent window or owner window for the new window.</span></span> <span data-ttu-id="07645-146">Legen Sie das übergeordnete Fenster fest, wenn Sie ein untergeordnetes Fenster erstellen.</span><span class="sxs-lookup"><span data-stu-id="07645-146">Set the parent if you are creating a child window.</span></span> <span data-ttu-id="07645-147">Legen Sie für ein Fenster der obersten Ebene diesen Wert auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="07645-147">For a top-level window, set this to **NULL**.</span></span>
- <span data-ttu-id="07645-148">Bei einem Anwendungsfenster definiert der nächste Parameter das Menü für das Fenster.</span><span class="sxs-lookup"><span data-stu-id="07645-148">For an application window, the next parameter defines the menu for the window.</span></span> <span data-ttu-id="07645-149">In diesem Beispiel wird kein Menü verwendet, daher ist der Wert **null**.</span><span class="sxs-lookup"><span data-stu-id="07645-149">This example does not use a menu, so the value is **NULL**.</span></span>
- <span data-ttu-id="07645-150">*HINSTANCE* ist das zuvor beschriebene Instanzhandle.</span><span class="sxs-lookup"><span data-stu-id="07645-150">*hInstance* is the instance handle, described previously.</span></span> <span data-ttu-id="07645-151">(Weitere Informationen finden Sie [unter WinMain: der Einstiegspunkt der Anwendung](winmain--the-application-entry-point.md).)</span><span class="sxs-lookup"><span data-stu-id="07645-151">(See [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).)</span></span>
- <span data-ttu-id="07645-152">Der letzte Parameter ist ein Zeiger auf beliebige Daten vom Typ **" \* void**".</span><span class="sxs-lookup"><span data-stu-id="07645-152">The last parameter is a pointer to arbitrary data of type **void\***.</span></span> <span data-ttu-id="07645-153">Sie können diesen Wert verwenden, um eine Datenstruktur an die Fenster Prozedur zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="07645-153">You can use this value to pass a data structure to your window procedure.</span></span> <span data-ttu-id="07645-154">Wir zeigen eine mögliche Möglichkeit, diesen Parameter im Abschnitt [Verwalten des Anwendungs Zustands](managing-application-state-.md)zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="07645-154">We'll show one possible way to use this parameter in the section [Managing Application State](managing-application-state-.md).</span></span>

<span data-ttu-id="07645-155">" [**Kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " gibt ein Handle für das neue Fenster zurück, oder 0 (null), wenn die Funktion fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="07645-155">[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) returns a handle to the new window, or zero if the function fails.</span></span> <span data-ttu-id="07645-156">Um das Fenster anzuzeigen – d. h., das Fenster sichtbar zu machen – übergeben Sie das Fenster Handle an die [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) -Funktion:</span><span class="sxs-lookup"><span data-stu-id="07645-156">To show the window—that is, make the window visible —pass the window handle to the [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) function:</span></span>

```C++
ShowWindow(hwnd, nCmdShow);
```

<span data-ttu-id="07645-157">Der *HWND* -Parameter ist das von " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" zurückgegebene Fenster handle.</span><span class="sxs-lookup"><span data-stu-id="07645-157">The *hwnd* parameter is the window handle returned by [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="07645-158">Der *nCmdShow* -Parameter kann verwendet werden, um ein Fenster zu minimieren oder zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="07645-158">The *nCmdShow* parameter can be used to minimize or maximize a window.</span></span> <span data-ttu-id="07645-159">Das Betriebssystem übergibt diesen Wert über die **wWinMain** -Funktion an das Programm.</span><span class="sxs-lookup"><span data-stu-id="07645-159">The operating system passes this value to the program through the **wWinMain** function.</span></span>

<span data-ttu-id="07645-160">Hier sehen Sie den gesamten Code zum Erstellen des Fensters.</span><span class="sxs-lookup"><span data-stu-id="07645-160">Here is the complete code to create the window.</span></span> <span data-ttu-id="07645-161">Beachten Sie, dass `WindowProc` noch immer nur eine vorwärts Deklaration einer Funktion ist.</span><span class="sxs-lookup"><span data-stu-id="07645-161">Remember that `WindowProc` is still just a forward declaration of a function.</span></span>

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

<span data-ttu-id="07645-162">Herzlichen Glückwunsch, Sie haben ein Fenster erstellt!</span><span class="sxs-lookup"><span data-stu-id="07645-162">Congratulations, you've created a window!</span></span> <span data-ttu-id="07645-163">Momentan enthält das Fenster keinen Inhalt oder interagiert mit dem Benutzer.</span><span class="sxs-lookup"><span data-stu-id="07645-163">Right now, the window does not contain any content or interact with the user.</span></span> <span data-ttu-id="07645-164">In einer echten GUI-Anwendung antwortet das Fenster auf Ereignisse vom Benutzer und dem Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="07645-164">In a real GUI application, the window would respond to events from the user and the operating system.</span></span> <span data-ttu-id="07645-165">Im nächsten Abschnitt wird beschrieben, wie Fenster Meldungen diese Art von Interaktivität bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="07645-165">The next section describes how window messages provide this sort of interactivity.</span></span>

### <a name="next"></a><span data-ttu-id="07645-166">Nächste</span><span class="sxs-lookup"><span data-stu-id="07645-166">Next</span></span>

[<span data-ttu-id="07645-167">Fenster Meldungen</span><span class="sxs-lookup"><span data-stu-id="07645-167">Window Messages</span></span>](window-messages.md)