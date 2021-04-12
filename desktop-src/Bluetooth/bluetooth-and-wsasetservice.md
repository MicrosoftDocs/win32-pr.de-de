---
title: Bluetooth und wsasetservice
description: Bluetooth verwendet die wsasetservice-Funktion, um eine Dienst Instanz im Bluetooth-Namespace (NS \_ BTH) aus der Registrierung zu registrieren oder zu entfernen.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- Wsasetservice Bluetooth
- Bluetooth und wsasetservice Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473245"
---
# <a name="bluetooth-and-wsasetservice"></a><span data-ttu-id="90d59-106">Bluetooth und wsasetservice</span><span class="sxs-lookup"><span data-stu-id="90d59-106">Bluetooth and WSASetService</span></span>

<span data-ttu-id="90d59-107">Bluetooth verwendet die [**wsasetservice**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) -Funktion, um eine Dienst Instanz im Bluetooth-Namespace (NS \_ BTH) aus der Registrierung zu registrieren oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="90d59-107">Bluetooth uses the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function to register or remove a service instance within the Bluetooth namespace (NS\_BTH) from the registry.</span></span> <span data-ttu-id="90d59-108">Das Handle, das von diesem Vorgang zurückgegeben wird, kann nur verwendet werden, um den Dienst zu löschen.</span><span class="sxs-lookup"><span data-stu-id="90d59-108">The handle returned by this operation may only be used to delete the service.</span></span>

<span data-ttu-id="90d59-109">Bluetooth bietet zwei Möglichkeiten, Dienste mithilfe der [**wsasetservice**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) -Funktion zu bewerben:</span><span class="sxs-lookup"><span data-stu-id="90d59-109">Bluetooth has two means of advertising services using the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function:</span></span>

-   <span data-ttu-id="90d59-110">Die Anwendung kann das System einen einfachen Bluetooth-SDP-Dienst Eintrag ankündigen, der aus Standard Mitgliedern in der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="90d59-110">The application can have the system advertise a simple Bluetooth SDP service record, constructed from standard members in the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span>
-   <span data-ttu-id="90d59-111">Die Anwendung kann das System einen eigenen Bluetooth-SDP-Datensatz ankündigen, indem er eine [**BTH- \_ Set- \_ Service**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) -Struktur im **lpblob** -Member der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur übergibt.</span><span class="sxs-lookup"><span data-stu-id="90d59-111">The application can have the system advertise their own Bluetooth SDP record by passing a [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure in the **lpBlob** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span> <span data-ttu-id="90d59-112">Dies ist ein komplexerer Ansatz.</span><span class="sxs-lookup"><span data-stu-id="90d59-112">This is a more complex approach.</span></span>

> [!Note]  
> <span data-ttu-id="90d59-113">SDP-Datensätze, die von [**wsasetservice**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) angekündigt werden, werden nicht beibehalten, nachdem der von Ihnen veröffentlichte Prozess beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="90d59-113">SDP records advertised by [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) do not persist after the process that published them has quit.</span></span>

 

<span data-ttu-id="90d59-114">Die Verwendung von [**wsasetservice**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) mit Bluetooth hat die folgenden Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="90d59-114">Use of [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="90d59-115">Der *lpqsreginfo* -Parameter ist die Adresse der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur, die registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="90d59-115">The *lpqsRegInfo* parameter is the address of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure to be registered.</span></span>
-   <span data-ttu-id="90d59-116">Der *ESS Operation* -Parameter ist eine Enumeration, die einen der in der folgenden Tabelle gezeigten Vorgänge enthält.</span><span class="sxs-lookup"><span data-stu-id="90d59-116">The *essOperation* parameter is an enumeration that contains one of the operations shown in the following table.</span></span>



| <span data-ttu-id="90d59-117">Wert</span><span class="sxs-lookup"><span data-stu-id="90d59-117">Value</span></span>                  | <span data-ttu-id="90d59-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90d59-118">Description</span></span>                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="90d59-119">rnrservice- \_ Registrierung</span><span class="sxs-lookup"><span data-stu-id="90d59-119">RNRSERVICE\_REGISTER</span></span>   | <span data-ttu-id="90d59-120">Startet die Ankündigung des dienstanterdienstanbieter mit dem Bluetooth-SDP-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="90d59-120">Starts advertising the service to remote radios querying using the Bluetooth SDP protocol.</span></span> |
| <span data-ttu-id="90d59-121">rnrservice \_ -Registrierung</span><span class="sxs-lookup"><span data-stu-id="90d59-121">RNRSERVICE\_DEREGISTER</span></span> | <span data-ttu-id="90d59-122">Ungültig.</span><span class="sxs-lookup"><span data-stu-id="90d59-122">Not valid.</span></span> <span data-ttu-id="90d59-123">Gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="90d59-123">Returns an error.</span></span>                                                               |
| <span data-ttu-id="90d59-124">rnrservice \_ Löschen</span><span class="sxs-lookup"><span data-stu-id="90d59-124">RNRSERVICE\_DELETE</span></span>     | <span data-ttu-id="90d59-125">Beendet die Ankündigung des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="90d59-125">Stops advertising the service.</span></span>                                                             |



 

> [!Note]  
> <span data-ttu-id="90d59-126">Dienst Handles, die während eines [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -oder [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Aufrufes erkannt werden, sind mit dem Löschvorgang rnrservice nicht kompatibel \_ .</span><span class="sxs-lookup"><span data-stu-id="90d59-126">Service handles discovered during a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) or [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) call are incompatible with the RNRSERVICE\_DELETE operation.</span></span>

 

-   <span data-ttu-id="90d59-127">Der *dwcontrolflags* -Parameter ist reserviert und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="90d59-127">The *dwControlFlags* parameter is reserved, and must be zero.</span></span>

<span data-ttu-id="90d59-128">Weitere Informationen und eine Liste der Optionen für Bluetooth-Sockets finden Sie unter [Optionen für Bluetooth und Socket](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="90d59-128">For more information and a list of Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="90d59-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90d59-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90d59-130">Windows-Sockets</span><span class="sxs-lookup"><span data-stu-id="90d59-130">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 