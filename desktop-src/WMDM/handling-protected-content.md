---
title: Behandeln geschützter Inhalte
description: Behandeln geschützter Inhalte
ms.assetid: f218d69e-ac80-43ba-be31-af3abf2b8de9
keywords:
- Windows Media Device Manager, Zertifikate
- Device Manager, Zertifikate
- Desktop Anwendungen, Zertifikate
- Dienstanbieter, Zertifikate
- Programmier Handbuch, Zertifikate
- certificates
- Windows Media Device Manager, Anbieter für sichere Inhalte (Secure Content Provider, SCP)
- Device Manager, sicherer Inhaltsanbieter (Secure Content Provider, SCP)
- Desktop Anwendungen, Secure Content Provider (SCP)
- Dienstanbieter, Anbieter für sichere Inhalte (Secure Content Provider, SCP)
- Programmier Handbuch, Anbieter für sichere Inhalte (Secure Content Provider, SCP)
- Secure Content Provider (SCP)
- SCP (sicherer Inhaltsanbieter)
- Windows Media Device Manager, DRM-geschützter Inhalt
- Device Manager, DRM-geschützter Inhalt
- Programmier Handbuch, DRM-geschützter Inhalt
- Desktop Anwendungen, DRM-geschützter Inhalt
- Dienstanbieter, DRM-geschützter Inhalt
- DRM-geschützter Inhalt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd0fb6ab155d08ed19eb84988709695f9ed63fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388168"
---
# <a name="handling-protected-content"></a><span data-ttu-id="0da7a-122">Behandeln geschützter Inhalte</span><span class="sxs-lookup"><span data-stu-id="0da7a-122">Handling Protected Content</span></span>

<span data-ttu-id="0da7a-123">Wenn Sie eine Anwendung oder einen Dienstanbieter entwickeln, die von Windows Media Digital Rights Management (DRM) geschützte Inhalte nutzen, müssen Sie über ein Schlüssel-/zertifikatpaar verfügen, das von Microsoft ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0da7a-123">If you are building an application or service provider that will consume content protected by Windows Media digital rights management (DRM), you must have a key/certificate pair issued by Microsoft.</span></span> <span data-ttu-id="0da7a-124">Informationen dazu, wo Sie dieses Zertifikat erhalten, finden Sie unter [Tools für die Entwicklung](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="0da7a-124">To learn where to get this certificate, see [Tools for Development](tools-for-development.md).</span></span> <span data-ttu-id="0da7a-125">Wenn Sie nicht beabsichtigen, geschützte Inhalte zu verarbeiten, können Sie den Dummy-Schlüssel und das Zertifikat, das mit diesem SDK bereitgestellt wird, in einer Datei namens Key. c verwenden.</span><span class="sxs-lookup"><span data-stu-id="0da7a-125">If you do not intend to handle protected content, you can use the dummy key and certificate provided with this SDK in a file named key.c.</span></span>

<span data-ttu-id="0da7a-126">Für alle Dateien, die durch DRM-Technologie geschützt sind, muss für Windows Media Device Manager ein sicherer Inhaltsanbieter (Secure Content Provider, SCP) für dieses Dateiformat vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0da7a-126">For any file that is protected by DRM technology, Windows Media Device Manager requires the presence of a secure content provider (SCP) for that file format.</span></span> <span data-ttu-id="0da7a-127">Microsoft stellt ein SCP-Modul für WMA-und WMV-Dateien bereit.</span><span class="sxs-lookup"><span data-stu-id="0da7a-127">Microsoft provides an SCP module for WMA and WMV files.</span></span> <span data-ttu-id="0da7a-128">Wenn Ihre Anwendung oder Ihr Dienstanbieter von DRM geschützten Inhalten in einem anderen Format verarbeitet, müssen Sie Ihr eigenes SCP-Modul bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0da7a-128">If your application or service provider will be handling DRM-protected content of another format, you must provide your own SCP module.</span></span> <span data-ttu-id="0da7a-129">Ein SCP-Modul ist ein COM-Objekt, das alle [Schnittstellen für sichere Inhaltsanbieter](interfaces-for-secure-content-providers.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="0da7a-129">An SCP module is a COM object that implements all the [interfaces for Secure Content Providers](interfaces-for-secure-content-providers.md).</span></span>

<span data-ttu-id="0da7a-130">Eine Anwendung kann DRM-geschützte Inhalte an Geräte senden, die entweder auf Windows Media DRM 10 für tragbare Geräte oder auf einem tragbaren Geräte-DRM (PDDRM) erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="0da7a-130">An application can send DRM-protected content to devices built on either Windows Media DRM 10 for Portable Devices, or Portable Device DRM (PDDRM).</span></span> <span data-ttu-id="0da7a-131">Sie können jedoch nur einen Dienstanbieter für Geräte erstellen, die auf PDDRM erstellt wurden. Es ist nicht möglich, einen Dienstanbieter für Geräte zu erstellen, die mit Windows Media DRM 10 für tragbare Geräte erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="0da7a-131">However, you can only create a service provider for devices built on PDDRM; you cannot create a service provider for devices built on Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="0da7a-132">Diese letzteren Geräte können nur den von Microsoft bereitgestellten MTP-Dienstanbieter verwenden.</span><span class="sxs-lookup"><span data-stu-id="0da7a-132">These latter devices can only use the Microsoft-provided MTP service provider.</span></span>

<span data-ttu-id="0da7a-133">Geräte, die auf PDDRM basieren, können nur Lizenzen für erworbene Inhalte unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0da7a-133">Devices built on PDDRM can only support licenses for purchased content.</span></span> <span data-ttu-id="0da7a-134">Lizenzen mit Zeitablauf Bedingungen werden nur von Geräten unterstützt, die auf Windows Media DRM 10 für tragbare Geräte basieren und spezielle Anforderungen erfüllen, wie z. b. eine sichere Uhr und eine individuelle Individualisierung.</span><span class="sxs-lookup"><span data-stu-id="0da7a-134">Licenses that have time-expiration conditions are only supported by devices built on Windows Media DRM 10 for Portable Devices, which have special requirements such as a secure clock and individualization.</span></span> <span data-ttu-id="0da7a-135">Windows Media DRM 10 for Portable Devices SDK enthält Details zu den Geräteanforderungen zur Unterstützung der Technologie der Version 10.</span><span class="sxs-lookup"><span data-stu-id="0da7a-135">Windows Media DRM 10 for Portable Devices SDK gives details on device requirements to support version 10 technology.</span></span>

<span data-ttu-id="0da7a-136">Vor dem Senden von DRM-Inhalten an das Gerät muss eine Anwendung verschiedene Dinge überprüfen:</span><span class="sxs-lookup"><span data-stu-id="0da7a-136">Before sending DRM content to the device, an application should verify several things:</span></span>

-   <span data-ttu-id="0da7a-137">Das Gerät unterstützt DRM-Technologie.</span><span class="sxs-lookup"><span data-stu-id="0da7a-137">That the device supports DRM technology.</span></span>
-   <span data-ttu-id="0da7a-138">Welche Version der DRM-Technologie unterstützt wird (Version 10 oder früher).</span><span class="sxs-lookup"><span data-stu-id="0da7a-138">What version of DRM technology it supports (version 10 or earlier).</span></span>
-   <span data-ttu-id="0da7a-139">Wenn das Gerät auf Version 10 basiert, sind alle Komponenten auf dem neuesten Stand (z. b. die sichere Uhr und alle individuellen Anforderungen).</span><span class="sxs-lookup"><span data-stu-id="0da7a-139">If the device is built on version 10, that all its components are up to date (such as the secure clock and any individualization requirements).</span></span>

<span data-ttu-id="0da7a-140">Alle Methodenaufrufe zum Beantworten dieser Fragen werden vom Client durchgeführt und von Windows Media Device Manager und der Komponente für den sicheren Inhaltsanbieter verarbeitet. der Dienstanbieter verarbeitet diese Aufrufe nicht.</span><span class="sxs-lookup"><span data-stu-id="0da7a-140">All method calls to answer these questions are made by the client and handled by Windows Media Device Manager and the secure content provider component; the service provider does not handle any of these calls.</span></span>

<span data-ttu-id="0da7a-141">Wenn das Gerät Windows Media DRM 10 für tragbare Geräte nicht unterstützt, kann es möglicherweise trotzdem geschützte Inhalte nutzen (abhängig von der Inhalts Lizenz und dem Geräte Entwurf), aber alle an ihn gesendeten Inhalte verfügen über eine vereinfachte Nutzungslizenz mit eingeschränkten Rechten (z. b. kein Zeitablauf).</span><span class="sxs-lookup"><span data-stu-id="0da7a-141">If the device does not support Windows Media DRM 10 for Portable Devices, it might still be able to consume protected content (depending on the content license and the device design), but any content sent to it will have a simplified use license with limited rights (for example, no time expiration).</span></span>

-   <span data-ttu-id="0da7a-142">Beispiele, die zeigen, wie eine Anwendung überprüft, ob ein Gerät geschützte Inhalte verarbeiten kann und ob die zugehörigen DRM-Komponenten aktualisiert werden müssen, finden Sie unter [behandeln geschützter Inhalte in der Anwendung](handling-protected-content-in-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="0da7a-142">For examples demonstrating how an application verifies whether a device can handle protected content, and whether it needs to update its DRM components, see [Handling Protected Content in the Application](handling-protected-content-in-the-application.md).</span></span>
-   <span data-ttu-id="0da7a-143">Weitere Informationen zum Aufbau eines Dienstanbieters, der geschützte Inhalte verarbeiten kann, finden Sie unter [verarbeiten geschützter Inhalte im Dienstanbieter](handling-protected-content-in-the-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0da7a-143">For more information about building a service provider that can handle protected content, see [Handling Protected Content in the Service Provider](handling-protected-content-in-the-service-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="0da7a-144">Beim Verarbeiten von DRM-geschützten Dateien mit einem angefügten Debugger tritt bei vielen Windows  Media Device Manager-Methoden zum Übertragen von Dateien oder beim Anfordern von Berechtigungen ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0da7a-144">Many Windows Media Device Manager file transfer or rights requesting methods will fail (often with a mysterious **HRESULT** value) when handling DRM-protected files with a debugger attached.</span></span> <span data-ttu-id="0da7a-145">Daher müssen Sie zum Debuggen des Codes Alternative Methoden verwenden, z. b. die Protokollierung von Ausgaben in eine Windows Form oder eine Protokolldatei.</span><span class="sxs-lookup"><span data-stu-id="0da7a-145">Therefore, you must use alternate ways to debug your code, such as logging outputs to a Windows form or a log file.</span></span> <span data-ttu-id="0da7a-146">Weitere Informationen zu Protokollierungs Optionen finden Sie unter [Aktivieren der Protokollierung](enabling-logging.md).</span><span class="sxs-lookup"><span data-stu-id="0da7a-146">For more information on logging options, see [Enabling Logging](enabling-logging.md).</span></span> <span data-ttu-id="0da7a-147">Wenn Sie einen Debugger für geschützte Inhalte ausführen, gibt eine Methode einen der im DRM-Abschnitt [Fehlercodes](error-codes.md)oder möglicherweise unbekannten Fehlercodes aufgelisteten Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="0da7a-147">If you are running a debugger on protected content, a method will return one of the error codes listed in the DRM section [Error Codes](error-codes.md), or possibly an unknown error code.</span></span> <span data-ttu-id="0da7a-148">Wenn Sie beim Ausführen eines Debuggers auf geschützten Inhalten oder Methoden rätselhafte **HRESULT** -Werte erhalten, könnte der DRM-Schutz die Ursache sein.</span><span class="sxs-lookup"><span data-stu-id="0da7a-148">If you get mysterious **HRESULT** values when running a debugger on protected content or methods, DRM protection might be the cause.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0da7a-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0da7a-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0da7a-150">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="0da7a-150">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




