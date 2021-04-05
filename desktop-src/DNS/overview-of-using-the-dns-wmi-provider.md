---
title: Übersicht über die Verwendung des DNS-WMI-Anbieters
description: Die folgenden allgemeinen Schritte erleichtern Ihnen den Einstieg in die Erstellung eines eigenen Skripts oder Programms, in dem der DNS-WMI-Anbieter verwendet wird.
ms.assetid: d9d64bda-0564-4074-9f0a-a249c7315042
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9188e14e0a0b1f73380434be0d4298b0748da12f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037246"
---
# <a name="overview-of-using-the-dns-wmi-provider"></a>Übersicht über die Verwendung des DNS-WMI-Anbieters

Die folgenden allgemeinen Schritte erleichtern Ihnen den Einstieg in die Erstellung eines eigenen Skripts oder Programms, in dem der DNS-WMI-Anbieter verwendet wird.

**So erstellen Sie ein Skript oder Programm mit dem DNS-WMI-Anbieter**

1.  Verbinden Sie sich mit dem DNS-WMI-Anbieter.
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > Der Namespace für den DNS-WMI-Anbieter ist immer "root \\ MicrosoftDNS".

     

2.  Verschaffen Sie sich eine DNS-Server Instanz.
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  Abhängig von der Art der auszuführenden Aktion können Sie eine DNS-Zone oder eine Daten Satz Instanz erhalten.
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  Führen Sie die gewünschten Aktionen aus:
    -   Methode ausführen
    -   Anzeigen einer Eigenschaft
    -   Ändern einer Eigenschaft (muss über Lese-/Schreibzugriff verfügen)

 

 




