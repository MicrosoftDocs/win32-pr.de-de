---
title: Dynamische Objekte
description: In Windows Server 2003 und neueren Versionen von Windows Active Directory Domain Services Unterstützung für das Speichern dynamischer Einträge im Verzeichnis bereitstellen.
ms.assetid: ac5779b6-f226-414c-92a9-091719b1515b
ms.tgt_platform: multiple
keywords:
- dynamische Objekte AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d521dabda8f82cbdcd46c00b3041f150f390d60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707709"
---
# <a name="dynamic-objects"></a>Dynamische Objekte

In Windows Server 2003 und neueren Versionen von Windows Active Directory Domain Services Unterstützung für das Speichern dynamischer Einträge im Verzeichnis bereitstellen. Ein dynamischer Eintrag ist ein Objekt im Verzeichnis, dem ein Gültigkeits Zeitraum (Time-to-Live, TTL) zugeordnet ist. Die Gültigkeitsdauer für einen Eintrag wird festgelegt, wenn der Eintrag erstellt wird. Die Gültigkeitsdauer wird automatisch verringert, und wenn Sie abläuft, verschwindet der dynamische Eintrag. Der Client kann bewirken, dass ein dynamischer Eintrag länger als die aktuelle verbleibende Lebensdauer bleibt, indem er den TTL-Wert aktualisiert (ändert). Clients, auf denen dynamische Daten im Verzeichnis gespeichert werden, müssen diese Daten regelmäßig aktualisieren, um zu verhindern, dass Sie verschwinden.

Viele Anwendungen und Dienste, die LDAP zum Speichern und Zugreifen auf relativ statische und Global interessante Daten von einem Active Directory Server verwenden, bevorzugen auch die Verwendung des LDAP-Zugriffs für Ihre dynamischen Datenanforderungen. Außerdem kann es für einige Anwendungen wünschenswert sein, die Aufgabe der Garbage Collection-Objekte in den DS zu deaktivieren, die eine begrenzte Lebensdauer für den Verzeichnisdienst haben. Anwendungsverzeichnis Partitionen (mit der Möglichkeit der kontrollierten Platzierung von Replikaten) und pro-Objekt-TTLS bieten die Möglichkeit, dynamische Daten in Active Directory Domain Services zu Hosting und so LDAP-Zugriff darauf zu ermöglichen.

Eine neue hilfsobjektklasse mit dem Namen **DynamicObject** mit OID = 1.3.6.1.4.1.1466.101.119.2 wird im AD-Basis Schema definiert, die von dynamischen Einträgen verwendet werden soll. Diese Hilfsklasse enthält das Attribut mit dem Namen " **entryttl** " mit OID = 1.3.6.1.4.1.1466.101.119.3 als Attribut vom Typ "System-May-". Der Wert dieses Attributs ist die Zeit in Sekunden, in der der entsprechende Verzeichniseintrag weiterhin vorhanden ist, bevor er aus dem Verzeichnis verschwindet. Wenn der Client bei der Objekt Erstellung nicht explizit einen Wert für dieses Attribut bereitstellt, stellt der DS einen Standardwert bereit, wie später angegeben.

Ein neuer erweiterter LDAP-Vorgang mit OID = 1.3.6.1.4.1.1466.101.119.1 für die Client Aktualisierung eines dynamischen Eintrags im Verzeichnis wird definiert und im **supportedextension** -Attribut des Stamm-DSE-Objekts veröffentlicht.

In der eigentlichen Implementierung ist **entryttl** ein konstruiertes Attribut. Die tatsächliche Ablaufzeit des Objekts wird als absolute Zeit gespeichert, wenn das Objekt in einem reinen System Attribut mit dem Namen **ms-DS-Entry-Time-to-Live** zerstört werden kann.

Alle dynamischen Objekte weisen die folgenden Einschränkungen auf:

-   Ein gelöschtes dynamisches Objekt, das aufgrund seiner Gültigkeitsdauer abläuft, hinterlässt keinen Tombstone.
-   Alle DCS mit Replikaten dynamischer Objekte müssen unter Windows Server 2003 ausgeführt werden.
-   Dynamische Einträge mit TTL-Werten werden in allen Partitionen außer der Konfigurations Partition und der Schema Partition unterstützt.
-   Active Directory Domain Services veröffentlichen das optionale **dynamicsubtrees** -Attribut, wie in RFC 2589 beschrieben, im Stamm-DSE-Objekt.
-   Dynamische Einträge werden ähnlich wie nicht dynamische Einträge bei der Verarbeitung von Such Vorgängen, vergleichen, hinzufügen, löschen, ändern und Ändern von Änderungs Vorgängen behandelt.
-   Es gibt keine Möglichkeit, einen statischen Eintrag in einen dynamischen Eintrag zu ändern und umgekehrt.
-   Ein nicht dynamischer Eintrag kann keinem dynamischen Eintrag untergeordnet werden.

 

 




