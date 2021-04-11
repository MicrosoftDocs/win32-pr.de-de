---
description: Der PNRP (Peer Name Resolution Protocol)-Namespace Anbieter (NSP) ist eine Server lose namens Auflösungs Technologie, die es Knoten ermöglicht, sich gegenseitig zu ermitteln.
ms.assetid: e11d0f07-f3a0-4c0f-94ce-1d4944a34230
title: Informationen zu PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec402548423ef6baeb15e64a859455fe52332cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131701"
---
# <a name="about-pnrp"></a><span data-ttu-id="6b759-103">Informationen zu PNRP</span><span class="sxs-lookup"><span data-stu-id="6b759-103">About PNRP</span></span>

<span data-ttu-id="6b759-104">Der PNRP (Peer Name Resolution Protocol)-Namespace Anbieter (NSP) ist eine Server lose namens Auflösungs Technologie, die es Knoten ermöglicht, sich gegenseitig zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="6b759-104">The Peer Name Resolution Protocol (PNRP) Namespace Provider (NSP) is a serverless name resolution technology that allows nodes to discover each other.</span></span> <span data-ttu-id="6b759-105">PNRP verwendet die-Namespace Anbieter-API von Winsock 2.</span><span class="sxs-lookup"><span data-stu-id="6b759-105">PNRP uses the Winsock 2 Namespace Provider API.</span></span>

<span data-ttu-id="6b759-106">Die IPv6-Unterstützung ist für PNRP erforderlich und ist das einzige Internet Protokoll, das der API eigen ist.</span><span class="sxs-lookup"><span data-stu-id="6b759-106">IPv6 support is required by PNRP and is the only Internet Protocol native to the API.</span></span> <span data-ttu-id="6b759-107">Allerdings kann PNRP IPv4-Adressen über die IPv6-zu-IPv4-oder [Teredo](/windows/desktop/Teredo/portal) -Übergangs Technologien auflösen.</span><span class="sxs-lookup"><span data-stu-id="6b759-107">However, PNRP can resolve IPv4 addresses via the 6to4 or [Teredo](/windows/desktop/Teredo/portal) transition technologies.</span></span> <span data-ttu-id="6b759-108">Benutzer von Windows XP mit Service Pack 1 (SP1) müssen das [Advanced Networking Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) herunterladen, um die von PNRP benötigte IPv6-Unterstützung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6b759-108">Windows XP with Service Pack 1 (SP1) users must download the [Advanced Networking Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) to enable the IPv6 support required by PNRP.</span></span>

> [!Note]  
> <span data-ttu-id="6b759-109">Anwendungen, die PNRP in einer Umgebung mit einer Firewall verwenden, benötigen Ausnahme Gruppen, die den für die Anwendung spezifischen Port abdecken, sowie den Port "3540-UDP" für PNRP.</span><span class="sxs-lookup"><span data-stu-id="6b759-109">Applications using PNRP in an environment with a firewall require exception groups that cover the port specific to the application, as well as port '3540-UDP' for PNRP.</span></span> <span data-ttu-id="6b759-110">Diese Ausnahme Gruppen sollten immer dann aktiviert werden, wenn die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b759-110">These exception groups should be enabled whenever the application is running.</span></span>

 

<span data-ttu-id="6b759-111">Obwohl PNRP 2,0 auf den Plattformen Windows Vista und Windows Server 2008 einheitlich ist, müssen Windows XP-Benutzer Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) herunterladen, um ein Upgrade auf PNRP 2,0 durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="6b759-111">While PNRP 2.0 is native to the Windows Vista and Windows Server 2008 platforms, Windows XP users must download Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) to upgrade to PNRP 2.0.</span></span>

 

 
