---
title: Informationen zu Menüs
description: In diesem Thema werden Menüs erläutert.
ms.assetid: fd0b26f1-93cd-421b-9097-8502ab7681e9
keywords:
- Ressourcen, Menüs
- Menüs, Informationen
- Untermenüs
- Menüleisten
- Menüs der obersten Ebene
- Popupmenüs
- Dropdownmenüs
- Menüs, oberste Ebene
- Menüs, Popup
- Menüs, Dropdown
- Menünamen
- Menüs, Verknüpfung
- Menüs, Fenster
- Menüs, System
- menus,Control
- Kontextmenüs
- Menü "Fenster"
- Systemmenü
- Menü "Steuerelement"
- Hilfebezeichner
- Menühandles
- Menüelemente
- Befehlselemente
- Menüelementbezeichner
- Menüelementposition
- Auswählen von Menüelementen
- Löschen von Menüelementen
- Vom Besitzer gezeichnete Menüs
- Menüs,Besitzer gezeichnet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34d35ddf55ad31ed27cc12c6adffa5517e0081db6d70b4d01d3b88780a8797bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034492"
---
# <a name="about-menus"></a>Informationen zu Menüs

Ein *Menü* ist eine Liste von Elementen, die Optionen oder Gruppen von Optionen (ein Untermenü) für eine Anwendung angeben. Wenn Sie auf ein Menüelement klicken, wird ein Untermenü geöffnet, oder die Anwendung führt einen Befehl aus. Dieser Abschnitt enthält Informationen zu den folgenden Themen:

-   [Menüleisten und Menüs](#menu-bars-and-menus)
    -   [Kontextmenüs](#shortcut-menus)
    -   [Menü "Fenster"](#the-window-menu)
    -   [Hilfebezeichner](#help-identifier)
-   [Tastaturzugriff auf Menüs](#keyboard-access-to-menus)
    -   [Standardtastaturschnittstelle](#standard-keyboard-interface)
    -   [Menüzugriffsschlüssel](#menu-access-keys)
    -   [Tastenkombinationen im Menü](#menu-shortcut-keys)
-   [Menüerstellung](#menu-creation)
    -   [Menüvorlagenressourcen](#menu-template-resources)
    -   [Menüvorlage im Arbeitsspeicher](#menu-template-in-memory)
    -   [Menühandles](#menu-handles)
    -   [Funktionen zur Menüerstellung](#menu-creation-functions)
    -   [Menüanzeige](#menu-display)
    -   [Fensterklassenmenüs](#window-class-menus)
-   [Menüelemente](#menu-items)
    -   [Befehlselemente und Elemente, die Untermenüs öffnen](#command-items-and-items-that-open-submenus)
    -   [Menüelementbezeichner](#menu-item-identifier)
    -   [Position des Menüelements](#menu-item-position)
    -   [Programmgesteuertes Zugreifen auf Menüelemente](#accessing-menu-items-programmatically)
    -   [Standardmenüelemente](#default-menu-items)
    -   [Ausgewählte und löschende Menüelemente](#selected-and-clear-menu-items)
    -   [Aktivierte, graue und deaktivierte Menüelemente](#enabled-grayed-and-disabled-menu-items)
    -   [Hervorgehobene Menüelemente](#highlighted-menu-items)
    -   [Vom Besitzer gezeichnete Menüelemente](#owner-drawn-menu-items)
    -   [Menüelementtrennzeichen und Zeilenumbrüche](#menu-item-separators-and-line-breaks)
-   [Mit Menüs verwendete Nachrichten](#messages-used-with-menus)
-   [Menüzerstörungen](#menu-destruction)

## <a name="menu-bars-and-menus"></a>Menüleisten und Menüs

Ein Menü wird in einer Hierarchie angeordnet. Auf der obersten Ebene der Hierarchie befindet sich die *Menüleiste*. , die eine Liste von *Menüs* enthält, die wiederum *Untermenüs* enthalten können. Eine Menüleiste wird manchmal als Menü der *obersten Ebene* bezeichnet, und die Menüs und Untermenüs werden auch als *Popupmenüs* bezeichnet.

Ein Menüelement kann entweder einen Befehl ausführen oder ein Untermenü öffnen. Ein Element, das einen Befehl ausführt, wird als *Befehlselement* oder *Befehl* bezeichnet.

Ein Element in der Menüleiste öffnet fast immer ein Menü. Menüleisten enthalten nur selten Befehlselemente. Ein über die Menüleiste geöffnetes Menü wird in der Menüleiste angezeigt und manchmal als *Dropdownmenü* bezeichnet. Wenn ein Dropdownmenü angezeigt wird, wird es an die Menüleiste angefügt. Ein Menüelement auf der Menüleiste, das ein Dropdownmenü öffnet, wird auch als *Menüname* bezeichnet.

Die Menünamen auf einer Menüleiste stellen die Hauptkategorien von Befehlen dar, die eine Anwendung bereitstellt. Wenn Sie einen Menünamen in der Menüleiste auswählen, wird in der Regel ein Menü geöffnet, dessen Menüelemente den Befehlen in einer Kategorie entsprechen. Beispielsweise kann eine Menüleiste **einen** Dateimenünamen enthalten, der beim Klicken durch den Benutzer ein Menü mit Menüelementen wie **Neu,** **Öffnen** und **Speichern** aktiviert. Rufen [**Sie GetMenuBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo)auf, um Informationen zu einer Menüleiste abzurufen.

Nur ein überlappendes oder Popupfenster kann eine Menüleiste enthalten. ein untergeordnetes Fenster darf keins enthalten. Wenn das Fenster über eine Titelleiste verfügt, positioniert das System die Menüleiste direkt darunter. Eine Menüleiste ist immer sichtbar. Ein Untermenü ist jedoch erst sichtbar, wenn der Benutzer ein Menüelement auswählt, das es aktiviert. Weitere Informationen zu überlappenden und Popupfenstern finden Sie unter [Fenstertypen.](/windows/desktop/winmsg/window-features)

Jedes Menü muss über ein Besitzerfenster verfügen. Das System sendet Nachrichten an das Besitzerfenster eines Menüs, wenn der Benutzer das Menü auswählt oder ein Element aus dem Menü auswählt.

In diesem Abschnitt werden die folgenden Themen erläutert.

-   [Kontextmenüs](#shortcut-menus)
-   [Menü "Fenster"](#the-window-menu)
-   [Hilfebezeichner](#help-identifier)

### <a name="shortcut-menus"></a>Kontextmenüs

Das System stellt auch *Kontextmenüs bereit.* An die Menüleiste ist kein Kontextmenü angefügt. sie kann an einer beliebigen Stelle auf dem Bildschirm angezeigt werden. Eine Anwendung ordnet ein Kontextmenü in der Regel einem Teil eines Fensters zu, z. B. dem Clientbereich, oder einem bestimmten Objekt, z. B. einem Symbol. Aus diesem Grund werden diese Menüs auch als *Kontextmenüs* bezeichnet.

Ein Kontextmenü bleibt ausgeblendet, bis der Benutzer es aktiviert, in der Regel durch Klicken mit der rechten Maustaste auf eine Auswahl, eine Symbolleiste oder eine Taskleistenschaltfläche. Das Menü wird in der Regel an der Position des Caret- oder Mauszeigers angezeigt.

### <a name="the-window-menu"></a>Menü "Fenster"

Das **Menü Fenster** (auch als **Systemmenü** oder **Steuerelement** bezeichnet) ist ein Popupmenü, das fast ausschließlich vom Betriebssystem definiert und verwaltet wird. Der Benutzer kann das Fenstermenü öffnen, indem er auf das Anwendungssymbol in der Titelleiste klickt oder mit der rechten Maustaste auf eine beliebige Stelle in der Titelleiste klickt.

Das Menü **Fenster** stellt einen Standardsatz von Menüelementen bereit, die der Benutzer auswählen kann, um die Größe oder Position eines Fensters zu ändern oder die Anwendung zu schließen. Elemente im Fenstermenü können hinzugefügt, gelöscht und geändert werden, aber die meisten Anwendungen verwenden nur den Standardsatz von Menüelementen. Ein überlappendes, Popup- oder untergeordnetes Fenster kann über ein Fenstermenü verfügen. Es ist ungewöhnlich, dass ein überlappendes oder Popupfenster kein Fenstermenü enthält.

Wenn der Benutzer im Menü  Fenster einen Befehl auswählt, sendet das System eine [**WM \_ SYSCOMMAND-Nachricht**](wm-syscommand.md) an das Besitzerfenster des Menüs. In den meisten Anwendungen werden von der Fensterprozedur keine Meldungen aus dem Fenstermenü verarbeiten. Stattdessen werden die Nachrichten einfach an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) für die systembasierte Verarbeitung der Nachricht übergeben. Wenn eine Anwendung dem Fenstermenü einen Befehl hinzufügt, muss die Fensterprozedur den Befehl verarbeiten.

Eine Anwendung kann die [**GetSystemMenu-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) verwenden, um eine Kopie des Standardfenstermenüs zu erstellen, das geändert werden soll. Jedes Fenster, das nicht die **GetSystemMenu-Funktion** verwendet, um eine eigene Kopie des Fenstermenüs zu erstellen, erhält das Standardfenstermenü.

### <a name="help-identifier"></a>Hilfebezeichner

Jedem Menüleisten-, Menü-, Untermenü- und Kontextmenü ist ein Hilfebezeichner zugeordnet. Wenn der Benutzer die Taste F1 drückt, während das Menü aktiv ist, wird dieser Wert als Teil einer WM HELP-Meldung an das [**\_ Besitzerfenster**](../shell/wm-help.md) gesendet.

## <a name="keyboard-access-to-menus"></a>Tastaturzugriff auf Menüs

Das System stellt eine Standardtastaturschnittstelle für Menüs bereit. Sie können diese Schnittstelle erweitern, indem Sie mnemonische Zugriffsschlüssel und Tastenkombinationen (Zugriffstasten) für Ihre Menüelemente bereitstellen.

In den folgenden Themen werden die Standardtastaturschnittstelle, Zugriffstasten und Tastenkombinationen beschrieben:

-   [Standardtastaturschnittstelle](#standard-keyboard-interface)
-   [Menüzugriffsschlüssel](#menu-access-keys)
-   [Tastenkombinationen im Menü](#menu-shortcut-keys)

### <a name="standard-keyboard-interface"></a>Standardtastaturschnittstelle

Das System ist für die Arbeit mit oder ohne Maus oder anderes zeigende Gerät konzipiert. Da das System eine Standardtastaturschnittstelle bietet, kann der Benutzer die Tastatur verwenden, um Menüelemente auszuwählen. Diese Tastaturschnittstelle benötigt keinen speziellen Code. Eine Anwendung empfängt eine Befehlsmeldung, unabhängig davon, ob der Benutzer ein Menüelement über die Tastatur oder mithilfe einer Maus auswählt. Die Standardtastaturschnittstelle verarbeitet die folgenden Tastatureingaben.



| Tastatureingabe              | Aktion                                                                                                                                                                                                                                   |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Alphabetisches Zeichen | Wählt das erste Menüelement mit dem angegebenen Zeichen als Zugriffsschlüssel aus. Wenn das ausgewählte Element ein Menü aufruft, wird das Menü angezeigt, und das erste Element wird hervorgehoben. Andernfalls wird das Menüelement ausgewählt.                            |
| ALT                    | Ein- und Ausschalten des Menüleistenmodus.                                                                                                                                                                                                     |
| ALT+LEERTASTE           | Zeigt das Fenstermenü an.                                                                                                                                                                                                                |
| EINGABETASTE                  | Aktiviert ein Menü und wählt das erste Menüelement aus, wenn einem Element ein Menü zugeordnet ist. Andernfalls wählt diese Tastatureingabe das Element so aus, als würde der Benutzer die Maustaste losgelassen, während das Element ausgewählt wurde.                              |
| ESC                    | Beendet den Menümodus.                                                                                                                                                                                                                         |
| NACH-LINKS-TASTE             | Zyklen zum vorherigen Menüelement der obersten Ebene. Menüelemente der obersten Ebene enthalten Menünamen und das Fenstermenü. Wenn sich das ausgewählte Element in einem Menü befindet, wird die vorherige Spalte im Menü oder das vorherige Menüelement der obersten Ebene ausgewählt. |
| NACH-RECHTS-TASTE            | Funktioniert wie die NACH-LINKS-TASTE, mit Ausnahme der umgekehrten Richtung. In Menüs verschiebt sich diese Tastatureingabe um eine Spalte nach vorn. Wenn sich das aktuell ausgewählte Element in der spalte ganz rechts befindet, wird das nächste Menü ausgewählt.                              |
| NACH-OBEN- oder NACH-UNTEN-TASTE      | Aktiviert ein Menü, wenn es in einem Menünamen gedrückt wird. Wenn sie in einem Menü gedrückt wird, wählt die NACH-OBEN-TASTE das vorherige Element aus. Die NACH-UNTEN-TASTE wählt das nächste Element aus.                                                                  |



 

### <a name="menu-access-keys"></a>Menüzugriffsschlüssel

Die Standardtastaturschnittstelle für Menüs kann verbessert werden, indem Menüelementen Zugriffstasten (mnemonische Tasten) hinzugefügt werden. Eine Zugriffsschlüssel ist ein unterstrichener Buchstabe im Text eines Menüelements. Wenn ein Menü aktiv ist, kann der Benutzer ein Menüelement auswählen, indem er die Taste drückt, die dem unterstrichenen Buchstaben des Elements entspricht. Der Benutzer macht die Menüleiste aktiv, indem er die ALT-TASTE drückt, um das erste Element auf der Menüleiste hervorzuheben. Ein Menü ist aktiv, wenn es angezeigt wird.

Um einen Zugriffsschlüssel für ein Menüelement zu erstellen, stellen Sie einem beliebigen Zeichen in der Textzeichenfolge des Elements ein ampersand voran. Beispielsweise bewirkt die Textzeichenfolge "&Move", dass das System den Buchstaben "M" unterstreicht.

### <a name="menu-shortcut-keys"></a>Tastenkombinationen im Menü

Zusätzlich zu einem Zugriffsschlüssel kann einem Menüelement eine Tastenkombination zugeordnet sein. Eine Tastenkombination ist anders als eine Zugriffstaste, da das Menü nicht aktiv sein muss, damit die Tastenkombination funktioniert. Außerdem ist eine Zugriffsschlüssel *immer* einem Menüelement zugeordnet, während eine Tastenkombination in der Regel *einem* Menüelement zugeordnet ist (aber nicht sein muss).

Text, der die Tastenkombination identifiziert, wird der Textzeichenfolge des Menüelements hinzugefügt. Der Verknüpfungstext wird rechts vom Namen des Menüelements nach einem schrägen Schrägstrich und einem Tabstoppzeichen ( \\ t) angezeigt. Beispielsweise stellt "&Schließen tAlt+F4" einen Close-Befehl mit der Tastenkombination ALT+F4 als Tastenkombination und dem Buchstaben "C" als Zugriffsschlüssel \\ dar. Weitere Informationen finden Sie unter [Tastaturbeschleunigungen.](keyboard-accelerators.md)

## <a name="menu-creation"></a>Menüerstellung

Sie können ein Menü erstellen, indem Sie entweder eine Menüvorlage oder Menüerstellungsfunktionen verwenden. Menüvorlagen werden in der Regel als Ressourcen definiert. Menüvorlagenressourcen können explizit geladen oder als Standardmenü für eine Fensterklasse zugewiesen werden. Sie können Menüvorlagenressourcen auch dynamisch im Arbeitsspeicher erstellen.

In den folgenden Themen wird die Menüerstellung ausführlich beschrieben:

-   [Menüvorlagenressourcen](#menu-template-resources)
-   [Menüvorlage im Arbeitsspeicher](#menu-template-in-memory)
-   [Menühandles](#menu-handles)
-   [Menüerstellungsfunktionen](#menu-creation-functions)
-   [Menüanzeige](#menu-display)
-   [Window-Klassenmenüs](#window-class-menus)

### <a name="menu-template-resources"></a>Menüvorlagenressourcen

Die meisten Anwendungen erstellen Menüs mithilfe von Menüvorlagenressourcen. Eine *Menüvorlage* definiert ein Menü, einschließlich der Elemente in der Menüleiste und aller Menüs. Informationen zum Erstellen einer Menüvorlagenressource finden Sie in der Dokumentation zu Ihren Entwicklungstools.

Nachdem Sie eine Menüvorlagenressource erstellt und der ausführbaren Datei (.exe) Ihrer Anwendung hinzugefügt haben, können Sie die [**LoadMenu-Funktion**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) verwenden, um die Ressource in den Arbeitsspeicher zu laden. Diese Funktion gibt ein Handle an das Menü zurück, das Sie dann mithilfe der [**SetMenu-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setmenu) einem Fenster zuweisen können. Sie können jedem Fenster, das kein untergeordnetes Fenster ist, ein Menü zuweisen.

Das Implementieren von Menüs als Ressourcen vereinfacht die Lokalisierung einer Anwendung für die Verwendung in mehreren Ländern/Regionen. Nur die Ressourcendefinitionsdatei muss für jede Sprache lokalisiert werden, nicht für den Quellcode der Anwendung.

### <a name="menu-template-in-memory"></a>Menüvorlage im Arbeitsspeicher

Ein Menü kann aus einer Menüvorlage erstellt werden, die zur Laufzeit im Arbeitsspeicher erstellt wird. Beispielsweise kann eine Anwendung, die es einem Benutzer ermöglicht, sein Menü anzupassen, eine Menüvorlage im Arbeitsspeicher basierend auf den Einstellungen des Benutzers erstellen. Die Anwendung könnte die Vorlage dann zur zukünftigen Verwendung in einer Datei oder in der Registrierung speichern. Verwenden Sie die [**LoadMenuIndirect-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) um ein Menü aus einer Vorlage im Arbeitsspeicher zu erstellen. Beschreibungen von Menüvorlagenformaten finden Sie unter [Menüvorlagenressourcen](#menu-template-resources).

Eine Standardmenüvorlage besteht aus einer [**MENUITEMTEMPLATEHEADER-Struktur**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) gefolgt von einer oder mehreren [**MENUITEMTEMPLATE-Strukturen.**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)

Eine erweiterte Menüvorlage besteht aus einer [**MENUEX \_ TEMPLATE \_ HEADER-Struktur,**](menuex-template-header.md) gefolgt von einer oder mehreren [**MENUEX \_ TEMPLATE \_ ITEM-Strukturen.**](menuex-template-item.md)

### <a name="menu-handles"></a>Menühandles

Das System generiert für jedes Menü ein eindeutiges Handle. Ein *Menühandpunkt* ist ein Wert vom **Typ HMENU.** Eine Anwendung muss in vielen Menüfunktionen ein Menühand handle angeben. Sie erhalten ein Handle für eine Menüleiste, wenn Sie das Menü erstellen oder eine Menüressource laden.

Verwenden Sie die [**GetMenu-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-getmenu) um ein Handle für die Menüleiste für ein erstelltes oder geladenes Menü abzurufen. Um ein Handle für das Einem Menüelement zugeordnete Untermenü abzurufen, verwenden Sie die Funktion [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) oder [**GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) Verwenden Sie die [**GetSystemMenu-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) um ein Handle für ein Fenstermenü abzurufen.

### <a name="menu-creation-functions"></a>Funktionen zur Menüerstellung

Mithilfe von Menüerstellungsfunktionen können Sie Menüs zur Laufzeit erstellen oder vorhandenen Menüs Menüelemente hinzufügen. Sie können die [**CreateMenu-Funktion**](/windows/desktop/api/Winuser/nf-winuser-createmenu) verwenden, um eine leere Menüleiste zu erstellen, und die [**CreatePopupMenu-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) um ein leeres Menü zu erstellen. Sie können bestimmte Einstellungsinformationen für ein Menü mithilfe der [**MENUINFO-Struktur**](/windows/win32/api/winuser/ns-winuser-menuinfo) speichern. Verwenden [**Sie GetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo) oder [**SetMenuInfo,**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)um die Einstellungen eines Menüs abzurufen oder abzurufen. Um einem Menü Elemente hinzuzufügen, verwenden Sie die [**InsertMenuItem-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) Die älteren [**AppendMenu-**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) und [**InsertMenu-Funktionen**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) werden weiterhin unterstützt, **aber InsertMenuItem** sollte für neue Anwendungen verwendet werden.

### <a name="menu-display"></a>Menüanzeige

Nachdem ein Menü geladen oder erstellt wurde, muss es einem Fenster zugewiesen werden, bevor es vom System angezeigt werden kann. Sie können ein Menü zuweisen, indem Sie ein Klassenmenü definieren. Weitere Informationen finden Sie unter [Fensterklassenmenüs.](#window-class-menus) Sie können einem Fenster auch ein Menü zuweisen, indem Sie ein Handle für das Menü als *hMenu-Parameter* der [**CreateWindow-**](/windows/desktop/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) angeben oder die [**SetMenu-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setmenu) aufrufen.

Um ein Kontextmenü anzuzeigen, verwenden Sie die [**TrackPopupMenuEx-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) Kontextmenüs, auch als unverankerte Popupmenüs oder Kontextmenüs bezeichnet, werden in der Regel angezeigt, wenn die [**WM \_ CONTEXTMENU-Nachricht**](wm-contextmenu.md) verarbeitet wird.

Sie können jedem Fenster, das kein untergeordnetes Fenster ist, ein Menü zuweisen.

Die ältere [**TrackPopupMenu-Funktion**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) wird weiterhin unterstützt, neue Anwendungen sollten jedoch die [**TrackPopupMenuEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) verwenden.

### <a name="window-class-menus"></a>Fensterklassenmenüs

Sie können ein Standardmenü angeben, das als Klassenmenü bezeichnet *wird,* wenn Sie eine Fensterklasse registrieren. Hierzu weisen Sie den Namen der Menüvorlagenressource dem **lpszMenuName-Member** der [**WNDCLASS-Struktur**](/windows/win32/api/winuser/ns-winuser-wndclassa) zu, die zum Registrieren der Klasse verwendet wird.

Standardmäßig wird jedem Fenster das Klassenmenü für seine Fensterklasse zugewiesen, sodass Sie das Menü nicht explizit laden und jedem Fenster zuweisen müssen. Sie können das Klassenmenü überschreiben, indem Sie in einem Aufruf der [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ein anderes Menühandle angeben. Sie können das Menü eines Fensters auch ändern, nachdem es erstellt wurde, indem Sie die [**SetMenu-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setmenu) verwenden. Weitere Informationen finden Sie unter [Fensterklassen.](/windows/desktop/winmsg/window-classes)

## <a name="menu-items"></a>Menüelemente

In den folgenden Themen wird beschrieben, was das System tut, wenn der Benutzer ein Menüelement ausgibt, und wie eine Anwendung die Darstellung und Funktionalität eines Elements steuern kann:

-   [Befehlselemente und Elemente, die Untermenüs öffnen](#command-items-and-items-that-open-submenus)
-   [Menüelementbezeichner](#menu-item-identifier)
-   [Position des Menüelements](#menu-item-position)
-   [Programmgesteuertes Zugreifen auf Menüelemente](#accessing-menu-items-programmatically)
-   [Standardmenüelemente](#default-menu-items)
-   [Ausgewählte und löschende Menüelemente](#selected-and-clear-menu-items)
-   [Aktivierte, graue und deaktivierte Menüelemente](#enabled-grayed-and-disabled-menu-items)
-   [Hervorgehobene Menüelemente](#highlighted-menu-items)
-   [Vom Besitzer gezeichnete Menüelemente](#owner-drawn-menu-items)
-   [Menüelementtrennzeichen und Zeilenumbrüche](#menu-item-separators-and-line-breaks)

### <a name="command-items-and-items-that-open-submenus"></a>Befehlselemente und Elemente, die Untermenüs öffnen

Wenn der Benutzer ein Befehlselement ausgibt, sendet das System eine Befehlsmeldung an das Fenster, das das Menü besitzt. Wenn sich das Befehlselement im Fenstermenü befindet, sendet das System die [**\_ WM-SYSCOMMAND-Nachricht.**](wm-syscommand.md) Andernfalls wird die [**WM \_ COMMAND-Nachricht**](wm-command.md) gesendet.

Jedem Menüelement zugeordnet, das ein Untermenü öffnet, ist ein Handle für das entsprechende Untermenü. Wenn der Benutzer auf ein solches Element zeigt, öffnet das System das Untermenü. Es wird keine Befehlsmeldung an das Besitzerfenster gesendet. Das System sendet jedoch eine [**\_ WM-INITMENUPOPUP-Nachricht**](wm-initmenupopup.md) an das Besitzerfenster, bevor das Untermenü angezeigt wird. Sie können ein Handle für das Einem Element zugeordnete Untermenü abrufen, indem Sie die Funktion [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) oder [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) verwenden.

Eine Menüleiste enthält in der Regel Menünamen, kann aber auch Befehlselemente enthalten. Ein Untermenü enthält in der Regel Befehlselemente, kann aber auch Elemente enthalten, die geschachtelte Untermenüs öffnen. Durch Hinzufügen solcher Elemente zu Untermenüs können Sie Menüs in beliebiger Tiefe schachteln. Um einen visuellen Hinweis für den Benutzer bereitzustellen, zeigt das System automatisch einen kleinen Pfeil rechts neben dem Text eines Menüelements an, das ein Untermenü öffnet.

### <a name="menu-item-identifier"></a>Menu-Item-Bezeichner

Jedem Menüelement ist eine eindeutige, anwendungsdefinierte ganze Zahl zugeordnet, die als *Menüelementbezeichner* bezeichnet wird. Wenn der Benutzer ein Befehlselement aus einem Menü auswählt, sendet das System den Bezeichner des Elements als Teil einer [**WM \_ COMMAND-Nachricht**](wm-command.md) an das Besitzerfenster. Die Fensterprozedur untersucht den Bezeichner, um die Quelle der Nachricht zu bestimmen, und verarbeitet die Nachricht entsprechend. Darüber hinaus können Sie ein Menüelement mit seinem Bezeichner angeben, wenn Sie Menüfunktionen aufrufen. beispielsweise, um ein Menüelement zu aktivieren oder zu deaktivieren.

Menüelemente, die Untermenüs öffnen, verfügen über Bezeichner wie Befehlselemente. Das System sendet jedoch keine Befehlsmeldung, wenn ein solches Element in einem Menü ausgewählt wird. Stattdessen öffnet das System das Untermenü, das dem Menüelement zugeordnet ist.

Um den Bezeichner des Menüelements an einer angegebenen Position abzurufen, verwenden Sie die Funktion [**GetMenuItemID**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid) oder [**GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)

### <a name="menu-item-position"></a>Menu-Item Position

Zusätzlich zu einem eindeutigen Bezeichner verfügt jedes Menüelement in einer Menüleiste oder einem Menü über einen eindeutigen Positionswert. Das element ganz links in einer Menüleiste oder das oberste Element in einem Menü hat die Position 0 (null). Der Positionswert wird für nachfolgende Menüelemente erhöht. Das System weist allen Elementen in einem Menü einen Positionswert zu, einschließlich Trennzeichen. Die folgende Abbildung zeigt die Positionswerte von Elementen in einer Menüleiste und in einem Menü.

![Menüleiste und Menü](images/csemn-01.png)

Wenn Sie eine Menüfunktion aufrufen, die Informationen zu einem bestimmten Menüelement ändert oder abruft, können Sie das Element entweder mit seinem Bezeichner oder seiner Position angeben. Weitere Informationen finden Sie im nächsten Abschnitt.

### <a name="accessing-menu-items-programmatically"></a>Programmgesteuertes Zugreifen auf Menüelemente

Mit den meisten Menüfunktionen können Sie ein Menüelement entweder nach Position oder nach Befehl angeben. Einige Funktionen verwenden die **Flags MF \_ BYPOSITION** und **MF \_ BYCOMMAND,** um den Suchalgorithmus anzugeben. Andere verfügen über einen expliziten *fByPosition-Parameter.* Wenn Sie das Menüelement nach Position angeben, ist die Elementnummer ein nullbasierter Index im Menü. Wenn Sie das Menüelement nach Befehl angeben, werden das Menü und seine Untermenüs nach einem Element durchsucht, dessen Menübezeichner der angegebenen Elementnummer entspricht. Wenn mehrere Elemente in der Menühierarchie mit der Elementnummer übereinstimmen, wird nicht angegeben, welches Element verwendet wird. Wenn Ihre Menüs doppelte Menübezeichner enthalten, sollten Sie positionsbasierte Menüvorgänge verwenden, um diese Mehrdeutigkeit zu vermeiden.

### <a name="default-menu-items"></a>Standardmenüelemente

Ein Untermenü kann ein Standardmenüelement enthalten. Wenn der Benutzer durch Doppelklicken ein Untermenü öffnet, sendet das System eine Befehlsmeldung an das Besitzerfenster des Menüs und schließt das Menü so, als ob das Standardbefehlselement ausgewählt worden wäre. Wenn kein Standardbefehlselement vorhanden ist, bleibt das Untermenü geöffnet. Um das Standardelement für ein Untermenü abzurufen und festzulegen, verwenden Sie die Funktionen [**GetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem) und [**SetMenuDefaultItem.**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem)

### <a name="selected-and-clear-menu-items"></a>Ausgewählte und löschende Menüelemente

Ein Menüelement kann entweder ausgewählt oder gelöscht werden. Das System zeigt eine Bitmap neben ausgewählten Menüelementen an, um ihren ausgewählten Zustand anzugeben. Das System zeigt keine Bitmap neben gelöschten Elementen an, es sei denn, es wird eine anwendungsdefinierte "clear"-Bitmap angegeben. Es können nur Menüelemente in einem Menü ausgewählt werden. Elemente in einer Menüleiste können nicht ausgewählt werden.

Anwendungen überprüfen oder deaktivieren in der Regel ein Menüelement, um anzugeben, ob eine Option aktiviert ist. Angenommen, eine Anwendung verfügt über eine Symbolleiste, die der Benutzer mithilfe eines **Symbolleistenbefehls** in einem Menü anzeigen oder ausblenden kann. Wenn die Symbolleiste ausgeblendet ist, wird das Menüelement **Symbolleiste** gelöscht. Wenn der Benutzer den Befehl ausgibt, überprüft die Anwendung das Menüelement und zeigt die Symbolleiste an.

Ein Häkchenattribut steuert, ob ein Menüelement ausgewählt ist. Sie können das Häkchenattribut eines Menüelements mithilfe der [**CheckMenuItem-Funktion**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) festlegen. Sie können die [**GetMenuState-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) verwenden, um zu bestimmen, ob ein Menüelement derzeit ausgewählt oder gelöscht wird.

Anstelle von [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) und [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate)können Sie die Funktionen [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) und [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) verwenden, um den Prüfzustand eines Menüelements abzurufen und festzulegen.

Manchmal entspricht eine Gruppe von Menüelementen einer Reihe von sich gegenseitig ausschließenden Optionen. In diesem Fall können Sie die ausgewählte Option angeben, indem Sie ein ausgewähltes Optionsmenüelement (analog zu einem Optionsfeld-Steuerelement) verwenden. Ausgewählte Optionselemente werden mit einer Aufzählungsbitmap anstelle einer Häkchenbitmap angezeigt. Um ein Menüelement zu überprüfen und zu einem Optionselement zu machen, verwenden Sie die [**CheckMenuRadioItem-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)

Standardmäßig zeigt das System ein Häkchen oder eine Aufzählungsbitmap neben ausgewählten Menüelementen und keine Bitmap neben gelöschten Menüelementen an. Sie können jedoch die [**SetMenuItemBitmaps-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) verwenden, um anwendungsdefinierte ausgewählte und gelöschte Bitmaps einem Menüelement zuzuordnen. Das System verwendet dann die angegebenen Bitmaps, um den ausgewählten oder gelöschten Zustand des Menüelements anzugeben.

Anwendungsdefinierte Bitmaps, die einem Menüelement zugeordnet sind, müssen die gleiche Größe aufweisen wie die Standardmäßige Häkchenbitmap, deren Abmessungen je nach Bildschirmauflösung variieren können. Verwenden Sie die [**GetSystemMetrics-Funktion,**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) um die richtigen Dimensionen abzurufen. Sie können mehrere Bitmapressourcen für verschiedene Bildschirmauflösungen erstellen. Erstellen Sie eine Bitmapressource, und skalieren Sie sie bei Bedarf. oder erstellen Sie zur Laufzeit eine Bitmap, und zeichnen Sie darin ein Bild. Die Bitmaps können entweder monocolore oder color sein. Da Menüelemente jedoch invertiert werden, wenn sie hervorgehoben werden, kann die Darstellung bestimmter invertierter Farbbitmaps unerwünscht sein. Weitere Informationen finden Sie unter [Bitmaps](/windows/desktop/gdi/bitmaps).

### <a name="enabled-grayed-and-disabled-menu-items"></a>Aktivierte, graue und deaktivierte Menüelemente

Ein Menüelement kann aktiviert, abgeblendet oder deaktiviert werden. Standardmäßig ist ein Menüelement aktiviert. Wenn der Benutzer ein aktiviertes Menüelement ausgibt, sendet das System eine Befehlsmeldung an das Besitzerfenster oder zeigt das entsprechende Untermenü an, je nachdem, um welche Art von Menüelement es sich handelt.

Wenn Menüelemente für den Benutzer nicht verfügbar sind, sollten sie abgeblendet oder deaktiviert sein. Graue und deaktivierte Menüelemente können nicht ausgewählt werden. Ein deaktiviertes Element sieht genauso wie ein aktiviertes Element aus. Wenn der Benutzer auf ein deaktiviertes Element klickt, wird das Element nicht ausgewählt, und es geschieht nichts. Deaktivierte Elemente können z. B. in einem Tutorial nützlich sein, in dem ein Menü angezeigt wird, das aktiv aussieht, aber nicht ist.

Eine Anwendung graut ein nicht verfügbares Menüelement, um dem Benutzer einen visuellen Hinweis zu geben, dass kein Befehl verfügbar ist. Sie können ein graues Element verwenden, wenn eine Aktion nicht geeignet ist (z. B. können Sie den Befehl **Drucken** im Menü **Datei** vergrauen, wenn auf dem System kein Drucker installiert ist).

Die [**EnableMenuItem-Funktion**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem) aktiviert, graut oder deaktiviert ein Menüelement. Verwenden Sie die [**GetMenuItemInfo-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) um zu bestimmen, ob ein Menüelement aktiviert, abgeblendet oder deaktiviert ist.

Anstelle von [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)können Sie auch die [**GetMenuState-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) verwenden, um zu bestimmen, ob ein Menüelement aktiviert, abgeblendet oder deaktiviert ist.

### <a name="highlighted-menu-items"></a>Hervorgehobene Menüelemente

Das System hebt Menüelemente in Menüs automatisch hervor, wenn der Benutzer sie auswählt. Die Hervorhebung kann jedoch mithilfe der [**Funktion "HiliteMenuItem"**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem) explizit einem Menünamen in der Menüleiste hinzugefügt oder daraus entfernt werden. Diese Funktion hat keine Auswirkungen auf Menüelemente in Menüs. Wenn Jedoch mitHilfe von **HiliteMenuItem** ein Menüname hervorgehoben wird, scheint nur der Name ausgewählt zu sein. Wenn der Benutzer die EINGABETASTE drückt, wird das hervorgehobene Element nicht ausgewählt. Dieses Feature kann z. B. in einer Trainingsanwendung nützlich sein, die die Verwendung von Menüs veranschaulicht.

### <a name="owner-drawn-menu-items"></a>Owner-Drawn-Menüelemente

Eine Anwendung kann die Darstellung eines Menüelements mithilfe eines *vom Besitzer gezeichneten Elements* vollständig steuern. Vom Besitzer gezeichnete Elemente erfordern, dass eine Anwendung die gesamte Verantwortung für das Zeichnen ausgewählter (hervorgehobener), ausgewählter und gelöschter Zustände übernimmt. Wenn eine Anwendung beispielsweise ein Schriftartmenü bereitgestellt hat, kann jedes Menüelement mithilfe der entsprechenden Schriftart gezeichnet werden. das Element für Roman würde mit roman gezeichnet werden, das Element für italisch wird italisch gezeichnet usw. Weitere Informationen finden Sie unter [Creating Owner-Drawn Menu Items](using-menus.md).

### <a name="menu-item-separators-and-line-breaks"></a>Menüelementtrennzeichen und Zeilenumbrüche

Das System stellt einen speziellen Typ von Menüelement bereit, das als *Trennzeichen* bezeichnet wird und als horizontale Linie angezeigt wird. Sie können ein Menü mithilfe eines Trennzeichens in Gruppen verwandter Elemente unterteilen. Ein Trennzeichen kann nicht in einer Menüleiste verwendet werden, und der Benutzer kann kein Trennzeichen auswählen.

Wenn eine Menüleiste mehr Menünamen enthält, als in eine Zeile passen, umschließt das System die Menüleiste, indem es sie automatisch in zwei oder mehr Zeilen unterteilt. Sie können dazu führen, dass an einem bestimmten Element in einer Menüleiste ein Zeilenbreak auftritt, indem Sie dem Element das **MFT \_ MENUBREAK-Typflag** zuweisen. Das System platziert dieses Element und alle nachfolgenden Elemente in einer neuen Zeile.

Wenn ein Menü mehr Elemente enthält, als in eine Spalte passen, wird das Menü abgeschnitten. Sie können dazu führen, dass ein Spaltenumbruch bei einem bestimmten Element in einem Menü auftritt, indem Sie dem Element das **MFT \_ MENUBREAK-Typflag** zuweisen oder die MENUBREAK-Option in der [MENUITEM-Anweisung](/windows/desktop/menurc/menuitem-statement) verwenden. Das System platziert dieses Element und alle nachfolgenden Elemente in einer neuen Spalte. Das **MFT \_ MENUBARBREAK-Typflag** hat den gleichen Effekt, mit der Ausnahme, dass eine vertikale Linie zwischen der neuen Spalte und der alten spalte angezeigt wird.

Wenn Sie die Funktionen [**AppendMenu,**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)oder [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) verwenden, um Zeilenumbrüche zuzuweisen, sollten Sie die Typflags **MF \_ MENUBREAK** oder **MF \_ MENUBARBREAK** zuweisen.

## <a name="messages-used-with-menus"></a>Mit Menüs verwendete Nachrichten

Das System meldet menübezogene Aktivitäten durch Senden von Nachrichten an die Fensterprozedur des Fensters, das das Menü besitzt. Das System sendet eine Reihe von Nachrichten, wenn der Benutzer Elemente in der Menüleiste auswählt oder mit der rechten Maustaste klickt, um ein Kontextmenü anzuzeigen.

Wenn der Benutzer ein Element in der Menüleiste aktiviert, erhält das Besitzerfenster zunächst eine [**\_ WM-SYSCOMMAND-Meldung.**](wm-syscommand.md) Diese Meldung enthält ein Flag, das angibt, ob der Benutzer das Menü über die Tastatur (SC \_ KEYMENU) oder die Maus (SC \_ MOUSEMENU) aktiviert hat. Weitere Informationen finden Sie unter [Tastaturzugriff auf Menüs.](#keyboard-access-to-menus)

Als Nächstes sendet das System vor dem Anzeigen von Menüs die [**\_ WM-INITMENU-Nachricht**](wm-initmenu.md) an die Fensterprozedur, damit eine Anwendung die Menüs ändern kann, bevor sie dem Benutzer angezeigt werden. Das System sendet die **\_ WM-INITMENU-Nachricht** nur einmal pro Menüaktivierung.

Wenn der Benutzer auf ein Menüelement zeigt, das ein Untermenü öffnet, sendet das System dem Besitzerfenster die [**\_ WM-Meldung INITMENUPOPUP,**](wm-initmenupopup.md) bevor das Untermenü angezeigt wird. Diese Meldung gibt der Anwendung die Möglichkeit, das Untermenü zu ändern, bevor es angezeigt wird.

Jedes Mal, wenn der Benutzer die Hervorhebung von einem Element in ein anderes verschiebt, sendet das System eine [**WM \_ MENUSELECT-Meldung**](wm-menuselect.md) an die Fensterprozedur des Besitzerfensters des Menüs. Diese Meldung identifiziert das aktuell ausgewählte Menüelement. Viele Anwendungen stellen unten in den Hauptfenstern einen Informationsbereich bereit und verwenden diese Meldung, um zusätzliche Informationen zum ausgewählten Menüelement anzuzeigen.

Wenn der Benutzer ein Befehlselement aus einem Menü auswählt, sendet das System eine [**WM \_ COMMAND-Meldung**](wm-command.md) an die Fensterprozedur. Das Wort mit niedriger Reihenfolge im *wParam-Parameter* der **WM \_ COMMAND-Nachricht** enthält den Bezeichner des ausgewählten Elements. Die Fensterprozedur sollte den Bezeichner untersuchen und die Nachricht entsprechend verarbeiten.

Sie können Informationen für ein Menü mithilfe der [**MENUINFO-Struktur**](/windows/win32/api/winuser/ns-winuser-menuinfo) speichern. Wenn das Menü mit einer **MENUINFO** definiert ist. **dwStyle-Wert** von MNS \_ NOTIFYBYPOS. Das System sendet [**WM \_ MENUCOMMAND**](wm-menucommand.md) anstelle des [**\_ WM-BEFEHLs,**](wm-command.md) wenn ein Element ausgewählt wird. Dadurch können Sie auf die Informationen in der **MENUINFO-Struktur** zugreifen und auch den Index des ausgewählten Elements direkt zur Verfügung stellen.

Nicht auf alle Menüs kann über die Menüleiste eines Fensters zugegriffen werden. Viele Anwendungen zeigen Kontextmenüs an, wenn der Benutzer an einer bestimmten Position mit der rechten Maustaste klickt. Solche Anwendungen sollten die [**WM \_ CONTEXTMENU-Nachricht**](wm-contextmenu.md) verarbeiten und ggf. ein Kontextmenü anzeigen. Wenn eine Anwendung kein Kontextmenü anzeigt, sollte sie die **WM \_ CONTEXTMENU-Nachricht** zur Standardverarbeitung an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) übergeben.

Die [**WM \_ MENURBUTTONUP-Meldung**](wm-menurbuttonup.md) wird gesendet, wenn der Benutzer die rechte Maustaste loslässt, während sich der Cursor auf einem Menüelement befindet. Diese Meldung wird bereitgestellt, damit Anwendungen ein kontextbezogenes Oder Kontextmenü für ein Menüelement anzeigen können.

Es gibt einige Nachrichten, die nur Drag & Drop-Menüs enthalten. The [**WM\_MENUGETOBJECT**](wm-menugetobject.md) is sent to the owner of a drag-and-drop menu when the mouse cursor enters a menu item or moves from the center of an item to the top or the bottom of an item. Die [**WM \_ MENUDRAG-Nachricht**](wm-menudrag.md) wird gesendet, wenn der Benutzer tatsächlich ein Menüelement zieht.

Wenn ein Dropdownmenü oder ein Untermenü zerstört wurde, sendet das System eine [**\_ WM-UNINITMENUPOPUP-Nachricht.**](wm-uninitmenupopup.md)

## <a name="menu-destruction"></a>Menüzerstörungen

Wenn einem Fenster ein Menü zugewiesen ist und dieses Fenster zerstört wird, zerstört das System automatisch das Menü und seine Untermenüs, wodurch das Handle des Menüs und der vom Menü belegte Arbeitsspeicher freigegeben werden. Das System zerstört nicht automatisch ein Menü, das keinem Fenster zugewiesen ist. Eine Anwendung muss das nicht zugewiesene Menü durch Aufrufen der [**DestroyMenu-Funktion**](/windows/desktop/api/Winuser/nf-winuser-destroymenu) zerstören. Andernfalls ist das Menü auch nach dem Schließen der Anwendung weiterhin im Arbeitsspeicher vorhanden. Verwenden Sie [**EndMenu,**](/windows/desktop/api/Winuser/nf-winuser-endmenu)um das aktive Menü des aufrufenden Threads zu beenden. Wenn eine Plattform **EndMenu** nicht unterstützt, senden Sie dem Besitzer des aktiven Menüs eine [**WM \_ CANCELMODE-Nachricht.**](/windows/desktop/winmsg/wm-cancelmode)

 

 