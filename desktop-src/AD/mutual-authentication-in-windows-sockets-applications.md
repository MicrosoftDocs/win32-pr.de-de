---
title: Gegenseitige Authentifizierung in Windows Sockets-Anwendungen
description: Microsoft Windows Sockets-Dienste können die Registrierungs-und Auflösungs-APIs (RNR) zum Veröffentlichen von Diensten verwenden, oder Sie können Dienst Verbindungspunkte verwenden.
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- Gegenseitige Authentifizierung in Windows Sockets-Anwendungen
- Active Directory mithilfe der gegenseitigen Authentifizierung in Windows Sockets-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29062fa5c9fa7b9b003f1c3aa6f8bc384a785f83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206257"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a><span data-ttu-id="8dc38-105">Gegenseitige Authentifizierung in Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="8dc38-105">Mutual Authentication in Windows Sockets Applications</span></span>

<span data-ttu-id="8dc38-106">Microsoft Windows Sockets-Dienste können die Registrierungs-und Auflösungs-APIs (RNR) zum Veröffentlichen von Diensten verwenden, oder Sie können Dienst Verbindungspunkte verwenden.</span><span class="sxs-lookup"><span data-stu-id="8dc38-106">Microsoft Windows Sockets services can use the Registration and Resolution (RnR) APIs to publish services, or they can use service connection points.</span></span>

<span data-ttu-id="8dc38-107">Weitere Informationen und ein Codebeispiel, das zeigt, wie die gegenseitige Authentifizierung für einen Windows Sockets-Dienst durchgeführt wird, der mithilfe eines Dienst Verbindungs Punkts veröffentlicht wird, finden Sie unter [gegenseitige Authentifizierung in einem Windows Sockets Service mit einem SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="8dc38-107">For more information and a code example that shows how to perform mutual authentication for a Windows Sockets service that publishes using a service connection point, see [Mutual Authentication in a Windows Sockets Service with an SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md).</span></span> <span data-ttu-id="8dc38-108">In diesem Codebeispiel wird ein SSPI-Sicherheitspaket verwendet, um die Authentifizierungs Verhandlungen zwischen einem Client und dem Winsock-Dienst zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="8dc38-108">This code example uses an SSPI security package to manage the authentication negotiations between a client and the WinSock service.</span></span>

<span data-ttu-id="8dc38-109">Ein Winsock RNR-Dienst kann ähnlichen Code verwenden, um die gegenseitige Authentifizierung mithilfe eines SSPI-Pakets auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8dc38-109">A WinSock RnR service can use similar code to perform mutual authentication using an SSPI package.</span></span> <span data-ttu-id="8dc38-110">In diesem Fall würde der Dienst seine SPNs mithilfe des Distinguished Name des Dienst Eintrags im winsockservices-Container im Verzeichnis zusammenstellen.</span><span class="sxs-lookup"><span data-stu-id="8dc38-110">In this case, the service would compose its SPNs using the distinguished name of the service's entry in the WinsockServices container in the directory.</span></span>

<span data-ttu-id="8dc38-111">Wenn sich der Dienst beispielsweise mit dem Namen "winsockrnrsampleservice" registriert, würden Sie den Dienst Prinzipal Namen aus dem folgenden Distinguished Name verfassen:</span><span class="sxs-lookup"><span data-stu-id="8dc38-111">For example, if the service registers itself with the name "WinSockRnRSampleService", you would compose the service's SPN from the following distinguished name:</span></span>


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




