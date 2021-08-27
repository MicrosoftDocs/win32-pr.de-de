---
title: Drucken (Designgrundkenntnisse)
description: Drucken ist die Benutzererfahrung auf Papier. Es ist leicht zu übersehen, aber es ist ein wichtiger Teil der allgemeinen Benutzererfahrung.
ms.assetid: 26f5a8dc-27b2-4c2d-a05a-f942784c3cf9
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 50eb7523b3f816e54bf296632687b4811fac1b1c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987263"
---
# <a name="printing-design-basics"></a>Drucken (Designgrundkenntnisse)

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Drucken ist die Benutzererfahrung auf Papier. Es ist leicht zu übersehen, aber es ist ein wichtiger Teil der allgemeinen Benutzererfahrung.

In diesem Artikel bezieht *sich der* Druck auf die Benutzererfahrung auf Papier, bei der die Ausgabe an Papier anstatt an die Bildschirmanzeige geleitet wird. *Das druckerfreundliche Format* bezieht sich auf Änderungen, die das Programm an der Bildschirmanzeigeausgabe machen kann, die es für die Papierausgabe besser geeignet machen.

Trotz der Vorhersage, dass das Computing zu einem "papierlosen Büro" führen würde, wird jetzt so viel wie je zuvor gedruckt. Wir verteilen hard copies of Microsoft PowerPoint presentation decks (Festplattenkopien von Microsoft PowerPoint Presentation Decks), drucken Onlineartikel, die wir online entdecken, möchten aber später genauer recherchiert werden. Wir drucken wichtige E-Mails oder Lebensläufe, die wir erhalten haben, in elektronischer Form und so weiter. Auch wenn das Drucken beim Entwerfen einer Benutzeroberfläche leicht übersehen werden kann, denken Sie daran, dass das Drucken ein wichtiger Bestandteil der allgemeinen Benutzeroberfläche ist.

**Hinweis:** Richtlinien im Zusammenhang [mit häufigen Dialogen](win-common-dlg.md) werden in einem separaten Artikel vorgestellt.

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Um zu entscheiden, ob Ihr Programm das Drucken unterstützen muss, sollten Sie die folgenden Fragen berücksichtigen:

-   **Welche Art von Programm entwerfen Sie?** Der Programmtyp ist ein guter Indikator für die entsprechende Druckunterstützung. Dokument- und Bilderstellungs-, Anzeige- und Browserprogramme benötigen eine hervorragende Druckunterstützung, während andere Arten von Programmen möglicherweise nur in geringerem Maße Druckunterstützung benötigen. (Eine Liste der Programmtypen finden Sie im Abschnitt [Druckmuster](#printing-patterns) dieses Artikels.)
-   **Wird das Programm in Szenarien verwendet, die von direkter Papierausgabe profitieren?** Wenn ja, ist es bequemer, dem Programm Druckunterstützung hinzuzufügen, als benutzer müssen die Daten in ein anderes Programm kopieren, um sie zu drucken.

## <a name="design-concepts"></a>Entwurfskonzepte

### <a name="design-your-program-to-eliminate-unnecessary-printing"></a>Entwerfen Des Programms, um unnötiges Drucken zu vermeiden

Es gibt viele Gründe, warum Benutzer einige gute und andere weniger gut drucken müssen. Benutzer sollten drucken, weil sie möchten, nicht, weil sie dies müssen. Die Anforderung, dass Benutzer drucken müssen, kann ein Zeichen für fehlende Features sein. In der Vergangenheit mussten Benutzer z. B. Dokumente drucken, um Kommentare zu machen und Revisionen vorschlagen zu können. Jetzt können Benutzer diese Aufgaben jedoch direkt innerhalb Microsoft Word ausführen. **Überprüfen Sie die Szenarios Ihres Programms, die drucken, und stellen Sie so weit wie möglich sicher, dass die Notwendigkeit des Druckens optional ist und nicht das Ergebnis fehlender Features ist.**

Es ist auch zu beachten, dass das Einsparen von Ressourcen wie Papier und Ink hilfreich ist und Organisationen langfristig Geld spart.

### <a name="understand-the-differences-between-screen-display-and-print"></a>Verstehen der Unterschiede zwischen Bildschirmanzeige und Drucken

Es gibt zwar viele Ähnlichkeiten zwischen Anzeigeausgabe und Druck, aber es gibt auch viele Unterschiede. Ausgabe drucken:

-   **Verfügt über einen hohen DPI-Durchdungs-/** Die Anzeigeausgabe liegt in der Regel bei 96 oder 120 DPI (Dots per Inch), während die Druckerausgabe in der Regel bei 600 dpi oder höher liegt.
-   **Verfügt über verschiedene optimale Schriftarten.** Obwohl gut entworfene Schriftarten sowohl für Anzeige- als auch für Druckschriftarten gut funktionieren, sind Serifenschriftarten bei hohen Auflösungen für große Mengen von Text besser lesbar als Serifenschriftarten. Daher sollten große Mengen von Text, der hauptsächlich für den Druck bestimmt ist, eine Serifenschriftart verwenden, während Text, der in erster Linie für die Anzeige vorgesehen ist, eine Sans Serif-Schriftart verwenden sollte. Weitere Informationen finden Sie unter [Schriftarten](vis-fonts.md) (Segoe UI).
-   **Verfügt über ein Seitenverhältnis.** Die Anzeige hat [](glossary.md) in der Regel ein niedriges Seitenverhältnis (4:3 oder 5:4), während der Druck ein hohes Seitenverhältnis verwendet (8,5:11 oder 1:1.4142 basierend auf den Standardseitengrößen). Dies liegt [daran, dass das Drucken](glossary.md) im Hochformat häufiger als der [Querformatmodus ist.](glossary.md)
-   **Verfügt über Seiten.** Folglich wird die Ausgabe ausgegeben:
    -   Verfügt über Standardseitengrößen. Der Standard in den USA und Kanada ist das Papier 8,5"x11". Der Standard ist überall sonst A4-Papier.
    -   Verfügt über Seitenumbrüche.
    -   Verfügt über Seitenränder.
    -   Verfügt über Kopf- und Fußzeilen.
    -   Verfügt über eine ein- oder doppelseitige Ausgabe.
    -   Kann mehrere Kopien haben.
    -   Kann in der reihenfolgen- oder selektiven Reihenfolge gedruckt werden.
-   **Verfügt über viele Optionen.** Benutzer können einen Drucker und eine Papiergröße, Druckeroptionen (z. B. Druckqualität, doppelseitiges Drucken und Heften), Anzahl von Kopien, Seitenbereichen, Sortierung und Druckformat auswählen.
-   **Benötigt Zeit und Geld.** Es kann sehr lange dauern, bis ein großes Dokument oder ein hochwertiges Foto gedruckt wird, und die Kosten für Papier und Ink summiert sich im Laufe der Zeit. Im Gegensatz dazu ist die Anzeigeausgabe sofort und im Wesentlichen kostenlos.
-   **Kann schwarz und weiß sein.** Viele Drucker sind heute schwarz und weiß, während nur wenige Displays monofarbig sind.
-   **Ist nicht interaktiv.** Benutzer können keine Seiten oder Steuerelemente scrollen, um weitere Inhalte anzuzeigen. Sie können nicht auf Links oder Schaltflächen klicken oder auf Steuerelemente bewegen. Interaktive Inhalte haben beim Drucken keinen Wert.
-   **Es kann nicht mehr auf Papier, Ink oder Toner oder offline gehen.** Folglich benötigt die Papierausgabe mehr Fehlerbehandlung und Problembehandlung.

Diese Unterschiede können sich auf Ihren Druckentwurf auswirken. Das Erstellen einer guten Druckerfahrung erfordert mehr als nur das Ansenden der Programmausgabe an den Drucker.

### <a name="wysiwyg-and-the-evolving-requirements-of-screen-display"></a>WYSIWYG und die sich entwickelnden Anforderungen der Bildschirmanzeige

In der Vergangenheit wird das grundlegendste Prinzip für die Benutzeroberfläche für das Drucken als WYSIWYG ("what you see is what you get" (Was Sie sehen, ist das, was Sie erhalten) bekannt. Dieses Prinzip legt nahe, dass eine starke Beziehung zwischen dem, was auf der Anzeige zu sehen ist, und dem Gedruckten besteht. Bevor WYSIWYG zur Standardübung wurde, gab es häufig keine Beziehung zwischen der Anzeige- und der Druckversion eines Dokuments. Benutzer mussten drucken, um zu sehen, wie das Dokument tatsächlich auf Papier aussieht. Die Verwendung von WYSIWYG war eine deutliche Verbesserung der Produktivität, da die meisten Programme zu diesem Zeitpunkt in erster Linie für die Dokumenterstellung und den Druck konzipiert wurden.

Heutzutage ist es üblich, dass Websites die Anzeige optimieren, und ihr druckerfreundliches Format kann sich deutlich unterscheiden. Darüber hinaus verfügen wir über verschiedene Computergeräte (z. B. Smartphones und persönliche digitale Assistenten), die häufig für kleine Displays optimierte Ausgaben benötigen. Obwohl WYSIWYG immer noch der beste Ansatz für Dokumenterstellungsprogramme ist, ist es für andere Programme oft sinnvoller, für eine Vielzahl von Zielgeräten zu optimieren. Bei solchen Programmen kann sich das, was auf einer PC-Anzeige angezeigt wird, von dem unterscheiden, was auf anderen Geräteanzeigen angezeigt wird. Dies kann sich von dem unterscheiden, was Sie auf der gedruckten Seite erhalten.

### <a name="optimize-for-printing"></a>Optimieren für das Drucken

Programme, die keine strenge WYSIWYG-Druckerfahrung verwenden, können für das Drucken weiterhin auf folgende Weise optimiert werden:

-   Formatieren Sie das Layout für die Zielseitengröße neu.
-   Stellen Sie eine Druckvorschau zur Verfügung, vorzugsweise mit einfachen Anpassungsoptionen, mit denen Benutzer direkt im Druckdialogfeld experimentieren können (z. B. ziehende Ränder).
-   Geben Sie gegebenenfalls eine druckerfreundliche Formatoption an.
    -   Konsolidieren Sie separate Teildokumente in einem einzelnen Dokument.
    -   Entfernen Sie Hintergründe und andere Entwurfselemente, z. B. Werbeanzeigen, insbesondere dann, wenn sie für einen Schwarz-Weiß-Drucker nicht geeignet sind.
    -   Entfernen Sie interaktive Elemente wie Navigationssteuerelemente und Befehlsschaltflächen.
    -   Stellen Sie sicher, dass alle Daten sichtbar sind, ohne auf scrollbars oder mit dem Maus mausern zu müssen.

        **Anzeigeversion:**

        ![Screenshot des für den Bildschirm optimierten Berichts ](images/exper-printing-image1.png)

        **Druckerfreundliche Version:**

        ![Screenshot desselben Berichts, der für den Druck optimiert ist ](images/exper-printing-image2.png)

        In der druckerfreundlichen Version sind alle Daten auf der gedruckten Seite sichtbar, und die interaktiven Elemente werden entfernt.

    -   Ersetzen Sie Links durch die entsprechende Textentsprechung.

        **Annehmbar:**

        Weitere Informationen finden Sie im UX-Handbuch.

        **Optimiert für das Drucken:**

        Weitere Informationen finden Sie im UX-Handbuch ( https://msdn.microsoft.com/windowsvista/uxguide) .

-   Konvertieren Sie hellen Text auf einem dunklen Hintergrund in dunklen Text auf einem weißen Hintergrund.

### <a name="include-the-right-print-options"></a>Schließen Sie die richtigen Druckoptionen ein.

Das Allgemeine Dialogfeld Druckoptionen bietet Optionen für:

-   Wählen Sie den Drucker und die Papiergröße aus.
-   Festlegen von Druckereigenschaften.
-   Wählen Sie den Seitenbereich, die Anzahl der Kopien und die Sortierung aus.
-   Verwenden Sie beide Seiten des Papiers.

Ihr Programm erfordert möglicherweise zusätzliche Optionen, z. B. Dokumentinhaltsoptionen (welche Inhalte gedruckt werden), Formatoptionen (Druck, einschließlich Druckqualität, Bildgrößen, Anpassung an Rahmen) und Farboptionen. Wenn Sie zusätzliche Optionen bereitstellen müssen, erweitern Sie dazu das allgemeine Dialogfeld Druckoptionen. Erstellen Sie kein benutzerdefiniertes Dialogfeld Drucken.

Berücksichtigen Sie beim Entwerfen der Druckoptionen die Benutzererfahrung beim Drucken mehrerer Dokumente. Die Wahrscheinlichkeit, dass der nächste Druckauftrag dem letzten Druckauftrag sehr ähnlich ist. Wenn Sie die Standardeinstellungen für Neudrucke und ähnliche Druckaufträge optimieren, werden Benutzer nicht jedes Mal vollständig neu gestartet.

### <a name="design-print-preview-for-performance-and-usability"></a>Entwerfen der Druckvorschau für Leistung und Benutzerfreundlichkeit

**Ein falscher Druckauftrag verschwendet Zeit und Geld. Bei Programmen zum Erstellen von Dokumenten sollten Benutzer in der Lage sein, die Ergebnisse vor dem eigentlichen Drucken auswerten zu können.** Eine Seitenansicht sollte Benutzern Dies ermöglichen:

-   Wertet Ränder, Seitenumbrüche, Seitenausrichtung, Kopf- und Fußzeilen aus.
-   Durchsuchen Sie alle Seiten.
-   Drucken Sie direkt aus der Druckvorschau.

Das Rendern einiger komplexer Dokumente (z. B. cad-Zeichnungen mit computergestütztem Entwurf) kann \[ \] sehr lange dauern. Die Leistung der Vorschau ist wichtig, dass eine Druckvorschau recht mühsam werden kann, wenn es einige Zeit dauert, jede Seite zu rendern. **Daher ist es besser, über eine Druckvorschau zu verfügen, die schnell gerendert wird und genau genug ist, damit Benutzer die Druckergebnisse auswerten können, anstatt eine vollständig genaue Vorschau zu haben, die langsam gerendert wird.**

Berücksichtigen Sie beim Entwerfen der Druckvorschau die gesamte Aufgabe der Vorbereitung des Drucks. Nach welchen Benutzern wird gesucht? Was werden sie ändern? Programme zum Erstellen von Dokumenten sollten eine interaktive Druckvorschau bieten, damit Benutzer häufig geänderte Einstellungen wie Ränder und Zeilenumbrüche innerhalb der Vorschau anpassen können.

Ihr Programm sollte jedoch im bestmöglichen Umfang standardmäßig das Richtige tun. Warnen Sie bei Bedarf vor Drucksituationen, bei denen es unwahrscheinlich ist, dass es sich um die vom Benutzer beabsichtigte Situation handelt. Verlassen Sie sich nicht darauf, dass Benutzer Probleme mit der Seitenansicht finden. Angenommen, eine Kalkulationstabelle enthält zu viele Spalten, um sie auf einer einzelnen Seite im Hochformat zu drucken. Während das Programm ein Bestätigungsdialogfeld präsentieren könnte, ist es eine bessere Lösung, automatisch im Querformat zu drucken.

**Wenn Sie nur fünf Dinge tun...**

1.  Entwerfen Sie eine Druckerfahrung, die für Ihren Programmtyp geeignet ist.
2.  Überprüfen Sie die Szenarios Ihres Programms, die das Drucken beinhalten, und machen Sie die Notwendigkeit des Druckens so weit wie möglich optional.
3.  Stellen Sie nützliche Druckerweiterungen zur Verfügung, indem Sie das Allgemeine Dialogfeld Drucken anpassen. Erstellen Sie zu diesem Zweck kein benutzerdefiniertes Dialogfeld Drucken.
4.  Optimieren Sie die Druckoptionen für Neudrucke und ähnliche Druckaufträge.
5.  Stellen Sie bei Bedarf eine Vorschaufunktion zur Verfügung.

## <a name="printing-patterns"></a>Druckmuster

Der Programmtyp ist der primäre Indikator für die entsprechende Druckerfahrung:




| Bezeichnung | Wert |
|--------|-------|
| <strong>Erweiterte Dokumenterstellung</strong><br /> Wird zum Erstellen, Anzeigen und Drucken von High-End-Dokumenten verwendet. Die Möglichkeit, hochwertige Drucke zu erstellen, ist einer der Hauptgründe, warum das Programm vorhanden ist. Für erfahrene Benutzer. <br /> | <strong>Benutzerziele:</strong> Perfekte Ergebnisse: Detaillierte Kontrolle über die Druckausgabe.<br /><strong>Beispiel:</strong> Microsoft Word<br /><strong>Empfohlene Druckerfahrung:</strong><br /><ul><li>Ausgabe optimiert für Print (WYSIWYG).</li><li>Erweiterte Dokumentformatierungsfeatures mit Optionen zum Drucken großer Objekte.</li><li>Erweiterte Druckoptionen, einschließlich Kopf- und Fußzeilen. Dokumentbezogene Druckoptionen werden im Dokument selbst gespeichert.</li><li>Schnelle, genaue und leistungsstarke Druckvorschauen.</li></ul> | 
| <strong>Erstellen von Zwischendokumenten</strong><br /> Wird zum Erstellen und Anzeigen komplexerer Dokumente verwendet. Die Fähigkeit, hochwertige Drucke zu erstellen, ist wichtig, aber nicht unbedingt einer der Hauptgründe, warum das Programm vorhanden ist. Für Zwischenbenutzer. <br /> | <strong>Benutzerziele:</strong> Gute Ergebnisse mit minimalem Aufwand. Etwas Kontrolle über die Druckausgabe.<br /><strong>Beispiele:</strong> Die Microsoft Office, z. B. Outlook und Excel.<br /><strong>Empfohlene Druckerfahrung:</strong><br /><ul><li>Ausgabe optimiert für Print (WYSIWYG).</li><li>Einige Dokumentformatierungsfeatures mit der Möglichkeit, große Objekte ohne Abschneiden zu drucken.</li><li>Einige benutzerdefinierte Druckoptionen, einschließlich Kopf- und Fußzeilen.</li><li>Präzise, einfach zu verwendende Druckvorschauen.</li></ul> | 
| <strong>Einfache Dokumenterstellung</strong><br /> Wird zum Erstellen und Anzeigen einfacher Dokumente verwendet. Für alle Benutzer. <br /> | <strong>Benutzerziele:</strong> Einfache Druckunterstützung mit Standarddruckoptionen. Benutzer erwarten gute Ergebnisse ohne Optimierung.<br /><strong>Beispiele:</strong> WordPad, Paint.<br /><strong>Empfohlene Druckerfahrung:</strong><br /><ul><li>Die Ausgabe kann für print (WYSIWYG) optimiert werden, dies ist jedoch nicht erforderlich.</li><li>Einige Dokumentformatierungsfeatures mit der Möglichkeit, große Objekte ohne Abschneiden zu drucken.</li><li>Standarddruckoptionen; Benutzerdefinierte Druckoptionen sind optional.</li><li>Einfache oder keine Druckvorschau.</li></ul> | 
| <strong>Dokument-Viewer</strong><br /> Wird zum Anzeigen von Dokumenten verwendet. Benutzer können den Dokumentinhalt oder das Format nicht ändern. <br /> | <strong>Benutzerziele:</strong> Einfache Druckunterstützung mit Standarddruckoptionen. Benutzer erwarten gute Ergebnisse ohne Optimierung. Druckprobleme werden automatisch behandelt, da Benutzer das Dokument nicht ändern können.<br /><strong>Beispiel:</strong> Windows Internet Explorer<br /><strong>Empfohlene Druckerfahrung:</strong><br /><ul><li>Die Ausgabe kann für print (WYSIWYG) optimiert werden, dies ist jedoch nicht erforderlich.</li><li>Das Programm verarbeitet Seitenumbrüche automatisch, entfernt leere Seiten, verarbeitet große Objekte und entfernt Hintergründe und andere Entwurfselemente.</li><li>Standarddruckoptionen; Benutzerdefinierte Druckoptionen sind optional.</li><li>Einfache oder keine Druckvorschau.</li></ul> | 
| <strong>Hilfsprogramme oder line-of-business-Anwendungen</strong><br /> Wird verwendet, um einfache, spezifische Aufgaben auszuführen. Für alle Benutzer. <br /> | <strong>Benutzerziele:</strong> Möglichkeit zum effizienten Exportieren ausgewählter Daten. Benutzer erwarten gute Ergebnisse ohne Optimierung. Häufig sind Benutzer bei solchen Programmen sehr versiert, überhaupt Druckunterstützung zu finden.<br /><strong>Empfohlene Druckerfahrung:</strong><br /><ul><li>Die Druckunterstützung ist abhängig von den unterstützten Szenarien optional.</li><li>Die Ausgabe kann für print (WYSIWYG) optimiert werden, dies ist jedoch nicht erforderlich.</li><li>Einige Dokumentformatierungsfeatures. Kann akzeptabel sein, wenn große Objekte abgeschnitten werden.</li><li>Standarddruckoptionen.</li><li>Druckvorschauen optional.</li></ul> | 




 

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Geben Sie keine leeren Seiten oder Seiten mit nur Kopf- und Fußzeilen aus.** Drucken Sie jedoch leere Seiten, wenn die Kopf- oder Fußzeilen Seitenzahlen enthalten und auf diese Seitennummern an anderer Stelle verwiesen werden kann.
-   **Spoolt alle ausstehenden Druckaufträge vollständig aus, bevor ein Programm heruntergefahren wird.**

### <a name="formatting-pages"></a>Formatieren von Seiten

-   **Formatiert das Textlayout so, dass es in die Größe der Zielseite passt.** Text nie abschneiden.
-   Wenn Benutzer das Format des Dokuments nicht steuern:
    -   **Behandeln Sie große Objekte automatisch durch Skalieren, Drehen oder Teilen auf mehrere Seiten.** Weitere Richtlinien zum Drucken großer Objekte finden Sie unter [Überdimensionierte Objekte.](#oversized-objects)
    -   **Optimieren Sie die Seitenumbrüche, um leere und fast leere Seiten zu vermeiden.**
    -   **Konvertieren von hellem Text auf einem dunklen Hintergrund in dunklen Text auf einem weißen Hintergrund.**
    -   **Entfernen Sie Hintergründe und andere Entwurfselemente,** insbesondere wenn sie für einen Schwarz-Weiß-Drucker nicht geeignet sind.
-   **Wenn Ihr Programm separate Teildokumente vorstellt, stellen Sie eine druckfreundliche Formatoption bereit, um sie in einem einzigen Dokument zum Drucken zu konsolidieren.**
-   **Entfernen interaktiver Elemente:**
    -   Entfernen Sie Navigationssteuerelemente und Befehlsschaltflächen.
    -   Stellen Sie sicher, dass alle Daten ohne Bildlaufleisten sichtbar sind.
    -   Ersetzen Sie Links durch die entsprechende Textentsprechung.

        **Annehmbar:**

        Weitere Informationen finden Sie im Leitfaden zur Benutzererfahrung.

        **Für den Druck optimiert:**

        Weitere Informationen finden Sie im Leitfaden zur Benutzererfahrung ( https://msdn.microsoft.com/windowsvista/uxguide) .

        In diesem Beispiel wird der Link durch die entsprechende Textentsprechung in Klammern ersetzt.

    -   Verschieben Sie nützliche Informationen, die angezeigt werden, wenn Sie mit dem Mauszeiger auf Inline zeigen.

### <a name="oversized-objects"></a>Überdimensionierte Objekte

Die Behandlung großer Objekte, z. B. Tabellen, Grafiken und Fotos, ist ein Problem, das nur beim Drucken auftritt. Wählen Sie einen der folgenden Ansätze aus:

-   **Skalieren Sie das Objekt so, dass es auf die Seite passt.** Dieser Ansatz funktioniert gut, wenn das Objekt nur etwas zu groß zum Drucken ist, das Objekt auf einer einzelnen Seite wichtig ist und das Objekt beim herunterskalieren noch lesbar ist.

    ![Screenshot des Fotos, das auf die Hälfte einer Seite skaliert wurde ](images/exper-printing-image3.png)

    In diesem Beispiel wird das große Bild so skaliert, dass es auf die Seite passt.

-   **Drehen Sie die Seite.** Dieser Ansatz funktioniert gut, wenn einige Seiten im Querformat im Hochformat (und umgekehrt) besser gedruckt werden.

    ![Screenshot des Querformatfotos, das ins Hochformat gedreht wird ](images/exper-printing-image4.png)

    In diesem Beispiel wird das große Bild gedreht, damit es besser auf die Seite passt.

-   **Drucken Sie das Objekt auf mehreren Seiten.** Der Ansatz funktioniert gut, wenn das Objekt nicht skaliert werden kann oder nicht skaliert werden sollte und das Rotieren der Seite nicht hilfreich ist oder nicht erwünscht ist. Wenn das Objekt interne Grenzen hat (z. B. die Spalten- und Zeilenteiler in einer Kalkulationstabelle), unterbrechen Sie die Seiten an diesen Grenzen anstatt innerhalb des Inhalts. Wiederholen Sie außerdem alle Elemente, die zum Verstehen der Seite erforderlich sind, z. B. Legenden oder Spaltenüberschriften. Weisen Sie beim Aufteilen eines Objekts auf mehrere Seiten die Seitenzahlen in Lesereihenfolge zu (von links nach rechts, von oben nach unten).

    ![Screenshot der Spaltenköpfe, die auf der nächsten Seite wiederholt werden ](images/exper-printing-image5.png)

    In diesem Beispiel wird die große Tabelle auf zwei Seiten gedruckt. Spaltenüberschriften bleiben von Seite zu Seite erhalten, um ein schnelles Verständnis zu ermöglichen.

-   **Schneidet das Objekt** ab (druckt nur den Teil des Objekts, der nach dem Abschneiden noch sichtbar ist). Dieser Ansatz ist die einfachste Zu implementierende Lösung, aber wahrscheinlich die am wenigsten akzeptable Lösung. Beachten Sie auch, dass das Abschneiden für Text nie akzeptabel ist.

    ![Screenshot des halb breiten Fotos auf der Hochformatseite ](images/exper-printing-image6.png)

    In diesem Beispiel wird das große Bild abgeschnitten.

### <a name="headers-and-footers"></a>Kopf- und Fußzeilen

-   **Stellen Sie Kopf- und Fußzeilen für erweiterte und zwischengeschaltete Dokumente bereit.** Erwägen Sie, Kopf- und Fußzeilen für andere Arten von Programmen bereitzustellen, wenn sie für mehrseitige Dokumente verwendet werden.
-   **Gestalten Sie Kopf- und Fußzeilen anpassbar.** Benutzern das Definieren der linken, mittleren und rechten Teile gestatten.
    -   Legen Sie für Header standardmäßig den Dokumentnamen auf der linken Seite ab.
    -   Legen Sie für Fußzeilen das Copyright oder die Quelle des Dokuments auf der linken Seite und die Seitenzahl standardmäßig auf der rechten Seite fest.
-   **Verwenden Sie benutzerfreundliche Dateipfade und URLs.** Zeigen Sie Leerzeichen als Leerzeichen an, nicht "%20".

### <a name="print-commands"></a>Drucken von Befehlen

-   **Verwenden Sie für Menüleisten und Kontextmenüs den Befehl Drucken, der das allgemeine Dialogfeld Druckoptionen anzeigt.** Verwenden Sie eine Auslassungszeichen, um anzugeben, dass zusätzliche Informationen erforderlich sind.

    ![Screenshot des Dateimenüs, Ausgewählter Druckbefehl ](images/exper-printing-image7.png)

    In diesem Beispiel weist der Befehl Drucken eine Auslassungszeichen auf, um anzugeben, dass das allgemeine Dialogfeld Druckoptionen angezeigt wird, um weitere Informationen zu erhalten.

-   **Verwenden Sie für Symbolleisten, die mit einer Menüleiste verwendet werden, einen sofortigen Befehl Drucken.** Wenn Sie auf die Schaltfläche klicken, wird eine einzelne Kopie des Dokuments auf dem Standarddrucker ausgegeben. Solche Symbolleistenbefehle sollten sofort sein. Um anzugeben, dass der Befehl sofort ist, legen Sie den Standarddrucker in die QuickInfo ein. Benutzer können über die Menüleiste auf den vollständigen Befehl Drucken zugreifen.

    ![Screenshot des Druckersymbols und der zugehörigen QuickInfo ](images/exper-printing-image8.png)

    In diesem Beispiel wird der Befehl Drucken auf einer Symbolleiste sofort gedruckt, anstatt das allgemeine Dialogfeld Druckoptionen anzuzeigen. Wenn Sie den Standarddrucker in die QuickInfo setzen, wird textverstärkt, dass der Benutzer das Dialogfeld umgeht.

-   **Verwenden Sie für Symbolleisten, die ohne Menüleiste verwendet werden, die Schaltfläche Teilen drucken.** Wenn Sie auf die Schaltfläche klicken, wird eine einzelne Kopie des Dokuments auf dem Standarddrucker ausgegeben. Wenn Sie auf den Pfeilteil der Schaltfläche klicken, wird ein Menü mit den vollständigen Befehlen Drucken, Seitenvorschau und Seiteneinrichtung angezeigt.

    ![Screenshot des Druckersymbols auf geteilter Schaltfläche ](images/exper-printing-image9.png)

    In diesem Beispiel verwendet die Windows Internet Explorer Symbolleiste ein Steuerelement für geteilte Schaltflächen, um alle Druckbefehle bereitzustellen.

-   **Legen Sie für die Benutzeroberfläche des Menübandbefehls den Befehl Drucken im Anwendungsmenü ab.**

    ![Screenshot der vertikal auf der linken Seite platzierten Befehle ](images/exper-printing-image10.png)

    Für Menübänder wird über das Anwendungsmenü auf den Befehl Drucken zugegriffen.

### <a name="print-options"></a>Druckoptionen

-   **Erstellen Sie kein benutzerdefiniertes Dialogfeld Druckoptionen.** Wenn Sie zusätzliche Optionen angeben müssen, erweitern Sie das allgemeine Dialogfeld Druckoptionen. Verwenden Sie kein separates Dialogfeld für zusätzliche Druckoptionen.

**Falsch:**

![Screenshot des Dialogfelds "Benutzerdefinierte Druckoptionen" ](images/exper-printing-image11.png)

In diesem Beispiel verwendet Fabrikam fälschlicherweise ein separates Dialogfeld für zusätzliche Druckoptionen.

**Entwickler:** Informationen zum Erweitern des allgemeinen Dialogfelds Drucken finden Sie unter [PRINTDLGEX-Struktur.](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

-   **Duplizieren Sie beim Erweitern des allgemeinen Dialogfelds Druckoptionen keine bereits bereitgestellten Features.**
-   **Wenn Benutzer die Einstellungen wahrscheinlich von einem Druckauftrag zum nächsten beibehalten, sollten Sie diese Einstellungen als Standardwerte festlegen.** Verwenden Sie für den ersten Druckauftrag nach dem Programmstart die Standardwerte, einschließlich des Standarddruckers. Behalten Sie bei nachfolgenden Druckaufträgen in der [Programminstanz](glossary.md)die zuletzt ausgewählte Drucker- und Papiergröße bei. Behalten Sie die Anzahl der Kopien oder Seitenbereiche nicht bei, da diese später deutlich seltener wieder ausgewählt werden.
-   **Optimieren Sie die Einstellungen, indem Sie Optionen entfernen, die derzeit nicht gelten.** Entfernen Sie Optionen, die mit den Funktionen des ausgewählten Druckers oder den Merkmalen des aktuellen Dokuments inkonsistent sind. Beispielsweise könnte eine Fotodruckanwendung die Kombinationen aus Papiergröße, Papiertyp und Druckqualität einschränken, die die besten Ergebnisse liefern, sodass die Auswahl einer Option für Papierdruckumschläge aus den Papierformaten entfernen kann. Wenn Benutzer aus irgendeinem Grund alle Optionen anzeigen möchten, können Sie diese Möglichkeit über ein Steuerelement wie ein Kontrollkästchen bereitstellen.

**Entwickler:** Informationen zum Bestimmen der Funktionen des ausgewählten Druckers finden Sie unter [Druckschema.](../printdocs/print-schema.md)

-   **Speichern Sie bei erweiterten Dokumentenerstellungsprogrammen die dokumentbezogenen Druckoptionen im Dokument selbst.** Für diese Programme sind die Druckoptionen ein integraler Bestandteil des Dokuments.
-   **Speichern Sie einstellungen für andere Arten von Programmen pro Benutzer.**
-   **Erwägen Sie die Auswahl eines nicht standardmäßigen Druckers für spezialisiertes Drucken.** Beispielsweise kann eine Fotodruckanwendung unabhängig vom Standarddrucker des Systems immer den zuletzt vom Programm verwendeten Drucker auswählen. Dabei wird davon ausgegangen, dass der Standarddrucker des Systems wahrscheinlich kein Fotodrucker ist. Solche Programme sollten die Einstellung für den zuletzt ausgewählten Drucker speichern.
-   **Sperren Sie Ihr Programm nicht, während Sie Druckerfunktionen erkennen.** Dies stellt eine schlechte Benutzererfahrung dar. Stattdessen haben Sie eine der beiden:
    -   Führen Sie die Druckerfunktionserkennung in einem separaten Thread aus.
    -   Time out after 10 seconds. (Time out nach 10 Sekunden.
    -   Geben Sie ein Dialogfeld an, in dem Benutzer abbrechen können.

![Screenshot des Dialogfelds "Herstellen einer Verbindung mit" ](images/exper-printing-image12.png)

In diesem Beispiel erleichtert das Dialogfeld das Abbrechen der Druckerfunktionserkennung, wenn der Benutzer entscheidet, dass die Aufgabe zu lange dauert.

### <a name="print-previews"></a>Druckvorschau

-   **Stellen Sie ggf. ein Druckvorschaufeature bereit.** Alle Programme zur Dokumenterstellung profitieren von Druckvorschau, benutzer erwarten sie jedoch nicht in einfachen Dokumentenerstellungsprogrammen. Bei erweiterten Programmen zur Dokumenterstellung sollten Sie erwägen, die Druckvorschau direkt im Hauptprogrammfenster zu unterstützen.

![Screenshot der Seite, die in der Druckvorschau angezeigt wird ](images/exper-printing-image13.png)

In diesem Beispiel unterstützt Word die Seitenansicht im Hauptprogrammfenster.

-   Bereitstellen von Druckvorschaufeatures, mit denen Benutzer:
    -   Werten Sie Ränder, Seitenumbrüche, Seitenausrichtung, Kopf- und Fußzeilen aus.
    -   Durchsuchen Sie alle Seiten.
    -   Direktes Drucken aus der Druckvorschau.

Erwägen Sie die Bereitstellung einer interaktiven Druckvorschau, damit Benutzer häufig geänderte Einstellungen wie Ränder und Zeilenumbrüche direkt innerhalb der Vorschau anpassen können.

-   **Lassen Sie Seiten der Druckvorschau innerhalb einer Sekunde rendern.** Es ist besser, eine Druckvorschau zu haben, die schnell gerendert wird und so genau ist, dass Benutzer die Druckergebnisse auswerten können, als eine vollständig genaue Vorschau zu haben, die langsam gerendert wird.
-   **Bei erweiterten Dokumentenerstellungsprogrammen sollten Sie erwägen, das Standarddialogfeld Drucken zu erweitern, indem Sie die Vorschaufunktionen direkt darin integrieren,** anstatt dafür ein separates Dialogfeld zu erstellen.
-   **Geben Sie eine offensichtliche Schaltfläche zum Schließen des Vorschaumodus an.**

![Screenshot des Symbols und der Bezeichnung zum Schließen der Druckvorschau ](images/exper-printing-image14.png)

Der Druckvorschaumodus in Word verfügt über einen offensichtlichen Befehl zum Schließen der Vorschau.

### <a name="printing-errors"></a>Druckfehler

**Hinweis:** Nachdem der Druckauftrag mit dem Drucker gespoolt wurde, ist Windows für alle nachfolgenden Fehler verantwortlich. Das Programm muss nur Fehler behandeln, die auftreten, bevor der Druckauftrag gespoolt wird.

-   **Überprüfen Sie vor dem Spooling eines Druckauftrags auf mögliche Druckprobleme, die der Benutzer beheben kann.** Stellen Sie eine klare, präzise Bestätigung vor, bevor Sie mit dem Drucken fortfahren. Bieten Sie nach Möglichkeit an, das Problem automatisch zu beheben. Auf diese Weise können Zeit- und Geldverschwendung vermieden werden.

## <a name="text"></a>Text

-   Wenn Sie auf beiden Seiten des Papiers drucken möchten, beschriften Sie die Option Doppelseitig drucken. Verwenden Sie nicht den Ausdruck Manual Duplex.

## <a name="documentation"></a>Dokumentation

-   Verwenden Sie print,, not print out, als Verb.
-   Es ist akzeptabel, printout zu verwenden, um auf das Ergebnis eines Druckauftrags zu verweisen.
-   Verwenden Sie die Druckwarteschlange, nicht die Druckerwarteschlange.

