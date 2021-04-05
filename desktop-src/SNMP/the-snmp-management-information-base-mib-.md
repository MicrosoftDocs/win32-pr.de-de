---
title: Die SNMP-Verwaltungs Informationsbasis (MIB)
description: Eine Management Information Base (MIB) beschreibt einen Satz verwalteter Objekte. Eine SNMP-Verwaltungs Konsolenanwendung kann die Objekte auf einem bestimmten Computer bearbeiten, wenn der SNMP-Dienst über eine Erweiterungs-Agent-dll verfügt, die das MIB unterstützt.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba4612c026aa5a3a1a1574556f58207bad08e06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708826"
---
# <a name="the-snmp-management-information-base-mib"></a>Die SNMP-Verwaltungs Informationsbasis (MIB)

Eine Management Information Base (MIB) beschreibt einen Satz verwalteter Objekte. Eine SNMP-Verwaltungs Konsolenanwendung kann die Objekte auf einem bestimmten Computer bearbeiten, wenn der SNMP-Dienst über eine Erweiterungs-Agent-dll verfügt, die das MIB unterstützt.

Jedes verwaltete Objekt in einem MIB hat einen eindeutigen Bezeichner. Der Bezeichner enthält den Objekttyp (z. b. Counter, String, Messgerät oder Address), die Zugriffsebene des Objekts (z. b. Lese-oder Lese-/Schreibzugriff), Größenbeschränkungen und Bereichs Informationen.

Die folgende Tabelle enthält eine partielle Liste der im System enthaltenen MISB. Sie werden mit dem SNMP-Dienst im Verzeichnis% systemroot% \\ System32 installiert. Eine umfassende Auflistung von MISB finden Sie im Windows Resource Kit.



| MIB         | BESCHREIBUNG                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfiguriert. MIB    | Von Microsoft definiertes MIB, das Objekttypen zum Überwachen des Netzwerk Datenverkehrs zwischen Remote Hosts und DHCP-Servern enthält                        |
| Hostmib. MIB | Enthält Objekttypen zum Überwachen und Verwalten von Host Ressourcen.                                                                                 |
| LMMIB2. MIB  | Umfasst Arbeitsstations-und Server Dienste                                                                                                           |
| MIB \_ II. MIB | Enthält die Management Information Base (MIB-II), die eine einfache, funktionierende Architektur und ein einfaches System zum Verwalten von TCP/IP-basierten Internetinformationsdienste bereitstellt. |
| Sie. MIB    | Von Microsoft definiertes MIB für den Windows Internet Name Service (WINS)                                                                               |



 

**Windows NT:** In der Regel können Sie ein MIB aus dem SNMP-Erweiterungs-Agent kopieren, der das jeweilige MIB unterstützt. Einige zusätzliche MISB sind mit dem Windows NT 4,0 Resource Kit verfügbar.

Die Erweiterungs-Agent-DLLs für MIB-II, LAN-Manager MIB-II und die Hostressourcen-MIB werden mit dem SNMP-Dienst installiert. Die Erweiterungs-Agent-DLLs für die anderen MISB werden installiert, wenn die entsprechenden Dienste installiert sind. Beim Startzeitpunkt des dienstanseins lädt der SNMP-Dienst alle Erweiterungs-Agent-DLLs, die in der Registrierung aufgeführt sind.

Benutzer können weitere DLLs für Erweiterungs-Agents hinzufügen, die zusätzliche MIB implementieren. Zu diesem Zweck müssen Sie einen Registrierungs Eintrag für die neue dll unter dem SNMP-Dienst hinzufügen. Außerdem müssen Sie das neue MIB bei der SNMP-Verwaltungs Konsolenanwendung registrieren. Weitere Informationen finden Sie in der Dokumentation, die in ihrer Verwaltungs Konsolenanwendung enthalten ist.

Weitere Informationen finden Sie unter [MIB Name Tree](mib-name-tree.md).

 

 




