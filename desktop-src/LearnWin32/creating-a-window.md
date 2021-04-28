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
# <a name="creating-a-window"></a>Erstellen eines Fensters

## <a name="window-classes"></a>Fensterklassen

Eine *Fensterklasse* definiert eine Reihe von Verhaltensweisen, die mehrere Fenster gemeinsam haben können. Beispielsweise weist jede Schaltfläche in einer Gruppe von Schaltflächen ein ähnliches Verhalten auf, wenn der Benutzer auf die Schaltfläche klickt. Natürlich sind Schaltflächen nicht vollständig identisch. Jede Schaltfläche zeigt eine eigene Textzeichenfolge an und verfügt über eigene Bildschirmkoordinaten. Daten, die für jedes Fenster eindeutig sind, werden als *Instanzdaten* bezeichnet.

Jedes Fenster muss einer Fensterklasse zugeordnet werden, auch wenn das Programm nur eine Instanz dieser Klasse erstellt. Es ist wichtig zu verstehen, dass eine Fensterklasse im C++-Sinn keine "Klasse" ist. Stattdessen handelt es sich um eine Datenstruktur, die intern vom Betriebssystem verwendet wird. Fensterklassen werden zur Laufzeit beim System registriert. Um eine neue Fensterklasse zu registrieren, füllen Sie zunächst eine [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) aus:

```C++
// Register the window class.
const wchar_t CLASS_NAME[]  = L"Sample Window Class";

WNDCLASS wc = { };

wc.lpfnWndProc   = WindowProc;
wc.hInstance     = hInstance;
wc.lpszClassName = CLASS_NAME;
```

Sie müssen die folgenden Strukturmember festlegen:

- **lpfnWndProc** ist ein Zeiger auf eine anwendungsdefinierte Funktion, die als *Fensterprozedur* oder "Fensterprozedur" bezeichnet wird. Die Fensterprozedur definiert den Großteil des Verhaltens des Fensters. Wir untersuchen die Fensterprozedur später im Detail. Behandeln Sie dies vorerst nur als Vorwärtsverweis.
- **hInstance** ist das Handle für die Anwendungsinstanz. Abrufen dieses Werts aus dem *hInstance-Parameter* von **wWinMain**.
- **lpszClassName** ist eine Zeichenfolge, die die Fensterklasse identifiziert.

Klassennamen sind lokal für den aktuellen Prozess, sodass der Name nur innerhalb des Prozesses eindeutig sein muss. Die Windows-Standardsteuerelemente verfügen jedoch auch über Klassen. Wenn Sie eines dieser Steuerelemente verwenden, müssen Sie Klassennamen auswählen, die keinen Konflikt mit den Steuerelementklassennamen verursachen. Die Fensterklasse für das Schaltflächensteuerelement heißt z. B. "Button".

Die [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) verfügt über andere Member, die hier nicht angezeigt werden. Sie können wie in diesem Beispiel gezeigt auf 0 (null) festlegen oder sie ausfüllen. In der MSDN-Dokumentation wird die Struktur ausführlich beschrieben.

Übergeben Sie als Nächstes die Adresse der [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) an die [**RegisterClass-Funktion.**](/windows/desktop/api/winuser/nf-winuser-registerclassa) Diese Funktion registriert die Fensterklasse beim Betriebssystem.

```C++
RegisterClass(&wc);
```

## <a name="creating-the-window"></a>Erstellen des Fensters

Um eine neue Instanz eines Fensters zu erstellen, rufen Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) auf:

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

Ausführliche Parameterbeschreibungen finden Sie auf MSDN, aber hier finden Sie eine kurze Zusammenfassung:

- Mit dem ersten Parameter können Sie einige optionale Verhaltensweisen für das Fenster angeben (z. B. transparente Fenster). Legen Sie diesen Parameter für die Standardverhalten auf 0 (null) fest.
- `CLASS_NAME` ist der Name der Fensterklasse. Dadurch wird der Typ des Fensters definiert, das Sie erstellen.
- Der Fenstertext wird von verschiedenen Fenstertypen auf unterschiedliche Weise verwendet. Wenn das Fenster über eine Titelleiste verfügt, wird der Text in der Titelleiste angezeigt.
- Der Fensterstil ist ein Satz von Flags, die einen Teil des Aussehens und Aussehens eines Fensters definieren. Die Konstante **WS \_ OVERLAPPEDWINDOW** besteht eigentlich aus mehreren Flags, die mit einem bitweisen **OR** kombiniert werden. Zusammen geben diese Flags dem Fenster eine Titelleiste, einen Rahmen, ein Systemmenü und die Schaltflächen **Minimieren** und **Maximieren.** Dieser Satz von Flags ist der gängigste Stil für ein Anwendungsfenster der obersten Ebene.
- Für Position und Größe bedeutet die konstante **CW \_ USEDEFAULT** die Verwendung von Standardwerten.
- Der nächste Parameter legt ein übergeordnetes Fenster oder Besitzerfenster für das neue Fenster fest. Legen Sie das übergeordnete Element fest, wenn Sie ein untergeordnetes Fenster erstellen. Legen Sie für ein Fenster der obersten Ebene diese auf **NULL** fest.
- Für ein Anwendungsfenster definiert der nächste Parameter das Menü für das Fenster. In diesem Beispiel wird kein Menü verwendet, sodass der Wert **NULL** ist.
- *hInstance* ist das zuvor beschriebene Instanzhandle. (Siehe [WinMain: Der Anwendungseinstiegspunkt.)](winmain--the-application-entry-point.md)
- Der letzte Parameter ist ein Zeiger auf beliebige Daten vom Typ **void \***. Sie können diesen Wert verwenden, um eine Datenstruktur an Ihre Fensterprozedur zu übergeben. Im Abschnitt Verwalten des [Anwendungszustands](managing-application-state-.md)wird eine mögliche Möglichkeit zur Verwendung dieses Parameters gezeigt.

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) gibt ein Handle für das neue Fenster oder 0 (null) zurück, wenn die Funktion fehlschlägt. Übergeben Sie das Fensterhandle an die [**ShowWindow-Funktion,**](/windows/desktop/api/winuser/nf-winuser-showwindow) um das Fenster anzuzeigen, d. b. das Fenster sichtbar zu machen:

```C++
ShowWindow(hwnd, nCmdShow);
```

Der *hwnd-Parameter* ist das Fensterhandle, das von [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)zurückgegeben wird. Der *nCmdShow-Parameter* kann verwendet werden, um ein Fenster zu minimieren oder zu maximieren. Das Betriebssystem übergibt diesen Wert über die **wWinMain-Funktion** an das Programm.

Hier ist der vollständige Code zum Erstellen des Fensters. Denken Sie daran, dass `WindowProc` immer noch nur eine Vorwärtsdeklaration einer Funktion ist.

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

Herzlichen Glückwunsch, Sie haben ein Fenster erstellt! Derzeit enthält das Fenster keine Inhalte und interagiert nicht mit dem Benutzer. In einer echten GUI-Anwendung würde das Fenster auf Ereignisse des Benutzers und des Betriebssystems reagieren. Im nächsten Abschnitt wird beschrieben, wie Fenstermeldungen diese Art von Interaktivität bereitstellen.

### <a name="next"></a>Nächste

[Fenstermeldungen](window-messages.md)
