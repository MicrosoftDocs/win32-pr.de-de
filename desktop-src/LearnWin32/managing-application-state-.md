---
title: Managing Application State (Verwalten eines Anwendungszustands)
description: Eine Fenster Prozedur ist nur eine Funktion, die für jede Nachricht aufgerufen wird, sodass Sie grundsätzlich zustandslos ist. Daher benötigen Sie eine Möglichkeit, den Status der Anwendung von einem Funktions Aufrufder nächsten zu verfolgen.
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e275833c30c612b5b40ab29d089d07ed7794b429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038965"
---
# <a name="managing-application-state"></a><span data-ttu-id="5967f-104">Managing Application State (Verwalten eines Anwendungszustands)</span><span class="sxs-lookup"><span data-stu-id="5967f-104">Managing Application State</span></span>

<span data-ttu-id="5967f-105">Eine Fenster Prozedur ist nur eine Funktion, die für jede Nachricht aufgerufen wird, sodass Sie grundsätzlich zustandslos ist.</span><span class="sxs-lookup"><span data-stu-id="5967f-105">A window procedure is just a function that gets invoked for every message, so it is inherently stateless.</span></span> <span data-ttu-id="5967f-106">Daher benötigen Sie eine Möglichkeit, den Status der Anwendung von einem Funktions Aufrufder nächsten zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="5967f-106">Therefore, you need a way to track the state of your application from one function call to the next.</span></span>

<span data-ttu-id="5967f-107">Der einfachste Ansatz besteht darin, alles in globalen Variablen zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="5967f-107">The simplest approach is simply to put everything in global variables.</span></span> <span data-ttu-id="5967f-108">Dies funktioniert gut für kleine Programme, und viele der SDK-Beispiele verwenden diesen Ansatz.</span><span class="sxs-lookup"><span data-stu-id="5967f-108">This works well enough for small programs, and many of the SDK samples use this approach.</span></span> <span data-ttu-id="5967f-109">In einem großen Programm führt dies jedoch zu einer Zunahme von globalen Variablen.</span><span class="sxs-lookup"><span data-stu-id="5967f-109">In a large program, however, it leads to a proliferation of global variables.</span></span> <span data-ttu-id="5967f-110">Außerdem verfügen Sie möglicherweise über mehrere Fenster, die jeweils über eine eigene Fenster Prozedur verfügen.</span><span class="sxs-lookup"><span data-stu-id="5967f-110">Also, you might have several windows, each with its own window procedure.</span></span> <span data-ttu-id="5967f-111">Es wird nachverfolgt, welches Fenster auf welche Variablen verwirrend und fehleranfällig wird.</span><span class="sxs-lookup"><span data-stu-id="5967f-111">Keeping track of which window should access which variables becomes confusing and error-prone.</span></span>

<span data-ttu-id="5967f-112">Die Funktion "up- [**windowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " bietet eine Möglichkeit, eine beliebige Datenstruktur an ein Fenster zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="5967f-112">The [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function provides a way to pass any data structure to a window.</span></span> <span data-ttu-id="5967f-113">Wenn diese Funktion aufgerufen wird, sendet Sie die folgenden zwei Nachrichten an die Fenster Prozedur:</span><span class="sxs-lookup"><span data-stu-id="5967f-113">When this function is called, it sends the following two messages to your window procedure:</span></span>

- [<span data-ttu-id="5967f-114">**WM- \_ nccreate**</span><span class="sxs-lookup"><span data-stu-id="5967f-114">**WM\_NCCREATE**</span></span>](/windows/desktop/winmsg/wm-nccreate)
- [<span data-ttu-id="5967f-115">**WM \_ Erstellen**</span><span class="sxs-lookup"><span data-stu-id="5967f-115">**WM\_CREATE**</span></span>](/windows/desktop/winmsg/wm-create)

<span data-ttu-id="5967f-116">Diese Nachrichten werden in der aufgeführten Reihenfolge gesendet.</span><span class="sxs-lookup"><span data-stu-id="5967f-116">These messages are sent in the order listed.</span></span> <span data-ttu-id="5967f-117">(Hierbei handelt es sich nicht um die beiden nach [**richten, die**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)während der Funktion "" von "" in "" von "" von "" in "" von ""</span><span class="sxs-lookup"><span data-stu-id="5967f-117">(These are not the only two messages sent during [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), but we can ignore the others for this discussion.)</span></span>

<span data-ttu-id="5967f-118">Die Meldung " [**WM \_ nccreate**](/windows/desktop/winmsg/wm-nccreate) " und " [**WM \_ Create**](/windows/desktop/winmsg/wm-create) " werden gesendet, bevor das Fenster sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="5967f-118">The [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) and [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message are sent before the window becomes visible.</span></span> <span data-ttu-id="5967f-119">Dadurch sind Sie ein guter Ausgangspunkt, um die Benutzeroberfläche zu initialisieren – beispielsweise, um das anfängliche Layout des Fensters zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="5967f-119">That makes them a good place to initialize your UI—for example, to determine the initial layout of the window.</span></span>

<span data-ttu-id="5967f-120">Der letzte Parameter von " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " ist ein Zeiger vom Typ " **void \***".</span><span class="sxs-lookup"><span data-stu-id="5967f-120">The last parameter of [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) is a pointer of type **void\***.</span></span> <span data-ttu-id="5967f-121">Sie können jeden gewünschten Zeiger Wert in diesem Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="5967f-121">You can pass any pointer value that you want in this parameter.</span></span> <span data-ttu-id="5967f-122">Wenn die Fenster Prozedur die " [**WM \_ nccreate**](/windows/desktop/winmsg/wm-nccreate) "-oder " [**WM \_ Create**](/windows/desktop/winmsg/wm-create) "-Meldung verarbeitet, kann Sie diesen Wert aus den Nachrichten Daten extrahieren.</span><span class="sxs-lookup"><span data-stu-id="5967f-122">When the window procedure handles the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) or [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, it can extract this value from the message data.</span></span>

<span data-ttu-id="5967f-123">Sehen wir uns nun an, wie Sie diesen Parameter verwenden, um Anwendungsdaten an Ihr Fenster zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="5967f-123">Let's see how you would use this parameter to pass application data to your window.</span></span> <span data-ttu-id="5967f-124">Definieren Sie zunächst eine Klasse oder Struktur, die Zustandsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="5967f-124">First, define a class or structure that holds state information.</span></span>

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

<span data-ttu-id="5967f-125">Wenn Sie " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" aufrufen, übergeben Sie einen Zeiger auf diese-Struktur im endgültigen **void \*** -Parameter.</span><span class="sxs-lookup"><span data-stu-id="5967f-125">When you call [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), pass a pointer to this structure in the final **void\*** parameter.</span></span>

```C++
StateInfo *pState = new (std::nothrow) StateInfo;

if (pState == NULL)
{
    return 0;
}

// Initialize the structure members (not shown).

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
    pState      // Additional application data
    );
```

<span data-ttu-id="5967f-126">Wenn Sie die Nachrichten " [**WM \_ nccreate**](/windows/desktop/winmsg/wm-nccreate) " und " [**WM \_ Create**](/windows/desktop/winmsg/wm-create) " erhalten, ist der *LPARAM* -Parameter jeder [**Nachricht ein Zeiger auf eine Struktur vom**](/windows/win32/api/winuser/ns-winuser-createstructa) Typ "Struktur".</span><span class="sxs-lookup"><span data-stu-id="5967f-126">When you receive the [**WM\_NCCREATE**](/windows/desktop/winmsg/wm-nccreate) and [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) messages, the *lParam* parameter of each message is a pointer to a [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure.</span></span> <span data-ttu-id="5967f-127">Die Struktur " **foratestruct** " wiederum enthält den Zeiger, den Sie an " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="5967f-127">The **CREATESTRUCT** structure, in turn, contains the pointer that you passed into [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>

![Diagramm, das das Layout der Struktur "Struktur erstellen" anzeigt](images/appstate01.png)

<span data-ttu-id="5967f-129">Im folgenden wird erläutert, wie Sie den Zeiger auf die Datenstruktur extrahieren.</span><span class="sxs-lookup"><span data-stu-id="5967f-129">Here is how you extract the pointer to your data structure.</span></span> <span data-ttu-id="5967f-130">Holen Sie zuerst die Struktur " [**foratestruct**](/windows/win32/api/winuser/ns-winuser-createstructa) " durch Umwandeln des *LPARAM* -Parameters.</span><span class="sxs-lookup"><span data-stu-id="5967f-130">First, get the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure by casting the *lParam* parameter.</span></span>

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

<span data-ttu-id="5967f-131">Der Member **lpkreateparameams** der Struktur " [**kreatestruct**](/windows/win32/api/winuser/ns-winuser-createstructa) " ist der ursprüngliche void-Zeiger, den Sie in " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="5967f-131">The **lpCreateParams** member of the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure is the original void pointer that you specified in [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span> <span data-ttu-id="5967f-132">Sie erhalten einen Zeiger auf Ihre eigene Datenstruktur durch Umwandeln von **lpkreateparametriams**.</span><span class="sxs-lookup"><span data-stu-id="5967f-132">Get a pointer to your own data structure by casting **lpCreateParams**.</span></span>

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

<span data-ttu-id="5967f-133">Aufrufen Sie als nächstes die Funktion [**setwindowlongptr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) , und übergeben Sie den Zeiger auf die Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="5967f-133">Next, call the [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) function and pass in the pointer to your data structure.</span></span>

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

<span data-ttu-id="5967f-134">Der Zweck dieses letzten Funktions Aufrufes ist, den *StatusInfo* -Zeiger in den Instanzdaten für das Fenster zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5967f-134">The purpose of this last function call is to store the *StateInfo* pointer in the instance data for the window.</span></span> <span data-ttu-id="5967f-135">Nachdem Sie dies getan haben, können Sie den Zeiger immer wieder aus dem Fenster abrufen, indem Sie [**getwindowlongptr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra)aufrufen:</span><span class="sxs-lookup"><span data-stu-id="5967f-135">Once you do this, you can always get the pointer back from the window by calling [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra):</span></span>

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

<span data-ttu-id="5967f-136">Jedes Fenster verfügt über eigene Instanzdaten, sodass Sie mehrere Fenster erstellen und jedem Fenster eine eigene Instanz der Datenstruktur zuordnen können.</span><span class="sxs-lookup"><span data-stu-id="5967f-136">Each window has its own instance data, so you can create multiple windows and give each window its own instance of the data structure.</span></span> <span data-ttu-id="5967f-137">Diese Vorgehensweise ist besonders nützlich, wenn Sie eine Klasse von Fenstern definieren und mehr als ein Fenster dieser Klasse erstellen, z. –. Wenn Sie eine benutzerdefinierte Steuerelement Klasse erstellen.</span><span class="sxs-lookup"><span data-stu-id="5967f-137">This approach is especially useful if you define a class of windows and create more than one window of that class—for example, if you create a custom control class.</span></span> <span data-ttu-id="5967f-138">Es ist praktisch, den [**getwindowlongptr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) -aufrufin eine kleine Hilfsfunktion einzubinden.</span><span class="sxs-lookup"><span data-stu-id="5967f-138">It is convenient to wrap the [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) call in a small helper function.</span></span>

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

<span data-ttu-id="5967f-139">Nun können Sie die Fenster Prozedur wie folgt schreiben.</span><span class="sxs-lookup"><span data-stu-id="5967f-139">Now you can write your window procedure as follows.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;
    if (uMsg == WM_CREATE)
    {
        CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
        pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
        SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
    }
    else
    {
        pState = GetAppState(hwnd);
    }

    switch (uMsg)
    {


    // Remainder of the window procedure not shown ...

    }
    return TRUE;
}
```

## <a name="an-object-oriented-approach"></a><span data-ttu-id="5967f-140">Ein Object-Oriented Ansatz</span><span class="sxs-lookup"><span data-stu-id="5967f-140">An Object-Oriented Approach</span></span>

<span data-ttu-id="5967f-141">Dieser Ansatz kann weiter erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="5967f-141">We can extend this approach further.</span></span> <span data-ttu-id="5967f-142">Wir haben bereits eine Datenstruktur zum Speichern von Zustandsinformationen über das Fenster definiert.</span><span class="sxs-lookup"><span data-stu-id="5967f-142">We have already defined a data structure to hold state information about the window.</span></span> <span data-ttu-id="5967f-143">Es ist sinnvoll, diese Datenstruktur mit Element Funktionen (Methoden) bereitzustellen, die mit den Daten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="5967f-143">It makes sense to provide this data structure with member functions (methods) that operate on the data.</span></span> <span data-ttu-id="5967f-144">Dies führt natürlich zu einem Entwurf, bei dem die Struktur (oder Klasse) für alle Vorgänge im Fenster verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="5967f-144">This naturally leads to a design where the structure (or class) is responsible for all of the operations on the window.</span></span> <span data-ttu-id="5967f-145">Die Fenster Prozedur würde dann Teil der Klasse werden.</span><span class="sxs-lookup"><span data-stu-id="5967f-145">The window procedure would then become part of the class.</span></span>

<span data-ttu-id="5967f-146">Das heißt, wir möchten Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="5967f-146">In other words, we would like to go from this:</span></span>

```C++
// pseudocode

LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    StateInfo *pState;

    /* Get pState from the HWND. */

    switch (uMsg)
    {
        case WM_SIZE:
            HandleResize(pState, ...);
            break;

        case WM_PAINT:
            HandlePaint(pState, ...);
            break;

       // And so forth.
    }
}
```

<span data-ttu-id="5967f-147">Folgendermaßen:</span><span class="sxs-lookup"><span data-stu-id="5967f-147">To this:</span></span>

```C++
// pseudocode

LRESULT MyWindow::WindowProc(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_SIZE:
            this->HandleResize(...);
            break;

        case WM_PAINT:
            this->HandlePaint(...);
            break;
    }
}
```

<span data-ttu-id="5967f-148">Das einzige Problem besteht darin, wie die- `MyWindow::WindowProc` Methode eingebunden wird.</span><span class="sxs-lookup"><span data-stu-id="5967f-148">The only problem is how to hook up the `MyWindow::WindowProc` method.</span></span> <span data-ttu-id="5967f-149">Die [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) -Funktion erwartet, dass die Fenster Prozedur ein Funktionszeiger ist.</span><span class="sxs-lookup"><span data-stu-id="5967f-149">The [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) function expects the window procedure to be a function pointer.</span></span> <span data-ttu-id="5967f-150">Sie können in diesem Kontext keinen Zeiger an eine (nicht statische) Member-Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="5967f-150">You can't pass a pointer to a (non-static) member function in this context.</span></span> <span data-ttu-id="5967f-151">Sie können jedoch einen Zeiger an eine *statische* Member-Funktion übergeben und dann an die Member-Funktion delegieren.</span><span class="sxs-lookup"><span data-stu-id="5967f-151">However, you can pass a pointer to a *static* member function and then delegate to the member function.</span></span> <span data-ttu-id="5967f-152">Im folgenden finden Sie eine Klassen Vorlage, die diese Vorgehensweise veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="5967f-152">Here is a class template that shows this approach:</span></span>

```C++
template <class DERIVED_TYPE> 
class BaseWindow
{
public:
    static LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
    {
        DERIVED_TYPE *pThis = NULL;

        if (uMsg == WM_NCCREATE)
        {
            CREATESTRUCT* pCreate = (CREATESTRUCT*)lParam;
            pThis = (DERIVED_TYPE*)pCreate->lpCreateParams;
            SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pThis);

            pThis->m_hwnd = hwnd;
        }
        else
        {
            pThis = (DERIVED_TYPE*)GetWindowLongPtr(hwnd, GWLP_USERDATA);
        }
        if (pThis)
        {
            return pThis->HandleMessage(uMsg, wParam, lParam);
        }
        else
        {
            return DefWindowProc(hwnd, uMsg, wParam, lParam);
        }
    }

    BaseWindow() : m_hwnd(NULL) { }

    BOOL Create(
        PCWSTR lpWindowName,
        DWORD dwStyle,
        DWORD dwExStyle = 0,
        int x = CW_USEDEFAULT,
        int y = CW_USEDEFAULT,
        int nWidth = CW_USEDEFAULT,
        int nHeight = CW_USEDEFAULT,
        HWND hWndParent = 0,
        HMENU hMenu = 0
        )
    {
        WNDCLASS wc = {0};

        wc.lpfnWndProc   = DERIVED_TYPE::WindowProc;
        wc.hInstance     = GetModuleHandle(NULL);
        wc.lpszClassName = ClassName();

        RegisterClass(&wc);

        m_hwnd = CreateWindowEx(
            dwExStyle, ClassName(), lpWindowName, dwStyle, x, y,
            nWidth, nHeight, hWndParent, hMenu, GetModuleHandle(NULL), this
            );

        return (m_hwnd ? TRUE : FALSE);
    }

    HWND Window() const { return m_hwnd; }

protected:

    virtual PCWSTR  ClassName() const = 0;
    virtual LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam) = 0;

    HWND m_hwnd;
};
```

<span data-ttu-id="5967f-153">Bei der- `BaseWindow` Klasse handelt es sich um eine abstrakte Basisklasse, von der bestimmte Fenster Klassen abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="5967f-153">The `BaseWindow` class is an abstract base class, from which specific window classes are derived.</span></span> <span data-ttu-id="5967f-154">Hier ist z. b. die Deklaration einer einfachen, von abgeleiteten Klasse `BaseWindow` :</span><span class="sxs-lookup"><span data-stu-id="5967f-154">For example, here is the declaration of a simple class derived from `BaseWindow`:</span></span>

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

<span data-ttu-id="5967f-155">Rufen Sie zum Erstellen des Fensters Folgendes auf `BaseWindow::Create` :</span><span class="sxs-lookup"><span data-stu-id="5967f-155">To create the window, call `BaseWindow::Create`:</span></span>

```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE, PWSTR pCmdLine, int nCmdShow)
{
    MainWindow win;

    if (!win.Create(L"Learn to Program Windows", WS_OVERLAPPEDWINDOW))
    {
        return 0;
    }

    ShowWindow(win.Window(), nCmdShow);

    // Run the message loop.

    MSG msg = { };
    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }

    return 0;
}
```

<span data-ttu-id="5967f-156">Die pure-Virtual- `BaseWindow::HandleMessage` Methode wird verwendet, um die Fenster Prozedur zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="5967f-156">The pure-virtual `BaseWindow::HandleMessage` method is used to implement the window procedure.</span></span> <span data-ttu-id="5967f-157">Beispielsweise entspricht die folgende Implementierung der Fenster Prozedur, die am Anfang von [Modul 1](your-first-windows-program.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5967f-157">For example, the following implementation is equivalent to the window procedure shown at the start of [Module 1](your-first-windows-program.md).</span></span>

```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_DESTROY:
        PostQuitMessage(0);
        return 0;

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            HDC hdc = BeginPaint(m_hwnd, &ps);
            FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
            EndPaint(m_hwnd, &ps);
        }
        return 0;

    default:
        return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
    }
    return TRUE;
}
```

<span data-ttu-id="5967f-158">Beachten Sie, dass das Fenster Handle in einer Element Variablen (*m \_ HWND*) gespeichert ist, daher muss es nicht als Parameter an übergeben werden `HandleMessage` .</span><span class="sxs-lookup"><span data-stu-id="5967f-158">Notice that the window handle is stored in a member variable (*m\_hwnd*), so we do not need to pass it as a parameter to `HandleMessage`.</span></span>

<span data-ttu-id="5967f-159">Viele der vorhandenen Windows-Programmier Frameworks, wie z. b. Microsoft Foundation Classes (MFC) und Active Template Library (ATL), verwenden Ansätze, die im Grunde der hier gezeigten ähneln.</span><span class="sxs-lookup"><span data-stu-id="5967f-159">Many of the existing Windows programming frameworks, such as Microsoft Foundation Classes (MFC) and Active Template Library (ATL), use approaches that are basically similar to the one shown here.</span></span> <span data-ttu-id="5967f-160">Natürlich ist ein vollständig generalisiertes Framework, wie z. b. MFC, komplexer als dieses relativ vereinfachte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="5967f-160">Of course, a fully generalized framework such as MFC is more complex than this relatively simplistic example.</span></span>

## <a name="next"></a><span data-ttu-id="5967f-161">Nächste</span><span class="sxs-lookup"><span data-stu-id="5967f-161">Next</span></span>

[<span data-ttu-id="5967f-162">Modul 2: Verwenden von com in Ihrem Windows-Programm</span><span class="sxs-lookup"><span data-stu-id="5967f-162">Module 2: Using COM in Your Windows Program</span></span>](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a><span data-ttu-id="5967f-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5967f-163">Related topics</span></span>

[<span data-ttu-id="5967f-164">Basewindow-Beispiel</span><span class="sxs-lookup"><span data-stu-id="5967f-164">BaseWindow Sample</span></span>](basewindow-sample.md)