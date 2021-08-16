---
title: Auswirkungen auf Directory-Enabled Anwendungen
description: In diesem Thema werden die Auswirkungen auf verzeichnisfähige Anwendungen beschrieben, wenn Versionsverstöße, Teilupdates oder Kollisionen auftreten.
ms.assetid: 0aec6fe3-7757-4472-bc18-add2327d4e1b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601a5bbffda08f0789875176193977cbecfc34596a9900c870f81cfd677b9ef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187675"
---
# <a name="impact-on-directory-enabled-applications"></a>Auswirkungen auf Directory-Enabled Anwendungen

## <a name="version-skew"></a>Versionsgefäussung

Eine Versionsänderung tritt auf, wenn Anwendungen dieselben Objekte aus verschiedenen Replikaten lesen, bevor eine Änderung repliziert wurde. Anwendungen, die das Remotereplikat lesen, erkennen das unveränderte Objekt. Versionsversatz ist ein Problem, wenn eine bestimmte Anwendung oder gruppe von Anwendungen die Daten im Verzeichnis für die Zusammenarbeit verwendet.

Beispielsweise kann ein RPC-Dienst seine Endpunkte im Verzeichnis mithilfe von RPC-Standard-APIs (z. B. [**RpcNsBindingExport) veröffentlichen.**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) Clients stellen eine Verbindung mit dem Dienst auf, indem sie den gewünschten Endpunkt im Verzeichnis suchen [**(RpcNsBindingLookupBegin,**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) [**RpcNsBindingLookupNext,**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)und so weiter) und eine Bindung an den Dienst herstellen.

Angenommen, ein RPC-₁ veröffentlicht den Endpunkt Es₁ und wechselt anschließend auf einen anderen Computer. Der ursprüngliche Endpunkt Es₁ wird in E<sub>s2 geändert, was</sub> die Adresse des neuen Computers wiederspiegelt. Clients, die Remotereplikate des Verzeichnisdiensts lesen, können erst dann eine Verbindung mit dem Dienst herstellen, wenn der aktualisierte Endpunkt repliziert wurde. Das Verschieben eines Diensts von einem Computer auf einen anderen ist jedoch selten. Daher sollte diese Unterbrechung/Verzögerung selten auftreten, insbesondere wenn die Verschiebung des Diensts gut geplant ist.

## <a name="partial-updates"></a>Teilupdates

Im Allgemeinen erfolgt eine teilielle Aktualisierung, wenn eine Anwendung einen Satz von Daten liest, während eine andere Anwendung in denselben Satz von Daten schreibt. Dies ist eine Situation, die bei jeder Anwendung in einem Multimastersystem auftreten kann. Es gibt viele Möglichkeiten, wie dies passieren kann. Sie können mehrere Anwendungen gleichzeitig in dasselbe DataSet schreiben. Wenn Sie dies auf diese Weise betrachten, ist der Verzeichnisreplikationsdienst nur eine andere Anwendung, die möglicherweise in das gleiche DataSet schreibt, das eine andere Anwendung möglicherweise liest. Dies kann ein potenzielles Problem für eine Anwendung sein. Das Zeitfenster, in dem sich ein teilielles Update auf Ihre Anwendung auswirken kann, ist jedoch relativ klein. Dies sollte selten, wenn überhaupt, ein Problem für Anwendungen sein, die nicht von der Synchronisierung mehrerer Objekte abhängig sind. Wenn Ihre Anwendung stark von der Synchronisierung eines zugehörigen Sets von Objekten abhängig ist, sollten Sie die Auswirkungen einer partiellen Aktualisierung im Anwendungsentwurf berücksichtigen.

Im Hinblick auf die Verzeichnisreplikation erfolgt eine teilielle Aktualisierung, wenn Anwendungen denselben Satz von Objekten aus verschiedenen Replikaten lesen, während die Replikation läuft. Anwendungen auf dem Remotereplikat sehen einige, aber nicht alle Änderungen.

> [!Note]  
> Das Fenster, in dem sich ein teilielles Update auf eine Anwendung auswirken kann, ist klein: Die Anwendung muss mit dem Lesen von Objekten beginnen, während die eingehende Replikation läuft, nachdem eines oder mehrere der verknüpften, geänderten Objekte empfangen wurden, aber bevor alle empfangen wurden. Die Zeit zwischen den Updates auf dem Quellreplikat wirkt sich direkt auf die Größe dieses Fensters aus. Updates, die nah beieinander auftreten, werden nah beieinander repliziert. Ein teilielles Update kann ein Problem sein, wenn eine Anwendung einen verknüpften Satz von Objekten verwendet.

 

Beispielsweise kann ein Remotezugriffsdienst das Verzeichnis verwenden, um Richtlinien- und Profildaten zu speichern. Die Richtliniendaten werden in einem Satz von Objekten und das Profil in einem anderen Satz gespeichert. Wenn ein Benutzer eine Verbindung mit dem RAS-Dienst herstellt, liest der RAS-Dienst die Richtlinie, um zu bestimmen, ob der Benutzer eine Verbindung herstellen darf und falls ja, welches Profil auf die Benutzersitzung angewendet werden soll. Ein teilielles Update kann sich auf verschiedene Arten auf den Remotezugriffsdienst auswirken:

-   Wenn die Richtlinie komplex ist und aus mehreren Objekten besteht, liest der Remotezugriffsdienst möglicherweise eine teilweise aktualisierte Richtlinie, was zu einer falschen Verweigerung oder Zuteilung des Diensts für den Benutzer führt, die Richtlinie aufgrund interner Inkonsistenz nicht verarbeiten kann und so weiter.
-   Wenn sowohl die Richtlinie als auch die Profile aktualisiert wurden, kann der Dienst die Richtlinie ordnungsgemäß verarbeiten, aber ein veraltetes Profil anwenden, da die Richtlinienobjekte repliziert wurden, die Profilobjekte jedoch nicht.
-   Wenn das Profil komplex ist und aus mehreren Objekten besteht, kann der Dienst die Richtlinie ordnungsgemäß verarbeiten, aber ein teilweise aktualisiertes Profil anwenden, da die Richtlinienobjekte repliziert wurden, aber nur einige der Profilobjekte dies getan haben.

## <a name="collisions"></a>Kollisionen

Kollisionen treten auf, wenn die gleichen Attribute von zwei oder mehr Replikaten eines bestimmten Objekts während desselben Replikationsintervalls geändert werden. Der Replikationsprozess gleicht den Kollisionsvorgang ab. aufgrund der Abstimmung kann ein Benutzer oder eine Anwendung einen anderen Wert als den, den er geschrieben hat, "sehen".

Ein einfaches Beispiel sind Informationen zur Benutzeradresse: Ein Benutzer ändert eine Adressenadresse bei Replikat R1, und ein Administrator ändert die gleiche Adressenadresse bei Replikat R2. Ein geschriebener Wert wird so lange propagiert, bis ein anderer Wert durch den Mechanismus zum Abgleich von Kollisionen über diesen Wert ausgewählt wird. Solange ein Wert im Konfliktauflösungsprozess gegenüber anderen Werten "gewonnen" wird, wird der Wert weiterhin fortgesetzt. Letztendlich wird dieser "gewinnende" Wert an R1, R2 und alle anderen Replikate propagiert, wenn keine weiteren Änderungen vorgenommen werden.

Die Konfliktlösung ist ein Problem für Anwendungen, die Annahmen über die interne Konsistenz von Objekten oder Objektsätzen treffen. Beispielsweise speichert ein Dienst zur Verwaltung der Netzwerkbandbreitenzuordnung Netzwerkbandbreitendaten für ein bestimmtes Netzwerksegment im Verzeichnis in einem Objekt O1. Das -Objekt enthält die verfügbare Bandbreite in Bits pro Sekunde und die maximale Bandbreite, die ein einzelner Benutzer reservieren kann. Der Dienst erwartet, dass die vom Benutzer beobachtbare Bandbreite immer kleiner oder gleich der verfügbaren Bandbreite ist.

Gehen Sie dabei vom folgenden Ereignisablauf aus:

-   Das Objekt im anfänglichen vollständig replizierten Zustand gibt die verfügbare Bandbreite als 56 KBit/s und die vom Benutzer beobachtbare Bandbreite 9.600 Bits pro Sekunde an.
-   Ein Administrator bei Replikat R₁ ändert die Werte in 64k bzw. 19.200.
-   Ein Administrator des Replikats R₂ ändert die Werte in 10 Millionen bzw. 1 Million, bevor das Update von R₁ eintrifft.

Unter der Annahme, dass die in Frage gestellten Attribute beim Auftreten der Updates über die gleichen Versionsnummern verfügen, besteht eine kleine, aber echte Möglichkeit, dass das Objekt eine maximale Bandbreite von 64.000 und einen Benutzerwert von maximal 1 Million beobachtbar hat– wenn die Anwendung die Updates als separate Schreibvorgänge ausführt. Die Anwendung sollte beide Eigenschaften immer in einem einzigen Vorgang aktualisieren.

 

 