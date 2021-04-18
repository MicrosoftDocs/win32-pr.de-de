---
title: Induktive Benutzeroberfläche
description: In diesem Thema wird das Benutzeroberflächen Modell beschrieben, das als "induktive User Interface" (IUI) bezeichnet wird.
ms.assetid: d99dc30a-68e5-4b7a-8cbd-0ac77a90a354
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 632e16191b7103cbf6be9fe209ada78781d4a53c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206239"
---
# <a name="inductive-user-interface"></a>Induktive Benutzeroberfläche

In diesem Thema wird das Benutzeroberflächen Modell beschrieben, das als "induktive User Interface" (IUI) bezeichnet wird. Das IUI-Modell, das auch als "induktive Navigation" bezeichnet wird, zeigt, wie Softwareanwendungen einfacher gemacht werden können, indem Features in Bildschirme oder Seiten unterteilt werden, die leicht erklärend sind Dieses IUI-Modell ist in verschiedenen Microsoft-Projekten ersichtlich, wie z. b. Microsoft Money 2000, den Windows-System Steuerungs Applets, verschiedenen Bildschirmen und Dialogfeldern in Microsoft Visual Studio 2010 und den Aufgabenbereichen in Microsoft Office.

-   [Introduction (Einführung)](#introduction)
-   [IUI in Aktion: Lösen eines allgemeinen Entwurfs Problems](#iui-in-action-solving-a-common-design-problem)
    -   [Problem: Software ist schwierig zu verwenden](#the-problem-software-is-hard-to-use)
    -   [Deduktive Benutzeroberfläche](#deductive-user-interface)
    -   [Eine Lösung: Induktive Benutzeroberfläche](#a-solution-inductive-user-interface)
-   [Schritte zum Erstellen einer induktiven Benutzeroberfläche](#steps-for-creating-an-inductive-user-interface)
    -   [Schritt 1: fokussieren der einzelnen Seiten auf eine einzelne Aufgabe](#step-one-focus-each-page-on-a-single-task)
    -   [Schritt 2: Zustand der Aufgabe](#step-two-state-the-task)
    -   [Schritt 3: Festlegen des Inhalts der Seite für die Aufgabe](#step-three-make-the-pages-contents-suit-the-task)
    -   [Schritt 4: anbieten von Links zu sekundären Aufgaben](#step-four-offer-links-to-secondary-tasks)
-   [Weitere Leitlinien](#additional-guidelines)
    -   [Konsistente Bildschirm Vorlagen verwenden](#use-consistent-screen-templates)
    -   [Machen Sie sich offensichtlich, wie die Aufgabe mit den Steuerelementen auf dem Bildschirm durchgeführt werden soll.](#make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen)
    -   [Stellen Sie eine einfache Möglichkeit bereit, um eine Aufgabe abzuschließen und eine neue zu starten](#provide-screens-for-starting-tasks)
    -   [Machen Sie den nächsten Navigations Schritt offensichtlich](#make-the-next-navigational-step-obvious)
-   [Benutzerunterstützung](#user-assistance)
    -   [Primäre Unterstützung](#primary-assistance)
    -   [Sekundäre Unterstützung](#secondary-assistance)
-   [Anhang: Entwerfen und Testen von Microsoft Money 2000](#appendix-designing-and-testing-microsoft-money-2000)
    -   [Entwerfen und Testen von Money 2000](#designing-and-testing-money-2000)
    -   [Benutznutzbarkeits Tests](#usability-tests)
    -   [Vergleich mit Websites](#comparison-with-web-sites)

## <a name="introduction"></a>Einführung

Das IUI ist ein Benutzeroberflächen Modell, das vorschlägt, wie Softwareanwendungen einfacher gemacht werden, indem Features in Bildschirme oder Seiten, die leicht erklärend und verständlich sind, unterteilt werden. Microsoft hat dieses Modell in Money 2000, einer großen kommerziellen Software Anwendung, implementiert. Bei informellen Tests wird empfohlen, dass Benutzer Aufgaben so schnell wie in herkömmlichen Schnittstellen ausführen können und leichter zu finden sind.

Viele kommerzielle Softwareanwendungen enthalten Benutzeroberflächen, bei denen ein Bildschirm eine Reihe von Steuerelementen anzeigt, die jedoch dem Benutzer überlässt, den Zweck der Seite abzuleiten und die Steuerelemente zu verwenden, um diesen Zweck zu erfüllen.

Die in diesem Dokument beschriebenen Prinzipien erfordern keine bestimmten festgelegten Sätze von Entwürfen, Steuerelementen oder visuellen Elementen. Wie grafische Benutzeroberflächen im Allgemeinen haben die Prinzipien in diesem Dokument viel Raum für Flexibilität und Kreativität bei der Entwicklung.

Die allgemeinen Prinzipien der induktiven Benutzeroberfläche werden mit Beispielen veranschaulicht, die aus Money 2000 gezeichnet werden.

> [!IMPORTANT]
> Das allgemeine Konzept von IUI liegt in der Kindheit. Designer, die diese Techniken einsetzen, erlernen und entdecken mehr darüber, wie Sie Sie für Ihre Software verwenden. Die Informationen in diesem Dokument werden im Laufe der Zeit weiterentwickelt, wenn sich Forschung und Wissen in diesem Bereich erhöhen. Dieses Thema bietet eine Einführung in IUI anstelle eines Unternehmens umfassenden Satzes von Richtlinien.

 

## <a name="iui-in-action-solving-a-common-design-problem"></a>IUI in Aktion: Lösen eines allgemeinen Entwurfs Problems

In diesem Abschnitt wird ein gängiges Entwurfsproblem mit den heutigen Softwareprodukten erläutert und IUI als Technik zur Problembewältigung vorgestellt.

### <a name="the-problem-software-is-hard-to-use"></a>Problem: Software ist schwierig zu verwenden

Die meisten Software sind zu schwer zu verwenden. Diese Schlussfolgerung stammt aus Nutzbarkeits Tests, anekdotischen beweisen und persönlichen Erfahrungen von Software Designern. Das Konzept von IUI wurde durch die Durchführung von Untersuchungen erstellt, um fundierte Schätzwerte zu machen, was die aktuelle Software schwer zu verwenden ist, und anschließend Lösungen vorzuschlagen. Designer, die IUI verwenden, sollten sich auf die Zufriedenheit der Kunden verlassen, um den endgültigen Erfolg des Entwurfs zu ermitteln.

Die meisten aktuellen Softwareprodukte sind aus den folgenden allgemeinen Gründen schwer zu verwenden:

-   Benutzer scheinen kein geeignetes geistiges Modell des Produkts zu konstruieren.

    Der Schnittstellen Entwurf für die meisten aktuellen Softwareprodukte geht davon aus, dass Benutzer ein konzeptionelles Modell verstehen, das von den Designern sorgfältig erstellt wurde. Leider scheinen die meisten Benutzer nicht jemals ein geistiges Modell zu erhalten, das gründlich und genau genug ist, um die Navigation zu steuern. Diese Benutzer sind wahrscheinlich sehr ausgelastet und mit Informationen überladen. Sie verfügen nicht über die Zeit, Energie oder den Wunsch, ein konzeptionelles Modell für Ihre Software zu untersuchen.

-   Sogar viele lange Benutzer haben niemals gängige Prozeduren.

    Entwickler wissen, dass neue Benutzer möglicherweise zunächst Probleme haben, aber erwarten, dass diese Probleme verschwinden, wenn Benutzer häufige Aufgaben erlernen. Nutzbarkeits Daten deuten darauf hin, dass dies häufig nicht der Fall ist. In einer Studie richten die Forscher automatisierte Geräte zu Hause für Videobänder ein. Die Bänder haben festgestellt, dass Benutzer, die sich auf die jeweilige Aufgabe konzentrieren, nicht notwendigerweise das folgende Verfahren bemerken und sich nicht von der Benutzer Arbeit aus informieren. Wenn Benutzer das nächste Mal denselben Vorgang ausführen, können Sie auf genau dieselbe Weise darauf stoßen.

-   Benutzer müssen hart arbeiten, um die einzelnen Features oder Bildschirme zu ermitteln.

    Die meisten Softwareprodukte sind für (die wenigen) Benutzer konzipiert, die das konzeptionelle Modell verstehen und gängige Verfahren haben. Bei den meisten Kunden ist jede Funktion oder Prozedur ein frustrierendes, unerwünschtes Rätsel. Benutzer können davon ausgehen, dass diese Rätsel eine unvermeidliche Kosten für die Verwendung von Computern darstellen, aber Sie sind ohne diese Belastung sicherlich glücklicher.

Die beste Lösung für diese Probleme besteht darin, eine allgemeine Strategie zu finden, mit der Sie die Features von Softwareprodukten besser erkennen und selbsterklärend gestalten können. Benutzer müssen in der Lage sein, jedes Mal, wenn Sie Sie benötigen, eine Funktion zu finden, und Sie müssen diese Funktion jedes Mal verwenden können, wenn Sie Sie verwenden möchten.

### <a name="deductive-user-interface"></a>Deduktive Benutzeroberfläche

Die meisten Elemente in Software erfordern, dass der Benutzer diese untersuchen und das Verhalten ableiten kann, wie im folgenden Screenshot veranschaulicht.

![Screenshot eines Beispiel Eigenschaften Dialogfelds.](images/iuiguidelines01.png)

Erfahrene Computerbenutzer, einschließlich Software-Designern, erkennen schnell, dass dieses Dialogfeld Ihnen ermöglicht, eine Liste der Dinge zu verwalten. Die Schaltflächen unter der Liste können Informationen zu Listenelementen hinzufügen, entfernen und bereitstellen. Beachten Sie jedoch, dass kein dieses Verhalten explizit im Dialogfeld selbst angegeben wird.

Sehen Sie sich jetzt den Dialog aus der Sicht des Benutzers an. Viele Benutzer werden bei diesem Dialogfeld gefragt: "Was soll ich damit tun?" Wenn das Dialogfeld angezeigt wird, muss der Benutzer das nächste Mal beenden und herausfinden, was zu tun ist. Zuerst muss der Benutzer die Tatsache ableiten, dass das große weiße Rechteck ein leeres Listenfeld ist, das mit Elementen aufgefüllt werden soll. Die kleine Text Bezeichnung "Things" in Box bietet einen vagen Hinweis. Einige Benutzer versuchen, das Listenfeld einzugeben, da es wie ein Bearbeitungs Textfeld aussieht.

Anschließend muss der Benutzer ableiten, dass sich die Schaltflächen unterhalb der Liste auf den Inhalt auswirken. Einige der Schaltflächen sind anfänglich deaktiviert. Dies ist eine andere potenzielle Quelle für Benutzer Verwirrung. Der Benutzer muss mit den Steuerelementen experimentieren, um zu erfahren, wie das Dialogfeld funktioniert.

Der Benutzer könnte auch andere Fragen stellen: "wie viele Elemente sollte ich in die Liste einfügen? Sollten die Elemente in einer bestimmten Reihenfolge eingegeben werden? Warum wurde dieses Dialogfeld an erster Stelle angezeigt? Was ist das? "

Benutzer werden von ihren Zielen abgelenkt, wenn Sie den Zweck eines Bildschirms ermitteln und die Verwendung der Anwendung durchführen müssen. Dies stellt letztendlich die Kosten für Zeit und Benutzer Zufriedenheit dar. Noch schlimmer ist, dass Benutzer diese Kosten immer wieder übertragen, wenn Sie bei jeder Verwendung einer Funktion ein Rätsel über die Schnittstelle haben.

Ein Bildschirm sollte über einen Titel verfügen, der seinen Zweck eindeutig erläutert. Wenn Designer einen Bildschirm erstellen, ist es selten erforderlich, dass Sie einen klar Aussage baren Zweck haben. Stattdessen kann Sie einfach Teil eines größeren konzeptionellen Modells sein, das der Benutzer ableiten muss.

Studien zeigen, dass viele Benutzer sogar durch grundlegende Vorgänge in der Software verwechselt werden. Sie haben Schwierigkeiten zu verstehen, was das Produkt für Sie tun kann, wo ein Vorgang durchgeführt wird und wie dieser Vorgang durchgeführt werden kann, sobald er gefunden wurde. Das Vereinfachen von Software durch die Durchführung grundlegender Änderungen ist eine leistungsstarke Möglichkeit, vorhandene Kunden vollständig zu erfüllen und neue Benutzer zu gewinnen.

### <a name="a-solution-inductive-user-interface"></a>Eine Lösung: Induktive Benutzeroberfläche

Als neue Methode zum Entwerfen von Software besteht das Ziel darin, die Menge der Benutzer zu verringern, die Benutzer durchführen müssen, um erfolgreich zwischen den Teilen eines Produkts zu wechseln und seine Features zu verwenden. Das Wort "induktive" ergibt sich aus der Verb Bewegung, d. h

IUI ist eine Erweiterung der Common Web-Style-Schnittstelle. In der Weboberfläche müssen Seiten einfach und Aufgaben basiert sein, da jede Information über eine relativ langsame Verbindung an einen Server gesendet werden muss. Der Server antwortet dann mit dem nächsten Schritt, usw. Ein guter Webentwurf bedeutet, dass Sie sich auf eine einzelne Aufgabe pro Seite konzentrieren und Navigations Seiten bereitstellen. Ebenso beginnt die induktive Navigation mit dem Fokus der Aktivität auf jeder Seite auf eine einzelne primäre Aufgabe.

Eine gut entworfene, induktive Oberfläche hilft Benutzern bei der Beantwortung von zwei grundlegenden Fragen, die Ihnen bei der Betrachtung eines Bildschirms begegnen:

-   Was soll ich jetzt tun?
-   Wo gehe ich von hier aus, um meine nächste Aufgabe zu erledigen?

Software, die gemäß diesen Prinzipien entworfen wurde, beantwortet diese Fragen, indem Sie mit einer grundlegenden Voraussetzung beginnen: ein Bildschirm mit einem einzelnen, eindeutig expliziten Zweck ist leichter zu verstehen als eine Seite ohne diesen Zweck. Wenn der Bildschirm leichter zu verstehen ist, ist es für den Benutzer leichter zu wissen, was zu tun ist und wo Sie als nächstes vorgehen sollten.

Diese grundlegende Voraussetzung kann in eine Reihe von vier Schritten für das Entwerfen von Software, die IUI verwendet, erweitert werden:

-   Fokussieren der einzelnen Bildschirme auf eine einzelne Aufgabe.
-   Geben Sie die Aufgabe an.
-   Festlegen, dass der Inhalt des Bildschirms der Aufgabe entspricht.
-   Bietet Links zu sekundären Aufgaben.

In diesem Dokument werden die allgemeinen Grundlagen von IUI beschrieben. es werden jedoch auch diese Prinzipien in Aktion veranschaulicht, indem Beispiele aus Money 2000 und anderer Software angezeigt werden. Sie sollten sich diese Beispiele als spezielle Ausdrücke von IUI vorstellen, nicht als Strict-Modell für die Implementierung.

Zusätzlich zu den vier oben aufgeführten Schritten können Sie Ihre Schnittstelle stärken, indem Sie diese fünf Richtlinien befolgen:

-   Verwenden Sie konsistente Bildschirm Vorlagen.
-   Stellen Sie Bildschirme zum Starten von Aufgaben bereit.
-   Machen Sie sich offensichtlich, wie die Aufgabe mit den Steuerelementen auf dem Bildschirm durchgeführt werden soll.
-   Stellen Sie eine einfache Möglichkeit bereit, um eine Aufgabe abzuschließen und eine neue zu starten.
-   Machen Sie den nächsten Navigations Schritt offensichtlich.

### <a name="processes"></a>Prozesse

Viele Aufgaben erfordern, dass Benutzer durch eine Reihe von Bildschirmen navigieren können. Ein Benutzer, der einen Task ausführt, kann auf einen Link zu einer sekundären Aufgabe klicken, die von der Sequenz der Bildschirme entfernt wird, aus denen der primäre Task besteht. Wenn der Benutzer die sekundäre Aufgabe abschließt, sollte es eine einfache Möglichkeit geben, den Benutzer direkt an den Verzweigungs Punkt in der ursprünglichen Aufgabe zurückzugeben. Benutzer haben wahrscheinlich Probleme, wenn Sie herkömmliche Navigations Steuerelemente verwenden, wie z. b. die Schaltflächen " **zurück** " und " **Vorwärts** ", um zum Start

Um diese Möglichkeit zu bieten, definiert IUI ein Navigationskonzept, das als Prozess, einen Bildschirm oder eine Reihe von Bildschirmen bezeichnet wird, die eine Aufgabe ausführen. Ein Prozess fungiert als eine Art Navigations Unterroutine. Benutzer können einen Prozess starten, ihre Reihe von Bildschirmen durcharbeiten und dann auf der letzten Seite auf eine "Done"-Schaltfläche klicken, um schnell zu der Seite zurückzukehren, auf der Sie mit dem Prozess begonnen haben.

## <a name="steps-for-creating-an-inductive-user-interface"></a>Schritte zum Erstellen einer induktiven Benutzeroberfläche

In diesem Abschnitt werden die vier Schritte beschrieben, die Sie zum Erstellen eines IUI verwenden können.

### <a name="step-one-focus-each-page-on-a-single-task"></a>Schritt 1: fokussieren der einzelnen Seiten auf eine einzelne Aufgabe

Der erste Schritt beim Entwerfen eines IUI besteht darin, ein Feature oder eine Reihe von Features zu nutzen und in separate Bildschirme aufzuteilen. Jeder Bildschirm sollte sich auf einen einzelnen Task konzentrieren, der als primärer Task des Bildschirms bezeichnet wird.

Diese Idee klingt einfach, aber nur wenige Anwendungen befolgen Sie. Die meisten Anwendungen bieten einen Bildschirm, von dem alle zugehörigen Features erreicht werden. Dieser Entwurf erfordert, dass Benutzer ermitteln (ableiten), was ausgeführt werden kann, und wie Sie dies tun.

Der primäre Task kann entweder spezifisch oder geöffnet sein. Beispielsweise kann in einem persönlichen Finanzprogramm eine bestimmte Aufgabe lauten: "wählen Sie die Rechnung aus, die Sie bezahlen möchten", während eine geöffnete Aufgabe möglicherweise "Überprüfen Sie die Leistung Ihrer Investitionen" ist.

Der primäre Task muss etwas sein, das für den Benutzer sinnvoll ist, anstatt ein Implementierungsdetail oder ein anderes abstraktes Konzept zu überdenken. Die Aufgabe sollte etwas sein, das Benutzer möglicherweise verwenden, vorzugsweise in ihren eigenen Wörtern beschrieben.

### <a name="example"></a>Beispiel

In diesem Abschnitt werden zwei unterschiedliche Ausgaben von Money verglichen. Die Beispiele zeigen sehr ähnliche Features, mit denen Benutzer Finanzkonten anzeigen und verwalten können.

Das IUI-Modell wurde während der Erstellung des Geldes 2000 entwickelt, einer Anwendung für die Verwaltung persönlicher Finanzen. Money 2000 ist die achte Hauptversion des Produkts. Money 2000 ist ein großes Windows-Programm mit mehr als 1 Million Codezeilen.

Money 2000 ist eine Webanwendung. Dabei handelt es sich nicht um eine Website, sondern um viele Attribute mit Websites. Die zugehörige Benutzeroberfläche besteht aus voll Bildseiten, die in einem freigegebenen Frame angezeigt werden, und Tools, mit denen Sie sich über einen Navigations Stapel vorwärts und rückwärts bewegen können. Auf dieser Grundlage bietet Money 2000 eine Reihe neuer Benutzeroberflächen Konventionen, die eine strukturiertere Benutzeroberfläche erstellen.

Obwohl IUI zuerst im Web-Style-Design von Money 2000 verwendet wurde, kann es auch mit herkömmlichen Schnittstellen Elementen wie Fenstern und Dialogfeldern verwendet werden.

In Money 99 haben Benutzer häufig eine Vielzahl von Aufgaben auf einem einzelnen Bildschirm ausgeführt. Der folgende Screenshot zeigt z. b. den **Konto-Manager** , der alle Konto bezogenen Features in Money 99 auf einem einzelnen Bildschirm präsentiert.

![Screenshot des Konto-Managers in Money 99.](images/iuiguidelines02.png)

In diesem Bildschirm wird eine allgemeine Aufgabe gruppiert, zu einem Konto und zu seltenen Aufgaben wie das Erstellen und Löschen von Konten. Keine dieser spezifischen Aufgaben wird direkt im Titel des Bildschirms ( **Account Manager**) ausgedrückt. Viele Benutzer finden diesen Bildschirm möglicherweise als Herausforderung, wie das Beispiel Dialogfeld in Abbildung 1. In beiden Fällen muss der Benutzer den Zweck des Bildschirms ableiten und ihn verwenden.

Money 2000, das auf IUI folgt, bietet einen fast identischen Satz an Konto bezogenen Features, stellt Sie jedoch auf zwei separaten Bildschirmen bereit. Der folgende Screenshot zeigt den ersten dieser Bildschirme, wobei der Fokus ausschließlich darauf besteht, dass der Benutzer ein Konto auswählen kann.

![Screenshot des Bildschirms zur Konto Auswahl in Money 2000.](images/iuiguidelines03.png)

Der Bildschirm "Money 2000" enthält ungefähr die gleiche Anzahl von visuellen Elementen wie der vorherige "Money 99"-Bildschirm, aber die Seite ist nun vollständig darauf ausgerichtet, dass der Benutzer ein Konto auswählen kann. In der Version "Money 99" musste ein Benutzer z. b. zwei Klicks erstellen, um ein Konto zu öffnen: ein Konto zum auswählen und ein weiteres, um den Öffnungsvorgang auszuwählen. In der Money 2000-Version ist der einzige Grund, warum ein Benutzer auf ein Konto klickt, das Öffnen des Kontos, sodass ein einzelner Mausklick ausreichen kann. Auf diese Weise wird die Anzahl der zum Ausführen einer allgemeinen Aufgabe erforderlichen Klicks häufig reduziert, obwohl sich die Anzahl der Bildschirme erhöhen kann.

Gelegentlich möchten Benutzer ein Konto hinzufügen oder entfernen. Um diese Aufgabe in Money 2000 auszuführen, navigieren Benutzer zu einem zweiten Bildschirm (im folgenden Screenshot gezeigt), der sich auf die Einrichtung von Konten konzentriert.

![Screenshot des Bildschirms zum Einrichten des Kontos in Money 2000.](images/iuiguidelines04.png)

Der Zweck der einzelnen Bildschirme ist in der IUI-Version von Money 2000 klarer. Außerdem verfügt jeder Bildschirm über mehr Platz, um seinen Zweck zu erfüllen. Der Money 99-Konto- **Manager** kann z. b. nur wenig Platz für die Schaltfläche **Konto löschen** geben, da er im Vergleich zu den anderen Befehlen auf dem Bildschirm selten verwendet wurde. Im Gegensatz dazu kann der Bildschirm zum Einrichten des Kontos in Money 2000 den Befehl genauer machen, sodass er leichter erkennbar und selbsterklärend ist.

### <a name="what-is-a-single-task"></a>Was ist eine einzelne Aufgabe?

Woher wissen Sie, ob sich ein Bildschirm tatsächlich auf nur eine Aufgabe konzentriert? Ein Bildschirm, der viele Aufgaben unterstützt, wird möglicherweise so erklärt, dass er nur einen Zweck hat, wenn dieser Zweck abstrakt genug Im folgenden finden Sie eine Faustregel: ein Bildschirm konzentriert sich auf einen Zweck, wenn der Designer diesen Zweck mit einem präzisen, sinnvollen und natürlichen Bildschirm Titel Ausdrücken kann.

Die Designer von Money 2000 haben diese Bildschirme als Unterbrechung angesehen (**Wählen Sie ein Konto aus, das Sie verwenden möchten,** und **richten Sie Ihre Konten in Geld** ein) Da jeder Bildschirm jedoch bereits einen präzisen, sinnvollen und sinnvollen Titel hat, haben die Designer geglaubt, dass die Bildschirme ausreichend sind. Wenn Sie einen Bildschirm entwerfen und sich keinen klaren und einfachen Titel vorstellen können, versuchen Sie wahrscheinlich, auf dem Bildschirm zu viel zu erreichen.

### <a name="step-two-state-the-task"></a>Schritt 2: Zustand der Aufgabe

Jeder Bildschirm sollte mit einer präzisen und expliziten Anweisung der primären Aufgabe versehen werden. Dies kann eine direkte Anweisung ("wählen Sie das Konto, das Sie ausgleichen möchten") oder eine Frage sein, die der Benutzer beantworten soll ("welches Konto soll ausgeglichen werden?").

Dies ist ein weiteres einfaches Prinzip, das häufig nicht praktiziert wird. Beispielsweise hatten frühere Ausgaben von Money Bildschirme mit Titeln, wie z. b. **Online-Finanzdienst-Manager** und **Guthabenkonto**. Benutzer mussten den Zweck und das Verhalten dieser Bildschirme von der Anordnung und den Bezeichnungen ihrer Steuerelemente ableiten.

Der Titel des Bildschirms oder der Seite ist sehr wichtig. Unabhängig davon, ob das Produkt Windows, Web-Style-Seiten, Dialoge oder einen anderen Entwurf verwendet, sollte der Titel keinen Bildlauf durchführen dürfen.

### <a name="usable-screens-have-clear-titles"></a>Verwendbare Bildschirme haben klare Titel

Bildschirme, die viele Aufgaben ausführen, erfordern abstrakte oder komplexe Titel. Beispielsweise ermöglichte der in Abbildung 2 gezeigte Bildschirm "Money 99" dem Benutzer das Navigieren zu Konten und das Einrichten von Konten. Der abstrakte Titel "Account Manager" wurde an diese Seite übergeben, um diese beiden Zwecke zu erfassen. Benutzer haben möglicherweise einige Ideen dazu, was eine "Konto-Manager"-Seite möglicherweise macht, aber Sie bemerken möglicherweise nicht, dass die häufigste Aufgabe für diesen Bildschirm lediglich das Auswählen eines Kontos war.

Einige Bildschirme oder Befehle verfügen über abstrakte Zwecke, die nicht ohne weiteres klare Titel vorschlagen. Für diese Bildschirme können Designernamen auswählen, die absichtlich vage sind, wie z. b. "Einstellungen", geprägte Schlagwörter, wie z. b. "Quickstep;" oder "Jargon", der Implementierungsdetails ("Database compaction") aufzeigt. Diese Arten von Namen sind häufig verwirrend oder irreführend für Benutzer. Außerdem handelt es sich bei diesen Namen normalerweise um Nomen, die die vom Benutzer gewünschte Aktion nicht ausdrücken, was zu Verwechslungen beiträgt.

Bildschirm Titel und andere Namen werden oft erst am Ende des Entwurfsprozesses bestimmt. Designer bitten die Writer oft, einen passenden Namen für einen Bildschirm zu erhalten, nachdem er entworfen und codiert wurde. An diesem Punkt gibt es keinen Fall, wenn ein guter Name nicht gefunden werden kann, und das Team muss sich möglicherweise für nicht klar eindeutige Namen befinden. Die Lösung für diesen Fehler besteht darin, dass Designer die Übersichtlichkeit in Bildschirmfunktionen und Titeln früh im Entwurfsprozess überprüfen können.

Bildschirmfunktionen und Titel sollten sich auf die gängigsten Aufgaben konzentrieren, die von Kunden ausgeführt werden. Designer sind häufig dazu verleitet, große Mengen an Funktionalität bereitzustellen, um die größte Anzahl von Kunden zu erfüllen, zusammen mit den Wünschen des Entwurfs Teams selbst. Zusätzliche Features erhöhen jedoch immer Komplexität und andere Kosten.

### <a name="screen-title-indicates-design-clarity"></a>Bildschirm Titel gibt Entwurfs Klarheit an

Im IUI-Modell wählen die Designer die Bildschirm Titel in den frühesten Phasen des Entwurfsprozesses aus. Anstatt einen Titel auszuwählen, um die Funktionsweise des Bildschirms zu rechtfertigen, wird der Titel verwendet, um zu bestimmen, ob der Bildschirm sinnvoll ist. Wenn kein geeigneter Titel gefunden werden kann, wird das Feature umgestaltet. Wenn kein Entwurf einen klaren und präzisen Titel zulässt (d. h., wenn es keine Möglichkeit gibt, das Feature zu erläutern), können die Designer das Feature verwerfen. Vergleichen Sie in den folgenden Screenshots den Bildschirm Money 99 Bill Payment auf der linken Seite, der eine statische Bezeichnung für die Seite ("anstehende Rechnungen &-Einlagen") und den entsprechenden Bildschirm "Money 2000" auf der rechten Seite mit einem expliziten Titel ("klicken Sie auf die Rechnung, die Sie bezahlen möchten") enthält:

![Screenshot, der einen statischen Titel in Money 99 und einen aktiven Titel in Money 2000 anzeigt.](images/iuiguidelines05.png)

Ein Bildschirm Titel, bei dem es sich natürlich nur um einen Ausdruck oder einen Satz handelt, ist einfacher zu ändern als ein Entwurf oder ein Code. Trotz dieses fakfakts hat die Verwendung von IUI gezeigt, dass durch das frühzeitige Beharren auf einen klaren Bildschirm Titel bessere Entwürfe erzeugt werden. Titel sollten mit Eingaben aus den Teammitgliedern der Benutzerschulung und Benutzerfreundlichkeit sowie den Produktdesignern ausgewählt werden.

Möglicherweise versuchen Team Mitglieder manchmal, diese Entscheidung zu verschieben, vorausgesetzt, dass die Kunden das Verständnis des Zwecks eines Bildschirms teilen. Wenn Sie dazu gezwungen werden, eine klare und präzise Anweisung zu diesem Zweck zu bieten, werden häufig Unterschiede von Meinungen offengelegt. Durch die Behebung dieser Unterschiede und die frühe Auswahl eines Titels können Entwurfs Diskussionen reibungslos fortgesetzt werden.

Wenn ein Titel ausgewählt ist, sollten Sie ihn nicht änderbar berücksichtigen. Designer verfeinern die Bildschirm Titel wahrscheinlich im zeitlichen Verlauf, wie bei jedem Design. Der erste gewählte Titel sollte jedoch in dieser Phase der Entwicklung so stark wie möglich sein.

### <a name="guidelines-for-choosing-screen-titles&quot;></a>Richtlinien für die Auswahl von Bildschirm Titeln

In diesem Abschnitt wird eine einfache Methode zum Auswählen von guten Bildschirm Titeln beschrieben. Um dieses Verfahren zu verwenden, stellen Designer sich einen Freund vor: &quot;Was ist dieser Bildschirm für?&quot; und dann erhalten Sie eine klare, hilfreiche Antwort, die den Satz &quot;Dies ist der Bildschirm, auf dem Sie sich befinden?&quot; abschließt. Die Wörter, die den Satz vervollständigen, werden zum Bildschirm Titel.

Während der Entwicklung von Money 2000 erstellten die Dokumentations Schreiber des Teams Bildschirm Titel Richtlinien, um Qualität und Konsistenz sicherzustellen. In diesen Richtlinien wurden z. b. Titel vorgeschlagen, die Verben verwendeten und als Fragen oder direkte Anweisungen formuliert wurden. Designer haben statische Namen vermieden, die mehr Abstraktion ermöglichten und möglicherweise ungenau sind.

Um Titel zu vereinfachen, haben Designer zusammengesetzte Sätze vermieden und versucht, die sprachsprache zu verwenden, sodass unschöne Begriffe und Fachjargon vermieden werden. Wenn Designer die Aufgabe nicht beschreiben können, ohne auf die Zusammenhänge (&quot;and&quot;, &quot;or") zurückgreifen zu müssen, versucht der Bildschirm wahrscheinlich, mehr als eine Aufgabe durchzuführen, und es ist weniger wahrscheinlich, dass der Benutzer sofort wissen kann, was zu tun ist.

Selbst wenn ein Titel sorgfältig ausgewählt wird, ist der Titelbereich möglicherweise zu klein, um eine komplexe Aufgabe adäquat zu erläutern. Um dieses Problem zu beheben, können Sie einen kurzen beschreibenden Absatz am oberen Rand des Inhalts Bereichs des Bildschirms einschließen, der die Aufgabe erläutert.

Die folgende Tabelle enthält einige Beispiele für Bildschirm Titel in Money 99 und Titel für dieselben oder Verwandte Bildschirme in Money 2000.



| Bildschirm Titel in Money 99             | Neue Bildschirm Titel in Money 2000                         | Kommentar                                         |
|---------------------------------------|---------------------------------------------------------|-------------------------------------------------|
| **Konto-Manager**                   | **Konto** zum **Einrichten Ihrer Konten** auswählen<br/> | Statischer Titel in aktive Titel geändert.          |
| **Kontodetails**                   | **Konto Einrichtung ändern**                                | Der statische Titel wurde in "aktiv" geändert. |
| **Zahlungs Kalender**                  | **Rechnung bezahlen**                                          | Beschreibender Titel beschreibend.                   |
| **Online-Finanzdienst-Manager** |                                                         | Die Seite ist nach der Umgestaltung nicht erforderlich.                 |



 

### <a name="making-the-screen-title-prominent"></a>Festlegen des Bildschirm Titels

Wenn Sie sich an einem nützlichen Bildschirm Titel befinden, müssen Sie sicherstellen, dass die Aufmerksamkeit des Benutzers auf den Titel aufmerksam gemacht wird. Einige Studien haben gezeigt, dass Benutzer selten Anweisungs Text lesen. Um dieses Problem zu beheben, sollten Bildschirm Titel so entworfen werden, dass Sie hervorgehoben und ansprechend sind, um die Aufmerksamkeit des Benutzers zu zeichnen. Der visuelle Entwurf des Bildschirms sollte den Benutzer darüber informieren, dass der Titel das wichtigste ist, das gelesen werden soll.

### <a name="step-three-make-the-pages-contents-suit-the-task"></a>Schritt 3: Festlegen des Inhalts der Seite für die Aufgabe

Beim Erstellen von Software, die den Richtlinien von IUI folgt, umfasst die schwierigste Entwurfsarbeit in der Regel das Unterbrechen von Features in Bildschirme oder Seiten. Der nächste Schritt besteht darin, zu bestimmen, welche Steuerelemente auf den einzelnen Bildschirmen zum Ausführen der primären Aufgabe verwendet werden. Diese Steuerelemente bilden den Inhalt der Seite, in dem der Benutzer die Arbeit erledigt. Der Bildschirm Titel und der Inhalt sind zwei Hälften eines Dialogs zwischen dem Programm und dem Benutzer. Der Titel stellt die Frage des Programms dar oder gibt eine Anweisung aus, und der Benutzer antwortet über die Benutzeroberfläche des Bildschirms.

Wenn der Bildschirm Titel klar und einfach ist, ist das Entwerfen des Bildschirms in der Regel unkompliziert. Beispielsweise hat einer der zuvor gezeigten "Money 2000"-Bildschirme den Titel "wählen Sie ein Konto für die Verwendung aus". Bei diesem Titel sollte der Bildschirm offensichtlich eine einfache Liste von Konten enthalten, aus denen der Benutzer auswählen kann. Ein weiterer Geld 2000-Bildschirm mit dem Titel "Überprüfen Sie die Elemente, die in Ihre Steuern eingeschlossen werden". Dieser Bildschirm enthält natürlich eine Prüfliste für Elemente.

Benutzer sollten in der Lage sein, leicht herauszufinden, wie Steuerelemente verwendet werden, um die primäre Aufgabe des Bildschirms zu erreichen. Wenn Benutzer aufgefordert werden, ein Konto auszuwählen, und Sie auf dem Bildschirm sehen können, um eine Liste der Konten zu finden, bestätigen Sie, dass Sie das Verständnis der Aufgabe erhalten. Dadurch erhöht sich die Wahrscheinlichkeit, dass Benutzer erfolgreich sein werden, wodurch auch das Vertrauen in andere Aufgaben erhöht wird.

### <a name="screen-content-areas"></a>Bildschirm Inhaltsbereiche

Die genaue Position und Form der Bildschirm Inhaltsbereiche hängt vom Entwurf der Software ab. In Money 2000 ist der Bildschirm Inhalts Bereich alles unterhalb des Bildschirm Titels und rechts neben der Aufgabenliste. Diese Region kann auf langen Bildschirmen scrollen. Einige nicht wesentliche Inhalte können auch im Statusbereich unterhalb der Aufgabenliste angezeigt werden.

Designer können sich dazu entscheiden, die primäre Aufgabe des Bildschirms in einem Absatz am oberen Rand des Inhalts Bereichs zu vertiefen. Benutzer müssen diesen Text nie lesen, aber Sie finden es möglicherweise hilfreich. Viele Benutzer können diese überspringen und den Bildschirm trotzdem erfolgreich verwenden. Anders als der Titel kann diese Beschreibung einen Bildlauf durchführen, wenn der Bildschirm ScrollBar ist. Weitere Informationen finden Sie unter [Richtlinien für die Auswahl von Bildschirm Titeln](#guidelines-for-choosing-screen-titles).

Wenn Designer möchten, dass auf einer Seite nicht wichtige Erinnerungen, Warnungen oder andere Statusinformationen angezeigt werden, kann Sie links neben dem Hauptinhalts Bereich unter der Aufgabenliste auf der linken Seite des Bildschirms angezeigt werden. Funktionell ist dieser Statusbereich eine zusätzliche Region für Bildschirminhalte. Dieser Bereich ist nicht hervorgehoben, um grundlegende Steuerelemente zu enthalten.

### <a name="provide-a-clear-exit-from-the-page"></a>Geben Sie einen Löschvorgang auf der Seite an.

Nachdem eine Aufgabe erfolgreich abgeschlossen wurde, sieht der Benutzer ein anderes Problem: Wann und wie der Bildschirm verlassen wird. Für Bildschirme, deren primärer Task Navigation ist, wird der Benutzer durch das Ausführen der Aufgabe selbst auf den nächsten Bildschirm verschoben. Auf anderen Bildschirmen ist es für den Benutzer möglicherweise schwieriger, zu wissen, wie der Vorgang fortgesetzt werden kann. Beispielsweise benötigt der Benutzer auf einem Bildschirm, der den Benutzer auffordert, Informationen in Felder einzugeben, möglicherweise Hilfe bei der Ermittlung, wann und wie Sie fortfahren. Auf solchen Seiten ist es häufig hilfreich, eine Schaltfläche " **weiter** " oder " **durch** klicken" an einem konsistenten Ort zu bieten.

Nutzbarkeits Studien haben gezeigt, dass Benutzer diese Schaltflächen auch dann verwenden, wenn globale Navigations Schaltflächen, wie z. b. die Schaltflächen " **zurück** " oder " **Start** " auf einer Symbolleiste Benutzer sind häufig auf Bildschirmen ohne Clear-Exit unbequem, auch wenn es nur Bildschirme gibt, deren einziger Zweck darin besteht, Informationen zu lesen.

Weitere Informationen zu diesem Thema finden Sie unter [Bereitstellen einer einfachen Möglichkeit zum Ausführen einer Aufgabe und Starten eines neuen](#provide-screens-for-starting-tasks) Themas im Abschnitt "Weitere Richtlinien".

### <a name="step-four-offer-links-to-secondary-tasks"></a>Schritt 4: anbieten von Links zu sekundären Aufgaben

Der letzte Schritt beim Entwerfen eines Bildschirms besteht darin, Links zu sekundären Aufgaben bereitzustellen. dabei handelt es sich um Funktionen, die die primäre Aufgabe nicht direkt ausführen, sondern mit dem Bildschirm verknüpft sind. Wenn z. b. die primäre Aufgabe auf einem Bildschirm darin besteht, einen Buchstaben zu schreiben, können sekundäre Aufgaben auf diesem Bildschirm darin bestehen, eine Postanschrift zu suchen oder einen Umschlag auszugeben.

Sekundäre Tasks können Dialogfelder anzeigen, die visuelle Darstellung des Bildschirm Inhalts ändern oder den Benutzer zu einem anderen Bildschirm navigieren. Ein sekundärer Task kann indirekt den primären Task ausführen oder verlorene Benutzer an den Ort umleiten, nach dem Sie suchen.

Wenn eine Seite eine Konversation zwischen dem Computer und dem Benutzer ist, kann ein sekundärer Task den Benutzer dazu auffordern, die aktuelle Frage des Computers zu ignorieren und den Computer dazu aufzufordern, etwas anderes zu tun. Stellen Sie sich beispielsweise folgendes Dialogfeld vor: Computer: "welche Rechnung möchten Sie bezahlen?" Benutzer: "tatsächlich möchte ich wirklich eine Rechnung finden, die ich einmal bezahlt habe."

Einige Bildschirme in Ihrem Produkt haben keine sekundären Aufgaben, andere dagegen mehrere. Vermeiden Sie das Erstellen einer langen Liste von Aufgaben, die für den Benutzer wahrscheinlich schwierig zu scannen sind. Wenn auf einem Bildschirm eine relativ lange Liste der sekundären Aufgaben enthalten ist, sollten die häufigsten Aufgaben zuerst platziert, in einem separaten Abschnitt gruppiert oder auf andere Weise visuell hervorgehoben werden.

Die Liste sollte nicht jede denkbare sekundäre Aufgabe enthalten, solange der nächste Navigations Schritt offensichtlich ist. Anstatt viele sekundäre Aufgaben anbieten zu müssen, kann ein Bildschirm sekundäre Aufgaben bereitstellen, die zu den neben geordneten Seiten navigieren, die weitere Aufgaben auflisten.

### <a name="visual-design-of-secondary-tasks"></a>Visueller Entwurf sekundärer Aufgaben

Sekundäre Tasks sollten an einer untergeordneten Position auf dem Bildschirm aufgeführt werden, auf der Sie ggf. verfügbar sind, aber nicht von der primären Aufgabe abgeleitet werden. Wenn Sie diese Liste auf den einzelnen Bildschirmen in einer konsistenten Position platzieren, können Benutzer die Liste schnell finden, wenn Sie Sie benötigen.

Wenn Sie die Liste der sekundären Aufgaben auf der linken Seite des Bildschirms anzeigen, sollte die Liste selbst weder scrollfähig sein noch einen Bildlauf mit der Seite durchführen, wie im folgenden Screenshot der Rechnung mit dem **Zahlen** Wert 2000.

![Screenshot der Rechnung zum bezahlen der Rechnung in Money 2000.](images/iuiguidelines07.png)

## <a name="additional-guidelines"></a>Weitere Leitlinien

In diesem Abschnitt werden fünf nützliche Richtlinien zum Erstellen eines IUI gemäß den vier Schritten beschrieben, die im vorherigen Abschnitt beschrieben wurden.

### <a name="use-consistent-screen-templates"></a>Konsistente Bildschirm Vorlagen verwenden

Beim Entwerfen von Software, die auf das IUI-Modell folgt, sollten Sie eine Vorlage erstellen, die für jeden Bildschirm als Leitfaden verwendet werden soll. Das induktive Modell erfordert nicht, dass Sie eine bestimmte Vorlage verwenden. Es gibt viele mögliche Variationen, die ein induktives Design erfüllen können. Ihr Produkt benötigt möglicherweise nur eine Vorlage für alle Bildschirme, oder Sie können mehrere verschiedene Vorlagen für verschiedene Zwecke erstellen.

Eine gute Vorlage ermöglicht einem neuen Benutzer, schnell zu verstehen, wie die Bildschirme des Produkts funktionieren. Eine konsistente Verwendung der Vorlage auf den Bildschirmen des Produkts ermöglicht einen guten Benutzeroberflächen Fluss von Bildschirm zu Bildschirm. Wenn Benutzer lernen, dass dieselben Elemente an denselben Stellen angezeigt werden, können Sie jeden neuen Bildschirm schneller überprüfen und verwenden.

### <a name="provide-screens-for-starting-tasks"></a>Anzeigen von Bildschirmen zum Starten von Aufgaben

Produkte, die mit IUI entwickelt wurden, verwenden häufig spezielle Bildschirme, die für das Starten von Benutzern in Gruppen von Aufgaben Diese Bildschirme werden als Aktivitätsseiten bezeichnet, da Sie Verwandte Gruppen von allgemeinen Aufgaben organisieren. Aktivitätsseiten stellen einen Ausgangspunkt für Benutzer dar. Eine Aktivitätsseite stellt in der Regel Links zu anderen Seiten dar, auf denen der Benutzer tatsächlich arbeitet. Aktivitätsseiten Fragen den Benutzer nach "Was möchten Sie jetzt tun?". und stellen eine Liste möglicher Antworten vor. Aktivitätsseiten können einer speziellen Vorlage folgen, damit Sie von den Benutzern erkannt werden können.

Eine Aktivitätsseite macht eine gute Standard Startseite für ein Produkt. Wenn Benutzer eine Anwendung starten, haben Sie im Allgemeinen eine Vorstellung von der Aufgabe, die Sie erreichen möchten. Normalerweise ist der Grund für das Starten des Produkts eine kleine Anzahl von sehr häufigen Aufgaben. Dies wird von der Standard Startseite des Produkts erkannt, indem es offensichtlich wird, wie häufige Aufgaben gestartet werden.

Die **Start** Seite Money 2000 ist ein Beispiel für eine Aktivitätsseite. Standardmäßig wird dieser Bildschirm angezeigt, auf dem der Zugriff auf allgemeine Finanz Aufgaben, z. b. das bezahlen einer Rechnung und der Lastenausgleich, beim Starten der Anwendung angezeigt wird.

Der folgende Screenshot zeigt die **Start** Seite Money 2000.

![Screenshot der Startseite für Money 2000. eine Aktivitätsseite, die einige häufige Aufgaben auflistet und Links zu Gruppen von Aufgaben auf anderen Seiten enthält.](images/iuiguidelines08.png)

Da Money viele finanzielle Features bietet, werden nur die gängigsten Finanz Aufgaben auf die **Start** Seite angepasst. Für alle anderen Aufgaben ist die **Start** Seite mit einem neben geordneten Satz von Aktivitätsseiten verknüpft, die als Finanzzentren bezeichnet werden. Jeder Hauptbereich des Geldes stellt ein Finanzzentrum bereit. Diese Bildschirme zeigen die nächste Ebene von Aufgaben an und fungieren als springende Punkte für alle Features in den einzelnen Bereichen.

Der **Bereich Money** Tax enthält z. b. die Steuer bezogenen Features des Produkts. Der Bereich **Steuern** bietet Links zu diesen Features auf einer **steuermittelseite** , wie im folgenden Screenshot zu sehen.

![Screenshot der Seite Money 2000 Tax Center. ](images/iuiguidelines09.png)

Eine Aktivitätsseite kann auch wesentlich einfacher sein, wenn weniger Optionen zur Verfügung stehen. Der folgende Screenshot zeigt, wie eine Aktivitätsseite zum Verwalten von Windows-Benutzerkonten verwendet werden kann.

![Screenshot einer Money-2000-Aktivitätsseite zum Verwalten von Windows-Benutzerkonten. ](images/iuiguidelines10.png)

### <a name="make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen"></a>Machen Sie sich offensichtlich, wie die Aufgabe mit den Steuerelementen auf dem Bildschirm durchgeführt werden soll.

Die beste Möglichkeit, diese Richtlinie zu befolgen, besteht darin, einen geeigneten Bildschirm Titel auszuwählen und den Umfang der primären Aufgaben auf die gängigsten Aufgaben einzuschränken. Wenn Sie einen klaren Titel und Zweck für die Seite erreicht haben, ist die Auswahl der richtigen Steuerungsgruppe unkompliziert.

### <a name="provide-an-easy-way-to-complete-a-task-and-start-a-new-one"></a>Stellen Sie eine einfache Möglichkeit bereit, um eine Aufgabe abzuschließen und eine neue zu starten

Das letzte Hindernis, dem ein Benutzer auf einem Bildschirm angezeigt wird, ist herauszufinden, wann und wie es verlassen werden soll. Der Benutzer verlässt den Bildschirm in der Regel durch Klicken auf einen Link oder durch Ausführen eines Befehls, der zu einem anderen Bildschirm navigiert. Diese Links können im Bereich Bildschirminhalt, in der Aufgabenliste oder auf Navigations Symbolleisten angezeigt werden. Benutzer können auch einen Bildschirm verlassen, indem Sie die aktuelle Datei oder die Anwendung selbst schließen.

Die Aufgabe auf einigen Bildschirmen besteht darin, einen Vorgang vorzubereiten, der vom Benutzer bestätigt oder abgebrochen werden muss. Solche Bildschirme bieten in der Regel einen Link, der den Vorgang ausführt und einen Commit ausführt, und einen weiteren Link, der abbricht. Wenn der Benutzer diese Optionen ignoriert und auf einen anderen Link klickt, sollte das Programm die weniger zerstörerische Option ausführen. Bildschirme sollten angeben, was geschehen soll, wenn der Benutzer diesen Pfad annimmt. Sie können die Verknüpfungen so formulieren, dass Sie deutlicher werden. Beispielsweise impliziert eine Commit-Schaltfläche mit der Bezeichnung "Änderungen speichern", dass auf dem Bildschirm vorgenommene Änderungen erst wirksam werden, wenn auf diese Schaltfläche geklickt wird.

Auch wenn die Benutzer Sie jederzeit verlassen können, bieten Sie möglicherweise trotzdem einen Link, der einen offensichtlichen Abbruch der Seite vorschlägt. Dasselbe gilt für Seiten, die nur statische Informationen anzeigen. Weitere Informationen zu diesem Betreff finden Sie im Abschnitt [Bereitstellen eines löschen auf der Seite](#provide-a-clear-exit-from-the-page).

### <a name="starting-and-completing-processes"></a>Starten und Abschließen von Prozessen

Bei diesem Artikel handelt es sich bei Prozessen um Techniken zum Umgang mit Aufgaben, bei denen der Benutzer mehr als einen Bildschirm verwendet.

Angenommen, ein Benutzer klickt auf einen Link in der Inhalts-oder Aufgabenliste eines Bildschirms und wird zu einem anderen Bildschirm weitergeleitet. Diese Seite kann wiederum der erste einer Reihe von Bildschirmen sein, die ein Gesamtergebnis erreichen. Am Ende dieser Reihe von Bildschirmen möchte der Benutzer zum Bildschirm zurückkehren, der dem Prozess vorangestellt ist. Der Benutzer kann auf mindestens zwei Arten zurückkehren? Klicken Sie wiederholt auf die Schaltfläche "zurück", oder kehren Sie zur Startseite zurück? aber keine dieser Methoden ist offensichtlich oder natürlich. Die meisten Benutzer erwarten, dass auf dem letzten Bildschirm eine Schaltfläche gefunden wird, die Sie direkt an den ursprünglichen Bildschirm zurückgibt.

Das IUI-Modell unterstützt dieses Szenario durch das Konzept eines Prozesses, einen Bildschirm oder eine Reihe von Bildschirmen, die als navigationseinheit behandelt werden. Benutzer können den Prozess eingeben, ihre Bildschirme durcharbeiten und auf dem letzten Bildschirm eine Schaltfläche Suchen, die Sie an der Stelle zurückgibt, an der Sie gestartet wurden. Wichtig: der Benutzer kann den Prozess von mehreren Stellen im Produkt aus starten. Benutzer werden immer an die Stelle zurückgegeben, an der Sie gestartet wurden, unabhängig davon, wo Sie mit dem Prozess begonnen haben.

### <a name="process-name"></a>Prozessname

Jedem Prozess sollte ein Name zugewiesen werden, und der Name sollte auf jedem Bildschirm des Prozesses angezeigt werden. Money 2000 verwendet diesen Ansatz. Jeder Bildschirm, der Teil eines allgemeinen Prozesses ist, enthält den Namen dieses Prozesses am oberen Rand. Dieser Prozess Name wird weniger wichtig angezeigt als der eindeutige Titel des Bildschirms, da er weniger wichtig ist. Der Prozess Name erinnert Benutzer daran, welchen Prozess Sie durchführen, und stärkt die Vorstellung, dass alle Bildschirme im Prozess Teil einer einzelnen Funktion sind. Beispielsweise enthält der Bereich **Money** **Tax einen Steuer schätzungs** Prozess, der mehrere Bildschirme umfasst. Jeder Bildschirm in diesem Prozess zeigt sowohl den Namen des gemeinsamen Prozesses als auch den eindeutigen Bildschirm Titel an.

### <a name="implementation-of-processes"></a>Implementierung von Prozessen

Der gleiche Prozess kann über verschiedene Links auf unterschiedlichen Bildschirmen gestartet werden, und Benutzer werden immer zur richtigen Startseite zurückgegeben. Dieses Verhalten kann nicht über einen hart codierten Link auf dem letzten Bildschirm des Prozesses erreicht werden, da das Ziel der Verknüpfung variiert. Stattdessen kann die Anwendung dieses Verhalten implementieren, indem ein Stapel aktiver Prozesse verwaltet wird, unabhängig vom normalen Navigations Stapel, der von den Befehlen " **zurück** " und " **Vorwärts** " verwendet wird. Wenn der Benutzer einen Prozess startet, wird der Startbildschirm per Pushvorgang auf dem Prozess Stapel abgelegt. Wenn der Benutzer auf dem letzten Bildschirm des Prozesses auf die Schaltfläche " **done** " klickt, wird die aktuelle Startseite vom Stapel angezeigt, und der Benutzer wird an den Bildschirm zurückgegeben.

Wenn Benutzer in einem Prozess von einem Bildschirm weg navigieren, bleibt der Prozess im Prozess Stapel aktiv. Benutzer können den Prozess zum Sichern auf dem Bildschirm beenden, an dem Sie Sie verlassen haben, und dann fortfahren. Dies ermöglicht es Benutzern, eine Umleitung und eine Sicherungskopie vorzunehmen und dann mit dem Prozess fortzufahren. Um zu sehen, wie dieses Verhalten funktioniert, starten Sie jeden Online-Einkaufsprozess auf dem World Wide Web, verlassen Sie die Website, und drücken Sie dann die Schaltfläche " **zurück** ". Sie können in der Regel den Ort auswählen, an dem Sie aufgehört haben.

### <a name="done-button"></a>Schaltfläche „Fertig“

Um einen Bildschirm zu beenden und zum nächsten Bildschirm zu gelangen, können Bildschirme eine Schaltfläche am unteren Rand der Seite anzeigen. Die Bezeichnung dieser Schaltfläche lautet "Next", "Done" oder etwas ähnliches. Wenn die Schaltfläche den Prozess beendet und der Prozess von mehreren Speicherorten aus aufgerufen werden kann, kann die Beschriftung der Schaltfläche " **done** " den Namen der aufrufenden Position enthalten.

### <a name="navigation-bar"></a>Navigationsleiste

Auf jedem Bildschirm können Benutzer entscheiden, dass Sie mit dem aktuellen Bereich des Produkts fertig sind und etwas anderes starten möchten. Möglicherweise möchten Sie den aktuellen Bildschirm nicht explizit vervollständigen, bevor Sie zu einem anderen Teil des Produkts übergehen. Eine Navigations Symbolleiste bietet dem Benutzer eine Reihe von Links zum Starten neuer Aufgaben. Wie bei anderen Listen von Aufgaben Verknüpfungen sollten diese dem Prinzip entsprechen, den nächsten Navigations Schritt offensichtlich zu machen, der im folgenden Abschnitt ausführlich erläutert wird.

### <a name="make-the-next-navigational-step-obvious"></a>Machen Sie den nächsten Navigations Schritt offensichtlich

Nur wenige Programme können gleichzeitig alle zugehörigen Features verfügbar machen. Benutzer müssen im Allgemeinen durch ein Programm navigieren, um ein bestimmtes Feature zu finden. Die Benutzer sind bei der Navigation erfolgreicher, wenn Sie leicht erkennen können, wie Sie wenigstens einen Schritt näher am gewünschten Ergebnis erhalten. Bildschirme, die IUI verwenden, sind mit diesem Prinzip konzipiert.

Aktivitätsseiten zeigen z. b. nicht unbedingt alle denkbaren Aufgaben oder Ziele an, die der Benutzer von diesem Punkt aus möglicherweise erreichen möchte. Stattdessen stellt die Aktivitätsseite eine Liste von Aufgaben bereit, die ausreichend sind, damit Benutzer problemlos den entsprechenden Link zum Klicken ermitteln können, auch wenn Sie nur auf eine andere Seite der Links gelangen. Die häufigsten Aufgaben sollten am wichtigsten sein und die geringste Menge an Navigation erfordern. Weniger häufige Aufgaben können mehr Schritte erfordern.

Im folgenden finden Sie ein Beispiel aus Money 2000. Angenommen, Benutzer möchten einen Vorgang ausführen, der nur gelegentlich durchgeführt wird, z. b. das Überprüfen der geschätzten Menge der Einkommens Steuerzahlung im nächsten Jahr. Benutzer beginnen zunächst, diese Funktion auf der Startseite von Money 2000 zu suchen. Da die Funktion nicht in der Liste der allgemeinen Aufgaben angezeigt wird, müssen Sie die Liste der Finanzbereiche scannen. Der Bereich " **Steuern** " klingt vielversprechend, also klicken Sie darauf. Die Seite " **Tax Center** " enthält einen Link zu dem Steuerelement, nach dem Sie suchen, um darauf zu klicken und ihre Aufgabe abzuschließen. Durch Anwenden von IUI-Prinzipien können Benutzer mit Money 2000 intuitiv feststellen, wonach Sie suchen.

## <a name="user-assistance"></a>Benutzerunterstützung

In diesem Abschnitt werden empfohlene Richtlinien für die Integration von Benutzer Unterstützungs Text in ein Produkt beschrieben, das IUI verwendet.

Die primäre Unterstützung bezieht sich auf den gesamten Text, der auf dem Bildschirm angezeigt wird (wie im folgenden Screenshot zu sehen). Die primäre Unterstützung bietet Aufgaben zentrierte, Text Hinweise, damit Benutzer alle auf dem Bildschirm dargestellten Informationen leicht verstehen können. Sie verstehen den Zweck der Seite und die Beziehung zwischen Objekten, um Aufgaben zu erledigen. Da der Text direkt auf dem Bildschirm angezeigt wird, finden Sie hier die Informationen, mit denen Sie Fragen wie "Was soll ich tun?" beantworten. ist leicht zugänglich und hochgradig sichtbar, ohne dass der Benutzer eine Aktion durchführen muss.

![Screenshot des Bildschirms zum Einrichten des Kontos mit dem Geld 2000.](images/iuiguidelines11.png)

Die sekundäre Unterstützung besteht aus dem gesamten Text, der auf dem Bildschirm nicht sichtbar ist, und erfordert eine gewisse Benutzerinteraktion, z. b. das Klicken auf ein Benutzeroberflächen Element oder den Mauszeiger darauf. Dieser Inhalt ist nicht zwingend erforderlich, um die Aufgabe zu erledigen, aber Sie ist weiterhin direkt verknüpft.

### <a name="primary-assistance"></a>Primäre Unterstützung

Die primäre Unterstützung kann einige oder alle der folgenden Komponenten enthalten:

-   Bildschirm Titel

    Beispiel: Ändern des Bilds

    Der Bildschirm Titel ist das erste und wichtigste Element, das auf dem Bildschirm angezeigt wird. Der Zweck besteht darin, die Aufgabe, die auf dieser Seite abgeschlossen werden kann, in der Sprache des Benutzers zu beschreiben. Der Bildschirm Titel sollte das Beschreiben der Details zum Ausführen der Aufgabe vermeiden. Der Text im Bildschirm Titel sollte nur auf die Hauptaufgabe des Bildschirms verweisen. Als Faustregel gilt: je einfacher und kürzer die Beschreibung der Aufgabe, desto besser ist die Aufgabe. Ausführlichere Informationen zu diesem Thema finden Sie unterschritt 2: [State the Task](#step-two-state-the-task).

-   Bildschirm Titel

    Beispiel: Sie können auch ein neues Bild aus dem Internet herunterladen.

    Selbst bei sorgfältiger Anstrengung reicht der Bildschirm Titel möglicherweise nicht aus, um eine komplexe Aufgabe adäquat zu erläutern. Mithilfe des Untertitels können Sie den Zweck des Bildschirms vertiefen. Sie können einen Untertitel verwenden, um den Zweck der Seite zu verdeutlichen, zusätzliche Aufgabenbeschreibungen bereitzustellen oder die Erwartungen festzulegen. Benutzer, die den Untertitel nicht lesen, sollten die Seite erfolgreich verwenden können. Ebenso wie der Titel sollte der Untertitel das Beschreiben von Details zum Abschließen der Aufgabe vermeiden.

-   Aufgaben

    Beispiel: Ändern des Bildschirmschoners

    Aufgaben können als Text Verknüpfungen oder grafische Bilder dargestellt werden, die eine Benutzerinteraktion erfordern. Befehle, die als Text Verknüpfungen dargestellt werden, sollten Verb-basiert sein und als klare und präzise Aufgaben geschrieben werden.

-   Bezeichnungen für Befehls Schaltflächen

    Beispiel: Erstellen eines Kennworts

    Es gibt drei Arten von Befehls Schaltflächen:

    -   Abbrechen
    -   Fertig
    -   Commit

    Die Schaltflächen Abbrechen und durchführen verwenden einfach "Abbrechen" und "abgeschlossen" als Bezeichnungen. Für Commit-Schaltflächen sollten anstelle von "OK" aktive Text Bezeichnungen verwendet werden. Verwenden Sie z. b. "Create Password" anstelle von "OK".

-   Bezeichnungen für andere Steuerelemente

    Beispiel: eingeben Ihres Kennworts

    Bezeichnungen für Steuerelemente, wie z. b. Options Felder, Kontrollkästchen und Textfelder, sollten eindeutig und kurz geschrieben werden, damit Benutzer genau wissen, wofür die Steuerelemente stehen, welche verwendet werden müssen und welche Informationen für Ihre Aufgabe bereitgestellt werden müssen.

-   Links zu verknüpften Aufgaben

    Beispiel: Verwandte Aufgaben-ändern eines anderen Kontos

    Links zu verknüpften Aufgaben sind explizite Einstiegspunkte zu anderen Aufgaben im Zusammenhang mit der aktuellen Funktion. Sie sollten als aufgabenbasierte Verknüpfungen geschrieben werden.

-   Links zu "Siehe auch"

    Beispiel: siehe auch: Ändern des Designs

    Links zu "Siehe auch" sind sekundäre Tasks. Diese beziehen sich auf den primären Task, aber der Benutzer wird aus dem aktuellen Kontext herausgenommen. Diese sollten als reguläre Aufgaben Verknüpfungen angezeigt werden. Weitere Informationen zu sekundären Aufgaben finden Sie unter [visueller Entwurf sekundärer Aufgaben](#visual-design-of-secondary-tasks).

### <a name="secondary-assistance"></a>Sekundäre Unterstützung

Sekundäre Unterstützung kann einige oder alle der folgenden Komponenten enthalten:

-   Infotipps

    Mithilfe eines infotip können Sie dem Benutzer zusätzliche Informationen zu einer Aufgaben Verknüpfung oder einer Befehls Schaltfläche bereitstellen. Beispielsweise könnte ein infotip über einen Aufgaben Link lauten: "zeigt eine Seite an, auf der Sie ein Bild auswählen können, das mit Ihrem Konto verwendet werden soll." Der infotip wird angezeigt, wenn der Benutzer mit der Maus auf das zugehörige Objekt zeigt. Sie sollten infotips für alle Elemente der Benutzeroberfläche erstellen, auf die der Benutzer klicken kann.

-   "Weitere Informationen" zu Hilfe Themen

    Beispiel: Weitere Informationen zum Herunterladen einer Datei

    "Weitere Informationen" Links zu offenen Hilfe Themen, wie z. b. Featureübersichten, konzeptionelle Informationen, unterstützende Informationen und Informationen zu Prozeduren. Um die Übersichtlichkeit zu verringern, sollten Sie die Anzahl der Hilfe Themen zu "Informationen" auf dem Bildschirm minimieren.

## <a name="appendix-designing-and-testing-microsoft-money-2000"></a>Anhang: Entwerfen und Testen von Microsoft Money 2000

Dieser Abschnitt wurde anhand der eigenen ersten Beschreibungen des Designers angepasst. Es wird erläutert, wie das Money 2000-Team den Entwurfs-und Testprozess für das IUI-Modell geändert hat.

### <a name="designing-and-testing-money-2000"></a>Entwerfen und Testen von Money 2000

Das Entwerfen von Money 2000 mithilfe des induktiven Navigations Modells führte dazu, dass das Team Entwürfe für eine lange Zeit im Produkt aufwies. Da die Prinzipien des Modells einfach sind, war es einfach, das Modell im Entwurfsprozess zu übernehmen und damit zu bleiben. Am Ende haben die Designer der Meinung, dass das Modell Ihnen geholfen hat, bessere Entwürfe zu erstellen, als Sie ohne dieses Modell erzeugt werden könnten.

### <a name="clearer-titles-and-designs"></a>Klarere Titel und Entwürfe

Die Designer von Money 2000 haben bemerkt, dass Sie häufig Funktionen mithilfe von Wörtern beschreiben würden, die eigentlich nicht auf dem Bildschirm angezeigt wurden. Im IUI-Modell sollten sich Bildschirme erklären. Das Team hat z. b. erklärt, dass der Bildschirm mit der Bezeichnung **Zahlungs Kalender** zum bezahlen von Rechnungen gedacht war. In Money 2000 heißt der Bildschirm **Pay-Rechnungen**. Alle Elemente, die nicht mit diesem Zweck verknüpft sind, wurden auf die untergeordneten Bildschirme verschoben, was zu einem klareren Entwurf führte.

Ein weiteres Beispiel ist ein Bildschirm mit dem Namen **Online Financial Services-Manager**. Das Team hat eine einfache Erläuterung des Zwecks dieses Bildschirms kennengelernt. Wenn Sie nicht bei einer gefunden werden konnten, haben Sie diesen Bildschirm entfernt und seine Features auf logisch definierte Seiten verteilt.

### <a name="helping-new-designers"></a>Unterstützung neuer Designer

Das Team fand Ihnen die einfache unter Lehre von IUI-Entwurfs Techniken für neue, unerfahrene Software Designer. Mit den Techniken konnten Designer auf allen Erfahrungsebenen ihre Entwürfe auswerten, indem Sie Bildschirm Titel als Test der Klarheit verwenden. Wenn Sie gezwungen sind, einen klaren und präzisen Titel auf einem schlecht entworfenen Bildschirm zu platzieren, haben Designer schnell erkannt, dass kein Titel für die Seite ausreichend ist. Sie erkannten, dass das Problem nicht in der Auswahl von Wörtern für einen Titel, sondern in einem fehlerhaften Bildschirmdesign aufgetreten ist. Mit diesem Verständnis können Sie den Bildschirm umgestalten, um eine klarere Benutzerinteraktion und somit einen klareren Titel zu unterstützen.

### <a name="including-writers"></a>Einschließen von Writern

Beim Entwurf des Entwurfs hat das Team erkannt, dass Dokumentations Schreiber und Editoren an der Erstellung von Bildschirm Titeln beteiligt sein sollten. Writer waren in der Lage, gute Titel in früheren Versionen auszuwählen, da Sie nur in einer späten Phase beteiligt waren. Bildschirme erhielten in der Regel temporäre Arbeitstitel durch Designer oder Programmierer. Diese Titel wurden bis zum späten Ende des Produkt Zeitraums verwendet, als Writer aufgefordert wurden, mit abschließenden Bildschirm Titeln zu kommen. An diesem Punkt war es zu spät, um schlecht gestaltete Bildschirme zu bearbeiten.

Im Gegensatz dazu beteiligte das Money 2000-Team Writer in den frühesten Phasen des Entwurfsprozesses. Dies hat wertvolle Eingaben für Bildschirm Titel zur Verfügung gestellt, wenn Sie den Entwurf weiterhin unterstützen können. Wenn ein Bildschirm zu komplex ist, um einen klaren Titel zuzulassen, können die Writer vorschlagen, dass die Seite neu gestaltet werden soll.

Am Ende des Projekts glaubten die Writer und Designer, dass die Bildschirm Titel klarer und stärker sind als in früheren Versionen. Die Writer fanden außerdem eine einfachere Erläuterung neuer Seiten, sodass das Produkt einfacher dokumentiert werden kann. Alle Teammitglieder dachten, dass das Produkt mit allen Disziplinen in der Entwurfsphase besser und einfacher zu verwenden ist.

### <a name="usability-tests"></a>Benutznutzbarkeits Tests

Beim Entwickeln von Money 2000 hat das Team mehrere Nutzbarkeits Tests durchgeführt, um die Unterschiede zwischen der alten Navigationsstruktur von Money 99 und den Änderungen, die aufgrund der Anwendung des IUI-Modells vorgenommen wurden, zu untersuchen.

### <a name="prototype-testing"></a>Prototyptests

Im frühzeitigen Verlauf des Produkt Entwicklungsprozesses haben die Designer einen Prototyp erstellt, um zu untersuchen, wie Benutzer auf IUI reagieren würden. Diese Arbeit wurde sehr früh im Entwicklungsprozess durchgeführt, um Zeit zum Verfeinern der Modell Prinzipien zu bieten, bevor Programmierer mit der Überarbeitung des Produkts beginnen.

Das Team hat einen Prototyp in Microsoft Visual Basic und HTML erstellt, das simulierte persönliche Finanzaktivitäten normalerweise in Geld durchgeführt hat. Im Prototyp konnten Benutzer zu mehr als 50 Seiten navigieren, die die Hauptbereiche des Produkts darstellen. In diesen Bereichen könnten Sie Finanzkonten einrichten, Rechnungen bezahlen, Berichte anzeigen und mit ihren Investitionen arbeiten.

Elf Teilnehmer haben denselben Satz von Aufgaben in Money 99 und dem IUI-Prototyp ausgeführt. Ihnen wurde nach dem Zufallsprinzip zugewiesen, dass Sie zuerst eines der Produkte verwenden. Vier Teilnehmer waren aktuelle Money-Benutzer, vier waren die aktuellen Benutzer eines konkurrierenden Produkts, und drei hatten bisher nie ein persönliches Finanzprodukt verwendet.

Die Gesamt Einstellungen gaben an, dass es sich bei den vier aktuellen Benutzern mit dem bevorzugten Geld um 99 (die Version, die Sie zu Hause verwendet haben), während die restlichen sieben Benutzer den neuen Prototyp für die aktuelle Version bevorzugten. Für alle anderen Measures gab es keinen Unterschied zwischen den Benutzern der drei Gruppen. Im Hinblick auf die Gesamtleistung befanden sich die Benutzer doppelt so 2,82 99 oft im falschen Bereich des Produkts wie im Prototyp (1,45-mal pro Task). Andere Einstellungsdaten und Leistungs Kennzahlen, die nicht signifikant sind, haben anscheinend den Prototyp bevorzugt. Basierend auf diesen Daten und anderen Tests entschied sich das Money-Produktteam für die Einbindung von IUI-Prinzipien in Money 2000.

### <a name="product-testing"></a>Produkttests

Nachdem der Großteil des Codes für das Produkt abgeschlossen wurde, hat das Team eine weitere Nutzbarkeits Studie durchgeführt, um die endgültige Implementierung von IUI zu untersuchen. In diesem Test wurden 10 Teilnehmer, die bisher nie ein persönliches Finanzprodukt verwendet haben, für die Verwendung von Money 99 oder Money 2000 ausgewählt. Alle Benutzer haben dieselben Aufgaben ausgeführt.

Die Benutzer von Money 2000 haben 89% der Aufgaben erfolgreich abgeschlossen, während die Benutzer des Geldes 99 erfolgreich nur 74% der Aufgaben abgeschlossen haben. Wie auch bei dem Prototyp scheint es auch, dass die Benutzer schneller, aber nicht bedeutend anders sind, bei der Navigation in Money 2000 im Vergleich zum Money 99. Außerdem verbessern die allgemeinen übergreifenden Zufriedenheits Maßnahmen für die Navigation auch eine höhere Summe für Geld 2000 als für Money 99.

### <a name="controlled-testing"></a>Gesteuerte Tests

Da Money 2000 enorm und komplex ist, eignet es sich nicht gut für die Durchführung von kontrollierten Experimenten in den Auswirkungen der Anwendung von IUI. Stattdessen hat das Team eine eingeschränktes Umgebung für den Test erstellt.

Der Test umfasste eine "Börsen-Viewer"-Anwendung, mit der Benutzer die Anzeige eines auf dem Bildschirm angezeigten Aktienmarkt Berichts ändern konnten. Benutzer können ändern, welche Datenspalten im Bericht enthalten waren, die Reihenfolge der Berichts Spalten, ihre Ausrichtung und die Anzahl der verwendeten Dezimalstellen. Die Designer wollten sehen, wie ein IUI-Ansatz für diese Aufgabe im Vergleich zu einer herkömmlichen grafischen Benutzeroberfläche durchgeführt würde.

Der folgende Screenshot zeigt die herkömmliche Benutzeroberfläche, die im Test verwendet wird. In einem einzelnen Dialogfeld werden alle Berichts Anpassungs Aufgaben ausgeführt. Viele Anwendungen bieten ein ähnliches Dialogfeld zum Auswählen einer Teilmenge aus einer Liste von Elementen. Das Dialogfeld enthält zwei Listen: in der linken Liste werden alle verfügbaren Berichts Spalten angezeigt, und die Rechte zeigt die Teilmenge der Spalten an, die der Benutzer für den Bericht ausgewählt hat. Zusätzliche Steuerelemente ändern die Reihenfolge und die Formatierungs Attribute für in der rechten Liste ausgewählte Berichts Spalten.

![Screenshot eines herkömmlichen Dialog Felds.](images/iuiguidelines12.png)

Für die IUI-Version dieser Aufgabe hat das Team eine Web-Style-Anwendung erstellt. Jede Anpassungsaufgabe wurde auf einer separaten Seite platziert. Die Anwendung enthielt außerdem eine Hauptseite, die im folgenden Screenshot gezeigt wird, mit der Benutzer gefragt werden, wie der Bericht angepasst werden soll.

![Screenshot eines IUI-Test Bildschirms.](images/iuiguidelines13.png)

Wenn Sie auf der Hauptseite auf Links klicken, werden die Benutzer zu weiteren Seiten aufgefordert, bestimmte Anpassungs Aufgaben auszuführen. Der folgende Screenshot zeigt z. b. die Seite, die zum Auswählen von Berichts Spalten verwendet wird.

![Screenshot eines IUI-Test Bildschirms zum Auswählen von Berichts Spalten.](images/iuiguidelines14.png)

In den Tests beider Versionen wurden die Betreff aufgefordert, Berichte von einem bestimmten Startstatus (auf dem Bildschirm angezeigt) an einen angegebenen Ziel Status anzupassen (angezeigt in einem Papier Handout). Der Computer hat die Zeitspanne und die Anzahl der Versuchspersonen verfolgt, die zum Anpassen des Berichts unternommen wurden. Der Computer hat die Benutzer informiert, als Sie den Bericht erfolgreich angepasst haben.

Der Test enthielt 88 Teilnehmer. Jeder Teilnehmer wurde aufgefordert, eine Gruppe von 11 Berichten mit einer der beiden Versionen der Anwendung anzupassen. Außerdem hat 72 dieser Teilnehmer eine Woche später zurückgegeben, um eine andere Gruppe von 11 Berichten mit derselben Version aus der ersten Sitzung anzupassen. Jeder Betreff wurde als Anfänger Computerbenutzer klassifiziert, wobei hauptsächlich der Computer für e-Mail, Wiedergabe von Solitär und das Surfen im Web verwendet wird.

Es gab keine signifikanten Unterschiede zwischen den Benutzern der beiden Versionen oder einer der anderen relevanten Variablen. Benutzer haben Aufgaben mit derselben Geschwindigkeit ausgeführt, die gleichzeitig auf der Aufgabe durchlaufen wurden, und hatten die gleichen allgemeinen Zufriedenheits Bewertungen für die beiden Versionen. Mit diesem Test konnten daher keine Measures angezeigt werden, bei denen IUI zu einer Verbesserung oder Verschlechterung der Leistung oder der subjektiven Bewertung geführt hat.

Es könnte so argumentiert werden, dass der Zeitaufwand für die Ausführung der Aufgabe größer ist, wenn der Benutzer mehr navigieren muss, um die Aufgabe auszuführen. Obwohl dieses Experiment dieses Ergebnis nicht vorschlägt, ist es wichtig zu beachten, dass die durchschnittlichen Leistungszeiten und die zugehörigen Standardabweichungen für die beiden unterschiedlichen Ansätze für diese Aufgabe nahezu identisch waren.

Weitere Untersuchungen sind erforderlich, um zu ermitteln, ob es messbare Verbesserungen bei der Verwendung von IUI gibt. Dieser Test enthielt zumindest keinen Beweis, dass IUI die Leistung oder die Produktnutzung beeinträchtigt.

### <a name="comparison-with-web-sites"></a>Vergleich mit Websites

Viele gut entworfene Websites verwenden Prinzipien, die dem in diesem Dokument beschriebenen IUI-Modell ähneln. Dies ist wahrscheinlich ein Nebeneffekt der Funktionsweise des webwebdiensts. Da es schwierig ist, komplexe Interaktionen zwischen Steuerelementen auf einer einzelnen Webseite zu implementieren, unterbrechen Designer häufig Aufgaben in Teile, die mehrere Fahrten zum Server umfassen, um eine neue Seite zu erhalten. Einige Websites enthalten sogar Seitentitel, die den Zweck der Seite eindeutig angeben.

Entwickler von herkömmlichen Anwendungen haben einen viel umfassenderen Satz an Tools. Dies bietet mehr Flexibilität, bietet aber auch mehr Möglichkeiten, komplexe und verwirrende Seiten zu erstellen. Beim Erstellen von induktiven Benutzeroberflächen sollten Designer diese Leistung mit Bedacht verwenden und sich auf die Klarheit und Einfachheit von Werten freuen.

 

 





