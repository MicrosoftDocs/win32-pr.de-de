---
description: NLA-Clients können Netzwerk Konfigurationsinformationen auf systemweite Basis aufzeichnen, sodass zukünftige Abfragen die angegebenen Konfigurationsinformationen unabhängig davon zurückgeben können, ob das Netzwerk aktiv ist.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Registrieren einer Dienst Instanz bei NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae2e73e638e4bf0152c2c6c5a4f5ab87dda7312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348550"
---
# <a name="registering-a-service-instance-with-nla"></a><span data-ttu-id="b178c-103">Registrieren einer Dienst Instanz bei NLA</span><span class="sxs-lookup"><span data-stu-id="b178c-103">Registering a Service Instance with NLA</span></span>

<span data-ttu-id="b178c-104">NLA-Clients können Netzwerk Konfigurationsinformationen auf systemweite Basis aufzeichnen, sodass zukünftige Abfragen die angegebenen Konfigurationsinformationen unabhängig davon zurückgeben können, ob das Netzwerk aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="b178c-104">NLA clients can record network configuration information on a system-wide basis, enabling future queries to return the specified configuration information regardless of whether the network is active.</span></span> <span data-ttu-id="b178c-105">Diese Funktion ermöglicht es NLA-Clients, eine konsistente Netzwerk Informations Benutzer-Benutzer Funktionalität über mehrere Anwendungen hinweg zu beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="b178c-105">This capability allows NLA clients to affect a consistent network information user experience across multiple applications.</span></span>

## <a name="parameters"></a><span data-ttu-id="b178c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b178c-106">Parameters</span></span>

<span data-ttu-id="b178c-107">Verwenden Sie die [**wsasetservice**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) -Funktion, um eine Dienst Instanz beim Network Location Awareness Service-Anbieter zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="b178c-107">To register a service instance with the Network Location Awareness service provider, use the [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) function.</span></span> <span data-ttu-id="b178c-108">Um eine Dienst Instanz ordnungsgemäß zu registrieren, müssen bestimmte Parameter der **wsasetservice** -Funktion mit den entsprechenden Informationen festgelegt werden, wie in diesem Abschnitt erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="b178c-108">In order to properly register a service instance certain parameters of the **WSASetService** function must be set with the appropriate information, as explained in this section.</span></span> <span data-ttu-id="b178c-109">Die **wsasetservice** -Funktion weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="b178c-109">For quick reference, the **WSASetService** function has the following syntax:</span></span>

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

<span data-ttu-id="b178c-110">Geben Sie für den *lpqsreginfo* -Parameter eine [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur entweder aus einem NLA SP-Abfrageergebnis an, oder erstellen Sie die Anforderungen einer NLA SP-Abfrage, wie unter [Abfragen von NLA](querying-nla-2.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="b178c-110">For the *lpqsRegInfo* parameter, provide a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure from either an NLA SP query result, or constructed adhering to the requirements of an NLA SP query, as specified in [Querying NLA](querying-nla-2.md).</span></span>

<span data-ttu-id="b178c-111">Folgende Vorgänge werden für den Parameter " *ESS Operation* " unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b178c-111">Operations supported for the *essOperation* parameter are the following:</span></span>

<dl> <dt>

<span data-ttu-id="b178c-112"><span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>rnrservice- \_ Registrierung</span><span class="sxs-lookup"><span data-stu-id="b178c-112"><span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>RNRSERVICE\_REGISTER</span></span>
</dt> <dd>

<span data-ttu-id="b178c-113">Das in der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur in *lpqsreginfo* angegebene Netzwerk wird für den aktiven Benutzer persistent gemacht, indem die Netzwerk Instanz in der Registrierungs Struktur für den aktuellen Benutzer gespeichert wird, wodurch der Identitätswechsel ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="b178c-113">The network defined in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure provided in *lpqsRegInfo* is made persistent for the active user by storing the network instance in the registry hive for the current user, which allows impersonation.</span></span>

</dd> <dt>

<span data-ttu-id="b178c-114"><span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>rnrservice \_ Löschen</span><span class="sxs-lookup"><span data-stu-id="b178c-114"><span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE\_DELETE</span></span>
</dt> <dd>

<span data-ttu-id="b178c-115">Wenn das in der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur in *lpqsreginfo* angegebene Netzwerk persistent ist, wird es entfernt.</span><span class="sxs-lookup"><span data-stu-id="b178c-115">If the network defined in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure provided in *lpqsRegInfo* is persistent, it will be removed.</span></span>

</dd> </dl>

<span data-ttu-id="b178c-116">Der im Parameter " *ESS Operation* " angegebene Vorgang kann mit den folgenden Optionen geändert werden, die mit binary oder Logic angegeben werden können:</span><span class="sxs-lookup"><span data-stu-id="b178c-116">The operation specified in the *essOperation* parameter can be modified by the following options, which can be specified with binary OR logic:</span></span>

<dl> <dt>

<span data-ttu-id="b178c-117"><span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>NLA-Anzeige \_ \_ Name</span><span class="sxs-lookup"><span data-stu-id="b178c-117"><span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>NLA\_FRIENDLY\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="b178c-118">Bei Verwendung mit rnrservice- \_ Register wird das *lpszcomment* -Feld des in *lpqsreginfo* definierten Netzwerks auf Gültigkeit überprüft und dauerhaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b178c-118">When used with RNRSERVICE\_REGISTER, the *lpszComment* field of the network defined in *lpqsRegInfo* is checked for validity and stored persistently.</span></span> <span data-ttu-id="b178c-119">Bei Verwendung mit rnrservice \_ delete und dem definierten Netzwerk mit einem anzeigen Amen wird der Anzeige Name entfernt, aber der Netzwerk Eintrag bleibt intakt.</span><span class="sxs-lookup"><span data-stu-id="b178c-119">When used with RNRSERVICE\_DELETE and the defined network has a friendly name, the friendly name is removed but the network entry is left intact.</span></span>

</dd> <dt>

<span data-ttu-id="b178c-120"><span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>NLA- \_ ALLUSERS- \_ Netzwerk</span><span class="sxs-lookup"><span data-stu-id="b178c-120"><span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>NLA\_ALLUSERS\_NETWORK</span></span>
</dt> <dd>

<span data-ttu-id="b178c-121">Bei Verwendung mit dem rnrservice- \_ Register wird der Eintrag dauerhaft unter HKEY \_ local \_ Machine gespeichert, sodass er während der Abfragen für alle Benutzer auf dem lokalen Computer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b178c-121">When used with RNRSERVICE\_REGISTER, the entry is stored persistently under HKEY\_LOCAL\_MACHINE, making it available during queries to all users on the local computer.</span></span> <span data-ttu-id="b178c-122">Bei Verwendung mit rnrservice \_ Delete wird das angegebene Netzwerk von HKEY \_ Local Machine entfernt \_ .</span><span class="sxs-lookup"><span data-stu-id="b178c-122">When used with RNRSERVICE\_DELETE, the specified network is removed from HKEY\_LOCAL\_MACHINE.</span></span> <span data-ttu-id="b178c-123">Wenn das angegebene Netzwerk nicht vorhanden ist, wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b178c-123">An error is returned if the specified network is not present.</span></span> <span data-ttu-id="b178c-124">Um ein Netzwerk aus der Registrierungs Struktur des aktuellen Benutzers zu löschen, darf dieses Flag nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b178c-124">In order to delete a network from the registry hive of the current user, this flag must not be specified.</span></span> <span data-ttu-id="b178c-125">Dieses Flag ist nur im Sicherheitskontext eines lokalen Systemadministrators gültig.</span><span class="sxs-lookup"><span data-stu-id="b178c-125">This flag is only valid in the security context of a local system administrator.</span></span>

</dd> </dl>

<span data-ttu-id="b178c-126">NLA unterstützt die folgenden Fehlercodes für [**wsasetservice**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) -Funktionsaufrufe:</span><span class="sxs-lookup"><span data-stu-id="b178c-126">NLA supports the following error codes for [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) function calls:</span></span>

| <span data-ttu-id="b178c-127">Fehler</span><span class="sxs-lookup"><span data-stu-id="b178c-127">Error</span></span>             | <span data-ttu-id="b178c-128">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b178c-128">Meaning</span></span>                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b178c-129">WSANOTINITIALISED</span><span class="sxs-lookup"><span data-stu-id="b178c-129">WSANOTINITIALISED</span></span> | <span data-ttu-id="b178c-130">Ein erfolgreicher Rückruf der [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Funktion zum Initialisieren der NLA wurde nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b178c-130">A successful call to the [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function to initialize NLA was not performed.</span></span>                                                                  |
| <span data-ttu-id="b178c-131">Wsaeaccess</span><span class="sxs-lookup"><span data-stu-id="b178c-131">WSAEACCESS</span></span>        | <span data-ttu-id="b178c-132">Das Netzwerk "NLA \_ ALLUSERS" \_ wurde in " *dwcontrolflags* " angegeben, während es sich nicht im Sicherheitskontext eines lokalen Systemadministrators befand.</span><span class="sxs-lookup"><span data-stu-id="b178c-132">NLA\_ALLUSERS\_NETWORK was specified in *dwControlFlags* while not in the security context of a local system administrator.</span></span>                                                |
| <span data-ttu-id="b178c-133">Wsaebereits</span><span class="sxs-lookup"><span data-stu-id="b178c-133">WSAEALREADY</span></span>       | <span data-ttu-id="b178c-134">Das angegebene Netzwerk wurde bereits dauerhaft in der angeforderten Weise gespeichert, und in *dwcontrolflags* wurden keine Flags angegeben, um ein Update für den vorhandenen Eintrag anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b178c-134">The specified network is already persistently stored in the requested manner, and no flags were specified in *dwControlFlags* to indicate an update to the existing entry.</span></span> |
| <span data-ttu-id="b178c-135">WSAEAFNOSUPPORT</span><span class="sxs-lookup"><span data-stu-id="b178c-135">WSAEAFNOSUPPORT</span></span>   | <span data-ttu-id="b178c-136">Es wurde eine Protokollfamilie angegeben, für die keine Unterstützung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b178c-136">A protocol family was specified for which there is no support.</span></span> <span data-ttu-id="b178c-137">In NLA werden nur IP-Protokoll Familien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b178c-137">Only IP protocol families are supported in NLA.</span></span>                                                             |
| <span data-ttu-id="b178c-138">Wsaepf NoSupport</span><span class="sxs-lookup"><span data-stu-id="b178c-138">WSAEPFNOSUPPORT</span></span>   | <span data-ttu-id="b178c-139">Es wurde ein Protokoll angegeben, für das keine Unterstützung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b178c-139">A protocol was specified for which there is no support.</span></span> <span data-ttu-id="b178c-140">In NLA wird nur das IP-Protokoll unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b178c-140">Only IP protocol is supported in NLA.</span></span>                                                                              |



 

 

 



