---
title: Überlegungen zu internationalen Märkten
description: Überlegungen zu internationalen Märkten
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Windows Media Player Online Stores, internationale Märkte
- Online Stores, internationale Märkte
- Typ 1 Online Stores, internationale Märkte
- Typ 2 Online Stores, internationale Märkte
- internationale Märkte
- Windows Media Player Online Stores, serviceingefo-Dokument
- Online Stores, serviceingefo-Dokument
- Typ 1 Online Stores, serviceInfo-Dokument
- Typ 2 Online Stores, serviceInfo-Dokument
- Servicinfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1822e4f647c9967d50d40fa19331cd58565cf2eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338203"
---
# <a name="considerations-for-international-markets"></a><span data-ttu-id="12887-113">Überlegungen zu internationalen Märkten</span><span class="sxs-lookup"><span data-stu-id="12887-113">Considerations for International Markets</span></span>

<span data-ttu-id="12887-114">Wenn Ihr Unternehmen Online-Stores für mehrere Märkte erstellt, müssen Sie Microsoft die URL eines serviceingefo-Dokuments für jeden Markt bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="12887-114">If your company creates online stores for multiple markets, you must provide Microsoft with the URL of a ServiceInfo document for each market.</span></span> <span data-ttu-id="12887-115">Hierfür gibt es zwei Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="12887-115">You can do this one of the following two ways:</span></span>

-   <span data-ttu-id="12887-116">Erstellen Sie ein separates servicinput Info-Dokument für jeden Markt.</span><span class="sxs-lookup"><span data-stu-id="12887-116">Create a separate ServiceInfo document for each market.</span></span> <span data-ttu-id="12887-117">In diesem Fall stellen Sie Microsoft URLs zur Verfügung, die auf einzelne serviceInfo-Dokumente für jeden Online Shop auf jedem Markt zeigen.</span><span class="sxs-lookup"><span data-stu-id="12887-117">In this case, you provide Microsoft with URLs that point to individual ServiceInfo documents for each online store in each market.</span></span>
-   <span data-ttu-id="12887-118">Erstellen Sie ein einzelnes serviceInfo-Dokument für alle Märkte.</span><span class="sxs-lookup"><span data-stu-id="12887-118">Create a single ServiceInfo document for all markets.</span></span> <span data-ttu-id="12887-119">Wenn Sie dies tun, geben Sie Microsoft die gleiche URL für jeden Markt.</span><span class="sxs-lookup"><span data-stu-id="12887-119">When you do this, you provide Microsoft with the same URL for each market.</span></span> <span data-ttu-id="12887-120">Ihr serviceingefo-Dokument, das als ASP-Seite erstellt wurde, kann dann den Speicherort des Benutzers basierend auf Abfrage Zeichenfolgen-Parametern dynamisch erkennen.</span><span class="sxs-lookup"><span data-stu-id="12887-120">Your ServiceInfo document, created as an ASP page, can then dynamically detect the user's location based on query string parameters.</span></span>

<span data-ttu-id="12887-121">Windows Media Player Fügt eine Abfrage Zeichenfolge an die serviceInfo-URL-Anforderung an, die Informationen über die Gebiets Schema-und Standorteinstellungen des Benutzers bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="12887-121">Windows Media Player appends a query string to the ServiceInfo URL request that provides information about the user's locale and location settings.</span></span> <span data-ttu-id="12887-122">Wenn Ihr Online Store diese Informationen verwendet, um zu bestimmen, welche Inhalte angezeigt werden sollen, sollten Sie diese Werte dynamisch an Ihre eigenen URLs in Ihrem serviceInfo-Dokument anfügen.</span><span class="sxs-lookup"><span data-stu-id="12887-122">If your online store uses this information to determine which content to display, you should dynamically append these values to your own URLs in your ServiceInfo document.</span></span> <span data-ttu-id="12887-123">Dies ist die beste Möglichkeit, um sicherzustellen, dass Ihre Webseiten-URLs immer die erwarteten Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="12887-123">This is the best way to ensure that your webpage URLs will always contain the parameters you expect.</span></span>

<span data-ttu-id="12887-124">Nachdem Sie den Speicherort und die Spracheinstellung des Benutzers bestimmt haben, können Sie diese Informationen für zukünftige Sitzungen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="12887-124">Once you have determined the user's location and language preference, you may want to persist this information for future sessions.</span></span> <span data-ttu-id="12887-125">Hierfür können Sie eine der Techniken verwenden, die Sie normalerweise auf einer Webseite verwenden, z. b. Cookies, oder das COM-Objekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="12887-125">You can do this using any of the techniques you would normally use in a webpage, such as cookies, or by using your COM object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12887-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="12887-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12887-127">**Dynamisches Erstellen des serviceingefo-Dokuments**</span><span class="sxs-lookup"><span data-stu-id="12887-127">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="12887-128">**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**</span><span class="sxs-lookup"><span data-stu-id="12887-128">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="12887-129">**Servicinput info-Element**</span><span class="sxs-lookup"><span data-stu-id="12887-129">**ServiceInfo Element**</span></span>](serviceinfo-element.md)
</dt> </dl>

 

 




