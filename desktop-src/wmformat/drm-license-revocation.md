---
title: Lizenz Sperrung (Microsoft Windows Media DRM-Client)
description: Lizenz Sperrung (Microsoft Windows Media DRM-Client)
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- Windows Media-Format-SDK, Lizenzen
- Windows Media-Format-SDK, Lizenz Sperrung
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), Lizenz Sperrung
- DRM (Digital Rights Management), Lizenz Sperrung
- Erweiterte APIs für den DRM-Client, Lizenzen
- Erweiterte Client-APIs, Lizenzen
- Erweiterte APIs für den DRM-Client, Lizenz Sperrung
- Erweiterte Client-APIs, Lizenz Sperrung
- Lizenzen, Sperren
- Lizenz Sperrung, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90388a7392c79f583143e06fb78ecfe45e188612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218928"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a><span data-ttu-id="20b31-115">Lizenz Sperrung (Microsoft Windows Media DRM-Client)</span><span class="sxs-lookup"><span data-stu-id="20b31-115">License Revocation (Microsoft Windows Media DRM Client)</span></span>

<span data-ttu-id="20b31-116">Der Lizenz Widerruf bezieht sich auf das Entfernen von Lizenzen aus einem lokalen Lizenz Speicher.</span><span class="sxs-lookup"><span data-stu-id="20b31-116">License revocation refers to the removal of licenses from a local license store.</span></span> <span data-ttu-id="20b31-117">Ein häufiges Szenario für die Lizenz Sperrung tritt auf, wenn ein Dienstanbieter, z. b. ein Musik Abonnement Dienst, den Dienst auf dem Computer eines Benutzers deaktivieren muss.</span><span class="sxs-lookup"><span data-stu-id="20b31-117">A common scenario for license revocation occurs when a service provider, such as a music subscription service, must deactivate the service on a user's computer.</span></span>

<span data-ttu-id="20b31-118">Der Lizenz Sperrprozess wird von einem Dienst initiiert, der vom Lizenz Aussteller bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="20b31-118">The license revocation process is initiated by a service provided by the license issuer.</span></span> <span data-ttu-id="20b31-119">Die Anwendung kann diesen Dienst hosten, oder es kann eine Webanwendung sein.</span><span class="sxs-lookup"><span data-stu-id="20b31-119">Your application can host this service or it can be a Web application.</span></span> <span data-ttu-id="20b31-120">In beiden Fällen muss Ihre Anwendung in der Lage sein, eine vom Dienst erstellte Lizenz Herausforderung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="20b31-120">In either case, your application must be able to receive a license challenge created by the service.</span></span>

<span data-ttu-id="20b31-121">Gehen Sie folgendermaßen vor, um Lizenzen aus dem Lizenz Speicher zu entfernen:</span><span class="sxs-lookup"><span data-stu-id="20b31-121">To remove licenses from the license store, do the following:</span></span>

1.  <span data-ttu-id="20b31-122">Erstellen Sie nach dem Empfang einer Lizenzanfrage vom Lizenz Aussteller eine Sperranforderung mithilfe der Methode [**iwmdrmlicencmanagement:: featelicenserevocationchallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) .</span><span class="sxs-lookup"><span data-stu-id="20b31-122">Upon receiving a license challenge from the license issuer, create a revocation challenge using the [**IWMDRMLicenseManagement::CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) method.</span></span> <span data-ttu-id="20b31-123">Diese Methode weist einen Puffer zu, der Sperr Aufforderungs Daten enthält, die über den Parameter *ppbdeleggeoutput* an die Anwendung übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="20b31-123">This method will allocate a buffer containing a revocation challenge data, which is passed to your application through the *ppbChallengeOutput* parameter.</span></span>
2.  <span data-ttu-id="20b31-124">Senden Sie die Lizenz Sperr Aufforderung an einen Lizenz Sperr Dienst.</span><span class="sxs-lookup"><span data-stu-id="20b31-124">Send the license revocation challenge to a license revocation service.</span></span> <span data-ttu-id="20b31-125">Der Server generiert als Antwort ein Lizenz Sperr-BLOB (LRB).</span><span class="sxs-lookup"><span data-stu-id="20b31-125">The server will generate a license revocation BLOB (LRB) in response.</span></span>
3.  <span data-ttu-id="20b31-126">Entfernen Sie die Lizenz aus dem lokalen Speicher mithilfe der [**iwmdrmlicenlmanagement::P rocess licenserevocationresponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) -Methode, und übergeben Sie dabei die vom Lizenzserver zurückgegebene LRB.</span><span class="sxs-lookup"><span data-stu-id="20b31-126">Remove the license from the local store using the [**IWMDRMLicenseManagement::ProcessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) method, passing the LRB returned by license server.</span></span>
4.  <span data-ttu-id="20b31-127">Hebt die Zuordnung des Puffers auf, **der von "" mit der** Funktion " **CoTaskMemFree** " zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="20b31-127">Deallocate the buffer allocated by **CreateLicenseRevocationChallenge** by using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="20b31-128">Weitere Informationen zur Funktionsweise der Lizenz Sperrung oder zum Schreiben eines Sperr Dienstanbieter finden Sie unter [Implementieren der Lizenz](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp)Sperrung.</span><span class="sxs-lookup"><span data-stu-id="20b31-128">For more information on how license revocation works or on how to write a revocation service, see [Implementing License Revocation](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="20b31-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20b31-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20b31-130">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="20b31-130">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="20b31-131">**Lokaler Lizenz Speicher**</span><span class="sxs-lookup"><span data-stu-id="20b31-131">**Local License Store**</span></span>](local-license-store.md)
</dt> <dt>

[<span data-ttu-id="20b31-132">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="20b31-132">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 