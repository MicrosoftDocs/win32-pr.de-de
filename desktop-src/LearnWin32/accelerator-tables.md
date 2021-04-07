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
# <a name="accelerator-tables"></a>Zugriffstasten Tabellen

Anwendungen definieren häufig Tastenkombinationen, wie z. b. STRG + O für den Befehl zum Öffnen von Dateien. Sie können Tastenkombinationen implementieren, indem Sie einzelne [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Meldungen verarbeiten, aber Zugriffstasten Tabellen bieten eine bessere Lösung:

-   Erfordert weniger Codierungen.
-   Konsolidiert all Ihre Verknüpfungen in einer Datendatei.
-   Unterstützt die Lokalisierung in andere Sprachen.
-   Ermöglicht es Verknüpfungen und Menübefehlen, dieselbe Anwendungslogik zu verwenden.

Eine Zugriffstasten *Tabelle* ist eine Daten Ressource, die Tastenkombinationen wie STRG + O zu Anwendungs Befehlen zuordnet. Bevor wir uns mit der Verwendung einer Zugriffstasten Tabelle beschäftigen, benötigen wir eine kurze Einführung in die Ressourcen. Eine *Ressource* ist ein Daten-BLOB, das in eine Anwendungs Binärdatei (exe oder dll) integriert ist. In Ressourcen werden Daten gespeichert, die von der Anwendung benötigt werden, z. b. Menüs, Cursor, Symbole, Bilder, Text Zeichenfolgen oder beliebige benutzerdefinierte Anwendungsdaten. Die Anwendung lädt die Ressourcen Daten zur Laufzeit aus der Binärdatei. Gehen Sie folgendermaßen vor, um Ressourcen in eine Binärdatei einzuschließen:

1.  Erstellen Sie eine Ressourcen Definitionsdatei (RC-Datei). Diese Datei definiert die Typen von Ressourcen und deren Bezeichner. Die Ressourcen Definitionsdatei kann Verweise auf andere Dateien enthalten. Beispielsweise wird eine Symbol Ressource in der RC-Datei deklariert, aber das Symbolbild wird in einer separaten Datei gespeichert.
2.  Verwenden Sie den Microsoft Windows-Ressourcen Compiler (RC), um die Ressourcen Definitionsdatei in eine kompilierte Ressourcen Datei (. res) zu kompilieren. Der RC-Compiler wird mit Visual Studio und dem Windows SDK bereitgestellt.
3.  Verknüpfen Sie die kompilierte Ressourcen Datei mit der Binärdatei.

Diese Schritte entsprechen ungefähr dem Kompilierungs-/Linkprozess für Code Dateien. Visual Studio bietet eine Reihe von Ressourcen-Editoren, mit denen Sie problemlos Ressourcen erstellen und ändern können. (Diese Tools sind in den Express-Editionen von Visual Studio nicht verfügbar.) Eine RC-Datei ist einfach eine Textdatei, und die Syntax wird auf MSDN dokumentiert. Daher ist es möglich, eine RC-Datei mit einem beliebigen Text-Editor zu erstellen. Weitere Informationen finden Sie unter Informationen [zu Ressourcen Dateien](/windows/desktop/menurc/about-resource-files).

## <a name="defining-an-accelerator-table"></a>Definieren einer Zugriffstasten Tabelle

Eine Zugriffstasten Tabelle ist eine Tabelle mit Tastenkombinationen. Jede Verknüpfung wird definiert durch:

-   Ein numerischer Bezeichner. Diese Nummer identifiziert den Anwendungs Befehl, der von der Verknüpfung aufgerufen wird.
-   Das ASCII-Zeichen oder der Code für den virtuellen Schlüssel der Verknüpfung.
-   Optionale Modifizierertasten: alt, UMSCHALT oder STRG.

Die Zugriffstasten Tabelle selbst hat einen numerischen Bezeichner, der die Tabelle in der Liste der Anwendungs Ressourcen identifiziert. Erstellen wir eine Zugriffstasten Tabelle für ein einfaches Zeichnungsprogramm. Dieses Programm verfügt über zwei Modi: den Zeichnungsmodus und den Auswahlmodus. Im Draw-Modus kann der Benutzer Formen zeichnen. Im Auswahlmodus kann der Benutzer Formen auswählen. Für dieses Programm möchten wir die folgenden Tastenkombinationen definieren.



| Abkürzung | Get-Help                   |
|----------|---------------------------|
| STRG+M   | Umschalten zwischen Modi.     |
| F1       | Wechseln Sie in den Zeichnungsmodus.      |
| F2       | Wechseln Sie in den Auswahlmodus. |



 

Definieren Sie zunächst numerische Bezeichner für die Tabelle und für die Anwendungs Befehle. Diese Werte sind willkürlich. Sie können symbolische Konstanten für die Bezeichner zuweisen, indem Sie Sie in einer Header Datei definieren. Beispiel:


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



In diesem Beispiel identifiziert der Wert `IDR_ACCEL1` die Zugriffstasten Tabelle, und die nächsten drei Konstanten definieren die Anwendungs Befehle. Gemäß der Konvention wird eine Header Datei, die Ressourcen Konstanten definiert, häufig als "Resource. h" bezeichnet. In der nächsten Liste wird die Ressourcen Definitionsdatei angezeigt.


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



Die Tastenkombinationen werden innerhalb der geschweiften Klammern definiert. Jede Verknüpfung enthält die folgenden Einträge.

-   Der Code des virtuellen Schlüssels oder das ASCII-Zeichen, das die Verknüpfung aufruft.
-   Der Anwendungs Befehl. Beachten Sie, dass im Beispiel symbolische Konstanten verwendet werden. Die Ressourcen Definitionsdatei enthält die Datei "Resource. h", in der diese Konstanten definiert sind.
-   Das Schlüsselwort **VIRTKEY** bedeutet, dass der erste Eintrag ein Code für den virtuellen Schlüssel ist. Die andere Option ist die Verwendung von ASCII-Zeichen.
-   Optionale modifiziererer: alt, Steuerelement oder UMSCHALT.

Wenn Sie ASCII-Zeichen für Verknüpfungen verwenden, ist ein Kleinbuchstabe eine andere Verknüpfung als ein Großbuchstabe. (Wenn Sie z. b. "a" eingeben, wird möglicherweise ein anderer Befehl als "a" aufgerufen.) Das mag Benutzer verwirrend sein, daher ist es in der Regel besser, anstelle von ASCII-Zeichen anstelle von ASCII-Zeichencode für Verknüpfungen zu verwenden.

## <a name="loading-the-accelerator-table"></a>Laden der Zugriffstasten Tabelle

Die Ressource für die Zugriffstasten Tabelle muss geladen werden, bevor Sie vom Programm verwendet werden kann. Wenn Sie eine Zugriffstasten Tabelle laden möchten, können Sie die [**loadaccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) -Funktion abrufen.


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



Diese Funktion wird aufgerufen, bevor Sie die Nachrichten Schleife eingeben. Der erste Parameter ist das Handle für das Modul. (Dieser Parameter wird an Ihre [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) -Funktion übergeben. Weitere Informationen finden Sie unter [WinMain: der Einstiegspunkt der Anwendung](winmain--the-application-entry-point.md).) Der zweite Parameter ist der Ressourcen Bezeichner. Die-Funktion gibt ein Handle für die Ressource zurück. Denken Sie daran, dass ein Handle ein nicht transparenter Typ ist, der auf ein Objekt verweist, das vom System verwaltet wird. Wenn die Funktion fehlschlägt, wird **null** zurückgegeben.

Sie können eine Zugriffstasten Tabelle freigeben, indem Sie [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable)aufrufen. Das System gibt die Tabelle jedoch automatisch frei, wenn das Programm beendet wird. Daher müssen Sie diese Funktion nur dann aufzurufen, wenn Sie eine Tabelle durch eine andere ersetzen. Ein interessantes Beispiel hierfür finden Sie im Thema Erstellen von [Benutzer bearbeitbaren Accelerators](/windows/desktop/menurc/using-keyboard-accelerators).

## <a name="translating-key-strokes-into-commands"></a>Übersetzen von Tastenkombinationen in Befehle

Eine Zugriffstasten Tabelle funktioniert durch Übersetzen von Tastenkombinationen in [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachrichten. Der *wParam* -Parameter des **WM- \_ Befehls** enthält den numerischen Bezeichner des Befehls. Beispielsweise wird der Schlüssel Strich STRG + M mithilfe der zuvor gezeigten Tabelle in eine **WM- \_ Befehls** Meldung mit dem Wert übersetzt `ID_TOGGLE_MODE` . Um dies zu erreichen, ändern Sie die Nachrichten Schleife wie folgt:


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



Dieser Code fügt der [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) -Funktion innerhalb der Nachrichten Schleife einen aufzurufenden Code hinzu. Die **TranslateAccelerator** -Funktion untersucht die einzelnen Fenster Meldungen und sucht nach Schlüsseln nach Schlüsseln. Wenn der Benutzer eine der Tastenkombinationen drückt, die in der Zugriffstasten Tabelle aufgeführt sind, sendet **TranslateAccelerator** eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung an das Fenster. Die Funktion sendet den **WM- \_ Befehl** durch direktes Aufrufen der Fenster Prozedur. Wenn **TranslateAccelerator** einen Schlüssel Strich erfolgreich übersetzt, gibt die Funktion einen Wert ungleich 0 (null) zurück, was bedeutet, dass Sie die normale Verarbeitung der Nachricht überspringen sollten. Andernfalls gibt **TranslateAccelerator** 0 (null) zurück. Übergeben Sie in diesem Fall die Fenster Meldung wie üblich an [**translatemess Age**](/windows/desktop/api/winuser/nf-winuser-translatemessage) und [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage).

Im folgenden wird erläutert, wie das Zeichnungsprogramm die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht verarbeiten kann:


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



Dieser Code setzt voraus, dass `SetMode` eine Funktion ist, die von der Anwendung definiert wird, um zwischen den beiden Modi zu wechseln. Die Details zur Handhabung der einzelnen Befehle hängen offensichtlich von Ihrem Programm ab.

## <a name="next"></a>Nächste

[Festlegen des Cursor Bilds](setting-the-cursor-image.md)

 

 