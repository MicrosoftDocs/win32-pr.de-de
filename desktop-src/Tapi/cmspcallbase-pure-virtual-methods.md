---
description: 'CMSPCallBase Pure Virtual Methods : Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.'
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: CMSPCallBase – reine virtuelle Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da8530ab3dae737bf1407f00d5d4a415a1437e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094458"
---
# <a name="cmspcallbase-pure-virtual-methods"></a><span data-ttu-id="e894f-103">CMSPCallBase – reine virtuelle Methoden</span><span class="sxs-lookup"><span data-stu-id="e894f-103">CMSPCallBase Pure Virtual Methods</span></span>

<span data-ttu-id="e894f-104">Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e894f-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="e894f-105">REINE VIRTUELLE CMSPCallBase-Methoden</span><span class="sxs-lookup"><span data-stu-id="e894f-105">CMSPCallBase pure virtual methods</span></span>                                 | <span data-ttu-id="e894f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e894f-106">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e894f-107">**MSPCallAddRef**</span><span class="sxs-lookup"><span data-stu-id="e894f-107">**MSPCallAddRef**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | <span data-ttu-id="e894f-108">Private AddRef-Methode für das Aufrufobjekt.</span><span class="sxs-lookup"><span data-stu-id="e894f-108">Private AddRef method for the call object.</span></span>                                                                                              |
| [<span data-ttu-id="e894f-109">**MSPCallRelease**</span><span class="sxs-lookup"><span data-stu-id="e894f-109">**MSPCallRelease**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | <span data-ttu-id="e894f-110">Private Release-Methode für das Aufrufobjekt.</span><span class="sxs-lookup"><span data-stu-id="e894f-110">Private Release method for the call object.</span></span>                                                                                             |
| [<span data-ttu-id="e894f-111">**Init**</span><span class="sxs-lookup"><span data-stu-id="e894f-111">**Init**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | <span data-ttu-id="e894f-112">Wird vom MSP-Adressobjekt (in der [**Methode CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) aufgerufen, um das MSP-Aufrufobjekt zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="e894f-112">Called by the MSP address object (in the method [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) to initialize the MSP call object.</span></span> |
| [<span data-ttu-id="e894f-113">**Herunterfahren**</span><span class="sxs-lookup"><span data-stu-id="e894f-113">**ShutDown**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | <span data-ttu-id="e894f-114">Wird vom MSP-Adressobjekt aufgerufen, um den Aufruf herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="e894f-114">Called by the MSP address object to shut down the call..</span></span>                                                                                |
| [<span data-ttu-id="e894f-115">**InternalCreateStream**</span><span class="sxs-lookup"><span data-stu-id="e894f-115">**InternalCreateStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | <span data-ttu-id="e894f-116">Wird von [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) aufgerufen, um ein Streamobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e894f-116">Called by [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) to create a stream object.</span></span>                                               |
| [<span data-ttu-id="e894f-117">**CreateStreamObject**</span><span class="sxs-lookup"><span data-stu-id="e894f-117">**CreateStreamObject**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | <span data-ttu-id="e894f-118">Wird von [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) aufgerufen, um ein Streamobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e894f-118">Called by [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) to create a stream object.</span></span>                                  |
| [<span data-ttu-id="e894f-119">**RemoveStream**</span><span class="sxs-lookup"><span data-stu-id="e894f-119">**RemoveStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | <span data-ttu-id="e894f-120">Wird von der Anwendung aufgerufen, um einen Stream aus dem Aufruf zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="e894f-120">Called by the application to remove a stream from the call</span></span>                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="e894f-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e894f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e894f-122">**CMSPCallBase**</span><span class="sxs-lookup"><span data-stu-id="e894f-122">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
