---
description: SNMP-Ereignis Anbieter empfangen SNMP-Ereignis Pakete vom WinSNMP-Stapel und übersetzen die Informationen, die in den Paketen enthalten sind, in WMI-Ereignisse.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Auswählen zwischen SNMP-Ereignis Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dabd8f6d432025406a5faecc3ace423cd6671e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352227"
---
# <a name="choosing-between-snmp-event-providers"></a>Auswählen zwischen SNMP-Ereignis Anbietern

SNMP-Ereignis Anbieter empfangen SNMP-Ereignis Pakete vom WinSNMP-Stapel und übersetzen die Informationen, die in den Paketen enthalten sind, in WMI-Ereignisse.

WMI umfasst die folgenden zwei SNMP-Ereignis Anbieter:

-   SNMP-gekapselter Ereignis Anbieter (SEEP)

    Gekapselte Bereitstellung bedeutet, dass die Ereignis Instanz einfache Eigenschaften hat, die die direkt aus dem SNMP-Trap zugeordneten Informationen beschreiben

-   SNMP-Referenz Ereignis Anbieter (SREP)

    Die Bereitstellung von Referenten abstrahiert die Informationen, die innerhalb des SNMP-Traps vorhanden sind, sodass Eigenschaften, die dieselbe Klasse und Instanz gemeinsam verwenden, als eingebettete Objekte Dadurch kann die eindeutige Instanz, mit der der Trap verknüpft ist, nach dem Empfang des Ereignisses mit dem SNMP- \_ \_ RelPath abgerufen werden.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

Unabhängig davon, ob es sich bei dem SNMP-Ereignis um eine SNMPv1 Trap oder eine SNMPv2C-Benachrichtigung handelt, meldet der Stapel Sie als SNMPv2-Benachrichtigung. Aus diesem Grund verarbeiten die Ereignis Anbieter alle SNMP-Ereignisse als SNMPv2-Benachrichtigungen.

Um die SNMP-Ereignisse für WMI-Consumer zu beschreiben, unterstützt jeder Ereignis Anbieter eine Hierarchie von Klassen, die von der [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) -System Klasse abgeleitet wird. Die [SnmpNotification](snmpnotification.md) -Klasse ist die übergeordnete Klasse für die-Hierarchie. die [snmpextendednotification](snmpextendednotification.md) -Klasse ist die übergeordnete Klasse der SREP-Hierarchie.

 

 



