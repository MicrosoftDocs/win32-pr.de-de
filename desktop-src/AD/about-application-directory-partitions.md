---
title: Informationen zu Anwendungsverzeichnis Partitionen
description: Entwickler, die ADSI oder LDAP verwenden, um relativ statische und globale Daten in Active Directory Domain Services zu speichern und darauf zuzugreifen, können auch aus Gründen der Einfachheit und Einheitlichkeit die Verwendung von ADSI oder LDAP-Zugriff für Ihre dynamischen Datenanforderungen bevorzugen. Dynamische Datenänderungen sind häufiger als die für das Speichern in Active Directory Domain Services empfohlenen Änderungen. Dynamische Daten ändern sich normalerweise häufiger als die Replikations Latenz bei der Weitergabe der Änderung an alle Replikate der Daten.
ms.assetid: bf856c3a-9061-474a-a536-c87ca50d5f83
ms.tgt_platform: multiple
keywords:
- Informationen zu Anwendungsverzeichnis Partitionen
- Anwendungsverzeichnis Partitionen, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc1970f27d18d760ab3a45fae389809a40a2a89
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036268"
---
# <a name="about-application-directory-partitions"></a>Informationen zu Anwendungsverzeichnis Partitionen

Entwickler, die ADSI oder LDAP verwenden, um relativ statische und globale Daten in Active Directory Domain Services zu speichern und darauf zuzugreifen, können auch aus Gründen der Einfachheit und Einheitlichkeit die Verwendung von ADSI oder LDAP-Zugriff für Ihre dynamischen Datenanforderungen bevorzugen. Dynamische Datenänderungen sind häufiger als die für das Speichern in Active Directory Domain Services empfohlenen Änderungen. Dynamische Daten ändern sich normalerweise häufiger als die Replikations Latenz bei der Weitergabe der Änderung an alle Replikate der Daten.

In Windows 2000 ist die Unterstützung für dynamische Daten eingeschränkt. Das Speichern dynamischer Daten in einer Domänen Partition kann kompliziert sein. Die Daten werden auf allen Domänen Controllern in der Domäne repliziert, was häufig unnötig ist und aufgrund von Replikations Latenz zu inkonsistenten Daten führen kann. Dies kann sich negativ auf die Netzwerkleistung auswirken. Außerdem sind Domänen Partitionen für Anwendungen, die Daten über Domänen Grenzen hinweg replizieren müssen, nicht wirksam. Eine weitere Option in Windows 2000 ist das Speichern dynamischer Daten in Attributen, die als nicht repliziert markiert sind. Diese Anordnung ist jedoch begrenzt, da Sie über einen Single Point of Failure verfügt, d. h., der einzige Domänen Controller, der die einzige Kopie der nicht replizierten Attribute des Objekts enthält.

Anwendungsverzeichnis Partitionen bieten die Möglichkeit, den Umfang der Replikation zu steuern und die Platzierung von Replikaten auf eine Weise zuzulassen, die für dynamische Daten besser geeignet ist. Folglich bietet die Anwendungsverzeichnis Partition die Möglichkeit, dynamische Daten auf dem Active Directory Server zu Hosting und so den ADSI/LDAP-Zugriff zu ermöglichen, ohne dass sich dies erheblich auf die Netzwerkleistung auswirkt.

Der DNS-Dienst von Windows 2000 ist ein Beispiel für einen Dienst, der die Anwendungsverzeichnis Partitionen nutzen kann. Wenn der DNS-Dienst in Windows 2000 optional für die Verwendung von Active Directory Domain Services konfiguriert ist, werden die Daten der DNS-Zone auf dem Active Directory Server in einer Domänen Partition gespeichert. Das heißt, dass die Daten auf allen Domänen Controllern in der Domäne repliziert werden, unabhängig davon, ob ein DNS-Server für die Serverkonfiguration auf dem Domänen Controller konfiguriert ist. Dies ist eine Instanz, bei der die vollständige Domänen übergreifende Replikation unnötig ist. Durch das Speichern der DNS-Zonendaten in einer Anwendungsverzeichnis Partition kann der Dienst den Bereich der Replikation auf diese Teilmenge von Domänen Controllern in der Domäne, in der der DNS-Server tatsächlich ausgeführt wird, neu definieren.

Beachten Sie die folgenden Szenarien zum Hosten eines Replikats einer Anwendungsverzeichnis Partition:

-   Ein Replikat einer Anwendungsverzeichnis Partition kann auf einem beliebigen Windows Server 2003-Betriebssystem und einem späteren Domänen Controller in einer Active Directory Domain Services-Gesamtstruktur erstellt werden.
-   Die Gruppe von Domänen Controllern, auf denen Replikate einer Anwendungsverzeichnis Partition gehostet werden, kann angegeben werden. Im Gegensatz zu einer Domänen Partition ist eine Anwendungsverzeichnis Partition nicht erforderlich, um auf alle Domänen Controller in einer Domäne zu replizieren, und Sie kann auf Domänen Controllern in verschiedenen Domänen der Gesamtstruktur repliziert werden.
-   Ein Domänen Controller mit einem Anwendungsverzeichnis-Partitions Replikat kann gleichzeitig in einer Umgebung im gemischten Modus mit anderen Computern mit Windows 2000 oder Windows NT 4,0 vorhanden sein und funktionsfähig sein.

Zu den Datentypen, die in einer Anwendungsverzeichnis Partition gespeichert werden können, gehören:

-   Eine Anwendungsverzeichnis Partition kann Instanzen eines beliebigen Objekt Typs mit Ausnahme von Sicherheits Prinzipale (z. b. Benutzer, Computer oder Gruppen) enthalten.
-   Objekte in einer Anwendungsverzeichnis Partition können DN-Wert-Verweise auf andere Objekte in derselben Anwendungsverzeichnis Partition, auf Objekte in der Konfigurations-und Schema Partition und an einen beliebigen namens Kontext Head (das oberste Objekt einer Verzeichnis Partition ist, z. b. das **domainDns** -Objekt oben in einer Anwendungsverzeichnis Partition) verwalten.
-   Weitere Informationen und ein Beispiel für den Typ dynamischer Daten, die in einer Anwendungsverzeichnis Partition gespeichert werden können, finden Sie unter [dynamische Objekte](dynamic-objects.md). Dynamische Objekte werden ab Windows Server 2003 unterstützt. Dynamische Objekte verfügen über eine Eigenschaft, die die Gültigkeitsdauer bestimmt, nach der das Objekt vom Active Directory Server gelöscht wird.

Zu den Einschränkungen von Anwendungsverzeichnis Partitionen zählen folgende:

-   Objekte in einer Anwendungsverzeichnis Partition können keine *DN-Wert-Verweise* auf Objekte in anderen Anwendungsverzeichnis Partitionen oder Domänen Partitionen verwalten. (DN-Wert-Verweise sind permanente Verweise auf einen Distinguished Name-Wert, z. b. "CN = SomeUser, DC = Corp, DC = fabrikam, DC = com"). Ebenso können Objekte in Domänen-, Konfigurations-und Schema Partitionen keine DN-Wert-Verweise auf Objekte in einer Anwendungsverzeichnis Partition verwalten. Ein DN-Wert-Verweis kann an den namens Kontext Head verwaltet werden. () )
-   Objekte in einer Anwendungsverzeichnis Partition werden nicht in den globalen Katalog repliziert. Wie bei jedem beliebigen Domänen Controller kann auch ein globaler Katalogserver so konfiguriert werden, dass er ein vollständiges Replikat einer Anwendungsverzeichnis Partition enthält, aber die Partitions Daten des Anwendungs Verzeichnisses sind vollständig von den globalen Katalogdaten getrennt.
-   Wenn ein Anwendungsverzeichnis-Partitions Replikat erstellt wird, muss sich die Domain-Naming-Rolle "Rolle" auf einem der Betriebssystem-Domänen Controller unter Windows Server 2003 und höher befinden. Nachdem das Anwendungsverzeichnis-Partitions Replikat erstellt wurde, kann die Domänen Namen-FSMO-Rolle einem Windows 2000-Domänen Controller zugewiesen werden.
-   Anwendungsverzeichnis-Partitions Objekte können nicht auf andere Active Directory Partitionen außerhalb der Partition verschoben werden, in der Sie erstellt wurden.

Zu anderen Anwendungsverzeichnis-Partitions Features gehören:

-   Das Sicherheits-und Zugriffs Steuerungsmodell für die Anwendungsverzeichnis Partition ist das gleiche wie bei anderen Partitionen in Active Directory Domain Services.
-   Die Zeitintervalle, die die Wartezeit für das Initiieren einer Ursprungs Änderungs Benachrichtigung an Replikations Partner innerhalb eines Standorts steuern, können separat für jede Anwendungsverzeichnis Partition konfiguriert werden.
-   Anwendungsverzeichnis Partitionen können genauso benannt werden wie reguläre Domänen, die an eine beliebige Stelle im Active Directory Namespace angefügt werden, in der eine Domäne vorhanden ist, und mit DNS selbst durch Windows 2000-Systeme auf der Ebene "".
-   Eine Anwendungsverzeichnis Partition kann erstellt werden, Ihr Replikations Bereich ist definiert, und die konfigurierbaren Einstellungen können Programm gesteuert mithilfe von standardmäßigen LDAP-und ADSI-APIs angepasst werden. Weitere Informationen zur programmgesteuerten Bearbeitung von Anwendungsverzeichnis Partitionen finden Sie unter [Anwendungsverzeichnis Partitionen](application-directory-partitions.md).

 

 




