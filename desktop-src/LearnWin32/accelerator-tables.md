---
title: Zugriffstastentabellen
description: Zugriffstastentabellen
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504749b6fad794f5f587e035f0dbc81662aa8b5faaf9b9eb13de365dd9a8d312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146443"
---
# <a name="accelerator-tables"></a>Zugriffstastentabellen

Anwendungen definieren häufig Tastenkombinationen, z. B. STRG+O für den Befehl Datei öffnen. Sie können Tastenkombinationen implementieren, indem Sie einzelne [**WM \_ KEYDOWN-Nachrichten**](/windows/desktop/inputdev/wm-keydown) behandeln. Zugriffstastentabellen bieten jedoch eine bessere Lösung für:

-   Erfordert weniger Codierung.
-   Konsolidiert alle Tastenkombinationen in einer Datendatei.
-   Unterstützt die Lokalisierung in anderen Sprachen.
-   Aktiviert Verknüpfungen und Menübefehle, um dieselbe Anwendungslogik zu verwenden.

Eine *Zugriffstastentabelle* ist eine Datenressource, die Tastenkombinationen wie STRG+O Anwendungsbefehlen zu ordnet. Bevor wir sehen, wie sie eine Zugriffstastentabelle verwenden, benötigen wir eine kurze Einführung in Ressourcen. Eine *Ressource* ist ein Datenblob, das in eine Anwendungsbin binär (EXE oder DLL) integriert ist. Ressourcen speichern Daten, die von der Anwendung benötigt werden, z. B. Menüs, Cursor, Symbole, Bilder, Textzeichenfolgen oder benutzerdefinierte Anwendungsdaten. Die Anwendung lädt die Ressourcendaten zur Laufzeit aus der Binärdatei. Gehen Sie wie folgt vor, um Ressourcen in eine Binärdatei ein-/aus zu schließen:

1.  Erstellen Sie eine Ressourcendefinitionsdatei (RC). Diese Datei definiert die Ressourcentypen und deren Bezeichner. Die Ressourcendefinitionsdatei kann Verweise auf andere Dateien enthalten. Beispielsweise wird eine Symbolressource in der RC-Datei deklariert, aber das Symbolbild wird in einer separaten Datei gespeichert.
2.  Verwenden Sie den Microsoft Windows Resource Compiler (RC), um die Ressourcendefinitionsdatei in eine kompilierte Ressourcendatei (RES) zu kompilieren. Der RC-Compiler wird mit Visual Studio und dem Windows SDK bereitgestellt.
3.  Verknüpfen Sie die kompilierte Ressourcendatei mit der Binärdatei.

Diese Schritte entsprechen in etwa dem Kompilierungs-/Linkprozess für Codedateien. Visual Studio stellt eine Reihe von Ressourcen-Editoren zur Verfügung, die das Erstellen und Ändern von Ressourcen ermöglichen. (Diese Tools sind in den Express-Editionen von Visual Studio.) Eine RC-Datei ist jedoch einfach eine Textdatei, und die Syntax ist auf MSDN dokumentiert, sodass es möglich ist, eine RC-Datei mit einem beliebigen Text-Editor zu erstellen. Weitere Informationen finden Sie unter [Informationen zu Ressourcendateien.](/windows/desktop/menurc/about-resource-files)

## <a name="defining-an-accelerator-table"></a>Definieren einer Zugriffstastentabelle

Eine Zugriffstastentabelle ist eine Tabelle mit Tastenkombinationen. Jede Verknüpfung wird definiert durch:

-   Ein numerischer Bezeichner. Diese Zahl gibt den Anwendungsbefehl an, der von der Verknüpfung aufgerufen wird.
-   Das ASCII-Zeichen oder der Virtuelle Schlüsselcode der Verknüpfung.
-   Optionale Modifizierertasten: ALT, UMSCHALT ODER STRG.

Die Zugriffstastentabelle selbst verfügt über einen numerischen Bezeichner, der die Tabelle in der Liste der Anwendungsressourcen identifiziert. Erstellen Sie eine Zugriffstastentabelle für ein einfaches Zeichenprogramm. Dieses Programm hat zwei Modi: den Draw-Modus und den Auswahlmodus. Im Draw-Modus kann der Benutzer Formen zeichnen. Im Auswahlmodus kann der Benutzer Formen auswählen. Für dieses Programm möchten wir die folgenden Tastenkombinationen definieren.



| Verknüpfung | Befehl                   |
|----------|---------------------------|
| STRG+M   | Umschalten zwischen Modi.     |
| F1       | Wechseln Sie in den Zeichnen-Modus.      |
| F2       | Wechseln Sie in den Auswahlmodus. |



 

Definieren Sie zunächst numerische Bezeichner für die Tabelle und für die Anwendungsbefehle. Diese Werte sind willkürlich. Sie können symbolische Konstanten für die Bezeichner zuweisen, indem Sie sie in einer Headerdatei definieren. Beispiel:


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



In diesem Beispiel identifiziert der `IDR_ACCEL1` -Wert die Accelerator-Tabelle, und die nächsten drei Konstanten definieren die Anwendungsbefehle. Standardmäßig wird eine Headerdatei, die Ressourcenkonst constants definiert, häufig als resource.h bezeichnet. In der nächsten Auflistung wird die Ressourcendefinitionsdatei angezeigt.


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



Die Tastenkombinationen werden in geschweiften Klammern definiert. Jede Verknüpfung enthält die folgenden Einträge.

-   Der Virtuelle Schlüsselcode oder das ASCII-Zeichen, das die Verknüpfung aufruft.
-   Der Anwendungsbefehl. Beachten Sie, dass symbolische Konstanten im Beispiel verwendet werden. Die Ressourcendefinitionsdatei enthält resource.h, in der diese Konstanten definiert sind.
-   Das Schlüsselwort **VIRTKEY bedeutet,** dass der erste Eintrag ein Virtueller Schlüsselcode ist. Die andere Option ist die Verwendung von ASCII-Zeichen.
-   Optionale Modifizierer: ALT, CONTROL oder SHIFT.

Wenn Sie ASCII-Zeichen für Tastenkombinationen verwenden, ist ein Kleinbuchstaben eine andere Verknüpfung als ein Großbuchstaben. (Wenn Sie beispielsweise "a" eingeben, kann ein anderer Befehl als die Eingabe von "A" aufgerufen werden.) Dies kann benutzerverwirrend sein, daher ist es im Allgemeinen besser, für Tastenkombinationen Anstelle von ASCII-Zeichen Codes mit virtuellen Schlüsseln zu verwenden.

## <a name="loading-the-accelerator-table"></a>Laden der Accelerator-Tabelle

Die Ressource für die Zugriffstastentabelle muss geladen werden, bevor das Programm sie verwenden kann. Um eine Zugriffstastentabelle zu laden, rufen Sie die [**LoadAccelerators-Funktion**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) auf.


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



Rufen Sie diese Funktion auf, bevor Sie die Meldungsschleife eingeben. Der erste Parameter ist das Handle für das Modul. (Dieser Parameter wird an Ihre [**WinMain-Funktion**](/windows/desktop/api/winbase/nf-winbase-winmain) übergeben. Weitere Informationen finden Sie unter [WinMain: Der Anwendungseinstiegspunkt](winmain--the-application-entry-point.md).) Der zweite Parameter ist der Ressourcenbezeichner. Die Funktion gibt ein Handle an die Ressource zurück. Denken Sie daran, dass ein Handle ein nicht transparenter Typ ist, der auf ein vom System verwaltetes Objekt verweist. Wenn die Funktion fehlschlägt, gibt sie **NULL zurück.**

Sie können eine Zugriffstastentabelle durch Aufrufen [**von DestroyAcceleratorTable veröffentlichen.**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable) Allerdings gibt das System die Tabelle automatisch frei, wenn das Programm beendet wird. Daher müssen Sie diese Funktion nur aufrufen, wenn Sie eine Tabelle durch eine andere ersetzen. Ein interessantes Beispiel hierfür finden Sie im Thema Creating User Editable Accelerators (Erstellen von [bearbeitbaren Beschleunigern für Benutzer).](/windows/desktop/menurc/using-keyboard-accelerators)

## <a name="translating-key-strokes-into-commands"></a>Übersetzen von Tastenstrichen in Befehle

Eine Zugriffstastentabelle übersetzt Schlüsselstriche in [**WM \_ COMMAND-Meldungen.**](/windows/desktop/menurc/wm-command) Der *wParam-Parameter* von **WM \_ COMMAND** enthält den numerischen Bezeichner des Befehls. Wenn Sie beispielsweise die zuvor gezeigte Tabelle verwenden, wird der Tastenstrich STRG+M in eine **WM \_ COMMAND-Meldung** mit dem Wert `ID_TOGGLE_MODE` übersetzt. Um dies zu ermöglichen, ändern Sie die Nachrichtenschleife wie folgt:


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



Dieser Code fügt einen Aufruf der [**TranslateAccelerator-Funktion**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) innerhalb der Nachrichtenschleife hinzu. Die **TranslateAccelerator-Funktion** untersucht jede Fenstermeldung und sucht nach Key-Down-Meldungen. Wenn der Benutzer eine der in der Zugriffstastentabelle aufgeführten Tastenkombinationen drückt, sendet **TranslateAccelerator** eine [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) an das Fenster. Die Funktion sendet **WM \_ COMMAND,** indem sie die Fensterprozedur direkt aufruft. Wenn **TranslateAccelerator** einen Schlüsselstrich erfolgreich übersetzt, gibt die Funktion einen Wert zurück, der nicht 0 (null) ist. Das bedeutet, dass Sie die normale Verarbeitung für die Nachricht überspringen sollten. Andernfalls **gibt TranslateAccelerator** 0 (null) zurück. Übergeben Sie in diesem Fall die Fensternachricht wie gewohnt [**an TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) und [**DispatchMessage.**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)

So könnte das Zeichnungsprogramm die [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) behandeln:


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



In diesem Code wird davon ausgegangen, `SetMode` dass eine funktion ist, die von der Anwendung definiert wird, um zwischen den beiden Modi zu wechseln. Die Details zur Handhabung der einzelnen Befehle hängen natürlich von Ihrem Programm ab.

## <a name="next"></a>Nächste

[Festlegen des Cursorbilds](setting-the-cursor-image.md)

 

 
