---
title: Sicherheitsüberlegungen Text Services-Framework
description: Sicherheitsüberlegungen Text Services-Framework
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- Text Dienst Framework (TSF), Sicherheit
- TSF (Text Dienst Framework), Sicherheit
- Text Dienste, Sicherheit
- TSF-aktivierte Anwendungen, Sicherheit
- Sicherheit für TSF
- Text Dienst Framework (TSF), bewährte Methoden
- TSF (Text Dienst Framework), bewährte Methoden
- TSF-aktivierte Anwendungen, bewährte Methoden
- Text Dienste, bewährte Methoden
- bewährte Methoden für TSF
- Text Services-Framework (TSF), Fehlerüberprüfung
- TSF (Text Dienst Framework), Fehlerüberprüfung
- TSF-aktivierte Anwendungen, Fehlerüberprüfung
- Text Dienste, Fehlerüberprüfung
- Fehlerüberprüfung
- Text Dienst Framework (TSF), digitale Signaturen
- TSF (Text Dienst Framework), digitale Signaturen
- Text Dienste, digitale Signaturen
- TSF-aktivierte Anwendungen, digitale Signaturen
- Digitale Signaturen
- Text Dienst Framework (TSF), LoadLibrary-Aufrufe
- TSF (Text Services Framework), LoadLibrary-Aufrufe
- Text Dienste, LoadLibrary-Aufrufe
- TSF-aktivierte Anwendungen, LoadLibrary-Aufrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d71966106cde0f59d39442f7e2bf9b2a216cd94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342349"
---
# <a name="security-considerations-text-services-framework"></a><span data-ttu-id="c409e-127">Sicherheitsüberlegungen: Text Services-Framework</span><span class="sxs-lookup"><span data-stu-id="c409e-127">Security Considerations: Text Services Framework</span></span>

## <a name="best-practices-for-developing-with-tsf"></a><span data-ttu-id="c409e-128">Bewährte Methoden für die Entwicklung mit TSF</span><span class="sxs-lookup"><span data-stu-id="c409e-128">Best Practices for Developing with TSF</span></span>

-   <span data-ttu-id="c409e-129">**Digitale Signaturen:** Text Dienstanbieter sollten digitale Signaturen mit Ihren binären ausführbaren Dateien bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c409e-129">**Digital Signatures:** Text service providers should provide digital signatures with their binary executables.</span></span> <span data-ttu-id="c409e-130">Ein registrierter Text Dienst hat Zugriff auf Systemthreads und kann Informationen verfügbar machen, auf die andernfalls nicht zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c409e-130">A registered text service has access to system threads and could expose information that would otherwise not be accessible.</span></span> <span data-ttu-id="c409e-131">Um einen stabilen und sicheren Betrieb sicherzustellen, muss der Benutzer die digitale Signatur eines Text Dienstanbieter überprüfen, bevor der Text Dienst geladen werden darf.</span><span class="sxs-lookup"><span data-stu-id="c409e-131">To help ensure stable and secure operation, the user should verify the digital signature of a text service before the text service is allowed to load.</span></span> <span data-ttu-id="c409e-132">Das richtige Verfahren zum Erstellen einer digitalen Signatur finden Sie unter [Einführung in die Code Signatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c409e-132">See [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) for the proper procedure to create a digital signature.</span></span>
-   <span data-ttu-id="c409e-133">**Fehlerüberprüfung:** Jeder Methoden-oder Funktionsaufrufe sollte auf Erfolg geprüft werden.</span><span class="sxs-lookup"><span data-stu-id="c409e-133">**Error Checking:** Each method or function call should be checked for success.</span></span> <span data-ttu-id="c409e-134">Im Fall eines Fehlers sollten die verbleibenden Methoden-oder Funktionsaufrufe übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="c409e-134">In the event of failure, the remaining method or function calls should be skipped.</span></span> <span data-ttu-id="c409e-135">Die meisten Codebeispiele in dieser Dokumentation enthalten nur eine begrenzte Fehlerüberprüfung oder gar keine Fehlerüberprüfung, um zu vermeiden, dass der zu Veranschaulichung Punkt verdeckt wird.</span><span class="sxs-lookup"><span data-stu-id="c409e-135">Most of the code examples in this documentation have limited error checking, or none at all, to avoid obscuring the point to be illustrated.</span></span> <span data-ttu-id="c409e-136">Sie sollten keine Beispiele aus der Dokumentation direkt in den Produktionscode einfügen. Stattdessen sollten Sie die Beispiele verbessern, indem Sie eine eigene Fehlerüberprüfung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c409e-136">You should not paste examples from the documentation directly into production code; rather, you should enhance the examples by adding your own error checking.</span></span>

-   <span data-ttu-id="c409e-137">**LoadLibrary-Aufrufe:** Zum Abrufen eines Zeigers auf eine der [TSF-Funktionen](text-services-framework-functions.md)müssen Sie [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)verwenden.</span><span class="sxs-lookup"><span data-stu-id="c409e-137">**LoadLibrary Calls:** To obtain a pointer to any of the [TSF functions](text-services-framework-functions.md), you will need to use [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="c409e-138">Es ist jedoch wichtig, die Prozeduren zum Formatieren des dll-Pfadnamens zu befolgen, wie in der **LoadLibrary** -Dokumentation angegeben.</span><span class="sxs-lookup"><span data-stu-id="c409e-138">However, it is important to follow procedures for formatting the DLL path name, as given in **LoadLibrary** documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c409e-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c409e-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c409e-140">Bewährte Sicherheitsmethoden</span><span class="sxs-lookup"><span data-stu-id="c409e-140">Security Best Practices</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

<span data-ttu-id="c409e-141">[Einführung in die Codesignatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c409e-141">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c409e-142">TSF-Funktionen</span><span class="sxs-lookup"><span data-stu-id="c409e-142">TSF functions</span></span>](text-services-framework-functions.md)
</dt> <dt>

[<span data-ttu-id="c409e-143">LoadLibrary</span><span class="sxs-lookup"><span data-stu-id="c409e-143">LoadLibrary</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="c409e-144">GetProcAddress</span><span class="sxs-lookup"><span data-stu-id="c409e-144">GetProcAddress</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 