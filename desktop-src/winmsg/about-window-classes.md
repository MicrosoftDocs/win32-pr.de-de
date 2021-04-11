---
description: Jede Fenster Klasse verfügt über eine zugeordnete Fenster Prozedur, die von allen Fenstern derselben Klasse gemeinsam genutzt wird. Die Fenster Prozedur verarbeitet Nachrichten für alle Fenster dieser Klasse und steuert somit das Verhalten und die Darstellung.
ms.assetid: db79fd4b-6a15-4bf9-a0d9-5f6415f6c75f
title: Informationen zu Fenster Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b683176c3fd7904cf3f89b385ce0fa393b89e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217823"
---
# <a name="about-window-classes"></a>Informationen zu Fenster Klassen

Jede Fenster Klasse verfügt über eine zugeordnete Fenster Prozedur, die von allen Fenstern derselben Klasse gemeinsam genutzt wird. Die Fenster Prozedur verarbeitet Nachrichten für alle Fenster dieser Klasse und steuert somit das Verhalten und die Darstellung. Weitere Informationen finden Sie unter [Window Procedures](window-procedures.md).

Ein Prozess muss eine Fenster Klasse registrieren, bevor ein Fenster dieser Klasse erstellt werden kann. Beim Registrieren einer Fenster Klasse werden eine Fenster Prozedur, Klassen Stile und andere Klassenattribute mit einem Klassennamen verknüpft. Wenn ein Prozess einen Klassennamen in der Funktion "" von " [](/windows/win32/api/winuser/nf-winuser-createwindowexa) " von "", "", "", "", "", "" und "" mit dem Namen " [**" des Klassen**](/windows/win32/api/winuser/nf-winuser-createwindowa) namens angibt, erstellt das System ein Fenster mit der Fenster Prozedur

In diesem Abschnitt werden die folgenden Themen behandelt.

-   [Typen von Fenster Klassen](#types-of-window-classes)
    -   [System Klassen](#system-classes)
    -   [Globale Anwendungs Klassen](#application-global-classes)
    -   [Lokale Anwendungs Klassen](#application-local-classes)
-   [Wie das System eine Fenster Klasse lokalisiert](#how-the-system-locates-a-window-class)
-   [Registrieren einer Fenster Klasse](#registering-a-window-class)
-   [Elemente einer Fenster Klasse](#elements-of-a-window-class)
    -   [Klassenname](#class-name)
    -   [Fenster Prozedur Adresse](#window-procedure-address)
    -   [Instanzhandle](#instance-handle)
    -   [Klassen Cursor](#class-cursor)
    -   [Klassen Symbole](#class-icons)
    -   [Klassenhintergrund Pinsel](#class-background-brush)
    -   [Klassen Menü](#class-menu)
    -   [Klassenstile](#class-styles)
    -   [Zusätzlicher Klassen Arbeitsspeicher](#extra-class-memory)
    -   [Zusätzlicher Fenster Speicher](#extra-window-memory)

## <a name="types-of-window-classes"></a>Typen von Fenster Klassen

Es gibt drei Arten von Fenster Klassen:

-   [System Klassen](#system-classes)
-   [Globale Anwendungs Klassen](#application-global-classes)
-   [Lokale Anwendungs Klassen](#application-local-classes)

Diese Typen unterscheiden sich im Gültigkeitsbereich, wann und wie Sie registriert und zerstört werden.

### <a name="system-classes"></a>System Klassen

Eine System Klasse ist eine vom System registrierte Fenster Klasse. Viele System Klassen sind für alle Prozesse verfügbar, während andere nur intern vom System verwendet werden. Da das System diese Klassen registriert, kann ein Prozess Sie nicht zerstören.

Das System registriert die System Klassen für einen Prozess, wenn ein Thread das erste Mal einen Benutzer oder eine Windows Graphics Device Interface-Funktion (GDI) aufruft.

Jede Anwendung erhält eine eigene Kopie der System Klassen. Alle 16-Bit-Windows-basierten Anwendungen im gleichen VDM Teilen System Klassen auf, genauso wie auf 16-Bit-Fenstern.

In der folgenden Tabelle werden die System Klassen beschrieben, die für die Verwendung durch alle-Prozesse verfügbar sind.



| Klasse     | BESCHREIBUNG                         |
|-----------|-------------------------------------|
| Schaltfläche    | Die-Klasse für eine Schaltfläche.             |
| Kombinationsfeld  | Die Klasse für ein Kombinations Feld.          |
| Bearbeiten      | Die-Klasse für ein Bearbeitungs Steuerelement.      |
| ListBox   | Die-Klasse für ein Listenfeld.           |
| MDIClient | Die-Klasse für ein MDI-Client Fenster. |
| ScrollBar | Die Klasse für eine Schiebe Leiste.         |
| statischen    | Die-Klasse für ein statisches-Steuerelement.     |



 

In der folgenden Tabelle werden die System Klassen beschrieben, die nur für die Verwendung durch das System verfügbar sind. Sie werden hier aus Gründen der Vollständigkeit aufgeführt.



| Klasse      | BESCHREIBUNG                                                            |
|------------|------------------------------------------------------------------------|
| Combolbox  | Die Klasse für das Listenfeld, das in einem Kombinations Feld enthalten ist.                   |
| Ddemlevent | Die-Klasse für Ddeml-Ereignisse (dynamischer Datenaustausch Management Library). |
| `Message`    | Die-Klasse für ein Nachrichten geschütztes Fenster.                                   |
| \#32768    | Die-Klasse für ein Menü.                                                  |
| \#32769    | Die-Klasse für das Desktop Fenster.                                      |
| \#32770    | Die-Klasse für ein Dialogfeld.                                            |
| \#32771    | Die-Klasse für das Fenster "Task Switch".                                  |
| \#32772    | Die Klasse für Symbol Titel.                                             |



 

### <a name="application-global-classes"></a>Globale Anwendungs Klassen

Eine [globale Anwendungsklasse](#application-global-classes) ist eine Fenster Klasse, die von einer ausführbaren Datei oder dll registriert wird, die für alle anderen Module im Prozess verfügbar ist. Beispielsweise kann die DLL-Datei die [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) -Funktion aufrufen, um eine Fenster Klasse zu registrieren, die ein benutzerdefiniertes Steuerelement als globale Anwendungsklasse definiert, sodass ein Prozess, der die DLL-Datei lädt, Instanzen des benutzerdefinierten Steuer Elements erstellen kann.

Erstellen Sie zum Erstellen einer Klasse, die in jedem Prozess verwendet werden kann, die Fenster Klasse in einer DLL, und laden Sie in jedem Prozess die dll. Fügen Sie den Namen des **AppInit- \_ DLLs** im folgenden Registrierungsschlüssel hinzu, um die DLL-Datei in jedem Prozess zu laden:

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows**

Wenn ein Prozess gestartet wird, lädt das System die angegebene DLL in den Kontext des neu gestarteten Prozesses, bevor die Einstiegspunkt Funktion aufgerufen wird. Die dll muss die Klasse während der Initialisierungs Prozedur registrieren und den **CS \_ Global Class** -Stil angeben. Weitere Informationen finden Sie unter [Klassen Stile](#class-styles).

Verwenden Sie die [**unregisterclass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) -Funktion, um eine globale Anwendungsklasse zu entfernen und den zugeordneten Speicher freizugeben.

### <a name="application-local-classes"></a>Lokale Anwendungs Klassen

Eine [lokale Anwendungsklasse](#application-local-classes) ist eine beliebige Fenster Klasse, die eine ausführbare Datei oder eine DLL-Datei für ihre ausschließliche Verwendung registriert. Obwohl Sie eine beliebige Anzahl von lokalen Klassen registrieren können, ist es üblich, nur eine zu registrieren. Diese Fenster Klasse unterstützt die Fenster Prozedur des Hauptfensters der Anwendung.

Das System zerstört eine lokale Klasse, wenn das Modul, das es registriert hat, geschlossen wird. Eine Anwendung kann auch die [**unregisterclass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) -Funktion verwenden, um eine lokale Klasse zu entfernen und den zugeordneten Speicher freizugeben.

## <a name="how-the-system-locates-a-window-class"></a>Wie das System eine Fenster Klasse lokalisiert

Das System verwaltet eine Liste von Strukturen für jeden der drei Typen von Fenster Klassen. Wenn eine Anwendung die Funktion "up [**Window**](/windows/win32/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " aufruft, um ein Fenster mit einer bestimmten Klasse zu erstellen, verwendet das System das folgende Verfahren, um die-Klasse zu suchen.

1.  Durchsuchen Sie die Liste der lokalen Anwendungs Klassen nach einer Klasse mit dem angegebenen Namen, deren Instanzhandle mit dem Instanzhandle des Moduls übereinstimmt. (Mehrere Module können den gleichen Namen verwenden, um lokale Klassen im gleichen Prozess zu registrieren.)
2.  Wenn der Name nicht in der Liste der lokalen Anwendungs Klassen enthalten ist, Durchsuchen Sie die Liste der globalen Anwendungs Klassen.
3.  Wenn der Name nicht in der globalen Klassenliste der Anwendung enthalten ist, Durchsuchen Sie die Liste der System Klassen.

Alle von der Anwendung erstellten Fenster verwenden dieses Verfahren, einschließlich Windows, das vom System im Namen der Anwendung (z. b. in Dialogfeldern) erstellt wurde. System Klassen können außer Kraft gesetzt werden, ohne dass sich dies auf andere Anwendungen auswirkt. Das heißt, eine Anwendung kann eine lokale Anwendungsklasse registrieren, die denselben Namen wie eine System Klasse hat. Dies ersetzt die System Klasse im Kontext der Anwendung, verhindert jedoch nicht, dass andere Anwendungen die System Klasse verwenden.

## <a name="registering-a-window-class"></a>Registrieren einer Fenster Klasse

Eine Fenster Klasse definiert die Attribute eines Fensters, z. b. Stil, Symbol, Cursor, Menü und Fenster Prozedur. Der erste Schritt beim Registrieren einer Fenster Klasse ist das Ausfüllen einer [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur mit den Fenster Klassen Informationen. Weitere Informationen finden Sie unter [Elemente einer Fenster Klasse](#elements-of-a-window-class). Übergeben Sie als nächstes die-Struktur an die [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) -Funktion. Weitere Informationen finden Sie unter [Verwenden von Fenster Klassen](using-window-classes.md).

Um eine globale Anwendungsklasse zu registrieren, geben Sie den CS \_ Global Class-Stil im **Style** -Member der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur an. Wenn Sie eine lokale Anwendungsklasse registrieren, geben Sie den **CS-Stil \_ Global Class** nicht an.

Wenn Sie die Fenster Klasse mithilfe der ANSI-Version von [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa), **registerclassexa**, registrieren, fordert die Anwendung an, dass das System Text Parameter von Meldungen an die Fenster der erstellten Klasse mit dem ANSI-Zeichensatz übergibt. Wenn Sie die Klasse mithilfe der Unicode-Version von **RegisterClassEx**, **registerclassexw**, registrieren, fordert die Anwendung an, dass das System Text Parameter von Meldungen an die Fenster der erstellten Klasse mit dem Unicode-Zeichensatz übergibt. Die [**iswindowunicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) -Funktion ermöglicht Anwendungen, die Art der einzelnen Fenster abzufragen. Weitere Informationen zu ANSI-und Unicode-Funktionen finden Sie unter [Konventionen für Funktionsprototypen](/windows/desktop/Intl/conventions-for-function-prototypes).

Die ausführbare Datei oder dll, die die Klasse registriert hat, ist der Besitzer der Klasse. Das System bestimmt den Klassen Besitz aus dem **HINSTANCE** -Member der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur, die an die [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) -Funktion übermittelt wird, wenn die Klasse registriert wird. Bei DLLs muss das **HINSTANCE** -Element das Handle für die dll-Instanz sein.

Die-Klasse wird nicht zerstört, wenn die DLL-Datei, die Sie besitzt, entladen wird. Wenn das System die Fenster Prozedur für ein Fenster dieser Klasse aufruft, wird daher eine Zugriffsverletzung verursacht, da sich die DLL-Datei, die die Fenster Prozedur enthält, nicht mehr im Arbeitsspeicher befindet. Der Prozess muss alle Fenster mit der-Klasse zerstören, bevor die DLL-Datei entladen und die [**unregisterclass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) -Funktion aufgerufen wird.

## <a name="elements-of-a-window-class"></a>Elemente einer Fenster Klasse

Die Elemente einer Fenster Klasse definieren das Standardverhalten von Fenstern, die zur-Klasse gehören. Die Anwendung, die eine Fenster Klasse registriert, weist der Klasse Elemente zu, indem geeignete Member in einer [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur festgelegt und die Struktur an die [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) -Funktion übergeben wird. Die Funktionen " [**getclassinfoex**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa) " und " [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga) " rufen Informationen über eine bestimmte Fenster Klasse ab. Die [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) -Funktion ändert Elemente einer lokalen oder globalen Klasse, die von der Anwendung bereits registriert wurde.

Obwohl eine komplette Fenster Klasse aus vielen Elementen besteht, erfordert das System lediglich, dass eine Anwendung einen Klassennamen, die Fenster Prozedur Adresse und einen Instanzhandle bereitstellt. Verwenden Sie die anderen-Elemente, um Standard Attribute für Fenster der-Klasse zu definieren, z. b. die Form des Cursors und den Inhalt des Menüs für das Fenster. Sie müssen alle nicht verwendeten Member der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur mit 0 (null) oder **null** initialisieren. Die Fenster Klassen Elemente sind wie in der folgenden Tabelle dargestellt.



| Element                                               | Zweck                                                                                                                                                                                                                                       |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Klassenname](#class-name)                             | Unterscheidet die Klasse von anderen registrierten Klassen.                                                                                                                                                                                        |
| [Fenster Prozedur Adresse](#window-procedure-address) | Ein Zeiger auf die Funktion, die alle an Windows in der-Klasse gesendeten Nachrichten verarbeitet und das Verhalten des Fensters definiert.                                                                                                                      |
| [Instanzhandle](#instance-handle)                   | Identifiziert die Anwendung oder. dll, die die Klasse registriert hat.                                                                                                                                                                                 |
| [Klassen Cursor](#class-cursor)                         | Definiert den Maus Cursor, den das System für ein Fenster der Klasse anzeigt.                                                                                                                                                                  |
| [Klassen Symbole](#class-icons)                           | Definiert das große Symbol und das kleine Symbol.                                                                                                                                                                                                    |
| [Klassenhintergrund Pinsel](#class-background-brush)     | Definiert die Farbe und das Muster, die den Client Bereich ausfüllen, wenn das Fenster geöffnet oder gezeichnet wird.                                                                                                                                                 |
| [Klassen Menü](#class-menu)                             | Gibt das Standardmenü für Windows an, in dem ein Menü nicht explizit definiert wird.                                                                                                                                                                  |
| [Klassenstile](#class-styles)                         | Definiert, wie das Fenster nach dem Verschieben oder Ändern der Größe aktualisiert wird, wie Doppelklicks der Maus verarbeitet werden, wie der Speicherplatz für den Gerätekontext und andere Aspekte des Fensters belegt werden.                                                       |
| [Zusätzlicher Klassen Arbeitsspeicher](#extra-class-memory)             | Gibt die Menge des zusätzlichen Arbeitsspeichers in Bytes an, den das System für die Klasse reservieren soll. Alle Fenster in der Klasse teilen den zusätzlichen Arbeitsspeicher und können ihn für beliebige Anwendungs definierte Zwecke verwenden. Das System initialisiert diesen Arbeitsspeicher mit 0 (null). |
| [Zusätzlicher Fenster Speicher](#extra-window-memory)           | Gibt die Menge an zusätzlichem Arbeitsspeicher in Bytes an, die das System für jedes Fenster reservieren sollte, das zur-Klasse gehört. Der zusätzliche Arbeitsspeicher kann für beliebige Anwendungs definierte Zwecke verwendet werden. Das System initialisiert diesen Arbeitsspeicher mit 0 (null).          |



 

### <a name="class-name"></a>Klassenname

Jede Fenster Klasse benötigt einen [Klassennamen](#class-name) , um eine Klasse von einer anderen Klasse zu unterscheiden. Weisen Sie einen Klassennamen zu, indem Sie den **lpszClassName** -Member der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur auf die Adresse einer auf NULL endenden Zeichenfolge festlegen, die den Namen angibt. Da Fenster Klassen Prozess spezifisch sind, müssen Fenster Klassennamen nur innerhalb desselben Prozesses eindeutig sein. Da Klassennamen Platz in der privaten Atom-Tabelle des Systems belegen, sollten Sie Klassennamen Zeichenfolgen so kurz wie möglich halten.

Die [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname) -Funktion Ruft den Namen der Klasse ab, zu der ein bestimmtes Fenster gehört.

### <a name="window-procedure-address"></a>Fenster Prozedur Adresse

Jede Klasse benötigt eine Fenster Prozedur Adresse, um den Einstiegspunkt der Fenster Prozedur zu definieren, die für die Verarbeitung aller Nachrichten für Windows in der Klasse verwendet wird. Das System übergibt Nachrichten an die Prozedur, wenn es erforderlich ist, dass das Fenster Aufgaben durchführt, z. b. das Zeichnen des Client Bereichs oder das reagieren auf Benutzereingaben. Ein Prozess weist einer Klasse eine Fenster Prozedur zu, indem er die Adresse in das **lpfnwndproc** -Element der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur kopiert. Weitere Informationen finden Sie unter [Window Procedures](window-procedures.md).

### <a name="instance-handle"></a>Instanzhandle

Jede Fenster Klasse erfordert ein Instanzhandle, um die Anwendung oder dll zu identifizieren, die die Klasse registriert hat. Das System erfordert Instanzhandles, um alle Module nachzuverfolgen. Das System weist jeder Kopie einer ausführbaren ausführbaren Datei oder dll ein Handle zu.

Das System übergibt ein Instanzhandle an die Einstiegspunkt Funktion der einzelnen ausführbaren Dateien (siehe [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)) und. dll (siehe [**DllMain**](/windows/desktop/Dlls/dllmain)). Die ausführbare Datei oder dll weist dieses Instanzhandle der-Klasse zu, indem es in das **HINSTANCE** -Element der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur kopiert wird.

### <a name="class-cursor"></a>Klassen Cursor

Der *Klassen Cursor* definiert die Form des Cursors, wenn er sich im Client Bereich eines Fensters in der-Klasse befindet. Das System legt den Cursor automatisch auf die angegebene Form fest, wenn der Cursor in den Client Bereich des Fensters wechselt, und stellt sicher, dass er diese Form beibehält, während er im Client Bereich verbleibt. Um einer Fenster Klasse eine Cursor Form zuzuweisen, laden Sie eine vordefinierte Cursor Form mithilfe der [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) -Funktion, und weisen Sie dann das zurückgegebene Cursor Handle dem **hcursor** -Member der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur zu. Alternativ dazu können Sie auch eine benutzerdefinierte Cursor Ressource bereitstellen und die **LoadCursor** -Funktion verwenden, um Sie aus den Ressourcen der Anwendung zu laden.

Das System erfordert keinen Klassen Cursor. Wenn eine Anwendung den **hcursor** -Member der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur auf **null** festlegt, wird kein Klassen Cursor definiert. Das System geht davon aus, dass das Fenster die Cursor Form jedes Mal festlegt, wenn der Cursor in das Fenster bewegt wird. Ein Fenster kann die Cursor Form durch Aufrufen der [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) -Funktion festlegen, wenn das Fenster die [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachricht empfängt. Weitere Informationen zu Cursorn finden Sie unter [Cursors](/windows/desktop/menurc/cursors).

### <a name="class-icons"></a>Klassen Symbole

Ein *Klassen Symbol* ist ein Bild, das vom System verwendet wird, um ein Fenster einer bestimmten Klasse darzustellen. Eine Anwendung kann zwei Klassen Symbole haben – eine große und eine kleine. Das System zeigt das *große Klassen Symbol* eines Fensters im Aufgaben Schalterfenster an, das angezeigt wird, wenn der Benutzer Alt + Tab drückt, und in den Ansichten mit dem großen Symbol der Taskleiste und im Explorer. Das *Symbol für die kleine Klasse* wird in der Titelleiste eines Fensters und in den Ansichten des kleinen Symbols der Taskleiste und des Explorers angezeigt.

Wenn Sie einer Fenster Klasse ein großes und kleines Symbol zuweisen möchten, geben Sie die Handles der Symbole in den **HICON** -und **hikonsm** -Membern der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur an. Die Symbol Dimensionen müssen den erforderlichen Dimensionen für große und kleine Klassen Symbole entsprechen. Für ein großes Klassen Symbol können Sie die erforderlichen Dimensionen ermitteln, indem Sie die **SM- \_ cxicon** -und **SM \_ cyicon** -Werte in einem Aufrufen der [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion angeben. Geben Sie für ein kleines Klassen Symbol die **SM \_ cxsmicon** -und **SM \_ cysmicon** -Werte an. Weitere Informationen finden Sie unter [Symbole](/windows/desktop/menurc/icons).

Wenn eine Anwendung die **HICON** -und **hikonsm** -Member der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur auf **null** festlegt, verwendet das System das Standard Anwendungssymbol als große und kleine Klassen Symbole für die Fenster Klasse. Wenn Sie ein Symbol für eine große Klasse angeben, aber keinen kleinen, erstellt das System ein kleines Klassen Symbol basierend auf dem großen. Wenn Sie jedoch ein kleines Klassen Symbol, aber keinen großen Wert angeben, verwendet das System das Standard Anwendungssymbol als großes Klassen Symbol und das angegebene Symbol als kleines Klassen Symbol.

Sie können das Symbol für groß-oder Kleinschreibung für ein bestimmtes Fenster überschreiben, indem Sie die [**WM \_**](wm-seticon.md) -Nachricht "*" verwenden. Sie können das aktuelle Symbol für große oder kleine Klassen mithilfe der [**WM- \_ GetIcon**](wm-geticon.md) -Nachricht abrufen.

### <a name="class-background-brush"></a>Klassenhintergrund Pinsel

Ein *klassenhintergrund Pinsel* bereitet den Client Bereich eines Fensters für nachfolgende Zeichnungen durch die Anwendung vor. Das System verwendet den Pinsel, um den Client Bereich mit einer voll Tonfarbe oder einem Muster auszufüllen. Dadurch werden alle vorherigen Bilder aus diesem Speicherort entfernt, unabhängig davon, ob Sie zum Fenster gehören oder nicht. Das System benachrichtigt ein Fenster, dass der Hintergrund durch das Senden der WM- [**\_ erasebkgnd**](wm-erasebkgnd.md) -Meldung an das Fenster gezeichnet werden soll. Weitere Informationen finden Sie unter [Pinsel](/windows/desktop/gdi/brushes).

Wenn Sie einer Klasse einen Hintergrund Pinsel zuweisen möchten, erstellen Sie einen Pinsel mithilfe der entsprechenden GDI-Funktionen, und weisen Sie das zurückgegebene Pinsel handle dem **hbrbackground** -Member der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur zu.

Anstatt einen Pinsel zu erstellen, kann eine Anwendung den **hbrbackground** -Member auf einen der standardmäßigen System Farbwerte festlegen. Eine Liste der standardmäßigen System Farbwerte finden Sie unter [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors).

Um eine Standardsystem Farbe zu verwenden, muss die Anwendung den Wert für die Hintergrundfarbe um 1 erhöhen. Beispielsweise ist **Color \_ Background** + 1 die System Hintergrundfarbe. Alternativ können Sie die [**getsyscolorbrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) -Funktion verwenden, um ein Handle für einen Pinsel abzurufen, der einer Standardsystem Farbe entspricht, und dann das Handle im **hbrbackground** -Member der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur angeben.

Das System erfordert nicht, dass eine Fenster Klasse über einen klassenhintergrund Pinsel verfügt. Wenn dieser Parameter auf **null** festgelegt ist, muss das Fenster beim Empfang der [**WM \_ erasebkgnd**](wm-erasebkgnd.md) -Meldung seinen eigenen Hintergrund zeichnen.

### <a name="class-menu"></a>Klassen Menü

Ein *Klassen Menü* definiert das Standardmenü, das von den Fenstern in der-Klasse verwendet werden soll, wenn beim Erstellen der Fenster kein explizites Menü angegeben wird. Ein Menü ist eine Liste der Befehle, aus denen ein Benutzeraktionen auswählen kann, die von der Anwendung durchgeführt werden sollen.

Sie können einer Klasse ein Menü zuweisen, indem Sie den **lpszmenuname** -Member der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur auf die Adresse einer auf NULL endenden Zeichenfolge festlegen, die den Ressourcennamen des Menüs angibt. Es wird davon ausgegangen, dass das Menü eine Ressource in der angegebenen Anwendung ist. Das System lädt das Menü automatisch, wenn es benötigt wird. Wenn die Menü Ressource durch eine ganze Zahl und nicht durch einen Namen identifiziert wird, kann die Anwendung das **lpszmenuname** -Element auf diese Ganzzahl festlegen, indem das [**makeintresource**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) -Makro vor dem Zuweisen des Werts angewendet wird.

Das System erfordert kein Klassen Menü. Wenn eine Anwendung das **lpszmenuname** -Element der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur auf **null** festlegt, haben Fenster in der-Klasse keine Menüleisten. Auch wenn kein Klassen Menü angegeben ist, kann eine Anwendung immer noch eine Menüleiste für ein Fenster definieren, wenn das Fenster erstellt wird.

Wenn ein Menü für eine Klasse angegeben wird und ein untergeordnetes Fenster dieser Klasse erstellt wird, wird das Menü ignoriert. Weitere Informationen finden Sie unter [Menüs](/windows/desktop/menurc/menus).

### <a name="class-styles"></a>Klassenstile

Die Klassen Stile definieren zusätzliche Elemente der Fenster Klasse. Zwei oder mehr Stile können mithilfe des bitweisen or ()-Operators kombiniert werden \| . Um einer Fenster Klasse einen Stil zuzuweisen, weisen Sie das Format dem **stilmember** der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur zu. Eine Liste der Klassen Stile finden Sie unter [**Fenster Klassen Stile**](window-class-styles.md).

### <a name="classes-and-device-contexts"></a>Klassen und Geräte Kontexte

Ein *Gerätekontext* ist ein spezieller Satz von Werten, die Anwendungen zum Zeichnen im Client Bereich ihrer Fenster verwenden. Das System benötigt für jedes Fenster in der Anzeige einen Gerätekontext, bietet jedoch einige Flexibilität bei der Speicherung und Überstellung dieses Geräte Kontexts durch das System.

Wenn kein Gerätekontext Stil explizit angegeben wird, geht das System davon aus, dass jedes Fenster einen Gerätekontext verwendet, der aus einem Pool von Kontexten abgerufen wurde, die vom System verwaltet werden. In solchen Fällen muss jedes Fenster den Gerätekontext abrufen und initialisieren, bevor er gezeichnet wird, und ihn nach dem Zeichnen freigeben.

Um zu vermeiden, dass jedes Mal, wenn es innerhalb eines Fensters gezeichnet werden muss, ein Gerätekontext abgerufen wird, kann eine Anwendung den **CS- \_ owndc** -Stil für die Fenster Klasse angeben. Dieser Klassen Stil weist das System an, einen privaten Gerätekontext zu erstellen, d. –., um einen eindeutigen Gerätekontext für jedes Fenster in der Klasse zuzuordnen. Die Anwendung muss den Kontext nur einmal abrufen und dann für alle nachfolgenden Zeichnungen verwenden.

### <a name="extra-class-memory"></a>Zusätzlicher Klassen Arbeitsspeicher

Das System verwaltet eine [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur intern für jede Fenster Klasse im System. Wenn eine Anwendung eine Fenster Klasse registriert, kann Sie das System anweisen, eine Anzahl zusätzlicher Arbeitsspeicher Bytes an das Ende der **WNDCLASSEX** -Struktur zuzuordnen und anzufügen. Dieser Arbeitsspeicher wird als *zusätzlicher Klassen Speicher* bezeichnet und wird von allen Fenstern gemeinsam genutzt, die zur-Klasse gehören. Verwenden Sie den zusätzlichen Klassen Speicher, um Informationen zur-Klasse zu speichern.

Da zusätzlicher Arbeitsspeicher aus dem lokalen Heap des Systems belegt wird, sollte eine Anwendung den zusätzlichen Klassen Speicher sparsam verwenden. Die [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) -Funktion schlägt fehl, wenn die Menge des angeforderten zusätzlichen Klassen Speichers größer als 40 Byte ist. Wenn eine Anwendung mehr als 40 Bytes erfordert, sollte Sie Ihren eigenen Arbeitsspeicher zuordnen und einen Zeiger auf den Arbeitsspeicher im zusätzlichen Klassen Speicher speichern.

Die Funktionen [**setclassword**](/windows/win32/api/winuser/nf-winuser-setclassword) und [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) kopieren einen Wert in den zusätzlichen Klassen Speicher. Um einen Wert aus dem zusätzlichen Klassen Speicher abzurufen, verwenden Sie die Funktionen [**getclassword**](/windows/win32/api/winuser/nf-winuser-getclassword) und [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga) . Der **CbClsExtra** -Member der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur gibt den Umfang des zu belegenden zusätzlichen Klassen Speichers an. Eine Anwendung, die keinen zusätzlichen Klassen Speicher verwendet, muss das **CbClsExtra** -Element auf 0 (null) initialisieren.

### <a name="extra-window-memory"></a>Zusätzlicher Fenster Speicher

Das System verwaltet für jedes Fenster eine interne Datenstruktur. Beim Registrieren einer Fenster Klasse kann eine Anwendung eine Anzahl zusätzlicher Arbeitsspeicher Bytes als *zusätzlichen Fenster Speicher* angeben. Beim Erstellen eines Fensters der-Klasse ordnet das System dem Ende der Fenster Struktur die angegebene Menge an zusätzlichem Fenster Arbeitsspeicher zu und fügt Sie an. Eine Anwendung kann diesen Arbeitsspeicher zum Speichern Fenster spezifischer Daten verwenden.

Da zusätzlicher Arbeitsspeicher vom lokalen Heap des Systems belegt wird, sollte eine Anwendung den zusätzlichen Fenster Speicher sparsam verwenden. Die [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) -Funktion schlägt fehl, wenn der angeforderte zusätzliche Fenster Speicher größer als 40 Bytes ist. Wenn eine Anwendung mehr als 40 Bytes erfordert, sollte Sie Ihren eigenen Arbeitsspeicher zuordnen und einen Zeiger auf den Arbeitsspeicher im zusätzlichen Fenster Speicher speichern.

Die [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) -Funktion kopiert einen Wert in den zusätzlichen Arbeitsspeicher. Die [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) -Funktion Ruft einen Wert aus dem zusätzlichen Arbeitsspeicher ab. Der **CbWndExtra** -Member der [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) -Struktur gibt den Umfang des zusätzlichen Fenster Speichers an, der belegt werden soll. Eine Anwendung, die den Arbeitsspeicher nicht verwendet, muss **CbWndExtra** auf Null initialisieren.

 

 
