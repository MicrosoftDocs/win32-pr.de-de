---
title: Automatisierte Sperrung und Erneuerung von Komponenten
description: Automatisierte Sperrung und Erneuerung von Komponenten
ms.assetid: be4899d7-1d87-4450-8c0e-75cf112ca66a
keywords:
- Windows Media-Format-SDK, automatisierte Sperrung und Verlängerung
- Windows Media-Format-SDK, Widerruf
- SDK für Windows Media-Format, Erneuerung
- Digital Rights Management (DRM), automatisierte Sperrung und Erneuerung
- DRM (Digital Rights Management), automatisierte Sperrung und Erneuerung
- Digital Rights Management (DRM), Sperrung
- DRM (Digital Rights Management), Sperrung
- Digital Rights Management (DRM), Erneuerung
- DRM (Digital Rights Management), Erneuerung
- Erweiterte APIs für den DRM-Client, automatisierte Sperrung und Verlängerung
- Erweiterte Client-APIs, automatisierte Sperrung und Verlängerung
- Erweiterte APIs für den DRM-Client, Sperrung
- Erweiterte Client-APIs, Sperrung
- Erweiterte APIs für den DRM-Client, Erneuerung
- Erweiterte Client-APIs, Erneuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9046d04d8ca7a138a06cba4d26cd82bc5a12b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315999"
---
# <a name="automated-component-revocation-and-renewal"></a><span data-ttu-id="22127-118">Automatisierte Sperrung und Erneuerung von Komponenten</span><span class="sxs-lookup"><span data-stu-id="22127-118">Automated Component Revocation and Renewal</span></span>

<span data-ttu-id="22127-119">Software Anwendungen oder Komponenten, die als kompromittiert angesehen werden, können von Microsoft widerrufen werden.</span><span class="sxs-lookup"><span data-stu-id="22127-119">Software applications or components that are considered compromised can be revoked by Microsoft.</span></span> <span data-ttu-id="22127-120">Die erweiterte API des Windows Media-Format Clients bietet einen Mechanismus für die automatisierte Sperrung und Erneuerung von-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="22127-120">The Windows Media Format Client Extended API provides a mechanism for the automated revocation and renewal of components.</span></span>

<span data-ttu-id="22127-121">Widerrufene Komponenten werden in einer Zertifikat Sperr Liste aufgelistet, die von Microsoft veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="22127-121">Revoked components are listed in a certificate revocation list, which is published by Microsoft.</span></span> <span data-ttu-id="22127-122">Wenn eine Komponente widerrufen wird, wird Ihr Zertifikat der Zertifikat Sperr Liste hinzugefügt, und das Sperr Informations-BLOB (Rev \_ Info) wird auf den Microsoft-Servern aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="22127-122">When a component is revoked, its certificate is added to the certificate revocation list, and the revocation information BLOB (REV\_INFO) is updated on the Microsoft servers.</span></span>

<span data-ttu-id="22127-123">Zum automatischen Sperren und erneuern, wenn ein Benutzer versucht, von Windows Media DRM geschützte Inhalte zu verarbeiten, muss Ihre Anwendung folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="22127-123">To perform automated revocation and renewal when a user attempts to process Windows Media DRM protected content, your application must do the following:</span></span>

1.  <span data-ttu-id="22127-124">Extrahieren Sie die Rev \_ Info-Version aus der Lizenz.</span><span class="sxs-lookup"><span data-stu-id="22127-124">Extract the REV\_INFO version from the license.</span></span> <span data-ttu-id="22127-125">Die Versionsnummer der Rev- \_ Info befindet sich an folgendem Speicherort in einer XMR-Lizenz:</span><span class="sxs-lookup"><span data-stu-id="22127-125">The REV\_INFO version number is located in the following location in an XMR license:</span></span>
    ```C++
    <LICENSE version="2.0.0.0">
        <LICENSORINFO/>
        <DATA>
            <LID>...</LID>
            <KID>...</KID>
            <RevInfoVersion>42</RevInfoVersion>
            ...
         </DATA>
    ....
    </LICENSE>
    ```

    

2.  <span data-ttu-id="22127-126">Vergleichen Sie die \_ Versionsnummer der Rev-Info der Lizenz mit der Versionsnummer der Rev- \_ Info im lokalen Speicher, indem Sie die [**iwmdrmsecurity:: getrevocationdataversion**](iwmdrmsecurity-getrevocationdataversion.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="22127-126">Compare the REV\_INFO version number of the license with the REV\_INFO version number in the local store by calling the [**IWMDRMSecurity::GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) method.</span></span>
3.  <span data-ttu-id="22127-127">Wenn die Rev \_ Info-Version nicht auf dem neuesten Stand ist, rufen Sie die [**iwmdrmsecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) -Methode auf, und übergeben Sie \_ \_ \_ \_ im *dwFlags* -Parameter das Flag für die WMDRM-Sicherheits Ausführung-Sperr Aktualisierung.</span><span class="sxs-lookup"><span data-stu-id="22127-127">If the REV\_INFO version is not up to date, call the [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method, passing the WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH flag in the *dwFlags* parameter.</span></span>
4.  <span data-ttu-id="22127-128">Rufen Sie die Zertifikat Sperr Liste aus dem lokalen Speicher ab, indem Sie die [**iwmdrmsecurity:: getrevocationdata**](iwmdrmsecurity-getrevocationdata.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="22127-128">Retrieve the certificate revocation list from the local store by calling the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>
5.  <span data-ttu-id="22127-129">Analysieren Sie die Sperr Liste, und überprüfen Sie, ob Windows Media DRM-Widerrufungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="22127-129">Parse the revocation list, and check for Windows Media DRM revocations.</span></span> <span data-ttu-id="22127-130">Weitere Informationen finden Sie unter über [Prüfen der Zertifikat](checking-certificate-revocation.md)Sperrung.</span><span class="sxs-lookup"><span data-stu-id="22127-130">For more information, see [Checking Certificate Revocation](checking-certificate-revocation.md).</span></span>
6.  <span data-ttu-id="22127-131">Wenn Windows Media DRM-widerrufen vorhanden sind:</span><span class="sxs-lookup"><span data-stu-id="22127-131">If there are any Windows Media DRM revocations:</span></span>
    1.  <span data-ttu-id="22127-132">Erstellen Sie einen Inhalts-Wegbereiter zum Erneuern der gesperrten Komponenten, indem Sie die [**iwmdrmsecurity:: getcontentenablersforrevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="22127-132">Create a content enabler to renew the revoked components by calling the [**IWMDRMSecurity::GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) method.</span></span>
    2.  <span data-ttu-id="22127-133">Der Aufruf von **imfcontentenabler:: automaticenable** leitet den Benutzer an eine URL weiter, die Informationen zur Erneuerung der Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="22127-133">Call **IMFContentEnabler::AutomaticEnable** which directs the user to a URL that contains component renewal information.</span></span> <span data-ttu-id="22127-134">Diese Methode wird im [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) () dokumentiert https://msdn.microsoft.com/library/ms694197(VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="22127-134">This method is documented in the [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) (https://msdn.microsoft.com/library/ms694197(VS.85).aspx).</span></span>
        > [!Note]  
        > <span data-ttu-id="22127-135">Sie müssen diesen Prozess für den Benutzer durch die Verwendung einer Datenschutzerklärung verdeutlichen, da der Aktualisierungsprozess Informationen vom Client Computer an eine Microsoft-Website sendet.</span><span class="sxs-lookup"><span data-stu-id="22127-135">You must clarify this process to the user through the use of a privacy statement because the update process sends information from the client computer to a Microsoft Web site.</span></span>

         

    3.  <span data-ttu-id="22127-136">Wenn möglich, erneuert der Benutzer die Komponente über die URL, entweder automatisch oder durch Befolgen bestimmter Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="22127-136">If possible, the user will renew the component from the URL, either automatically or by following specific instructions.</span></span> <span data-ttu-id="22127-137">Es gibt Situationen, in denen die Komponente nicht erneuert werden kann.</span><span class="sxs-lookup"><span data-stu-id="22127-137">There will be some situations in which the component cannot be renewed.</span></span>
    4.  <span data-ttu-id="22127-138">Versuchen Sie erneut, auf den Inhalt zuzugreifen, bis keine weiteren widerrufen vorhanden sind oder der Prozess aus irgendeinem Grund angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="22127-138">Try to access the content again until there are no more revocations, or the process is halted for some reason.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22127-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22127-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22127-140">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="22127-140">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 