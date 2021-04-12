---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: e81068db-ab8e-420c-a0be-93bc92f3df6f
title: Options Definitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10016b295cc2da7ede4e6a4f8944f279a25f6f9b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219081"
---
# <a name="option-definitions"></a>Options Definitionen

Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Der wichtigste Aspekt beim Definieren einer Option ist, dies so zu tun, dass es im Vergleich zu anderen Options Instanzen, die in der gleichen Funktion enthalten sind, sinnvoll sein kann. Der Vergleich muss sinnvoll sein, da die Options Instanz verwendet wird, um die Konfiguration nicht nur des Geräts, sondern des Auftrags, unabhängig von dem Gerät oder den Print-Funktionen zu definieren, die zum Erstellen der Konfiguration verwendet wurden. Die anderen Options Instanzen in der Funktion können entweder im gleichen Printworks-Dokument oder in einem anderen printfunktionalitäten-Dokument, das ein anderes Gerät darstellt, angezeigt werden, einem printfunktionalitäten-Dokument, das von einer anderen Partei unabhängig voneinander definiert wird. Nachdem ein Client die Gerätekonfiguration ausgewählt hat, die zum Renderingvorgang eines Auftrags oder Dokuments verwendet werden soll, wird diese Konfiguration in der Regel zusammen mit dem Auftrag oder Dokument in Form eines PrintTicket gespeichert. Das PrintTicket enthält eine Reihe von Options Instanzen, die in der Regel eine für jede im printfunktionalitäten-Dokument definierte Funktion sind. Options Instanzen müssen portabel sein und die Druck Absicht beibehalten, damit die Absicht kommuniziert werden kann, wenn dieses PrintTicket einem anderen Gerät zugewiesen wird. Dies gilt auch für einen, der über ein anderes printfunktionalitäten-Dokument verfügt, das von einem anderen Autor geschrieben wurde. Der Hauptvorteil dieser Portabilität besteht darin, dass der Gerätetreiber oder das Subsystem, wenn ein anderes Gerät nicht explizit eine Option unterstützt, die in PrintTicket enthalten ist, die Option identifizieren und auswählen kann, die der nächstgelegenen Funktionalität entspricht.

Eine der Hauptfunktionen von PrintTicket des Treibers ist die Identifizierung der Geräte Option im printfunctions-Dokument, das mit einer bestimmten im PrintTicket aufgelisteten Option am ehesten übereinstimmt. Während dieses Vergleichs-oder Gerätetreiber definierten Bewertungsprozesses wird die-Option in PrintTicket als *Verweis* Option bezeichnet, während die-Option im printfunktionalitäten-Dokument als *Candidate* -Option bezeichnet wird. Bei der Allgemeinen übereinstimmenden Metrik handelt es sich um die Anzahl der übereinstimmenden ScoredProperty-Instanzen in den Instanzen Candidate und Reference eine größere Anzahl von Übereinstimmungen deutet normalerweise auf eine bessere Beibehaltung der Druck Absicht hin. In Ihrem Bewertungsprozess können Sie für einige ScoredProperty-Elemente eine höhere Gewichtung als für andere Elemente festlegen.

Sie können Options Instanzen portabel machen, indem Sie sicherstellen, dass alle Options Instanzen, die zur gleichen Funktion gehören, ein oder mehrere ScoredProperty- *Elemente* aufweisen. Dies bedeutet, dass es eine Reihe von ScoredProperty-Elementen gibt, die in jeder Options Instanz (die zur gleichen Funktion gehört) angezeigt werden. Beispielsweise können Options Instanzen für das PageMediaSize-Feature portabel sein, wenn jede Options Instanz ScoredProperty-Elemente enthält, die die systeminternen PageMediaSize-Eigenschaften definieren: mediasizewidth und mediasizeheight. Der Gerätetreiber oder Subsystem-Code kann dann ermitteln, wie genau zwei Options Instanzen zustimmen, indem die Unterschiede in diesen ScoredProperty-Werten verglichen werden. Wenn im Printworks-Dokument keine Option vorhanden ist, die genau mit der in PrintTicket übereinstimmt, kann der Gerätetreiber die Option mit den nächstgelegenen übereinstimmenden Medien Dimensionen problemlos ermitteln und auswählen.

Zwei-Objekte (in diesem Fall die Options Instanzen) werden als *Elemente* bezeichnet, die die *entsprechenden Elemente* aufweisen, wenn die folgenden drei Bedingungen erfüllt sind.

1.  Die beiden-Elemente weisen denselben Elementtyp auf.

2.  Die namens Attribute der beiden Elemente sind identisch (oder keines der Elemente enthält ein Name-Attribut).

3.  Die Kette der übergeordneten Elemente der zu vergleichenden Elemente, die über die beiden zu berücksichtigenden Objekte hinausgeht, muss die Bedingungen 1 und 2 erfüllen.

Stellen Sie sich z. b. eine Situation vor, in der zwei Options Instanzen vorhanden sind, die jeweils eine ScoredProperty-Instanz enthalten, und jede dieser ScoredProperty-Instanzen eine Eigenschaften Instanz enthält. Die erste Bedingung ist eindeutig (die beiden Eigenschaften Instanzen sind derselbe Typ), und ein Teil der dritten Bedingung ist erfüllt (die übergeordneten Elemente der Eigenschaften Instanzen sind derselbe Typ, ScoredProperty, und die übergeordneten Elemente dieser Elemente sind die Options Instanzen, die ebenfalls denselben Typ aufweisen). Wenn die namens Attribute von bzw. die Eigenschaften Instanzen, die ScoredProperty-Instanzen und die Options Instanzen entweder identisch sind oder nicht angegeben werden, verfügen die beiden Options Instanzen über gemeinsame Elemente.

Der erste Schritt beim Erstellen von Options Instanzen besteht darin, einen Satz von ScoredProperty-Elementen zu definieren, die in den meisten oder allen Options Instanzen vorhanden sind. Wenn Ihr Geräte Konfigurations Attribut durch ein Standard Feature (in den Schlüsselwörtern des Print-Schemas aufgelistet) dargestellt werden kann, notieren Sie sich die in den Standard Options Instanzen gemeinsamen ScoredProperty-Elemente. Stellen Sie sicher, dass alle neuen Options Instanzen, die Sie einführen, auch diese ScoredProperty-Elemente enthalten. Sie können jederzeit weitere ScoredProperty-Elemente hinzufügen, um die Options Instanzen von den Standard Options Instanzen zu unterscheiden. Sie können sogar ein oder mehrere der ScoredProperty-Elemente in Common löschen, wenn es einen guten Grund gibt, obwohl dadurch die Portabilität einer solchen Option verringert wird. Natürlich empfehlen Portabilitäts Überlegungen die Verwendung der nicht geänderten Standard Options Instanzen, es sei denn, es gibt einen intrinsischen Unterschied zwischen Ihrer Option und der standardmäßigen Options Instanz, die in der neuen Options Instanz reflektiert werden muss.

Das folgende Beispiel veranschaulicht eine Situation, für die Sie möglicherweise ein ScoredProperty-Element zu einer Options Instanz hinzufügen möchten. Alle Instanzen der Standard Option für die PageMediaSize-Funktion haben die Elemente "mediasizewidth" und "mediasizeheight ScoredProperty" gemeinsam. Angenommen, Ihr Gerät kann eine der Standardgrößen für Großbuchstaben unterstützen, indem das Papier entweder quer (longedgefirst) oder quer (shortedgefirst) durch tragen wird. Wenn Sie nicht möchten, dass Sie eine neue Funktion für die Funktion "Feed" einführen, um diesen Freiheitsgrad verfügbar zu machen, können Sie stattdessen die zwei PageMediaSize-Options Instanzen für "Letter" so ändern, dass Sie die Ausrichtung des Papier Feeds enthalten. Beginnen Sie für diese zwei Buchstaben Options Instanzen mit der standardmäßigen PageMediaSize-Options Instanz, und fügen Sie ein neues ScoredProperty-Element hinzu, das die feeddirection darstellt. Legen Sie in einer Options Instanz die "feeddirection ScoredProperty" auf "longedgefirst;" fest. Legen Sie in der anderen Options Instanz für feeddirection den Wert shortedgefirst fest. Beachten Sie, dass diese neuen Options Instanzen ihre Portabilität beibehalten. Wenn die Option Letter, shortedgefirst, in einem PrintTicket gespeichert wird, und ein anderes Gerät, das nur die Option Letter Standard unterstützt, zum Renderingvorgang ausgewählt ist, kann der Option-Match-Code schnell feststellen, dass der standardmäßige Options Buchstabe die beste Übereinstimmung mit dem Options Buchstaben, shortedgefirst, ist. Die beste Übereinstimmung ist, dass alle ScoredProperty-Instanzen mit Ausnahme von "feeddirection ScoredProperty" übereinstimmen, die in der Option "Letter Standard" nicht vorhanden ist.

Es können auch Fälle auftreten, in denen die Änderungen an der-Option tatsächlich die Bedeutung ändern, sodass die geänderte Option nicht mehr als spezieller Fall des Originals betrachtet werden kann. In solchen Fällen sollten Sie den Namen der Option ändern, um den Unterschied zwischen der geänderten Options Instanz und der nicht geänderten Option widerzuspiegeln. Nur der Autor des Printworks-Dokuments für ein bestimmtes Gerät kann entscheiden, ob die vom Gerät angebotene Option ausreichend von einer Standard Options Instanz abweicht, um eine nicht kompatible Definition zu gewährleisten.

Beachten Sie nun den Fall, in dem das Gerät über ein Geräte Konfigurations Attribut verfügt, das keiner der Standard Funktions Instanzen entspricht. In diesem Fall können Sie nicht auf die Standard Options Instanzen zurückgreifen, um die Liste der allgemeinen ScoredProperty-Elemente anzugeben. Wenn Sie eine ScoredProperty-Instanz erstellen, besteht das Hauptziel darin, die einzelnen Optionen von den anderen in der Funktion zu unterscheiden und zu beschreiben, warum ein Benutzer eine Option für einen anderen Benutzer ausgewählt hat. Die Baseline besteht darin, jede Option mit einem eindeutigen Namensattribut zu charakterisieren, und die ScoredProperty, die das Name-Attribut enthält, wird zur Bestimmung der allgemeinen Elemente verwendet.

Nachdem eine Reihe von ScoredProperty-Elementen festgelegt wurde, ist es eine einfache Sache, jeder ScoredProperty geeignete Werte zuzuweisen, um die einzelnen Optionen zu erstellen. Wie im vorherigen Beispiel müssen Sie für bestimmte Options Instanzen möglicherweise weitere ScoredProperty-Instanzen hinzufügen oder einige der allgemeinen Elemente löschen, um eine entsprechende Options Instanz zu erstellen.

Beachten Sie, dass das Druck Schema erfordert, dass der Satz der ScoredProperty-Instanzen, ihre Speicherorte und die Werte, die den einzelnen ScoredProperty in einer Option zugewiesen sind, unabhängig von der Konfiguration konstant bleiben müssen. Das gesamte Konzept des Druck Schemas basiert auf Options Instanzen, die über eine festgelegte, identifizierbare Eigenschaft und ScoredProperty-Instanzen verfügen, die von vielen Geräten gemeinsam genutzt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Druck Schema Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



