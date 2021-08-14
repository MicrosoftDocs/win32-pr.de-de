---
title: Entwerfen eines Benutzeroberfläche
description: In diesem Abschnitt werden einige der Aufgaben im Zusammenhang mit dem Entwerfen einer Benutzeroberfläche für eine Windows Anwendung ausführlich beschrieben.
ms.assetid: 22deda0c-bf03-4fcd-9cc9-6381b601c152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914f8a2bf2afb532e3deed8876ce0ddea0fe71a0e8ad5457e5967e5f48eeb2c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440310"
---
# <a name="designing-a-user-interface"></a>Entwerfen eines Benutzeroberfläche

In diesem Abschnitt werden einige der Aufgaben im Zusammenhang mit dem Entwerfen einer Benutzeroberfläche für eine Windows Anwendung ausführlich beschrieben.

-   [Introduction (Einführung)](#introduction)
-   [Funktionale Anforderungen](#functional-requirements)
-   [Benutzeranalyse](#user-analysis)
    -   [Problemanweisungen](#problem-statements)
    -   [Prioritäten](#priorities)
-   [Konzeption](#conceptual-design)
-   [Logischer Entwurf](#logical-design)
-   [Physischer Entwurf](#physical-design)

## <a name="introduction"></a>Einführung

Der Entwurf der Benutzeroberfläche kann in drei wesentliche Elemente unterteilt werden: Funktionalität, Funktionalität und Leistung.

In den meisten Fällen liegt der Hauptfokus bei der Anwendungsentwicklung auf der Funktionalität. Kann die Anwendung verwendet werden? Ermöglicht es Benutzern das Ausführen von Aufgaben? Die Funktionalität ist jedoch nur ein Teil der Geschichte.

Mit Der Schrift wird beschrieben, wie Dinge dargestellt und dargestellt werden, und zwar in dem Stil, in dem dinge an den Benutzer kommuniziert werden. Die Wahrnehmung ist sehr subjektiv und viel schwieriger zu quantifizieren als funktionale Anforderungen und Leistungsmetriken. In der Regel geht es um einfache Entscheidungen – wie Farben einander ergänzen oder wie Benutzeroberflächenelemente ihre Bedeutung vermitteln –, die sich häufig auf die Art und Weise auswirken, wie eine Person etwas versteht und wie erfolgreich sie sie verwendet.

Die Leistung wird nicht nur anhand der Geschwindigkeit, sondern auch der Zuverlässigkeit gemessen. Wenn eine Anwendung gut aussieht und sich gut anfühlt, einfach zu verwenden ist, aber wiederholt abstürzt, wird sie wahrscheinlich nicht sehr erfolgreich sein. Die Anwendung muss einem Benutzer volles Vertrauen in seine Zuverlässigkeit bieten.

Im Folgenden finden Sie einige Aufgaben in der Entwurfsphase, die zu einer erfolgreichen Benutzeroberfläche für eine Windows Anwendung beitragen können.

## <a name="functional-requirements"></a>Funktionale Anforderungen

Berücksichtigen Sie die folgenden Vorschläge frühzeitig in der Entwurfsphase, um die Benutzerfreundlichkeit für eine möglichst breite Zielgruppe zu optimieren:

-   Befolgen Sie die Richtlinien für den Benutzeroberflächenentwurf.

    Machen Sie sich mit den Windows Richtlinien für die Interaktion mit der [Benutzeroberfläche](../uxguide/guidelines.md) vertraut, und verweisen Sie häufig darauf, wenn der Entwurf, die Implementierung und das Testen der Benutzeroberfläche der Anwendung ausgeführt werden.

-   Stellen Sie sicher, dass auf die Benutzeroberfläche zugegriffen werden kann.

    Achten Sie darauf, die Barrierefreiheit vom Anfang des Produktlebenszyklus an in den Benutzeroberflächenentwurf zu integrieren. Die Erstellung der Barrierefreiheit kann äußerst kostspielig sein, da ein Teil der Entwicklung der Barrierefreiheit Aufmerksamkeit auf der Architekturebene erfordert. Weitere Informationen finden Sie unter [Engineering Software for Accessibility eBook](https://www.microsoft.com/download/details.aspx?id=19262).

-   Unterstützung des internationalen Marketplace.

    Windows umfasst Technologien, die unterstützung für viele Kulturen und geschriebene Sprachen in einer Windows-Anwendung ermöglichen. Wenn die Anwendung auf den internationalen Marketplace ausgerichtet ist, ist es wichtig, die Internationalisierungsunterstützung vom Anfang des Projekts an in den Benutzeroberflächenentwurf einzubeziehen. Weitere Informationen finden Sie unter [Internationalisierung für Windows Anwendungen.](../intl/international-support.md)

## <a name="user-analysis"></a>Benutzeranalyse

Ein wichtiger Schritt beim Entwerfen einer erfolgreichen Schnittstelle ist das Erreichen eines grundlegenden Verständnisses, was Benutzer von einer Anwendung benötigen und wünschen, bevor Code geschrieben wird. Denken Sie daran, dass potenzielle Benutzer einer Anwendung ihre Arbeit bereits in irgendeiner Weise erledigen, und vorhandene Tools und Prozesse sollten so umfassend wie möglich verstanden werden. Entwerfen Sie nicht, ohne diese Probleme vollständig zu berücksichtigen.

Der einfachste und informellste Ansatz besteht darin, mit den vorgesehenen Benutzern des Produkts zu sprechen. Abrufen von Informationen direkt aus der Quelle: Vermeiden Sie die Verwendung von Managern oder Führungskräften als Proxys für tatsächliche Consumer. Erwägen Sie, kleine Gruppen von Entwicklern und Programmmanagern an ihren Arbeitsbereichen informell zu besuchen, wo es die Möglichkeit gibt, die Funktionsweise zu besprechen und Details zu den Problemen zu sammeln, mit denen sie mit ihren aktuellen Tools konfrontiert sind.

Denken Sie daran, keine führenden oder voreingenommenen Fragen zu stellen, da sich dies direkt auf die Qualität und Gültigkeit des Benutzerfeedbacks auswirkt. Beachten Sie beim Verfassen von Fragen in dieser Phase Folgendes:

-   Wer sind unsere Benutzer? Über welche Qualifikationen und Kenntnisse verfügen sie?
-   Welche verschiedenen Datenquellen können wir verwenden, um deren Erfahrung zu verstehen?
-   Welche Ziele und Aufgaben werden mit unserem Produkt abgeschlossen?
-   Welche Annahmen treffen wir und wie können wir sie überprüfen?
-   Welche Datenquellen haben wir? (Nutzbarkeitsstudien und heuristische Auswertungen sind gute Ausgangspunkte.)

### <a name="problem-statements"></a>Problemanweisungen

Sobald das gesamte Benutzerfeedback gesammelt wurde, analysieren und analysieren Sie es in verwandte Probleme und Anforderungen. Versuchen Sie, an dieser Stelle nicht über Lösungen nachzudenken. Stellen Sie sicher, dass die Probleme vollständig identifiziert sind, nicht nur die Symptome.

Es ist häufig hilfreich, für jedes Problem oder jede Anforderung eine Liste mit einem Satz Problemanweisungen (aus Sicht der Benutzer) zu erstellen. Beispielsweise ist "Größe des Bearbeitungsfelds auf 15 Zeichen ändern" kein Problem. "Es ist zu schwierig, lange Suchbegriffe einzugeben" ist jedoch eine gültige Problemhinweisstellung. Der Unterschied ist erheblich. Versuchen Sie nicht, die Lösung und das Problem gleichzeitig zu definieren: Häufig geht das eigentliche Problem verloren. In diesem Beispiel gibt es möglicherweise viele andere Möglichkeiten, das Problem von Suchbegriffen zu lösen, einschließlich der Änderung der Größe des Bearbeitungsfelds. Denken Sie immer an alternative Lösungen.

Im Folgenden finden Sie weitere Beispiele für Problemanweisungen:

-   Es ist schwierig, von einem Abschnitt der Website zu einem anderen zu navigieren.
-   Benutzer müssen zu lange warten, bis die Software geladen wurde.
-   Unsere Sicherheitsfehlermeldungen sind schwer zu verstehen.
-   Die Registrierungsseite hat zu viele Fragen, und Benutzer verwerfen sie häufig.
-   Es ist zu schwierig, ein bestimmtes Produkt auf dem Standortindex zu finden.

Wenn die Problemanweisungen breit genug sind, gibt es wahrscheinlich viele innovative und kreative Möglichkeiten, sie zu lösen.

### <a name="priorities"></a>Prioritäten

Durch das Erstellen einer Liste von Elementen und deren Rangfolge nach Priorität wird ein Release definiert. Ohne klare Prioritäten können sich Teams darüber im Klaren sein, welche Aufgaben ausgeführt und welche Punkte abgeschnitten werden sollten. Die Arbeit am Festlegen von Prioritäten sollte mit dem Abschluss der Forschung einfacher sein, aber es ist immer eine Herausforderung.

Das Festlegen von Prioritäten erfordert die Möglichkeit, anhand von mindestens drei Kriterien zu bewerten: Zeitplan, Team und Unternehmen. Möglicherweise gibt es einen vordefinierten Zeitplansatz für das Projekt, der die Größe und Skalierung der Arbeit einschränkt, die ausgeführt werden kann. Ein Problem, bei dem wahrscheinlich die Hälfte der Codebasis neu geschrieben werden muss, sollte während eines kleinen Releasezyklus nicht versucht werden.

Das Make-up und die Art eines Teams definieren, welche Arten von Arbeit ausgeführt werden können. Welche weiteren Verpflichtungen hat das Team? Gibt es einen Designer oder Usability Engineer im Team? Über welche Kenntnisse im Web- oder Benutzeroberflächendesign verfügt das Team? Die letzten und wichtigsten Aspekte sind geschäftliche Überlegungen. Was sind die Umsatzziele für dieses Projekt? Wer sind die Mitbewerber? Welche Vorteile bietet die Lösung bestimmter Probleme? Welche Partnerschaften können gefälscht werden? Vor der Priorisierung der Liste sollten auch andere Überlegungen berücksichtigt werden.

Nach der Priorisierung legt die Liste der Problemanweisungen die Richtung für das Produkt fest und stellt sicher, dass die Entwicklung in den richtigen Bereichen ausgerichtet ist.

## <a name="conceptual-design"></a>Konzeption

In der Regel wird die Benutzeroberfläche in der Konzeptionellen Entwurfsphase nicht behandelt. Für diese Phase ist jedoch ein umfassendes Geschäftsmodell mit vollständigen Benutzerprofilen und Nutzungsszenarien erforderlich, die für eine erfolgreiche Benutzererfahrung unerlässlich sind.

## <a name="logical-design"></a>Logischer Entwurf

Die logische Entwurfsphase ist, wenn die ersten Prototypen, die den konzeptionellen Entwurf unterstützen, entwickelt werden.

Die spezifischen Hardware- und Softwaretechnologien, die während der Entwicklung verwendet werden sollen, werden auch in dieser Phase identifiziert, die die Funktionen der Benutzeroberfläche im Endgültigen Produkt bestimmen können. Weitere Informationen finden Sie unter [Benutzeroberfläche Technologies](user-interface-technologies-for-windows-applications.md).

Zusätzlich zu den Entwicklungstools sollten die verschiedenen Hardwareanforderungen und Formfaktoren identifiziert werden, die von der Anwendung berücksichtigt werden sollen.

## <a name="physical-design"></a>Physischer Entwurf

Die Phase des physischen Entwurfs bestimmt, wie ein Benutzeroberflächenentwurf für die spezifische Hardware und die Formfaktoren implementiert werden soll, die im logischen Entwurf identifiziert wurden.

Während dieser Phase können Hardware- oder Formfaktoreinschränkungen zu unerwarteten Einschränkungen auf der Benutzeroberfläche führen, die erhebliche Verbesserungen am Entwurf erfordern.

 

 