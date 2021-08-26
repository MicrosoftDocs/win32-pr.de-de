---
title: Die SNMP-Verwaltungsinformationsbasis (MIB)
description: Eine Verwaltungsinformationsbasis (Management Information Base, MIB) beschreibt einen Satz verwalteter Objekte. Eine SNMP-Verwaltungskonsolenanwendung kann die Objekte auf einem bestimmten Computer bearbeiten, wenn der SNMP-Dienst über eine Erweiterungs-Agent-DLL verfügt, die MIB unterstützt.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf3fac2e24b79da3ea7277010da5a3f96e3664416809bc440097f4ec0b1384e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127600"
---
# <a name="the-snmp-management-information-base-mib"></a>Die SNMP-Verwaltungsinformationsbasis (MIB)

Eine Verwaltungsinformationsbasis (Management Information Base, MIB) beschreibt einen Satz verwalteter Objekte. Eine SNMP-Verwaltungskonsolenanwendung kann die Objekte auf einem bestimmten Computer bearbeiten, wenn der SNMP-Dienst über eine Erweiterungs-Agent-DLL verfügt, die MIB unterstützt.

Jedes verwaltete Objekt in einem MIB verfügt über einen eindeutigen Bezeichner. Der Bezeichner umfasst den Typ des Objekts (z. B. Zähler, Zeichenfolge, Messgerät oder Adresse), die Zugriffsebene des Objekts (z. B. Lesen oder Lesen/Schreiben), Größenbeschränkungen und Bereichsinformationen.

Die folgende Tabelle enthält eine partielle Liste der MIBs, die mit dem System versendet werden. Sie werden mit dem SNMP-Dienst im Verzeichnis %systemroot% \\ system32 installiert. Eine vollständige Liste der MIBs finden Sie im Windows Resource Kit.



| MIB         | BESCHREIBUNG                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Dhcp. Mib    | Von Microsoft definierte MIB mit Objekttypen zum Überwachen des Netzwerkdatenverkehrs zwischen Remotehosts und DHCP-Servern                        |
| HOSTMIB. Mib | Enthält Objekttypen zum Überwachen und Verwalten von Hostressourcen.                                                                                 |
| LMMIB2. Mib  | Informationen zu Arbeitsstations- und Serverdiensten                                                                                                           |
| MIB \_ II.MIB | Enthält die Verwaltungsinformationsbasis (MIB-II), die eine einfache, funktionsfähige Architektur und ein System für die Verwaltung von TCP/IP-basierten Internets bereitstellt. |
| Gewinnt. Mib    | Von Microsoft definierte MIB für den Windows Internet name Service (WINS)                                                                               |



 

**Windows NT:** In der Regel können Sie eine MIB aus dem SNMP-Erweiterungs-Agent kopieren, der die jeweilige MIB unterstützt. Einige zusätzliche MIBs sind mit dem Windows NT 4.0 Resource Kit verfügbar.

Die Erweiterungs-Agent-DLLs für MIB-II, LAN Manager MIB-II und host resources MIB werden mit dem SNMP-Dienst installiert. Die Erweiterungs-Agent-DLLs für die anderen MIBs werden installiert, wenn die jeweiligen Dienste installiert werden. Beim Start des Diensts lädt der SNMP-Dienst alle Erweiterungs-Agent-DLLs, die in der Registrierung aufgeführt sind.

Benutzer können weitere Erweiterungs-Agent-DLLs hinzufügen, die zusätzliche MIBs implementieren. Hierzu müssen sie einen Registrierungseintrag für die neue DLL unter dem SNMP-Dienst hinzufügen. Außerdem muss der neue MIB bei der SNMP-Verwaltungskonsolenanwendung registriert werden. Weitere Informationen finden Sie in der Dokumentation, die in Ihrer Verwaltungskonsolenanwendung enthalten ist.

Weitere Informationen finden Sie unter [MIB-Namensstruktur.](mib-name-tree.md)

 

 




