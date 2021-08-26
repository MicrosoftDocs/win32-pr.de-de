---
title: Trapformate
description: Das Format von Trap-PDUs unterscheidet sich von dem anderer PDUs. Das Format von SNMPv1-Traps und SNMPv2C-Traps unterscheidet sich ebenfalls.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b73e9cd2a5396bbe258fcb67c88cc207ea0243a9e8aff9f31e4866b9ee8adcc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885680"
---
# <a name="trap-formats"></a>Trapformate

Das Format von Trap-PDUs unterscheidet sich von dem anderer PDUs. Das Format von SNMPv1-Traps und SNMPv2C-Traps unterscheidet sich ebenfalls.

Unter dem SNMPv2C-Framework ist das PDU-Trapformat eine Variablenbindungsliste mit *n* Variablenbindungseinträgen, die wie folgt organisiert sind:

-   Der erste Variablenbindungseintrag enthält einen Zeitstempel.
-   Der zweite Variablenbindungseintrag ist ein Objektbezeichner, der den Trap identifiziert.
-   Die Dritten bis *n* Variablenbindungseinträge enthalten, sofern vorhanden, zusätzliche Informationen, die dem Trap zugeordnet sind.

Unter dem SNMPv1-Framework lautet das PDU-Trapformat wie folgt.

| Feld                      | BESCHREIBUNG                                                      |
|----------------------------|------------------------------------------------------------------|
| Enterprise                 | Gibt den Typ des Geräts an, das den Trap generiert hat.           |
| agent-addr                 | Identifiziert die IP-Adresse des Geräts, das den Trap generiert hat. |
| generic-trap/specific-trap | Identifiziert einen vordefinierten Traptyp.                               |
| Zeitstempel                 | Gibt an, wann der Trap generiert wurde.                          |
| Variablenbindungen          | Enthält zusätzliche Informationen, die dem Trap zugeordnet sind.        |



 

Die [**SnmpRecvMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) gibt immer eine Nachricht im SNMPv2C-Format zurück. Wenn die Nachricht den Vorgangstyp **SNMP \_ PDU \_ TRAP** enthält, kann die Anwendung die Variablenbindungseinträge der Nachricht lesen und die dem Trap zugeordneten Informationen abrufen.

 

 




