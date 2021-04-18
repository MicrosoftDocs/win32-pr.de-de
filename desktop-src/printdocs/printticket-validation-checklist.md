---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 4698f151-2237-4d16-b32f-4d15024cd063
title: Prüfprüfliste für PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a0e9f3eb71b1e9a3b670456e04e2efa3c8b15
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106361132"
---
# <a name="printticket-validation-checklist"></a>Prüfprüfliste für PrintTicket

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Print Ticket-Anbieter müssen das PrintTicket validieren, bevor Sie es für einen beliebigen Zweck verwenden. Nachdem das PrintTicket überprüft wurde, kann es an den Client zurückgegeben werden, oder es kann nach der Verwendung verworfen werden. Diese Prüfliste enthält die Aufgaben, die der Anbieter während der Überprüfung ausführen muss. Bei der Überprüfung wird der Inhalt von PrintTicket häufig geändert, obwohl ein zuvor überprüftes Print Ticket nicht geändert wird.

Die Überprüfung erfolgt immer für ein bestimmtes Gerät, das über eine Reihe von Funktionen-, Options-und ParameterDef-Instanzen verfügt, die in einem Printworks-Dokument definiert sind. Der Überprüfungs Code muss Zugriff auf den Satz von featureinstanzen (und die enthaltenen Options Instanzen) und ParameterDef-Instanzen für das jeweilige Gerät haben und sollte nicht auf printfunktionen zugreifen müssen. Die Informationen aus den Funktionen, der Option und der ParameterDef-Instanz werden in bestimmten Teilen des Validierungsprozesses benötigt.

1.  Beachten Sie bei der Suche nach entsprechenden oder übereinstimmenden Elementen, dass die Namespaces der Elemente übereinstimmen müssen, bevor ein qualifizierter Name als Übereinstimmung betrachtet werden kann. Alle Elementnamen, Attributnamen und Instanznamen sind Namespace qualifiziert. Bei Elementen, die sich in der Liste befinden, müssen die Speicherorte identisch sein, bevor die Elemente als eine Entsprechung betrachtet werden.

2.  Vergewissern Sie sich, dass sich alle Element Tags im öffentlichen Namespace befinden, vom PrintTicket-Schema definiert werden, die richtigen XML-Attribute und-Attributwerte enthalten und dass der Speicherort der einzelnen Elementtypen der Schema definierten PrintTicket-Verwendung entspricht.

3.  Bestimmen Sie alle vom printfunktionalitäten-Dokument gemeldeten Namespaces. Entfernen Sie alle Elemente (und deren Nachfolger) aus dem PrintTicket, dessen Instanznamen zu Namespaces gehören, die nicht von printfunktionalitäten dokumentiert werden. Beachten Sie den Unterschied zwischen diesem und dem folgenden Fall, der nicht erkannte Instanznamen innerhalb eines bekannten Namespace umfasst.

4.  Aufgrund der Tatsache, dass die Schemas ständig durch das Hinzufügen neuer elementinstanzdefinitionen erweitert werden, sollte der Validierungscode nicht unter der Annahme geschrieben werden, dass jeder Instanzname in einem bestimmten Namespace bekannt ist. Der Validierungscode kann keine unbekannten Instanznamen innerhalb eines bekannten Namespaces als Fehler behandeln und auch nicht aus Print Ticket löschen.

5.  Wenn eine Element Instanz über ein doppeltes gleich geordnetes Element verfügt, das nicht durch das PrintTicket-Schema zulässig ist, behalten Sie nur das erste Vorkommen bei, und löschen Sie die Duplikate, einschließlich des Inhalts des duplizierten Elements.

6.  Entfernen Sie aus der PrintTicket any-Funktion oder-Unterfunktion (und alle zugehörigen untergeordneten Elemente), die über keine entsprechende Funktion im printfunktionalitäten-Dokument verfügt.

7.  Überprüfen Sie die im Printworks-Dokument definierte SelectionType-Eigenschaft für jede der verbleibenden Merkmals Instanzen in PrintTicket. Für jede Funktion, deren SelectionType-Eigenschaft auf pickone festgelegt ist, muss genau eine Options Instanz im PrintTicket vorhanden sein, während eine Funktion, deren SelectionType-Eigenschaft pickmany ist, mehr als eine Instanz aufweisen kann. Wenn eine PrintTicket-Funktion keine Options Instanz aufweist, geben Sie die standardmäßige Options Instanz an. Da Sie der Anbieter sind, wissen Sie, welche Option die Standardoption für jede Funktion ist.

    Für eine Funktion, deren SelectionType-Eigenschaft pickmany ist, bei der Sie mehr als eine Option im PrintTicket ausgewählt haben, stellen Sie sicher, dass keine Option als identityoption festgelegt ist. Wenn dies der Fall ist, löschen Sie alle anderen Optionen, und behalten Sie nur die festgelegte identityoption.

8.  Entfernen Sie eine beliebige parameterinit-Instanz im PrintTicket, die keine entsprechende ParameterDef-Instanz im Print-Funktionen-Dokument enthält.

    Überprüfen Sie für alle anderen parameterinit-Instanzen in PrintTicket, ob der Wert für jede der ParameterDef-Instanz des printfunktionalitäten-Dokuments entspricht. Wenn ein Wert fehlt, geben Sie den Standardwert an, der in der ParameterDef bereitgestellt wird.

9.  Koppeln Sie jede Options Instanz im PrintTicket, und wählen Sie eine Option aus, die im Dokument printfunktionen in der entsprechenden Funktion aufgelistet ist, und zwar basierend auf den Ergebnissen des Bewertungsprozesses. Bei der Bewertung wird die Option im Printworks-Dokument gesucht, die am besten mit der Option in PrintTicket übereinstimmt. Eine Beschreibung der Vorgänge, die während der Bewertung berücksichtigt werden, finden Sie unter [options Definitionen](option-definitions.md). Ersetzen Sie jede Verweis Option in PrintTicket durch die entsprechende Best stimmende Kandidaten printfunktionalitäten-Dokument Option. Sie können auch alle Kandidaten nach Bewertung als Rangfolge bewerten und diese Informationen an die Auflösungsphase übergeben, falls ein Einschränkungs Konflikt verhindert, dass der beste übereinstimmende Kandidat verwendet wird. In solchen Fällen kann der Auflösungsprozess den zweitbesten Kandidaten verwenden, anstatt einen anderen Kandidaten zufällig auszuwählen.

10. Für eine Funktion, deren SelectionType-Eigenschaft auf pickmany festgelegt ist und mehr als eine Option im PrintTicket ausgewählt ist, vergewissern Sie sich, dass keine Option als identityoption festgelegt ist. Wenn eine solche Option vorhanden ist, löschen Sie alle anderen Optionen, und behalten Sie nur die festgelegte identityoption. Dieser Schritt muss ausgeführt werden, bevor und nachdem der Bewertungsprozess angewendet wurde.

    Der Grund dafür, dass dieser Schritt zweimal ausgeführt werden muss, besteht darin, dass es möglich ist, dass der Bewertungsprozess mehrere Verweis Options Instanzen derselben Kandidaten Option zuordnet. Wenn dies der Fall ist, löschen Sie alle doppelten Options Instanzen, damit die für eine bestimmte pickmany-Funktion aufgeführten Optionen eindeutig sind.

11. Fügen Sie das PrintTicket-Feature hinzu, das im Print-Funktionen-Dokument vorhanden ist, das nicht im PrintTicket angezeigt wird. Legen Sie für eine solche Funktion die Standardoption als ausgewählte Option fest.

12. Stellen Sie fest, ob ParameterDef-Instanzen vorhanden sind, die alle folgenden Kriterien erfüllen:

    -   Die ParameterDef-Instanz wird im Printworks-Dokument angezeigt, aber nicht im PrintTicket.

    -   Die obligatorische-Eigenschaft der ParameterDef-Instanz ist entweder auf bedingungslos oder Conditional festgelegt.

    -   Auf die ParameterDef-Instanz wird von einer ParameterRef-Instanz im PrintTicket innerhalb einer Options Instanz verwiesen.

    Fügen Sie für jede solche ParameterDef-Instanz im printfunktionalitäten-Dokument dem PrintTicket eine entsprechende parameterinit-Instanz hinzu. Legen Sie den Wert der neu hinzugefügten parameterinit-Instanzen auf den Standardwert fest, der durch die entsprechenden ParameterDef-Instanzen angegeben wird.

13. Führen Sie eine Einschränkungs Konflikterkennung aus, und ändern Sie die Konfiguration, um derartige Konflikte auszuschließen. In diesem Thema wird kein bestimmter Prozess zum Auflösen von Einschränkungs Konflikten definiert. Sie müssen entscheiden, welche Funktion oder parameterinit-Instanz geändert werden kann, und eine entsprechende Option bzw. einen entsprechenden Wert auswählen, die die geringsten Auswirkungen auf die allgemeine Absicht der im PrintTicket angegebenen Konfiguration hat. Wie bereits erwähnt, empfiehlt es sich, die zuder zuordnungsbewertung der einzelnen Optionen zu verwenden und die Option mit der zweiten höchsten Bewertung zu verwenden. Wenn Sie bestimmen möchten, welche Funktion oder parameterinit geändert werden soll, sollten Sie eine private Eigenschaft definieren, die der Client dem PrintTicket hinzufügen kann. Diese Eigenschaft kann eine Priorität für Feature-und parameterinit-Instanzen definieren, sodass der Auflösungsprozess informiert wird, welche Funktion oder parameterinit-Instanzen für den Client wichtig sind (und im PrintTicket aufbewahrt werden müssen) und welche weniger wichtig sind.

14. Wenn der Einschränkungs Prozess für die Einschränkung Änderungen im PrintTicket für alle ParameterRef-Instanzen verursacht hat, für die die obligatorische Eigenschaft auf Conditional festgelegt ist, fügen Sie parameterinit-Instanzen mit Standardwerten für diejenigen hinzu, die nun angezeigt werden, und entfernen Sie alle parameterinit-Instanzen für eine ParameterRef-Instanz, die nicht mehr angezeigt wird.

15. Entfernen Sie alle Eigenschaften Instanzen und deren Inhalte, die in Options Instanzen in PrintTicket angezeigt werden. Eigenschaften Elemente haben keine Rolle in PrintTicket. Wenn die Option überprüft für eine bestimmte Funktion perfekt mit der Option prevalion übereinstimmt, übertragen Sie alle Eigenschaften Instanzen in dieser Option vom vorab Überprüfung PrintTicket auf das jetzt validierte PrintTicket, unterliegen der Bedingung, dass Namespaces von Eigenschaften Instanzen im Dokument printfunktionalitäten registriert sind. Beachten Sie, dass es für zwei Options Instanzen als perfekte Übereinstimmung betrachtet werden muss. für jede ScoredProperty, die in einer Option enthalten ist, muss in der anderen Option eine entsprechende ScoredProperty vorhanden sein, und die Werte der beiden ScoredProperty-Instanzen müssen identisch sein.

16. Wenn Ihr PrintTicket-Anbieter private oder öffentliche Eigenschaften Instanzen erkennt und unterstützt, die bis zu diesem Punkt noch vorhanden sind, führen Sie eine Überprüfung durch. Löschen Sie an dieser Stelle eine Eigenschaft nicht, da Sie Sie nicht erkennen kann, da Sie möglicherweise für eine andere Phase der Dokument Verarbeitung vorgesehen ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



