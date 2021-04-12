---
description: Die folgende Liste enthält die cmspcallbase-Member.
ms.assetid: a3193639-e0c4-4851-a879-551eca8023f9
title: Cmspcallbase-Member
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ddae67d85a64a5a443727b3950054957c7f24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216184"
---
# <a name="cmspcallbase-members"></a><span data-ttu-id="6e91f-103">Cmspcallbase-Member</span><span class="sxs-lookup"><span data-stu-id="6e91f-103">CMSPCallBase Members</span></span>



| <span data-ttu-id="6e91f-104">Memberart</span><span class="sxs-lookup"><span data-stu-id="6e91f-104">Member type</span></span>                   | <span data-ttu-id="6e91f-105">Name</span><span class="sxs-lookup"><span data-stu-id="6e91f-105">Name</span></span>             | <span data-ttu-id="6e91f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e91f-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e91f-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="6e91f-107">IUnknown</span></span>                      | <span data-ttu-id="6e91f-108">\*Mio. \_ pftm</span><span class="sxs-lookup"><span data-stu-id="6e91f-108">\*m\_pFTM</span></span>        | <span data-ttu-id="6e91f-109">Zeiger auf den Free Threaded Marshaller.</span><span class="sxs-lookup"><span data-stu-id="6e91f-109">Pointer to the free threaded marshaller.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="6e91f-110">Cmspaddress\*</span><span class="sxs-lookup"><span data-stu-id="6e91f-110">CMSPAddress\*</span></span>                 | <span data-ttu-id="6e91f-111">\*m \_ pmspaddress</span><span class="sxs-lookup"><span data-stu-id="6e91f-111">\*m\_pMSPAddress</span></span> | <span data-ttu-id="6e91f-112">Der Zeiger auf das MSP-Adress Objekt.</span><span class="sxs-lookup"><span data-stu-id="6e91f-112">The pointer to the MSP address object.</span></span> <span data-ttu-id="6e91f-113">Sie wird verwendet, um die Standard Terminals zu erhalten, wenn die Anwendung keine Auswahl spielt.</span><span class="sxs-lookup"><span data-stu-id="6e91f-113">It is used to get the default terminals if the application doesn't select any.</span></span> <span data-ttu-id="6e91f-114">Außerdem enthält es eine refcount (über [**mspaddressaddressf**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), nicht adressf), sodass die aggregierte Adresse nicht entfernt wird, während der Aufruf noch aktiv ist, aber die Adresse von TAPI 3 nicht adressiert wird.</span><span class="sxs-lookup"><span data-stu-id="6e91f-114">It also carries a refcount (via [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), not AddRef) so that the aggregated address will not go away while the call is still alive, but TAPI 3's address is not AddRef'ed.</span></span> |
| <span data-ttu-id="6e91f-115">MSP- \_ handle</span><span class="sxs-lookup"><span data-stu-id="6e91f-115">MSP\_HANDLE</span></span>                   | <span data-ttu-id="6e91f-116">\*m- \_ HT-Rückruf</span><span class="sxs-lookup"><span data-stu-id="6e91f-116">\*m\_htCall</span></span>      | <span data-ttu-id="6e91f-117">Das Handle für den TAPI3's-Befehl.</span><span class="sxs-lookup"><span data-stu-id="6e91f-117">The handle to TAPI3's call.</span></span> <span data-ttu-id="6e91f-118">Wird zum Auslösen von Ereignis Ereignissen verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e91f-118">Used to fire call events.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="6e91f-119">DWORD</span><span class="sxs-lookup"><span data-stu-id="6e91f-119">DWORD</span></span>                         | <span data-ttu-id="6e91f-120">Mio. \_ dwmediatype</span><span class="sxs-lookup"><span data-stu-id="6e91f-120">m\_dwMediaType</span></span>   | <span data-ttu-id="6e91f-121">Die Bitmaske der Medientypen bei diesem-Befehl.</span><span class="sxs-lookup"><span data-stu-id="6e91f-121">Bitmask of the media types on this call.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="6e91f-122">Cmsparray <itstream \*></span><span class="sxs-lookup"><span data-stu-id="6e91f-122">CMSPArray <ITStream \*></span></span> | <span data-ttu-id="6e91f-123">m- \_ Streams</span><span class="sxs-lookup"><span data-stu-id="6e91f-123">m\_Streams</span></span>       | <span data-ttu-id="6e91f-124">Die Liste der Streamobjekte im-Befehl.</span><span class="sxs-lookup"><span data-stu-id="6e91f-124">The list of stream objects in the call.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="6e91f-125">Cmspcritsection</span><span class="sxs-lookup"><span data-stu-id="6e91f-125">CMSPCritSection</span></span>               | <span data-ttu-id="6e91f-126">m- \_ Sperre</span><span class="sxs-lookup"><span data-stu-id="6e91f-126">m\_lock</span></span>          | <span data-ttu-id="6e91f-127">Die Sperre, mit der die Datenstrom Listen geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="6e91f-127">The lock that protects the stream lists.</span></span>                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="6e91f-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e91f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e91f-129">**Cmspcallbase**</span><span class="sxs-lookup"><span data-stu-id="6e91f-129">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 



