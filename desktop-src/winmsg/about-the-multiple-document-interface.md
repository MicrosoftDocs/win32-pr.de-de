---
description: Jedes Dokument in einer MDI-Anwendung (Multiple Document Interface) wird in einem separaten untergeordneten Fenster im Clientbereich des Hauptfensters der Anwendung angezeigt.
ms.assetid: 35dff281-3b11-4954-85cf-a0f1c9ed346a
title: Informationen zur Schnittstelle für mehrere Dokumente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071d3bebad8e6aba48b69b66fd41f9f7933c1d9785ae38512003aaf1bd9a19e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706000"
---
# <a name="about-the-multiple-document-interface"></a>Informationen zur Schnittstelle für mehrere Dokumente

Jedes Dokument in einer MDI-Anwendung (Multiple Document Interface) wird in einem separaten untergeordneten Fenster im Clientbereich des Hauptfensters der Anwendung angezeigt. Typische MDI-Anwendungen sind Anwendungen zur Textverarbeitung, die es dem Benutzer ermöglichen, mit mehreren Textdokumenten zu arbeiten, und Tabellenkalkulationsanwendungen, die es dem Benutzer ermöglichen, mit mehreren Diagrammen und Kalkulationstabellen zu arbeiten. Weitere Informationen finden Sie in den folgenden Themen.

-   [Frame-, Client- und untergeordnete Windows](#frame-client-and-child-windows)
-   [Erstellung eines untergeordneten Fensters](#child-window-creation)
-   [Aktivierung des untergeordneten Fensters](#child-window-activation)
-   [Mehrere Dokumentmenüs](#multiple-document-menus)
-   [Mehrere Dokumentbeschleuniger](#multiple-document-accelerators)
-   [Größe und Anordnung des untergeordneten Fensters](#child-window-size-and-arrangement)
-   [Symboltitel Windows](#icon-title-windows)
-   [Daten des untergeordneten Fensters](#child-window-data)
    -   [Fensterstruktur](#window-structure)
    -   [Fenstereigenschaften](#window-properties)

## <a name="frame-client-and-child-windows"></a>Frame-, Client- und untergeordnete Windows

Eine MDI-Anwendung verfügt über drei Arten von Fenstern: ein Rahmenfenster, ein MDI-Clientfenster sowie eine Reihe untergeordneter Fenster. Das *Rahmenfenster* ist wie das Hauptfenster der Anwendung: Es verfügt über einen Größenrahmen, eine Titelleiste, ein Fenstermenü, eine Schaltfläche zum Minimieren und eine Schaltfläche zum Maximieren. Die Anwendung muss eine Fensterklasse für das Rahmenfenster registrieren und eine Fensterprozedur zur Unterstützung bereitstellen.

Eine MDI-Anwendung zeigt keine Ausgabe im Clientbereich des Rahmenfensters an. Stattdessen wird das MDI-Clientfenster angezeigt. Ein *MDI-Clientfenster* ist ein spezieller Typ von untergeordnetem Fenster, das zur vorab registrierten Fensterklasse **MDICLIENT gehört.** Das Clientfenster ist ein untergeordnetes Fenster des Rahmenfensters. sie dient als Hintergrund für untergeordnete Fenster. Sie bietet auch Unterstützung für das Erstellen und Bearbeiten von untergeordneten Fenstern. Beispielsweise kann eine MDI-Anwendung untergeordnete Fenster erstellen, aktivieren oder maximieren, indem Nachrichten an das MDI-Clientfenster gesendet werden.

Wenn der Benutzer ein Dokument öffnet oder erstellt, erstellt das Clientfenster ein untergeordnetes Fenster für das Dokument. Das Clientfenster ist das übergeordnete Fenster aller untergeordneten MDI-Fenster in der Anwendung. Jedes untergeordnete Fenster verfügt über einen Größenrahmen, eine Titelleiste, ein Fenstermenü, eine Schaltfläche zum Minimieren und eine Schaltfläche zum Maximieren. Da ein untergeordnetes Fenster abgeschnitten wird, ist es auf das Clientfenster beschränkt und kann nicht außerhalb des Fensters angezeigt werden.

Eine MDI-Anwendung kann mehrere Arten von Dokumenten unterstützen. Eine typische Tabellenkalkulationsanwendung ermöglicht es dem Benutzer beispielsweise, sowohl mit Diagrammen als auch mit Tabellen zu arbeiten. Für jeden unterstützten Dokumenttyp muss eine MDI-Anwendung eine untergeordnete Fensterklasse registrieren und eine Fensterprozedur bereitstellen, um die Fenster zu unterstützen, die zu dieser Klasse gehören. Weitere Informationen zu Fensterklassen finden Sie unter [Fensterklassen.](window-classes.md) Weitere Informationen zu Fenster-Prozeduren finden Sie unter [Fenster prozeduren](window-procedures.md).

Es folgt eine typische MDI-Anwendung. Er heißt Multipad.

![Multipad-mdi-Anwendungsframefenster und Clientfenster](images/csmdi-01.png)

## <a name="child-window-creation"></a>Erstellung eines untergeordneten Fensters

Zum Erstellen eines untergeordneten Fensters ruft eine MDI-Anwendung entweder die [**CreateMDIWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) auf oder sendet die [**WM \_ MDICREATE-Nachricht**](wm-mdicreate.md) an das MDI-Clientfenster. Eine effizientere Möglichkeit zum Erstellen eines untergeordneten MDI-Fensters ist das Aufrufen der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) unter Angabe des erweiterten **WS \_ EX \_ MDICHILD-Stils.**

Um ein untergeordnetes Fenster zu zerstören, sendet eine MDI-Anwendung eine [**WM \_ MDIDESTROY-Nachricht**](wm-mdidestroy.md) an das MDI-Clientfenster.

## <a name="child-window-activation"></a>Aktivierung des untergeordneten Fensters

Eine beliebige Anzahl von untergeordneten Fenstern kann gleichzeitig im Clientfenster angezeigt werden, aber nur eines kann aktiv sein. Das aktive untergeordnete Fenster wird vor allen anderen untergeordneten Fenstern positioniert, und sein Rahmen ist hervorgehoben.

Der Benutzer kann ein inaktives untergeordnetes Fenster aktivieren, indem er darauf klickt. Eine MDI-Anwendung aktiviert ein untergeordnetes Fenster, indem eine [**WM \_ MDIACTIVATE-Nachricht**](wm-mdiactivate.md) an das MDI-Clientfenster gesendet wird. Während das Clientfenster diese Nachricht verarbeitet, sendet es eine **WM \_ MDIACTIVATE-Nachricht** an die Fensterprozedur des zu aktivierenden untergeordneten Fensters und an die Fensterprozedur des untergeordneten Fensters, das deaktiviert wird.

Um zu verhindern, dass ein untergeordnetes Fenster aktiviert wird, behandeln Sie die [**WM \_ NCACTIVATE-Nachricht**](wm-ncactivate.md) an das untergeordnete Fenster, indem Sie **FALSE zurückgeben.**

Das System verfolgt die Position jedes untergeordneten Fensters im Stapel überlappender Fenster nach. Diese Stapelung wird als [Z-Order bezeichnet.](window-features.md) Der Benutzer kann das nächste untergeordnete Fenster in  der Z-Reihenfolge aktivieren, indem er im aktiven Fenster im Fenstermenü auf Weiter klickt. Eine Anwendung aktiviert das nächste (oder vorherige) untergeordnete Fenster in der Z-Reihenfolge, indem eine [**WM \_ MDINEXT-Nachricht**](wm-mdinext.md) an das Clientfenster gesendet wird.

Um das Handle für das aktive untergeordnete Fenster abzurufen, sendet die MDI-Anwendung eine [**WM \_ MDIGETACTIVE-Nachricht**](wm-mdigetactive.md) an das Clientfenster.

## <a name="multiple-document-menus"></a>Mehrere Dokumentmenüs

Das Rahmenfenster einer MDI-Anwendung sollte eine Menüleiste mit einem Fenstermenü enthalten. Das Fenstermenü sollte Elemente enthalten, die die untergeordneten Fenster im Clientfenster anordnen oder alle untergeordneten Fenster schließen. Das Fenstermenü einer typischen MDI-Anwendung kann die Elemente in der folgenden Tabelle enthalten.



| Menüelement         | Zweck                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Kachel**          | Ordnet untergeordnete Fenster in einem Kachelformat an, sodass jedes fenster vollständig im Clientfenster angezeigt wird.                       |
| **Cascade**       | Ordnet untergeordnete Fenster in einem kaskadierten Format an. Die untergeordneten Fenster überlappen sich, aber die Titelleiste der einzelnen Fenster ist sichtbar. |
| **Symbole anordnen** | Ordnet die Symbole minimierter untergeordneter Fenster am unteren Rand des Clientfensters an.                                     |
| **Alle schließen**     | Schließt alle untergeordneten Fenster.                                                                                                |



 

Jedes Mal, wenn ein untergeordnetes Fenster erstellt wird, fügt das System automatisch ein neues Menüelement an das Fenstermenü an. Der Text des Menüelements ist mit dem Text auf der Menüleiste des neuen untergeordneten Fensters identisch. Durch Klicken auf das Menüelement kann der Benutzer das entsprechende untergeordnete Fenster aktivieren. Wenn ein untergeordnetes Fenster zerstört wird, entfernt das System automatisch das entsprechende Menüelement aus dem Fenstermenü.

Das System kann dem Fenstermenü bis zu zehn Menüelemente hinzufügen. Wenn das zehnte untergeordnete Fenster erstellt wird, fügt das System das Element **Weitere Windows** dem Fenstermenü hinzu. Wenn Sie auf dieses Element klicken, wird **das Dialogfeld Fenster** auswählen angezeigt. Das Dialogfeld enthält ein Listenfeld mit den Titeln aller derzeit verfügbaren untergeordneten MDI-Fenster. Der Benutzer kann ein untergeordnetes Fenster aktivieren, indem er auf seinen Titel im Listenfeld klickt.

Wenn Ihre MDI-Anwendung mehrere Arten von untergeordneten Fenstern unterstützt, passen Sie die Menüleiste an die Vorgänge an, die dem aktiven Fenster zugeordnet sind. Stellen Sie hierzu separate Menüressourcen für jeden untergeordneten Fenstertyp zur Verfügung, den die Anwendung unterstützt. Wenn ein neuer Typ von untergeordnetem Fenster aktiviert wird, sollte die Anwendung eine [**WM \_ MDISETMENU-Nachricht**](wm-mdisetmenu.md) an das Clientfenster senden und das Handle an das entsprechende Menü übergeben.

Wenn kein untergeordnetes Fenster vorhanden ist, sollte die Menüleiste nur Elemente enthalten, die zum Erstellen oder Öffnen eines Dokuments verwendet werden.

Wenn der Benutzer mithilfe von Cursortasten durch die Menüs einer MDI-Anwendung navigiert, verhalten sich die Schlüssel anders als wenn der Benutzer durch die Menüs einer typischen Anwendung navigiert. In einer MDI-Anwendung übergibt das Steuerelement vom Fenstermenü der Anwendung an das Fenstermenü des aktiven untergeordneten Fensters und dann an das erste Element in der Menüleiste.

## <a name="multiple-document-accelerators"></a>Mehrere Dokumentbeschleuniger

Um Zugriffstasten für die untergeordneten Fenster zu empfangen und zu verarbeiten, muss eine MDI-Anwendung die [**TranslateMDISysAccel-Funktion**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) in die Meldungsschleife enthalten. Die Schleife muss **TranslateMDISysAccel aufrufen,** bevor die [**TranslateAccelerator-**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) oder [**DispatchMessage-Funktion aufruft.**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)

Zugriffstasten im Fenstermenü für ein untergeordnetes MDI-Fenster unterscheiden sich von denen für ein untergeordnetes Fenster ohne MDI. In einem untergeordneten MDI-Fenster öffnet die Tastenkombination ALT+ – (Minus) das Fenstermenü, die Tastenkombination STRG+F4 schließt das aktive untergeordnete Fenster, und die Tastenkombination STRG+F6 aktiviert das nächste untergeordnete Fenster.

## <a name="child-window-size-and-arrangement"></a>Größe und Anordnung des untergeordneten Fensters

Eine MDI-Anwendung steuert die Größe und Position der untergeordneten Fenster, indem sie Nachrichten an das MDI-Clientfenster sendet. Um das aktive untergeordnete Fenster zu maximieren, sendet die Anwendung die [**WM \_ MDIMAXIMIZE-Nachricht**](wm-mdimaximize.md) an das Clientfenster. Wenn ein untergeordnetes Fenster maximiert ist, füllt sein Clientbereich das MDI-Clientfenster vollständig aus. Darüber hinaus blendet das System automatisch die Titelleiste des untergeordneten Fensters aus und fügt der Menüleiste der MDI-Anwendung das Fenstermenüsymbol und die Schaltfläche Wiederherstellen des untergeordneten Fensters hinzu. Die Anwendung kann das Clientfenster auf seine ursprüngliche (vorabmaximierte) Größe und Position wiederherstellen, indem sie dem Clientfenster eine [**WM \_ MDUNGSTORE-Nachricht**](wm-mdirestore.md) sendet.

Eine MDI-Anwendung kann ihre untergeordneten Fenster entweder in einem Kaskadierungs- oder Kachelformat anordnen. Wenn die untergeordneten Fenster kaskadiert werden, werden die Fenster in einem Stapel angezeigt. Das Fenster am unteren Rand des Stapels nimmt die obere linke Ecke des Bildschirms ein, und die verbleibenden Fenster werden vertikal und horizontal versetzt, sodass der linke Rahmen und die Titelleiste jedes untergeordneten Fensters sichtbar sind. Um untergeordnete Fenster im kaskadierten Format zu anordnen, sendet eine MDI-Anwendung die [**WM \_ MDICASCADE-Nachricht.**](wm-mdicascade.md) In der Regel sendet die Anwendung diese Meldung, wenn der Benutzer im Fenstermenü auf **Cascade** klickt.

Wenn die untergeordneten Fenster gekachelt werden, zeigt das System jedes untergeordnete Fenster in seiner Gesamtheit an– überlappend keines der Fenster. Alle Fenster sind nach Bedarf so dimensionieren, dass sie in das Clientfenster passen. Um untergeordnete Fenster im Kachelformat anzuordnen, sendet eine MDI-Anwendung eine [**WM \_ MDITILE-Nachricht**](wm-mditile.md) an das Clientfenster. In der Regel sendet die Anwendung diese Meldung, wenn der Benutzer im Fenstermenü auf **Kachel** klickt.

Eine MDI-Anwendung sollte ein anderes Symbol für jeden Typ des unterstützten untergeordneten Fensters bereitstellen. Die Anwendung gibt beim Registrieren der untergeordneten Fensterklasse ein Symbol an. Das System zeigt automatisch das Symbol eines untergeordneten Fensters im unteren Teil des Clientfensters an, wenn das untergeordnete Fenster minimiert wird. Eine MDI-Anwendung weist das System an, untergeordnete Fenstersymbole anzuordnen, indem eine [**WM \_ MDIICONARRANGE-Nachricht**](wm-mdiiconarrange.md) an das Clientfenster gesendet wird. In der Regel sendet die Anwendung diese Meldung, wenn der Benutzer im Fenstermenü auf **Symbole anordnen** klickt.

## <a name="icon-title-windows"></a>Symboltitel Windows

Da untergeordnete MDI-Fenster minimiert werden können, muss eine MDI-Anwendung das Bearbeiten von Symboltitelfenstern vermeiden, als wären sie normale untergeordnete MDI-Fenster. Symboltitelfenster werden angezeigt, wenn die Anwendung untergeordnete Fenster des MDI-Clientfensters aufzählt. Symboltitelfenster unterscheiden sich jedoch von anderen untergeordneten Fenstern, da sie sich im Besitz eines untergeordneten MDI-Fensters befinden.

Um zu bestimmen, ob ein untergeordnetes Fenster ein Symboltitelfenster ist, verwenden Sie die [**GetWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-getwindow) mit dem GW \_ OWNER-Index. Fenster ohne Titel geben **NULL** zurück. Beachten Sie, dass dieser Test für Fenster der obersten Ebene nicht ausreicht, da Menüs und Dialogfelder sich im Besitz von Fenstern befinden.

## <a name="child-window-data"></a>Daten des untergeordneten Fensters

Da die Anzahl der untergeordneten Fenster abhängig davon variiert, wie viele Dokumente der Benutzer öffnet, muss eine MDI-Anwendung daten (z. B. den Namen der aktuellen Datei) jedem untergeordneten Fenster zuordnen können. Hierfür gibt es zwei Möglichkeiten:

-   Store untergeordnete Fensterdaten in der Fensterstruktur.
-   Verwenden Sie Fenstereigenschaften.

### <a name="window-structure"></a>Fensterstruktur

Wenn eine MDI-Anwendung eine Fensterklasse registriert, reserviert sie möglicherweise zusätzlichen Platz in der Fensterstruktur für Anwendungsdaten, die für diese bestimmte Windows-Klasse spezifisch sind. Um Daten in diesem zusätzlichen Bereich zu speichern und abzurufen, verwendet die Anwendung die Funktionen [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) und [**SetWindowLong.**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)

Um eine große Datenmenge für ein untergeordnetes Fenster zu verwalten, kann eine Anwendung Speicher für eine Datenstruktur zuordnen und dann das Handle im Speicher speichern, der die Struktur enthält, in dem zusätzlichen Speicherplatz, der dem untergeordneten Fenster zugeordnet ist.

### <a name="window-properties"></a>Fenstereigenschaften

Eine MDI-Anwendung kann auch Dokumentdaten mithilfe von Fenstereigenschaften speichern. *Daten pro Dokument* sind Daten, die für den Typ des Dokuments in einem bestimmten untergeordneten Fenster spezifisch sind. Eigenschaften unterscheiden sich von zusätzlichem Speicherplatz in der Fensterstruktur in , da Sie beim Registrieren der Fensterklasse keinen zusätzlichen Speicherplatz zuweisen müssen. Ein Fenster kann eine beliebige Anzahl von Eigenschaften aufweisen. Wenn Offsets verwendet werden, um auf den zusätzlichen Platz in Fensterstrukturen zuzugreifen, werden Eigenschaften durch Zeichenfolgennamen bezeichnet. Weitere Informationen zu Fenstereigenschaften finden Sie unter [Fenstereigenschaften.](window-properties.md)

 

 
