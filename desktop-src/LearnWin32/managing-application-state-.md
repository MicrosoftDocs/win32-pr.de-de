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
# <a name="managing-application-state"></a>Managing Application State (Verwalten eines Anwendungszustands)

Eine Fenster Prozedur ist nur eine Funktion, die für jede Nachricht aufgerufen wird, sodass Sie grundsätzlich zustandslos ist. Daher benötigen Sie eine Möglichkeit, den Status der Anwendung von einem Funktions Aufrufder nächsten zu verfolgen.

Der einfachste Ansatz besteht darin, alles in globalen Variablen zu platzieren. Dies funktioniert gut für kleine Programme, und viele der SDK-Beispiele verwenden diesen Ansatz. In einem großen Programm führt dies jedoch zu einer Zunahme von globalen Variablen. Außerdem verfügen Sie möglicherweise über mehrere Fenster, die jeweils über eine eigene Fenster Prozedur verfügen. Es wird nachverfolgt, welches Fenster auf welche Variablen verwirrend und fehleranfällig wird.

Die Funktion "up- [**windowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " bietet eine Möglichkeit, eine beliebige Datenstruktur an ein Fenster zu übergeben. Wenn diese Funktion aufgerufen wird, sendet Sie die folgenden zwei Nachrichten an die Fenster Prozedur:

- [**WM- \_ nccreate**](/windows/desktop/winmsg/wm-nccreate)
- [**WM \_ Erstellen**](/windows/desktop/winmsg/wm-create)

Diese Nachrichten werden in der aufgeführten Reihenfolge gesendet. (Hierbei handelt es sich nicht um die beiden nach [**richten, die**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)während der Funktion "" von "" in "" von "" von "" in "" von ""

Die Meldung " [**WM \_ nccreate**](/windows/desktop/winmsg/wm-nccreate) " und " [**WM \_ Create**](/windows/desktop/winmsg/wm-create) " werden gesendet, bevor das Fenster sichtbar wird. Dadurch sind Sie ein guter Ausgangspunkt, um die Benutzeroberfläche zu initialisieren – beispielsweise, um das anfängliche Layout des Fensters zu bestimmen.

Der letzte Parameter von " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " ist ein Zeiger vom Typ " **void \***". Sie können jeden gewünschten Zeiger Wert in diesem Parameter übergeben. Wenn die Fenster Prozedur die " [**WM \_ nccreate**](/windows/desktop/winmsg/wm-nccreate) "-oder " [**WM \_ Create**](/windows/desktop/winmsg/wm-create) "-Meldung verarbeitet, kann Sie diesen Wert aus den Nachrichten Daten extrahieren.

Sehen wir uns nun an, wie Sie diesen Parameter verwenden, um Anwendungsdaten an Ihr Fenster zu übergeben. Definieren Sie zunächst eine Klasse oder Struktur, die Zustandsinformationen enthält.

```C++
// Define a structure to hold some state information.

struct StateInfo {
    // ... (struct members not shown)
};
```

Wenn Sie " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" aufrufen, übergeben Sie einen Zeiger auf diese-Struktur im endgültigen **void \*** -Parameter.

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

Wenn Sie die Nachrichten " [**WM \_ nccreate**](/windows/desktop/winmsg/wm-nccreate) " und " [**WM \_ Create**](/windows/desktop/winmsg/wm-create) " erhalten, ist der *LPARAM* -Parameter jeder [**Nachricht ein Zeiger auf eine Struktur vom**](/windows/win32/api/winuser/ns-winuser-createstructa) Typ "Struktur". Die Struktur " **foratestruct** " wiederum enthält den Zeiger, den Sie an " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" übergeben haben.

![Diagramm, das das Layout der Struktur "Struktur erstellen" anzeigt](images/appstate01.png)

Im folgenden wird erläutert, wie Sie den Zeiger auf die Datenstruktur extrahieren. Holen Sie zuerst die Struktur " [**foratestruct**](/windows/win32/api/winuser/ns-winuser-createstructa) " durch Umwandeln des *LPARAM* -Parameters.

```C++
CREATESTRUCT *pCreate = reinterpret_cast<CREATESTRUCT*>(lParam);
```

Der Member **lpkreateparameams** der Struktur " [**kreatestruct**](/windows/win32/api/winuser/ns-winuser-createstructa) " ist der ursprüngliche void-Zeiger, den Sie in " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" angegeben haben. Sie erhalten einen Zeiger auf Ihre eigene Datenstruktur durch Umwandeln von **lpkreateparametriams**.

```C++
pState = reinterpret_cast<StateInfo*>(pCreate->lpCreateParams);
```

Aufrufen Sie als nächstes die Funktion [**setwindowlongptr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) , und übergeben Sie den Zeiger auf die Datenstruktur.

```C++
SetWindowLongPtr(hwnd, GWLP_USERDATA, (LONG_PTR)pState);
```

Der Zweck dieses letzten Funktions Aufrufes ist, den *StatusInfo* -Zeiger in den Instanzdaten für das Fenster zu speichern. Nachdem Sie dies getan haben, können Sie den Zeiger immer wieder aus dem Fenster abrufen, indem Sie [**getwindowlongptr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra)aufrufen:

```C++
LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
```

Jedes Fenster verfügt über eigene Instanzdaten, sodass Sie mehrere Fenster erstellen und jedem Fenster eine eigene Instanz der Datenstruktur zuordnen können. Diese Vorgehensweise ist besonders nützlich, wenn Sie eine Klasse von Fenstern definieren und mehr als ein Fenster dieser Klasse erstellen, z. –. Wenn Sie eine benutzerdefinierte Steuerelement Klasse erstellen. Es ist praktisch, den [**getwindowlongptr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) -aufrufin eine kleine Hilfsfunktion einzubinden.

```C++
inline StateInfo* GetAppState(HWND hwnd)
{
    LONG_PTR ptr = GetWindowLongPtr(hwnd, GWLP_USERDATA);
    StateInfo *pState = reinterpret_cast<StateInfo*>(ptr);
    return pState;
}
```

Nun können Sie die Fenster Prozedur wie folgt schreiben.

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

## <a name="an-object-oriented-approach"></a>Ein Object-Oriented Ansatz

Dieser Ansatz kann weiter erweitert werden. Wir haben bereits eine Datenstruktur zum Speichern von Zustandsinformationen über das Fenster definiert. Es ist sinnvoll, diese Datenstruktur mit Element Funktionen (Methoden) bereitzustellen, die mit den Daten arbeiten. Dies führt natürlich zu einem Entwurf, bei dem die Struktur (oder Klasse) für alle Vorgänge im Fenster verantwortlich ist. Die Fenster Prozedur würde dann Teil der Klasse werden.

Das heißt, wir möchten Folgendes tun:

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

Das einzige Problem besteht darin, wie die- `MyWindow::WindowProc` Methode eingebunden wird. Die [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) -Funktion erwartet, dass die Fenster Prozedur ein Funktionszeiger ist. Sie können in diesem Kontext keinen Zeiger an eine (nicht statische) Member-Funktion übergeben. Sie können jedoch einen Zeiger an eine *statische* Member-Funktion übergeben und dann an die Member-Funktion delegieren. Im folgenden finden Sie eine Klassen Vorlage, die diese Vorgehensweise veranschaulicht:

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

Bei der- `BaseWindow` Klasse handelt es sich um eine abstrakte Basisklasse, von der bestimmte Fenster Klassen abgeleitet werden. Hier ist z. b. die Deklaration einer einfachen, von abgeleiteten Klasse `BaseWindow` :

```C++
class MainWindow : public BaseWindow<MainWindow>
{
public:
    PCWSTR  ClassName() const { return L"Sample Window Class"; }
    LRESULT HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam);
};
```

Rufen Sie zum Erstellen des Fensters Folgendes auf `BaseWindow::Create` :

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

Die pure-Virtual- `BaseWindow::HandleMessage` Methode wird verwendet, um die Fenster Prozedur zu implementieren. Beispielsweise entspricht die folgende Implementierung der Fenster Prozedur, die am Anfang von [Modul 1](your-first-windows-program.md)angezeigt wird.

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

Beachten Sie, dass das Fenster Handle in einer Element Variablen (*m \_ HWND*) gespeichert ist, daher muss es nicht als Parameter an übergeben werden `HandleMessage` .

Viele der vorhandenen Windows-Programmier Frameworks, wie z. b. Microsoft Foundation Classes (MFC) und Active Template Library (ATL), verwenden Ansätze, die im Grunde der hier gezeigten ähneln. Natürlich ist ein vollständig generalisiertes Framework, wie z. b. MFC, komplexer als dieses relativ vereinfachte Beispiel.

## <a name="next"></a>Nächste

[Modul 2: Verwenden von com in Ihrem Windows-Programm](module-2--using-com-in-your-windows-program.md)

## <a name="related-topics"></a>Zugehörige Themen

[Basewindow-Beispiel](basewindow-sample.md)