---
title: In- und Benutzeroberfläche
description: In diesem Thema wird das Benutzeroberflächenmodell beschrieben, das als iniveive Benutzeroberfläche (IUI) bezeichnet wird.
ms.assetid: d99dc30a-68e5-4b7a-8cbd-0ac77a90a354
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a16282248e1942070f5dc3e1418016657de2e84f39e1f8473eaedcbc0eeccbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589428"
---
# <a name="inductive-user-interface"></a>In- und Benutzeroberfläche

In diesem Thema wird das Benutzeroberflächenmodell beschrieben, das als iniveive Benutzeroberfläche (IUI) bezeichnet wird. Das IUI-Modell wird auch als inleiterive Navigation bezeichnet und schlägt vor, wie Softwareanwendungen vereinfacht werden können, indem Features in Bildschirme oder Seiten eingedrungen werden, die leicht zu erklären und zu verstehen sind. Dieses IUI-Modell ist in verschiedenen Microsoft-Projekten wie Microsoft Money 2000, den Applets der Windows-Systemsteuerung, verschiedenen Bildschirmen und Dialogfeldern in Microsoft Visual Studio 2010 und den Aufgabenbereichen in Microsoft Office.

-   [Introduction (Einführung)](#introduction)
-   [IUI in Aktion: Lösen eines allgemeinen Entwurfsproblems](#iui-in-action-solving-a-common-design-problem)
    -   [Das Problem: Software ist schwer zu verwenden](#the-problem-software-is-hard-to-use)
    -   [Benutzeroberfläche mit Vorsteuerabzug](#deductive-user-interface)
    -   [Eine Lösung: Inive Benutzeroberfläche](#a-solution-inductive-user-interface)
-   [Schritte zum Erstellen einer Benutzeroberfläche](#steps-for-creating-an-inductive-user-interface)
    -   [Schritt 1: Konzentrieren Sie jede Seite auf eine einzelne Aufgabe.](#step-one-focus-each-page-on-a-single-task)
    -   [Schritt 2: Status der Aufgabe](#step-two-state-the-task)
    -   [Schritt 3: Passen Sie den Inhalt der Seite für die Aufgabe an.](#step-three-make-the-pages-contents-suit-the-task)
    -   [Schritt 4: Anbieten von Links zu sekundären Aufgaben](#step-four-offer-links-to-secondary-tasks)
-   [Weitere Leitlinien](#additional-guidelines)
    -   [Verwenden konsistenter Bildschirmvorlagen](#use-consistent-screen-templates)
    -   [Machen Sie deutlich, wie die Aufgabe mit den Steuerelementen auf dem Bildschirm durchgeführt wird.](#make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen)
    -   [Bereitstellen einer einfachen Möglichkeit zum Abschließen einer Aufgabe und Starten einer neuen Aufgabe](#provide-screens-for-starting-tasks)
    -   [Machen Sie den nächsten Navigationsschritt offensichtlich](#make-the-next-navigational-step-obvious)
-   [Benutzerunterstützung](#user-assistance)
    -   [Primäre Unterstützung](#primary-assistance)
    -   [Sekundäre Unterstützung](#secondary-assistance)
-   [Anhang: Entwerfen und Testen von Microsoft Money 2000](#appendix-designing-and-testing-microsoft-money-2000)
    -   [Entwerfen und Testen von Money 2000](#designing-and-testing-money-2000)
    -   [Benutzerfreundlichkeitstests](#usability-tests)
    -   [Vergleich mit Websites](#comparison-with-web-sites)

## <a name="introduction"></a>Einführung

Die IUI ist ein Benutzeroberflächenmodell, das vorschlägt, wie Softwareanwendungen vereinfacht werden können, indem Features in Bildschirme oder Seiten zerlegt werden, die leicht zu erklären und zu verstehen sind. Microsoft hat dieses Modell in Money 2000 implementiert, einer großen kommerziellen Softwareanwendung. In formlosen Tests wird darauf hindeutet, dass Benutzer aufgaben in diesem Modell so schnell wie in herkömmlichen Schnittstellen ausführen können und dies möglicherweise einfacher finden.

Viele kommerzielle Softwareanwendungen enthalten Benutzeroberflächen, in denen ein Bildschirm eine Reihe von Steuerelementen zeigt, aber es dem Benutzer überlässt, den Zweck der Seite abzuleiten und die Steuerelemente zu verwenden, um diesen Zweck zu erreichen.

Die in diesem Dokument beschriebenen Prinzipien erfordern oder implizieren keine bestimmten festen Sätze von Entwürfen, Steuerelementen oder visuellen Elementen. Wie grafische Benutzeroberflächen im Allgemeinen lassen die Prinzipien in diesem Dokument viel Platz für Flexibilität und Kreativität im Design.

Die allgemeinen Prinzipien der inleitenden Benutzeroberfläche werden anhand von Beispielen aus Money 2000 demonstriert.

> [!IMPORTANT]
> Das allgemeine Konzept von IUI befindet sich in den Kinder. Designer, die diese Techniken verwenden, lernen und erfahren mehr darüber, während sie sie für ihre Software verwenden. Die Informationen in diesem Dokument werden im Laufe der Zeit weiterentwickelt, wenn die Forschung und das Wissen in diesem Bereich wächst. Dieses Thema bietet eine Einführung in IUI und nicht in einen festen, umfassenden Satz von Richtlinien.

 

## <a name="iui-in-action-solving-a-common-design-problem"></a>IUI in Aktion: Lösen eines allgemeinen Entwurfsproblems

In diesem Abschnitt wird ein häufiges Entwurfsproblem mit den heutigen Softwareprodukten erläutert und IUI als Technik zur Lösung des Problems erläutert.

### <a name="the-problem-software-is-hard-to-use"></a>Das Problem: Software ist schwer zu verwenden

Die meisten Software ist zu schwer zu verwenden. Diese Schlussfolgerung wird aus Benutzerfreundlichkeitstests, einem beweiserheblichen Beweis und persönlichen Erfahrungen von Softwaredesignern gezogen. Das Konzept der IUI wurde erstellt, indem forscht wurde, indem fundierte Erraten, was die aktuelle Software schwierig zu verwenden macht, und dann Lösungen vorgeschlagen wurden. Designer, die IUI verwenden, sollten sich auf die Kundenzufriedenheit verlassen, um den endgültigen Erfolg des Entwurfs zu bestimmen.

Die meisten aktuellen Softwareprodukte sind aus den folgenden allgemeinen Gründen schwer zu verwenden:

-   Benutzer scheinen kein angemessenes mentales Modell des Produkts zu erstellen.

    Beim Schnittstellenentwurf für die meisten aktuellen Softwareprodukte wird davon ausgegangen, dass Benutzer ein konzeptionelles Modell verstehen, das die Designer sorgfältig entworfen haben. Leider scheinen die meisten Benutzer nie ein mentales Modell zu erhalten, das gründlich und genau genug ist, um ihre Navigation zu leiten. Diese Benutzer sind wahrscheinlich sehr ausgelastet und mit Informationen überlastet. Sie haben nicht die Zeit, Energie oder den Wunsch, ein konzeptionelles Modell für ihre Software zu untersuchen.

-   Selbst viele Langzeitbenutzer können keine gängigen Prozeduren meistern.

    Designer wissen, dass neue Benutzer zunächst möglicherweise Probleme haben, aber erwarten, dass diese Probleme verschwinden, wenn Benutzer häufige Aufgaben erlernen. Benutzerfreundlichkeitsdaten geben an, dass dies häufig nicht der Fall ist. In einer Studie richten Forscher automatisierte Geräte ein, um Benutzer zu Hause zu videotapen. Die Bänder zeigten, dass Benutzer, die sich auf die aufgabe konzentrieren, nicht unbedingt die Prozedur bemerken, die sie folgen, und nicht aus der Erfahrung lernen. Wenn Benutzer das nächste Mal denselben Vorgang ausführen, können sie genau auf die gleiche Weise durch ihn stürzten.

-   Benutzer müssen hart daran arbeiten, die einzelnen Features oder Bildschirme zu finden.

    Die meisten Softwareprodukte sind für (die wenigen) Benutzer konzipiert, die ihr konzeptionelles Modell verstehen und über gängige Prozeduren verfügen. Für die Mehrheit der Kunden ist jedes Feature oder jede Prozedur ein frustrierendes, unerwünschtesZzle. Benutzer könnten davon ausgehen, dass diese Unzweisungen ein unvermeidbarer Kostenaufwand für die Verwendung von Computern sind, aber sie wären ohne diese Belastung sicherlich belastbarer.

Die beste Lösung für diese Probleme besteht in der Suche nach einer allgemeinen Strategie, um die Features von Softwareprodukten selbstverständlicher und selbsterklärender zu machen. Benutzer müssen in der Lage sein, ein Feature jedes Mal zu finden, wenn sie es benötigen, und dieses Feature jedes Mal verwenden können, wenn sie es verwenden möchten.

### <a name="deductive-user-interface"></a>Benutzeroberfläche mit Vorsteuerabzug

Die meisten Elemente in der Software erfordern heute, dass der Benutzer sie untersucht und ihr Verhalten ableiten muss, wie im folgenden Screenshot gezeigt.

![Screenshot eines Beispieleigenschaftendialogfelds.](images/iuiguidelines01.png)

Erfahrene Computerbenutzer, einschließlich Softwaredesignern, erkennen schnell, dass dieser Dialog es ihnen ermöglicht, eine Liste von Dingen zu verwalten. Sie verstehen, dass die Schaltflächen unter der Liste Informationen zu Listenelementen hinzufügen, entfernen und bereitstellen können. Beachten Sie jedoch, dass keines dieser Verhaltensweisen explizit im Dialog selbst angegeben wird.

Sehen Sie sich nun den Dialog aus der Sicht eines gelegentlichen Benutzers noch einmal an. Viele Benutzer fragen sich bei diesem Dialog: "Was soll ich damit machen?" Wenn das Dialogfeld angezeigt wird, muss der Benutzer anhalten und herausfinden, was als Nächstes zu tun ist. Zunächst muss der Benutzer daraus schließen, dass das große weiße Rechteck ein leeres Listenfeld ist, das mit Elementen gefüllt werden soll. Die kleine Textbezeichnung "Things" (Dinge) des Felds bietet einen ungenauen Hinweis. Einige Benutzer würden versuchen, in das Listenfeld ein tippen, da es wie ein Bearbeitungstextfeld aussieht.

Als Nächstes muss der Benutzer darausleiten, dass sich die Schaltflächen unter der Liste auf seinen Inhalt auswirken. Einige der Schaltflächen sind anfänglich deaktiviert, was eine weitere mögliche Ursache für Benutzerverwechslungen ist. Der Benutzer muss mit den Steuerelementen experimentieren, um zu erfahren, wie der Dialog funktioniert.

Der Benutzer kann auch andere Fragen stellen: "Wie viele Elemente sollte ich in die Liste stellen? Sollte ich Elemente in einer bestimmten Reihenfolge eingeben? Warum habe ich diesen Dialog von Anfang an erhalten? Wofür ist es?

Benutzer sind von ihren Zielen abgelenkt, wenn sie den Zweck eines Bildschirms und seine Verwendung herausfinden müssen. Dies stellt letztendlich einen Zeit- und Benutzerzufriedenheitspreis dar. Noch schlechter ist, dass Benutzer diese Kosten immer wieder bezahlen, wenn sie jedes Mal, wenn sie ein Feature verwenden, über die Schnittstelle raten.

Ein Bildschirm sollte einen Titel haben, der seinen Zweck eindeutig erklärt. Wenn Designer einen Bildschirm erstellen, ist es selten erforderlich, dass er einen eindeutigen Zweck hat. Stattdessen kann es einfach Teil eines größeren konzeptionellen Modells sein, das der Benutzer ableiten muss.

Studien zeigen, dass viele Benutzer selbst durch grundlegende Vorgänge in software verwirrend sind. Sie haben Schwierigkeiten damit, zu verstehen, was das Produkt für sie tun kann, wo sie einen Vorgang ausführen und wie dieser Vorgang durchgeführt werden kann, sobald sie ihn gefunden haben. Die Vereinfachung von Software durch grundlegende Änderungen ist eine leistungsstarke Möglichkeit, bestehende Kunden besser zu erfüllen und neue Benutzer zu gewinnen.

### <a name="a-solution-inductive-user-interface"></a>Eine Lösung: Inive Benutzeroberfläche

Als neue Methode zum Entwerfen von Software besteht das Ziel von IUI in der Reduzierung der Menge an unnentwegten Denken, die Benutzer tun müssen, um erfolgreich zwischen Teilen eines Produkts zu wechseln und seine Features zu nutzen. Das Wort iniveive stammt aus dem Verbinduzierten, was bedeutet, durch Einfluss oder Persuasion zu führen oder sich zu bewegen.

IUI ist eine Erweiterung der allgemeinen Weboberfläche. In der Webumgebung müssen Seiten einfach und aufgabenbasierte Seiten sein, da jede Information über eine relativ langsame Verbindung an einen Server gesendet werden muss. Der Server antwortet dann mit dem nächsten Schritt und so weiter. Ein gutes Webdesign bedeutet, sich auf eine einzelne Aufgabe pro Seite zu konzentrieren und die Navigation durch Seiten zu ermöglichen. Ebenso beginnt die intakte Navigation damit, die Aktivität auf jeder Seite auf eine einzelne primäre Aufgabe zu konzentrieren.

Mit einer gut entworfenen inintiviven Benutzeroberfläche können Benutzer zwei grundlegende Fragen beantworten, denen sie beim Anzeigen eines Bildschirms gegenüber stehen:

-   Was soll ich jetzt tun?
-   Wo gehe ich von hier aus, um meine nächste Aufgabe auszuführen?

Software, die gemäß diesen Prinzipien entwickelt wurde, beantwortet diese Fragen, indem sie mit einer grundlegenden Prämisse beginnt: Ein Bildschirm mit einem einzelnen, eindeutig angegebenen, expliziten Zweck ist einfacher zu verstehen als eine Seite ohne einen solchen Zweck. Wenn der Bildschirm leichter zu verstehen ist, ist es für den Benutzer einfacher zu wissen, was zu tun ist und wo er als Nächstes hingehen soll.

Diese grundlegende Prämisse kann in eine Reihe von vier Schritten zum Entwerfen von Software erweitert werden, die IUI verwendet:

-   Konzentrieren Sie sich auf jeden Bildschirm auf eine einzelne Aufgabe.
-   Geben Sie den Task an.
-   Passen Sie den Inhalt des Bildschirms an die Aufgabe an.
-   Stellen Sie Links zu sekundären Aufgaben zur Verfügung.

Dieses Dokument beschreibt zwar allgemeine Prinzipien von IUI, veranschaulicht diese Prinzipien jedoch auch in Aktion, indem Beispiele aus Money 2000 und anderer Software gezeigt werden. Sie sollten sich diese Beispiele als bestimmte Ausdrücke der IUI und nicht als striktes Implementierungsmodell überlegen.

Zusätzlich zu den vier oben aufgeführten Schritten können Sie Ihre Schnittstelle stärken, indem Sie diese fünf Richtlinien befolgen:

-   Verwenden Sie konsistente Bildschirmvorlagen.
-   Stellen Sie Bildschirme zum Starten von Aufgaben zur Verfügung.
-   Machen Sie deutlich, wie die Aufgabe mit den Steuerelementen auf dem Bildschirm durchgeführt wird.
-   Stellen Sie eine einfache Möglichkeit zum Abschließen einer Aufgabe und zum Starten einer neuen Aufgabe zur Verfügung.
-   Machen Sie den nächsten Navigationsschritt offensichtlich.

### <a name="processes"></a>Prozesse

Viele Aufgaben erfordern, dass Benutzer durch eine Reihe von Bildschirmen navigieren. Benutzer, die eine Aufgabe ausführen, können auf einen Link zu einer sekundären Aufgabe klicken, die sich von der Abfolge der Bildschirme entfernt, aus denen die primäre Aufgabe besteht. Wenn der Benutzer die sekundäre Aufgabe abgeschlossen hat, sollte es eine einfache Möglichkeit geben, den Benutzer direkt zum Verzweigungspunkt in der ursprünglichen Aufgabe zurückzukehren. Benutzer haben wahrscheinlich Probleme mit herkömmlichen  Navigationssteuerelementen wie Denk- und Vorwärtsschaltflächen, um zu dem Ort zurückzukehren, an dem sie gestartet wurden. 

Um diese Möglichkeit zu bieten, definiert IUI ein Navigationskonzept, das als Prozess bezeichnet wird, einen Bildschirm oder eine Reihe von Bildschirmen, die eine Aufgabe ausführen. Ein Prozess fungiert als eine Art Navigationsunterroutine. Benutzer können einen Prozess starten, die Bildschirmreihe durcharbeiten und dann auf der letzten Seite auf die Schaltfläche "Fertig" klicken, um schnell zu der Seite zurückzukehren, auf der sie den Prozess begonnen haben.

## <a name="steps-for-creating-an-inductive-user-interface"></a>Schritte zum Erstellen einer Benutzeroberfläche

In diesem Abschnitt werden die vier Schritte ausführlich beschrieben, die Sie zum Erstellen einer IUI verwenden können.

### <a name="step-one-focus-each-page-on-a-single-task"></a>Schritt 1: Konzentrieren Sie jede Seite auf eine einzelne Aufgabe.

Der erste Schritt beim Entwerfen einer IUI besteht im Verwenden eines Features oder einer Reihe von Features und deren Unterbricht in separate Bildschirme. Jeder Bildschirm sollte sich auf eine einzelne Aufgabe konzentrieren, die als primäre Aufgabe des Bildschirms bezeichnet wird.

Diese Idee klingt einfach, aber es folgen nur wenige Anwendungen. Die meisten Anwendungen stellen einen Bildschirm vor, auf dem alle zugehörigen Features erreicht werden. Bei diesem Entwurf müssen Benutzer herausfinden, was sie tun können und wie sie dies tun.

Die primäre Aufgabe kann entweder spezifisch oder offen beendet sein. In einem Meine Finanzen-Programm kann eine bestimmte Aufgabe z. B. "Wählen Sie die Rechnung aus, die Sie bezahlen möchten", während eine offene Aufgabe "Überprüfen der Leistung Ihrer Investitionen" sein kann.

Die primäre Aufgabe muss für den Benutzer sinnvoll sein, anstatt eine Reflektion eines Implementierungsdetails oder eines anderen abstrakten Konzepts zu sein. Die Aufgabe sollte etwas sein, was Benutzer möglicherweise tun möchten, vorzugsweise in eigenen Worten beschrieben.

### <a name="example"></a>Beispiel

In diesem Abschnitt werden zwei verschiedene Versionen von Money verglichen. Die Beispiele zeigen sehr ähnliche Features, mit denen Benutzer Finanzkonten anzeigen und verwalten können.

Das IUI-Modell wurde während der Erstellung von Money 2000 entwickelt, einer Anwendung für die Verwaltung persönlicher Finanzen. Money 2000 ist die achte Hauptversion des Produkts. Money 2000 ist ein umfangreiches Windows mit deutlich mehr als einer Million Codezeilen.

Money 2000 ist eine Webanwendung im Webstil. Es handelt sich nicht um eine Website, sondern es gibt viele Attribute für Websites. Die Benutzeroberfläche besteht aus Vollbildseiten, die in einem freigegebenen Frame angezeigt werden, mit Tools zum Zurück- und Vorwärtsschalten durch einen Navigationsstapel. Auf dieser Grundlage fügt Money 2000 eine Reihe neuer Benutzeroberflächenkonventionen hinzu, die eine strukturiertere Benutzeroberfläche schaffen.

Obwohl IUI zum ersten Mal im Webdesign von Money 2000 verwendet wurde, kann es auch mit herkömmlichen Schnittstellenelementen wie Fenstern und Dialogfeldern verwendet werden.

In Money 99 haben Benutzer häufig eine Vielzahl von Aufgaben auf einem einzelnen Bildschirm ausgeführt. Der folgende Screenshot zeigt z. B. den **Konto-Manager,** der alle kontobezogenen Features in Money 99 auf einem einzigen Bildschirm angezeigt hat.

![Screenshot des Konto-Managers in money 99.](images/iuiguidelines02.png)

Auf diesem Bildschirm werden eine allgemeine Aufgabe, die Navigation zu einem Konto, sowie selten auftretende Aufgaben wie das Erstellen und Löschen von Konten gegruppen. Keine dieser spezifischen Aufgaben wird direkt im Titel des Bildschirms ausgedrückt: **Account Manager**. Viele Benutzer finden diesen Bildschirm möglicherweise so schwierig wie das Beispieldialogfeld in Abbildung 1. In beiden Fällen muss der Benutzer den Zweck des Bildschirms und seine Verwendung ableiten.

Money 2000, das IUI folgt, bietet eine nahezu identische Reihe von kontobezogenen Features, stellt sie jedoch auf zwei separaten Bildschirmen zur Seite. Der folgende Screenshot zeigt den ersten dieser Bildschirme, der sich ausschließlich darauf konzentriert, den Benutzer zur Auswahl eines Kontos zu bringen.

![Screenshot des Bildschirms für die Kontoauswahl in money 2000.](images/iuiguidelines03.png)

Der Money 2000-Bildschirm enthält ungefähr die gleiche Anzahl visueller Elemente wie der frühere Money 99-Bildschirm, aber die Seite konzentriert sich jetzt vollständig darauf, den Benutzer zur Auswahl eines Kontos zu bringen. Beispielsweise musste ein Benutzer in der Money 99-Version zwei Klicks zum Öffnen eines Kontos machen: eins, um es auszuwählen, und ein weiteres zum Auswählen des Open-Vorgangs. In der Money 2000-Version klickt ein Benutzer nur auf ein Konto, um es zu öffnen, sodass ein einzelner Klick ausreichen kann. Auf diese Weise wird die Anzahl der Klicks, die zum Ausführen einer allgemeinen Aufgabe erforderlich sind, häufig reduziert, obwohl die Anzahl der Bildschirme zunehmen kann.

Gelegentlich möchten Benutzer ein Konto hinzufügen oder entfernen. Um diese Aufgabe in Money 2000 auszuführen, navigieren Benutzer zu einem zweiten Bildschirm (wie im folgenden Screenshot gezeigt), der sich auf das Einrichten von Konten konzentriert.

![Screenshot des Kontoeinrichtungsbildschirms in money 2000.](images/iuiguidelines04.png)

Der Zweck jedes Bildschirms ist in der IUI-Version von Money 2000 eindeutiger. Darüber hinaus verfügt jeder Bildschirm über mehr Platz, um seinen Zweck zu erfüllen. Beispielsweise könnte der Money 99-Konto-Manager der  Schaltfläche Konto löschen sehr wenig Platz geben, da sie im Vergleich zu den anderen Befehlen auf dem Bildschirm nur selten verwendet wurde.  Im Gegensatz dazu kann der Bildschirm für die Kontoeinrichtung in Money 2000 diesen Befehl an prominenterer Stelle anzeigen, wodurch er besser erkennbar und selbsterklärender wird.

### <a name="what-is-a-single-task"></a>Was ist eine einzelne Aufgabe?

Woher wissen Sie, ob sich ein Bildschirm wirklich auf nur eine Aufgabe konzentriert? Ein Bildschirm, der viele Aufgaben unterstützt, kann so erklärt werden, dass er nur einen Zweck hat, wenn dieser Zweck abstrakt genug ist. Hier ist eine Faustregel: Ein Bildschirm ist auf einen Zweck ausgerichtet, wenn der Designer diesen Zweck mit einem präzisen, aussagekräftigen und natürlich klingenden Bildschirmtitel ausdrücken kann.

Die Designer von Money 2000 haben in Betracht gezogen, diese Bildschirme **zu** durchbrechen ( Wählen Sie ein zu verwendende Konto aus, und richten Sie Ihre Konten **in Money** ein) weitere Bildschirme ein. Da jeder Bildschirm jedoch bereits über einen präzisen, aussagekräftigen und natürlich klingenden Titel verfügt, waren die Designer der Meinung, dass die Bildschirme ausreichend fokussiert waren. Wenn Sie sich beim Entwerfen eines Bildschirms keinen eindeutigen und einfachen Titel denken können, versuchen Sie wahrscheinlich, zu viel auf dem Bildschirm zu erreichen.

### <a name="step-two-state-the-task"></a>Schritt 2: Status der Aufgabe

Jeder Bildschirm sollte mit einer präzisen und expliziten Anweisung seiner primären Aufgabe betitelt werden. Dies kann eine direkte Anweisung ("Wählen Sie das Konto aus, das Sie ausgleichen möchten") oder eine Frage sein, die der Benutzer beantworten soll ("Welches Konto möchten Sie ausgleichen?).

Dies ist ein weiteres einfach klingende Prinzip, das häufig nicht verwendet wird. Frühere Versionen von Money hatten z. B. Bildschirme mit Titeln wie **Online Financial Services Manager** und Balance **Account**. Benutzer mussten den Zweck und das Verhalten dieser Bildschirme von der Anordnung und den Bezeichnungen ihrer Steuerelemente ableiten.

Der Titel des Bildschirms oder der Seite ist sehr wichtig. Unabhängig davon, ob das Produkt Fenster, Seiten im Webstil, Dialoge oder einen anderen Entwurf verwendet, darf für den Titel kein Bildlauf ausgeführt werden.

### <a name="usable-screens-have-clear-titles"></a>Nutzbare Bildschirme haben klare Titel

Bildschirme, die viele Aufgaben ausführen, erfordern abstrakte oder komplexe Titel. Auf dem in Abbildung 2 gezeigten Bildschirm Money 99 konnte der Benutzer beispielsweise sowohl zu Konten navigieren als auch Konten einrichten. Dieser Seite wurde der abstrakte Titel "Konto-Manager" gegeben, um beide Zwecke zu erfassen. Benutzer haben vielleicht ideenreich, was eine Seite "Konto-Manager" tun könnte, aber sie werden vielleicht nicht merken, dass die häufigste Aufgabe für diesen Bildschirm einfach die Auswahl eines Kontos war.

Einige Bildschirme oder Befehle haben abstrakte Zwecke, die keine eindeutigen Titel vorschlagen. Für diese Bildschirme können Designer Namen auswählen, die absichtlich ungenau sind, z. B. "Einstellungen;", mit Bezeichnungen wie "QuickStep; " oder einem Jargon, der Implementierungsdetails ("Datenbankkompaktion") preis gibt. Diese Arten von Namen sind für Benutzer oft verwirrend oder irreführend. Darüber hinaus sind solche Namen in der Regel Nomen, die nicht die Aktion ausdrücken, die der Benutzer ausführen möchte, was die Verwirrung erhöht.

Bildschirmtitel und andere Namen werden häufig erst am Ende des Entwurfsprozesses bestimmt. Designer fordern Writer häufig auf, einen passenden Namen für einen Bildschirm zu finden, nachdem er entworfen und codiert wurde. An diesem Punkt gibt es keineRlei Regung, wenn kein guter Name gefunden werden kann. Daher muss sich das Team möglicherweise auf namen, die nicht eindeutig sind, begleichen. Die Lösung für diesen Fehler ist, dass Designer frühzeitig im Entwurfsprozess über Klarheit in Bildschirmfunktionen und Titeln nachdenken.

Bildschirmfunktionen und Titel sollten sich auf die gängigsten Aufgaben konzentrieren, die von Kunden ausgeführt werden. Designer sind oft versucht, riesige Mengen an Funktionalität zur Verfügung zu stellen, um die größte Anzahl von Kunden zu erfüllen, zusammen mit den Wünschen des Entwurfsteams selbst. Zusätzliche Features erhöhen jedoch immer die Komplexität und andere Kosten.

### <a name="screen-title-indicates-design-clarity"></a>Bildschirmtitel gibt Entwurfsklarheit an

Im IUI-Modell wählen die Designer die Bildschirmtitel in den frühesten Phasen des Entwurfsprozesses aus. Anstatt einen Titel zu verwenden, um die Art und Weise zu rechtfertigen, wie der Bildschirm funktioniert, wird der Titel verwendet, um zu bestimmen, ob der Bildschirm sinnvoll ist. Wenn kein geeigneter Titel gefunden wird, wird das Feature neu gestaltet. Wenn kein Entwurf einen eindeutigen und präzisen Titel zulasst (d. h., wenn es keine Möglichkeit gibt, das Feature zu erklären), können die Designer das Feature verabbruchen. Vergleichen Sie in den folgenden Screenshots den Zahlungsbildschirm für Geld 99 auf der linken Seite, der eine statische Bezeichnung für die Seite ("Upcoming Bills & 2000") und den entsprechenden Bildschirm Money 2000 auf der rechten Seite mit einem expliziten Titel ("Klicken Sie auf die Rechnung, die Sie bezahlen möchten"):

![Screenshot, der einen statischen Titel in money 99 und einen aktiven Titel in money 2000 zeigt.](images/iuiguidelines05.png)

Ein Bildschirmtitel, bei dem es sich natürlich nur um einen Ausdruck oder Satz handelt, ist einfacher zu ändern als ein Entwurf oder Code. Trotz dieser Tatsache hat die Erfahrung mit IUI gezeigt, dass die frühe Verandruckung auf einem Klarbildschirmtitel bessere Entwürfe erzeugt. Titel sollten mit Eingaben aus den Mitgliedern des Benutzerbildungs- und Benutzerfreundlichkeitsteams sowie von den Produktdesignern ausgewählt werden.

Teammitglieder versuchen manchmal, diese Entscheidung zurückgestellt zu haben, vorausgesetzt, kunden werden ihr Verständnis des Zwecks eines Bildschirms teilen. Wenn Sie jedoch gezwungen werden, eine klare und präzise Aussage zu diesem Zweck zu geben, werden häufig Meinungsunterschiede deutlich. Durch das Auflösen dieser Unterschiede und die frühe Auswahl eines Titels können Entwurfsdiskussionen reibungsloser verlaufen.

Sobald ein Titel ausgewählt wurde, sollten Sie ihn nicht als unveränderlich betrachten. Designer verfeinern bildschirmtitel wahrscheinlich im Laufe der Zeit, wie bei jedem Design. Der erste ausgewählte Titel sollte jedoch so stark sein, wie es in dieser Phase der Entwicklung möglich ist.

### <a name="guidelines-for-choosing-screen-titles"></a>Richtlinien für die Auswahl von Bildschirmtiteln

In diesem Abschnitt wird eine einfache Technik zum Auswählen guter Bildschirmtitel beschrieben. Um diese Technik zu verwenden, stellen sich Designer vor, dass ein Freund fragt: "Wofür ist dieser Bildschirm?". und dann eine klare, hilfreiche Antwort erhalten, die den Satz "This is the screen where you?" (Dies ist der Bildschirm, auf dem Sie sich befindet) vervollständigt. Die Wörter, die den Satz vervollständigen, werden zum Bildschirmtitel.

Während der Entwicklung von Money 2000 haben die Dokumentationsautoren des Teams Bildschirmtitelrichtlinien erstellt, um Qualität und Konsistenz sicherzustellen. Diese Richtlinien vorgeschlagenen beispielsweise Titel, die Verben verwendet und als Fragen oder direkte Anweisungen formuliert wurden. Designer haben statische Namen vermieden, die mehr Abstraktion ermöglichten und möglicherweise ungenau sind.

Zur Vereinfachung von Titeln haben Designer zusammengesetzte Sätze vermieden und versucht, konversationssprachliche Sprache zu verwenden, um umknachige Begriffe und Fachbegriffe zu vermeiden. Wenn Designer die Aufgabe nicht beschreiben können, ohne auf Konjunktionen ("und", "oder") zurück zu schreiten, versucht der Bildschirm wahrscheinlich, mehr als eine Aufgabe auszuführen, und es ist weniger wahrscheinlich, dass der Benutzer sofort verstehen kann, was zu tun ist.

Selbst wenn ein Titel sorgfältig ausgewählt wird, ist der Titelbereich möglicherweise zu klein, um eine komplexe Aufgabe angemessen zu erklären. Um dieses Problem zu beheben, können Sie oben im Inhaltsbereich des Bildschirms einen kurzen beschreibenden Absatz hinzufügen, der die Aufgabe beschreibt.

Die folgende Tabelle enthält einige Beispiele für Bildschirmtitel in Money 99 und Titel für denselben oder verwandten Bildschirm in Money 2000.



| Bildschirmtitel in Money 99             | Neue Bildschirmtitel in Money 2000                         | Kommentar                                         |
|---------------------------------------|---------------------------------------------------------|-------------------------------------------------|
| **Konto-Manager**                   | **Auswählen eines Kontos** **Einrichten Ihrer Konten**<br/> | Statischer Titel wurde in aktive Titel geändert.          |
| **Kontodetails**                   | **Ändern der Kontoeinrichtung**                                | Statischer Titel wurde in einen aktiven, spezifischen Titel geändert. |
| **Zahlungskalender**                  | **Bezahlen einer Rechnung**                                          | Titel des Titels wurde deskriptiv gemacht.                   |
| **Online Financial Services Manager** |                                                         | Die Seite ist nach dem Umgestalten nicht mehr erforderlich.                 |



 

### <a name="making-the-screen-title-prominent"></a>So wird der Bildschirmtitel deutlich

Sobald Sie sich mit einem nützlichen Bildschirmtitel begnzeichnet haben, müssen Sie sicherstellen, dass die Aufmerksamkeit des Benutzers darauf gezogen wird. Einige Studien haben ergeben, dass Benutzer nur selten Anweisungstext lesen. Um dieses Problem zu beheben, sollten Bildschirmtitel so entworfen werden, dass sie gut und ansprechend sind, um die Aufmerksamkeit des Benutzers zu gewinnen. Der visuelle Entwurf des Bildschirms sollte den Benutzer darüber informieren, dass der Titel das Wichtigste ist, das gelesen werden muss.

### <a name="step-three-make-the-pages-contents-suit-the-task"></a>Schritt 3: Passen Sie den Inhalt der Seite für die Aufgabe an.

Beim Erstellen von Software, die den IUI-Richtlinien entspricht, besteht die härteste Entwurfsarbeit in der Regel darin, Features in Bildschirme oder Seiten zu unterbrechen. Der nächste Schritt besteht darin, zu bestimmen, welche Steuerelemente auf jedem Bildschirm verwendet werden, um die primäre Aufgabe zu erfüllen. Diese Steuerelemente machen den Inhalt der Seite aus, in dem der Benutzer die Arbeit erledigt. Titel und Inhalt des Bildschirms sind zwei Hälften eines Dialogs zwischen dem Programm und dem Benutzer. Der Titel stellt die Frage des Programms oder gibt eine Anweisung, und der Benutzer antwortet über die Benutzeroberfläche des Bildschirms.

Wenn der Bildschirmtitel klar und einfach ist, ist das Entwerfen des Bildschirms in der Regel unkompliziert. Beispielsweise hat einer der oben gezeigten Money 2000-Bildschirme den Titel "Wählen Sie ein zu verwendende Konto aus". Angesichts dieses Titels sollte der Bildschirm natürlich eine einfache Liste von Konten enthalten, aus der der Benutzer auswählen kann. Ein weiterer Money 2000-Bildschirm hat den Titel "Check the items to include in your taxes". Dieser Bildschirm enthält natürlich eine Checkliste mit Elementen.

Benutzer sollten leicht herausfinden können, wie Steuerelemente verwendet werden, um die primäre Aufgabe des Bildschirms zu erreichen. Wenn Benutzern die Auswahl eines Kontos mitgeteilt wird und sie auf dem Bildschirm nach einer Liste von Konten suchen können, bestätigen sie ihr Verständnis der Aufgabe. Dies erhöht die Wahrscheinlichkeit, dass Benutzer erfolgreich sind, was auch ihr Vertrauen in die Ausführung anderer Aufgaben erhöht.

### <a name="screen-content-areas"></a>Bildschirminhaltsbereiche

Die genaue Position und Form der Bildschirminhaltsbereiche hängt vom Design der Software ab. In Money 2000 befindet sich der Bildschirminhaltsbereich alles unterhalb des Bildschirmtitels und rechts neben der Aufgabenliste. Dieser Bereich kann auf langen Bildschirmen scrollen. Einige nicht wichtige Inhalte werden möglicherweise auch im Statusbereich unter der Aufgabenliste angezeigt.

Designer können die Primäre Aufgabe des Bildschirms in einem Absatz am oberen Ende des Inhaltbereichs näher erläutert. Benutzer müssen diesen Text nie lesen, aber sie finden ihn möglicherweise hilfreich. Viele Benutzer können dies überspringen und den Bildschirm trotzdem erfolgreich verwenden. Im Gegensatz zum Titel kann diese Beschreibung wegscrollen, wenn der Bildschirm scrollbar ist. Weitere Informationen finden Sie unter [Richtlinien für die Auswahl von Bildschirmtiteln.](#guidelines-for-choosing-screen-titles)

Wenn Designer möchten, dass auf einer Seite nicht wichtige Erinnerungen, Warnungen oder andere Statusinformationen angezeigt werden, kann sie links neben dem Hauptinhaltsbereich unter der Aufgabenliste auf der linken Seite des Bildschirms angezeigt werden. Funktionell ist dieser Statusbereich eine zusätzliche Region für Bildschirminhalte. Dieser Bereich ist nicht gut genug, um wichtige Steuerelemente zu enthalten.

### <a name="provide-a-clear-exit-from-the-page"></a>Stellen Sie eine klare Beendigung der Seite zur Verfügung.

Nach dem erfolgreichen Abschließen einer Aufgabe steht der Benutzer vor einem anderen Problem: wann und wie der Bildschirm verlassen wird. Bei Bildschirmen, deren Primäre Aufgabe die Navigation ist, wird der Benutzer durch Ausführen der Aufgabe selbst zum nächsten Bildschirm bewegt. Auf anderen Bildschirmen kann es für den Benutzer schwieriger sein, zu wissen, wie der Vorgang fortgesetzt werden soll. Beispielsweise benötigt der Benutzer auf einem Bildschirm, auf dem er aufgefordert wird, Informationen in Felder ein geben, Hilfe, um herauszufinden, wann und wie er weiterfänden soll. Auf solchen Seiten ist es häufig hilfreich,  eine klare Schaltfläche Weiter oder Fertig an einem konsistenten Ort zu bieten. 

Benutzerfreundlichkeitsstudien haben gezeigt, dass Benutzer solche Schaltflächen bevorzugen, auch wenn globale Navigationsschaltflächen wie Die Schaltflächen "Zurück" oder **"Start"** auf einer Symbolleiste verfügbar sind.  Benutzer sind häufig auf Bildschirmen ohne klares Beenden zu sehen, sogar bildschirme, deren einziger Zweck es ist, Informationen zum Lesen zur Verfügung zu stellen.

Weitere Informationen zu diesem [](#provide-screens-for-starting-tasks) Thema finden Sie unter Bereitstellen einer einfachen Möglichkeit zum Abschließen einer Aufgabe und Starten einer neuen Aufgabe im Abschnitt Zusätzliche Richtlinien.

### <a name="step-four-offer-links-to-secondary-tasks"></a>Schritt 4: Anbieten von Links zu sekundären Aufgaben

Der letzte Schritt beim Entwerfen eines Bildschirms ist das Bereitstellen von Links zu sekundären Aufgaben, bei denen es sich um Features handelt, die die primäre Aufgabe nicht direkt ausführen, sondern mit dem Bildschirm verknüpft sind. Wenn die primäre Aufgabe auf einem Bildschirm beispielsweise das Schreiben eines Buchstabens ist, können sekundäre Aufgaben auf diesem Bildschirm darin besteht, eine Adressenadresse zu suchen oder einen Umschlag zu drucken.

Sekundäre Aufgaben können Dialogfelder öffnen, die visuelle Darstellung des Bildschirminhalts ändern oder den Benutzer zu einem anderen Bildschirm navigieren. Eine sekundäre Aufgabe kann indirekt die primäre Aufgabe ausführen oder verloren gegangene Benutzer an den Gesuchten umleiten.

Wenn es sich bei einer Seite um eine Konversation zwischen dem Computer und dem Benutzer handelt, kann der Benutzer mit einer sekundären Aufgabe die aktuelle Frage des Computers ignorieren und den Computer stattdessen bitten, etwas anderes zu tun. Stellen Sie sich beispielsweise dieses Dialogfeld vor: Computer: "Welche Rechnung möchten Sie bezahlen?" Benutzer: "Eigentlich möchte ich eine Rechnung finden, die ich eine Weile bezahlt habe."

Einige Bildschirme in Ihrem Produkt haben keine sekundären Aufgaben, während andere mehrere haben. Sie sollten vermeiden, eine lange Liste von Aufgaben zu erstellen, deren Überprüfung für den Benutzer wahrscheinlich schwierig sein wird. Wenn ein Bildschirm über eine relativ lange Liste sekundärer Aufgaben verfügt, sollten die häufigsten Aufgaben zuerst platziert, in einem separaten Abschnitt gruppiert oder anderweitig visuell hervorgehoben werden.

Die Liste sollte nicht alle möglichen sekundären Aufgaben enthalten, solange der nächste Navigationsschritt offensichtlich ist. Anstatt viele sekundäre Aufgaben zu bieten, kann ein Bildschirm sekundäre Aufgaben bereitstellen, die zu untergeordneten Seiten navigieren, die weitere Aufgaben auflisten.

### <a name="visual-design-of-secondary-tasks"></a>Visueller Entwurf sekundärer Aufgaben

Sekundäre Aufgaben sollten an einer untergeordneten Position auf dem Bildschirm aufgeführt werden, wo sie bei Bedarf zugänglich sind, den Benutzer jedoch nicht von der primären Aufgabe ablenken. Wenn Sie diese Liste an einer konsistenten Position auf jedem Bildschirm platzieren, können Benutzer die Liste schnell finden, wenn sie sie benötigen.

Wenn Sie die Liste der sekundären Aufgaben auf der linken Seite des Bildschirms anzeigen, sollte die Liste selbst weder scrollbar  sein noch mit der Seite scrollen, wie im folgenden Screenshot des Bildschirms "Zahlung in Rechnung" von Money 2000 gezeigt.

![Screenshot des Bildschirms zur Zahlung der Rechnung in Money 2000.](images/iuiguidelines07.png)

## <a name="additional-guidelines"></a>Weitere Leitlinien

In diesem Abschnitt werden fünf nützliche Richtlinien zum Erstellen einer IUI gemäß den vier Im vorherigen Abschnitt beschriebenen Schritten beschrieben.

### <a name="use-consistent-screen-templates"></a>Verwenden konsistenter Bildschirmvorlagen

Beim Entwerfen von Software, die dem IUI-Modell folgt, sollten Sie eine Vorlage erstellen, die als Leitfaden für jeden Bildschirm verwendet werden soll. Das in- und inleiterische Modell schreibt nicht vor, dass Sie eine bestimmte Vorlage verwenden. Es gibt viele mögliche Variationen, die einem invarianten Entwurf entsprechen können. Ihr Produkt benötigt möglicherweise nur eine Vorlage für alle Bildschirme, oder Sie können mehrere verschiedene Vorlagen für verschiedene Zwecke erstellen.

Eine gute Vorlage ermöglicht es einem neuen Benutzer, schnell zu verstehen, wie die Bildschirme des Produkts funktionieren. Die konsistente Verwendung der Vorlage auf den Bildschirmen des Produkts bietet einen guten Benutzeroberflächenfluss von Bildschirm zu Bildschirm. Da Benutzer lernen, zu erwarten, dass dieselben Elemente an denselben Stellen angezeigt werden, können sie jeden neuen Bildschirm schneller scannen und verwenden.

### <a name="provide-screens-for-starting-tasks"></a>Bereitstellen von Bildschirmen zum Starten von Aufgaben

Produkte, die mit IUI entworfen wurden, verwenden häufig spezielle Bildschirme, um Benutzer bei Aufgabengruppen zu starten. Diese Bildschirme werden als Aktivitätsseiten bezeichnet, da sie verwandte Gruppen von allgemeinen Aufgaben organisieren. Aktivitätsseiten stellen einen Ausgangspunkt für Benutzer dar. Auf einer Aktivitätsseite werden in der Regel Links zu anderen Seiten angezeigt, auf denen der Benutzer die Arbeit tatsächlich erledigt. Aktivitätsseiten fragen den Benutzer: "Was möchten Sie jetzt tun?" und stellen eine Liste möglicher Antworten vor. Aktivitätsseiten können einer speziellen Vorlage folgen, damit Benutzer sie erkennen können.

Eine Aktivitätsseite ist eine gute Standardstartseite für ein Produkt. Wenn Benutzer eine Anwendung starten, haben sie im Allgemeinen eine Vorstellung von der Aufgabe, die sie ausführen möchten. Der Grund für den Start des Produkts ist in der Regel eine kleine Anzahl sehr häufiger Aufgaben. Die Standardstartseite des Produkts erkennt dies, indem sie deutlich macht, wie allgemeine Aufgaben beginnen.

Die Money 2000-Startseite ist ein Beispiel für eine Aktivitätsseite.  Standardmäßig wird Benutzern dieser Bildschirm angezeigt, auf dem der Zugriff auf allgemeine Finanzaufgaben wie das Bezahlen einer Rechnung und das Ausgleichen eines Kontos angezeigt wird, wenn sie die Anwendung starten.

Der folgende Screenshot zeigt die Money **2000-Startseite.**

![Screenshot der Money 2000-Homepage. Eine Aktivitätsseite, die einige allgemeine Aufgaben auflistet und Links zu Aufgabensätzen auf anderen Seiten enthält.](images/iuiguidelines08.png)

Da Money viele finanzielle Features bietet, passen nur die gängigsten Finanzaufgaben auf die **Startseite.** Für alle anderen Aufgaben ist die **Startseite mit** einem subsidiären Satz von Aktivitätsseiten verknüpft, die als Finanzcenter bezeichnet werden. Jeder Hauptbereich von Money bietet einen Finanzplatz. Auf diesen Bildschirmen wird die nächste Aufgabenebene angezeigt, die als Ausgangspunkt für alle Features in jedem Bereich dient.

Beispielsweise enthält der Bereich **Geldsteuer** die steuerbezogenen Features des Produkts. Der **Bereich** Steuern enthält Links zu diesen Features auf einer Seite des **Steuercenters,** wie im folgenden Screenshot gezeigt.

![Screenshot der Steuercenterseite "Money 2000". ](images/iuiguidelines09.png)

Eine Aktivitätsseite kann auch viel einfacher sein, wenn weniger Optionen verfügbar sind. Der folgende Screenshot zeigt, wie eine Aktivitätsseite zum Verwalten Windows verwendet werden kann.

![Screenshot einer Money 2000-Aktivitätsseite zum Verwalten von Windows-Benutzerkonten. ](images/iuiguidelines10.png)

### <a name="make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen"></a>Machen Sie deutlich, wie die Aufgabe mit den Steuerelementen auf dem Bildschirm durchgeführt wird.

Die beste Möglichkeit, diese Richtlinie zu befolgen, besteht in der Auswahl eines geeigneten Bildschirmtitels und der Beschränkung des Bereichs primärer Aufgaben auf die am häufigsten zu verwendenden Aufgaben. Wenn Sie einen eindeutigen Titel und Zweck für die Seite erreicht haben, ist es einfach, die richtigen Steuerelemente zu wählen.

### <a name="provide-an-easy-way-to-complete-a-task-and-start-a-new-one"></a>Bereitstellen einer einfachen Möglichkeit zum Abschließen einer Aufgabe und Starten einer neuen Aufgabe

Das letzte Hindernis, mit dem ein Benutzer auf einem Bildschirm konfrontiert wird, besteht in der Ermittlung, wann und wie er das Bild verlassen soll. Der Benutzer verlässt den Bildschirm in der Regel durch Klicken auf einen Link oder ausführen eines Befehls, der zu einem anderen Bildschirm navigiert. Diese Links können im Inhaltsbereich des Bildschirms, in der Aufgabenliste oder auf Navigationssymbolleisten angezeigt werden. Benutzer können einen Bildschirm auch verlassen, indem sie die aktuelle Datei oder die Anwendung selbst schließen.

Die Aufgabe auf einigen Bildschirmen besteht darin, sich auf einen Vorgang vorzubereiten, den der Benutzer bestätigen oder abbrechen muss. Solche Bildschirme bieten in der Regel einen Link, der den Vorgang ausführt und ausführt, und einen anderen Link, der abgebrochen wird. Wenn der Benutzer diese Optionen ignoriert und auf einen anderen Link klickt, sollte das Programm die weniger destruktive Option ausführen. Bildschirme sollten angeben, was geschieht, wenn der Benutzer diesen Pfad verwendet. Sie können die Links ausdrücken, um dies offensichtlicher zu machen. Eine Commitschaltfläche mit der Bezeichnung "Änderungen speichern" bedeutet beispielsweise, dass die auf dem Bildschirm vorgenommenen Änderungen erst wirksam werden, wenn auf diese Schaltfläche geklickt wird.

Auch wenn Benutzer jederzeit verlassen können, können Sie trotzdem einen Link anbieten, der einen offensichtlichen Verlassen der Seite vorschlägt. Dasselbe gilt für Seiten, auf denen nur statische Informationen angezeigt werden. Weitere Informationen zu diesem Thema finden Sie im Abschnitt Bereitstellen eines eindeutigen [Exits von der Seite](#provide-a-clear-exit-from-the-page).

### <a name="starting-and-completing-processes"></a>Starten und Abschließen von Prozessen

Im Rahmen dieses Artikels sind Prozesse Techniken für den Umgang mit Aufgaben, die den Benutzer auf mehrere Bildschirme bringen.

Angenommen, ein Benutzer klickt auf einen Link in der Inhalts- oder Aufgabenliste eines Bildschirms und wird auf einen anderen Bildschirm aufgenommen. Diese Seite kann wiederum die erste einer Reihe von Bildschirmen sein, die ein Gesamtergebnis erzielen. Am Ende dieser Bildschirmreihe möchte der Benutzer zu dem Bildschirm zurückkehren, der dem Prozess vorausgegangen ist. Es gibt mindestens zwei Möglichkeiten, wie der Benutzer zurückkommen kann? Wenn Sie wiederholt Schaltfläche "Zurück" oder zur Startseite zurückkehren und von dort aus navigieren? aber keine dieser Methoden ist offensichtlich oder natürlich. Die meisten Benutzer erwarten, dass sie auf dem letzten Bildschirm eine Schaltfläche finden, die sie direkt auf den ursprünglichen Bildschirm zurückgibt.

Das IUI-Modell unterstützt dieses Szenario durch das Konzept eines Prozesses, eines Bildschirms oder einer Reihe von Bildschirmen, die als Navigationseinheit behandelt werden. Benutzer können den Prozess eingeben, die Bildschirme durcharbeiten und auf dem letzten Bildschirm nach einer Schaltfläche suchen, über die sie an den Start zurückgegeben werden. Wichtig ist, dass der Benutzer den Prozess an mehreren Stellen im Produkt starten kann. Benutzer werden immer an den Ort zurückgegeben, an dem sie gestartet wurden, unabhängig davon, wo sie sich zu Beginn des Prozesses befinden.

### <a name="process-name"></a>Prozessname

Jeder Prozess sollte einen Namen erhalten, und der Name sollte auf jedem Bildschirm des Prozesses angezeigt werden. Money 2000 verwendet diesen Ansatz. Jeder Bildschirm, der Teil eines Gesamtprozesses ist, enthält den Namen dieses Prozesses am oberen Ende. Dieser Prozessname wird weniger gut als der eindeutige Titel des Bildschirms angezeigt, da er weniger wichtig ist. Der Prozessname erinnert Benutzer daran, welchen Prozess sie durchführen, und verstärkt das Konzept, dass alle Bildschirme im Prozess Teil eines einzelnen Features sind. Der Bereich Geldsteuer **umfasst beispielsweise** einen **Steuerschätzungsprozess,** der sich über mehrere Bildschirme erstreckt. Auf jedem Bildschirm in diesem Prozess werden sowohl der gemeinsame Prozessname als auch der eindeutige Bildschirmtitel angezeigt.

### <a name="implementation-of-processes"></a>Implementierung von Prozessen

Derselbe Prozess kann über verschiedene Links auf verschiedenen Bildschirmen gestartet werden, und Benutzer werden immer zur richtigen Startseite zurückverknungen. Dieses Verhalten kann nicht über einen hart codierten Link auf dem letzten Bildschirm des Prozesses erreicht werden, da das Ziel des Links variiert. Stattdessen kann die Anwendung dieses Verhalten implementieren, indem ein Stapel aktiver Prozesse unabhängig vom normalen Navigationsstapel beibehalten wird, der von **Back-** und **Forward-Befehlen verwendet** wird. Wenn der Benutzer einen Prozess startet, wird der Startbildschirm auf den Prozessstapel pusht. Wenn der Benutzer  auf dem letzten Bildschirm des Prozesses auf die Schaltfläche Fertig klickt, wird der letzte Startbildschirm von der Anwendung aus dem Stapel geschaltet, und der Benutzer wird auf diesen Bildschirm zurückübergibt.

Wenn Benutzer in einem Prozess von einem Bildschirm weg navigieren, bleibt der Prozess im Prozessstapel aktiv. Benutzer können den Prozess zum Sichern auf dem Bildschirm abschließen, auf dem sie ihn verlassen haben, und dann fortfahren. Auf diese Weise können Benutzer einen Umweg, eine Back-Up-Methode und dann den Prozess durchgehen. Um zu sehen, wie dieses Verhalten funktioniert, beginnen Sie jeden Onlineeinkaufsprozess auf dem World Wide Web, verlassen sie die Website, und klicken Sie dann auf **die Schaltfläche Zurück.** In der Regel können Sie dort weiterlesen, wo Sie aufgelassen haben.

### <a name="done-button"></a>Schaltfläche „Fertig“

Um einen Bildschirm fertig zu stellen und zum nächsten Bildschirm im Prozess zu wechseln, können Bildschirme eine Schaltfläche am unteren Rand der Seite anzeigen. Die Bezeichnung dieser Schaltfläche ist "Weiter", "Fertig" oder etwas ähnliches. Wenn die Schaltfläche den Prozess beendet und der Prozess  von mehreren Speicherorten aus aufgerufen werden kann, kann die Beschriftung der Schaltfläche Fertig den Namen des aufrufenden Speicherorts enthalten.

### <a name="navigation-bar"></a>Navigationsleiste

Auf jedem Bildschirm können Benutzer entscheiden, dass sie mit dem aktuellen Bereich des Produkts fertig sind und etwas anderes starten möchten. Möglicherweise möchten sie den aktuellen Bildschirm nicht explizit abschließen, bevor sie mit einem anderen Teil des Produkts fahren. Eine Navigationssymbolleiste kann dem Benutzer eine Reihe von Links zum Starten neuer Aufgaben anbieten. Wie bei anderen Listen von Aufgabenlinks sollten diese dem Prinzip folgen, den nächsten Navigationsschritt offensichtlich zu machen, der im folgenden Abschnitt ausführlich erläutert wird.

### <a name="make-the-next-navigational-step-obvious"></a>Machen Sie den nächsten Navigationsschritt offensichtlich

Nur wenige Programme können alle features gleichzeitig verfügbar machen. Benutzer müssen in der Regel durch ein Programm navigieren, um ein bestimmtes Feature zu finden. Benutzer sind bei der Navigation erfolgreicher, wenn sie leicht erkennen können, wie sie ihrem gewünschten Ergebnis mindestens einen Schritt näher kommen. Bildschirme, die IUI verwenden, werden unter Berücksichtigung dieses Prinzips entworfen.

Auf Aktivitätsseiten werden beispielsweise nicht unbedingt alle aufgaben- oder zielseitigen Aufgaben angezeigt, die der Benutzer von diesem Zeitpunkt an erreichen möchte. Stattdessen stellen Aktivitätsseiten eine Liste der Aufgaben bereit, die so abgeschlossen sind, dass Benutzer leicht den entsprechenden Link für das Klicken ermitteln können, auch wenn sie nur zu einer anderen Seite mit Links gelangen. Die häufigsten Aufgaben sollten besonders hervorgehoben sein und die geringste Navigation erfordern. Weniger häufige Aufgaben können mehr Schritte erfordern.

Hier ist ein Beispiel aus Money 2000. Angenommen, Benutzer möchten einen Vorgang ausführen, den sie nur gelegentlich ausführen, z. B. die Überprüfung des geschätzten Betrags der Einkommenssteuerzahlung des nächsten Jahres. Benutzer beginnen zunächst auf der Money 2000-Startseite mit der Suche nach diesem Feature. Da das Feature nicht in der Liste der allgemeinen Aufgaben angezeigt wird, müssen sie die Liste der Finanzbereiche überprüfen. Der Bereich **Steuern** klingt rauschend, sodass er darauf klickt. Die Seite **"Tax Center"** enthält einen Link zu dem gesuchten Feature für die Steuerschätzung, sodass sie darauf klicken und ihre Aufgabe ausführen. Durch die Anwendung von IUI-Prinzipien ermöglicht Money 2000 Es Benutzern, intuitiv zu finden, was sie suchen.

## <a name="user-assistance"></a>Benutzerunterstützung

In diesem Abschnitt wird eine Reihe vorgeschlagener Richtlinien für die Integration von Benutzerunterstützungstext in ein Produkt beschrieben, das IUI verwendet.

Primäre Unterstützung bezieht sich auf den gesamten Text, der auf dem Bildschirm angezeigt wird (wie im folgenden Screenshot gezeigt). Die primäre Hilfe bietet aufgabenorientierte Texthinweise, damit Benutzer alle auf dem Bildschirm angezeigten Informationen leicht verstehen können. Sie verstehen den Zweck der Seite und die Beziehung zwischen den Objekten, um Aufgaben zu erledigen. Da sich der Text direkt auf dem Bildschirm befindet, beantworten die Informationen fragen wie "Was soll ich tun?" ist einfach zugänglich und stark sichtbar, ohne dass der Benutzer Maßnahmen ergreifen muss.

![Screenshot des Kontoeinrichtungsbildschirms von "money 2000".](images/iuiguidelines11.png)

Die sekundäre Unterstützung besteht aus dem gesamten Text, der auf dem Bildschirm nicht sichtbar ist, und erfordert eine gewisse Benutzerinteraktion, um darauf zuzugreifen, z. B. klicken oder mit dem Mauszeiger auf ein Benutzeroberflächenelement zeigen. Dieser Inhalt ist für die Durchführung der vorliegenden Aufgabe nicht zwingend erforderlich, steht aber weiterhin in direktem Zusammenhang.

### <a name="primary-assistance"></a>Primäre Unterstützung

Die primäre Unterstützung kann einige oder alle der folgenden Komponenten umfassen:

-   Bildschirmtitel

    Beispiel: Ändern Ihres Bilds

    Der Bildschirmtitel ist das erste und wichtigste Element, das auf dem Bildschirm angezeigt wird. Der Zweck besteht darin, die Aufgabe, die auf dieser Seite ausgeführt werden kann, in der eigenen Sprache des Benutzers zu beschreiben. Der Bildschirmtitel sollte es vermeiden, die Details zum Abschließen der Aufgabe zu beschreiben. Der Text im Bildschirmtitel sollte nur auf die Kernaufgabe des Bildschirms verweisen. Als Faustregel gilt: Je einfacher und kürzer die Beschreibung der Aufgabe ist, desto besser wird die Aufgabe wahrscheinlich definiert. Ausführlichere Informationen zu diesem Thema finden Sie unter Schritt 2: [Zustand der Aufgabe.](#step-two-state-the-task)

-   Bildschirmuntertitel

    Beispiel: Sie können auch ein neues Bild aus dem Internet herunterladen.

    Auch mit bedachter Sorgfalt reicht der Bildschirmtitel möglicherweise nicht aus, um eine komplexe Aufgabe angemessen zu erklären. Mit dem Untertitel können Sie den Zweck des Bildschirms genauer erläutern. Sie können einen Untertitel verwenden, um den Zweck der Seite zu verdeutlichen, zusätzliche Aufgabenbeschreibungen bereitzustellen oder Erwartungen festzulegen. Benutzer, die den Untertitel nicht lesen, sollten die Seite erfolgreich verwenden können. Genau wie der Titel sollte der Untertitel vermeiden, Details zum Abschließen der Aufgabe zu beschreiben.

-   Aufgaben

    Beispiel: Ändern des Bildschirmschonrs

    Aufgaben können als Textlinks oder grafische Bilder dargestellt werden, die eine Benutzerinteraktion erfordern. Befehle, die als Textlinks dargestellt werden, sollten verbbasiert sein und als klare und präzise Aufgaben geschrieben werden.

-   Bezeichnungen für Befehlsschaltflächen

    Beispiel: Kennwort erstellen

    Es gibt drei Arten von Befehlsschaltflächen:

    -   Abbrechen
    -   Vorgehensweise
    -   Commit

    Die Schaltflächen Abbrechen und Fertig verwenden einfach "Abbrechen" und "Fertig" als Bezeichnungen. Commitschaltflächen sollten aktive Textbezeichnungen anstelle von "OK" verwenden. Verwenden Sie beispielsweise "Kennwort erstellen" anstelle von "OK".

-   Bezeichnungen für andere Steuerelemente

    Beispiel: Geben Sie Ihr Kennwort ein.

    Bezeichnungen für Steuerelemente wie Optionsfelder, Kontrollkästchen und Textfelder sollten klar und präzise geschrieben werden, damit Benutzer genau wissen, wofür die Steuerelemente vorgesehen sind, welche verwendet werden sollen und welche Informationen bereitgestellt werden müssen, um ihre Aufgabe zu erfüllen.

-   Links zu "Verwandte Aufgaben"

    Beispiel: Verwandte Aufgaben – Ändern eines anderen Kontos

    Links zu "Verknüpfte Aufgaben" sind explizite Einstiegspunkte zu anderen Aufgaben im Zusammenhang mit dem aktuellen Feature. Sie sollten als aufgabenbasierte Links geschrieben werden.

-   Links zu "Siehe auch"

    Beispiel: Siehe auch : Ändern Ihres Designs

    Links zu "Siehe auch" sind sekundäre Aufgaben. Diese beziehen sich auf die primäre Aufgabe, nehmen den Benutzer jedoch aus dem aktuellen Kontext. Diese sollten als reguläre Aufgabenlinks angezeigt werden. Weitere Informationen zu sekundären Aufgaben finden Sie unter [Visueller Entwurf sekundärer Aufgaben.](#visual-design-of-secondary-tasks)

### <a name="secondary-assistance"></a>Sekundäre Unterstützung

Die sekundäre Unterstützung kann einige oder alle der folgenden Komponenten umfassen:

-   InfoTips

    Sie können einen InfoTip verwenden, um dem Benutzer zusätzliche Informationen zu einem Aufgabenlink oder einer Befehlsschaltfläche bereitzustellen. Beispielsweise könnte ein InfoTip auf einem Aufgabenlink wie folgt lauten: "Zeigt eine Seite an, auf der Sie ein Bild auswählen können, das Sie mit Ihrem Konto verwenden können". Der InfoTip wird angezeigt, wenn der Benutzer mit der Maus auf das zugeordnete Objekt zeigt. Sie sollten InfoTips für alle Benutzeroberflächenelemente erstellen, auf die der Benutzer klicken kann.

-   Hilfethemen zu "Informationen zu"

    Beispiel: Informationen zu – Herunterladen einer Datei

    Links zu "Informationen zu" öffnen Hilfethemen wie Featureübersichten, konzeptionelle Informationen, unterstützende Informationen und Informationen zu Verfahren. Um die Unübersichtlichkeit zu reduzieren, sollten Sie die Anzahl der Hilfethemen "Informationen zu" auf dem Bildschirm minimieren.

## <a name="appendix-designing-and-testing-microsoft-money-2000"></a>Anhang: Entwerfen und Testen von Microsoft Money 2000

Dieser Abschnitt wurde aus den eigenen Beschreibungen der Designer angepasst. Es wird erläutert, wie das Money 2000-Team den Entwurfs- und Testprozess geändert hat, um das IUI-Modell zu berücksichtigen.

### <a name="designing-and-testing-money-2000"></a>Entwerfen und Testen von Money 2000

Das Entwerfen von Money 2000 mithilfe des inductiven Navigationsmodells führte dazu, dass das Team Entwürfe in Frage stellte, die schon lange im Produkt waren. Da die Prinzipien des Modells einfach sind, war es einfach, das Modell in den Entwurfsprozess zu übernehmen und dabei zu bleiben. Am Ende glauben die Designer, dass das Modell ihnen dabei half, bessere Entwürfe zu erstellen, als sie ohne sie hätten erstellen können.

### <a name="clearer-titles-and-designs"></a>Klarere Titel und Entwürfe

Die Designer von Money 2000 haben bemerkt, dass sie häufig Features mit Wörtern beschreiben würden, die nicht tatsächlich auf dem Bildschirm angezeigt wurden. Im IUI-Modell sollten bildschirme sich selbst erklären. Das Team hat beispielsweise erklärt, dass der Bildschirm mit der Bezeichnung **Zahlungskalender** für die Zahlung von Rechnungen vorgesehen war. In Money 2000 wird dieser Bildschirm als **"Rechnungen bezahlen"** bezeichnet. Alle Elemente, die nicht mit diesem Zweck in Zusammenhang stehen, wurden auf untergeordnete Bildschirme verschoben, was zu einem klareren Entwurf führt.

Ein weiteres Beispiel ist ein Bildschirm mit dem Namen **Online Financial Services Manager.** Das Team hatte Schwierigkeiten, eine einfache Erklärung des Zwecks dieses Bildschirms zu liefern. Wenn sie nicht zu einem Bildschirm gelangen konnten, entfernten sie diesen Bildschirm und verteilten seine Features auf logischer definierte Seiten.

### <a name="helping-new-designers"></a>Unterstützen neuer Designer

Das Team hat es leicht gefunden, neuen, unerfahrenen Softwaredesignern IUI-Entwurfstechniken beizubringen. Die Techniken ermöglichten Es Designern auf allen Erfahrungsebenen, ihre Entwürfe anhand von Bildschirmtiteln als Test der Übersichtlichkeit auszuwerten. Wenn er gezwungen wurde, einen klaren und präzisen Titel auf einem schlecht entworfenen Bildschirm zu setzen, erkannten Designer schnell, dass kein Titel für die Seite gut genug war. Sie erkannten, dass das Problem nicht darin lag, Wörter für einen Titel auszuwählen, sondern in einem fehlerhaften Bildschirmdesign. Mit diesem Verständnis könnten sie dann den Bildschirm umgestalten, um eine klarere Benutzerinteraktion und somit einen klareren Titel zu unterstützen.

### <a name="including-writers"></a>Einschließlich Writer

Im Verlauf des Entwurfs erkannte das Team, dass Dokumentationsautoren und -editoren an der Erstellung von Bildschirmtiteln beteiligt sein sollten. Writer konnten in früheren Releases nur eingeschränkt gute Titel auswählen, da sie erst zu einem späteren Zeitpunkt beteiligt waren. Bildschirme wurden in der Regel temporäre Arbeitstitel von Designern oder Programmierern erhalten. Diese Titel wurden bis spät in den Produktzyklus verwendet, als Autoren aufgefordert wurden, endgültige Bildschirmtitel zu erhalten. Zu diesem Zeitpunkt war es zu spät, schlecht entworfene Bildschirme zu überarbeiten.

Im Gegensatz dazu hat das Money 2000-Team Writer in den frühesten Phasen des Entwurfsprozesses einbezogen. Dies führte zu wertvollen Eingaben auf Bildschirmtiteln, wenn dies dem Entwurf immer noch helfen konnte. Wenn ein Bildschirm zu komplex war, um einen eindeutigen Titel zu ermöglichen, könnten die Writer vorschlagen, dass die Seite neu gestaltet wird.

Am Ende des Projekts waren die Autoren und Designer der Meinung, dass die Bildschirmtitel klarer und stärker als in früheren Versionen waren. Die Autoren haben es auch einfacher gefunden, neue Seiten zu erklären, was die Dokumentierung des Produkts vereinfacht. Alle Teammitglieder waren der Meinung, dass die Einbeziehung aller Disziplinen in die Entwurfsphase das Produkt besser und einfacher zu verwenden macht.

### <a name="usability-tests"></a>Benutzerfreundlichkeitstests

Während der Entwicklung von Money 2000 führte das Team mehrere Benutzerfreundlichkeitstests durch, um die Unterschiede zwischen der alten Navigationsstruktur von Money 99 und den Änderungen zu überprüfen, die als Ergebnis der Anwendung des IUI-Modells vorgenommen wurden.

### <a name="prototype-testing"></a>Prototyptests

Zu Beginn des Produktentwicklungsprozesses haben die Designer einen Prototyp erstellt, um zu untersuchen, wie Benutzer auf IUI reagieren würden. Diese Arbeit wurde sehr früh im Entwicklungsprozess durchgeführt, um Zeit zu geben, die Prinzipien des Modells zu verfeinern, bevor Programmierer damit begonnen haben, das Produkt selbst zu überarbeiten.

Das Team hat einen Prototyp in Microsoft Visual Basic html erstellt, der Meine Finanzen aktivitäten simuliert, die normalerweise in Money ausgeführt werden. Im Prototyp konnten Benutzer zu mehr als 50 Seiten navigieren, die die Hauptbereiche des Produkts darstellen. In diesen Bereichen könnten sie Finanzkonten einrichten, Rechnungen bezahlen, Berichte anzeigen und mit ihren Investitionen arbeiten.

Elf Teilnehmer haben die gleichen Aufgaben sowohl im Money 99- als auch im IUI-Prototyp ausgeführt. Sie wurden zufällig zugewiesen, um eines der Produkte zuerst zu verwenden. Vier Teilnehmer waren aktuelle Money-Benutzer, vier waren aktuelle Benutzer eines konkurrierenden Produkts, und drei hatten noch nie ein Meine Finanzen verwendet.

Allgemeine Einstellungen deuteten darauf hin, dass die vier aktuellen Benutzer von Money Money 99 bevorzugt haben (die Version, die sie zu Hause verwendet haben), während die verbleibenden sieben Benutzer den neuen Prototyp der aktuellen Version vorgezogen haben. Bei allen anderen Measures gab es keinen Unterschied zwischen den Benutzern der drei Gruppen. In Bezug auf die Gesamtleistung waren Benutzer doppelt so oft im falschen Bereich des Produkts, indem sie Money 99 (2,82-mal pro Aufgabe) wie im Prototyp (1,45-mal pro Aufgabe) verwendet haben. Andere Einstellungsdaten und Leistungsindikatoren, die zwar nicht signifikant sind, jedoch den Prototyp zu bevorzugen. Basierend auf diesen Daten und anderen Tests hat das Money-Produktteam entschieden, IUI-Prinzipien in Money 2000 zu integrieren.

### <a name="product-testing"></a>Produkttests

Nachdem der Großteil des Codes für das Produkt abgeschlossen wurde, hat das Team eine weitere Benutzerfreundlichkeitsstudie durchgeführt, um die endgültige Implementierung von IUI zu untersuchen. In diesem Test wurden 10 Teilnehmer, die noch nie ein Meine Finanzen-Produkt verwendet hatten, entweder money 99 oder money 2000 ausgewählt. Alle Benutzer haben die gleichen Aufgaben ausgeführt.

Benutzer von Money 2000 haben 89 % der Aufgaben erfolgreich abgeschlossen, während Benutzer von Money 99 nur 74 % der Aufgaben erfolgreich abgeschlossen haben. Wie beim Prototyp zeigten sich die Benutzer auch bei der Navigation in Money 2000 schneller, aber nicht wesentlich anders als bei Money 99. Darüber hinaus waren die allgemeinen maßnahmen zur zufriedenheitszufriedenheit für die Navigation auch für Money 2000 höher als für Money 99.

### <a name="controlled-testing"></a>Kontrollierte Tests

Da Money 2000 sehr komplex und komplex ist, eignet es sich nicht gut für kontrollierte Experimente zu den Auswirkungen der Anwendung von IUI. Stattdessen hat das Team eine eingeschränktere Umgebung für den Test erstellt.

Für den Test wurde eine Anwendung "Stock Market Viewer" verwendet, mit der Benutzer die Anzeige eines auf dem Bildschirm angezeigten Aktienberichts ändern konnten. Benutzer können ändern, welche Datenspalten in den Bericht aufgenommen wurden, welche Reihenfolge die Berichtsspalten, ihre Ausrichtung und die Anzahl der verwendeten Dezimalstellen haben. Die Designer wollten sehen, wie ein IUI-Ansatz für diese Aufgabe im Vergleich zu einer herkömmlichen grafischen Benutzeroberfläche funktioniert.

Der folgende Screenshot zeigt die herkömmliche Benutzeroberfläche, die im Test verwendet wird. Ein einzelner Dialog führt alle Berichtanpassungsaufgaben aus. Viele Anwendungen bieten ein ähnliches Dialogfeld zum Auswählen einer Teilmenge aus einer Liste von Elementen. Das Dialogfeld enthält zwei Listen: In der linken Liste werden alle verfügbaren Berichtsspalten angezeigt, und auf der rechten Seite wird die Teilmenge der Spalten angezeigt, die der Benutzer für den Bericht ausgewählt hat. Zusätzliche Steuerelemente ändern die Reihenfolge und formatierungsattribute für Berichtsspalten, die in der rechten Liste ausgewählt sind.

![Screenshot eines konventionellen Dialogfelds.](images/iuiguidelines12.png)

Für die IUI-Version dieser Aufgabe hat das Team eine Webanwendung erstellt. Jede Anpassungsaufgabe wurde auf einer separaten Seite platziert. Die Anwendung enthielt auch eine Hauptseite, die im folgenden Screenshot angezeigt wird und benutzer fragt, wie sie den Bericht anpassen möchten.

![Screenshot eines iui-Testbildschirms.](images/iuiguidelines13.png)

Durch Klicken auf Links auf dieser Hauptseite wird der Benutzer zu weiteren Seiten zum Ausführen bestimmter Anpassungsaufgaben führt. Der folgende Screenshot zeigt beispielsweise die Seite, die zum Auswählen von Berichtsspalten verwendet wird.

![Screenshot eines iui-Testbildschirms zum Auswählen von Berichtsspalten.](images/iuiguidelines14.png)

In Tests beider Versionen wurden die Personen aufgefordert, Berichte von einem bestimmten Startzustand (auf dem Bildschirm dargestellt) in einen angegebenen Zielzustand (auf einem Papierblatt dargestellt) anzupassen. Der Computer hat die Zeit und die Anzahl der Versuche nachverfolgt, die die Benutzer zum Anpassen des Berichts unternommen haben. Der Computer informierte Die Benutzer, wenn sie den Bericht erfolgreich angepasst hatten.

Der Test umfasste 88 Teilnehmer. Jeder Teilnehmer wurde gebeten, einen Satz von 11 Berichten mit einer der beiden Versionen der Anwendung anzupassen. Darüber hinaus haben 72 dieser Teilnehmer eine Woche später zurückgegeben, um einen weiteren Satz von 11 Berichten mit der gleichen Version aus der ersten Sitzung anzupassen. Jedes Subjekt wurde als ein unerfahrener Computerbenutzer klassifiziert, der hauptsächlich den Computer für E-Mails verwendet, einsam spielt und das Web durchschn.

Es gab keine signifikanten Unterschiede zwischen Benutzern der beiden Versionen oder einer der anderen variablen von Interesse. Benutzer haben Aufgaben mit der gleichen Geschwindigkeit ausgeführt, die Aufgabe mit der gleichen Anzahl von Malen durch iteriert und für die beiden Versionen die gleichen allgemeinen, zufriedenen Bewertungen erhalten. Bei diesem Test konnten daher keine Measures angezeigt werden, bei denen IUI zu einer Verbesserung oder Verschlechterung der Leistung oder zu einer Verschlechterung der Bewertungen geführt hat.

Wenn der Benutzer mehr navigieren muss, um die Aufgabe auszuführen, sollte die Zeit zum Ausführen der Aufgabe größer sein. Auch wenn dieses Experiment dieses Ergebnis nicht vermuten lässt, ist es wichtig zu beachten, dass die mittleren Leistungszeiten und die zugehörigen Standardabweichungen für die beiden verschiedenen Ansätze für diese Aufgabe nahezu identisch waren.

Weitere Untersuchungen sind erforderlich, um zu ermitteln, ob durch die Verwendung von IUI messbare Verbesserungen vorgenommen wurden. Dieser Test hat zumindest keinen Beweis dafür liefern, dass IUI die Leistung oder produktbasierte Nutzung beeinträchtigen würde.

### <a name="comparison-with-web-sites"></a>Vergleich mit Websites

Viele gut entworfene Websites verwenden Prinzipien, die dem in diesem Dokument beschriebenen IUI-Modell ähneln. Dies ist wahrscheinlich ein Nebeneffekt der Art und Weise, wie das Web funktioniert. Da es schwierig ist, komplexe Interaktionen zwischen Steuerelementen auf einer einzelnen Webseite zu implementieren, unterteilen Designer Aufgaben häufig in Teile, die mehrere Trips zum Server umfassen, um eine neue Seite zu erhalten. Einige Websites enthalten sogar Seitentitel, die den Zweck der Seite eindeutig enthalten.

Designer herkömmlicher Anwendungen verfügen über einen viel größeren Satz von Tools. Dies bietet ihnen mehr Flexibilität, bietet aber auch mehr Möglichkeiten, komplexe und verwirrende Seiten zu erstellen. Designer sollten diese Leistung beim Erstellen von inleiteriven Benutzeroberflächen mit Eigenem Ermessen nutzen und auf Klarheit und Einfachheit wert denken.

 

 





