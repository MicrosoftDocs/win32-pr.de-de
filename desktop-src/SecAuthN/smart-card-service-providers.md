---
description: Smart Card Service Providers (SCSP) ermöglichen den Zugriff auf Smartcardfunktionen.
ms.assetid: f214385f-3e65-4175-925c-3d1dc4060185
title: Smartcarddienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc60e9987912426fcca3f6605b9218e085e61ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352465"
---
# <a name="smart-card-service-providers"></a><span data-ttu-id="18c59-103">Smartcarddienstanbieter</span><span class="sxs-lookup"><span data-stu-id="18c59-103">Smart Card Service Providers</span></span>

<span data-ttu-id="18c59-104">Smart Card Service Providers (SCSP) ermöglichen den Zugriff auf [*Smartcardfunktionen*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="18c59-104">Smart Card Service Providers (SCSP) provide access to [*Smart Card*](../secgloss/s-gly.md) capabilities.</span></span> <span data-ttu-id="18c59-105">Sie können den Zugriff auf eine einzelne Funktion ermöglichen, wie z. b. die vom Smartcard-SDK bereitgestellten Basis Dienstanbieter, oder Sie können Zugriff auf verschiedene Funktionen bereitstellen, um eine komplexere Aufgabe zu erledigen.</span><span class="sxs-lookup"><span data-stu-id="18c59-105">They can provide access to a single capability, such as the base service providers provided by the Smart Card SDK, or they can provide access to several capabilities to accomplish a more complex task.</span></span>

<span data-ttu-id="18c59-106">Dienstanbieter ermöglichen den Zugriff über COM-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="18c59-106">Service providers provide access through COM interfaces.</span></span> <span data-ttu-id="18c59-107">Das Smartcard SDK stellt die COM-Schnittstellen bereit, die von den eigenen Basis Dienstanbietern verwendet werden, sowie mehrere Anwendungsschnittstellen, die beim Entwickeln von benutzerdefinierten Dienstanbietern verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="18c59-107">The Smart Card SDK provides the COM interfaces used by its own base service providers as well as several application interfaces that can be used when developing custom service providers.</span></span>



| <span data-ttu-id="18c59-108">Thema</span><span class="sxs-lookup"><span data-stu-id="18c59-108">Topic</span></span>                                                                                   | <span data-ttu-id="18c59-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18c59-109">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="18c59-110">Basis Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="18c59-110">Base Service Providers</span></span>](base-service-providers.md)<br/>                         | <span data-ttu-id="18c59-111">Basis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="18c59-111">Base service providers.</span></span><br/>                     |
| [<span data-ttu-id="18c59-112">Aufbauen eines ISO7816-4-APDU-Befehls</span><span class="sxs-lookup"><span data-stu-id="18c59-112">Building an ISO7816-4 APDU Command</span></span>](building-an-iso7816-4-apdu-command.md)<br/> | <span data-ttu-id="18c59-113">Hinzufügen von Funktionen zu einem Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="18c59-113">Adding functionality to a service provider.</span></span><br/> |
| [<span data-ttu-id="18c59-114">Anbieter-Wrapper Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="18c59-114">Vendor Wrapper Service Provider</span></span>](vendor-wrapper-service-provider.md)<br/>       | <span data-ttu-id="18c59-115">Ein Beispiel für einen Hersteller Wrapper.</span><span class="sxs-lookup"><span data-stu-id="18c59-115">A vendor wrapper example.</span></span><br/>                   |



 

<span data-ttu-id="18c59-116">Eine Übersicht über alle COM-Schnittstellen, die vom Smartcard SDK (Basis Dienstanbieter und Anwendungsschnittstellen) bereitgestellt werden, finden Sie unter [Smartcard-Schnittstellen](smart-card-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="18c59-116">For an overview of all the COM interfaces provided by the smart card SDK (base service provider and application interfaces), see [Smart Card Interfaces](smart-card-interfaces.md).</span></span>

 

 
