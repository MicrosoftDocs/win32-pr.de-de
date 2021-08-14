---
title: Informationen zu SNMP-Nachrichten
description: Das Simple Network Management-Protokoll verwendet Nachrichten für die Kommunikation und den Austausch von Informationen zwischen Remote-SNMP-Entitäten.
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90c8e6aba33384ddaf16fbe847f20488f0be4d584c70563a34d052a37e80a23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009948"
---
# <a name="about-snmp-messages"></a>Informationen zu SNMP-Nachrichten

Das Simple Network Management-Protokoll verwendet Nachrichten für die Kommunikation und den Austausch von Informationen zwischen Remote-SNMP-Entitäten. SNMP-Nachrichten enthalten Protokolldateneinheiten (PDUs) sowie zusätzliche Nachrichtenheaderelemente, die von der relevanten RFC definiert werden. Ein PDU ist ein Datenpaket, das SNMP-Datenkomponenten (oder -Felder) enthält.

Das Format einer SNMP-Nachricht ist für SNMPv1 und SNMPv2C identisch. SNMPv2C unterstützt jedoch zusätzliche PDU-Typen. Beispielsweise wird der [SNMP \_ PDU \_ GETBULK-Anforderungstyp](snmp-variable-types-and-request-pdu-types.md) unterstützt, der es einer Anwendung ermöglicht, große Datenblöcke effizient aus Zielentitäten abzurufen.

 

 




