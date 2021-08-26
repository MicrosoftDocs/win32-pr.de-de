---
title: Systemdateien für SNMP
description: In der folgenden Tabelle werden die Prinzipaldateien beschrieben, die sich auf den SNMP-Dienst beziehen.
ms.assetid: 513d7c75-2f68-4d7d-897f-493089f045cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 139b83a2d2117af693bcd7ae624ff18d7a18ab5618c9a9597c1e142f62aba07d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886050"
---
# <a name="system-files-for-snmp"></a>Systemdateien für SNMP

In der folgenden Tabelle werden die Prinzipaldateien beschrieben, die sich auf den SNMP-Dienst beziehen.



| Dateiname     | BESCHREIBUNG                                                                                                                                                                                                                         |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCPMIB.DLL  | Erweiterungs-Agent-DLL, die den von Microsoft definierten DHCP-MIB implementiert. Nur auf DHCP-Servern installiert.                                                                                                                                 |
| EVNTAGNT.DLL | SNMP-DLL, die Ereignisprotokolle in SNMP-Traps übersetzt. wird auch als SNMP-Ereignisübersetzung bezeichnet.                                                                                                                                       |
| HOSTMIB.DLL  | Erweiterungs-Agent-DLL, die den MIB für Hostressourcen implementiert.                                                                                                                                                                         |
| LMMIB2.DLL   | Erweiterungs-Agent-DLL, die LAN-Manager MIB-II implementiert.                                                                                                                                                                             |
| MGMTAPI.DLL  | Microsoft SNMP Verwaltungs-API Bibliothek. Diese API ermöglicht es SNMP-Manager-Anwendungen, auf SNMP-Manager-Anforderungen zu lauschen und Anforderungen an SNMP-Agents zu senden und Antworten von diesen zu empfangen.                                                |
| Mib. BIN      | Kompilierte MIB-Informationen, die von MGMTAPI.DLL.                                                                                                                                                                                       |
| SNMP.EXE     | SNMP-Dienst. Dies ist der Master-Agent, der SNMP-Anforderungen empfängt und diese an die entsprechende Erweiterungs-Agent-DLL übergibt.                                                                                                        |
| SNMPAPI.DLL  | Dll der SNMP-Hilfsprogramme, die von DLLs und Manager-Anwendungen des SNMP-Erweiterungs-Agents verwendet wird. Diese DLL enthält ein Framework für die Entwicklung von Erweiterungs-Agent-DLLs.                                                                                   |
| SNMPSNAP.DLL | SNMP-Konfigurationsanwendung, die eine Microsoft Management Console (MMC)-Snap-In-Komponente ist. Das Snap-In fügt dem Blatt mit den SNMP-Diensteigenschaften mehrere Seiten hinzu. Weitere Informationen finden Sie in der Onlinehilfe für den SNMP-Dienst. |
| SNMPTRAP.EXE | SNMP-Trapdienst. Empfängt SNMP-Traps und gibt sie an SNMP-Manager-Anwendungen weiter.                                                                                                                                              |
| WINSMIB.DLL  | Erweiterungs-Agent-DLL, die den von Microsoft definierten WINS MIB implementiert. Nur auf WINS-Servern installiert.                                                                                                                                 |
| WSNMP32.DLL  | Microsoft [WinSNMP-API-Bibliothek.](winsnmp-api.md) Diese API ermöglicht es SNMP-Manager-Anwendungen, auf SNMP-Manager-Anforderungen zu lauschen und Anforderungen an SNMP-Agents zu senden und Antworten von diesen zu empfangen.                                     |



 

Weitere Informationen finden Sie unter [The SNMP Management Information Base (MIB) .](the-snmp-management-information-base-mib-.md) (Sie können sich auch auf das Windows 2000 Resource Kit beziehen.)

 

 




