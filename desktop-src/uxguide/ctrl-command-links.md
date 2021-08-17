---
title: Befehlsverknüpfungen
description: Mit Befehlslinks wählen Benutzer eine einzelne Antwort auf eine main-Anweisung aus und gehen dann mit dem nächsten Schritt einer Aufgabe fort.
ms.assetid: a77819b1-9a32-4468-94fb-3f73a469fb81
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ac24618b70d96b1b625549582af27e47b5386f354f09e7147000fc5ed438a36f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091048"
---
# <a name="command-links"></a>Befehlsverknüpfungen

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Mit Befehlslinks wählen Benutzer eine einzelne Antwort auf eine main-Anweisung aus und gehen dann mit dem nächsten Schritt einer Aufgabe fort.

Befehlslinks weisen eine saubere, einfache Darstellung auf, die beschreibende Bezeichnungen zulässt, und werden entweder mit einem Standardpfeil oder einem benutzerdefinierten Symbol und einer optionalen zusätzlichen Erklärung angezeigt.

![Screenshot eines typischen Befehlslinkdialogfelds ](images/ctrl-command-links-image1.png)

Ein typischer Satz von Befehlslinks.

Befehlslinks ähneln [Optionsfeldern,](ctrl-radio-buttons.md) da sie verwendet werden, um eine Reihe von sich gegenseitig ausschließenden, verwandten Optionen auszuwählen. Wie Optionsfelder werden Befehlslinks immer in Sätzen und nie einzeln angezeigt. Im Aussehen haben Befehlslinks eine einfache Darstellung, die regulären Links [ähnelt,](ctrl-links.md)ohne einen Frame oder einen anderen Starkenklick. [](glossary.md) Befehlslinks ähneln auch [Befehlsschaltflächen,](ctrl-command-buttons.md)da sie die Standardmäßige "Befehlsschaltfläche" sein können und ihnen ein Zugriffsschlüssel zugewiesen werden kann. Wie [bei Commitschaltflächen](glossary.md)schließen sie beim Klicken entweder das Fenster (für Dialogfelder) oder blättern zur nächsten Seite (für Assistenten und Seitenflüsse).

> [!Note]  
> Richtlinien im Zusammenhang [mit Links](ctrl-links.md) [und Layout](vis-layout.md) werden in separaten Artikeln vorgestellt.

 

## <a name="is-this-the-right-control"></a>Ist dies das richtige Steuerelement?

Orientieren Sie sich an folgenden Fragen:

-   **Sind die Optionen Antworten auf die Main-Anweisung und stehen im Zusammenhang mit dem primären Zweck des Fensters oder der Seite?** Müssen Benutzer auf sie reagieren, um etwas anderes zu tun, als nur zu einer anderen Seite zu navigieren? Falls nicht, verwenden Sie ein anderes Steuerelement, z. B. Befehlsschaltflächen oder Links. Befehlslinks sind nicht für sekundäre oder optionale Optionen oder reine Navigation geeignet.

    ![Screenshot eines Personalisierens eines Systemsteuerungselements ](images/ctrl-command-links-image2.png)

    Während das Personalisierungselement Systemsteuerung, als würde es Befehlslinks verwenden, handelt es sich bei den Optionen um reguläre Links, da diese Hubseite für die reine Navigation verwendet wird. [](winenv-ctrl-panels.md)

-   **Wird das Steuerelement verwendet, um eine Antwort aus einer Reihe von sich gegenseitig ausschließenden Antworten zu wählen?** Wenn dies nicht erwünscht ist, verwenden Sie ein anderes Steuerelement. Damit Benutzer einzelne Befehle auswählen können, verwenden Sie Befehlsschaltflächen oder Links.
-   **Schließt das Klicken auf das Steuerelement das Fenster für Dialogfelder?** Falls nicht, verwenden Sie ein Steuerelement, das das Schließen des Fensters nicht erfordert, z. B. Optionsfelder, Befehlsschaltflächen oder Links.

    **Falsch:**

    ![Screenshot des Dialogfelds "Firewalleinstellungen im Registerkartenmodus" ](images/ctrl-command-links-image3.png)

    Befehlslinks können nicht in Eigenschaftenfenstern oder Dialogfeldern im Registerkartenfenster verwendet werden, da das Fenster durch Klicken auf das Steuerelement geschlossen wird.

-   **Wird bei Assistenten und Seitenflüssen ohne Verpflichtung auf die nächste Seite geklickt?** Verwenden Sie keine Befehlslinks, um einen Commit für eine Aufgabe auszuführen. Verwenden Sie stattdessen Commitschaltflächen. Da Befehlslinks wie Links aussehen und Benutzer Links der Navigation innerhalb [](glossary.md) eines Seitenflusses zuordnen, sind Links für Commitseiten nicht geeignet, da Benutzer immer in der Lage sein sollten, das Back-Out auszuführen.
-   **Verwenden andere Seiten für Assistenten und Seitenflüsse Befehlslinks?** Wenn dies der Wert ist und alle anderen Faktoren gleich sind, bevorzugen Sie Befehlslinks für seitenübergreifende Konsistenz.
-   **Liegt die Anzahl der Antworten zwischen zwei und fünf?** Es sollte nie einen einzelnen Befehlslink geben. Da Befehlslinks große Steuerelemente sind und der verwendete Bildschirmbereich proportional zur Anzahl der Optionen ist, sollten Sie die Anzahl der Antworten auf fünf oder weniger festlegen. Verwenden Sie für sechs oder mehr Optionen Optionsfelder, reguläre Links oder eine Listenansicht mit [nur einer Auswahl.](ctrl-list-views.md)

    ![Screenshot des Dialogfelds mit einer Liste von Befehlen ](images/ctrl-command-links-image4.png)

    In diesem Beispiel verwendet das AutoPlay-Feature in Microsoft Windows eine Listenansicht.

-   **Wäre eine Kombination aus Optionsfeldern und einer Commitschaltfläche die bessere Wahl?** Optionsfelder sind eine bessere Wahl, wenn eine der folgenden Bedingungen zutrifft:
    -   **Es gibt eine starke Standardoption, die von den meisten Benutzern ausgewählt werden soll.** Benutzer ändern eher ein Standardschaltfeld als einen Standardbefehlslink, insbesondere in einem Assistenten, in dem Benutzer gewohnt sind, auf Weiter zu klicken, um die entsprechenden Standardwerte zu übernehmen. Andererseits sind Befehlslinks eine bessere Wahl, wenn Sie Benutzer dazu ermutigen möchten, eine explizite Auswahl zu treffen.
    -   **Benutzer müssen mit den Optionen interagieren (um möglicherweise zusätzliche Informationen zu erhalten), bevor sie eine Entscheidung treffen.** Wenn Sie beispielsweise ein Optionsfeld auswählen, wird möglicherweise dynamisch eine Beschreibung der Option angezeigt.

        ![Screenshot des Dialogfelds mit Optionsfeldern ](images/ctrl-command-links-image5.png)

        In diesem Beispiel zeigt das Auswählen eines Optionsfelds eine Beschreibung der Option an.

    -   **Es gibt sekundäre oder verwandte Optionen auf der Seite.** Befehlslinks tendieren dazu, die Seite zu überrennen, was es einfach macht, alles andere zu übersehen. Darüber hinaus ist es nach dem Klicken auf einen Befehlslink nicht mehr möglich, sekundäre Optionen auszuwählen.

        **Falsch:**

        ![Screenshot des Dialogfelds mit gemischten Steuerelementen ](images/ctrl-command-links-image6.png)

        In diesem Beispiel gibt es zwei verschiedene Möglichkeiten, auf die main-Anweisung zu reagieren. Für die erste Antwort wurde kein Befehlslink verwendet, da es schwierig wäre, sekundäre Optionen auszuwählen.

        **Richtig:**

        ![Screenshot des Dialogfelds mit denselben Steuerelementen ](images/ctrl-command-links-image7.png)

        In diesem Beispiel machen Optionsfelder die Antworten klar, während Benutzer sekundäre Optionen auswählen können.

-   **Wäre eine Gruppe von Commitschaltflächen für Dialogfelder die bessere Wahl?** Befehlslinks funktionieren besser, wenn die Optionen längere, erläuternde Antworten und ergänzende Erklärungen erfordern, aber eine Gruppe von Commitschaltflächen ist eine bessere Wahl, wenn es einige einfache Optionen gibt.

    **Falsch:**

    ![Screenshot des Dialogfelds mit speichern und nicht speichern ](images/ctrl-command-links-image8.png)

    In diesem Beispiel macht die Verwendung von Befehlslinks für einfache Befehle das Dialogfeld unnötig kompliziert.

    **Richtig:**

    ![Screenshot: Dialogfeld mit den Commitschaltflächen "Speichern", "Nicht speichern" und "Abbrechen"](images/ctrl-command-links-image9.png)

    In diesem Beispiel wird die Verwendung von einfachen Commitschaltflächen direkt bis zum Punkt angezeigt.

    Selbsterklärende Befehlslinks sind jedoch immer besser, wenn Text verwendet wird, um Commitschaltflächen zu erklären.

    **Falsch:**

    ![Screenshot des Dialogfelds mit unnötigem Text ](images/ctrl-command-links-image10.png)

    In diesem Beispiel wird Text verwendet, um die Commitschaltflächen zu erläutern.

    **Richtig:**

    ![Screenshot von Bezeichnungen, die nicht mehr Text benötigen ](images/ctrl-command-links-image11.png)

    In diesem Beispiel sind die Befehlslinks selbsterklärend.

> [!Note]  
> Befehlslinks Windows Vista oder höher erforderlich, sodass sie nicht für frühere Versionen von Windows. Sie können reguläre Links als Ersatz verwenden.

 

![Screenshot von regulären Links mit Symbolen und Text ](images/ctrl-command-links-image12.png)

In diesem Beispiel werden reguläre Links mit einem Symbol und einer ergänzenden Erklärung als Ersatz für Befehlslinks in Windows XP verwendet.

## <a name="design-concepts"></a>Entwurfskonzepte

Nur weil Befehlslinks es Ihnen ermöglichen, aussagekräftigere Bezeichnungen zu verwenden, und optionale ergänzende Erläuterungen dies nicht bedeuten. Betrachten Sie das folgenden Beispiel:

**Falsch:**

![Screenshot des Dialogfelds mit zu viel Text ](images/ctrl-command-links-image13.png)

Dieses Dialogfeld ist eine zu viele Kommunikation.

In diesem Dialogfeld wird eine einfache Frage gestellt und unnötigerweise mit Befehlslinktext verkompliziert. Benutzer möchten diesen Text nicht für so einfache Fragen lesen.

Wir können dieses Dialogfeld vereinfachen, indem wir drei Richtlinien für Befehlslinks anwenden:

-   **Verwenden Sie keine ergänzende Erklärung, bei der es sich um eine wortliche Neunotierung des Befehlslinks handelt.** Verwenden Sie eine ergänzende Erklärung nur, wenn Sie einen Befehlslink nicht selbsterklärend machen können. Das Bereitstellen einer ergänzenden Erklärung für einen Befehlslink bedeutet nicht, dass Sie sie für alle Befehle bereitstellen müssen.
-   **Wählen Sie die sicherste Antwort (um Datenverlust oder Systemzugriff zu verhindern) und die sicherste Antwort als Standard aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequemste Antwort aus.
-   **Geben Sie eine explizite Schaltfläche Abbrechen an.** Verwenden Sie zu diesem Zweck keinen Befehlslink.

Durch Die Anwendung dieser Richtlinien können wir unnötige zusätzliche Erklärungen vermeiden, die bequemste Antwort als Standardantwort festlegen und eine explizite Schaltfläche Abbrechen bereitstellen.

**Besser:**

![Screenshot des Dialogfelds mit Befehlen und Bezeichnungen ](images/ctrl-command-links-image14.png)

Eine verbesserte Version mit einfacheren Befehlslinks.

Obwohl es zutrifft, dass diese Version nicht explizit erklärt, dass das Speichern nicht als Verlust gezählt wird, ändern nur wenige Benutzer ihre Entscheidung basierend auf diesen Informationen und machen dies zu einem guten Kompromiss.

Dieses Dialogfeld kann noch besser gestaltet werden, indem analysiert wird, ob Befehlslinks in diesem Fall sogar das richtige Steuerelement sind. Commitschaltflächen sind tatsächlich eine bessere Wahl, da längere, erläuternde Antworten nicht erforderlich sind.

**Beste:**

![Screenshot des Dialogfelds mit Commitschaltflächen ](images/ctrl-command-links-image15.png)

Die richtige Version verwendet Commitschaltflächen, um direkt auf den Punkt zu gelangen.

Befehlslinks haben viele Vorteile, führen aber bei unkluger Verwendung zu Überkommunikation. Erwägen Sie für Dialogfelder zuerst die Verwendung von Commitschaltflächen, und verwenden Sie Befehlslinks nur, wenn commit-Schaltflächen die Aufgabe nicht gut erledigen.

**Bei entsprechender Verwendung sollten Befehlslinks Ihre Benutzeroberfläche vereinfachen und verdeutlichen.** Wenn die Ergebnisse das Gegenteil sind, gehen Sie einen Schritt zurück, überprüfen Sie die Alternativen, und konzentrieren Sie sich auf das, was Sie wirklich kommunizieren müssen.

**Wenn Sie nur eine Sache durchführen...** Verwenden Sie keine Befehlslinks für die überhändige Kommunikation. Befehlslinks sollten die Kommunikation vereinfachen und verdeutlichen, dürfen sie nicht komplizierter machen.

## <a name="usage-patterns"></a>Verwendungsmuster

Befehlslinks weisen mehrere Verwendungsmuster auf:



| Verwendung                                                                                                                      | Beispiel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Seitenantworten** Befehlslinks werden verwendet, um auf die Hauptanweisung zu reagieren und zur nächsten Seite zu gelangen.    | Mit diesem Muster ersetzen die Befehlslinks die nächste Schaltfläche, aber es gibt immer noch eine Schaltfläche zum Abbrechen.<br/>Seitenantworten bedeuten keine Verpflichtung. Da Befehlslinks wie Links aussehen und Benutzer Links der Navigation innerhalb eines Seitenflows zuordnen, sind Links für Commitseiten nicht geeignet. Benutzer sollten immer in der Lage sein, das Back-Out durchzuführen. <br/> ![Screenshot: Dialogfeld "Verbinden zum Internet" mit Den Befehlslinks "Drahtlos", "Breitband (PPPoE)" und "DFÜ"](images/ctrl-command-links-image16.png)<br/>In diesem Beispiel werden Befehlslinks verwendet, um beschreibende Antworten auf die Hauptanweisung zu geben. Während hier Optionsfelder verwendet werden können, ermöglichen Befehlslinks Benutzern, mit einem einzigen Klick zu antworten.<br/> |
| **Dialogfeldantworten** Befehlslinks werden verwendet, um auf die Hauptanweisung zu reagieren und das Dialogfeld zu schließen.  | Mit diesem Muster ersetzen die Befehlslinks die Commitschaltflächen (z. B. OK), aber es gibt immer noch eine Schaltfläche zum Abbrechen.<br/>Im Gegensatz zu Seitenflows gibt es keine Möglichkeit, aus einer dialogfeldbasierten Antwort zurückzukehren, sobald sie erfolgt ist. Folglich impliziert die Dialogfeld-Befehlslinks eine Verpflichtung. <br/> ![Screenshot des Dialogfelds mit Befehlslinks ](images/ctrl-command-links-image17.png)<br/>In diesem Beispiel werden Befehlslinks verwendet, um beschreibende Antworten auf die Hauptanweisung zu geben. Obwohl hier Optionsfelder verwendet werden können, können Benutzer über Befehlslinks mit einem einzigen Klick auswählen.<br/>                                                   |
| **Detaillierte Antworten** Eine Seiten- oder Dialogantwort, die ausführliche Informationen enthält.                          | Gelegentlich benötigen Benutzer möglicherweise ausführlichere Informationen, um ihre Antwort auszuwählen. <br/> ![Screenshot: Dialogfeld "Datei kopieren" und Miniaturansichten ](images/ctrl-command-links-image18.png)<br/> In diesem Beispiel werden detaillierte Befehlslinks verwendet, damit Benutzer fundierte Entscheidungen treffen können. Die Miniaturansichten und Dateidetails helfen Benutzern bei der Entscheidung.<br/>                                                                                                                                                                                                                                                                                                         |



 

## <a name="guidelines"></a>Richtlinien

### <a name="interaction"></a>Interaktion

-   **Zeigt einen ausgelasteten Zeiger an, wenn das Ergebnis des Klickens auf einen Befehlslink nicht sofort erfolgt.** Ohne Feedback gehen Benutzer möglicherweise davon aus, dass der Klick nicht erfolgt ist, und klicken erneut.

### <a name="presentation"></a>Präsentation

-   **Befehlslinks werden immer in einer Gruppe von zwei oder mehr Befehlslinks dargestellt.** Logischerweise gibt es keinen Grund, eine Frage mit nur einer Antwort zu stellen.

    **Falsch:**

    ![Screenshot des Dialogfelds mit einem Befehlslink ](images/ctrl-command-links-image19.png)

    In diesem Beispiel scheint das Dialogfeld dem Benutzer eine Auswahl zu bieten, aber es gibt nur eine Anweisung. Dies sollte stattdessen ein Informationsdialogfeld sein.

-   **Zeigen Sie zuerst die am häufigsten verwendeten Befehlslinks an.** Die resultierende Reihenfolge sollte ungefähr der Wahrscheinlichkeit der Verwendung entsprechen, aber auch einen logischen Ablauf aufweisen.
    -   **Ausnahme:** Befehlslinks, die dazu führen, dass alles erledigt wird, sollten zuerst platziert werden.
-   **Geben Sie eine explizite Schaltfläche Abbrechen an.** Verwenden Sie zu diesem Zweck keinen Befehlslink. Häufig stellen Benutzer fest, dass sie keine Aufgabe ausführen möchten. Wenn Sie einen Befehlslink zum Abbrechen verwenden, müssten Benutzer alle Befehlslinks sorgfältig lesen, um zu bestimmen, welcher Befehl "abbrechen" bedeutet. Mit einer expliziten Schaltfläche Abbrechen können Benutzer eine Aufgabe effizient abbrechen.

    **Falsch:**

    ![Screenshot des Dialogfelds mit dem Link "Nicht beenden" ](images/ctrl-command-links-image20.png)

    In diesem Beispiel sollte der Befehlslink Nicht beenden eine Schaltfläche Abbrechen sein.

-   **Wenn eine explizite Schaltfläche Abbrechen einen einzelnen Befehlslink verlässt, geben Sie sowohl einen Befehlslink zum Abbrechen als auch eine Schaltfläche Abbrechen an.** Dadurch wird deutlich, dass Benutzer eine Auswahl treffen können. Formulieren Sie diesen Befehlslink in Bezug darauf, wie er sich von der ersten Antwort unterscheidet, anstatt nur "Abbrechen" oder eine Variation.

    ![Screenshot von zwei Links und einer Schaltfläche zum Abbrechen ](images/ctrl-command-links-image21.png)

    In diesem Beispiel gibt der zweite Befehlslink an, dass der Benutzer eine Auswahl hat, aber alles, was er macht, ist abbrechen. Es wird jedoch in Bezug auf seine Unterschiede zum ersten Befehlslink formuliert.

-   **Verwenden Sie Schließen anstelle von Abbrechen, wenn Sie den vorherigen Zustand der Umgebung nicht kehren können, sodass keine Nebeneffekte vorhanden sind.**
-   **Zeigen Sie keine deaktivierten Befehlslinks an.** Wenn ein Befehlslink nicht für den aktuellen Kontext gilt, entfernen Sie ihn stattdessen. Wenn beim Entfernen aller nicht angewendeten Befehlslinks ein einzelner Befehlslink verbleibt, entfernen Sie entweder das Fenster oder die Seite, oder zeigen Sie eine [Bestätigung](mess-confirm.md) an, wenn eine explizite Benutzereinwilligung erforderlich ist.

### <a name="icons"></a>Symbole

-   **Alle Befehlslinks benötigen ein Symbol.** Mithilfe der Symbole können Benutzer Befehlslinks von regulären Links und Benutzeroberflächentext unterscheiden.
-   **Verwenden Sie das Pfeilsymbol nur für Befehlslinks.** Reguläre Links sollten nur dann das Pfeilsymbol verwenden, wenn sie als Ersatz für Befehlslinks in Windows XP verwendet werden.
-   **Verwenden Sie das Sicherheitsschutzsymbol, um anzugeben, dass für eine Antwort eine sofortige Erhöhung erforderlich ist.** Weitere Richtlinien zur Verwendung des Sicherheitsschutzsymbols finden Sie unter [Benutzerkontensteuerung.](winenv-uac.md)
-   **Verwenden Sie benutzerdefinierte Symbole nur, wenn benutzerdefiniert die Optionen visuell identifizieren und unterscheiden können.** Verwenden Sie keine benutzerdefinierten Symbole, wenn sie nicht sofort erkennbar oder sinnvoll sind.

    **Falsch:**

    ![Screenshot von zwei Befehlslinks mit benutzerdefinierten Symbolen ](images/ctrl-command-links-image22.png)

    In diesem Beispiel sind die benutzerdefinierten Symbole nicht sofort erkennbar.

-   **Verwenden Sie für benutzerdefinierte Symbole Symbole mit 16 x 16 oder 32 x 32 Pixeln.** Verwenden Sie die größeren Symbole, wenn ausreichend Platz vorhanden ist und sie visuell von der größeren Größe profitieren. Wenn Sie Sicherheitsschutzüberlagerungen benötigen, verwenden Sie Symbole mit 32 x 32 oder 48 x 48 Pixeln.

    ![Screenshot von drei Befehlslinks mit Symbolen ](images/ctrl-command-links-image23.png)

    In diesem Beispiel werden benutzerdefinierte Symbole mit 32 x 32 Pixeln verwendet.

    ![Screenshot von zwei Befehlslinks mit größeren Symbolen ](images/ctrl-command-links-image24.png)

    In diesem Beispiel werden benutzerdefinierte 48 x 48 Pixel-Symbole mit einer Sicherheitsschutzüberlagerung verwendet.

-   **Vermeiden Sie das Kombinieren von benutzerdefinierten Symbolen mit dem Standardpfeilsymbol in einem Fenster oder einer Seite.** Wenn Sie ein benutzerdefiniertes Symbol auf einer Oberfläche verwenden, versuchen Sie, alle benutzerdefinierten Symbole zu verwenden. Bevorzugen Sie jedoch das Standardpfeilsymbol gegenüber bedeutungslosen benutzerdefinierten Symbolen.

### <a name="default-values"></a>Standardwerte

-   **Wählen Sie die sicherste (um Daten- oder Systemzugriffsverluste zu verhindern) und die sicherste Antwort als Standard aus.** Wenn Sicherheit und Sicherheit keine Faktoren sind, wählen Sie die wahrscheinlichste oder bequemste Antwort aus.
-   Machen Sie die erste Antwort in **der Praxis zur Standardoption,** da Benutzer dies häufig erwarten, es sei denn, diese Reihenfolge ist nicht logisch.
-   **Machen Sie für Dialogfelder keine destruktive Aktion als Standardbefehlslink,** es sei denn, es gibt eine einfache Möglichkeit, die Aktion rückgängig zu machen.

## <a name="recommended-sizing-and-spacing"></a>Empfohlene Größen- und Abstände

![Screenshot der Größe und des Abstands von Befehlslinks ](images/ctrl-command-links-image25.png)

## <a name="labels"></a>Bezeichnungen

> [!Note]  
> Da Befehlslinks Antworten auf eine Hauptanweisung sind, sollten Sie eine [gute Hauptanweisung](text-ui.md) erstellen, bevor Sie deren Antworten bestimmen.

 

**Befehlslinkbezeichnungen**

-   **Wählen Sie eine präzise Bezeichnung aus, die klar kommuniziert und die Funktionen des Befehlslinks unterscheidet.** Sie sollte selbsterklärend sein und der Hauptanweisung entsprechen. Konzentrieren Sie die Bezeichnungen auf die Unterschiede zwischen den Antworten. Benutzer sollten nicht herausfinden müssen, was der Befehlslink wirklich bedeutet oder wie er sich von anderen Befehlslinks unterscheidet.

    **Falsch:**

    ![Screenshot eines redundanten Befehlslinks ](images/ctrl-command-links-image26.png)

    Was ist in diesem Beispiel der Unterschied zwischen der zweiten und dritten Antwort? Freuen Sie sich nicht, dass die Schaltfläche Abbrechen angezeigt wird?

-   **Fokusbefehlslinkbezeichnungen, die Benutzern dabei helfen, die richtige Entscheidung zu treffen.** Lassen Sie Details aus, die sich nicht auf die Auswahl auswirken. Die Bezeichnungen müssen keine vollständige Spezifikation sein, was geschieht.
-   **Startbefehlslinks mit einem Verb.** Verwenden Sie jedoch keine Klicks, da die Bezeichnung die Funktion des Befehlslinks und nicht die Funktionsweise kommunizieren soll.
    -   **Ausnahme:** Wenn alle Befehlslinks mit demselben Verb oder Ausdruck beginnen, entfernen Sie das redundante Verb oder den gleichen Ausdruck.
-   Verwenden Sie im Allgemeinen **positive Ausdrücke** (mit einer Auswahl). Negative Ausdrücke (das Bereitstellen einer Entscheidung, etwas nicht zu tun) sind akzeptabel, wenn die Bezeichnungen leichter zu verstehen sind.
-   **Verwenden Sie parallele Ausdrücke und einzeilige Bezeichnungen.** Lange Bezeichnungen raten vom Lesen ab und sollten nicht erforderlich sein. Außerdem sind Bezeichnungen mit mittlerer Größe in der Dokumentation einfacher zu finden.
-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
-   **Verwenden Sie keine endende Interpunktion, es sei denn, die Bezeichnung ist eine Frage.**
-   **Weisen Sie einen eindeutigen Zugriffsschlüssel zu.** Richtlinien finden Sie unter [Tastatur](inter-keyboard.md).
-   **Verwenden Sie keine Ellipsen.** Ellipsen bedeuten, dass möglicherweise weitere Informationen erforderlich sind, um die Aktion auszuführen. Ordnungsgemäß verwendete Befehlslinks benötigen keine Ellipsen, da sie sofortige Auswirkungen haben.
-   **Wenn eine Antwort dringend empfohlen wird, fügen Sie der Bezeichnung "(empfohlen)" hinzu.** Achten Sie darauf, der Bezeichnung und nicht der ergänzenden Erklärung hinzuzufügen.
-   **Wenn eine Antwort nur für fortgeschrittene Benutzer vorgesehen ist, sollten Sie der Bezeichnung "(advanced)" hinzufügen.** Achten Sie darauf, der Bezeichnung und nicht der ergänzenden Erklärung hinzuzufügen.

**Tipp:** Sie können Befehlslinks auswerten, indem Sie sich vorstellen, dass ein Freund die Hauptanweisung angegeben hat und Sie mit den Befehlslinks geantwortet haben. Wenn die Antwort mit den Befehlslinks unnatürlich oder umständlich wäre, überarbeiten Sie die Befehlslinks und möglicherweise die Hauptanweisung.

**Ergänzende Erläuterungen**

-   Wenn ein Befehlslink eine weitere Erläuterung erfordert, **geben Sie eine zusätzliche Erklärung** an. Ergänzende Erklärungen beschreiben, warum Benutzer möglicherweise eine Antwort auswählen möchten oder was geschieht, wenn eine Antwort ausgewählt wird.

    ![Screenshot des Texts, der die Ergebnisse der Option beschreibt ](images/ctrl-command-links-image27.png)

    In diesem Beispiel beschreibt die ergänzende Erklärung die Auswirkungen der Option.

-   **Verwenden Sie keine ergänzende Erklärung, die eine wortliche Neustellung des Befehlslinks ist.** Verwenden Sie eine ergänzende Erklärung nur, wenn Sie einen Befehlslink nicht selbsterklärend machen können. Das Bereitstellen einer ergänzenden Erklärung für einen Befehlslink bedeutet nicht, dass Sie sie für alle bereitstellen müssen.
-   **Konzentrieren Sie sich auf ergänzende Erklärungen, um Benutzern dabei zu helfen, die richtige Entscheidung zu treffen.** Lassen Sie Details aus, die sich nicht auf die Auswahl auswirken. Die ergänzenden Erklärungen müssen keine vollständige Spezifikation des Geschehens sein.
-   **Verwenden Sie parallele Ausdrücke und höchstens drei Textzeilen.** Lange ergänzende Erklärungen raten vom Lesen ab und sollten nicht erforderlich sein.
-   **Verwenden Sie vollständige Sätze und endende Interpunktion.**

**Bezeichnungen von Befehlslinkgruppen**

-   **Verwenden Sie keine Gruppenbezeichnungen.** Hauptanweisungen fungieren als Gruppenbezeichnung für Befehlslinks.

## <a name="documentation"></a>Dokumentation

Wenn Sie auf Befehlslinks verweisen:

-   Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Großschreibung, aber nicht den Zugriffsschlüsselunterstrich.
-   Wenn die Bezeichnung einen Objektnamen enthält, lassen Sie entweder den Objektnamen aus, oder verwenden Sie Platzhaltertext.
-   Um die Benutzerinteraktion zu beschreiben, klicken Sie auf .
-   Formatieren Sie die Bezeichnung nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnung nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

**Beispiele:** Klicken Sie zum Kopieren des Bilds auf **Kopieren und Ersetzen.**

Klicken Sie auf **Netzwerkadapter zurücksetzen.** (Für einen Befehlslink mit der Bezeichnung "Name des *Netzwerkadapteradapters* zurücksetzen".)

 

