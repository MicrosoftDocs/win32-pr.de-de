---
title: Grundlegendes zu mprinfo-Funktionen und Informations Headern
description: Die folgenden Funktionen erfordern, dass der Aufrufer eine Informationsstruktur oder einen Header als einen der Parameter übergibt.
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947779"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a><span data-ttu-id="9d159-103">Grundlegendes zu mprinfo-Funktionen und Informations Headern</span><span class="sxs-lookup"><span data-stu-id="9d159-103">Understanding MprInfo Functions and Information Headers</span></span>

<span data-ttu-id="9d159-104">Die folgenden Funktionen erfordern, dass der Aufrufer eine Informationsstruktur oder einen *Header* als einen der Parameter übergibt.</span><span class="sxs-lookup"><span data-stu-id="9d159-104">The following functions require that the caller pass an information structure or *header* as one of the parameters.</span></span>



| <span data-ttu-id="9d159-105">Verwaltungsfunktion</span><span class="sxs-lookup"><span data-stu-id="9d159-105">Administration function</span></span>                                                        | <span data-ttu-id="9d159-106">Konfigurationsfunktion</span><span class="sxs-lookup"><span data-stu-id="9d159-106">Configuration function</span></span>                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9d159-107">Keine Verwaltungsfunktion</span><span class="sxs-lookup"><span data-stu-id="9d159-107">No administration function</span></span>                                                     | [<span data-ttu-id="9d159-108">**Mprconfigtransportcreate**</span><span class="sxs-lookup"><span data-stu-id="9d159-108">**MprConfigTransportCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [<span data-ttu-id="9d159-109">**Mpradmintransporteintinfo**</span><span class="sxs-lookup"><span data-stu-id="9d159-109">**MprAdminTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [<span data-ttu-id="9d159-110">**Mprconfigtransporteintinfo**</span><span class="sxs-lookup"><span data-stu-id="9d159-110">**MprConfigTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [<span data-ttu-id="9d159-111">**Mpradmininterfacetransportabfo**</span><span class="sxs-lookup"><span data-stu-id="9d159-111">**MprAdminInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [<span data-ttu-id="9d159-112">**Mprconfiginterfacetransportantinfo**</span><span class="sxs-lookup"><span data-stu-id="9d159-112">**MprConfigInterfaceTransportSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [<span data-ttu-id="9d159-113">**Mpradmininterfacetransportadd**</span><span class="sxs-lookup"><span data-stu-id="9d159-113">**MprAdminInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [<span data-ttu-id="9d159-114">**Mprconfiginterfacetransportadd**</span><span class="sxs-lookup"><span data-stu-id="9d159-114">**MprConfigInterfaceTransportAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

<span data-ttu-id="9d159-115">Ebenso geben die folgenden Funktionen Informations Header zurück.</span><span class="sxs-lookup"><span data-stu-id="9d159-115">Similarly, the following functions return information headers.</span></span>



| <span data-ttu-id="9d159-116">Verwaltungsfunktion</span><span class="sxs-lookup"><span data-stu-id="9d159-116">Administration function</span></span>                                                        | <span data-ttu-id="9d159-117">Konfigurationsfunktion</span><span class="sxs-lookup"><span data-stu-id="9d159-117">Configuration function</span></span>                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="9d159-118">**Mpradmintransportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="9d159-118">**MprAdminTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [<span data-ttu-id="9d159-119">**Mprconfigtransportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="9d159-119">**MprConfigTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [<span data-ttu-id="9d159-120">**Mpradmininterfacetransportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="9d159-120">**MprAdminInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [<span data-ttu-id="9d159-121">**Mprconfiginterfacetransportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="9d159-121">**MprConfigInterfaceTransportGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

<span data-ttu-id="9d159-122">Für die Transportfunktionen enthält der Informations Header globale Informationen für den Transport.</span><span class="sxs-lookup"><span data-stu-id="9d159-122">For the transport functions, the information header contains global information for the transport.</span></span> <span data-ttu-id="9d159-123">Der-Header enthält für die Client Funktionen (interfacetransport) spezifische Informationen für den Client (z. b. OSPF), der verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="9d159-123">For the client (InterfaceTransport) functions, the header contains information specific to the client (for example, OSPF) being administered.</span></span>

<span data-ttu-id="9d159-124">Die Informations Header und ihre Inhalte sollten nur mithilfe der [mprinfo](router-information-functions.md) -Funktionen bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9d159-124">The information headers and their contents should be manipulated only by using the [MprInfo](router-information-functions.md) functions.</span></span> <span data-ttu-id="9d159-125">Entwickler sollten nicht versuchen, den Inhalt der Informations Header direkt zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9d159-125">Developers should not attempt to manipulate the contents of the information headers directly.</span></span>

<span data-ttu-id="9d159-126">Die reinen Schnittstellen Funktionen, wie z. b. [**mpradmininterfakesetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) , erfordern nicht die Verwendung von mprinfo-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="9d159-126">The interface-only functions such as [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) do not require the use of MprInfo functions.</span></span> <span data-ttu-id="9d159-127">Die Informationen, die mit diesen Funktionen übermittelt und zurückgegeben werden, sind immer in Form einer [**MPR- \_ Schnittstellen**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) Struktur.</span><span class="sxs-lookup"><span data-stu-id="9d159-127">The information that is passed and returned with these functions is always in the form of an [**MPR\_INTERFACE**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) structure.</span></span>

 

 




