---
title: Tunnel Modus
description: Im Tunnel Modus-IPSec-Richtlinien Szenario wird der IPSec-tunnelmodusschutz für den gesamten übereinstimmenden Datenverkehr zwischen zwei Tunnel Endpunkten angewendet.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75fdecb7f959a2f95aae2649a6e3f8f94def9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310692"
---
# <a name="tunnel-mode"></a><span data-ttu-id="7aa4c-103">Tunnel Modus</span><span class="sxs-lookup"><span data-stu-id="7aa4c-103">Tunnel Mode</span></span>

<span data-ttu-id="7aa4c-104">Im Tunnel Modus-IPSec-Richtlinien Szenario wird der IPSec-tunnelmodusschutz für den gesamten übereinstimmenden Datenverkehr zwischen zwei Tunnel Endpunkten angewendet.</span><span class="sxs-lookup"><span data-stu-id="7aa4c-104">The Tunnel Mode IPsec policy scenario is used to apply IPsec tunnel mode protection for all matching traffic between two tunnel endpoints.</span></span>

<span data-ttu-id="7aa4c-105">Dieses Richtlinien Szenario wird normalerweise verwendet, um den Datenverkehr zwischen mehreren Zweigstellen Subnetzen zu schützen, wenn dieser zwischen den entsprechenden Gateways im Internet weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="7aa4c-105">This policy scenario is typically used to protect traffic between multiple branch-office subnets, when it gets forwarded between the corresponding gateways on the Internet.</span></span> <span data-ttu-id="7aa4c-106">Sie kann auch verwendet werden, um die End-to-End-Kommunikation zwischen zwei Host Computern zu sichern, auch als Punkt-zu-Punkt-Tunnel bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7aa4c-106">It can also be used to secure end-to-end communication between two host machines, also referred to as point-to-point tunnels.</span></span>

<span data-ttu-id="7aa4c-107">Um eine tunnelmodusrichtlinie mithilfe der Windows-Filter Plattform (WFP) zu implementieren, nennen Sie die [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) -Funktion, die die entsprechenden Tunnel Modusfilter auf den entsprechenden Ebenen im Namen des Aufrufers instanziiert.</span><span class="sxs-lookup"><span data-stu-id="7aa4c-107">To implement Tunnel Mode policy using the Windows Filtering Platform (WFP), call the [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) function that instantiates the appropriate tunnel mode filters at the appropriate layers on behalf of the caller.</span></span> <span data-ttu-id="7aa4c-108">Der Aufrufer muss den Hauptmodus, den Schnellmodus-Anbieter Kontext und die Filterbedingungen angeben, die den Datenverkehr beschreiben, der innerhalb des Tunnels gesichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7aa4c-108">The caller needs to specify the Main Mode, Quick Mode provider contexts, and the filter conditions describing the traffic that should be secured inside the tunnel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7aa4c-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7aa4c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7aa4c-110">Beispielcode: Verwenden des Tunnel Modus</span><span class="sxs-lookup"><span data-stu-id="7aa4c-110">Sample code: Using Tunnel Mode</span></span>](using-tunnel-mode.md)
</dt> <dt>

[<span data-ttu-id="7aa4c-111">**Filtern von ebenenbezeichgern**</span><span class="sxs-lookup"><span data-stu-id="7aa4c-111">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




