---
title: Informationen zu SNMP-Nachrichten
description: Das Simple Network Management-Protokoll verwendet Nachrichten zum kommunizieren und Austauschen von Informationen zwischen Remote-SNMP-Entitäten.
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0426bf44d976ddf9e2eafe2093dcea94956cb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388115"
---
# <a name="about-snmp-messages"></a>Informationen zu SNMP-Nachrichten

Das Simple Network Management-Protokoll verwendet Nachrichten zum kommunizieren und Austauschen von Informationen zwischen Remote-SNMP-Entitäten. SNMP-Nachrichten enthalten Protokolldaten Einheiten (PDUs) sowie zusätzliche Nachrichten Header Elemente, die durch die relevante RFC definiert werden. Bei einem PDU handelt es sich um ein Datenpaket, das SNMP-Daten Komponenten (oder Felder) enthält.

Das Format einer SNMP-Nachricht ist für SNMPv1 und SNMPv2C identisch. SNMPv2C unterstützt jedoch zusätzliche PDU-Typen. Beispielsweise wird der [SNMP \_ PDU \_ Getbulk](snmp-variable-types-and-request-pdu-types.md) -Anforderungstyp unterstützt, mit dem eine Anwendung große Datenblöcke aus Ziel Entitäten effizient abrufen kann.

 

 




