---
title: Exportieren von komprimiertem Inhalt
description: Exportieren von komprimiertem Inhalt
ms.assetid: b312aa5e-d693-4d0a-9d74-b443713cec8c
keywords:
- Windows Media-Format-SDK, DRM-Export
- SDK für Windows Media-Format, exportieren
- Windows Media-Format-SDK, komprimierter Inhalt
- Digital Rights Management (DRM), exportieren
- DRM (Digital Rights Management), exportieren
- Digital Rights Management (DRM), komprimierter Inhalt
- DRM (Digital Rights Management), komprimierter Inhalt
- Erweiterte APIs für den DRM-Client, komprimierter Inhalt
- Erweiterte Client-APIs, komprimierter Inhalt
- Erweiterte APIs für den DRM-Client, exportieren
- Erweiterte Client-APIs, exportieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37781d5575dbffb7103f07307a149f4bd5e9e4fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855919"
---
# <a name="exporting-compressed-content"></a><span data-ttu-id="fd73e-114">Exportieren von komprimiertem Inhalt</span><span class="sxs-lookup"><span data-stu-id="fd73e-114">Exporting Compressed Content</span></span>

<span data-ttu-id="fd73e-115">In diesem Abschnitt wird das Exportieren von Windows Media DRM-geschützten Medien in eine Windows Media-Datei beschrieben, in der die Anwendung komprimierte digitale Mediendaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="fd73e-115">This section describes exporting Windows Media DRM protected media on a Windows Media file where the application receives compressed digital media data.</span></span> <span data-ttu-id="fd73e-116">Zu diesem Zweck muss Ihre Anwendung die Inline Entschlüsselung sämtlicher verschlüsselter Nutzlasten von Windows Media DRM in einer ASF-Datei durchführen.</span><span class="sxs-lookup"><span data-stu-id="fd73e-116">To do this, your application must perform inline decryption of all Windows Media DRM encrypted payloads in an ASF file.</span></span>

> [!Note]  
> <span data-ttu-id="fd73e-117">Eine DRM-Bibliotheks Bibliothek wird Ihnen als Teil des Windows Media DRM-Export Vertrags bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="fd73e-117">An ASF parsing library is supplied to you as part of the Windows Media DRM Export agreement.</span></span>

 

<span data-ttu-id="fd73e-118">Die wichtigsten Schritte zum Exportieren komprimierter Inhalte sind:</span><span class="sxs-lookup"><span data-stu-id="fd73e-118">The primary steps involved in exporting compressed content are:</span></span>

1.  <span data-ttu-id="fd73e-119">Führen Sie bei Bedarf DRM-Individualisierung durch.</span><span class="sxs-lookup"><span data-stu-id="fd73e-119">Perform DRM individualization, if needed.</span></span>
2.  <span data-ttu-id="fd73e-120">Vergewissern Sie sich, dass das Ziel Inhalts Schutz-Schema explizit zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="fd73e-120">Verify that the target content protection scheme is explicitly permitted.</span></span>
3.  <span data-ttu-id="fd73e-121">Erstellen Sie ein Entschlüsselungs-Objekt, um jede ASF-Nutzlast zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="fd73e-121">Create a decryptor object to decrypt each ASF payload.</span></span>
4.  <span data-ttu-id="fd73e-122">Das DRM-System durchläuft die einzelnen ASF-Nutzlasten von Windows Media DRM in RC4, bevor es an die Anwendung übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd73e-122">The DRM system transcrypts each ASF payload from Windows Media DRM into RC4 before passing it to your application.</span></span>

<span data-ttu-id="fd73e-123">Wenn die Größe einer ASF-Nutzlast von der Anwendung während der Durchgängen geändert wird, müssen Sie auch die ASF-Datei neu angleichen.</span><span class="sxs-lookup"><span data-stu-id="fd73e-123">If your application changes the size of an ASF payload during transcryption, you must also remultiplex the ASF file.</span></span>

<span data-ttu-id="fd73e-124">Übergeben Sie an die Stub-Bibliothek ein Windows Media DRM-Export Anwendungs Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="fd73e-124">Pass to the stub library a Windows Media DRM Export Application Certificate.</span></span> <span data-ttu-id="fd73e-125">Das Zertifikat wird überprüft. wenn es gültig ist, generiert das DRM-System einen Initialisierungs Vektor und verschlüsselt es mit RSA OAEP.</span><span class="sxs-lookup"><span data-stu-id="fd73e-125">The certificate is verified, and if it is valid, the DRM system generates an initialization vector and encrypts it using RSA OAEP.</span></span>

-   <span data-ttu-id="fd73e-126">Ein RC4-Sitzungsschlüssel wird für jede Nutzlast erstellt, indem der Initialisierungs Vektor und ein Salt-Wert verkettet werden.</span><span class="sxs-lookup"><span data-stu-id="fd73e-126">An RC4 session key is created for each payload by concatenating the initialization vector and a salt value.</span></span> <span data-ttu-id="fd73e-127">Sie geben den Salt-Wert für die Entschlüsselungs-API an, und Sie müssen ihn durch einen positiven ganzzahligen Wert ungleich 0 (null) für jede Nutzlast erhöhen.</span><span class="sxs-lookup"><span data-stu-id="fd73e-127">You supply the salt value to the decryption API, and you must increment it by a positive non-zero integer value for each payload.</span></span>

<span data-ttu-id="fd73e-128">Sie werden ein Tool von Microsoft als Teil des Windows Media DRM-Export Vertrags bereitstellen, mit dem Sie Ihr eigenes RSA-Schlüsselpaar aus öffentlichem und privatem Schlüssel generieren können.</span><span class="sxs-lookup"><span data-stu-id="fd73e-128">You will be provided a tool by Microsoft as part of the Windows Media DRM export agreement that will enable you to generate your own RSA public/private key pair.</span></span> <span data-ttu-id="fd73e-129">Der öffentliche Schlüssel wird an Microsoft gesendet, wobei Microsoft ihn in ein signiertes Windows Media DRM-Anwendungs Zertifikat integrieren und zurückgeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd73e-129">You will send the public key to Microsoft, where Microsoft will incorporate it into a signed Windows Media DRM Application Certificate, and return it.</span></span>

<span data-ttu-id="fd73e-130">Jede Nutzlast, nachdem Sie mit dem RC4-Entschlüsselungsschlüssel entschlüsselt wurde, muss sofort in die Ausgabe-CPS verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="fd73e-130">Each payload, after it is decrypted using the RC4 decryption key, must be immediately encrypted into the output CPS.</span></span> <span data-ttu-id="fd73e-131">Es gibt weitere Einschränkungen bei der Behandlung unverschlüsselter Nutzlasten, die in den Regeln für Stabilität und Konformität beschrieben werden, die mit dem Windows Media DRM-Export Vertrag einhergehen.</span><span class="sxs-lookup"><span data-stu-id="fd73e-131">There are other restrictions on handling of unencrypted payloads that are outlined in the robustness and compliance rules, which accompany the Windows Media DRM Export agreement.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd73e-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd73e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd73e-133">**Entschlüsselung und erneute Verschlüsselung von ASF-Nutzlast**</span><span class="sxs-lookup"><span data-stu-id="fd73e-133">**ASF Payload Decryption and Re-encryption**</span></span>](asf-payload-decryption-and-re-encryption.md)
</dt> <dt>

[<span data-ttu-id="fd73e-134">**DRM-Export**</span><span class="sxs-lookup"><span data-stu-id="fd73e-134">**DRM Export**</span></span>](drm-export.md)
</dt> <dt>

[<span data-ttu-id="fd73e-135">**Durchführen der DRM-Individualisierung**</span><span class="sxs-lookup"><span data-stu-id="fd73e-135">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> <dt>

[<span data-ttu-id="fd73e-136">**Überprüfung und Initialisierung**</span><span class="sxs-lookup"><span data-stu-id="fd73e-136">**Verification and Initialization**</span></span>](verification-and-initialization.md)
</dt> </dl>

 

 




