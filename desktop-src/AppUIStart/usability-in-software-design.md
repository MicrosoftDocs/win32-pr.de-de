---
title: Nutzbarkeit im Softwareentwurf
description: In diesem Thema wird das Konzept der Benutzerfreundlichkeit und derEntspricht, warum es ein wichtiger Bestandteil jedes Softwareentwurfsprojekts sein sollte.
ms.assetid: 912b3224-e36d-44d6-98fa-a7f28e68a2d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482fd749a797c58656d987e1bde9e995ac58b8fdf98a6c056cd327e846665749
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589130"
---
# <a name="usability-in-software-design"></a>Nutzbarkeit im Softwareentwurf

In diesem Thema wird das Konzept der Benutzerfreundlichkeit und derEntspricht, warum es ein wichtiger Bestandteil jedes Softwareentwurfsprojekts sein sollte.

-   [Introduction (Einführung)](#introduction)
-   [Definieren der Benutzerfreundlichkeit](#defining-usability)
    -   [Benutzerfreundlichkeit](#ease-of-use)
    -   [Nutzbarkeit im Vergleich zum Hilfsprogramm](#usability-vs-utility)
    -   [Vergleich von "Liking It" und "Using It"](#liking-it-vs-using-it)
    -   [Ermittlung im Vergleich zu Learning im Vergleich zur Effizienz](#discovery-vs-learning-vs-efficiency)
    -   [Keine Arbeit](#slogans-do-not-work)
-   [Warum ist die Benutzerfreundlichkeit wichtig?](#why-is-usability-important)
    -   [Warum sollten Sie sich darum kümmern?](#why-should-you-care)
    -   [Was kostet es?](#what-does-it-cost)
    -   [Wie kann ich die Benutzerfreundlichkeit erhöhen?](#how-do-i-increase-usability)
    -   [Warum sollte ich Benutzer einbeziehen?](#why-should-i-involve-users)
    -   [Kann ich die Richtlinien nicht einfach befolgen?](#cant-i-just-follow-guidelines)
    -   [Muss ich ein Usability Lab erstellen?](#do-i-need-to-build-a-usability-lab)
    -   [Wie kann ich Erste Schritte?](#how-do-i-get-started)

## <a name="introduction"></a>Einführung

Der Begriff "Benutzerfreundlichkeit" im Kontext des Erstellens von Software stellt einen Ansatz dar, bei dem der Benutzer anstelle des Systems in den Mittelpunkt des Prozesses stellt. Diese als benutzerzentriertes Design bezeichnete Philosophie umfasst Benutzerbedenken und -unterstützung vom Anfang des Entwurfsprozesses und schreibt vor, dass die Anforderungen des Benutzers die wichtigste aller Entwurfsentscheidungen sein sollten.

Der sichtbarste Aspekt dieses Ansatzes sind Benutzerfreundlichkeitstests, bei denen Benutzer mit der Produktschnittstelle arbeiten und mit ihnen interagieren und ihre Ansichten und Bedenken mit den Designern und Entwicklern teilen.

## <a name="defining-usability"></a>Definieren der Benutzerfreundlichkeit

Im Abschnitt wird definiert, was Benutzerfreundlichkeit im Kontext der Softwareentwicklung bedeutet und wie sie mit anderen Aspekten des Entwicklungsprozesses in Zusammenhang steht.

### <a name="ease-of-use"></a>Benutzerfreundlichkeit

Die Benutzerfreundlichkeit ist ein Maß, wie einfach es ist, ein Produkt zum Ausführen vorgeschriebener Aufgaben zu verwenden. Dies ist ein Unterschied zu den verwandten Konzepten von Nützlichkeit und Gleichbarkeit.

### <a name="usability-vs-utility"></a>Nutzbarkeit im Vergleich zum Hilfsprogramm

Ein zentrales Attribut, das die Qualität eines Produkts bestimmt, ist nützlich. Dies misst, ob die tatsächlichen Verwendungen eines Produkts die Ziele erreichen können, die die Designer erreichen möchten. Das Konzept der Nützlichkeit ist ein weiterer Teil des Nutzens und der Nutzbarkeit. Obwohl diese Begriffe verknüpft sind, sind sie nicht austauschbar.

Hilfsprogramm bezieht sich auf die Fähigkeit des Produkts, eine Aufgabe oder Aufgaben auszuführen. Wenn das Produkt mehr Aufgaben ausführen soll, desto nützlicher ist es.

Betrachten Sie typische Microsoft MS-DOS-Textprozessoren aus den ende 1980er Jahren. Solche Programme stellten viele leistungsstarke Textbearbeitungs- und Bearbeitungsfeatures zur Verfügung, erforderten jedoch, dass Benutzer Dutzende von arkanen Tastatureingaben lernen und sich merken mussten, um sie durchzuführen. Anwendungen wie diese verfügen über ein hohes Hilfsprogramm (sie bieten Benutzern die erforderliche Funktionalität), aber eine geringe Benutzerfreundlichkeit (die Benutzer müssen viel Zeit und Aufwand damit verbringen, sie zu lernen und zu verwenden). Im Gegensatz dazu kann eine gut entworfene, einfache Anwendung wie ein Rechner sehr einfach zu verwenden sein, aber nicht viel Nutzen bieten.

Beide Qualitäten sind für die Akzeptanz des Markts erforderlich und sind Teil des allgemeinen Nutzenkonzepts. Wenn ein Programm sehr gut verwendet werden kann, aber nichts von Nutzen ist, wird es natürlich von niemandem verwendet. Und Benutzer, denen ein leistungsstarkes Programm präsentiert wird, das schwer zu verwenden ist, werden sich wahrscheinlich dagegen sträubt oder Alternativen suchen.

Benutzerfreundlichkeitstests helfen Ihnen zu bestimmen, wie einfach es benutzern ist, bestimmte Aufgaben auszuführen. Sie können jedoch nicht direkt feststellen, ob das Produkt selbst einen Wert oder einen Nutzen hat. (Benutzer können während der Benutzerfreundlichkeitstests kommentare im Zusammenhang mit dem Hilfsprogramm abgeben, aber alle Kommentare sollten mit anderen, stabileren Forschungsmethoden überprüft werden.)

### <a name="liking-it-vs-using-it"></a>Vergleich von "Liking It" und "Using It"

Die Freundlichkeit ist in einem Produkt immer ein wünschenswertes Merkmal. Wenn Menschen das Produkt mag, verwenden sie es eher und empfehlen es anderen Personen. Wie beim -Hilfsprogramm sollten Sie jedoch darauf achten, dass Sie die Benutzerfreundlichkeit nicht mit der Nutzbarkeit verwechseln.

Menschen gefällt ein Produkt häufig aus Gründen, die nicht mit dem Nutzen und der Nutzbarkeit in Zusammenhang stehen. Sie sind möglicherweise an ihrem Stil oder dem Status, den sie glauben, dass das Produkt ihnen überträgt, ungniert. Menschen möchten in der Regel hochverfetzbare Produkte, aber Sie sollten nicht davon ausgehen, dass ein gut gefälltes Produkt verwendet werden kann.

Bei der Nutzbarkeit geht es darum, ob eine Person das Produkt verwenden kann, um die Aufgaben auszuführen, die sie ausführen muss. Benutzerfreundlichkeitstests misst in erster Linie die Leistung, nicht die Einstellung. Standardisierte Fragekataloge können jedoch verwendet werden, um Präferenzen produktübergreifend zu messen.

### <a name="discovery-vs-learning-vs-efficiency"></a>Ermittlung im Vergleich zu Learning im Vergleich zur Effizienz

Es gibt viele Aspekte der Benutzerfreundlichkeit, aber normalerweise bezieht sich der Begriff speziell auf die Attribute der Ermittlung, des Lernens und der Effizienz.

-   Bei der Ermittlung wird das Feature eines Produkts als Reaktion auf eine bestimmte Notwendigkeit gesucht und gesucht. Benutzerfreundlichkeitstests können bestimmen, wie lange es dauert, bis ein Benutzer ein Feature findet, und wie viele Fehler (falsche Standortauswahl) der Benutzer dabei macht.
-   Learning bezieht sich auf den Prozess, mit dem der Benutzer versteht, wie ein gefundenes Feature zum Abschließen einer Aufgabe verwendet wird. Benutzerfreundlichkeitstests können bestimmen, wie lange dieser Prozess dauert und wie viele Fehler der Benutzer beim Erlernen des Features macht.
-   Effizienz bezieht sich auf den Punkt, an dem der Benutzer das Feature "gemastert" hat und es ohne weiteres Lernen verwendet. Benutzerfreundlichkeitstests können bestimmen, wie lange es dauert, bis der erfahrene Benutzer die erforderlichen Schritte zur Verwendung des Features ausgeführt hat.

Diese drei grundlegenden Aspekte der Benutzerfreundlichkeit werden stark von der Art der aufgabe und der Häufigkeit beeinflusst, mit der der Benutzer sie ausführt. Einige Features werden so selten oder so komplex verwendet, dass der Benutzer sie jedes Mal erneut verleert. Für diese Features entwickelt Microsoft häufig Assistenten, um den Benutzer durch den Prozess zu führen.

### <a name="slogans-do-not-work"></a>Keine Arbeit

Softwareentwickler denken manchmal, dass einfache Schwierigkeiten wie "Das Produkt nutzbarer machen" bei der Lösung von Problemen mit der Benutzerfreundlichkeit helfen. Eine positive Einstellung zur Benutzerfreundlichkeit ist zwar wichtig, aber nur ordnungsgemäße Benutzerfreundlichkeitstests mit normalen Benutzern im Kontext des spezifischen Produkts, das erstellt wird, können Entwicklern die Informationen bereitstellen, die sie benötigen, um ein Produkt zu erstellen, das die Anforderungen der Benutzer erfüllt. "Make the product more usable" (Das Produkt nutzbarer machen) sollte das Ziel jedes Softwareentwicklers sein, aber es ist nur sinnvoll, wenn der Entwickler weiß, was Benutzerfreundlichkeit bedeutet. Tests mit normalen Benutzern sind die zuverlässigste Möglichkeit, dies herauszufinden.

## <a name="why-is-usability-important"></a>Warum ist die Benutzerfreundlichkeit wichtig?

Im Abschnitt werden einige häufig gestellte Fragen beantwortet, warum Benutzerfreundlichkeit wichtig ist und wie benutzerzentrierte Entwurfsprinzipien in den Entwicklungsprozess integriert werden.

### <a name="why-should-you-care"></a>Warum sollten Sie sich darum kümmern?

Wenn benutzerfreundlichkeitsaspekte noch nicht in den Produktentwurfsprozess integriert wurden, fragen Sie sich vielleicht, warum dies notwendig oder wünschenswert ist. Schließlich ist es sicherlich möglich, ein funktionierendes, fehlerfreies Produkt frei zu geben, ohne benutzerfreundlichkeitsbasierte Aufgaben ausführen zu müssen. Die Integration benutzerzentrierter Entwurfsprinzipien kann jedoch in mehreren Bereichen zu einem deutlich verbesserten Produkt führen.

Der beste Grund für Benutzerfreundlichkeitstests ist die Reduzierung der Anzahl von Supportanrufen von Benutzern. Eine schlechte Benutzerfreundlichkeit ist ein hauptgrund dafür, dass Benutzer softwaretechnische Supportzeilen aufrufen und jeder Softwareunternehmensleiter und Information Services-Manager weiß, wie teuer der Produktsupport sein kann. Darüber hinaus erhöht sich die potenzielle Unzufriedenheit der Benutzer mit dem Produkt. Wenn Es für Benutzer einfach ist, Ihr Produkt zu verwenden, müssen sie nicht so oft technischen Support anrufen.

Für Software, die für die interne Verwendung erstellt wird, besteht der nächste beste Grund, die Benutzerfreundlichkeit zu einem wichtigen Bestandteil des Entwicklungsprozesses zu machen, in der Reduzierung der Trainingskosten. Ein hochgradig verwendbares Produkt ist für Benutzer viel einfacher zu erlernen als ein Produkt, bei dem die Benutzerfreundlichkeit keine hohe Priorität hatte. Benutzer lernen Features schneller und behalten ihr Wissen länger bei, was direkt mit verringerten Trainingskosten und -zeit korreliert.

Benutzerfreundlichkeitstests helfen dabei, die Benutzerakzeptanz zu verbessern. Die Akzeptanz ergibt sich aus einer Reihe von Faktoren, z. B. Benutzerfreundlichkeit, Nützlichkeit und Anpassungsfähigkeit. Bei Einzelhandelsprodukten korreliert die Benutzerakzeptanz häufig direkt mit dem wiederholten Kauf oder der Bindung, was bedeutet, dass der Benutzer das Produkt wahrscheinlich anderen empfehlen wird. Bei internen Anwendungen korreliert die Benutzerakzeptanz mit der Bereitschaft, die Software für die Aufgaben zu verwenden, für die sie entworfen wurde, wodurch die Produktivität gesteigert wird. Die Verbesserung der Benutzerfreundlichkeit ist einer der Faktoren, die zu einer höheren Benutzerakzeptanz beitragen können.

Die Benutzerfreundlichkeit kann dabei helfen, Ihre Produkte von denen Ihrer Mitbewerber zu unterscheiden. Wenn zwei Produkte im Wesentlichen gleich sind, wird das Produkt mit besserer Benutzerfreundlichkeit wahrscheinlich als überlegen betrachtet. Darüber hinaus haben die Windows-Look-and-Feel und die zugehörigen Programmierrichtlinien die Spielregeln für die grundlegende Benutzeroberfläche ge gleicht, sodass viele Programme, die ähnliche Funktionen bedienen, ähnlich aussehen und agieren. Diese Ähnlichkeiten bedeuten, dass kleine Unterschiede bei der Benutzerfreundlichkeit einen großen Einfluss auf die Benutzereinstellung haben können.

Schließlich wird jedes Produkt schließlich auf Benutzerfreundlichkeit getestet. Benutzer führen jedes Mal Benutzerfreundlichkeitstests für das Produkt durch, wenn sie es verwenden, und sie rendern ihr Diktat durch ihre weitere Verwendung oder deren Fehlen. Wenn Sie das Produkt testen, bevor es auf den Markt gebracht wird, können Sie sicherstellen, dass die Erfahrungen der Benutzer mit dem Produkt positiv sind.

### <a name="what-does-it-cost"></a>Was kostet es?

Softwareentwickler und Projektleiter machen sich häufig Sorgen, dass das Initiieren eines benutzerzentrierten Entwurfsprozesses und das Durchführen von geeigneten Benutzerfreundlichkeitstests nicht akzeptable Zeit und Geld erfordern. Die Realität ist, dass die Zeit- und Geldkosten, die sich auf den Benutzer konzentrieren, häufig relativ gering sind und dies im Vergleich zu den Kosten, die dafür nicht zu tun sind.

Berücksichtigen Sie beispielsweise die Zeit- und Geldkosten für die Erstellung von Entwurfsrevisionen zu einem späteren Zeitpunkt im Entwicklungszyklus als früher, wenn sich das Produkt noch auf dem Zeichenbrett befindet. Wenn Sie bis zur Betaphase warten, um Benutzer für Benutzerfreundlichkeitstests für das Produkt verfügbar zu machen, kann dies dazu führen, dass Teile des Programms sehr lange entwickelt wurden. Und wenn Sie warten, bis das Produkt tatsächlich freigegeben wird, und dann Änderungen basierend auf negativem Feedback oder unterstützung eines schlechten Designs vornehmen, können die Kosten aufgrund hoher Produktsupportkosten oder schlechter Aufnahme durch Benutzer unermesslich höher sein.

Eine sinnvolle Benutzerfreundlichkeitsstudie kann in der Regel in etwa zwei Wochen oder weniger durchgeführt werden und kann die Zeit und Kosten für Änderungen zu einem späteren Zeitpunkt im Entwicklungszyklus erheblich reduzieren. Die Kosten für die Durchführung von Tests variieren je nach Art des Produkts und den Teilen der getesteten Schnittstelle.

Stellen Sie sich das Testen der Benutzerfreundlichkeit so vor, als würden Sie es mit Codetests vergleichbar machen. Erfolgreiche Projektmanager berücksichtigen Codetests bei der Planung eines Entwicklungsprojekts. Sie sehen es nicht als etwas Zusätzliches, das dem Projektzeitplan und -budget entspricht. Stattdessen akzeptieren Projektmanager Codetests als Kosten für die Geschäftstätigkeit, da die Alternative so viel teurer ist. Dasselbe gilt für Benutzerfreundlichkeitstests.

### <a name="how-do-i-increase-usability"></a>Wie kann ich die Benutzerfreundlichkeit erhöhen?

Nach dem Lesen und Verstehen der Bedeutung der Benutzerfreundlichkeit sind Softwareentwickler manchmal verlockend, benutzerfreundlicher zu sein, als ob es sich um eine Freundlichkeit handelte, die einfach zu einem Produkt hinzugefügt werden kann, um es besser nutzbar zu machen. Stattdessen sollte benutzerfreundlichkeit Teil des Entwurfsprozesses selbst sein, anstatt ein "Ding", das dem Prozess hier oder dort hinzugefügt wird. Der Grund dafür, dass Benutzerfreundlichkeitsexperten auf "Benutzerfokus" und "benutzerzentriertes Design" verweisen, ist, dass die Benutzerfreundlichkeit davon abhängt, dass die Anforderungen der Benutzer für den Entwurfsprozess zentral bleiben. Benutzerzentriertes Design umfasst notwendigerweise mehr als nur das Befolgen einer Reihe von Regeln, die die Platzierung von Schaltflächen und Menüs in einer Schnittstelle steuern. Benutzerfreundlichkeitstests sind eine Möglichkeit, die Entwurfsarbeit zu überprüfen. Es ist keine Möglichkeit, die Benutzerfreundlichkeit eines Produkts zu "erweitern".

Die folgenden vier wichtigen Grundsätze des benutzerzentrierten Designs werden von Denkerld, Boies und Einem (1991) identifiziert:

-   Frühzeitiger Fokus auf Benutzer.

    Entwickler sollten sich darauf konzentrieren, die Anforderungen der Benutzer frühzeitig im Entwurfsprozess zu verstehen.

-   Integrierter Entwurf.

    Alle Aspekte des Entwurfs sollten parallel und nicht nacheinander weiterentwickelt werden. Halten Sie den internen Entwurf des Produkts mit den Anforderungen der Benutzeroberfläche konsistent.

-   Frühe und kontinuierliche Tests.

    Der derzeit einzige mögliche Ansatz für den Softwareentwurf ist ein empirischer Ansatz: Der Entwurf funktioniert, wenn echte Benutzer entscheiden, dass er funktioniert. Die Integration von Benutzerfreundlichkeitstests im gesamten Entwicklungsprozess gibt Benutzern die Möglichkeit, Feedback zum Entwurf zu übermitteln, bevor das Produkt veröffentlicht wird.

-   Iteratives Design.

    Große Probleme maskieren häufig kleine Probleme. Designer und Entwickler sollten den Entwurf iterativ durch Testläufe überarbeiten.

### <a name="why-should-i-involve-users"></a>Warum sollte ich Benutzer einbeziehen?

Entwickler sollten erkennen, dass sie keine typischen Benutzer sind. Sie verfügen über ein tieferes Wissen und Verständnis des Systems, das sie entwickeln, als der durchschnittliche Benutzer jemals. Aspekte der Schnittstelle, die für die meisten Benutzer unklar oder verwirrend sind, können daher für jemanden, der am Projekt gearbeitet hat, eindeutig sein. Einige Softwareentwickler sind in der Lage, sich bis zu einem gewissen Grad mit dem durchschnittlichen Benutzer zu beschäftigen, aber es gibt keinen Ersatz für die tatsächlichen Interaktionen der tatsächlichen Benutzer mit dem Produkt.

Entsprechend erzeugen benutzerorientierte Softwareentwickler bessere Entwürfe und somit bessere Produkte, indem sie sich frühzeitig auf die typischen Benutzeranforderungen konzentrieren und den Entwurf basierend auf Benutzertests häufig überarbeiten.

Durch einen besseren Entwurf wird die Akzeptanz der Benutzer verbessert. Der Vorteil von Einzelhandelssoftware ist offensichtlich: Umsatzsteigerung. Die Akzeptanz ist auch bei Software wichtig, die für die interne Verwendung entwickelt wurde: Ein erhöhter Fokus auf benutzerzentriertes Design führt zu einer höheren Produktivität und einem verringerten Supportbedarf. Die sichtbare Einbeziehung von Benutzern von Beginn der Entwicklung an zeigt auch ein Interesse an ihren Belangen und Bedürfnissen, was ihre Bereitschaft erhöht, bei den Entwicklungsbemühungen zu helfen.

### <a name="cant-i-just-follow-guidelines"></a>Kann ich die Richtlinien nicht einfach befolgen?

Microsoft hat eine Reihe von Schnittstellenrichtlinien für die Windows Computingplattform entwickelt, um sicherzustellen, dass Windows Programme ein einheitliches Aussehen und Gefühl aufweisen. Andere Unternehmen haben ähnliche Richtlinien für andere Computingplattformen entwickelt, und Benutzerfreundlichkeitsexperten wie Wies Nielsen haben ausführlich über das Entwerfen verwendbarer Webseiten geschrieben. Mit der Vielzahl von Informationen zu diesen Themen sind Designer manchmal der Meinung, dass die strikte Einhaltung von Richtlinien und Standards alles ist, was erforderlich ist, um verwendbare Produkte zu erzeugen.

Das Problem bei diesem Ansatz besteht darin, dass Richtlinien grundsätzlich allgemein sind. Richtlinien müssen für eine Vielzahl von Fällen gelten und daher nicht immer die beste Vorgehensweise für die bestimmte Anwendung vorgeben, die entwickelt wird. Die Einhaltung eines gut geschriebenen Satzes von Richtlinien kann beim Entwurf einer konsistenten Schnittstelle hilfreich sein, aber sie können die Usablilität nur garantieren, wenn sie mit echten Benutzern getestet wurde. Wenn Sie Richtlinien verwenden, verwenden Sie sie nicht wie ein Cookbook, in dem Richtlinien den Weg zum Besten aller Ergebnisse weisen. Zwei Entwickler können die gleiche Richtlinie auf zwei verschiedene Arten implementieren, und beide Implementierungen sind für die Situation möglicherweise nicht gleichermaßen geeignet. Gelegentlich kann die strikte Einhaltung von Richtlinien zu schlechten Ergebnissen oder zu Konflikten zwischen Richtlinien führen. Nur ein benutzerzentrierter Entwurf kann dabei helfen, diese Probleme zu leeren, bevor sie zu Problemen werden.

Eine andere Möglichkeit, dies zu berücksichtigen, ist: Lassen Sie den benutzerzentrierten Entwurf die Entscheidungsberechtigung für Entwurfsentscheidungen, nicht die Richtlinien für die Benutzeroberfläche.

### <a name="do-i-need-to-build-a-usability-lab"></a>Muss ich ein Benutzerfreundlichkeitslab erstellen?

Gehen Sie nicht davon aus, dass Benutzerfreundlichkeitstests die Verpflichtung zu einem teuren Lab mit Kameras mit Deckenbelegung, Einwegspiegeln und anderen Fokusgruppenaufnahmen bedeuten. Allerdings ist es für Unternehmen, die viele Tests durchführen, häufig praktisch, dedizierte Labs zu erstellen, und Benutzerfreundlichkeitsberater verfügen häufig über eine Vielzahl von Einrichtungen und Geräten, die ihren Kunden zur Verfügung stehen. Aber nützliche, gültige Benutzerfreundlichkeitstests können in einer Vielzahl von Einstellungen und Umständen durchgeführt werden.

Ein Ansatz besteht darin, einfach einen Tester zu haben? Jemand, der mit dem Durchführen menschlicher Teilnehmerstudien und dem Sammeln von Daten vertraut ist? befindet sich hinter einem Benutzer, während er arbeitet, und beobachtet den Benutzer, der Aufgaben ausführt. Dies kann problemlos in einem Konferenzraum oder büro erfolgen. Weitere Informationen zum Testen durch Beobachtung finden Sie im Eintrag Dumas und Redish unter [Andere Ressourcen.](other-resources.md)

Wenn Benutzerfreundlichkeitstests entwickelt werden und immer komplexer werden, können Geräte wie eine Videokamera, ein eindirektionler Spiegel oder Tools hinzugefügt werden, mit denen Sie den Monitor eines Benutzers in Echtzeit anzeigen und aufzeichnen können.

Alternativ können Tests an Benutzerfreundlichkeitsberater ausgelagert werden. Der folgende Abschnitt enthält Tipps zum Suchen der richtigen Berater.

### <a name="how-do-i-get-started"></a>Wie Erste Schritte ich?

Nachdem Sie sich entschieden haben, benutzerzentrierte Entwurfsprinzipien in den Entwicklungsprozess zu integrieren, müssen Sie entscheiden, ob Sie Benutzerfreundlichkeitsexperten einstellen oder die Benutzerfreundlichkeitstests an einen Anbieter auslagern möchten.

Die Usability Professionals Association (UPA) verfügt über einen Anbieterleitfaden, der Ihnen bei der Suche nach Nutzbarkeitsberatern helfen kann.

Einige Beratungsgruppen können auch dabei helfen, Benutzerfreundlichkeitslabs einzurichten oder ein eigenes Benutzerfreundlichkeitsprogramm zu entwickeln, um Benutzerfreundlichkeitsprinzipien in den Entwurfsprozess zu integrieren.

Wenn Sie Benutzerfreundlichkeitsexperten einstellen, verfügt die Human Factors and Placements Society über einen Platzierungsdienst, der bei der Suche nach potenziellen Mitarbeitern helfen kann. Viele Benutzerfreundlichkeitsexperten gehören auch zu ACM Special Interest Group on Computer-Human Interaction (SIGCHI) und UPA. Stellen Sie Inserate für die Arbeit in ihren Veröffentlichungen oder auf ihren Konferenzen ein.

Denken Sie daran, dass es sich dabei um Testdienste handelt, unabhängig davon, welche Route ausgeführt wird. Das Prinzip, dass Designer keine typischen Benutzer sind, gilt auch für Benutzerfreundlichkeitsexperten.

Weitere Informationen zu diesen Unternehmen und Organisationen sowie weitere Informationen zu Benutzerfreundlichkeitstests und benutzerzentriertem Design finden Sie unter [Weitere Ressourcen.](other-resources.md)

 

 




