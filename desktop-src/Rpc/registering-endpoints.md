---
title: Registrieren von Endpunkten
description: Wenn Sie das Serverprogramm in der Endpunkt Zuordnung des Server Host Computers registrieren, können Client Programme bestimmen, welcher Endpunkt (in der Regel ein TCP/IP-Port oder eine Named Pipe), an dem das Serverprogramm lauscht.
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Registrieren von Endpunkten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23e02aaae18a9d28b989d16850693a8a8f0678e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707326"
---
# <a name="registering-endpoints"></a><span data-ttu-id="11148-104">Registrieren von Endpunkten</span><span class="sxs-lookup"><span data-stu-id="11148-104">Registering Endpoints</span></span>

<span data-ttu-id="11148-105">Wenn Sie das Serverprogramm in der Endpunkt Zuordnung des Server Host Computers registrieren, können Client Programme bestimmen, welcher Endpunkt (in der Regel ein TCP/IP-Port oder eine Named Pipe), an dem das Serverprogramm lauscht.</span><span class="sxs-lookup"><span data-stu-id="11148-105">Registering the server program in the endpoint map of the server host computer enables client programs to determine which endpoint (usually a TCP/IP port or a named pipe) the server program is listening to.</span></span> <span data-ttu-id="11148-106">Um sich selbst in der Endpunkt Zuordnung des Server Host Systems zu registrieren, Ruft ein Serverprogramm die [**rpcepregister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) -Funktion auf, wie im folgenden Code Fragment gezeigt:</span><span class="sxs-lookup"><span data-stu-id="11148-106">To register itself in the server host system's endpoint map, a server program calls the [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) function as shown in the following code fragment:</span></span>


```C++
// This example assumes that MyInterface_v1_0_s_ifspec is a valid data
// structure that represents the interface being registered. The 
// variable is a valid pointer to a binding vector.
RPC_STATUS status;
status = RpcEpRegister(
    MyInterface_v1_0_s_ifspec,
    rpcBindingVector,
    NULL,
    NULL);
```



<span data-ttu-id="11148-107">Der erste Parameter für [**rpcepregiester**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) ist die-Struktur, die die-Schnittstelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="11148-107">The first parameter to [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) is the structure that represents the interface.</span></span> <span data-ttu-id="11148-108">Sie finden Sie in der Header Datei, die der-Mittelwert Compiler aus der mittleren l-Datei für diese verteilte Anwendung generiert hat.</span><span class="sxs-lookup"><span data-stu-id="11148-108">You can find it in the header file that the MIDL compiler generated from your MIDL file for this distributed application.</span></span> <span data-ttu-id="11148-109">Siehe [entwickeln der-Schnittstelle](developing-the-interface.md).</span><span class="sxs-lookup"><span data-stu-id="11148-109">See [Developing the Interface](developing-the-interface.md).</span></span> <span data-ttu-id="11148-110">Als nächstes muss die Anwendung von **rpcepregiester** eine Reihe von Bindungs Handles übergeben, die in einem Bindungs Vektor gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="11148-110">Next, **RpcEpRegister** needs your application to pass a set of binding handles that are stored in a binding vector.</span></span>

<span data-ttu-id="11148-111">Zusätzlich zum Registrieren von Schnittstellennamen kann die Serveranwendung auch Objekt-UUIDs in der Endpunkt Zuordnung registrieren.</span><span class="sxs-lookup"><span data-stu-id="11148-111">In addition to registering interface names, your server application can also register object UUIDs in the endpoint map.</span></span> <span data-ttu-id="11148-112">In diesem Beispiel sind keine Objekt-UUIDs vorhanden, die registriert werden können, sodass der dritte Parameter für [**rpcepregister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) auf **null** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="11148-112">In this example, there are no object UUIDs to register, so the third parameter to [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) is set to **NULL**.</span></span>

<span data-ttu-id="11148-113">Der letzte Parameter ist eine Kommentar Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="11148-113">The last parameter is a comment string.</span></span> <span data-ttu-id="11148-114">Obwohl die RPC-Lauf Zeit Bibliothek diese Zeichenfolge nicht verwendet, wird das Festlegen der Zeichenfolge empfohlen, da dadurch die Verwaltbarkeit des Systems verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="11148-114">Although the RPC run-time library does not use this string, setting the string is recommended, as it improves manageability of the system.</span></span> <span data-ttu-id="11148-115">Ein Systemadministrator kann mithilfe der Zeichenfolge erkennen, welche Ports von welchen-Anwendungen verwendet werden, um zu bestimmen, welche Ports von Firewalls verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="11148-115">A system administrator can use the string to detect which ports are used by which applications, which can then be used to determine which ports to be managed by firewalls.</span></span>

 

 




