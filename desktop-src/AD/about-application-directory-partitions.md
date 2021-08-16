---
title: Informationen zu Anwendungsverzeichnispartitionen
description: Entwickler, die ADSI oder LDAP verwenden, um relativ statische und globale Daten in Active Directory Domain Services zu speichern und darauf zu zugreifen, möchten der Einfachheit und Einheitlichkeit halber auch weiterhin ADSI- oder LDAP-Zugriff für ihre dynamischen Datenanforderungen verwenden. Dynamische Daten ändern sich häufiger als das, was für die Speicherung in der Active Directory Domain Services. Dynamische Daten ändern sich in der Regel häufiger als die Replikationslatenz, die mit der Verteilung der Änderung an alle Replikate der Daten verbunden ist.
ms.assetid: bf856c3a-9061-474a-a536-c87ca50d5f83
ms.tgt_platform: multiple
keywords:
- Informationen zu Anwendungsverzeichnispartitionen
- Anwendungsverzeichnispartitionen, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9063a05bdb6f04681f012f1e6317b3343833c79c8f6a5af39a1a7865eccbab63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841030"
---
# <a name="about-application-directory-partitions"></a>Informationen zu Anwendungsverzeichnispartitionen

Entwickler, die ADSI oder LDAP verwenden, um relativ statische und globale Daten in Active Directory Domain Services zu speichern und darauf zu zugreifen, möchten der Einfachheit und Einheitlichkeit halber auch weiterhin ADSI- oder LDAP-Zugriff für ihre dynamischen Datenanforderungen verwenden. Dynamische Daten ändern sich häufiger als das, was für die Speicherung in der Active Directory Domain Services. Dynamische Daten ändern sich in der Regel häufiger als die Replikationslatenz, die mit der Verteilung der Änderung an alle Replikate der Daten verbunden ist.

In Windows 2000 ist die Unterstützung für dynamische Daten eingeschränkt. Das Speichern dynamischer Daten in einer Domänenpartition kann kompliziert sein. Die Daten werden auf alle Domänencontroller in der Domäne repliziert. Dies ist häufig unnötig und kann aufgrund der Replikationslatenz zu inkonsistenten Daten führen. Dies kann sich negativ auf die Netzwerkleistung auswirken. Darüber hinaus sind Domänenpartitionen nicht effektiv für Anwendungen, die Daten über Domänengrenzen hinweg replizieren müssen. Eine weitere Option in Windows 2000 ist das Speichern dynamischer Daten in Attributen, die als nicht repliziert markiert sind. Diese Anordnung ist jedoch darauf beschränkt, dass sie über einen single point of failure verfügt, nämlich den einzelnen Domänencontroller, der die einzige Kopie der nicht replizierten Attribute des Objekts enthält.

Anwendungsverzeichnispartitionen bieten die Möglichkeit, den Replikationsbereich zu steuern und die Platzierung von Replikaten auf eine Weise zu ermöglichen, die für dynamische Daten besser geeignet ist. Daher bietet die Anwendungsverzeichnispartition die Möglichkeit, dynamische Daten auf dem Active Directory-Server zu hosten, sodass ADSI/LDAP-Zugriff darauf möglich ist, ohne die Netzwerkleistung erheblich zu beeinträchtigen.

Der Windows 2000 DNS-Dienst ist ein Beispiel für einen Dienst, der Anwendungsverzeichnispartitionen nutzen kann. Wenn Windows 2000 der DNS-Dienst optional für die Verwendung von Active Directory Domain Services konfiguriert ist, werden die DNS-Zonendaten auf dem Active Directory-Server in einer Domänenpartition gespeichert. Das heißt, die Daten werden auf allen Domänencontrollern in der Domäne repliziert, unabhängig davon, ob ein DNS-Server für die Ausführung auf dem Domänencontroller konfiguriert ist. Dies ist eine Instanz, in der eine vollständige domänenweite Replikation nicht erforderlich ist. Indem die DNS-Zonendaten in einer Anwendungsverzeichnispartition gespeichert werden, kann der Dienst den Replikationsbereich nur auf die Teilmenge der Domänencontroller in der Domäne neu definieren, auf denen der DNS-Server tatsächlich ausgeführt wird.

Betrachten Sie die folgenden Szenarien zum Hosten eines Replikats einer Anwendungsverzeichnispartition:

-   Ein Replikat einer Anwendungsverzeichnispartition kann auf jedem Windows Server 2003-Betriebssystem und einem späteren Domänencontroller in einer Active Directory Domain Services werden.
-   Der Satz von Domänencontrollern, die Replikate einer Anwendungsverzeichnispartition hosten, kann angegeben werden. Im Gegensatz zu einer Domänenpartition ist eine Anwendungsverzeichnispartition nicht erforderlich, um auf alle Domänencontroller in einer Domäne zu replizieren, und sie kann auf Domänencontroller in verschiedenen Domänen der Gesamtstruktur repliziert werden.
-   Ein Domänencontroller mit einem Anwendungsverzeichnispartitionsreplikat kann in einer Umgebung im gemischten Modus mit anderen Computern mit Windows 2000 oder Windows NT 4.0 koexistieren und funktionieren.

Folgende Datentypen können in einer Anwendungsverzeichnispartition gespeichert werden:

-   Eine Anwendungsverzeichnispartition kann Instanzen eines beliebigen Objekttyps mit Ausnahme von Sicherheitsprinzipals enthalten, z. B. Benutzer, Computer oder Gruppen.
-   Objekte in einer Anwendungsverzeichnispartition können DN-Wertverweise auf andere Objekte in derselben Anwendungsverzeichnispartition, auf Objekte in der Konfigurations- und Schemapartition und auf jeden Namenkontextkopf (das oberste Objekt einer Verzeichnispartition, z. B. das **domainDNS-Objekt** am Anfang einer Anwendungsverzeichnispartition) verwalten.
-   Weitere Informationen und ein Beispiel für den Typ dynamischer Daten, die in einer Anwendungsverzeichnispartition gespeichert werden können, finden Sie unter [Dynamische Objekte.](dynamic-objects.md) Dynamische Objekte werden ab Windows Server 2003 unterstützt. Dynamische Objekte verfügen über eine Eigenschaft, die die Livezeit bestimmt, nach der das Objekt vom Active Directory-Server gelöscht wird.

Folgende Einschränkungen gelten für Anwendungsverzeichnispartitionen:

-   Objekte in einer Anwendungsverzeichnispartition können *keine DN-Wertverweise* auf Objekte in anderen Anwendungsverzeichnispartitionen oder Domänenpartitionen verwalten. (DN-Wertverweise sind permanente Verweise auf einen Distinguished Name-Wert wie "CN=someuser,DC=corp,DC=Fabrikam,DC=com"). Ebenso können Objekte in Domänen-, Konfigurations- und Schemapartitionen keine DN-Wertverweise auf Objekte in einer Anwendungsverzeichnispartition verwalten. Ein DN-Wertverweis kann für den Namenkontextkopf beibehalten werden. () )
-   Objekte in einer Anwendungsverzeichnispartition werden nicht in den globalen Katalog repliziert. Wie bei jedem Domänencontroller kann auch ein globaler Katalogserver so konfiguriert werden, dass er ein vollständiges Replikat einer Anwendungsverzeichnispartition enthält, aber die Partitionsdaten des Anwendungsverzeichnisses sind vollständig von den globalen Katalogdaten getrennt.
-   Wenn ein Anwendungsverzeichnispartitionsreplikat erstellt wird, muss sich die Domain-Naming FSMO-Rolle auf einem der Windows Server 2003- und höher-Betriebssystemdomänencontroller befinden. Nachdem das Partitionsreplikat des Anwendungsverzeichnisses erstellt wurde, kann die FSMO-Rolle "Domain Naming" einem Windows 2000-Domänencontroller zugewiesen werden.
-   Anwendungsverzeichnispartitionsobjekte können nicht in andere Active Directory-Partitionen außerhalb der Partition verschoben werden, in der sie erstellt wurden.

Weitere Partitionsfeatures des Anwendungsverzeichnisses sind:

-   Das Sicherheits- und Zugriffssteuerungsmodell für die Anwendungsverzeichnispartition ist das gleiche wie für andere Partitionen in Active Directory Domain Services.
-   Die Zeitintervalle, die die Latenz beim Initiieren einer ursprünglichen Änderungsbenachrichtigung an Replikationspartner innerhalb eines Standorts steuern, können für jede Anwendungsverzeichnispartitionsbasis separat konfiguriert werden.
-   Anwendungsverzeichnispartitionen können genauso wie reguläre Domänen benannt, an eine beliebige Stelle im Active Directory-Namespace angefügt werden, in der eine Domäne verwendet werden kann, und über DNS auch von 2000-Systemen Windows werden.
-   Eine Anwendungsverzeichnispartition kann erstellt, der Replikationsbereich definiert und die konfigurierbaren Einstellungen programmgesteuert mithilfe von LDAP- und ADSI-Standard-APIs angepasst werden. Weitere Informationen zum programmgesteuerten Bearbeiten von Anwendungsverzeichnispartitionen finden Sie unter [Application Directory Partitions](application-directory-partitions.md).

 

 




