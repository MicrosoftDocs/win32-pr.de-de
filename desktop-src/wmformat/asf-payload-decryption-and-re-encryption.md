---
title: Entschlüsselung und erneute Verschlüsselung von ASF-Nutzlast
description: Entschlüsselung und erneute Verschlüsselung von ASF-Nutzlast
ms.assetid: 0a8c996d-2167-483a-93af-6fe22f0efaf1
keywords:
- SDK für Windows Media-Format, ASF-Nutz Last Entschlüsselung und erneute Verschlüsselung
- Windows Media-Format-SDK, Nutzlast entschlüsseln und erneute Verschlüsselung
- SDK für Windows Media-Format, Entschlüsselung
- SDK für Windows Media-Format, erneute Verschlüsselung
- Digital Rights Management (DRM), ASF-Nutz Last Entschlüsselung und erneute Verschlüsselung
- DRM (Digital Rights Management), ASF-Nutz Last Entschlüsselung und erneute Verschlüsselung
- Digital Rights Management (DRM), Nutzlast entschlüsseln und erneute Verschlüsselung
- DRM (Digital Rights Management), Nutzlast entschlüsseln und erneute Verschlüsselung
- Digital Rights Management (DRM), Entschlüsselung
- DRM (Digital Rights Management), Entschlüsselung
- Digital Rights Management (DRM), erneute Verschlüsselung
- DRM (Digital Rights Management), erneute Verschlüsselung
- Erweiterte APIs für den DRM-Client, die Entschlüsselung der ASF-Nutzlast und die erneute Verschlüsselung
- Erweiterte Client-APIs, ASF-Nutz Last Entschlüsselung und erneute Verschlüsselung
- Erweiterte APIs für den DRM-Client, Nutzlast entschlüsseln und erneute Verschlüsselung
- Erweiterte Client-APIs, Nutzlast entschlüsseln und erneute Verschlüsselung
- Erweiterte APIs für den DRM-Client, Entschlüsselung
- Erweiterte Client-APIs, Entschlüsselung
- Erweiterte APIs für den DRM-Client, erneute Verschlüsselung
- Erweiterte Client-APIs, erneute Verschlüsselung
- Advanced Systems Format (ASF), erneute Verschlüsselung
- ASF (Advanced Systems Format), erneute Verschlüsselung
- Advanced Systems Format (ASF), Entschlüsselung
- ASF (Advanced Systems Format), Entschlüsselung
- Advanced Systems Format (ASF), Nutzlast entschlüsseln und erneute Verschlüsselung
- ASF (Advanced Systems Format), Nutzlast entschlüsseln und erneute Verschlüsselung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c6dcab1d483b737b6b05636b51b8af0502350
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707866"
---
# <a name="asf-payload-decryption-and-re-encryption"></a><span data-ttu-id="24cb0-129">Entschlüsselung und erneute Verschlüsselung von ASF-Nutzlast</span><span class="sxs-lookup"><span data-stu-id="24cb0-129">ASF Payload Decryption and Re-encryption</span></span>

<span data-ttu-id="24cb0-130">In den folgenden Schritten werden die Aktionen beschrieben, die eine Anwendung zum Entschlüsseln und erneuten Verschlüsseln der einzelnen Nutzlasten ausführen muss:</span><span class="sxs-lookup"><span data-stu-id="24cb0-130">The steps below describe the actions that an application must complete to decrypt and re-encrypt each payload:</span></span>

1.  <span data-ttu-id="24cb0-131">Erhöhen Sie den Salt-Wert.</span><span class="sxs-lookup"><span data-stu-id="24cb0-131">Increment the salt value.</span></span>
2.  <span data-ttu-id="24cb0-132">Übergeben Sie die mit Windows Media DRM verschlüsselte Nutzlast (mit Windows Media DRM) und den Salt-Wert an die Entschlüsselungs Funktion [**iwmdrmentschlüsseln::D ecrypt**](iwmdrmdecrypt-decrypt.md), die die Nutzlast zurückgibt, die mithilfe des öffentlichen RC4-Schlüssels verschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="24cb0-132">Pass the payload (encrypted with Windows Media DRM) and the salt value to the decryption function, [**IWMDRMDecrypt::Decrypt**](iwmdrmdecrypt-decrypt.md), which will return the payload, encrypted using the RC4 public key.</span></span>
3.  <span data-ttu-id="24cb0-133">Leiten Sie einen vorübergehendes RC4-Schlüssel ab, indem Sie einen SHA-1-Hash des Initialisierungs Vektors anwenden, der mit dem Salt-Wert verkettet ist.</span><span class="sxs-lookup"><span data-stu-id="24cb0-133">Derive a transitory RC4 key by applying an SHA-1 hash of the initialization vector concatenated with the salt value.</span></span>
4.  <span data-ttu-id="24cb0-134">Verwenden Sie Ihren vorübergehendes-Schlüssel, um die Nutzlast zu entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="24cb0-134">Use your transitory key to decrypt the payload.</span></span>
5.  <span data-ttu-id="24cb0-135">Erneutes Verschlüsseln der Nutzlast mit dem autorisierten Inhalts Schutzschema gemäß den Windows Media DRM-Regeln zum Exportieren von Konformität und Stabilität.</span><span class="sxs-lookup"><span data-stu-id="24cb0-135">Immediately re-encrypt the payload with the authorized content protection scheme according to the Windows Media DRM export compliance and robustness rules.</span></span>
6.  <span data-ttu-id="24cb0-136">Suchen Sie die nächste Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="24cb0-136">Locate the next payload.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24cb0-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24cb0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24cb0-138">**Exportieren von komprimiertem Inhalt**</span><span class="sxs-lookup"><span data-stu-id="24cb0-138">**Exporting Compressed Content**</span></span>](exporting-compressed-content.md)
</dt> </dl>

 

 




