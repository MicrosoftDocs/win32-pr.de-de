---
title: Ändern der Neuübertragungsrichtlinie
description: Die Microsoft WinSNMP-Implementierung bietet Unterstützung für Neuübertragungsrichtlinien, indem ein Time out-Wert und eine Wiederholungsanzahl für die WinSNMP-Anwendung in einer Datenbank gespeichert werden.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed160de40b300d1b2430304b7a487f4544fee9a13db6049d1d837958276da8e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009768"
---
# <a name="changing-the-retransmission-policy"></a>Ändern der Neuübertragungsrichtlinie

Die Microsoft WinSNMP-Implementierung bietet Unterstützung für Neuübertragungsrichtlinien, indem ein Time out-Wert und eine Wiederholungsanzahl für die WinSNMP-Anwendung in einer Datenbank gespeichert werden. Die Implementierung speichert Werte für einzelne Zielentitäten. Die Implementierung stellt anfänglich Standardwerte für diese Elemente zur Verfügung, aber eine Anwendung kann Werte für einzelne Entitäten hinzufügen oder ändern.

Ein Aufruf der Funktionen [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) und [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) gibt die Timeout- und Wiederholungsanzahlwerte für eine bestimmte Zielentität zurück. Um den Timeoutwert zu ändern, muss eine WinSNMP-Anwendung die [**SnmpSetTimeout-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) aufrufen. Um den Wert der Wiederholungsanzahl zu ändern, muss die Anwendung die [**SnmpSetRetry-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) aufrufen. Die aktualisierten Einstellungen wirken sich auf neue SNMP-Nachrichtenanforderungen an die Zielentität aus.

 

 




