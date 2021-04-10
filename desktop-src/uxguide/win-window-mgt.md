---
title: Fensterverwaltung
description: Dieser Artikel befasst sich mit der Standard Platzierung von Windows, wenn Sie anfänglich auf dem Bildschirm angezeigt wird, der Stapelreihenfolge relativ zu anderen Fenstern (Z-Reihenfolge), der Anfangs Größe und der Auswirkung der Anzeige auf den Eingabefokus
ms.assetid: d81bd71c-6d8f-45a9-82cb-bdb9b8bcbb11
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dc194741713a139f643ad84b829294577d020d94
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103961076"
---
# <a name="window-management"></a>Fensterverwaltung

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Dieser Artikel befasst sich mit der Standard Platzierung von Windows, wenn Sie anfänglich auf dem Bildschirm angezeigt wird, der Stapelreihenfolge relativ zu anderen Fenstern ([Z-Reihenfolge](glossary.md)), der Anfangs Größe und der Auswirkung der Anzeige auf den Eingabefokus

Für die folgenden Richtlinien:

-   Ein Fenster der obersten Ebene verfügt über kein Besitzer Fenster und wird auf der Taskleiste angezeigt. Beispiele: Anwendungsfenster. In Windows Vista und höher werden Dialogfelder ohne Besitzer Fenster und Eigenschaften Blätter auch als oberste Ebene betrachtet.
-   Ein eigenes Fenster verfügt über ein Besitzer Fenster und wird nicht auf der Taskleiste angezeigt. Beispiele: modale Dialogfelder, nicht modale Dialogfelder.
-   Ein Benutzer initiiertes Fenster wird als direktes Ergebnis der Aktion eines Benutzers angezeigt. Andernfalls wird das Programm initiiert, wenn es von einem Programm initiiert wird, oder das von Microsoft Windows initiierte System initiiert. Beispielsweise wird ein Dialogfeld "Optionen" vom Benutzer initiiert, aber eine Besprechungs Erinnerung ist Programm initiiert.
-   Ein Kontext Fenster ist ein vom Benutzer initiiertes Fenster, das eine starke Beziehung zu dem Objekt aufweist, von dem es gestartet wurde. Beispielsweise sind Fenster, die von Kontextmenüs oder Benachrichtigungs Bereichs Symbolen angezeigt werden, kontextbezogen, aber von Menüleisten angezeigte Fenster nicht.
-   Der aktive Monitor ist der Monitor, auf dem das aktive Programm ausgeführt wird.
-   Der Standard Monitor ist der Standard Monitor mit dem Startmenü, der Taskleiste und dem Benachrichtigungsbereich.

## <a name="design-concepts"></a>Entwurfskonzepte

Die Fensterverwaltung ist eine der grundlegendsten Benutzeraktivitäten. Vor Windows Vista wurden Windows häufig kleine Standardgrößen und in der Mitte des Bildschirms platziert. Diese Vorgehensweise eignet sich gut für ältere Monitore mit niedriger Auflösung, aber nicht für moderne Video Hardware.

Windows ist für die Unterstützung moderner Video Hardware konzipiert, die häufig bei Auflösungen mit einer deutlich höheren Auflösung als der mindestens unterstützten Bildschirmauflösung und möglicherweise über mehrere Monitore ausgeführt wird. Dies geschieht:

-   Ermöglicht es Benutzern, vollständig von der erweiterten Hardware zu profitieren.
-   Erfordert weniger Aufwand von Benutzern, um Ihre Maus über größere Entfernungen hinweg zu bewegen.
-   Macht die Fensterplatzierung besser vorhersagbar und somit leichter zu finden.

### <a name="the-minimum-supported-screen-resolution"></a>Die mindestens unterstützte Bildschirmauflösung

Die von Windows unterstützte minimale [effektive Bildschirmauflösung](glossary.md) beträgt 800 x 600 Pixel. Dies bedeutet, dass Fenster mit fester Größe vollständig mit der minimalen Auflösung angezeigt werden sollten (beim Reservieren von Speicherplatz für die Taskleiste), aber die Größe der Fenstergröße kann für eine effektive Auflösung von 1024 x 768 Pixel optimiert werden, solange Sie bei minimaler Auflösung funktionsfähig sind.

Die gängigsten physischen Bildschirmauflösungen für Windows-PCs sind momentan 1024 x 768 Pixel oder höher, mit einer Zielplattform von 800 x 600 Pixel können Windows folgende Aktionen ausführen:

-   Arbeiten Sie gut mit der gesamten modernen Hardware, einschließlich der kleinen Notebook-PCs.
-   Unterstützung von hohen DPI-Einstellungen (dots per inch).
-   Unterstützung größerer Schriftarten für Barrierefreiheit.
-   Unterstützen Sie Hardware, die auf globaler Basis verwendet wird.

Wenn Sie die minimale Auflösung für die Unterstützung auswählen, müssen Sie die richtige Balance drücken. Das Ziel einer höheren Auflösung würde zu einer suboptimalen Oberfläche für einen erheblichen Prozentsatz moderner Hardware führen, während das Ziel einer niedrigeren Auflösung verhindern würde, dass Designer den verfügbaren Bildschirmbereich voll ausschöpfen.

Wenn Sie der Ansicht sind, dass die Ziel Benutzer bedeutend höhere Auflösungen als das Windows-Mindestwert verwenden, können Sie das Programm so entwerfen, dass der zusätzliche Bildschirmbereich vollständig genutzt wird, indem Sie die Größe anpassen, die sich gut skalieren lässt.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Unterstützen Sie die minimale effektive Windows-Auflösung von 800 x 600 Pixel.** Für wichtige Benutzeroberflächen (UIs), die im abgesicherten Modus funktionieren müssen, unterstützen Sie eine effektive Auflösung von 640 x 480 Pixeln. Achten Sie darauf, den von der Taskleiste verwendeten Speicherplatz zu berücksichtigen, indem Sie 48 vertikale [relative Pixel](glossary.md) für Windows reservieren, der mit der Taskleiste angezeigt wird.
-   **Optimieren Sie die Größe der Größe der Fensterlayouts für eine effektive Auflösung von 1024 x 768 Pixeln.** Ändern Sie automatisch die Größe dieser Fenster für niedrigere Bildschirmauflösungen auf eine Weise, die noch funktionsfähig ist.
-   **Achten Sie darauf, dass Sie Ihre Fenster in 96 dpi (100 Prozent) mit 800 x 600 Pixel, 120 dpi (125 Prozent) bei 1024 x 768 Pixel und 144 dpi (150 Prozent) bei 1200 x 900 Pixeln testen.** Überprüfen Sie Layoutprobleme, z. b. das Abschneiden von Steuerelementen, Text und Fenstern und das Strecken von Symbolen und Bitmaps.
-   **Für Programme mit Berührungs-und mobilen Verwendungs Szenarien optimieren Sie für 120 dpi.** High-dpi-Bildschirme sind aktuell auf touchpcs und mobilen PCs weit verbreitet.
-   In der Größe von Fenstern mit Größen **Änderung muss das Symbol für die Größenänderung** in der unteren rechten Ecke nicht mehr angezeigt werden, da:
    -   Alle Seiten und Kanten eines Fensters können in der Größe geändert werden, nicht nur in der unteren rechten Ecke.
    -   Das Symbol erfordert, dass eine Statusleiste angezeigt wird, aber viele Fenster mit Größenänderung enthalten keine Status leisten.
    -   Die Größe der Fensterränder und Größenänderung von Fenstern ist effektiver bei der Kommunikation, dass die Größe eines Fensters geändert werden kann, als das Symbol für die Größenänderung.

### <a name="title-bar-controls"></a>Titelleisten-Steuerelemente

Verwenden Sie die Steuerelemente der Titelleiste wie folgt:

-   **Ihrer.** Alle primären und sekundären Fenster mit einem Standardfenster Rahmen sollten in der Titelleiste eine Schaltfläche Schließen aufweisen. Wenn Sie auf Schließen klicken, wird das Fenster abgebrochen oder geschlossen.

![Screenshot des Dialog Felds ohne Schaltfläche "Schließen" ](images/win-window-mgt-image1.png)

In diesem Beispiel hat das Dialogfeld in der Titelleiste keine Schaltfläche Schließen.

-   **Verkleinern.** Alle primären Fenster und sekundären Fenster mit langer Laufzeit (z. b. Fortschritts Dialoge) sollten eine Schaltfläche Minimieren aufweisen. Durch Klicken auf minimieren wird das Fenster auf die Task leisten Schaltfläche reduziert Folglich ist für Windows, das minimiert werden kann, ein Titelleisten Symbol erforderlich.
-   **Maximieren/Wiederherstellen.** Alle in der Größe geänderten Fenster sollten eine Schaltfläche "Maximieren/Wiederherstellen" aufweisen. Wenn Sie auf maximieren klicken, wird das Fenster in der größten Größe angezeigt, in dem die meisten Fenster den Vollbildmodus Wenn Sie auf Wiederherstellen klicken, wird das Fenster in der vorherigen Größe angezeigt. Einige Fenster profitieren jedoch nicht von der Verwendung eines voll Bildschirms, daher sollten diese Fenster die größte nützliche Größe maximieren.

### <a name="window-size"></a>Fenstergröße

-   **Wählen Sie eine Standardfenster Größe aus, die für den Inhalt geeignet ist.** Achten Sie darauf, größere anfängliche Fenstergrößen zu verwenden, wenn Sie den Raum effektiv verwenden können.
-   **Verwenden Sie nach Möglichkeit die Größe der Fenstergröße, um Scrollleisten und abgeschnittene Daten zu vermeiden.** Fenster mit dynamischen Inhalten und Listen profitieren am meisten von Fenstern mit Größenänderung.
-   **Bei Textdokumenten wird eine maximale Zeilenlänge von 65 Zeichen berücksichtigt** , damit der Text leichter lesbar ist. (Zeichen umfassen Buchstaben, Interpunktions Zeichen und Leerzeichen.)
-   Fenster mit fester Größe:
    -   **Muss vollständig sichtbar sein und in den Arbeitsbereich passen.**
-   Fenster mit Größenänderung:
    -   **Kann für eine höhere Auflösung optimiert werden, aber nach Bedarf zur Anzeigezeit auf die tatsächliche Bildschirmauflösung verkleinert werden.**
    -   **Für progressivere Fenstergrößen müssen progressivere Informationen angezeigt werden.** Stellen Sie sicher, dass mindestens ein Fenster Teil bzw. das Steuerelement Inhalt geändert werden konnte.
    -   **Vermeiden Sie die wiederhergestellten Standardgrößen, die maximiert oder nahezu maximiert sind.** Wählen Sie stattdessen eine Standardgröße aus, die in der Regel die nützlichste ist, ohne voll Bildschirm zu verwenden. Angenommen, die Benutzer maximieren das Fenster, anstatt die Größe zu ändern, um den voll Bildschirm zu machen.
    -   **Sollte eine minimale Fenstergröße festlegen, wenn eine Größe vorhanden ist, unter der der Inhalt nicht mehr verwendbar ist.** Legen Sie für Steuerelemente, die in der Größe geändert werden können, die Element Größen mit minimaler Größe auf die kleinsten funktionsgrößen fest, z. b. die minimale funktionale Spaltenbreite
    -   **Sollten Sie die Präsentation ändern, wenn der Inhalt dadurch in geringerer Größe verwendet werden kann.**

![Screenshot der Media Player-Schaltflächen ](images/win-window-mgt-image2.png)

In diesem Beispiel ändert Windows Media Player sein Format, wenn das Fenster für das Standardformat zu klein wird.

### <a name="window-location"></a>Fensterposition

-   **Für die folgenden Richtlinien bedeutet "Centering", dass die vertikale Platzierung leicht auf den oberen Rand des Monitors ausgerichtet ist, anstatt genau in der Mitte zu platzieren.** Legen Sie 45 Prozent des Speicherplatzes zwischen dem oberen Rand des Monitors/Besitzers und dem oberen Fenster des Fensters und 55 Prozent zwischen dem unteren Rand des Monitors/Besitzers und des unteren Fensters ab. Gehen Sie wie folgt vor, da das Auge natürlich am oberen Bildschirmrand ausgerichtet ist.

    ![Abbildung des Fensters, das sich leicht oberhalb der Mitte befindet ](images/win-window-mgt-image3.png)

    "Centering" bedeutet, dass die vertikale Platzierung leicht auf den oberen Rand des Monitors ausgerichtet wird.

-   **Wenn ein Fenster kontextbezogen ist, sollten Sie es immer in der Nähe des Objekts anzeigen, von dem es gestartet wurde.** Platzieren Sie die Methode so, dass das Quell Objekt nicht durch das Fenster abgedeckt wird.

    -   Wenn Sie mit der Maus angezeigt werden, legen Sie nach Möglichkeit den Offset nach unten und nach rechts ab.

    ![Abbildung des Kontext Fensters, das rechts vom Objekt platziert wird ](images/win-window-mgt-image4.png)

    Kontext Fenster in der Nähe des Objekts anzeigen, von dem es gestartet wurde.

    ![Abbildung des Benachrichtigungs Bereichs Fensters ](images/win-window-mgt-image5.png)

    Fenster, die über das Symbol für den Benachrichtigungsbereich gestartet werden, werden im Infobereich angezeigt

-   Wenn dies mithilfe eines Stifts angezeigt wird, platzieren Sie es nach Möglichkeit so, als ob es von der Hand des Benutzers abgedeckt wird. Zeigen Sie für Benutzer mit rechten Hand auf der linken Seite an. Andernfalls rechts anzeigen.

    ![Abbildung des Kontext Fensters, das sich links vom Objekt befindet ](images/win-window-mgt-image6.png)

    Wenn Sie einen Stift verwenden, zeigen Sie auch Kontext Fenster an, sodass Sie nicht von der Hand des Benutzers abgedeckt werden.

-   **Entwickler:** Mithilfe der [getMessageExtraInfo](../tablet/system-events-and-mouse-messages.md) -API können Sie zwischen Mausereignissen und Stift Ereignissen unterscheiden. Mithilfe der [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -API mit SPI getmenudropalignment können Sie die Benutzer [häntigkeit](/previous-versions/ms819495(v=msdn.10)) ermitteln \_ .
-   **Fügen Sie in der unteren rechten Ecke des aktiven Monitors Fortschritt Dialoge ein.**

    ![Abbildung der Statusanzeige in der unteren rechten Ecke ](images/win-window-mgt-image7.png)

    Positionieren Sie die Status Dialogfelder in der unteren rechten Ecke.

-   **Wenn ein Fenster nicht mit dem aktuellen Kontext oder der Benutzeraktion verknüpft ist, platzieren Sie es von der aktuellen Zeigerposition Weg.** Dadurch wird eine versehentliche Interaktion verhindert.
-   **Wenn ein Fenster eine Anwendung oder ein Dokument der obersten Ebene ist, kaskadieren Sie seinen Ursprung immer von der oberen linken Ecke des Monitors.** Wenn vom aktiven Programm erstellt, verwenden Sie den aktiven Monitor. Andernfalls verwenden Sie den Standard Monitor.

    ![Abbildung von drei Windows-kaskadierenden von oben links ](images/win-window-mgt-image8.png)

    Kaskadierte Anwendungs-oder Dokument Fenster der obersten Ebene werden von der oberen linken Ecke des Monitors aus kaskadiert.

-   **Wenn ein Fenster ein Hilfsprogramm der obersten Ebene ist, zeigen Sie es im Monitor immer als "zentriert" an.** Wenn vom aktiven Programm erstellt, verwenden Sie den aktiven Monitor. Andernfalls verwenden Sie den Standard Monitor.

    ![Abbildung des im Monitor zentrierten hilfsprogrammfensters ](images/win-window-mgt-image9.png)

    Mittelpunkt Fenster der obersten Ebene zentrieren.

-   **Wenn es sich bei einem Fenster um ein eigenes Fenster handelt, zeigen Sie es anfänglich oben im Besitzer Fenster an.** In der nachfolgenden Anzeige sollten Sie die Anzeige an der letzten Position (relativ zum Besitzer Fenster) anzeigen, wenn dies wahrscheinlich bequemer ist.

    ![Abbildung des eigenen Fensters, zentriert über Besitzer Fenster ](images/win-window-mgt-image10.png)

    Anfänglich zentrieren Sie die eigenen Fenster auf das Besitzer Fenster.

-   **Bei nicht modalem Dialogfeldern wird die Anzeige zuerst über dem Besitzer Fenster angezeigt, damit Sie leicht zu finden sind.** Wenn der Benutzer jedoch das Besitzer Fenster aktiviert, kann dies das nicht modante Dialogfeld verbergen.

    ![Abbildung des nicht modalem Dialog Felds über Besitzer Fenster ](images/win-window-mgt-image11.png)

    Anzeigen von nicht modaldialogfeldern, die anfänglich oberhalb des Besitzer Fensters angezeigt werden, damit Sie leicht gefunden werden.

-   **Passen Sie ggf. den ursprünglichen Speicherort so an, dass das gesamte Fenster innerhalb des Ziel Monitors sichtbar ist.** Wenn ein Fenster, das in der Größe geändert werden kann, größer als der Ziel Monitor ist, verringern Sie es.

### <a name="window-order-z-order"></a>Fenster Reihenfolge (Z-Reihenfolge)

-   **Platzieren Sie eigene Fenster immer über ihrem Besitzer Fenster.** Platzieren Sie keine eigenen Fenster unter den Besitzer Fenstern, da Sie von den Benutzern wahrscheinlich nicht angezeigt werden.
-   **Achten Sie auf die Z-Reihenfolge Auswahl der Benutzer. Wenn Benutzer ein Fenster auswählen, müssen Sie nur die Fenster, die mit dieser Instanz des Programms verknüpft sind (das Fenster plus einen beliebigen Besitzer oder eigene Fenster), auf die Z-Reihenfolge setzen.** Ändern Sie nicht die Reihenfolge anderer Fenster, z. b. unabhängige Instanzen desselben Programms.

### <a name="window-activation"></a>Fenster Aktivierung

-   **Fenster Zustands Auswahl für Benutzer berücksichtigen. Wenn ein vorhandenes Fenster Eingreifen erfordert, blinken Sie dreimal die Task leisten Schaltfläche, um die Aufmerksamkeit zu zeichnen, und lassen Sie Sie hervorgehoben, aber nichts anderes.** Stellen Sie das Fenster nicht wieder her oder aktivieren Sie es. Verwenden Sie keine Soundeffekte. Gestatten Sie stattdessen Benutzern, das Fenster zu aktivieren, wenn Sie bereit sind.
    -   **Ausnahme:** Wenn das Fenster nicht auf der Taskleiste angezeigt wird, verschieben Sie es am oberen Rand aller anderen Fenster, und blinken Sie stattdessen die Titelleiste.
-   Beim **Wiederherstellen eines primären Fensters sollten auch alle sekundären Fenster wieder hergestellt** werden, auch wenn die sekundären Fenster über eine eigene Task leisten Schaltfläche verfügen. Platzieren Sie bei der Wiederherstellung sekundäre Fenster oberhalb des primären Fensters.

### <a name="input-focus"></a>Eingabefokus

-   **Fenster, die von Benutzer initiierten Aktionen angezeigt werden, sollten den Eingabefokus übernehmen, aber nur, wenn das Fenster sofort** (innerhalb von 5 Sekunden) gerendert wird. Nachdem das Fenster gerendert wurde, kann der Eingabefokus einmal übernommen werden.
    -   Wenn ein Fenster langsam (mehr als 5 Sekunden) gerendert wird, führen Benutzer wahrscheinlich eine andere Aufgabe aus, während Sie warten. Wenn Sie sich an diesem Punkt konzentrieren, wäre es ein Ärgernis, insbesondere wenn Sie mehr als einmal ausgeführt werden.
-   **Fenster, die nicht sofort angezeigt oder durch eine vom System initiierte Aktion angezeigt werden, sollten den Eingabefokus nicht übernehmen.** Stattdessen wird die Anzeige ganz oben ohne Fokus angezeigt, und Benutzer können Sie aktivieren, wenn Sie bereit sind.
    -   **Ausnahme:** Anmelde Informationsverwaltung.

### <a name="persistence"></a>Persistenz

-   **Wenn ein Fenster erneut angezeigt wird, sollten Sie es in demselben Zustand wie zuletzt aufgerufen anzeigen.** Speichern Sie beim schließen den verwendeten Monitor, die Fenstergröße, den Speicherort und den Status (maximiert und Wiederherstellung). Stellen Sie bei der erneuten Anzeige die Größe, den Speicherort und den Zustand des gespeicherten Fensters mithilfe des entsprechenden Monitors wieder her. Sie sollten diese Attribute auch auf Benutzerbasis über Programm Instanzen hinweg beibehalten. **Ausnahmen:**
    -   Speichern Sie diese Attribute nicht, oder machen Sie diese Attribute für Windows persistent, wenn die Verwendung so ist, dass es sehr wahrscheinlich ist, dass Benutzer ganz wahrscheinlich vollständig anfangen möchten.
    -   Für Programme, die wahrscheinlich auf Computern mit Tablet-und Fingerabdruck Computern von Windows verwendet werden, speichern Sie zwei Windows-Zustände für den quer-und Hochformat. Weitere Informationen finden Sie unter [Entwerfen für verschiedene Anzeige Größen](/previous-versions/windows/desktop/ms695587(v=vs.85)).
-   **Wenn die aktuelle Monitor Konfiguration das Anzeigen eines Fensters mit dem letzten Zustand verhindert:**
    -   Versuchen Sie, das Fenster mit dem letzten Monitor anzuzeigen.
    -   Wenn das Fenster größer als der Monitor ist, ändern Sie die Größe des Fensters nach Bedarf.
    -   Verschieben Sie den Speicherort in die obere linke Ecke, sodass er bei Bedarf in den Monitor passt.
    -   Wenn das Problem durch die oben genannten Schritte nicht behoben werden kann, setzen Sie die Standardeinstellungen für die Fensterplatzierung zurück. Stellen Sie ggf. die vorherige Größe wieder her.

 

 