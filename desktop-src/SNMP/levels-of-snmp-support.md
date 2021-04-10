---
title: Ebenen der SNMP-Unterstützung
description: Die Microsoft WinSNMP-Implementierung bietet SNMP-Kommunikationsunterstützung auf Ebene 2.
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b48c930266073f10e5cb8019a7462317bd798c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100635"
---
# <a name="levels-of-snmp-support"></a>Ebenen der SNMP-Unterstützung

Die Microsoft WinSNMP-Implementierung bietet SNMP-Kommunikationsunterstützung auf Ebene 2. Ebene 2 unterstützt das IETF (Internet Engineering Task Force)-Standard-SNMPv2-Protokoll, wie in RFCs 1902-1908 definiert. Außerdem wird der in RFC 1901 (SNMPv2C) definierte Community-basierte Nachrichten Wrapper unterstützt.

Die Kommunikationsunterstützung auf Ebene 2 umfasst Nachrichten Codierungs-und Decodierungs Dienste, die zuvor in WinSNMP, Version 1.1 a, Unterstützung für die Ebene 0 Ebene 2 unterstützt auch alle SNMPv1-Protokoll Vorgänge, die zuvor in WinSNMP Version 1.1 a als Unterstützung für die Unterstützung von Ebene 1 bezeichnet wurden

Die-Implementierung gibt die maximale Ebene der SNMP-Kommunikation zurück, die Sie als Reaktion auf einen-Rückruf von der WinSNMP-Anwendung an die [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) -Funktion unterstützt.

Wenn die WinSNMP-Anwendung die Implementierung nur für die SNMP-Nachrichten Codierung und-Decodierung verwendet, muss die Anwendung erforderliche Transformationen durchführen, die von der Implementierung durchgeführt worden wären. Dies schließt das Übersetzen von SNMPv1 Traps ein, die von einem Rückruf der [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) -Funktion zurückgegeben werden, in SNMPv2C Traps. Es umfasst auch das Übersetzen von durch SNMPv1 definierten PDU-Typen in den entsprechenden PDU-Typ, der in Übereinstimmung mit RFC 1908 durch SNMPv2C definiert ist.

 

 




