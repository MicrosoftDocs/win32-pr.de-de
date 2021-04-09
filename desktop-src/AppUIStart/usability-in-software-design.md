---
title: Nutzbarkeit beim Software Entwurf
description: In diesem Thema wird das Konzept der Nutzbarkeit vorgestellt und erläutert, warum es ein wichtiger Bestandteil eines beliebigen Software Entwurfsprojekts sein sollte.
ms.assetid: 912b3224-e36d-44d6-98fa-a7f28e68a2d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b302e63a475d060748e896440b28915816d910e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036508"
---
# <a name="usability-in-software-design"></a>Nutzbarkeit beim Software Entwurf

In diesem Thema wird das Konzept der Nutzbarkeit vorgestellt und erläutert, warum es ein wichtiger Bestandteil eines beliebigen Software Entwurfsprojekts sein sollte.

-   [Introduction (Einführung)](#introduction)
-   [Definieren der Benutzerfreundlichkeit](#defining-usability)
    -   [Einfache Verwendung](#ease-of-use)
    -   [Nutzbarkeit und Dienstprogramm](#usability-vs-utility)
    -   [Im Vergleich zur Verwendung](#liking-it-vs-using-it)
    -   [Ermittlung im Vergleich zu lernen und Effizienz](#discovery-vs-learning-vs-efficiency)
    -   [Slogans funktionieren nicht](#slogans-do-not-work)
-   [Warum ist die Benutzerfreundlichkeit wichtig?](#why-is-usability-important)
    -   [Warum sollten Sie sich für Sie interessieren?](#why-should-you-care)
    -   [Was kostet dies?](#what-does-it-cost)
    -   [Wie kann ich die Nutzbarkeit erhöhen?](#how-do-i-increase-usability)
    -   [Warum sollte ich Benutzer einbeziehen?](#why-should-i-involve-users)
    -   [Kann ich nicht einfach die Richtlinien befolgen?](#cant-i-just-follow-guidelines)
    -   [Muss ich ein Nutz barkeits Labor erstellen?](#do-i-need-to-build-a-usability-lab)
    -   [Wie gehe ich vor?](#how-do-i-get-started)

## <a name="introduction"></a>Einführung

Der Begriff "Nutzbarkeit" im Kontext der Software Erstellung ist ein Ansatz, bei dem der Benutzer statt des Systems in den Mittelpunkt des Prozesses versetzt wird. Diese Philosophie, die als benutzerzentrierter Entwurf bezeichnet wird, beinhaltet Benutzer Belange und das Eintreten vor dem Anfang des Entwurfsprozesses und legt fest, dass die Anforderungen des Benutzers die Wichtigkeit von Entwurfsentscheidungen sein sollten.

Der am häufigsten sichtbare Aspekt dieses Ansatzes ist das Testen der Benutzerfreundlichkeit, bei dem Benutzer arbeiten und mit der Produkt Schnittstelle interagieren und ihre Ansichten und Probleme mit den Designern und Entwicklern teilen.

## <a name="defining-usability"></a>Definieren der Benutzerfreundlichkeit

Der Abschnitt definiert, welche Nutzbarkeit im Zusammenhang mit der Softwareentwicklung bedeutet und wie Sie sich auf andere Aspekte des Entwicklungsprozesses bezieht.

### <a name="ease-of-use"></a>Einfache Verwendung

Die Nutzbarkeit ist ein Maß dafür, wie einfach es ist, ein Produkt zum Ausführen von vorgeschriebenen Aufgaben zu verwenden. Dies unterscheidet sich von den verwandten Konzepten von Utility und Likeability.

### <a name="usability-vs-utility"></a>Nutzbarkeit und Dienstprogramm

Ein zentrales Attribut, das die Qualität eines Produkts bestimmt, ist Nützlichkeit. Dadurch wird gemessen, ob die tatsächliche Verwendung eines Produkts die Ziele erreichen kann, die die Designer für diese erreichen möchten. Das Konzept der Nützlichkeit verzweigt sich weiter in das Hilfsprogramm und die Benutzerfreundlichkeit Obwohl diese Begriffe verwandt sind, sind Sie nicht austauschbar.

Das Hilfsprogramm bezieht sich auf die Fähigkeit des Produkts, eine Aufgabe oder Aufgaben auszuführen. Die weiteren Aufgaben, die das Produkt ausführen soll, desto mehr Dienstprogramm ist es.

Beachten Sie typische Microsoft MS-DOS-Wörter Prozessoren aus den späten 80er Jahren. Solche Programme stellten viele leistungsstarke Funktionen für die Bearbeitung und Bearbeitung von Text bereit, benötigten jedoch, dass Benutzer Dutzende von Arkans Tastatureingaben erlernen und merken konnten, um Sie auszuführen. Anwendungen wie diese können so lauten, dass Sie über ein hohes Hilfsprogramm verfügen (Sie bieten den Benutzern die erforderliche Funktionalität), aber wenig Nutzbarkeit (die Benutzer müssen viel Zeit und Mühe aufwenden, um Sie zu erlernen und zu verwenden). Eine gut entworfene, einfache Anwendung, wie z. b. ein Rechner, kann jedoch sehr einfach zu verwenden sein, bietet jedoch kein viel Hilfsprogramm.

Beide Qualitäten sind für Marktakzeptanz erforderlich, und beide sind Teil des Gesamtkonzepts der Nützlichkeit. Wenn ein Programm zwar hochgradig verwendbar ist, aber keinen Wert hat, wird es von niemandem verwendet. Und Benutzern, die ein leistungsfähiges Programm haben, das nur schwer zu verwenden ist, wird es wahrscheinlich gegen Sie widersprechen oder Alternativen suchen.

Mithilfe von Nutzbarkeits Tests können Sie feststellen, wie einfach es für Benutzer ist, bestimmte Aufgaben auszuführen. Es hilft Ihnen jedoch nicht direkt festzustellen, ob das Produkt selbst über einen Wert oder ein Hilfsprogramm verfügt. (Benutzer können sich im Zusammenhang mit dem Hilfsprogramm im Zusammenhang mit dem Testen der Benutzerfreundlichkeit informieren, aber Kommentare sollten mit anderen, robusteren Forschungsmethoden überprüft werden.)

### <a name="liking-it-vs-using-it"></a>Im Vergleich zur Verwendung

"Likeability" ist immer ein wünschenswert in einem Produkt. Wenn Personen wie das Produkt, ist es wahrscheinlicher, dass Sie es verwenden und es anderen Personen empfehlen. Aber wie beim-Hilfsprogramm sollten Sie darauf achten, die Sympathie in Bezug auf die Verwendbarkeit nicht zu verwechseln.

Personen, die sich häufig wie ein Produkt befinden, aus Gründen, die nicht mit dem Hilfsprogramm Sie werden möglicherweise auf den Stil oder den Status, den Sie dem Produkt zuweist, erhalten. Benutzer sind in der Regel sehr nutzbare Produkte, aber Sie sollten nicht davon ausgehen, dass ein bekanntes Produkt verwendbar ist.

Die Nutzbarkeit besteht darin, ob eine Person das Produkt verwenden kann, um die Aufgaben auszuführen, die Sie ausführen müssen. Das Testen der Benutzerfreundlichkeit misst primär die Leistung und nicht die bevorzugte. Allerdings können standardisierte Fragebögen verwendet werden, um die Einstellungen über mehrere Produkte hinweg zu messen.

### <a name="discovery-vs-learning-vs-efficiency"></a>Ermittlung im Vergleich zu lernen und Effizienz

Es gibt viele Aspekte der Verwendbarkeit, aber in der Regel bezieht sich der Begriff auf die Attribute der Ermittlung, des Lernens und der Effizienz.

-   Die Ermittlung umfasst das Suchen und Auffinden der Funktion eines Produkts als Reaktion auf einen bestimmten Bedarf. Durch das Testen der Benutzerfreundlichkeit können Sie feststellen, wie lange ein Benutzer das Auffinden eines Features und die Anzahl der Fehler (falsche Entscheidungen zum Speicherort) des Benutzers auf dem Weg nimmt.
-   Learning bezieht sich auf den Prozess, mit dem der Benutzer versteht, wie ein ermitteltes Feature verwendet wird, um eine Aufgabe abzuschließen. Benutzerbarkeits Tests können bestimmen, wie lange dieser Prozess dauert und wie viele Fehler der Benutzer beim Erlernen des Features trifft.
-   Effizienz bezieht sich auf den Punkt, an dem der Benutzer die Funktion "gemasterte" hat, und verwendet diese, ohne dass weitere Kenntnisse erforderlich sind. Mithilfe von Nutzbarkeits Tests kann festgelegt werden, wie lange es dauert, bis der erfahrene Benutzer die erforderlichen Schritte zur Verwendung der Funktion ausführt.

Diese drei grundlegenden Aspekte der Nutzbarkeit werden stark von der Art der Aufgabe und der Häufigkeit beeinflusst, mit der der Benutzer Sie ausführt. Einige Features werden so selten verwendet oder sind so komplex, dass der Benutzer Sie im Grunde jedes Mal erneut lernt. für diese Features entwickelt Microsoft häufig Assistenten, um den Benutzer durch den Prozess zu leiten.

### <a name="slogans-do-not-work"></a>Slogans funktionieren nicht

Software Entwickler stellen manchmal fest, dass einfache Slogans wie "das Produkt besser verwendbar" helfen, Probleme mit der Benutzerfreundlichkeit zu lösen. Eine positive Haltung zur Benutzerfreundlichkeit ist zwar wichtig, aber nur durch die ordnungsgemäße Verwendung von Benutzerfreundlichkeit mit normalen Benutzern, im Zusammenhang mit dem jeweiligen erstellten Produkt, können Entwickler die Informationen bereitstellen, die Sie benötigen, um ein Produkt zu erstellen, das die Anforderungen der Benutzer erfüllt. "Machen Sie das Produkt verwendbar", sollte der Slogan jedes Softwareentwicklers lauten, aber es ist nur sinnvoll, wenn der Entwickler weiß, welche Benutzerfreundlichkeit es bedeutet. Das Testen mit normalen Benutzern ist die zuverlässigste Möglichkeit, herauszufinden.

## <a name="why-is-usability-important"></a>Warum ist die Benutzerfreundlichkeit wichtig?

Der Abschnitt beantwortet einige häufig gestellte Fragen dazu, warum die Benutzerfreundlichkeit wichtig ist und wie Sie Benutzer zentrierte Entwurfs Prinzipien in den Entwicklungsprozess integrieren können.

### <a name="why-should-you-care"></a>Warum sollten Sie sich für Sie interessieren?

Wenn die Überlegungen zur Nutzbarkeit nicht bereits in den Produkt Entwurfsprozess integriert wurden, Fragen Sie sich vielleicht, warum dies notwendig oder wünschenswert ist. Schließlich ist es sicherlich möglich, ein funktionierendes, fehlerfreies Produkt zu veröffentlichen, ohne jegliche Nutzbarkeit auszuführen. Die Einbindung von Benutzer zentrierten Entwurfs Prinzipien kann jedoch zu einem viel verbesserten Produkt in verschiedenen Bereichen führen.

Der beste Grund für die Durchführung von Nutzbarkeits Tests besteht darin, die Anzahl der Support Anrufe durch Benutzer zu verringern. Schlechte Nutzbarkeit ist ein wichtiger Grund, warum Benutzer den technischen Support von Software anrufen, und jeder Softwareunternehmen und Informationsdienste-Manager weiß, wie teuer der Produktsupport sein kann. Außerdem erhöht das Berechnen von Benutzern für die Unterstützung die potenziellen Unzufriedenheit mit dem Produkt. Wenn Benutzer die Verwendung Ihres Produkts leicht finden, müssen Sie nicht so häufig technische Unterstützung erhalten.

Für Software, die für die interne Verwendung erstellt wurde, ist der beste Grund für die Verwendbarkeit ein wichtiger Bestandteil des Entwicklungsprozesses, die Trainingskosten zu reduzieren. Ein sehr nutzbares Produkt ist für Benutzer viel einfacher zu erlernen als eine, bei der die Benutzerfreundlichkeit keine hohe Priorität hatte. Benutzer erlernen Features schneller und bewahren ihr Wissen länger auf, was sich direkt mit geringeren Schulungskosten und-Zeit korreliert.

Nutzbarkeits Tests helfen, die Benutzer Akzeptanz zu verbessern. Die Annahme ergibt sich aus einer Reihe von Faktoren, einschließlich Nutzbarkeit, Hilfsprogramm und Likeability. Für Einzelhandelsprodukte korreliert die Benutzer Akzeptanz häufig direkt mit dem wiederholten Kauf oder der Treue, was bedeutet, dass der Benutzer das Produkt wahrscheinlich für andere empfehlen wird. Bei internen Anwendungen korreliert die Benutzer Akzeptanz der Bereitschaft, die Software zu verwenden, um die Aufgaben auszuführen, für die Sie entworfen wurde, wodurch die Produktivität gesteigert werden kann. Das Erhöhen der Nutzbarkeit ist einer der Faktoren, die zu einer verbesserten Benutzer Akzeptanz beitragen können.

Die Nutzbarkeit kann Ihnen helfen, ihre Produkte von denjenigen ihrer Mitbewerber zu unterscheiden. Wenn zwei Produkte im-Hilfsprogramm im Wesentlichen gleich sind, wird das Produkt mit besserer Benutzerfreundlichkeit wahrscheinlich als überlegen angesehen. Außerdem haben die Windows-Richtlinien für Aussehen und Verhalten und begleitende Programmierung das Spiel Feld für die grundlegende Benutzeroberfläche festgestellt, sodass viele Programme, die ähnliche Funktionen bedienen, etwas ähnliches Aussehen und agieren. Diese Ähnlichkeiten bedeuten, dass kleine Unterschiede bei der Nutzbarkeit eine große Auswirkung auf die Benutzereinstellung haben können.

Schließlich wird jedes Produkt auf die Verwendbarkeit getestet. Benutzer führen jedes Mal, wenn Sie Sie verwenden, Nutz barkeits Tests für das Produkt aus, und Sie geben ihr Ergebnis durch die fortgesetzte Verwendung oder das Fehlen aus. Das Testen des Produkts vor der Freigabe auf dem Markt kann dazu beitragen, dass die Benutzererfahrung mit dem Produkt positiv ist.

### <a name="what-does-it-cost"></a>Was kostet dies?

Software Entwickler und Projektmanager sind häufig besorgt, dass die Initiierung eines benutzerorientierten Entwurfsprozesses und die Durchführung ordnungsgemäßer benutzerbarkeits Tests unzulässige Zeit und Geld erfordern. Die Realität ist, dass die Kosten in Zeit und Geld, die sich auf den Benutzer konzentrieren, häufig relativ klein sind, und sicherlich auch im Vergleich zu den Kosten, die nicht durchgeführt werden müssen.

Berücksichtigen Sie z. b. die Kosten in Zeit und Geld, um Entwurfs Revisionen zu spät im Entwicklungszeitraum zu erstellen, und zwar im Gegensatz zu früheren Versionen, wenn sich das Produkt noch auf der Zeichnungs Platine befindet. Wenn Sie warten, bis der Beta Zeitraum die Benutzer für das Produkt verfügbar macht, um die Benutzerfreundlichkeit zu testen, kann dies dazu führen, dass Teile des Programms, die viel Zeit für die Entwicklung benötigte, nicht mehr benötigt werden. Und warten Sie, bis das Produkt tatsächlich freigegeben ist, und nehmen Sie dann Änderungen auf der Grundlage von negativem Feedback oder der Unterstützung eines schlechten Entwurfs vor

Eine sinnvolle Nutzbarkeits Studie kann in der Regel in etwa zwei Wochen ausgeführt werden und die Zeit und die Kosten für Änderungen im Entwicklungs Durchlauf erheblich verkürzen. Die Kosten für die Durchführung von Tests variieren in Abhängigkeit von der Art des Produkts und den Teilen der Schnittstelle, die getestet werden.

Stellen Sie sich das Testen der Benutzerfreundlichkeit als vergleichbar mit Code Tests vor. Erfolgreiches Projekt-Manager-Konto für Code Tests beim Planen eines Entwicklungsprojekts. Sie sehen Sie nicht als etwas zusätzliches, das auf den Projektplan und das Budget hin zu tackiert werden muss. Stattdessen akzeptieren Projektmanager Code Tests als Kosten für Geschäftsabläufe, da die Alternative so viel teurer ist. Das gleiche gilt für benutzerbarkeits Tests.

### <a name="how-do-i-increase-usability"></a>Wie kann ich die Nutzbarkeit erhöhen?

Wenn Sie die Wichtigkeit der Nutzbarkeit kennen und verstehen, sind Softwareentwickler manchmal dazu verleitet, Nutzbarkeit hinzuzufügen, als wäre es ein Bestandteil, der einfach einem Produkt hinzugefügt werden kann, um ihn verwendbar zu machen. Stattdessen sollte die Verwendbarkeit Teil des Entwurfsprozesses selbst sein, statt eines "Thing", das dem Prozess hier oder dort hinzugefügt wird. Der Grund für die Benutzerfreundlichkeit der Benutzerfreundlichkeit liegt darin, dass die Benutzerfreundlichkeit auf "Benutzer Fokus" und "benutzerzentrierter Entwurf" verweist. Der Benutzer zentrierte Entwurf umfasst mehr als nur das befolgen eines Satzes von Regeln, die die Schaltfläche und die Menü Platzierung in einer Schnittstelle steuern. Das Testen der Benutzerfreundlichkeit bietet die Möglichkeit, die Entwurfsarbeit zu überprüfen. Es ist keine Möglichkeit, einem Produkt "Benutzerfreundlichkeit" hinzuzufügen.

Gould, Boies und Lewis (1991) identifizieren vier wichtige Grundsätze des Benutzer zentrierten Entwurfs:

-   Der frühe Fokus auf Benutzer.

    Entwickler sollten sich darauf konzentrieren, die Anforderungen der Benutzer frühzeitig im Entwurfsprozess zu verstehen.

-   Integrierter Entwurf.

    Alle Aspekte des Entwurfs sollten parallel und nicht nacheinander weiterentwickelt werden. Sorgen Sie dafür, dass der interne Entwurf des Produkts den Anforderungen der Benutzeroberfläche entspricht.

-   Frühe und fortlaufende Tests.

    Der einzige derzeit realisierbare Ansatz für den Software Entwurf ist ein empirischer Ansatz: der Entwurf funktioniert, wenn echte Benutzer entscheiden, ob er funktioniert. Das Integrieren von Nutzbarkeits Tests im gesamten Entwicklungsprozess bietet Benutzern die Möglichkeit, Feedback zum Entwurf zu liefern, bevor das Produkt veröffentlicht wird.

-   Iterativer Entwurf.

    Große Probleme maskieren häufig kleine Probleme. Designer und Entwickler sollten den Entwurf iterativ durch Tests überprüfen.

### <a name="why-should-i-involve-users"></a>Warum sollte ich Benutzer einbeziehen?

Entwickler sollten erkennen, dass es sich nicht um typische Benutzer handelt. Sie verfügen über genauere Kenntnisse und Kenntnisse des Systems, das Sie entwickeln, als der durchschnittliche Benutzer jemals. Aspekte der Schnittstelle, die für die meisten Benutzer unklar oder verwirrend sind, sind daher für jemanden, der an dem Projekt gearbeitet hat, völlig klar. Einige Softwareentwickler sind in der Lage, mit dem durchschnittlichen Benutzer zu einem gewissen Grad zu arbeiten, aber es gibt keinen Ersatz für die tatsächlichen Interaktionen der tatsächlichen Benutzer mit dem Produkt.

Dementsprechend werden durch benutzerorientierte Softwareentwickler häufig bessere Entwürfe und somit bessere Produkte erzielt, wenn Sie sich frühzeitig auf die Anforderungen typischer Benutzer konzentrieren und den Entwurf auf der Grundlage von Benutzer Tests überarbeiten.

Ein besseres Design ergibt eine bessere Akzeptanz durch Benutzer. Der Vorteil der Einzelhandels Software ist offensichtlich: mehr Umsätze. Die Akzeptanz ist auch bei der für die interne Verwendung entwickelten Software wichtig: ein erhöhter Fokus auf den Benutzer zentrierten Entwurf führt zu einer höheren Produktivität und einem verringerten Bedarf an Support. Die sichtbare Einbindung von Benutzern ab dem Anfang der Entwicklung demonstriert auch ein Interesse an ihren Anliegen und Anforderungen, was die Bereitschaft der Entwicklungsarbeit erhöht.

### <a name="cant-i-just-follow-guidelines"></a>Kann ich nicht einfach die Richtlinien befolgen?

Microsoft hat einen Satz von Schnittstellen Richtlinien für die Windows Computing-Plattform entwickelt, um sicherzustellen, dass Windows-Programme ein konsistentes Erscheinungsbild haben. Andere Unternehmen haben ähnliche Richtlinien für andere Computerplattformen entwickelt, und Nutz Fachexperten wie Jakob Nielsen haben ausführlich auf das Entwerfen verwendbarer Webseiten geschrieben. Dank der Fülle an Informationen, die in diesen Themen verfügbar sind, ist es für Designer manchmal sehr üblich, dass Sie sich an Richtlinien und Standards halten, sodass Sie nutzbare Produkte entwickeln können.

Das Problem bei diesem Ansatz ist, dass Richtlinien grundsätzlich allgemein sind. Richtlinien müssen auf eine Vielzahl von Fällen angewendet werden und sollten daher nicht immer die beste Vorgehensweise für die jeweilige entwickelte Anwendung vorschreiben. Die Einhaltung eines gut geschriebenen Satzes von Richtlinien kann beim Entwerfen einer konsistenten Schnittstelle hilfreich sein, aber Sie können nicht gewährleisten, dass Sie Ihre Anwendung ist, es sei denn, Sie wird mit echten Benutzern getestet. Wenn Sie Richtlinien verwenden, sollten Sie Sie nicht wie ein Cookbook verwenden, bei dem Richtlinien auf das Beste aus allen Ergebnissen hinweisen. Zwei Entwickler können dieselbe Richtlinie auf zwei verschiedene Arten implementieren, und beide Implementierungen sind möglicherweise nicht gleichermaßen für die Situation geeignet. Gelegentlich kann eine strikte Einhaltung von Richtlinien zu schlechten Ergebnissen oder zu Konflikten zwischen Richtlinien führen. Nur Benutzer zentrierte Entwürfe können dabei helfen, diese Probleme zu leeren, bevor Sie zu Problemen werden.

Eine andere Möglichkeit, dies zu überdenken, besteht darin, den Benutzer zentrierten Entwurf als Arbiter von Entwurfsentscheidungen und nicht als Richtlinien für die Benutzeroberfläche zu betrachten.

### <a name="do-i-need-to-build-a-usability-lab"></a>Muss ich ein Nutz barkeits Labor erstellen?

Gehen Sie nicht davon aus, dass die Benutzerfreundlichkeit für die Benutzerfreundlichkeit einen Commit für ein kostspieliger Lab durchführt. Um sicher zu sein, ist es für Unternehmen, die viele Tests durchführen, sehr praktisch, dedizierte Labs zu erstellen, und Benutzerfreundlichkeit für die Benutzerfreundlichkeit verfügen häufig über eine große Bandbreite an Einrichtungen und Ausrüstung, um Ihre Clients anzubieten Es können jedoch nützliche Nutzbarkeits Tests in einer Vielzahl von Einstellungen und Umständen ausgeführt werden.

Ein Ansatz besteht darin, einfach einen Tester zu haben? jemand, der sich mit der Durchführung von Menschen Teilnehmer Studien und dem Sammeln von Daten vertraut gemacht hat. Dies kann problemlos in einem Konferenzraum oder in einem Büro durchgeführt werden. Weitere Informationen zu Testzwecken finden Sie im Abschnitt "Dumas und Redish" in [anderen Ressourcen](other-resources.md).

Wenn Nutzbarkeits Tests entwickelt werden und mehr beteiligt sind, können Geräte wie z. b. eine Videokamera, eine unidirektionale Spiegelung oder Tools, mit denen Sie den Monitor eines Benutzers in Echtzeit anzeigen und aufzeichnen können, hinzugefügt werden.

Alternativ können Tests auch an benutzerbarkeits Berater ausgelagert werden. Der folgende Abschnitt enthält Tipps zum finden der richtigen Berater.

### <a name="how-do-i-get-started"></a>Wie gehe ich vor?

Nachdem die Entscheidung getroffen wurde, Benutzer zentrierte Entwurfs Prinzipien in den Entwicklungsprozess einzubinden, müssen Sie entscheiden, ob Sie Nutz barkeits Experten einstellen oder die Nutzbarkeits Tests an einen Hersteller auslagern möchten.

Die Benutzerfreundlichkeit der Nutzbarkeit (Professionals Professionals Association, UPA) verfügt über einen Hersteller Leit Faden, der Ihnen helfen kann,

Einige Beratungsgruppen können auch beim Einrichten von Nutzbarkeits Labs helfen oder ein internes Nutz barkeits Programm entwickeln, um Verwendbarkeits Prinzipien in den Entwurfsprozess einzubeziehen.

Wenn Sie Nutz barkeits Experten einstellen, verfügt die menschliche Faktoren und die Ergonomie-Gesellschaft über einen Platzierungs Dienst, mit dem Sie potenzielle Mitarbeiter finden können. Viele Nutz Fachexperten gehören auch zur ACM Special Interest Group bei Computer-Human Interaktion (SIGCHI) und UPA. Platzieren Sie Arbeits anzeigen in ihren Veröffentlichungen oder auf ihren Konferenzen.

Unabhängig davon, welche Route verwendet wird, denken Sie daran, dass es sich um Testdienste Das Prinzip, dass Designer keine typischen Benutzer sind, gilt auch für Nutz Fachanwender.

Weitere Informationen zu diesen Unternehmen und Organisationen sowie weitere Informationen zum Testen der Benutzerfreundlichkeit und zum Benutzer zentrierten Entwurf finden Sie unter [andere Ressourcen](other-resources.md).

 

 




