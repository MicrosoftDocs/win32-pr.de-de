---
title: Individualisieren von DRM-Anwendungen
description: Individualisieren von DRM-Anwendungen
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- Windows Media-Format-SDK, Individualisieren von DRM-Anwendungen
- Windows Media-Format-SDK, Anwendungs Individualisierung
- Advanced Systems Format (ASF), Individualisieren von DRM-Anwendungen
- ASF (Advanced Systems Format), Individualisieren von DRM-Anwendungen
- Advanced Systems Format (ASF), Anwendungs Individualisierung
- ASF (Advanced Systems Format), Anwendungs Individualisierung
- Digital Rights Management (DRM), Individual Anwendungen
- DRM (Digital Rights Management), Individual Anwendungen
- Digital Rights Management (DRM), Anwendungs Individualisierung
- DRM (Digital Rights Management), Anwendungs Individualisierung
- Anwendungs Individualisierung
- Individualisieren von DRM-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c3fc0166332c52e39fc0882238fa9009aa0cc1
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "103948502"
---
# <a name="individualizing-drm-applications"></a><span data-ttu-id="43918-115">Individualisieren von DRM-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="43918-115">Individualizing DRM Applications</span></span>

<span data-ttu-id="43918-116">Um die Sicherheit zu erhöhen, kann die DRM-Komponente der Anwendungen *individuell individualisiert* werden.</span><span class="sxs-lookup"><span data-stu-id="43918-116">To increase security, the DRM component of applications can be *individualized*.</span></span> <span data-ttu-id="43918-117">Eine individualisierte Anwendung ist eine Anwendung, die ein Upgrade auf die DRM-Komponenten erhalten hat, die Sie von allen anderen Kopien der gleichen Anwendung unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="43918-117">An individualized application is one that has received an upgrade to its DRM components that differentiates it from all other copies of the same application.</span></span> <span data-ttu-id="43918-118">Inhalts Besitzer können verlangen, dass Ihre geschützten Dateien nur in einer Anwendung wiedergegeben werden, die individuell ist.</span><span class="sxs-lookup"><span data-stu-id="43918-118">Content owners can require that their protected files be played only on an application that has been individualized.</span></span>

<span data-ttu-id="43918-119">Der Individualisierungsprozess wird gestartet, wenn die Anwendung den Microsoft-Individualisierungs Dienst kontaktiert, der dann ein Sicherheits Upgrade auf dem Computer des Benutzers installiert.</span><span class="sxs-lookup"><span data-stu-id="43918-119">The individualization process starts when the application contacts the Microsoft Individualization Service, which then installs a security upgrade on the user's computer.</span></span> <span data-ttu-id="43918-120">Da der Individualisierungs Dienst Informationen vom Benutzer verarbeitet, müssen Sie die Microsoft-Datenschutzrichtlinie anzeigen oder einen Link zu dieser Seite auf der Microsoft-Website angeben: <https://privacy.microsoft.com/privacystatement> .</span><span class="sxs-lookup"><span data-stu-id="43918-120">Because the Individualization Service handles information from the user, you must display the Microsoft privacy policy or provide a link to that page at the Microsoft Web site: <https://privacy.microsoft.com/privacystatement>.</span></span>

<span data-ttu-id="43918-121">Die Individualisierung kann auf unterschiedliche Weise durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="43918-121">Individualization can be accomplished in different ways.</span></span> <span data-ttu-id="43918-122">So kann z. b. eine Individualisierung erfolgen, wenn ein Benutzer eine geschützte Datei spielt.</span><span class="sxs-lookup"><span data-stu-id="43918-122">For example, individualization can take place when a user plays a protected file.</span></span> <span data-ttu-id="43918-123">Die Lizenz Anforderung wird an den [*Windows Media License Service*](wmformat-glossary.md)gesendet, der das Zertifikat der Anwendung überprüft, die die [*Lizenz*](wmformat-glossary.md)anfordert.</span><span class="sxs-lookup"><span data-stu-id="43918-123">The license request is sent to the [*Windows Media License Service*](wmformat-glossary.md), which inspects the certificate of the application requesting the [*license*](wmformat-glossary.md).</span></span> <span data-ttu-id="43918-124">Wenn die DRM-Komponente der Anwendung nicht individualisiert wurde, lehnt der Windows Media License Service die Lizenz ab, da es sich hierbei um die Richtlinie von Windows Media License Service handelt, die nur für individualisierte Spieler Lizenzen ausgibt.</span><span class="sxs-lookup"><span data-stu-id="43918-124">If the DRM component of the application has not been individualized, Windows Media License Service refuses to issue the license, because it is the policy of Windows Media License Service to issue licenses only to individualized players.</span></span> <span data-ttu-id="43918-125">Die Anwendung kann dann den Benutzer benachrichtigen, dass ein Upgrade der Anwendung ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="43918-125">The application can then notify the user that the application must be upgraded.</span></span> <span data-ttu-id="43918-126">Wenn der Benutzer zustimmt, wird ein Sicherheits Upgrade bereitgestellt, um die DRM-Komponente der Anwendung zu individualisieren.</span><span class="sxs-lookup"><span data-stu-id="43918-126">If the user agrees, a security upgrade is provided to individualize the DRM component of the application.</span></span>

<span data-ttu-id="43918-127">Um eine bessere Benutzer Leistung zu erzielen, können Sie den Individualisierungsprozess während des Setups als Sicherheits upgradeschritt initiieren. Anschließend wird der Benutzer nicht unterbrochen, um beim Versuch, eine geschützte Datei wiederzugeben, ein Sicherheits Upgrade zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="43918-127">For a better user experience, you can initiate the individualization process as a security upgrade step during setup; then the user is not interrupted to get a security upgrade while trying to play a protected file.</span></span> <span data-ttu-id="43918-128">Sie können die Individualisierung auch durch Hinzufügen eines Menübefehls oder einer Schaltfläche zur **Sicherheitsaktualisierung** zur Anwendung aktiv fördern.</span><span class="sxs-lookup"><span data-stu-id="43918-128">You can also actively encourage individualization by adding a **Security Upgrade** menu command or button to the application.</span></span>

> [!Note]  
> <span data-ttu-id="43918-129">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="43918-129">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="43918-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43918-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43918-131">**Features digitaler Rights Management**</span><span class="sxs-lookup"><span data-stu-id="43918-131">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="43918-132">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="43918-132">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




