---
title: Zwischenspeichern von Verbindungen
description: Wenn eine Verbindung mit einem Server hergestellt wird, wird das Verbindungs Handle für diesen Prozess auf dem Client Computer zwischengespeichert, bis die Verbindung geschlossen wird.
ms.assetid: 927afd35-8703-4234-b6a8-6320a3667532
ms.tgt_platform: multiple
keywords:
- Verbindungs Caching (ADSI)
- Zwischenspeichern von Verbindungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857d102a52be9c7ccf40f9076892a85d5b3b8683
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036317"
---
# <a name="connection-caching"></a><span data-ttu-id="2239c-105">Zwischenspeichern von Verbindungen</span><span class="sxs-lookup"><span data-stu-id="2239c-105">Connection Caching</span></span>

<span data-ttu-id="2239c-106">Wenn eine Verbindung mit einem Server hergestellt wird, wird das Verbindungs Handle für diesen Prozess auf dem Client Computer zwischengespeichert, bis die Verbindung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="2239c-106">When a connection to a server is made, the connection handle is cached on the client computer for that process until that connection is closed.</span></span> <span data-ttu-id="2239c-107">Wenn derselbe Server, Port und die gleichen Anmelde Informationen in einer nachfolgenden Verbindung verwendet werden, und nur die **ADS \_ fast \_ Bind** -oder **ADS \_ Server \_ Bind** -Authentifizierungsflags unterschiedlich sind, wird die vorhandene Verbindung von ADSI wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="2239c-107">If the same server, port, and credentials are used in a subsequent connection, and only the **ADS\_FAST\_BIND** or **ADS\_SERVER\_BIND** authentication flags differ, ADSI will reuse the existing connection.</span></span> <span data-ttu-id="2239c-108">ADSI führt diese Verbindungs Zwischenspeicherung pro Prozess durch.</span><span class="sxs-lookup"><span data-stu-id="2239c-108">ADSI performs this connection caching on a per-process basis.</span></span>

<span data-ttu-id="2239c-109">Um die Leistung zu verbessern, verwenden Sie nach Möglichkeit vorhandene Verbindungen wieder.</span><span class="sxs-lookup"><span data-stu-id="2239c-109">To increase performance, reuse existing connections when possible.</span></span>

<span data-ttu-id="2239c-110">Das folgende Codebeispiel zeigt, wie das Verbindungs Caching funktioniert.</span><span class="sxs-lookup"><span data-stu-id="2239c-110">The following code example shows how connection caching works.</span></span>


```VB
Dim cachedConn As IADs
Dim obj As IADs
Dim cachedName As String
Dim objName As String
 
' Connect to the server and maintain this handle to cache the connection.
Set cachedConn = GetObject("LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com")
 
cachedName = cachedConn.Get("distinguishedName")
Debug.Print (cachedName)
 
' Reuse the connection to MyMachine opened by cachedConn.
' Be aware that this line executes quickly because it is not required
' to transmit over the network again.
Set obj = GetObject("LDAP://MyMachine/CN=Bob,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection.
Set obj = Nothing
 
' Reuse the connection to MyMachine opened by cachedConn again.
Set obj = GetObject("LDAP://MyMachine/CN=Administrator,CN=Users,DC=MyDomain,DC=Fabrikam,DC=com")
 
objName = obj.Get("distinguishedName")
Debug.Print (objName)
 
' Release the second connection again.
Set obj = Nothing
 
' Release the first connection.
Set cachedConn = Nothing
 
' The connection to MyMachine is closed.
```



 

 




