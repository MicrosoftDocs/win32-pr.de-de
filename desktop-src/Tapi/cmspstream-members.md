---
description: Die folgende Liste enthält die cmspstream-Member.
ms.assetid: 792a29ac-ebbb-4bb2-bebf-fbf870b18e84
title: Cmspstream-Member
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacee41ff95cdf16c7cd50c2e39017d9dfa7e83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131720"
---
# <a name="cmspstream-members"></a><span data-ttu-id="4a3de-103">Cmspstream-Member</span><span class="sxs-lookup"><span data-stu-id="4a3de-103">CMSPStream Members</span></span>



| <span data-ttu-id="4a3de-104">Memberart</span><span class="sxs-lookup"><span data-stu-id="4a3de-104">Member type</span></span>                     | <span data-ttu-id="4a3de-105">Name</span><span class="sxs-lookup"><span data-stu-id="4a3de-105">Name</span></span>                | <span data-ttu-id="4a3de-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a3de-106">Description</span></span>                                                                                                                                |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a3de-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a3de-107">IUnknown</span></span>                        | <span data-ttu-id="4a3de-108">\*Mio. \_ pftm</span><span class="sxs-lookup"><span data-stu-id="4a3de-108">\*m\_pFTM</span></span>           | <span data-ttu-id="4a3de-109">Zeiger auf den Free Threaded Marshaller.</span><span class="sxs-lookup"><span data-stu-id="4a3de-109">Pointer to the free threaded marshaller.</span></span>                                                                                                   |
| <span data-ttu-id="4a3de-110">DWORD</span><span class="sxs-lookup"><span data-stu-id="4a3de-110">DWORD</span></span>                           | <span data-ttu-id="4a3de-111">m \_ dwstate</span><span class="sxs-lookup"><span data-stu-id="4a3de-111">m\_dwState</span></span>          | <span data-ttu-id="4a3de-112">Der aktuelle Zustand des Streams.</span><span class="sxs-lookup"><span data-stu-id="4a3de-112">The current state of the stream.</span></span>                                                                                                           |
| <span data-ttu-id="4a3de-113">HANDLE</span><span class="sxs-lookup"><span data-stu-id="4a3de-113">HANDLE</span></span>                          | <span data-ttu-id="4a3de-114">m \_ had-Kleid</span><span class="sxs-lookup"><span data-stu-id="4a3de-114">m\_hAddress</span></span>         | <span data-ttu-id="4a3de-115">Die Adresse, für die dieser Stream verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4a3de-115">The address on which this stream is being used.</span></span>                                                                                            |
| <span data-ttu-id="4a3de-116">DWORD</span><span class="sxs-lookup"><span data-stu-id="4a3de-116">DWORD</span></span>                           | <span data-ttu-id="4a3de-117">Mio. \_ dwmediatype</span><span class="sxs-lookup"><span data-stu-id="4a3de-117">m\_dwMediaType</span></span>      | <span data-ttu-id="4a3de-118">Der [**Medientyp**](tapimediatype--constants.md) dieses Streams (Audiodaten, Video usw.).</span><span class="sxs-lookup"><span data-stu-id="4a3de-118">The [**media type**](tapimediatype--constants.md) of this stream (audio, video, etc.).</span></span>                                                    |
| <span data-ttu-id="4a3de-119">Terminal \_ Richtung</span><span class="sxs-lookup"><span data-stu-id="4a3de-119">TERMINAL\_DIRECTION</span></span>             | <span data-ttu-id="4a3de-120">m \_ Richtung</span><span class="sxs-lookup"><span data-stu-id="4a3de-120">m\_Direction</span></span>        | <span data-ttu-id="4a3de-121">Die [**Richtung**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) dieses Streams (eingehend oder ausgehend).</span><span class="sxs-lookup"><span data-stu-id="4a3de-121">The [**direction**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) of this stream (incoming or outgoing).</span></span>                                                         |
| <span data-ttu-id="4a3de-122">Cmspcallbase</span><span class="sxs-lookup"><span data-stu-id="4a3de-122">CMSPCallBase</span></span>                    | <span data-ttu-id="4a3de-123">\*m \_ pmspcallcenter</span><span class="sxs-lookup"><span data-stu-id="4a3de-123">\*m\_pMSPCall</span></span>       | <span data-ttu-id="4a3de-124">Zeiger auf das-Objekt des Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="4a3de-124">Pointer to the call object.</span></span>                                                                                                                |
| <span data-ttu-id="4a3de-125">Igraphbuilder</span><span class="sxs-lookup"><span data-stu-id="4a3de-125">IGraphBuilder</span></span>                   | <span data-ttu-id="4a3de-126">\*m \_ pigraphbuilder</span><span class="sxs-lookup"><span data-stu-id="4a3de-126">\*m\_pIGraphBuilder</span></span> | <span data-ttu-id="4a3de-127">Zeiger auf Diagramm Objekt Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="4a3de-127">Pointer to graph object interfaces.</span></span>                                                                                                        |
| <span data-ttu-id="4a3de-128">IMediaControl</span><span class="sxs-lookup"><span data-stu-id="4a3de-128">IMediaControl</span></span>                   | <span data-ttu-id="4a3de-129">\*m \_ pimediacontrol</span><span class="sxs-lookup"><span data-stu-id="4a3de-129">\*m\_pIMediaControl</span></span> | <span data-ttu-id="4a3de-130">Ein Zeiger auf die Medien Steuerungs Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4a3de-130">Pointer to the media control interface.</span></span>                                                                                                    |
| <span data-ttu-id="4a3de-131">Cmsparray <itterminal \*></span><span class="sxs-lookup"><span data-stu-id="4a3de-131">CMSPArray <ITTerminal \*></span></span> | <span data-ttu-id="4a3de-132">m- \_ Terminals</span><span class="sxs-lookup"><span data-stu-id="4a3de-132">m\_Terminals</span></span>        | <span data-ttu-id="4a3de-133">Die Liste der Terminals im Stream.</span><span class="sxs-lookup"><span data-stu-id="4a3de-133">The list of terminals on the stream.</span></span>                                                                                                       |
| <span data-ttu-id="4a3de-134">Cmspcritsection</span><span class="sxs-lookup"><span data-stu-id="4a3de-134">CMSPCritSection</span></span>                 | <span data-ttu-id="4a3de-135">m- \_ Sperre</span><span class="sxs-lookup"><span data-stu-id="4a3de-135">m\_lock</span></span>             | <span data-ttu-id="4a3de-136">Die Sperre, die das Datenstrom Objekt schützt.</span><span class="sxs-lookup"><span data-stu-id="4a3de-136">The lock that protects the stream object.</span></span> <span data-ttu-id="4a3de-137">Das Stream-Objekt sollte die Sperre nie abrufen und dann eine mspcallcenter-Methode, die möglicherweise sperrt, aufruft.</span><span class="sxs-lookup"><span data-stu-id="4a3de-137">The stream object should never acquire the lock and then call an MSPCall method that might lock.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4a3de-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a3de-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a3de-139">**Cmspstream**</span><span class="sxs-lookup"><span data-stu-id="4a3de-139">**CMSPStream**</span></span>](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



