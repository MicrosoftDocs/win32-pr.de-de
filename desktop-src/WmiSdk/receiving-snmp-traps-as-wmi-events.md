---
description: WMI ordnet SNMP-Traps automatisch WMI-Ereignissen zu. Das System platziert die im Trap enthaltenen Daten in den entsprechenden Eigenschaften einer WMI-Ereignis Instanz für den Zugriff durch den WMI-Host Computer.
ms.assetid: 549f58a9-9d3b-41b9-a374-ab83877f63a7
ms.tgt_platform: multiple
title: Empfangen von SNMP-Traps als WMI-Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da24be8ea9a4882af0b961b1d0f6f0c3d442c70c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528508"
---
# <a name="receiving-snmp-traps-as-wmi-events"></a>Empfangen von SNMP-Traps als WMI-Ereignisse

WMI ordnet SNMP-Traps automatisch WMI-Ereignissen zu. Das System platziert die im Trap enthaltenen Daten in den entsprechenden Eigenschaften einer WMI-Ereignis Instanz für den Zugriff durch den WMI-Host Computer.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

Das Empfangen eines SNMP-Traps ist nahezu identisch mit dem Empfang von Ereignissen von einem beliebigen anderen WMI-Anbieter. Der SNMP-Ereignis Filter hat jedoch mehrere eindeutige Klassen, die Sie beachten sollten, bevor Sie sich für Ereignisse registrieren. Außerdem erfordert der Ereignis Anbieter ausschließlich die Verwendung des \\ SMIR-Namespace.

Die gängigsten Klassen für die Registrierung bei sind [SnmpNotification](snmpnotification.md) und [snmpextendednotification](snmpextendednotification.md). Consumer, die Ereignis Benachrichtigungen verwenden, um Werte in überwachten SNMP-Geräten zu aktualisieren, müssen sich für snmpextendednotification-Ereignisse registrieren. Die Informationen aus SnmpNotification-Ereignissen sind nicht wiederverwendbar.

In der folgenden Tabelle sind Informationen zum Einrichten des Computers zum Empfangen von SNMP-Traps als WMI-Ereignisse aufgeführt.



| Aufgabe                                                                               | BESCHREIBUNG                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Auswählen zwischen SNMP-Ereignis Anbietern](choosing-between-snmp-event-providers.md) | WMI umfasst zwei SNMP-Ereignis Anbieter.                                             |
| [Empfangen von SNMP-Ereignissen](receiving-snmp-events.md)                                 | SNMP-Ereignis Anbieter unterstützen drei Arten von SNMPv1 Traps und SNMPv2-Benachrichtigungen. |



 

Im folgenden Beispiel wird ein Computer festgelegt, der für das **snmplinkupnotification** -Ereignis von einem verwalteten Hub überwacht werden soll.


```VB
Set objLocator = CreateObject("wbemscripting.swbemlocator")
Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")

set objwbemEventsource = _ 
    objServices.ExecNotificationQuery _
   ("SELECT * FROM SnmpLinkUpNotification")

set objWbemObject = objwbemEventsource.NextEvent()

wscript.echo "Received " & objWbemObject.path_.class

for each prop in objWbemObject.properties_
    wscript.echo prop.name & " -- " & prop.value
next
```



 

 



