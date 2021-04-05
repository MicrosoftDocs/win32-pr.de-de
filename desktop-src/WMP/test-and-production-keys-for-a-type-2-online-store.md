---
title: Test-und Produktions Schlüssel für einen Typ 2-Online Shop
description: Test-und Produktions Schlüssel für einen Typ 2-Online Shop
ms.assetid: 4fce47e2-d73d-4484-9bda-48257268ed96
keywords:
- Windows Media Player Online Stores, Testschlüssel
- Online Stores, Testschlüssel
- Typ 2 Online Stores, Testschlüssel
- Windows Media Player Online Stores, Produktions Schlüssel
- Online Stores, Produktions Schlüssel
- Typ 2 Online Stores, Produktions Schlüssel
- Windows Media Player Online Stores, serviceingefo-Dokument
- Online Stores, serviceingefo-Dokument
- Typ 2 Online Stores, serviceInfo-Dokument
- Testschlüssel
- Produktions Schlüssel
- Servicinfo-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f009e1b0ca58a66820e193e3b66f8ca50ccadc43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947989"
---
# <a name="test-and-production-keys-for-a-type-2-online-store"></a><span data-ttu-id="5a695-115">Test-und Produktions Schlüssel für einen Typ 2-Online Shop</span><span class="sxs-lookup"><span data-stu-id="5a695-115">Test and Production Keys for a Type 2 Online Store</span></span>

<span data-ttu-id="5a695-116">Wenn Sie mit der Entwicklung Ihres Online Stores beginnen, bietet Microsoft Ihnen zwei numerische Schlüssel: einen Testschlüssel und einen Produktions Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="5a695-116">When you begin development of your online store, Microsoft provides you with two numeric keys: a test key and a production key.</span></span> <span data-ttu-id="5a695-117">Gleichzeitig müssen Sie Microsoft zwei URLs bereitstellen: eines, das auf Ihr Test serviceInfo-Dokument verweist, und eines, das auf Ihr Produktions-serviceInfo-Dokument verweist.</span><span class="sxs-lookup"><span data-stu-id="5a695-117">At the same time, you must provide Microsoft with two URLs: one that points to your test ServiceInfo document and one that points to your production ServiceInfo document.</span></span>

<span data-ttu-id="5a695-118">Während der Entwicklungs-und Testphase ist Ihr Online Store in Windows Media Player nur dann sichtbar, wenn sich Ihr Testschlüssel oder Ihr Produktions Schlüssel in der Registrierung auf dem Computer des Benutzers befindet.</span><span class="sxs-lookup"><span data-stu-id="5a695-118">During the development and testing stage, your online store is visible in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="5a695-119">Wenn sich Ihr Testschlüssel in der Registrierung befindet, ruft Windows Media Player das Test serviceInfo-Dokument ab, das auf das Plug-in, Webseiten und Bilder verweist, die zu Ihrem Test Speicher gehören.</span><span class="sxs-lookup"><span data-stu-id="5a695-119">If your test key is in the registry, Windows Media Player retrieves your test ServiceInfo document, which points to the plug-in, webpages, and images that belong to your test store.</span></span> <span data-ttu-id="5a695-120">Wenn sich Ihr Produktions Schlüssel in der Registrierung befindet, ruft Windows Media Player das Produktions-serviceInfo-Dokument ab, das auf das Plug-in, Webseiten und Images verweist, die zu Ihrem Produktionsspeicher gehören.</span><span class="sxs-lookup"><span data-stu-id="5a695-120">If your production key is in the registry, Windows Media Player retrieves your production ServiceInfo document, which points to the plug-in, webpages, and images that belong to your production store.</span></span>

<span data-ttu-id="5a695-121">Sie können Ihre Test-und Produktionsspeicher in beliebiger Weise verwenden, die Sie nützlich finden.</span><span class="sxs-lookup"><span data-stu-id="5a695-121">You can use your test and production stores in any way you find useful.</span></span> <span data-ttu-id="5a695-122">In der Regel ist der Unterschied jedoch wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5a695-122">Typically, however, the distinction is as follows:</span></span>

-   <span data-ttu-id="5a695-123">Der Test Speicher ist der Ort, an dem Sie tägliche Änderungen an Ihrem Plug-in, Webseiten, Images und anderen Komponenten Ihres Dienstanbieter vornehmen.</span><span class="sxs-lookup"><span data-stu-id="5a695-123">Your test store is the place where you make daily changes to your plug-in, webpages, images, and other components of your service.</span></span>
-   <span data-ttu-id="5a695-124">Der Produktionsspeicher ist der Ort, an dem Sie eine stabile Version Ihres dienplatzes aufbewahren, die Ihr Plug-in, Webseiten, Bilder und andere Komponenten umfasst.</span><span class="sxs-lookup"><span data-stu-id="5a695-124">Your production store is the place where you keep a stable release of your service, which includes your plug-in, webpages, images, and other components.</span></span>

<span data-ttu-id="5a695-125">Bevor der Online Shop in Windows Media Player veröffentlicht werden kann, muss Microsoft überprüfen, ob der Dienst ordnungsgemäß ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a695-125">Before your online store can be published in Windows Media Player, Microsoft must validate that your service performs correctly.</span></span> <span data-ttu-id="5a695-126">Während der Überprüfungsphase verwendet Microsoft ihren Produktions Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="5a695-126">During the validation phase, Microsoft uses your production key.</span></span> <span data-ttu-id="5a695-127">Microsoft verwendet den Testschlüssel während der Überprüfungsphase nicht.</span><span class="sxs-lookup"><span data-stu-id="5a695-127">Microsoft does not use your test key during the validation phase.</span></span>

<span data-ttu-id="5a695-128">Wenn Ihr Onlinespeicher für die Produktion den Überprüfungsprozess erfolgreich abgeschlossen hat, veröffentlicht Microsoft ihren Store. Dies bedeutet, dass Ihr Produktionsspeicher in Windows Media Player für alle Benutzer angezeigt wird, nicht nur für diejenigen, die ihren Produktions Schlüssel in der Registrierung besitzen.</span><span class="sxs-lookup"><span data-stu-id="5a695-128">When your production online store successfully completes the validation process, Microsoft publishes your store, which means that your production store appears in Windows Media Player for all users, not just the ones who have your production key in the registry.</span></span> <span data-ttu-id="5a695-129">Nach der Veröffentlichung des Stores werden die Test-und Produktions Schlüssel nicht mehr benötigt.</span><span class="sxs-lookup"><span data-stu-id="5a695-129">After your store is published, the test and production keys are no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="5a695-130">Benutzer sind möglicherweise in der Lage, den Test-oder Produktions Schlüssel für Ihren Online Shop zu erraten und ihren Store während der Entwicklung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5a695-130">Users might be able to guess the test or production key for your online store and view your store while it is being developed.</span></span> <span data-ttu-id="5a695-131">Sie sollten sorgfältig vorgehen, wenn Sie die Features verfügbar machen möchten, die Sie geheim halten möchten, bis zum öffentlichen Release.</span><span class="sxs-lookup"><span data-stu-id="5a695-131">You should be careful about exposing features that you want to keep secret until public release.</span></span>

 

<span data-ttu-id="5a695-132">Ausführliche Informationen dazu, wo Sie Produktions-und Testschlüssel in der Registrierung des Benutzers platzieren, finden Sie unter [Registrierungsschlüssel und-Einträge für den Online Store vom Typ 2](registry-keys-and-entries-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="5a695-132">For detailed information about where to put your production and test keys in the user's registry, see [Registry Keys and Entries for a Type 2 Online Store](registry-keys-and-entries-for-a-type-2-online-store.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a695-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5a695-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a695-134">**Informationen zu Typ 2 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="5a695-134">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="5a695-135">**Type 2 Online Store-Beispiele**</span><span class="sxs-lookup"><span data-stu-id="5a695-135">**Type 2 Online Store Samples**</span></span>](type-2-online-store-samples.md)
</dt> </dl>

 

 




