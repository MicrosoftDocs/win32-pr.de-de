---
description: Überprüfen Sie die Prüfliste für die PrintTicket-Überprüfung. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: 4698f151-2237-4d16-b32f-4d15024cd063
title: Prüfliste für die PrintTicket-Überprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd9f6c04bc1cd57ce453c061e30c25d2111964f5f82bdaa21bf5921cd53c30e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091710"
---
# <a name="printticket-validation-checklist"></a>Prüfliste für die PrintTicket-Überprüfung

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

PrintTicket-Anbieter müssen das PrintTicket überprüfen, bevor es für einen beliebigen Zweck verwendet wird. Nachdem das PrintTicket überprüft wurde, kann es an den Client zurückgegeben oder nach der Verwendung verworfen werden. In dieser Prüfliste werden die Aufgaben behandelt, die der Anbieter während der Überprüfung ausführen muss. Der Überprüfungsprozess ändert häufig den Inhalt des PrintTicket, obwohl er kein zuvor überprüftes PrintTicket ändert.

Die Überprüfung wird immer für ein bestimmtes Gerät ausgeführt, für das ein Satz von Feature-, Options- und ParameterDef-Instanzen in einem PrintCapabilities-Dokument definiert ist. Der Validierungscode sollte Zugriff auf den Satz von Featureinstanzen (und die enthaltenen Optionsinstanzen) und ParameterDef-Instanzen für das jeweilige Gerät haben und nicht auf printCapabilities zugreifen müssen. Die Informationen aus den Instanzen Feature, Option und ParameterDef werden in bestimmten Teilen des Überprüfungsprozesses benötigt.

1.  Beachten Sie bei versuchen, entsprechende oder übereinstimmende Elemente zu finden, dass die Namespaces der Elemente übereinstimmen müssen, bevor ein qualifizierter Name als Übereinstimmung betrachtet werden kann. Alle Elementnamen, Attributnamen und Instanznamen sind namespacequalifiziert. Für geschachtelte Elemente müssen ihre Positionen übereinstimmen, bevor die Elemente als Übereinstimmung betrachtet werden.

2.  Stellen Sie sicher, dass sich alle Elementtags im öffentlichen Namespace befinden, durch das PrintTicket-Schema definiert sind, die richtigen XML-Attribute und Attributwerte enthalten und ob der Speicherort jedes Elementtyps der vom PrintTicket-Schema definierten Verwendung entspricht.

3.  Bestimmen Sie alle Namespaces, die vom PrintCapabilities-Dokument gemeldet werden. Entfernen Sie alle Elemente (und ihre Nachfolger) aus dem PrintTicket, dessen Instanznamen zu Namespaces gehören, die nicht vom PrintCapabilities-Dokument gemeldet werden. Beachten Sie den Unterschied zwischen diesem und dem folgenden Fall, der nicht erkannte Instanznamen innerhalb eines bekannten Namespace umfasst.

4.  Da die Schemas ständig um neue Elementinstanzdefinitionen erweitert werden, sollte der Validierungscode nicht unter der Annahme geschrieben werden, dass jeder Instanzname in einem bestimmten Namespace bekannt ist. Der Validierungscode kann nicht erkannte Instanznamen innerhalb eines bekannten Namespace nicht als Fehler behandeln und auch nicht aus dem PrintTicket löschen.

5.  Wenn eine Elementinstanz über ein doppeltes gleichgeordnetes Element verfügt, das vom PrintTicket-Schema nicht zugelassen wird, behalten Sie nur das erste Vorkommen bei, und löschen Sie die Duplikate, einschließlich des Inhalts des duplizierten Elements.

6.  Entfernen Sie alle Funktionen oder Untergeordneten Features (und alle untergeordneten Elemente), die keine entsprechende Funktion im PrintCapabilities-Dokument enthalten, aus printTicket.

7.  Überprüfen Sie die SelectionType-Eigenschaft, die im PrintCapabilities-Dokument für jede der verbleibenden Featureinstanzen im PrintTicket definiert ist. Jedes Feature, dessen SelectionType-Eigenschaft auf PickOne festgelegt ist, muss genau eine Option-Instanz im PrintTicket enthalten, während ein Feature, dessen SelectionType-Eigenschaft PickMany ist, über mehrere Instanzen verfügen kann. Wenn ein PrintTicket-Feature über keine Option-Instanz verfügt, geben Sie die Standardoptionsinstanz an. Da Sie der Anbieter sind, wissen Sie, welche Option die Standardoption für jedes Feature ist.

    Vergewissern Sie sich für ein Feature, dessen SelectionType-Eigenschaft PickMany lautet und bei dem mehr als eine Option im PrintTicket ausgewählt ist, dass keine Option als IdentityOption festgelegt ist. Wenn vorhanden, löschen Sie jede andere Option, und lassen Sie nur die angegebene IdentityOption übrig.

8.  Entfernen Sie alle ParameterInit-Instanzen im PrintTicket, die keine entsprechende ParameterDef-Instanz im PrintCapabilities-Dokument aufweisen.

    Überprüfen Sie für alle anderen ParameterInit-Instanzen im PrintTicket, ob der Wert für jedes der ParameterDef-Instanz des PrintCapabilities-Dokuments entspricht. Wenn ein Wert fehlt, stellen Sie den Standardwert bereit, der in der ParameterDef bereitgestellt wird.

9.  Koppeln Sie jede Optionsinstanz im PrintTicket basierend auf den Ergebnissen des Bewertungsprozesses mit einer Option, die im entsprechenden Feature im PrintCapabilities-Dokument aufgeführt ist. Bewertung ist der Prozess, bei dem die Option im PrintCapabilities-Dokument gesucht wird, die der Option im PrintTicket am besten entspricht. Eine Beschreibung der Berücksichtigung während des Bewertungsprozesses finden Sie unter [Optionsdefinitionen.](option-definitions.md) Ersetzen Sie jede Verweisoption im PrintTicket durch die entsprechende Best Matching Candidate PrintCapabilities-Dokumentoption. Sie können auch alle Kandidaten nach Bewertung bewerten und diese Informationen an die Auflösungsphase übergeben, falls ein Einschränkungskonflikt verhindert, dass der beste Abgleichskandidat verwendet wird. In solchen Fällen kann der Auflösungsprozess den zweitbesten Kandidaten verwenden, anstatt nach dem Zufallsprinzip einen anderen Kandidaten zu wählen.

10. Überprüfen Sie für ein Feature, dessen SelectionType-Eigenschaft auf PickMany festgelegt ist und für das im PrintTicket mehrere Optionen ausgewählt sind, dass keine Option als IdentityOption festgelegt ist. Wenn eine solche Option vorhanden ist, löschen Sie jede andere Option, und lassen Sie nur die angegebene IdentityOption übrig. Dieser Schritt muss vor und nach dem Anwenden des Bewertungsprozesses ausgeführt werden.

    Der Grund dafür, dass dieser Schritt zweimal ausgeführt werden muss, ist, dass der Bewertungsprozess mehrere Verweisoptionsinstanzen derselben Kandidatenoption zuordnen kann. Löschen Sie in diesem Fall alle doppelten Optionsinstanzen, sodass die für ein bestimmtes PickMany-Feature aufgelisteten Optionen eindeutig sind.

11. Fügen Sie dem PrintTicket ein beliebiges Feature im PrintCapabilities-Dokument hinzu, das nicht im PrintTicket angezeigt wird. Legen Sie für ein solches Feature die Standardoption als ausgewählte Option fest.

12. Bestimmen Sie, ob ParameterDef-Instanzen vorhanden sind, die alle folgenden Kriterien erfüllen:

    -   Die ParameterDef-Instanz wird im PrintCapabilities-Dokument, jedoch nicht im PrintTicket angezeigt.

    -   Die mandatory-Eigenschaft der ParameterDef-Instanz ist entweder auf "Bedingungslos" oder "Bedingt" festgelegt.

    -   Auf die ParameterDef-Instanz wird von einer ParameterRef-Instanz im PrintTicket innerhalb einer Option-Instanz verwiesen.

    Fügen Sie für jede solche ParameterDef-Instanz im PrintCapabilities-Dokument dem PrintTicket eine entsprechende ParameterInit-Instanz hinzu. Legen Sie den Wert der neu hinzugefügten ParameterInit-Instanzen auf den Standardwert fest, der von den entsprechenden ParameterDef-Instanzen angegeben wird.

13. Führen Sie die Einschränkungskonflikterkennung durch, und ändern Sie die Konfiguration, um solche Konflikte zu vermeiden. In diesem Thema wird kein bestimmter Prozess zum Auflösen von Einschränkungskonflikten definiert. Sie müssen entscheiden, welche Feature- oder ParameterInit-Instanz geändert werden kann, und eine entsprechende Option bzw. einen wert auswählen, die die geringsten Auswirkungen auf die Gesamtabsicht der im PrintTicket angegebenen Konfiguration hat. Wie bereits erwähnt, sollten Sie die Zuordnungsbewertung jeder Option verwenden und die Option mit der zweitrangigen Bewertung verwenden. Um zu bestimmen, welches Feature oder welche ParameterInit geändert werden soll, können Sie eine private Eigenschaft definieren, die der Client dem PrintTicket hinzufügen kann. Diese Eigenschaft kann eine Priorität für Feature- und ParameterInit-Instanzen definieren, sodass der Konfliktlöserprozess darüber informiert wird, welche Feature- oder ParameterInit-Instanzen für den Client wichtig sind (und im PrintTicket beibehalten werden müssen) und welche weniger wichtig sind.

14. Wenn der Einschränkungsauflösungsprozess Änderungen im PrintTicket an parameterRef-Instanzen verursacht hat, für die die mandatory-Eigenschaft auf Conditional festgelegt ist, fügen Sie ParameterInit-Instanzen mit Standardwerten für die jetzt angezeigten Hinzufügewerte hinzu, und entfernen Sie alle ParameterInit-Instanzen für eine ParameterRef-Instanz, die nicht mehr angezeigt wird.

15. Entfernen Sie alle Eigenschafteninstanzen und deren Inhalte, die in Optionsinstanzen im PrintTicket angezeigt werden. Eigenschaftselemente haben keine Rolle im PrintTicket. Wenn die überprüfte Option für ein bestimmtes Feature perfekt mit der vorvalidierten Option übereinstimmt, übertragen Sie alle Eigenschafteninstanzen in dieser Option von der Vorabvalidierung PrintTicket an das jetzt überprüfte PrintTicket. Dies unterliegt der Bedingung, dass Namespaces von Eigenschafteninstanzen im PrintCapabilities-Dokument registriert werden. Beachten Sie, dass für zwei Optionsinstanzen, die als perfekte Übereinstimmung betrachtet werden, für jede ScoredProperty in einer Option eine entsprechende ScoredProperty in der anderen Option vorhanden sein muss, und die Werte beider ScoredProperty-Instanzen müssen identisch sein.

16. Wenn Ihr PrintTicket-Anbieter private oder öffentliche Property-Instanzen erkennt und unterstützt, die bis zu diesem Zeitpunkt noch vorhanden sind, führen Sie die Überprüfung für diese instanzen durch. Löschen Sie eine Eigenschaft zu diesem Zeitpunkt nicht, nur weil Sie sie nicht erkennen. Sie kann für eine andere Phase der Dokumentverarbeitung vorgesehen sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



