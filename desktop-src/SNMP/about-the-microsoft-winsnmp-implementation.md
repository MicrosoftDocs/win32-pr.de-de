---
title: Informationen zur Microsoft WinSNMP-Implementierung
description: Die Microsoft WinSNMP-Implementierung entspricht der WinSNMP-Version 2,0.
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbf142ba85458374105af5b80ca5af30a6c5082
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947309"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a>Informationen zur Microsoft WinSNMP-Implementierung

Die Microsoft WinSNMP-Implementierung entspricht der WinSNMP-Version 2,0. Es werden alle Funktionen und Vorgänge unterstützt, die sowohl in der Version von WinSNMP, Version 1.1, als auch in den Nachtrag der WinSNMP-Version 2,0 definiert sind. Die-Implementierung stellt die folgenden Dienste für WinSNMP-Anwendungen bereit:

-   Verwaltet die Kommunikation zu und von Verwaltungs Entitäten. Die Entität kann sich auf dem lokalen Computer befinden oder über ein lokales oder weites Netzwerk oder über das Internet verbunden sein. Weitere Informationen finden Sie [Unterebenen der SNMP-Unterstützung](levels-of-snmp-support.md).
-   Blendet die Details des SNMP-Protokolls (Abstract Syntax Notation One, ASN. 1) und die grundlegenden Codierungsregeln (ber) zum Beschreiben der Übertragungs Syntax aus.
-   Überprüft die Richtigkeit von PDUs und lehnt ungültige PDUs ab. Weitere Informationen finden Sie unter [Arbeiten mit Protokolldaten Einheiten](working-with-protocol-data-units.md).
-   Wandelt SNMPv2C PDU-Typen bei Bedarf in Übereinstimmung mit den entsprechenden RFCs um.
-   Konvertiert SNMPv1 Traps von einem SNMPv1-Agent in SNMPv2C Traps in Übereinstimmung mit RFC 1908, "Koexistenz zwischen Version 1 und Version 2 des Internet-Standard-Netzwerk Verwaltungs-Frameworks". Weitere Informationen finden Sie unter Translation [Traps from SNMPv1 to SNMPv2C](translating-traps-from-snmpv1-to-snmpv2c.md).
-   Unterstützt die Neuübertragungs Richtlinie der Anwendung und bietet Unterstützung für die erneute Übertragungs Ausführung. Weitere Informationen finden Sie in [der WinSNMP-Datenbank](the-winsnmp-database.md) und Informationen [zur erneuten Übertragung](about-retransmission.md).
-   Stellt Entitäts-und Kontext Übersetzungsunterstützung für die Anwendung bereit. Weitere Informationen finden Sie in [der WinSNMP-Datenbank](the-winsnmp-database.md) und [Festlegen des Entitäts-und Kontext Übersetzungsmodus](setting-the-entity-and-context-translation-mode.md).

Weitere Informationen zur Beziehung zwischen einer WinSNMP-Anwendung und der-Implementierung finden Sie unter [WinSNMP-Datenverwaltung Konzepte](winsnmp-data-management-concepts.md) und [WinSNMP-Sitzungen](winsnmp-sessions.md).

 

 




