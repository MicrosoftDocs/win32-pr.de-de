---
description: Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: Reine virtuelle cmspaddress-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93c9b2a995554dd2f7412c8fa5bf153ea8871e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348635"
---
# <a name="cmspaddress-pure-virtual-methods"></a><span data-ttu-id="2b589-103">Reine virtuelle cmspaddress-Methoden</span><span class="sxs-lookup"><span data-stu-id="2b589-103">CMSPAddress Pure Virtual Methods</span></span>

<span data-ttu-id="2b589-104">Diese Methoden müssen von abgeleiteten Klassen überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2b589-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="2b589-105">Reine virtuelle cmspaddress-Methoden</span><span class="sxs-lookup"><span data-stu-id="2b589-105">CMSPAddress pure virtual methods</span></span>                           | <span data-ttu-id="2b589-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b589-106">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b589-107">**Mspaddressadressf**</span><span class="sxs-lookup"><span data-stu-id="2b589-107">**MSPAddressAddRef**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | <span data-ttu-id="2b589-108">Private adressf-Methode für die Adresse.</span><span class="sxs-lookup"><span data-stu-id="2b589-108">Private AddRef method for the address.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="2b589-109">**Mspaddressrelease**</span><span class="sxs-lookup"><span data-stu-id="2b589-109">**MSPAddressRelease**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | <span data-ttu-id="2b589-110">Private releasemethode für die Adresse.</span><span class="sxs-lookup"><span data-stu-id="2b589-110">Private Release method for the address.</span></span>                                                                                                                                                |
| [<span data-ttu-id="2b589-111">**"" Für ""**</span><span class="sxs-lookup"><span data-stu-id="2b589-111">**CreateMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | <span data-ttu-id="2b589-112">Wird von TAPI aufgerufen, um ein Aufruf Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2b589-112">Called by TAPI to create a call object.</span></span> <span data-ttu-id="2b589-113">Die Implementierung in der abgeleiteten Klasse sollte einfach die Funktion " [**deatemspcallhelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) " aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2b589-113">The implementation in the derived class should simply call the [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) function.</span></span>        |
| [<span data-ttu-id="2b589-114">**Shutdownmspcallcenter**</span><span class="sxs-lookup"><span data-stu-id="2b589-114">**ShutdownMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | <span data-ttu-id="2b589-115">Wird von TAPI aufgerufen, um ein Aufruf Objekt zu schließen.</span><span class="sxs-lookup"><span data-stu-id="2b589-115">Called by TAPI to shut down a call object.</span></span> <span data-ttu-id="2b589-116">Die Implementierung in der abgeleiteten Klasse sollte einfach die [**shutdownmspcallhelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2b589-116">The implementation in the derived class should simply call the [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) function.</span></span> |
| [<span data-ttu-id="2b589-117">**Getcallmediatypes**</span><span class="sxs-lookup"><span data-stu-id="2b589-117">**GetCallMediaTypes**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | <span data-ttu-id="2b589-118">Ruft die vom MSP unterstützten Medientypen ab.</span><span class="sxs-lookup"><span data-stu-id="2b589-118">Gets media types supported by the MSP.</span></span>                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="2b589-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b589-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b589-120">**Cmspaddress**</span><span class="sxs-lookup"><span data-stu-id="2b589-120">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



