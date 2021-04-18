---
description: Ein Netzwerkanbieter ist eine DLL, mit der das Windows-Betriebssystem mit anderen Arten von Netzwerken interagieren kann, z. b. Novell. Es handelt sich um einen Client des Windows-WNET-Treibers.
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: Netzwerkanbieter-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc68184f60639a603614cbaf71631a2521012cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368942"
---
# <a name="network-provider-api"></a><span data-ttu-id="ec93d-104">Netzwerkanbieter-API</span><span class="sxs-lookup"><span data-stu-id="ec93d-104">Network Provider API</span></span>

<span data-ttu-id="ec93d-105">Ein Netzwerkanbieter ist eine DLL, mit der das Windows-Betriebssystem mit anderen Arten von Netzwerken interagieren kann, z. b. Novell.</span><span class="sxs-lookup"><span data-stu-id="ec93d-105">A network provider is a DLL that enables the Windows operating system to interact with other kinds of networks, such as Novell.</span></span> <span data-ttu-id="ec93d-106">Es handelt sich um einen Client des Windows-WNET-Treibers.</span><span class="sxs-lookup"><span data-stu-id="ec93d-106">It is a client of the Windows WNet driver.</span></span> <span data-ttu-id="ec93d-107">Ein Netzwerkanbieter implementiert Netzwerk spezifische Aktionen (z. b. das Herstellen einer Verbindung) und macht eine gemeinsame Schnittstelle für Windows verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ec93d-107">A network provider implements network-specific actions, such as making a connection, and exposes a common interface to Windows.</span></span> <span data-ttu-id="ec93d-108">Diese Schnittstelle wird als Netzwerkanbieter-API bezeichnet und besteht aus Funktionen, die vom Netzwerkanbieter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="ec93d-108">This interface is called the Network Provider API and consists of functions implemented by the network provider.</span></span> <span data-ttu-id="ec93d-109">Sie können eine Netzwerkanbieter-dll erstellen, um neue Netzwerkprotokolle zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ec93d-109">You can create a network provider DLL to support new network protocols.</span></span>

<span data-ttu-id="ec93d-110">Da jedes Netzwerk über seinen Anbieter eine gemeinsame Schnittstelle verfügbar macht, kann Windows mit verschiedenen Typen von Netzwerken interagieren, ohne die Netzwerk spezifischen Implementierungsdetails kennen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="ec93d-110">Because each network exposes a common interface through its provider, Windows can interact with several types of networks without knowing their network-specific implementation details.</span></span>

<span data-ttu-id="ec93d-111">Der [*multianbieterrouter*](../secgloss/m-gly.md) (MPR) übernimmt die Kommunikation mit allen verschiedenen Netzwerkanbietern im System und stellt dem Benutzer ein integriertes Netzwerk dar.</span><span class="sxs-lookup"><span data-stu-id="ec93d-111">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) handles communication with all of the various network providers on the system and presents an integrated network to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec93d-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ec93d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec93d-113">Netzwerkanbieter</span><span class="sxs-lookup"><span data-stu-id="ec93d-113">Network Providers</span></span>](network-providers.md)
</dt> <dt>

[<span data-ttu-id="ec93d-114">Anmeldeinformationsverwaltung</span><span class="sxs-lookup"><span data-stu-id="ec93d-114">Credential Manager</span></span>](credential-manager.md)
</dt> <dt>

[<span data-ttu-id="ec93d-115">Mehrere Anbieter Router</span><span class="sxs-lookup"><span data-stu-id="ec93d-115">Multiple Provider Router</span></span>](multiple-provider-router.md)
</dt> <dt>

[<span data-ttu-id="ec93d-116">Von Netzwerkanbietern implementierte Funktionen</span><span class="sxs-lookup"><span data-stu-id="ec93d-116">Functions Implemented by Network Providers</span></span>](functions-implemented-by-network-providers.md)
</dt> <dt>

[<span data-ttu-id="ec93d-117">Credential Management-API</span><span class="sxs-lookup"><span data-stu-id="ec93d-117">Credential Management API</span></span>](credential-management-api.md)
</dt> <dt>

[<span data-ttu-id="ec93d-118">Verbindungs Benachrichtigungs-API</span><span class="sxs-lookup"><span data-stu-id="ec93d-118">Connection Notification API</span></span>](connection-notification-api.md)
</dt> </dl>

 

 
