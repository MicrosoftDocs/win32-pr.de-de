---
description: Erfahren Sie mehr über Optionsdefinitionen im PrintCapabilities-Schema. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: e81068db-ab8e-420c-a0be-93bc92f3df6f
title: Optionsdefinitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f71f4201bb9bd38860a79fead7fd3e8738429fc34b729981af68c0d2d1f38d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098954"
---
# <a name="option-definitions"></a>Optionsdefinitionen

Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)

Der wichtigste Aspekt beim Definieren einer Option besteht darin, dies so zu tun, dass sie sinnvoll mit anderen Optionsinstanzen verglichen werden kann, die im selben Feature enthalten sind. Der Vergleich muss sinnvoll sein, da die Option-Instanz verwendet wird, um die Konfiguration nicht nur des Geräts, sondern auch des Auftrags zu definieren, unabhängig vom Gerät oder PrintCapabilities, das zum Erstellen der Konfiguration verwendet wurde. Die anderen Optionsinstanzen im Feature können entweder im gleichen PrintCapabilities-Dokument oder in einem anderen PrintCapabilities-Dokument angezeigt werden, das ein anderes Gerät darstellt, ein PrintCapabilities-Dokument, das von einer anderen Unabhängigen definiert wird. Nachdem ein Client die Gerätekonfiguration ausgewählt hat, die zum Rendern eines Auftrags oder Dokuments verwendet werden soll, wird diese Konfiguration in der Regel zusammen mit dem Auftrag oder Dokument in Form eines PrintTickets gespeichert. PrintTicket enthält eine Reihe von Optionsinstanzen, in der Regel eine für jedes Feature, das im PrintCapabilities-Dokument definiert ist. Optionsinstanzen müssen portabel sein und die Druckabsicht beibehalten, damit die Absicht kommuniziert werden kann, wenn dieses PrintTicket an ein anderes Gerät übermittelt wird, selbst wenn es ein anderes PrintCapabilities-Dokument enthält, das von einem anderen Autor geschrieben wurde. Der Hauptvorteil dieser Portabilität besteht darin, dass der Gerätetreiber oder das Subsystem in der Lage ist, die Option zu identifizieren und auszuwählen, die der Funktionalität am nächsten liegt, wenn ein anderes Gerät eine im PrintTicket enthaltene Option nicht ausdrücklich unterstützt.

Eine der wichtigsten PrintTicket-Funktionen des Treibers besteht in der Identifizierung der Geräteoption im PrintCapabilities-Dokument, die einer bestimmten Option am besten entspricht, die im PrintTicket aufgeführt ist. Während dieses Abgleichs- oder Gerätetreiber-definierten Bewertungsprozesses wird  die Option im PrintTicket als Referenzoption bezeichnet, während die Option im PrintCapabilities-Dokument als Kandidatenoption *bezeichnet* wird. Die allgemeine Abgleichsmetrik ist die Anzahl der übereinstimmenden ScoredProperty-Instanzen in den Kandidaten- und Referenzoptionsinstanzen. Eine größere Anzahl von Übereinstimmungen weist in der Regel auf eine bessere Aufrechterhaltung der Druckabsicht hin. In Ihrem Bewertungsprozess können Sie einige ScoredProperty-Elemente stärker gewichten als anderen.

Sie können Option-Instanzen portabel machen, indem Sie sicherstellen, dass alle Option-Instanzen, die zum gleichen Feature gehören, mindestens ein ScoredProperty-Element *gemeinsam haben.* Dies bedeutet, dass es eine Reihe von ScoredProperty-Elementen gibt, die in jeder Option-Instanz (die zum gleichen Feature gehört) angezeigt werden. Beispielsweise können Optionsinstanzen für das PageMediaSize-Feature portabel sein, wenn jede Option-Instanz ScoredProperty-Elemente enthält, die die systeminternen PageMediaSize-Eigenschaften definieren: MediaSizeWidth und MediaSizeHeight. Der Gerätetreiber- oder Subsystemcode kann dann bestimmen, wie genau zwei Optionsinstanzen sich einigen, indem die Unterschiede in diesen ScoredProperty-Werten verglichen werden. Wenn im PrintCapabilities-Dokument keine Option angezeigt wird, die genau mit der Option im PrintTicket-Ticket übereinstimmen soll, kann der Gerätetreiber die Option mit den am ehesten übereinstimmenden Mediendimensionen leicht bestimmen und auswählen.

Zwei -Objekte (in diesem Fall Optionsinstanzen) werden als gemeinsame Elemente bezeichnet oder verfügen entsprechend über entsprechende *Elemente,* wenn die folgenden drei Bedingungen erfüllt sind. 

1.  Die beiden Elemente sind vom gleichen Elementtyp.

2.  Die Namensattribute der beiden Elemente sind identisch (oder kein Element enthält ein Namensattribut).

3.  Die Kette der verketteten Elemente der verglichenen Elemente bis zu den beiden zu berücksichtigenden Objekten muss die Bedingungen 1 und 2 erfüllen.

Stellen Sie sich beispielsweise eine Situation vor, in der es zwei Optionsinstanzen gibt, bei denen jede eine ScoredProperty-Instanz enthält und jede dieser ScoredProperty-Instanzen eine Property-Instanz enthält. Die erste Bedingung ist eindeutig erfüllt (die beiden Property-Instanzen sind vom gleichen Typ), und ein Teil der dritten Bedingung ist erfüllt (die über-Elemente der Property-Instanzen sind der gleiche Typ, ScoredProperty, und die über-elemente sind die Option-Instanzen, die ebenfalls vom gleichen Typ sind). Wenn die Namensattribute der Property-Instanzen, der ScoredProperty-Instanzen und der Option-Instanzen entweder identisch oder nicht angegeben sind, haben die beiden Option-Instanzen gemeinsame Elemente.

Der erste Schritt beim Erstellen von Option-Instanzen besteht im Definieren einer Reihe von ScoredProperty-Elementen, die in den meisten oder allen Optionsinstanzen vorhanden sind. Wenn Ihr Gerätekonfigurationsattribut durch ein Standardfeature dargestellt werden kann (das unter Druckschemaschlüsselwörter aufgeführt ist), beachten Sie die ScoredProperty-Elemente, die in den Standardoptionsinstanzen gemeinsam sind. Sie sollten sicherstellen, dass alle neuen Option-Instanzen, die Sie einführen, auch diese ScoredProperty-Elemente enthalten. Sie können nach Bedarf jederzeit zusätzliche ScoredProperty-Elemente hinzufügen, um Ihre Optionsinstanzen von den Standardoptionsinstanzen zu unterscheiden. Sie können sogar eines oder mehrere der ScoredProperty-Elemente gemeinsam löschen, wenn es einen guten Grund gibt, obwohl dies die Portabilität einer solchen Option verringert. Natürlich empfehlen Portabilitätsüberlegungen die Verwendung der unveränderten Standardoptionsinstanzen, es sei denn, es gibt einen intrinsischen Unterschied zwischen Ihrer Option und der Standardoptionsinstanz, die in der neuen Option-Instanz widergespiegelt werden muss.

Das folgende Beispiel veranschaulicht eine Situation, in der Sie einer Option-Instanz möglicherweise ein ScoredProperty-Element hinzufügen möchten. Alle Standardinstanzen von Option für das PageMediaSize-Feature haben die Elemente MediaSizeWidth und MediaSizeHeight ScoredProperty gemeinsam. Angenommen, Ihr Gerät kann eine der standardmäßigen Letter-Mediengrößen unterstützen, indem es das Papier entweder transversal (LongEdgeFirst) oder gediehen (ShortEdgeFirst) einfängt. Unter der Annahme, dass Sie keine neue Feedrichtungsfunktion einführen möchten, um diesen Freiheitsgrad verfügbar zu machen, können Sie stattdessen die beiden PageMediaSize-Optionsinstanzen für Letter ändern, um die Papierfeedausrichtung zu integrieren. Beginnen Sie für diese beiden Letter Option-Instanzen mit der PageMediaSize-Standardoptionsinstanz, und fügen Sie ein neues ScoredProperty-Element hinzu, das feedDirection repräsentiert. Legen Sie in einer Optionsinstanz feedDirection ScoredProperty auf LongEdgeFirst fest. Legen Sie in der anderen Option-Instanz FeedDirection auf ShortEdgeFirst fest. Beachten Sie, dass diese neuen Option-Instanzen ihre Portabilität merken. Wenn die Option letter, ShortEdgeFirst in einem PrintTicket gespeichert wird und ein anderes Gerät, das nur die Letter-Standardoption unterstützt, ausgewählt ist, um den Auftrag zu rendern, kann der Optionsabgleichscode schnell feststellen, dass der Standardoptionsbuchstaben die beste Übereinstimmung mit dem Optionsbuchstaben ShortEdgeFirst ist. Dies ist die beste Übereinstimmung, da alle ScoredProperty-Instanzen übereinstimmen, mit Ausnahme der FeedDirection ScoredProperty, die in der Standardoption Letter nicht vorhanden ist.

Es kann auch fälle geben, in denen die Änderungen an der Option die Bedeutung so stark ändern, dass die geänderte Option nicht mehr als spezieller Fall des Originals betrachtet werden kann. In solchen Fällen sollten Sie den Namen der Option ändern, um den Unterschied zwischen der geänderten Option-Instanz und der unveränderten Instanz widerzu spiegeln. Nur der Autor des PrintCapabilities-Dokuments für ein bestimmtes Gerät kann entscheiden, ob sich die vom Gerät angebotene Option ausreichend von einer Standardoptionsinstanz unterscheidet, um eine inkompatible Definition zu garantieren.

Betrachten Sie nun den Fall, dass Ihr Gerät über ein Gerätekonfigurationsattribut verfügt, das keinem der Standardfunktionsinstanzen entspricht. In diesem Fall können Sie sich nicht darauf verlassen, dass die Standardinstanzen von Option die Liste der Gemeinsamen ScoredProperty-Elemente bereitstellen. Wenn Sie eine ScoredProperty-Instanz erstellen, besteht Ihr Hauptziel darin, jede Option von den anderen Optionen im Feature zu unterscheiden und zu beschreiben, warum ein Benutzer eine Option gegenüber einer anderen auswählen würde. Die Baseline besteht in der Charakterisierung jeder Option mit einem eindeutigen Namensattribut, und die ScoredProperty, die das Namensattribut enthält, wird zum Attribut, das zum Bestimmen gemeinsamer Elemente verwendet wird.

Nachdem eine Reihe gemeinsamer ScoredProperty-Elemente eingerichtet wurde, ist es einfach, jeder ScoredProperty geeignete Werte zu zuweisen, um jede Option zu erstellen. Wie im vorherigen Beispiel müssen Sie für bestimmte Optionsinstanzen möglicherweise zusätzliche ScoredProperty-Instanzen hinzufügen oder einige der gemeinsamen Elemente löschen, um eine entsprechende Option-Instanz zu erstellen.

Beachten Sie, dass das Druckschema erfordert, dass der Satz von ScoredProperty-Instanzen, ihre Speicherorte und die Werte, die jeder ScoredProperty in einer Option zugewiesen sind, unabhängig von der Konfiguration konstant bleiben müssen. Das gesamte Konzept des Druckschemas basiert darauf, dass Optionsinstanzen feste, identifizierbare Property- und ScoredProperty-Instanzen haben, die von vielen Geräten gemeinsam genutzt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezifikation des Druckschemas](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



