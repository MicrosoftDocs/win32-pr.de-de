---
title: Enumerationstypen für Microsoft Windows Media DRM-Clients
description: Enumerationstypen
ms.assetid: 940f66e1-1dc1-414f-bba9-b91f4f0dfc45
keywords:
- Windows Media-Format-SDK, Enumerationstypen
- Digital Rights Management (DRM), Enumerationstypen
- DRM (Digital Rights Management), Enumerationstypen
- Erweiterte APIs des DRM-Clients, Enumerationstypen
- Erweiterte Client-APIs, Enumerationstypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159342367035767d213d57987d93d23eb321a6c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039969"
---
# <a name="microsoft-windows-media-drm-client-enumeration-types"></a><span data-ttu-id="54cb9-108">Enumerationstypen für Microsoft Windows Media DRM-Clients</span><span class="sxs-lookup"><span data-stu-id="54cb9-108">Microsoft Windows Media DRM Client Enumeration Types</span></span>

<span data-ttu-id="54cb9-109">In der folgenden Tabelle werden die Enumerationen beschrieben, die von den erweiterten APIs des Microsoft Windows Media DRM-Clients unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="54cb9-109">The following table describes the enumerations that are supported by the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="54cb9-110">Enumeration</span><span class="sxs-lookup"><span data-stu-id="54cb9-110">Enumeration</span></span>                                                                      | <span data-ttu-id="54cb9-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54cb9-111">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54cb9-112">**\_ \_ zulässige \_ \_ Ergebnisse der DRM-Aktion**</span><span class="sxs-lookup"><span data-stu-id="54cb9-112">**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**</span></span>](drm-action-allowed-query-results.md) | <span data-ttu-id="54cb9-113">Wird von der [**iwmdrmlicensequery:: queryAction Allowed**](iwmdrmlicensequery-queryactionallowed.md) -Schnittstelle verwendet, um den Grund anzugeben, warum eine Aktion nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="54cb9-113">Used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span> |
| [<span data-ttu-id="54cb9-114">**DRM- \_ attr- \_ Datentyp**</span><span class="sxs-lookup"><span data-stu-id="54cb9-114">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)                                 | <span data-ttu-id="54cb9-115">Definiert die Datentypen, die für DRM-Attribute und-Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54cb9-115">Defines the data types used for DRM attributes and properties.</span></span>                                                                                                |
| [<span data-ttu-id="54cb9-116">**DRM- \_ Crypto- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="54cb9-116">**DRM\_CRYPTO\_TYPE**</span></span>](drm-crypto-type.md)                                     | <span data-ttu-id="54cb9-117">Definiert die kryptografiealgorithmustypen, die zum Verschlüsseln von Inhalten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="54cb9-117">Defines the cryptographic algorithm types that can be used to encrypt content.</span></span>                                                                                |
| [<span data-ttu-id="54cb9-118">**DRM- \_ http- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="54cb9-118">**DRM\_HTTP\_STATUS**</span></span>](drmdrm-http-status.md)                                  | <span data-ttu-id="54cb9-119">Definiert einen Bereich von http-Zuständen für eine DRM-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="54cb9-119">Defines a range of HTTP states for a DRM request.</span></span>                                                                                                             |
| [<span data-ttu-id="54cb9-120">**DRM- \_ Individualisierungs \_ Status**</span><span class="sxs-lookup"><span data-stu-id="54cb9-120">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drmdrm-individualization-status.md)        | <span data-ttu-id="54cb9-121">Definiert die gültigen Zustände für die DRM-Individualisierung.</span><span class="sxs-lookup"><span data-stu-id="54cb9-121">Defines the valid states for DRM individualization.</span></span>                                                                                                           |
| [<span data-ttu-id="54cb9-122">**DRM- \_ Lizenz \_ Zustands \_ Kategorie**</span><span class="sxs-lookup"><span data-stu-id="54cb9-122">**DRM\_LICENSE\_STATE\_CATEGORY**</span></span>](drmdrm-license-state-category.md)           | <span data-ttu-id="54cb9-123">Gibt den Typ der Lizenz Beschränkung an, der durch eine [**DRM- \_ Lizenz \_ Zustands \_ Daten**](drmdrm-license-state-data.md) Struktur beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="54cb9-123">Specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>                    |
| [<span data-ttu-id="54cb9-124">**msdrm- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="54cb9-124">**MSDRM\_STATUS**</span></span>](msdrm-status.md)                                            | <span data-ttu-id="54cb9-125">Definiert Status Bedingungen für das DRM-Subsystem.</span><span class="sxs-lookup"><span data-stu-id="54cb9-125">Defines status conditions for the DRM subsystem.</span></span>                                                                                                              |
| [<span data-ttu-id="54cb9-126">**wmdrmnet \_ - \_ Richtlinientyp**</span><span class="sxs-lookup"><span data-stu-id="54cb9-126">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)                           | <span data-ttu-id="54cb9-127">Listet die Typen von Richtlinien auf, die für Windows Media DRM für Netzwerkgeräte Vorgänge verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="54cb9-127">Lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>                                                          |
| [<span data-ttu-id="54cb9-128">**WMT- \_ Rechte**</span><span class="sxs-lookup"><span data-stu-id="54cb9-128">**WMT\_RIGHTS**</span></span>](drm-wmt-rights.md)                                            | <span data-ttu-id="54cb9-129">Definiert die Rechte, die in einer DRM-Lizenz angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="54cb9-129">Defines the rights that may be specified in a DRM license.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="54cb9-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="54cb9-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54cb9-131">**Programmierverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="54cb9-131">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




