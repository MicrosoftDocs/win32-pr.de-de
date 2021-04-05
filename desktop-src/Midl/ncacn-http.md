---
title: ncacn_http-Attribut
description: Das http-Schlüsselwort ncacn \_ identifiziert den Microsoft Internet Information Server (IIS) als Protokollfamilie für den Endpunkt.
ms.assetid: 92d2b44c-2eab-4474-826b-ccafd26db124
keywords:
- ncacn_http Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_http
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7043aaa3a011b37a4b593a03b2d74658caab6fde
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726337"
---
# <a name="ncacn_http-attribute"></a><span data-ttu-id="1a06c-104">ncacn \_ http-Attribut</span><span class="sxs-lookup"><span data-stu-id="1a06c-104">ncacn\_http attribute</span></span>

<span data-ttu-id="1a06c-105">Das **\_ http-Schlüsselwort ncacn** identifiziert den Microsoft Internet Information Server (IIS) als Protokollfamilie für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="1a06c-105">The **ncacn\_http** keyword identifies the Microsoft Internet Information Server (IIS) as the protocol family for the endpoint.</span></span>

``` syntax
ncacn_http:rpc_server[endpoint]
```

## <a name="parameters"></a><span data-ttu-id="1a06c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a06c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a06c-107">*RPC- \_ Server*</span><span class="sxs-lookup"><span data-stu-id="1a06c-107">*rpc\_server*</span></span> 
</dt> <dd>

<span data-ttu-id="1a06c-108">Die Internet Adresse oder der Name des Computers, auf dem der RPC-Server Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a06c-108">The Internet address or name of the machine that the RPC server process is running on.</span></span>

</dd> <dt>

<span data-ttu-id="1a06c-109">*Dreher*</span><span class="sxs-lookup"><span data-stu-id="1a06c-109">*endpoint*</span></span> 
</dt> <dd>

<span data-ttu-id="1a06c-110">Der bekannte (statische) TCP/IP-Port, der vom RPC-Server Prozess überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="1a06c-110">The well-known (static) TCP/IP port that the RPC server process is listening on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a06c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a06c-111">Remarks</span></span>

<span data-ttu-id="1a06c-112">Durch die Identifizierung von Microsoft Internet Information Server (IIS) als Protokollfamilie können Client-und Server Anwendungen über das Internet über den Microsoft Internet Information Server (IIS) als Proxy kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1a06c-112">Identifying the Microsoft Internet Information Server (IIS) as the protocol family allows client and server applications to communicate across the internet by using the Microsoft Internet Information Server (IIS) as a proxy.</span></span> <span data-ttu-id="1a06c-113">Da Aufrufe über einen eingerichteten HTTP-Port getunniert werden, können Sie Firewalls überwinden.</span><span class="sxs-lookup"><span data-stu-id="1a06c-113">Because calls are tunneled through an established HTTP port, they can cross firewalls.</span></span>

<span data-ttu-id="1a06c-114">Alle RPC-Client-und-Server Anwendungen können das **ncacn- \_ http** -Protokoll unterstützen, solange Sie mit einem Internet Informationsserver vernetzt sind.</span><span class="sxs-lookup"><span data-stu-id="1a06c-114">Any RPC client and server applications can support the **ncacn\_http** protocol as long as they are networked to an Internet Information Server.</span></span> <span data-ttu-id="1a06c-115">IIS kontaktiert den RPC-Server und richtet einen TCP/IP-Socket ein, der für den Client verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="1a06c-115">The IIS contacts the RPC server and establishes a TCP/IP socket, which it maintains for the client.</span></span> <span data-ttu-id="1a06c-116">IIS verhandelt eine TCP/IP-Verbindung mit dem RPC-Server und fungiert nach Abschluss der Aushandlung als RPC-Proxy, um Daten zwischen dem Client seitigen TCP/IP-Socket und dem serverseitigen TCP/IP-Socket weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="1a06c-116">The IIS negotiates a TCP/IP connection with the RPC server, and once the negotiation is complete, acts as an RPC proxy, forwarding data between the client-side TCP/IP socket and the server-side TCP/IP socket.</span></span> <span data-ttu-id="1a06c-117">Wenn der IIS-RPC-Proxy erkennt, dass eine Sitzung auf dem Client oder auf der Serverseite geschlossen wird, wird der verbleibende Socket geschlossen.</span><span class="sxs-lookup"><span data-stu-id="1a06c-117">When the IIS RPC proxy detects a session close on either the client or the server side, it closes the remaining socket.</span></span>

<span data-ttu-id="1a06c-118">Die Client Anwendung verwendet implizit statische Bindungen an IIS, aber der Server kann dynamische Endpunkte verwenden, wobei der RPCSS-Server (Endpoint Mapper) des Servers den RPC-Serverport auflöst.</span><span class="sxs-lookup"><span data-stu-id="1a06c-118">The client application implicitly uses static binding to the IIS, but the server can use dynamic endpoints, with the server's RPCSS (endpoint mapper) resolving the RPC server port.</span></span> <span data-ttu-id="1a06c-119">Wenn IIS sich auf einem anderen Computer als der RPC-Server befindet, empfängt IIS den Remote Aufruf, kontaktiert RPCSS auf dem RPC-Server Computer, um den Server Prozess Endpunkt abzurufen, und leitet den Aufruf an den entsprechenden RPC-Server weiter.</span><span class="sxs-lookup"><span data-stu-id="1a06c-119">If the IIS is on a different machine than the RPC server, the IIS receives the remote call, contacts RPCSS on the RPC server machine to get the server process endpoint, and then forwards the call to the appropriate RPC server.</span></span>

<span data-ttu-id="1a06c-120">Wenn Internet Explorer installiert ist, überprüft der Transport die Registrierung, um festzustellen, ob eine Konfiguration für einen HTTP-Proxy vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1a06c-120">If Internet Explorer is installed, the transport will check the registry to see if there is a configuration for an HTTP proxy.</span></span> <span data-ttu-id="1a06c-121">Wenn ein Proxy vorhanden ist, wird er vom Transport verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a06c-121">If a proxy exists, the transport will use it.</span></span>

## <a name="examples"></a><span data-ttu-id="1a06c-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a06c-122">Examples</span></span>

``` syntax
//RPC client accesses an RPC server application, which is listening on //endpoint 2225 of an IIS Web Server named major7.microsoft.com 
[   
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.0), 
    endpoint("ncacn_http:major7.microsoft.com[2225]") 
] 
interface iface
{
    // Interface definition statements.
}

//string binding format. 
//IIS Web server (websvr1)is on a different machine than the RPC
//server, and endpoints are dynamic
"obj_uuid@ncacn_http:major7.microsoft.com
    [,]"

//tells the transport to use proxysvr, port 80, as the outgoing http 
//server:
"obj_uuid@ncacn_http:major7.microsoft.com[,]"
```

## <a name="see-also"></a><span data-ttu-id="1a06c-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1a06c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a06c-124">**Dreher**</span><span class="sxs-lookup"><span data-stu-id="1a06c-124">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="1a06c-125">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="1a06c-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="1a06c-126">**Zeichen folgen Bindung**</span><span class="sxs-lookup"><span data-stu-id="1a06c-126">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 