---
title: Managing Application State (Verwalten eines Anwendungszustands)
description: Eine Fensterprozedur ist nur eine Funktion, die für jede Nachricht aufgerufen wird, sodass sie grundsätzlich zustandslos ist. Daher benötigen Sie eine Möglichkeit, den Zustand Ihrer Anwendung von einem Funktionsaufruf zum nächsten nachzuverfolgen.
ms.assetid: 2f03961e-a886-4947-8f5d-62543c6b8815
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b0cde27195ba0dfc16668da11beac243821902995a9d01daa337f8962944343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068064"
---
# <a name="managing-application-state"></a>Managing Application State (Verwalten eines Anwendungszustands)

Eine Fensterprozedur ist nur eine Funktion, die für jede Nachricht aufgerufen wird, sodass sie grundsätzlich zustandslos ist. Daher benötigen Sie eine Möglichkeit, den Zustand Ihrer Anwendung von einem Funktionsaufruf zum nächsten nachzuverfolgen.

Der einfachste Ansatz besteht darin, alles einfach in globale Variablen zu setzen. Dies funktioniert gut genug für kleine Programme, und viele der SDK-Beispiele verwenden diesen Ansatz. In einem großen Programm führt dies jedoch zu einer Verbreitung globaler Variablen. Außerdem verfügen Sie möglicherweise über mehrere Fenster, von denen jedes über eine eigene Fensterprozedur verfügt. Nachverfolgen, welches Fenster auf welche Variablen zugreifen soll, wird verwirrend und fehleranfällig.

Die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) bietet eine Möglichkeit, jede Datenstruktur an ein Fenster zu übergeben. Wenn diese Funktion aufgerufen wird, sendet sie die folgenden beiden Nachrichten an Ihre Fensterprozedur:

- [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)
- [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)

Diese Nachrichten werden in der aufgeführten Reihenfolge gesendet. (Dies sind nicht die einzigen beiden Nachrichten, die während [**von CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)gesendet werden, aber wir können die anderen für diese Diskussion ignorieren.)

Die [**WM \_ NCCREATE-**](/windows/desktop/winmsg/wm-nccreate) und [**WM \_ CREATE-Nachricht**](/windows/desktop/winmsg/wm-create) wird gesendet, bevor das Fenster sichtbar wird. Dies macht sie zu einem guten Ort zum Initialisieren Ihrer Benutzeroberfläche, z. B. zum Bestimmen des anfänglichen Layouts des Fensters.

Der letzte Parameter von [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ist ein Zeiger vom Typ **void \** _. Sie können einen beliebigen Zeigerwert in diesem Parameter übergeben. Wenn die Fensterprozedur die Meldung [_ *WM \_ NCCREATE* *](/windows/desktop/winmsg/wm-nccreate) oder [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) verarbeitet, kann sie diesen Wert aus den Nachrichtendaten extrahieren.

Sehen wir uns an, wie Sie diesen Parameter verwenden, um Anwendungsdaten an Ihr Fenster zu übergeben. Definieren Sie zunächst eine Klasse oder Struktur, die Zustandsinformationen enthält.

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

Wenn Sie [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)aufrufen, übergeben Sie einen Zeiger auf diese Struktur im letzten **\* void-Parameter.**

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

Wenn Sie die [**WM \_ NCCREATE-**](/windows/desktop/winmsg/wm-nccreate) und [**WM \_ CREATE-Nachrichten**](/windows/desktop/winmsg/wm-create) erhalten, ist der *lParam-Parameter* jeder Nachricht ein Zeiger auf eine [**CREATESTRUCT-Struktur.**](/windows/win32/api/winuser/ns-winuser-createstructa) Die **CREATESTRUCT-Struktur** enthält wiederum den Zeiger, den Sie an [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)übergeben haben.

![Diagramm, das das Layout der Struktur "create" zeigt](images/appstate01.png)

So extrahieren Sie den Zeiger auf Ihre Datenstruktur. Zunächst erhalten Sie die [**CREATESTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-createstructa) indem Sie den *lParam-Parameter* umwandeln.

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

Der **lpCreateParams-Member** der [**CREATESTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-createstructa) ist der ursprüngliche void-Zeiger, den Sie in [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)angegeben haben. Erhalten Sie einen Zeiger auf Ihre eigene Datenstruktur, indem Sie **lpCreateParams** umwandeln.

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

Rufen Sie als Nächstes die [**SetWindowLongPtr-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) auf, und übergeben Sie den Zeiger auf Ihre Datenstruktur.

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

Der Zweck dieses letzten Funktionsaufrufs besteht darin, den *StateInfo-Zeiger* in den Instanzdaten für das Fenster zu speichern. Sobald Sie dies tun, können Sie den Zeiger immer aus dem Fenster abrufen, indem [**Sie GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra)aufrufen:

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

Jedes Fenster verfügt über eigene Instanzdaten, sodass Sie mehrere Fenster erstellen und jedem Fenster eine eigene Instanz der Datenstruktur geben können. Dieser Ansatz ist besonders nützlich, wenn Sie eine Klasse von Fenstern definieren und mehr als ein Fenster dieser Klasse erstellen, z. B. wenn Sie eine benutzerdefinierte Steuerelementklasse erstellen. Es ist praktisch, den [**GetWindowLongPtr-Aufruf**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) in einer kleinen Hilfsfunktion zu umschließen.

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

Nun können Sie die Fensterprozedur wie folgt schreiben.

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

## <a name="an-object-oriented-approach"></a>Ein Object-Oriented-Ansatz

Wir können diesen Ansatz weiter ausweiten. Wir haben bereits eine Datenstruktur definiert, die Zustandsinformationen zum Fenster enthalten soll. Es ist sinnvoll, diese Datenstruktur mit Memberfunktionen (Methoden) bereitzustellen, die mit den Daten arbeiten. Dies führt natürlich zu einem Entwurf, bei dem die Struktur (oder Klasse) für alle Vorgänge im Fenster verantwortlich ist. Die Fensterprozedur würde dann Teil der -Klasse werden.

Das heißt, wir möchten von diesem Beispiel aus gehen:

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

Folgendermaßen:

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

Das einzige Problem besteht darin, die -Methode zu `MyWindow::WindowProc` verknüpfen. Die [**RegisterClass-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerclassa) erwartet, dass die Fensterprozedur ein Funktionszeiger ist. Sie können in diesem Kontext keinen Zeiger auf eine (nicht statische) Memberfunktion übergeben. Sie können jedoch einen Zeiger auf eine *statische* Memberfunktion übergeben und dann an die Memberfunktion delegieren. Im Folgenden finden Sie eine Klassenvorlage, die diesen Ansatz veranschaulicht:

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

Die `BaseWindow` -Klasse ist eine abstrakte Basisklasse, von der bestimmte Fensterklassen abgeleitet werden. Hier ist beispielsweise die Deklaration einer einfachen Klasse, die von abgeleitet `BaseWindow` wurde:

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

Rufen Sie auf, um das Fenster zu `BaseWindow::Create` erstellen:

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

Die rein virtuelle `BaseWindow::HandleMessage` Methode wird verwendet, um die Fensterprozedur zu implementieren. Die folgende Implementierung entspricht beispielsweise der Fensterprozedur, die am Anfang von [Modul 1](your-first-windows-program.md)gezeigt wird.

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

Beachten Sie, dass das Fensterhandle in einer Membervariablen *(m \_ hwnd)* gespeichert ist, sodass wir es nicht als Parameter an übergeben `HandleMessage` müssen.

Viele der vorhandenen Windows Programmierframeworks, z. B. Microsoft Foundation Classes (MFC) und Active Template Library (ATL), verwenden Ansätze, die im Grunde dem hier gezeigten ähneln. Natürlich ist ein vollständig generalisiertes Framework wie MFC komplexer als dieses relativ einfache Beispiel.

## <a name="next"></a>Nächste

[Modul 2: Verwenden von COM in Ihrem Windows-Programm](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a>Zugehörige Themen

[BaseWindow-Beispiel](basewindow-sample.md)