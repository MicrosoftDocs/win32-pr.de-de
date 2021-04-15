---
description: Auf SNMP-Geräte können Sie zugreifen, indem Sie im WMI-SMIR (SNMP-modulinformationenrepository) aus der entsprechenden Klasseninstanz lesen oder in ihr schreiben.
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: Lesen und Schreiben von SNMP-Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc25f384d499e16e19c5e909f7d091ea34f9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528604"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a>Lesen und Schreiben von SNMP-Geräten

Auf SNMP-Geräte können Sie zugreifen, indem Sie im WMI-SMIR (SNMP-modulinformationenrepository) aus der entsprechenden Klasseninstanz lesen oder in ihr schreiben. Wenn Sie mit mehreren Geräten desselben Typs arbeiten, laden Sie aus Effizienzgründen die MIB-Daten für einen SNMP-Gerätetyp in SMIR.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

Wählen Sie eine der folgenden Optionen aus, um jeden SNMP-Gerätetyp zu lesen oder zu schreiben, indem Sie die Kontextinformationen der Instanz aktualisieren, bevor Sie miteinander kommunizieren.

-   Verwenden Sie beim Verweisen auf ein bestimmtes Gerät einen DNS-Namen anstelle der IP-Adresse.

    Im folgenden Beispiel wird gezeigt, wie Sie den DNS-Namen für ein bestimmtes Gerät verwenden.

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   Erstellen Sie einen separaten Namespace, und ordnen Sie dem Namespace Objekt mithilfe des AgentAddress-instanzqualifizierers eine Geräteadresse zu, sodass der Namespace dauerhaft an das Gerät gebunden ist. In diesem Fall müssen Sie die Kontext Objektinformationen nicht angeben.
-   Lesen von einem SNMP-Gerät

    Im folgenden Beispiel wird ein Get-Vorgang für eine Geräteklasse durchführt.

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set objSet = objServices.ExecQuery _
        ("SELECT * FROM SNMP_NET_DEVICE_123 WHERE hdwr_idx>1",, _
          wbemFlagReturnWhenComplete)
    for each obj in objset 
      'do whatever 
    next
    ```

    

-   Schreiben Sie auf ein SNMP-Gerät.

    Im folgenden Beispiel wird ein Set-Vorgang für eine Geräteklasse durchführt.

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

Korrelierte Klassen sind solche, die ein bestimmtes SNMP-Gerät unterstützt, wenn eine Enumeration auftritt. Korrelation wirkt sich auf den Satz von Klassen aus, die von SMIR zurückgegeben werden. Nicht korrelierte Enumeration gibt alle innerhalb des SMIR vorhandenen Klassen zurück, unabhängig davon, ob Sie vom Gerät unterstützt werden. Weitere Informationen zur Verwendung von WMI-Korrelations Techniken finden Sie unter [WMI-SNMP-Klassen Korrelation](wmi-snmp-class-correlation.md).

 

 



