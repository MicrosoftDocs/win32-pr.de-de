---
description: Der Protokoll Parameter in Socket und wsasocket ist ein Bezeichner, der einen Netzwerktyp und eine Methode zum Identifizieren der verschiedenen Transportprotokolle festlegt, die im Netzwerk ausgeführt werden.
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: IPX-Familie von Protokoll bezeichlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fc808a04f1cf10bb099cd7d923bf471e9bd8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129165"
---
# <a name="ipx-family-of-protocol-identifiers"></a><span data-ttu-id="60ae4-103">IPX-Familie von Protokoll bezeichlern</span><span class="sxs-lookup"><span data-stu-id="60ae4-103">IPX Family of Protocol Identifiers</span></span>

<span data-ttu-id="60ae4-104">Der *Protokoll* Parameter in [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) und [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) ist ein Bezeichner, der einen Netzwerktyp und eine Methode zum Identifizieren der verschiedenen Transportprotokolle festlegt, die im Netzwerk ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="60ae4-104">The *protocol* parameter in [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) and [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) is an identifier that establishes a network type and a method for identifying the various transport protocols that run on the network.</span></span> <span data-ttu-id="60ae4-105">Anders als bei IP verwendet IPX keinen einzelnen Protokoll Wert für die Auswahl eines Transport Stapels.</span><span class="sxs-lookup"><span data-stu-id="60ae4-105">Unlike IP, IPX does not use a single protocol value for selecting a transport stack.</span></span> <span data-ttu-id="60ae4-106">Da es keine Netzwerk Anforderung gibt, einen bestimmten Wert für jedes Transportprotokoll zu verwenden, können wir diese auf eine Weise zuweisen, die für Winsock-Anwendungen geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="60ae4-106">Since there is no network requirement to use a specific value for each transport protocol, we are free to assign them in a manner convenient for Winsock applications.</span></span> <span data-ttu-id="60ae4-107">Wir vermeiden Werte 0 – 255, um Konflikte mit den entsprechenden PF- \_ inet-Protokoll Werten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="60ae4-107">We avoid values 0–255 in order to avoid collisions with the corresponding PF\_INET protocol values.</span></span>



| <span data-ttu-id="60ae4-108">Name</span><span class="sxs-lookup"><span data-stu-id="60ae4-108">Name</span></span>         | <span data-ttu-id="60ae4-109">Wert</span><span class="sxs-lookup"><span data-stu-id="60ae4-109">Value</span></span>       | <span data-ttu-id="60ae4-110">Sockettypen</span><span class="sxs-lookup"><span data-stu-id="60ae4-110">Socket types</span></span>              | <span data-ttu-id="60ae4-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60ae4-111">Description</span></span>                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| <span data-ttu-id="60ae4-112">Reserviert</span><span class="sxs-lookup"><span data-stu-id="60ae4-112">Reserved</span></span>     | <span data-ttu-id="60ae4-113">0 - 255</span><span class="sxs-lookup"><span data-stu-id="60ae4-113">0-255</span></span>       |                           | <span data-ttu-id="60ae4-114">Reserviert für PF- \_ inet-Protokoll Werte.</span><span class="sxs-lookup"><span data-stu-id="60ae4-114">Reserved for PF\_INET protocol values.</span></span>              |
| <span data-ttu-id="60ae4-115">nsproto- \_ IPX</span><span class="sxs-lookup"><span data-stu-id="60ae4-115">NSPROTO\_IPX</span></span> | <span data-ttu-id="60ae4-116">1000-1255</span><span class="sxs-lookup"><span data-stu-id="60ae4-116">1000 - 1255</span></span> | <span data-ttu-id="60ae4-117">sock- \_ dgram Sock- \_ Rohdaten</span><span class="sxs-lookup"><span data-stu-id="60ae4-117">SOCK\_DGRAM SOCK\_RAW</span></span>     | <span data-ttu-id="60ae4-118">Datagramm-Dienst für IPX.</span><span class="sxs-lookup"><span data-stu-id="60ae4-118">Datagram service for IPX.</span></span>                           |
| <span data-ttu-id="60ae4-119">nsproto- \_ SPX</span><span class="sxs-lookup"><span data-stu-id="60ae4-119">NSPROTO\_SPX</span></span> | <span data-ttu-id="60ae4-120">1256</span><span class="sxs-lookup"><span data-stu-id="60ae4-120">1256</span></span>        | <span data-ttu-id="60ae4-121">sock-Datenstrom (sock) \_ \_</span><span class="sxs-lookup"><span data-stu-id="60ae4-121">SOCK\_STREAM SOCK\_SEQPKT</span></span> | <span data-ttu-id="60ae4-122">Zuverlässiger Paket Austausch mithilfe von Paketen mit fester Größe.</span><span class="sxs-lookup"><span data-stu-id="60ae4-122">Reliable packet exchange using fixed-sized packets.</span></span> |



 

> [!Note]  
> <span data-ttu-id="60ae4-123">Wenn nsproto \_ SPX angegeben ist, wird das SPX II-Protokoll automatisch verwendet, wenn beide Endpunkte dies tun können.</span><span class="sxs-lookup"><span data-stu-id="60ae4-123">When NSPROTO\_SPX is specified, the SPX II protocol is automatically utilized if both endpoints are capable of doing so.</span></span>

 

 

 



