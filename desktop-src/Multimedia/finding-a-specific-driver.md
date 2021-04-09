---
title: Auffinden eines bestimmten Treibers
description: Auffinden eines bestimmten Treibers
ms.assetid: d48dc313-4606-4f70-b2fe-ed99160e53fc
keywords:
- Audiokomprimierungs-Manager (ACM), suchen nach Treibern
- ACM (Audiokomprimierungs-Manager), suchen nach Treibern
- ACM-Beispiele, Auffinden von Treibern
- Suchen nach Treibern
- acmdriverenum-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d8e8198fdf3bc742c2705e1a83b3ea8036c80f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856755"
---
# <a name="finding-a-specific-driver"></a><span data-ttu-id="96371-108">Auffinden eines bestimmten Treibers</span><span class="sxs-lookup"><span data-stu-id="96371-108">Finding a Specific Driver</span></span>

<span data-ttu-id="96371-109">Möglicherweise möchten Sie, dass Ihre Anwendung eine Nachricht direkt an einen bestimmten Treiber sendet oder bestimmte Treiber aus der Liste identifiziert.</span><span class="sxs-lookup"><span data-stu-id="96371-109">You might want your application to send a message directly to a specific driver or to identify certain drivers from the list.</span></span> <span data-ttu-id="96371-110">Beispielsweise möchten Sie, dass Ihre Anwendung die Treiber identifiziert, die Filter unterstützen, und dann jeden Treiber Abfragen, um zu bestimmen, welche Filter Tags er unterstützt.</span><span class="sxs-lookup"><span data-stu-id="96371-110">For example, you might want your application to identify those drivers that support filters and then query each driver to determine which filter tags it supports.</span></span> <span data-ttu-id="96371-111">Sie können die [**acmdriverenum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) -Funktion verwenden, um ein Handle für die gewünschten Treiber oder Treiber zu erhalten. Dieses Handle kann dann verwendet werden, um mit diesem Treiber zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="96371-111">You can use the [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum) function to obtain a handle to the desired driver or drivers; this handle can then be used to communicate with that driver.</span></span>

<span data-ttu-id="96371-112">Beachten Sie, dass die [**acmdriveradd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) -Funktion ein Treiber handle zurückgibt, das für die Kommunikation mit dem Treiber verwendet werden kann, wenn eine Anwendung einen lokalen Treiber für die eigene Verwendung installiert.</span><span class="sxs-lookup"><span data-stu-id="96371-112">Note that when an application installs a local driver for its own use, the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function returns a driver handle, which can be used to communicate with the driver.</span></span> <span data-ttu-id="96371-113">Es ist in diesem Fall nicht erforderlich, " **acmdriverenum** " zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="96371-113">It is not necessary to use **acmDriverEnum** in this case.</span></span>

 

 




