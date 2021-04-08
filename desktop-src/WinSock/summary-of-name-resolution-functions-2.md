---
description: 'Die namens Auflösungs Funktionen können in drei Kategorien unterteilt werden: Dienst Installation, Client Abfragen und Hilfsobjekte (mit Makros).'
ms.assetid: c16a7163-11f5-4ad6-9df1-9bad2a964e48
title: Zusammenfassung der namens Auflösungs Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5969cb2cf145124446374dcb86eb1e0a8a837c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751400"
---
# <a name="summary-of-name-resolution-functions"></a><span data-ttu-id="287ab-103">Zusammenfassung der namens Auflösungs Funktionen</span><span class="sxs-lookup"><span data-stu-id="287ab-103">Summary of Name Resolution Functions</span></span>

<span data-ttu-id="287ab-104">Die namens Auflösungs Funktionen können in drei Kategorien unterteilt werden: Dienst Installation, Client Abfragen und Hilfsobjekte (mit Makros).</span><span class="sxs-lookup"><span data-stu-id="287ab-104">The name resolution functions can be grouped into three categories: Service installation, client queries, and helper (with macros).</span></span> <span data-ttu-id="287ab-105">In den folgenden Abschnitten werden die Funktionen in den einzelnen Kategorien identifiziert und die beabsichtigte Verwendung kurz beschrieben.</span><span class="sxs-lookup"><span data-stu-id="287ab-105">The sections that follow identify the functions in each category and briefly describe their intended use.</span></span> <span data-ttu-id="287ab-106">Wichtige Datenstrukturen werden ebenfalls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="287ab-106">Key data structures are also described.</span></span>

## <a name="service-installation"></a><span data-ttu-id="287ab-107">Dienst Installation</span><span class="sxs-lookup"><span data-stu-id="287ab-107">Service Installation</span></span>

-   [<span data-ttu-id="287ab-108">**Wsainstallserviceclass**</span><span class="sxs-lookup"><span data-stu-id="287ab-108">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
-   [<span data-ttu-id="287ab-109">**Wsareviveserviceclass**</span><span class="sxs-lookup"><span data-stu-id="287ab-109">**WSARemoveServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
-   [<span data-ttu-id="287ab-110">**Wsasetservice**</span><span class="sxs-lookup"><span data-stu-id="287ab-110">**WSASetService**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

<span data-ttu-id="287ab-111">Wenn die erforderliche Dienstklasse nicht bereits vorhanden ist, wird von einer Anwendung [**wsainstallserviceclass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) verwendet, um eine neue Dienstklasse zu installieren. hierzu werden ein Dienst Klassenname, eine GUID für den Dienst Klassen Bezeichner und eine Reihe von [**wsansclassinfo**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) -Strukturen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="287ab-111">When the required service class does not already exist, an application uses [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) to install a new service class by supplying a service class name, a GUID for the service class identifier, and a series of [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) structures.</span></span> <span data-ttu-id="287ab-112">Diese Strukturen sind jeweils spezifisch für einen bestimmten Namespace und geben allgemeine Werte wie empfohlene TCP-Portnummern oder NetWare-SAP-IDs an.</span><span class="sxs-lookup"><span data-stu-id="287ab-112">These structures are each specific to a particular namespace, and supply common values such as recommended TCP port numbers or NetWare SAP Identifiers.</span></span> <span data-ttu-id="287ab-113">Eine Dienstklasse kann entfernt werden, indem Sie [**wsarewveserviceclass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) aufrufen und die GUID angeben, die dem Klassen Bezeichner entspricht.</span><span class="sxs-lookup"><span data-stu-id="287ab-113">A service class can be removed by calling [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) and supplying the GUID corresponding to the class identifier.</span></span>

<span data-ttu-id="287ab-114">Sobald eine Dienstklasse vorhanden ist, können bestimmte Instanzen eines Dienstanbieter mithilfe von [**wsasetservice**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)installiert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="287ab-114">Once a service class exists, specific instances of a service can be installed or removed through [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea).</span></span> <span data-ttu-id="287ab-115">Diese Funktion nimmt eine [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur als Eingabeparameter zusammen mit einem Vorgangs Code und Vorgangs Flags an.</span><span class="sxs-lookup"><span data-stu-id="287ab-115">This function takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as an input parameter along with an operation code and operation flags.</span></span> <span data-ttu-id="287ab-116">Der Vorgangs Code gibt an, ob der Dienst installiert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="287ab-116">The operation code indicates whether the service is being installed or removed.</span></span> <span data-ttu-id="287ab-117">Die **wsaqueryset** -Struktur stellt alle relevanten Informationen über den Dienst bereit, einschließlich der Dienst Klassen-ID, des Dienst namens (für diese Instanz), der anwendbaren Namespace-ID und der Protokollinformationen sowie einer Gruppe von Transport Adressen, die vom Dienst überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="287ab-117">The **WSAQUERYSET** structure provides all of the relevant information about the service including service class identifier, service name (for this instance), applicable namespace identifier and protocol information, and a set of transport addresses at which the service listens.</span></span> <span data-ttu-id="287ab-118">Dienste sollten **wsasetservice** aufrufen, wenn diese initialisiert werden, um Ihre Anwesenheit in dynamischen Namespaces ankündigen zu können.</span><span class="sxs-lookup"><span data-stu-id="287ab-118">Services should invoke **WSASetService** when they initialize to advertise their presence in dynamic namespaces.</span></span>

## <a name="client-query"></a><span data-ttu-id="287ab-119">Client Abfrage</span><span class="sxs-lookup"><span data-stu-id="287ab-119">Client Query</span></span>

-   [<span data-ttu-id="287ab-120">**Wsaenumnamespaceproviders**</span><span class="sxs-lookup"><span data-stu-id="287ab-120">**WSAEnumNameSpaceProviders**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
-   [<span data-ttu-id="287ab-121">**Wsalookupservicebegin**</span><span class="sxs-lookup"><span data-stu-id="287ab-121">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
-   [<span data-ttu-id="287ab-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="287ab-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
-   [<span data-ttu-id="287ab-123">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="287ab-123">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

<span data-ttu-id="287ab-124">Mithilfe der Funktion [**wsaenumnamespaceproviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) kann eine Anwendung ermitteln, auf welche Namespaces über die Winsock-namens Auflösungs Funktionen zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="287ab-124">The [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) function allows an application to discover which namespaces are accessible through Winsock name resolution facilities.</span></span> <span data-ttu-id="287ab-125">Außerdem kann eine Anwendung ermitteln, ob ein bestimmter Namespace von mehreren Namespace Anbietern unterstützt wird, und die Anbieter-ID für einen bestimmten Namespace Anbieter ermitteln.</span><span class="sxs-lookup"><span data-stu-id="287ab-125">It also allows an application to determine whether a given namespace is supported by more than one namespace provider, and to discover the provider identifier for any particular namespace provider.</span></span> <span data-ttu-id="287ab-126">Mithilfe eines Anbieter Bezeichners kann die Anwendung einen Abfrage Vorgang auf einen angegebenen Namespace Anbieter beschränken.</span><span class="sxs-lookup"><span data-stu-id="287ab-126">Using a provider identifier, the application can restrict a query operation to a specified namespace provider.</span></span>

<span data-ttu-id="287ab-127">Winsock-Namespace – Abfrage Vorgänge beinhalten eine Reihe von aufrufen: [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), gefolgt von einem oder mehreren Aufrufen von [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) und endend mit einem Aufruf von [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span><span class="sxs-lookup"><span data-stu-id="287ab-127">Winsock namespace–query operations involve a series of calls: [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), followed by one or more calls to [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) and ending with a call to [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span></span> <span data-ttu-id="287ab-128">**Wsalookupservicebegin** übernimmt eine [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur als Eingabe, um die Abfrage Parameter zusammen mit einem Satz von Flags zu definieren, um eine zusätzliche Kontrolle über den Suchvorgang bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="287ab-128">**WSALookupServiceBegin** takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as input to define the query parameters along with a set of flags to provide additional control over the search operation.</span></span> <span data-ttu-id="287ab-129">Es wird ein Abfrage Handle zurückgegeben, das bei nachfolgenden Aufrufen von **WSALookupServiceNext** und **WSALookupServiceEnd** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="287ab-129">It returns a query handle which is used in the subsequent calls to **WSALookupServiceNext** and **WSALookupServiceEnd**.</span></span>

<span data-ttu-id="287ab-130">Die Anwendung ruft [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) auf, um Abfrageergebnisse abzurufen, wobei Ergebnisse in einem von der Anwendung bereitgestellten [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Puffer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="287ab-130">The application invokes [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) to obtain query results, with results supplied in an application-supplied [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) buffer.</span></span> <span data-ttu-id="287ab-131">Die Anwendung ruft weiterhin **WSALookupServiceNext** auf, bis der Fehlercode WSA \_ E \_ nicht \_ mehr zurückgegeben wird, was darauf hinweist, dass alle Ergebnisse abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="287ab-131">The application continues to call **WSALookupServiceNext** until the error code WSA\_E\_NO\_MORE is returned indicating that all results have been retrieved.</span></span> <span data-ttu-id="287ab-132">Die Suche wird dann durch einen [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)-Aufrufvorgang beendet.</span><span class="sxs-lookup"><span data-stu-id="287ab-132">The search is then terminated by a call to [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span></span> <span data-ttu-id="287ab-133">Die **WSALookupServiceEnd** -Funktion kann auch verwendet werden, um einen aktuell ausstehenden **WSALookupServiceNext** abzubrechen, wenn er von einem anderen Thread aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="287ab-133">The **WSALookupServiceEnd** function can also be used to cancel a currently pending **WSALookupServiceNext** when called from another thread.</span></span>

<span data-ttu-id="287ab-134">In Windows Sockets 2 werden widersprüchliche Fehlercodes für wsaumomore (10102) und WSA \_ E \_ nicht \_ mehr (10110) definiert.</span><span class="sxs-lookup"><span data-stu-id="287ab-134">In Windows Sockets 2, conflicting error codes are defined for WSAENOMORE (10102) and WSA\_E\_NO\_MORE (10110).</span></span> <span data-ttu-id="287ab-135">Der Fehlercode wsaeromore wird in einer zukünftigen Version entfernt, und nur WSA \_ E \_ \_ bleibt erhalten.</span><span class="sxs-lookup"><span data-stu-id="287ab-135">The error code WSAENOMORE will be removed in a future version and only WSA\_E\_NO\_MORE will remain.</span></span> <span data-ttu-id="287ab-136">Für Windows Sockets 2 sollten Anwendungen jedoch sowohl auf wsaenomore als auch auf WSA \_ E \_ nicht mehr zugreifen, \_ um die größtmögliche Kompatibilität mit Namespace Anbietern zu ermöglichen, die beide verwenden.</span><span class="sxs-lookup"><span data-stu-id="287ab-136">For Windows Sockets 2, however, applications should check for both WSAENOMORE and WSA\_E\_NO\_MORE for the widest possible compatibility with namespace providers that use either one.</span></span>

## <a name="helper-functions"></a><span data-ttu-id="287ab-137">Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="287ab-137">Helper Functions</span></span>

-   [<span data-ttu-id="287ab-138">**Wsagetserviceclassnamebyclassid**</span><span class="sxs-lookup"><span data-stu-id="287ab-138">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
-   [<span data-ttu-id="287ab-139">**Wsaadresssstostring**</span><span class="sxs-lookup"><span data-stu-id="287ab-139">**WSAAddressToString**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa)
-   [<span data-ttu-id="287ab-140">**WSAStringToAddress**</span><span class="sxs-lookup"><span data-stu-id="287ab-140">**WSAStringToAddress**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa)
-   [<span data-ttu-id="287ab-141">**Wsagetserviceclassinfo**</span><span class="sxs-lookup"><span data-stu-id="287ab-141">**WSAGetServiceClassInfo**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa)

<span data-ttu-id="287ab-142">Die Hilfsfunktionen für die Namensauflösung enthalten eine Funktion zum Abrufen eines Dienst Klassen namens mit einer Dienst Klassen Kennung, einem Funktions Paar, mit dem eine Transport Adresse zwischen einer [**sockaddr**](sockaddr-2.md) -Struktur und einer ASCII-Zeichen folgen Darstellung, einer Funktion zum Abrufen der Dienst Klassen Schema Informationen für eine bestimmte Dienstklasse und einer Reihe von Makros für die Zuordnung bekannter Dienste zu vorab zugeordneten GUIDs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="287ab-142">The name resolution helper functions include a function to retrieve a service class name given a service class identifier, a pair of functions used to translate a transport address between a [**SOCKADDR**](sockaddr-2.md) structure and an ASCII string representation, a function to retrieve the service class schema information for a given service class, and a set of macros for mapping well known services to preallocated GUIDs.</span></span>

<span data-ttu-id="287ab-143">Die folgenden Makros aus Winsock2. h unterstützen die Zuordnung zwischen bekannten Dienst Klassen und diesen Namespaces:</span><span class="sxs-lookup"><span data-stu-id="287ab-143">The following macros from Winsock2.h aid in mapping between well known service classes and these namespaces:</span></span>

| <span data-ttu-id="287ab-144">Makro</span><span class="sxs-lookup"><span data-stu-id="287ab-144">Macro</span></span>                                                                                                            | <span data-ttu-id="287ab-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="287ab-145">Description</span></span>                                                                                                                |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="287ab-146">Svcid \_ TCP (Port) svcid \_ UDP (Port)</span><span class="sxs-lookup"><span data-stu-id="287ab-146">SVCID\_TCP(Port) SVCID\_UDP(Port)</span></span><br/> <span data-ttu-id="287ab-147">Svcid- \_ NetWare (Objekttyp)</span><span class="sxs-lookup"><span data-stu-id="287ab-147">SVCID\_NETWARE(Object Type)</span></span><br/>                              | <span data-ttu-id="287ab-148">Bei einem Port für TCP/IP oder UDP/IP oder dem Objekttyp im Fall von NetWare wird die GUID (Portnummer in der Reihenfolge der Hosts) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="287ab-148">Given a port for TCP/IP or UDP/IP or the object type in the case of NetWare, returns the GUID (port number in host order).</span></span> |
| <span data-ttu-id="287ab-149">ist \_ svcid \_ TCP (GUID) ist \_ svcid \_ UDP (GUID)</span><span class="sxs-lookup"><span data-stu-id="287ab-149">IS\_SVCID\_TCP(GUID)IS\_SVCID\_UDP(GUID)</span></span><br/> <span data-ttu-id="287ab-150">ist \_ svcid \_ NetWare (GUID)</span><span class="sxs-lookup"><span data-stu-id="287ab-150">IS\_SVCID\_NETWARE(GUID)</span></span><br/>                          | <span data-ttu-id="287ab-151">Gibt **true** zurück, wenn die GUID innerhalb des zulässigen Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="287ab-151">Returns **TRUE** if the GUID is within the allowable range.</span></span>                                                                |
| <span data-ttu-id="287ab-152">Festlegen der \_ TCP- \_ svcid (GUID, Port) festlegen der \_ UDP- \_ svcid (GUID, Port)</span><span class="sxs-lookup"><span data-stu-id="287ab-152">SET\_TCP\_SVCID(GUID, port)SET\_UDP\_SVCID(GUID, port)</span></span><br/>                                                | <span data-ttu-id="287ab-153">Initialisiert eine GUID-Struktur mit der GUID-Entsprechung für eine TCP-oder UDP-Portnummer (die Portnummer muss in der Reihenfolge der Hosts angegeben werden).</span><span class="sxs-lookup"><span data-stu-id="287ab-153">Initializes a GUID structure with the GUID equivalent for a TCP or UDP port number (port number must be in host order).</span></span>    |
| <span data-ttu-id="287ab-154">Port \_ vom \_ svcid- \_ TCP-Port (GUID) \_ von \_ svcid \_ UDP (GUID)</span><span class="sxs-lookup"><span data-stu-id="287ab-154">PORT\_FROM\_SVCID\_TCP(GUID)PORT\_FROM\_SVCID\_UDP(GUID)</span></span><br/> <span data-ttu-id="287ab-155">SAPID \_ von \_ svcid \_ NetWare (GUID)</span><span class="sxs-lookup"><span data-stu-id="287ab-155">SAPID\_FROM\_SVCID\_NETWARE(GUID)</span></span><br/> | <span data-ttu-id="287ab-156">Gibt den Port oder Objekttyp zurück, der der GUID (Portnummer in der Host Reihenfolge) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="287ab-156">Returns the port or object type associated with the GUID (port number in host order).</span></span>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="287ab-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="287ab-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="287ab-158">**getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="287ab-158">**getaddrinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[<span data-ttu-id="287ab-159">**GetAddrInfoEx**</span><span class="sxs-lookup"><span data-stu-id="287ab-159">**GetAddrInfoEx**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
</dt> <dt>

[<span data-ttu-id="287ab-160">**Getaddrinfow**</span><span class="sxs-lookup"><span data-stu-id="287ab-160">**GetAddrInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
</dt> <dt>

[<span data-ttu-id="287ab-161">**getnameingefo**</span><span class="sxs-lookup"><span data-stu-id="287ab-161">**getnameinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
</dt> <dt>

[<span data-ttu-id="287ab-162">**Getnameingefow**</span><span class="sxs-lookup"><span data-stu-id="287ab-162">**GetNameInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)
</dt> <dt>

[<span data-ttu-id="287ab-163">Datenstrukturen für die Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="287ab-163">Name Resolution Data Structures</span></span>](name-resolution-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="287ab-164">Namens Auflösungs Modell</span><span class="sxs-lookup"><span data-stu-id="287ab-164">Name Resolution Model</span></span>](name-resolution-model-2.md)
</dt> <dt>

[<span data-ttu-id="287ab-165">Protokoll unabhängige Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="287ab-165">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="287ab-166">Registrierung und Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="287ab-166">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="287ab-167">**SOCKADDR**</span><span class="sxs-lookup"><span data-stu-id="287ab-167">**SOCKADDR**</span></span>](sockaddr-2.md)
</dt> <dt>

[<span data-ttu-id="287ab-168">**Wsaenumnamespaceproviders**</span><span class="sxs-lookup"><span data-stu-id="287ab-168">**WSAEnumNameSpaceProviders**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
</dt> <dt>

[<span data-ttu-id="287ab-169">**Wsagetserviceclassnamebyclassid**</span><span class="sxs-lookup"><span data-stu-id="287ab-169">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[<span data-ttu-id="287ab-170">**Wsainstallserviceclass**</span><span class="sxs-lookup"><span data-stu-id="287ab-170">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[<span data-ttu-id="287ab-171">**Wsalookupservicebegin**</span><span class="sxs-lookup"><span data-stu-id="287ab-171">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="287ab-172">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="287ab-172">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="287ab-173">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="287ab-173">**WSALookupServiceNext**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="287ab-174">**Wsareviveserviceclass**</span><span class="sxs-lookup"><span data-stu-id="287ab-174">**WSARemoveServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
</dt> <dt>

[<span data-ttu-id="287ab-175">**Wsasetservice**</span><span class="sxs-lookup"><span data-stu-id="287ab-175">**WSASetService**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)
</dt> <dt>

[<span data-ttu-id="287ab-176">**Wsaqueryset**</span><span class="sxs-lookup"><span data-stu-id="287ab-176">**WSAQUERYSET**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="287ab-177">**Wsansclassinfo**</span><span class="sxs-lookup"><span data-stu-id="287ab-177">**WSANSCLASSINFO**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)
</dt> </dl>

 

 




