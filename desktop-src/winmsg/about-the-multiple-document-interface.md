---
description: Jedes Dokument in einer MDI-Anwendung (Multiple Document Interface) wird in einem separaten untergeordneten Fenster im Client Bereich des Hauptfensters der Anwendung angezeigt.
ms.assetid: 35dff281-3b11-4954-85cf-a0f1c9ed346a
title: Informationen zur Schnittstelle für mehrere Dokumente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0397127d7ec343ebdb7696c2dd7d57204a5d5ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352771"
---
# <a name="about-the-multiple-document-interface"></a>Informationen zur Schnittstelle für mehrere Dokumente

Jedes Dokument in einer MDI-Anwendung (Multiple Document Interface) wird in einem separaten untergeordneten Fenster im Client Bereich des Hauptfensters der Anwendung angezeigt. Typische MDI-Anwendungen enthalten Textverarbeitungsanwendungen, die es dem Benutzer ermöglichen, mit mehreren Textdokumenten zu arbeiten und Arbeitsblatt Anwendungen, mit denen der Benutzer mit mehreren Diagrammen und Kalkulations Tabellen arbeiten kann. Weitere Informationen finden Sie in den nachfolgenden Themen.

-   [Frame, Client und untergeordnete Fenster](#frame-client-and-child-windows)
-   [Erstellung des untergeordneten Fensters](#child-window-creation)
-   [Aktivierung des untergeordneten Fensters](#child-window-activation)
-   [Mehrere Dokument Menüs](#multiple-document-menus)
-   [Mehrere Dokument Beschleuniger](#multiple-document-accelerators)
-   [Größe und Anordnung des untergeordneten Fensters](#child-window-size-and-arrangement)
-   [Symbol Titel Fenster](#icon-title-windows)
-   [Daten des untergeordneten Fensters](#child-window-data)
    -   [Fenster Struktur](#window-structure)
    -   [Fenstereigenschaften](#window-properties)

## <a name="frame-client-and-child-windows"></a>Frame, Client und untergeordnete Fenster

Eine MDI-Anwendung verfügt über drei Arten von Fenstern: ein Rahmen Fenster, ein MDI-Client Fenster sowie eine Reihe von untergeordneten Fenstern. Das *Rahmen Fenster* ist wie das Hauptfenster der Anwendung: Es verfügt über einen Größen Anpassungsrahmen, eine Titelleiste, ein Fenstermenü, eine Minimieren-Schaltfläche und eine Schaltfläche zum maximieren. Die Anwendung muss eine Fenster Klasse für das Rahmen Fenster registrieren und eine Fenster Prozedur zur Unterstützung bereitstellen.

In einer MDI-Anwendung wird die Ausgabe im Client Bereich des Rahmen Fensters nicht angezeigt. Stattdessen wird das MDI-Client Fenster angezeigt. Ein *MDI-Client Fenster* ist ein spezieller Typ von untergeordnetem Fenster, der zur vorregistrierten Fenster Klasse **MdiClient** gehört. Das Client Fenster ist ein untergeordnetes Element des Rahmen Fensters. Er dient als Hintergrund für untergeordnete Fenster. Es bietet auch Unterstützung für das Erstellen und Bearbeiten von untergeordneten Fenstern. Eine MDI-Anwendung kann z. b. untergeordnete Fenster erstellen, aktivieren oder maximieren, indem Sie Nachrichten an das MDI-Client Fenster sendet.

Wenn der Benutzer ein Dokument öffnet oder erstellt, erstellt das Client Fenster ein untergeordnetes Fenster für das Dokument. Das Client Fenster ist das übergeordnete Fenster aller untergeordneten MDI-Fenster in der Anwendung. Jedes untergeordnete Fenster hat einen Größen Anpassungsrahmen, eine Titelleiste, ein Fenstermenü, eine Minimieren-Schaltfläche und eine Schaltfläche zum maximieren. Da ein untergeordnetes Fenster abgeschnitten wird, ist es auf das Client Fenster beschränkt und kann nicht außerhalb des Fensters angezeigt werden.

Eine MDI-Anwendung kann mehr als eine Art von Dokument unterstützen. Eine typische Tabellenkalkulationsanwendung ermöglicht dem Benutzer beispielsweise das Arbeiten mit Diagrammen und Kalkulations Tabellen. Für jeden Dokumenttyp, der von ihm unterstützt wird, muss eine MDI-Anwendung eine untergeordnete Fenster Klasse registrieren und eine Fenster Prozedur zur Unterstützung der Fenster bereitstellen, die zu dieser Klasse gehören. Weitere Informationen zu Fenster Klassen finden Sie unter [window classes](window-classes.md). Weitere Informationen zu Fenster Prozeduren finden Sie unter [Fenster Prozeduren](window-procedures.md).

Im folgenden finden Sie eine typische MDI-Anwendung. Der Name ist "MULTIPAD".

![MULTIPAD-MDI-Anwendungsrahmen Fenster und-Client Fenster](images/csmdi-01.png)

## <a name="child-window-creation"></a>Erstellung des untergeordneten Fensters

Zum Erstellen eines untergeordneten Fensters Ruft eine MDI-Anwendung entweder die Funktion " [**anatemdiwindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) " auf oder sendet die [**WM- \_ mdicreate**](wm-mdicreate.md) -Meldung an das MDI-Client Fenster. Ein effizienteres Verfahren zum Erstellen eines untergeordneten MDI-Fensters ist das Aufrufen [**der Funktion "**](/windows/win32/api/winuser/nf-winuser-createwindowexa) -Funktion", wobei der erweiterte **WS Ex- \_ \_ MDIChild** -Stil angegeben wird.

Um ein untergeordnetes Fenster zu zerstören, sendet eine MDI-Anwendung eine [**WM- \_ mdidestroy**](wm-mdidestroy.md) -Nachricht an das MDI-Client Fenster.

## <a name="child-window-activation"></a>Aktivierung des untergeordneten Fensters

Eine beliebige Anzahl von untergeordneten Fenstern kann jeweils im Client Fenster angezeigt werden, aber nur eine kann aktiv sein. Das aktive untergeordnete Fenster wird vor allen anderen untergeordneten Fenstern positioniert, und der Rahmen wird hervorgehoben.

Der Benutzer kann ein inaktives untergeordnetes Fenster aktivieren, indem er darauf klickt. Eine MDI-Anwendung aktiviert ein untergeordnetes Fenster, indem eine [**WM- \_ mdiaktivierungs**](wm-mdiactivate.md) -Meldung an das MDI-Client Fenster gesendet wird. Wenn das Client Fenster diese Nachricht verarbeitet, sendet Sie eine **WM- \_ mdiaktivierungs** -Meldung an die Fenster Prozedur des untergeordneten Fensters, das aktiviert werden soll, und an die Fenster Prozedur des untergeordneten Fensters, das deaktiviert wird.

Um zu verhindern, dass ein untergeordnetes Fenster aktiviert wird, müssen Sie die [**WM \_ ncaktivierungs**](wm-ncactivate.md) -Meldung an das untergeordnete Fenster durch Zurückgeben von **false**

Das System verfolgt die Position jedes untergeordneten Fensters im Stapel überlappenden Fenster nach. Diese Stapel wird als [Z-Reihenfolge](window-features.md)bezeichnet. Der Benutzer kann das nächste untergeordnete Fenster in der Z-Reihenfolge aktivieren, indem er im Menü "Fenster" im aktiven Fenster auf " **weiter** " klickt. Eine Anwendung aktiviert das nächste (oder vorherige) untergeordnete Fenster in der Z-Reihenfolge, indem eine [**WM- \_ mdinext**](wm-mdinext.md) -Nachricht an das Client Fenster gesendet wird.

Um das Handle für das aktive untergeordnete Fenster abzurufen, sendet die MDI-Anwendung eine [**WM- \_ mdigetactive**](wm-mdigetactive.md) -Nachricht an das Client Fenster.

## <a name="multiple-document-menus"></a>Mehrere Dokument Menüs

Das Rahmen Fenster einer MDI-Anwendung sollte eine Menüleiste mit einem Fenstermenü enthalten. Das Fenstermenü muss Elemente enthalten, die die untergeordneten Fenster im Client Fenster anordnen oder alle untergeordneten Fenster schließen. Das Fenstermenü einer typischen MDI-Anwendung kann die Elemente in der folgenden Tabelle enthalten.



| Menüelement         | Zweck                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Kachel**          | Ordnet untergeordnete Fenster in einem Kachel Format an, sodass jede im Client Fenster vollständig angezeigt wird.                       |
| **Cascade**       | Ordnet untergeordnete Fenster in einem kaskadierenden Format an. Die untergeordneten Fenster überlappen einander, aber die Titelleiste jedes ist sichtbar. |
| **Symbole anordnen** | Ordnet die Symbole der minimierten untergeordneten Fenster am unteren Rand des Client Fensters an.                                     |
| **Alle schließen**     | Schließt alle untergeordneten Fenster.                                                                                                |



 

Wenn ein untergeordnetes Fenster erstellt wird, fügt das System automatisch ein neues Menü Element an das Fenstermenü an. Der Text des Menü Elements ist mit dem Text in der Menüleiste des neuen untergeordneten Fensters identisch. Durch Klicken auf das Menü Element kann der Benutzer das zugehörige untergeordnete Fenster aktivieren. Wenn ein untergeordnetes Fenster zerstört wird, entfernt das System automatisch das entsprechende Menü Element aus dem Fenstermenü.

Das System kann dem Menü "Fenster" bis zu zehn Menü Elemente hinzufügen. Wenn das zehnte untergeordnete Fenster erstellt wird, fügt das System dem Menü Fenster das **Weitere Windows** -Element hinzu. Wenn Sie auf dieses Element klicken, wird das Dialogfeld **Fenster auswählen** angezeigt. Das Dialogfeld enthält ein Listenfeld mit den Titeln aller untergeordneten MDI-Fenster, die derzeit verfügbar sind. Der Benutzer kann ein untergeordnetes Fenster aktivieren, indem er auf seinen Titel im Listenfeld klickt.

Wenn die MDI-Anwendung verschiedene Typen von untergeordneten Fenstern unterstützt, passen Sie die Menüleiste an, um die dem aktiven Fenster zugeordneten Vorgänge widerzuspiegeln. Stellen Sie hierzu separate Menü Ressourcen für jeden Typ von untergeordnetem Fenster bereit, der von der Anwendung unterstützt wird. Wenn ein neuer Typ von untergeordnetem Fenster aktiviert wird, sollte die Anwendung eine [**WM- \_ mdisetmenu**](wm-mdisetmenu.md) -Meldung an das Client Fenster senden und ihr das Handle für das entsprechende Menü übergeben.

Wenn kein untergeordnetes Fenster vorhanden ist, sollte die Menüleiste nur Elemente enthalten, die zum Erstellen oder Öffnen eines Dokuments verwendet werden.

Wenn der Benutzer durch die Verwendung von Cursor Schlüsseln durch die Menüs einer MDI-Anwendung navigiert, Verhalten sich die Schlüssel anders, als wenn der Benutzer durch ein typisches Anwendungsmenü navigiert. In einer MDI-Anwendung übergibt die Steuerung vom Fenstermenü der Anwendung an das Fenstermenü des aktiven untergeordneten Fensters und dann an das erste Element in der Menüleiste.

## <a name="multiple-document-accelerators"></a>Mehrere Dokument Beschleuniger

Zum empfangen und Verarbeiten von Zugriffstasten für die untergeordneten Fenster muss eine MDI-Anwendung die [**translatemdisysaccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) -Funktion in der Nachrichten Schleife enthalten. Die-Schleife muss **translatemdisysaccel** aufrufen, bevor die [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) -oder [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) -Funktion aufgerufen wird.

Zugriffstasten im Menü Fenster für ein untergeordnetes MDI-Fenster unterscheiden sich von denen für ein untergeordnetes MDI-Fenster. In einem untergeordneten MDI-Fenster öffnet die Tastenkombination Alt + – (minus) das Fenstermenü, die Tastenkombination STRG + F4 schließt das aktive untergeordnete Fenster, und die Tastenkombination STRG + F6 aktiviert das nächste untergeordnete Fenster.

## <a name="child-window-size-and-arrangement"></a>Größe und Anordnung des untergeordneten Fensters

Eine MDI-Anwendung steuert die Größe und Position der untergeordneten Fenster durch das Senden von Nachrichten an das MDI-Client Fenster. Zum Maximieren des aktiven untergeordneten Fensters sendet die Anwendung die [**WM- \_ mdimaximiernachricht**](wm-mdimaximize.md) an das Client Fenster. Wenn ein untergeordnetes Fenster maximiert ist, füllt der Client Bereich das MDI-Client Fenster vollständig aus. Außerdem verbirgt das System automatisch die Titelleiste des untergeordneten Fensters und fügt der Menüleiste der MDI-Anwendung das Fenstermenü Symbol und die Schaltfläche Wiederherstellen des untergeordneten Fensters hinzu. Die Anwendung kann das Client Fenster mit der ursprünglichen (vormaximierten) Größe und Position wiederherstellen, indem das Client Fenster eine [**WM- \_ mversstore**](wm-mdirestore.md) -Nachricht sendet.

Eine MDI-Anwendung kann die untergeordneten Fenster in einem Cascade-oder Tile-Format anordnen. Wenn die untergeordneten Fenster kaskadiert werden, werden die Fenster in einem Stapel angezeigt. Das Fenster am unteren Rand des Stapels befindet sich in der oberen linken Ecke des Bildschirms, und die verbleibenden Fenster werden vertikal und horizontal versetzt, sodass der linke Rahmen und die Titelleiste jedes untergeordneten Fensters sichtbar sind. Zum Anordnen von untergeordneten Fenstern im Cascade-Format wird von einer MDI-Anwendung die [**WM- \_ mdicascade**](wm-mdicascade.md) -Nachricht gesendet. In der Regel sendet die Anwendung diese Nachricht, wenn der Benutzer im Menü Fenster auf " **Cascade** " klickt.

Wenn die untergeordneten Fenster nebeneinander angeordnet sind, zeigt das System jedes untergeordnete Fenster in seiner Gesamtheit an – überlappen keines der Fenster. Alle Fenster verfügen ggf. Übergrößen, damit Sie in das Client Fenster passen. Um untergeordnete Fenster im Kachel Format anzuordnen, sendet eine MDI-Anwendung eine [**WM- \_ mditile**](wm-mditile.md) -Nachricht an das Client Fenster. In der Regel sendet die Anwendung diese Nachricht, wenn der Benutzer im Menü Fenster auf die **Kachel** klickt.

Eine MDI-Anwendung sollte ein anderes Symbol für jeden unterstützten Typ von untergeordnetem Fenster bereitstellen. Die Anwendung gibt ein Symbol an, wenn die untergeordnete Fenster Klasse registriert wird. Das System zeigt automatisch das Symbol eines untergeordneten Fensters im unteren Teil des Client Fensters an, wenn das untergeordnete Fenster minimiert wird. Eine MDI-Anwendung leitet das System zum Anordnen von Symbolen für untergeordnete Fenster, indem eine [**WM- \_ mdiiconarrange**](wm-mdiiconarrange.md) -Meldung an das Client Fenster gesendet wird. Normalerweise sendet die Anwendung diese Nachricht, wenn der Benutzer im Menü Fenster auf **Symbole anordnen** klickt.

## <a name="icon-title-windows"></a>Symbol Titel Fenster

Da untergeordnete MDI-Fenster möglicherweise minimiert werden, muss eine MDI-Anwendung die Bearbeitung von Symbol Titel Fenstern so vermeiden, als wären Sie normale untergeordnete MDI-Fenster. Symbol Titel Fenster werden angezeigt, wenn die Anwendung untergeordnete Fenster des MDI-Client Fensters aufzählt. Symbol Titel Fenster unterscheiden sich jedoch insofern von anderen untergeordneten Fenstern, als im Besitz eines untergeordneten MDI-Fensters.

Um zu ermitteln, ob ein untergeordnetes Fenster ein Symbol Titel Fenster ist, verwenden Sie die [**GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) -Funktion mit dem GW- \_ Besitzer Index. Nicht-Titel Fenster geben **null** zurück. Beachten Sie, dass dieser Test für Fenster der obersten Ebene unzureichend ist, da Menüs und Dialogfelder im Besitz von Fenstern sind.

## <a name="child-window-data"></a>Daten des untergeordneten Fensters

Da die Anzahl der untergeordneten Fenster in Abhängigkeit davon variiert, wie viele Dokumente der Benutzer öffnet, muss eine MDI-Anwendung in der Lage sein, Daten (z. b. den Namen der aktuellen Datei) jedem untergeordneten Fenster zuzuordnen. Hierfür gibt es zwei Möglichkeiten:

-   Speichert die Daten des untergeordneten Fensters in der Fenster Struktur.
-   Verwenden Sie die Fenster Eigenschaften.

### <a name="window-structure"></a>Fenster Struktur

Wenn eine MDI-Anwendung eine Fenster Klasse registriert, reserviert Sie möglicherweise zusätzlichen Platz in der Fenster Struktur für Anwendungsdaten, die für diese bestimmte Klasse von Windows spezifisch sind. Zum Speichern und Abrufen von Daten in diesem zusätzlichen Bereich verwendet die Anwendung die Funktionen " [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) " und " [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) ".

Um eine große Datenmenge für ein untergeordnetes Fenster beizubehalten, kann eine Anwendung Arbeitsspeicher für eine Datenstruktur zuweisen und dann das Handle in dem Arbeitsspeicher speichern, der die Struktur im zusätzlichen, dem untergeordneten Fenster zugeordneten Bereich enthält.

### <a name="window-properties"></a>Fenstereigenschaften

In einer MDI-Anwendung können auch Dokument spezifische Daten mithilfe von Fenster Eigenschaften gespeichert werden. *Pro-Dokument-Daten* sind Daten, die für den Dokumenttyp spezifisch sind, der in einem bestimmten untergeordneten Fenster enthalten ist. Eigenschaften unterscheiden sich von zusätzlichem Platz in der Fenster Struktur in, dass Sie beim Registrieren der Fenster Klasse keinen zusätzlichen Platz zuweisen müssen. Ein Fenster kann über eine beliebige Anzahl von Eigenschaften verfügen. Auch wenn Offsets verwendet werden, um auf den zusätzlichen Platz in Fenster Strukturen zuzugreifen, werden Eigenschaften durch Zeichen folgen Namen bezeichnet. Weitere Informationen zu Fenster Eigenschaften finden Sie unter [Fenster Eigenschaften](window-properties.md).

 

 
