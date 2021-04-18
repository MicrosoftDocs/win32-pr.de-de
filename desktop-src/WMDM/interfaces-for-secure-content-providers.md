---
title: Schnittstellen für sichere Inhaltsanbieter
description: Schnittstellen für sichere Inhaltsanbieter
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows Media Device Manager, DRM-geschützter Inhalt
- Device Manager, DRM-geschützter Inhalt
- Programmier Referenz, DRM-geschützter Inhalt
- Referenz für Windows Media Device Manager, DRM-geschützten Inhalt
- DRM-geschützter Inhalt
- Windows Media Device Manager, Anbieter für sichere Inhalte (Secure Content Provider, SCP)
- Device Manager, sicherer Inhaltsanbieter (Secure Content Provider, SCP)
- Programmier Referenz, Anbieter für sichere Inhalte (Secure Content Provider, SCP)
- Referenz für Windows Media Device Manager, Secure Content Provider (SCP)
- Secure Content Provider (SCP)
- SCP (sicherer Inhaltsanbieter)
- Windows Media Device Manager, SCP-Schnittstellen
- Device Manager, SCP-Schnittstellen
- Programmier Referenz, SCP-Schnittstellen
- Referenz für Windows Media Device Manager, SCP-Schnittstellen
- SCP-Schnittstellen, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e4483a5bfb62e165b1bc17e588dfe3bd5b73f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340624"
---
# <a name="interfaces-for-secure-content-providers"></a><span data-ttu-id="882d2-119">Schnittstellen für sichere Inhaltsanbieter</span><span class="sxs-lookup"><span data-stu-id="882d2-119">Interfaces for Secure Content Providers</span></span>

<span data-ttu-id="882d2-120">Ein sicherer Inhaltsanbieter (Secure Content Provider, SCP) ist eine Plug-in-Komponente, die es Windows Media Device Manager ermöglicht, Rechte Informationen von DRM-geschützten Inhalten zu übertragen und anzufordern.</span><span class="sxs-lookup"><span data-stu-id="882d2-120">A secure content provider (SCP) is a plug-in component that enables Windows Media Device Manager to transfer and request rights information from DRM-protected content.</span></span> <span data-ttu-id="882d2-121">Microsoft stellt eine SCP-Komponente bereit, die von DRM geschützte WMA-und WMV-Dateien verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="882d2-121">Microsoft provides an SCP component that can handle DRM-protected WMA and WMV files.</span></span> <span data-ttu-id="882d2-122">Wenn Ihr Gerät oder Ihre Anwendung DRM-geschützten Inhalt anderer Formate verwendet, sollte eine SCP-Komponente erstellt werden, indem alle diese Schnittstellen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="882d2-122">If your device or application will use DRM-protected content of other formats, it should create an SCP component by implementing all of these interfaces.</span></span> <span data-ttu-id="882d2-123">Andernfalls müssen Sie diese Schnittstellen nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="882d2-123">Otherwise, you will not need to use these interfaces.</span></span>



| <span data-ttu-id="882d2-124">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="882d2-124">Interface</span></span>                                                  | <span data-ttu-id="882d2-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="882d2-125">Description</span></span>                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="882d2-126">**Iscpsecureauthenticate**</span><span class="sxs-lookup"><span data-stu-id="882d2-126">**ISCPSecureAuthenticate**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | <span data-ttu-id="882d2-127">Die primäre Schnittstelle des sicheren Inhalts Anbieters.</span><span class="sxs-lookup"><span data-stu-id="882d2-127">The primary interface of the secure content provider.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="882d2-128">**ISCPSecureAuthenticate2**</span><span class="sxs-lookup"><span data-stu-id="882d2-128">**ISCPSecureAuthenticate2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | <span data-ttu-id="882d2-129">Erweitert **iscpsecureauthenticate** durch Bereitstellen einer Möglichkeit, ein Sitzungs Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="882d2-129">Extends **ISCPSecureAuthenticate** by providing a way to get a session object.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="882d2-130">**Iscpsecureexchange**</span><span class="sxs-lookup"><span data-stu-id="882d2-130">**ISCPSecureExchange**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | <span data-ttu-id="882d2-131">Dient zum Austauschen geschützter Inhalte und Rechte, die mit Inhalten verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="882d2-131">Used to exchange secured content and rights associated with content.</span></span>                                                                                                                                                                                 |
| [<span data-ttu-id="882d2-132">**ISCPSecureExchange2**</span><span class="sxs-lookup"><span data-stu-id="882d2-132">**ISCPSecureExchange2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | <span data-ttu-id="882d2-133">Erweitert **iscpsecureexchange** durch Bereitstellen einer neuen Version der **transfercontainerdata** -Methode.</span><span class="sxs-lookup"><span data-stu-id="882d2-133">Extends **ISCPSecureExchange** by providing a new version of the **TransferContainerData** method.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="882d2-134">**ISCPSecureExchange3**</span><span class="sxs-lookup"><span data-stu-id="882d2-134">**ISCPSecureExchange3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | <span data-ttu-id="882d2-135">Erweitert **ISCPSecureExchange2** durch eine verbesserte Datenaustausch Leistung und eine Übertragungs Complete-Rückruf Methode.</span><span class="sxs-lookup"><span data-stu-id="882d2-135">Extends **ISCPSecureExchange2** by providing improved data exchange performance, and a transfer complete callback method.</span></span>                                                                                                                            |
| [<span data-ttu-id="882d2-136">**Iscpsecurequery**</span><span class="sxs-lookup"><span data-stu-id="882d2-136">**ISCPSecureQuery**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | <span data-ttu-id="882d2-137">Wird von Windows Media Device Manager abgefragt, um den Besitz geschützter Inhalte zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="882d2-137">Queried by Windows Media Device Manager to determine ownership of secured content.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="882d2-138">**ISCPSecureQuery2**</span><span class="sxs-lookup"><span data-stu-id="882d2-138">**ISCPSecureQuery2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | <span data-ttu-id="882d2-139">Erweitert **iscpsecurequery** durch Funktionalität, die bestimmt, ob der Anbieter für sichere Inhalte für den Inhalt zuständig ist, und wenn dies der Fall ist, die Bereitstellung einer URL zum Aktualisieren von widerrufenen Komponenten und zum Ermitteln der abrufenden Komponenten.</span><span class="sxs-lookup"><span data-stu-id="882d2-139">Extends **ISCPSecureQuery** through functionality that determines whether the secure content provider is responsible for the content, and if so, providing a URL for updating revoked components and determining which components have been revoked.</span></span> |
| [<span data-ttu-id="882d2-140">**ISCPSecureQuery3**</span><span class="sxs-lookup"><span data-stu-id="882d2-140">**ISCPSecureQuery3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | <span data-ttu-id="882d2-141">Erweitert **ISCPSecureQuery2** durch die Bereitstellung eines Satzes neuer Methoden zum Abrufen der Rechte und Treffen der Entscheidung für einen unverschlüsselten Kanal.</span><span class="sxs-lookup"><span data-stu-id="882d2-141">Extends **ISCPSecureQuery2** by providing a set of new methods for retrieving the rights and making decision on a clear channel.</span></span>                                                                                                                     |
| [<span data-ttu-id="882d2-142">**Iscpsession**</span><span class="sxs-lookup"><span data-stu-id="882d2-142">**ISCPSession**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | <span data-ttu-id="882d2-143">Bietet eine effiziente allgemeine Zustands Verwaltung für mehrere Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="882d2-143">Provides efficient common state management for multiple operations.</span></span>                                                                                                                                                                                  |



 

 

 




