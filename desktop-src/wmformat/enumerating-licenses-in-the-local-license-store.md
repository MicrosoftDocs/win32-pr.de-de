---
title: Auflisten von Lizenzen im lokalen Lizenz Speicher
description: Auflisten von Lizenzen im lokalen Lizenz Speicher
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Windows Media-Format-SDK, Auflisten von Lizenzen
- Windows Media-Format-SDK, Lizenzen
- Windows Media-Format-SDK, lokaler Lizenz Speicher
- Digital Rights Management (DRM), Auflisten von Lizenzen
- DRM (Digital Rights Management), Auflisten von Lizenzen
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), lokaler Lizenz Speicher
- DRM (Digital Rights Management), lokaler Lizenz Speicher
- Erweiterte APIs für den DRM-Client, Auflisten von Lizenzen
- Erweiterte Client-APIs, Auflisten von Lizenzen
- Erweiterte APIs für den DRM-Client, Lizenzen
- Erweiterte Client-APIs, Lizenzen
- Erweiterte APIs für den DRM-Client, lokaler Lizenz Speicher
- Erweiterte Client-APIs, lokaler Lizenz Speicher
- Lizenzen, auflisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b1384e08a6789fedca9704f36ad8da1e31b4ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388127"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a><span data-ttu-id="e0386-119">Auflisten von Lizenzen im lokalen Lizenz Speicher</span><span class="sxs-lookup"><span data-stu-id="e0386-119">Enumerating Licenses in the Local License Store</span></span>

<span data-ttu-id="e0386-120">Die Enumeration ist ein Prozess zum erhalten von Informationen zu den Lizenzen im lokalen Lizenz Speicher, indem Sie nacheinander nacheinander durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="e0386-120">Enumeration is a process of getting information about the licenses in the local license store, by stepping through them one by one.</span></span> <span data-ttu-id="e0386-121">Sie können eine Lizenzierungs Enumeration erstellen, indem Sie die [**iwmdrmlicenaberation**](iwmdrmlicensemanagement-createlicenseenumeration.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e0386-121">You can create a license enumeration by calling the [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).</span></span>

<span data-ttu-id="e0386-122">Der häufigste Grund für das Auflisten von Lizenzen im Speicher ist das Auffinden einer bestimmten Lizenz für das Entschlüsseln einiger Inhalte.</span><span class="sxs-lookup"><span data-stu-id="e0386-122">The most common reason for enumerating through licenses in the store is to find a particular license for decryption of some content.</span></span>

<span data-ttu-id="e0386-123">Die [**iwmdrmlicense**](iwmdrmlicense.md) -Schnittstelle dient sowohl als Portal für die einzelnen Lizenz Ergebnisse als auch als Enumerator.</span><span class="sxs-lookup"><span data-stu-id="e0386-123">The [**IWMDRMLicense**](iwmdrmlicense.md) interface serves as both a portal to the individual license results and as the enumerator.</span></span> <span data-ttu-id="e0386-124">Wenn die Lizenz-Enumeration erstellt wird, wird die erste Lizenz in der Liste in die **iwmdrmlicense** -Schnittstelle geladen.</span><span class="sxs-lookup"><span data-stu-id="e0386-124">When the license enumeration is created, the first license in the list is loaded into the **IWMDRMLicense** interface.</span></span> <span data-ttu-id="e0386-125">Die meisten Methoden von **iwmdrmlicense** ermöglichen es Ihnen, Informationen über die Lizenz zu erhalten oder Objekte zu erstellen, um Inhalte basierend auf der Lizenz zu verschlüsseln oder zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="e0386-125">Most of the methods of **IWMDRMLicense** enable you to get information about the license or to create objects to encrypt or decrypt content based on the license.</span></span> <span data-ttu-id="e0386-126">Es gibt jedoch zwei Methoden, die die Enumeration steuern: [**GetNext**](iwmdrmlicense-getnext.md) und [**resstenumeration**](iwmdrmlicense-resetenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="e0386-126">However, there are two methods that control the enumeration: [**GetNext**](iwmdrmlicense-getnext.md) and [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md).</span></span> <span data-ttu-id="e0386-127">**GetNext** lädt die nächste Lizenz in der Liste in die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e0386-127">**GetNext** loads the next license in the list into the interface.</span></span> <span data-ttu-id="e0386-128">**Resegtenumeration** gibt die Enumeration in den Zustand zurück, in dem Sie sich bei der ersten Erstellung befand.</span><span class="sxs-lookup"><span data-stu-id="e0386-128">**ResetEnumeration** returns the enumeration to the state it was in when it was first created.</span></span> <span data-ttu-id="e0386-129">Wenn die Enumeration zurückgesetzt wird, wird die erste Lizenz in der Liste wieder in die **iwmdrmlicense** -Schnittstelle geladen.</span><span class="sxs-lookup"><span data-stu-id="e0386-129">When the enumeration is reset, the first license in the list is loaded back into the **IWMDRMLicense** interface.</span></span>

<span data-ttu-id="e0386-130">Wenn Sie die letzte Lizenz in der Liste erreicht haben, gibt der nächste **GetNext** -Befehl \_ einen Fehler ohne \_ Weitere Elemente zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="e0386-130">When you have reached the last license in the list, the next call to **GetNext** returns ERROR\_NO\_MORE\_ITEMS.</span></span>

<span data-ttu-id="e0386-131">Wenn Ihre Anwendung eine Aktion mit dem von DRM behandelten Inhalt ausführt, sollten Sie die Lizenzen im lokalen Lizenz Speicher auf die Rechte und auf andere einschränkende Faktoren (z. b. Ausgabe Schutz Ebenen) überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e0386-131">If your application performs an action with the content that is covered by DRM, you should check the licenses in the local license store for the rights and for other limiting factors, such as output protection levels (OPLs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0386-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0386-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0386-133">**Informationen aus Lizenzen im lokalen Lizenz Speicher erhalten**</span><span class="sxs-lookup"><span data-stu-id="e0386-133">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




