---
title: System Dateien für SNMP
description: In der folgenden Tabelle werden die Prinzipal Dateien beschrieben, die sich auf den SNMP-Dienst beziehen.
ms.assetid: 513d7c75-2f68-4d7d-897f-493089f045cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb917276fd807835fea703ec27cc66a0d493766d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471100"
---
# <a name="system-files-for-snmp"></a>System Dateien für SNMP

In der folgenden Tabelle werden die Prinzipal Dateien beschrieben, die sich auf den SNMP-Dienst beziehen.



| Dateiname     | BESCHREIBUNG                                                                                                                                                                                                                         |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DHCPMIB.DLL  | Erweiterungs-Agent-dll, die das von Microsoft definierte DHCP-MIB implementiert. Nur auf DHCP-Servern installiert.                                                                                                                                 |
| EVNTAGNT.DLL | SNMP-dll, die Ereignisprotokolle in SNMP-Traps übersetzt. wird auch als SNMP-Ereignis Übersetzung bezeichnet.                                                                                                                                       |
| HOSTMIB.DLL  | Erweiterungs-Agent-dll, die den Host Ressourcen-MIB implementiert.                                                                                                                                                                         |
| LMMIB2.DLL   | Erweiterungs-Agent-dll, die LAN-Manager MIB-II implementiert.                                                                                                                                                                             |
| MGMTAPI.DLL  | Microsoft SNMP-Verwaltungs-API-Bibliothek. Diese API ermöglicht es SNMP-Manager-Anwendungen, SNMP-Manager-Anforderungen zu "lauschen" und Anforderungen zu senden und Antworten von SNMP-Agents zu erhalten.                                                |
| MIB. BIN      | Kompilierte MIB-Informationen, die MGMTAPI.DLL verwendet werden.                                                                                                                                                                                       |
| SNMP.EXE     | SNMP-Dienst. Dies ist der Master-Agent, der SNMP-Anforderungen empfängt und Sie an die entsprechende Erweiterungs-Agent-dll übergibt.                                                                                                        |
| SNMPAPI.DLL  | Die von SNMP-Erweiterungs-Agent-DLLs und Manager-Anwendungen verwendete DLL der SNMP-Hilfsprogramme. Diese DLL enthält ein Framework zum Entwickeln von Erweiterungs-Agent-DLLs.                                                                                   |
| SNMPSNAP.DLL | SNMP-Konfigurationsanwendung, die eine Microsoft Management Console (MMC)-Snap-in-Komponente ist. Das Snap-in fügt dem Eigenschaften Blatt für den SNMP-Dienst mehrere Seiten hinzu. Weitere Informationen finden Sie in der Online Hilfe zum SNMP-Dienst. |
| SNMPTRAP.EXE | SNMP-Trap Dienst. Empfängt SNMP-Traps und leitet Sie an SNMP-Manager-Anwendungen weiter.                                                                                                                                              |
| WINSMIB.DLL  | Erweiterungs-Agent-dll, die das von Microsoft definierte WINS-MIB implementiert. Nur auf WINS-Servern installiert.                                                                                                                                 |
| WSNMP32.DLL  | Microsoft [WinSNMP-API](winsnmp-api.md) -Bibliothek. Diese API ermöglicht es SNMP-Manager-Anwendungen, SNMP-Manager-Anforderungen zu "lauschen" und Anforderungen zu senden und Antworten von SNMP-Agents zu erhalten.                                     |



 

Weitere Informationen finden Sie in [der SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md). (Sie können auch auf das Windows 2000 Resource Kit verweisen.)

 

 




