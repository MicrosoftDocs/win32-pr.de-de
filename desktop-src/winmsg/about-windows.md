---
description: In diesem Thema werden die Programmierelemente beschrieben, die Anwendungen zum Erstellen und Verwenden von Fenstern verwenden. Verwalten von Beziehungen zwischen Fenstern; und Größe, Verschiebung und Anzeige von Fenstern.
ms.assetid: e325f8dc-004f-44a9-9122-3be5e44764d6
title: Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b085ed246ef6f13627d678e3ede68fa6349a780a74c0c89ee7cbafb24c501f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849888"
---
# <a name="about-windows"></a>Info

In diesem Thema werden die Programmierelemente beschrieben, die Anwendungen zum Erstellen und Verwenden von Fenstern verwenden. Verwalten von Beziehungen zwischen Fenstern; und Größe, Verschiebung und Anzeige von Fenstern.

Die Übersicht enthält die folgenden Themen.

-   [Desktopfenster](#desktop-window)
-   [Anwendungs-Windows](#application-windows)
    -   [Clientbereich](#client-area)
    -   [Nichtclientbereich](#nonclient-area)
-   [Steuerelemente und Dialogfelder](#controls-and-dialog-boxes)
-   [Fensterattribute](#window-attributes)
    -   [Klassenname](#class-name)
    -   [Fenstername](#window-name)
    -   [Fensterstil](#window-style)
    -   [Erweiterter Fensterstil](#extended-window-style)
    -   [Position](#position)
    -   [Größe](#size)
    -   [Übergeordnetes oder Besitzerfensterhandle](#parent-or-owner-window-handle)
    -   [Menühandle oder Child-Window-Bezeichner](#menu-handle-or-child-window-identifier)
    -   [Anwendungsinstanzhandle](#application-instance-handle)
    -   [Erstellungsdaten](#creation-data)
    -   [Fensterhandle](#window-handle)
-   [Fenstererstellung](#creation-data)
    -   [Erstellung des Hauptfensters](#main-window-creation)
    -   [Meldungen zur Fenstererstellung](#window-creation-messages)
    -   [Multithreadanwendungen](#multithread-applications)

## <a name="desktop-window"></a>Desktopfenster

Wenn Sie das System starten, wird automatisch das Desktopfenster erstellt. Das *Desktopfenster* ist ein systemdefiniertes Fenster, das den Hintergrund des Bildschirms zeichnet und als Basis für alle Fenster dient, die von allen Anwendungen angezeigt werden.

Das Desktopfenster verwendet eine Bitmap, um den Hintergrund des Bildschirms zu zeichnen. Das von der Bitmap erstellte Muster wird als *Desktophintergrund* bezeichnet. Standardmäßig verwendet das Desktopfenster die Bitmap aus einer .bmp Datei, die in der Registrierung als Desktophintergrund angegeben ist.

Die [**GetDesktopWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-getdesktopwindow) gibt ein Handle an das Desktopfenster zurück.

Eine Systemkonfigurationsanwendung, z. B. ein Systemsteuerung Element, ändert das Desktophintergrund mithilfe der [**SystemParametersInfo-Funktion,**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) wobei der *wAction-Parameter* auf **SPI \_ SETDESKWALLPAPER** und der *lpvParam-Parameter* festgelegt ist, der einen Bitmapdateinamen angibt. **SystemParametersInfo** lädt dann die Bitmap aus der angegebenen Datei, verwendet die Bitmap, um den Hintergrund des Bildschirms zu zeichnen, und gibt den neuen Dateinamen in die Registrierung ein.

## <a name="application-windows"></a>Anwendungs-Windows

Jede grafische Windows-basierte Anwendung erstellt mindestens ein Fenster, das als *Hauptfenster* bezeichnet wird und als primäre Schnittstelle zwischen dem Benutzer und der Anwendung dient. Die meisten Anwendungen erstellen auch direkt oder indirekt andere Fenster, um Aufgaben im Zusammenhang mit dem Hauptfenster auszuführen. Jedes Fenster spielt eine Rolle beim Anzeigen der Ausgabe und beim Empfangen von Eingaben vom Benutzer.

Wenn Sie eine Anwendung starten, ordnet das System der Anwendung auch eine Taskleistenschaltfläche zu. Die *Taskleistenschaltfläche* enthält das Programmsymbol und den Titel. Wenn die Anwendung aktiv ist, wird ihre Taskleistenschaltfläche im Gedrückt-Zustand angezeigt.

Ein Anwendungsfenster enthält Elemente wie eine Titelleiste, eine Menüleiste, das Fenstermenü (früher als Systemmenü bezeichnet), die Schaltfläche "Minimieren", die Schaltfläche "Maximieren", die Schaltfläche "Wiederherstellen", die Schaltfläche "Schließen", einen Größenrahmen, einen Clientbereich, eine horizontale Scrollleiste und eine vertikale Bildlaufleiste. Das Hauptfenster einer Anwendung umfasst in der Regel alle diese Komponenten. Die folgende Abbildung zeigt diese Komponenten in einem typischen Hauptfenster.

![Typisches Fenster](images/cswin-02.png)

### <a name="client-area"></a>Clientbereich

Der *Clientbereich* ist der Teil eines Fensters, in dem die Anwendung Ausgaben wie Text oder Grafiken anzeigt. Beispielsweise zeigt eine Desktopveröffentlichungsanwendung die aktuelle Seite eines Dokuments im Clientbereich an. Die Anwendung muss eine Funktion bereitstellen, die als Fensterprozedur bezeichnet wird, um die Eingabe für das Fenster zu verarbeiten und die Ausgabe im Clientbereich anzuzeigen. Weitere Informationen finden Sie unter [Window Procedures](window-procedures.md).

### <a name="nonclient-area"></a>Nichtclientbereich

Titelleiste, Menüleiste, Fenstermenü, Schaltflächen zum Minimieren und Maximieren, Dimensionierungsrahmen und Scrollleisten werden zusammen als *Nichtclientbereich* des Fensters bezeichnet. Das System verwaltet die meisten Aspekte des Nichtclientbereichs. Die Anwendung verwaltet die Darstellung und das Verhalten ihres Clientbereichs.

In der *Titelleiste* werden ein anwendungsdefiniertes Symbol und eine Textzeile angezeigt. in der Regel gibt der Text den Namen der Anwendung oder den Zweck des Fensters an. Eine Anwendung gibt das Symbol und den Text beim Erstellen des Fensters an. Die Titelleiste ermöglicht dem Benutzer auch das Verschieben des Fensters mithilfe einer Maus oder eines anderen zeigenden Geräts.

Die meisten Anwendungen enthalten eine *Menüleiste,* die die von der Anwendung unterstützten Befehle auflistet. Elemente in der Menüleiste stellen die Hauptkategorien von Befehlen dar. Durch Klicken auf ein Element in der Menüleiste wird in der Regel ein Popupmenü geöffnet, dessen Elemente den Aufgaben innerhalb einer bestimmten Kategorie entsprechen. Durch Klicken auf einen Befehl weist der Benutzer die Anwendung an, eine Aufgabe auszuführen.

Das *Fenstermenü* wird vom System erstellt und verwaltet. Sie enthält einen Standardsatz von Menüelementen, die bei Auswahl durch den Benutzer die Größe oder Position eines Fensters festlegen, die Anwendung schließen oder Aufgaben ausführen. Weitere Informationen finden Sie unter [Menüs](/windows/desktop/menurc/menus).

Die Schaltflächen in der oberen rechten Ecke beeinflussen die Größe und Position des Fensters. Wenn Sie auf die *Schaltfläche "Maximieren"* klicken, vergrößert das System das Fenster auf die Größe des Bildschirms und positioniert das Fenster, sodass es den gesamten Desktop abzüglich der Taskleiste abdeckt. Gleichzeitig ersetzt das System die Schaltfläche "Maximieren" durch die Schaltfläche "Wiederherstellen". Wenn Sie auf die *Schaltfläche "Wiederherstellen"* klicken, stellt das System das Fenster auf die vorherige Größe und Position wieder her. Wenn Sie auf die *Schaltfläche minimieren* klicken, reduziert das System das Fenster auf die Größe der Taskleistenschaltfläche, positioniert das Fenster über der Taskleistenschaltfläche und zeigt die Taskleistenschaltfläche im normalen Zustand an. Klicken Sie auf die Zugehörige Taskleistenschaltfläche, um die vorherige Größe und Position der Anwendung wiederherzustellen. Wenn Sie auf die *Schaltfläche "Schließen"* klicken, wird die Anwendung beendet.

Der *Größenrahmen* ist ein Bereich um den Umkreis des Fensters, der es dem Benutzer ermöglicht, das Fenster mithilfe einer Maus oder eines anderen zeigenden Geräts zu dimensionieren.

Die *horizontale Scrollleiste* und *die vertikale Bildlaufleiste* konvertieren Maus- oder Tastatureingaben in Werte, mit denen eine Anwendung den Inhalt des Clientbereichs horizontal oder vertikal verschiebt. Beispielsweise stellt eine Anwendung zur Textverarbeitung, die ein langes Dokument anzeigt, in der Regel eine vertikale Bildlaufleiste bereit, damit der Benutzer das Dokument auf- und abblättern kann.

## <a name="controls-and-dialog-boxes"></a>Steuerelemente und Dialogfelder

Eine Anwendung kann zusätzlich zum Hauptfenster mehrere Arten von Fenstern erstellen, einschließlich Steuerelementen und Dialogfeldern.

Ein *Steuerelement* ist ein Fenster, das eine Anwendung verwendet, um bestimmte Informationen vom Benutzer abzurufen, z. B. den Namen einer zu öffnende Datei oder die gewünschte Punktgröße einer Textauswahl. Anwendungen verwenden auch Steuerelemente, um Informationen abzurufen, die zum Steuern eines bestimmten Features einer Anwendung erforderlich sind. Beispielsweise stellt eine Anwendung zur Textverarbeitung in der Regel ein Steuerelement bereit, mit dem der Benutzer das Umschließen von Wörtern aktivieren und deaktivieren kann. Weitere Informationen finden Sie unter [Windows Controls](/windows/desktop/Controls/window-controls).

Steuerelemente werden immer in Verbindung mit einem anderen Fenster verwendet , in der Regel einem Dialogfeld. Ein *Dialogfeld* ist ein Fenster, das ein oder mehrere Steuerelemente enthält. Eine Anwendung fordert den Benutzer mithilfe eines Dialogfelds zur Eingabe auf, die zum Ausführen eines Befehls erforderlich ist. Beispielsweise würde eine Anwendung, die einen Befehl zum Öffnen einer Datei enthält, ein Dialogfeld anzeigen, das Steuerelemente enthält, in denen der Benutzer einen Pfad und dateinamen angibt. Dialogfelder verwenden in der Regel nicht den gleichen Satz von Fensterkomponenten wie ein Hauptfenster. Die meisten verfügen über eine Titelleiste, ein Fenstermenü, einen Rahmen (nicht dimensioniert) und einen Clientbereich, aber sie verfügen in der Regel nicht über eine Menüleiste, minimieren und maximieren Schaltflächen oder Scrollleisten. Weitere Informationen finden Sie unter [Dialogfelder](/windows/desktop/dlgbox/dialog-boxes).

Ein *Meldungsfeld* ist ein spezielles Dialogfeld, in dem dem Benutzer eine Notiz, Vorsicht oder Warnung angezeigt wird. Beispielsweise kann ein Meldungsfeld den Benutzer über ein Problem informieren, das bei der Ausführung einer Aufgabe in der Anwendung aufgetreten ist. Weitere Informationen finden Sie unter [Meldungsfelder.](/windows/desktop/dlgbox/about-dialog-boxes)

## <a name="window-attributes"></a>Fensterattribute

Eine Anwendung muss beim Erstellen eines Fensters die folgenden Informationen bereitstellen. (Mit Ausnahme des [Fensterhandle](#window-handle), das die Erstellungsfunktion zurückgibt, um das neue Fenster eindeutig zu identifizieren.)

-   [Klassenname](#class-name)
-   [Fenstername](#window-name)
-   [Fensterstil](#window-style)
-   [Erweiterter Fensterstil](#extended-window-style)
-   [Position](#position)
-   [Größe](#size)
-   [Übergeordnetes oder Besitzerfensterhandle](#parent-or-owner-window-handle)
-   [Menühandle oder Child-Window-Bezeichner](#menu-handle-or-child-window-identifier)
-   [Anwendungsinstanzhandle](#application-instance-handle)
-   [Erstellungsdaten](#creation-data)
-   [Fensterhandle](#window-handle)

Diese Fensterattribute werden in den folgenden Abschnitten beschrieben.

### <a name="class-name"></a>Klassenname

Jedes Fenster gehört zu einer Fensterklasse. Eine Anwendung muss vor dem Erstellen von Fenstern dieser Klasse eine Fensterklasse registrieren. Die *Fensterklasse* definiert die meisten Aspekte der Darstellung und des Verhaltens eines Fensters. Die Hauptkomponente einer Fensterklasse ist die *Fensterprozedur*, eine Funktion, die alle Eingaben und Anforderungen empfängt und verarbeitet, die an das Fenster gesendet werden. Das System stellt die Eingaben und Anforderungen in Form von *Nachrichten* bereit. Weitere Informationen finden Sie unter [Window Classes](window-classes.md), [Window Procedures](window-procedures.md)und Messages and [Message Queues](messages-and-message-queues.md).

### <a name="window-name"></a>Fenstername

Ein *Fenstername* ist eine Textzeichenfolge, die ein Fenster für den Benutzer identifiziert. Ein Hauptfenster, Dialogfeld oder Meldungsfeld zeigt in der Regel seinen Fensternamen in der Titelleiste an(sofern vorhanden). Ein Steuerelement zeigt abhängig von der Klasse des Steuerelements möglicherweise seinen Fensternamen an. Schaltflächen, Bearbeitungssteuerelemente und statische Steuerelemente zeigen beispielsweise ihre Fensternamen innerhalb des Rechtecks an, das vom Steuerelement belegt wird. Steuerelemente wie Listenfelder und Kombinationsfelder zeigen ihre Fensternamen jedoch nicht an.

Um den Fensternamen nach dem Erstellen eines Fensters zu ändern, verwenden Sie die [**SetWindowText-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) . Diese Funktion verwendet die Funktionen [**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha) und [**GetWindowText,**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) um die zeichenfolge des aktuellen Fensternamens aus dem Fenster abzurufen.

### <a name="window-style"></a>Fensterstil

Jedes Fenster verfügt über einen oder mehrere Fensterstile. Ein Fensterstil ist eine benannte Konstante, die einen Aspekt der Darstellung und des Verhaltens des Fensters definiert, der nicht von der -Klasse des Fensters angegeben wird. Eine Anwendung legt beim Erstellen von Fenstern in der Regel Fensterstile fest. Sie kann die Stile auch nach dem Erstellen eines Fensters mithilfe der [**SetWindowLong-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) festlegen.

Das System und, bis zu einem gewissen Grad, die Fensterprozedur für die -Klasse interpretieren die Fensterstile.

Einige Fensterstile gelten für alle Fenster, die meisten für Fenster bestimmter Fensterklassen. Die allgemeinen Fensterstile werden durch Konstanten dargestellt, die mit dem \_ WS-Präfix beginnen. Sie können mit dem OR-Operator kombiniert werden, um verschiedene Arten von Fenstern zu bilden, einschließlich Hauptfenstern, Dialogfeldern und untergeordneten Fenstern. Die klassenspezifischen Fensterstile definieren die Darstellung und das Verhalten von Fenstern, die zu den vordefinierten Steuerelementklassen gehören. Beispielsweise gibt die **SCROLLBAR-Klasse** ein Bildlaufleisten-Steuerelement an, aber die [**SBS \_ HORZ-**](../controls/scroll-bar-control-styles.md) und **SBS \_ VERT-Stile** bestimmen, ob ein horizontales oder vertikales Scrollleisten-Steuerelement erstellt wird.

Listen der Stile, die von Fenstern verwendet werden können, finden Sie in den folgenden Themen:

-   [**Fensterstile**](window-styles.md)
-   [Schaltflächenstile](../controls/button-styles.md)
-   [Kombinationsfeldstile](../controls/combo-box-styles.md)
-   [Bearbeiten von Steuerelementstilen](../controls/edit-control-styles.md)
-   [Listenfeldstile](../controls/list-box-styles.md)
-   [Rich Edit-Steuerelementstile](../controls/rich-edit-control-styles.md)
-   [Bildlaufleisten-Steuerelementstile](../controls/scroll-bar-control-styles.md)
-   [Statische Steuerelementstile](../controls/static-control-styles.md)

### <a name="extended-window-style"></a>Erweiterter Fensterstil

Jedes Fenster kann optional einen oder mehrere erweiterte Fensterstile aufweisen. Ein *erweiterter Fensterstil* ist eine benannte Konstante, die einen Aspekt der Darstellung und des Verhaltens des Fensters definiert, der nicht von der Fensterklasse oder den anderen Fensterstilen angegeben wird. Eine Anwendung legt beim Erstellen von Fenstern in der Regel erweiterte Fensterstile fest. Sie kann die Stile auch nach dem Erstellen eines Fensters mithilfe der [**SetWindowLong-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) festlegen.

Weitere Informationen finden Sie unter [**CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa)

### <a name="position"></a>Position

Die Position eines Fensters wird als die Koordinaten der oberen linken Ecke definiert. Diese Koordinaten, die manchmal als Fensterkoordinaten bezeichnet werden, sind immer relativ zur oberen linken Ecke des Bildschirms oder für ein untergeordnetes Fenster die obere linke Ecke des Clientbereichs des übergeordneten Fensters. Beispielsweise wird ein Fenster der obersten Ebene mit den Koordinaten (10,10) 10 Pixel rechts von der oberen linken Ecke des Bildschirms und 10 Pixel unten davon platziert. Ein untergeordnetes Fenster mit den Koordinaten (10,10) wird 10 Pixel rechts von der oberen linken Ecke des Clientbereichs des übergeordneten Fensters platziert und 10 Pixel nach unten entfernt.

Die [**WindowFromPoint-Funktion**](/windows/win32/api/winuser/nf-winuser-windowfrompoint) ruft ein Handle für das Fenster ab, das einen bestimmten Punkt auf dem Bildschirm einnimmt. Auf ähnliche Weise rufen die Funktionen [**ChildWindowFromPoint**](/windows/win32/api/winuser/nf-winuser-childwindowfrompoint) und [**ChildWindowFromPointEx**](/windows/win32/api/winuser/nf-winuser-childwindowfrompointex) ein Handle für das untergeordnete Fenster ab, das einen bestimmten Punkt im Clientbereich des übergeordneten Fensters einnimmt. **ChildWindowFromPointEx** kann zwar unsichtbare, deaktivierte und transparente untergeordnete Fenster ignorieren, **ChildWindowFromPoint** jedoch nicht.

### <a name="size"></a>Size

Die Größe eines Fensters (Breite und Höhe) wird in Pixel angegeben. Ein Fenster kann eine Breite oder Höhe von null aufweisen. Wenn eine Anwendung die Breite und Höhe eines Fensters auf 0 (null) festlegt, legt das System die Größe auf die minimale Standardfenstergröße fest. Um die minimale Standardfenstergröße zu ermitteln, verwendet eine Anwendung die [**GetSystemMetrics-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) mit den SM **\_ CXMIN-** und **SM \_ CYMIN-Flags.**

Eine Anwendung muss möglicherweise ein Fenster mit einem Clientbereich einer bestimmten Größe erstellen. Die Funktionen [**AdjustWindowRect**](/windows/win32/api/winuser/nf-winuser-adjustwindowrect) und [**AdjustWindowRectEx**](/windows/win32/api/winuser/nf-winuser-adjustwindowrectex) berechnen die erforderliche Größe eines Fensters basierend auf der gewünschten Größe des Clientbereichs. Die Anwendung kann die resultierenden Größenwerte an die [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) übergeben.

Eine Anwendung kann ein Fenster so dimensionen, dass es extrem groß ist. Ein Fenster sollte jedoch nicht so groß sein, dass es größer als der Bildschirm ist. Vor dem Festlegen der Fenstergröße sollte die Anwendung die Breite und Höhe des Bildschirms überprüfen, indem [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) mit den **SM \_ CXSCREEN-** und **SM \_ CYSCREEN-Flags** verwendet wird.

### <a name="parent-or-owner-window-handle"></a>Übergeordnetes oder Besitzerfensterhandle

Ein Fenster kann ein übergeordnetes Fenster aufweisen. Ein Fenster, das über ein übergeordnetes Fenster verfügt, wird als *untergeordnetes Fenster* bezeichnet. Das *übergeordnete Fenster* stellt das Koordinatensystem bereit, das zum Positionieren eines untergeordneten Fensters verwendet wird. Das Verwenden eines übergeordneten Fensters wirkt sich auf Aspekte der Darstellung eines Fensters aus. Beispielsweise wird ein untergeordnetes Fenster abgeschnitten, sodass kein Teil des untergeordneten Fensters außerhalb der Rahmen des übergeordneten Fensters angezeigt werden kann.

Ein Fenster ohne übergeordnetes Fenster oder dessen übergeordnetes Fenster das Desktopfenster ist, wird als *Fenster der obersten Ebene* bezeichnet. Eine Anwendung kann die [**EnumWindows-Funktion**](/windows/win32/api/winuser/nf-winuser-enumwindows) verwenden, um ein Handle für jedes Fenster der obersten Ebene auf dem Bildschirm abzurufen. **EnumWindows** übergibt das Handle an jedes Fenster der obersten Ebene wiederum an die anwendungsdefinierte Rückruffunktion [**EnumWindowsProc.**](/previous-versions/windows/desktop/legacy/ms633498(v=vs.85))

Ein Fenster der obersten Ebene kann ein anderes Fenster besitzen oder dessen Besitzer sein. Ein *eigenes Fenster* wird immer vor seinem Besitzerfenster angezeigt, wird ausgeblendet, wenn das Besitzerfenster minimiert wird, und wird zerstört, wenn das Besitzerfenster zerstört wird. Weitere Informationen finden Sie unter [Owned Windows](window-features.md#owned-windows).

### <a name="menu-handle-or-child-window-identifier"></a>Menühandle oder Child-Window-Bezeichner

Ein untergeordnetes Fenster kann über einen Bezeichner für untergeordnete *Fenster* verfügen, einen eindeutigen, anwendungsdefinierte Wert, der dem untergeordneten Fenster zugeordnet ist. Bezeichner für untergeordnete Fenster sind besonders nützlich in Anwendungen, die mehrere untergeordnete Fenster erstellen. Beim Erstellen eines untergeordneten Fensters gibt eine Anwendung den Bezeichner des untergeordneten Fensters an. Nach dem Erstellen des Fensters kann die Anwendung den Bezeichner des Fensters mithilfe der [**SetWindowLong-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) ändern oder den Bezeichner mithilfe der [**GetWindowLong-Funktion**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) abrufen.

Jedes Fenster, mit Ausnahme eines untergeordneten Fensters, kann über ein Menü verfügen. Eine Anwendung kann ein Menü enthalten, indem sie entweder beim Registrieren der -Klasse des Fensters oder beim Erstellen des Fensters ein Menühandle bereitstellt.

### <a name="application-instance-handle"></a>Anwendungsinstanzhandle

Jeder Anwendung ist ein Instanzhandle zugeordnet. Das System stellt das Instanzhandle für eine Anwendung bereit, wenn die Anwendung gestartet wird. Da mehrere Kopien derselben Anwendung ausgeführt werden können, verwendet das System intern Instanzhandles, um eine Instanz einer Anwendung von einer anderen zu unterscheiden. Die Anwendung muss das Instanzhandle in vielen verschiedenen Fenstern angeben, einschließlich der Fenster, die Fenster erstellen.

### <a name="creation-data"></a>Erstellungsdaten

Jedem Fenster können anwendungsdefinierte Erstellungsdaten zugeordnet sein. Wenn das Fenster zum ersten Mal erstellt wird, übergibt das System einen Zeiger auf die Daten an die Fensterprozedur des zu erstellenden Fensters. Die Fensterprozedur verwendet die Daten, um anwendungsdefinierte Variablen zu initialisieren.

### <a name="window-handle"></a>Fensterhandle

Nach dem Erstellen eines Fensters gibt die Erstellungsfunktion ein *Fensterhandle* zurück, das das Fenster eindeutig identifiziert. Ein Fensterhandle weist den **HWND-Datentyp** auf. Eine Anwendung muss diesen Typ verwenden, wenn sie eine Variable deklariert, die ein Fensterhandle enthält. Eine Anwendung verwendet dieses Handle in anderen Funktionen, um ihre Aktionen an das Fenster weiterzuleiten.

Eine Anwendung kann die [**FindWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-findwindowa) verwenden, um zu ermitteln, ob ein Fenster mit dem angegebenen Klassennamen oder Fensternamen im System vorhanden ist. Wenn ein solches Fenster vorhanden ist, gibt **FindWindow** ein Handle an das Fenster zurück. Verwenden Sie die [**FindWindowEx-Funktion,**](/windows/win32/api/winuser/nf-winuser-findwindowexa) um die Suche auf die untergeordneten Fenster einer bestimmten Anwendung zu beschränken.

Die [**IsWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-iswindow) bestimmt, ob ein Fensterhandle ein gültiges, vorhandenes Fenster identifiziert. Es gibt spezielle Konstanten, die ein Fensterhandle in bestimmten Funktionen ersetzen können. Eine Anwendung kann beispielsweise **HWND \_ BROADCAST** in den Funktionen [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) und [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) oder **HWND \_ DESKTOP** in der [**MapWindowPoints-Funktion**](/windows/desktop/api/winuser/nf-winuser-mapwindowpoints) verwenden.

## <a name="window-creation"></a>Fenstererstellung

Verwenden Sie zum Erstellen von Anwendungsfenstern [**die Funktion CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Sie müssen die informationen angeben, die zum Definieren der Fensterattribute erforderlich sind. **CreateWindowEx verfügt** über den Parameter *dwExStyle,* über den **CreateWindow** nicht verfügt. andernfalls sind die Funktionen identisch. Tatsächlich ruft **CreateWindow einfach** **CreateWindowEx** auf, und *der dwExStyle-Parameter* ist auf 0 (null) festgelegt. Aus diesem Grund bezieht sich der Rest dieser Übersicht nur auf **CreateWindowEx.**

Dieser Abschnitt enthält die folgenden Themen:

-   [Erstellung des Hauptfensters](#main-window-creation)
-   [Meldungen zur Fenstererstellung](#window-creation-messages)
-   [Multithreadanwendungen](#multithread-applications)

> [!Note]  
> Es gibt zusätzliche Funktionen zum Erstellen von Speziellen Fenstern, z. B. Dialogfelder und Meldungsfelder. Weitere Informationen finden Sie unter [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa), [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga)und [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).

 

### <a name="main-window-creation"></a>Erstellung des Hauptfensters

Jede Windows-basierte Anwendung muss [**über WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) als Einstiegspunktfunktion verfügen. **WinMain** führt eine Reihe von Aufgaben aus, einschließlich der Registrierung der Fensterklasse für das Hauptfenster und der Erstellung des Hauptfensters. **WinMain** registriert die Hauptfensterklasse durch Aufrufen der [**RegisterClass-Funktion**](/windows/win32/api/winuser/nf-winuser-registerclassa) und erstellt das Hauptfenster durch Aufrufen der [**CreateWindowEx-Funktion.**](/windows/win32/api/winuser/nf-winuser-createwindowexa)

Ihre [**WinMain-Funktion**](/windows/win32/api/winbase/nf-winbase-winmain) kann Ihre Anwendung auch auf eine einzelne Instanz beschränken. Erstellen Sie mithilfe der [**CreateMutex-Funktion einen benannten Mutex.**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) Wenn [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) **ERROR ALREADY \_ \_ EXISTS** zurückgibt, ist eine andere Instanz Ihrer Anwendung vorhanden (sie hat den Mutex erstellt), und Sie sollten **WinMain beenden.**

Das Hauptfenster wird nach der Erstellung nicht automatisch angezeigt. Stattdessen muss eine Anwendung die [**ShowWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-showwindow) verwenden, um das Hauptfenster anzuzeigen. Nach dem Erstellen des Hauptfensters ruft die [**WinMain-Funktion**](/windows/win32/api/winbase/nf-winbase-winmain) der Anwendung **ShowWindow** auf und über gibt zwei Parameter an: ein Handle an das Hauptfenster und ein Flag, das an gibt, ob das Hauptfenster minimiert oder maximiert werden soll, wenn es zum ersten Mal angezeigt wird. Normalerweise kann das Flag auf jede der Konstanten festgelegt werden, die mit dem SW-Präfix \_ beginnen. Wenn **ShowWindow jedoch** aufgerufen wird, um das Hauptfenster der Anwendung anzuzeigen, muss das Flag auf **SW \_ SHOWDEFAULT festgelegt werden.** Dieses Flag weist das System an, das Fenster wie vom Programm, das die Anwendung gestartet hat, anzuzeigen.

Wenn eine Fensterklasse mit der Unicode-Version von [**RegisterClass registriert**](/windows/win32/api/winuser/nf-winuser-registerclassa)wurde, empfängt das Fenster nur Unicode-Nachrichten. Um zu bestimmen, ob ein Fenster den Unicode-Zeichensatz verwendet, rufen Sie [**IsWindowUnicode auf.**](/windows/win32/api/winuser/nf-winuser-iswindowunicode)

### <a name="window-creation-messages"></a>Window-Creation Nachrichten

Beim Erstellen eines Fensters sendet das System Nachrichten an die Fensterprozedur für das Fenster. Das System sendet die [**WM \_ NCCREATE-Nachricht**](wm-nccreate.md) nach dem Erstellen des Nicht-Clientbereichs des Fensters und der [**WM \_ CREATE-Nachricht**](wm-create.md) nach dem Erstellen des Clientbereichs. Die Fensterprozedur empfängt beide Meldungen, bevor das System das Fenster anzeigt. Beide Meldungen enthalten einen Zeiger auf eine [**CREATESTRUCT-Struktur,**](/windows/win32/api/winuser/ns-winuser-createstructa) die alle in der [**CreateWindowEx-Funktion angegebenen Informationen**](/windows/win32/api/winuser/nf-winuser-createwindowexa) enthält. In der Regel führt die Fensterprozedur Beim Empfang dieser Meldungen Initialisierungsaufgaben aus.

Beim Erstellen eines untergeordneten Fensters sendet das System die [**WM \_ PARENTNOTIFY-Nachricht**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) an das übergeordnete Fenster, nachdem die [**WM \_ NCCREATE-**](wm-nccreate.md) und [**WM \_ CREATE-Nachrichten gesendet**](wm-create.md) wurden. Beim Erstellen eines Fensters werden auch andere Nachrichten gesendet. Die Anzahl und Reihenfolge dieser Meldungen hängt von der Fensterklasse und dem Stil sowie von der Funktion ab, die zum Erstellen des Fensters verwendet wird. Diese Meldungen werden in anderen Themen in dieser Hilfedatei beschrieben.

### <a name="multithread-applications"></a>Multithreadanwendungen

Eine Windows-basierte Anwendung kann mehrere Ausführungsthreads haben, und jeder Thread kann Fenster erstellen. Der Thread, der ein Fenster erstellt, muss den Code für seine Fensterprozedur enthalten.

Eine Anwendung kann die [**EnumThreadWindows-Funktion**](/windows/win32/api/winuser/nf-winuser-enumthreadwindows) verwenden, um die von einem bestimmten Thread erstellten Fenster zu aufzählen. Diese Funktion übergibt das Handle wiederum an jedes Threadfenster an die anwendungsdefinierte Rückruffunktion [**EnumThreadWndProc.**](/previous-versions/windows/desktop/legacy/ms633496(v=vs.85))

Die [**GetWindowThreadProcessId-Funktion**](/windows/win32/api/winuser/nf-winuser-getwindowthreadprocessid) gibt den Bezeichner des Threads zurück, der ein bestimmtes Fenster erstellt hat.

Verwenden Sie die [**ShowWindowAsync-Funktion,**](/windows/win32/api/winuser/nf-winuser-showwindowasync) um den Showzustand eines Fensters, das von einem anderen Thread erstellt wurde, zu ändern.

 

 
