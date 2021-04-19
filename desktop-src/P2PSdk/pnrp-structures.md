---
description: 'Die PNRP-Namespace Anbieter-API verwendet die folgenden Strukturen:'
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: PNRP-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e2ee85f3673395ade31417c79c010354f16b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362474"
---
# <a name="pnrp-structures"></a><span data-ttu-id="ffb60-103">PNRP-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ffb60-103">PNRP Structures</span></span>

<span data-ttu-id="ffb60-104">Die PNRP-Namespace Anbieter-API verwendet die folgenden Strukturen:</span><span class="sxs-lookup"><span data-stu-id="ffb60-104">The PNRP Namespace Provider API uses the following structures:</span></span>



| <span data-ttu-id="ffb60-105">Struktur</span><span class="sxs-lookup"><span data-stu-id="ffb60-105">Structure</span></span>                                                             | <span data-ttu-id="ffb60-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ffb60-106">Description</span></span>                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ffb60-107">**Peer- \_ PNRP- \_ Endpunkt \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="ffb60-107">**PEER\_PNRP\_ENDPOINT\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | <span data-ttu-id="ffb60-108">Enthält die IP-Adressen und Daten, die einem Peer Endpunkt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ffb60-108">Contains the IP addresses and data associated with a peer endpoint.</span></span>                                                                                                 |
| [<span data-ttu-id="ffb60-109">**Peer- \_ PNRP- \_ \_ cloudinformationen**</span><span class="sxs-lookup"><span data-stu-id="ffb60-109">**PEER\_PNRP\_CLOUD\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | <span data-ttu-id="ffb60-110">Enthält Informationen zu einer PNRP-Cloud (Peer Name Resolution Protocol).</span><span class="sxs-lookup"><span data-stu-id="ffb60-110">Contains information about a Peer Name Resolution Protocol (PNRP) cloud.</span></span>                                                                                            |
| [<span data-ttu-id="ffb60-111">**Peer- \_ PNRP- \_ Registrierungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="ffb60-111">**PEER\_PNRP\_REGISTRATION\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | <span data-ttu-id="ffb60-112">Enthält die Informationen, die von einer Peer Identität bereitgestellt werden, wenn Sie bei einer PNRP-Cloud registriert wird.</span><span class="sxs-lookup"><span data-stu-id="ffb60-112">Contains the information provided by a peer identity when it registers with a PNRP cloud.</span></span>                                                                           |
| [<span data-ttu-id="ffb60-113">PNRP und BLOB</span><span class="sxs-lookup"><span data-stu-id="ffb60-113">PNRP and BLOB</span></span>](pnrp-and-blob.md)                                    | <span data-ttu-id="ffb60-114">Übergibt während Aufrufen mehrerer Funktionen Daten an die [**wsaqueryset**](winsock-nsp-reference-links.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ffb60-114">Passes data to the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure during calls to several functions.</span></span>                                                  |
| [<span data-ttu-id="ffb60-115">PNRP und wsaqueryset</span><span class="sxs-lookup"><span data-stu-id="ffb60-115">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)                      | <span data-ttu-id="ffb60-116">Ermöglicht das Auflösen von Namen und die Enumeration von Namen und Clouds.</span><span class="sxs-lookup"><span data-stu-id="ffb60-116">Facilitates the resolving of names and the enumeration of names and clouds.</span></span>                                                                                         |
| [<span data-ttu-id="ffb60-117">**PNRP- \_ Cloud- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="ffb60-117">**PNRP\_CLOUD\_ID**</span></span>](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | <span data-ttu-id="ffb60-118">Enthält die Werte, die eine netzwerkcloud definieren.</span><span class="sxs-lookup"><span data-stu-id="ffb60-118">Contains the values that define a network cloud.</span></span>                                                                                                                    |
| [<span data-ttu-id="ffb60-119">**Pnrpcloudinfo**</span><span class="sxs-lookup"><span data-stu-id="ffb60-119">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | <span data-ttu-id="ffb60-120">Auf den **lpblob** -Member der [**wsaqueryset**](winsock-nsp-reference-links.md) -Struktur verweist.</span><span class="sxs-lookup"><span data-stu-id="ffb60-120">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure.</span></span>                                                            |
| [<span data-ttu-id="ffb60-121">**Pnrpinfo \_ v1**</span><span class="sxs-lookup"><span data-stu-id="ffb60-121">**PNRPINFO\_V1**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | <span data-ttu-id="ffb60-122">Verweis auf den **lpblob** -Member der [**wsaqueryset**](winsock-nsp-reference-links.md) -Struktur</span><span class="sxs-lookup"><span data-stu-id="ffb60-122">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure</span></span>                                                             |
| <span data-ttu-id="ffb60-123">[**Pnrpinfo \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ffb60-123">[**PNRPINFO\_V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))</span></span>                                   | <span data-ttu-id="ffb60-124">Verweist auf das **lpblob** -Member der [**wsaqueryset**](winsock-nsp-reference-links.md) -Struktur und bietet Unterstützung für anwendungsspezifische, nicht transparente Daten.</span><span class="sxs-lookup"><span data-stu-id="ffb60-124">Pointed to by the **lpBlob** member of the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure, and provides support for application-specific opaque data.</span></span> |



 

 

 
