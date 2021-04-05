---
title: Arbeiten mit Protokolldaten Einheiten
description: Das Simple Network Management-Protokoll (SNMP) sendet Vorgangs Anforderungen und-Antworten als SNMP-Nachrichten.
ms.assetid: 0928981c-4d60-4583-9eef-8127e05b1ba8
keywords:
- Arbeiten mit Protokolldaten Einheiten SNMP
- Protokolldaten Einheiten SNMP, arbeiten mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e40f36fa28f7ff17974d79f4f8ac29b8b6130b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037281"
---
# <a name="working-with-protocol-data-units"></a>Arbeiten mit Protokolldaten Einheiten

Das Simple Network Management-Protokoll (SNMP) sendet Vorgangs Anforderungen und-Antworten als SNMP-Nachrichten. Eine SNMP-Nachricht ist eine SNMP-Protokolldaten Einheit (PDU) und zusätzliche Nachrichten Header Elemente, die durch die relevante RFC definiert werden. Ein PDU enthält eine Variablen Bindungs Liste.

Die Struktur eines PDU ist auf die Microsoft WinSNMP-Implementierung beschränkt. Eine WinSNMP-Anwendung kann mit einem Handle des Typs **hsnmp \_ PDU** auf ein PDU zugreifen. Die WinSNMP-Anwendung muss ein PDU erstellen, bevor Sie die Funktion [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) oder die Funktion [**snmpencodemsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) aufruft.

Die Anwendung kann die Datenelemente eines PDU extrahieren und aktualisieren und die für PDUs zugewiesenen Ressourcen freigeben. Um diese Vorgänge auszuführen, verwendet die Anwendung die-Funktionen von WinSNMP [PDU](winsnmp-functions.md). In der folgenden Tabelle sind Themen aufgeführt, in denen die Arbeit mit PDUs in der WinSNMP-Programmierumgebung erläutert wird.



| Thema                                                                        | BESCHREIBUNG                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Erstellen eines PDU](creating-a-pdu.md)                                         | Hier wird beschrieben, wie ein PDU erstellt wird.                                     |
| [Aktualisieren eines PDU](updating-a-pdu.md)                                         | Hier wird beschrieben, wie PDU-Felder abgerufen und aktualisiert werden.                   |
| [Duplizieren eines PDU](duplicating-a-pdu.md)                                   | Beschreibt, wie ein PDU dupliziert wird.                                  |
| [Validieren eines PDU](validating-a-pdu.md)                                     | Beschreibt die Validierung eines PDU.                                 |
| [Übereinstimmende Antworten und Anforderungs-PDUs](matching-response-and-request-pdus.md) | Beschreibt den Prozess der Übereinstimmung eines Antwort-PDU an eine Anforderungs-PDU. |



 

Weitere Informationen finden Sie unter [Arbeiten mit Variablen Bindungs Listen](working-with-variable-binding-lists.md) und [Ressourcen handle-Objekten](resource-handle-objects.md).

 

 




