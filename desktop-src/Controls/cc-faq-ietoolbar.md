---
title: Erstellen einer Internet Explorer-Style Symbolleiste
description: Eine der wichtigsten Funktionen der Benutzeroberfläche von Windows Internet Explorer ist die Symbolleiste. Sie ermöglicht Benutzern nicht nur den Zugriff auf eine Vielzahl von Features, sondern ermöglicht Benutzern auch das Anpassen des Layouts gemäß Ihren persönlichen Vorlieben.
ms.assetid: d24969ec-4dea-44c6-b045-5611de8f1cce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32228f941a7c7e1253884ab5d72368f66f25c7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102427"
---
# <a name="how-to-create-an-internet-explorer-style-toolbar"></a>Erstellen einer Internet Explorer-Style Symbolleiste

Eine der wichtigsten Funktionen der Benutzeroberfläche von Windows Internet Explorer ist die Symbolleiste. Sie ermöglicht Benutzern nicht nur den Zugriff auf eine Vielzahl von Features, sondern ermöglicht Benutzern auch das Anpassen des Layouts gemäß Ihren persönlichen Vorlieben.

Der folgende Screenshot zeigt die Internet Explorer-Symbolleiste und zeigt einige der wichtigsten Features.

![Screenshot der Windows Internet Explorer-Symbolleiste mit Bezeichnungen für acht Features](images/howto1a.jpg)

Diese Symbolleiste besteht im Wesentlichen aus einem Grund leisten-Steuerelement mit vier Bändern: drei Symbolleisten und einer Menüleiste. Da es mit der Common Controls-API implementiert ist, können Entwickler Symbolleisten mit allen Funktionen von oder allen Funktionen erstellen. In diesem Thema werden die wesentlichen Features der Internet Explorer-Symbolleiste erläutert und erläutert, wie Sie in Ihrer Anwendung implementiert werden.

-   [Das Grund leisten-Steuerelement](#the-rebar-control)
    -   [Implementieren des Grund leisten-Steuer Elements](#implementing-the-rebar-control)
-   [Die Symbolleisten](#how-to-create-an-internet-explorer-style-toolbar)
    -   [Dropdown Schaltflächen](#drop-down-buttons)
    -   [Schaltflächen im Listenformat](#list-style-buttons)
    -   [Spitze Klammern](#handling-chevrons)
    -   [Hot-Tracking](#hot-tracking)
-   [Zugehörige Themen](#related-topics)

## <a name="the-rebar-control"></a>Das Grund leisten-Steuerelement

Die zugrunde liegende Struktur der Internet Explorer-Symbolleiste wird von einem Grund leisten- [Steuer](rebar-controls.md)Element bereitgestellt. Dieses Steuerelement bietet Benutzern die Möglichkeit, die Anordnung einer Auflistung von Tools anzupassen. Jede Info Leiste enthält ein oder mehrere *Bänder*, in der Regel lange, schmale Rechtecke, die ein untergeordnetes Fenster enthalten, häufig ein Symbolleisten-Steuerelement.

Das Grund leisten-Steuerelement zeigt seine Bänder in einem rechteckigen Bereich an, in der Regel am oberen Rand des Fensters. Dieses Rechteck ist in einen oder mehrere Striche unterteilt, die die Höhe eines Bands sind. Jedes Band kann sich in einem separaten Bereich befinden, oder es können mehrere Bänder auf demselben Strip platziert werden.

Ein Grund leisten-Steuerelement bietet Benutzern zwei Möglichkeiten zum Anordnen Ihrer Tools:

-   Jedes Band *verfügt in der Regel über einen Zieh* Punkt am linken Rand. Greifer werden verwendet, wenn zwei oder mehr Bänder an einem einzelnen Strip die Breite des Fensters überschreiten. Durchziehen des Zieh Elements nach links oder rechts können Benutzer steuern, wie viel Speicherplatz jedem Band zugeordnet wird.
-   Benutzer können die Bänder innerhalb des Anzeige Rechtecks der Info Leiste durchziehen und Ablegen verschieben. Das Grund leisten-Steuerelement ändert dann die Anzeige, um der neuen Anordnung von Bändern Rechnung zu tragen. Wenn alle Bänder aus einem Strip entfernt werden, wird die Höhe der Info Leiste reduziert und der Anzeigebereich vergrößert.

Eine Anwendung kann Bänder nach Bedarf hinzufügen oder entfernen. In der Regel können Benutzer mithilfe von Anwendungen auswählen, welche Bänder im Menü Ansicht oder Kontextmenü angezeigt werden sollen.

Wenn die kombinierte Breite der Bänder auf einem Strip die Breite des Fensters überschreitet, passt das Grund leisten-Steuerelement die Breite nach Bedarf an. Einige der Tools können von dem angrenzenden Band abgedeckt werden.

[Version 5,80](common-control-versions.md) der allgemeinen Steuerelemente bietet eine Möglichkeit, Tools, die von einem anderen Band abgedeckt wurden, für den Benutzer zugänglich zu machen. Wenn Sie das Flag RBBS \_ usechevron im **fstyle** -Member der [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur des Bands festlegen, wird ein *Chevron* für Symbolleisten angezeigt, die abgedeckt wurden. Wenn ein Benutzer auf das Chevron klickt, wird ein Menü angezeigt, in dem der Benutzer die ausgeblendeten Tools verwenden kann. Der folgende Screenshot von Microsoft Internet Explorer 6 zeigt das Menü, das angezeigt wird, wenn ein Teil der Standard Symbolleiste abgedeckt wird.

![Screenshot, der das durch Klicken auf das Chevron angezeigte Menü anzeigt](images/howto2.jpg)

Da jedes Band ein Steuerelement enthält, können Sie zusätzliche Flexibilität über die API des-Steuer Elements bereitstellen. Beispielsweise können Sie die Symbolleisten Anpassung implementieren, um Benutzern das Hinzufügen, verschieben oder Löschen von Schaltflächen auf einer Symbolleiste zu ermöglichen.

### <a name="implementing-the-rebar-control"></a>Implementieren des Grund leisten-Steuer Elements

Die meisten Features der Internet Explorer-Symbolleiste sind tatsächlich in den einzelnen Bändern implementiert. Die Implementierung des Grund leisten-Steuer Elements selbst ist unkompliziert und wird unten aufgeführt.

1.  Erstellen Sie das Grund leisten-Steuerelement mit " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)". Legen Sie *dwExStyle* auf [**WS \_ Ex \_ ToolWindow**](/windows/desktop/winmsg/extended-window-styles) und *lpClassName* auf [**rebarclassname**](common-control-window-classes.md)fest. Internet Explorer verwendet die folgenden Fenster Stile:

    -   [**RSB- \_ Band Rahmen**](rebar-control-styles.md)
    -   [**RSB \_ dblclktoggle**](rebar-control-styles.md)
    -   [**RSB- \_ Register Drop**](rebar-control-styles.md)
    -   [**RSB \_ varHeight**](rebar-control-styles.md)
    -   [**CCS- \_ nodivider**](common-control-styles.md)
    -   [**CCS \_ noparentalign**](common-control-styles.md)
    -   [**WS \_ -Rahmen**](/windows/desktop/winmsg/window-styles)
    -   [**untergeordnetes Element \_**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ clipchildren**](/windows/desktop/winmsg/window-styles)
    -   [**WS- \_ clipneben Elemente**](/windows/desktop/winmsg/window-styles)
    -   [**WS- \_ sichtbar**](/windows/desktop/winmsg/window-styles)

    Legen Sie die anderen Parameter entsprechend Ihren Anwendungen fest.

2.  Erstellen Sie ein Steuerelement mit der Funktion " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " oder einer spezialisierten Steuerelement Erstellungs Funktion [**, wie z. b**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex). "".
3.  Initialisieren Sie ein Band für das-Steuerelement, indem Sie die Member von [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)ausfüllen. Schließen Sie den RBBS \_ usechevron-Stil mit dem **fstyle** -Member ein, um Chevrons zu aktivieren.
4.  Fügen Sie das Band mit einer [**RB \_ InsertBand**](rb-insertband.md) -Meldung zum Info leisten-Steuerelement hinzu.
5.  Wiederholen Sie die Schritte 2-4 für die verbleibenden Bänder.
6.  Implementieren von Handlern für die Benachrichtigungs Benachrichtigungen. Insbesondere müssen Sie [RBN \_ chevronpushvorgang](rbn-chevronpushed.md) verarbeiten, um ein Dropdown Menü anzuzeigen, wenn auf ein Chevron geklickt wird. Weitere Informationen finden Sie unter [Verarbeiten von Chevrons](#handling-chevrons).

Die Greifer sind standardmäßig enthalten. Wenn Sie den Zieh Punkt für ein Band weglassen möchten, legen Sie das RBBS \_ nogripperflag im **fstyle** -Member der [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur des Bands fest. Weitere Informationen zum Implementieren von Grund leisten-Steuerelementen finden Sie unter Informationen zu Grund leisten-Steuer [Elementen](rebar-controls.md).

### <a name="handling-chevrons"></a>Verarbeiten von Chevrons

Wenn ein Benutzer auf ein Chevron klickt, sendet das Grund leisten-Steuerelement ihrer Anwendung eine [RBN- \_ chevronpushbenachrichtigung](rbn-chevronpushed.md) . Die [**nmrebarchevron**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) -Struktur, die mit der Benachrichtigung übermittelt wird, enthält den Bezeichner des Bands und eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur mit dem Rechteck, das vom Chevron besetzt ist. Der Handler muss bestimmen, welche Schaltflächen ausgeblendet sind, und die zugehörigen Befehle in einem Popup Menü anzeigen.

Im folgenden Verfahren wird beschrieben, wie eine [RBN- \_ chevronpushbenachrichtigung](rbn-chevronpushed.md) behandelt wird:

1.  Abrufen des aktuellen umschließenden Rechtecks für das ausgewählte Band durch Senden des Info Leiste-Steuer Elements an eine [**RB \_ GetRect**](rb-getrect.md) -Nachricht.
2.  Rufen Sie die Gesamtzahl der Schaltflächen ab, indem Sie das Symbolleisten-Steuerelement des Bands an eine [**TB \_ ButtonCount**](tb-buttoncount.md) -Meldung
3.  Beginnend mit der linken Schaltfläche rufen Sie das umgebende Rechteck der Schaltfläche ab, indem Sie das Symbolleisten-Steuerelement mit einer [**TB \_ GetItemRect**](tb-getitemrect.md) -Nachricht senden.
4.  Übergeben Sie das Band und die Schaltflächen Rechtecke an die [**intersectRect**](/windows/desktop/api/winuser/nf-winuser-intersectrect) -Funktion. Diese Funktion gibt eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur zurück, die dem sichtbaren Teil der Schaltfläche entspricht.
5.  Übergeben Sie das Schaltflächen Rechteck und das Rechteck für den sichtbaren Teil der Schaltfläche an die [**equalrect**](/windows/desktop/api/winuser/nf-winuser-equalrect) -Funktion.
6.  Wenn [**equalrect**](/windows/desktop/api/winuser/nf-winuser-equalrect) **true** zurückgibt, ist die gesamte Schaltfläche sichtbar. Wiederholen Sie die Schritte 3-5 für die Schaltfläche weiter auf der Symbolleiste. Wenn **equalrect** **false** zurückgibt, ist die Schaltfläche zumindest teilweise ausgeblendet, und alle verbleibenden Schaltflächen werden vollständig ausgeblendet. Fahren Sie mit dem nächsten Schritt fort.
7.  Erstellen Sie ein Popupmenü mit Elementen für jede der ausgeblendeten Schaltflächen.
8.  Zeigen Sie das Popup Menü mithilfe der [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) -Funktion an. Verwenden Sie das Chevron-Rechteck, das mit der [RBN \_ chevronpushbenachrichtigung](rbn-chevronpushed.md) übergeben wurde, um das Menü zu positionieren. Das Menü sollte sich unmittelbar unterhalb des Chevron befinden, wobei die linken Kanten ausgerichtet sind.
9.  Behandeln Sie die Menübefehle.

## <a name="the-toolbars"></a>Die Symbolleisten

Der größte Teil der Komplexität der Internet Explorer-Symbolleiste liegt in der Implementierung von Steuerelementen, die die Grund leisten Bänder bilden. Internet Explorer zeigt im Allgemeinen vier Bänder an:

-   Die Menüleiste
-   Standard Symbolleiste
-   Die Symbolleiste Verknüpfungen
-   Die Adress Symbolleiste

Alle diese Bänder, einschließlich der Menüleiste, enthalten tatsächlich Symbolleisten-Steuerelemente. In diesem Abschnitt wird die Implementierung der Symbolleisten Standard und Links erläutert. Die Menüleiste ist etwas komplizierter und wird separat unter [How to Create a Internet Explorer-Style Menu Bar](cc-faq-iemenubar.md)erläutert.

Grundlegende Verfahren zum Implementieren von Symbolleisten-Steuerelementen finden Sie unter [Informationen zu Symbol](toolbar-controls-overview.md)leisten Dieser Abschnitt konzentriert sich auf einige der neueren Symbolleisten Features, die von Internet Explorer verwendet werden, um die Verwendbarkeit des Steuer Elements zu erhöhen.

-   [Dropdown Schaltflächen](#drop-down-buttons)
-   [Schaltflächen im Listenformat](#list-style-buttons)
-   [Spitze Klammern](#handling-chevrons)
-   [Hot-Tracking](#hot-tracking)

### <a name="drop-down-buttons"></a>Dropdown Schaltflächen

Dropdown-Schaltflächen unterstützen mehrere Befehle. Wenn der Benutzer auf eine Dropdown-Schaltfläche klickt, zeigt die Schaltfläche ein Popup Menü an, anstatt einen Befehl zu starten. Der Benutzer öffnet einen Befehl, indem er ihn aus dem Menü auswählt. Der folgende Screenshot zeigt eine Dropdown-Schaltfläche und ein Menü von der Internet Explorer-Standard Symbolleiste.

![Screenshot mit dem Dropdown Menü "e-Mail"](images/howto3.jpg)

Sie können einem beliebigen Schaltflächen Stil eine Dropdown-Funktionalität hinzufügen, indem Sie dem **fstyle** -Member der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur der Schaltfläche ein stilflag hinzufügen. Es gibt drei Arten von Dropdown-Schaltflächen, die alle von Internet Explorer verwendet werden:

-   Einfache Dropdown-Schaltflächen haben den [**btns- \_ Dropdown**](toolbar-control-and-button-styles.md) Stil. Sie sehen wie normale Schaltflächen aus, aber Sie zeigen ein Menü an, wenn darauf geklickt wird, anstatt einen Befehl zu starten.
-   Einfache Dropdown Pfeil Schaltflächen haben das btns-Format " [**\_ wholedropdown**](toolbar-control-and-button-styles.md) ". Es wird ein Pfeil neben dem Schaltflächen Bild oder Text angezeigt. Abgesehen von den Unterschieden in der Darstellung sind Sie mit einfachen Dropdown-Schaltflächen identisch. Die Schaltfläche "Mail", die als Beispiel in der obigen Abbildung verwendet wird, ist eine Dropdown-Pfeil Schaltfläche.
-   Dropdown-Pfeil Schaltflächen, die die erweiterte Formatvorlage " [**tbstyle \_ Ex \_ drawddarrows**](toolbar-extended-styles.md) " zur [**btns- \_ Dropdown**](toolbar-control-and-button-styles.md) Liste hinzufügen, haben einen Pfeil, der vom Text oder Bild getrennt ist. Dieser Schaltflächen Stil kombiniert die Funktionalität von Dropdown-und Standard-Schaltflächen. Wenn der Benutzer auf den Pfeil klickt, wird ein Menü angezeigt, und der Benutzer kann mehrere Befehle auswählen. Wenn der Benutzer auf die angrenzende Schaltfläche klickt, wird ein Standardbefehl gestartet. Der folgende Screenshot zeigt die Internet Explorer-Schaltfläche " **zurück** ", die einen getrennten Pfeil verwendet.

    ![Screenshot mit dem Menü der Schaltfläche "zurück teilen"](images/howto4.jpg)

Wenn der Benutzer auf eine Dropdown-Schaltfläche mit den Pfeil Stilen "einfach" oder "einfach" klickt, sendet das Symbolleisten-Steuerelement eine [TBN- \_ Dropdown](tbn-dropdown.md) Benachrichtigung. Wenn Ihre Anwendung diese Nachricht empfängt, ist Sie für das Erstellen und Anzeigen des Menüs sowie für die Verarbeitung des ausgewählten Befehls verantwortlich.

Wenn der Benutzer auf einen getrennten Pfeil klickt, sendet das Symbolleisten-Steuerelement eine [TBN- \_ Dropdown](tbn-dropdown.md) Benachrichtigung an Ihre Anwendung. Die Anwendung sollte Sie auf die gleiche Weise behandeln wie die anderen beiden Dropdown-Schaltflächen. Wenn der Benutzer auf die Haupt Schaltfläche klickt, erhält die Anwendung eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung mit der Befehls-ID der Schaltfläche, so als ob es sich um eine Standard Schaltfläche handelt. Anwendungen Antworten in der Regel, indem Sie den obersten Befehl im Dropdown Menü starten, aber Sie können auf beliebige Weise Antworten.

### <a name="list-style-buttons"></a>List-Style Schaltflächen

Wenn Sie bei Standard Schaltflächen Text hinzufügen, wird dieser unter der Bitmap angezeigt. Der folgende Screenshot zeigt die Internet Explorer-Schaltflächen " **Suchen**" und " **Favoriten** " mit Standard Schaltflächen Text.

![Screenshot mit der Symbolleiste "suchen und Favoriten" mit Standard Schaltflächen](images/howto6.jpg)

Microsoft Internet Explorer 5 und höhere Versionen verwenden den [**tbstyle- \_ Listen**](toolbar-control-and-button-styles.md) Stil. Der Text befindet sich rechts von der Bitmap, wodurch die Höhe der Schaltfläche reduziert und der Anzeigebereich vergrößert wird. In der folgenden Abbildung sind die Schaltflächen für die Internet Explorer 6- **Suche** und- **Favoriten** mit dem **tbstyle- \_ Listen** Stil dargestellt.

![Screenshot der Symbolleiste "suchen und Favoriten" mit Schaltflächen im Listenformat](images/howto5.jpg)

### <a name="chevrons"></a>Spitze Klammern

Wenn der Benutzer die Bänder im Grund leisten-Steuerelement neu anordnet, kann ein Teil einer Symbolleiste abgedeckt werden. Wenn das Band mit dem Format RBBS \_ usechevron erstellt wurde, zeigt das Grund leisten-Steuerelement am rechten Rand der Symbolleiste ein Chevron an. Der Benutzer klickt auf das Chevron, um ein Menü mit den ausgeblendeten Tools anzuzeigen.

### <a name="hot-tracking"></a>Hot-Tracking

Wenn die Hot-Tracking-Funktion aktiviert ist, wird eine Schaltfläche *heiß* , wenn sich der Cursor darüber befindet. Die Schaltfläche "Hot" wird normalerweise von den anderen Schaltflächen auf der Symbolleiste durch ein charakteristisches Bild unterschieden. Standardmäßig wird über dem Rest der Symbolleiste eine Schaltfläche mit dem Häkchen angezeigt. Wenn eine neue Schaltfläche heiß wird, empfängt Ihre Anwendung eine [TBN \_ ](tbn-hotitemchange.md) -""-Benachrichtigung. In der folgenden Abbildung sind die Schaltflächen " **Suchen** " und " **Favoriten** " für Internet Explorer 5 mit der Schaltfläche "Hot **Search** " Zusätzlich zu einer erhöhten Darstellung wurde die graue Bitmap der Schaltfläche durch einen farbigen ersetzt.

![Screenshot mit den Schaltflächen "suchen" und "Favoriten" mit einer Schaltfläche "Hot Search"](images/howto7.jpg)

Um die Hot-Tracking-Datei zu aktivieren, erstellen Sie ein ToolBar-Steuerelement mit dem [**tbstyle \_ Flat**](toolbar-control-and-button-styles.md) -oder [**tbstyle- \_ Listen**](toolbar-control-and-button-styles.md) Stil. Diese werden als *flache* Symbolleisten bezeichnet, da die einzelnen Schaltflächen normalerweise in keiner Weise hervorgehoben werden. Die Bitmaps werden einfach nebeneinander angezeigt. Sie übernehmen eine Schaltfläche, die nur angezeigt wird, wenn Sie heiß sind. Diese beiden Stile sind ebenfalls transparent, was bedeutet, dass der Hintergrund der Symbole die Farbe des zugrunde liegenden Client Fensters ist.

Wenn eine andere Bitmap angezeigt werden soll, wenn die Schaltfläche heiß ist, erstellen Sie eine zweite [Bildliste](image-lists.md) , die für alle Schaltflächen auf der Symbolleiste heiße Bilder enthält. Größe und Reihenfolge dieser Bilder sollten mit denen in der Standard Bildliste identisch sein. Senden Sie das Symbolleisten-Steuerelement eine [**TB \_ SetHotImageList**](tb-sethotimagelist.md) -Nachricht, um die Liste mit den heißen Images festzulegen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Menüleiste für Internet Explorer-Style](cc-faq-iemenubar.md)
</dt> </dl>

 

 