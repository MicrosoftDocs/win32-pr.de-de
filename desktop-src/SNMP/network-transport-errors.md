---
title: Netzwerktransportfehler
description: Die Microsoft WinSNMP-Implementierung kann einen Netzwerktransportfehler erkennen, nachdem eine SNMP-Nachricht übertragen wurde.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15284bba97f2dda8d2fb4224dc2c94bd14050afb9463c73b4d297c1647ec273f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009308"
---
# <a name="network-transport-errors"></a>Netzwerktransportfehler

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows Remoteverwaltung,](/windows/desktop/WinRM/portal)bei der es sich um die Microsoft-Implementierung von WS-Man handelt.\]

Die Microsoft WinSNMP-Implementierung kann einen Netzwerktransportfehler erkennen, nachdem eine SNMP-Nachricht übertragen wurde. In diesem Fall sendet die Implementierung eine Datenbestätigungsbenachrichtigung an die WinSNMP-Sitzung, die die Kommunikationsanforderung initiiert hat. Die Implementierung gibt auch SNMPAPI \_ FAILURE beim nächsten Aufruf der [**SnmpRecvMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) für die Sitzung zurück. Die **SnmpRecvMsg-Funktion** schlägt mit einem erweiterten Fehlercode fehl, der auf einen Netzwerktransportebenenfehler hinweist.

Eine Liste der spezifischen Transportebenenfehler finden Sie auf den Referenzseiten für die Funktionen [**SnmpRegister,**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)und [**SnmpRecvMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)

 

 