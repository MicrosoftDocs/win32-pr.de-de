---
title: Replikation von Anwendungsverzeichnispartitionen
description: Anwendungsverzeichnispartitionen werden am häufigsten zum Speichern dynamischer Daten verwendet.
ms.assetid: b5fbec54-ee1a-4fe6-b4b7-67fc4e77d043
ms.tgt_platform: multiple
keywords:
- Anwendungsverzeichnispartitionsreplikation AD
- Anwendungsverzeichnispartitionen AD , Replikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7df6c50653fe1660bbf95f0f6ca580404d38c366c1045bc3d1b712ca771d3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024410"
---
# <a name="application-directory-partition-replication"></a>Replikation von Anwendungsverzeichnispartitionen

Anwendungsverzeichnispartitionen werden am häufigsten zum Speichern dynamischer Daten verwendet. Da sich Daten häufiger ändern als die Konfigurationsdaten für eine Gesamtstruktur, können der Replikationsbereich und die Häufigkeit einer Anwendungsverzeichnispartition für jede Partition festgelegt werden. Die Replikationsfunktionen von Active Directory Domain Services können verwendet werden, aber die Replikationsdaten können an den Typ der in der Partition gespeicherten Daten angepasst werden.

Das Betriebssystem erzwingt keine maximale Anzahl von Replikaten, aber die Anzahl der Replikate sollte auf ein Minimum beschränkt werden, um die Auswirkungen der Replikation der dynamischen Anwendungsverzeichnispartitionsdaten auf die Leistung zu reduzieren.

Der KCC generiert und verwaltet die Replikationstopologie für eine Anwendungsverzeichnispartition.

## <a name="application-directory-partition-replication-within-a-site"></a>Replikation von Anwendungsverzeichnispartitionen an einem Standort

Die Replikationsintervalle, die die standortinterne Replikation einer Anwendungsverzeichnispartition steuern, können konfiguriert werden. Dadurch können die dynamischen Daten in einer Anwendungsverzeichnispartition schneller synchronisiert werden als die statischen Daten in einer Domänenpartition. Weitere Informationen zum programmgesteuerten Konfigurieren einer Anwendungsverzeichnispartition finden Sie unter Ändern der Konfiguration der [Anwendungsverzeichnispartition.](modifying-application-directory-partition-configuration.md)

Zwei Attribute auf dem [**crossRef-Objekt**](/windows/desktop/ADSchema/c-crossref) der Anwendungsverzeichnispartition und zwei Registrierungswerte auf jedem Windows 2000 und höher des Domänencontrollers steuern die Latenz beim Initiieren einer ursprünglichen Änderungsbenachrichtigung an Replikationspartner innerhalb eines Standorts.

-   Das [**msDS-Replication-Notify-First-DSA-Delay-Attribut**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay) eines [**crossRef-Objekts**](/windows/desktop/ADSchema/c-crossref) gibt die Verzögerung in Sekunden nach einer Ursprünglichen Objektänderung an, bevor der erste Replikationspartner benachrichtigt wird. Ein Registrierungswert auf jedem Domänencontroller kann einen ähnlichen Wert angeben. In einer Windows Server 2003-Gesamtstruktur beträgt die erste Standardverzögerung 15 Sekunden. In einer Gesamtstruktur im gemischten Modus beträgt die erste Standardverzögerung fünf Minuten.
-   Das [**msDS-Replication-Notify-Subsequent-DSA-Delay-Attribut**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) eines [**crossRef-Objekts**](/windows/desktop/ADSchema/c-crossref) gibt die Verzögerung zwischen nachfolgenden Benachrichtigungen an den zweiten, dritten und so weiter Replikationspartnern in Sekunden an. Ein Registrierungswert auf jedem Domänencontroller kann einen ähnlichen Wert angeben. In einer Windows Server 2003-Gesamtstruktur beträgt die nachfolgende Standardverzögerung 3 Sekunden. In einer Gesamtstruktur im gemischten Modus beträgt die nachfolgende Verzögerung standardmäßig 30 Sekunden.

Die [**crossRef-Attribute**](/windows/desktop/ADSchema/c-crossref) gelten für alle Domänencontroller, die ein Replikat der Anwendungsverzeichnispartition hosten, und wirken sich nur auf die Replikation der Anwendungsverzeichnispartition aus, die durch das **crossRef-Objekt** identifiziert wird. Die Registrierungswerte gelten nur für den Domänencontroller, auf dem sie festgelegt sind, und wirken sich auf die standortinterne Replikation für alle Partitionen aus, die der Domänencontroller hostet. Wenn weder die **crossRef-Attribute** noch die zugehörigen Registrierungswerte festgelegt sind, verwendet ein Domänencontroller die Standardwerte. Wenn die Registrierungswerte festgelegt sind, überschreiben sie alle Werte, die im **crossRef-Objekt** festgelegt sind. Standardmäßig sind die Registrierungs- und **crossRef-Werte** nicht festgelegt, sodass die Standardwerte verwendet werden. Dadurch kann ein Administrator die Replikation für alle Replikate einer Anwendungsverzeichnispartition beschleunigen, indem er die **crossRef-Werte** festlegt und gleichzeitig eine feineren Optimierung mit den Registrierungseinstellungen auf jedem Domänencontroller ermöglicht.

Ab Windows Server 2003 verwenden Domänenpartitionen auch diese Attribute des [**crossRef-Objekts,**](/windows/desktop/ADSchema/c-crossref) um die Replikationslatenz zwischen Standorten zu steuern. Dies ist eine Änderung gegenüber früheren Serverversionen, bei der die Verzögerungsintervalle durch Registrierungswerte auf jedem Domänencontroller gesteuert wurden. Wenn die Gesamtstruktur auf Windows Server 2003 aktualisiert wird, werden die vorhandenen Registrierungswerte nur beibehalten, wenn sie von den Standardwerten geändert wurden. Die Benachrichtigungsintervalle der Domänencontroller in der Registrierung überschreiben die Benachrichtigungsintervalle, die im **crossRef-Objekt** der Partition gespeichert sind.

## <a name="application-directory-partition-replication-across-sites"></a>Replikation von Anwendungsverzeichnispartitionen zwischen Standorten

Die Replikate einer Anwendungsverzeichnispartition, die sich standortübergreifend befinden, beobachten den Zeitplan für die standortübergreifende Replikation wie für die Domänenpartition und die globale Katalogreplikation. Replikate einer Anwendungsverzeichnispartition befinden sich jedoch häufiger an einem Standort, wenn sie wirklich flüchtige Daten hosten, da die Replikationslatenz zwischen Standorten möglicherweise nicht akzeptabel ist, um die Replikate konsistent zu machen.

## <a name="application-directory-partitions-are-not-replicated-to-global-catalogs"></a>Anwendungsverzeichnispartitionen werden nicht in globale Kataloge repliziert

Objekte in einer Anwendungsverzeichnispartition werden nicht in den globalen Katalog repliziert. Die Anwendungsverzeichnispartition ist als Host für dynamische Daten und Objekte vorgesehen, für die es weder sinnvoll noch möglich ist, die Objekte umfassend zu replizieren. Aus diesem Grund bietet die Anwendungsverzeichnispartition einen kontrollierten Umfang und eine kontrollierte Replikationshäufigkeit. Aus diesem Grund gibt es keinen Grund, diese Objekte in den globalen Katalog zu replizieren und somit auf die gesamte Gesamtstruktur verteilt zu werden, in der ein globaler Katalogserver vorhanden ist. Dies hindert Objekte in einer Anwendungsverzeichnispartition nicht daran, Attribute im Schema zu verwenden, das als [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset)markiert ist. Wie bei jedem Domänencontroller kann ein globaler Katalogserver weiterhin als vollständiges Replikat einer Anwendungsverzeichnispartition konfiguriert werden.

 

 