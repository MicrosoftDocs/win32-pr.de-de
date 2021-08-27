---
title: Benutzeroberfläche Text
description: Erfahren Sie mehr über den Text der Benutzeroberfläche, der auf Benutzeroberflächenoberflächen angezeigt wird.
ms.assetid: db42fe22-9baf-453a-9b89-9bbb251b0b6f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b24b6fd105c89484e1ef935141acfa91ef5b2b39
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481196"
---
# <a name="user-interface-text"></a>Benutzeroberfläche Text

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Benutzeroberflächentext wird auf Benutzeroberflächenoberflächen angezeigt. Dieser Text enthält Steuerelementbezeichnungen und statischen Text:

-   Steuerelementbezeichnungen identifizieren Steuerelemente und werden direkt auf oder neben den Steuerelementen platziert.
-   Statischer Text, der so genannt wird, da er nicht Teil eines interaktiven Steuerelements ist, bietet Benutzern detaillierte Anweisungen oder Erklärungen, damit sie fundierte Entscheidungen treffen können.

**Hinweis:** Richtlinien im Zusammenhang [mit Stil und Ton,](text-style-tone.md) [Schriftarten](vis-fonts.md)und [Comon-Steuerelementbezeichnungen](controls.md) werden in separaten Artikeln vorgestellt.

## <a name="usage-patterns"></a>Verwendungsmuster

Benutzeroberflächentext verfügt über mehrere Verwendungsmuster:



|   Verwendung                                                                                                                                                                                          |    BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Titelleistentext**<br/> Verwenden Sie Titelleistentext, um ein Fenster oder die Quelle eines Dialogfelds zu identifizieren. <br/>                                                                            | ![Screenshot der Titelleiste der Ordneroptionen](images/text-ui-image1.png)<br/> In diesem Beispiel identifiziert der Titelleistentext ein Fenster.<br/>                                                                                                                                                                                                                                                                                                             |
| **Hauptanweisungen**<br/> Verwenden Sie die prominente Hauptanweisung, um kurz zu erläutern, was im Fenster oder auf der Seite zu tun ist. <br/>                                                      | Die Anweisung sollte eine bestimmte Anweisung, imperative Richtung oder Frage sein. gute Hauptanweisungen kommunizieren das Ziel des Benutzers, anstatt sich nur auf die Bearbeitung der Benutzeroberfläche zu konzentrieren. <br/> ![Screenshot der Frage: Möchten Sie die neueste Hilfe? ](images/text-ui-image2.png)<br/> In diesem Beispiel bespricht der Hauptanweisungstext den Benutzer direkt mit einer Frage in Bezug auf den eigenen Vorteil oder das Interesse des Benutzers.<br/>             |
| **Zusätzliche Anweisungen**<br/> Verwenden Sie bei Bedarf eine zusätzliche Anweisung, um zusätzliche Informationen anzuzeigen, die für das Verständnis oder die Verwendung des Fensters oder der Seite hilfreich sind. <br/> | Sie können ausführlichere Informationen bereitstellen, Kontext bereitstellen und Terminologie definieren. Ergänzende Anweisungen werden auf die Hauptanweisung näher erläutert, ohne sie einfach neu zu formuliert. <br/> ![Screenshot des Texts beim Wechseln zum Administratorkonto ](images/text-ui-image3.png)<br/> In diesem Beispiel bieten die ergänzenden Anweisungen zwei mögliche Aktionskurse, die als Reaktion auf die in der Hauptanweisung dargestellten Informationen verwendet werden können.<br/> |
| **Steuerelementbezeichnungen**<br/> Bezeichnungen direkt auf oder neben Steuerelementen. <br/>                                                                                                           | ![Screenshot der Desktopuhroptionen ](images/text-ui-image4.png)<br/> In diesem Beispiel identifizieren Steuerelementbezeichnungen Desktopuhreinstellungen, die Benutzer auswählen oder ändern können.<br/>                                                                                                                                                                                                                                                                       |
| **Ergänzende Erläuterungen**<br/> eine Leiste der Steuerelementbezeichnungen (in der Regel für Befehlslinks, Optionsfelder und Kontrollkästchen). <br/>                                    | ![Screenshot: Dialogfeld "Sicherheitseinstellungen"](images/text-ui-image5.png)<br/> In diesem Beispiel verdeutlichen die ergänzenden Erklärungen die Auswahlmöglichkeiten.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="design-concepts"></a>Entwurfskonzepte

Softwareentwickler stellen sich Text häufig als delegiert an die Produktdokumentation und den technischen Support vor. "Zuerst schreiben wir den Code, und dann stellen wir einen Mitarbeiter ein, der uns hilft zu erklären, was wir entwickelt haben." In Wirklichkeit wird wichtiger Text jedoch früher im Prozess geschrieben, da die Benutzeroberfläche neu geschrieben und codiert wird. Dieser Text wird immerhin häufiger und von mehr Personen als vielleicht jede andere Art von technischem Schreiben gesehen.

**Verständlicher Text ist entscheidend für eine effektive Benutzeroberfläche.** Professional und Editoren sollten mit Softwareentwicklern an Benutzeroberflächentext als integralen Bestandteil des Entwurfsprozesses arbeiten. Lassen Sie sie frühzeitig an Text arbeiten, da Textprobleme häufig Designprobleme aufschlussweise. Wenn Ihr Team Probleme beim Erläutern eines Entwurfs hat, ist es häufig der Entwurf und nicht die Erklärung, der verbessert werden muss.

### <a name="a-design-model-for-ui-text"></a>Ein Entwurfsmodell für Benutzeroberflächentext

Berücksichtigen Sie beim Betrachten von Benutzeroberflächentext und seiner Platzierung auf Den Benutzeroberflächenoberflächen folgende Fakten:

-   Während des fokussierten, immersiven Lesens lesen Die Menschen in der Reihenfolge von links nach rechts, von oben nach unten (in den Kulturen des Westens).
-   Wenn Sie Software verwenden, werden Benutzer nicht in der Benutzeroberfläche selbst, sondern in ihrer Arbeit versunken. Daher lesen Benutzer keinen Benutzeroberflächentext, den sie scannen.
-   Beim Scannen eines Fensters scheinen Benutzer Text zu lesen, wenn sie ihn in Wirklichkeit filtern. Sie verstehen den Benutzeroberflächentext häufig nur dann wirklich, wenn sie dies für notwendig halten.
-   Innerhalb eines Fensters erhalten verschiedene Benutzeroberflächenelemente unterschiedliche Aufmerksamkeitsebenen. Benutzer tendieren dazu, Steuerelementbezeichnungen zuerst zu lesen, insbesondere solche, die für die Durchführung der jeweiligen Aufgabe relevant erscheinen. Im Gegensatz dazu tendieren Benutzer dazu, statischen Text nur zu lesen, wenn sie der Meinung sind, dass sie dies benötigen.

Gehen Sie bei einem allgemeinen Entwurfsmodell nicht davon aus, dass Benutzer den Text von links nach rechts von oben nach unten sorgfältig lesen. Gehen Sie vielmehr davon aus, dass Benutzer zunächst schnell das gesamte Fenster scannen und dann den Text der Benutzeroberfläche in ungefähr der folgenden Reihenfolge lesen:

-   Interaktive Steuerelemente in der Mitte
-   Die [Commitschaltflächen](glossary.md)
-   Interaktive Steuerelemente an anderer Stelle gefunden
-   Main-Anweisung
-   Ergänzende Erläuterungen
-   Fenstertitel
-   Anderer statischer Text im Haupttext
-   Fußnoten

Sie sollten auch davon ausgehen, dass Benutzer sofort das Lesen und Tun beenden, sobald sie sich entschieden haben, was sie tun sollen.

### <a name="eliminate-redundancy"></a>Beseitigen von Redundanz

Redundanter Text benötigt nicht nur wertvollen Platz auf dem Bildschirm, sondern schwächt auch die Effektivität wichtiger Ideen oder Aktionen, die Sie vermitteln möchten. Es ist auch eine Verschwendung der Zeit des Lesers, und dies gilt vor allem in einem Kontext, in dem das Scannen die Norm ist. **Windows zielte darauf ab, zu erklären, was Benutzer einmal gut und präzise tun müssen.**

Überprüfen Sie jedes Fenster, und vermeiden Sie doppelte Wörter und Anweisungen, sowohl innerhalb als auch über Steuerelemente hinweg. Vermeiden Sie nicht, dass wichtiger Text immer dann explizit ist, wenn dies notwendig ist, aber nicht redundant ist, und erläutern Sie das Offensichtliche nicht.

### <a name="avoid-over-communication"></a>Vermeiden von Überkommunikation

Auch wenn Text nicht redundant ist, kann es einfach zu wortig sein, um jedes Detail zu erklären. **Zu viel Text rät davon ab, das Auge zu lesen, tendiert dazu, ihn ironisch direkt zu überspringen, was zu weniger Kommunikation statt zu mehr führt.** Kommunizieren Sie im Text der Benutzeroberfläche die wesentlichen Informationen präzise. Wenn für einige Benutzer oder szenarien weitere Informationen erforderlich [](winenv-help.md)sind, stellen Sie einen Link zu ausführlicheren Hilfeinhalten oder möglicherweise zu einem Glossareintrag zur Erläuterung eines Begriffs zur Verfügung.

**Falsch:**

![Screenshot des Dialogfelds mit 6 Absätzen](images/text-ui-image6.png)

In diesem Beispiel ist zu viel Text für die einfache Überprüfung enthalten. Obwohl dies vom Designer nicht beabsichtigt ist, gibt es so viel Text, dass Benutzer wahrscheinlich auf Weiter klicken, ohne etwas zu lesen.

Um Text zu vermeiden, der vom Lesen abraten soll, erstellen Sie Ihren Text, um jedes Wort zu zählen. Was keine Subtrakte hinzufüge, verwende also einfachen, präzisen Text.

### <a name="use-the-inverted-pyramid"></a>Verwenden der umgekehrten Pyramid

Die akademische Schrift verwendet in der Regel einen strukturellen Pyramidenstil, der eine Grundlage von Fakten bildet, mit diesen Fakten arbeitet und bis zu einer Schlussfolgerung aufbaut, die eine pyramidenförmige Struktur bildet. Im Gegensatz dazu verwenden Leser einen "invertierten Pyramidenstil", der mit der Schlussfolgerung beginnt, die für Leser von grundlegender Bedeutung ist. Anschließend werden zunehmend mehr Details für leserische Überprüfungen verwendet, die möglicherweise nur für die Überprüfung von Interesse sind. Der Vorteil dieses Stils ist, dass er direkt auf den Punkt kommt und es Lesern ermöglicht, das Lesen an jedem beliebigen Punkt zu beenden und dennoch die wesentlichen Informationen zu verstehen.

Sie sollten die umgekehrte Pyramidenstruktur auf Benutzeroberflächentext anwenden. Machen Sie sich mit den grundlegenden Informationen auf den Punkt vor, lassen Sie Benutzer das Lesen jederzeit beenden, und verwenden Sie einen Hilfelink, um den Rest der Pyramide zu präsentieren.

![Screenshot der Meldung zum Beitreten zum Windows-Programm ](images/text-ui-image7.png)

In diesem Beispiel sind die wesentlichen Informationen in der Abfrage des Hauptanweisungstexts enthalten, zusätzliche hilfreiche Informationen finden Sie in den zusätzlichen Anweisungen, und Details sind verfügbar, indem Sie auf einen Hilfelink klicken.

**Wenn Sie nur fünf Dinge tun...**

1.  Arbeiten Sie frühzeitig an Text, da Textprobleme häufig Designprobleme aufschlussweise.
2.  Entwerfen Sie Ihren Text für die Überprüfung.
3.  Beseitigen Sie redundanten Text.
4.  Leicht verständlichen Text verwenden; nicht über die Kommunikation.
5.  Geben Sie bei Bedarf Links zu Hilfeinhalten an, um ausführlichere Informationen zu erhalten.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Entfernen Sie redundanten Text.** Suchen Sie in Fenstertiteln, Hauptanweisungen, zusätzlichen Anweisungen, Inhaltbereichen, Befehlslinks und Commitschaltflächen nach redundanten Text. Lassen Sie im Allgemeinen den vollständigen Text in den Hauptanweisungen und interaktiven Steuerelementen, und entfernen Sie alle Redundanzen von den anderen Stellen.
-   **Vermeiden Sie große Blöcke von Benutzeroberflächentext.** Dies kann u. a. wie im folgenden Beispiel erfolgen:
    -   Segmentieren von Text in kürzere Sätze und Absätze.
    -   Stellen Sie bei Bedarf [Hilfelinks](winenv-help.md) zu nützlichen, aber nicht wesentlichen Informationen bereit.
-   **Wählen Sie Objektnamen und Bezeichnungen aus, die eindeutig kommunizieren und unterscheiden, was das Objekt tut.** Benutzer sollten nicht herausfinden müssen, was das Objekt wirklich bedeutet oder wie es sich von anderen Objekten unterscheidet.

    Falsch:

    ![Screenshot der Liste unbenannter Monitore](images/text-ui-image8.png)

    Empfohlen:

    ![Screenshot der Liste mit bestimmten Netzwerkadaptern](images/text-ui-image9.png)

    Im falschen Beispiel werden die Objektnamen überhaupt nicht unterschieden. das bessere Beispiel zeigt eine starke Unterscheidung nach Produktnamen.

-   **Wenn Sie sicherstellen möchten, dass Benutzer bestimmten Text im Zusammenhang mit einer Aktion lesen, platzieren Sie ihn in einem interaktiven Steuerelement.**
    -   **Annehmbar:**
    -   ![Screenshot der Formatierungswarnung mithilfe der Schaltfläche "OK" ](images/text-ui-image10.png)
    -   In diesem Beispiel besteht die Möglichkeit, dass Benutzer den Text nicht lesen, der erklärt, was sie bestätigen.
    -   **Besser:**
    -   ![Screenshot der Formatierungswarnung und der Formatschaltfläche ](images/text-ui-image11.png)
    -   In diesem Beispiel können Sie sicherstellen, dass benutzer zumindest verstehen, dass sie einen Datenträger formatieren werden.
-   **Verwenden Sie ein Leerzeichen zwischen Sätzen.** Nicht zwei.

### <a name="text-fonts-sizes-and-colors"></a>Textschriftarten, -größen und -farben

-   **Verwenden Sie blauen Text nur für Links und Hauptanweisungen.**
-   **Verwenden Sie grünen Text nur für URLs in Suchergebnissen.**

Die folgenden Schriftarten und Farben sind Standardeinstellungen für Windows.



| Muster                                                                                     | Designsymbol                            | Schriftart, Farbe                                                           |
|--------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![erste Spalte: Titelleistentext ](images/text-ui-image12.png)<br/>              | CaptionFont<br/>      | 9 pt. black ( \# 000000) Segoe UI<br/>                 |
| ![erste Spalte: Hauptanweisungen ](images/text-ui-image13.png)<br/>           | MainInstruction<br/>  | 12 pt. blue \# (003399) Segoe UI<br/>                 |
| ![erste Spalte: sekundäre Anweisungen ](images/text-ui-image14.png)<br/>      | Anweisung<br/>      | 9 pt. black ( \# 000000) Segoe UI<br/>                 |
| ![erste Spalte: normaler Text ](images/text-ui-image15.png)<br/>                 | BodyText<br/>         | 9 pt. black ( \# 000000) Segoe UI<br/>                 |
| ![erste Spalte: hervorgehobener Text ](images/text-ui-image16.png)<br/>             | BodyText<br/>         | 9 pt. black ( \# 000000) Segoe UI, fett oder kursiv<br/> |
| ![erste Spalte: bearbeitbarer Text ](images/text-ui-image17.png)<br/>               | BodyText<br/>         | 9 pt. black ( \# 000000) Segoe UI, in einem Feld<br/>       |
| ![erste Spalte: Deaktivierter Text ](images/text-ui-image18.png)<br/>               | Disabled<br/>         | 9 pt. dunkelgrau \# (323232) Segoe UI<br/>             |
| ![erste Spalte: link ](images/text-ui-image19.png)<br/>                        | HyperLinkText<br/>    | 9 pt. blue ( \# 0066CC) Segoe UI<br/>                  |
| ![erste Spalte: Links (Zeigen) ](images/text-ui-image20.png)<br/>               | Hot<br/>              | 9 pt. hellblau ( \# 3399FF) Segoe UI<br/>            |
| ![erste Spalte: Gruppenheader ](images/text-ui-image21.png)<br/>                |  <br/>                | 11 pt. blue \# (003399) Segoe UI<br/>                 |
| ![erste Spalte: Dateiname (in der Inhaltsansicht) ](images/text-ui-image22.png)<br/> |  <br/>                | 11 pt. black ( \# 000000) Segoe UI<br/>                |
| ![Erste Spalte: Dokumenttext ](images/text-ui-image23.png)<br/>               | (none)<br/>           | 9 pt. black ( \# 0000000) Calibri<br/>                  |
| ![erste Spalte: Dokumentüberschriften ](images/text-ui-image24.png)<br/>           | (none)<br/>           | 17 pt. black ( \# 0000000) Calibri<br/>                 |



 

Weitere Informationen und Beispiele finden Sie unter [Schriftarten](vis-fonts.md) und [Farben.](vis-color.md)

### <a name="other-text-characteristics"></a>Andere Textmerkmale

**Fett**

-   **Verwenden Sie fett, um die Aufmerksamkeit auf Text zu lenken, den Benutzer lesen müssen.** Beispielsweise können Benutzer, die eine Liste von Optionsfeldern scannen, die Bezeichnungen fett dargestellt sehen, um sich von Text abzuheben, der zusätzliche Informationen zu den einzelnen Optionen hinzufügt. Beachten Sie, dass die Verwendung von zu viel Fett die Auswirkungen verringert.
-   **Verwenden Sie bei beschrifteten Daten fett, um zu verdeutlichen, was für die Daten als Ganzes wichtiger ist.**
    -   Verwenden Sie für größtenteils generische Daten (bei denen die Daten ohne ihre Bezeichnungen wenig Bedeutung haben, wie bei Ziffern oder Datumsangaben) fett formatierte Bezeichnungen und einfache Daten, damit Benutzer die Datentypen einfacher überprüfen und verstehen können.
    -   Verwenden Sie für größtenteils selbsterklärende Daten einfache Bezeichnungen und fett formatierte Daten, damit benutzer sich auf die Daten selbst konzentrieren können.
    -   Alternativ können Sie dunkelgrauen Text verwenden, um weniger wichtige Informationen hervorzuheben, anstatt fett zu verwenden, um die wichtigeren Informationen hervorzuheben.

        ![Screenshot der Miniaturansicht des Windows-Explorers ](images/text-ui-image25.png)

        In diesem Beispiel werden die Bezeichnungen nicht fett hervorgehoben, sondern mithilfe von Dunkelgrau hervorgehoben.

-   **Nicht alle Schriftarten unterstützen Fettdruck, daher sollte es nie entscheidend sein, den Text zu verstehen.**

**Kursiv**

-   Verwenden Sie , um auf Text zu verweisen. Verwenden Sie für diesen Zweck keine Anführungszeichen.

    **Richtig:**

    Die Begriffe Dokument und Datei werden häufig austauschbar verwendet.

-   Verwenden Sie [für Eingabeaufforderungen](glossary.md) in [Textfeldern](ctrl-text-boxes.md) und [bearbeitbaren Dropdownlisten.](/windows/desktop/uxguide/ctrl-drop)

    ![Screenshot des Suchtextfelds ](images/text-ui-image26.png)

    In diesem Beispiel wird die Eingabeaufforderung im Suchfeld als italischer Text formatiert.

-   Verwenden Sie nur wenig, um bestimmte Wörter zu hervorheben, um beim Verständnis zu helfen.
-   **Nicht alle Schriftarten unterstützen italisch, daher sollte es nie entscheidend sein, den Text zu verstehen.**

**Fett italisch**

-   Verwenden Sie nicht im Benutzeroberflächentext.

**Underline**

-   Verwenden Sie nicht, mit Ausnahme von Links.
-   Verwenden Sie nicht zur Hervorhebung. Verwenden Sie stattdessen italisch.

### <a name="punctuation&quot;></a>Interpunktion

**Zeiten**

-   **Platzieren Sie nicht am Ende von Steuerelementbezeichnungen, Hauptanweisungen oder Hilfelinks.**
-   Platzieren Sie am Ende ergänzender Anweisungen, ergänzender Erklärungen oder eines beliebigen anderen statischen Texts, der einen vollständigen Satz bildet.

**Fragezeichen**

-   **Platzieren Sie am Ende aller Fragen.** Im Gegensatz zu Zeiträumen werden Fragezeichen für alle Texttypen verwendet.

**Ausrufezeichen**

-   Vermeiden Sie es in Geschäftsanwendungen.
    -   **Ausnahmen:** Ausrufezeichen werden manchmal im Kontext des Downloadabschlusses (&quot;Fertig!") verwendet, um auf Webinhalte ("Neu!" zu achten).

**Kommas**

-   Setzen Sie in einer Liste mit drei oder mehr Elementen immer ein Komma nach dem vorletzten Element in der Liste.

**Doppelpunkte**

-   **Verwenden Sie Doppelpunkte am Ende externer Steuerelementbezeichnungen.** Dies ist besonders wichtig für die Barrierefreiheit, da einige Hilfstechnologien nach Doppelpunkt suchen, um Steuerelementbezeichnungen zu identifizieren.
-   Verwenden Sie einen Doppelpunkt, um eine Liste von Elementen einzuführen.

**Ellipsen**

-   **Ellipsen bedeuten Vollständigkeit.** Verwenden Sie Ellipsen im Benutzeroberflächentext wie folgt:
    -   **Befehle:** Geben Sie an, dass ein Befehl zusätzliche Informationen benötigt. Verwenden Sie keine Auslassungsellipse, wenn eine Aktion nur dann ein anderes Fenster anzeigt, wenn zusätzliche Informationen erforderlich sind. Weitere Informationen finden Sie unter [Befehlsschaltflächen.](ctrl-command-buttons.md)
    -   **Daten:** Geben Sie an, dass Text abgeschnitten wird.
    -   **Bezeichnungen:** Geben Sie an, dass eine Aufgabe in Bearbeitung ist (z. B. "Suchen...").

        **Tipp:** Abgeschnittener Text in einem Fenster oder einer Seite mit nicht verwendetem Platz weist auf ein schlechtes Layout oder eine zu kleine Standardfenstergröße hin. Arbeiten Sie nach Layouts und Standardfenstergrößen, die die Menge abgeschnittenen Texts beseitigen oder reduzieren. Weitere Informationen finden Sie unter [Layout](vis-layout.md).

-   **Machen Sie Ellipsen nicht interaktiv.** Um abgeschnittenen Text zu zeigen, können Benutzer die Größe des Steuerelements ändern, um mehr Text zu sehen, oder stattdessen ein [progressives Offenlegungssteuerfeld](ctrl-progressive-disclosure-controls.md) verwenden.

**Anführungszeichen und Apostrophe**

-   Um auf Text zu verweisen, verwenden Sie kursale Formatierung anstelle von Anführungszeichen.
-   Setzen Sie Fenstertitel und Steuerelementbezeichnungen nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden, und Sie können nicht stattdessen fett formatieren.
-   Bei Anführungszeichen werden doppelte Anführungszeichen bevorzugt (" "); Vermeiden Sie einfache Anführungszeichen.

    **Richtig:**

    Möchten Sie "Sparkys Cat-Ordner" wirklich löschen?

    **Falsch:**

    Möchten Sie sicher sein, dass Sie den Ordner "Sparky es cat" löschen möchten?

### <a name="capitalization"></a>Großbuchstaben

-   **Verwenden Sie Die Groß-/Groß-/Format für alle anderen Benutzeroberflächenelemente.** Dies ist für den Windows [besser geeignet.](text-style-tone.md)

    -   **Ausnahme:** Bei älteren Anwendungen können Sie bei Bedarf Die Groß-/Großschrift für Befehlsschaltflächen, Menüs und Spaltenüberschriften verwenden, um das Mischen von Groß-/Groß-/Formatvorlagen zu vermeiden.

        ![Screenshot des generischen Eigenschaftenblatts ](images/text-ui-image27.png)

    Dieses generische Beispiel zeigt die richtige Groß- und Interpunktion für Eigenschaftenblätter.

    ![Screenshot des generischen Dialogfelds ](images/text-ui-image28.png)

    Dieses generische Beispiel zeigt die richtige Groß- und Interpunktion für Dialoge.

-   **Bei Funktions- und Technologienamen sollten Sie bei der Groß-//A-Groß-/A-Groß-/A-Synchronisierung konservativ sein.** In der Regel sollten nur Hauptkomponenten großformatiert werden (mithilfe der Groß-/Groß-/Formatvorlage).

    **Richtig:**

    Analysis Services, Cubes, Dimensionen

    Analysis Services ist eine Hauptkomponente der SQL Server, sodass die Groß-/SQL Server im Titelstil geeignet ist. Cubes und Dimensionen sind allgemeine Elemente der Datenbankanalysesoftware, daher ist es nicht erforderlich, sie groß zu formatieren.

-   **Bei Feature- und Technologienamen sollten Sie bei der Groß-/A-Groß-/Groß-/Weise konsistent sein.** Wenn der Name auf einem Bildschirm auf der Benutzeroberfläche mehr als einmal angezeigt wird, sollte er immer auf die gleiche Weise angezeigt werden. Ebenso sollte der Name auf allen Bildschirmen der Benutzeroberfläche im Programm konsistent dargestellt werden.
-   Lassen Sie die Namen generischer Benutzeroberflächenelemente groß, z. B. Symbolleiste, Menü, Scrollleiste, Schaltfläche und Symbol.
    -   **Ausnahmen:** Adressleiste, Linksleiste.
-   Verwenden Sie nicht alle Großbuchstaben für Tastaturtasten. Befolgen Sie stattdessen die Groß-/Kleinschreibung, die von Standardtastaturen verwendet wird, oder Kleinbuchstaben, wenn die Taste nicht auf der Tastatur beschriftet ist.

    **Richtig:**

    LEERZEICHENTASTE, TAB, EINGABETASTE, SEITE NACH OBEN, STRG+ALT+ENTF

    **Falsch:**

    SPACEBAR, TAB, ENTER, PG UP, STRG+ALT+ENTF

-   **Verwenden Sie nicht alle Großbuchstaben für die Hervorhebung.** Studien haben ergeben, dass dies schwer zu lesen ist, und Benutzer betrachten dies in der Regel als "besingend". Verwenden Sie für Warnungen ein Warnsymbol und eine klar definierte Erklärung der Situation. Es ist nicht notwendig, z. B. den Begriff WARNING in allen Großbuchstaben hinzuzufügen.

Weitere Informationen finden Sie im Abschnitt "Text" oder "Bezeichnungen" in den spezifischen Richtlinien für Benutzeroberflächenkomponenten.

### <a name="dates-and-times"></a>Datums- und Zeitangaben

-   **Codieren Sie das Format von Datums- und Zeitangaben nicht hart.** Achten Sie auf die Auswahl des Lokalen und der Anpassungsoptionen des Benutzers für die Datums- und Uhrzeitformate. Der Benutzer wählt diese im Systemsteuerungselement Region und Sprache aus.

    ![Screenshot des Datumsformats: Montag, 6. Juli 2009](images/text-ui-image29.png)![Screenshot des Datumsformats: 06. Juli 2009](images/text-ui-image30.png)

    In diesen Beispielen von Microsoft Outlook sind beide Formate für das lange Datum richtig. Sie spiegeln verschiedene Auswahlmöglichkeiten wider, die Benutzer im Systemsteuerungselement Region und Sprache getroffen haben.

-   **Verwenden Sie das lange Datumsformat für Szenarien, die von zusätzlichen Informationen profitieren.** Verwenden Sie das kurze Datumsformat für Kontexte, die nicht über genügend Platz für das lange Format verfügen. Während Benutzer auswählen, welche Informationen sie in die langen und kurzen Formate einplanen möchten, wählen Designer basierend auf dem Szenario und dem Kontext aus, welches Format in ihren Programmen angezeigt werden soll.

    ![Screenshot des Formats mit Start- und Fälligkeitsdaten](images/text-ui-image31.png)

    In diesem Beispiel hilft das lange Datumsformat Benutzern bei der Organisation von Aufgaben und Stichtagen.

### <a name="globalization-and-localization"></a>Globalisierung und Lokalisierung

Globalisierung bedeutet, Dokumente oder Produkte zu erstellen, die in jedem Land, jeder Region oder Kultur verwendet werden können. Lokalisierung bedeutet, Dokumente oder Produkte für die Verwendung in einem anderen Als dem Ursprungsland/der Ursprungsregion anzupassen. Berücksichtigen Sie beim Schreiben von Benutzeroberflächentext die Globalisierung und Lokalisierung. Ihr Programm kann in andere Sprachen übersetzt und in Kulturen verwendet werden, die sich stark von Ihren eigenen unterscheiden.

-   Wählen Sie für Steuerelemente mit variablen Inhalten (z. B. Listenansichten und Strukturansichten) eine Breite aus, die für **die längsten gültigen Daten geeignet ist.**
-   Fügen Sie auf der Benutzeroberflächenoberfläche genügend Platz für zusätzliche **30** Prozent (bis zu 200 Prozent für kürzeren Text) für jeden Text (aber keine Zahlen) ein, der lokalisiert wird. Die Übersetzung von einer Sprache in eine andere ändert häufig die Zeilenlänge des Texts.
-   Erstellen Sie zur Laufzeit keine Zeichenfolgen aus Teilzeichenfolgen. Verwenden Sie stattdessen vollständige Sätze, damit der Translator nicht mehrdeutig ist.
-   **Verwenden Sie kein untergeordnetes Steuerelement, die darin enthaltenen Werte oder seine Einheitenbezeichnung, um einen Satz oder Ausdruck zu erstellen.** Ein solcher Entwurf ist nicht lokalisierbar, da die Satzstruktur je nach Sprache variiert.

    **Falsch:**

    ![Screenshot des Textfelds innerhalb einer Kontrollkästchenbezeichnung ](images/text-ui-image32.png)

    **Richtig:**

    ![Screenshot des Textfelds nach einer Kontrollkästchenbezeichnung ](images/text-ui-image33.png)

    Im falschen Beispiel wird das Textfeld innerhalb der Kontrollkästchenbezeichnung platziert.

-   Machen Sie nicht nur einen Teil eines Satzes zu einem Link, da dieser Text bei der Übersetzung möglicherweise nicht zusammen bleibt. Linktext sollte daher selbst einen vollständigen Satz bilden.
    -   **Ausnahme:** Glossarlinks können als Teil eines Satzes inline eingefügt werden.

Weitere Informationen finden Sie im [Go Global Developer Center.](https://msdn.microsoft.com/goglobal/)

### <a name="title-bar-text"></a>Titelleistentext

-   Wählen Sie den Titelleistentext basierend auf dem Typ des Fensters aus:
    -   Dokumentorientierte Programmfenster der **obersten Ebene:** Verwenden Sie das Format "Programmname des Dokumentnamens". Dokumentnamen werden zuerst angezeigt, um ein dokumentzentriertes Gefühl zu vermitteln.
    -   **Programmfenster der obersten Ebene, die nicht dokumentzentrierend sind:** Zeigt nur den Programmnamen an.
    -   **Dialogfelder:** Zeigt den Befehl, das Feature oder das Programm an, von dem das Dialogfeld stammt. Verwenden Sie den Titel nicht, um den Zweck des Dialogfelds zu erläutern, der dem Zweck der Hauptanweisungen entspricht. Weitere Richtlinien finden Sie unter [Dialogfelder](win-dialog-box.md).
    -   **Assistenten:** Zeigt den Namen des Assistenten an. Beachten Sie, dass das Wort "Assistent" nicht in Assistentennamen enthalten sein sollte. Weitere Richtlinien finden Sie unter [Assistenten](win-wizards.md).
-   **Wenn die Titelleistenbeschriftung und das Symbol für Programmfenster der obersten Ebene am oberen Rand des Fensters hervorgehoben angezeigt werden, können Sie die Titelleistenbeschriftung und das Symbol ausblenden, um Redundanz zu vermeiden.** Sie müssen jedoch intern einen geeigneten Titel für die Verwendung durch Windows festlegen.
-   **Schließen Sie für Dialogfelder nicht die Wörter "dialog" oder "progress" in die Titel ein.** Diese Konzepte werden impliziert, und das Weglassen dieser Wörter erleichtert benutzern das Scannen der Titel.

### <a name="main-instructions"></a>Hauptanweisungen

-   **Verwenden Sie die Hauptanweisung, um präzise zu erläutern, was Benutzer in einem bestimmten Fenster oder auf einer bestimmten Seite tun sollten.** Gute Hauptanweisungen kommunizieren das Ziel des Benutzers, anstatt sich nur auf die Bearbeitung der Benutzeroberfläche zu konzentrieren.
-   **Ausdrücken der Hauptanweisung in Form einer imperativen Richtung oder einer bestimmten Frage.**

    **Falsch:**

    ![Screenshot des Programmnamens als Hauptanweisung ](images/text-ui-image34.png)

    In diesem Beispiel gibt die Hauptanweisung einfach den Namen des Programms an. Er lädt den Benutzer nicht explizit zu einer Aktion ein.

    **Ausnahmen:** Fehlermeldungen, Warnmeldungen und Bestätigungen können unterschiedliche Satzstrukturen in ihren Hauptanweisungen verwenden.

-   **Verwenden Sie nach Möglichkeit bestimmte Verben.** Bestimmte Verben (Beispiele: Verbinden, Speichern, Installieren) sind für Benutzer sinnvoller als generische Verben (Beispiele: Konfigurieren, Verwalten, Festlegen).
    -   Wenn Sie für Systemsteuerungsseiten und Assistentenseiten kein bestimmtes Verb verwenden können, sollten Sie das Verb möglicherweise vollständig weglassen.

        **Annehmbar:**

        Geben Sie Ihr Gebietsschema, Ihre Region und Ihre Sprache ein.

        **Besser:**

        Gebietsschema, Region und Sprache

    -   Lassen Sie für Dialoge, z. B. Fehlermeldungen und Warnungen, das Verb nicht aus.

-   Sie möchten den Hauptanweisungstext nicht verwenden, wenn das Hinzufügen nur redundant oder offensichtlich aus dem Kontext der Benutzeroberfläche wäre.

    ![Screenshot des Dialogfelds "Speichern unter" ](images/text-ui-image35.png)

    In diesem Beispiel ist der Kontext der Benutzeroberfläche bereits sehr klar. es ist nicht erforderlich, Hauptanweisungstext hinzuzufügen.

-   **Verwenden Sie nur einen einzigen vollständigen Satz.** Analysieren Sie die Hauptanweisung auf die grundlegenden Informationen. Wenn Sie weitere Informationen benötigen, sollten Sie eine zusätzliche Anweisung verwenden.
-   Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.
-   **Schließen Sie keine abschließenden Zeiträume ein, wenn die Anweisung eine -Anweisung ist.** Wenn die Anweisung eine Frage ist, fügen Sie ein abschließendes Fragezeichen ein.
-   Verwenden Sie für **Statusdialoge einen Gerund-Ausdruck, der den ausgeführten Vorgang kurz erläutert und** mit einer Auslassungszeichen endet. Beispiel: "Drucken ihrer Bilder..."
-   **Tipp:** Sie können eine Hauptanweisung auswerten, indem Sie sich vorstellen, was Sie einem Freund sagen würden, wenn Sie erklären, was mit dem Fenster oder der Seite geschehen soll. Wenn die Antwort mit der Hauptanweisung unnatürlich, nicht hilfreich oder umständlich wäre, sollten Sie die Anweisung umarbeiten.

Weitere Informationen finden Sie im Abschnitt "Hauptanweisung" in den spezifischen Richtlinien für Benutzeroberflächenkomponenten.

### <a name="supplemental-instructions"></a>Zusätzliche Anweisungen

-   Verwenden Sie bei Bedarf **eine ergänzende Anweisung, um zusätzliche Informationen darzustellen, die hilfreich sind, um das Fenster oder die Seite zu verstehen oder zu verwenden,** z. B.:
    -   Bereitstellen von Kontext, um zu erklären, warum das Fenster angezeigt wird, wenn es programm- oder systeminitiiert ist.
    -   Qualifizieren von Informationen, mit denen Benutzer entscheiden können, wie auf die Hauptanweisung reagiert werden soll.
    -   Definieren wichtiger Terminologie.
-   **Verwenden Sie keine ergänzende Anweisung, wenn keine erforderlich ist.** Kommunizieren Sie lieber alles mit der Hauptanweisung, wenn Sie dies präzise tun können.
-   **Wiederholen Sie die Hauptanweisung nicht mit leicht abweichenden Formulierungen.** Lassen Sie stattdessen die zusätzliche Anweisung aus, wenn sie nicht mehr hinzugefügt werden muss.
-   Verwenden Sie vollständige Sätze und Großbuchstaben im Satzstil.

### <a name="control-labels"></a>Steuerelementbezeichnungen

-   **Bezeichnen Sie jedes Steuerelement oder jede Gruppe von Steuerelementen. Ausnahmen:**
    -   Textfelder und Dropdownlisten können mithilfe von Eingabeaufforderungen bezeichnet werden.
    -   Kontrollen zur progressiven Offenlegung sind im Allgemeinen nicht bezeichnet.
    -   **Untergeordnete Steuerelemente verwenden die Bezeichnung ihres zugeordneten Steuerelements.** Drehsteuerelemente sind immer untergeordnete Steuerelemente.
    -   **Lassen Sie Steuerelementbezeichnungen aus, die die Hauptanweisung neu erstellen.** In diesem Fall übernimmt die Main-Anweisung den Zugriffsschlüssel.

        **Annehmbar:**

        ![Screenshot des Textfelds mit Anweisung und Bezeichnung ](images/text-ui-image36.png)

        In diesem Beispiel ist die Bezeichnung des Textfelds nur eine Neuanordnung der Hauptanweisung.

        **Besser:**

        ![Screenshot des Textfelds mit nur Anweisung ](images/text-ui-image37.png)

        In diesem Beispiel wird die redundante Bezeichnung entfernt, sodass die Main-Anweisung den Zugriffsschlüssel annimmt.

-   Bezeichnungsplatzierung:
    -   Sprechblasen, Kontrollkästchen, Befehlsschaltflächen, Gruppenfelder, Links, Registerkarten und Tipps werden direkt vom Steuerelement selbst bezeichnet.
    -   Dropdownlisten, Listenfelder, Listenansichten, Statusleisten, Schieberegler, Textfelder und Strukturansichten sind oben, links oder links gekennzeichnet.
    -   Kontrollen zur progressiven Offenlegung sind in der Regel nicht gekennzeichnet. Chevron-Schaltflächen sind rechts beschriftet.
-   Weisen Sie für jedes interaktive Steuerelement mit Ausnahme von Links **einen eindeutigen Zugriffsschlüssel** zu. Weitere Informationen finden Sie unter [Tastatur](inter-keyboard.md).
-   **Halten Sie Bezeichnungen kurz.** Beachten Sie jedoch, dass das Hinzufügen von ein oder zwei Wörtern zu einer Bezeichnung zur Übersichtlichkeit beitragen kann und manchmal zusätzliche Erklärungen überflüssig macht.
-   **Bevorzugen Sie bestimmte Bezeichnungen gegenüber generischen Bezeichnungen.** Im Idealfall sollten Benutzer nichts anderes lesen müssen, um die Bezeichnung zu verstehen.

    **Falsch:**

    ![Screenshot der Befehlsschaltfläche "OK" ](images/text-ui-image38.png)

    **Richtig:**

    ![Screenshot der Schaltfläche "Befehl veröffentlichen" ](images/text-ui-image39.png)

    Im richtigen Beispiel wird eine bestimmte Bezeichnung für die Commitschaltfläche verwendet.

-   Verwenden Sie für **Listen von Bezeichnungen, z. B. Optionsfelder, parallele Ausdrücke,** und versuchen Sie, die Länge für alle Bezeichnungen ungefähr gleich zu halten.
-   **Bei Bezeichnungslisten konzentrieren Sie den Bezeichnungstext auf die Unterschiede zwischen den Optionen.** Wenn alle Optionen denselben einführenden Text aufweisen, verschieben Sie diesen Text in die Gruppenbezeichnung.

    **Falsch:**

    ![Screenshot von Bezeichnungen mit doppelten ersten Ausdrücken](images/text-ui-image40.png)

    **Richtig:**

    ![Screenshot des ersten Ausdrucks, der in die Gruppenbezeichnung verschoben wurde](images/text-ui-image41.png)

    Im richtigen Beispiel wird der identische einführende Ausdruck auf die Bezeichnung bewegt, sodass die beiden Optionen genauer unterschieden werden.

-   **Im Allgemeinen bevorzugen Sie positive Formulierungen.** Verwenden Sie beispielsweise do anstelle von nicht, und benachrichtigen Sie, anstatt nicht zu benachrichtigen.
    -   **Ausnahme:** Die Kontrollkästchenbezeichnung "Diese Meldung nicht mehr anzeigen" wird häufig verwendet.
-   **Weglassen von Anweisungsverben, die für alle Steuerelemente des angegebenen Typs gelten.** Konzentrieren Sie sich bei Bezeichnungen vielmehr darauf, was an den Steuerelementen einzigartig ist. Es ist beispielsweise nicht selbstverständlich, dass Benutzer in ein Textfeld-Steuerelement eingeben müssen oder dass Benutzer auf einen Link klicken müssen.

    **Falsch:**

    ![Screenshot der Bezeichnung: "Geben Sie Ihren Namen ein" ](images/text-ui-image42.png)

    **Richtig:**

    ![Screenshot der Bezeichnung: "Ihr Name" ](images/text-ui-image43.png)

    In den falschen Beispielen verfügen die Steuerelementbezeichnungen über Anweisungsverben, die für alle Steuerelemente ihres Typs gelten.

-   In einigen Fällen können die folgenden klammerischen Anmerkungen zum Steuern von Bezeichnungen hilfreich sein:
    -   **Wenn eine Option optional ist, sollten Sie der Bezeichnung "(optional)" hinzufügen.**
    -   **Wenn eine Option dringend empfohlen wird, fügen Sie der Bezeichnung "(recommended)" hinzu.** Dies bedeutet, dass die Einstellung optional ist, aber trotzdem festgelegt werden sollte.
    -   **Wenn eine Option nur für fortgeschrittene Benutzer vorgesehen ist, sollten Sie der Bezeichnung "(advanced)" hinzufügen.**
-   Sie können Einheiten (Sekunden, Verbindungen und so weiter) in Klammern hinter der Bezeichnung angeben.

    ![Screenshot der Bezeichnung: Anfangsgröße (mb) ](images/text-ui-image44.png)

    Dieses Beispiel zeigt, dass die Maßeinheit megabytes (MB) ist.

Weitere Informationen finden Sie im Abschnitt "Text" oder "Bezeichnungen" in den spezifischen Richtlinien für Benutzeroberflächenkomponenten.

### <a name="supplemental-explanations"></a>Ergänzende Erläuterungen

-   **Verwenden Sie ergänzende Erklärungen, wenn Steuerelemente mehr Informationen benötigen, als durch ihre Bezeichnung vermittelt werden können.** Verwenden Sie jedoch keine ergänzende Erklärung, wenn sie nicht notwendig ist, es vorziehen, alles mit der Steuerelementbezeichnung zu kommunizieren, wenn Sie dies präzise tun können. In der Regel werden ergänzende Erklärungen mit Befehlslinks, Optionsfeldern und Kontrollkästchen verwendet.
-   Verwenden Sie bei **Bedarf fett in den Steuerelementbezeichnungen,** damit der Text leichter durchsucht werden kann, wenn zusätzliche Erklärungen enthalten sind.

    ![Screenshot des Dialogfelds "Sicherheitseinstellungen" ](images/text-ui-image45.png)

    In diesem Beispiel sind die Optionsfeldbezeichnungen fett formatiert, um die Überprüfung zu vereinfachen.

-   **Das Hinzufügen einer ergänzenden Erklärung zu einem Steuerelement in einer Gruppe bedeutet nicht, dass Sie Erklärungen für alle anderen Steuerelemente in der Gruppe bereitstellen müssen.** Geben Sie nach Bedarf die relevanten Informationen in der Bezeichnung an, und verwenden Sie Erklärungen nur bei Bedarf. Sie haben keine zusätzlichen Erklärungen, die lediglich die Bezeichnung aus Konsistenz-Heiterkeit neu erklären.

    ![Screenshot von drei Optionsfeldern ](images/text-ui-image46.png)

    In diesem Beispiel enthalten zwei Steuerelemente in der Gruppe ergänzende Erklärungen, das dritte jedoch nicht.

-   Wenn eine ergänzende Erklärung auf einen Befehlslink folgt, schreiben Sie den ergänzenden Text in der zweiten Person.

    **Beispiel:** Befehlslink: Erstellen von Drahtlosnetzwerkeinstellungen und Speichern auf USB-Speicher

    Ergänzende Erläuterung: Dadurch werden Einstellungen erstellt, die Sie mit einem USB-Speicherb gegen den Router übertragen können. Dies ist nur dann der Fall, wenn Sie über einen Drahtlosrouter verfügen, der die Konfiguration des USB-Flashlaufwerks unterstützt.

-   Verwenden Sie vollständige Sätze und endende Interpunktion.

### <a name="commit-button-labels"></a>Schaltflächenbezeichnungen für Commits

In der folgenden Tabelle sind die gängigsten Schaltflächenbezeichnungen für Commits und ihre Verwendung aufgeführt.




| | | <strong>Schaltflächenbezeichnung</strong><br /> | <strong>Bedeutung</strong><br /> | <strong>Verwendung</strong><br /> | <strong>Zugriffsschlüssel</strong><br /> | | <strong>OK</strong><br /> | <ul><li>In Dialogfeldern: Wenden Sie die Änderungen an, oder führen Sie einen Commit für die Aufgabe durch, und schließen Sie das Fenster.</li><li>In Besitzer-Eigenschaftenfenstern: Übernehmen Sie die ausstehenden Änderungen (seit dem Öffnen des Fensters oder des letzten Apply-Fensters), und schließen Sie das Fenster.</li><li>In Eigenschaftenfenstern im Besitz: Behalten Sie die Änderungen bei, schließen Sie das Fenster, und wenden Sie die Änderungen an, wenn die Änderungen des Besitzerfensters angewendet werden.</li></ul> | <ul><li>Verwenden Sie mit Fenstern, die nicht aufgabenspezifisch sind, z. B. Eigenschaftenblätter.</li><li>Verwenden Sie für Fenster, die zum Ausführen einer bestimmten Aufgabe verwendet werden, stattdessen eine bestimmte Bezeichnung, die mit einem Verb beginnt (Beispiel: Drucken).</li><li>Verwenden Sie für Fenster, in denen Benutzer keine Änderungen vornehmen können, Schließen.</li></ul> | Eingeben<br /> | | <strong>Ja/Nein</strong><br /> | Ja ist die positive Antwort auf eine Ja- oder Nein-Frage, während Nein die negative Antwort ist.<br /> | <ul><li>Verwenden Sie die Schaltflächen Ja und Nein, um nur auf Ja- oder Nein-Fragen zu antworten. Verwenden Sie für Ja- oder Nein-Fragen niemals OK und Abbrechen.</li><li>Bevorzugen Sie bestimmte Antworten den Schaltflächen Ja und Nein. Auch wenn die Verwendung von Ja und Nein kein Fehler ist, können bestimmte Antworten schneller verstanden werden, was zu einer effizienten Entscheidungsfindung führt.</li><li>Erwägen Sie jedoch die Verwendung von Ja- und Nein-Antworten, wenn sich der Ausdruck bestimmter Antworten als lang oder ums andere Zeit erweist.</li><li>Verwenden Sie die Schaltflächen Ja und Nein nicht, wenn die Bedeutung der Antwort Nein unklar ist. Falls ja, verwenden Sie stattdessen bestimmte Antworten.</li><li>Ja und Nein müssen immer als Paar verwendet werden.</li></ul> | Y und N<br /> | | <strong>Abbrechen</strong><br /> | <ul><li>In Dialogfeldern: Verwerfen Sie alle Änderungen oder arbeiten Sie in Bearbeitung, führen Sie den vorherigen Zustand zurück (ohne erkennbaren Nebeneffekt), und schließen Sie das Fenster.</li><li>In Eigenschaftenblättern: Verwerfen Sie alle ausstehenden Änderungen (seit dem Öffnen des Fensters oder dem letzten Anwenden), und schließen Sie das Fenster.</li><li>In Systemsteuerungselementen: Verwerfen Sie alle Änderungen, oder arbeiten Sie in Bearbeitung, kehren Sie zum vorherigen Zustand zurück, und kehren Sie zu der Hubseite zurück, von der die Aufgabe gestartet wurde. Wenn keine solche Hubseite verfügbar ist, schließen Sie stattdessen das Fenster des Systemsteuerungselements.</li></ul> | <ul><li>Verwenden Sie , wenn alle ausstehenden Änderungen oder Aktionen verworfen und alle Nebeneffekte rückgängig gemacht werden können.</li><li>Für Änderungen, die nicht verworfen werden können, verwenden Sie Schließen. Verwenden Sie Für Aktionen, die in Bearbeitung sind und beendet werden können, Beenden. Wenn anfänglich Änderungen oder Aktionen verworfen werden können, können Sie Zunächst abbrechen verwenden und dann zu Schließen oder Beenden wechseln, sobald dies nicht rückgängig gemacht werden kann.</li></ul> | Esc<br /> | | <strong>Schließen</strong><br /> | Schließen Sie das Fenster. Änderungen oder Nebeneffekte werden nicht verworfen.<br /> | <ul><li>Verwenden Sie , wenn Änderungen oder Nebeneffekte nicht verworfen werden können. Verwenden Sie close anstelle von Cancel für primäre Fenster.</li><li>Verwenden Sie für Fenster, in denen Benutzer keine Änderungen vornehmen können.</li></ul> | ALT+F4, STRG+F4<br /> | | <strong>Beenden</strong><br /> | Beenden Sie einen aktuell ausgeführten Task, und schließen Sie das Fenster. Arbeits- oder Nebeneffekte werden nicht verworfen.<br /> | <ul><li>Verwenden Sie , wenn die Arbeit in Bearbeitung ist und Nebeneffekte nicht verworfen werden können oder werden, in der Regel mit Statusleisten oder Animationen.</li></ul> | Esc<br /> | | <strong>Anwenden</strong><br /> | In Besitzer-Eigenschaftenblättern: Übernehmen Sie die ausstehenden Änderungen (seit dem Öffnen des Fensters oder des letzten Apply-Fensters), lassen Sie das Fenster jedoch geöffnet. Auf diese Weise können Benutzer die Änderungen auswerten, bevor sie das Eigenschaftenblatt schließen. In Eigenschaftenblättern im Besitz: nicht verwenden.<br /> | <ul><li>Verwenden Sie nur in Eigenschaftenblättern.</li><li>Geben Sie nur dann eine Schaltfläche Anwenden an, wenn das Eigenschaftenblatt Über Einstellungen (mindestens eine) mit Effekten verfügt, die Benutzer sinnvoll auswerten können. In der Regel werden Schaltflächen anwenden verwendet, wenn Einstellungen sichtbare Änderungen vornehmen. Benutzer sollten in der Lage sein, eine Änderung anzuwenden, die Änderung zu bewerten und weitere Änderungen basierend auf dieser Auswertung vorzunehmen. Wenn nicht, entfernen Sie die Schaltfläche Anwenden, anstatt sie zu deaktivieren.</li></ul> | Eine<br /> | | <strong>Weiter</strong><br /> | In Assistenten und mehrstufigen Aufgaben: Mit dem nächsten Schritt fort, ohne sich für die Aufgabe zu committen.<br /> | <ul><li>Verwenden Sie nur in Assistenten und mehrstufigen Aufgaben, um ohne Verpflichtung mit dem nächsten Schritt fort zu arbeiten.</li><li>Die Auswirkung einer Schaltfläche Weiter kann immer durch Klicken auf Zurück rückgängig gemacht werden.</li></ul> | N<br /> | | <strong>Fertig stellen</strong><br /> | In Assistenten und mehrstufigen Aufgaben: Schließen Sie das Fenster. Wenn die Aufgabe noch nicht ausgeführt wurde, führen Sie die Aufgabe aus. Wenn diese Aufgabe bereits ausgeführt wurde, werden änderungen oder Nebeneffekte nicht verworfen.<br /> | <ul><li>Nur in Assistenten und mehrstufigen Aufgaben verwenden. Von der Verwendung von Finish wird jedoch abgeraten, da es in der Regel eine bessere, spezifischere Commitschaltfläche gibt:<ul><li>Wenn durch Klicken auf die Schaltfläche ein Commit für die Aufgabe ausgeführt wird (damit die Aufgabe noch nicht ausgeführt wurde), verwenden Sie eine bestimmte Bezeichnung, die mit einem Verb beginnt (Beispiele: Print, Verbinden, Start), das eine Antwort auf die Hauptanweisung ist.</li><li>Wenn die Aufgabe bereits im Assistenten ausgeführt wurde, verwenden Sie stattdessen Schließen.</li></ul></li><li>Sie können jedoch Fertig stellen verwenden, wenn:<ul><li>Die spezifische Bezeichnung ist weiterhin generisch, z. B. Speichern, Auswählen, Auswählen oder Get.</li><li>Die Aufgabe umfasst das Ändern einer Einstellung oder Sammlung von Einstellungen.</li></ul></li></ul> | Eingeben<br /> | | <strong>Fertig</strong><br /> | Nicht zutreffend.<br /> | <ul><li>Nicht verwenden. Der Befehl ist grammatikalisch falsch.</li></ul> | Nicht zutreffend.<br /> | 




 

