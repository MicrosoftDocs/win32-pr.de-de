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

Jedes Dokument in einer MDI-Anwendung (Multiple Document Interface) wird in einem separaten untergeordneten Fenster im Clientbereich des Hauptfensters der Anwendung angezeigt. Typische MDI-Anwendungen sind Anwendungen für die Wortverarbeitung, die es dem Benutzer ermöglichen, mit mehreren Textdokumenten zu arbeiten, und Tabellenkalkulationsanwendungen, mit denen der Benutzer mit mehreren Diagrammen und Tabellen arbeiten kann. Weitere Informationen finden Sie in den folgenden Themen.

-   [Frame-, Client- und untergeordnete Windows](#frame-client-and-child-windows)
-   [Erstellen von untergeordneten Fenstern](#child-window-creation)
-   [Aktivierung des untergeordneten Fensters](#child-window-activation)
-   [Mehrere Dokumentmenüs](#multiple-document-menus)
-   [Mehrere Dokumentbeschleuniger](#multiple-document-accelerators)
-   [Größe und Anordnung des untergeordneten Fensters](#child-window-size-and-arrangement)
-   [Symboltitel Windows](#icon-title-windows)
-   [Daten des untergeordneten Fensters](#child-window-data)
    -   [Fensterstruktur](#window-structure)
    -   [Fenstereigenschaften](#window-properties)

## <a name="frame-client-and-child-windows"></a>Frame-, Client- und untergeordnete Windows

Eine MDI-Anwendung verfügt über drei Arten von Fenstern: ein Rahmenfenster, ein MDI-Clientfenster sowie eine Reihe von untergeordneten Fenstern. Das *Rahmenfenster* ähnelt dem Hauptfenster der Anwendung: Es verfügt über einen Größenrahmen, eine Titelleiste, ein Fenstermenü, eine Schaltfläche zum Minimieren und eine Schaltfläche zum Maximieren. Die Anwendung muss eine Fensterklasse für das Rahmenfenster registrieren und eine Fensterprozedur bereitstellen, um es zu unterstützen.

Eine MDI-Anwendung zeigt keine Ausgabe im Clientbereich des Rahmenfensters an. Stattdessen wird das MDI-Clientfenster angezeigt. Ein *MDI-Clientfenster* ist ein spezieller Typ von untergeordnetem Fenster, das zur vorab registrierten Fensterklasse **MDICLIENT** gehört. Das Clientfenster ist ein untergeordnetes Element des Rahmenfensters. sie dient als Hintergrund für untergeordnete Fenster. Es bietet auch Unterstützung für das Erstellen und Bearbeiten von untergeordneten Fenstern. Beispielsweise kann eine MDI-Anwendung untergeordnete Fenster erstellen, aktivieren oder maximieren, indem Nachrichten an das MDI-Clientfenster gesendet werden.

Wenn der Benutzer ein Dokument öffnet oder erstellt, erstellt das Clientfenster ein untergeordnetes Fenster für das Dokument. Das Clientfenster ist das übergeordnete Fenster aller untergeordneten MDI-Fenster in der Anwendung. Jedes untergeordnete Fenster verfügt über einen Größenrahmen, eine Titelleiste, ein Fenstermenü, eine Schaltfläche zum Minimieren und eine Schaltfläche zum Maximieren. Da ein untergeordnetes Fenster abgeschnitten wird, ist es auf das Clientfenster beschränkt und kann nicht außerhalb des Fensters angezeigt werden.

Eine MDI-Anwendung kann mehrere Arten von Dokumenten unterstützen. Mit einer typischen Tabellenkalkulationsanwendung kann der Benutzer beispielsweise sowohl mit Diagrammen als auch mit Tabellen arbeiten. Für jeden unterstützten Dokumenttyp muss eine MDI-Anwendung eine untergeordnete Fensterklasse registrieren und eine Fensterprozedur bereitstellen, um die zu dieser Klasse gehörenden Fenster zu unterstützen. Weitere Informationen zu Fensterklassen finden Sie unter [Fensterklassen.](window-classes.md) Weitere Informationen zu Fensterprozessen finden Sie unter [Window Procedures](window-procedures.md).

Es folgt eine typische MDI-Anwendung. Der Name lautet Multipad.

![Multipad-mdi-Anwendungsrahmenfenster und Clientfenster](images/csmdi-01.png)

## <a name="child-window-creation"></a>Erstellen von untergeordneten Fenstern

Um ein untergeordnetes Fenster zu erstellen, ruft eine MDI-Anwendung entweder die [**CreateMDIWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) auf oder sendet die [**\_ WM-MDICREATE-Nachricht**](wm-mdicreate.md) an das MDI-Clientfenster. Eine effizientere Möglichkeit zum Erstellen eines untergeordneten MDI-Fensters besteht darin, die [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) aufzurufen und den erweiterten **WS \_ EX \_ MDICHILD-Stil** anzugeben.

Um ein untergeordnetes Fenster zu zerstören, sendet eine MDI-Anwendung eine [**WM \_ MDIDESTROY-Nachricht**](wm-mdidestroy.md) an das MDI-Clientfenster.

## <a name="child-window-activation"></a>Aktivierung des untergeordneten Fensters

Eine beliebige Anzahl von untergeordneten Fenstern kann im Clientfenster gleichzeitig angezeigt werden, aber nur eines kann aktiv sein. Das aktive untergeordnete Fenster wird vor allen anderen untergeordneten Fenstern positioniert, und sein Rahmen ist hervorgehoben.

Der Benutzer kann ein inaktives untergeordnetes Fenster aktivieren, indem er darauf klickt. Eine MDI-Anwendung aktiviert ein untergeordnetes Fenster, indem eine [**\_ WM-MDIACTIVATE-Nachricht**](wm-mdiactivate.md) an das MDI-Clientfenster gesendet wird. Während das Clientfenster diese Nachricht verarbeitet, sendet es eine **WM \_ MDIACTIVATE-Nachricht** an die Fensterprozedur des zu aktivierenden untergeordneten Fensters und an die Fensterprozedur des zu deaktivierenden untergeordneten Fensters.

Um zu verhindern, dass ein untergeordnetes Fenster aktiviert wird, behandeln Sie die [**WM \_ NCACTIVATE-Meldung**](wm-ncactivate.md) an das untergeordnete Fenster, indem Sie **FALSE** zurückgeben.

Das System verfolgt die Position jedes untergeordneten Fensters im Stapel überlappender Fenster. Diese Stapelung wird als [Z-Order](window-features.md)bezeichnet. Der Benutzer kann das nächste untergeordnete Fenster in der Z-Reihenfolge aktivieren, indem er im Fenstermenü im aktiven Fenster auf **Weiter** klickt. Eine Anwendung aktiviert das nächste (oder vorherige) untergeordnete Fenster in der Z-Reihenfolge, indem eine [**\_ WM-MUDIXT-Nachricht**](wm-mdinext.md) an das Clientfenster gesendet wird.

Um das Handle für das aktive untergeordnete Fenster abzurufen, sendet die MDI-Anwendung eine [**WM \_ MDIGETACTIVE-Nachricht**](wm-mdigetactive.md) an das Clientfenster.

## <a name="multiple-document-menus"></a>Mehrere Dokumentmenüs

Das Rahmenfenster einer MDI-Anwendung sollte eine Menüleiste mit einem Fenstermenü enthalten. Das Fenstermenü sollte Elemente enthalten, die die untergeordneten Fenster im Clientfenster anordnen oder alle untergeordneten Fenster schließen. Das Fenstermenü einer typischen MDI-Anwendung kann die Elemente in der folgenden Tabelle enthalten.



| Menüelement         | Zweck                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Kachel**          | Ordnet untergeordnete Fenster in einem Kachelformat so an, dass jedes in seiner Gesamtheit im Clientfenster angezeigt wird.                       |
| **Cascade**       | Ordnet untergeordnete Fenster in einem kaskadierten Format an. Die untergeordneten Fenster überlappen sich, aber die Titelleiste jedes Fensters ist sichtbar. |
| **Symbole anordnen** | Ordnet die Symbole minimierter untergeordneter Fenster am unteren Rand des Clientfensters an.                                     |
| **Alle schließen**     | Schließt alle untergeordneten Fenster.                                                                                                |



 

Wenn ein untergeordnetes Fenster erstellt wird, fügt das System automatisch ein neues Menüelement an das Fenstermenü an. Der Text des Menüelements entspricht dem Text auf der Menüleiste des neuen untergeordneten Fensters. Durch Klicken auf das Menüelement kann der Benutzer das entsprechende untergeordnete Fenster aktivieren. Wenn ein untergeordnetes Fenster zerstört wird, entfernt das System automatisch das entsprechende Menüelement aus dem Fenstermenü.

Das System kann dem Fenstermenü bis zu zehn Menüelemente hinzufügen. Wenn das zehnte untergeordnete Fenster erstellt wird, fügt das System dem Fenstermenü das Element **More Windows** hinzu. Wenn Sie auf dieses Element klicken, wird das Dialogfeld **Fenster auswählen** angezeigt. Das Dialogfeld enthält ein Listenfeld mit den Titeln aller derzeit verfügbaren untergeordneten MDI-Fenster. Der Benutzer kann ein untergeordnetes Fenster aktivieren, indem er im Listenfeld auf seinen Titel klickt.

Wenn Ihre MDI-Anwendung mehrere Arten von untergeordneten Fenstern unterstützt, passen Sie die Menüleiste an die Vorgänge an, die dem aktiven Fenster zugeordnet sind. Stellen Sie hierzu separate Menüressourcen für jeden Typ des untergeordneten Fensters bereit, das von der Anwendung unterstützt wird. Wenn ein neuer Typ des untergeordneten Fensters aktiviert wird, sollte die Anwendung eine [**WM \_ MDISETMENU-Nachricht**](wm-mdisetmenu.md) an das Clientfenster senden und das Handle an das entsprechende Menü übergeben.

Wenn kein untergeordnetes Fenster vorhanden ist, sollte die Menüleiste nur Elemente enthalten, die zum Erstellen oder Öffnen eines Dokuments verwendet werden.

Wenn der Benutzer mithilfe von Cursortasten durch die Menüs einer MDI-Anwendung navigiert, verhalten sich die Schlüssel anders als wenn der Benutzer durch die Menüs einer typischen Anwendung navigiert. In einer MDI-Anwendung wird die Steuerung vom Fenstermenü der Anwendung an das Fenstermenü des aktiven untergeordneten Fensters und dann an das erste Element in der Menüleiste übergeben.

## <a name="multiple-document-accelerators"></a>Mehrere Dokumentbeschleuniger

Um Zugriffstasten für die untergeordneten Fenster zu empfangen und zu verarbeiten, muss eine MDI-Anwendung die [**TranslateMDISysAccel-Funktion**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) in ihre Nachrichtenschleife einschließen. Die Schleife muss **TranslateMDISysAccel aufrufen,** bevor die [**TranslateAccelerator-**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) oder [**DispatchMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) aufgerufen wird.

Zugriffstasten im Fenstermenü für ein untergeordnetes MDI-Fenster unterscheiden sich von denen für ein untergeordnetes MDI-nicht-Fenster. In einem untergeordneten MDI-Fenster öffnet die Tastenkombination ALT+ (minus) das Fenstermenü, die Tastenkombination STRG+F4 schließt das aktive untergeordnete Fenster, und die Tastenkombination STRG+F6 aktiviert das nächste untergeordnete Fenster.

## <a name="child-window-size-and-arrangement"></a>Größe und Anordnung des untergeordneten Fensters

Eine MDI-Anwendung steuert die Größe und Position ihrer untergeordneten Fenster, indem Nachrichten an das MDI-Clientfenster gesendet werden. Um das aktive untergeordnete Fenster zu maximieren, sendet die Anwendung die [**WM \_ MDIMAXIMIZE-Nachricht**](wm-mdimaximize.md) an das Clientfenster. Wenn ein untergeordnetes Fenster maximiert wird, füllt sein Clientbereich das MDI-Clientfenster vollständig aus. Darüber hinaus blendet das System die Titelleiste des untergeordneten Fensters automatisch aus und fügt der Menüleiste der MDI-Anwendung das Fenstermenüsymbol und die Schaltfläche Wiederherstellen hinzu. Die Anwendung kann das Clientfenster auf die ursprüngliche (vorabmaximierte) Größe und Position wiederherstellen, indem sie eine [**WM \_ MDMAKERSTORE-Nachricht**](wm-mdirestore.md) an das Clientfenster sendet.

Eine MDI-Anwendung kann ihre untergeordneten Fenster im Kaskadieren- oder Kachelformat anordnen. Wenn die untergeordneten Fenster kaskadiert werden, werden die Fenster in einem Stapel angezeigt. Das Fenster am unteren Rand des Stapels nimmt die obere linke Ecke des Bildschirms ein, und die verbleibenden Fenster werden vertikal und horizontal versetzt, sodass der linke Rahmen und die Titelleiste jedes untergeordneten Fensters sichtbar sind. Um untergeordnete Fenster im kaskadierten Format anzuordnen, sendet eine MDI-Anwendung die [**\_ WM-MDICASCADE-Nachricht.**](wm-mdicascade.md) In der Regel sendet die Anwendung diese Nachricht, wenn der Benutzer im Fenstermenü auf **Cascade** klickt.

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

 

 
