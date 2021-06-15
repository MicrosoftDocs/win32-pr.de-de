---
title: Microsoft Windows Media DRM-Clientenumerationstypen
description: Erfahren Sie mehr über die Enumerationen, die von den erweiterten APIs des Microsoft Windows Media DRM-Clients unterstützt werden.
ms.assetid: 940f66e1-1dc1-414f-bba9-b91f4f0dfc45
keywords:
- Windows Media Format SDK, Enumerationstypen
- Digital Rights Management (DRM), Enumerationstypen
- DRM (Digital Rights Management), Enumerationstypen
- ERWEITERTE APIs des DRM-Clients, Enumerationstypen
- Erweiterte Client-APIs, Enumerationstypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574136f8016161f4d2c208865a72ad2a86d98f68
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068427"
---
# <a name="microsoft-windows-media-drm-client-enumeration-types"></a><span data-ttu-id="be741-108">Microsoft Windows Media DRM-Clientenumerationstypen</span><span class="sxs-lookup"><span data-stu-id="be741-108">Microsoft Windows Media DRM Client Enumeration Types</span></span>

<span data-ttu-id="be741-109">In der folgenden Tabelle werden die Enumerationen beschrieben, die von den erweiterten APIs des Microsoft Windows Media DRM-Clients unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="be741-109">The following table describes the enumerations that are supported by the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="be741-110">Enumeration</span><span class="sxs-lookup"><span data-stu-id="be741-110">Enumeration</span></span>                                                                      | <span data-ttu-id="be741-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be741-111">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be741-112">**ZULÄSSIGE \_ ABFRAGEERGEBNISSE \_ DER \_ DRM-AKTION \_**</span><span class="sxs-lookup"><span data-stu-id="be741-112">**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**</span></span>](drm-action-allowed-query-results.md) | <span data-ttu-id="be741-113">Wird von [**der IWMDRMLicenseQuery::QueryActionAllowed-Schnittstelle**](iwmdrmlicensequery-queryactionallowed.md) verwendet, um den Grund anzugeben, aus dem eine Aktion nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="be741-113">Used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span> |
| [<span data-ttu-id="be741-114">**DRM \_ \_ ATTR-DATENTYP**</span><span class="sxs-lookup"><span data-stu-id="be741-114">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)                                 | <span data-ttu-id="be741-115">Definiert die Datentypen, die für DRM-Attribute und -Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be741-115">Defines the data types used for DRM attributes and properties.</span></span>                                                                                                |
| [<span data-ttu-id="be741-116">**DRM \_ CRYPTO \_ TYPE**</span><span class="sxs-lookup"><span data-stu-id="be741-116">**DRM\_CRYPTO\_TYPE**</span></span>](drm-crypto-type.md)                                     | <span data-ttu-id="be741-117">Definiert die Kryptografiealgorithmustypen, die zum Verschlüsseln von Inhalten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="be741-117">Defines the cryptographic algorithm types that can be used to encrypt content.</span></span>                                                                                |
| [<span data-ttu-id="be741-118">**\_DRM-HTTP-STATUS \_**</span><span class="sxs-lookup"><span data-stu-id="be741-118">**DRM\_HTTP\_STATUS**</span></span>](drmdrm-http-status.md)                                  | <span data-ttu-id="be741-119">Definiert einen Bereich von HTTP-Zuzuständen für eine DRM-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="be741-119">Defines a range of HTTP states for a DRM request.</span></span>                                                                                                             |
| [<span data-ttu-id="be741-120">**\_DRM-INDIVIDUALISIERUNGSSTATUS \_**</span><span class="sxs-lookup"><span data-stu-id="be741-120">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drmdrm-individualization-status.md)        | <span data-ttu-id="be741-121">Definiert die gültigen Zustände für die DRM-Individualisierung.</span><span class="sxs-lookup"><span data-stu-id="be741-121">Defines the valid states for DRM individualization.</span></span>                                                                                                           |
| [<span data-ttu-id="be741-122">**\_ \_ DRM-LIZENZSTATUSKATEGORIE \_**</span><span class="sxs-lookup"><span data-stu-id="be741-122">**DRM\_LICENSE\_STATE\_CATEGORY**</span></span>](drmdrm-license-state-category.md)           | <span data-ttu-id="be741-123">Gibt den Typ der Lizenzeinschränkung an, der von einer [**DRM \_ LICENSE STATE \_ \_ DATA-Struktur beschrieben**](drmdrm-license-state-data.md) wird.</span><span class="sxs-lookup"><span data-stu-id="be741-123">Specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>                    |
| [<span data-ttu-id="be741-124">**MSDRM-STATUS \_**</span><span class="sxs-lookup"><span data-stu-id="be741-124">**MSDRM\_STATUS**</span></span>](msdrm-status.md)                                            | <span data-ttu-id="be741-125">Definiert Statusbedingungen für das DRM-Subsystem.</span><span class="sxs-lookup"><span data-stu-id="be741-125">Defines status conditions for the DRM subsystem.</span></span>                                                                                                              |
| [<span data-ttu-id="be741-126">**WMDRMNET-RICHTLINIENTYP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be741-126">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)                           | <span data-ttu-id="be741-127">Listet die Arten von Richtlinien auf, die für Windows Media DRM für Netzwerkgerätevorgänge verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="be741-127">Lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>                                                          |
| [<span data-ttu-id="be741-128">**\_WMT-RECHTE**</span><span class="sxs-lookup"><span data-stu-id="be741-128">**WMT\_RIGHTS**</span></span>](drm-wmt-rights.md)                                            | <span data-ttu-id="be741-129">Definiert die Rechte, die in einer DRM-Lizenz angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="be741-129">Defines the rights that may be specified in a DRM license.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="be741-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be741-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be741-131">**Programmierverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="be741-131">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




