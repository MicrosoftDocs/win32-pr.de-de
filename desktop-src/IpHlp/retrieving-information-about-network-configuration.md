---
description: IP-Hilfsobjekt enthält Informationen zur Netzwerkkonfiguration des lokalen Computers.
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: Abrufen von Informationen zur Netzwerkkonfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a6860b329ba7c69575be1dfeaaa2e19c57558f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960645"
---
# <a name="retrieving-information-about-network-configuration"></a><span data-ttu-id="480e0-103">Abrufen von Informationen zur Netzwerkkonfiguration</span><span class="sxs-lookup"><span data-stu-id="480e0-103">Retrieving Information About Network Configuration</span></span>

<span data-ttu-id="480e0-104">IP-Hilfsobjekt enthält Informationen zur Netzwerkkonfiguration des lokalen Computers.</span><span class="sxs-lookup"><span data-stu-id="480e0-104">IP Helper provides information about the network configuration of the local computer.</span></span> <span data-ttu-id="480e0-105">Um allgemeine Konfigurationsinformationen abzurufen, verwenden Sie die [**getnetworkparameams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="480e0-105">To retrieve general configuration information, use the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) function.</span></span> <span data-ttu-id="480e0-106">Diese Funktion gibt Informationen zurück, die nicht spezifisch für einen bestimmten Adapter oder eine bestimmte Schnittstelle sind.</span><span class="sxs-lookup"><span data-stu-id="480e0-106">This function returns information that is not specific to a particular adapter or interface.</span></span> <span data-ttu-id="480e0-107">Beispielsweise gibt **getnetworkparameams** eine Liste der DNS-Server zurück, die vom lokalen Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="480e0-107">For example, **GetNetworkParams** returns a list of the DNS servers that are used by the local computer.</span></span>

-   <span data-ttu-id="480e0-108">Codebeispiele, die [**getnetworkparser**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) betreffen, finden [Sie unter Abrufen von Informationen mithilfe von getnetworkpara](retrieving-information-using-getnetworkparams.md)Metern.</span><span class="sxs-lookup"><span data-stu-id="480e0-108">For code samples involving [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) see [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md).</span></span>

 

 



