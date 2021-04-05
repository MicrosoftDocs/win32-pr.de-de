---
title: Implementieren der Lizenz Sperrung
description: Implementieren der Lizenz Sperrung
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- Windows Media-Format-SDK, Implementieren der Lizenz Sperrung
- Windows Media-Format-SDK, Lizenz Sperrung
- Windows Media-Format-SDK, Sperren von Lizenzen
- Advanced Systems Format (ASF), Implementieren der Lizenz Sperrung
- ASF (Advanced Systems Format), Implementieren der Lizenz Sperrung
- Advanced Systems Format (ASF), Lizenz Sperrung
- ASF (Advanced Systems Format), Lizenz Sperrung
- Advanced Systems Format (ASF), Widerruf von Lizenzen
- ASF (Advanced Systems Format), Sperrung von Lizenzen
- Digital Rights Management (DRM), Implementieren der Lizenz Sperrung
- DRM (Digital Rights Management), Implementieren der Lizenz Sperrung
- Digital Rights Management (DRM), Lizenz Sperrung
- DRM (Digital Rights Management), Lizenz Sperrung
- Digital Rights Management (DRM), Sperren von Lizenzen
- DRM (Digital Rights Management), Sperren von Lizenzen
- Lizenz Sperrung, implementieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83bfb1a512b031f5b7c297ecede4ed33fba8f2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723568"
---
# <a name="implementing-license-revocation"></a><span data-ttu-id="354a2-119">Implementieren der Lizenz Sperrung</span><span class="sxs-lookup"><span data-stu-id="354a2-119">Implementing License Revocation</span></span>

<span data-ttu-id="354a2-120">Das Windows Media Rights Manager 10 SDK enthält eine Funktion mit dem Namen "Lizenz Sperrung".</span><span class="sxs-lookup"><span data-stu-id="354a2-120">The Windows Media Rights Manager 10 SDK includes a feature called license revocation.</span></span> <span data-ttu-id="354a2-121">Mit dieser Funktion können Lizenzserver anfordern, dass Lizenzen vom Client Computer entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="354a2-121">This feature enables license servers to request that licenses be removed from the client computer.</span></span> <span data-ttu-id="354a2-122">Das Windows Media-Format-SDK stellt Methoden bereit, mit denen Sperr Nachrichten verarbeitet und die Lizenzen aus dem lokalen Lizenz Speicher entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="354a2-122">The Windows Media Format SDK provides methods that process revocation messages and remove the licenses from the local license store.</span></span>

<span data-ttu-id="354a2-123">Der Lizenz Sperrprozess wird von einem Dienst initiiert, der vom Lizenz Aussteller bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="354a2-123">The license revocation process is initiated by a service provided by the license issuer.</span></span> <span data-ttu-id="354a2-124">Die Anwendung kann diesen Dienst hosten, oder Sie kann eine Webanwendung sein.</span><span class="sxs-lookup"><span data-stu-id="354a2-124">Your application can host this service, or it can be a Web application.</span></span> <span data-ttu-id="354a2-125">In beiden Fällen muss Ihre Anwendung in der Lage sein, eine vom Dienst erstellte Lizenz Herausforderung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="354a2-125">In either case, your application must be able to receive a license challenge created by the service.</span></span>

<span data-ttu-id="354a2-126">Um Lizenzen aus dem Lizenz Speicher zu entfernen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="354a2-126">To remove licenses from the license store, perform the following steps:</span></span>

1.  <span data-ttu-id="354a2-127">Wenn Sie eine Lizenzanfrage vom Lizenz Aussteller erhalten haben, rufen Sie die [**wmfeatelicenserevocationagent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) -Funktion auf, um ein Lizenz Sperr-Agent-Objekt zu erstellen und einen Zeiger auf die [**iwmlicenserevocationagent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="354a2-127">Upon receiving a license challenge from the license issuer, call the [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) function to create a license revocation agent object and obtain a pointer to the [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) interface.</span></span>
2.  <span data-ttu-id="354a2-128">Rufen Sie die [**iwmlicenserevocationagent:: getlrbchallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) -Methode auf, um die Abfrage Antwort zu generieren.</span><span class="sxs-lookup"><span data-stu-id="354a2-128">Call the [**IWMLicenseRevocationAgent::GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) method to generate the challenge response.</span></span>
3.  <span data-ttu-id="354a2-129">Senden Sie die Abfrage Antwort zurück an die Lizenz Dienst Komponente, von der Sie die Herausforderung erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="354a2-129">Send the challenge response back to the license service component from which you received the challenge.</span></span>
4.  <span data-ttu-id="354a2-130">Die Lizenz Dienst Komponente sendet ein signiertes Lizenz Sperr-BLOB (LRB) an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="354a2-130">The license service component sends a signed license revocation blob (LRB) to your application.</span></span> <span data-ttu-id="354a2-131">Wenn Sie Sie empfangen, nennen Sie die [**iwmlicenserevocationagent::P rocess LRB**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) -Methode.</span><span class="sxs-lookup"><span data-stu-id="354a2-131">When you receive it, call the [**IWMLicenseRevocationAgent::ProcessLRB**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) method.</span></span> <span data-ttu-id="354a2-132">**Processlrb** erstellt eine Bestätigungsnachricht, die Sie zurück an den Lizenz Dienst senden müssen, um zu überprüfen, ob die Lizenzen entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="354a2-132">**ProcessLRB** creates an acknowledgement message that you must send back to the license service to verify that the licenses were removed.</span></span>

> [!Note]  
> <span data-ttu-id="354a2-133">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="354a2-133">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="354a2-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="354a2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="354a2-135">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="354a2-135">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="354a2-136">**Iwmlicenserevocationagent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="354a2-136">**IWMLicenseRevocationAgent Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 




