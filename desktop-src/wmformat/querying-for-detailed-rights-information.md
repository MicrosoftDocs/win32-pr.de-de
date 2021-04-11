---
title: Abfragen ausführlicher Rechte Informationen
description: Abfragen ausführlicher Rechte Informationen
ms.assetid: d9d5c299-1f61-41df-ab2c-7f4d196e9290
keywords:
- Windows Media-Format-SDK, Abfragen detaillierter Rechte
- Windows Media-Format-SDK, ausführliche Rechte Abfragen
- Digital Rights Management (DRM), Abfragen detaillierter Rechte
- DRM (Digital Rights Management), Abfragen detaillierter Rechte
- Digital Rights Management (DRM), ausführliche Rechte Abfragen
- DRM (Digital Rights Management), ausführliche Rechte Abfragen
- Erweiterte APIs für den DRM-Client, Abfragen detaillierter Rechte
- Erweiterte Client-APIs, Abfragen detaillierter Rechte
- Erweiterte APIs für den DRM-Client, ausführliche Rechte Abfragen
- Erweiterte Client-APIs, ausführliche Rechte Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a21fa974f0289c4e4e8983ee6d4fd1757de824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206859"
---
# <a name="querying-for-detailed-rights-information"></a><span data-ttu-id="fdae5-113">Abfragen ausführlicher Rechte Informationen</span><span class="sxs-lookup"><span data-stu-id="fdae5-113">Querying for Detailed Rights Information</span></span>

<span data-ttu-id="fdae5-114">Mithilfe der [**iwmdrmlicensequery:: querylicenserstate**](iwmdrmlicensequery-querylicensestate.md) -Methode können Sie ausführliche Informationen zu den von den Lizenzen gewährten Rechten für eine Schlüssel-ID abrufen.</span><span class="sxs-lookup"><span data-stu-id="fdae5-114">By using the [**IWMDRMLicenseQuery::QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) method, you can obtain detailed information about the rights granted by licenses for a key ID.</span></span> <span data-ttu-id="fdae5-115">Die Informationen, die Sie von dieser Methode erhalten, werden von allen Lizenzen im lokalen Lizenz Speicher aggregiert, die auf die angegebene Schlüssel-ID angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdae5-115">The information that you get from this method is aggregated from all licenses in the local license store that apply to the specified key ID.</span></span>

<span data-ttu-id="fdae5-116">**Querylicenserstate** verwendet die [**DRM- \_ Lizenz \_ Zustands \_ Daten**](drmdrm-license-state-data.md) Struktur, um aggregierte Informationen zu allen Lizenzen für die angegebene Schlüssel-ID anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fdae5-116">**QueryLicenseState** uses the [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure to display aggregate information about all the licenses for the specified key ID.</span></span> <span data-ttu-id="fdae5-117">Diese Verwendung unterscheidet sich von anderen Objekten im Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="fdae5-117">This usage is different than by other objects in the Windows Media Format SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdae5-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fdae5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdae5-119">**Informationen aus Lizenzen im lokalen Lizenz Speicher erhalten**</span><span class="sxs-lookup"><span data-stu-id="fdae5-119">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




