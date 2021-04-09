---
title: Trap-Formate
description: Das Format von Trap-PDUs unterscheidet sich von dem anderer PDUs. Das Format von SNMPv1 Traps und SNMPv2C Traps ist ebenfalls unterschiedlich.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87adc3222808fcc7e81904ade07c09afa13bc6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036617"
---
# <a name="trap-formats"></a>Trap-Formate

Das Format von Trap-PDUs unterscheidet sich von dem anderer PDUs. Das Format von SNMPv1 Traps und SNMPv2C Traps ist ebenfalls unterschiedlich.

Im SNMPv2C Framework ist das PDU-Trap-Format eine Variablen Bindungs Liste von *n* Variablen Bindungs Einträgen, die folgendermaßen organisiert sind:

-   Der erste Variablen Bindungs Eintrag enthält einen Zeitstempel.
-   Der zweite Variablen Bindungs Eintrag ist ein Objekt Bezeichner, der den Trap identifiziert.
-   Die dritten bis *n* Variablen Bindungs Einträge enthalten ggf. zusätzliche Informationen, die mit dem Trap verknüpft sind.

Im SNMPv1 Framework lautet das PDU-Trap Format wie folgt.

| Feld                      | BESCHREIBUNG                                                      |
|----------------------------|------------------------------------------------------------------|
| Enterprise                 | Identifiziert den Typ des Geräts, das den Trap generiert hat.           |
| Agent-addr                 | Gibt die IP-Adresse des Geräts an, von dem der Trap generiert wurde. |
| generischer Trap/spezifischer Trap | Identifiziert einen vordefinierten Trap-Typ.                               |
| Zeitstempel                 | Gibt an, wann der Trap generiert wurde.                          |
| Variablen Bindungen          | Enthält zusätzliche Informationen, die mit dem Trap verknüpft sind.        |



 

Die [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) -Funktion gibt immer eine Nachricht im SNMPv2C-Format zurück. Wenn die Nachricht den Vorgangstyp **SNMP \_ PDU \_ Trap** enthält, kann die Anwendung die Variablen Bindungs Einträge der Nachricht lesen und die dem Trap zugeordneten Informationen abrufen.

 

 




