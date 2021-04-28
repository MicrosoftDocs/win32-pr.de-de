---
description: 'REINE VIRTUELLE CMSPAddress-Methoden: Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.'
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: CMSPAddress Pure Virtual Methods
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d9b9494e4ee42972d97433927fd587034af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084208"
---
# <a name="cmspaddress-pure-virtual-methods"></a><span data-ttu-id="bd69a-103">CMSPAddress Pure Virtual Methods</span><span class="sxs-lookup"><span data-stu-id="bd69a-103">CMSPAddress Pure Virtual Methods</span></span>

<span data-ttu-id="bd69a-104">Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bd69a-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="bd69a-105">REINE VIRTUELLE CMSPAddress-Methoden</span><span class="sxs-lookup"><span data-stu-id="bd69a-105">CMSPAddress pure virtual methods</span></span>                           | <span data-ttu-id="bd69a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd69a-106">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd69a-107">**MSPAddressAddRef**</span><span class="sxs-lookup"><span data-stu-id="bd69a-107">**MSPAddressAddRef**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | <span data-ttu-id="bd69a-108">Private AddRef-Methode für die Adresse.</span><span class="sxs-lookup"><span data-stu-id="bd69a-108">Private AddRef method for the address.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="bd69a-109">**MSPAddressRelease**</span><span class="sxs-lookup"><span data-stu-id="bd69a-109">**MSPAddressRelease**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | <span data-ttu-id="bd69a-110">Private Release-Methode für die Adresse.</span><span class="sxs-lookup"><span data-stu-id="bd69a-110">Private Release method for the address.</span></span>                                                                                                                                                |
| [<span data-ttu-id="bd69a-111">**CreateMSPCall**</span><span class="sxs-lookup"><span data-stu-id="bd69a-111">**CreateMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | <span data-ttu-id="bd69a-112">Wird von TAPI aufgerufen, um ein Aufrufobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bd69a-112">Called by TAPI to create a call object.</span></span> <span data-ttu-id="bd69a-113">Die Implementierung in der abgeleiteten Klasse sollte einfach die [**CreateMSPCallHelper-Funktion**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bd69a-113">The implementation in the derived class should simply call the [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) function.</span></span>        |
| [<span data-ttu-id="bd69a-114">**ShutdownMSPCall**</span><span class="sxs-lookup"><span data-stu-id="bd69a-114">**ShutdownMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | <span data-ttu-id="bd69a-115">Wird von TAPI aufgerufen, um ein Aufrufobjekt herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="bd69a-115">Called by TAPI to shut down a call object.</span></span> <span data-ttu-id="bd69a-116">Die Implementierung in der abgeleiteten Klasse sollte einfach die [**ShutdownMSPCallHelper-Funktion**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bd69a-116">The implementation in the derived class should simply call the [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) function.</span></span> |
| [<span data-ttu-id="bd69a-117">**GetCallMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="bd69a-117">**GetCallMediaTypes**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | <span data-ttu-id="bd69a-118">Ruft vom MSP unterstützte Medientypen ab.</span><span class="sxs-lookup"><span data-stu-id="bd69a-118">Gets media types supported by the MSP.</span></span>                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="bd69a-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bd69a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd69a-120">**CMSPAddress**</span><span class="sxs-lookup"><span data-stu-id="bd69a-120">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



