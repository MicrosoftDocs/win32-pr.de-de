---
title: NDF-Schnittstellen
description: Die folgenden Schnittstellen können verwendet werden, um die Funktionalität von Microsoft-Hilfsklassen zu erweitern, die als erweiterbar identifiziert werden.
ms.assetid: 55e58eb8-d04e-4398-a892-8c343a88adc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fac7b53329f8d157382f1c68df34d1b0e663327
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036235"
---
# <a name="ndf-interfaces"></a><span data-ttu-id="e6f24-103">NDF-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e6f24-103">NDF Interfaces</span></span>

<span data-ttu-id="e6f24-104">Die folgenden Schnittstellen können verwendet werden, um die Funktionalität von Microsoft-Hilfsklassen zu erweitern, die als erweiterbar identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="e6f24-104">The following interfaces can be used to extend the functionality of Microsoft Helper Classes that are identified as extensible.</span></span> <span data-ttu-id="e6f24-105">Obwohl diese Funktionalität für die meisten Anwendungen nicht erforderlich ist, kann Sie in einigen Fällen spezifischere Diagnosen und Auflösungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e6f24-105">Although this functionality is not required for most applications, it can provide more specific diagnoses and resolutions in some cases.</span></span>

> [!Note]  
> <span data-ttu-id="e6f24-106">Diese Schnittstellen und die zugehörigen Methoden sind für Entwickler konzipiert, die ihre eigenen Hilfsklassen von Drittanbietern implementieren, die die NDF-Funktionalität erweitern.</span><span class="sxs-lookup"><span data-stu-id="e6f24-106">These interfaces and their associated methods are for developers implementing their own third party helper classes that extend NDF functionality.</span></span>

 



| <span data-ttu-id="e6f24-107">Schnittstellenname</span><span class="sxs-lookup"><span data-stu-id="e6f24-107">Interface Name</span></span>                                                 | <span data-ttu-id="e6f24-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6f24-108">Description</span></span>                                                                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6f24-109">**Inetdiaghelper**</span><span class="sxs-lookup"><span data-stu-id="e6f24-109">**INetDiagHelper**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper)                       | <span data-ttu-id="e6f24-110">Wird von der NDF für die meisten Aktivitäten aufgerufen, die während einer Diagnose auftreten.</span><span class="sxs-lookup"><span data-stu-id="e6f24-110">Called by the NDF for most activities that occur during a diagnosis.</span></span>                                                     |
| [<span data-ttu-id="e6f24-111">**Inetdiaghelperex**</span><span class="sxs-lookup"><span data-stu-id="e6f24-111">**INetDiagHelperEx**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperex)                   | <span data-ttu-id="e6f24-112">Wird von der NDF aufgerufen, um Informationen zu Diagnosen und zur Behebung von netzwerkbezogenen Problemen zu erfassen und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e6f24-112">Called by the NDF to capture and provide information associated with diagnoses and resolution of network-related issues.</span></span> |
| [<span data-ttu-id="e6f24-113">**Inetdiaghelperinfo**</span><span class="sxs-lookup"><span data-stu-id="e6f24-113">**INetDiagHelperInfo**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo)               | <span data-ttu-id="e6f24-114">Wird von der NDF aufgerufen, um zu überprüfen, ob Sie über erforderliche Informationen verfügt</span><span class="sxs-lookup"><span data-stu-id="e6f24-114">Called by the NDF to validate that it has required information</span></span>                                                           |
| [<span data-ttu-id="e6f24-115">**Inetdiaghelperutilfactory**</span><span class="sxs-lookup"><span data-stu-id="e6f24-115">**INetDiagHelperUtilFactory**</span></span>](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperutilfactory) | <span data-ttu-id="e6f24-116">Ist für das System reserviert.</span><span class="sxs-lookup"><span data-stu-id="e6f24-116">Reserved for system use.</span></span>                                                                                                 |



 

 

 




