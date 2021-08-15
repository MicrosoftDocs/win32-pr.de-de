---
title: Aktualisieren eines dynamischen Objekts
description: 'Ein Client kann die Lebenszeit (Time To Live, TTL) eines bestimmten Verzeichniseintrags aktualisieren, um ihn auf zwei Arten zu erhalten: Durchführen einer LDAP-Aktualisierung des Werts seines entryTTL-Attributs vor der Garbage Collection des Eintrags.'
ms.assetid: 5f51013c-b278-4ef7-a235-b238eed79a35
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c351b559da8d08ccca3346f7126a9bbe47fcd3774486ea64a8dff29ac7e799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025177"
---
# <a name="refreshing-a-dynamic-object"></a>Aktualisieren eines dynamischen Objekts

Ein Client kann die Lebenszeit (Time To Live, TTL) eines bestimmten Verzeichniseintrags aktualisieren, um ihn auf zwei Arten zu erhalten:

-   Durchführen einer LDAP-Aktualisierung des Werts des **entryTTL-Attributs,** bevor der Eintrag garbage collected wird. Diese Methode zum Aktualisieren eines dynamischen Eintrags im Verzeichnis ist ein zusätzliches (optionales) Feature von Active Directory Domain Services, das nicht von RFC 2589 angegeben wird.
-   Ausführen eines erweiterten LDAP-Vorgangs mit der OID 1.3.6.1.4.1.1466.101.119.1 für die TTL-Aktualisierung, wie in RFC 2589 festgelegt. Diese OID ist als **LDAP \_ TTL \_ EXTENDED OP \_ \_ OID** in WINLDAP.H definiert.

 
**Hinweis:: Dynamische Objekte werden vom Garbage Collector entfernt, wenn sie abgelaufen sind. Es gibt keine Phase, in der das Objekt ein Tombstone ist, wenn es abgelaufen ist. Beim Aktualisieren von Objekten müssen Sie mit der AD-Replikationslatenz vorsichtig sein. Sie müssen sicherstellen, dass das Update zum Aktualisieren der Tl so früh eintrifft, dass alle Replikate des Namenskontexts (vollständiger und globaler Katalog) die Aktualisierungstransaktion sehen, bevor das Objekt lokal abläuft.

 




