---
description: Das TAPI-Objekt ist das Hauptobjekt für TAPI 3.
ms.assetid: 046f2646-6043-4d68-a42a-8750c016b3c8
title: TAPI-Objekt Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906bda205f0d00a54cdb14cf408431cc45cad124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363640"
---
# <a name="tapi-object-interfaces"></a><span data-ttu-id="93293-103">TAPI-Objekt Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="93293-103">TAPI Object Interfaces</span></span>

<span data-ttu-id="93293-104">Das [TAPI-Objekt](tapi-object.md) ist das Hauptobjekt für TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="93293-104">The [TAPI Object](tapi-object.md) is the main object for TAPI 3.</span></span>

<span data-ttu-id="93293-105">Die [**ittapiobjectevent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) -Schnittstelle wird nicht direkt für das TAPI-Objekt verfügbar gemacht, ist jedoch eng mit ihr verknüpft und wird hier zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="93293-105">The [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent) interface is not directly exposed on the TAPI Object, but is tightly related to it and is listed here for reference convenience.</span></span>



| <span data-ttu-id="93293-106">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="93293-106">Interfaces</span></span>                                                 | <span data-ttu-id="93293-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93293-107">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93293-108">**Ittapi**</span><span class="sxs-lookup"><span data-stu-id="93293-108">**ITTAPI**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)                                   | <span data-ttu-id="93293-109">Primäre TAPI 3-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="93293-109">Primary TAPI 3 interface.</span></span>                                                                                                                              |
| [<span data-ttu-id="93293-110">**ITTAPI2**</span><span class="sxs-lookup"><span data-stu-id="93293-110">**ITTAPI2**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2)                                 | <span data-ttu-id="93293-111">Wird von [**ittapi**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi)abgeleitet. bietet zusätzliche Methoden zur Unterstützung von Telefongeräten.</span><span class="sxs-lookup"><span data-stu-id="93293-111">Derives from [**ITTAPI**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapi); provides additional methods that support phone devices.</span></span>                                                         |
| [<span data-ttu-id="93293-112">**Ittapieventnotification**</span><span class="sxs-lookup"><span data-stu-id="93293-112">**ITTAPIEventNotification**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) | <span data-ttu-id="93293-113">Ausgehende Schnittstelle, mit der asynchrone Informationen zu TAPI 3-Ereignissen empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="93293-113">Outgoing interface used to receive asynchronous information about TAPI 3 events.</span></span>                                                                       |
| [<span data-ttu-id="93293-114">**Ittapicallcenter**</span><span class="sxs-lookup"><span data-stu-id="93293-114">**ITTAPICallCenter**</span></span>](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter)               | <span data-ttu-id="93293-115">Stellt eine Einstiegs Schnittstelle in callcentersteuerelemente bereit.</span><span class="sxs-lookup"><span data-stu-id="93293-115">Provides an entry interface into call center controls.</span></span>                                                                                                 |
| [<span data-ttu-id="93293-116">**Ittapiobjectevent**</span><span class="sxs-lookup"><span data-stu-id="93293-116">**ITTAPIObjectEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent)             | <span data-ttu-id="93293-117">Stellt Methoden zum Abrufen von Informationen zu TAPI-Objekt Ereignissen bereit.</span><span class="sxs-lookup"><span data-stu-id="93293-117">Provides methods to retrieve information concerning TAPI object events.</span></span>                                                                                |
| [<span data-ttu-id="93293-118">**ITTAPIObjectEvent2**</span><span class="sxs-lookup"><span data-stu-id="93293-118">**ITTAPIObjectEvent2**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2)           | <span data-ttu-id="93293-119">Erweitert [**ittapiobjectevent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); stellt eine Methode zum Abrufen eines Zeigers auf das Telefon Objekt bereit, das das TAPI-Objekt Ereignis verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="93293-119">Extends [**ITTAPIObjectEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent); provides a method to retrieve a pointer to the phone object that caused the TAPI object event.</span></span> |



 

 

 
