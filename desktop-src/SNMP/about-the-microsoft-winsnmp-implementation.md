---
title: Informationen zur Microsoft WinSNMP-Implementierung
description: Die Microsoft WinSNMP-Implementierung entspricht WinSNMP Version 2.0.
ms.assetid: 99e11d30-d159-4d9b-94d0-baa6e49d82cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693a2fd5c6aa21d684d485f75b04160e72bfe1455c13ef8c320c863b61ab696b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009868"
---
# <a name="about-the-microsoft-winsnmp-implementation"></a>Informationen zur Microsoft WinSNMP-Implementierung

Die Microsoft WinSNMP-Implementierung entspricht WinSNMP Version 2.0. Es unterstützt alle Funktionen und Vorgänge, die sowohl in der WinSNMP-Version 1.1a-Spezifikation als auch im WinSNMP-Nachtrag 2.0 definiert sind. Die Implementierung stellt die folgenden Dienste für WinSNMP-Anwendungen bereit:

-   Verwaltet die Kommunikation mit und von Verwaltungsentitäten. Die Entität kann sich auf dem lokalen Computer befinden oder über ein lokales Netzwerk oder ein Wide Area Network oder das Internet verbunden sein. Weitere Informationen finden Sie unter [Ebenen der SNMP-Unterstützung.](levels-of-snmp-support.md)
-   Blendet die Details des SNMP-Protokolls, der abstrakten Syntax notation One (ASN.1) und der Grundlegenden Codierungsregeln (BER) zum Beschreiben der Übertragungssyntax aus.
-   Überprüft die Richtigkeit von PDUs und lehnt ungültige PDUs ab. Weitere Informationen finden Sie unter [Arbeiten mit Protokolldateneinheiten.](working-with-protocol-data-units.md)
-   Transformiert SNMPv2C-PDU-Typen bei Bedarf in Übereinstimmung mit den relevanten RFCs.
-   Konvertiert SNMPv1-Traps von einem SNMPv1-Agent in SNMPv2C-Traps gemäß RFC 1908, "Koexistenz zwischen Version 1 und Version 2 des Internetstandard-Netzwerkverwaltungsframeworks". Weitere Informationen finden Sie unter [Übersetzen von Traps von SNMPv1 in SNMPv2C.](translating-traps-from-snmpv1-to-snmpv2c.md)
-   Unterstützt die Neuübertragungsrichtlinie der Anwendung und bietet Unterstützung für die Ausführung von Neuübertragungen. Weitere Informationen finden Sie unter [Die WinSNMP-Datenbank](the-winsnmp-database.md) und [Informationen zur neu übertragenen](about-retransmission.md).
-   Stellt Entitäts- und Kontextübersetzungsunterstützung für die Anwendung bereit. Weitere Informationen finden Sie unter [Die WinSNMP-Datenbank](the-winsnmp-database.md) und [Festlegen des Entitäts- und Kontextübersetzungsmodus.](setting-the-entity-and-context-translation-mode.md)

Weitere Informationen zur Beziehung zwischen einer WinSNMP-Anwendung und der Implementierung finden Sie unter [WinSNMP Datenverwaltung Concepts](winsnmp-data-management-concepts.md) and [WinSNMP Sessions](winsnmp-sessions.md).

 

 




