---
description: Die TAPI-DLLs sind zusammen mit dem TAPI-Server (Tapisvr.exe) wichtige Abstraktionen, die Endbenutzer-oder Server Anwendungen von Dienstanbietern trennen. Eine TAPI-dll in Verbindung mit dem TAPI-Server stellt eine konsistente Schnittstelle zwischen diesen beiden Ebenen bereit.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: TAPI-dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482045ec16a999957121aff669e93b34b605069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563736"
---
# <a name="tapi-dll"></a><span data-ttu-id="5d485-104">TAPI-dll</span><span class="sxs-lookup"><span data-stu-id="5d485-104">TAPI DLL</span></span>

<span data-ttu-id="5d485-105">Die TAPI-DLLs sind zusammen mit dem TAPI-Server (Tapisvr.exe) wichtige Abstraktionen, die Endbenutzer-oder Server Anwendungen von Dienstanbietern trennen.</span><span class="sxs-lookup"><span data-stu-id="5d485-105">The TAPI DLLs, along with the TAPI Server (Tapisvr.exe), are crucial abstractions separating end-user or server applications from service providers.</span></span> <span data-ttu-id="5d485-106">Eine TAPI-dll in Verbindung mit dem TAPI-Server stellt eine konsistente Schnittstelle zwischen diesen beiden Ebenen bereit.</span><span class="sxs-lookup"><span data-stu-id="5d485-106">A TAPI DLL in conjunction with the TAPI Server provides a consistent interface between these two layers.</span></span>

<span data-ttu-id="5d485-107">Eine TAPI-Anwendung lädt die entsprechende dll in den Prozessbereich.</span><span class="sxs-lookup"><span data-stu-id="5d485-107">A TAPI application loads the appropriate DLL into its process space.</span></span> <span data-ttu-id="5d485-108">Während der Initialisierung richtet TAPI eine RPC-Verbindung mit Tapisvr.exe ein.</span><span class="sxs-lookup"><span data-stu-id="5d485-108">During initialization, TAPI establishes an RPC link with Tapisvr.exe.</span></span> <span data-ttu-id="5d485-109">Der TAPI-Server wird im Kontext von svchost ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d485-109">The TAPI Server runs in the context of SVCHOST.</span></span>

<span data-ttu-id="5d485-110">TAPI: Tapi.dll, Tapi32.dll und Tapi3.dll sind drei DLLs zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5d485-110">There are three DLLs associated with TAPI: Tapi.dll, Tapi32.dll, and Tapi3.dll.</span></span> <span data-ttu-id="5d485-111">Diese DLLs befinden sich im Verzeichnis% systemroot% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="5d485-111">These DLLs are located in %SystemRoot%\\system32.</span></span> <span data-ttu-id="5d485-112">In der folgenden Abbildung werden die Rollen ihrer jeweiligen Rollen in Microsoft-telefonietelefoniefunktionen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="5d485-112">The following figure illustrates the roles of their respective roles in Microsoft Telephony:</span></span>

![Rollen der drei TAPI-DLLs](images/dllserv.png)

<span data-ttu-id="5d485-114">Vorhandene 16-Bit-Anwendungen können mit Tapi.dll verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="5d485-114">Existing 16-bit applications link to Tapi.dll.</span></span> <span data-ttu-id="5d485-115">Tapi.dll ist einfach eine Thunk-Ebene, die 16-Bit-Adressen 32-Bit-Adressen zuordnet und Anforderungen an Tapi32.dll übergibt.</span><span class="sxs-lookup"><span data-stu-id="5d485-115">Tapi.dll is simply a thunk layer that maps 16-bit addresses to 32-bit addresses and pass requests to Tapi32.dll.</span></span>

<span data-ttu-id="5d485-116">Vorhandene 32-Bit-TAPI 2. x-Anwendungen können mit Tapi32.dll verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="5d485-116">Existing 32-bit TAPI 2.x applications link to Tapi32.dll.</span></span> <span data-ttu-id="5d485-117">Tapi32.dll ist eine schlanke Marshalling-Ebene, die Funktionsanforderungen an den TAPI-Server (tapisrv) überträgt und bei Bedarf die Medien Dienstanbieter-DLLs im Prozess der Anwendung lädt und aufruft.</span><span class="sxs-lookup"><span data-stu-id="5d485-117">Tapi32.dll is a thin marshalling layer that transfers function requests to the TAPI Server (TAPISRV) and, when needed, loads and invokes media service provider DLLs in the application's process.</span></span>

<span data-ttu-id="5d485-118">TAPI 3. x-Anwendungen können mit Tapi3.dll verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="5d485-118">TAPI 3.x applications link to Tapi3.dll.</span></span>

 

 



