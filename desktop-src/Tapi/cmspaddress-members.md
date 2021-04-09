---
description: In der folgenden Liste sind die CMSP-adressmember enthalten.
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: Cmspaddress-Member
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83213646427e7379b3eb2b45a0670f7908877175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869200"
---
# <a name="cmspaddress-members"></a><span data-ttu-id="e32b8-103">Cmspaddress-Member</span><span class="sxs-lookup"><span data-stu-id="e32b8-103">CMSPAddress Members</span></span>



| <span data-ttu-id="e32b8-104">Elementtypen</span><span class="sxs-lookup"><span data-stu-id="e32b8-104">Member types</span></span>                    | <span data-ttu-id="e32b8-105">Name</span><span class="sxs-lookup"><span data-stu-id="e32b8-105">Name</span></span>                    | <span data-ttu-id="e32b8-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e32b8-106">Description</span></span>                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e32b8-107">Iunknown</span><span class="sxs-lookup"><span data-stu-id="e32b8-107">Iunknown</span></span>                        | <span data-ttu-id="e32b8-108">\*Mio. \_ pftm</span><span class="sxs-lookup"><span data-stu-id="e32b8-108">\*m\_pFTM</span></span>               | <span data-ttu-id="e32b8-109">Zeiger auf den Free Threaded Marshaller.</span><span class="sxs-lookup"><span data-stu-id="e32b8-109">Pointer to the free threaded marshaller.</span></span>                                                         |
| <span data-ttu-id="e32b8-110">HANDLE</span><span class="sxs-lookup"><span data-stu-id="e32b8-110">HANDLE</span></span>                          | <span data-ttu-id="e32b8-111">m \_ htevent</span><span class="sxs-lookup"><span data-stu-id="e32b8-111">m\_htEvent</span></span>              | <span data-ttu-id="e32b8-112">Handle für Tapi3.dll-Ereignis, das verwendet wird, um TAPI darüber zu benachrichtigen, dass der MSP Daten an ihn senden möchte.</span><span class="sxs-lookup"><span data-stu-id="e32b8-112">Handle to Tapi3.dll's event, which is used to notify TAPI that the MSP wants to send data to it.</span></span> |
| <span data-ttu-id="e32b8-113">\_Eintrag auflisten</span><span class="sxs-lookup"><span data-stu-id="e32b8-113">LIST\_ENTRY</span></span>                     | <span data-ttu-id="e32b8-114">m \_ EventList</span><span class="sxs-lookup"><span data-stu-id="e32b8-114">m\_EventList</span></span>            | <span data-ttu-id="e32b8-115">Die Liste der Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="e32b8-115">List of events.</span></span>                                                                                  |
| <span data-ttu-id="e32b8-116">Cmspcritsection</span><span class="sxs-lookup"><span data-stu-id="e32b8-116">CMSPCritSection</span></span>                 | <span data-ttu-id="e32b8-117">m \_ eventdatalock</span><span class="sxs-lookup"><span data-stu-id="e32b8-117">m\_EventDataLock</span></span>        | <span data-ttu-id="e32b8-118">Die Sperre, die die Daten im Zusammenhang mit der Ereignis Behandlung mit TAPI schützt.</span><span class="sxs-lookup"><span data-stu-id="e32b8-118">The lock that protects the data related to event handling with TAPI.</span></span>                             |
| <span data-ttu-id="e32b8-119">Itterminalmanager</span><span class="sxs-lookup"><span data-stu-id="e32b8-119">ITTerminalManager</span></span>               | <span data-ttu-id="e32b8-120">\*m \_ pitterminalmanager</span><span class="sxs-lookup"><span data-stu-id="e32b8-120">\*m\_pITTerminalManager</span></span> | <span data-ttu-id="e32b8-121">Der Zeiger auf das Terminal-Manager-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e32b8-121">The pointer to the Terminal Manager object.</span></span>                                                      |
| <span data-ttu-id="e32b8-122">Cmsparray <itterminal \*></span><span class="sxs-lookup"><span data-stu-id="e32b8-122">CMSPArray <ITTerminal \*></span></span> | <span data-ttu-id="e32b8-123">m- \_ Terminals</span><span class="sxs-lookup"><span data-stu-id="e32b8-123">m\_Terminals</span></span>            | <span data-ttu-id="e32b8-124">Die Liste der statischen Terminals, die für die Adresse verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e32b8-124">The list of static terminals that can be used on the address.</span></span>                                    |
| <span data-ttu-id="e32b8-125">BOOL</span><span class="sxs-lookup"><span data-stu-id="e32b8-125">BOOL</span></span>                            | <span data-ttu-id="e32b8-126">m- \_ terminalsuptag</span><span class="sxs-lookup"><span data-stu-id="e32b8-126">m\_fTerminalsUpToDate</span></span>   | <span data-ttu-id="e32b8-127">Dieses Flag ist **true** , wenn die Terminal Liste auf dem neuesten Stand ist.</span><span class="sxs-lookup"><span data-stu-id="e32b8-127">This flag is **TRUE** if the terminal list is up to date.</span></span>                                        |
| <span data-ttu-id="e32b8-128">Cmspcritsection</span><span class="sxs-lookup"><span data-stu-id="e32b8-128">CMSPCritSection</span></span>                 | <span data-ttu-id="e32b8-129">m \_ terminaldatalock</span><span class="sxs-lookup"><span data-stu-id="e32b8-129">m\_TerminalDataLock</span></span>     | <span data-ttu-id="e32b8-130">Die Sperre, die die Terminal bezogenen Datenmember schützt.</span><span class="sxs-lookup"><span data-stu-id="e32b8-130">The lock that protects the terminal-related data members.</span></span>                                        |



 

 

 



