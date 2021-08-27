---
title: Das WinSNMP-Modell
description: Das WinSNMP-kompatible Modell umfasst die folgenden grundlegenden Komponenten.
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8814786b6ae44527460930daf5a9e8164645ca0ecfce52824831b2dbc7e61e80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127580"
---
# <a name="the-winsnmp-model"></a>Das WinSNMP-Modell

Das WinSNMP-kompatible Modell umfasst die folgenden grundlegenden Komponenten:

-   Eine WinSNMP-fähige SNMP-Netzwerkverwaltungsanwendung, also eine WinSNMP-kompatible *Anwendung*
-   Die WinSNMP-Funktionsschicht
-   Ein WinSNMP-fähiger SNMP-Dienstanbieter, also eine WinSNMP-kompatible *Implementierung*

Netzwerkverwaltungsanwendungen, die SNMP-Nachrichten übermitteln müssen, funktionieren effizient in einer ereignisgesteuerten Umgebung. Dies liegt daran, dass SNMP ein datagrambasiertes oder verbindungsloses Protokoll zwischen Remoteentitäten ist, die keine virtuellen Verbindungen herstellen.

Da Microsoft Windows Anwendungen auch ereignisgesteuert sind, verwendet WinSNMP ein Programmiermodell, bei dem der Empfang und die Verarbeitung asynchroner *Nachrichtenereignisse* Verwaltungsanwendungen steuern. Ein asynchrones Nachrichtenereignis kann eine SNMP-Vorgangsanforderung von einer Manageranwendung oder die Antwort einer Agentanwendung auf eine Anforderung sein.

SNMP sendet Anforderungen und Antworten als SNMP-Nachrichten. Eine SNMP-Nachricht ist eine SNMP-Protokolldateneinheit (PDU) sowie zusätzliche Nachrichtenheaderelemente, die von der relevanten RFC definiert werden. Weitere Informationen finden Sie unter [Informationen zu SNMP-Nachrichten,](about-snmp-messages.md) [Arbeiten mit Variablenbindungslisten](working-with-variable-binding-lists.md) und [Arbeiten mit Protokolldateneinheiten.](working-with-protocol-data-units.md)

 

 




