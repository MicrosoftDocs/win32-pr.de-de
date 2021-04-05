---
title: Funktionsweise von SNMP
description: Gibt an, wie eine Anwendung der SNMP-Verwaltungskonsole von Drittanbietern Informationen aus dem SNMP-Dienst zurückgibt.
ms.assetid: 2edbf9ff-b9e3-4103-affc-a5c0f22b80a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d58943f0765b60f9c235094642d3fa759402db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947575"
---
# <a name="how-snmp-works"></a>Funktionsweise von SNMP

In den folgenden Schritten wird beschrieben, wie die SNMP-Verwaltungs Konsolenanwendung eines Drittanbieters Informationen aus dem SNMP-Dienst zurückgibt:

1.  Die SNMP-Verwaltungs Konsolenanwendung formuliert eine SNMP-Nachricht basierend auf der Eingabe des Benutzers. Die Meldung enthält eine Protokolldaten Einheit (PDU) und Authentifizierungsinformationen. Die Verwaltungs Konsolenanwendung kann die Microsoft SNMP-Verwaltungs-API-Bibliothek (MGMTAPI.DLL) oder die Microsoft [WinSNMP-API](winsnmp-api.md) -Bibliothek (WSNMP32.DLL) verwenden, um diesen Schritt auszuführen.
2.  Die SNMP-Verwaltungs Konsolenanwendung sendet die SNMP-Nachricht mithilfe der SNMP-Dienst Bibliotheken an den SNMP-Dienst.
3.  Der SNMP-Dienst empfängt die Anforderung. Dabei werden die Authentifizierungsinformationen und die Quell-IP-Adresse überprüft.
4.  Der SNMP-Dienst wählt den geeigneten Erweiterungs-Agent aus und fordert an, dass der Agent die angeforderten Informationen abruft.
5.  Der SNMP-Dienst sendet die Antwort an die Anwendung der SNMP-Verwaltungskonsole.

 

 




