---
title: Das WinSNMP-Modell
description: Das WinSNMP-kompatible Modell umfasst die folgenden grundlegenden Komponenten.
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7ae4fa1c1ee56fc534e4aa4c9bffefb8d7f4d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036618"
---
# <a name="the-winsnmp-model"></a>Das WinSNMP-Modell

Das WinSNMP-kompatible Modell umfasst die folgenden grundlegenden Komponenten:

-   Eine mit WinSNMP aktivierte SNMP-Netzwerk Verwaltungs Anwendung, d. h. eine WinSNMP-kompatible *Anwendung*
-   Die WinSNMP-Funktionsebene
-   Einen WinSNMP-aktivierten SNMP-Dienstanbieter, d. h. eine WinSNMP-kompatible *Implementierung*

Netzwerk Verwaltungs Anwendungen, die SNMP-Nachrichten vermitteln müssen, funktionieren effizient in einer ereignisgesteuerten Umgebung. Dies liegt daran, dass SNMP ein datagrammbasiertes oder verbindungsloses Protokoll zwischen Remote Entitäten ist, die keine virtuellen Verbindungen einrichten.

Da Microsoft Windows-Anwendungen auch ereignisgesteuert sind, verwendet WinSNMP ein Programmiermodell, bei dem das empfangen und Verarbeiten von Anwendungen für die Verwaltung von asynchronen *Nachrichten Ereignissen* erfolgt. Ein asynchrones Nachrichten Ereignis kann eine SNMP-Vorgangs Anforderung von einer Manager-Anwendung oder die Antwort auf eine Anforderung durch eine Agent-Anwendung sein.

SNMP sendet Anforderungen und Antworten als SNMP-Nachrichten. Eine SNMP-Nachricht ist eine SNMP-Protokolldaten Einheit (PDU) und zusätzliche Nachrichten Header Elemente, die durch die relevante RFC definiert werden. Weitere Informationen finden Sie unter Informationen [zu SNMP-Nachrichten](about-snmp-messages.md), [Arbeiten mit Variablen Bindungs Listen](working-with-variable-binding-lists.md) und [Arbeiten mit Protokolldaten Einheiten](working-with-protocol-data-units.md).

 

 




