---
title: Tools für die Entwicklung
description: Tools für die Entwicklung
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Media Device Manager, Entwicklungs Tools
- Device Manager, Entwicklungs Tools
- Windows Media Device Manager, Zertifikate
- Device Manager, Zertifikate
- Windows Media-Device Manager, Schlüssel
- Device Manager, Schlüssel
- Windows Media-Device Manager, Bibliotheken
- Device Manager, Bibliotheken
- Windows Media Device Manager, Software Development Kit (SDK)
- Device Manager, Software Development Kit (SDK)
- Windows Media Device Manager SDK
- Device Manager SDK
- Windows Media Player SDK
- SDK für Windows Media-Format
- Windows Media Rights Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45a3e419b87c56a447ad2412234a80432b1598e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "106340288"
---
# <a name="tools-for-development"></a><span data-ttu-id="a5333-118">Tools für die Entwicklung</span><span class="sxs-lookup"><span data-stu-id="a5333-118">Tools for Development</span></span>

<span data-ttu-id="a5333-119">In diesem Abschnitt werden die verschiedenen Zertifikate und Schlüssel, Bibliotheken und SDKs beschrieben, die Sie zum Programmieren mit dem Windows Media Device Manager SDK benötigen.</span><span class="sxs-lookup"><span data-stu-id="a5333-119">This section describes the various certificates and keys, libraries, and SDKs you will need to program using the Windows Media Device Manager SDK.</span></span>

<span data-ttu-id="a5333-120">Zertifikate und Schlüssel</span><span class="sxs-lookup"><span data-stu-id="a5333-120">Certificates and Keys</span></span>

<span data-ttu-id="a5333-121">Das Windows Media Device Manager SDK wird mit einem Testschlüssel/-Zertifikat Paar (in der Key. c-Datei) ausgeliefert, das von einer Anwendung oder einem Dienstanbieter verwendet werden kann, um Windows Media Device Manager-Methoden für ungeschützten Inhalt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a5333-121">The Windows Media Device Manager SDK ships with a test key/certificate pair (in the key.c file) that can be used by an application or a service provider to use Windows Media Device Manager methods on unprotected content.</span></span> <span data-ttu-id="a5333-122">Mit diesem Schlüssel-/zertifikatpaar kann die Anwendung oder der Dienstanbieter den größten Teil der Windows Media Device Manager-Funktionalität nutzen.</span><span class="sxs-lookup"><span data-stu-id="a5333-122">This key/certificate pair allows the application or service provider to use most of the Windows Media Device Manager functionality.</span></span>

<span data-ttu-id="a5333-123">Wenn Sie jedoch eine Anwendung oder einen Dienstanbieter entwickeln möchten, die von DRM-geschützten Inhalten verarbeitet werden kann, müssen Sie ein oder mehrere Zertifikate (jedes mit einem Schlüssel) von der [Windows Media Licensing-Seite](https://www.microsoft.com/licensing/default)anfordern.</span><span class="sxs-lookup"><span data-stu-id="a5333-123">However, to develop an application or service provider that can handle DRM-protected content, you must request one or more certificates (each with a key) from the [Windows Media Licensing Page](https://www.microsoft.com/licensing/default).</span></span> <span data-ttu-id="a5333-124">Für die folgenden Anwendungen oder Objekte sind Zertifikate erforderlich:</span><span class="sxs-lookup"><span data-stu-id="a5333-124">Certificates are required for the following applications or objects:</span></span>

-   <span data-ttu-id="a5333-125">Dienstanbieter, die von DRM geschützten Inhalten verarbeiten, benötigen ein Windows Media Device Manager-Dienstanbieter Zertifikat (und einen Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="a5333-125">Service Providers that handle DRM-protected content require a Windows Media Device Manager Service Provider Certificate (and key)</span></span>
-   <span data-ttu-id="a5333-126">Anwendungen, die DRM-geschützten Inhalt übertragen, benötigen ein Windows Media Device Manager Transfer Certificate (und einen Schlüssel)</span><span class="sxs-lookup"><span data-stu-id="a5333-126">Applications that transfer DRM-protected content require a Windows Media Device Manager Transfer Certificate (and key)</span></span>
-   <span data-ttu-id="a5333-127">Anwendungen, die DRM-geschützten Inhalt abspielen, benötigen ein DRM-Zertifikat (und einen Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="a5333-127">Applications that play DRM-protected content require a DRM Certificate (and key).</span></span>
-   <span data-ttu-id="a5333-128">Für Lizenz Messungs Komponenten ist ein Messungs Zertifikat erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a5333-128">License metering components require a metering certificate.</span></span> <span data-ttu-id="a5333-129">Diese wird von einem Lizenz Messungs Dienst bereitgestellt, der auf dem Windows Media Rights Manager SDK basiert und auf der Seite Windows Media-Lizenzierung angefordert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a5333-129">This is provided by a license metering service built on the Windows Media Rights Manager SDK, which can be requested on the Windows Media Licensing Page.</span></span>

<span data-ttu-id="a5333-130">Bibliotheken und Header</span><span class="sxs-lookup"><span data-stu-id="a5333-130">Libraries and Headers</span></span>

<span data-ttu-id="a5333-131">Zusätzlich zu den Bibliotheken und Headern, die in [erforderlichen Bibliotheks-und Header Dateien für eine Anwendung](required-library-and-header-files-for-an-application.md) oder [erforderliche Bibliotheken und Header für einen Dienstanbieter](required-libraries-and-headers-for-a-service-provider.md)erwähnt wurden, sollten alle Anwendungen und Plug-ins, die zuvor mit wmdrmsdk. lib verknüpft waren, um die Windows Media-Format-SDK-Funktionen aufzurufen, jetzt mit wmdrmsdkstub. lib verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="a5333-131">In addition to the libraries and headers mentioned in [Required Library and Header Files for an Application](required-library-and-header-files-for-an-application.md) or [Required Libraries and Headers for a Service Provider](required-libraries-and-headers-for-a-service-provider.md), any application or plug-in that formerly linked to WMDRMSDK.lib to call Windows Media Format SDK functions should now instead link to WMDRMSDKStub.Lib.</span></span> <span data-ttu-id="a5333-132">Diese Bibliotheksdatei wird verwendet, um auf von DRM geschützte Dateien zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="a5333-132">This library file is used to access DRM-protected files.</span></span> <span data-ttu-id="a5333-133">Sie können diese Bibliothek auch auf der Seite Windows Media-Lizenzierung anfordern.</span><span class="sxs-lookup"><span data-stu-id="a5333-133">You can request this library from the Windows Media Licensing Page as well.</span></span>

<span data-ttu-id="a5333-134">Verwandte sdche</span><span class="sxs-lookup"><span data-stu-id="a5333-134">Related SDKs</span></span>

<span data-ttu-id="a5333-135">Die folgenden Microsoft sdert stellen Elemente bereit, die Sie möglicherweise beim Entwerfen von Lösungen für tragbare Mediengeräte benötigen.</span><span class="sxs-lookup"><span data-stu-id="a5333-135">The following Microsoft SDKs provide elements you may need in designing solutions for portable media devices.</span></span>



| <span data-ttu-id="a5333-136">SDK erforderlich</span><span class="sxs-lookup"><span data-stu-id="a5333-136">SDK Required</span></span>                     | <span data-ttu-id="a5333-137">Erforderlich für...</span><span class="sxs-lookup"><span data-stu-id="a5333-137">Required for...</span></span>                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5333-138">Windows Media Device Manager SDK</span><span class="sxs-lookup"><span data-stu-id="a5333-138">Windows Media Device Manager SDK</span></span> | <span data-ttu-id="a5333-139">Desktop Media Player-Anwendungen, die mit tragbaren Geräten kommunizieren</span><span class="sxs-lookup"><span data-stu-id="a5333-139">Desktop media player applications that communicate with portable devices</span></span><br/> <span data-ttu-id="a5333-140">Desktop Anwendungen, die Dateien oder Informationen mit tragbaren Geräten austauschen können</span><span class="sxs-lookup"><span data-stu-id="a5333-140">Desktop applications that can exchange files or information with portable devices</span></span><br/> <span data-ttu-id="a5333-141">Windows Media Player Messungs-com-Objekte</span><span class="sxs-lookup"><span data-stu-id="a5333-141">Windows Media Player metering COM objects</span></span><br/> |
| <span data-ttu-id="a5333-142">Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="a5333-142">Windows Media Player SDK</span></span>         | <span data-ttu-id="a5333-143">Windows Media Player-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="a5333-143">Windows Media Player plug-ins</span></span><br/> <span data-ttu-id="a5333-144">Windows Media Player Messungs-com-Objekte</span><span class="sxs-lookup"><span data-stu-id="a5333-144">Windows Media Player metering COM objects</span></span><br/> <span data-ttu-id="a5333-145">Windows Media Player Skins</span><span class="sxs-lookup"><span data-stu-id="a5333-145">Windows Media Player skins</span></span><br/>                                                                                                   |
| <span data-ttu-id="a5333-146">SDK für Windows Media-Format</span><span class="sxs-lookup"><span data-stu-id="a5333-146">Windows Media Format SDK</span></span>         | <span data-ttu-id="a5333-147">Audio-oder Video Player, die Dateien erstellen oder wiedergeben können (vor allem bei ASF-Dateien)</span><span class="sxs-lookup"><span data-stu-id="a5333-147">Audio or video players that can create or play files (particularly ASF files)</span></span><br/> <span data-ttu-id="a5333-148">Anwendungen für die Audiobearbeitung oder Videobearbeitung</span><span class="sxs-lookup"><span data-stu-id="a5333-148">Audio or video editing applications</span></span><br/>                                                                                               |
| <span data-ttu-id="a5333-149">Windows Media Rights Manager SDK</span><span class="sxs-lookup"><span data-stu-id="a5333-149">Windows Media Rights Manager SDK</span></span> | <span data-ttu-id="a5333-150">Anwendungen und Plug-ins, die die Anzahl von spielen Messen, werden auf dem Desktop oder Gerät angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a5333-150">Applications or plug-ins that meter play counts on the desktop or device.</span></span>                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="a5333-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a5333-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5333-152">**Einstieg**</span><span class="sxs-lookup"><span data-stu-id="a5333-152">**Getting Started**</span></span>](getting-started.md)
</dt> </dl>

 

 





