---
description: SNMP-Ereignisanbieter empfangen SNMP-Ereignispakete aus dem WINSNMP-Stapel und übersetzen die in den Paketen enthaltenen Informationen in WMI-Ereignisse.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Auswählen zwischen SNMP-Ereignisanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0902c463ee0fc51505e125a329f592ebced6df20ec7f63296ba7248cd8dade98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131873"
---
# <a name="choosing-between-snmp-event-providers"></a>Auswählen zwischen SNMP-Ereignisanbietern

SNMP-Ereignisanbieter empfangen SNMP-Ereignispakete aus dem WINSNMP-Stapel und übersetzen die in den Paketen enthaltenen Informationen in WMI-Ereignisse.

WMI umfasst die folgenden beiden SNMP-Ereignisanbieter:

-   SNMP-Anbieter für gekapselte Ereignisse (SEEP)

    Gekapselte Bereitstellung bedeutet, dass die Ereignisinstanz über einfache Eigenschaften verfügt, die die Informationen beschreiben, die direkt aus dem SNMP-Trap zugeordnet sind.

-   SNMP-Referenzereignisanbieter (SREP)

    Die Referenzbereitstellung abstrahiert die informationen, die im SNMP-Trap vorhanden sind, sodass Eigenschaften, die dieselbe Klasse und Instanz gemeinsam haben, als eingebettete Objekte dargestellt werden. Dadurch kann die eindeutige Instanz, der der Trap zugeordnet ist, nach dem Empfang des Ereignisses mithilfe von SNMP \_ \_ RELPATH abgerufen werden.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

Unabhängig davon, ob das SNMP-Ereignis ein SNMPv1-Trap oder eine SNMPv2C-Benachrichtigung ist, meldet der Stapel es als SNMPv2-Benachrichtigung. Daher verarbeiten die Ereignisanbieter alle SNMP-Ereignisse als SNMPv2-Benachrichtigungen.

Um die SNMP-Ereignisse für WMI-Consumers zu beschreiben, unterstützt jeder Ereignisanbieter eine Hierarchie von Klassen, die von der [**\_ \_ ExtrinsicEvent-Systemklasse**](--extrinsicevent.md) ableiten. Die [SNMPNotification-Klasse](snmpnotification.md) ist die übergeordnete Klasse für die SEEP-Hierarchie. Die [SNMPExtendedNotification-Klasse](snmpextendednotification.md) ist die übergeordnete Klasse für die SREP-Hierarchie.

 

 



