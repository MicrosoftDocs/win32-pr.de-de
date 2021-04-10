---
title: Gründe für die Nichterreichbarkeit
description: In der folgenden Tabelle werden Konstante Werte aufgelistet, die angeben, warum eine Schnittstelle nicht erreichbar ist.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b99d36ba895394a417130ab3ae45d1a47c7ed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039340"
---
# <a name="unreachability-reasons"></a><span data-ttu-id="08ad4-103">Gründe für die Nichterreichbarkeit</span><span class="sxs-lookup"><span data-stu-id="08ad4-103">Unreachability Reasons</span></span>

<span data-ttu-id="08ad4-104">In der folgenden Tabelle werden Konstante Werte aufgelistet, die angeben, warum eine Schnittstelle nicht erreichbar ist.</span><span class="sxs-lookup"><span data-stu-id="08ad4-104">The following table lists constant values that indicate why an interface is unreachable.</span></span>



| <span data-ttu-id="08ad4-105">Wert</span><span class="sxs-lookup"><span data-stu-id="08ad4-105">Value</span></span>                                       | <span data-ttu-id="08ad4-106">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="08ad4-106">Meaning</span></span>                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08ad4-107">MPR- \_ Schnittstellen \_ Administrator \_ deaktiviert</span><span class="sxs-lookup"><span data-stu-id="08ad4-107">MPR\_INTERFACE\_ADMIN\_DISABLED</span></span>             | <span data-ttu-id="08ad4-108">Der Administrator hat die Schnittstelle deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="08ad4-108">The administrator has disabled the interface.</span></span>                                                  |
| <span data-ttu-id="08ad4-109">MPR- \_ Schnittstellen \_ Verbindungs \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="08ad4-109">MPR\_INTERFACE\_CONNECTION\_FAILURE</span></span>         | <span data-ttu-id="08ad4-110">Der vorherige Verbindungsversuch ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="08ad4-110">The previous connection attempt failed.</span></span> <span data-ttu-id="08ad4-111">Überprüfen Sie den **dwlasterror** -Member auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="08ad4-111">Look at the **dwLastError** member for the error code.</span></span> |
| <span data-ttu-id="08ad4-112">Einschränkung der MPR- \_ Schnittstellen-ddstunden \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="08ad4-112">MPR\_INTERFACE\_DIALOUT\_HOURS\_RESTRICTION</span></span> | <span data-ttu-id="08ad4-113">Das auswählgerät ist zum aktuellen Zeitpunkt nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="08ad4-113">Dial-out is not allowed at the current time.</span></span>                                                   |
| <span data-ttu-id="08ad4-114">MPR- \_ Schnittstelle \_ aus \_ \_ Ressourcen</span><span class="sxs-lookup"><span data-stu-id="08ad4-114">MPR\_INTERFACE\_OUT\_OF\_RESOURCES</span></span>          | <span data-ttu-id="08ad4-115">Es sind keine Ports oder Geräte zur Verwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="08ad4-115">No ports or devices are available for use.</span></span>                                                     |
| <span data-ttu-id="08ad4-116">MPR- \_ Schnittstellen \_ Dienst \_ angehalten</span><span class="sxs-lookup"><span data-stu-id="08ad4-116">MPR\_INTERFACE\_SERVICE\_PAUSED</span></span>             | <span data-ttu-id="08ad4-117">Der Dienst wurde angehalten.</span><span class="sxs-lookup"><span data-stu-id="08ad4-117">The service is paused.</span></span>                                                                         |
| <span data-ttu-id="08ad4-118">MPR- \_ Schnittstelle \_ ohne \_ Medien \_ Sinn</span><span class="sxs-lookup"><span data-stu-id="08ad4-118">MPR\_INTERFACE\_NO\_MEDIA\_SENSE</span></span>            | <span data-ttu-id="08ad4-119">Das Netzwerkkabel ist von der Netzwerkkarte getrennt.</span><span class="sxs-lookup"><span data-stu-id="08ad4-119">The network cable is disconnected from the network card.</span></span>                                       |
| <span data-ttu-id="08ad4-120">MPR- \_ Schnittstelle \_ ohne \_ Gerät</span><span class="sxs-lookup"><span data-stu-id="08ad4-120">MPR\_INTERFACE\_NO\_DEVICE</span></span>                  | <span data-ttu-id="08ad4-121">Die Netzwerkkarte wurde vom Computer entfernt.</span><span class="sxs-lookup"><span data-stu-id="08ad4-121">The network card has been removed from the machine.</span></span>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="08ad4-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08ad4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08ad4-123">**MPR- \_ Schnittstelle \_ 0**</span><span class="sxs-lookup"><span data-stu-id="08ad4-123">**MPR\_INTERFACE\_0**</span></span>](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[<span data-ttu-id="08ad4-124">**MPR- \_ Schnittstelle \_ 1**</span><span class="sxs-lookup"><span data-stu-id="08ad4-124">**MPR\_INTERFACE\_1**</span></span>](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[<span data-ttu-id="08ad4-125">**MIB \_ ifrow**</span><span class="sxs-lookup"><span data-stu-id="08ad4-125">**MIB\_IFROW**</span></span>](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[<span data-ttu-id="08ad4-126">**MIB \_ if-Status**</span><span class="sxs-lookup"><span data-stu-id="08ad4-126">**MIB\_IFSTATUS**</span></span>](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 