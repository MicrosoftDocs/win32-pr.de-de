---
title: Das sichere Audiopfad-Modell (veraltet)
description: Das sichere Audiopfad-Modell (veraltet)
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- Windows Media-Format-SDK, Microsoft Secure-Audiopfad (SAP)
- Digital Rights Management (DRM), Microsoft Secure-Audiopfad (SAP)
- DRM (Digital Rights Management), Microsoft Secure-Audiopfad (SAP)
- Windows Media-Format-SDK, sicherer Audiopfad (SAP)
- Digital Rights Management (DRM), sicherer Audiopfad (SAP)
- DRM (Digital Rights Management), sicherer Audiopfad (SAP)
- Microsoft Secure-Audiopfad (SAP), Modell
- Sicherer Audiopfad (SAP), Modell
- SAP (sicherer Audiopfad), Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee21d05113deb3c4e8d64141374c87da090f41c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388204"
---
# <a name="the-secure-audio-path-model-deprecated"></a><span data-ttu-id="82d0f-112">Das sichere Audiopfad-Modell (veraltet)</span><span class="sxs-lookup"><span data-stu-id="82d0f-112">The Secure Audio Path Model (deprecated)</span></span>

<span data-ttu-id="82d0f-113">Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows mit einer anderen technischen Lösung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="82d0f-113">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="82d0f-114">Microsoft Secure-Audiopfad (SAP) ist ein Feature von Microsoft Windows® Me und Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="82d0f-114">Microsoft Secure Audio Path (SAP) is a feature of Microsoft Windows® Me and Microsoft Windows XP.</span></span> <span data-ttu-id="82d0f-115">Die Anforderung, dass eine Audiodatei nur über einen sicheren Audiopfad abgespielt werden soll, wird in der DRM-Lizenz angegeben und durch die DRM-Client Komponenten erzwungen.</span><span class="sxs-lookup"><span data-stu-id="82d0f-115">The requirement that an audio file be played only through a secure audio path is specified in the DRM license and enforced by the DRM client components.</span></span> <span data-ttu-id="82d0f-116">Es wird keine zusätzliche Verschlüsselung für reine SAP-Dateien hinzugefügt, wenn Sie anfänglich geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="82d0f-116">There is no extra encryption added for SAP-only files when they are initially protected.</span></span> <span data-ttu-id="82d0f-117">Die SAP-Verschlüsselung wird von den DRM-Komponenten zur Wiedergabezeit automatisch hinzugefügt, ebenso wie der Authentifizierungsprozess für alle Softwarekomponenten, die an der Wiedergabe beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="82d0f-117">The SAP encryption is added automatically by the DRM components at playback time, as is the authentication process for all software components involved in playback.</span></span> <span data-ttu-id="82d0f-118">Die Funktionsweise von SAP ist daher für Anwendungen vollständig transparent, und aus diesem Grund gibt es keine Methode oder Eigenschaft im Windows Media-Format-SDK zum Aktivieren oder Deaktivieren von SAP.</span><span class="sxs-lookup"><span data-stu-id="82d0f-118">The workings of SAP are therefore completely transparent to applications, and that is why there is no method or property in the Windows Media Format SDK for enabling or disabling SAP.</span></span> <span data-ttu-id="82d0f-119">Wenn gewünscht, kann ein Inhalts Besitzer beim Erstellen einer geschützten Datei ein benutzerdefiniertes Header Attribut mit dem Namen "drmHeader. saprequired" hinzufügen, um einen Lizenzserver anzuweisen, die SAP-Anforderung der Lizenz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="82d0f-119">If desired, when creating a protected file a content owner can add a custom header attribute called something like "DRMHeader.SAPRequired" in order to instruct a license server to add the SAP requirement to the license.</span></span> <span data-ttu-id="82d0f-120">Die Implementierung eines solchen Schemas ist der Besitzer des Inhalts und der Lizenz Dienst.</span><span class="sxs-lookup"><span data-stu-id="82d0f-120">The implementation of such a scheme is up to the content owner and the license service.</span></span>

<span data-ttu-id="82d0f-121">Wenn beim aktuellen DRM-Modell SAP nicht angewendet wird, wird der verschlüsselte Inhalt bei der Wiedergabe geschützter digitaler Musik an die DRM-Client Komponente weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="82d0f-121">In the current DRM model, if SAP is not applied, when protected digital music is played, the encrypted content passes to the DRM client component.</span></span> <span data-ttu-id="82d0f-122">Der DRM-Client überprüft, ob die Anwendung und die DRM-Komponente, die das Windows Media Format SDK umfasst, gültig sind.</span><span class="sxs-lookup"><span data-stu-id="82d0f-122">The DRM client verifies that the application and the DRM component incorporating the Windows Media Format SDK are valid.</span></span> <span data-ttu-id="82d0f-123">Wenn Sie gültig sind, entschlüsselt der DRM-Client den Inhalt und sendet ihn an die Anwendung, die ihn dann an die untergeordneten Audiokomponenten sendet.</span><span class="sxs-lookup"><span data-stu-id="82d0f-123">If they are valid, the DRM client decrypts the content and sends it to the application, which then sends it to the lower-level audio components.</span></span> <span data-ttu-id="82d0f-124">An diesem Punkt ist die entschlüsselte Musik für Benutzermodusanwendungen und Plug-ins und Kernelmodustreiber verfügbar, die die entschlüsselten audiobits abfangen können.</span><span class="sxs-lookup"><span data-stu-id="82d0f-124">At this point, the decrypted music is available to user mode applications and plug-ins and kernel mode drivers that can intercept the decrypted audio bits.</span></span>

<span data-ttu-id="82d0f-125">Wenn die Anforderung für den sicheren Audiopfad angewendet wird, wird der Inhalt nicht von der Anwendung entschlüsselt, sondern stattdessen in einem verschlüsselten Zustand an Komponenten auf niedrigerer Ebene, die alle von Microsoft als vertrauenswürdig authentifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="82d0f-125">When the Secure Audio Path requirement is applied, the content is not decrypted by the application, but rather is passed in an encrypted state to lower level components, all of which have been authenticated by Microsoft as trustworthy.</span></span> <span data-ttu-id="82d0f-126">Eine vertrauenswürdige Audiokomponente ist eine, die den Audioinhalt nicht für eine Systemkomponente verfügbar macht, außer für andere bestimmte vertrauenswürdige Komponenten.</span><span class="sxs-lookup"><span data-stu-id="82d0f-126">A trusted audio component is one that does not make the audio content available to any system component except other specific trusted components.</span></span> <span data-ttu-id="82d0f-127">Auf diese Weise bleibt der digitale Inhalt bis hin zur Treiber Ebene geschützt.</span><span class="sxs-lookup"><span data-stu-id="82d0f-127">In this way, the digital content remains protected all the way down to the driver level.</span></span>

<span data-ttu-id="82d0f-128">Im folgenden Diagramm wird das aktuelle Modell im Vergleich zum sicheren Audiopfad-Modell angezeigt.</span><span class="sxs-lookup"><span data-stu-id="82d0f-128">The following diagram displays the current model in comparison to the Secure Audio Path model.</span></span>

![Diagramm des sicheren Audiopfad Modells](images/sap.png)

 

 




