---
title: Ebenen der SNMP-Unterstützung
description: Die Microsoft WinSNMP-Implementierung bietet SNMP-Kommunikationsunterstützung auf Ebene 2.
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa76a475ed266a7a4928a79f809b7011a537c777c89ea0a97d06983d6656a9ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009458"
---
# <a name="levels-of-snmp-support"></a>Ebenen der SNMP-Unterstützung

Die Microsoft WinSNMP-Implementierung bietet SNMP-Kommunikationsunterstützung auf Ebene 2. Ebene 2 unterstützt das SNMPv2-Standardprotokoll der Internet Engineering Task Force (IETF), wie in RFCs 1902-1908 definiert. Außerdem wird der communitybasierte Nachrichtenwrapper gemäß RFC 1901 (SNMPv2C) unterstützt.

Die Kommunikationsunterstützung auf Ebene 2 umfasst Nachrichtencodierungs- und Decodierungsdienste, die zuvor in WinSNMP Version 1.1a als Kommunikationsunterstützung auf Ebene 0 bezeichnet wurden. Ebene 2 unterstützt auch alle SNMPv1-Protokollvorgänge, zuvor als Level 1-Kommunikationsunterstützung in WinSNMP Version 1.1a bezeichnet.

Die Implementierung gibt die maximale Ebene der SNMP-Kommunikation zurück, die sie als Reaktion auf einen Aufruf der WinSNMP-Anwendung an die [**SnmpStartup-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) unterstützt.

Wenn die WinSNMP-Anwendung die -Implementierung nur für die SNMP-Nachrichtencodierung und -Decodierung verwendet, muss die Anwendung die erforderlichen Transformationen ausführen, die die Implementierung durchgeführt hätte. Dies umfasst das Übersetzen von SNMPv1-Traps, die durch einen Aufruf der [**SnmpRecvMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) zurückgegeben werden, in SNMPv2C-Traps. Sie umfasst auch die Übersetzung von PDU-Typen, die von SNMPv1 definiert werden, in den relevanten PDU-Typ, der von SNMPv2C gemäß RFC 1908 definiert wird.

 

 




