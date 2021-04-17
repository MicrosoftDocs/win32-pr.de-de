---
title: Informationen zur Geräte Host-API
description: Die Geräte Host-API mit UPnP-Technologie ist ein Framework für die Implementierung von UPnP-basierter Gerätefunktionalität auf der Windows-Plattform.
ms.assetid: fa716c59-d3f0-4cd4-b92d-939b258b0102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c751328696d6524208dc95a0b7961829f8ee231c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388645"
---
# <a name="about-the-device-host-api"></a><span data-ttu-id="8aa01-103">Informationen zur Geräte Host-API</span><span class="sxs-lookup"><span data-stu-id="8aa01-103">About the Device Host API</span></span>

<span data-ttu-id="8aa01-104">Die Geräte Host-API mit UPnP-Technologie ist ein Framework für die Implementierung von UPnP-basierter Gerätefunktionalität auf der Windows-Plattform.</span><span class="sxs-lookup"><span data-stu-id="8aa01-104">The Device Host API with UPnP technology is a framework for implementing UPnP-based device functionality on the Windows platform.</span></span> <span data-ttu-id="8aa01-105">Entwickler, die Geräte mithilfe der Geräte Host-API mit UPnP-Technologie (als [*gehostete Geräte*](h-gly.md)bezeichnet) erstellen, müssen nur die Kernfunktionen des Geräts implementieren.</span><span class="sxs-lookup"><span data-stu-id="8aa01-105">Developers who are creating devices by using the Device Host API with UPnP technology (referred to as [*hosted devices*](h-gly.md)) need only implement the device's core functionality.</span></span> <span data-ttu-id="8aa01-106">Entwickler können sich auf den Geräte Host verlassen, um die UPnP-spezifischen Details von Ermittlung, Beschreibung, Steuerung, Ereignis und Präsentation zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="8aa01-106">Developers can rely on the device host to handle the UPnP-specific details of discovery, description, control, eventing, and presentation.</span></span> <span data-ttu-id="8aa01-107">Der Geräte Host überprüft eingehende Daten von UPnP-basierten Clients und formatiert alle ausgehenden Daten von gehosteten Geräten entsprechend der UPnP-Geräte Architektur.</span><span class="sxs-lookup"><span data-stu-id="8aa01-107">The device host validates incoming data from UPnP-based clients and formats all outgoing data from hosted devices according to the UPnP device architecture.</span></span>

<span data-ttu-id="8aa01-108">In den folgenden Abschnitten wird im allgemeinen erläutert, wie der UPnP-Geräte Host funktioniert:</span><span class="sxs-lookup"><span data-stu-id="8aa01-108">The following sections explain, in general, how the UPnP device host works:</span></span>

-   [<span data-ttu-id="8aa01-109">Implementieren eines gehosteten Geräts</span><span class="sxs-lookup"><span data-stu-id="8aa01-109">Implementing a Hosted Device</span></span>](implementing-a-hosted-device.md)
-   [<span data-ttu-id="8aa01-110">Registrieren eines gehosteten Geräts beim Geräte Host</span><span class="sxs-lookup"><span data-stu-id="8aa01-110">Registering a Hosted Device with the Device Host</span></span>](registering-a-hosted-device-with-the-device-host.md)
-   [<span data-ttu-id="8aa01-111">Geräte Anbieter</span><span class="sxs-lookup"><span data-stu-id="8aa01-111">Device Providers</span></span>](device-providers.md)
-   [<span data-ttu-id="8aa01-112">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8aa01-112">Eventing</span></span>](eventing.md)
-   [<span data-ttu-id="8aa01-113">Präsentation</span><span class="sxs-lookup"><span data-stu-id="8aa01-113">Presentation</span></span>](presentation.md)

 

 




