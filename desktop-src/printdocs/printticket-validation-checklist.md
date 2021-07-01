---
description: Überprüfen Sie die Prüfliste für die PrintTicket-Überprüfung. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 4698f151-2237-4d16-b32f-4d15024cd063
title: Prüfliste für die PrintTicket-Überprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6154b7cabb5825a0f0edcc8f90b8294557001f1a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120145"
---
# <a name="printticket-validation-checklist"></a>Prüfliste für die PrintTicket-Überprüfung

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

PrintTicket-Anbieter müssen das PrintTicket überprüfen, bevor es für einen beliebigen Zweck verwendet wird. Nachdem das PrintTicket überprüft wurde, kann es an den Client zurückgegeben oder nach der Verwendung verworfen werden. In dieser Prüfliste werden die Aufgaben behandelt, die der Anbieter während der Validierung ausführen muss. Der Überprüfungsprozess ändert häufig den Inhalt von PrintTicket, obwohl er kein zuvor überprüftes PrintTicket ändert.

Die Validierung wird immer für ein bestimmtes Gerät ausgeführt, für das in einem PrintCapabilities-Dokument eine Reihe von Feature-, Options- und ParameterDef-Instanzen definiert ist. Der Validierungscode sollte Zugriff auf die Funktionsinstanzen (und die enthaltenen Optionsinstanzen) und ParameterDef-Instanzen für das spezifische Gerät haben und nicht auf PrintCapabilities zugreifen müssen. Die Informationen aus den Instanzen Feature, Option und ParameterDef werden in bestimmten Teilen des Überprüfungsprozesses benötigt.

1.  Beachten Sie bei versuchen, entsprechende oder übereinstimmende Elemente zu finden, dass die Namespaces der Elemente übereinstimmen müssen, bevor ein qualifizierter Name als Übereinstimmung betrachtet werden kann. Alle Elementnamen, Attributnamen und Instanznamen sind namespacequalifiziert. Bei geschachtelten Elementen müssen ihre Positionen übereinstimmen, bevor die Elemente als Übereinstimmung betrachtet werden.

2.  Stellen Sie sicher, dass sich alle Elementtags im öffentlichen Namespace befinden, durch das PrintTicket-Schema definiert sind, die richtigen XML-Attribute und Attributwerte enthalten und ob der Speicherort jedes Elementtyps der vom PrintTicket-Schema definierten Verwendung entspricht.

3.  Bestimmen Sie alle Namespaces, die vom PrintCapabilities-Dokument gemeldet werden. Entfernen Sie alle Elemente (und deren Nachfolger) aus dem PrintTicket, deren Instanznamen zu Namespaces gehören, die nicht vom PrintCapabilities-Dokument gemeldet werden. Beachten Sie den Unterschied zwischen diesem Fall und dem folgenden Fall, der nicht bekannte Instanznamen in einem bekannten Namespace umfasst.

4.  Aufgrund der Tatsache, dass die Schemas ständig durch das Hinzufügen neuer Elementinstanzdefinitionen erweitert werden, sollte der Validierungscode nicht unter der Annahme geschrieben werden, dass jeder Instanzname in einem bestimmten Namespace bekannt ist. Der Validierungscode kann nicht erkennende Instanznamen in einem bekannten Namespace nicht als Fehler behandeln und auch nicht aus dem PrintTicket löschen.

5.  Wenn eine Elementinstanz über ein doppeltes gleichgeordnetes Element verfügt, das vom PrintTicket-Schema nicht zugelassen wird, behalten Sie nur das erste Vorkommen bei, und löschen Sie die Duplikate, einschließlich des Inhalts des duplizierten Elements.

6.  Entfernen Sie alle Funktionen oder Unterfeatures (und alle untergeordneten Funktionen) aus PrintTicket, die im PrintCapabilities-Dokument kein entsprechendes Feature haben.

7.  Überprüfen Sie die im PrintCapabilities-Dokument definierte SelectionType-Eigenschaft für jede der verbleibenden Feature-Instanzen im PrintTicket. Jede Funktion, deren SelectionType-Eigenschaft auf PickOne festgelegt ist, muss genau eine Option-Instanz im PrintTicket haben, während ein Feature, dessen SelectionType-Eigenschaft PickMany ist, möglicherweise mehr als eine Instanz hat. Wenn ein PrintTicket-Feature über keine Option-Instanz verfügt, geben Sie die Standardoptionsinstanz an. Da Sie der Anbieter sind, wissen Sie, welche Option die Standardoption für jedes Feature ist.

    Stellen Sie für ein Feature, dessen SelectionType-Eigenschaft PickMany ist, mit mehr als einer Option, die im PrintTicket ausgewählt ist, sicher, dass keine Option als IdentityOption festgelegt ist. Wenn dies der Dert ist, löschen Sie alle anderen Optionen, und lassen Sie nur die designierte IdentityOption."

8.  Entfernen Sie alle ParameterInit-Instanzen im PrintTicket, die keine entsprechende ParameterDef-Instanz im PrintCapabilities-Dokument enthält.

    Stellen Sie für alle anderen ParameterInit-Instanzen im PrintTicket sicher, dass der Wert für jede der ParameterDef-Instanz des PrintCapabilities-Dokuments entspricht. Wenn ein Wert fehlt, geben Sie den Standardwert an, der in der ParameterDef bereitgestellt wird.

9.  Koppeln Sie jede Optionsinstanz im PrintTicket mit einer Option, die im entsprechenden Feature im PrintCapabilities-Dokument aufgeführt ist, basierend auf den Ergebnissen des Bewertungsprozesses. Die Bewertung ist der Prozess, bei dem die Option im PrintCapabilities-Dokument findet, die am besten mit der Option im PrintTicket-Dokument entspricht. Eine Beschreibung, was während des Bewertungsprozesses berücksichtigt wird, finden Sie unter [Optionsdefinitionen.](option-definitions.md) Ersetzen Sie jede Referenzoption im PrintTicket durch die entsprechende PrintCapabilities-Dokumentoption für den besten Übereinstimmenden Kandidaten. Sie können auch alle Kandidaten nach Bewertung einstufen und diese Informationen an die Auflösungsphase übergeben, falls ein Einschränkungskonflikt verhindert, dass der beste übereinstimmende Kandidat verwendet wird. In solchen Fällen kann der Auflösungsprozess den zweitbesten Kandidaten verwenden, anstatt einen anderen Kandidaten nach dem Zufallsprinzip zu wählen.

10. Stellen Sie für ein Feature, dessen SelectionType-Eigenschaft auf PickMany festgelegt ist und für das im PrintTicket mehrere Optionen ausgewählt sind, sicher, dass keine Option als IdentityOption festgelegt ist. Wenn eine solche Option vorhanden ist, löschen Sie alle anderen Optionen, und lassen Sie nur die designierte IdentityOption." Dieser Schritt muss vor und nach anwendung des Bewertungsprozesses ausgeführt werden.

    Der Grund dafür, dass dieser Schritt zweimal ausgeführt werden muss, ist, dass der Bewertungsprozess mehrere Referenzinstanzen der Option demselben Kandidaten zuordnen kann. Löschen Sie in diesem Fall alle doppelten Optionsinstanzen, damit die für ein bestimmtes PickMany-Feature aufgeführten Optionen eindeutig sind.

11. Fügen Sie printTicket ein beliebiges Feature hinzu, das im PrintCapabilities-Dokument vorhanden ist und nicht im PrintTicket angezeigt wird. Geben Sie für ein solches Feature die Standardoption als ausgewählte Option an.

12. Bestimmen Sie, ob ParameterDef-Instanzen verwendet werden, die alle der folgenden Kriterien erfüllen:

    -   Die ParameterDef-Instanz wird im PrintCapabilities-Dokument, aber nicht im PrintTicket angezeigt.

    -   Die Mandatory-Eigenschaft der ParameterDef-Instanz ist entweder auf "Bedingungslos" oder "Bedingt" festgelegt.

    -   Auf die ParameterDef-Instanz wird von einer ParameterRef-Instanz im PrintTicket innerhalb einer Optionsinstanz verwiesen.

    Fügen Sie für jede dieser ParameterDef-Instanzen im PrintCapabilities-Dokument dem PrintTicket eine entsprechende ParameterInit-Instanz hinzu. Legen Sie den Wert der neu hinzugefügten ParameterInit-Instanzen auf den Standardwert fest, der von den entsprechenden ParameterDef-Instanzen angegeben wird.

13. Führen Sie die Einschränkungskonflikterkennung durch, und ändern Sie die Konfiguration, um solche Konflikte zu vermeiden. In diesem Thema wird kein bestimmter Prozess definiert, der zum Lösen von Einschränkungskonflikten verwendet werden soll. Sie müssen entscheiden, welche Feature- oder ParameterInit-Instanz geändert werden kann, und eine geeignete Option bzw. einen entsprechenden Wert auswählen, die die geringsten Auswirkungen auf die Gesamtabsicht der im PrintTicket angegebenen Konfiguration hat. Wie bereits erwähnt, möchten Sie möglicherweise die Zuordnungswertung jeder Option und die Option mit der zweit höchsten Bewertung verwenden. Um zu bestimmen, welches Feature oder ParameterInit geändert werden soll, sollten Sie eine private Eigenschaft definieren, die der Client dem PrintTicket hinzufügen kann. Diese Eigenschaft kann eine Priorität für Feature- und ParameterInit-Instanzen definieren, sodass der Konfliktlöserprozess darüber informiert wird, welche Feature- oder ParameterInit-Instanzen für den Client wichtig sind (und im PrintTicket beibehalten werden müssen) und welche weniger wichtig sind.

14. Wenn der Einschränkungsauflösungsprozess Änderungen im PrintTicket an allen ParameterRef-Instanzen verursacht hat, für die die Mandatory-Eigenschaft auf Bedingt festgelegt ist, fügen Sie ParameterInit-Instanzen mit Standardwerten für die jetzt angezeigten hinzu, und entfernen Sie alle ParameterInit-Instanzen für eine ParameterRef-Instanz, die nicht mehr angezeigt wird.

15. Entfernen Sie alle Property-Instanzen und deren Inhalt, die in Option-Instanzen im PrintTicket angezeigt werden. Eigenschaftselemente haben keine Rolle in PrintTicket. Wenn die überprüfte Option für ein bestimmtes Feature der vorvalidierten Option perfekt entspricht, übertragen Sie alle Property-Instanzen in dieser Option von der Vorabvalidierung PrintTicket in das jetzt überprüfte PrintTicket, sofern Namespaces von Property-Instanzen im PrintCapabilities-Dokument registriert sind. Beachten Sie, dass für zwei Optionsinstanzen, die als perfekte Übereinstimmung betrachtet werden, für jede ScoredProperty, die in einer Option gefunden wird, eine entsprechende ScoredProperty in der anderen Option enthalten sein muss, und die Werte beider ScoredProperty-Instanzen müssen identisch sein.

16. Wenn Ihr PrintTicket-Anbieter private oder öffentliche Eigenschafteninstanzen erkennt und unterstützt, die bis zu diesem Zeitpunkt erhalten sind, führen Sie eine Validierung für diese durch. Löschen Sie eine Eigenschaft an diesem Punkt nicht, nur weil Sie sie nicht erkennen. Sie ist möglicherweise für eine andere Phase der Dokumentverarbeitung vorgesehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



