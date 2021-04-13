---
title: Informationen zu Menüs
description: In diesem Thema werden Menüs erläutert.
ms.assetid: fd0b26f1-93cd-421b-9097-8502ab7681e9
keywords:
- Ressourcen, Menüs
- Menüs, Info
- Untermenüs
- Menüleisten
- Menüs der obersten Ebene
- Popupmenüs
- Dropdown Menüs
- Menüs, oberste Ebene
- Menüs, Popup
- Menüs, Dropdown
- Menü Namen
- Menüs, Verknüpfung
- Menüs, Fenster
- Menüs, System
- Menüs, Steuerelemente
- Kontextmenüs
- Menü "Fenster"
- System Menü
- Menü "Steuerung"
- Hilfe Bezeichner
- Menü Handles
- Menüelemente
- Befehls Elemente
- Menü Element Bezeichner
- Position des Menü Elements
- Auswählen von Menü Elementen
- Löschen von Menü Elementen
- vom Besitzer gezeichnete Menüs
- Menüs, gezeichnete Besitzer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed5d42eb42aaaaa16eef0b5b118adcfe0f91156e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390213"
---
# <a name="about-menus"></a>Informationen zu Menüs

Bei einem *Menü* handelt es sich um eine Liste von Elementen, die Optionen oder Gruppen von Optionen (ein Untermenü) für eine Anwendung angeben. Wenn Sie auf ein Menü Element klicken, wird ein Untermenü geöffnet, oder die Anwendung führt einen Befehl aus. Dieser Abschnitt enthält Informationen zu den folgenden Themen:

-   [Menüleisten und Menüs](#menu-bars-and-menus)
    -   [Kontextmenüs](#shortcut-menus)
    -   [Das Menü "Fenster"](#the-window-menu)
    -   [Hilfe Bezeichner](#help-identifier)
-   [Tastatur Zugriff auf Menüs](#keyboard-access-to-menus)
    -   [Standard Tastaturschnittstelle](#standard-keyboard-interface)
    -   [Menü Zugriffstasten](#menu-access-keys)
    -   [Tastenkombinationen für Menüs](#menu-shortcut-keys)
-   [Menüerstellung](#menu-creation)
    -   [Menü Vorlagen Ressourcen](#menu-template-resources)
    -   [Menüvorlage im Speicher](#menu-template-in-memory)
    -   [Menü Handles](#menu-handles)
    -   [Menü Erstellungs Funktionen](#menu-creation-functions)
    -   [Menüanzeige](#menu-display)
    -   [Fenster Klassen Menüs](#window-class-menus)
-   [Menü Elemente](#menu-items)
    -   [Befehls Elemente und Elemente, die Untermenüs öffnen](#command-items-and-items-that-open-submenus)
    -   [Menü Element Bezeichner](#menu-item-identifier)
    -   [Position des Menü Elements](#menu-item-position)
    -   [Programm gesteuertes zugreifen auf Menü Elemente](#accessing-menu-items-programmatically)
    -   [Standardmenü Elemente](#default-menu-items)
    -   [Ausgewählte und Menü Elemente löschen](#selected-and-clear-menu-items)
    -   [Aktivierte, ausgegraut und deaktivierte Menü Elemente](#enabled-grayed-and-disabled-menu-items)
    -   [Markierte Menü Elemente](#highlighted-menu-items)
    -   [Vom Besitzer gezeichnete Menü Elemente](#owner-drawn-menu-items)
    -   [Trennzeichen für Menü Elemente und Zeilenumbrüche](#menu-item-separators-and-line-breaks)
-   [Mit Menüs verwendete Nachrichten](#messages-used-with-menus)
-   [Menü Zerstörung](#menu-destruction)

## <a name="menu-bars-and-menus"></a>Menüleisten und Menüs

Ein Menü wird in einer Hierarchie angeordnet. Auf der obersten Ebene der Hierarchie befindet sich die *Menüleiste*. , das eine Liste von *Menüs* enthält, die wiederum *Untermenüs* enthalten können. Eine Menüleiste wird manchmal als *Menü der obersten Ebene* bezeichnet, und die Menüs und Untermenüs werden auch als *Popup Menüs* bezeichnet.

Ein Menü Element kann entweder einen Befehl ausführen oder ein Untermenü öffnen. Ein Element, das einen Befehl ausführt, wird als *Befehls Element* oder als *Befehl* bezeichnet.

Ein Element in der Menüleiste öffnet fast immer ein Menü. Menüleisten enthalten selten Befehls Elemente. Ein Menü, das in der Menüleiste geöffnet ist, wird von der Menüleiste herunter und auch als *Dropdown Menü* bezeichnet. Wenn ein Dropdown Menü angezeigt wird, wird es an die Menüleiste angefügt. Ein Menü Element in der Menüleiste, das ein Dropdown Menü öffnet, wird auch als *Menüname* bezeichnet.

Die Menü Namen in einer Menüleiste stellen die Hauptkategorien von Befehlen dar, die von einer Anwendung bereitstellt werden. Wenn Sie einen Menünamen in der Menüleiste auswählen, wird in der Regel ein Menü geöffnet, dessen Menü Elemente den Befehlen in einer Kategorie entsprechen. Eine Menüleiste kann z. b. einen **Datei** Menü Namen enthalten, der, wenn der Benutzer darauf klickt, ein Menü mit Menü Elementen, z. b. " **neu**", " **Öffnen**" und " **Speichern**" aktiviert. Zum Abrufen von Informationen zu einer Menüleiste aufrufen Sie [**getmenubarinfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo).

Nur ein überlappendes oder Popup Fenster kann eine Menüleiste enthalten. ein untergeordnetes Fenster darf keines enthalten. Wenn das Fenster über eine Titelleiste verfügt, positioniert das System die Menüleiste direkt darunter. Eine Menüleiste ist immer sichtbar. Ein Untermenü ist jedoch erst sichtbar, wenn der Benutzer ein Menü Element auswählt, das es aktiviert. Weitere Informationen zu überlappenden und Popup Fenstern finden Sie unter [Fenstertypen](/windows/desktop/winmsg/window-features).

Jedes Menü muss über ein Besitzer Fenster verfügen. Das System sendet Nachrichten an das Besitzer Fenster eines Menüs, wenn der Benutzer das Menü auswählt oder im Menü ein Element auswählt.

In diesem Abschnitt werden die folgenden Themen behandelt.

-   [Kontextmenüs](#shortcut-menus)
-   [Das Menü "Fenster"](#the-window-menu)
-   [Hilfe Bezeichner](#help-identifier)

### <a name="shortcut-menus"></a>Kontextmenüs

Das System stellt auch Kontext *Menüs* bereit. Ein Kontextmenü ist nicht an die Menüleiste angefügt. Sie kann überall auf dem Bildschirm angezeigt werden. In einer Anwendung wird in der Regel ein Kontextmenü mit einem Teil eines Fensters verknüpft, z. b. dem Client Bereich oder einem bestimmten Objekt, z. b. einem Symbol. Aus diesem Grund werden diese Menüs auch als *Kontextmenüs* bezeichnet.

Ein Kontextmenü bleibt ausgeblendet, bis der Benutzer es aktiviert. in der Regel Klicken Sie mit der rechten Maustaste auf eine Auswahl, eine Symbolleiste oder auf eine Task leisten Schaltfläche. Das Menü wird normalerweise an der Position der Einfügemarke oder des Mauszeigers angezeigt.

### <a name="the-window-menu"></a>Das Menü "Fenster"

Das Menü **Fenster** (auch als **Systemmenü** oder **Steuer** Element Menü bezeichnet) ist ein Popupmenü, das fast exklusiv vom Betriebs System definiert und verwaltet wird. Der Benutzer kann das Menü Fenster öffnen, indem er auf das Anwendungssymbol auf der Titelleiste klickt oder mit der rechten Maustaste auf eine beliebige Stelle in der Titelleiste klickt.

Das Menü **Fenster** enthält eine Standardgruppe von Menü Elementen, die der Benutzer auswählen kann, um die Größe oder Position eines Fensters zu ändern oder die Anwendung zu schließen. Elemente im Menü Fenster können hinzugefügt, gelöscht und geändert werden, aber die meisten Anwendungen verwenden nur den Standardsatz von Menü Elementen. Ein überlappendes, Popup-oder untergeordnetes Fenster kann über ein Fenstermenü verfügen. Es ist nicht üblich, dass ein überlappendes oder ein Popup Fenster ein Fenstermenü enthält.

Wenn der Benutzer im Menü **Fenster** einen Befehl auswählt, sendet das System eine [**WM- \_ syscommand**](wm-syscommand.md) -Meldung an das Besitzer Fenster des Menüs. In den meisten Anwendungen verarbeitet die Fenster Prozedur keine Meldungen aus dem Menü Fenster. Stattdessen übergibt Sie die Nachrichten einfach an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion für die System Standard Verarbeitung der Nachricht. Wenn eine Anwendung dem Menü Fenster einen Befehl hinzufügt, muss die Fenster Prozedur den Befehl verarbeiten.

Eine Anwendung kann die [**getsystemmenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) -Funktion verwenden, um eine Kopie des Standardmenü Fensters zu erstellen, das geändert werden soll. Jedes Fenster, in dem die **getsystemmenu** -Funktion nicht verwendet wird, um eine eigene Kopie des Menü Fensters zu erstellen, erhält das Standardfenster Menü.

### <a name="help-identifier"></a>Hilfe Bezeichner

Der einzelnen Menüleiste, dem Menü, dem Untermenü und dem Kontextmenü ist ein Hilfe Bezeichner zugeordnet. Wenn der Benutzer die F1-Taste drückt, während das Menü aktiv ist, wird dieser Wert als Teil einer [**WM- \_ Hilfe**](../shell/wm-help.md) Nachricht an das Besitzer Fenster gesendet.

## <a name="keyboard-access-to-menus"></a>Tastatur Zugriff auf Menüs

Das System stellt eine Standardtastatur Schnittstelle für Menüs bereit. Sie können diese Schnittstelle verbessern, indem Sie für Ihre Menü Elemente mnetmonische Zugriffstasten und Tastenkombinationen (Zugriffstasten) bereitstellen.

In den folgenden Themen werden die Standardtastatur Schnittstelle, Zugriffstasten und Tastenkombinationen beschrieben:

-   [Standard Tastaturschnittstelle](#standard-keyboard-interface)
-   [Menü Zugriffstasten](#menu-access-keys)
-   [Tastenkombinationen für Menüs](#menu-shortcut-keys)

### <a name="standard-keyboard-interface"></a>Standard Tastaturschnittstelle

Das System ist so konzipiert, dass es mit oder ohne Maus oder einem anderen Zeigegerät funktioniert. Da das System eine standardmäßige Tastaturschnittstelle bereitstellt, kann der Benutzer die Tastatur verwenden, um Menü Elemente auszuwählen. Diese Tastaturschnittstelle benötigt keinen speziellen Code. Eine Anwendung empfängt eine Befehls Meldung, ob der Benutzer ein Menü Element über die Tastatur oder mithilfe einer Maus auswählt. Die Standardtastatur Schnittstelle verarbeitet die folgenden Tastatureingaben.



| Tastatureingabe              | Aktion                                                                                                                                                                                                                                   |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Alphabetisches Zeichen | Wählt das erste Menü Element mit dem angegebenen Zeichen als Zugriffsschlüssel aus. Wenn das ausgewählte Element ein Menü aufruft, wird das Menü angezeigt, und das erste Element wird hervorgehoben. Andernfalls wird das Menü Element ausgewählt.                            |
| ALT                    | Schaltet den Menüleisten Modus ein und aus.                                                                                                                                                                                                     |
| ALT+LEERTASTE           | Zeigt das Fenstermenü an.                                                                                                                                                                                                                |
| EINGABETASTE                  | Aktiviert ein Menü und wählt das erste Menü Element aus, wenn ein Element einem Element zugeordnet ist. Andernfalls wählt diese Tastenkombination das Element so aus, als ob der Benutzer die Maustaste losgelassen hat, während das Element ausgewählt wurde.                              |
| ESC                    | Beendet den Menü Modus.                                                                                                                                                                                                                         |
| NACH-LINKS-TASTE             | Wechselt zum vorherigen Menü Element der obersten Ebene. Menü Elemente der obersten Ebene enthalten Menü Namen und das Menü Fenster. Wenn das ausgewählte Element in einem Menü angezeigt wird, wird die vorherige Spalte im Menü ausgewählt, oder das vorherige Menü Element der obersten Ebene ist ausgewählt. |
| NACH-RECHTS-TASTE            | Funktioniert wie die nach-links-Taste, außer in umgekehrter Richtung. In Menüs verschiebt diese Tastenkombination eine Spalte vorwärts. Wenn sich das aktuell ausgewählte Element in der Spalte ganz rechts befindet, wird das nächste Menü ausgewählt.                              |
| Pfeile nach oben oder nach unten      | Aktiviert ein Menü, wenn in einem Menünamen gedrückt. Wenn Sie in einem Menü gedrückt werden, wählt der nach-oben-Taste das vorherige Element aus. mit der nach-unten-Taste wird das nächste Element ausgewählt.                                                                  |



 

### <a name="menu-access-keys"></a>Menü Zugriffstasten

Die Standardtastatur Schnittstelle für Menüs kann durch Hinzufügen von Zugriffs Schlüsseln (mnetmonics) zu Menü Elementen erweitert werden. Bei einer Zugriffstaste handelt es sich um einen unterstrichenen Buchstaben im Text eines Menü Elements. Wenn ein Menü aktiv ist, kann der Benutzer ein Menü Element auswählen, indem er die Taste drückt, die dem unterstrichenen Buchstaben des Elements entspricht. Der Benutzer aktiviert die Menüleiste durch Drücken der Alt-Taste, um das erste Element in der Menüleiste hervorzuheben. Ein Menü ist aktiv, wenn es angezeigt wird.

Um einen Zugriffsschlüssel für ein Menü Element zu erstellen, stellen Sie einem beliebigen Zeichen in der Text Zeichenfolge des Elements ein kaufmännisches und-Zeichen voran. Beispielsweise bewirkt die Text Zeichenfolge "&Move", dass das System den Buchstaben "M" unterstreicht.

### <a name="menu-shortcut-keys"></a>Tastenkombinationen für Menüs

Zusätzlich zu einer Zugriffstaste kann einem Menü Element eine Tastenkombination zugeordnet werden. Eine Tastenkombination unterscheidet sich von einer Zugriffstaste, da das Menü nicht aktiv sein muss, damit die Tastenkombination funktioniert. Außerdem ist eine Zugriffstaste *immer* einem Menü Element zugeordnet, während eine Tastenkombination *in der Regel* (aber nicht muss) einem Menü Element zugeordnet ist.

Text, der die Tastenkombination identifiziert, wird der Text Zeichenfolge für das Menü Element hinzugefügt. Der Kontext Text wird rechts neben dem Menü Elementnamen angezeigt, nach einem umgekehrten Schrägstrich und einem Tabstopp Zeichen ( \\ t). Beispielsweise stellt "&close \\ Talt + F4" einen Close-Befehl mit der Tastenkombination ALT + F4 als Tastenkombination und mit dem Buchstaben "C" als Zugriffstaste dar. Weitere Informationen finden Sie unter [Tastaturbeschleuniger](keyboard-accelerators.md).

## <a name="menu-creation"></a>Menüerstellung

Sie können ein Menü erstellen, indem Sie entweder eine Menüvorlage oder Menü Erstellungs Funktionen verwenden. Menü Vorlagen werden in der Regel als Ressourcen definiert. Menü Vorlagen Ressourcen können explizit geladen oder als Standardmenü für eine Fenster Klasse zugewiesen werden. Sie können Menü Vorlagen Ressourcen auch dynamisch im Arbeitsspeicher erstellen.

In den folgenden Themen wird die Menüerstellung ausführlich beschrieben:

-   [Menü Vorlagen Ressourcen](#menu-template-resources)
-   [Menüvorlage im Speicher](#menu-template-in-memory)
-   [Menü Handles](#menu-handles)
-   [Menü Erstellungs Funktionen](#menu-creation-functions)
-   [Menüanzeige](#menu-display)
-   [Fenster Klassen Menüs](#window-class-menus)

### <a name="menu-template-resources"></a>Menü Vorlagen Ressourcen

Die meisten Anwendungen erstellen Menüs mithilfe von Menü Vorlagen Ressourcen. Eine *Menüvorlage* definiert ein Menü, einschließlich der Elemente in der Menüleiste und aller Menüs. Weitere Informationen zum Erstellen einer Menü Vorlagen Ressource finden Sie in der Dokumentation, die in ihren Entwicklungs Tools enthalten ist.

Nachdem Sie eine Menü Vorlagen Ressource erstellt und der ausführbaren Datei (exe-Datei) Ihrer Anwendung hinzugefügt haben, können Sie die [**loadmenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) -Funktion verwenden, um die Ressource in den Arbeitsspeicher zu laden. Diese Funktion gibt ein Handle für das Menü zurück, das Sie dann mithilfe der [**setMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) -Funktion einem Fenster zuweisen können. Sie können einem beliebigen Fenster ein Menü zuweisen, das kein untergeordnetes Fenster ist.

Das Implementieren von Menüs als Ressourcen vereinfacht die Lokalisierung einer Anwendung für die Verwendung in mehreren Ländern/Regionen. Nur die Ressourcen Definitionsdatei muss für jede Sprache lokalisiert werden, nicht für den Quellcode der Anwendung.

### <a name="menu-template-in-memory"></a>Menüvorlage im Speicher

Ein Menü kann aus einer Menüvorlage erstellt werden, die zur Laufzeit in den Arbeitsspeicher integriert ist. Beispielsweise kann eine Anwendung, die einem Benutzer das Anpassen des Menüs ermöglicht, basierend auf den Benutzereinstellungen eine Menüvorlage im Arbeitsspeicher erstellen. Die Anwendung kann die Vorlage dann für die spätere Verwendung in einer Datei oder in der Registrierung speichern. Verwenden Sie die [**loadmenuindirekte**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) -Funktion, um ein Menü aus einer Vorlage im Arbeitsspeicher zu erstellen. Beschreibungen von Menü Vorlagen Formaten finden Sie unter [Menü Vorlagen Ressourcen](#menu-template-resources).

Eine Standardmenü Vorlage besteht aus einer [**menuitemtemplateheader**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) -Struktur, gefolgt von einer oder mehreren [**menuitemtemplate**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) -Strukturen.

Eine erweiterte Menüvorlage besteht aus einer [**menuex- \_ Vorlagen \_ Header**](menuex-template-header.md) Struktur, gefolgt von einer oder mehreren [**menuex- \_ Vorlagen \_ Element**](menuex-template-item.md) Strukturen.

### <a name="menu-handles"></a>Menü Handles

Das System generiert für jedes Menü einen eindeutigen handle. Ein *Menü handle* ist ein Wert des **HMENU** -Typs. Eine Anwendung muss ein Menü Handle in vielen der Menüfunktionen angeben. Sie erhalten ein Handle für eine Menüleiste, wenn Sie das Menü Erstellen oder eine Menü Ressource laden.

Zum Abrufen eines Handles für die Menüleiste eines Menüs, das erstellt oder geladen wurde, verwenden Sie die [**getMenu**](/windows/desktop/api/Winuser/nf-winuser-getmenu) -Funktion. Zum Abrufen eines Handles für das unter Menü, das einem Menü Element zugeordnet ist, verwenden Sie die [**getsubmenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) -oder [**getmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) -Funktion. Um ein Handle für ein Fenstermenü abzurufen, verwenden Sie die [**getsystemmenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) -Funktion.

### <a name="menu-creation-functions"></a>Menü Erstellungs Funktionen

Mithilfe von Menü Erstellungs Funktionen können Sie Menüs zur Laufzeit erstellen oder Menü Elemente zu vorhandenen Menüs hinzufügen. Sie können die Funktion " [**anatemenu**](/windows/desktop/api/Winuser/nf-winuser-createmenu) " verwenden, um eine leere Menüleiste zu erstellen, und die Funktion " [**kreatepopupmenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) ", um ein leeres Menü zu erstellen. Sie können bestimmte Einstellungs Informationen für ein Menü mithilfe der [**menuinfo**](/windows/win32/api/winuser/ns-winuser-menuinfo) -Struktur speichern. Verwenden Sie [**getmenuinfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo) oder [**setmenuinfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo), um die Einstellungen eines Menüs abzurufen oder abzurufen. Verwenden Sie zum Hinzufügen von Elementen zu einem Menü die [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) -Funktion. Die älteren [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) -und [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) -Funktionen werden weiterhin unterstützt, aber **InsertMenuItem** sollte für neue Anwendungen verwendet werden.

### <a name="menu-display"></a>Menüanzeige

Nachdem ein Menü geladen oder erstellt wurde, muss es einem Fenster zugewiesen werden, bevor es vom System angezeigt werden kann. Sie können ein Menü zuweisen, indem Sie ein Klassen Menü definieren. Weitere Informationen finden Sie unter [Fenster Klassen Menüs](#window-class-menus). Sie können ein Menü auch einem Fenster zuweisen, indem Sie ein Handle für das Menü als *HMENU* -Parameter der [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) -oder [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) -Funktion angeben oder indem Sie die [**setMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) -Funktion aufrufen.

Verwenden Sie die [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) -Funktion, um ein Kontextmenü anzuzeigen. Kontextmenüs, auch als unverankerte Popup Menüs oder Kontextmenüs bezeichnet, werden normalerweise angezeigt, wenn die ""-" [**\_ ContextMenu**](wm-contextmenu.md) "-Nachricht verarbeitet wird.

Sie können einem beliebigen Fenster ein Menü zuweisen, das kein untergeordnetes Fenster ist.

Die ältere [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) -Funktion wird weiterhin unterstützt, aber neue Anwendungen sollten die [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) -Funktion verwenden.

### <a name="window-class-menus"></a>Fenster Klassen Menüs

Sie können ein Standardmenü, das als *Klassen Menü bezeichnet wird,* beim Registrieren einer Fenster Klasse angeben. Zu diesem Zweck weisen Sie den Namen der Menü Vorlagen Ressource dem **lpszmenuname** -Member der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur zu, die zum Registrieren der Klasse verwendet wird.

Standardmäßig wird jedem Fenster das Klassen Menü für die Fenster Klasse zugewiesen, sodass Sie das Menü nicht explizit laden und jedem Fenster zuweisen müssen. Sie können das Klassen Menü überschreiben, indem Sie einen anderen Menü Zieh Punkt in einem aufzurufenden Befehl an die Funktion " [**roatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " angeben Sie können auch das Menü eines Fensters ändern, nachdem es mithilfe der [**setMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) -Funktion erstellt wurde. Weitere Informationen finden Sie unter [Fenster Klassen](/windows/desktop/winmsg/window-classes).

## <a name="menu-items"></a>Menüelemente

In den folgenden Themen wird erläutert, was das System bewirkt, wenn der Benutzer ein Menü Element auswählt, und wie eine Anwendung das Aussehen und die Funktionalität eines Elements steuern kann:

-   [Befehls Elemente und Elemente, die Untermenüs öffnen](#command-items-and-items-that-open-submenus)
-   [Menü Element Bezeichner](#menu-item-identifier)
-   [Position des Menü Elements](#menu-item-position)
-   [Programm gesteuertes zugreifen auf Menü Elemente](#accessing-menu-items-programmatically)
-   [Standardmenü Elemente](#default-menu-items)
-   [Ausgewählte und Menü Elemente löschen](#selected-and-clear-menu-items)
-   [Aktivierte, ausgegraut und deaktivierte Menü Elemente](#enabled-grayed-and-disabled-menu-items)
-   [Markierte Menü Elemente](#highlighted-menu-items)
-   [Vom Besitzer gezeichnete Menü Elemente](#owner-drawn-menu-items)
-   [Trennzeichen für Menü Elemente und Zeilenumbrüche](#menu-item-separators-and-line-breaks)

### <a name="command-items-and-items-that-open-submenus"></a>Befehls Elemente und Elemente, die Untermenüs öffnen

Wenn der Benutzer ein Befehls Element auswählt, sendet das System eine Befehls Meldung an das Fenster, das das Menü besitzt. Wenn sich das Befehls Element im Menü Fenster befindet, sendet das System die [**WM- \_ syscommand**](wm-syscommand.md) -Nachricht. Andernfalls sendet Sie die [**WM- \_ Befehls**](wm-command.md) Nachricht.

Jedem Menü Element, das ein Untermenü öffnet, ist ein Handle für das entsprechende Untermenü zugeordnet. Wenn der Benutzer auf ein solches Element zeigt, öffnet das System das Untermenü. Es wird keine Befehls Meldung an das Besitzer Fenster gesendet. Das System sendet jedoch eine [**WM- \_ initmenupopup**](wm-initmenupopup.md) -Meldung an das Besitzer Fenster, bevor das Untermenü angezeigt wird. Sie können ein Handle für das unter Menü, das einem Element zugeordnet ist, mithilfe der [**getsubmenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) -Funktion oder der [**getmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) -Funktion erhalten.

Eine Menüleiste enthält in der Regel Menü Namen, aber Sie kann auch Befehls Elemente enthalten. Ein Untermenü enthält in der Regel Befehls Elemente, es kann aber auch Elemente enthalten, die Untermenüs öffnen. Durch Hinzufügen dieser Elemente zu Untermenüs können Sie Menüs in beliebiger tiefe schachteln. Um einen visuellen Hinweis für den Benutzer bereitzustellen, zeigt das System automatisch einen kleinen Pfeil rechts neben dem Text eines Menü Elements an, das ein Untermenü öffnet.

### <a name="menu-item-identifier"></a>Menu-Item Bezeichner

Jedes Menü Element ist eine eindeutige, von der Anwendung definierte ganze Zahl, die als *Menü Element Bezeichner* bezeichnet wird. Wenn der Benutzer ein Befehls Element aus einem Menü auswählt, sendet das System den Bezeichner des Elements als Teil einer [**WM- \_ Befehls**](wm-command.md) Meldung an das Besitzer Fenster. Die Fenster Prozedur überprüft den Bezeichner, um die Quelle der Nachricht zu bestimmen, und verarbeitet die Nachricht entsprechend. Darüber hinaus können Sie ein Menü Element mithilfe seines Bezeichners angeben, wenn Sie Menüfunktionen aufzurufen. beispielsweise, um ein Menü Element zu aktivieren oder zu deaktivieren.

Menü Elemente, die Untermenüs öffnen, weisen Bezeichner auf, ebenso wie Befehls Elemente. Das System sendet jedoch keine Befehls Meldung, wenn ein solches Element aus einem Menü ausgewählt wird. Stattdessen öffnet das System das Untermenü, das dem Menü Element zugeordnet ist.

Um den Bezeichner des Menü Elements an einer bestimmten Position abzurufen, verwenden Sie die [**getmenuitemid**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid) -oder [**getmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) -Funktion.

### <a name="menu-item-position"></a>Menu-Item Position

Zusätzlich zu einem eindeutigen Bezeichner weist jedes Menü Element in einer Menüleiste oder einem Menü einen eindeutigen Positionswert auf. Das äußerste Element in einer Menüleiste oder das oberste Element in einem Menü hat die Position 0 (null). Der Positionswert wird für nachfolgende Menü Elemente inkrementiert. Das System weist allen Elementen in einem Menü einen Positionswert zu, einschließlich Trennzeichen. Die folgende Abbildung zeigt die Positionswerte von Elementen in einer Menüleiste und in einem Menü.

![Menüleiste und Menü](images/csemn-01.png)

Wenn Sie eine Menüfunktion aufrufen, die Informationen zu einem bestimmten Menü Element ändert oder abruft, können Sie das Element entweder mithilfe seines Bezeichners oder seiner Position angeben. Weitere Informationen finden Sie im nächsten Abschnitt.

### <a name="accessing-menu-items-programmatically"></a>Programm gesteuertes zugreifen auf Menü Elemente

Mit den meisten Menüfunktionen können Sie ein Menü Element entweder über die Position oder den Befehl angeben. Einige Funktionen verwenden die **MF- \_ byposition** -und **MF- \_ bycommand** -Flags, um den Suchalgorithmus anzugeben; andere verfügen über einen expliziten *fbyposition* -Parameter. Wenn Sie das Menü Element nach Position angeben, ist die Element Nummer ein NULL basierter Index im Menü. Wenn Sie das Menü Element nach Befehl angeben, werden das Menü und seine Untermenüs nach einem Element durchsucht, dessen Menü Bezeichner gleich der angegebenen Element Nummer ist. Wenn mehr als ein Element in der Menühierarchie mit der Element Nummer übereinstimmt, wird nicht angegeben, welches Element verwendet wird. Wenn die Menüs doppelte Menü Bezeichner enthalten, sollten Sie Positions basierte Menü Vorgänge verwenden, um diese Mehrdeutigkeit zu vermeiden.

### <a name="default-menu-items"></a>Standardmenü Elemente

Ein Untermenü kann ein Standardmenü Element enthalten. Wenn der Benutzer ein Untermenü durch Doppelklicken öffnet, sendet das System eine Befehls Meldung an das Besitzer Fenster des Menüs und schließt das Menü so, als ob das Standard Befehls Element ausgewählt wurde. Wenn kein Standard Befehls Element vorhanden ist, bleibt das Untermenü geöffnet. Um das Standardelement für ein Untermenü abzurufen und festzulegen, verwenden Sie die Funktionen [**getmenudefaultitem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem) und [**setmenudefaultitem**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem) .

### <a name="selected-and-clear-menu-items"></a>Ausgewählte und Menü Elemente löschen

Ein Menü Element kann entweder ausgewählt oder gelöscht werden. Das System zeigt eine Bitmap neben den ausgewählten Menü Elementen an, um den ausgewählten Zustand anzuzeigen. Das System zeigt keine Bitmap nebenelemente löschen an, es sei denn, eine von der Anwendung definierte "Clear"-Bitmap wird angegeben. Nur Menü Elemente in einem Menü können ausgewählt werden. Elemente in einer Menüleiste können nicht ausgewählt werden.

Anwendungen aktivieren oder löschen in der Regel ein Menü Element, um anzugeben, ob eine Option aktiviert ist. Angenommen, eine Anwendung verfügt über eine Symbolleiste, die der Benutzer mit einem **Toolbar** -Befehl in einem Menü anzeigen oder ausblenden kann. Wenn die Symbolleiste ausgeblendet ist, ist das Menü Element für die **Symbolleiste** deaktiviert. Wenn der Benutzer den Befehl auswählt, überprüft die Anwendung das Menü Element und zeigt die Symbolleiste an.

Mit einem Häkchen-Attribut wird gesteuert, ob ein Menü Element ausgewählt ist. Mithilfe der [**checkmenuitem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) -Funktion können Sie das Häkchen Attribut eines Menü Elements festlegen. Sie können die [**getmenustate**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) -Funktion verwenden, um zu bestimmen, ob ein Menü Element derzeit ausgewählt oder gelöscht ist.

Anstelle von " [**checkmenuitem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) " und " [**getmenustate**](/windows/desktop/api/Winuser/nf-winuser-getmenustate)" können Sie die Funktionen " [**getmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) " und " [**setmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) " verwenden, um den Überprüfungs Zustand eines Menü Elements abzurufen und festzulegen.

Manchmal entspricht eine Gruppe von Menü Elementen einem Satz von Optionen, die sich gegenseitig ausschließen. In diesem Fall können Sie die ausgewählte Option angeben, indem Sie ein ausgewähltes Optionsfeld Element (analog zu einem Optionsfeld-Steuerelement) verwenden. Ausgewählte Options Felder werden mit einer Aufzählungs Bitmap anstelle einer Bitmap für das Häkchen angezeigt. Verwenden Sie die [**checkmenuradioitem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) -Funktion, um ein Menü Element zu überprüfen und es als Radio Element festzulegen.

Standardmäßig zeigt das System ein Häkchen oder eine Aufzählungs Bitmap neben ausgewählte Menü Elemente und keine Bitmap neben gelöschten Menü Elementen an. Sie können jedoch die [**setmenuitembitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) -Funktion verwenden, um Anwendungs definierte und gelöschte Bitmaps einem Menü Element zuzuordnen. Das System verwendet dann die angegebenen Bitmaps, um den Status des ausgewählten oder gelöschten Menü Elements anzugeben.

Anwendungs definierte Bitmaps, die einem Menü Element zugeordnet sind, müssen die gleiche Größe wie die Standard Bitmap für das Häkchen aufweisen. die Dimensionen, die je nach Bildschirmauflösung variieren können, müssen identisch sein. Verwenden Sie die [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion, um die richtigen Dimensionen abzurufen. Sie können mehrere Bitmapressourcen für verschiedene Bildschirmauflösungen erstellen. Erstellen Sie eine Bitmap-Ressource, und Skalieren Sie Sie bei Bedarf. oder erstellen Sie zur Laufzeit eine Bitmap, und zeichnen Sie ein Bild darin. Die Bitmaps können entweder monochrome oder Color sein. Da Menü Elemente jedoch beim hervorheben umgekehrt werden, ist die Darstellung bestimmter invertierter Farb Bitmaps möglicherweise nicht erwünscht. Weitere Informationen finden Sie unter [Bitmaps](/windows/desktop/gdi/bitmaps).

### <a name="enabled-grayed-and-disabled-menu-items"></a>Aktivierte, ausgegraut und deaktivierte Menü Elemente

Ein Menü Element kann aktiviert, abgeblendet oder deaktiviert werden. Standardmäßig ist ein Menü Element aktiviert. Wenn der Benutzer ein aktiviertes Menü Element auswählt, sendet das System eine Befehls Meldung an das Besitzer Fenster oder zeigt das entsprechende Untermenü an, je nachdem, welche Art von Menü Element es darstellt.

Wenn für den Benutzer keine Menü Elemente verfügbar sind, sollten diese abgeblendet oder deaktiviert sein. Ausgegraute und deaktivierte Menü Elemente können nicht ausgewählt werden. Ein deaktiviertes Element sieht genau wie ein aktiviertes Element aus. Wenn der Benutzer auf ein deaktiviertes Element klickt, wird das Element nicht ausgewählt, und es passiert nichts. Deaktivierte Elemente können z. b. in einem Tutorial nützlich sein, das ein Menü anzeigt, das aktiv ist, aber nicht ist.

Eine Anwendung ist ein nicht verfügbares Menü Element, um dem Benutzer einen visuellen Hinweis zu geben, dass ein Befehl nicht verfügbar ist. Sie können ein ausgegrautes Element verwenden, wenn eine Aktion nicht geeignet ist (Sie können z. b. den Befehl **Drucken** im Menü **Datei** grauen, wenn auf dem System kein Drucker installiert ist).

Die [**EnableMenuItem**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem) -Funktion aktiviert oder deaktiviert ein Menü Element. Verwenden Sie die [**getmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) -Funktion, um zu bestimmen, ob ein Menü Element aktiviert, abgeblendet oder deaktiviert ist.

Anstelle von [**getmenuiteminfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)können Sie auch die [**getmenustate**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) -Funktion verwenden, um zu bestimmen, ob ein Menü Element aktiviert, ausgegraut oder deaktiviert ist.

### <a name="highlighted-menu-items"></a>Markierte Menü Elemente

Die Menü Elemente in Menüs werden vom System automatisch hervorgehoben, wenn Sie vom Benutzer ausgewählt werden. Mithilfe der [**hilitemenuitem**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem) -Funktion kann jedoch eine Hervorhebung explizit hinzugefügt oder aus einem Menünamen in der Menüleiste entfernt werden. Diese Funktion hat keine Auswirkungen auf Menü Elemente in Menüs. Wenn **hilitemenuitem** zum Markieren eines Menü namens verwendet wird, wird der Name jedoch nur angezeigt. Wenn der Benutzer die EINGABETASTE drückt, wird das hervorgehobene Element nicht ausgewählt. Diese Funktion kann beispielsweise in einer Schulungs Anwendung nützlich sein, die die Verwendung von Menüs veranschaulicht.

### <a name="owner-drawn-menu-items"></a>Menü Elemente Owner-Drawn

Eine Anwendung kann die Darstellung eines Menü Elements vollständig steuern, indem ein vom *Besitzer gezeichnetes Element* verwendet wird. Für Besitzer gezeichnete Elemente ist es erforderlich, dass eine Anwendung für das Zeichnen ausgewählter (hervorgehobener), ausgewählter und gelöschter Zustände verantwortlich ist. Wenn eine Anwendung z. b. ein Schriftart Menü bereitgestellt hat, könnte Sie jedes Menü Element mit der entsprechenden Schriftart zeichnen. das Element für Roman würde mit Roman gezeichnet werden, das Element für kursiv Schrift wird kursiv dargestellt usw. Weitere Informationen finden Sie unter [Erstellen von Owner-Drawn Menü Elementen](using-menus.md).

### <a name="menu-item-separators-and-line-breaks"></a>Trennzeichen für Menü Elemente und Zeilenumbrüche

Das System stellt eine besondere Art von Menü Element bereit, das als *Trenn* Zeichen bezeichnet wird, das als horizontale Linie angezeigt wird. Sie können ein Trennzeichen verwenden, um ein Menü in Gruppen verwandter Elemente aufzuteilen. Ein Trennzeichen kann nicht in einer Menüleiste verwendet werden, und der Benutzer kann kein Trennzeichen auswählen.

Wenn eine Menüleiste mehr Menü Namen enthält, als in eine Zeile passen, umschließt das System die Menüleiste, indem es automatisch in zwei oder mehr Zeilen unterteilt wird. Sie können bewirken, dass ein Zeilenumbruch an einem bestimmten Element in einer Menüleiste auftritt, indem Sie dem Element das Flag " **MFT \_ menubreak** Type" zuweisen. Das System platziert dieses Element und alle nachfolgenden Elemente in einer neuen Zeile.

Wenn ein Menü mehr Elemente enthält, als in eine Spalte passen, wird das Menü abgeschnitten. Sie können bewirken, dass ein Spalten Umbruch an einem bestimmten Element in einem Menü auftritt, indem Sie dem Element das Flag " **MFT \_ menubreak** Type" zuweisen oder die Option menubreak in der [MenuItem](/windows/desktop/menurc/menuitem-statement) -Anweisung verwenden. Das System platziert dieses Element und alle nachfolgenden Elemente in einer neuen Spalte. Das Flag " **MFT \_ menubarbreak** Type" hat denselben Effekt, mit der Ausnahme, dass eine vertikale Linie zwischen der neuen Spalte und der alten angezeigt wird.

Wenn Sie die Funktionen [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)oder [**modifymenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) zum Zuweisen von Zeilenumbrüchen verwenden, sollten Sie die Typflags **MF \_ menubreak** oder **MF \_ menubarbreak** zuweisen.

## <a name="messages-used-with-menus"></a>Mit Menüs verwendete Nachrichten

Das System meldet eine Menü bezogene Aktivität, indem Meldungen an die Fenster Prozedur des Fensters gesendet werden, das das Menü besitzt. Das System sendet eine Reihe von Nachrichten, wenn der Benutzer Elemente in der Menüleiste auswählt oder mit der rechten Maustaste ein Kontextmenü anzeigt.

Wenn der Benutzer ein Element in der Menüleiste aktiviert, empfängt das Besitzer Fenster zuerst eine [**WM- \_ syscommand**](wm-syscommand.md) -Nachricht. Diese Meldung enthält ein Flag, das angibt, ob der Benutzer das Menü mithilfe der Tastatur (SC \_ keymenu) oder der Maus (SC \_ mousemenu) aktiviert hat. Weitere Informationen finden Sie unter [Tastatur Zugriff auf Menüs](#keyboard-access-to-menus).

Als nächstes sendet das System vor dem Anzeigen von Menüs die " [**WM \_ InitMenu**](wm-initmenu.md) "-Meldung an die Fenster Prozedur, sodass eine Anwendung die Menüs ändern kann, bevor Sie dem Benutzer angezeigt werden. Das System sendet die **WM- \_ InitMenu** -Nachricht nur einmal pro Menü Aktivierung.

Wenn der Benutzer auf ein Menü Element verweist, das ein Untermenü öffnet, sendet das System das Besitzer Fenster an die " [**WM \_ initmenupopup**](wm-initmenupopup.md) "-Meldung, bevor das Untermenü angezeigt wird. Diese Meldung gibt der Anwendung die Möglichkeit, das Untermenü zu ändern, bevor es angezeigt wird.

Jedes Mal, wenn der Benutzer die Hervorhebung von einem Element zu einem anderen verschiebt, sendet das System eine [**WM- \_ MenuSelect**](wm-menuselect.md) -Meldung an die Fenster Prozedur des Besitzer Fensters des Menüs. Diese Meldung identifiziert das aktuell ausgewählte Menü Element. Viele Anwendungen stellen einen Informationsbereich am unteren Rand der Hauptfenster bereit und verwenden diese Meldung, um zusätzliche Informationen zum ausgewählten Menü Element anzuzeigen.

Wenn der Benutzer ein Befehls Element aus einem Menü auswählt, sendet das System eine [**WM- \_ Befehls**](wm-command.md) Meldung an die Fenster Prozedur. Das nieder wertige Wort des *wParam* -Parameters der **WM- \_ Befehls** Nachricht enthält den Bezeichner des ausgewählten Elements. Die Fenster Prozedur sollte den Bezeichner überprüfen und die Nachricht entsprechend verarbeiten.

Sie können Informationen für ein Menü mithilfe der [**menuinfo**](/windows/win32/api/winuser/ns-winuser-menuinfo) -Struktur speichern. , Wenn das Menü mit **menuinfo** definiert ist. der **dwstyle** -Wert von MNS \_ notifybypos, das System sendet [**WM \_ MenuCommand**](wm-menucommand.md) anstelle des [**WM- \_ Befehls**](wm-command.md) , wenn ein Element ausgewählt wird. Auf diese Weise können Sie auf die Informationen in der **menuinfo** -Struktur zugreifen und auch den Index des ausgewählten Elements direkt bereitstellen.

Nicht alle Menüs sind über die Menüleiste eines Fensters zugänglich. Viele Anwendungen zeigen Kontextmenüs an, wenn der Benutzer an einem bestimmten Speicherort auf die Rechte Maustaste klickt. Solche Anwendungen sollten die [**WM- \_ ContextMenu**](wm-contextmenu.md) -Meldung verarbeiten und ggf. ein Kontextmenü anzeigen. Wenn eine Anwendung kein **\_ Kontext** Menü anzeigt, sollte Sie der " [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) "-Funktion zur Standard Verarbeitung die ".

Die WM-Meldung " [**\_ menurbuttonup**](wm-menurbuttonup.md) " wird gesendet, wenn der Benutzer die Rechte Maustaste loslässt, während sich der Cursor auf einem Menü Element befindet. Diese Meldung wird bereitgestellt, damit Anwendungen ein Kontext abhängiger Kontextmenü oder ein Kontextmenü für ein Menü Element anzeigen können.

Es gibt einige Nachrichten, die nur Drag & Drop-Menüs einschließen. Das " [**WM \_ menugetobject**](wm-menugetobject.md) " wird an den Besitzer eines Drag & Drop-Menüs gesendet, wenn der Mauszeiger in ein Menü Element oder von der Mitte eines Elements nach oben oder unten verschoben wird. Die [**WM- \_ menudrag**](wm-menudrag.md) -Nachricht wird gesendet, wenn der Benutzer tatsächlich ein Menü Element zieht.

Wenn ein Dropdown Menü oder ein Untermenü zerstört wurde, sendet das System eine " [**WM \_ uninitmenupopup**](wm-uninitmenupopup.md) "-Meldung.

## <a name="menu-destruction"></a>Menü Zerstörung

Wenn ein Menü einem Fenster zugewiesen ist und dieses Fenster zerstört wird, zerstört das System automatisch das Menü und seine Untermenüs, wodurch das Handle des Menüs und der vom Menü belegte Arbeitsspeicher freigegeben werden. Das System zerstört nicht automatisch ein Menü, das einem Fenster nicht zugewiesen ist. Eine Anwendung muss das nicht zugewiesene Menü durch Aufrufen der [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu) -Funktion zerstören. Andernfalls ist das Menü weiterhin im Arbeitsspeicher vorhanden, auch nachdem die Anwendung geschlossen wurde. Um das aktive Menü des aufrufenden Threads zu beenden, verwenden Sie [**endmenu**](/windows/desktop/api/Winuser/nf-winuser-endmenu). Wenn eine Plattform **endmenu** nicht unterstützt, senden Sie den Besitzer des aktiven Menüs an eine [**WM \_ cancelmode**](/windows/desktop/winmsg/wm-cancelmode) -Meldung.

 

 