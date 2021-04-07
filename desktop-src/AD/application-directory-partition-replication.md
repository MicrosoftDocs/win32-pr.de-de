---
title: Anwendungsverzeichnis-Partitions Replikation
description: Anwendungsverzeichnis Partitionen werden am häufigsten zum Speichern dynamischer Daten verwendet.
ms.assetid: b5fbec54-ee1a-4fe6-b4b7-67fc4e77d043
ms.tgt_platform: multiple
keywords:
- Anwendungsverzeichnis-Partitions Replikations Anzeige
- Anwendungsverzeichnis Partitionen AD, Replikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41523b86ae8d3a744d4eb288c5b240a60222aa21
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038806"
---
# <a name="application-directory-partition-replication"></a>Anwendungsverzeichnis-Partitions Replikation

Anwendungsverzeichnis Partitionen werden am häufigsten zum Speichern dynamischer Daten verwendet. Da sich Daten häufiger ändern als die Konfigurationsdaten für eine Gesamtstruktur, können der Replikations Bereich und die Häufigkeit einer Anwendungsverzeichnis Partition für jede Partition festgelegt werden. Die Replikations Funktionen von Active Directory Domain Services können verwendet werden, aber die Replikations Daten können so angepasst werden, dass Sie den Typ der Daten entsprechen, die auf der Partition gespeichert sind.

Das Betriebssystem erzwingt keine maximale Anzahl von Replikaten, aber die Anzahl der Replikate sollte auf ein Minimum beschränkt werden, um die Auswirkungen der Replikation der dynamischen Anwendungsverzeichnis-Partitions Daten auf die Leistung zu reduzieren.

Die KCC generiert und verwaltet die Replikations Topologie für eine Anwendungsverzeichnis Partition.

## <a name="application-directory-partition-replication-within-a-site"></a>Anwendungsverzeichnis-Partitions Replikation innerhalb eines Standorts

Die Replikations Intervalle, die die Standort interne Replikation einer Anwendungsverzeichnis Partition steuern, können konfiguriert werden. Dadurch können dynamische Daten in einer Anwendungsverzeichnis Partition schneller synchronisiert werden als die statischeren Daten in einer Domänen Partition. Weitere Informationen zum programmgesteuerten Konfigurieren einer Anwendungsverzeichnis Partition finden Sie unter [Ändern der Konfiguration der Anwendungsverzeichnis Partition](modifying-application-directory-partition-configuration.md).

Zwei Attribute für das [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt der Anwendungsverzeichnis Partition und zwei Registrierungs Werte auf den einzelnen Domänen Controllern unter Windows 2000 und höher steuern die Latenz beim Initiieren einer Ursprungs Änderungs Benachrichtigung an Replikations Partner innerhalb eines Standorts.

-   Das [**msDS-Replication-notify-First-DSA-Delay-**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay) Attribut eines [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekts gibt die Verzögerung in Sekunden an, nach der ein Ursprungs Objekt geändert wird, bevor der erste Replikations Partner benachrichtigt wird. Ein Registrierungs Wert auf jedem Domänen Controller kann einen ähnlichen Wert angeben. In einer Windows Server 2003-Gesamtstruktur beträgt die standardmäßige erste Verzögerung 15 Sekunden. In einer Gesamtstruktur mit gemischtem Modus beträgt die standardmäßige erste Verzögerung fünf Minuten.
-   Das [**msDS-Replication-notify-Replication-DSA-Delay-**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) Attribut eines [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekts gibt die Verzögerung (in Sekunden) zwischen den nachfolgenden Benachrichtigungen an die zweiten, dritten usw. Replikations Partner an. Ein Registrierungs Wert auf jedem Domänen Controller kann einen ähnlichen Wert angeben. In einer Windows Server 2003-Gesamtstruktur beträgt die nachfolgende Standard Verzögerung 3 Sekunden. In einer Gesamtstruktur mit gemischtem Modus beträgt die standardmäßige nachfolgende Verzögerung 30 Sekunden.

Die [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Attribute gelten für alle Domänen Controller, die ein Replikat der Anwendungsverzeichnis Partition hosten, und wirken sich nur auf die Replikation der vom **CrossRef** -Objekt identifizierten Anwendungsverzeichnis Partition aus. Die Registrierungs Werte gelten nur für den Domänen Controller, auf dem Sie festgelegt sind, und wirken sich auf die standortübergreifende Replikation für alle Partitionen aus, die vom Domänen Controller gehostet werden. Wenn weder das **CrossRef** -Attribut noch seine Registrierungs Werte festgelegt sind, verwendet ein Domänen Controller die Standardwerte. Wenn die Registrierungs Werte festgelegt sind, überschreiben Sie alle Werte, die im **CrossRef** -Objekt festgelegt sind. Standardmäßig sind die Registrierungs-und **CrossRef** -Werte nicht festgelegt, sodass die Standardwerte verwendet werden. Dies ermöglicht es einem Administrator, die Replikation für alle Replikate einer Anwendungsverzeichnis Partition zu beschleunigen, indem die **CrossRef** -Werte festgelegt werden, während eine präzisere Optimierung mit den Registrierungs Einstellungen auf den einzelnen Domänen Controllern

Ab Windows Server 2003 verwenden Domänen Partitionen diese Attribute des [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekts, um die Replikations Latenz Zwischenstand Orten zu steuern. Dies ist eine Änderung gegenüber früheren Serverversionen, bei denen die Verzögerungs Intervalle durch Registrierungs Werte auf den einzelnen Domänen Controllern gesteuert wurden. Wenn die Gesamtstruktur auf Windows Server 2003 aktualisiert wird, werden die vorhandenen Registrierungs Werte nur beibehalten, wenn Sie von den Standardwerten geändert wurden. Die Benachrichtigungs Intervalle der Domänen Controller in der Registrierung überschreiben die Benachrichtigungs Intervalle, die im **Querverweis** Objekt der Partition gespeichert sind.

## <a name="application-directory-partition-replication-across-sites"></a>Standortübergreifende Replikation von Anwendungsverzeichnis Partitionen

Die Replikate einer Anwendungsverzeichnis Partition, die standortübergreifend gefunden wird, beobachten den standortübergreifenden Replikations Zeitplan für die Domänen Partition und die globale Katalog Replikation. Replikate einer Anwendungsverzeichnis Partition befinden sich jedoch häufiger innerhalb eines Standorts, wenn Sie tatsächlich flüchtige Daten Hosting, da die Replikations Latenz Zwischenstand Orten möglicherweise nicht akzeptabel ist, um die Replikate konsistent zu machen.

## <a name="application-directory-partitions-are-not-replicated-to-global-catalogs"></a>Anwendungsverzeichnis Partitionen werden nicht in globalen Katalogen repliziert.

Objekte in einer Anwendungsverzeichnis Partition werden nicht in den globalen Katalog repliziert. Die Anwendungsverzeichnis Partition ist als Host für dynamische Daten und Objekte konzipiert, für die Sie möglicherweise weder vernünftig noch für die weit verbreitete Replikation der Objekte konzipiert ist. Aus diesem Grund bietet die Anwendungsverzeichnis Partition den kontrollierten Bereich und die Häufigkeit der Replikation. Aus diesem Grund gibt es keinen Grund, zuzulassen, dass diese Objekte in den globalen Katalog repliziert werden und daher über die gesamte Gesamtstruktur verteilt werden, in der ein globaler Katalogserver vorhanden ist. Dadurch wird verhindert, dass Objekte in einer Anwendungsverzeichnis Partition die Attribute im Schema verwenden, die als [**ismembership ofpartialattributeset**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset)gekennzeichnet sind. Wie bei jedem beliebigen Domänen Controller kann ein globaler Katalogserver weiterhin als vollständiges Replikat einer Anwendungsverzeichnis Partition konfiguriert werden.

 

 