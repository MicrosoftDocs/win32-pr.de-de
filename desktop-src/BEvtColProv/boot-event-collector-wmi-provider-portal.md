---
description: Der WMI-Anbieter des Start Ereignis Sammlers ermöglicht den Zugriff auf Verbindungs-und Konfigurationsinformationen für das Setup-und Start Ereignis Sammlungs Feature unter Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: WMI-Anbieter für Start Ereignis Sammler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38ef27b2989f856fdcfda82d4ee0e68c3913167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860596"
---
# <a name="boot-event-collector-wmi-provider"></a><span data-ttu-id="9b919-103">WMI-Anbieter für Start Ereignis Sammler</span><span class="sxs-lookup"><span data-stu-id="9b919-103">Boot Event Collector WMI Provider</span></span>

## <a name="purpose"></a><span data-ttu-id="9b919-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="9b919-104">Purpose</span></span>

<span data-ttu-id="9b919-105">Der WMI-Anbieter des Start Ereignis Sammlers ermöglicht den Zugriff auf Verbindungs-und Konfigurationsinformationen für das Setup-und Start Ereignis Sammlungs Feature unter Windows Server.</span><span class="sxs-lookup"><span data-stu-id="9b919-105">The Boot Event Collector WMI provider provides access to connection and configuration information for the Setup and Boot Event Collection feature on Windows Server.</span></span> <span data-ttu-id="9b919-106">Auf diese Weise können Sie eine Liste der aktuellen Verbindungen und den Verbindungs Verlauf zwischen einem Collector-Server und den zugehörigen Ziel Computern anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9b919-106">This allows you to view a list of the current connections and the connection history between a collector server and its target computers.</span></span> <span data-ttu-id="9b919-107">Außerdem können Sie mit diesem Anbieter die Konfiguration eines Collector-Servers verwalten.</span><span class="sxs-lookup"><span data-stu-id="9b919-107">In addition, this provider allows you to manage the configuration of a collector server.</span></span>

> [!Note]  
> <span data-ttu-id="9b919-108">Der WMI-Anbieter des Start Ereignis Sammlers wird in BEvtCol.exe implementiert.</span><span class="sxs-lookup"><span data-stu-id="9b919-108">The Boot Event Collector WMI provider is implemented in BEvtCol.exe.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="9b919-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9b919-109">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="9b919-110">**Targetforwarding**</span><span class="sxs-lookup"><span data-stu-id="9b919-110">**TargetForwarding**</span></span>](targetforwarding.md)
</dt> <dd>

<span data-ttu-id="9b919-111">Ruft Weiterleitungs Daten von einem Bereitstellungs Zielcomputer ab.</span><span class="sxs-lookup"><span data-stu-id="9b919-111">Retrieves forwarding data from a target computer.</span></span>

</dd> <dt>

[<span data-ttu-id="9b919-112">**Targetforwardingdestination**</span><span class="sxs-lookup"><span data-stu-id="9b919-112">**TargetForwardingDestination**</span></span>](targetforwardingdestination.md)
</dt> <dd>

<span data-ttu-id="9b919-113">Die bekannten Ziele, die die gesammelten Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="9b919-113">The known destinations containing the collected data.</span></span> <span data-ttu-id="9b919-114">Nur verfügbar, wenn der Collector mit aktiviertem Status Protokoll ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b919-114">Available only if the collector is running with the status log enabled.</span></span>

</dd> <dt>

[<span data-ttu-id="9b919-115">**Targetforwardinghistory**</span><span class="sxs-lookup"><span data-stu-id="9b919-115">**TargetForwardingHistory**</span></span>](targetforwardinghistory.md)
</dt> <dd>

<span data-ttu-id="9b919-116">Aktueller Verlauf der Änderungen an den Weiterleitungs Daten für einen Bereitstellungs Zielcomputer.</span><span class="sxs-lookup"><span data-stu-id="9b919-116">The recent history of changes to the forwarding data for a target computer.</span></span>

</dd> <dt>

[<span data-ttu-id="9b919-117">**Control**</span><span class="sxs-lookup"><span data-stu-id="9b919-117">**Control**</span></span>](control.md)
</dt> <dd>

<span data-ttu-id="9b919-118">Steuerung der Collector-Instanz.</span><span class="sxs-lookup"><span data-stu-id="9b919-118">Control of the collector instance.</span></span> <span data-ttu-id="9b919-119">Erfordert die Administrator Rechte (BA).</span><span class="sxs-lookup"><span data-stu-id="9b919-119">Requires the Administrator (BA) privileges.</span></span>

</dd> </dl>

 

 



