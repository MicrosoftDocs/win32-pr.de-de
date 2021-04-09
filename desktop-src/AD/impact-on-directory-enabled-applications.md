---
title: Auswirkung auf Directory-Enabled Anwendungen
description: In diesem Thema werden die Auswirkungen auf Verzeichnis aktivierte Anwendungen beschrieben, wenn Versions Verzeichner, Teil Updates oder Konflikte auftreten.
ms.assetid: 0aec6fe3-7757-4472-bc18-add2327d4e1b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061818fc791e1c75d440d0c477a321b8c4e5edfb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948563"
---
# <a name="impact-on-directory-enabled-applications"></a>Auswirkung auf Directory-Enabled Anwendungen

## <a name="version-skew"></a>Versions Schiefe

Die Versions Abweichung tritt auf, wenn Anwendungen die gleichen Objekte aus verschiedenen Replikaten lesen, bevor eine Änderung repliziert wurde. Anwendungen, die das Remote Replikat lesen, erkennen das unverändert Objekt. Die Versions Schiefe ist ein Problem, wenn eine bestimmte Anwendung oder ein Satz von Anwendungen die Daten im Verzeichnis für die Interoperabilität verwendet.

Beispielsweise kann ein RPC-Dienst seine Endpunkte im Verzeichnis mithilfe von Standard-RPC-APIs (z. [**b. rpcnsbindingexport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta)) veröffentlichen. Clients stellen eine Verbindung mit dem Dienst her, indem Sie den gewünschten Endpunkt im Verzeichnis ( [**rpcnsbindinglookupbegin**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), [**rpcnsbindinglookupnext**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)usw.) nachschlagen und eine Bindung an ihn herstellen.

Angenommen, ein RPC-Dienst ₁ veröffentlicht Endpunkt-e ₁ und wechselt anschließend zu einem anderen Computer. Der ursprüngliche Endpunkt s ₁ wird in E<sub>S2 geändert und</sub> spiegelt die Adresse des neuen Computers wider. Clients, die Remote Replikate des Verzeichnis Dienstanbieter lesen, können erst eine Verbindung mit dem Dienst herstellen, wenn der aktualisierte Endpunkt repliziert wird Das Verschieben eines Dienstanbieter von einem Computer auf einen anderen wird jedoch selten vorkommen. Diese Unterbrechung/Verzögerung sollte daher nur selten auftreten, insbesondere dann, wenn die Bewegung des Dienstanbieter gut geplant ist.

## <a name="partial-updates"></a>Teilupdates

Im Allgemeinen erfolgt die partielle Aktualisierung, wenn eine Anwendung einen Datensatz liest, während eine andere Anwendung in denselben Daten Satz schreibt. Dies ist eine Situation, die bei jeder Anwendung in einem multimastersystem auftreten kann. Es gibt viele Möglichkeiten, dies zu tun. Sie können mehrere Anwendungen gleichzeitig in dasselbe Dataset schreiben. Wenn Sie sich auf diese Weise ansehen, ist der Verzeichnis Replikations Dienst nur eine andere Anwendung, die potenziell in dasselbe Dataset schreiben könnte, das auch von einer anderen Anwendung gelesen wird. Dies könnte ein mögliches Problem für eine Anwendung darstellen. Allerdings ist das Zeitfenster, in dem sich ein partielles Update auf Ihre Anwendung auswirken kann, relativ klein. Dies sollte in seltenen Fällen für Anwendungen, die nicht von der Synchronisierung mehrerer Objekte abhängen, ein Problem sein. Wenn die Anwendung stark von der Synchronisierung eines verknüpften Satzes von Objekten abhängig ist, sollten Sie die Auswirkungen einer partiellen Aktualisierung im Anwendungs Entwurf berücksichtigen.

Im Hinblick auf die Verzeichnisreplikation erfolgt eine partielle Aktualisierung, wenn Anwendungen denselben Satz von Objekten aus unterschiedlichen Replikaten lesen, während die Replikation ausgeführt wird. Anwendungen auf dem Remote Replikat sehen einige, jedoch nicht alle Änderungen.

> [!Note]  
> Das Fenster, in dem partielle Aktualisierungen sich auf eine Anwendung auswirken können, ist klein: die Anwendung muss mit dem Lesen von Objekten beginnen, während die eingehende Replikation ausgeführt wird, nachdem mindestens ein geändertes, geändertes Objekt empfangen wurde, aber bevor alle Daten empfangen wurden. Die Zeit zwischen den Updates am Quell Replikat wirkt sich direkt auf die Größe dieses Fensters aus – Updates, die in der Zeit geschlossen werden, werden zeitlich nah beieinander repliziert. Ein Teil Update kann ein Problem sein, wenn eine Anwendung einen zugehörigen Satz von Objekten verwendet.

 

Beispielsweise kann ein Remote Zugriffs Dienst das Verzeichnis zum Speichern von Richtlinien-und Profildaten verwenden. Die Richtlinien Daten werden in einem Satz von Objekten und im Profil in einem anderen Satz gespeichert. Wenn ein Benutzer eine Verbindung mit dem RAS-Dienst herstellt, liest der RAS-Dienst die Richtlinie, um zu bestimmen, ob der Benutzer eine Verbindung herstellen kann, und wenn dies der Fall ist, welches Profil auf die Benutzersitzung angewendet werden soll. Die partielle Aktualisierung kann sich auf verschiedene Arten auf den RAS-Dienst auswirken:

-   Wenn die Richtlinie Komplex ist und aus mehreren Objekten besteht, liest der RAS-Dienst möglicherweise eine teilweise aktualisierte Richtlinie, was zu einer falschen Verweigerung oder Gewährung des dienstanweises des Benutzers führt, die die Richtlinie aufgrund interner Inkonsistenzen nicht verarbeiten kann usw.
-   Wenn die Richtlinie und die Profile aktualisiert wurden, kann der Dienst die Richtlinie ordnungsgemäß verarbeiten, aber ein veraltetes Profil anwenden, da die Richtlinien Objekte repliziert wurden, die Profil Objekte dies jedoch nicht.
-   Wenn das Profil Komplex ist und aus mehreren Objekten besteht, kann der Dienst die Richtlinie ordnungsgemäß verarbeiten, aber ein teilweise aktualisiertes Profil anwenden, da die Richtlinien Objekte repliziert wurden, aber nur einige der Profil Objekte haben dies erreicht.

## <a name="collisions"></a>Kollisionen

Konflikte treten auf, wenn dieselben Attribute von mindestens zwei Replikaten eines bestimmten Objekts während desselben Replikations Intervalls geändert werden. Beim Replikationsprozess wird der Konflikt zusammen mit der aufgrund der Abstimmung kann ein Benutzer oder eine Anwendung einen anderen Wert als den geschrieben haben, den er geschrieben hat.

Ein einfaches Beispiel sind Benutzer Adressinformationen: ein Benutzer ändert eine e-Mail-Adresse auf dem Replikat R1, und ein Administrator ändert dieselbe Mailingadresse bei Replikat R2. Ein geschriebener Wert wird weitergegeben, bis ein anderer Wert durch den Konflikt Abstimmungsmechanismus über diesem Wert ausgewählt wird. Solange ein Wert für andere Werte im Konflikt Auflösungsprozess weiterhin "gewinnt", wird der Wert weiter verteilt. Letztendlich wird dieser "gewinnende" Wert an R1, R2 und alle anderen Replikate weitergegeben, wenn keine anderen Änderungen vorgenommen werden.

Die Konfliktlösung ist ein Problem für Anwendungen, die Annahmen über die interne Konsistenz von Objekten oder Objekt Sätzen treffen. Ein Verwaltungsdienst für die Netzwerk-Bandbreiten Zuordnung speichert z. b. Netzwerk Bandbreitendaten für ein bestimmtes Netzwerksegment im Verzeichnis in einem Objekt O1. Das-Objekt enthält die in Bits pro Sekunde verfügbare Bandbreite und die maximale Bandbreite, die ein einzelner Benutzer reservieren kann. Der Dienst erwartet, dass die vom Benutzer Reservierbare Bandbreite immer kleiner oder gleich der verfügbaren Bandbreite ist.

Gehen Sie dabei vom folgenden Ereignisablauf aus:

-   Das Objekt im ursprünglichen vollständig replizierten Status gibt die verfügbare Bandbreite als 56 Kilobits pro Sekunde an, und der Benutzer kann die Bandbreite als 9.600 Bits pro Sekunde reservieren.
-   Ein Administrator bei Replikat R ₁ ändert die Werte in 64K bzw. 19.200.
-   Ein Administrator bei Replikat r, ändert die Werte in 10 Millionen bzw. 1 Million, bevor das Update von R ₁ eingeht.

Wenn Sie davon ausgehen, dass die fraglichen Attribute bei der Aktualisierung die gleichen Versionsnummern aufweisen, gibt es eine kleine, aber reale Möglichkeit, dass das Objekt eine maximale Bandbreite von 64K und eine Benutzer reservierbare maximal 1 Million –, wenn die Anwendung die Updates als separate Schreibvorgänge ausführt. Die Anwendung sollte immer beide Eigenschaften in einem einzelnen Vorgang aktualisieren.

 

 