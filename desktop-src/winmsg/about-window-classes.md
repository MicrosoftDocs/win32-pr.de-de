---
description: Jede Fensterklasse verfügt über eine zugeordnete Fensterprozedur, die von allen Fenstern derselben Klasse gemeinsam genutzt wird. Die Fensterprozedur verarbeitet Meldungen für alle Fenster dieser Klasse und steuert daher deren Verhalten und Darstellung.
ms.assetid: db79fd4b-6a15-4bf9-a0d9-5f6415f6c75f
title: Informationen zu Fensterklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fcb46d862bf5b9249bb4f13b111ac10c441c3e687dd3fb1784f355c40d14b72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932330"
---
# <a name="about-window-classes"></a>Informationen zu Fensterklassen

Jede Fensterklasse verfügt über eine zugeordnete Fensterprozedur, die von allen Fenstern derselben Klasse gemeinsam genutzt wird. Die Fensterprozedur verarbeitet Meldungen für alle Fenster dieser Klasse und steuert daher deren Verhalten und Darstellung. Weitere Informationen finden Sie unter [Window Procedures](window-procedures.md).

Ein Prozess muss eine Fensterklasse registrieren, bevor er ein Fenster dieser Klasse erstellen kann. Beim Registrieren einer Fensterklasse werden eine Fensterprozedur, Klassenstile und andere Klassenattribute einem Klassennamen zu ordnet. Wenn ein Prozess einen Klassennamen in der [**CreateWindow-**](/windows/win32/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) angibt, erstellt das System ein Fenster mit der Fensterprozedur, stilen und anderen Attributen, die diesem Klassennamen zugeordnet sind.

In diesem Abschnitt werden die folgenden Themen erläutert.

-   [Typen von Fensterklassen](#types-of-window-classes)
    -   [Systemklassen](#system-classes)
    -   [Globale Anwendungsklassen](#application-global-classes)
    -   [Lokale Anwendungsklassen](#application-local-classes)
-   [So sucht das System nach einer Fensterklasse](#how-the-system-locates-a-window-class)
-   [Registrieren einer Fensterklasse](#registering-a-window-class)
-   [Elemente einer Window-Klasse](#elements-of-a-window-class)
    -   [Klassenname](#class-name)
    -   [Fensterprozeduradresse](#window-procedure-address)
    -   [Instanzhandle](#instance-handle)
    -   [Klassencursor](#class-cursor)
    -   [Klassensymbole](#class-icons)
    -   [Klassenhintergrundpinsel](#class-background-brush)
    -   [Klassenmenü](#class-menu)
    -   [Klassenstile](#class-styles)
    -   [Zusätzlicher Klassenspeicher](#extra-class-memory)
    -   [Zusätzlicher Fensterspeicher](#extra-window-memory)

## <a name="types-of-window-classes"></a>Typen von Fensterklassen

Es gibt drei Typen von Fensterklassen:

-   [Systemklassen](#system-classes)
-   [Globale Anwendungsklassen](#application-global-classes)
-   [Lokale Anwendungsklassen](#application-local-classes)

Diese Typen unterscheiden sich im Gültigkeitsbereich und in wann und wie sie registriert und zerstört werden.

### <a name="system-classes"></a>Systemklassen

Eine Systemklasse ist eine vom System registrierte Fensterklasse. Viele Systemklassen sind für alle Prozesse verfügbar, während andere nur intern vom System verwendet werden. Da das System diese Klassen registriert, kann ein Prozess sie nicht zerstören.

Das System registriert die Systemklassen für einen Prozess, wenn einer seiner Threads zum ersten Mal eine User- oder Windows Graphics Device Interface(GDI)-Funktion aufruft.

Jede Anwendung erhält eine eigene Kopie der Systemklassen. Alle 16-Bit-Windows-basierten Anwendungen in denselben SYSTEMklassen teilen sich systemklassen, genau wie bei 16-Bit-Windows.

In der folgenden Tabelle werden die Systemklassen beschrieben, die für alle Prozesse verfügbar sind.



| Klasse     | Beschreibung                         |
|-----------|-------------------------------------|
| Schaltfläche    | Die Klasse für eine Schaltfläche.             |
| Kombinationsfeld  | Die Klasse für ein Kombinationsfeld.          |
| Bearbeiten      | Die -Klasse für ein Bearbeitungssteuer steuerelement.      |
| ListBox   | Die Klasse für ein Listenfeld.           |
| MDIClient | Die -Klasse für ein MDI-Clientfenster. |
| ScrollBar | Die -Klasse für eine Bildlaufleiste.         |
| statischen    | Die -Klasse für ein statisches Steuerelement.     |



 

In der folgenden Tabelle werden die Systemklassen beschrieben, die nur für die Verwendung durch das System verfügbar sind. Sie werden aus Gründen der Vollständigkeit hier aufgeführt.



| Klasse      | Beschreibung                                                            |
|------------|------------------------------------------------------------------------|
| ComboLBox  | Die Klasse für das Listenfeld, das in einem Kombinationsfeld enthalten ist.                   |
| DDEMLEvent | Die -Klasse für dynamische Daten Exchange DDEML-Ereignisse (Management Library). |
| `Message`    | Die -Klasse für ein Nur-Nachrichten-Fenster.                                   |
| \#32768    | Die -Klasse für ein Menü.                                                  |
| \#32769    | Die -Klasse für das Desktopfenster.                                      |
| \#32770    | Die -Klasse für ein Dialogfeld.                                            |
| \#32771    | Die Klasse für das Aufgabenwechselfenster.                                  |
| \#32772    | Die Klasse für Symboltitel.                                             |



 

### <a name="application-global-classes"></a>Globale Anwendungsklassen

Eine [globale Anwendungsklasse ist](#application-global-classes) eine Von einer ausführbaren Datei oder DLL registrierte Fensterklasse, die für alle anderen Module im Prozess verfügbar ist. Ihr .dll kann beispielsweise die [**RegisterClassEx-Funktion**](/windows/win32/api/winuser/nf-winuser-registerclassexa) aufrufen, um eine Fensterklasse zu registrieren, die ein benutzerdefiniertes Steuerelement als globale Anwendungsklasse definiert, sodass ein Prozess, der die .dll lädt, Instanzen des benutzerdefinierten Steuerelements erstellen kann.

Um eine Klasse zu erstellen, die in jedem Prozess verwendet werden kann, erstellen Sie die Fensterklasse in .dll und laden die .dll in jedem Prozess. Um die .dll in jedem Prozess zu laden, fügen Sie ihren Namen dem **Wert der AppInit-DLLs \_** im folgenden Registrierungsschlüssel hinzu:

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows**

Wenn ein Prozess gestartet wird, lädt das System die angegebene .dll im Kontext des neu gestarteten Prozesses, bevor die Einstiegspunktfunktion aufruft. Der .dll muss die Klasse während der Initialisierungsprozedur registrieren und den **CS \_ GLOBALCLASS-Stil** angeben. Weitere Informationen finden Sie unter [Klassenstile.](#class-styles)

Verwenden Sie die [**UnregisterClass-Funktion,**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) um eine globale Anwendungsklasse zu entfernen und den zugeordneten Speicher frei zu geben.

### <a name="application-local-classes"></a>Lokale Anwendungsklassen

Eine [lokale Anwendungsklasse ist](#application-local-classes) eine beliebige Fensterklasse, die von einer ausführbaren datei oder .dll zur exklusiven Verwendung registriert wird. Obwohl Sie eine beliebige Anzahl von lokalen Klassen registrieren können, ist es typisch, nur eine zu registrieren. Diese Fensterklasse unterstützt die Fensterprozedur des Hauptfensters der Anwendung.

Das System zerstört eine lokale Klasse, wenn das Modul, das sie registriert hat, geschlossen wird. Eine Anwendung kann auch die [**UnregisterClass-Funktion**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) verwenden, um eine lokale Klasse zu entfernen und den zugeordneten Speicher frei zu geben.

## <a name="how-the-system-locates-a-window-class"></a>So sucht das System nach einer Fensterklasse

Das System verwaltet eine Liste von Strukturen für jeden der drei Typen von Fensterklassen. Wenn eine Anwendung die [**CreateWindow-**](/windows/win32/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) aufruft, um ein Fenster mit einer angegebenen Klasse zu erstellen, verwendet das System das folgende Verfahren, um die Klasse zu suchen.

1.  Suchen Sie in der Liste der lokalen Anwendungsklassen nach einer Klasse mit dem angegebenen Namen, deren Instanzhand handle dem Instanzhand handle des Moduls entspricht. (Mehrere Module können denselben Namen verwenden, um lokale Klassen im gleichen Prozess zu registrieren.)
2.  Wenn der Name nicht in der Lokalen Klassenliste der Anwendung enthalten ist, durchsuchen Sie die Liste der globalen Anwendungsklassen.
3.  Wenn der Name nicht in der globalen Klassenliste der Anwendung enthalten ist, durchsuchen Sie die Liste der Systemklassen.

Alle von der Anwendung erstellten Fenster verwenden dieses Verfahren, einschließlich der Fenster, die vom System im Auftrag der Anwendung erstellt werden, z. B. Dialogfelder. Es ist möglich, Systemklassen außer Kraft zu setzen, ohne andere Anwendungen zu beeinträchtigen. Das heißt, eine Anwendung kann eine lokale Anwendungsklasse registrieren, die den gleichen Namen wie eine Systemklasse hat. Dadurch wird die Systemklasse im Kontext der Anwendung ersetzt, aber es wird nicht verhindert, dass andere Anwendungen die Systemklasse verwenden.

## <a name="registering-a-window-class"></a>Registrieren einer Fensterklasse

Eine Fensterklasse definiert die Attribute eines Fensters, z. B. Stil, Symbol, Cursor, Menü und Fensterprozedur. Der erste Schritt beim Registrieren einer Fensterklasse besteht im Ausfüllen einer [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) mit den Fensterklasseninformationen. Weitere Informationen finden Sie unter [Elemente einer Window-Klasse.](#elements-of-a-window-class) Übergeben Sie als Nächstes die -Struktur an die [**RegisterClassEx-Funktion.**](/windows/win32/api/winuser/nf-winuser-registerclassexa) Weitere Informationen finden Sie unter [Verwenden von Fensterklassen.](using-window-classes.md)

Um eine globale Anwendungsklasse zu registrieren, geben Sie den CS \_ GLOBALCLASS-Stil im Stil member der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) an.  Geben Sie beim Registrieren einer lokalen Anwendungsklasse nicht den **CS \_ GLOBALCLASS-Stil** an.

Wenn Sie die Fensterklasse mit der ANSI-Version von [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa), **RegisterClassExA** registrieren, fordert die Anwendung an, dass das System Textparameter von Nachrichten mithilfe des ANSI-Zeichensets an die Fenster der erstellten Klasse über gibt. Wenn Sie die -Klasse mithilfe der Unicode-Version von **RegisterClassEx**, **RegisterClassExW** registrieren, fordert die Anwendung an, dass das System Textparameter von Nachrichten mithilfe des Unicode-Zeichensets an die Fenster der erstellten Klasse über gibt. Mit [**der IsWindowUnicode-Funktion**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) können Anwendungen die Art der einzelnen Fenster abfragen. Weitere Informationen zu ANSI- und Unicode-Funktionen finden Sie unter [Konventionen für Funktionsprototypen.](/windows/desktop/Intl/conventions-for-function-prototypes)

Die ausführbare Datei oder DLL, die die Klasse registriert hat, ist der Besitzer der Klasse. Das System bestimmt den Klassenbesitz vom **hInstance-Member** der [**WNDCLASSEX-Struktur,**](/windows/win32/api/winuser/ns-winuser-wndclassexa) der an die [**RegisterClassEx-Funktion**](/windows/win32/api/winuser/nf-winuser-registerclassexa) übergeben wird, wenn die Klasse registriert wird. Bei DLLs muss **das hInstance-Member** das Handle für die .dll sein.

Die -Klasse wird nicht zerstört, wenn der .dll, der sie besitzt, entladen wird. Wenn das System die Fensterprozedur für ein Fenster dieser Klasse aufruft, verursacht dies daher eine Zugriffsverletzung, da sich die .dll, die die Fensterprozedur enthält, nicht mehr im Arbeitsspeicher befindet. Der Prozess muss alle Fenster mithilfe der -Klasse zerstören, bevor .dll entlädt und die [**UnregisterClass-Funktion aufruft.**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)

## <a name="elements-of-a-window-class"></a>Elemente einer Window-Klasse

Die Elemente einer Fensterklasse definieren das Standardverhalten von Fenstern, die zur -Klasse gehören. Die Anwendung, die eine Fensterklasse registriert, weist der Klasse Elemente zu, indem sie die entsprechenden Member in einer [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) festlegen und die Struktur an die [**RegisterClassEx-Funktion übergeben.**](/windows/win32/api/winuser/nf-winuser-registerclassexa) Die [**Funktionen GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa) und [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga) rufen Informationen zu einer bestimmten Fensterklasse ab. Die [**SetClassLong-Funktion**](/windows/win32/api/winuser/nf-winuser-setclasslonga) ändert Elemente einer lokalen oder globalen Klasse, die die Anwendung bereits registriert hat.

Obwohl eine vollständige Fensterklasse aus vielen Elementen besteht, erfordert das System nur, dass eine Anwendung einen Klassennamen, die Fensterprozeduradresse und ein Instanzhand handle anfordert. Verwenden Sie die anderen Elemente, um Standardattribute für Fenster der -Klasse zu definieren, z. B. die Form des Cursors und den Inhalt des Menüs für das Fenster. Sie müssen alle nicht verwendeten Member der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) auf null oder **NULL initialisieren.** Die Fensterklassenelemente sind wie in der folgenden Tabelle dargestellt.



| Element                                               | Zweck                                                                                                                                                                                                                                       |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Klassenname](#class-name)                             | Unterscheidet die -Klasse von anderen registrierten Klassen.                                                                                                                                                                                        |
| [Fensterprozeduradresse](#window-procedure-address) | Zeiger auf die Funktion, die alle Nachrichten verarbeitet, die an Fenster in der -Klasse gesendet werden, und das Verhalten des Fensters definiert.                                                                                                                      |
| [Instanzhandle](#instance-handle)                   | Identifiziert die Anwendung oder den .dll, der die Klasse registriert hat.                                                                                                                                                                                 |
| [Klassencursor](#class-cursor)                         | Definiert den Mauszeiger, der vom System für ein Fenster der -Klasse angezeigt wird.                                                                                                                                                                  |
| [Klassensymbole](#class-icons)                           | Definiert das große Symbol und das kleine Symbol.                                                                                                                                                                                                    |
| [Klassenhintergrundpinsel](#class-background-brush)     | Definiert die Farbe und das Muster, die den Clientbereich ausfüllen, wenn das Fenster geöffnet oder gestrichet wird.                                                                                                                                                 |
| [Klassenmenü](#class-menu)                             | Gibt das Standardmenü für Fenster an, die kein Menü explizit definieren.                                                                                                                                                                  |
| [Klassenstile](#class-styles)                         | Definiert, wie das Fenster nach dem Verschieben oder Ändern der Größe aktualisiert wird, wie Doppelklicks mit der Maus verarbeiten, wie Speicherplatz für den Gerätekontext und andere Aspekte des Fensters reserviert werden.                                                       |
| [Zusätzlicher Klassenspeicher](#extra-class-memory)             | Gibt den zusätzlichen Arbeitsspeicher in Bytes an, den das System für die Klasse reservieren soll. Alle Fenster in der -Klasse nutzen den zusätzlichen Arbeitsspeicher gemeinsam und können ihn für jeden anwendungsdefinierten Zweck verwenden. Das System initialisiert diesen Arbeitsspeicher auf 0 (null). |
| [Zusätzlicher Fensterspeicher](#extra-window-memory)           | Gibt die Menge an zusätzlichem Arbeitsspeicher in Bytes an, die das System für jedes Fenster reservieren soll, das zur -Klasse gehört. Der zusätzliche Arbeitsspeicher kann für jeden anwendungsdefinierten Zweck verwendet werden. Das System initialisiert diesen Arbeitsspeicher auf 0 (null).          |



 

### <a name="class-name"></a>Klassenname

Jede Fensterklasse benötigt einen [Klassennamen,](#class-name) um eine Klasse von einer anderen zu unterscheiden. Weisen Sie einen Klassennamen zu, indem Sie den **lpszClassName-Member** der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) auf die Adresse einer auf NULL beendeten Zeichenfolge festlegen, die den Namen angibt. Da Fensterklassen prozessspezifisch sind, müssen Fensterklassennamen nur innerhalb desselben Prozesses eindeutig sein. Da Klassennamen den Platz in der privaten Atomtabelle des Systems belegen, sollten Sie klassennamenszeichenfolgen so kurz wie möglich halten.

Die [**GetClassName-Funktion**](/windows/win32/api/winuser/nf-winuser-getclassname) ruft den Namen der Klasse ab, zu der ein bestimmtes Fenster gehört.

### <a name="window-procedure-address"></a>Adresse der Fensterprozedur

Jede Klasse benötigt eine Fensterprozeduradresse, um den Einstiegspunkt der Fensterprozedur zu definieren, die zum Verarbeiten aller Meldungen für Fenster in der -Klasse verwendet wird. Das System übergibt Nachrichten an die Prozedur, wenn das Fenster Aufgaben ausführen muss, z. B. das Malen des Clientbereichs oder das Reagieren auf Eingaben des Benutzers. Ein Prozess weist einer Klasse eine Fensterprozedur zu, indem seine Adresse in den **lpfnWndProc-Member** der [**WNDCLASSEX-Struktur kopiert**](/windows/win32/api/winuser/ns-winuser-wndclassexa) wird. Weitere Informationen finden Sie unter [Window Procedures](window-procedures.md).

### <a name="instance-handle"></a>Instanzhandle

Jede Fensterklasse erfordert ein Instanzhand handle, um die Anwendung oder den .dll, der die Klasse registriert hat, zu identifizieren. Das System erfordert Instanzhandles, um alle Module nachverfolgen zu können. Das System weist jeder Kopie einer ausgeführten ausführbaren Datei oder eines ausgeführten .dll.

Das System übergibt ein Instanzhandl an die Einstiegspunktfunktion jeder ausführbaren Datei (siehe [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)) und .dll (siehe [**DllMain**](/windows/desktop/Dlls/dllmain)). Die ausführbare Datei oder .dll weist der -Klasse dieses Instanzhand handle zu, indem es in den **hInstance-Member** der [**WNDCLASSEX-Struktur kopiert**](/windows/win32/api/winuser/ns-winuser-wndclassexa) wird.

### <a name="class-cursor"></a>Klassencursor

Der *Klassencursor* definiert die Form des Cursors, wenn er sich im Clientbereich eines Fensters in der -Klasse befindet. Das System legt den Cursor automatisch auf die gegebene Form fest, wenn der Cursor in den Clientbereich des Fensters eintritt, und stellt sicher, dass diese Form erhalten bleibt, solange sie im Clientbereich verbleibt. Um einer Fensterklasse eine Cursorform zu zuweisen, laden Sie eine vordefinierte Cursorform mithilfe der [**LoadCursor-Funktion,**](/windows/desktop/api/winuser/nf-winuser-loadcursora) und weisen Sie dann das zurückgegebene Cursorhandle dem **hCursor-Member** der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) zu. Alternativ können Sie eine benutzerdefinierte Cursorressource bereitstellen und die **LoadCursor-Funktion** verwenden, um sie aus den Ressourcen der Anwendung zu laden.

Das System erfordert keinen Klassencursor. Wenn eine Anwendung den **hCursor-Member** der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) auf **NULL** setzt, wird kein Klassencursor definiert. Das System geht davon aus, dass das Fenster die Cursorform jedes Mal fest legt, wenn der Cursor in das Fenster bewegt wird. Ein Fenster kann die Cursorform festlegen, indem die [**SetCursor-Funktion**](/windows/desktop/api/winuser/nf-winuser-setcursor) immer dann aufruft, wenn das Fenster die [**WM \_ MOUSEMOVE-Nachricht**](/windows/desktop/inputdev/wm-mousemove) empfängt. Weitere Informationen zu Cursorn finden Sie unter [Cursor.](/windows/desktop/menurc/cursors)

### <a name="class-icons"></a>Klassensymbole

Ein *Klassensymbol* ist ein Bild, das das System verwendet, um ein Fenster einer bestimmten Klasse zu darstellen. Eine Anwendung kann über zwei Klassensymbole verfügen: eins groß und ein kleines. Das System zeigt das große Klassensymbol eines Fensters *im* Taskschalterfenster an, das angezeigt wird, wenn der Benutzer ALT+TAB drückt, sowie in den großen Symbolansichten der Taskleiste und des Explorers. Das *kleine Klassensymbol* wird in der Titelleiste eines Fensters und in den kleinen Symbolansichten der Taskleiste und des Explorers angezeigt.

Um einer Fensterklasse ein großes und kleines Symbol zu zuweisen, geben Sie die Handles der Symbole in den **Membern hIcon** **und hIconSm** der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) an. Die Symboldimensionen müssen den erforderlichen Dimensionen für große und kleine Klassensymbole entsprechen. Für ein großes Klassensymbol können Sie die erforderlichen Dimensionen ermitteln, indem Sie die **SM \_ CXICON-** und **SM \_ CYICON-Werte** in einem Aufruf der [**GetSystemMetrics-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) angeben. Geben Sie für ein kleines Klassensymbol die **Werte SM \_ CXSMICON** und **SM \_ CYSMICON** an. Weitere Informationen finden Sie unter [Symbole](/windows/desktop/menurc/icons).

Wenn eine Anwendung die **Member hIcon** und **hIconSm** der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) auf **NULL** setzt, verwendet das System das Standardanwendungssymbol als große und kleine Klassensymbole für die Fensterklasse. Wenn Sie ein großes Klassensymbol angeben, aber kein kleines, erstellt das System ein kleines Klassensymbol basierend auf dem großen. Wenn Sie jedoch ein kleines, aber kein großes Klassensymbol angeben, verwendet das System das Standardanwendungssymbol als großes Klassensymbol und das angegebene Symbol als kleines Klassensymbol.

Sie können das große oder kleine Klassensymbol für ein bestimmtes Fenster überschreiben, indem Sie die [**WM \_ SETICON-Meldung**](wm-seticon.md) verwenden. Sie können das aktuelle große oder kleine Klassensymbol mithilfe der [**WM \_ GETICON-Nachricht**](wm-geticon.md) abrufen.

### <a name="class-background-brush"></a>Klassenhintergrundpinsel

Ein *Klassenhintergrundpinsel* bereitet den Clientbereich eines Fensters für das nachfolgende Zeichnen durch die Anwendung vor. Das System verwendet den Pinsel, um den Clientbereich mit einer Volltonfarbe oder einem Muster zu füllen, wodurch alle vorherigen Bilder von diesem Speicherort entfernt werden, unabhängig davon, ob sie zum Fenster gehören oder nicht. Das System benachrichtigt ein Fenster, dass sein Hintergrund gezeichnet werden soll, indem die [**WM \_ ERASEBKGND-Nachricht**](wm-erasebkgnd.md) an das Fenster gesendet wird. Weitere Informationen finden Sie unter [Pinsel.](/windows/desktop/gdi/brushes)

Um einer Klasse einen Hintergrundpinsel zuzuweisen, erstellen Sie einen Pinsel mithilfe der entsprechenden GDI-Funktionen und weisen das zurückgegebene Pinselhandle dem **hbrBackground-Member** der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) zu.

Anstatt einen Pinsel zu erstellen, kann eine Anwendung den **hbrBackground-Member** auf einen der Standard-Systemfarbwerte festlegen. Eine Liste der Standard-Systemfarbwerte finden Sie unter [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors).

Um eine Standardsystemfarbe zu verwenden, muss die Anwendung den Hintergrundfarbwert um eins erhöhen. COLOR **\_ BACKGROUND** + 1 ist beispielsweise die Hintergrundfarbe des Systems. Alternativ können Sie die [**GetSysColorBrush-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) verwenden, um ein Handle für einen Pinsel abzurufen, der einer Standardsystemfarbe entspricht, und dann das Handle im **hbrBackground-Member** der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) angeben.

Das System erfordert nicht, dass eine Fensterklasse über einen Klassenhintergrundpinsel verfügt. Wenn dieser Parameter auf **NULL** festgelegt ist, muss das Fenster seinen eigenen Hintergrund zeichnen, sobald es die [**WM \_ ERASEBKGND-Nachricht**](wm-erasebkgnd.md) empfängt.

### <a name="class-menu"></a>Klassenmenü

Ein *Klassenmenü* definiert das Standardmenü, das von den Fenstern in der -Klasse verwendet werden soll, wenn beim Erstellen der Fenster kein explizites Menü angegeben wird. Ein Menü ist eine Liste von Befehlen, über die ein Benutzer Aktionen auswählen kann, die von der Anwendung ausgeführt werden sollen.

Sie können einer Klasse ein Menü zuweisen, indem Sie den **lpszMenuName-Member** der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) auf die Adresse einer auf NULL endende Zeichenfolge festlegen, die den Ressourcennamen des Menüs angibt. Das Menü wird als Ressource in der angegebenen Anwendung angenommen. Das System lädt das Menü automatisch, wenn es benötigt wird. Wenn die Menüressource durch eine ganze Zahl und nicht durch einen Namen identifiziert wird, kann die Anwendung das **lpszMenuName-Element** auf diese ganze Zahl festlegen, indem das [**MAKEINTRESOURCE-Makro**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) angewendet wird, bevor der Wert zugewiesen wird.

Das System erfordert kein Klassenmenü. Wenn eine Anwendung den **lpszMenuName-Member** der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) auf **NULL** festlegt, haben Fenster in der -Klasse keine Menüleisten. Auch wenn kein Klassenmenü angegeben ist, kann eine Anwendung beim Erstellen des Fensters trotzdem eine Menüleiste für ein Fenster definieren.

Wenn ein Menü für eine Klasse angegeben und ein untergeordnetes Fenster dieser Klasse erstellt wird, wird das Menü ignoriert. Weitere Informationen finden Sie unter [Menüs](/windows/desktop/menurc/menus).

### <a name="class-styles"></a>Klassenstile

Die Klassenstile definieren zusätzliche Elemente der Fensterklasse. Zwei oder mehr Stile können mithilfe des bitweisen OR \| ()-Operators kombiniert werden. Um einer Fensterklasse einen Stil zuzuweisen, weisen Sie den Stil dem **Stilmember** der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) zu. Eine Liste der Klassenstile finden Sie unter [**Fensterklassenstile.**](window-class-styles.md)

### <a name="classes-and-device-contexts"></a>Klassen und Gerätekontexte

Ein *Gerätekontext* ist ein spezieller Satz von Werten, die Anwendungen zum Zeichnen im Clientbereich ihrer Fenster verwenden. Das System erfordert einen Gerätekontext für jedes Fenster auf dem Display, ermöglicht aber eine gewisse Flexibilität bei der Speicherung und Behandlung dieses Gerätekontexts durch das System.

Wenn kein Gerätekontextstil explizit angegeben wird, geht das System davon aus, dass jedes Fenster einen Gerätekontext verwendet, der aus einem Pool von Kontexten abgerufen wird, die vom System verwaltet werden. In solchen Fällen muss jedes Fenster den Gerätekontext vor dem Zeichnen abrufen und initialisieren und nach dem Zeichnen freigeben.

Um das Abrufen eines Gerätekontexts bei jedem Zeichnen innerhalb eines Fensters zu vermeiden, kann eine Anwendung den **CS \_ OWNDC-Stil** für die Fensterklasse angeben. Dieser Klassenstil weist das System an, einen privaten Gerätekontext zu erstellen, d.h. einen eindeutigen Gerätekontext für jedes Fenster in der Klasse zuzuordnen. Die Anwendung muss den Kontext nur einmal abrufen und ihn dann für alle nachfolgenden Zeichnungen verwenden.

### <a name="extra-class-memory"></a>Zusätzlicher Klassenspeicher

Das System verwaltet intern eine [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) für jede Fensterklasse im System. Wenn eine Anwendung eine Fensterklasse registriert, kann sie das System anweisen, am Ende der **WNDCLASSEX-Struktur** eine Reihe zusätzlicher Bytes an Arbeitsspeicher zuzuordnen und anzufügen. Dieser Speicher wird als *zusätzlicher Klassenspeicher* bezeichnet und wird von allen Fenstern gemeinsam genutzt, die zur -Klasse gehören. Verwenden Sie den zusätzlichen Klassenspeicher, um alle Informationen zur -Klasse zu speichern.

Da zusätzlicher Arbeitsspeicher vom lokalen Heap des Systems belegt wird, sollte eine Anwendung zusätzlichen Klassenarbeitsspeicher verwenden. Die [**RegisterClassEx-Funktion**](/windows/win32/api/winuser/nf-winuser-registerclassexa) schlägt fehl, wenn der angeforderte zusätzliche Klassenspeicher größer als 40 Bytes ist. Wenn eine Anwendung mehr als 40 Bytes erfordert, sollte sie ihren eigenen Arbeitsspeicher zuordnen und einen Zeiger auf den Arbeitsspeicher im zusätzlichen Klassenspeicher speichern.

Die Funktionen [**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword) und [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) kopieren einen Wert in den zusätzlichen Klassenspeicher. Um einen Wert aus dem zusätzlichen Klassenspeicher abzurufen, verwenden Sie die Funktionen [**GetClassWord**](/windows/win32/api/winuser/nf-winuser-getclassword) und [**GetClassLong.**](/windows/win32/api/winuser/nf-winuser-getclasslonga) Der **cbClsExtra-Member** der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) gibt die Menge an zusätzlichem Klassenspeicher an, der zugeordnet werden soll. Eine Anwendung, die keinen zusätzlichen Klassenspeicher verwendet, muss den **cbClsExtra-Member** mit 0 (null) initialisieren.

### <a name="extra-window-memory"></a>Zusätzlicher Fensterspeicher

Das System verwaltet eine interne Datenstruktur für jedes Fenster. Beim Registrieren einer Fensterklasse kann eine Anwendung eine Anzahl zusätzlicher Bytes an Arbeitsspeicher angeben, die als *zusätzlicher Fensterarbeitsspeicher* bezeichnet wird. Beim Erstellen eines Fensters der -Klasse ordnet das System die angegebene Menge an zusätzlichem Fensterspeicher an das Ende der Fensterstruktur zu und fügt sie an. Eine Anwendung kann diesen Arbeitsspeicher verwenden, um fensterspezifische Daten zu speichern.

Da vom lokalen Heap des Systems zusätzlicher Arbeitsspeicher belegt wird, sollte eine Anwendung zusätzlichen Fensterarbeitsspeicher verwenden. Die [**RegisterClassEx-Funktion**](/windows/win32/api/winuser/nf-winuser-registerclassexa) schlägt fehl, wenn der angeforderte zusätzliche Fensterspeicher größer als 40 Bytes ist. Wenn eine Anwendung mehr als 40 Bytes erfordert, sollte sie ihren eigenen Arbeitsspeicher zuordnen und einen Zeiger auf den Arbeitsspeicher im zusätzlichen Fensterspeicher speichern.

Die [**SetWindowLong-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) kopiert einen Wert in den zusätzlichen Arbeitsspeicher. Die [**GetWindowLong-Funktion**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) ruft einen Wert aus dem zusätzlichen Arbeitsspeicher ab. Der **cbWndExtra-Member** der [**WNDCLASSEX-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassexa) gibt die Menge an zusätzlichem Fensterspeicher an, der zugeordnet werden soll. Eine Anwendung, die den Arbeitsspeicher nicht verwendet, muss **cbWndExtra** mit 0 (null) initialisieren.

 

 
