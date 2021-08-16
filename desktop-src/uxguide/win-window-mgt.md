---
title: Fensterverwaltung
description: In diesem Artikel werden die Standardplatzierung von Fenstern bei der ersten Anzeige auf dem Bildschirm, ihre Stapelreihenfolge relativ zu anderen Fenstern (Z-Reihenfolge), ihre Anfangsgröße und die Auswirkungen der Anzeige auf den Eingabefokus behandelt.
ms.assetid: d81bd71c-6d8f-45a9-82cb-bdb9b8bcbb11
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b8dc2858b0e3cc3b2a451210a61315c610afc727ac42156d5c4fc5c112135807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118212118"
---
# <a name="window-management"></a>Fensterverwaltung

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

In diesem Artikel werden die Standardplatzierung von Fenstern bei der ersten Anzeige auf dem Bildschirm, ihre Stapelreihenfolge relativ zu anderen Fenstern[(Z-Reihenfolge),](glossary.md)ihre Anfangsgröße und die Auswirkungen der Anzeige auf den Eingabefokus behandelt.

Für die folgenden Richtlinien:

-   Ein Fenster der obersten Ebene verfügt über kein Besitzerfenster und wird auf der Taskleiste angezeigt. Beispiele: Anwendungsfenster. In Windows Vista und höher werden Dialogfelder ohne Besitzerfenster und Eigenschaftenblätter auch als oberste Ebene betrachtet.
-   Ein eigenes Fenster verfügt über ein Besitzerfenster und wird nicht auf der Taskleiste angezeigt. Beispiele: modale Dialogfelder, dialogfelder ohne Modus.
-   Ein vom Benutzer initiiertes Fenster wird als direktes Ergebnis der Aktion eines Benutzers angezeigt. Andernfalls wird es programminitiiert, wenn es von einem Programm initiiert wird, oder systeminitiiert, wenn es von Microsoft Windows initiiert wird. Beispielsweise wird ein Dialogfeld Optionen vom Benutzer initiiert, aber eine Besprechungs-Erinnerung wird vom Programm initiiert.
-   Ein kontextbezogenes Fenster ist ein vom Benutzer initiiertes Fenster, das eine starke Beziehung zu dem Objekt hat, aus dem es gestartet wurde. Fenster, die von Kontextmenüs oder Symbolen für den Benachrichtigungsbereich angezeigt werden, sind beispielsweise kontextabhängig, Fenster, die von Menüleisten angezeigt werden, sind dies nicht.
-   Der aktive Monitor ist der Monitor, auf dem das aktive Programm ausgeführt wird.
-   Der Standardmonitor ist der Monitor mit dem Startmenü, der Taskleiste und dem Benachrichtigungsbereich.

## <a name="design-concepts"></a>Entwurfskonzepte

Die Fensterverwaltung ist eine der grundlegendsten Benutzeraktivitäten. Vor Windows Vista wurden Fenster häufig mit kleinen Standardgrößen versehen und in der Mitte des Bildschirms platziert. Dieser Ansatz funktioniert gut für ältere Monitore mit niedriger Auflösung, aber nicht für moderne Videohardware.

Windows ist für die Unterstützung moderner Videohardware konzipiert, die häufig mit Auflösungen ausgeführt wird, die deutlich höher als die unterstützte Bildschirmauflösung sind und möglicherweise über mehrere Monitore verfügen. Gehen Sie dabei wie hier vor:

-   Ermöglicht Es Benutzern, vollständig von ihrer erweiterten Hardware zu profitieren.
-   Erfordert weniger Aufwand von Benutzern, um ihre Maus über größere Entfernungen zu bewegen.
-   Macht die Fensterplatzierung besser vorhersagbar und somit leichter zu finden.

### <a name="the-minimum-supported-screen-resolution"></a>Die mindestens unterstützte Bildschirmauflösung

Die minimale [effektive Bildschirmauflösung,](glossary.md) die von Windows unterstützt wird, beträgt 800 x 600 Pixel. Dies bedeutet, dass Fenster fester Größe vollständig mit der minimalen Auflösung angezeigt werden sollten (während Platz für die Taskleiste reserviert wird), aber fenster mit größenveränderlicher Größe für eine effektive Auflösung von 1024 x 768 Pixeln optimiert werden können, solange sie mit der minimalen Auflösung funktionieren.

Während derzeit die gängigsten physischen Bildschirmauflösungen für Windows PCs 1024 x 768 Pixel oder höher sind, ermöglicht die Ausrichtung auf 800 x 600 Pixel Windows:

-   Arbeiten Sie gut mit der gesamten modernen Hardware, einschließlich kleiner Notebook-PCs.
-   Unterstützung von Einstellungen für hohe DPI-Einstellungen (Punkte pro Zoll).
-   Unterstützung größerer Schriftarten für die Barrierefreiheit.
-   Unterstützung von Hardware, die auf globaler Basis verwendet wird.

Für die Auswahl der minimalen Lösung, die unterstützt werden soll, muss das richtige Gleichgewicht gefunden werden. Die Festlegung einer höheren Auflösung würde zu einer suboptimalen Erfahrung für einen erheblichen Prozentsatz moderner Hardware führen, während die Festlegung einer niedrigeren Auflösung designer daran hindern würde, den verfügbaren Bildschirmbereich vollständig zu nutzen.

Wenn Sie der Meinung sind, dass Ihre Zielbenutzer deutlich höhere Auflösungen als die Windows Minimum verwenden, können Sie Ihr Programm so entwerfen, dass es den zusätzlichen Bildschirmbereich in vollem Umfang nutzt, indem Sie fensterfähige Fenster verwenden, die gut skaliert werden können.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Unterstützen Sie die minimale Windows effektive Auflösung von 800 x 600 Pixeln.** Für kritische Benutzeroberflächen , die im abgesicherten Modus funktionieren müssen, wird eine effektive Auflösung von 640 x 480 Pixel unterstützt. Achten Sie darauf, den von der Taskleiste belegten Speicherplatz zu berücksichtigen, indem Sie 48 vertikale [relative Pixel](glossary.md) für Fenster reservieren, die mit der Taskleiste angezeigt werden.
-   **Optimieren Sie größenveränderbare Fensterlayouts für eine effektive Auflösung von 1024 x 768 Pixeln.** Ändern Sie die Größe dieser Fenster für niedrigere Bildschirmauflösungen automatisch auf eine Weise, die weiterhin funktionsfähig ist.
-   **Stellen Sie sicher, dass Sie Ihre Fenster in 96 DPI (100 Prozent) bei 800 x 600 Pixel, 120 DPI (125 Prozent) bei 1024 x 768 Pixel und 144 DPI (150 Prozent) bei 1200 x 900 Pixel testen.** Überprüfen Sie, ob Layoutprobleme auftreten, z. B. Das Ausschneiden von Steuerelementen, Text und Fenstern und das Strecken von Symbolen und Bitmaps.
-   **Für Programme mit Toucheingabe- und mobilen Verwendungsszenarien optimieren Sie für 120 dpi.** Bildschirme mit hohem DPI-Wert sind derzeit auf Touch- und mobilen PCs weit verbreitet.
-   **Größenänderungsfähige Fenster müssen das Größenänderungsglyph in** der unteren rechten Ecke nicht mehr anzeigen, da:
    -   Die Größe aller Seiten und Ränder eines Fensters kann nicht nur in der unteren rechten Ecke geändert werden.
    -   Das Glyphen erfordert eine Statusleiste, aber viele fensterveränderbare Fenster stellen keine Statusleisten bereit.
    -   Die Größenänderungs- und Größenänderungszeiger des Fensters sind effektiver bei der Kommunikation, dass die Größe eines Fensters geändert werden kann als das Größenänderungsglyph.

### <a name="title-bar-controls"></a>Titelleisten-Steuerelemente

Verwenden Sie die Titelleistensteuerelemente wie folgt:

-   **Schließen.** Alle primären und sekundären Fenster mit einem Standardfensterrahmen sollten auf der Titelleiste über die Schaltfläche Schließen verfügen. Wenn Sie auf Schließen klicken, wird das Fenster abgebrochen oder geschlossen.

![Screenshot des Dialogfelds ohne Schaltfläche "Schließen" ](images/win-window-mgt-image1.png)

In diesem Beispiel enthält das Dialogfeld keine Schaltfläche Schließen in der Titelleiste.

-   **Minimieren.** Alle primären Fenster und zeitintensiven, moduslosen sekundären Fenster (z. B. Statusdialogfelder) sollten über die Schaltfläche Minimieren verfügen. Wenn Sie auf Minimieren klicken, wird das Fenster auf die Zugehörige Taskleistenschaltfläche reduziert. Daher ist für Fenster, die minimiert werden können, ein Titelleistensymbol erforderlich.
-   **Maximieren/Wiederherstellen nach unten.** Alle Fenster, deren Größe geändert werden kann, sollten über die Schaltfläche Maximieren/Wiederherstellen nach unten verfügen. Wenn Sie auf Maximieren klicken, wird das Fenster in der größten Größe angezeigt, die für die meisten Fenster vollbildig ist. Wenn Sie dagegen auf Wiederherstellen klicken, wird das Fenster in der vorherigen Größe angezeigt. Einige Fenster profitieren jedoch nicht von der Verwendung eines Vollbilds, sodass diese Fenster auf ihre größte nützliche Größe maximieren sollten.

### <a name="window-size"></a>Fenstergröße

-   **Wählen Sie eine für den Inhalt geeignete Standardfenstergröße aus.** Sie sollten keine größeren Anfangsfenster verwenden, wenn Sie den Platz effektiv nutzen können.
-   **Verwenden Sie nach Möglichkeit fensterveränderbare Fenster, um Scrollleisten und abgeschnittene Daten zu vermeiden.** Windows mit dynamischen Inhalten und Listen profitieren am meisten von fensterveränderbaren Fenstern.
-   **Ziehen Sie für Textdokumente eine maximale Zeilenlänge von 65 Zeichen** in Betracht, um das Lesen des Texts zu vereinfachen. (Zeichen enthalten Buchstaben, Interpunktionszeichen und Leerzeichen.)
-   Fenster mit fester Größe:
    -   **Muss vollständig sichtbar sein und die Größe so anpassen, dass er in den Arbeitsbereich passt.**
-   Fenster mit größenveränderbarer Größe:
    -   **Kann für höhere Auflösungen optimiert sein, aber bei Bedarf zur Anzeigezeit auf die tatsächliche Bildschirmauflösung verkleinert werden.**
    -   **Bei zunehmend größeren Fenstergrößen muss progressiv mehr Informationen anzeigen.** Stellen Sie sicher, dass mindestens ein Fensterteil oder -steuerelement über inhalte verfügt, deren Größe geändert werden kann.
    -   **Sollte standardmäßig wiederhergestellte Größen vermeiden, die maximiert oder nahezu maximiert sind.** Wählen Sie stattdessen eine Standardgröße aus, die in der Regel am nützlichsten ist, ohne vollbildig zu sein. Gehen Sie davon aus, dass Benutzer das Fenster maximieren, anstatt die Größe so zu ändern, dass es im Vollbildmodus angezeigt wird.
    -   **Sollte eine minimale Fenstergröße festlegen, wenn eine Größe vorhanden ist, unter der der Inhalt nicht mehr verwendet werden kann.** Legen Sie bei Steuerelementen, deren Größe geändert werden kann, die minimalen Größen für größenveränderbare Elemente auf ihre kleinsten Funktionalen Größen fest, z. B. minimale Funktionale Spaltenbreiten in Listenansichten.
    -   **Sollte die Präsentation ändern, wenn dadurch der Inhalt in kleineren Größen verwendet werden kann.**

![Screenshot von Media Player-Schaltflächen ](images/win-window-mgt-image2.png)

In diesem Beispiel ändert Windows Media Player sein Format, wenn das Fenster für das Standardformat zu klein wird.

### <a name="window-location"></a>Fensterposition

-   **Für die folgenden Richtlinien bedeutet "Zentrieren", dass die vertikale Platzierung leicht nach oben im Monitor zentriert wird, anstatt genau in der Mitte zu platzieren.** Legen Sie 45 Prozent des Platzes zwischen dem oberen Rand des Monitors/Besitzers und dem Fenster oben und 55 Prozent zwischen dem unteren Rand des Monitors/Besitzers und dem Fenster unten ab. Dies geschieht, da das Auge auf natürliche Weise nach oben auf dem Bildschirm bewegt wird.

    ![Abbildung des Fensters, das leicht über der Mitte platziert ist ](images/win-window-mgt-image3.png)

    "Zentrieren" bedeutet, dass die vertikale Platzierung leicht nach oben im Monitor zentriert wird.

-   **Wenn ein Fenster kontextabhängig ist, zeigen Sie es immer in der Nähe des Objekts an, von dem aus es gestartet wurde.** Platzieren Sie es aus dem Weg, sodass das Quellobjekt nicht durch das Fenster abgedeckt wird.

    -   Wenn sie mit der Maus angezeigt wird, platzieren Sie sie nach Möglichkeit nach unten und rechts.

    ![Abbildung des kontextbezogenen Fensters, das rechts vom Objekt platziert wird ](images/win-window-mgt-image4.png)

    Kontextfenster in der Nähe des Objekts anzeigen, aus dem es gestartet wurde.

    ![Abbildung des Benachrichtigungsbereichsfensters ](images/win-window-mgt-image5.png)

    Windows, die über Benachrichtigungsbereichssymbole gestartet werden, werden in der Nähe des Benachrichtigungsbereichs angezeigt.

-   Wenn sie mithilfe eines Stifts angezeigt wird, platzieren Sie ihn nach Möglichkeit so, dass er nicht von der Hand des Benutzers abgedeckt wird. Für rechtshändige Benutzer wird auf der linken Seite angezeigt. andernfalls rechts angezeigt.

    ![Abbildung des kontextbezogenen Fensters links vom Objekt ](images/win-window-mgt-image6.png)

    Wenn Sie einen Stift verwenden, zeigen Sie auch kontextbezogene Fenster an, damit sie nicht von der Hand des Benutzers abgedeckt werden.

-   **Entwickler:** Sie können mithilfe der [GetMessageExtraInfo-API](../tablet/system-events-and-mouse-messages.md) zwischen Mausereignissen und Stiftereignissen unterscheiden. Sie können die Übergabe des Benutzers [mithilfe](/previous-versions/ms819495(v=msdn.10)) der [SystemParametersInfo-API](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) mit SPI \_ GETMENUDROPALIGNMENT bestimmen.
-   **Platzieren Sie Statusdialogfelder in der unteren rechten Ecke des aktiven Monitors.**

    ![Abbildung der Statusleiste in der unteren rechten Ecke ](images/win-window-mgt-image7.png)

    Platzieren Sie Statusdialogfelder in der unteren rechten Ecke.

-   **Wenn ein Fenster nicht mit dem aktuellen Kontext oder der aktuellen Benutzeraktion verknüpft ist, platzieren Sie es von der aktuellen Zeigerposition.** Dadurch wird eine versehentliche Interaktion verhindert.
-   **Wenn es sich bei einem Fenster um eine Anwendung oder ein Dokument der obersten Ebene handelt, kaskadieren Sie seinen Ursprung immer über die obere linke Ecke des Monitors.** Verwenden Sie den aktiven Monitor, wenn er vom aktiven Programm erstellt wurde. Verwenden Sie andernfalls den Standardmonitor.

    ![Abbildung von drei Fenstern, die von oben links kaskadiert werden ](images/win-window-mgt-image8.png)

    Kaskadieren von Anwendungs- oder Dokumentfenstern der obersten Ebene in der oberen linken Ecke des Monitors.

-   **Wenn es sich bei einem Fenster um ein Hilfsprogramm der obersten Ebene handelt, zeigen Sie es immer "zentriert" im Monitor an.** Verwenden Sie den aktiven Monitor, wenn er vom aktiven Programm erstellt wurde. Verwenden Sie andernfalls den Standardmonitor.

    ![Abbildung des im Monitor zentrierten Hilfsprogrammfensters ](images/win-window-mgt-image9.png)

    Hilfsprogrammfenster der obersten Ebene in der Mitte.

-   **Wenn es sich bei einem Fenster um ein Fenster im Besitz handelt, wird es zunächst "zentriert" über dem Besitzerfenster angezeigt.** Erwägen Sie für die nachfolgende Anzeige die Anzeige an der letzten Position (relativ zum Besitzerfenster), wenn dies wahrscheinlich bequemer ist.

    ![Abbildung des fensters im Besitz, das über dem Besitzerfenster zentriert ist ](images/win-window-mgt-image10.png)

    Zunächst zentriert die fenstereigenen Fenster über dem Besitzerfenster.

-   **Bei nicht moduslosen Dialogen wird immer zuerst über dem Besitzerfenster angezeigt, damit sie leicht zu finden sind.** Wenn der Benutzer jedoch das Besitzerfenster aktiviert, kann dies den moduslosen Dialog verdecken.

    ![Abbildung des moduslosen Dialogfelds über dem Besitzerfenster ](images/win-window-mgt-image11.png)

    Zeigen Sie zunächst moduslose Dialogfelder über dem Besitzerfenster an, damit sie leicht zu finden sind.

-   **Passen Sie bei Bedarf den anfänglichen Speicherort an, damit das gesamte Fenster im Zielmonitor angezeigt wird.** Wenn ein Fenster, das die Größe ändern kann, größer als der Zielmonitor ist, reduzieren Sie es an seine Größe.

### <a name="window-order-z-order"></a>Fenster reihenfolge (Z-Reihenfolge)

-   **Platzieren Sie im Besitz befindliche Fenster immer über dem Besitzerfenster.** Platzieren Sie niemals eigene Fenster unter ihren Besitzerfenstern, da die meisten Benutzer sie wahrscheinlich nicht sehen werden.
-   **Achten Sie auf die Z-Reihenfolgenauswahl der Benutzer. Wenn Benutzer ein Fenster auswählen, bringen Sie nur die Fenster, die dieser Instanz des Programms zugeordnet sind (das Fenster plus alle Besitzer- oder besitzereigenen Fenster), an den Anfang der Z-Reihenfolge.** Ändern Sie die Reihenfolge anderer Fenster, z. B. unabhängiger Instanzen desselben Programms, nicht.

### <a name="window-activation"></a>Aktivieren von Fenstern

-   **Achten Sie auf die Fensterzustandsauswahl von Benutzern. Wenn ein vorhandenes Fenster Aufmerksamkeit erfordert, blinken Sie dreimal auf die Taskleistenschaltfläche, um die Aufmerksamkeit zu erhalten, und lassen Sie es hervorgehoben, aber machen Sie keine anderen Maßnahmen.** Das Fenster wird nicht wiederhergestellt oder aktiviert. Verwenden Sie keine Soundeffekte. Lassen Sie benutzer stattdessen das Fenster aktivieren, wenn sie bereit sind.
    -   **Ausnahme:** Wenn das Fenster nicht auf der Taskleiste angezeigt wird, bringen Sie es an den Anfang aller anderen Fenster, und blinken Sie stattdessen auf die Titelleiste.
-   **Beim Wiederherstellen eines primären Fensters sollten auch** alle sekundären Fenster wiederhergestellt werden, auch wenn diese sekundären Fenster über eine eigene Taskleistenschaltfläche verfügen. Platzieren Sie bei der Wiederherstellung sekundäre Fenster über dem primären Fenster.

### <a name="input-focus"></a>Eingabefokus

-   **Windows, die** von vom Benutzer initiierten Aktionen angezeigt werden, sollten den Eingabefokus erhalten, jedoch nur, wenn das Fenster sofort gerendert wird (innerhalb von 5 Sekunden). Sobald das Fenster gerendert wurde, kann es den Eingabefokus einmal übernehmen.
    -   Wenn ein Fenster langsam gerendert wird (mehr als 5 Sekunden), werden Benutzer wahrscheinlich eine andere Aufgabe ausführen, während sie warten. An diesem Punkt den Fokus zu nehmen, wäre ein Genervität, insbesondere, wenn dies mehr als einmal erfolgt.
-   **Windows, die nicht sofort von einer vom System initiierten Aktion angezeigt oder angezeigt werden, sollten keinen Eingabefokus haben.** Zeigen Sie stattdessen oben ohne Fokus an, und lassen Sie Benutzer sie aktivieren, wenn sie bereit sind.
    -   **Ausnahme:** Anmeldeinformationsverwaltung.

### <a name="persistence"></a>Persistenz

-   **Wenn ein Fenster erneut angezeigt wird, sollten Sie es im gleichen Zustand wie beim letzten Zugriff anzeigen.** Speichern Sie beim Schließen den verwendeten Monitor, die Fenstergröße, den Speicherort und den Zustand (maximiert im Vergleich zur Wiederherstellung). Stellen Sie beim erneuten Anzeigen die Größe, den Speicherort und den Zustand des gespeicherten Fensters mithilfe des entsprechenden Monitors wieder wieder auf. Erwägen Sie außerdem, diese Attribute pro Benutzer über Programminstanzen hinweg persistent zu halten. **Ausnahmen:**
    -   Speichern Oder lassen Sie diese Attribute nicht für Fenster erhalten, wenn ihre Verwendung so ist, dass Benutzer viel wahrscheinlicher von vorn beginnen möchten.
    -   Bei Programmen, die wahrscheinlich auf Computern Windows Tablet- und Touchtechnologie werden, speichern Sie zwei Fensterzustände für querformatige und Hochformatmodi. Weitere Informationen finden Sie unter [Entwerfen für unterschiedliche Anzeigegrößen.](/previous-versions/windows/desktop/ms695587(v=vs.85))
-   **Wenn die aktuelle Monitorkonfiguration verhindert, dass ein Fenster mit seinem letzten Zustand angezeigt wird:**
    -   Versuchen Sie, das Fenster mit dem letzten Monitor anzuzeigen.
    -   Wenn das Fenster größer als der Monitor ist, ändern Sie die Größe des Fensters nach Bedarf.
    -   Verschieben Sie die Position nach Bedarf in die obere linke Ecke, damit sie in den Monitor passt.
    -   Wenn das Problem mit den oben genannten Schritten nicht behoben werden kann, löse die Standardrichtlinien für die Fensterplatzierung zurück. Erwägen Sie nach Möglichkeit die Wiederherstellung der vorherigen Größe.

 

 