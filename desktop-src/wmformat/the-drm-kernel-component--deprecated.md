---
title: Die DRM-Kernel Komponente (veraltet)
description: Die DRM-Kernel Komponente (veraltet)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- Windows Media-Format-SDK, Microsoft Secure-Audiopfad (SAP)
- Digital Rights Management (DRM), Microsoft Secure-Audiopfad (SAP)
- DRM (Digital Rights Management), Microsoft Secure-Audiopfad (SAP)
- Windows Media-Format-SDK, sicherer Audiopfad (SAP)
- Digital Rights Management (DRM), sicherer Audiopfad (SAP)
- DRM (Digital Rights Management), sicherer Audiopfad (SAP)
- Windows Media-Format-SDK, DRM-Kernel Komponente
- Digital Rights Management (DRM), Kernel Komponente
- DRM (Digital Rights Management), Kernel Komponente
- Microsoft Secure-Audiopfad (SAP), DRM-Kernel Komponente
- Secure-Audiopfad (SAP), DRM-Kernel Komponente
- SAP (sicherer Audiopfad), DRM-Kernel Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacc0074fdf390ca478ed41b59188ad42ec193c1
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039822"
---
# <a name="the-drm-kernel-component-deprecated"></a><span data-ttu-id="5ad19-115">Die DRM-Kernel Komponente (veraltet)</span><span class="sxs-lookup"><span data-stu-id="5ad19-115">The DRM Kernel Component (deprecated)</span></span>

<span data-ttu-id="5ad19-116">Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows mit einer anderen technischen Lösung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5ad19-116">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="5ad19-117">Im SAP-Modell (Secure audiopath) von Microsoft bietet die DRM-Kernel Komponente zwei grundlegende Features, mit denen die Integrität verschlüsselter Musik geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="5ad19-117">In the Microsoft Secure Audio Path (SAP) model, the DRM kernel component provides two basic features that protect the integrity of encrypted music.</span></span>

<span data-ttu-id="5ad19-118">Zuerst werden die DRM-Client Komponente und die DRM-Kernel Komponente bei der Wiedergabe einer Musikdatei kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="5ad19-118">First, the DRM client component and the DRM kernel component are in communication when a music file is played.</span></span> <span data-ttu-id="5ad19-119">Diese Kommunikation zwischen Komponenten verhindert, dass jemand das verschlüsselte Signal manipuliert oder falsche Informationen einfügt.</span><span class="sxs-lookup"><span data-stu-id="5ad19-119">This communication between components prevents anyone from tampering with the encrypted signal or from inserting false information.</span></span>

<span data-ttu-id="5ad19-120">Zweitens entschlüsselt die DRM-Kernel Komponente das Musiksignal erst, wenn alle verbleibenden Komponenten authentifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="5ad19-120">Second, the DRM kernel component does not decrypt the music signal until all remaining components are authenticated.</span></span> <span data-ttu-id="5ad19-121">Das heißt, vor dem Entschlüsseln von Inhalten und der Übergabe an die nächste Systemkomponente überprüft die DRM-Kernel Komponente jede Komponente, die im Pfad zur Audiokarte verbleibt (jede Komponente, die auf den Inhalt zugreifen kann) und überprüft, ob diese Komponenten mit einem Zertifikat von Microsoft signiert sind.</span><span class="sxs-lookup"><span data-stu-id="5ad19-121">That is, before decrypting content and passing it to the next system component, the DRM kernel component checks each component that remains in the path to the sound card (each component that can access the content) and verifies that these components are signed with a certificate from Microsoft.</span></span> <span data-ttu-id="5ad19-122">Eine nicht signierte Komponente weist möglicherweise auf eine verdächtige Komponente oder einen bösartigen Treiber hin.</span><span class="sxs-lookup"><span data-stu-id="5ad19-122">An unsigned component might indicate a suspicious component or a malicious driver.</span></span> <span data-ttu-id="5ad19-123">Wenn also die DRM-Kernel Komponente die verbleibenden Komponenten überprüft, wird das Signal angehalten und kann nicht wiedergegeben werden, wenn eine Komponente den Test nicht bestanden hat.</span><span class="sxs-lookup"><span data-stu-id="5ad19-123">So, when the DRM kernel component validates remaining components, if any component fails this test, the signal is halted and cannot be played.</span></span> <span data-ttu-id="5ad19-124">Wenn alle Komponenten die Überprüfung bestehen, entschlüsselt die DRM-Kernel Komponente andernfalls die Musik und übergibt sie an die nächste Komponente.</span><span class="sxs-lookup"><span data-stu-id="5ad19-124">Otherwise, if all components pass validation, the DRM kernel component decrypts the music and passes it to the next component.</span></span>

<span data-ttu-id="5ad19-125">Microsoft signiert Treiber, die die Tests der Windows®-Hardware Qualität (WHQL) bestanden haben, Digital, um Benutzern zu gewährleisten, dass Sie die Treiber mit der höchsten Qualität verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ad19-125">Microsoft digitally signs drivers that pass the Windows® Hardware Quality Lab (WHQL) tests to assure users that they are using the highest-quality drivers.</span></span> <span data-ttu-id="5ad19-126">Diese Vorgehensweise ist Standard und garantiert die Authentizität von Komponenten, da die Signatur nicht gefälscht werden kann, und der Code kann nicht geändert werden, ohne die Signatur zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="5ad19-126">This practice is standard and guarantees the authenticity of components because the signature cannot be forged, nor can the code be modified without destroying the signature.</span></span> <span data-ttu-id="5ad19-127">Treiber, die für einen sicheren Audiopfad zertifiziert sind, müssen die Audiodaten, die Sie verarbeiten, vor dem Zugriff durch nicht vertrauenswürdige Komponenten schützen.</span><span class="sxs-lookup"><span data-stu-id="5ad19-127">Drivers that are certified for Secure Audio Path must protect the audio data they process from access by untrusted components.</span></span> 

<span data-ttu-id="5ad19-128">Treiber, die in der Windows Millennium Edition und Windows XP enthalten sind, werden für einen sicheren Audiopfad aktualisiert und signiert.</span><span class="sxs-lookup"><span data-stu-id="5ad19-128">Drivers included with Windows Millennium Edition and Windows XP are updated for Secure Audio Path and signed.</span></span> <span data-ttu-id="5ad19-129">Treiber, die nicht für die Verwendung mit Windows Me oder Windows XP signiert sind, können geschützte Musik nicht wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="5ad19-129">Drivers that are not signed for use with Windows Me or Windows XP cannot play protected music.</span></span> <span data-ttu-id="5ad19-130">Treiber Hersteller können aktualisierte Versionen ihrer von WHQL signierten Treiber neu ausstellen und im Internet veröffentlichen, damit Consumer Sie herunterladen können.</span><span class="sxs-lookup"><span data-stu-id="5ad19-130">Driver manufacturers can reissue updated versions of their drivers that are signed by WHQL, and publish them on the Internet for consumers to download.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ad19-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5ad19-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ad19-132">**Microsoft Secure-Audiopfad**</span><span class="sxs-lookup"><span data-stu-id="5ad19-132">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




