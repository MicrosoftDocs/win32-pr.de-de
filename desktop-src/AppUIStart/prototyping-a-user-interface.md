---
title: Prototyperstellung für eine Benutzeroberfläche
description: In diesem Thema wird erläutert, wie die Prototyperstellung einer Benutzeroberfläche dazu beitragen kann, Entwurfsfehler zu minimieren und eine erfolgreiche Benutzererfahrung sicherzustellen.
ms.assetid: 16e3fabb-9cd1-4517-8f19-b1d80c956ee0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce42ad4240c3a06716f0db851e98b31e713b1ce0e23d1d485bc3e154375d9e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507435"
---
# <a name="prototyping-a-user-interface"></a>Prototyperstellung für eine Benutzeroberfläche

In diesem Thema wird erläutert, wie die Prototyperstellung einer Benutzeroberfläche dazu beitragen kann, Entwurfsfehler zu minimieren und eine erfolgreiche Benutzererfahrung sicherzustellen.

## <a name="introduction"></a>Einführung

Manchmal sammeln sich im Laufe eines Projekts kleine Annahmen und wohlgemeinte, aber schlechte Entscheidungen an, wodurch stundenweise Arbeit zu einer heiteren Benutzererfahrung wird. Die intelligenten Teams beseitigen ihre Fehler vor dem Versand mithilfe einer Technik namens UI-Prototyperstellung. In Kombination mit Benutzerfreundlichkeitsstudien halten Prototypen Teams auf dem richtigen Weg.

## <a name="why-prototype"></a>Gründe für den Prototyp

Prototyperstellung ist eine Möglichkeit, Ideen zu untersuchen, bevor Sie in sie investieren. Alle erfahrenen Mitarbeiter und Techniker erstellen Prototypen ihrer Arbeit, bevor sie etwas erstellen: Architekten erstellen Modelle aus Papier oder Mitwirkenden oder mit Virtual Reality-Tools. Techniker verwenden Windtunnel. Bridge Builders erstellen Belastungsmodelle. Software- und Webdesigner erstellen Modellmodelle, wie Benutzer mit ihren Entwürfen interagieren.

Der beste Grund für den Prototyp ist das Sparen von Zeit und Ressourcen. Der Wert eines Prototyps besteht darin, dass es sich um eine Fassade handelt – wie bei einem Gebäudesatz, in dem nur die Vorderseite des Gebäudes erstellt wird. Im Vergleich zum echten Produkt sind Prototypen einfach und kostengünstig zu erstellen. Für eine minimale Investition können also Benutzerfreundlichkeits- und Entwurfsprobleme gefunden und die Benutzeroberfläche angepasst werden, bevor erhebliche Investitionen in den endgültigen Entwurf und die Technologien getätigt werden.

Bei der Untersuchung der Anforderungen eines bestimmten Projekts finden sich möglicherweise Gründe für die Erstellung eines Prototyps, der keine Kosten spart. Soll ein neues Schnittstellenmodell untersucht werden? Nehmen Sie Änderungen an einem Teil des vorhandenen Entwurfs vor? Untersuchen einer neuen Technologie? Bevor Sie beginnen, müssen Sie sich darüber im Klaren sein, warum Sie das erstellen, was Sie erstellen. Wenn Sie mit klaren Zielen beginnen, können Sie den Aufwand direkt und effektiv gestalten. Die Gründe für die Erstellung von Prototypen lassen sich in drei grundlegende Kategorien unterteilen:

-   Proof of Concept.

    Unter einigen Teams gibt es Stimmungen über die zukünftige Richtung eines Projekts. Ein Prototyp kann verwendet werden, um nachzuweisen, dass eine Idee oder ein neuer Ansatz einen Mehrwert hat. Ein Prototyp kann dabei helfen, zu veranschaulichen, dass eine Idee funktioniert, ihre Qualitäten visuell und interaktiv ausdrücken und/oder Teammitglieder dazu bringen kann, aus einer anderen Perspektive über das Problem nachzudenken.

-   Designuntersuchung.

    Wenn Sie interaktive Software entwerfen, besteht die einzige Möglichkeit, zu untersuchen, wie etwas verwendet wird, darin, ein Modell zu erstellen und damit zu interagieren. Manchmal ist das Modell an eine Nutzbarkeitsstudie gebunden, bei der Teile des Prototyps strukturiert ausgewertet werden können. Manchmal ist es nur eine Möglichkeit, einem Entwickler klar auszudrücken, wie etwas funktionieren oder aussehen sollte. In vielen Fällen experimentiert ein Designer möglicherweise einfach, um einen Eindruck davon zu bekommen, welcher Ansatz funktionieren könnte. Jeder im Team kann Prototypen verwenden, um Entwurfsprobleme zu untersuchen, obwohl Designer im Allgemeinen am besten qualifiziert sind. Entwurfserkundungen sollten darauf ausgerichtet sein, bestimmte Probleme zu lösen, die im Produkt erkannt werden.

-   Technische Untersuchung.

    Entwickler, die Implementierungsansätze für ein Problem untersuchen, probieren häufig verschiedene Programmiertechniken aus, um festzustellen, ob sie gut funktionieren. Die Verwendung von COM+, dynamischem HTML (DHTML), Microsoft Win32 oder bestimmten Codierungsansätzen innerhalb jeder Technologie hat unterschiedliche Kompromisse. Manchmal stellt ein Prototyp eine Untersuchung dar, welche Technologie gut funktioniert, um ein bestimmtes Benutzeroberflächenfeature zu unterstützen.

Manchmal werden Prototypen aus einer Kombination dieser Gründe erstellt. Wenn ein Team ausreichend plant, kann es einem Entwickler und einem Designer oder Projektleiter Zeit für die Zusammenarbeit an einem Prototyp einplanen. In solchen Fällen ist es äußerst wichtig, die Ziele und die Beiträge, die jedes Teammitglied leisten soll, eindeutig zu definieren. Jeder sollte sich darüber im Klaren sein, was die Ziele sind, was am Ende steht und wie das potenzielle Ergebnis ausgeht.

## <a name="who-is-involved"></a>Wer Ist beteiligt?

Die Prototyperstellung kann informell von allen Personen durchgeführt werden, unabhängig von ihrem Hintergrund oder ihrer Rolle im Projekt. Es ist einfach, einen einfachen, aber effektiven Prototyp zu erstellen, indem Sie eine Bitmap von Adobe Nokia verwenden, sie in das Erstellungs- und Verwaltungstool der Microsoft FrontPage-Website einfügen und aktive Schaltflächen oder Links hinzufügen. Diese einfachen Prototypen gehen nur so weit und können für komplexe Interaktionen unhandlich werden.

Für formalere Prototypen durch größere Teams arbeitet ein Entwickler oder Projektleiter häufig mit einem Designer und einem Benutzerfreundlichkeitstechniker zusammen. Zusammen generieren sie Ideen, erstellen einen Prototyp, der die besten Ideen darstellt, und besuchen dann das Lab, um zu sehen, wie effektiv es bei der Lösung von Benutzerproblemen ist. Entwickler werden möglicherweise einbezogen, wenn sie Zeit sparen können oder wenn ihr technisches Fachwissen erforderlich ist. Häufig führt der Designer oder Der Projektmanager die meisten Skripts oder Codierungen aus, um den Prototyp zu erstellen.

## <a name="when-should-a-prototype-be-built"></a>Wann sollte ein Prototyp erstellt werden?

Abhängig vom Umfang des Prototyps und der erforderlichen Detailstufe können Prototypen jederzeit während des Projekts erstellt werden. In den meisten Fällen werden sie früh im Projekt während der Planungs- und Spezifikationsphase erstellt, bevor Entwickler Produktionscode schreiben. Dies ist der Zeitpunkt, an dem die Untersuchung am größten ist und die benötigte Zeit am sinnvollsten ist. Wenn Entwickler anstelle von Programm-Managern oder Designern Prototypen erstellen, wird die Zeitplanung noch wichtiger, da sichergestellt werden muss, dass die in den Prototyp investierte Arbeit im Entwicklungszeitplan berücksichtigt wird. Die Planung für ein beliebiges Benutzeroberflächen-Release sollte ein gewisses Maß an Prototyperstellung umfassen.

Später in einem Projekt können kleinere Prototypen dabei helfen, schwierige Entwurfs- und technische Probleme zu lösen. Eine schnelle HTML-Darstellung des Verhaltens eines Dialogfelds oder einer Webseite kann dabei helfen, die Frage eines Entwicklers zu beantworten oder anderen Teammitgliedern ein Gefühl dafür zu geben, wie die gewünschte Erfahrung aussehen sollte. In einigen Fällen kann ein starker Programm-Manager oder Designer das Verhalten in Microsoft JScript-Entwicklungssoftware implementieren und einen Großteil der Programmierlogik annähern, die Entwickler durchgehen müssen.

Die Zeit, die zum Erstellen eines Prototyps benötigt wird, kann je nach Umfang und Genauigkeit des Endergebnisses erheblich variieren. Ein informeller Prototyp kann ein paar Stunden Arbeit durch eine Person bedeuten. ein stärker organisierter Aufwand kann wochenlangen Aufwand durch ein gesamtes Team umfassen.

## <a name="where-should-the-focus-be"></a>Wo sollte der Fokus liegen?

Erstellen Sie in einem Prototyp nur so viel des Entwurfs wie erforderlich. Es ist in Ordnung, Schaltflächen zu verwenden, die nicht funktionieren, oder Text, der nie aktualisiert wird. Solange die erforderlichen Interaktionen auftreten können, ist es in Ordnung, für den Rest Feuer und Spiegel zu verwenden. Im Folgenden finden Sie einige Gründe, warum die Bemühungen sorgfältig konzentriert werden sollten:

-   Kosten für die Erstellung des Prototyps.

    Die Kosten für die Erstellung des Prototyps sollten minimiert werden. Die Herausforderung bei der Prototyperstellung besteht darin, die minimalen Investitionen zu erkennen, die erforderlich sind, um Fragen zum Entwurf effektiv zu beantworten. Hier sind Benutzerfreundlichkeitsstudien wichtig, da sie die Teile der Benutzeroberfläche eindeutig identifizieren, die die meiste Arbeit benötigen. Auch ohne Benutzerfreundlichkeitsstudien können Sie mit dem Entwurf im Prototyp klar definieren, welche Benutzerprobleme gelöst werden oder welche Aufgaben verbessert werden.

-   Begrenzte Lebensdauer.
-   Prototypen sollten eine klar definierte Lebensdauer aufweisen. Ist das Endziel eine Präsentation bei einer Teambesprechung? Eine Besprechung der Geschäftsleitung? Eine Spezifikationsüberprüfung? Eine Benutzerfreundlichkeitsstudie? Identifizieren, dass der Entwurf ein Benutzerproblem löst? Sobald die Anforderungen für diese spezifischen Ziele erfüllt sind, sollte der Prototyp außer Kraft gesetzt werden. Die grundlegende Mentalität besteht darin, dass der in einem Prototyp generierte Code oder die Bitmaps zurückbleiben. Es kann Ausnahmen geben, bei denen Code oder Visuals im Produkt weiter vorhanden sind, aber es sollte davon auszugehen sein, dass dies nicht der Fall ist.
-   Risiko, das Team zu überfordern.

    Das Anzeigen von Prototypen für Entwickler und Teamkollegen kann schwierig sein. Ein übermäßig komplexer oder aufwendiger Prototyp, der beeindruckende Visuals und Animationen erstellt, kann Menschen überfordern. Haben Sie immer ein Gefühl dafür, wie weit sie gehen müssen und wie viel des Prototyps wirklich angenommen werden sollte.

## <a name="what-is-the-scope"></a>Was ist der Bereich?

Da der Fokus für den Prototyperstellungsaufwand bestimmt wird, sollten Sie Folgendes berücksichtigen:

-   Kundenanforderungen.

    Beginnend mit einem Verständnis der wichtigsten Probleme oder Anforderungen der Benutzer (vielleicht etwas, das ein Benutzerfreundlichkeitstechniker bereitgestellt hat) bietet eine Vorstellung davon, welche Teile des Benutzeroberflächenentwurfs die meisten Untersuchungen erfordern.

-   Aufgaben zur Benutzerfreundlichkeitsuntersuchung.

    Wenn Sie den Prototyp für eine Benutzerfreundlichkeitsstudie erstellen, besprechen Sie mit dem Usability Engineer, welche spezifischen Aufgaben Teil der Studie sein werden, und entwerfen Sie diese Elemente.

-   Teameingabe.

    Sprechen Sie mit wichtigen Entwicklern im Team, während die Ideen im Prototyp zusammenkommen. Verschaffen Sie sich einen grundlegenden Eindruck davon, was sinnvoll ist, was möglich ist und was für das nächste Release außer Betracht gezogen werden kann. In einigen Fällen sollten Sie erwägen, über das hinauszugehen, was für einen Aspekt des Entwurfs möglich ist, wenn dies ein wichtiger Punkt ist und das Team aufgefordert werden muss. Tun Sie dies jedoch nicht bei jedem Aspekt Ihres Prototyps, da es eine fine line zwischen dem Überschreiten der Grenzwerte und der Überforderung Ihres Teams gibt. Wenn der Wunsch darin besteht, das Team zu inspirieren, indem es ihm eine Vision für mehrere Versionen zeigt, gehen Sie dafür. Wenn es jedoch erforderlich ist, bestimmte Änderungen für das nächste Release zu definieren, konzentrieren Sie sich auf diese Änderungen. Stellen Sie sicher, dass Sie die spezifischen Änderungen modular herausstellen und Entwicklern einen Pfad zum Erstellen der Entwürfe zeigen.

-   Breite und Tiefe.

    Bei größeren Prototypen gibt es die zusätzliche Berücksichtigung von Breite und Tiefe. Sollte jedes Feature im Entwurf nur ein wenig funktionieren, oder sollte ein Feature als Prototyp mit fast allen Teilen und Optionen ausgewählt werden? Versuchen Sie, nicht beides zu tun, da das Ergebnis ein großer, unhandlicher Prototyp sein kann, der schwer zu ändern und schwer zu verwerfen ist.

## <a name="flexible-prototypes"></a>Flexible Prototypen

Eine Möglichkeit, prototyperstellungsressourcen zu konzentrieren, besteht darin, sich auf intelligentes Design zu konzentrieren. Effektivere Prototypen können erstellt werden, indem ein Teil des Prototypcodes viele verschiedene Ideen umsetzen kann. Anstatt fünf verschiedene Prototypen zu verwenden, sollten Sie einen Prototyp erstellen, der die Optionen zum Wechseln der verschiedenen Attribute des Prototyps bietet.

Sollte sich die Symbolleiste links oder oben befinden? Sollen 10 Elemente auf der Startseite oder 20 angezeigt werden? Ein guter Prototyp verfügt über einen integrierten Optionsbereich, mit dem Sie die Parameter ändern können, wie der Prototyp aussieht oder funktioniert. Lassen Sie diese Optionspanels im Prototyp ausgeblendet. Versuchen Sie, zu vermeiden, dass ein Benutzerfreundlichkeitsteilnehmer sie versehentlich während eines Tests findet.

Die Herausforderung besteht darin, den Prototyp einfach zu halten, aber dennoch so nützlich zu sein, dass er einem Teamkameraden angezeigt werden kann, verschiedene Optionen demonstriert werden können und Feedback erhalten werden kann.

## <a name="beta-vs-prototype"></a>Beta und Prototyp

Betaversionen sind nicht als Prototypen qualifiziert, da es sich um vollständige Technische Maßnahmen handelt. Wenn ein kritischer Fehler in einem Feature eines Beta-Release gefunden wird, wird er wahrscheinlich nicht verworfen, auch wenn er möglicherweise im besten Interesse des Produkts liegt. Die Entwickler, Tester und Designer haben bereits viel Zeit investiert, und der Druck, mit schlechten Entscheidungen zu leben, ist sehr hoch. Betaversionen sind sicherlich hilfreich bei der Suche nach Fehlern und Fehlern, aber sie sind nur selten nützlich, um kontrollierte Studien zum Wert bestimmter Entwurfsanweisungen zu erstellen.

## <a name="tools-and-technologies"></a>Tools und Technologien

Es gibt mehrere verschiedene Tools und Technologien, die zum Erstellen von Prototypen verwendet werden können, von denen jede ihre Vor- und Nachteile hat. Berücksichtigen Sie die Art der Entwurfsarbeit, die als Prototyp verwendet wird, und die Ziele des Prototyperstellungsaufwands, bevor Sie entscheiden, welches Tool oder welche Technologie das richtige ist.

-   Microsoft Visual Basic oder C#.

    Dies ist die schnellste Technologie zum Erstellen Windows Benutzeroberflächenprototypen. Das Webbrowserobjekt erleichtert die Integration von HTMLUI in Standardkomponenten im Windows Stil. Es ist zwar richtig, dass ein Entwickler, der mit Microsoft Visual Studio kann, in C/C++ möglicherweise schneller benutzeroberfläche generieren kann, aber dies schafft die Gefahr, Code aus dem UI-Prototyp im Produktionscode wiederzuverwenden. Es erfordert Disziplin, um zu erkennen, dass die Ziele eines schnellen und geänderten Ui-Prototyps stark von der qualitativ hochwertigen Entwicklung abweichen. Stellen Sie sicher, dass klar ist, welche Art von Code geschrieben wird und dass das Team oder der Vorgesetzte versteht, was verworfen wird.

-   Microsoft Expression Blend + SketchFlow.

    SketchFlow ist ein visuelles Tool zum Entwerfen, Erstellen von Prototypen und Erstellen anspruchsvoller Benutzeroberflächen für Windows Presentation Foundation (WPF) und Microsoft Silverlight-Desktop- und -Webanwendungen. Anwendungen werden erstellt, indem Formen, Zeichensteuerelemente wie Schaltflächen und Listenfelder gezeichnet werden, sodass die Teile einer Anwendung auf Mausklicks und andere Benutzereingaben reagieren und alles so formatiert werden, dass es eindeutig aussieht.

-   Adobe Director oder Adobe Flash.

    Director ist ein beliebtes Prototyperstellungstools für die Benutzeroberfläche von Designern. Es ist besonders nützlich für Multimedia- oder nicht standardmäßige GUI-Entwürfe oder für Prototypen, die signifikante Animationen erfordern. Aufgrund der hohen Flexibilität ist es im Vergleich zu Visual Basic umständlich, die Benutzeroberfläche im Benutzeroberflächenstil zu gestalten. Ein wissenschaftlicher Director-Benutzer kann jedoch ohne Schwierigkeiten Windows oder web ui generieren.

-   HTML.

    FrontPage und andere HTML-Editoren ermöglichen die schnelle Erstellung einfacher Prototypen. Um eine Idee auszudrücken, ist es oft möglich, Bitmaps zu erstellen, die eine Abfolge der Benutzerinteraktion veranschaulichen und in FrontPage platzieren. Diese Bilder können verwendet werden, um die Interaktion mit dem Entwurf zu simulieren. JScript und DHTML führen die Dinge auf eine andere Ebene, sodass eine sehr komplexe Logik und Interaktion möglich ist. Wenn Sie HTML zum Erstellen eines Prototyps für eine Website verwenden, gilt die soeben für C/C++ beschriebene Warnung auch hier. Sie sollten nicht in den Fall eines verwirrenden schnellen Prototypcodes mit Produktionsqualitätsentwicklung fallen.

 

 




