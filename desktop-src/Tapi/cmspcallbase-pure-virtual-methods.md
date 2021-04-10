---
description: Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Reine virtuelle cmspcallbase-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d8dea4c1a240e362a4dc3a19b3c09a37a318947
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865379"
---
# <a name="cmspcallbase-pure-virtual-methods"></a><span data-ttu-id="96821-103">Reine virtuelle cmspcallbase-Methoden</span><span class="sxs-lookup"><span data-stu-id="96821-103">CMSPCallBase Pure Virtual Methods</span></span>

<span data-ttu-id="96821-104">Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="96821-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="96821-105">Reine virtuelle cmspcallbase-Methoden</span><span class="sxs-lookup"><span data-stu-id="96821-105">CMSPCallBase pure virtual methods</span></span>                                 | <span data-ttu-id="96821-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96821-106">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96821-107">**Mspcalladressf**</span><span class="sxs-lookup"><span data-stu-id="96821-107">**MSPCallAddRef**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | <span data-ttu-id="96821-108">Private adressf-Methode für das calltobjekt.</span><span class="sxs-lookup"><span data-stu-id="96821-108">Private AddRef method for the call object.</span></span>                                                                                              |
| [<span data-ttu-id="96821-109">**Mspcallrelease**</span><span class="sxs-lookup"><span data-stu-id="96821-109">**MSPCallRelease**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | <span data-ttu-id="96821-110">Private releasemethode für das-Objekt des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="96821-110">Private Release method for the call object.</span></span>                                                                                             |
| [<span data-ttu-id="96821-111">**Init**</span><span class="sxs-lookup"><span data-stu-id="96821-111">**Init**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | <span data-ttu-id="96821-112">Wird vom MSP-Adress Objekt (in [**der Methode "**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)" "" "" "" "" "" "" "" "" "" "" "</span><span class="sxs-lookup"><span data-stu-id="96821-112">Called by the MSP address object (in the method [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) to initialize the MSP call object.</span></span> |
| [<span data-ttu-id="96821-113">**Abschlusses**</span><span class="sxs-lookup"><span data-stu-id="96821-113">**ShutDown**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | <span data-ttu-id="96821-114">Wird vom MSP-Adress Objekt aufgerufen, um den Aufruf zu beenden.</span><span class="sxs-lookup"><span data-stu-id="96821-114">Called by the MSP address object to shut down the call..</span></span>                                                                                |
| [<span data-ttu-id="96821-115">**Internalkreatestream**</span><span class="sxs-lookup"><span data-stu-id="96821-115">**InternalCreateStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | <span data-ttu-id="96821-116">Wird von " [**kreatestream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) " aufgerufen, um ein Streamobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="96821-116">Called by [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) to create a stream object.</span></span>                                               |
| [<span data-ttu-id="96821-117">**"Kreatestreamobject"**</span><span class="sxs-lookup"><span data-stu-id="96821-117">**CreateStreamObject**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | <span data-ttu-id="96821-118">Wird von [**internalkreatestream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) aufgerufen, um ein Stream-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="96821-118">Called by [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) to create a stream object.</span></span>                                  |
| [<span data-ttu-id="96821-119">**Removestream**</span><span class="sxs-lookup"><span data-stu-id="96821-119">**RemoveStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | <span data-ttu-id="96821-120">Wird von der Anwendung aufgerufen, um einen Stream aus dem Aufruf zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="96821-120">Called by the application to remove a stream from the call</span></span>                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="96821-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="96821-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96821-122">**Cmspcallbase**</span><span class="sxs-lookup"><span data-stu-id="96821-122">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
