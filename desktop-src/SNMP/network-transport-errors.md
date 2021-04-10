---
title: Netzwerk Transport Fehler
description: Die Microsoft WinSNMP-Implementierung kann einen Netzwerk Transport Fehler erkennen, nachdem eine SNMP-Nachricht übermittelt wurde.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cf6b7610fbfe8d19a375bd3e3146263b9e9f0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858411"
---
# <a name="network-transport-errors"></a>Netzwerk Transport Fehler

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

Die Microsoft WinSNMP-Implementierung kann einen Netzwerk Transport Fehler erkennen, nachdem eine SNMP-Nachricht übermittelt wurde. In diesem Fall sendet die-Implementierung eine Daten Empfangs Benachrichtigung an die WinSNMP-Sitzung, die die Kommunikations Anforderung initiiert hat. Die-Implementierung gibt beim \_ nächsten Aufrufe der [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) -Funktion für die Sitzung auch einen Snmpapi-Fehler zurück. Die **snmprecvmsg** -Funktion schlägt mit einem erweiterten Fehlercode fehl, der auf einen Fehler in der Netzwerk Transportschicht hinweist.

Eine Liste der spezifischen Fehler auf der Transportschicht finden Sie auf den Referenzseiten für die Funktionen " [**snmpregiester**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)", " [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)" und " [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) ".

 

 