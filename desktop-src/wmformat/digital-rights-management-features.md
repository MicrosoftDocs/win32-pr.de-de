---
title: Features digitaler Rights Management
description: Features digitaler Rights Management
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- Windows Media-Format-SDK, DRM-Features
- Digital Rights Management (DRM), Features
- DRM (Digital Rights Management), Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd9c30b350fdf430d5b20bbe112c5309ac9da4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728009"
---
# <a name="digital-rights-management-features"></a><span data-ttu-id="b9176-106">Features digitaler Rights Management</span><span class="sxs-lookup"><span data-stu-id="b9176-106">Digital Rights Management Features</span></span>

<span data-ttu-id="b9176-107">\[Das Windows Media DRM-Feature ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9176-107">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="b9176-108">Verwenden Sie stattdessen [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="b9176-108">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="b9176-109">Die digitale Rechteverwaltung (Digital Rights Management, DRM) ist eine Technologie, mit der Inhalts Besitzer digitale Mediendateien schützen können, indem Sie mit einem Schlüssel verschlüsselt werden (ein Datenelement, das den Inhalt sperrt und entsperrt).</span><span class="sxs-lookup"><span data-stu-id="b9176-109">Digital rights management (DRM) is a technology that content owners can use to protect digital media files by encrypting them with a key (a piece of data that locks and unlocks the content).</span></span> <span data-ttu-id="b9176-110">Zum Wiedergeben einer geschützten ASF-Datei muss ein Consumer eine separate Lizenz abrufen, die den Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="b9176-110">To play a protected ASF file, a consumer must obtain a separate license containing the key.</span></span> <span data-ttu-id="b9176-111">Jede Lizenz enthält auch Rechte, die vom Inhalts Besitzer oder Lizenz Aussteller festgelegt werden, die angeben, wie der Consumer die Datei verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="b9176-111">Each license also contains rights, determined by the content owner or license issuer, which specify how the consumer can use the file.</span></span> <span data-ttu-id="b9176-112">Mithilfe der DRM-Technologie können Inhalts Besitzer Lieder, Videos und andere digitale Mediendateien über das Internet in einem geschützten Dateiformat bereitstellen und die Verwendung Ihrer digitalen Inhalte steuern.</span><span class="sxs-lookup"><span data-stu-id="b9176-112">Using DRM technology, content owners can deliver songs, videos, and other digital media files over the Internet in a protected file format and control the use of their digital content.</span></span> <span data-ttu-id="b9176-113">Die Microsoft DRM-Technologie wird auch vom Windows Media Rights Manager, dem Windows Media Encoder und Windows Media Player unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9176-113">Microsoft DRM technology is also supported by the Windows Media Rights Manager, the Windows Media Encoder, and Windows Media Player.</span></span> <span data-ttu-id="b9176-114">Weitere Hintergrundinformationen zur DRM-Technologie von Microsoft finden Sie auf der [Microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media)-Website.</span><span class="sxs-lookup"><span data-stu-id="b9176-114">For more background information on Microsoft's DRM technology, see the [Microsoft Windows Media Web site](https://support.microsoft.com/help/17946/windows-media).</span></span>

> [!Note]  
> <span data-ttu-id="b9176-115">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9176-115">DRM is not supported by the x64-based version of this SDK.</span></span>

 

<span data-ttu-id="b9176-116">In den folgenden Abschnitten werden die wichtigsten DRM-bezogenen Features des Windows Media Format SDK erläutert.</span><span class="sxs-lookup"><span data-stu-id="b9176-116">The following sections discuss the main DRM-related features of the Windows Media Format SDK.</span></span>



| <span data-ttu-id="b9176-117">`Section`</span><span class="sxs-lookup"><span data-stu-id="b9176-117">Section</span></span>                                                                                            | <span data-ttu-id="b9176-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9176-118">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9176-119">DRM-Grundlagen</span><span class="sxs-lookup"><span data-stu-id="b9176-119">DRM Basics</span></span>](drm-basics.md)                                                                       | <span data-ttu-id="b9176-120">Bietet eine kurze Übersicht über die DRM-Funktionalität, die vom SDK für den Windows Media-Format bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b9176-120">Provides a brief overview of the DRM functionality provided by the Windows Media Format SDK.</span></span>                                         |
| [<span data-ttu-id="b9176-121">DRM-Versionen</span><span class="sxs-lookup"><span data-stu-id="b9176-121">DRM Versions</span></span>](drm-versions.md)                                                                   | <span data-ttu-id="b9176-122">Beschreibt die Hauptunterschiede zwischen den Versionen des DRM-Schutzes, die für-Anwendungen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b9176-122">Describes the main differences between the versions of DRM protection available to applications.</span></span>                                     |
| [<span data-ttu-id="b9176-123">Live DRM</span><span class="sxs-lookup"><span data-stu-id="b9176-123">Live DRM</span></span>](live-drm.md)                                                                           | <span data-ttu-id="b9176-124">Hier werden die Szenarien beschrieben, die durch den "on-the-the"-DRM-Schutz</span><span class="sxs-lookup"><span data-stu-id="b9176-124">Describes the scenarios made possible by "on the fly" DRM protection.</span></span>                                                                |
| [<span data-ttu-id="b9176-125">DRM-Individualisierung</span><span class="sxs-lookup"><span data-stu-id="b9176-125">DRM Individualization</span></span>](drm-individualization.md)                                                 | <span data-ttu-id="b9176-126">Beschreibt das Anwendungs Sicherheits Upgrade, das von DRM-Inhalts Besitzern oder Lizenz Ausstellern angefordert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b9176-126">Describes the application security upgrade that DRM content owners or license issuers can require.</span></span>                                   |
| [<span data-ttu-id="b9176-127">Sichern und Wiederherstellen von DRM-Lizenzen</span><span class="sxs-lookup"><span data-stu-id="b9176-127">Backing Up and Restoring of DRM Licenses</span></span>](backing-up-and-restoring-of-drm-licenses.md)           | <span data-ttu-id="b9176-128">Beschreibt die vor-und Nachteile, die es Benutzern ermöglichen, ihre Inhalts Lizenzen zu sichern und wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="b9176-128">Describes the pros and cons of permitting users to back up and restore their content licenses.</span></span>                                       |
| [<span data-ttu-id="b9176-129">Anzeigen von DRM-Attributen im Metadateneditor</span><span class="sxs-lookup"><span data-stu-id="b9176-129">Viewing DRM Attributes in the Metadata Editor</span></span>](viewing-drm-attributes-in-the-metadata-editor.md) | <span data-ttu-id="b9176-130">Beschreibt die Funktionen dieses DRM-Hilfsobjekts und der Szenarien, die unterstützt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b9176-130">Describes the capabilities of this DRM helper object and the scenarios it was designed to support.</span></span>                                   |
| [<span data-ttu-id="b9176-131">Ausgabe Schutz Ebenen</span><span class="sxs-lookup"><span data-stu-id="b9176-131">Output Protection Levels</span></span>](output-protection-levels.md)                                           | <span data-ttu-id="b9176-132">In diesem Thema wird beschrieben, wie durch Ausgabe Schutz Ebenen DRM-Lizenzen der Version 10 flexibler werden</span><span class="sxs-lookup"><span data-stu-id="b9176-132">Describes how Output Protection Levels make DRM version 10 licenses more flexible.</span></span>                                                   |
| [<span data-ttu-id="b9176-133">Lizenz Sperrung</span><span class="sxs-lookup"><span data-stu-id="b9176-133">License Revocation</span></span>](license-revocation.md)                                                       | <span data-ttu-id="b9176-134">Beschreibt die Lizenz Sperrung.</span><span class="sxs-lookup"><span data-stu-id="b9176-134">Describes license revocation.</span></span>                                                                                                        |
| [<span data-ttu-id="b9176-135">Windows Media DRM 10 für Netzwerkgeräte</span><span class="sxs-lookup"><span data-stu-id="b9176-135">Windows Media DRM 10 for Network Devices</span></span>](windows-media-drm-10-for-network-devices.md)           | <span data-ttu-id="b9176-136">Führt Windows Media DRM 10 für Netzwerkgeräte und deren Implementierung in diesem SDK ein.</span><span class="sxs-lookup"><span data-stu-id="b9176-136">Introduces Windows Media DRM 10 for Network Devices and its implementation in this SDK.</span></span>                                              |
| [<span data-ttu-id="b9176-137">Microsoft Secure-Audiopfad</span><span class="sxs-lookup"><span data-stu-id="b9176-137">Microsoft Secure Audio Path</span></span>](microsoft-secure-audio-path--deprecated.md)                         | <span data-ttu-id="b9176-138">Beschreibt die Microsoft Secure-Audiopfad-Architektur, die das höchste Maß an Schutz für geschützte Audioinhalte bietet.</span><span class="sxs-lookup"><span data-stu-id="b9176-138">Describes the Microsoft Secure Audio Path architecture, which provides the highest degree of protection for protected audio content.</span></span> |
| [<span data-ttu-id="b9176-139">Wiedergabelisten brennen</span><span class="sxs-lookup"><span data-stu-id="b9176-139">Playlist Burning</span></span>](playlist-burning.md)                                                           | <span data-ttu-id="b9176-140">Beschreibt die Funktion zum Brennen der Wiedergabeliste von DRM und wie Sie im Windows Media-Format-SDK unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b9176-140">Describes the playlist-burning feature of DRM and how it is supported in the Windows Media Format SDK.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="b9176-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b9176-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9176-142">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="b9176-142">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="b9176-143">**Features**</span><span class="sxs-lookup"><span data-stu-id="b9176-143">**Features**</span></span>](features.md)
</dt> </dl>

 

 