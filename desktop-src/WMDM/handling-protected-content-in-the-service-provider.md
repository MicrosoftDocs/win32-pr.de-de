---
title: Behandeln geschützter Inhalte im Dienstanbieter
description: Behandeln geschützter Inhalte im Dienstanbieter
ms.assetid: 5c18c8ec-d579-41df-8c25-c143fb9cdbef
keywords:
- Windows Media Device Manager, Zertifikate
- Device Manager, Zertifikate
- Programmier Handbuch, Zertifikate
- Dienstanbieter, Zertifikate
- Erstellen von Dienstanbietern, Zertifikaten
- certificates
- Windows Media Device Manager, DRM-geschützter Inhalt
- Device Manager, DRM-geschützter Inhalt
- Programmier Handbuch, DRM-geschützter Inhalt
- Dienstanbieter, DRM-geschützter Inhalt
- Erstellen von Dienstanbietern, DRM-geschütztem Inhalt
- DRM-geschützter Inhalt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d10cf9078cf9aaf631b65de968f01491a97781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337977"
---
# <a name="handling-protected-content-in-the-service-provider"></a><span data-ttu-id="68179-115">Behandeln geschützter Inhalte im Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="68179-115">Handling Protected Content in the Service Provider</span></span>

<span data-ttu-id="68179-116">Sie können einen Dienstanbieter erstellen, der DRM-geschützten Inhalt an ein auf portable Geräte-DRM (PDDRM) aufgebautes Gerät senden kann. Sie können jedoch keinen Dienstanbieter erstellen, der von DRM-geschützten Inhalten an Geräte senden kann, die auf Windows Media DRM 10 für tragbare Geräte erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="68179-116">You can build a service provider that can send DRM-protected content to a device built on Portable Device DRM (PDDRM), but you cannot build a service provider that can send DRM-protected content to devices built on Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="68179-117">Diese Geräte verwenden MTP, und Sie können keinen eigenen MTP-Dienstanbieter erstellen.</span><span class="sxs-lookup"><span data-stu-id="68179-117">These devices use MTP, and you cannot build your own MTP service provider.</span></span>

<span data-ttu-id="68179-118">Der einzige zusätzliche Schritt, den ein Dienstanbieter zum Senden von DRM-Material an ein PDDRM-Gerät ausführen muss, besteht darin, ein von Microsoft ausgestelltes Zertifikat/Schlüssel-Paar zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="68179-118">The only extra step that a service provider must take to send DRM material to a PDDRM device is to get a Microsoft-issued certificate/key pair.</span></span> <span data-ttu-id="68179-119">Informationen dazu, wo Sie dieses Zertifikat/welchen Schlüssel erhalten, finden Sie unter [Tools für die Entwicklung](tools-for-development.md) .</span><span class="sxs-lookup"><span data-stu-id="68179-119">See [Tools for Development](tools-for-development.md) to learn where to get this certificate/key.</span></span> <span data-ttu-id="68179-120">Die Lizenzen, die für diese Geräte ausgestellt werden, sind vereinfachte Lizenzen, die nur die einfache Wiedergabe erworbener Inhalte unterstützen. Es werden keine Zeitablauf Lizenzen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68179-120">The licenses issued to these devices will be simplified licenses that only support simple playback of purchased content; they will not support time-expiring licenses.</span></span> <span data-ttu-id="68179-121">Diese Lizenz wird vom Anbieter für sichere Inhalte (von Microsoft für WMA/WMV-Dateien bereitgestellt) erstellt und im Header der Datei gespeichert, die an den Dienstanbieter gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="68179-121">This license will be created for you by the secure content provider (provided by Microsoft for WMA/WMV files) and stored in the header of the file sent to the service provider.</span></span> <span data-ttu-id="68179-122">Sie müssen keine speziellen Schritte für geschützte Dateien ausführen.</span><span class="sxs-lookup"><span data-stu-id="68179-122">You will not have to take any special steps for protected files.</span></span>

<span data-ttu-id="68179-123">Nachdem die geschützte Datei gesendet wurde, ruft der Windows Media-Device Manager den Dienstanbieter auf, um eine spezielle Lizenz Speicherdatei vom Gerät anzufordern.</span><span class="sxs-lookup"><span data-stu-id="68179-123">After sending the protected file, Windows Media Device Manager will call the service provider to request a special license storage file from the device.</span></span> <span data-ttu-id="68179-124">Windows Media Device Manager fügt dieser Datei eine Kopie der neuen Lizenz hinzu und sendet Sie an den Dienstanbieter zurück, um Sie zurück an das Gerät zu senden.</span><span class="sxs-lookup"><span data-stu-id="68179-124">Windows Media Device Manager will add a copy of the new license to this file, and return it to the service provider to send back to the device.</span></span> <span data-ttu-id="68179-125">Auch wenn der Dienstanbieter diese Datei nicht finden oder zurückgeben kann, sollte das Gerät weiterhin in der Lage sein, die geschützte Datei mit der Lizenz Kopie im Dateiheader wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="68179-125">However, even if the service provider fails to find or return this file, the device should still be able to play the protected file by using the license copy in the file header.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68179-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="68179-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68179-127">**Erstellen eines Dienstanbieters**</span><span class="sxs-lookup"><span data-stu-id="68179-127">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="68179-128">**Behandeln geschützter Inhalte**</span><span class="sxs-lookup"><span data-stu-id="68179-128">**Handling Protected Content**</span></span>](handling-protected-content.md)
</dt> </dl>

 

 




