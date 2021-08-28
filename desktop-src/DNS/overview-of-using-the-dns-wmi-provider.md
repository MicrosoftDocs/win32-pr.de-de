---
title: Übersicht über die Verwendung des DNS-WMI-Anbieters
description: Mit den folgenden allgemeinen Schritten beginnen Sie mit dem Erstellen Ihres eigenen Skripts oder Programms, das den DNS-WMI-Anbieter verwendet.
ms.assetid: d9d64bda-0564-4074-9f0a-a249c7315042
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9eaa50e4ed1a237ed5b42abd4375ab301a2106498e929e42993cd634ca9ba18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077030"
---
# <a name="overview-of-using-the-dns-wmi-provider"></a>Übersicht über die Verwendung des DNS-WMI-Anbieters

Mit den folgenden allgemeinen Schritten beginnen Sie mit dem Erstellen Ihres eigenen Skripts oder Programms, das den DNS-WMI-Anbieter verwendet.

**So erstellen Sie ein Skript oder Programm mithilfe des DNS-WMI-Anbieters**

1.  Verbinden zum DNS-WMI-Anbieter.
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > Der Namensraum für den DNS-WMI-Anbieter ist immer "root \\ microsoftdns".

     

2.  Hier erhalten Sie eine DNS-Serverinstanz.
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  Abhängig von der Typaktion, die Sie ausführen möchten, erhalten Sie eine DNS-Zone oder eine Eintragsinstanz.
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  Führen Sie die gewünschten Aktionen aus:
    -   Ausführen einer Methode
    -   Anzeigen einer Eigenschaft
    -   Ändern einer Eigenschaft (muss über Lese-/Schreibzugriff verfügen)

 

 




