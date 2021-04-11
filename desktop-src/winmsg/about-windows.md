---
description: In diesem Thema werden die Programmier Elemente beschrieben, die von Anwendungen zum Erstellen und Verwenden von Windows verwendet werden. Verwalten von Beziehungen zwischen Windows und Größe, verschieben und Anzeige Fenster.
ms.assetid: e325f8dc-004f-44a9-9122-3be5e44764d6
title: Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2df510deea689d70bd1ebf5e59cafc92b0389d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216082"
---
# <a name="about-windows"></a>Info

In diesem Thema werden die Programmier Elemente beschrieben, die von Anwendungen zum Erstellen und Verwenden von Windows verwendet werden. Verwalten von Beziehungen zwischen Windows und Größe, verschieben und Anzeige Fenster.

Die Übersicht umfasst die folgenden Themen.

-   [Desktop Fenster](#desktop-window)
-   [Anwendungsfenster](#application-windows)
    -   [Client Bereich](#client-area)
    -   [Nicht-Client Bereich](#nonclient-area)
-   [Steuerelemente und Dialog Felder](#controls-and-dialog-boxes)
-   [Fenster Attribute](#window-attributes)
    -   [Klassenname](#class-name)
    -   [Fenstername](#window-name)
    -   [Fensterstil](#window-style)
    -   [Erweiterter Fenster Stil](#extended-window-style)
    -   [Position](#position)
    -   [Größe](#size)
    -   [Übergeordnetes Fenster oder Besitzer Fenster handle](#parent-or-owner-window-handle)
    -   [Menü handle oder Child-Window Bezeichner](#menu-handle-or-child-window-identifier)
    -   [Anwendungsinstanzhandle](#application-instance-handle)
    -   [Erstellungs Daten](#creation-data)
    -   [Fensterhandle](#window-handle)
-   [Fenster Erstellung](#creation-data)
    -   [Hauptfenster Erstellung](#main-window-creation)
    -   [Fenster Erstellungs Meldungen](#window-creation-messages)
    -   [Multithreadanwendungen](#multithread-applications)

## <a name="desktop-window"></a>Desktop Fenster

Wenn Sie das System starten, wird das Desktop Fenster automatisch erstellt. Das *Desktop Fenster* ist ein System definiertes Fenster, das den Hintergrund des Bildschirms zeichnet und als Grundlage für alle Fenster dient, die von allen Anwendungen angezeigt werden.

Im Desktop Fenster wird eine Bitmap verwendet, um den Hintergrund des Bildschirms zu zeichnen. Das von der Bitmap erstellte Muster wird als *Desktop Hintergrund* bezeichnet. Standardmäßig verwendet das Desktop Fenster die Bitmap aus einer BMP-Datei, die in der Registrierung als Desktop Hintergrund angegeben ist.

Die [**GetDesktopWindow**](/windows/win32/api/winuser/nf-winuser-getdesktopwindow) -Funktion gibt ein Handle für das Desktop Fenster zurück.

Eine Systemkonfigurations Anwendung, z. b. ein System Steuerungselement, ändert das Desktop-Hintergrundbild mithilfe der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion, wobei der *waction* -Parameter auf **SPI \_ setdeskwallpaper** und der *lpvparam* -Parameter einen bitmapdateinamen angibt. **SystemParametersInfo** lädt dann die Bitmap aus der angegebenen Datei, verwendet die Bitmap, um den Hintergrund des Bildschirms zu zeichnen, und gibt den neuen Dateinamen in der Registrierung ein.

## <a name="application-windows"></a>Anwendungsfenster

Jede grafische Windows-basierte Anwendung erstellt mindestens ein als *Hauptfenster* bezeichnete Fenster, das als primäre Schnittstelle zwischen dem Benutzer und der Anwendung fungiert. Die meisten Anwendungen erstellen auch andere Fenster direkt oder indirekt, um Aufgaben im Zusammenhang mit dem Hauptfenster auszuführen. Jedes Fenster spielt eine Rolle beim Anzeigen der Ausgabe und beim Empfang von Eingaben vom Benutzer.

Wenn Sie eine Anwendung starten, ordnet das System der Anwendung auch eine Task leisten Schaltfläche zu. Die *Task leisten Schaltfläche* enthält das Programmsymbol und den Titel. Wenn die Anwendung aktiv ist, wird die zugehörige Task leisten Schaltfläche im gedrückten Zustand angezeigt.

Ein Anwendungsfenster umfasst Elemente wie z. b. eine Titelleiste, eine Menüleiste, das Menü Fenster (früher als System-Menü bezeichnet), die Schaltfläche Minimieren, die Schaltfläche "maximieren", die Schaltfläche "Wiederherstellen", die Schaltfläche "Schließen", einen Größen Anpassungsrahmen, einen Client Bereich, eine horizontale Schiebe Leiste und eine vertikale Schiebe Leiste Das Hauptfenster einer Anwendung umfasst in der Regel alle diese Komponenten. Die folgende Abbildung zeigt diese Komponenten in einem typischen Hauptfenster.

![typisches Fenster](images/cswin-02.png)

### <a name="client-area"></a>Client Bereich

Der *Client Bereich* ist der Teil eines Fensters, in dem die Anwendung Ausgaben anzeigt, z. b. Text oder Grafiken. Beispielsweise zeigt eine Desktop Publishing Anwendung die aktuelle Seite eines Dokuments im Client Bereich an. Die Anwendung muss eine Funktion bereitstellen, die als Fenster Prozedur bezeichnet wird, um die Eingabe im Fenster zu verarbeiten und die Ausgabe im Client Bereich anzuzeigen. Weitere Informationen finden Sie unter [Window Procedures](window-procedures.md).

### <a name="nonclient-area"></a>Nicht-Client Bereich

Die Titelleiste, die Menüleiste, das Fenstermenü, die Schaltflächen zum minimieren und maximieren, die Größenanpassung und die Bild Lauf leisten werden zusammen als *nicht-Client Bereich* des Fensters bezeichnet. Das System verwaltet die meisten Aspekte des nicht-Client Bereichs. die Anwendung verwaltet die Darstellung und das Verhalten des Client Bereichs.

In der *Titelleiste* werden ein von der Anwendung definiertes Symbol und eine Textzeile angezeigt. in der Regel gibt der Text den Namen der Anwendung an oder gibt den Zweck des Fensters an. Eine Anwendung gibt das Symbol und den Text beim Erstellen des Fensters an. Die Titelleiste ermöglicht es dem Benutzer auch, das Fenster mit einer Maus oder einem anderen Zeigegerät zu verschieben.

Die meisten Anwendungen enthalten eine *Menüleiste* , in der die von der Anwendung unterstützten Befehle aufgeführt sind. Elemente in der Menüleiste stellen die Hauptkategorien von Befehlen dar. Wenn Sie auf ein Element in der Menüleiste klicken, wird in der Regel ein Popup Menü geöffnet, dessen Elemente den Aufgaben in einer bestimmten Kategorie entsprechen. Durch Klicken auf einen Befehl leitet der Benutzer die Anwendung an, um eine Aufgabe auszuführen.

Das *Menü Fenster* wird vom System erstellt und verwaltet. Sie enthält einen Standardsatz von Menü Elementen, die, wenn Sie vom Benutzer ausgewählt werden, die Größe oder Position eines Fensters festlegen, die Anwendung schließen oder Tasks ausführen. Weitere Informationen finden Sie unter [Menüs](/windows/desktop/menurc/menus).

Die Schaltflächen in der oberen rechten Ecke beeinflussen die Größe und Position des Fensters. Wenn Sie auf die *Schaltfläche maximieren* klicken, vergrößert das System das Fenster auf die Bildschirmgröße und positioniert das Fenster, sodass es den gesamten Desktop (abzüglich der Taskleiste) abdeckt. Gleichzeitig ersetzt das System die Schaltfläche "maximieren" durch die Schaltfläche "Wiederherstellen". Wenn Sie auf die *Schaltfläche Wiederherstellen* klicken, stellt das System die vorherige Größe und Position des Fensters wieder her. Wenn Sie auf die *Schaltfläche Minimieren* klicken, verringert das System das Fenster auf die Größe der Task leisten Schaltfläche, positioniert das Fenster auf der Task leisten Schaltfläche und zeigt die Task leisten Schaltfläche im normalen Zustand an. Um die vorherige Größe und Position der Anwendung wiederherzustellen, klicken Sie auf die zugehörige Task leisten Schaltfläche. Wenn Sie auf die *Schaltfläche Schließen* klicken, wird die Anwendung beendet.

Der *Größen* Anpassungsrahmen ist ein Bereich um den Umkreis des Fensters, der es dem Benutzer ermöglicht, das Fenster mit einer Maus oder einem anderen Zeigegerät zu vergrößern.

Die *horizontale Schiebe Leiste* und die vertikale Bild Lauf *Leiste* konvertieren Maus-oder Tastatureingaben in Werte, die eine Anwendung verwendet, um den Inhalt des Client Bereichs entweder horizontal oder vertikal zu verschieben. Beispielsweise stellt eine Textverarbeitungsanwendung, die ein langes Dokument anzeigt, in der Regel eine vertikale Schiebe Leiste zur Verfügung, mit der der Benutzer das Dokument nach oben und unten durchblättern kann.

## <a name="controls-and-dialog-boxes"></a>Steuerelemente und Dialog Felder

Eine Anwendung kann neben dem Hauptfenster, einschließlich Steuerelementen und Dialogfeldern, mehrere Windows-Typen erstellen.

Ein *Steuer* Element ist ein Fenster, das von einer Anwendung verwendet wird, um bestimmte Informationen vom Benutzer zu erhalten, z. b. den Namen einer zu öffnenden Datei oder die gewünschte Punktgröße einer Textauswahl. Anwendungen verwenden außerdem Steuerelemente zum Abrufen von Informationen, die zum Steuern eines bestimmten Anwendungs Features erforderlich sind. Beispielsweise stellt eine Textverarbeitungsanwendung in der Regel ein Steuerelement bereit, damit der Benutzer das Wort Umbruch aktivieren und deaktivieren kann. Weitere Informationen finden Sie unter [Windows](/windows/desktop/Controls/window-controls)-Steuerelemente.

Steuerelemente werden immer in Verbindung mit einem anderen Fenster verwendet – in der Regel in einem Dialogfeld. Ein *Dialogfeld* ist ein Fenster, das ein oder mehrere Steuerelemente enthält. Eine Anwendung verwendet ein Dialogfeld, um den Benutzer zur Eingabe der Eingabe aufzufordern, die zum Ausführen eines Befehls benötigt wird. Beispielsweise würde eine Anwendung, die einen Befehl zum Öffnen einer Datei enthält, ein Dialogfeld anzeigen, in dem die Steuerelemente enthalten sind, in denen der Benutzer einen Pfad und einen Dateinamen angibt. In Dialog Feldern wird in der Regel nicht der gleiche Satz von Fenster Komponenten verwendet wie ein Hauptfenster. Die meisten verfügen über eine Titelleiste, ein Fenstermenü, einen Rahmen (keine Größenänderung) und einen Client Bereich, aber Sie verfügen in der Regel nicht über eine Menüleiste, minimieren und maximieren von Schaltflächen oder Scrollleisten. Weitere Informationen finden Sie unter [Dialog Felder](/windows/desktop/dlgbox/dialog-boxes).

Ein Meldungs *Feld* ist ein spezielles Dialogfeld, in dem ein Hinweis, eine Vorsicht oder eine Warnung für den Benutzer angezeigt wird. Beispielsweise kann ein Meldungs Feld den Benutzer über ein Problem informieren, das die Anwendung beim Ausführen einer Aufgabe gefunden hat. Weitere Informationen finden Sie in den Meldungs [Feldern](/windows/desktop/dlgbox/about-dialog-boxes).

## <a name="window-attributes"></a>Fenster Attribute

Wenn ein Fenster erstellt wird, muss eine Anwendung die folgenden Informationen bereitstellen. (Mit Ausnahme des [Fenster Handles](#window-handle), das die Erstellungs Funktion zurückgibt, um das neue Fenster eindeutig zu identifizieren.)

-   [Klassenname](#class-name)
-   [Fenstername](#window-name)
-   [Fensterstil](#window-style)
-   [Erweiterter Fenster Stil](#extended-window-style)
-   [Position](#position)
-   [Größe](#size)
-   [Übergeordnetes Fenster oder Besitzer Fenster handle](#parent-or-owner-window-handle)
-   [Menü handle oder Child-Window Bezeichner](#menu-handle-or-child-window-identifier)
-   [Anwendungsinstanzhandle](#application-instance-handle)
-   [Erstellungs Daten](#creation-data)
-   [Fensterhandle](#window-handle)

Diese Fenster Attribute werden in den folgenden Abschnitten beschrieben.

### <a name="class-name"></a>Klassenname

Jedes Fenster gehört zu einer Fenster Klasse. Vor dem Erstellen von Fenstern dieser Klasse muss eine Anwendung eine Fenster Klasse registrieren. Die *Fenster Klasse* definiert die meisten Aspekte des Erscheinungs Bilds und Verhaltens eines Fensters. Die Hauptkomponente einer Fenster Klasse ist die *Fenster Prozedur*, eine Funktion, die alle Eingaben und Anforderungen empfängt und verarbeitet, die an das Fenster gesendet werden. Das System stellt die Eingaben und Anforderungen in Form von *Nachrichten* bereit. Weitere Informationen finden Sie unter [Fenster Klassen](window-classes.md), [Fenster Prozeduren](window-procedures.md)und [Meldungen und Nachrichten Warteschlangen](messages-and-message-queues.md).

### <a name="window-name"></a>Fenstername

Ein *Fenster Name* ist eine Text Zeichenfolge, die ein Fenster für den Benutzer identifiziert. Ein Hauptfenster, ein Dialogfeld oder ein Meldungs Feld zeigt in der Regel seinen Fensternamen in der Titelleiste an, falls vorhanden. Ein Steuerelement kann seinen Fensternamen abhängig von der Klasse des Steuer Elements anzeigen. Beispielsweise werden durch Schaltflächen, Bearbeitungs Steuerelemente und statische Steuerelemente die Fensternamen innerhalb des Rechtecks angezeigt, das vom-Steuerelement belegt wird. Steuerelemente, wie z. b. Listenfelder und Kombinations Felder, zeigen jedoch keine Fensternamen an.

Um den Fensternamen nach dem Erstellen eines Fensters zu ändern, verwenden Sie die [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) -Funktion. Diese Funktion verwendet die Funktionen [**getwindowtextlength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha) und [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) zum Abrufen der aktuellen Zeichenfolge für den Fensternamen aus dem Fenster.

### <a name="window-style"></a>Fensterstil

Jedes Fenster verfügt über ein oder mehrere Fenster Stile. Ein Fenster Stil ist eine benannte Konstante, die einen Aspekt der Darstellung und des Verhaltens des Fensters definiert, das nicht von der Klasse des Fensters angegeben wird. Beim Erstellen von Fenstern legt eine Anwendung normalerweise Fenster Stile fest. Sie können die Stile auch nach dem Erstellen eines Fensters mithilfe der [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) -Funktion festlegen.

Das System und, in gewissem Umfang, die Fenster Prozedur für die Klasse, interpretiert die Fenster Stile.

Einige Fenster Stile gelten für alle Fenster, aber die meisten gelten für Fenster spezifischer Fenster Klassen. Die allgemeinen Fenster Stile werden durch Konstanten dargestellt, die mit dem WS- \_ Präfix beginnen. Sie können mit dem or-Operator kombiniert werden, um unterschiedliche Arten von Fenstern zu bilden, darunter Hauptfenster, Dialogfelder und untergeordnete Fenster. Die klassenspezifischen Fenster Stile definieren die Darstellung und das Verhalten von Fenstern, die zu den vordefinierten Steuerelement Klassen gehören. Beispielsweise gibt die **ScrollBar** -Klasse ein Bild Lauf leisten-Steuerelement an, aber die Stile [**SB \_ Horz**](../controls/scroll-bar-control-styles.md) und **SSB \_ Vert** bestimmen, ob ein horizontales oder vertikales Schiebe leisten-Steuerelement erstellt wird.

Eine Liste der Stile, die von Windows verwendet werden können, finden Sie in den folgenden Themen:

-   [**Fensterstile**](window-styles.md)
-   [Schaltflächenstile](../controls/button-styles.md)
-   [Kombinations Feld Stile](../controls/combo-box-styles.md)
-   [Steuerelement Stile bearbeiten](../controls/edit-control-styles.md)
-   [Listenfeld Stile](../controls/list-box-styles.md)
-   [Rich Edit-Steuerelement Stile](../controls/rich-edit-control-styles.md)
-   [ScrollBar-Steuerelement Stile](../controls/scroll-bar-control-styles.md)
-   [Statische Steuerelement Stile](../controls/static-control-styles.md)

### <a name="extended-window-style"></a>Erweiterter Fenster Stil

Jedes Fenster kann optional über ein oder mehrere erweiterte Fenster Stile verfügen. Ein *Erweitertes Fenster Stil* ist eine benannte Konstante, die einen Aspekt der Darstellung und des Verhaltens des Fensters definiert, das nicht durch die Fenster Klasse oder die anderen Fenster Stile angegeben wird. Beim Erstellen von Fenstern legt eine Anwendung normalerweise erweiterte Fenster Stile fest. Sie können die Stile auch nach dem Erstellen eines Fensters mithilfe der [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) -Funktion festlegen.

Weitere Informationen finden Sie unter " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa)".

### <a name="position"></a>Position

Die Position eines Fensters ist als die Koordinaten der linken oberen Ecke definiert. Diese Koordinaten (manchmal auch als Fenster Koordinaten bezeichnet) sind immer relativ zur oberen linken Ecke des Bildschirms oder, bei einem untergeordneten Fenster, in der linken oberen Ecke des Client Bereichs des übergeordneten Fensters. Beispielsweise wird ein Fenster der obersten Ebene mit den Koordinaten (10, 10) rechts von der oberen linken Ecke des Bildschirms 10 Pixel und 10 Pixel davon entfernt. Ein untergeordnetes Fenster, das über die Koordinaten (10, 10) verfügt, wird rechts von der oberen linken Ecke des Client Bereichs des übergeordneten Fensters 10 Pixel und 10 Pixel davon entfernt.

Die [**WindowFromPoint**](/windows/win32/api/winuser/nf-winuser-windowfrompoint) -Funktion Ruft ein Handle für das Fenster ab, das einen bestimmten Punkt auf dem Bildschirm einnimmt. Ebenso rufen die Funktionen [**childwindowfrompoint**](/windows/win32/api/winuser/nf-winuser-childwindowfrompoint) und [**ChildWindowFromPointEx**](/windows/win32/api/winuser/nf-winuser-childwindowfrompointex) ein Handle für das untergeordnete Fenster ab, das einen bestimmten Punkt im Client Bereich des übergeordneten Fensters einnimmt. Obwohl **ChildWindowFromPointEx** unsichtbare, deaktivierte und transparente untergeordnete Fenster ignorieren kann, ist **childwindowfrompoint** nicht möglich.

### <a name="size"></a>Size

Die Größe eines Fensters (Breite und Höhe) wird in Pixel angegeben. Ein Fenster kann eine Breite oder Höhe von 0 (null) aufweisen. Wenn eine Anwendung die Breite und Höhe eines Fensters auf NULL festlegt, legt das System die Größe auf die standardmäßige minimale Fenstergröße fest. Um die standardmäßige minimale Fenstergröße zu ermitteln, verwendet eine Anwendung die [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion mit den **SM- \_ cxMin** -und **SM \_ Cymin** -Flags.

Möglicherweise muss eine Anwendung ein Fenster mit einem Client Bereich einer bestimmten Größe erstellen. Die Funktionen "Setting [**WindowRect**](/windows/win32/api/winuser/nf-winuser-adjustwindowrect) " und "Setting [**windowrectex**](/windows/win32/api/winuser/nf-winuser-adjustwindowrectex) " berechnen die erforderliche Größe eines Fensters basierend auf der gewünschten Größe des Client Bereichs. Die Anwendung kann die resultierenden Größen Werte an die Funktion " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " übergeben.

Eine Anwendung kann ein Fenster verkleinern, damit Sie sehr groß ist. Das Fenster sollte jedoch nicht mit der Größe des Bildschirms vergrößert werden. Vor dem Festlegen der Größe eines Fensters sollte die Anwendung die Breite und Höhe des Bildschirms überprüfen, indem [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) mit den **SM- \_ cxscreen** -und **SM \_ cyscreen** -Flags verwendet wird.

### <a name="parent-or-owner-window-handle"></a>Übergeordnetes Fenster oder Besitzer Fenster handle

Ein Fenster kann über ein übergeordnetes Fenster verfügen. Ein Fenster, das über ein übergeordnetes Element verfügt, wird als untergeordnetes *Fenster* bezeichnet. Das über *geordnete Fenster* stellt das Koordinatensystem bereit, das zum Positionieren eines untergeordneten Fensters verwendet wird. Ein übergeordnetes Fenster wirkt sich auf Aspekte der Darstellung eines Fensters aus. Beispielsweise wird ein untergeordnetes Fenster abgeschnitten, sodass kein Teil des untergeordneten Fensters außerhalb der Grenzen des übergeordneten Fensters angezeigt werden kann.

Ein Fenster, das kein übergeordnetes Element aufweist oder dessen übergeordnetes Element das Desktop Fenster ist, wird als *Fenster der obersten Ebene* bezeichnet. Eine Anwendung kann die [**EnumWindows**](/windows/win32/api/winuser/nf-winuser-enumwindows) -Funktion verwenden, um ein Handle für jedes Fenster der obersten Ebene auf dem Bildschirm zu erhalten. **EnumWindows** übergibt das Handle an jedes Fenster der obersten Ebene, wiederum an eine Anwendungs definierte Rückruffunktion, [**EnumWindowsProc**](/previous-versions/windows/desktop/legacy/ms633498(v=vs.85)).

Ein Fenster der obersten Ebene kann ein anderes Fenster besitzen oder im Besitz eines anderen Fensters sein. Ein *eigenes Fenster* wird immer vor dem Besitzer Fenster angezeigt, wird ausgeblendet, wenn das Besitzer Fenster minimiert wird, und wird zerstört, wenn das Besitzer Fenster zerstört wird. Weitere Informationen finden Sie unter [Windows-Besitzer](window-features.md#owned-windows).

### <a name="menu-handle-or-child-window-identifier"></a>Menü handle oder Child-Window Bezeichner

Ein untergeordnetes Fenster kann einen *Bezeichner* des untergeordneten Fensters aufweisen, einen eindeutigen, von der Anwendung definierten Wert, der mit dem untergeordneten Fenster verknüpft ist. Bezeichner für untergeordnete Fenster sind besonders nützlich für Anwendungen, die mehrere untergeordnete Fenster erstellen. Beim Erstellen eines untergeordneten Fensters gibt eine Anwendung den Bezeichner des untergeordneten Fensters an. Nachdem Sie das Fenster erstellt haben, kann die Anwendung den Bezeichner des Fensters mithilfe der [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) -Funktion ändern oder den Bezeichner mithilfe der [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) -Funktion abrufen.

Jedes Fenster, mit Ausnahme eines untergeordneten Fensters, kann über ein Menü verfügen. Eine Anwendung kann ein Menü einschließen, indem ein Menü handle entweder beim Registrieren der Klasse des Fensters oder beim Erstellen des Fensters bereitgestellt wird.

### <a name="application-instance-handle"></a>Anwendungsinstanzhandle

Jeder Anwendung ist ein Instanzhandle zugeordnet. Das System stellt den Instanzhandle für eine Anwendung bereit, wenn die Anwendung gestartet wird. Da es mehrere Kopien derselben Anwendung ausführen kann, verwendet das System intern Instanzhandles, um eine Instanz einer Anwendung von anderen zu unterscheiden. Die Anwendung muss den Instanzhandle in vielen verschiedenen Fenstern angeben, einschließlich derjenigen, die Fenster erstellen.

### <a name="creation-data"></a>Erstellungs Daten

Jedem Fenster können Anwendungs definierte Erstellungs Daten zugeordnet werden. Wenn das Fenster erstmalig erstellt wird, übergibt das System einen Zeiger auf die Daten in der Fenster Prozedur des Fensters, das erstellt wird. Die Fenster Prozedur verwendet die Daten, um Anwendungs definierte Variablen zu initialisieren.

### <a name="window-handle"></a>Fensterhandle

Nachdem Sie ein Fenster erstellt haben, gibt die Erstellungs Funktion ein *Fenster Handle* zurück, das das Fenster eindeutig identifiziert. Ein Fenster Handle weist den **HWND** -Datentyp auf. beim Deklarieren einer Variablen, die ein Fenster Handle enthält, muss eine Anwendung diesen Typ verwenden. Eine Anwendung verwendet dieses Handle in anderen Funktionen, um Ihre Aktionen an das Fenster weiterzuleiten.

Eine Anwendung kann die [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) -Funktion verwenden, um zu ermitteln, ob im System ein Fenster mit dem angegebenen Klassennamen oder Fensternamen vorhanden ist. Wenn ein solches Fenster vorhanden ist, gibt **FindWindow** ein Handle für das Fenster zurück. Verwenden Sie die Funktion [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) , um die Suche auf die untergeordneten Fenster einer bestimmten Anwendung einzuschränken.

Die [**IsWindow**](/windows/win32/api/winuser/nf-winuser-iswindow) -Funktion bestimmt, ob ein Fenster Handle ein gültiges, vorhandenes Fenster identifiziert. Es gibt spezielle Konstanten, die ein Fenster Handle in bestimmten Funktionen ersetzen können. Eine Anwendung kann z. b. **HWND- \_ Broadcast** in den Funktionen [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) und [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) oder **HWND \_ Desktop** in der [**mapwindowpoints**](/windows/desktop/api/winuser/nf-winuser-mapwindowpoints) -Funktion verwenden.

## <a name="window-creation"></a>Fenster Erstellung

Um Anwendungsfenster zu erstellen, verwenden Sie die Funktion "up [**Window**](/windows/win32/api/winuser/nf-winuser-createwindowa) " oder " [**deatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ". Sie müssen die zum Definieren der Fenster Attribute erforderlichen Informationen bereitstellen. " **Kreatewindowex** " hat den Parameter " *dwExStyle*", der von "up **Window** " nicht verwendet wird. Andernfalls sind die Funktionen identisch. Tatsächlich ruft " **kreatewindow** " einfach " **kreatewindowex** " auf, wobei der *dwExStyle* -Parameter auf NULL festgelegt ist. Aus diesem Grund bezieht sich der Rest dieser Übersicht nur auf " **kreatewindowex**".

Dieser Abschnitt enthält die folgenden Themen:

-   [Hauptfenster Erstellung](#main-window-creation)
-   [Fenster Erstellungs Meldungen](#window-creation-messages)
-   [Multithreadanwendungen](#multithread-applications)

> [!Note]  
> Es gibt zusätzliche Funktionen zum Erstellen spezieller Fenster, z. b. Dialogfelder und Meldungs Felder. Weitere Informationen finden Sie unter [**Dialogbox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa), [**kreatedialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga)und [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).

 

### <a name="main-window-creation"></a>Hauptfenster Erstellung

Jede Windows-basierte Anwendung muss über [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) als Einstiegspunkt Funktion verfügen. **WinMain** führt eine Reihe von Aufgaben aus, einschließlich der Registrierung der Fenster Klasse für das Hauptfenster und Erstellen des Hauptfensters. **WinMain** registriert die Hauptfenster Klasse durch Aufrufen der [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) -Funktion und erstellt das Hauptfenster durch Aufrufen der Funktion [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

Die [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) -Funktion kann die Anwendung auch auf eine einzelne Instanz beschränken. Erstellen Sie einen benannten Mutex mithilfe der Funktion " [**kreatemutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) ". Wenn [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) einen Fehler zurückgibt, ist bereits eine andere Instanz der Anwendung vorhanden (der Mutex wurde erstellt), und Sie sollten **\_ \_** **WinMain** beenden.

Das System zeigt das Hauptfenster nach der Erstellung nicht automatisch an. Stattdessen muss eine Anwendung die [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) -Funktion verwenden, um das Hauptfenster anzuzeigen. Nachdem Sie das Hauptfenster erstellt haben, ruft die [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) -Funktion der Anwendung **ShowWindow** auf und übergibt zwei Parameter: ein Handle an das Hauptfenster und ein Flag, das angibt, ob das Hauptfenster beim ersten anzeigen minimiert oder maximiert werden soll. Normalerweise kann das-Flag auf eine beliebige Konstante festgelegt werden, die mit dem SW- \_ Präfix beginnt. Wenn jedoch **ShowWindow** aufgerufen wird, um das Hauptfenster der Anwendung anzuzeigen, muss das-Flag auf " **SW \_ showdefault**" festgelegt werden. Dieses Flag weist das System an, das Fenster wie von dem Programm, das die Anwendung gestartet hat, anzuzeigen.

Wenn eine Fenster Klasse bei der Unicode-Version von [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)registriert wurde, empfängt das Fenster nur Unicode-Nachrichten. Um zu ermitteln, ob ein Fenster den Unicode-Zeichensatz verwendet oder nicht, nennen Sie [**iswindowunicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode).

### <a name="window-creation-messages"></a>Window-Creation Meldungen

Beim Erstellen eines beliebigen Fensters sendet das System Nachrichten an die Fenster Prozedur für das Fenster. Das System sendet die [**WM \_ nccreate**](wm-nccreate.md) -Meldung, nachdem der nicht-Client Bereich des Fensters erstellt wurde, und die [**WM \_ Create**](wm-create.md) -Meldung nach dem Erstellen des Client Bereichs. Die Fenster Prozedur empfängt beide Meldungen, bevor das System das Fenster anzeigt. Beide Meldungen enthalten einen Zeiger auf eine Struktur vom Typ " [**foratestruct**](/windows/win32/api/winuser/ns-winuser-createstructa) ", die alle Informationen enthält, die in der Funktion " [**kreatewindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa) " angegeben sind. In der Regel führt die Fenster Prozedur Initialisierungs Aufgaben aus, wenn diese Nachrichten empfangen werden.

Wenn Sie ein untergeordnetes Fenster erstellen, sendet das System nach dem Senden der " [**WM \_ nccreate**](wm-nccreate.md) "-und " [**WM \_ Create**](wm-create.md) "-Nachricht die WM-Nachricht " [**\_ Parser**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) " an das übergeordnete Fenster Beim Erstellen eines Fensters werden auch andere Nachrichten gesendet. Die Anzahl und Reihenfolge dieser Meldungen hängt von der Fenster Klasse und dem Stil und von der Funktion ab, die zum Erstellen des Fensters verwendet wird. Diese Nachrichten werden in anderen Themen in dieser Hilfedatei beschrieben.

### <a name="multithread-applications"></a>Multithreadanwendungen

Eine Windows-basierte Anwendung kann mehrere Ausführungs Threads aufweisen, und jeder Thread kann Fenster erstellen. Der Thread, der ein Fenster erstellt, muss den Code für die Fenster Prozedur enthalten.

Eine Anwendung kann die [**enumthreadwindows**](/windows/win32/api/winuser/nf-winuser-enumthreadwindows) -Funktion verwenden, um die von einem bestimmten Thread erstellten Fenster aufzulisten. Diese Funktion übergibt das Handle an jedes Thread Fenster, wiederum an eine Anwendungs definierte Rückruffunktion, [**enumthreadwndproc**](/previous-versions/windows/desktop/legacy/ms633496(v=vs.85)).

Die [**getwindowthreadprocessid-**](/windows/win32/api/winuser/nf-winuser-getwindowthreadprocessid) Funktion gibt den Bezeichner des Threads zurück, der ein bestimmtes Fenster erstellt hat.

Um den Anzeige Zustand eines von einem anderen Thread erstellten Fensters festzulegen, verwenden Sie die [**ShowWindowAsync**](/windows/win32/api/winuser/nf-winuser-showwindowasync) -Funktion.

 

 
