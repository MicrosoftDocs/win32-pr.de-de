---
description: Nspgetserviceclassinfo
ms.assetid: 6fbe9c0c-ac1f-4f2b-a542-eae2195b1335
title: Hilfsfunktionen in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e687529bf1ede1598225708cf288e49bb7e9b5c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345062"
---
# <a name="helper-functions-in-the-spi"></a><span data-ttu-id="3d1dc-103">Hilfsfunktionen in der SPI</span><span class="sxs-lookup"><span data-stu-id="3d1dc-103">Helper Functions in the SPI</span></span>

-   [<span data-ttu-id="3d1dc-104">**Nspgetserviceclassinfo**</span><span class="sxs-lookup"><span data-stu-id="3d1dc-104">**NSPGetServiceClassInfo**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

<span data-ttu-id="3d1dc-105">Die [**nspgetserviceclassinfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) -Funktion ruft Schema Informationen der Dienstklasse ab, die von einem Namespace Anbieter beibehalten wurden.</span><span class="sxs-lookup"><span data-stu-id="3d1dc-105">The [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) function retrieves service class schema information that has been retained by a namespace provider.</span></span> <span data-ttu-id="3d1dc-106">Sie wird auch von der Windows Sockets 2-dll in der Implementierung von [**wsagetserviceclassnamebyclassid**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)verwendet.</span><span class="sxs-lookup"><span data-stu-id="3d1dc-106">It is also used by the Windows Sockets 2 DLL in its implementation of [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).</span></span>

<span data-ttu-id="3d1dc-107">Die folgenden Makros, die in der Header Datei " *svcguid. h* " definiert sind, können bei der Zuordnung von bekannten Dienst Klassen und diesen Namespaces helfen.</span><span class="sxs-lookup"><span data-stu-id="3d1dc-107">The following macros defined in the *Svcguid.h* header file and can aid in mapping between well known service classes and these namespaces.</span></span>

| <span data-ttu-id="3d1dc-108">Makroname</span><span class="sxs-lookup"><span data-stu-id="3d1dc-108">Macro name</span></span>                                                                              | <span data-ttu-id="3d1dc-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d1dc-109">Description</span></span>                                                                                                                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1dc-110">**Svcid \_ TCP (Port)**</span><span class="sxs-lookup"><span data-stu-id="3d1dc-110">**SVCID\_TCP(Port)**</span></span><br/> <span data-ttu-id="3d1dc-111">**Svcid \_ UDP (Port)**</span><span class="sxs-lookup"><span data-stu-id="3d1dc-111">**SVCID\_UDP(Port)**</span></span><br/>                         | <span data-ttu-id="3d1dc-112">Bei einem TCP-oder UDP-Port für das Internet Protokoll wird die GUID zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3d1dc-112">Given a TCP or UDP port for the Internet protocol, returns the GUID.</span></span>                                                                               |
| <span data-ttu-id="3d1dc-113">**ist \_ svcid \_ TCP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="3d1dc-113">**IS\_SVCID\_TCP(GUID)**</span></span><br/> <span data-ttu-id="3d1dc-114">**ist \_ svcid \_ UDP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="3d1dc-114">**IS\_SVCID\_UDP(GUID)**</span></span><br/>                 | <span data-ttu-id="3d1dc-115">Gibt **true** zurück, wenn die GUID für TCP oder UDP innerhalb des zulässigen Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="3d1dc-115">Returns **TRUE** if the GUID for TCP or UDP is within the allowable range.</span></span>                                                                         |
| <span data-ttu-id="3d1dc-116">**Port \_ von \_ svcid \_ TCP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="3d1dc-116">**PORT\_FROM\_SVCID\_TCP(GUID)**</span></span><br/> <span data-ttu-id="3d1dc-117">**Port \_ von \_ svcid \_ UDP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="3d1dc-117">**PORT\_FROM\_SVCID\_UDP(GUID)**</span></span><br/> | <span data-ttu-id="3d1dc-118">Gibt den TCP-oder UDP-Port zurück, der der GUID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3d1dc-118">Returns the TCP or UDP port associated with the GUID.</span></span>                                                                                              |
| <span data-ttu-id="3d1dc-119">**svcid \_ NetWare (SAPID)**</span><span class="sxs-lookup"><span data-stu-id="3d1dc-119">**SVCID\_NETWARE(SAPID)**</span></span><br/>                                                    | <span data-ttu-id="3d1dc-120">Gibt die GUID zurück, wenn der Dienst Ankündigungs Protokoll (SAP)-Bezeichner angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="3d1dc-120">Given the Service Advertising Protocol (SAP) identifier, returns the GUID.</span></span> <span data-ttu-id="3d1dc-121">Dieses Makro wird mit dem SAP-Namespace in einer NetWare-Umgebung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3d1dc-121">This macro is used with the SAP namespace within a NetWare environment.</span></span> |
| <span data-ttu-id="3d1dc-122">**SAPID \_ von \_ svcid \_ NetWare (GUID)**</span><span class="sxs-lookup"><span data-stu-id="3d1dc-122">**SAPID\_FROM\_SVCID\_NETWARE(GUID)**</span></span><br/>                                        | <span data-ttu-id="3d1dc-123">Gibt den NetWare-SAP-Bezeichner zurück, der der GUID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3d1dc-123">Returns the NetWare SAP identifier associated with the GUID.</span></span> <span data-ttu-id="3d1dc-124">Dieses Makro wird mit dem SAP-Namespace in einer NetWare-Umgebung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3d1dc-124">This macro is used with the SAP namespace within a NetWare environment.</span></span>               |
| <span data-ttu-id="3d1dc-125">**ist \_ svcid \_ NetWare (GUID)**</span><span class="sxs-lookup"><span data-stu-id="3d1dc-125">**IS\_SVCID\_NETWARE(GUID)**</span></span><br/>                                                 | <span data-ttu-id="3d1dc-126">Gibt **true** zurück, wenn die GUID für NetWare innerhalb des zulässigen Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="3d1dc-126">Returns **TRUE** if the GUID for NetWare is within the allowable range.</span></span> <span data-ttu-id="3d1dc-127">Dieses Makro wird mit dem SAP-Namespace in einer NetWare-Umgebung verwendet.</span><span class="sxs-lookup"><span data-stu-id="3d1dc-127">This macro is used with the SAP namespace within a NetWare environment.</span></span>    |



 

> [!Note]  
> <span data-ttu-id="3d1dc-128">Die Header Datei " *svcguid. h* " ist nicht automatisch in der Header Datei " *Winsock2. h* " enthalten.</span><span class="sxs-lookup"><span data-stu-id="3d1dc-128">The *Svcguid.h* header file is not automatically included by the *Winsock2.h* header file.</span></span>

 

 

 




