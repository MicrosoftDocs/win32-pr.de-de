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
# <a name="creating-a-window"></a>Erstellen eines Fensters

## <a name="window-classes"></a>Fensterklassen

Eine *Fenster Klasse* definiert eine Reihe von Verhaltensweisen, die mehrere Fenster gemeinsam haben können. Beispielsweise weist eine Schaltfläche in einer Gruppe von Schaltflächen ein ähnliches Verhalten auf, wenn der Benutzer auf die Schaltfläche klickt. Natürlich sind die Schaltflächen nicht vollständig identisch. jede Schaltfläche zeigt eine eigene Text Zeichenfolge an und verfügt über eigene Bildschirm Koordinaten. Daten, die für jedes Fenster eindeutig sind, werden als *Instanzdaten* bezeichnet.

Jedes Fenster muss einer Fenster Klasse zugeordnet werden, auch wenn das Programm immer nur eine Instanz dieser Klasse erstellt. Es ist wichtig zu verstehen, dass eine Fenster Klasse nicht "Class" in der C++ Sense ist. Vielmehr handelt es sich um eine Datenstruktur, die intern vom Betriebssystem verwendet wird. Fenster Klassen werden zur Laufzeit beim System registriert. Um eine neue Fenster Klasse zu registrieren, müssen Sie zunächst eine [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur ausfüllen:

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

Sie müssen die folgenden Strukturmember festlegen:

- **lpfnwndproc** ist ein Zeiger auf eine Anwendungs definierte Funktion, die als *Fenster Prozedur* oder "Fenster proc" bezeichnet wird. Die Fenster Prozedur definiert den größten Teil des Verhaltens des Fensters. Die Fenster Prozedur wird später ausführlich untersucht. Behandeln Sie dies vorerst als vorwärts Verweis.
- **HINSTANCE** ist das Handle für die Anwendungs Instanz. Diesen Wert erhalten Sie vom *HINSTANCE* -Parameter von **wWinMain**.
- **lpszClassName** ist eine Zeichenfolge, die die Fenster Klasse identifiziert.

Klassennamen sind für den aktuellen Prozess lokal, sodass der Name nur innerhalb des Prozesses eindeutig sein muss. Die standardmäßigen Windows-Steuerelemente verfügen jedoch auch über Klassen. Wenn Sie eines dieser Steuerelemente verwenden, müssen Sie Klassennamen auswählen, die nicht mit den Steuerelement Klassennamen in Konflikt stehen. Beispielsweise hat die Fenster Klasse für das Schaltflächen-Steuerelement den Namen "Button".

Die [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur enthält andere Member, die hier nicht angezeigt werden. Sie können Sie auf 0 (null) festlegen, wie im folgenden Beispiel gezeigt, oder Sie können Sie in ausfüllen. In der MSDN-Dokumentation wird die Struktur ausführlich beschrieben.

Übergeben Sie anschließend die Adresse der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur an die [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) -Funktion. Diese Funktion registriert die Fenster Klasse beim Betriebssystem.

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a>Erstellen des Fensters

Um eine neue Instanz eines Fensters zu erstellen, rufen Sie die Funktion "up- [**windowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " auf:

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

Sie können ausführliche Parameter Beschreibungen auf MSDN lesen, aber hier finden Sie eine kurze Zusammenfassung:

- Mit dem ersten Parameter können Sie einige optionale Verhalten für das Fenster angeben (z. b. transparente Fenster). Legen Sie diesen Parameter für das Standardverhalten auf NULL fest.
- `CLASS_NAME` der Name der Fenster Klasse. Hiermit wird der Typ des Fensters definiert, das Sie erstellen.
- Der Fenster Text wird von unterschiedlichen Windows-Typen auf unterschiedliche Weise verwendet. Wenn das Fenster über eine Titelleiste verfügt, wird der Text in der Titelleiste angezeigt.
- Der Fenster Stil ist ein Satz von Flags, die ein paar aus dem Aussehen und dem Gefühl eines Fensters definieren. Die Konstante **WS \_ overlappedwindow** ist tatsächlich mehrere Flags, die mit einem bitweisen **or** kombiniert werden. Diese Flags versehen das Fenster in einer Titelleiste, einem Rahmen, einem Systemmenü und den Schaltflächen **minimieren** und **Maxi** mieren. Diese Gruppe von Flags ist der gängigste Stil für ein Anwendungsfenster der obersten Ebene.
- Für Position und Größe bedeutet die Konstante **CW \_ usedefault** , dass Standardwerte verwendet werden.
- Mit dem nächsten Parameter wird ein übergeordnetes Fenster oder Besitzer Fenster für das neue Fenster festgelegt. Legen Sie das übergeordnete Fenster fest, wenn Sie ein untergeordnetes Fenster erstellen. Legen Sie für ein Fenster der obersten Ebene diesen Wert auf **null** fest.
- Bei einem Anwendungsfenster definiert der nächste Parameter das Menü für das Fenster. In diesem Beispiel wird kein Menü verwendet, daher ist der Wert **null**.
- *HINSTANCE* ist das zuvor beschriebene Instanzhandle. (Weitere Informationen finden Sie [unter WinMain: der Einstiegspunkt der Anwendung](winmain--the-application-entry-point.md).)
- Der letzte Parameter ist ein Zeiger auf beliebige Daten vom Typ **" \* void**". Sie können diesen Wert verwenden, um eine Datenstruktur an die Fenster Prozedur zu übergeben. Wir zeigen eine mögliche Möglichkeit, diesen Parameter im Abschnitt [Verwalten des Anwendungs Zustands](managing-application-state-.md)zu verwenden.

" [**Kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " gibt ein Handle für das neue Fenster zurück, oder 0 (null), wenn die Funktion fehlschlägt. Um das Fenster anzuzeigen – d. h., das Fenster sichtbar zu machen – übergeben Sie das Fenster Handle an die [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) -Funktion:

```C++
ShowWindow(hwnd, nCmdShow);
```

Der *HWND* -Parameter ist das von " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" zurückgegebene Fenster handle. Der *nCmdShow* -Parameter kann verwendet werden, um ein Fenster zu minimieren oder zu maximieren. Das Betriebssystem übergibt diesen Wert über die **wWinMain** -Funktion an das Programm.

Hier sehen Sie den gesamten Code zum Erstellen des Fensters. Beachten Sie, dass `WindowProc` noch immer nur eine vorwärts Deklaration einer Funktion ist.

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

Herzlichen Glückwunsch, Sie haben ein Fenster erstellt! Momentan enthält das Fenster keinen Inhalt oder interagiert mit dem Benutzer. In einer echten GUI-Anwendung antwortet das Fenster auf Ereignisse vom Benutzer und dem Betriebssystem. Im nächsten Abschnitt wird beschrieben, wie Fenster Meldungen diese Art von Interaktivität bereitstellen.

### <a name="next"></a>Nächste

[Fenster Meldungen](window-messages.md)