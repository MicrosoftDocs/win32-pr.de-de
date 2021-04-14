---
title: Entwerfen einer Benutzeroberfläche
description: In diesem Abschnitt werden einige der Aufgaben im Zusammenhang mit dem Entwerfen einer Benutzeroberfläche für eine Windows-Anwendung ausführlich beschrieben.
ms.assetid: 22deda0c-bf03-4fcd-9cc9-6381b601c152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97d5027baf7276b1353e03254478545e554daa5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473732"
---
# <a name="designing-a-user-interface"></a>Entwerfen einer Benutzeroberfläche

In diesem Abschnitt werden einige der Aufgaben im Zusammenhang mit dem Entwerfen einer Benutzeroberfläche für eine Windows-Anwendung ausführlich beschrieben.

-   [Introduction (Einführung)](#introduction)
-   [Funktionale Anforderungen](#functional-requirements)
-   [Benutzer Analyse](#user-analysis)
    -   [Problem Anweisungen](#problem-statements)
    -   [Prioritäten](#priorities)
-   [Konzeptioneller Entwurf](#conceptual-design)
-   [Logischer Entwurf](#logical-design)
-   [Physischer Entwurf](#physical-design)

## <a name="introduction"></a>Einführung

Der Benutzeroberflächen Entwurf kann in drei wesentliche Elemente unterteilt werden: Funktionalität, Ästhetik und Leistung.

Der Hauptschwerpunkt bei der Anwendungsentwicklung ist in der Regel die Funktionalität. Kann die Anwendung verwendet werden? Ermöglicht es Benutzern das Ausführen von Aufgaben? Die Funktionalität ist jedoch nur ein Teil der Story.

Die Ästhetik beschreibt, wie Dinge angezeigt und dargestellt werden, die Art und Weise, in der die Elemente an den Benutzer übermittelt werden. Die Ästhetik ist sehr subjektiv und viel schwieriger zu quantifizieren als funktionale Anforderungen und Leistungsmetriken. Die Ästhetik kommt in der Regel zu einfachen Optionen – wie sich Farben ergänzen, oder wie Benutzeroberflächen Elemente ihre Bedeutung vermitteln –, die sich häufig auf die Art und Weise auswirken, wie sich eine Person etwas fühlt und beeinflussen, wie erfolgreich Sie verwendet wird.

Die Leistung wird mit nicht nur Geschwindigkeit, sondern auch mit der Zuverlässigkeit gemessen. Wenn eine Anwendung sehr gut aussieht und sich gut eignet, ist leicht zu verwenden, stürzt aber wiederholt ab, aber Sie ist wahrscheinlich nicht sehr erfolgreich. Die Anwendung muss einem Benutzer volles Vertrauen in seine Zuverlässigkeit bieten.

Im folgenden finden Sie einige Aufgaben der Entwurfsphase, die zu einer erfolgreichen Benutzeroberfläche für eine Windows-Anwendung beitragen können.

## <a name="functional-requirements"></a>Funktionale Anforderungen

Beachten Sie die folgenden Vorschläge in der Entwurfsphase, um die Benutzer Leistung für die größtmögliche Zielgruppe zu optimieren:

-   Befolgen Sie die Richtlinien zur Benutzeroberfläche

    Machen Sie sich mit den [Richtlinien](../uxguide/guidelines.md) für die Interaktion der Windows-Benutzeroberfläche vertraut, und informieren Sie sich häufig über das Design, die Implementierung und das Testen der Benutzeroberfläche der Anwendung.

-   Stellen Sie sicher, dass die Benutzeroberfläche zugänglich ist.

    Stellen Sie sicher, dass Sie vom Anfang des Produktlebenszyklus aus den Barrierefreiheit in den Benutzeroberflächen Entwurf integrieren. Die Barrierefreiheits Barrierefreiheit kann sehr kostspielig sein, da ein Teil der Barrierefreiheits Entwicklung auf der Architekturebene Aufmerksamkeit erfordert. Weitere Informationen erhalten Sie, wenn Sie das e- [Book für die Barrierefreiheit](https://www.microsoft.com/download/details.aspx?id=19262)herunterladen.

-   Unterstützung des internationalen Marketplace.

    Windows umfasst Technologien, die Unterstützung für viele Kulturen und geschriebene Sprachen in einer Windows-Anwendung ermöglichen. Wenn die Anwendung auf den internationalen Marketplace abzielt, ist es wichtig, die Internationalisierungsunterstützung am Anfang des Projekts in das Design der Benutzeroberfläche einzubeziehen. Weitere Informationen finden Sie unter [Internationalisierung für Windows-Anwendungen](../intl/international-support.md).

## <a name="user-analysis"></a>Benutzer Analyse

Ein wichtiger Schritt beim Entwerfen einer erfolgreichen Oberfläche ist die Erzielung eines grundlegenden Verständnisses, was Benutzer vor dem Schreiben von Code für eine Anwendung benötigen und benötigen. Beachten Sie, dass potenzielle Benutzer einer Anwendung ihre Arbeit bereits auf irgendeine Weise erledigen und vorhandene Tools und Prozesse so umfassend wie möglich verstanden werden können. Entwerfen Sie diese Probleme nicht, ohne Sie vollständig zu berücksichtigen.

Der einfachste und aktuellste Ansatz besteht im Gespräch mit den beabsichtigten Benutzern des Produkts. Informationen direkt aus der Quelle erhalten – vermeiden Sie die Verwendung von Managern oder Führungskräften als Proxys für tatsächliche Consumer. Nehmen Sie an, dass kleine Gruppen von Entwicklern und Programmmanagern informelle Besuche an den Benutzern an ihren Arbeitsplätzen bezahlen, wenn Sie die Möglichkeit haben, zu besprechen, wie Sie arbeiten, und die Details der Probleme, die Sie mit ihren aktuellen Tools haben, erfassen.

Denken Sie daran, dass Sie keine führenden oder unausgewogenen Fragen stellen müssen, da sich dies direkt auf die Qualität und die Gültigkeit des Benutzer Feedbacks auswirkt. Beachten Sie beim Verfassen von Fragen in dieser Phase Folgendes:

-   Wer sind die Benutzer? Welche Fähigkeiten und Kenntnisse haben Sie?
-   Welche unterschiedlichen Datenquellen können wir verwenden, um Ihre Arbeit zu verstehen?
-   Welche Ziele und Aufgaben werden für die Fertigstellung des Produkts verwendet?
-   Welche Annahmen treffen wir an, und wie können wir Sie verifizieren?
-   Welche Datenquellen haben wir? (Nutzbarkeits Studien und heuristische Auswertungen sind gute Ausgangspunkte.)

### <a name="problem-statements"></a>Problem Anweisungen

Nachdem Sie das gesamte Benutzer Feedback gesammelt haben, analysieren Sie es in Bezug auf verwandte Probleme und Anforderungen. Versuchen Sie, die Lösungen an dieser Stelle nicht zu überdenken. Stellen Sie sicher, dass die Probleme vollständig identifiziert werden, nicht nur die Symptome.

Häufig ist es hilfreich, eine Liste von Problem Anweisungen für einen Satz (aus Sicht der Benutzer) für jedes Problem oder jede Anforderung zu verfassen. Beispiel: "die Breite von Bearbeitungs Feldern in 15 Zeichen ändern" ist kein Problem. Aber "Es ist zu schwierig, lange Suchbegriffe einzugeben" ist eine gültige Problem Anweisung. Der Unterschied ist dramatisch. Versuchen Sie nicht, die Lösung und das Problem gleichzeitig zu definieren: häufig geht das eigentliche Problem verloren. In diesem Beispiel gibt es möglicherweise viele weitere Möglichkeiten, um das Problem der Suchbegriffe zu beheben, einschließlich der Änderung der Größe des Bearbeitungs Felds. Behalten Sie immer alternative Lösungen in Betracht.

Im folgenden finden Sie weitere Beispiele für Problem Anweisungen:

-   Es ist schwierig, von einem Abschnitt der Website zu einem anderen zu navigieren.
-   Benutzer müssen zu lange warten, bis die Software geladen ist.
-   Unsere Sicherheits Fehlermeldungen sind schwer zu verstehen.
-   Die Registrierungsseite weist zu viele Fragen auf, und Benutzer verwerfen Sie häufig.
-   Das Auffinden eines bestimmten Produkts am Site Index ist zu schwierig.

Wenn die Problem Anweisungen breit genug sind, gibt es wahrscheinlich viele innovative und kreative Möglichkeiten, Sie zu beheben.

### <a name="priorities"></a>Prioritäten

Durch das Durchführen einer Liste von Elementen und die Rangfolge nach Priorität wird ein Release definiert. Ohne klare Prioritäten können Teams Maßnahmen zur Durchsetzung und zum Ausschneiden der Dinge tun. Der Aufwand für das Festlegen von Prioritäten sollte mit dem Abschluss der Recherche einfacher sein, aber es ist immer eine Herausforderung.

Zum Festlegen von Prioritäten müssen mindestens drei Kriterien erfüllt werden: "Schedule", "Team" und "Business". Möglicherweise ist für das Projekt ein vordefinierter Zeitplan festgelegt, der die Größe und die Skalierung der Arbeit einschränkt, die erledigt werden kann. Ein Problem, bei dem wahrscheinlich ein Umschreiben der Hälfte der Codebasis erforderlich ist, sollte während eines kleinen Releasezyklen nicht versucht werden.

Die Zusammensetzung und Art eines Teams definieren, welche Arten von Arbeit durchgeführt werden können. Welche anderen Verpflichtungen hat das Team? Gibt es einen Designer oder einen Nutzbarkeits Techniker für das Team? Welche Fähigkeiten hat das Team mit dem Web-oder UI-Design? Die letzten und wichtigsten Aspekte sind geschäftliche Überlegungen. Was sind die Umsatzziele für dieses Projekt? Wer sind die Mitbewerber? Was sind die Vorteile der Behebung bestimmter Probleme? Welche Partnerschaften können gefälscht werden? Weitere Überlegungen sollten auch vor der Priorisierung der Liste identifiziert werden.

Nach der priorisierten Priorität legt die Liste der Problem Anweisungen die Richtung für das Produkt fest und stellt sicher, dass die Entwicklung auf die richtigen Bereiche ausgerichtet ist.

## <a name="conceptual-design"></a>Konzeptioneller Entwurf

In der Regel wird die Benutzeroberfläche nicht in der konzeptionellen Entwurfsphase behandelt. Allerdings ist für diese Phase ein umfassendes Geschäftsmodell mit vollständigen Benutzerprofilen und Verwendungs Szenarien erforderlich, die für eine erfolgreiche Benutzer Leistung unabdingbar sind.

## <a name="logical-design"></a>Logischer Entwurf

Die logische Entwurfsphase ist, wenn die anfänglichen Prototypen entwickelt werden, die den konzeptionellen Entwurf unterstützen.

Die spezifischen Hardware-und Softwaretechnologien, die während der Entwicklung verwendet werden sollen, werden auch in dieser Phase identifiziert, die die Funktionen der Benutzeroberfläche im endgültigen Produkt bestimmen kann. Weitere Informationen finden Sie unter [Benutzeroberflächen Technologien](user-interface-technologies-for-windows-applications.md).

Zusätzlich zu den Entwicklungs Tools sollten die verschiedenen Hardwareanforderungen und Formfaktoren, die für die Anwendung gelten, identifiziert werden.

## <a name="physical-design"></a>Physischer Entwurf

Die physische Entwurfsphase bestimmt, wie ein UI-Entwurf für die jeweilige Hardware und die im logischen Entwurf identifizierten Formen Faktoren implementiert wird.

In dieser Phase kann es durch Hardware-oder Formfaktor Einschränkungen zu unerwarteten Einschränkungen auf der Benutzeroberfläche kommen, die wesentliche Verbesserungen des Entwurfs erfordern.

 

 