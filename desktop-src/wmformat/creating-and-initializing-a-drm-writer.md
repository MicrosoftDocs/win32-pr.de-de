---
title: Erstellen und Initialisieren eines DRM-Writers
description: Erstellen und Initialisieren eines DRM-Writers
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- Windows Media-Format-SDK, DRM-Writer
- Digital Rights Management (DRM), Erstellen von DRM-Writern
- DRM (Digital Rights Management), Erstellen von DRM-Writern
- Digital Rights Management (DRM), Initialisieren von DRM-Writern
- DRM (Digital Rights Management), Initialisieren von DRM-Writern
- Erweiterte APIs für den DRM-Client, DRM-Writer
- Erweiterte Client-APIs, DRM-Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed40b7f9dd9c486b1ef22e5042261c5ce03d2f7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "106337268"
---
# <a name="creating-and-initializing-a-drm-writer"></a><span data-ttu-id="f7818-110">Erstellen und Initialisieren eines DRM-Writers</span><span class="sxs-lookup"><span data-stu-id="f7818-110">Creating and Initializing a DRM Writer</span></span>

<span data-ttu-id="f7818-111">Die folgenden Schritte sind erforderlich, um ein ASF Writer-Objekt zum Importieren verschlüsselter Medien Beispiele in Windows Media DRM zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="f7818-111">The following steps are required to initialize an ASF writer object for importing encrypted media samples in Windows Media DRM.</span></span>

1.  <span data-ttu-id="f7818-112">Führen Sie die Schritte 1 bis 4 zum [Importieren von Lizenz-und Schlüssel Material](importing-license-and-key-material.md)aus.</span><span class="sxs-lookup"><span data-stu-id="f7818-112">Follow steps 1 to 4 of [Importing License and Key Material](importing-license-and-key-material.md).</span></span>
2.  <span data-ttu-id="f7818-113">Erstellen und initialisieren Sie ein ASF-Writer-Objekt mit dem entsprechenden Windows Media DRM-Schlüsselmaterial.</span><span class="sxs-lookup"><span data-stu-id="f7818-113">Create and initialize an ASF writer object using the appropriate Windows Media DRM key material.</span></span> <span data-ttu-id="f7818-114">Weitere Informationen finden Sie [unter Aktivieren der DRM-Unterstützung](enabling-drm-support.md).</span><span class="sxs-lookup"><span data-stu-id="f7818-114">For more information, see [Enabling DRM Support](enabling-drm-support.md).</span></span>
3.  <span data-ttu-id="f7818-115">Legen Sie jedes der folgenden Attribute fest, indem Sie [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)aufrufen:</span><span class="sxs-lookup"><span data-stu-id="f7818-115">Set each of the following attributes by calling [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):</span></span>
    -   <span data-ttu-id="f7818-116">DRM \_ headersignprivkey</span><span class="sxs-lookup"><span data-stu-id="f7818-116">DRM\_HeaderSignPrivKey</span></span>
    -   <span data-ttu-id="f7818-117">DRM- \_ V1LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="f7818-117">DRM\_V1LicenseAcqURL</span></span>
    -   <span data-ttu-id="f7818-118">DRM- \_ Schlüssel-ID</span><span class="sxs-lookup"><span data-stu-id="f7818-118">DRM\_KeyID</span></span>
    -   <span data-ttu-id="f7818-119">DRM- \_ Lizenz-AcqURL</span><span class="sxs-lookup"><span data-stu-id="f7818-119">DRM\_LicenseAcqURL</span></span>
4.  <span data-ttu-id="f7818-120">Wenn auf dem Computer, auf dem die Software ausgeführt wird, keine lizenzierte Version von Windows Media Rights Manager installiert ist, müssen auch die folgenden vier Attribute festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f7818-120">If a licensed version of Windows Media Rights Manager is not installed on the computer running your software, then the following four attributes must also be set:</span></span>
    -   <span data-ttu-id="f7818-121">DRM \_ lasignaturerootcert</span><span class="sxs-lookup"><span data-stu-id="f7818-121">DRM\_LASignatureRootCert</span></span>
    -   <span data-ttu-id="f7818-122">DRM- \_ lasignaturecert</span><span class="sxs-lookup"><span data-stu-id="f7818-122">DRM\_LASignatureCert</span></span>
    -   <span data-ttu-id="f7818-123">DRM \_ lasignaturelicsrvcert</span><span class="sxs-lookup"><span data-stu-id="f7818-123">DRM\_LASignatureLicSrvCert</span></span>
    -   <span data-ttu-id="f7818-124">DRM- \_ lasignatureprivkey</span><span class="sxs-lookup"><span data-stu-id="f7818-124">DRM\_LASignaturePrivKey</span></span>
    -   <span data-ttu-id="f7818-125">Die Anwendung für die erforderlichen Verschlüsselungs Zertifikate kann durch Ausfüllen des [Windows Media Licensing Agreement (wmla)](https://www.microsoft.com/licensing/default) Online abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="f7818-125">Application for the necessary encryption certificates can be completed by filling out the [Windows Media Licensing Agreement (WMLA)](https://www.microsoft.com/licensing/default) online.</span></span>
5.  <span data-ttu-id="f7818-126">Erstellen Sie einen Sitzungsschlüssel, und füllen Sie eine [**WMDRM- \_ \_ \_ Schlüssel**](wmdrm-import-session-key.md) Struktur zum Importieren der Sitzung aus.</span><span class="sxs-lookup"><span data-stu-id="f7818-126">Create a session key and fill out a [**WMDRM\_IMPORT\_SESSION\_KEY**](wmdrm-import-session-key.md) structure.</span></span> <span data-ttu-id="f7818-127">Der Sitzungsschlüssel wird zum Verschlüsseln eines Inhalts Schlüssels verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7818-127">The session key will be used for encrypting a content key.</span></span> <span data-ttu-id="f7818-128">Ein Beispiel finden Sie unter [Beispiel für das Erstellen eines Sitzungsschlüssels](create-session-key-example.md).</span><span class="sxs-lookup"><span data-stu-id="f7818-128">For an example, see [Create Session Key Example](create-session-key-example.md).</span></span>
6.  <span data-ttu-id="f7818-129">Erstellen Sie einen Inhalts Schlüssel aus einem zufälligen RC4-Initialisierungs Vektor, und füllen Sie eine [**WMDRM- \_ \_ \_ Schlüssel**](wmdrm-import-content-key.md) Struktur zum Importieren von Inhalten aus.</span><span class="sxs-lookup"><span data-stu-id="f7818-129">Create a content key from a random RC4 initialization vector, and fill out a [**WMDRM\_IMPORT\_CONTENT\_KEY**](wmdrm-import-content-key.md) structure.</span></span> <span data-ttu-id="f7818-130">Der Inhalts Schlüssel wird zum Verschlüsseln der Medien Beispiele verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7818-130">The content key is used for encrypting the media samples.</span></span> <span data-ttu-id="f7818-131">Ein Beispiel finden Sie unter [Create Content Key example](create-content-key-example.md).</span><span class="sxs-lookup"><span data-stu-id="f7818-131">For an example, see [Create Content Key Example](create-content-key-example.md).</span></span>
7.  <span data-ttu-id="f7818-132">Verschlüsseln Sie den Inhalts Schlüssel mit dem Sitzungsschlüssel, indem Sie die RC4-Verschlüsselung verwenden.</span><span class="sxs-lookup"><span data-stu-id="f7818-132">Encrypt the content key with the session key, using RC4 encryption.</span></span>
8.  <span data-ttu-id="f7818-133">Extrahieren Sie den Schlüssel für die Computer Zertifikat Sammlung.</span><span class="sxs-lookup"><span data-stu-id="f7818-133">Extract the machine certificate collection key.</span></span> <span data-ttu-id="f7818-134">Ein Beispiel finden Sie unter [Get Machine Certificate example](get-machine-certificate-example.md).</span><span class="sxs-lookup"><span data-stu-id="f7818-134">For an example, see [Get Machine Certificate Example](get-machine-certificate-example.md).</span></span>
9.  <span data-ttu-id="f7818-135">Verschlüsseln Sie den Sitzungsschlüssel mit dem aus dem Zertifikat extrahierten öffentlichen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="f7818-135">Encrypt the session key with the public key extracted from the certificate.</span></span>
10. <span data-ttu-id="f7818-136">Füllen Sie eine [**WMDRM- \_ Import \_ Init \_ struct**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) -Struktur aus.</span><span class="sxs-lookup"><span data-stu-id="f7818-136">Fill out a [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>
11. <span data-ttu-id="f7818-137">Aufrufen der [**IWMDRMWriter3:: setprotectstreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) -Methode, um das SDK zu benachrichtigen, dass die im Writer kommenden Beispiele bereits geschützt sind und für den Import direkt an den Windows Media DRM-Client gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7818-137">Call the [**IWMDRMWriter3::SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) method to notify the SDK that samples coming into the writer are already protected and should be sent directly to the Windows Media DRM client for import.</span></span>
12. <span data-ttu-id="f7818-138">Nennen Sie [**iwmwriter:: BeginWrite**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="f7818-138">Call [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="f7818-139">Die verbleibenden Schritte zum Erstellen einer DRM-geschützten Datei werden im Windows Media Format SDK-Programmier Handbuch dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="f7818-139">The remaining steps for creating a DRM-protected file are documented in the Windows Media Format SDK Programming Guide.</span></span> <span data-ttu-id="f7818-140">Weitere Informationen finden Sie unter [Erstellen geschützter Dateien](creating-protected-files.md).</span><span class="sxs-lookup"><span data-stu-id="f7818-140">For more information, see [Creating Protected Files](creating-protected-files.md).</span></span>

<span data-ttu-id="f7818-141">Der nächste Schritt besteht darin, die einzelnen Medien Beispiele zu durchlaufen, zu verschlüsseln und an das Writer-Objekt zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="f7818-141">The next step is to iterate through each media sample, encrypt it, and pass it to the writer object.</span></span> <span data-ttu-id="f7818-142">Weitere Informationen finden Sie unter [verschlüsseln und Importieren von Medien Beispielen](encrypting-and-importing-media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="f7818-142">For more information, see the [Encrypting and Importing Media Samples](encrypting-and-importing-media-samples.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7818-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f7818-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7818-144">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f7818-144">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="f7818-145">**DRM-Import**</span><span class="sxs-lookup"><span data-stu-id="f7818-145">**DRM Import**</span></span>](drm-import.md)
</dt> </dl>

 

 




