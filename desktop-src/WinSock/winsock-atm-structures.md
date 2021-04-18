---
description: Die folgende Liste enthält präzise Beschreibungen der einzelnen Winsock-ATM-Strukturen. Wenn Sie weitere Informationen zu einer Struktur haben, klicken Sie auf den Struktur Namen.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Winsock ATM-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf28266de89e5346727a9ad42fdb90d9167bc9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345806"
---
# <a name="winsock-atm-structures"></a><span data-ttu-id="cd6f0-104">Winsock ATM-Strukturen</span><span class="sxs-lookup"><span data-stu-id="cd6f0-104">Winsock ATM Structures</span></span>

<span data-ttu-id="cd6f0-105">Die folgende Liste enthält präzise Beschreibungen der einzelnen Winsock-ATM-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="cd6f0-105">The following list provides concise descriptions of each Winsock ATM structure.</span></span> <span data-ttu-id="cd6f0-106">Wenn Sie weitere Informationen zu einer Struktur haben, klicken Sie auf den Struktur Namen.</span><span class="sxs-lookup"><span data-stu-id="cd6f0-106">For additional information on any structure, click the structure name.</span></span>



| <span data-ttu-id="cd6f0-107">ATM-Struktur</span><span class="sxs-lookup"><span data-stu-id="cd6f0-107">ATM Structure</span></span>                           | <span data-ttu-id="cd6f0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd6f0-108">Description</span></span>                                                |
|-----------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="cd6f0-109">**ATM- \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="cd6f0-109">**ATM\_ADDRESS**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | <span data-ttu-id="cd6f0-110">Speichert ATM-Adressdaten für ATM-basierte Sockets.</span><span class="sxs-lookup"><span data-stu-id="cd6f0-110">Stores ATM address data for ATM-based sockets.</span></span>             |
| [<span data-ttu-id="cd6f0-111">**ATM- \_ bhli**</span><span class="sxs-lookup"><span data-stu-id="cd6f0-111">**ATM\_BHLI**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | <span data-ttu-id="cd6f0-112">Identifiziert B-HLI-Informationen für einen zugeordneten ATM-Socket.</span><span class="sxs-lookup"><span data-stu-id="cd6f0-112">Identifies B-HLI information for an associated ATM socket.</span></span> |
| [<span data-ttu-id="cd6f0-113">**ATM \_ blli**</span><span class="sxs-lookup"><span data-stu-id="cd6f0-113">**ATM\_BLLI**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | <span data-ttu-id="cd6f0-114">Identifiziert B-lli-Informationen für einen zugeordneten ATM-Socket.</span><span class="sxs-lookup"><span data-stu-id="cd6f0-114">Identifies B-LLI information for an associated ATM socket.</span></span> |
| [<span data-ttu-id="cd6f0-115">**sockaddr \_ ATM**</span><span class="sxs-lookup"><span data-stu-id="cd6f0-115">**sockaddr\_atm**</span></span>](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | <span data-ttu-id="cd6f0-116">Speichert socketadressinformationen für ATM-Sockets.</span><span class="sxs-lookup"><span data-stu-id="cd6f0-116">Stores socket address information for ATM sockets.</span></span>         |



 

<span data-ttu-id="cd6f0-117">Verwenden Sie für systemeigene ATM \_ -Dienste den AF-ATM für die Adressfamilie und die [**sockaddr \_ ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) -socketadressstruktur.</span><span class="sxs-lookup"><span data-stu-id="cd6f0-117">For native ATM services, use AF\_ATM for address family and the [**sockaddr\_atm**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) socket address structure.</span></span> <span data-ttu-id="cd6f0-118">Um einen systemeigenen ATM-Socket zu öffnen, übergeben Sie AF \_ ATM, sock \_ RAW und atmproto \_ AAL5 bzw. atmproto \_ aaluser an die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) .</span><span class="sxs-lookup"><span data-stu-id="cd6f0-118">To open a native ATM socket, pass AF\_ATM, SOCK\_RAW, and ATMPROTO\_AAL5 or ATMPROTO\_AALUSER into the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function, respectively.</span></span>

 

 



