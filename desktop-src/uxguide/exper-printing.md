---
title: Drucken (Entwurfs Grundlagen)
description: Der Druckvorgang ist die Benutzer Darstellung auf dem Papier. Es ist leicht zu übersehen, aber es ist ein wichtiger Bestandteil der allgemeinen Benutzer Leistung.
ms.assetid: 26f5a8dc-27b2-4c2d-a05a-f942784c3cf9
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a98bf29da1169ad43a3b1d16ab52298d62612037
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104558225"
---
# <a name="printing-design-basics"></a>Drucken (Entwurfs Grundlagen)

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Der Druckvorgang ist die Benutzer Darstellung auf dem Papier. Es ist leicht zu übersehen, aber es ist ein wichtiger Bestandteil der allgemeinen Benutzer Leistung.

In diesem Artikel bezieht sich der *Druck* auf die Benutzer Darstellung auf dem Papier, in der die Ausgabe an Papier anstatt an die Bildschirm Anzeige weitergeleitet wird. *Druckerfreundliches Format* bezieht sich auf Änderungen, die das Programm für die Anzeige der Bildschirm Anzeige vornehmen kann, die es besser für die Papierausgabe geeignet machen.

Trotz der Vorhersage, dass die Berechnung der "Taschen losen Büro" zur Folge hat Wir verteilen harte Kopien von Microsoft PowerPoint Presentation-Karten, wir drucken Artikel, die wir Online ermitteln, möchten aber später genauer erforscht werden, wir Drucken wichtige e-Mails oder fortsetzen, die wir in elektronischer Form erhalten haben, usw. Es ist zwar einfach, den Druck beim Entwerfen einer Benutzeroberfläche zu übersehen, aber denken Sie daran, dass das Drucken ein wichtiger Bestandteil der gesamten Benutzeroberfläche ist.

**Hinweis:** Richtlinien für [Allgemeine Dialog](win-common-dlg.md) Felder werden in einem separaten Artikel dargestellt.

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Um zu entscheiden, ob das Programm den Druck unterstützen muss, sollten Sie die folgenden Fragen beachten:

-   **Welche Art von Programm entwerfen Sie?** Der Programmtyp ist ein guter Indikator für die geeignete Ebene der Druckunterstützung. Dokument-und Bild Erstellung, anzeigen und Durchsuchen von Programmen benötigen eine hervorragende Druckunterstützung, während andere Programmtypen nur eine Druckunterstützung in geringerem Umfang benötigen. (Eine Liste der Programmtypen finden Sie im Abschnitt " [Druckmuster](#printing-patterns) " in diesem Artikel.)
-   **Wird das Programm in Szenarien verwendet, die von der direkt Papierausgabe profitieren?** Wenn dies der Fall ist, ist es bequemer, dem Programm Druckunterstützung hinzuzufügen, als die Benutzer dazu aufzufordern, die Daten in ein anderes zu Druck Ende Programm zu kopieren.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="design-your-program-to-eliminate-unnecessary-printing"></a>Entwerfen Sie Ihr Programm so, dass unnötige Druck Vermeidung vermieden werden

Es gibt zahlreiche Gründe, warum Benutzer einige gut drucken müssen. Benutzer sollten drucken, weil Sie dies tun möchten, nicht, weil Sie dies tun müssen. Das Drucken von Benutzern kann ein Vorzeichen für fehlende Features sein. In der Vergangenheit mussten Benutzer z. b. Dokumente drucken, um Kommentare zu erstellen und Revisionen vorzuschlagen, aber jetzt können Benutzer diese Aufgaben direkt in Microsoft Word-Dokumenten ausführen. **Überprüfen Sie die Szenarios des Programms, in denen gedruckt werden soll, und stellen Sie im bestmöglichen Bereich sicher, dass die Anforderung zum Drucken optional ist und nicht das Ergebnis fehlender Features.**

Sie sollten auch daran denken, dass das Einsparen von Ressourcen wie Papier-und frei Hand Eingaben hilfreich ist, und Unternehmen langfristig Geld sparen.

### <a name="understand-the-differences-between-screen-display-and-print"></a>Grundlegendes zu den Unterschieden zwischen Bildschirm Anzeige und Druck

Obwohl es viele Ähnlichkeiten zwischen Anzeige Ausgabe und Druck gibt, gibt es auch viele Unterschiede. Ausgabe Drucken:

-   **Hat einen hohen dpi-.** Die Anzeige Ausgabe beträgt normalerweise 96 oder 120 Punkte pro Zoll (dpi), während die Druckerausgabe in der Regel bei 600 dpi oder höher liegt.
-   **Weist andere optimale Schriftarten auf.** Obwohl gut entworfene Schriftarten sowohl für die Anzeige als auch für den Druck geeignet sind, sind Serif-Schriftarten bei hohen Auflösungen für große Mengen an Text besser lesbar als Sans-Serif-Schriftarten. Daher sollten große Textmengen, die in erster Linie für den Druck vorgesehen sind, eine "Serif"-Schriftart verwenden, während für Text, der in erster Linie für die Anzeige gedacht ist, eine Sans Weitere Informationen finden Sie unter [Schriftarten](vis-fonts.md) (Segoe UI).
-   **Hat ein Seitenverhältnis.** Die Anzeige hat normalerweise ein niedriges [Seitenverhältnis](glossary.md) (4:3 oder 5:4), wohingegen Print ein hohes Seitenverhältnis (8,5:11 oder 1:1.4142 basierend auf den Standardseiten Größen) verwendet. Der Grund hierfür ist [, dass das](glossary.md) Drucken im Hochformat eher üblich ist als der [quer](glossary.md)Format.
-   **Hat Seiten.** Folglich Ausgabe Drucken:
    -   Hat Standardseiten Größen. Der Standard in den USA und Kanada ist 8,5 "X11"-Papier. der Standardwert für "überall" ist A4-Papier.
    -   Hat Seitenumbrüche.
    -   Hat Seitenränder.
    -   Verfügt über Kopf-und Fußzeilen.
    -   Verfügt über eine Einzel-oder zweiseitige Ausgabe.
    -   Kann über mehrere Kopien verfügen.
    -   Kann nicht in der richtigen Reihenfolge oder selektiv gedruckt werden.
-   **Verfügt über viele Optionen.** Benutzer können einen Drucker und eine Papiergröße, Druckeroptionen (z. b. Druckqualität, Doppelseitiger Druck, Heftung), die Anzahl der Kopien, die Seitenbereiche, die Sortierung und das Druckformat auswählen.
-   **Nimmt Zeit und Geld in Rechnung.** Es kann sehr viel Zeit in Anspruch nehmen, ein großes Dokument oder ein qualitativ hochwertiges Foto auszugeben, und die Kosten für das Papier und die Hand Eingaben werden im Laufe der Zeit erhöht. Im Gegensatz dazu ist die Anzeige Ausgabe sofort und im Grunde kostenlos.
-   **Kann schwarz und weiß sein.** Viele Drucker sind heute schwarz und weiß, während nur wenige anzeigen monochrome sind.
-   **Ist nicht interaktiv.** Benutzer können keinen Bildlauf für Seiten oder Steuerelemente durchführen, um weitere Inhalte Sie können nicht auf Links oder Schaltflächen klicken oder auf Steuerelemente zeigen. Interaktiver Inhalt hat keinen Wert, wenn er gedruckt wird.
-   **Kann aus Papier, frei Hand Eingaben oder Toner bestehen oder offline sein.** Folglich benötigt die Papierausgabe mehr Fehlerbehandlung und Problembehandlung.

Diese Unterschiede können sich auf den Druck Entwurf auswirken. Das Erstellen einer guten Druckdarstellung erfordert mehr als nur das Umleiten der Programmausgabe an den Drucker.

### <a name="wysiwyg-and-the-evolving-requirements-of-screen-display"></a>WYSIWYG und die sich entwickelnden Anforderungen der Bildschirm Anzeige

In der Vergangenheit ist das grundlegendste Prinzip der Druck Benutzerfunktion WYSIWYG ("was Sie sehen, was Sie sehen"). Dieses Prinzip deutet darauf hin, dass es eine starke Beziehung zwischen dem, was in der Anzeige angezeigt wird, und dem gedruckten gibt. Bevor WYSIWYG zu einer Standardübung geworden ist, gab es häufig keine Beziehung zwischen der Anzeige und den Druckversionen eines Dokuments. Die Benutzer mussten drucken, um zu sehen, wie das Dokument im Whitepaper tatsächlich ausgesehen hat. Die Verwendung von WYSIWYG war eine gute Verbesserung der Produktivität, da die meisten Programme zu diesem Zeitpunkt hauptsächlich für die Erstellung und den Druck von Dokumenten entwickelt wurden.

Heutzutage ist es üblich, dass Websites für die Anzeige optimiert werden, und Ihr Druckerfreundliches Format mag viel anders erscheinen. Außerdem verfügen wir über verschiedene Computergeräte (z. b. Smartphones und persönliche digitale Assistenten), für die häufig eine Ausgabe optimiert ist, die für kleine anzeigen optimiert ist. Wenngleich WYSIWYG immer noch der beste Ansatz für die Erstellung von Dokumenten ist, ist es für andere Programme oft sinnvoller, eine Optimierung für eine Vielzahl von Ziel Geräten zu erzielen. Bei solchen Programmen unterscheiden sich die Anzeige auf einer PC-Anzeige möglicherweise von der Anzeige auf anderen Geräte anzeigen, die sich möglicherweise von der auf der gedruckten Seite ausgegebene Seite unterscheiden.

### <a name="optimize-for-printing"></a>Zum Drucken optimieren

Programme, die keine strikte WYSIWYG-Druckfunktion verwenden, können wie folgt zum Drucken optimiert werden:

-   Formatieren Sie das Layout für die Größe der Ziel Seite neu.
-   Geben Sie die Seitenansicht an, vorzugsweise mit einfachen Anpassungsoptionen, mit denen Benutzer direkt im Dialogfeld "Drucken" experimentieren können (z. b. beim Ziehen von Seiten
-   Geben Sie ggf. eine druckerfreundliche Format Option an.
    -   Konsolidieren Sie separate Teil Dokumente in einem einzelnen Dokument.
    -   Entfernen Sie Hintergründe und andere Entwurfs Elemente, wie z. b. ADS, insbesondere dann, wenn Sie für einen schwarzen und einen weißen Drucker ungeeignet sind.
    -   Entfernen Sie interaktive Elemente, z. b. Navigations Steuerelemente und Befehls Schaltflächen.
    -   Stellen Sie sicher, dass alle Daten ohne Scrollleisten oder Mauszeiger sichtbar sind.

        **Anzeige Version:**

        ![Screenshot des Berichts optimiert für Bildschirm ](images/exper-printing-image1.png)

        **Druckerfreundliche Version:**

        ![Screenshot des gleichen Berichts, optimiert für Drucken ](images/exper-printing-image2.png)

        In der druckerfreundlichen Version werden alle Daten auf der gedruckten Seite angezeigt, und die interaktiven Elemente werden entfernt.

    -   Ersetzen Sie Verknüpfungen durch ihre Text Entsprechung.

        **Annehmbar:**

        Weitere Informationen finden Sie im UX-Handbuch.

        **Für Druck optimiert:**

        Weitere Informationen finden Sie im UX-Handbuch ( https://msdn.microsoft.com/windowsvista/uxguide) .

-   Konvertiert hellen Text auf einem dunklen Hintergrund in einen dunklen Text auf einem weißen Hintergrund.

### <a name="include-the-right-print-options"></a>Die richtigen Druckoptionen einschließen

Im Dialogfeld "Druckoptionen" werden Optionen für Folgendes bereitstellt:

-   Wählen Sie den Drucker und das Papierformat aus.
-   Legen Sie Druckereigenschaften fest.
-   Wählen Sie den Seitenbereich, die Anzahl der Kopien und die Sortierung aus.
-   Verwenden Sie beide Seiten des Papiers.

Das Programm erfordert möglicherweise zusätzliche Optionen, wie z. b. Dokument Inhalts Optionen (zu druckender Inhalt), Formatoptionen (Drucken, einschließlich Druckqualität, Bildgrößen, Anpassung an Frame) und Farboptionen. Wenn Sie zusätzliche Optionen angeben müssen, erweitern Sie das Dialogfeld "Druckoptionen" (allgemein). Erstellen Sie kein benutzerdefiniertes Druck Dialogfeld.

Beim Entwerfen der Druckoptionen sollten Sie die beim Drucken mehrerer Dokumente berücksichtigende Zeit beachten. Die Wahrscheinlichkeit ist, dass der nächste Druckauftrag dem letzten Druckauftrag sehr ähnlich ist. Durch die Optimierung der Standardeinstellungen für Neudrucke und ähnliche Druckaufträge wird der Benutzer nicht jedes Mal vollständig neu gestartet.

### <a name="design-print-preview-for-performance-and-usability"></a>Entwerfen der Druckvorschau für Leistung und Benutzerfreundlichkeit

**Ein falscher Druckauftrag verschwendet Zeit und Geld. Bei Dokumenten Erstellungs Programmen sollten Benutzer in der Lage sein, die Ergebnisse auszuwerten, bevor Sie den eigentlichen Druckvorgang ausführen.** In einer Seitenansicht sollten Benutzer folgende Aktionen ausführen können:

-   Evaluieren Sie Ränder, Seitenumbrüche, Seitenausrichtung, Kopfzeilen und Fußzeilen.
-   Durchsuchen Sie alle Seiten.
-   Direkt aus der Druckvorschau drucken.

Einige komplexe Dokumente (z. b. computergestützte Design- \[ CAD- \] Zeichnungen) können viel Zeit in Anspruch nehmen. Die Leistung der Vorschau ist wichtig: eine Seitenansicht kann recht mühsam werden, wenn es eine Weile dauert, jede Seite zu Rendering. **Folglich ist es besser, eine Druckvorschau zu haben, die schnell gerendert wird und genau genug ist, damit Benutzer die Druckergebnisse auswerten können, als eine vollständig genaue Vorschau zu erhalten, die langsam gerendert wird.**

Wenn Sie die Seitenansicht entwerfen, sollten Sie die gesamte Aufgabe der Druckvorbereitung in Erwägung gezogen. Was werden Benutzer suchen? Welche Änderungen werden geändert? Programme zur Dokument Erstellung sollten eine interaktive Seitenansicht bereitstellen, sodass Benutzer häufig geänderte Einstellungen wie Ränder und Zeilenumbrüche innerhalb der Vorschau anpassen können.

Allerdings sollte das Programm in der Standardeinstellung das richtige tun. Warnen Sie bei Bedarf vor Drucksituationen, die unwahrscheinlich sind, was der Benutzer beabsichtigt hat. Verlassen Sie sich nicht darauf, dass Benutzer mit der Seitenansicht Probleme finden. Angenommen, eine Kalkulations Tabelle weist zu viele Spalten auf, die auf einer einzelnen Seite im Hochformat gedruckt werden können. Während das Programm ein Bestätigungs Dialogfeld anzeigen kann, empfiehlt es sich, automatisch im Querformat zu drucken.

**Wenn Sie nur fünf Dinge tun...**

1.  Entwerfen Sie eine geeignete Druckdarstellung für Ihren Programmtyp.
2.  Überprüfen Sie die Szenarios des Programms, in denen das Drucken und das bestmögliche Ausmaß beschrieben werden muss.
3.  Stellen Sie nützliche Druck Erweiterungen bereit, indem Sie das Dialogfeld "Drucken" im Dialogfeld Erstellen Sie zu diesem Zweck kein benutzerdefiniertes Druck Dialogfeld.
4.  Optimieren Sie die Druckoptionen für Neudrucke und ähnliche Druckaufträge.
5.  Stellen Sie nach Bedarf ein Vorschau Feature bereit.

## <a name="printing-patterns"></a>Druckmuster

Der Programmtyp ist der primäre Indikator der entsprechenden Druckdarstellung:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Erweiterte Dokument Erstellung</strong><br/> Wird verwendet, um High-End-Dokumente zu erstellen, anzuzeigen und zu drucken. Die Möglichkeit zum Erstellen hochwertiger Ausdrucke ist einer der Hauptgründe, warum das Programm vorhanden ist. Als Ziel für erfahrene Benutzer. <br/></td>
<td><strong>Benutzer Ziele:</strong> Perfekte Ergebnisse detaillierte Steuerung der Druckausgabe.<br/> <strong>Beispiel:</strong> Microsoft Word<br/> <strong>Empfohlene Druckdarstellung:</strong><br/>
<ul>
<li>Ausgabe optimiert für Print (WYSIWYG).</li>
<li>Erweiterte Funktionen für die Dokument Formatierung mit Optionen zum Drucken von großen Objekten.</li>
<li>Erweiterte Druckoptionen, einschließlich Kopf-und Fußzeilen. Dokument bezogene Druckoptionen werden im Dokument selbst gespeichert.</li>
<li>Schnelle, genaue und leistungsstarke Druckvorschau.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Zwischen Dokument Erstellung</strong><br/> Wird verwendet, um komplexere Dokumente zu erstellen und anzuzeigen. Die Möglichkeit zum Erstellen von ausdrucken mit guter Qualität ist wichtig, aber nicht unbedingt einer der Hauptgründe, warum das Programm vorhanden ist. Als Ziel für zwischen Benutzer. <br/></td>
<td><strong>Benutzer Ziele:</strong> Gute Ergebnisse mit minimalem Aufwand. Eine Steuerung der Druckausgabe.<br/> <strong>Beispiele:</strong> Die meisten Microsoft Office Programme, z. b. Outlook und Excel.<br/> <strong>Empfohlene Druckdarstellung:</strong><br/>
<ul>
<li>Ausgabe optimiert für Print (WYSIWYG).</li>
<li>Einige Dokument Formatierungsfunktionen, mit der Möglichkeit, große Objekte ohne Abschneiden zu drucken.</li>
<li>Einige benutzerdefinierte Druckoptionen, einschließlich Kopf-und Fußzeilen.</li>
<li>Genaue, leicht zu verwendende Druckvorschau.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Einfache Dokument Erstellung</strong><br/> Wird verwendet, um einfache Dokumente zu erstellen und anzuzeigen. Als Ziel für alle Benutzer. <br/></td>
<td><strong>Benutzer Ziele:</strong> Grundlegende Druckunterstützung mit Standarddruck Optionen. Benutzer erwarten gute Ergebnisse, ohne Anpassungen vorzunehmen.<br/> <strong>Beispiele:</strong> WordPad, zeichnen.<br/> <strong>Empfohlene Druckdarstellung:</strong><br/>
<ul>
<li>Die Ausgabe kann für Print (WYSIWYG) optimiert werden, dies ist jedoch nicht erforderlich.</li>
<li>Einige Dokument Formatierungsfunktionen, mit der Möglichkeit, große Objekte ohne Abschneiden zu drucken.</li>
<li>Standard Druckoptionen; benutzerdefinierte Druckoptionen sind optional.</li>
<li>Einfache oder keine Druckvorschau.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Dokument-Viewer</strong><br/> Wird zum Anzeigen von Dokumenten verwendet. Benutzer können den Inhalt oder das Format des Dokuments nicht ändern. <br/></td>
<td><strong>Benutzer Ziele:</strong> Grundlegende Druckunterstützung mit Standarddruck Optionen. Benutzer erwarten gute Ergebnisse, ohne Anpassungen vorzunehmen. Druckprobleme werden automatisch behandelt, da Benutzer das Dokument nicht ändern können.<br/> <strong>Beispiel:</strong> Windows Internet Explorer<br/> <strong>Empfohlene Druckdarstellung:</strong><br/>
<ul>
<li>Die Ausgabe kann für Print (WYSIWYG) optimiert werden, dies ist jedoch nicht erforderlich.</li>
<li>Programm verarbeitet Seitenumbrüche automatisch, entfernt leere Seiten, verarbeitet große Objekte und entfernt Hintergründe und andere Entwurfs Elemente.</li>
<li>Standard Druckoptionen; benutzerdefinierte Druckoptionen sind optional.</li>
<li>Einfache oder keine Druckvorschau.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Hilfsprogramme oder Line-of-Business-Anwendungen</strong><br/> Wird verwendet, um einfache, bestimmte Aufgaben auszuführen. Als Ziel für alle Benutzer. <br/></td>
<td><strong>Benutzer Ziele:</strong> Die Möglichkeit, die ausgewählten Daten effizient zu exportieren. Benutzer erwarten gute Ergebnisse, ohne Anpassungen vorzunehmen. Bei solchen Programmen sind Benutzer häufig überrascht, dass Sie überhaupt keine Druckunterstützung finden.<br/> <strong>Empfohlene Druckdarstellung:</strong><br/>
<ul>
<li>Die Druckunterstützung ist abhängig von den unterstützten Szenarien optional.</li>
<li>Die Ausgabe kann für Print (WYSIWYG) optimiert werden, dies ist jedoch nicht erforderlich.</li>
<li>Einige Funktionen für die Dokument Formatierung. Kann akzeptabel sein, wenn große Objekte abgeschnitten werden.</li>
<li>Standard Druckoptionen.</li>
<li>Die Druckvorschau ist optional.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Drucken Sie keine leeren Seiten oder Seiten mit nur Kopf-und Fußzeilen.** Drucken Sie jedoch leere Seiten, wenn die Kopf-oder Fußzeilen Seitenzahlen enthalten und auf diese Seitenzahlen möglicherweise an anderer Stelle verwiesen wird.
-   **Stellen Sie vor dem Herunterfahren eines Programms alle ausstehenden Druckaufträge vollständig ein.**

### <a name="formatting-pages"></a>Formatieren von Seiten

-   **Formatieren Sie das Text Layout neu, damit es in die Größe der Zielseite passt.** Text nie abschneiden.
-   Wenn Benutzer das Format des Dokuments nicht steuern:
    -   **Verarbeiten Sie große Objekte automatisch durch Skalieren, drehen oder aufteilen zwischen Seiten.** Weitere Richtlinien zum Drucken von großen Objekten finden Sie unter über [dimensionale Objekte](#oversized-objects).
    -   **Optimieren Sie die Seitenumbrüche, um leere und nahezu leere Seiten auszuschließen.**
    -   **Konvertiert hellen Text auf einem dunklen Hintergrund in einen dunklen Text auf einem weißen Hintergrund.**
    -   **Entfernen Sie Hintergründe und andere Entwurfs Elemente,** insbesondere dann, wenn Sie für einen schwarzen und einen weißen Drucker ungeeignet sind.
-   **Wenn das Programm separate partielle Dokumente bereitstellt, stellen Sie eine druckerfreundliche Format Option bereit, um Sie in einem einzelnen Dokument zum Drucken zu konsolidieren.**
-   **Interaktive Elemente entfernen:**
    -   Entfernen Sie Navigations Steuerelemente und Befehls Schaltflächen.
    -   Stellen Sie sicher, dass alle Daten ohne Scrollleisten sichtbar sind.
    -   Ersetzen Sie Verknüpfungen durch ihre Text Entsprechung.

        **Annehmbar:**

        Weitere Informationen finden Sie im UX-Handbuch.

        **Für Druck optimiert:**

        Weitere Informationen finden Sie im UX-Handbuch ( https://msdn.microsoft.com/windowsvista/uxguide) .

        In diesem Beispiel wird der Link durch den entsprechenden Text in Klammern ersetzt.

    -   Verschieben Sie nützliche Informationen, die beim zeigen auf Inline angezeigt werden.

### <a name="oversized-objects"></a>Überdimensionale Objekte

Das Behandeln von großen Objekten, wie z. b. Kalkulations Tabellen, Grafiken und Fotos, ist ein Problem, das für das Drucken eindeutig ist Wählen Sie einen der folgenden Ansätze aus:

-   **Skalieren Sie das Objekt so, dass es auf die Seite passt.** Diese Vorgehensweise funktioniert gut, wenn das Objekt nur wenig zu groß ist, um das Objekt auf einer einzelnen Seite zu halten, und das Objekt immer noch lesbar ist, wenn es herunterskaliert wird.

    ![Screenshot des Fotos, das auf die Hälfte der Seite skaliert wurde ](images/exper-printing-image3.png)

    In diesem Beispiel wird das große Bild so skaliert, dass es auf die Seite passt.

-   **Drehen Sie die Seite.** Diese Vorgehensweise funktioniert gut, wenn einige Seiten im Hochformat (und umgekehrt) besser im Querformat gedruckt werden.

    ![Screenshot des quer fotofotos in Hochformat gedreht ](images/exper-printing-image4.png)

    In diesem Beispiel wird das große Bild so gedreht, dass es besser auf die Seite passt.

-   **Drucken Sie das Objekt auf mehreren Seiten.** Der Ansatz funktioniert gut, wenn das Objekt nicht skaliert werden kann oder nicht skaliert werden soll, und das Drehen der Seite ist nicht erwünscht oder nicht erwünscht. Wenn das Objekt über interne Grenzen verfügt (z. b. die Spalten-und Zeilen unter Teiler in einer Kalkulations Tabelle), brechen Sie die Seiten an diesen Grenzen und nicht innerhalb des Inhalts ab. Wiederholen Sie außerdem alle Elemente, die zum Verständnis der Seite erforderlich sind, z. b. Legenden oder Spaltenüberschriften. Wenn Sie ein Objekt auf mehreren Seiten aufteilen, weisen Sie die Seitenzahlen in der Lesereihenfolge (von links nach rechts, von oben nach unten) zu.

    ![Screenshot der auf der nächsten Seite wiederholten Spaltenköpfe ](images/exper-printing-image5.png)

    In diesem Beispiel wird die große Tabelle auf zwei Seiten gedruckt. Spaltenkopfzeilen werden von Seite zu Seite persistent gespeichert, um das schnelle Verständnis zu vereinfachen.

-   Schneidet **das-Objekt** ab (und druckt nur den Teil des Objekts, der nach dem Abschneiden weiterhin sichtbar ist). Diese Vorgehensweise ist die einfachste Lösung für die Implementierung, aber wahrscheinlich die geringste akzeptable Lösung. Beachten Sie auch, dass das Abschneiden für Text nie akzeptabel ist.

    ![Screenshot der Hälfte des breit Fotos auf der Hochformat Seite ](images/exper-printing-image6.png)

    In diesem Beispiel wird das große Bild abgeschnitten.

### <a name="headers-and-footers"></a>Kopf- und Fußzeilen

-   **Stellen Sie Kopf-und Fußzeilen für Fortgeschrittene und zwischen Programme zur Dokument Erstellung bereit.** Es empfiehlt sich, Kopf-und Fußzeilen für andere Programmtypen bereitzustellen, wenn Sie für mehrseitige Dokumente verwendet werden.
-   **Anpassen von Kopf-und Fußzeilen.** Ermöglicht es Benutzern, die linken, mittleren und rechten Teile zu definieren.
    -   Legen Sie den Dokumentnamen bei Headern standardmäßig auf der linken Seite ab.
    -   Legen Sie für die Fußzeilen das Dokument Copyright oder die Quelle auf der linken Seite und die Seitenzahl auf der rechten Seite (standardmäßig) ab.
-   **Verwenden Sie den benutzerfreundlichen Dateipfad und die URLs.** Zeigt Leerzeichen als Leerzeichen an, nicht "%20".

### <a name="print-commands"></a>Befehl "Drucken"

-   **Verwenden Sie für Menüleisten und Kontextmenüs den Befehl Drucken, mit dem das Dialogfeld "Druckoptionen" angezeigt wird.** Verwenden Sie ein Auslassungs Zeichen, um anzugeben, dass zusätzliche Informationen erforderlich sind.

    ![Screenshot des Menüs "Datei", "Druckbefehl" ausgewählt ](images/exper-printing-image7.png)

    In diesem Beispiel verfügt der Befehl Drucken über ein Auslassungs Zeichen, um anzugeben, dass das Dialogfeld "Druckoptionen" angezeigt wird, um weitere Informationen zu erhalten.

-   **Verwenden Sie für Symbolleisten, die mit einer Menüleiste verwendet werden, einen Befehl für den sofortigen Druck.** Wenn Sie auf die Schaltfläche klicken, wird eine einzelne Kopie des Dokuments auf dem Standarddrucker gedruckt. Solche Symbolleisten Befehle sollten direkt erfolgen. Um anzugeben, dass der Befehl sofort ist, platzieren Sie den Standarddrucker in der QuickInfo. Benutzer können über die Menüleiste auf den Befehl vollständiger Druck zugreifen.

    ![Screenshot des Drucker Symbols und seiner QuickInfo ](images/exper-printing-image8.png)

    In diesem Beispiel druckt der Befehl Drucken in einer Symbolleiste sofort, anstatt das Dialogfeld "Druckoptionen" anzuzeigen. Wenn Sie den Standarddrucker in der QuickInfo platzieren, wird die Text Verstärkung angezeigt, wenn der Benutzer das Dialogfeld umgeht.

-   **Verwenden Sie für Symbolleisten, die ohne eine Menüleiste verwendet werden, eine Schaltfläche zum Teilen drucken.** Wenn Sie auf die Schaltfläche klicken, wird eine einzelne Kopie des Dokuments auf dem Standarddrucker gedruckt. Wenn Sie auf den Pfeil Bereich der Schaltfläche klicken, wird ein Menü mit den Befehlen vollständiger Druck, Druckvorschau und Seite einrichten angezeigt.

    ![Screenshot des Drucker Symbols auf der Trenn Schaltfläche ](images/exper-printing-image9.png)

    In diesem Beispiel verwendet die Windows Internet Explorer-Symbolleiste ein Steuerelement für eine unterteilte Schaltfläche, um alle Druckbefehle bereitzustellen.

-   **Legen Sie für die Benutzeroberfläche des Menüband Befehls den Befehl Drucken im Menü Anwendung ab.**

    ![Screenshot der auf der linken Seite vertikalen Befehle ](images/exper-printing-image10.png)

    Für Multifunktionsleisten wird über das Anwendungsmenü auf den Befehl Drucken zugegriffen.

### <a name="print-options"></a>Druckoptionen

-   **Erstellen Sie kein benutzerdefiniertes Dialogfeld "Druckoptionen".** Wenn Sie zusätzliche Optionen angeben müssen, erweitern Sie das Dialogfeld "Druckoptionen". Verwenden Sie kein separates Dialogfeld für zusätzliche Druckoptionen.

**Falsch:**

![Screenshot des Dialog Felds "benutzerdefinierte Druckoptionen" ](images/exper-printing-image11.png)

In diesem Beispiel verwendet Fabrikam fälschlicherweise ein separates Dialogfeld für zusätzliche Druckoptionen.

**Entwickler:** Weitere Informationen zum Erweitern des Dialog Felds "Drucken" (allgemein) finden Sie unter [printdlgex-Struktur](/windows/win32/api/commdlg/ns-commdlg-printdlgexa).

-   **Wenn Sie das Dialogfeld "Druckoptionen" erweitern, sollten Sie keine bereits bereitgestellten Features duplizieren.**
-   **Wenn Benutzer wahrscheinlich Einstellungen von einem Druckauftrag zum nächsten behalten, nehmen Sie die Standardeinstellungen für diese Einstellungen vor.** Verwenden Sie für den ersten Druckauftrag nach dem Programmstart die Standard Standardwerte, einschließlich des Standard Druckers. Behalten Sie für nachfolgende Druckaufträge in der Programm [Instanz](glossary.md)den zuletzt ausgewählten Drucker und das Papierformat bei. Behalten Sie nicht die Anzahl der Kopien oder Seitenbereiche bei, da diese möglicherweise später erneut ausgewählt werden.
-   **Optimieren Sie die Einstellungen, indem Sie Optionen entfernen, die derzeit nicht zutreffen.** Entfernen Sie Optionen, die nicht mit den Funktionen des ausgewählten Druckers oder der Eigenschaften des aktuellen Dokuments konsistent sind. Beispielsweise könnte eine Foto Druckanwendung die Kombinationen aus Papiergröße, Papiertyp und Druckqualität begrenzen, die die besten Ergebnisse erzielen. Wenn Sie also die Option "Hochglanzpapier" auswählen, können Umschläge aus den Papierformaten entfernt werden. Wenn Benutzer aus irgendeinem Grund alle Optionen anzeigen möchten, können Sie diese Möglichkeit über ein Steuerelement wie z. b. ein Kontrollkästchen bereitstellen.

**Entwickler:** Informationen zum Bestimmen der Funktionen des ausgewählten Druckers finden Sie unter [Print Schema (Druck Schema](../printdocs/print-schema.md)).

-   **Speichern Sie die Dokument bezogenen Druckoptionen für erweiterte Dokumenten Erstellungs Programme im Dokument selbst.** Für diese Programme sind die Druckoptionen ein wesentlicher Bestandteil des Dokuments.
-   **Bei anderen Programmtypen speichern Sie Einstellungen auf Benutzerbasis.**
-   **Es empfiehlt sich, einen nicht standardmäßigen Drucker für den spezialisierten Druck auszuwählen.** Beispielsweise könnte eine Foto Druckanwendung immer den Drucker auswählen, der zuletzt vom Programm verwendet wurde, unabhängig vom Standarddrucker des Systems. Dabei wird davon ausgegangen, dass es sich bei dem Standarddrucker des Systems wahrscheinlich nicht um einen Fotodrucker handelt. Diese Programme sollten die Einstellung für den zuletzt ausgewählten Drucker speichern.
-   **Sperren Sie das Programm nicht, während Sie Druckerfunktionen erkennen.** Dies stellt eine schlechte Benutzer Leistung dar. Verwenden Sie stattdessen Folgendes:
    -   Führen Sie die Drucker Funktionserkennung in einem separaten Thread aus.
    -   Timeout nach 10 Sekunden.
    -   Stellen Sie ein Dialogfeld bereit, um Benutzern das Abbrechen zu gestatten.

![Screenshot des Dialog Felds "Verbinden mit" ](images/exper-printing-image12.png)

In diesem Beispiel erleichtert das Dialogfeld das Abbrechen der Drucker Funktionserkennung, wenn der Benutzer entscheidet, dass die Aufgabe zu lange dauert.

### <a name="print-previews"></a>Druckvorschau

-   **Stellen Sie nach Bedarf ein Druckvor Schau Feature bereit.** Alle Programme zur Dokument Erstellung profitieren von der Druckvorschau, aber Benutzer erwarten Sie nicht in einfachen Dokumenten Erstellungs Programmen. Bei erweiterten Dokumenten Erstellungs Programmen sollten Sie die Unterstützung von Druck Vorgängen direkt im Hauptprogrammfenster unterstützen.

![Screenshot der Seite, die in der Seitenansicht angezeigt wird ](images/exper-printing-image13.png)

In diesem Beispiel verfügt Word über die Unterstützung der Druckvorschau innerhalb des Hauptprogramm Fensters.

-   Bereitstellen von Features für die Druckvorschau, die Benutzern Folgendes ermöglichen:
    -   Evaluieren Sie Ränder, Seitenumbrüche, Seitenausrichtung, Kopfzeilen und Fußzeilen.
    -   Durchsuchen Sie alle Seiten.
    -   Direkt aus der Druckvorschau drucken.

Sie sollten eine interaktive Seitenansicht bereitstellen, damit Benutzer häufig geänderte Einstellungen wie Ränder und Zeilenumbrüche direkt innerhalb der Vorschau anpassen können.

-   **Seiten Seiten Seiten werden innerhalb einer Sekunde dargestellt.** Es ist besser, eine Druckvorschau zu haben, die schnell gerendert wird und genau genug ist, damit Benutzer die Druckergebnisse auswerten können, als eine vollständig genaue Vorschau zu erhalten, die langsam gerendert wird.
-   **Bei erweiterten Dokumenten Erstellungs Programmen können Sie das Standard Dialogfeld "Drucken" erweitern, indem Sie die Vorschau Funktionalität direkt darin einbinden,** anstatt ein separates Dialogfeld dafür zu erstellen.
-   **Stellen Sie eine offensichtliche Schaltfläche zum Schließen des Vorschaumodus bereit.**

![Screenshot des Fensters "Druckvorschau schließen" und "Bezeichnung" ](images/exper-printing-image14.png)

Der Seiten Ansichtsmodus in Word weist einen offensichtlichen Befehl zum Schließen der Vorschau auf.

### <a name="printing-errors"></a>Druckfehler

**Hinweis:** Nachdem der Druckauftrag für den Drucker gespooltet wurde, ist Windows für alle nachfolgenden Fehler verantwortlich. In Ihrem Programm müssen nur Fehler behandelt werden, die vor dem Spoolvorgang des Druckauftrags auftreten.

-   **Überprüfen Sie vor dem Spoolvorgang eines Druckauftrags auf mögliche Druckprobleme, die der Benutzer beheben kann.** Stellen Sie eine klare, präzise Bestätigung vor, bevor Sie den Druck fortsetzen. Stellen Sie nach Möglichkeit ein Angebot zur automatischen Behebung des Problems bereit. Auf diese Weise können Zeit und Geld verschwendet werden.

## <a name="text"></a>Text

-   Damit die Option auf beiden Seiten des Papiers gedruckt werden kann, bezeichnen Sie die Option mit doppelter Seite drucken. Verwenden Sie den Ausdruck "manueller Duplex" nicht.

## <a name="documentation"></a>Dokumentation

-   Verwenden Sie Print, nicht Print out als Verb.
-   Es ist akzeptabel, mit Ausdruck auf das Ergebnis eines Druckauftrags zu verweisen.
-   Druck Warteschlange verwenden, nicht Drucker Warteschlange.

