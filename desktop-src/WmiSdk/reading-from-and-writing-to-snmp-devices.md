---
description: Auf SNMP-Geräte kann zugegriffen werden, indem aus der entsprechenden Klasseninstanz im WMI SMIR (SNMP Module Information Repository) gelesen oder in diese geschrieben wird.
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: Lesen von und Schreiben auf SNMP-Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c0419a5fc426c183ee1eb89a957a0c2f6a210ecd9b5d4612b6c4deb4e0f775a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554255"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a>Lesen von und Schreiben auf SNMP-Geräten

Auf SNMP-Geräte kann zugegriffen werden, indem aus der entsprechenden Klasseninstanz im WMI SMIR (SNMP Module Information Repository) gelesen oder in diese geschrieben wird. Wenn Sie mit mehreren Geräten desselben Typs arbeiten, laden Sie die MIBs für einen SNMP-Gerätetyp aus Effizienz- und Effizienzgefässen in SMIR.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

Wählen Sie eine der folgenden Optionen zum Lesen oder Schreiben aus jedem SNMP-Gerätetyp aus, indem Sie die Kontextinformationen der Instanz aktualisieren, bevor Sie mit den einzelnen Geräten kommunizieren.

-   Verwenden Sie beim Verweisen auf ein bestimmtes Gerät einen DNS-Namen anstelle der IP-Adresse.

    Das folgende Beispiel zeigt, wie der DNS-Name für ein bestimmtes Gerät verwendet wird.

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   Erstellen Sie einen separaten Namespace, und ordnen Sie dem Namespaceobjekt mithilfe des AgentAddress-Instanzqualifizierers eine Geräteadresse zu, damit der Namespace dauerhaft an das Gerät gebunden ist. In diesem Fall müssen Sie die Kontextobjektinformationen nicht angeben.
-   Lesen von einem SNMP-Gerät.

    Im folgenden Beispiel wird ein Get-Vorgang für eine Geräteklasse durchgeführt.

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

    

-   Schreiben sie auf ein SNMP-Gerät.

    Im folgenden Beispiel wird ein Set-Vorgang für eine Geräteklasse durchgeführt.

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

Korrelierte Klassen sind klassen, von denen bekannt ist, dass ein bestimmtes SNMP-Gerät unterstützt, wenn eine Enumeration auftritt. Die Korrelation wirkt sich auf den Satz von Klassen aus, die vom SMIR zurückgegeben werden. Nicht korrelierte Enumeration gibt alle Klassen zurück, die in SMIR vorhanden sind, unabhängig davon, ob das Gerät sie unterstützt. Weitere Informationen zur Verwendung von WMI-Korrelationstechniken finden Sie unter [WMI-SNMP-Klassenkorrelation.](wmi-snmp-class-correlation.md)

 

 



