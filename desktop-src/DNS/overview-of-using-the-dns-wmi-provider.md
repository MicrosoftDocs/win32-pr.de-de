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
# <a name="overview-of-using-the-dns-wmi-provider"></a><span data-ttu-id="84680-103">Übersicht über die Verwendung des DNS-WMI-Anbieters</span><span class="sxs-lookup"><span data-stu-id="84680-103">Overview of Using the DNS WMI Provider</span></span>

<span data-ttu-id="84680-104">Die folgenden allgemeinen Schritte erleichtern Ihnen den Einstieg in die Erstellung eines eigenen Skripts oder Programms, in dem der DNS-WMI-Anbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84680-104">The following general steps get you started in creating your own script or program that makes use of the DNS WMI Provider.</span></span>

<span data-ttu-id="84680-105">**So erstellen Sie ein Skript oder Programm mit dem DNS-WMI-Anbieter**</span><span class="sxs-lookup"><span data-stu-id="84680-105">**To create a script or program using the DNS WMI Provider**</span></span>

1.  <span data-ttu-id="84680-106">Verbinden Sie sich mit dem DNS-WMI-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="84680-106">Connect to the DNS WMI Provider.</span></span>
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > <span data-ttu-id="84680-107">Der Namespace für den DNS-WMI-Anbieter ist immer "root \\ MicrosoftDNS".</span><span class="sxs-lookup"><span data-stu-id="84680-107">The name space for the DNS WMI Provider will always be "root\\microsoftdns".</span></span>

     

2.  <span data-ttu-id="84680-108">Verschaffen Sie sich eine DNS-Server Instanz.</span><span class="sxs-lookup"><span data-stu-id="84680-108">Get a DNS Server instance.</span></span>
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  <span data-ttu-id="84680-109">Abhängig von der Art der auszuführenden Aktion können Sie eine DNS-Zone oder eine Daten Satz Instanz erhalten.</span><span class="sxs-lookup"><span data-stu-id="84680-109">Depending on the type action you want to perform, get a DNS zone or record instance.</span></span>
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  <span data-ttu-id="84680-110">Führen Sie die gewünschten Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="84680-110">Perform the desired actions:</span></span>
    -   <span data-ttu-id="84680-111">Methode ausführen</span><span class="sxs-lookup"><span data-stu-id="84680-111">Execute a method</span></span>
    -   <span data-ttu-id="84680-112">Anzeigen einer Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="84680-112">Display a property</span></span>
    -   <span data-ttu-id="84680-113">Ändern einer Eigenschaft (muss über Lese-/Schreibzugriff verfügen)</span><span class="sxs-lookup"><span data-stu-id="84680-113">Modify a property (must have Read/Write access)</span></span>

 

 




