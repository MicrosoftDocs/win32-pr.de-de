---
description: Details der Winsock-Netzwerk Ereignis Ablauf Verfolgung
ms.assetid: f0386bd3-15d0-45f3-82c9-365d1c9f59c5
title: Details der Winsock-Netzwerk Ereignis Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588363420aee9c3b04f4f8060bbd9c77b9cc3232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217285"
---
# <a name="winsock-network-event-tracing-details"></a><span data-ttu-id="6ec97-103">Details der Winsock-Netzwerk Ereignis Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="6ec97-103">Winsock Network Event Tracing Details</span></span>

<span data-ttu-id="6ec97-104">Im folgenden werden die einzelnen Winsock-Netzwerkereignisse erläutert, die verfolgt werden können, und es wird beschrieben, welche Parameter und Informationen protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="6ec97-104">The following details each of the Winsock network events that can be traced and describes which parameters and information are logged.</span></span>

## <a name="socket-creation"></a><span data-ttu-id="6ec97-105">Socketerstellung</span><span class="sxs-lookup"><span data-stu-id="6ec97-105">Socket Creation</span></span>

<span data-ttu-id="6ec97-106">Ereignis-ID = 1</span><span class="sxs-lookup"><span data-stu-id="6ec97-106">Event ID = 1</span></span>

<span data-ttu-id="6ec97-107">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-107">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-108">Die folgenden Winsock-Ereignisse werden für die Socketerstellung nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-108">The following Winsock events are traced for socket creation:</span></span>

-   <span data-ttu-id="6ec97-109">Sockethandles, die durch Aufrufe der [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -oder [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) -Funktionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6ec97-109">Socket handles created by calls to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) or [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) functions.</span></span>
-   <span data-ttu-id="6ec97-110">Akzeptierte Sockethandles für Abhör Sockets.</span><span class="sxs-lookup"><span data-stu-id="6ec97-110">Accepted socket handles on listening sockets.</span></span>
-   <span data-ttu-id="6ec97-111">Sockethandles, die durch Aufrufe der [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) -Funktion erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6ec97-111">Socket handles created by calls to the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span>
-   <span data-ttu-id="6ec97-112">Sockethandles, die von Aufrufen der [**akzeptex**](/windows/win32/api/mswsock/nf-mswsock-acceptex) -Funktion oder der [**connectex**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) -Funktion wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ec97-112">Socket handles re-used by calls to the [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) or [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) functions.</span></span>

<span data-ttu-id="6ec97-113">Die folgenden Parameter werden für ein Socket-Erstellungs Ereignis protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-113">The following parameters are logged for a socket creation event:</span></span>



| <span data-ttu-id="6ec97-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-114">Parameter</span></span>                                                                                                        | <span data-ttu-id="6ec97-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-115">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-116"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-116"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                 | <span data-ttu-id="6ec97-117">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-117">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-118"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-118"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>             | <span data-ttu-id="6ec97-119">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-119">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-120"><span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType</span><span class="sxs-lookup"><span data-stu-id="6ec97-120"><span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType</span></span><br/>     | <span data-ttu-id="6ec97-121">Der Typ des Sockets.</span><span class="sxs-lookup"><span data-stu-id="6ec97-121">The type of the socket.</span></span><br/>                                                     |
| <span data-ttu-id="6ec97-122"><span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>Spezifische</span><span class="sxs-lookup"><span data-stu-id="6ec97-122"><span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>Protocol</span></span><br/>             | <span data-ttu-id="6ec97-123">Das Protokoll des Sockets.</span><span class="sxs-lookup"><span data-stu-id="6ec97-123">The protocol of the socket.</span></span><br/>                                                 |
| <span data-ttu-id="6ec97-124"><span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>Usermodepid</span><span class="sxs-lookup"><span data-stu-id="6ec97-124"><span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid</span></span><br/> | <span data-ttu-id="6ec97-125">Die Benutzermodus-Prozess-ID, die den Socket erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="6ec97-125">The user-mode process ID that created the socket.</span></span><br/>                           |



 

## <a name="socket-bind"></a><span data-ttu-id="6ec97-126">Socketbindung</span><span class="sxs-lookup"><span data-stu-id="6ec97-126">Socket Bind</span></span>

<span data-ttu-id="6ec97-127">Ereignis-ID = 2 (IPv4), Ereignis-ID = 3 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="6ec97-127">Event ID = 2 (IPv4), Event ID = 3 (IPv6)</span></span>

<span data-ttu-id="6ec97-128">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-128">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-129">Die folgenden Winsock-Ereignisse werden für einen Bindungs Vorgang nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-129">The following Winsock events are traced for a bind operation:</span></span>

-   <span data-ttu-id="6ec97-130">Implizite oder explizite Bindung eines Sockethandles.</span><span class="sxs-lookup"><span data-stu-id="6ec97-130">Implicit or explicit binding of a socket handle.</span></span>

<span data-ttu-id="6ec97-131">Die folgenden Parameter werden für ein Bindungs Ereignis protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-131">The following parameters are logged for a bind event:</span></span>



| <span data-ttu-id="6ec97-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-132">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-133">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-134"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-134"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-135">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-135">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-136"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-136"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-137">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-137">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-138"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse</span><span class="sxs-lookup"><span data-stu-id="6ec97-138"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="6ec97-139">Die lokale IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="6ec97-139">The local IP address.</span></span><br/>                                                       |
| <span data-ttu-id="6ec97-140"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span><span class="sxs-lookup"><span data-stu-id="6ec97-140"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="6ec97-141">Die lokale IP-Portnummer.</span><span class="sxs-lookup"><span data-stu-id="6ec97-141">The local IP port number.</span></span><br/>                                                   |
| <span data-ttu-id="6ec97-142"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Stands</span><span class="sxs-lookup"><span data-stu-id="6ec97-142"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Status</span></span><br/>         | <span data-ttu-id="6ec97-143">Der Status oder Fehlercode, der für den Bindungs Vorgang zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-143">The status or error code returned for the bind operation.</span></span><br/>                   |



 

## <a name="failed-bind"></a><span data-ttu-id="6ec97-144">Fehlerhafte Bindung</span><span class="sxs-lookup"><span data-stu-id="6ec97-144">Failed Bind</span></span>

<span data-ttu-id="6ec97-145">Ereignis-ID = 40</span><span class="sxs-lookup"><span data-stu-id="6ec97-145">Event ID = 40</span></span>

<span data-ttu-id="6ec97-146">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-146">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-147">Die folgenden Winsock-Ereignisse werden für einen fehlgeschlagenen Bindungs Vorgang nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-147">The following Winsock events are traced for a failed bind operation:</span></span>

-   <span data-ttu-id="6ec97-148">Implizite oder explizite Bindung eines Sockethandles, der fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="6ec97-148">Implicit or explicit binding of a socket handle that fails.</span></span>

<span data-ttu-id="6ec97-149">Die folgenden Parameter werden für ein fehlerhafter Bindungs Ereignis protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-149">The following parameters are logged for a failed bind event:</span></span>



| <span data-ttu-id="6ec97-150">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-150">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-151">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-151">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-152"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-152"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-153">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-153">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-154"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-154"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-155">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-155">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-156"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit</span><span class="sxs-lookup"><span data-stu-id="6ec97-156"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="6ec97-157">Der für den fehlgeschlagenen Bindungs Vorgang zurückgegebene Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6ec97-157">The error code returned for the failing bind operation.</span></span><br/>                     |



 

## <a name="socket-connect"></a><span data-ttu-id="6ec97-158">Socketverbindung</span><span class="sxs-lookup"><span data-stu-id="6ec97-158">Socket Connect</span></span>

<span data-ttu-id="6ec97-159">Ereignis-ID = 4 (IPv4), Ereignis-ID = 5 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="6ec97-159">Event ID = 4 (IPv4), Event ID = 5 (IPv6)</span></span>

<span data-ttu-id="6ec97-160">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-160">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-161">Die folgenden Winsock-Ereignisse werden für eine Anforderung zum Verbindungsvorgang nachverfolgt (ein Rückruf der [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)-, [**connectex**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)-, [**wsaconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect)-, [**wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)-oder [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) -Funktion):</span><span class="sxs-lookup"><span data-stu-id="6ec97-161">The following Winsock events are traced for a connect operation request (a call to the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function):</span></span>

-   <span data-ttu-id="6ec97-162">Verbinden eines Sockets mit einem Ziel entweder für einen Verbindungs orientierten oder einen Verbindungs losen Socket.</span><span class="sxs-lookup"><span data-stu-id="6ec97-162">Connecting a socket to a destination for either a connection-oriented or a connectionless socket.</span></span>

<span data-ttu-id="6ec97-163">Die folgenden Parameter werden für ein Connect-Ereignis protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-163">The following parameters are logged for a connect event:</span></span>



| <span data-ttu-id="6ec97-164">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-164">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-165">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-165">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-166"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-166"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-167">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-167">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-168"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-168"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-169">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-169">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-170"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse</span><span class="sxs-lookup"><span data-stu-id="6ec97-170"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="6ec97-171">Die Remote-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="6ec97-171">The remote IP address.</span></span><br/>                                                      |
| <span data-ttu-id="6ec97-172"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span><span class="sxs-lookup"><span data-stu-id="6ec97-172"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="6ec97-173">Die Remote-IP-Portnummer.</span><span class="sxs-lookup"><span data-stu-id="6ec97-173">The remote IP port number.</span></span><br/>                                                  |



 

## <a name="connect-completed"></a><span data-ttu-id="6ec97-174">Verbindung abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="6ec97-174">Connect Completed</span></span>

<span data-ttu-id="6ec97-175">Ereignis-ID = 6</span><span class="sxs-lookup"><span data-stu-id="6ec97-175">Event ID = 6</span></span>

<span data-ttu-id="6ec97-176">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-176">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-177">Die folgenden Winsock-Ereignisse werden nachverfolgt, wenn eine Verbindung abgeschlossen wurde:</span><span class="sxs-lookup"><span data-stu-id="6ec97-177">The following Winsock events are traced for a connect completed:</span></span>

-   <span data-ttu-id="6ec97-178">Der Verbindungsvorgang ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ec97-178">The connect operation is completed.</span></span>

<span data-ttu-id="6ec97-179">Die folgenden Parameter werden für ein Connect-abgeschlossenes Ereignis protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-179">The following parameters are logged for a connect completed event:</span></span>



| <span data-ttu-id="6ec97-180">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-180">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-181">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-181">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-182"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-182"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-183">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-183">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-184"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-184"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-185">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-185">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-186"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit</span><span class="sxs-lookup"><span data-stu-id="6ec97-186"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="6ec97-187">Der Fehlercode, der für den Verbindungsvorgang zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-187">The error code returned for the connect operation.</span></span><br/>                          |



 

## <a name="afd-initiated-abort"></a><span data-ttu-id="6ec97-188">Abbruch AFD-Initiated</span><span class="sxs-lookup"><span data-stu-id="6ec97-188">AFD-Initiated Abort</span></span>

<span data-ttu-id="6ec97-189">Ereignis-ID = 7</span><span class="sxs-lookup"><span data-stu-id="6ec97-189">Event ID = 7</span></span>

<span data-ttu-id="6ec97-190">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-190">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-191">Die folgenden Winsock-Ereignisse werden für durch Winsock initiierte Abbrüche oder Abbruch Vorgänge nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-191">The following Winsock events are traced for Winsock-initiated aborts or cancel operations:</span></span>

-   <span data-ttu-id="6ec97-192">Ein Abbruch aufgrund von ungelesenen Empfangsdaten, die nach dem Schließen gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="6ec97-192">An abort due to unread receive data buffered after close.</span></span>
-   <span data-ttu-id="6ec97-193">Ein Abbruch nach einem Aufrufen der [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) -Funktion *mit dem fest* gelegten Parameter auf SD \_ Receive und einem Aufrufen der [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Funktion mit ausstehenden Daten empfangen.</span><span class="sxs-lookup"><span data-stu-id="6ec97-193">An abort after a call to the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function with the *how* parameter set to SD\_RECEIVE and a call to the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function with receive data pending.</span></span>
-   <span data-ttu-id="6ec97-194">Ein Abbruch nach einem fehlgeschlagenen Versuch, den Endpunkt zu leeren.</span><span class="sxs-lookup"><span data-stu-id="6ec97-194">An abort after a failed attempt to flush the endpoint.</span></span>
-   <span data-ttu-id="6ec97-195">Abbruch nach einem internen Winsock-Fehler.</span><span class="sxs-lookup"><span data-stu-id="6ec97-195">An abort after an internal Winsock error occurred.</span></span>
-   <span data-ttu-id="6ec97-196">Ein Abbruch aufgrund einer Verbindung mit Fehlern und der Anwendung, die zuvor angefordert hat, dass die Verbindung unter bestimmten Umständen abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-196">An abort due to a connection with errors and the application previously requested that the connection be aborted on certain circumstances.</span></span> <span data-ttu-id="6ec97-197">Ein Beispiel für diesen Fall wäre eine Anwendung, die " \_ LINGER" mit einem Timeout von 0 (null) festgelegt hat und noch nicht bestätigte Daten für die Verbindung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6ec97-197">One example of this case would be an application that set SO\_LINGER with a timeout of zero and there is still unacknowledged data on the connection.</span></span>
-   <span data-ttu-id="6ec97-198">Ein Abbruch für eine Verbindung, die nicht vollständig mit dem akzeptieren des Endpunkts verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="6ec97-198">An abort on a connection not fully associated with accepting endpoint.</span></span>
-   <span data-ttu-id="6ec97-199">Ein Abbruch bei einem fehlgeschlagenen Aufrufs der [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) -oder [**Accept tex**](/windows/win32/api/mswsock/nf-mswsock-acceptex) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="6ec97-199">An abort on a failed call to the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) or [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) function.</span></span>
-   <span data-ttu-id="6ec97-200">Ein Abbruch aufgrund eines fehlgeschlagenen Empfangs Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="6ec97-200">An abort due to a failed receive operation.</span></span>
-   <span data-ttu-id="6ec97-201">Ein Abbruch aufgrund eines Plug & Play Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="6ec97-201">An abort due to a Plug and Play event.</span></span>
-   <span data-ttu-id="6ec97-202">Ein Abbruch aufgrund einer fehlgeschlagenen Leerungs Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6ec97-202">An abort due to a failed flush request.</span></span>
-   <span data-ttu-id="6ec97-203">Ein Abbruch aufgrund einer fehlgeschlagenen Anforderung zum Empfangen von Daten.</span><span class="sxs-lookup"><span data-stu-id="6ec97-203">An abort due to a failed expedited data receive request.</span></span>
-   <span data-ttu-id="6ec97-204">Ein Abbruch aufgrund einer fehlgeschlagenen Sende Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6ec97-204">An abort due to a failed send request.</span></span>
-   <span data-ttu-id="6ec97-205">Ein Abbruch aufgrund einer abgebrochenen Sende Anforderung.</span><span class="sxs-lookup"><span data-stu-id="6ec97-205">An abort due to canceled send request.</span></span>
-   <span data-ttu-id="6ec97-206">Ein Abbruch aufgrund eines abgebrochenen Aufrufs für die [**transmitpaketen**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="6ec97-206">An abort due to a canceled called to the [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) function.</span></span>

<span data-ttu-id="6ec97-207">Die folgenden Parameter werden für einen Winsock-initiierten Abbruch-oder Abbruch Vorgang protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-207">The following parameters are logged for a Winsock-initiated abort or cancel operation:</span></span>



| <span data-ttu-id="6ec97-208">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-208">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-209">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-209">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-210"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-210"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-211">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-211">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-212"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-212"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-213">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-213">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-214"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Weshalb</span><span class="sxs-lookup"><span data-stu-id="6ec97-214"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>         | <span data-ttu-id="6ec97-215">Der Grund für den Abbruch-oder Abbruch Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6ec97-215">The reason for the abort or cancel operation.</span></span><br/>                               |



 

## <a name="transport-initiated-abort"></a><span data-ttu-id="6ec97-216">Abbruch Transport-Initiated</span><span class="sxs-lookup"><span data-stu-id="6ec97-216">Transport-Initiated Abort</span></span>

<span data-ttu-id="6ec97-217">Ereignis-ID = 8</span><span class="sxs-lookup"><span data-stu-id="6ec97-217">Event ID = 8</span></span>

<span data-ttu-id="6ec97-218">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-218">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-219">Die folgenden Winsock-Ereignisse werden für vom Transport initiierte Abbruch-oder Abbruch Vorgänge verfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-219">The following Winsock events are traced for transport-initiated abort or cancel operations:</span></span>

-   <span data-ttu-id="6ec97-220">Zurücksetzen, angegeben durch den Transport.</span><span class="sxs-lookup"><span data-stu-id="6ec97-220">Reset indicated by the transport.</span></span>

<span data-ttu-id="6ec97-221">Die folgenden Parameter werden für einen Winsock-initiierten Abbruch-oder Abbruch Vorgang protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-221">The following parameters are logged for a Winsock-initiated abort or cancel operation:</span></span>



| <span data-ttu-id="6ec97-222">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-222">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-223">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-223">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-224"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-224"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-225">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-225">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-226"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-226"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-227">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-227">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-228"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Weshalb</span><span class="sxs-lookup"><span data-stu-id="6ec97-228"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>         | <span data-ttu-id="6ec97-229">Der Grund für den Abbruch-oder Abbruch Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6ec97-229">The reason for the abort or cancel operation.</span></span><br/>                               |



 

## <a name="failed-send-request"></a><span data-ttu-id="6ec97-230">Fehlgeschlagene Sende Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ec97-230">Failed Send Request</span></span>

<span data-ttu-id="6ec97-231">Ereignis-ID = 9</span><span class="sxs-lookup"><span data-stu-id="6ec97-231">Event ID = 9</span></span>

<span data-ttu-id="6ec97-232">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-232">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-233">Die folgenden Winsock-Ereignisse werden bei [**Sende**](/windows/desktop/api/Winsock2/nf-winsock2-send) -oder [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) -Anforderungen auf Fehler nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-233">The following Winsock events are traced for errors on [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) or [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) requests:</span></span>

-   <span data-ttu-id="6ec97-234">Bei fehlgeschlagenen [**Sende**](/windows/desktop/api/Winsock2/nf-winsock2-send) -oder [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) -Anforderungen zurückgegebene Fehler.</span><span class="sxs-lookup"><span data-stu-id="6ec97-234">Errors returned on failed [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) or [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) requests.</span></span>

<span data-ttu-id="6ec97-235">Die folgenden Parameter werden für Sende Anforderungen protokolliert, die zu einem Fehler führen:</span><span class="sxs-lookup"><span data-stu-id="6ec97-235">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="6ec97-236">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-236">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-237">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-237">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-238"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-238"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-239">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-239">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-240"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-240"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-241">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-241">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-242"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit</span><span class="sxs-lookup"><span data-stu-id="6ec97-242"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="6ec97-243">Der für den Vorgang zurückgegebene Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6ec97-243">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-wsasendmsg-request"></a><span data-ttu-id="6ec97-244">Wsasendmsg-Anforderung fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="6ec97-244">Failed WsaSendMsg Request</span></span>

<span data-ttu-id="6ec97-245">Ereignis-ID = 10</span><span class="sxs-lookup"><span data-stu-id="6ec97-245">Event ID = 10</span></span>

<span data-ttu-id="6ec97-246">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-246">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-247">Die folgenden Winsock-Ereignisse werden auf Fehler bei [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Anforderungen nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-247">The following Winsock events are traced for errors on [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) requests:</span></span>

-   <span data-ttu-id="6ec97-248">Bei fehlgeschlagenen [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Anforderungen zurückgegebene Fehler.</span><span class="sxs-lookup"><span data-stu-id="6ec97-248">Errors returned on failed [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) requests.</span></span>

<span data-ttu-id="6ec97-249">Die folgenden Parameter werden für Sende Anforderungen protokolliert, die zu einem Fehler führen:</span><span class="sxs-lookup"><span data-stu-id="6ec97-249">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="6ec97-250">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-250">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-251">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-251">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-252"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-252"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-253">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-253">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-254"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-254"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-255">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-255">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-256"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit</span><span class="sxs-lookup"><span data-stu-id="6ec97-256"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="6ec97-257">Der für den Vorgang zurückgegebene Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6ec97-257">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-recv-request"></a><span data-ttu-id="6ec97-258">Fehlgeschlagene recv-Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ec97-258">Failed Recv Request</span></span>

<span data-ttu-id="6ec97-259">Ereignis-ID = 11</span><span class="sxs-lookup"><span data-stu-id="6ec97-259">Event ID = 11</span></span>

<span data-ttu-id="6ec97-260">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-260">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-261">Die folgenden Winsock-Ereignisse werden auf Fehler bei [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv)-, [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)-oder [**wsarecvexeanforderungen**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-261">The following Winsock events are traced for errors on [**recv**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), or [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) requests:</span></span>

-   <span data-ttu-id="6ec97-262">Bei fehlgeschlagenen Empfangs Anforderungen zurückgegebene Fehler.</span><span class="sxs-lookup"><span data-stu-id="6ec97-262">Errors returned on failed receive requests.</span></span>

<span data-ttu-id="6ec97-263">Die folgenden Parameter werden für Sende Anforderungen protokolliert, die zu einem Fehler führen:</span><span class="sxs-lookup"><span data-stu-id="6ec97-263">The following parameters are logged for a send requests that results in an error:</span></span>



| <span data-ttu-id="6ec97-264">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-264">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-265">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-265">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-266"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-266"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-267">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-267">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-268"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-268"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-269">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-269">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit</span><span class="sxs-lookup"><span data-stu-id="6ec97-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="6ec97-271">Der für den Vorgang zurückgegebene Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6ec97-271">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="failed-recvfrom-request"></a><span data-ttu-id="6ec97-272">Fehlgeschlagene recvfrom-Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ec97-272">Failed Recvfrom Request</span></span>

<span data-ttu-id="6ec97-273">Ereignis-ID = 12</span><span class="sxs-lookup"><span data-stu-id="6ec97-273">Event ID = 12</span></span>

<span data-ttu-id="6ec97-274">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-274">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-275">Die folgenden Winsock-Ereignisse werden auf Fehler bei [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) -oder [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) -Anforderungen nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-275">The following Winsock events are traced for errors on [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) requests:</span></span>

-   <span data-ttu-id="6ec97-276">Fehler, die für fehlerhafte [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) -oder [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) -Anforderungen zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="6ec97-276">Errors returned on failed [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) requests.</span></span>

<span data-ttu-id="6ec97-277">Die folgenden Parameter werden für eine Anforderung vom Typ " [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) " oder " [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) " protokolliert, die zu einem Fehler führt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-277">The following parameters are logged for a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) or [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) request that results in an error:</span></span>



| <span data-ttu-id="6ec97-278">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-278">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-279">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-279">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-280"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-280"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-281">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-281">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-282"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-282"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-283">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-283">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-284"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit</span><span class="sxs-lookup"><span data-stu-id="6ec97-284"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="6ec97-285">Der für den Vorgang zurückgegebene Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6ec97-285">The error code returned for the operation.</span></span><br/>                                  |



 

## <a name="socket-close"></a><span data-ttu-id="6ec97-286">SocketClose</span><span class="sxs-lookup"><span data-stu-id="6ec97-286">Socket Close</span></span>

<span data-ttu-id="6ec97-287">Ereignis-ID = 13</span><span class="sxs-lookup"><span data-stu-id="6ec97-287">Event ID = 13</span></span>

<span data-ttu-id="6ec97-288">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-288">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-289">Die folgenden Winsock-Ereignisse werden für SocketClose-Vorgänge nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-289">The following Winsock events are traced for socket close operations:</span></span>

-   <span data-ttu-id="6ec97-290">Ein Sockethandle ist geschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ec97-290">A socket handle is closed.</span></span>

<span data-ttu-id="6ec97-291">Die folgenden Parameter werden für ein Socket Close-Ereignis protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-291">The following parameters are logged for a socket close event:</span></span>



| <span data-ttu-id="6ec97-292">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-292">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-293">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-293">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-294"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-294"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-295">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-295">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-296"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-296"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-297">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-297">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit</span><span class="sxs-lookup"><span data-stu-id="6ec97-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="6ec97-299">Der Rückgabewert für den SocketClose-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6ec97-299">The return value for the socket close operation.</span></span><br/>                            |



 

## <a name="socket-cleanup"></a><span data-ttu-id="6ec97-300">Socketcleanup</span><span class="sxs-lookup"><span data-stu-id="6ec97-300">Socket Cleanup</span></span>

<span data-ttu-id="6ec97-301">Ereignis-ID = 14</span><span class="sxs-lookup"><span data-stu-id="6ec97-301">Event ID = 14</span></span>

<span data-ttu-id="6ec97-302">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-302">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-303">Die folgenden Winsock-Ereignisse werden für die socketbereinigungs Vorgänge (Herunterfahren) nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-303">The following Winsock events are traced for socket cleanup (shutdown) operations:</span></span>

-   <span data-ttu-id="6ec97-304">Die [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) -Funktion wird für einen Socket aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ec97-304">The [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function is called on a socket.</span></span>
-   <span data-ttu-id="6ec97-305">Der Transport gibt an, dass eine fehlerhafte Verbindung getrennt wurde</span><span class="sxs-lookup"><span data-stu-id="6ec97-305">The transport indicates a failed graceful disconnect.</span></span>

<span data-ttu-id="6ec97-306">Die folgenden Parameter werden für ein socketcleanup (Shutdown) oder ein Socket Close-Ereignis protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-306">The following parameters are logged for a socket cleanup (shutdown) or socket close event:</span></span>



| <span data-ttu-id="6ec97-307">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-307">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-308">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-308">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-309"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-309"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-310">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-310">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-311"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-311"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-312">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-312">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-313"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit</span><span class="sxs-lookup"><span data-stu-id="6ec97-313"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="6ec97-314">Der Rückgabewert für die socketbereinigungs Operation (Shutdown).</span><span class="sxs-lookup"><span data-stu-id="6ec97-314">The return value for the socket cleanup (shutdown) operation.</span></span><br/>               |



 

## <a name="socket-accept"></a><span data-ttu-id="6ec97-315">Socketannahme</span><span class="sxs-lookup"><span data-stu-id="6ec97-315">Socket Accept</span></span>

<span data-ttu-id="6ec97-316">Ereignis-ID = 15 (IPv4), Ereignis-ID = 16 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="6ec97-316">Event ID = 15 (IPv4), Event ID = 16 (IPv6)</span></span>

<span data-ttu-id="6ec97-317">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-317">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-318">Die folgenden Winsock-Ereignisse werden für eine [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)-, [**akzeptex**](/windows/win32/api/mswsock/nf-mswsock-acceptex)-oder [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Funktions Anforderung nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-318">The following Winsock events are traced for an [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function request:</span></span>

-   <span data-ttu-id="6ec97-319">Eine [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)-, [**akzeptex**](/windows/win32/api/mswsock/nf-mswsock-acceptex)-oder [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Funktions Anforderung für ein Sockethandle.</span><span class="sxs-lookup"><span data-stu-id="6ec97-319">An [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function request on a socket handle.</span></span>

<span data-ttu-id="6ec97-320">Die folgenden Parameter werden für ein Accept-Ereignis protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-320">The following parameters are logged for an accept event:</span></span>



| <span data-ttu-id="6ec97-321">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-321">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-322">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-322">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-323"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-323"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-324">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-324">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-325"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-325"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-326">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-326">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-327"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse</span><span class="sxs-lookup"><span data-stu-id="6ec97-327"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="6ec97-328">Die Remote-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="6ec97-328">The remote IP address.</span></span><br/>                                                      |
| <span data-ttu-id="6ec97-329"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span><span class="sxs-lookup"><span data-stu-id="6ec97-329"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="6ec97-330">Die Remote-IP-Portnummer.</span><span class="sxs-lookup"><span data-stu-id="6ec97-330">The remote IP port number.</span></span><br/>                                                  |
| <span data-ttu-id="6ec97-331"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Stands</span><span class="sxs-lookup"><span data-stu-id="6ec97-331"><span id="Status"></span><span id="status"></span><span id="STATUS"></span>Status</span></span><br/>         | <span data-ttu-id="6ec97-332">Der Status oder Fehlercode, der für den Accept-Vorgang zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-332">The status or error code returned for the accept operation.</span></span><br/>                 |



 

## <a name="accept-failed"></a><span data-ttu-id="6ec97-333">Annahme fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="6ec97-333">Accept Failed</span></span>

<span data-ttu-id="6ec97-334">Ereignis-ID = 17</span><span class="sxs-lookup"><span data-stu-id="6ec97-334">Event ID = 17</span></span>

<span data-ttu-id="6ec97-335">Ebene = 4 (Informationen)</span><span class="sxs-lookup"><span data-stu-id="6ec97-335">Level = 4 (Information)</span></span>

<span data-ttu-id="6ec97-336">Die folgenden Winsock-Ereignisse werden für einen fehlgeschlagenen Accept-Vorgang nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-336">The following Winsock events are traced for a failed accept operation:</span></span>

-   <span data-ttu-id="6ec97-337">Eine [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)-, [**akzeptex**](/windows/win32/api/mswsock/nf-mswsock-acceptex)-oder [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Anforderung für ein Sockethandle, das fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="6ec97-337">An [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) request on a socket handle that fails.</span></span>

<span data-ttu-id="6ec97-338">Die folgenden Parameter werden für ein fehlgeschlagenes Accept-Ereignis protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-338">The following parameters are logged for a failed accept event:</span></span>



| <span data-ttu-id="6ec97-339">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-339">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-340">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-340">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-341"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-341"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-342">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-342">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-343"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-343"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-344">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-344">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-345"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit</span><span class="sxs-lookup"><span data-stu-id="6ec97-345"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="6ec97-346">Der für den fehlgeschlagenen Accept-Vorgang zurückgegebene Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6ec97-346">The error code returned for the failing accept operation.</span></span><br/>                   |



 

## <a name="send-posted"></a><span data-ttu-id="6ec97-347">Senden gepostet</span><span class="sxs-lookup"><span data-stu-id="6ec97-347">Send Posted</span></span>

<span data-ttu-id="6ec97-348">Ereignis-ID = 18</span><span class="sxs-lookup"><span data-stu-id="6ec97-348">Event ID = 18</span></span>

<span data-ttu-id="6ec97-349">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-349">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-350">Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports.</span><span class="sxs-lookup"><span data-stu-id="6ec97-350">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="6ec97-351">Die folgenden Winsock-Ereignisse werden nach Vorgängen für Socket Send-und Receive-Puffer nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-351">The following Winsock events are traced for socket send and receive buffer post operations:</span></span>

-   <span data-ttu-id="6ec97-352">Eine Anwendung sendet einen Send-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6ec97-352">An application posts a send.</span></span>
-   <span data-ttu-id="6ec97-353">Ein Sendevorgang wird in Winsock abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ec97-353">A send operation completes to Winsock.</span></span>

<span data-ttu-id="6ec97-354">Die folgenden Parameter werden für Socketsendevorgänge protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-354">The following parameters are logged for socket send operations:</span></span>



| <span data-ttu-id="6ec97-355">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-355">Parameter</span></span>                                                                                                            | <span data-ttu-id="6ec97-356">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-356">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-357"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-357"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="6ec97-358">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-358">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="6ec97-359"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-359"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="6ec97-360">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-360">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="6ec97-361"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="6ec97-361"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="6ec97-362">Ein boolescher Wert, der angibt, ob ein schnelles Pfad-e/a verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6ec97-362">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="6ec97-363"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="6ec97-363"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="6ec97-364">Die Puffer Anzahl.</span><span class="sxs-lookup"><span data-stu-id="6ec97-364">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="6ec97-365"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert</span><span class="sxs-lookup"><span data-stu-id="6ec97-365"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="6ec97-366">Die virtuelle Adresse des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6ec97-366">The virtual address of the buffer.</span></span> <span data-ttu-id="6ec97-367">Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.</span><span class="sxs-lookup"><span data-stu-id="6ec97-367">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="6ec97-368"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge</span><span class="sxs-lookup"><span data-stu-id="6ec97-368"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="6ec97-369">Die Länge des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6ec97-369">The length of the buffer.</span></span> <span data-ttu-id="6ec97-370">Bei verketteten Puffern ist dieser Parameter die Gesamtzahl der Bytes in allen Puffern in der Kette.</span><span class="sxs-lookup"><span data-stu-id="6ec97-370">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="6ec97-371">Wenn FastPath den Wert true hat, wird die Usermode-Adresse des ersten Puffers im Puffer Array im Puffer Parameter protokolliert.</span><span class="sxs-lookup"><span data-stu-id="6ec97-371">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="6ec97-372">Wenn FastPath den Wert false hat, wird die Winsock-Kernel Puffer Adresse im buffer-Parameter protokolliert.</span><span class="sxs-lookup"><span data-stu-id="6ec97-372">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="receive-posted"></a><span data-ttu-id="6ec97-373">Empfangen gesendet</span><span class="sxs-lookup"><span data-stu-id="6ec97-373">Receive Posted</span></span>

<span data-ttu-id="6ec97-374">Ereignis-ID = 19</span><span class="sxs-lookup"><span data-stu-id="6ec97-374">Event ID = 19</span></span>

<span data-ttu-id="6ec97-375">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-375">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-376">Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports.</span><span class="sxs-lookup"><span data-stu-id="6ec97-376">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="6ec97-377">Die folgenden Winsock-Ereignisse werden für Post-Vorgänge des Socket-Empfangspuffers nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-377">The following Winsock events are traced for socket receive buffer post operations:</span></span>

-   <span data-ttu-id="6ec97-378">Eine Anwendung sendet einen Empfangs-.</span><span class="sxs-lookup"><span data-stu-id="6ec97-378">An application posts a receive.</span></span>
-   <span data-ttu-id="6ec97-379">Ein Empfangsvorgang wird in Winsock abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ec97-379">A receive operation completes to Winsock.</span></span>

<span data-ttu-id="6ec97-380">Die folgenden Parameter werden für Socket-Empfangs Vorgänge protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-380">The following parameters are logged for socket receive operations:</span></span>



| <span data-ttu-id="6ec97-381">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-381">Parameter</span></span>                                                                                                            | <span data-ttu-id="6ec97-382">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-382">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-383"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-383"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="6ec97-384">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-384">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="6ec97-385"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-385"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="6ec97-386">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-386">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="6ec97-387"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="6ec97-387"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="6ec97-388">Ein boolescher Wert, der angibt, ob ein schnelles Pfad-e/a verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6ec97-388">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="6ec97-389"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="6ec97-389"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="6ec97-390">Die Puffer Anzahl.</span><span class="sxs-lookup"><span data-stu-id="6ec97-390">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="6ec97-391"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert</span><span class="sxs-lookup"><span data-stu-id="6ec97-391"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="6ec97-392">Die virtuelle Adresse des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6ec97-392">The virtual address of the buffer.</span></span> <span data-ttu-id="6ec97-393">Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.</span><span class="sxs-lookup"><span data-stu-id="6ec97-393">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="6ec97-394"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge</span><span class="sxs-lookup"><span data-stu-id="6ec97-394"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="6ec97-395">Die Länge des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6ec97-395">The length of the buffer.</span></span> <span data-ttu-id="6ec97-396">Bei verketteten Puffern ist dieser Parameter die Gesamtzahl der Bytes in allen Puffern in der Kette.</span><span class="sxs-lookup"><span data-stu-id="6ec97-396">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="6ec97-397">Wenn FastPath den Wert true hat, wird die Usermode-Adresse des ersten Puffers im Puffer Array im Puffer Parameter protokolliert.</span><span class="sxs-lookup"><span data-stu-id="6ec97-397">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="6ec97-398">Wenn FastPath den Wert false hat, wird die Winsock-Kernel Puffer Adresse im buffer-Parameter protokolliert.</span><span class="sxs-lookup"><span data-stu-id="6ec97-398">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="recvfrom-posted"></a><span data-ttu-id="6ec97-399">Recvfrom gepostet</span><span class="sxs-lookup"><span data-stu-id="6ec97-399">RecvFrom Posted</span></span>

<span data-ttu-id="6ec97-400">Ereignis-ID = 20</span><span class="sxs-lookup"><span data-stu-id="6ec97-400">Event ID = 20</span></span>

<span data-ttu-id="6ec97-401">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-401">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-402">Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports.</span><span class="sxs-lookup"><span data-stu-id="6ec97-402">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="6ec97-403">Die folgenden Winsock-Ereignisse werden nach einem postvorgang eines [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) -Puffers für einen Socket nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-403">The following Winsock events are traced for a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) buffer post operation on a socket:</span></span>

-   <span data-ttu-id="6ec97-404">Eine Anwendung sendet einen Receive from-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6ec97-404">An application posts a receive from operation.</span></span>

<span data-ttu-id="6ec97-405">Die folgenden Parameter werden für den Vorgang "recvfrom" protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-405">The following parameters are logged for the recvfrom operation:</span></span>



| <span data-ttu-id="6ec97-406">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-406">Parameter</span></span>                                                                                                            | <span data-ttu-id="6ec97-407">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-407">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-408"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-408"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="6ec97-409">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-409">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="6ec97-410"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-410"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="6ec97-411">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-411">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="6ec97-412"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="6ec97-412"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="6ec97-413">Ein boolescher Wert, der angibt, ob ein schnelles Pfad-e/a verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6ec97-413">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="6ec97-414"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="6ec97-414"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="6ec97-415">Die Puffer Anzahl.</span><span class="sxs-lookup"><span data-stu-id="6ec97-415">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="6ec97-416"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert</span><span class="sxs-lookup"><span data-stu-id="6ec97-416"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="6ec97-417">Die virtuelle Adresse des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6ec97-417">The virtual address of the buffer.</span></span> <span data-ttu-id="6ec97-418">Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.</span><span class="sxs-lookup"><span data-stu-id="6ec97-418">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="6ec97-419"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge</span><span class="sxs-lookup"><span data-stu-id="6ec97-419"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="6ec97-420">Die Länge des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6ec97-420">The length of the buffer.</span></span> <span data-ttu-id="6ec97-421">Bei verketteten Puffern ist dieser Parameter die Gesamtzahl der Bytes in allen Puffern in der Kette.</span><span class="sxs-lookup"><span data-stu-id="6ec97-421">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |



 

<span data-ttu-id="6ec97-422">Wenn FastPath den Wert true hat, wird die Usermode-Adresse des ersten Puffers im Puffer Array im Puffer Parameter protokolliert.</span><span class="sxs-lookup"><span data-stu-id="6ec97-422">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="6ec97-423">Wenn FastPath den Wert false hat, wird die Winsock-Kernel Puffer Adresse im buffer-Parameter protokolliert.</span><span class="sxs-lookup"><span data-stu-id="6ec97-423">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="sendto-posted"></a><span data-ttu-id="6ec97-424">SendTo gepostet</span><span class="sxs-lookup"><span data-stu-id="6ec97-424">SendTo Posted</span></span>

<span data-ttu-id="6ec97-425">Ereignis-ID = 21 (IPv4), Ereignis-ID = 22 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="6ec97-425">Event ID = 21 (IPv4), Event ID = 22 (IPv6)</span></span>

<span data-ttu-id="6ec97-426">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-426">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-427">Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports.</span><span class="sxs-lookup"><span data-stu-id="6ec97-427">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="6ec97-428">Die folgenden Winsock-Ereignisse werden nachverfolgt [**, wenn ein SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) -Puffer postvorgang für einen Socket ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="6ec97-428">The following Winsock events are traced for a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) buffer post operation on a socket:</span></span>

-   <span data-ttu-id="6ec97-429">Eine Anwendung sendet einen Sendevorgang von.</span><span class="sxs-lookup"><span data-stu-id="6ec97-429">An application posts a send from.</span></span>

<span data-ttu-id="6ec97-430">Die folgenden Parameter werden für den [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) -Vorgang protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-430">The following parameters are logged for the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) operation:</span></span>



| <span data-ttu-id="6ec97-431">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-431">Parameter</span></span>                                                                                                            | <span data-ttu-id="6ec97-432">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-432">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-433"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-433"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="6ec97-434">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-434">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                          |
| <span data-ttu-id="6ec97-435"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-435"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="6ec97-436">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-436">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                     |
| <span data-ttu-id="6ec97-437"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span><span class="sxs-lookup"><span data-stu-id="6ec97-437"><span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath</span></span><br/>                 | <span data-ttu-id="6ec97-438">Ein boolescher Wert, der angibt, ob ein schnelles Pfad-e/a verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6ec97-438">A Boolean value that indicates if fast path I/O was used.</span></span><br/>                                                                       |
| <span data-ttu-id="6ec97-439"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="6ec97-439"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="6ec97-440">Die Puffer Anzahl.</span><span class="sxs-lookup"><span data-stu-id="6ec97-440">The buffer count.</span></span><br/>                                                                                                               |
| <span data-ttu-id="6ec97-441"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert</span><span class="sxs-lookup"><span data-stu-id="6ec97-441"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="6ec97-442">Die virtuelle Adresse des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6ec97-442">The virtual address of the buffer.</span></span> <span data-ttu-id="6ec97-443">Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.</span><span class="sxs-lookup"><span data-stu-id="6ec97-443">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/> |
| <span data-ttu-id="6ec97-444"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge</span><span class="sxs-lookup"><span data-stu-id="6ec97-444"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="6ec97-445">Die Länge des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6ec97-445">The length of the buffer.</span></span> <span data-ttu-id="6ec97-446">Bei verketteten Puffern ist dieser Parameter die Gesamtzahl der Bytes in allen Puffern in der Kette.</span><span class="sxs-lookup"><span data-stu-id="6ec97-446">For chained buffers, this parameter is the total number of bytes in all of the buffers in the chain.</span></span><br/>  |
| <span data-ttu-id="6ec97-447"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse</span><span class="sxs-lookup"><span data-stu-id="6ec97-447"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="6ec97-448">Die Remote-IP-Adresse des Sockets.</span><span class="sxs-lookup"><span data-stu-id="6ec97-448">The remote IP address of the socket.</span></span><br/>                                                                                            |
| <span data-ttu-id="6ec97-449"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span><span class="sxs-lookup"><span data-stu-id="6ec97-449"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="6ec97-450">Die Remote-IP-Portnummer des Sockets.</span><span class="sxs-lookup"><span data-stu-id="6ec97-450">The remote IP port number of the socket.</span></span><br/>                                                                                        |



 

<span data-ttu-id="6ec97-451">Wenn FastPath den Wert true hat, wird die Usermode-Adresse des ersten Puffers im Puffer Array im Puffer Parameter protokolliert.</span><span class="sxs-lookup"><span data-stu-id="6ec97-451">When FastPath is true, the usermode address of the first buffer in the array of buffers is logged in the Buffer parameter.</span></span> <span data-ttu-id="6ec97-452">Wenn FastPath den Wert false hat, wird die Winsock-Kernel Puffer Adresse im buffer-Parameter protokolliert.</span><span class="sxs-lookup"><span data-stu-id="6ec97-452">When FastPath is false, the Winsock kernel buffer address is logged in the Buffer parameter.</span></span>

## <a name="recv-completed"></a><span data-ttu-id="6ec97-453">Recv abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="6ec97-453">Recv Completed</span></span>

<span data-ttu-id="6ec97-454">Ereignis-ID = 23</span><span class="sxs-lookup"><span data-stu-id="6ec97-454">Event ID = 23</span></span>

<span data-ttu-id="6ec97-455">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-455">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-456">Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports.</span><span class="sxs-lookup"><span data-stu-id="6ec97-456">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="6ec97-457">Die folgenden Winsock-Ereignisse werden für abgeschlossene Socket-Empfangs Vorgänge nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-457">The following Winsock events are traced for socket receive completed operations:</span></span>

-   <span data-ttu-id="6ec97-458">Ein Sendevorgang wird für den Transport abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ec97-458">A send operation completes to the transport.</span></span>
-   <span data-ttu-id="6ec97-459">Ein Empfangsvorgang wird für den Transport abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ec97-459">A receive operation completes to the transport.</span></span>

<span data-ttu-id="6ec97-460">Die folgenden Parameter werden für den Abschluss eines Sendevorgangs protokolliert, oder der Empfangsvorgang wurde abgeschlossen:</span><span class="sxs-lookup"><span data-stu-id="6ec97-460">The following parameters are logged for a send completed or receive completed:</span></span>



| <span data-ttu-id="6ec97-461">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-461">Parameter</span></span>                                                                                                            | <span data-ttu-id="6ec97-462">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-462">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-463"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-463"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="6ec97-464">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-464">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                                   |
| <span data-ttu-id="6ec97-465"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-465"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="6ec97-466">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-466">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                              |
| <span data-ttu-id="6ec97-467"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert</span><span class="sxs-lookup"><span data-stu-id="6ec97-467"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="6ec97-468">Die virtuelle Adresse des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6ec97-468">The virtual address of the buffer.</span></span> <span data-ttu-id="6ec97-469">Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.</span><span class="sxs-lookup"><span data-stu-id="6ec97-469">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>          |
| <span data-ttu-id="6ec97-470"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge</span><span class="sxs-lookup"><span data-stu-id="6ec97-470"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="6ec97-471">Die Länge des Puffers der empfangenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="6ec97-471">The length of the buffer of bytes received.</span></span> <span data-ttu-id="6ec97-472">Bei verketteten Puffern handelt es sich bei diesem Parameter um die Gesamtanzahl der Bytes, die in allen Puffern der</span><span class="sxs-lookup"><span data-stu-id="6ec97-472">For chained buffers, this parameter is the total bytes received in all buffers in the chain.</span></span><br/> |



 

## <a name="send-completed"></a><span data-ttu-id="6ec97-473">Sendevorgang abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="6ec97-473">Send Completed</span></span>

<span data-ttu-id="6ec97-474">Ereignis-ID = 24</span><span class="sxs-lookup"><span data-stu-id="6ec97-474">Event ID = 24</span></span>

<span data-ttu-id="6ec97-475">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-475">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-476">Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports.</span><span class="sxs-lookup"><span data-stu-id="6ec97-476">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="6ec97-477">Die folgenden Winsock-Ereignisse werden für abgeschlossene Socket Send-Vorgänge nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-477">The following Winsock events are traced for socket send completed operations:</span></span>

-   <span data-ttu-id="6ec97-478">Ein Sendevorgang wird für den Transport abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="6ec97-478">A send operation completes to the transport.</span></span>

<span data-ttu-id="6ec97-479">Die folgenden Parameter werden für den Abschluss eines Sendevorgangs protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-479">The following parameters are logged for a send completed:</span></span>



| <span data-ttu-id="6ec97-480">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-480">Parameter</span></span>                                                                                                            | <span data-ttu-id="6ec97-481">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-481">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-482"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-482"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="6ec97-483">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-483">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="6ec97-484"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-484"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="6ec97-485">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-485">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="6ec97-486"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert</span><span class="sxs-lookup"><span data-stu-id="6ec97-486"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="6ec97-487">Die virtuelle Adresse des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6ec97-487">The virtual address of the buffer.</span></span> <span data-ttu-id="6ec97-488">Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.</span><span class="sxs-lookup"><span data-stu-id="6ec97-488">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="6ec97-489"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge</span><span class="sxs-lookup"><span data-stu-id="6ec97-489"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="6ec97-490">Die Länge des Puffers von gesendeten Bytes.</span><span class="sxs-lookup"><span data-stu-id="6ec97-490">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="6ec97-491">Bei verketteten Puffern handelt es sich bei diesem Parameter um die gesamten bytes, die von allen Puffern in der Kette</span><span class="sxs-lookup"><span data-stu-id="6ec97-491">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |



 

## <a name="sendmsg-completed"></a><span data-ttu-id="6ec97-492">Sendmsg abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="6ec97-492">SendMsg Completed</span></span>

<span data-ttu-id="6ec97-493">Ereignis-ID = 25</span><span class="sxs-lookup"><span data-stu-id="6ec97-493">Event ID = 25</span></span>

<span data-ttu-id="6ec97-494">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-494">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-495">Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports.</span><span class="sxs-lookup"><span data-stu-id="6ec97-495">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="6ec97-496">Die folgenden Winsock-Ereignisse werden nachverfolgt, wenn ein [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Puffer postvorgang für einen Socket abgeschlossen wird:</span><span class="sxs-lookup"><span data-stu-id="6ec97-496">The following Winsock events are traced when a [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="6ec97-497">Eine Anwendung schließt einen [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="6ec97-497">An application completes a [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) operation.</span></span>

<span data-ttu-id="6ec97-498">Die folgenden Parameter werden für die Ausführung von [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-498">The following parameters are logged for the [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) completion:</span></span>



| <span data-ttu-id="6ec97-499">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-499">Parameter</span></span>                                                                                                            | <span data-ttu-id="6ec97-500">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-500">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-501"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-501"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="6ec97-502">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-502">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="6ec97-503"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-503"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="6ec97-504">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-504">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="6ec97-505"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="6ec97-505"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="6ec97-506">Die Puffer Anzahl.</span><span class="sxs-lookup"><span data-stu-id="6ec97-506">The buffer count.</span></span><br/>                                                                                                                  |
| <span data-ttu-id="6ec97-507"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert</span><span class="sxs-lookup"><span data-stu-id="6ec97-507"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="6ec97-508">Die virtuelle Adresse des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6ec97-508">The virtual address of the buffer.</span></span> <span data-ttu-id="6ec97-509">Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.</span><span class="sxs-lookup"><span data-stu-id="6ec97-509">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="6ec97-510"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge</span><span class="sxs-lookup"><span data-stu-id="6ec97-510"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="6ec97-511">Die Länge des Puffers von gesendeten Bytes.</span><span class="sxs-lookup"><span data-stu-id="6ec97-511">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="6ec97-512">Bei verketteten Puffern handelt es sich bei diesem Parameter um die gesamten bytes, die von allen Puffern in der Kette</span><span class="sxs-lookup"><span data-stu-id="6ec97-512">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="6ec97-513"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse</span><span class="sxs-lookup"><span data-stu-id="6ec97-513"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="6ec97-514">Die Remote-IP-Adresse des Sockets.</span><span class="sxs-lookup"><span data-stu-id="6ec97-514">The remote IP address of the socket.</span></span><br/>                                                                                               |
| <span data-ttu-id="6ec97-515"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span><span class="sxs-lookup"><span data-stu-id="6ec97-515"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="6ec97-516">Die Remote-IP-Portnummer des Sockets.</span><span class="sxs-lookup"><span data-stu-id="6ec97-516">The remote IP port number of the socket.</span></span><br/>                                                                                           |



 

## <a name="recvfrom-completed"></a><span data-ttu-id="6ec97-517">Recvfrom abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="6ec97-517">RecvFrom Completed</span></span>

<span data-ttu-id="6ec97-518">Ereignis-ID = 26 (IPv4), Ereignis-ID = 27 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="6ec97-518">Event ID = 26 (IPv4), Event ID = 27 (IPv6)</span></span>

<span data-ttu-id="6ec97-519">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-519">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-520">Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports.</span><span class="sxs-lookup"><span data-stu-id="6ec97-520">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="6ec97-521">Die folgenden Winsock-Ereignisse werden nachverfolgt, wenn ein [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) -Puffer postvorgang für einen Socket abgeschlossen wird:</span><span class="sxs-lookup"><span data-stu-id="6ec97-521">The following Winsock events are traced when a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="6ec97-522">Eine Anwendung schließt einen [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) -Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="6ec97-522">An application completes a [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) operation.</span></span>

<span data-ttu-id="6ec97-523">Die folgenden Parameter werden für [**den Abschluss der**](/windows/desktop/api/winsock/nf-winsock-recvfrom) Wiederholung protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-523">The following parameters are logged for the [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) completion:</span></span>



| <span data-ttu-id="6ec97-524">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-524">Parameter</span></span>                                                                                                            | <span data-ttu-id="6ec97-525">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-525">Description</span></span>                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-526"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-526"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="6ec97-527">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-527">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                                   |
| <span data-ttu-id="6ec97-528"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-528"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="6ec97-529">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-529">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                              |
| <span data-ttu-id="6ec97-530"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="6ec97-530"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="6ec97-531">Die Puffer Anzahl.</span><span class="sxs-lookup"><span data-stu-id="6ec97-531">The buffer count.</span></span><br/>                                                                                                                        |
| <span data-ttu-id="6ec97-532"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert</span><span class="sxs-lookup"><span data-stu-id="6ec97-532"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="6ec97-533">Die virtuelle Adresse des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6ec97-533">The virtual address of the buffer.</span></span> <span data-ttu-id="6ec97-534">Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.</span><span class="sxs-lookup"><span data-stu-id="6ec97-534">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>          |
| <span data-ttu-id="6ec97-535"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge</span><span class="sxs-lookup"><span data-stu-id="6ec97-535"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="6ec97-536">Die Länge des Puffers der empfangenen Bytes.</span><span class="sxs-lookup"><span data-stu-id="6ec97-536">The length of the buffer of bytes received.</span></span> <span data-ttu-id="6ec97-537">Bei verketteten Puffern handelt es sich bei diesem Parameter um die Gesamtanzahl der Bytes, die in allen Puffern der</span><span class="sxs-lookup"><span data-stu-id="6ec97-537">For chained buffers, this parameter is the total bytes received in all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="6ec97-538"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse</span><span class="sxs-lookup"><span data-stu-id="6ec97-538"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="6ec97-539">Die Remote-IP-Adresse des Sockets.</span><span class="sxs-lookup"><span data-stu-id="6ec97-539">The remote IP address of the socket.</span></span><br/>                                                                                                     |
| <span data-ttu-id="6ec97-540"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span><span class="sxs-lookup"><span data-stu-id="6ec97-540"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="6ec97-541">Die Remote-IP-Portnummer des Sockets.</span><span class="sxs-lookup"><span data-stu-id="6ec97-541">The remote IP port number of the socket.</span></span><br/>                                                                                                 |



 

## <a name="sendto-completed"></a><span data-ttu-id="6ec97-542">SendTo abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="6ec97-542">SendTo Completed</span></span>

<span data-ttu-id="6ec97-543">Ereignis-ID = 28</span><span class="sxs-lookup"><span data-stu-id="6ec97-543">Event ID = 28</span></span>

<span data-ttu-id="6ec97-544">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-544">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-545">Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports.</span><span class="sxs-lookup"><span data-stu-id="6ec97-545">In order to diagnose user buffer corruption (for example, when an application re-uses the same buffer in another send or receive call while it's still in use), the data buffer is logged when posted to Winsock and upon completion by the underlying transport.</span></span> <span data-ttu-id="6ec97-546">Die folgenden Winsock-Ereignisse werden nachverfolgt [**, wenn ein SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) -Puffer postvorgang für einen Socket abgeschlossen wird:</span><span class="sxs-lookup"><span data-stu-id="6ec97-546">The following Winsock events are traced when a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) buffer post operation completes on a socket:</span></span>

-   <span data-ttu-id="6ec97-547">Eine Anwendung schließt einen [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) -Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="6ec97-547">An application completes a [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) operation.</span></span>

<span data-ttu-id="6ec97-548">Die folgenden Parameter werden für die Beendigung der [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-548">The following parameters are logged for the [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) completion:</span></span>



| <span data-ttu-id="6ec97-549">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-549">Parameter</span></span>                                                                                                            | <span data-ttu-id="6ec97-550">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-550">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-551"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-551"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                     | <span data-ttu-id="6ec97-552">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-552">The kernel EPROCESS structure address for the process.</span></span><br/>                                                                             |
| <span data-ttu-id="6ec97-553"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-553"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                 | <span data-ttu-id="6ec97-554">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-554">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                                                        |
| <span data-ttu-id="6ec97-555"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span><span class="sxs-lookup"><span data-stu-id="6ec97-555"><span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount</span></span><br/>     | <span data-ttu-id="6ec97-556">Die Puffer Anzahl.</span><span class="sxs-lookup"><span data-stu-id="6ec97-556">The buffer count.</span></span><br/>                                                                                                                  |
| <span data-ttu-id="6ec97-557"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert</span><span class="sxs-lookup"><span data-stu-id="6ec97-557"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer</span></span><br/>                         | <span data-ttu-id="6ec97-558">Die virtuelle Adresse des Puffers.</span><span class="sxs-lookup"><span data-stu-id="6ec97-558">The virtual address of the buffer.</span></span> <span data-ttu-id="6ec97-559">Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.</span><span class="sxs-lookup"><span data-stu-id="6ec97-559">For chained buffers, this parameter is the virtual address of the first buffer in the chain.</span></span><br/>    |
| <span data-ttu-id="6ec97-560"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge</span><span class="sxs-lookup"><span data-stu-id="6ec97-560"><span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength</span></span><br/> | <span data-ttu-id="6ec97-561">Die Länge des Puffers von gesendeten Bytes.</span><span class="sxs-lookup"><span data-stu-id="6ec97-561">The length of the buffer of bytes sent.</span></span> <span data-ttu-id="6ec97-562">Bei verketteten Puffern handelt es sich bei diesem Parameter um die gesamten bytes, die von allen Puffern in der Kette</span><span class="sxs-lookup"><span data-stu-id="6ec97-562">For chained buffers, this parameter is the total bytes sent from all buffers in the chain.</span></span><br/> |
| <span data-ttu-id="6ec97-563"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse</span><span class="sxs-lookup"><span data-stu-id="6ec97-563"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                     | <span data-ttu-id="6ec97-564">Die Remote-IP-Adresse des Sockets.</span><span class="sxs-lookup"><span data-stu-id="6ec97-564">The remote IP address of the socket.</span></span><br/>                                                                                               |
| <span data-ttu-id="6ec97-565"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span><span class="sxs-lookup"><span data-stu-id="6ec97-565"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                 | <span data-ttu-id="6ec97-566">Die Remote-IP-Portnummer des Sockets.</span><span class="sxs-lookup"><span data-stu-id="6ec97-566">The remote IP port number of the socket.</span></span><br/>                                                                                           |



 

## <a name="socket-option-set"></a><span data-ttu-id="6ec97-567">Socketoptionssatz</span><span class="sxs-lookup"><span data-stu-id="6ec97-567">Socket Option Set</span></span>

<span data-ttu-id="6ec97-568">Ereignis-ID = 29</span><span class="sxs-lookup"><span data-stu-id="6ec97-568">Event ID = 29</span></span>

<span data-ttu-id="6ec97-569">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-569">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-570">Wenn eine Anwendung bestimmte socketoptionswerte und IOCTLs ändert, werden die neuen Werte protokolliert.</span><span class="sxs-lookup"><span data-stu-id="6ec97-570">Whenever an application changes certain socket option values and Ioctls, the new values will be logged.</span></span> <span data-ttu-id="6ec97-571">Die protokollierten Optionen können verwendet werden, um eine schlechte Leistung oder ein ungewöhnliches Verhalten in Anwendungen zu diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="6ec97-571">The options logged can be used to diagnose poor performance or strange behavior in applications.</span></span> <span data-ttu-id="6ec97-572">Die folgenden Winsock-Ereignisse werden für bestimmte Socketoptionen und IOCTLs nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-572">The following Winsock events are traced for certain socket options and Ioctls:</span></span>

-   <span data-ttu-id="6ec97-573">\_Sndbuf ändert sich also.</span><span class="sxs-lookup"><span data-stu-id="6ec97-573">SO\_SNDBUF changes.</span></span>
-   <span data-ttu-id="6ec97-574">\_Rcvbuf ändert sich also.</span><span class="sxs-lookup"><span data-stu-id="6ec97-574">SO\_RCVBUF changes.</span></span>
-   <span data-ttu-id="6ec97-575">FIONBIO</span><span class="sxs-lookup"><span data-stu-id="6ec97-575">FIONBIO</span></span>
-   <span data-ttu-id="6ec97-576">SIO \_ Aktivieren von \_ zirkulären \_ Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="6ec97-576">SIO\_ENABLE\_CIRCULAR\_QUEUEING</span></span>
-   <span data-ttu-id="6ec97-577">\_Konfigurations-UDP-Zusammensetzung \_</span><span class="sxs-lookup"><span data-stu-id="6ec97-577">SIO\_UDP\_CONNRESET</span></span>
-   <span data-ttu-id="6ec97-578">\_oobinline</span><span class="sxs-lookup"><span data-stu-id="6ec97-578">SO\_OOBINLINE</span></span>

<span data-ttu-id="6ec97-579">Die folgenden Parameter werden für [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -und [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktionsaufrufe protokolliert, die jeden der obigen Werte ändern:</span><span class="sxs-lookup"><span data-stu-id="6ec97-579">The following parameters are logged for [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) and [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function calls that change any of the above values:</span></span>



| <span data-ttu-id="6ec97-580">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-580">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-581">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-581">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-582"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-582"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-583">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-583">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-584"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-584"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-585">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-585">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-586"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>Andere</span><span class="sxs-lookup"><span data-stu-id="6ec97-586"><span id="Option"></span><span id="option"></span><span id="OPTION"></span>Option</span></span><br/>         | <span data-ttu-id="6ec97-587">Die Socketoption oder IOCTL, die geändert wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-587">The socket option or Ioctl that is changed.</span></span> <br/>                                |
| <span data-ttu-id="6ec97-588"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert</span><span class="sxs-lookup"><span data-stu-id="6ec97-588"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span><br/>             | <span data-ttu-id="6ec97-589">Der neue Wert für die Socketoption oder ioctl.</span><span class="sxs-lookup"><span data-stu-id="6ec97-589">The new value for the socket option or Ioctl.</span></span> <br/>                              |



 

## <a name="selectpoll-posted"></a><span data-ttu-id="6ec97-590">SELECT/Abruf gepostet</span><span class="sxs-lookup"><span data-stu-id="6ec97-590">Select/Poll Posted</span></span>

<span data-ttu-id="6ec97-591">Ereignis-ID = 30</span><span class="sxs-lookup"><span data-stu-id="6ec97-591">Event ID = 30</span></span>

<span data-ttu-id="6ec97-592">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-592">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-593">Die folgenden Winsock-Ereignisse werden nachverfolgt, wenn eine Anwendung die Funktion [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) aufruft:</span><span class="sxs-lookup"><span data-stu-id="6ec97-593">The following Winsock events are traced when an application calls the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function:</span></span>

-   <span data-ttu-id="6ec97-594">Die Anwendung stellt eine [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Anforderung zur Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6ec97-594">Application posts a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) request.</span></span>

<span data-ttu-id="6ec97-595">Die folgenden Parameter werden für [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Ereignisse protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-595">The following parameters are logged for [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) events:</span></span>



| <span data-ttu-id="6ec97-596">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-596">Parameter</span></span>                                                                                                        | <span data-ttu-id="6ec97-597">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-597">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-598"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-598"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                 | <span data-ttu-id="6ec97-599">Die besitzende Prozess-ID.</span><span class="sxs-lookup"><span data-stu-id="6ec97-599">The owning process ID.</span></span><br/>                                                                              |
| <span data-ttu-id="6ec97-600"><span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount</span><span class="sxs-lookup"><span data-stu-id="6ec97-600"><span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount</span></span><br/> | <span data-ttu-id="6ec97-601">Die Anzahl der Handles, die von der Anwendung weitergegeben werden (nur gültig für das initiierende Ereignis).</span><span class="sxs-lookup"><span data-stu-id="6ec97-601">The number of handles passed in by the application (only valid on the initiating event).</span></span><br/>            |
| <span data-ttu-id="6ec97-602"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Zeit</span><span class="sxs-lookup"><span data-stu-id="6ec97-602"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Timeout</span></span><br/>                 | <span data-ttu-id="6ec97-603">Die maximale Zeit, die die [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Funktion warten soll.</span><span class="sxs-lookup"><span data-stu-id="6ec97-603">The maximum time for the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function to wait.</span></span><br/> |



 

## <a name="selectpoll-completed"></a><span data-ttu-id="6ec97-604">SELECT/Abruf abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="6ec97-604">Select/Poll Completed</span></span>

<span data-ttu-id="6ec97-605">Ereignis-ID = 31</span><span class="sxs-lookup"><span data-stu-id="6ec97-605">Event ID = 31</span></span>

<span data-ttu-id="6ec97-606">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-606">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-607">Die folgenden Winsock-Ereignisse werden nachverfolgt, wenn eine Anwendung die Funktion [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) aufruft:</span><span class="sxs-lookup"><span data-stu-id="6ec97-607">The following Winsock events are traced when an application calls the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) function:</span></span>

-   <span data-ttu-id="6ec97-608">Winsock schließt einen [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Befehl ab.</span><span class="sxs-lookup"><span data-stu-id="6ec97-608">Winsock completes a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) call.</span></span>

<span data-ttu-id="6ec97-609">Die folgenden Parameter werden protokolliert, wenn ein [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Vorgang abgeschlossen wird:</span><span class="sxs-lookup"><span data-stu-id="6ec97-609">The following parameters are logged when a [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) operation completes:</span></span>



| <span data-ttu-id="6ec97-610">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-610">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-611">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-611">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-612"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-612"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-613">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-613">The kernel EPROCESS structure address for the process.</span></span><br/>                                              |
| <span data-ttu-id="6ec97-614"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-614"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-615">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-615">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/>                         |
| <span data-ttu-id="6ec97-616"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit</span><span class="sxs-lookup"><span data-stu-id="6ec97-616"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>Error</span></span><br/>             | <span data-ttu-id="6ec97-617">Der für den [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Vorgang zurückgegebene Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="6ec97-617">The error code returned for the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) operation.</span></span><br/> |



 

## <a name="wsaeventselect"></a><span data-ttu-id="6ec97-618">WSAEventSelect</span><span class="sxs-lookup"><span data-stu-id="6ec97-618">WSAEventSelect</span></span>

<span data-ttu-id="6ec97-619">Ereignis-ID = 32</span><span class="sxs-lookup"><span data-stu-id="6ec97-619">Event ID = 32</span></span>

<span data-ttu-id="6ec97-620">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-620">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-621">Die folgenden Winsock-Ereignisse werden nachverfolgt, wenn eine Anwendung die [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) -Funktion aufruft:</span><span class="sxs-lookup"><span data-stu-id="6ec97-621">The following Winsock events are traced when an application calls the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function:</span></span>

-   <span data-ttu-id="6ec97-622">Protokolliert die Ereignis Maske, die in der [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) -Funktion gegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6ec97-622">Log the event mask passed in the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function.</span></span>

<span data-ttu-id="6ec97-623">Die folgenden Parameter werden für [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) -Funktionsaufrufe protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-623">The following parameters are logged for [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function calls:</span></span>



| <span data-ttu-id="6ec97-624">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-624">Parameter</span></span>                                                                                                | <span data-ttu-id="6ec97-625">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-625">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-626"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-626"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>         | <span data-ttu-id="6ec97-627">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-627">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-628"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-628"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>     | <span data-ttu-id="6ec97-629">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-629">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-630"><span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask</span><span class="sxs-lookup"><span data-stu-id="6ec97-630"><span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask</span></span><br/> | <span data-ttu-id="6ec97-631">Der Wert für die Ereignis Maske.</span><span class="sxs-lookup"><span data-stu-id="6ec97-631">The value for the event mask.</span></span> <br/>                                              |



 

## <a name="dropped-datagram"></a><span data-ttu-id="6ec97-632">Gelöschter Datagramm</span><span class="sxs-lookup"><span data-stu-id="6ec97-632">Dropped Datagram</span></span>

<span data-ttu-id="6ec97-633">Ereignis-ID = 33 (IPv4), Ereignis-ID = 34 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="6ec97-633">Event ID = 33 (IPv4), Event ID = 34 (IPv6)</span></span>

<span data-ttu-id="6ec97-634">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-634">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-635">Um Probleme mit datagrammanwendungen zu diagnostizieren, werden die folgenden Winsock-Ereignisse nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-635">To help diagnose issues around datagram applications, the following Winsock events are traced:</span></span>

-   <span data-ttu-id="6ec97-636">Wenn ein Datagramm eintrifft und es gelöscht wird, reicht dies nicht aus.</span><span class="sxs-lookup"><span data-stu-id="6ec97-636">When a datagram arrives and it is dropped do to insufficient buffer space.</span></span>
-   <span data-ttu-id="6ec97-637">Bei einem verbundenen Datagramm, wenn Daten von einer anderen Quelle als dem verbundenen Ziel empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="6ec97-637">On a connected datagram, if data arrives from a source other than connected destination.</span></span>

<span data-ttu-id="6ec97-638">Die folgenden Parameter werden für gelöschte Datagramme protokolliert:</span><span class="sxs-lookup"><span data-stu-id="6ec97-638">The following parameters are logged for dropped datagrams:</span></span>



| <span data-ttu-id="6ec97-639">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-639">Parameter</span></span>                                                                                                    | <span data-ttu-id="6ec97-640">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-640">Description</span></span>                                                                            |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-641"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-641"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>             | <span data-ttu-id="6ec97-642">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-642">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-643"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-643"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>         | <span data-ttu-id="6ec97-644">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-644">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-645"><span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize</span><span class="sxs-lookup"><span data-stu-id="6ec97-645"><span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize</span></span><br/> | <span data-ttu-id="6ec97-646">Die Größe des Pakets, das gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="6ec97-646">The size of the packet that was dropped.</span></span> <br/>                                   |
| <span data-ttu-id="6ec97-647"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse</span><span class="sxs-lookup"><span data-stu-id="6ec97-647"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>             | <span data-ttu-id="6ec97-648">Die IP-Adresse der Quelle des Pakets.</span><span class="sxs-lookup"><span data-stu-id="6ec97-648">The IP address of the source of the packet.</span></span> <br/>                                |
| <span data-ttu-id="6ec97-649"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span><span class="sxs-lookup"><span data-stu-id="6ec97-649"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                         | <span data-ttu-id="6ec97-650">Die IP-Portnummer der Quelle des Pakets.</span><span class="sxs-lookup"><span data-stu-id="6ec97-650">The IP port number of the source of the packet.</span></span><br/>                             |
| <span data-ttu-id="6ec97-651"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Weshalb</span><span class="sxs-lookup"><span data-stu-id="6ec97-651"><span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Reason</span></span><br/>                 | <span data-ttu-id="6ec97-652">Der Fehlercode oder der Grund, warum das Paket gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="6ec97-652">The error code or reason the packet was dropped.</span></span><br/>                            |



 

## <a name="connection-indicated"></a><span data-ttu-id="6ec97-653">Verbindung angegeben</span><span class="sxs-lookup"><span data-stu-id="6ec97-653">Connection Indicated</span></span>

<span data-ttu-id="6ec97-654">Ereignis-ID = 35 (IPv4), Ereignis-ID = 36 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="6ec97-654">Event ID = 35 (IPv4), Event ID = 36 (IPv6)</span></span>

<span data-ttu-id="6ec97-655">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-655">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-656">Die folgenden Winsock-Ereignisse werden für die von der Verbindung genannten Vorgänge nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-656">The following Winsock events are traced for connection indicated operations:</span></span>

-   <span data-ttu-id="6ec97-657">Eine Anwendung empfängt eine Verbindungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="6ec97-657">An application receives a connection request.</span></span>

<span data-ttu-id="6ec97-658">Die folgenden Parameter werden für Verbindungen protokolliert, die von Transport Ereignissen angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="6ec97-658">The following parameters are logged for connections indicated from transport events:</span></span>



| <span data-ttu-id="6ec97-659">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-659">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-660">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-660">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-661"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-661"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-662">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-662">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-663"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-663"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-664">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-664">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-665"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse</span><span class="sxs-lookup"><span data-stu-id="6ec97-665"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>     | <span data-ttu-id="6ec97-666">Die Remote-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="6ec97-666">The remote IP address.</span></span> <br/>                                                     |
| <span data-ttu-id="6ec97-667"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span><span class="sxs-lookup"><span data-stu-id="6ec97-667"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                 | <span data-ttu-id="6ec97-668">Die Remote-IP-Portnummer.</span><span class="sxs-lookup"><span data-stu-id="6ec97-668">The remote IP port number.</span></span><br/>                                                  |



 

## <a name="data-indicated"></a><span data-ttu-id="6ec97-669">Daten angegeben</span><span class="sxs-lookup"><span data-stu-id="6ec97-669">Data Indicated</span></span>

<span data-ttu-id="6ec97-670">Ereignis-ID = 37</span><span class="sxs-lookup"><span data-stu-id="6ec97-670">Event ID = 37</span></span>

<span data-ttu-id="6ec97-671">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-671">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-672">Die folgenden Winsock-Ereignisse werden für Daten, die für die Daten angezeigt werden, verfolgt</span><span class="sxs-lookup"><span data-stu-id="6ec97-672">The following Winsock events are traced for data indicated operations:</span></span>

-   <span data-ttu-id="6ec97-673">Eine Anwendung empfängt Daten auf einem verbundenen Socket.</span><span class="sxs-lookup"><span data-stu-id="6ec97-673">An application receives data on a connected socket.</span></span>

<span data-ttu-id="6ec97-674">Die folgenden Parameter werden für Daten protokolliert, die von Transport Ereignissen angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="6ec97-674">The following parameters are logged for data indicated from transport events:</span></span>



| <span data-ttu-id="6ec97-675">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-675">Parameter</span></span>                                                                                                                        | <span data-ttu-id="6ec97-676">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-676">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-677"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-677"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                                 | <span data-ttu-id="6ec97-678">Die besitzende Prozess-ID.</span><span class="sxs-lookup"><span data-stu-id="6ec97-678">The owning process ID.</span></span><br/>                                                      |
| <span data-ttu-id="6ec97-679"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-679"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                             | <span data-ttu-id="6ec97-680">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-680">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-681"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes angegeben</span><span class="sxs-lookup"><span data-stu-id="6ec97-681"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes Indicated</span></span><br/> | <span data-ttu-id="6ec97-682">Die Anzahl der Bytes, die im Socket empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="6ec97-682">The number of bytes received on the socket.</span></span><br/>                                 |



 

## <a name="data-indicated-from-transport"></a><span data-ttu-id="6ec97-683">Daten, die vom Transport angegeben werden</span><span class="sxs-lookup"><span data-stu-id="6ec97-683">Data Indicated from Transport</span></span>

<span data-ttu-id="6ec97-684">Ereignis-ID = 38 (IPv4), Ereignis-ID = 39 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="6ec97-684">Event ID = 38 (IPv4), Event ID = 39 (IPv6)</span></span>

<span data-ttu-id="6ec97-685">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-685">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-686">Die folgenden Winsock-Ereignisse werden für Daten nachverfolgt, die von Transportvorgängen angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="6ec97-686">The following Winsock events are traced for data indicated from transport operations:</span></span>

-   <span data-ttu-id="6ec97-687">Eine Anwendung sendet eine Empfangs Anforderung und empfängt Daten.</span><span class="sxs-lookup"><span data-stu-id="6ec97-687">An application posts a receive request and receives data.</span></span>

<span data-ttu-id="6ec97-688">Die folgenden Parameter werden für Daten protokolliert, die von Transport Ereignissen angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="6ec97-688">The following parameters are logged for data indicated from transport events:</span></span>



| <span data-ttu-id="6ec97-689">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-689">Parameter</span></span>                                                                                                                        | <span data-ttu-id="6ec97-690">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-690">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-691"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-691"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>                                 | <span data-ttu-id="6ec97-692">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-692">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-693"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-693"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/>                             | <span data-ttu-id="6ec97-694">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-694">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |
| <span data-ttu-id="6ec97-695"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse</span><span class="sxs-lookup"><span data-stu-id="6ec97-695"><span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Address</span></span><br/>                                 | <span data-ttu-id="6ec97-696">Die Remote-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="6ec97-696">The remote IP address.</span></span> <br/>                                                     |
| <span data-ttu-id="6ec97-697"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span><span class="sxs-lookup"><span data-stu-id="6ec97-697"><span id="Port"></span><span id="port"></span><span id="PORT"></span>Port</span></span><br/>                                             | <span data-ttu-id="6ec97-698">Die Remote-IP-Portnummer.</span><span class="sxs-lookup"><span data-stu-id="6ec97-698">The remote IP port number.</span></span><br/>                                                  |
| <span data-ttu-id="6ec97-699"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes angegeben</span><span class="sxs-lookup"><span data-stu-id="6ec97-699"><span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes Indicated</span></span><br/> | <span data-ttu-id="6ec97-700">Die Anzahl der Bytes, die im Socket empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="6ec97-700">The number of bytes received on the socket.</span></span><br/>                                 |



 

## <a name="disconnect-indicated-from-transport"></a><span data-ttu-id="6ec97-701">Verbindung wird vom Transport angegeben</span><span class="sxs-lookup"><span data-stu-id="6ec97-701">Disconnect Indicated from Transport</span></span>

<span data-ttu-id="6ec97-702">Ereignis-ID = 41</span><span class="sxs-lookup"><span data-stu-id="6ec97-702">Event ID = 41</span></span>

<span data-ttu-id="6ec97-703">Ebene = 5 (ausführlich)</span><span class="sxs-lookup"><span data-stu-id="6ec97-703">Level = 5 (Verbose)</span></span>

<span data-ttu-id="6ec97-704">Die folgenden Winsock-Ereignisse werden für die durch Trenn Vorgänge gekennzeichneten Vorgänge nachverfolgt:</span><span class="sxs-lookup"><span data-stu-id="6ec97-704">The following Winsock events are traced for disconnect indicated operations:</span></span>

-   <span data-ttu-id="6ec97-705">Eine Anwendung empfängt eine Disconnect-Anzeige.</span><span class="sxs-lookup"><span data-stu-id="6ec97-705">An application receives a disconnect indication.</span></span>

<span data-ttu-id="6ec97-706">Die folgenden Parameter werden für die Trennung protokolliert, die von Transport Ereignissen angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="6ec97-706">The following parameters are logged for disconnect indicated from transport events:</span></span>



| <span data-ttu-id="6ec97-707">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ec97-707">Parameter</span></span>                                                                                            | <span data-ttu-id="6ec97-708">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ec97-708">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec97-709"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS</span><span class="sxs-lookup"><span data-stu-id="6ec97-709"><span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Process</span></span><br/>     | <span data-ttu-id="6ec97-710">Die Kernel-EPROCESS-Struktur Adresse für den Prozess.</span><span class="sxs-lookup"><span data-stu-id="6ec97-710">The kernel EPROCESS structure address for the process.</span></span><br/>                      |
| <span data-ttu-id="6ec97-711"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher</span><span class="sxs-lookup"><span data-stu-id="6ec97-711"><span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint</span></span><br/> | <span data-ttu-id="6ec97-712">Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ec97-712">The Winsock kernel socket address used as a unique identifier for a socket.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="6ec97-713">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ec97-713">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ec97-714">Kontrolle über die Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="6ec97-714">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="6ec97-715">Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="6ec97-715">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="6ec97-716">Details zur Änderung der Winsock-Katalog Änderung</span><span class="sxs-lookup"><span data-stu-id="6ec97-716">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="6ec97-717">Winsock-Ablauf Verfolgungs Ebenen</span><span class="sxs-lookup"><span data-stu-id="6ec97-717">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> </dl>

 

 
