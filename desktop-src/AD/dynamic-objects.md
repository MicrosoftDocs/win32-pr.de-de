---
title: Dynamische Objekte
description: In Windows Server 2003 und höher von Windows bietet Active Directory Domain Services Unterstützung für das Speichern dynamischer Einträge im Verzeichnis.
ms.assetid: ac5779b6-f226-414c-92a9-091719b1515b
ms.tgt_platform: multiple
keywords:
- dynamische Objekte AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74660728179365f6585bce2462cd22f2508e68318eb84312d039a431330329b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191718"
---
# <a name="dynamic-objects"></a>Dynamische Objekte

In Windows Server 2003 und höher von Windows bietet Active Directory Domain Services Unterstützung für das Speichern dynamischer Einträge im Verzeichnis. Ein dynamischer Eintrag ist ein Objekt im Verzeichnis, das über einen zugeordneten TTL-Wert (Time-to-Live) verfügt. Die Tl für einen Eintrag wird festgelegt, wenn der Eintrag erstellt wird. Die Livezeit wird automatisch dekrementiert, und wenn sie abläuft, wird der dynamische Eintrag nicht mehr angezeigt. Der Client kann dazu führen, dass ein dynamischer Eintrag länger als die aktuelle verbleibende Lebensdauer bleibt, indem er seinen TTL-Wert aktualisiert (ändert). Clients, die dynamische Daten im Verzeichnis speichern, müssen diese Daten regelmäßig aktualisieren, um zu verhindern, dass sie nicht mehr angezeigt werden.

Viele Anwendungen und Dienste, die LDAP verwenden, um relativ statische und global interessante Daten von einem Active Directory-Server zu speichern und darauf zu zugreifen, würden auch weiterhin LDAP-Zugriff für ihre dynamischen Datenanforderungen verwenden. Darüber hinaus kann es für einige Anwendungen wünschenswert sein, die Aufgabe der Garbage Collection von Objekten im DS zu entfernen, die eine begrenzte Nutzungsdauer für den Verzeichnisdienst haben. Anwendungsverzeichnispartitionen (mit der Möglichkeit zur kontrollierten Platzierung von Replikaten) und objektspezifische TTLs bieten zusammen die Möglichkeit, dynamische Daten in Active Directory Domain Services zu hosten und so LDAP-Zugriff darauf zu ermöglichen.

Eine neue Hilfsobjektklasse namens **dynamicObject** mit OID = 1.3.6.1.4.1.1466.101.119.2 wird im AD-Basisschema definiert, das von dynamischen Einträgen verwendet werden soll. Diese Hilfsklasse enthält das Attribut **entryTTL** mit OID = 1.3.6.1.4.1.1466.101.119.3 als system-may-contain-Attribut. Der Wert dieses Attributs ist die "Zeit in Sekunden", in der der entsprechende Verzeichniseintrag weiterhin vorhanden ist, bevor er aus dem Verzeichnis verschwindet. Wenn der Client bei der Objekterstellung keinen expliziten Wert für dieses Attribut anliefert, stellt der DS einen Standardwert wie später angegeben zurEntspricht.

Ein neuer erweiterter LDAP-Vorgang mit OID = 1.3.6.1.4.1.1466.101.119.1 für die Clientaktualisierung eines dynamischen Eintrags im Verzeichnis wird definiert und im **supportedExtension-Attribut** des DSE-Stammobjekts veröffentlicht.

In der tatsächlichen Implementierung **ist entryTTL** ein konstruiertes Attribut. Die Tatsächliche Objektablaufzeit wird als absolute Zeit gespeichert, zu der das Objekt in einem systemspezifischen Attribut namens **ms-DS-Entry-Time-To-Live zerstört werden kann.**

Für alle dynamischen Objekte gelten die folgenden Einschränkungen:

-   Ein gelöschtes dynamisches Objekt aufgrund des Ablaufs der Tl hinterlässt keinen Tombstone.
-   Alle Dcs, die Replikate von dynamischen Objekten enthalten, müssen auf Windows Server 2003 ausgeführt werden.
-   Dynamische Einträge mit TTL-Werten werden in allen Partitionen mit Ausnahme der Partition "Configuration" und "Schema" unterstützt.
-   Active Directory Domain Services optionale **dynamicSubtrees-Attribut,** wie in RFC 2589 beschrieben, nicht im DSE-Stammobjekt veröffentlichen.
-   Dynamische Einträge werden ähnlich wie nicht dynamische Einträge behandelt, wenn Such-, Vergleichs-, Add-, Lösch-, Änderungs- und ModifyDN-Vorgänge verarbeitet werden.
-   Es gibt keine Möglichkeit, einen statischen Eintrag in einen dynamischen Eintrag zu ändern und umgekehrt.
-   Ein nicht dynamischer Eintrag kann einem dynamischen Eintrag nicht untergeordnet hinzugefügt werden.

 

 




