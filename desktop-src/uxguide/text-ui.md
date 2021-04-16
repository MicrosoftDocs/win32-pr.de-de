---
title: Text der Benutzeroberfläche
description: Der Benutzeroberflächen Text wird auf UI-Oberflächen angezeigt.
ms.assetid: db42fe22-9baf-453a-9b89-9bbb251b0b6f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 1c1a60ba0bfef33dcf1e72c5ba19b11c4a5f38a2
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104558527"
---
# <a name="user-interface-text"></a>Text der Benutzeroberfläche

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Der Benutzeroberflächen Text wird auf UI-Oberflächen angezeigt. Dieser Text umfasst Steuerelement Bezeichnungen und statischen Text:

-   Steuerelement Bezeichnungen identifizieren Steuerelemente und werden direkt in oder neben den Steuerelementen platziert.
-   Statischer Text, der so aufgerufen wird, weil er nicht Teil eines interaktiven Steuer Elements ist, bietet Benutzern Ausführliche Anweisungen oder Erläuterungen, damit Sie fundierte Entscheidungen treffen können.

**Hinweis:** Richtlinien im Zusammenhang mit [Stil und Ton](text-style-tone.md), [Schriftarten](vis-fonts.md)und [Allgemeine-Steuer](controls.md) Element Bezeichnungen werden in separaten Artikeln dargestellt.

## <a name="usage-patterns"></a>Verwendungsmuster

Der Benutzeroberflächen Text weist mehrere Verwendungs Muster auf:



|                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Text der Titelleiste**<br/> Verwenden Sie den Text der Titelleiste, um ein Fenster oder die Quelle eines Dialog Felds zu identifizieren. <br/>                                                                            | ![Screenshot der Ordneroptionen-Titelleiste](images/text-ui-image1.png)<br/> In diesem Beispiel identifiziert der Titelleisten Text ein Fenster.<br/>                                                                                                                                                                                                                                                                                                             |
| **Haupt Anleitung**<br/> Verwenden Sie die prominente Haupt Anweisung, um die Vorgehensweise im Fenster oder auf der Seite zu erläutern. <br/>                                                      | Die Anweisung sollte eine bestimmte Anweisung, eine imperative Richtung oder eine Frage sein. gute Haupt Anweisungen vermitteln das Ziel des Benutzers, anstatt sich auf die Bearbeitung der Benutzeroberfläche zu konzentrieren. <br/> ![Screenshot der Frage: möchten Sie die neueste Hilfe? ](images/text-ui-image2.png)<br/> In diesem Beispiel bindet der Haupt Anweisungs Text den Benutzer direkt mit einer Frage in Bezug auf den eigenen Vorteil oder das Interesse des Benutzers ein.<br/>             |
| **Ergänzende Anweisungen**<br/> Verwenden Sie ggf. eine ergänzende Anweisung, um zusätzliche Informationen zu präsentieren, die für das Verständnis oder die Verwendung des Fensters oder der Seite hilfreich sind. <br/> | Sie können ausführlichere Informationen bereitstellen, Kontext bereitstellen und Terminologie definieren. Ergänzende Anweisungen werden in der Main-Anweisung ausführlich erläutert, ohne dass Sie einfach neu formuliert wird. <br/> ![Screenshot des Texts beim Wechseln zum Administrator Konto ](images/text-ui-image3.png)<br/> In diesem Beispiel stellen die ergänzenden Anweisungen zwei mögliche Aktions Kurse bereit, die als Reaktion auf die in der Haupt Anweisung dargestellten Informationen ausgeführt werden.<br/> |
| **Steuerelement Bezeichnungen**<br/> Bezeichnungen direkt auf oder neben Steuerelementen. <br/>                                                                                                           | ![Screenshot der Optionen für die Desktop Uhr ](images/text-ui-image4.png)<br/> In diesem Beispiel identifizieren Steuerelement Bezeichnungen die Desktop-Takt Einstellungen, die Benutzer auswählen oder ändern können.<br/>                                                                                                                                                                                                                                                                       |
| **Ergänzende Erläuterungen**<br/> eine Ausarbeitung der Steuerelement Bezeichnungen (in der Regel für Befehls Verknüpfungen, Options Felder und Kontrollkästchen). <br/>                                    | ![Screenshot, der das Dialogfeld "Sicherheitseinstellungen" anzeigt.](images/text-ui-image5.png)<br/> In diesem Beispiel verdeutlichen die ergänzenden Erläuterungen die Auswahlmöglichkeiten.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="design-concepts"></a>Entwurfskonzepte

Software Entwickler betrachten Text häufig als Dokumentation zur Produktdokumentation und technischen Support. "Zuerst schreiben wir den Code, und dann nehmen wir eine Person an, um uns dabei zu erklären, was wir entwickelt haben." In Wirklichkeit wird jedoch wichtiger Text bereits in den Prozess geschrieben, da die Benutzeroberfläche konzipiert und programmiert ist. Dieser Text wird schließlich immer häufiger und durch mehr Personen als eventuell andere technische Schreibvorgänge erkannt.

**Verständlicher Text ist entscheidend für die effektive Benutzeroberfläche.** Professionelle Writer und Editoren sollten mit Softwareentwicklern an einem Benutzeroberflächen Text als integraler Bestandteil des Entwurfsprozesses arbeiten. Lassen Sie Sie frühzeitig an Text arbeiten, da Text Probleme häufig Entwurfs Probleme offenlegen. Wenn Ihr Team Probleme bei der Erläuterung eines Entwurfs hat, ist es oft der Entwurf, nicht die Erklärung, der verbessert werden muss.

### <a name="a-design-model-for-ui-text"></a>Ein Entwurfs Modell für den UI-Text

Berücksichtigen Sie bei der Überlegung von UI-Text und seiner Platzierung auf den Benutzeroberflächen-Oberflächen die folgenden Fakten:

-   Während der fokussierten, immersiven Lese-und Schreibvorgänge von links nach rechts, von oben nach unten (in westlichen Kulturen).
-   Bei der Verwendung von Software werden Benutzer nicht in die Benutzeroberfläche übernommen, sondern in ihrer Arbeit. Folglich lesen Benutzer den UI-Text, den Sie scannen, nicht.
-   Wenn Sie ein Fenster Scannen, werden die Benutzer möglicherweise anscheinend Text lesen, wenn Sie Sie filtern. Sie verstehen den UI-Text oft nicht wirklich, es sei denn, Sie nehmen den Bedarf an.
-   Innerhalb eines Fensters erhalten verschiedene Benutzeroberflächen Elemente unterschiedliche Ebenen der Aufmerksamkeit. Benutzer neigen dazu, die Steuerelement Bezeichnungen zuerst zu lesen, insbesondere diejenigen, die für das Abschließen der Aufgabe relevant sind. Im Gegensatz dazu neigen Benutzer eher zum Lesen von statischem Text, wenn Sie der Ansicht sind.

Nehmen Sie bei einem allgemeinen Entwurfs Modell nicht an, dass Benutzer den Text von links nach rechts, von oben nach unten in der Reihenfolge lesen. Gehen Sie stattdessen davon aus, dass der Benutzer zunächst das gesamte Fenster scannt und dann den UI-Text in ungefähr der folgenden Reihenfolge liest:

-   Interaktive Steuerelemente im Mittelpunkt
-   Die [Commit-Schalt](glossary.md) Flächen
-   Interaktive Steuerelemente gefunden an anderer Stelle
-   Main-Anweisung
-   Ergänzende Erläuterungen
-   Fenstertitel
-   Anderer statischer Text im Haupttext
-   Fußnoten

Sie sollten auch davon ausgehen, dass das Lesen und Ausführen sofort beendet wird, sobald Benutzer entschieden haben, was zu tun ist.

### <a name="eliminate-redundancy"></a>Redundanz vermeiden

Redundanter Text benötigt nicht nur wertvolle Bildschirmfläche, sondern auch die Effektivität der wichtigen Ideen oder Aktionen, die Sie zu vermitteln versuchen. Es ist auch eine Verschwendung der Zeit des Readers und umso mehr in einem Kontext, in dem die Überprüfung der Norm ist. **Windows ist bestrebt, zu erläutern, was Benutzer genau tun müssen.**

Überprüfen Sie jedes Fenster, und vermeiden Sie doppelte Wörter und Anweisungen sowohl innerhalb als auch über Steuerelemente hinweg. Vermeiden Sie, dass wichtiger Text bei Bedarf explizit ist, aber nicht redundant ist, und erläutern Sie den offensichtlichen nicht.

### <a name="avoid-over-communication"></a>Vermeiden der über Kommunikation

Auch wenn der Text nicht redundant ist, kann es einfach sein, alle Details zu erläutern. **Zu viele Text Verluste beim Lesen des Auges neigen dazu, das Recht zu überspringen, was zu weniger Kommunikation und nicht mehr führt.** Übermitteln Sie die wesentlichen Informationen in der Benutzeroberfläche. Wenn für einige Benutzer oder einige Szenarios weitere Informationen erforderlich sind, stellen Sie einen Link zu ausführlicheren [Hilfe Inhalten](winenv-help.md)bereit, oder vielleicht einen Glossar Eintrag zur Erläuterung eines Begriffs.

**Falsch:**

![Screenshot des Dialog Felds mit 6 Absätzen](images/text-ui-image6.png)

In diesem Beispiel ist zu viel Text zum einfachen Scannen vorhanden. Obwohl es nicht vom Designer beabsichtigt ist, gibt es so viel Text, den Benutzer höchstwahrscheinlich auf Weiter klicken, ohne etwas zu lesen.

Um Text zu vermeiden, der das Lesen verhindert, erstellen Sie Ihren Text, um jede Wort Zählung zu erstellen. Wenn keine subtrahieren hinzugefügt werden, verwenden Sie daher einfachen, präzisen Text.

### <a name="use-the-inverted-pyramid"></a>Verwenden der invertierten Pyramide

Academic Writing verwendet in der Regel den strukturellen Stil "Pyramid", der eine Grundlage von Fakten bildet, mit diesen Fakten arbeitet und eine Schlussfolgerung bildet, die eine Pyramiden ähnliche Struktur bildet. Im Gegensatz dazu verwenden Journalisten den Stil "invertiert Pyramid", der mit der Schlussfolgerung der grundlegenden "Take Away" beginnt, den Reader haben müssen. Anschließend werden die Leser progressiv ausführlicher ausgefüllt, die möglicherweise nur für die Überprüfung interessiert sind. Der Vorteil dieses Stils liegt darin, dass es direkt zu dem Punkt kommt und es den Lesern ermöglicht, den Lesevorgang zu jedem beliebigen Punkt zu unterbinden, der die wesentlichen Informationen versteht.

Sie sollten die invertierte Pyramidenstruktur auf den Benutzeroberflächen Text anwenden. Wenn Sie mit den wesentlichen Informationen zurechtkommen, lassen Sie die Benutzer das Lesen jederzeit abbrechen, und verwenden Sie einen Hilfelink, um den Rest der Pyramide darzustellen.

![Screenshot der Meldung zum beitreten zu einem Windows-Programm ](images/text-ui-image7.png)

In diesem Beispiel befinden sich die wesentlichen Informationen in der Abfrage des Hauptanweisungs Texts. Weitere hilfreiche Informationen finden Sie in den ergänzenden Anweisungen, und Details finden Sie durch Klicken auf einen Hilfelink.

**Wenn Sie nur fünf Dinge tun...**

1.  Arbeiten Sie früh mit Text, da Text Probleme häufig Entwurfs Probleme offenlegen.
2.  Entwerfen Sie den Text für die Überprüfung.
3.  Entfernen Sie redundante Text.
4.  Verwenden von leicht verständlichen Text nicht über die Kommunikation.
5.  Stellen Sie bei Bedarf Links zu Hilfe Inhalten bereit, um ausführlichere Informationen zu erhalten.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Entfernen Sie den redundanten Text.** Suchen Sie nach redundantem Text in Fenstertiteln, Haupt Anweisungen, ergänzenden Anweisungen, Inhalts Bereichen, Befehls Verknüpfungen und Commit-Schaltflächen. Im Allgemeinen sollten Sie voll Text in den Haupt Anweisungen und interaktiven Steuerelementen belassen und Redundanz von den anderen Orten entfernen.
-   **Vermeiden Sie große Blöcke von UI-Text.** Hierzu gehören:
    -   Segmentieren von Text in kürzere Sätze und Absätze.
    -   Stellen Sie bei Bedarf [Hilfe Links](winenv-help.md) zu nützlichen, aber nicht wichtigen Informationen bereit.
-   **Wählen Sie Objektnamen und Bezeichnungen aus, die eindeutig kommunizieren und den Inhalt des Objekts unterscheiden.** Benutzer müssen nicht ermitteln, was das Objekt wirklich bedeutet, oder wie es sich von anderen Objekten unterscheidet.

    Falsch:

    ![Screenshot der Liste unbenannter Monitore](images/text-ui-image8.png)

    Empfohlen:

    ![Screenshot der Liste mit bestimmten Netzwerkadaptern](images/text-ui-image9.png)

    Im falschen Beispiel unterscheiden sich die Objektnamen überhaupt nicht. das bessere Beispiel zeigt eine starke Differenzierung nach Produktnamen.

-   **Wenn Sie sicherstellen möchten, dass Benutzer bestimmten Text im Zusammenhang mit einer Aktion lesen, platzieren Sie ihn auf einem interaktiven Steuerelement.**
    -   **Annehmbar:**
    -   ![Screenshot der Formatierungs Warnung mit der Schaltfläche "OK" ](images/text-ui-image10.png)
    -   In diesem Beispiel besteht die Möglichkeit, dass Benutzer den Text nicht lesen, der erklärt, was Sie bestätigen.
    -   **Besserer**
    -   ![Screenshot der Schaltfläche "Formatierung warnen" und "Format" ](images/text-ui-image11.png)
    -   In diesem Beispiel können Sie sicherstellen, dass mindestens Benutzer verstehen, dass Sie im Begriff sind, einen Datenträger zu formatieren.
-   **Verwenden Sie ein Leerzeichen zwischen Sätzen.** Nicht zwei.

### <a name="text-fonts-sizes-and-colors"></a>Text Schriftarten, Größen und Farben

-   **Verwenden Sie blauen Text nur für Verknüpfungen und Haupt Anweisungen.**
-   **Verwenden Sie grünen Text nur für URLs in den Suchergebnissen.**

Die folgenden Schriftarten und Farben sind Standardwerte für Windows.



| Muster                                                                                     | Design Symbol                            | Schriftart, Farbe                                                           |
|--------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![erste Spalte: Text der Titelleiste ](images/text-ui-image12.png)<br/>              | CaptionFont<br/>      | 9 pt. schwarz ( \# 000000) Segoe UI<br/>                 |
| ![erste Spalte: Haupt Anweisungen ](images/text-ui-image13.png)<br/>           | Maininstruction<br/>  | 12 pt. blau ( \# 003399) Segoe UI<br/>                 |
| ![erste Spalte: sekundäre Anweisungen ](images/text-ui-image14.png)<br/>      | Anweisung<br/>      | 9 pt. schwarz ( \# 000000) Segoe UI<br/>                 |
| ![erste Spalte: normaler Text ](images/text-ui-image15.png)<br/>                 | BodyText<br/>         | 9 pt. schwarz ( \# 000000) Segoe UI<br/>                 |
| ![erste Spalte: hervorgehobene Text ](images/text-ui-image16.png)<br/>             | BodyText<br/>         | 9 pt. schwarz ( \# 000000) Segoe UI, Fett oder kursiv<br/> |
| ![erste Spalte: bearbeitbarer Text ](images/text-ui-image17.png)<br/>               | BodyText<br/>         | 9 pt. schwarz ( \# 000000) Segoe UI in einem Feld<br/>       |
| ![erste Spalte: deaktivierter Text ](images/text-ui-image18.png)<br/>               | Disabled<br/>         | 9 pt. dunkelgrau ( \# 323232) Segoe UI<br/>             |
| ![erste Spalte: Link ](images/text-ui-image19.png)<br/>                        | Hyperlinktext<br/>    | 9 pt. Blue ( \# 0066cc)-Segoe UI<br/>                  |
| ![erste Spalte: Links (Hover) ](images/text-ui-image20.png)<br/>               | Hot<br/>              | 9 pt. hellblau ( \# 3399ff)-Segoe UI<br/>            |
| ![erste Spalte: Gruppen Kopfzeile ](images/text-ui-image21.png)<br/>                |  <br/>                | 11 PT. blau ( \# 003399) Segoe UI<br/>                 |
| ![erste Spalte: Dateiname (in der Inhaltsansicht) ](images/text-ui-image22.png)<br/> |  <br/>                | 11 PT. schwarz ( \# 000000) Segoe UI<br/>                |
| ![erste Spalte: Dokument Text ](images/text-ui-image23.png)<br/>               | (none)<br/>           | 9 pt. schwarz ( \# 000000) Calibri<br/>                  |
| ![erste Spalte: Dokument Überschriften ](images/text-ui-image24.png)<br/>           | (none)<br/>           | 17 PT. schwarz ( \# 000000) Calibri<br/>                 |



 

Weitere Informationen und Beispiele finden Sie unter [Schriftarten](vis-fonts.md) und [Farben](vis-color.md).

### <a name="other-text-characteristics"></a>Andere Textmerkmale

**Fett**

-   **Verwenden Sie fett formatiert, um Aufmerksamkeit auf den Text zu zeichnen, den Benutzer lesen müssen.** Beispielsweise können Benutzer, die eine Liste der Optionsfeld Optionen durchsuchen, die Bezeichnungen fett formatieren, um den Text zu markieren, mit dem zusätzliche Informationen zu den einzelnen Optionen hinzugefügt werden. Beachten Sie, dass bei einer zu großen fettabnahme die Auswirkungen verringert werden.
-   **Verwenden Sie die Bezeichnung Daten fett, um hervorzuheben, was für die Daten insgesamt wichtiger ist.**
    -   Verwenden Sie bei größtenteils generischen Daten (bei denen die Daten ohne ihre Bezeichnungen, wie z. a. Ziffern oder Datumsangaben), Fett Bezeichnungen und einfache Daten, damit Benutzer die Datentypen leichter Scannen und verstehen können.
    -   Verwenden Sie für größtenteils selbsterklärende Daten einfache Bezeichnungen und Fett formatierte Daten, damit sich die Benutzer auf die Daten selbst konzentrieren können.
    -   Alternativ dazu können Sie auch dunkelgrauen Text verwenden, um weniger wichtige Informationen hervorzuheben, anstatt Fett formatierte Informationen hervorzuheben.

        ![Screenshot der Vorschau Ansicht von Windows-Explorer ](images/text-ui-image25.png)

        In diesem Beispiel werden die Bezeichnungen nicht mit fett hervorgehoben, sondern mit dunkelgrau hervorgehoben.

-   **Nicht alle Schriftarten unterstützen fett formatiert, daher sollte es niemals wichtig sein, den Text zu verstehen.**

**Kursiv**

-   Verwenden Sie, um buchstäblich auf Text zu verweisen. Verwenden Sie für diesen Zweck keine Anführungszeichen.

    **Richtig:**

    Die Begriffe Dokument und Datei werden häufig austauschbar verwendet.

-   Verwenden Sie dies für [Eingabe Aufforderungen](glossary.md) in [Textfeldern](ctrl-text-boxes.md) und [bearbeitbaren Dropdown Listen](/windows/desktop/uxguide/ctrl-drop).

    ![Screenshot des suchtextfelds ](images/text-ui-image26.png)

    In diesem Beispiel ist die Eingabeaufforderung im Suchfeld als kursiv formatierter Text formatiert.

-   Verwenden Sie sparsam, um bestimmte Wörter hervorzuheben, um das Verständnis zu unterstützen.
-   **Nicht alle Schriftarten unterstützen kursiv, daher sollte es niemals wichtig sein, den Text zu verstehen.**

**Fett kursiv**

-   Nicht in UI-Text verwenden.

**Streichen**

-   Verwenden Sie nicht, mit Ausnahme von Links.
-   Verwenden Sie für die Betonung nicht. Verwenden Sie stattdessen kursiv.

### <a name="punctuation&quot;></a>Interpunktion

**Punkte**

-   **Platzieren Sie nicht am Ende von Steuerelement Bezeichnungen, Haupt Anweisungen oder Hilfe Links.**
-   Fügen Sie am Ende der ergänzenden Anweisungen, ergänzenden Erklärungen oder anderen statischen Text ein, der einen vollständigen Satz bildet.

**Fragezeichen**

-   **Am Ende aller Fragen platzieren.** Im Gegensatz zu Zeiträume werden Fragezeichen für alle Text Typen verwendet.

**Ausrufezeichen**

-   Vermeiden Sie in Geschäftsanwendungen.
    -   **Ausnahmen:** Ausrufezeichen werden manchmal im Zusammenhang mit dem Download abgeschlossen (&quot;Done!") und für die Aufmerksamkeit auf Webinhalte ("New!") verwendet.

**Kommas**

-   Fügen Sie in einer Liste mit drei oder mehr Elementen immer ein Komma nach dem nächsten Element in der Liste ein.

**Doppelpunkte**

-   **Verwenden Sie Doppelpunkte am Ende externer Steuerelement Bezeichnungen.** Dies ist besonders wichtig für Barrierefreiheit, da einige Hilfstechnologien nach Doppelpunkten suchen, um Steuerelement Bezeichnungen zu identifizieren.
-   Verwenden Sie einen Doppelpunkt, um eine Liste von Elementen einzuführen.

**Auslassungs Punkte**

-   **Ellipsen bedeutet Vollständigkeit.** Verwenden Sie Ellipsen im Benutzeroberflächen Text wie folgt:
    -   **Befehle:** Geben Sie an, dass ein Befehl zusätzliche Informationen benötigt. Verwenden Sie immer dann keine Ellipsen, wenn eine Aktion ein anderes Fenster nur dann anzeigt, wenn zusätzliche Informationen erforderlich sind. Weitere Informationen finden Sie unter [Befehls](ctrl-command-buttons.md)Schaltflächen.
    -   **Daten:** Geben Sie an, dass der Text abgeschnitten wird.
    -   **Bezeichnungen:** Geben Sie an, dass eine Aufgabe ausgeführt wird (z. b. "suchen...").

        **Tipp:** Abgeschnittener Text in einem Fenster oder auf einer Seite mit nicht verwendetem Speicherplatz zeigt ein schlechtes Layout oder eine zu geringe Standardfenster Größe an. Bemühen Sie sich um Layouts und Standardfenster Größen, die den Umfang des abgeschnittene Texts eliminieren oder verringern. Weitere Informationen finden Sie unter [Layout](vis-layout.md).

-   **Lassen Sie Ellipsen nicht interaktiv.** Damit der abgeschnittene Text angezeigt wird, können Benutzer die Größe des Steuer Elements ändern, um mehr Text anzuzeigen oder stattdessen ein [progressives offen legungs Steuer](ctrl-progressive-disclosure-controls.md) Element zu verwenden.

**Anführungszeichen und Apostrophe**

-   Um auf Text wörtlich zu verweisen, verwenden Sie kursiv formatierte Formatierung anstelle von Anführungszeichen.
-   Legen Sie Fenstertitel und Steuerelement Bezeichnungen nur bei Bedarf in Anführungszeichen ein, um Verwechslungen zu vermeiden.
-   Für Anführungszeichen bevorzugen Sie doppelte Anführungszeichen (""); vermeiden Sie einfache Anführungszeichen.

    **Richtig:**

    Möchten Sie "Sparky es Cat Folder" Löschen?

    **Falsch:**

    Möchten Sie "Sparky es Cat Folder" Löschen?

### <a name="capitalization"></a>Großbuchstaben

-   **Verwenden Sie die Groß-/Kleinschreibung von Titeln für Titel im Satz Stil für alle anderen Benutzeroberflächen Elemente.** Dies ist für den [Windows-Ton](text-style-tone.md)besser geeignet.

    -   **Ausnahme:** Bei älteren Anwendungen können Sie bei Bedarf die Groß-/Kleinschreibung von Titeln für Befehls Schaltflächen, Menüs und Spaltenüberschriften verwenden.

        ![Screenshot des generischen Eigenschaften Blatts ](images/text-ui-image27.png)

    Dieses generische Beispiel zeigt die korrekte Groß-und Kleinschreibung für Eigenschaften Blätter.

    ![Screenshot des generischen Dialog Felds ](images/text-ui-image28.png)

    Dieses generische Beispiel zeigt die korrekte Groß-und Kleinschreibung für Dialoge.

-   **Bei Funktions-und Technologie Namen ist die Groß-und Kleinschreibung konservativ.** In der Regel sollten nur Hauptkomponenten groß geschrieben werden (mithilfe der Groß-/Kleinschreibung im Titel).

    **Richtig:**

    Analysis Services, Cubes, Dimensionen

    Analysis Services ist eine Hauptkomponente von SQL Server, daher ist die Groß-/Kleinschreibung im Titel sinnvoll. Cubes und Dimensionen sind allgemeine Elemente der Datenbankanalyse Software, daher ist es unnötig, Sie zu nutzen.

-   **Bei Funktions-und Technologie Namen muss die Groß-und Kleinschreibung einheitlich sein.** Wenn der Name mehr als einmal auf einem Bildschirm der Benutzeroberfläche angezeigt wird, sollte er immer auf dieselbe Weise angezeigt werden. Ebenso sollte der Name auf allen UI-Bildschirmen im Programm einheitlich dargestellt werden.
-   Stellen Sie die Namen generischer Benutzeroberflächen Elemente, z. b. Symbolleiste, Menü, Scrollleiste, Schaltfläche und Symbol, nicht groß.
    -   **Ausnahmen:** Adressleiste, Verknüpfungs Leiste.
-   Verwenden Sie nicht alle Großbuchstaben für Tastenkombinationen. Befolgen Sie stattdessen die Groß-/Kleinschreibung, die von Standard Tastaturen verwendet wird, oder Kleinbuchstaben, wenn der Schlüssel nicht auf der Tastatur gekennzeichnet ist.

    **Richtig:**

    Leertaste, Tab, EINGABETASTE, Seite nach oben, STRG + ALT + ENTF

    **Falsch:**

    Leertaste, Tab, EINGABETASTE, PG-Taste, STRG + ALT + ENTF

-   **Verwenden Sie für die Betonung nicht alle Großbuchstaben.** Studien haben gezeigt, dass dies schwer zu lesen ist, und Benutzer neigen dazu, Sie als "schreiende" zu betrachten. Verwenden Sie für Warnungen ein Warnsymbol und eine klar formulierte Erläuterung der Situation. Es ist nicht erforderlich, beispielsweise den Begriff "Warning" in allen Großbuchstaben hinzuzufügen.

Weitere Informationen finden Sie im Abschnitt "Text" oder "Bezeichnungen" in den spezifischen Richtlinien für die Benutzeroberflächen Komponente.

### <a name="dates-and-times"></a>Datums- und Zeitangaben

-   **Sie sollten das Format von Datums-und Uhrzeitwerten nicht hart codieren.** Beachten Sie die Auswahl der Gebiets Schema-und Anpassungsoptionen des Benutzers für das Datums-und Uhrzeit Format. Der Benutzer wählt diese im Bereich Region und Sprache der Systemsteuerung aus.

    ![Screenshot des Datums Formats: Montag, 06. Juli 2009](images/text-ui-image29.png)![Screenshot des Datums Formats: 06. Juli 2009](images/text-ui-image30.png)

    In diesen Beispielen aus Microsoft Outlook sind beide Formate für das lange Datum richtig. Sie reflektieren verschiedene Optionen, die Benutzer in der Region und in der Sprache der Systemsteuerung vorgenommen haben.

-   **Verwenden Sie das lange Datumsformat für Szenarien, die von zusätzlichen Informationen profitieren.** Verwenden Sie das kurze Datumsformat für Kontexte, die nicht über genügend Speicherplatz für das lange Format verfügen. Während Benutzer auswählen, welche Informationen in den langen und kurzen Formaten enthalten sein sollen, wählen Designer das Format aus, das in den Programmen basierend auf dem Szenario und dem Kontext angezeigt werden soll.

    ![Screenshot des Formats mit Start-und Fälligkeitsdaten](images/text-ui-image31.png)

    In diesem Beispiel unterstützt das lange Datumsformat Benutzern das Organisieren von Aufgaben und Terminen.

### <a name="globalization-and-localization"></a>Globalisierung und Lokalisierung

Globalisierung bedeutet, dass Dokumente oder Produkte erstellt werden, die in beliebigen Ländern, Regionen oder Kulturen verwendet werden können. Lokalisierung bedeutet, dass Dokumente oder Produkte zur Verwendung in einem anderen Gebiets Schema als dem Land bzw. der Ursprungsregion angepasst werden. Beim Schreiben von UI-Text sollten Sie Globalisierung und Lokalisierung in Erwägung gezogen Ihr Programm kann in andere Sprachen übersetzt und in Kulturen verwendet werden, die sich von ihren eigenen unterscheiden.

-   Wählen Sie für Steuerelemente mit variablen Inhalten (z. b. Listenansichten und Struktur Ansichten) **eine Breite aus, die für die längsten gültigen Daten geeignet ist.**
-   **Fügen Sie in der UI-Oberfläche ausreichend Speicherplatz für einen weiteren 30-prozentigen** Text (bis zu 200 Prozent für kürzerer Text) für Text (aber nicht für Zahlen) ein, der lokalisiert wird. Durch die Übersetzung von einer Sprache in eine andere wird häufig die Zeilenlänge von Text geändert.
-   Erstellen Sie keine Zeichen folgen aus Teil Zeichenfolgen zur Laufzeit. Verwenden Sie stattdessen vollständige Sätze, damit der Konvertierer keine Mehrdeutigkeit hat.
-   **Verwenden Sie kein untergeordnetes Steuerelement, die darin enthaltenen Werte oder die zugehörige Einheiten Bezeichnung, um einen Satz oder einen Ausdruck zu erstellen.** Ein solcher Entwurf ist nicht lokalisierbar, da die Satzstruktur von der Sprache abweicht.

    **Falsch:**

    ![Screenshot des Textfelds in einer Kontrollkästchen Bezeichnung ](images/text-ui-image32.png)

    **Richtig:**

    ![Screenshot des Textfelds nach der Bezeichnung eines Kontrollkästchens ](images/text-ui-image33.png)

    Im falschen Beispiel wird das Textfeld in der Bezeichnung des Kontrollkästchens platziert.

-   Machen Sie keinen Teil eines Satzes zu einem Link, denn wenn übersetzt, bleibt dieser Text möglicherweise nicht zusammen. Der Linktext sollte daher einen vollständigen Satz selbst bilden.
    -   **Ausnahme:** Glossar Links können als Teil eines Satzes Inline eingefügt werden.

Weitere Informationen finden Sie im [Go Global Developer Center](https://msdn.microsoft.com/goglobal/).

### <a name="title-bar-text"></a>Text der Titelleiste

-   Wählen Sie den Text der Titelleiste basierend auf dem Typ des Fensters aus:
    -   **Dokument zentrierte Programmfenster der obersten Ebene:** Verwenden Sie das Format "Dokumentnamen Programmname". Dokumentnamen werden zuerst angezeigt, um eine Dokument zentrierte Darstellung zu erzielen.
    -   **Programmfenster der obersten Ebene, die nicht Dokument zentriert sind:** Nur der Programmname anzeigen.
    -   **Dialog Felder:** Anzeigen des Befehls, der Funktion oder des Programms, von dem aus das Dialogfeld kam. Verwenden Sie den Titel nicht, um den Zweck des Dialog Felds zu erläutern, der den Zweck der Haupt Anweisungen ist. Weitere Richtlinien finden Sie unter [Dialog Felder](win-dialog-box.md).
    -   **Assistenten:** Zeigen Sie den Namen des Assistenten an. Beachten Sie, dass das Wort "Wizard" nicht in den Namen des Assistenten enthalten sein sollte. Weitere Richtlinien finden Sie unter [Assistenten](win-wizards.md).
-   **Wenn die Titelleisten Beschriftung und das Symbol am oberen Rand des Fensters hervorgehoben angezeigt werden, können Sie für Programmfenster der obersten Ebene die Titelleisten Beschriftung und das Symbol ausblenden, um Redundanz zu vermeiden.** Sie müssen jedoch immer noch einen passenden Titel für die Verwendung durch Windows festlegen.
-   **Schließen Sie für Dialogfelder nicht die Wörter "Dialog" oder "Fortschritt" in die Titel ein.** Diese Konzepte werden impliziert, und wenn diese Wörter deaktiviert werden, werden die Titel für Benutzer einfacher zu scannen.

### <a name="main-instructions"></a>Haupt Anleitung

-   **Verwenden Sie die main-Anweisung, um näher zu erklären, welche Benutzer in einem bestimmten Fenster oder einer bestimmten Seite vorgehen sollten.** Gute Haupt Anweisungen vermitteln das Ziel des Benutzers, anstatt sich auf die Bearbeitung der Benutzeroberfläche zu konzentrieren.
-   **Stellen Sie die main-Anweisung in Form einer imperativen Richtung oder einer bestimmten Frage dar.**

    **Falsch:**

    ![Screenshot des Programm namens als Haupt Anweisung ](images/text-ui-image34.png)

    In diesem Beispiel gibt die main-Anweisung einfach den Namen des Programms an. Er lädt nicht explizit eine Vorgehensweise für den Benutzer ein.

    **Ausnahmen:** Fehlermeldungen, Warnmeldungen und Bestätigungen können unterschiedliche Satzstrukturen in Ihren Haupt Anweisungen verwenden.

-   **Verwenden Sie nach Möglichkeit bestimmte Verben.** Bestimmte Verben (Beispiele: verbinden, speichern, installieren) sind für Benutzer aussagekräftiger als generische (Beispiele: konfigurieren, verwalten, festlegen).
    -   Wenn Sie für System Steuerungs Seiten und Assistenten Seiten kein bestimmtes Verb verwenden können, empfiehlt es sich, das Verb nicht vollständig auszulassen.

        **Annehmbar:**

        Gebiets Schema, Region und Sprache eingeben

        **Besserer**

        Gebiets Schema, Region und Sprache

    -   Lassen Sie für Dialogfelder, wie z. b. Fehlermeldungen und Warnungen, das Verb nicht weglassen.

-   Sie sind nicht verpflichtet, den Hauptanweisungs Text zu verwenden, wenn das Hinzufügen nur redundant oder offensichtlich über den Kontext der Benutzeroberfläche ist.

    ![Screenshot des Dialog Felds "Speichern unter" ](images/text-ui-image35.png)

    In diesem Beispiel ist der Kontext der Benutzeroberfläche bereits eindeutig. Es ist nicht erforderlich, den Hauptanweisungs Text hinzuzufügen.

-   **Bei der präzisen Verwendung wird nur ein einzelner, kompletter Satz verwendet.** PiST die Haupt Anweisung der wichtigen Informationen. Wenn Sie weitere Erläuterungen benötigen, sollten Sie die Verwendung einer ergänzenden Anweisung in Erwägung gezogen.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   **Schließen Sie keine abschließenden Zeiträume ein, wenn die Anweisung eine-Anweisung ist.** Wenn die Anweisung eine Frage ist, müssen Sie ein endgültiges Fragezeichen einschließen.
-   **Verwenden Sie für Fortschritts Dialogfelder einen partizipformen-Ausdruck, der den gerade ausgeführten Vorgang kurz erläutert und** mit einem Ellipsen endet. Beispiel: "Drucken Ihrer Bilder..."
-   **Tipp:** Sie können eine Haupt Anweisung auswerten, indem Sie die Vorgehensweise eines Friend-Codes vorstellen, wenn Sie erläutern, was mit dem Fenster oder der Seite geschehen soll. Wenn die Antwort mit der Main-Anweisung unnatürlich, nicht hilfreich oder umständlich ist, bearbeiten Sie die Anweisung erneut.

Weitere Informationen finden Sie im Abschnitt "Main Instruction" in den spezifischen Richtlinien für die Benutzeroberflächen Komponente.

### <a name="supplemental-instructions"></a>Ergänzende Anweisungen

-   Verwenden Sie ggf. **eine ergänzende Anweisung, um zusätzliche Informationen zu präsentieren, die hilfreich sind, um das Fenster oder die Seite zu verstehen oder zu verwenden, Beispiels** Weise:
    -   Bereitstellen von Kontext, um zu erläutern, warum das Fenster angezeigt wird, wenn es Programm oder System initiiert wird.
    -   Qualifizierende Informationen, die Benutzern bei der Entscheidung helfen, wie die Haupt Anweisung agieren soll.
    -   Definieren wichtiger Begriffe.
-   **Verwenden Sie keine ergänzende Anweisung, wenn dies nicht erforderlich ist.** Es empfiehlt sich, alles mit der Main-Anweisung zu kommunizieren, wenn Sie dies möglich machen.
-   **Wiederholen Sie die main-Anweisung nicht mit etwas anderen Formulierungen.** Lassen Sie stattdessen die ergänzende Anweisung Weg, wenn nichts mehr hinzugefügt werden muss.
-   Verwenden Sie vollständige Sätze und Groß-/Kleinschreibung im Satz.

### <a name="control-labels"></a>Steuerelement Bezeichnungen

-   **Bezeichnen Sie jedes Steuerelement oder jede Gruppe von Steuerelementen. Ausnahmen**
    -   Text Felder und Dropdown Listen können mithilfe von Eingabe Aufforderungen beschriftet werden.
    -   Progressive Offenlegungs Steuerelemente sind in der Regel nicht beschriftet.
    -   **Untergeordnete Steuerelemente verwenden die Bezeichnung Ihres zugeordneten Steuer Elements.** Dreh Steuerelemente sind immer untergeordnete Steuerelemente.
    -   **Lassen Sie Steuerelement Bezeichnungen aus, die die main-Anweisung wiedergeben.** In diesem Fall übernimmt die Haupt Anweisung den Zugriffsschlüssel.

        **Annehmbar:**

        ![Screenshot von Textfeld mit Anweisung und Bezeichnung ](images/text-ui-image36.png)

        In diesem Beispiel ist die Textfeld-Bezeichnung lediglich eine erneute Anweisung der Main-Anweisung.

        **Besserer**

        ![Bildschirm Abbildung von Textfeld nur mit Anweisung ](images/text-ui-image37.png)

        In diesem Beispiel wird die redundante Bezeichnung entfernt, sodass die Haupt Anweisung den Zugriffsschlüssel annimmt.

-   Bezeichnungs Platzierung:
    -   Ballons, Kontrollkästchen, Befehls Schaltflächen, Gruppen Felder, Links, Registerkarten und Tipps werden direkt durch das Steuerelement selbst bezeichnet.
    -   Dropdown Listen, Listenfelder, Listenansichten, Status anzeigen, Schieberegler, Textfelder und Struktur Ansichten sind oben gekennzeichnet, Links Links oder Links.
    -   Progressive Offenlegungs Steuerelemente sind in der Regel nicht beschriftet. Chevron-Schaltflächen werden rechts bezeichnet.
-   Weisen Sie mit Ausnahme von Links **einen eindeutigen Zugriffsschlüssel für jedes interaktive Steuerelement zu** . Weitere Informationen finden Sie unter [Tastatur](inter-keyboard.md).
-   **Halten Sie Bezeichnungen kurz.** Beachten Sie jedoch, dass das Hinzufügen eines Worts oder zweier zu einer Bezeichnung zur besseren Übersichtlichkeit werden kann, und die Notwendigkeit zusätzlicher Erklärungen entfällt.
-   **Bevorzugen spezifischer Bezeichnungen gegenüber generischen Bezeichnungen.** Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen.

    **Falsch:**

    ![Screenshot der Befehls Schaltfläche "OK" ](images/text-ui-image38.png)

    **Richtig:**

    ![Screenshot der Befehls Schaltfläche "veröffentlichen" ](images/text-ui-image39.png)

    Im richtigen Beispiel wird eine bestimmte Bezeichnung für die Commit-Schaltfläche verwendet.

-   **Verwenden Sie für Listen von Bezeichnungen, z** . b. Options Felder, parallele Ausdrücke, und versuchen Sie, die Länge für alle Bezeichnungen gleich zu halten.
-   **Legen Sie für Listen von Bezeichnungen den Bezeichnungs Text auf die Unterschiede zwischen den Optionen.** Wenn alle Optionen denselben einführenden Text aufweisen, verschieben Sie diesen Text in die Gruppen Bezeichnung.

    **Falsch:**

    ![Screenshot von Bezeichnungen mit doppelten ersten Ausdrücken](images/text-ui-image40.png)

    **Richtig:**

    ![Screenshot des ersten Ausdrucks, der in die Gruppen Bezeichnung verschoben wurde](images/text-ui-image41.png)

    Im richtigen Beispiel wird der identische einführende Ausdruck in die Bezeichnung verschoben, sodass sich die beiden Optionen leichter unterscheiden.

-   **Im Allgemeinen sollten Sie die positive Formulierung bevorzugen.** Verwenden Sie z. b. do anstelle of do not, und notify anstelle von nicht benachrichtigen.
    -   **Ausnahme:** Die Kontrollkästchen Bezeichnung "Diese Meldung nicht mehr anzeigen" wird häufig verwendet.
-   **Lassen Sie Anweisungs Verben aus, die für alle Steuerelemente des angegebenen Typs gelten.** Konzentrieren Sie sich stattdessen auf Bezeichnungen, die für die Steuerelemente eindeutig sind. Beispielsweise ist es nicht zu sagen, dass Benutzer in ein Textfeld-Steuerelement eingeben müssen oder dass Benutzer auf einen Link klicken müssen.

    **Falsch:**

    ![Screenshot der Bezeichnung: "Type your Name" ](images/text-ui-image42.png)

    **Richtig:**

    ![Screenshot der Bezeichnung: "Ihr Name" ](images/text-ui-image43.png)

    In den falschen Beispielen weisen die Steuerelement Bezeichnungen Anweisungs Verben auf, die für alle Steuerelemente ihres Typs gelten.

-   In einigen Fällen sind die folgenden Klammern zum Steuern von Bezeichnungen möglicherweise hilfreich:
    -   **Wenn eine Option optional ist, sollten Sie der Bezeichnung "(optional)" hinzufügen.**
    -   **Wenn eine Option dringend empfohlen wird, fügen Sie "(empfohlen)" der Bezeichnung hinzu.** Dies bedeutet, dass die Einstellung optional ist, aber trotzdem festgelegt werden sollte.
    -   **Wenn eine Option nur für fortgeschrittene Benutzer vorgesehen ist, sollten Sie der Bezeichnung "(Advanced)" hinzufügen.**
-   Sie können Einheiten (Sekunden, Verbindungen usw.) in Klammern nach der Bezeichnung angeben.

    ![Screenshot der Bezeichnung: Anfangs Größe (MB) ](images/text-ui-image44.png)

    Dieses Beispiel zeigt, dass die Maßeinheit Megabyte (MB) ist.

Weitere Informationen finden Sie im Abschnitt "Text" oder "Bezeichnungen" in den spezifischen Richtlinien für die Benutzeroberflächen Komponente.

### <a name="supplemental-explanations"></a>Ergänzende Erläuterungen

-   **Verwenden Sie ergänzende Erläuterungen, wenn Steuerelemente mehr Informationen benötigen, als von ihrer Bezeichnung übermittelt werden können.** Verwenden Sie jedoch keine ergänzende Erklärung, wenn es nicht erforderlich ist, alles mit der Steuerelement Bezeichnung zu kommunizieren, wenn Sie dies in gewisser Weise tun können. In der Regel werden ergänzende Erläuterungen mit Befehls Verknüpfungen, Options Feldern und Kontrollkästchen verwendet.
-   **Verwenden Sie bei Bedarf in den Steuerelement Bezeichnungen fett formatieren, um den Text zu über** prüfen, wenn ergänzende Erläuterungen vorhanden sind.

    ![Screenshot des Dialog Felds "Sicherheitseinstellungen" ](images/text-ui-image45.png)

    In diesem Beispiel sind die Optionsfeld Bezeichnungen fett formatiert, damit Sie leichter zu scannen sind.

-   **Das Hinzufügen einer ergänzenden Erläuterung zu einem Steuerelement in einer Gruppe bedeutet nicht, dass Sie Erklärungen für alle anderen Steuerelemente in der Gruppe angeben müssen.** Geben Sie die relevanten Informationen in der Bezeichnung an, wenn Sie Sie verwenden können, und verwenden Sie nur bei Bedarf Erklärungen. Sie haben keine ergänzenden Erklärungen, die die Bezeichnung lediglich auf Konsistenz umbenennen.

    ![Screenshot von drei Options Feldern ](images/text-ui-image46.png)

    In diesem Beispiel enthalten zwei Steuerelemente in der Gruppe ergänzende Erklärungen, das dritte jedoch nicht.

-   Wenn eine ergänzende Erklärung auf einen Befehls Link folgt, schreiben Sie den ergänzenden Text in Second Person.

    **Beispiel:** Befehls Link: Erstellen von Einstellungen für Drahtlos Netzwerke und speichern auf einem USB-Speicherstick

    Ergänzende Erläuterung: Hiermit werden Einstellungen erstellt, die Sie mit einem USB-Speicherstick an den Router übertragen können. Dies ist nur möglich, wenn Sie über einen drahtlosen Router verfügen, der die Konfiguration des USB-Flash Laufwerks

-   Verwenden Sie vollständige Sätze und endinterpunktions Zeichen.

### <a name="commit-button-labels"></a>Commit-Schaltflächen Bezeichnungen

In der folgenden Tabelle werden die gängigsten Schaltflächen Beschriftungen und deren Verwendung angezeigt.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Schaltflächen Bezeichnung</strong><br/></td>
<td><strong>Bedeutung</strong><br/></td>
<td><strong>Einsatzgebiete</strong><br/></td>
<td><strong>Zugriffsschüssel</strong><br/></td>
</tr>
<tr class="even">
<td><strong>OK</strong><br/></td>
<td><ul>
<li>In Dialogfeldern: übernehmen Sie die Änderungen, oder führen Sie die Aufgabe aus, und schließen Sie das Fenster.</li>
<li>In Besitzer Eigenschaften Fenster: wenden Sie die ausstehenden Änderungen an (die seit dem Öffnen oder letzten Anwenden des Fensters vorgenommen wurden), und schließen Sie das Fenster.</li>
<li>In Eigenschaften Fenstern im Besitz: behalten Sie die Änderungen bei, schließen Sie das Fenster, und wenden Sie die Änderungen an, wenn die Änderungen des Besitzer Fensters angewendet werden.</li>
</ul></td>
<td><ul>
<li>Verwendung mit Windows, die keine aufgabenspezifisch sind, z. b. Eigenschaften Blätter.</li>
<li>Verwenden Sie für Windows, das verwendet wird, um eine bestimmte Aufgabe auszuführen, stattdessen eine bestimmte Bezeichnung, die mit einem Verb beginnt (Beispiel: Print).</li>
<li>Verwenden Sie für Windows, in dem Benutzer keine Änderungen vornehmen können, close.</li>
</ul></td>
<td>EINGABETASTE<br/></td>
</tr>
<tr class="odd">
<td><strong>Ja/Nein</strong><br/></td>
<td>Ja ist die positive Antwort auf eine yes-oder No-Frage, während No die negative Antwort ist.<br/></td>
<td><ul>
<li>Verwenden Sie die Schaltflächen Ja und Nein, um auf Ja oder keine Fragen zu antworten. Verwenden Sie niemals OK und Abbrechen für Ja oder keine Fragen.</li>
<li>Bevorzugen spezifischer Antworten über die Schaltflächen Ja und Nein. Obwohl es keine Probleme mit der Verwendung von "Ja" und "Nein" gibt, können bestimmte Antworten schneller interpretiert werden, was zu einer effizienten Entscheidungsfindung führt.</li>
<li>Beachten Sie jedoch, dass ja und keine Antworten verwendet werden, wenn sich der Ausdruck bestimmter Antworten als lang oder umständlich erweist.</li>
<li>Verwenden Sie nicht die Schaltflächen Ja und Nein, wenn die Bedeutung der No-Antwort unklar ist. Wenn dies der Fall ist, verwenden Sie stattdessen bestimmte Antworten.</li>
<li>Ja und Nein müssen immer als Paar verwendet werden.</li>
</ul></td>
<td>Y und N<br/></td>
</tr>
<tr class="even">
<td><strong>Kündigen</strong><br/></td>
<td><ul>
<li>In Dialogfeldern: verwerfen Sie alle Änderungen oder in Bearbeitung befindlichen Aufgaben, kehren Sie zum vorherigen Zustand zurück (ohne erkennbare Nebeneffekte), und schließen Sie das Fenster.</li>
<li>In den Eigenschaften Blättern: verwerfen Sie alle ausstehenden Änderungen (seit dem Öffnen des Fensters oder dem letzten anwenden), und schließen Sie das Fenster.</li>
<li>Wechseln Sie in System Steuerungselemente: alle Änderungen verwerfen oder arbeiten in Bearbeitung, kehren Sie zum vorherigen Zustand zurück, und kehren Sie zu der Hub-Seite zurück, von der aus die Aufgabe gestartet wurde. Wenn keine solche Hub-Seite vorhanden ist, schließen Sie stattdessen das Fenstersystem Steuerungselement.</li>
</ul></td>
<td><ul>
<li>Verwenden Sie, wenn alle ausstehenden Änderungen oder Aktionen verworfen werden können und alle Nebeneffekte rückgängig gemacht werden können.</li>
<li>Für Änderungen, die nicht verworfen werden können, verwenden Sie Close. Verwenden Sie zum Beenden von Aktionen, die beendet werden können, beenden. Wenn anfänglich Änderungen oder Aktionen verworfen werden können, können Sie anfänglich Abbrechen verwenden und dann in schließen oder beenden wechseln, wenn Sie nicht rückgängig gemacht werden können.</li>
</ul></td>
<td>ESC<br/></td>
</tr>
<tr class="odd">
<td><strong>Schließen</strong><br/></td>
<td>Schließen Sie das Fenster. Änderungen oder Nebeneffekte werden nicht verworfen.<br/></td>
<td><ul>
<li>Verwenden Sie, wenn Änderungen oder Nebeneffekte nicht verworfen werden können. Verwenden Sie Close anstelle von Cancel für primäre Fenster.</li>
<li>Verwenden Sie für Windows, in dem Benutzer keine Änderungen vornehmen können.</li>
</ul></td>
<td>Alt + F4, STRG + F4<br/></td>
</tr>
<tr class="even">
<td><strong>Beenden</strong><br/></td>
<td>Beendet einen aktuell laufenden Task und schließt das Fenster. Alle in Bearbeitung befindlichen oder Nebeneffekte werden nicht verworfen.<br/></td>
<td><ul>
<li>Verwenden Sie, wenn die Arbeit in Bearbeitung und alle Nebeneffekte nicht verworfen werden können, in der Regel mit Status anzeigen oder Animationen.</li>
</ul></td>
<td>ESC<br/></td>
</tr>
<tr class="odd">
<td><strong>Anwenden</strong><br/></td>
<td>In Besitzer Eigenschaften Blätter: wenden Sie die ausstehenden Änderungen an (die seit dem Öffnen oder letzten Anwenden des Fensters vorgenommen wurden), lassen Sie das Fenster geöffnet. Auf diese Weise können Benutzer die Änderungen auswerten, bevor Sie das Eigenschaften Blatt schließen. In besitzende Eigenschaften Blätter: Verwenden Sie nicht.<br/></td>
<td><ul>
<li>Nur in Eigenschaften Blättern verwenden.</li>
<li>Geben Sie nur dann eine Apply-Schaltfläche an, wenn das Eigenschaften Blatt über Einstellungen (mindestens eine) mit Effekten verfügt, die Benutzer auf sinnvolle Weise auswerten können. Normalerweise werden Schaltflächen anwenden verwendet, wenn Einstellungen sichtbare Änderungen vornehmen. Benutzer sollten in der Lage sein, eine Änderung anzuwenden, die Änderung zu evaluieren und auf der Grundlage dieser Auswertung weitere Änderungen vorzunehmen. Wenn dies nicht der Fall ist, entfernen Sie die Schaltfläche anwenden, anstatt Sie zu deaktivieren.</li>
</ul></td>
<td>A<br/></td>
</tr>
<tr class="even">
<td><strong>Nächste</strong><br/></td>
<td>In Assistenten und mehrstufigen Aufgaben: fahren Sie mit dem nächsten Schritt fort, ohne einen Commit für die Aufgabe auszuführen.<br/></td>
<td><ul>
<li>Verwenden Sie nur in Assistenten und mehrstufigen Aufgaben, um mit dem nächsten Schritt ohne Verpflichtung fortzufahren.</li>
<li>Die Auswirkung einer Schaltfläche "weiter" kann immer rückgängig gemacht werden, indem Sie auf Zurück klicken.</li>
</ul></td>
<td>N<br/></td>
</tr>
<tr class="odd">
<td><strong>Fertig stellen</strong><br/></td>
<td>In Assistenten und mehrstufigen Aufgaben: Schließen Sie das Fenster. Wenn die Aufgabe noch nicht ausgeführt wurde, führen Sie die Aufgabe aus. Wenn diese Aufgabe bereits ausgeführt wurde, werden alle Änderungen oder Nebeneffekte nicht verworfen.<br/></td>
<td><ul>
<li>Nur in Assistenten und mehrstufigen Tasks verwenden. Die Verwendung von "Finish" wird jedoch davon abgeraten, da normalerweise eine bessere, spezifischere Commit-Schaltfläche vorliegt:
<ul>
<li>Wenn Sie auf die Schaltfläche zum Ausführen eines Commits für die Aufgabe klicken (sodass die Aufgabe noch nicht ausgeführt wurde), verwenden Sie eine bestimmte Bezeichnung, die mit einem Verb beginnt (z.b. Print, Connect, Start), das eine Antwort auf die Haupt Anweisung ist.</li>
<li>Wenn die Aufgabe bereits im Assistenten ausgeführt wurde, verwenden Sie stattdessen close.</li>
</ul></li>
<li>Sie können jedoch Fertigstellen verwenden, wenn:
<ul>
<li>Die jeweilige Bezeichnung ist weiterhin generisch, wie z. b. speichern, auswählen, auswählen oder Get.</li>
<li>Die Aufgabe umfasst das Ändern einer Einstellung oder einer Sammlung von Einstellungen.</li>
</ul></li>
</ul></td>
<td>EINGABETASTE<br/></td>
</tr>
<tr class="even">
<td><strong>Fertig</strong><br/></td>
<td>Nicht zutreffend<br/></td>
<td><ul>
<li>Verwenden Sie nicht. Dies ist der Fall, wenn ein Befehl falsch ist.</li>
</ul></td>
<td>Nicht zutreffend<br/></td>
</tr>
</tbody>
</table>



 

