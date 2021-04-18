---
title: Aktualisieren eines dynamischen Objekts
description: Ein Client kann die Gültigkeitsdauer (Time to Live, TTL) eines bestimmten Verzeichniseintrags aktualisieren, um ihn auf zwei Arten zu verbleiben, bevor ein LDAP-Update auf den Wert seines entryttl-Attributs durchgeführt wird, bevor der Eintrag in die Garbage Collection aufgenommen wird
ms.assetid: 5f51013c-b278-4ef7-a235-b238eed79a35
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7866c423fcb715289793a7beefa564150954257
ms.sourcegitcommit: 4d6ff888fd5825e78bc8fd5cdb21d4b542205039
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "106338103"
---
# <a name="refreshing-a-dynamic-object"></a>Aktualisieren eines dynamischen Objekts

Ein Client kann die Gültigkeitsdauer (Time to Live, TTL) eines bestimmten Verzeichniseintrags aktualisieren, um ihn auf zwei Arten aktiv zu halten:

-   Das Ausführen eines LDAP-Updates auf den Wert seines **entryttl** -Attributs vor der Garbage Collection. Diese Methode zum Aktualisieren eines dynamischen Eintrags im Verzeichnis ist eine zusätzliche (optionale) Funktion von Active Directory Domain Services, die nicht von RFC 2589 angegeben wird.
-   Ausführen eines erweiterten LDAP-Vorgangs mit der OID 1.3.6.1.4.1.1466.101.119.1 für die TTL-Aktualisierung, wie in RFC 2589 festgelegt. Diese OID ist als **erweiterte LDAP- \_ TTL-op- \_ \_ \_ OID** in winldap. H definiert.

 
* * Anmerkung * * *: dynamische Objekte werden vom Garbage Collector entfernt, wenn Sie abgelaufen sind. es gibt keine Phase des Objekts, das ein Tombstone ist, wenn es abgelaufen ist. Beim Aktualisieren von Objekten müssen Sie mit der AD-Replikations Latenz vorsichtig sein. Sie müssen sicherstellen, dass das Update zum Aktualisieren der Gültigkeitsdauer früh genug eintrifft, sodass alle Replikate des Namens Kontexts (vollständiger und globaler Katalog) die Aktualisierungs Transaktion sehen, bevor das Objekt lokal abläuft.

 




