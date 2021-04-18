---
title: Microsoft Windows Media DRM-Client Schnittstellen
description: Microsoft Windows Media DRM-Client Schnittstellen
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- Windows Media-Format-SDK, Schnittstellen
- Digital Rights Management (DRM), Schnittstellen
- DRM (Digital Rights Management), Schnittstellen
- Erweiterte APIs des DRM-Clients, Schnittstellen
- Erweiterte Client-APIs, Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4e259ef5b8ef410db072a7f942d139f682bc90
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391373"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a><span data-ttu-id="c2bbd-108">Microsoft Windows Media DRM-Client Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c2bbd-108">Microsoft Windows Media DRM Client Interfaces</span></span>

<span data-ttu-id="c2bbd-109">In der folgenden Tabelle werden die von den Windows Media DRM-Client-APIs unterstützten Schnittstellen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-109">The following table describes the interfaces supported by the Windows Media DRM Client APIs.</span></span>



| <span data-ttu-id="c2bbd-110">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c2bbd-110">Interface</span></span>                                                                    | <span data-ttu-id="c2bbd-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2bbd-111">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2bbd-112">**Idrmstatus Callback**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-112">**IDRMStatusCallback**</span></span>](idrmstatuscallback.md)                             | <span data-ttu-id="c2bbd-113">Stellt die Definition für einen Status Rückruf bereit, den Sie implementieren können, um asynchrone DRM-Vorgänge zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-113">Provides the definition for a status callback that you can implement to handle asynchronous DRM operations.</span></span>     |
| [<span data-ttu-id="c2bbd-114">**Iwmdrmentschlüsseln**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-114">**IWMDRMDecrypt**</span></span>](iwmdrmdecrypt.md)                                       | <span data-ttu-id="c2bbd-115">Stellt eine Methode für das Entschlüsseln von Inhalten bereit.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-115">Provides a method for decrypting content.</span></span>                                                                       |
| [<span data-ttu-id="c2bbd-116">**Iwmdrmencrypt**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-116">**IWMDRMEncrypt**</span></span>](iwmdrmencrypt.md)                                       | <span data-ttu-id="c2bbd-117">Bietet eine Methode zum Verschlüsseln von Daten an Ort und Stelle.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-117">Provides a method for encrypting data in place.</span></span>                                                                 |
| [<span data-ttu-id="c2bbd-118">**Iwmdrmencryptscatter**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-118">**IWMDRMEncryptScatter**</span></span>](iwmdrmencryptscatter.md)                         | <span data-ttu-id="c2bbd-119">Verschlüsselt Daten aus nicht zusammenhängenden Blöcken.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-119">Encrypts data from non-contiguous blocks.</span></span>                                                                       |
| [<span data-ttu-id="c2bbd-120">**Iwmdrmeventgenerator**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-120">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)                         | <span data-ttu-id="c2bbd-121">Erweiterung der **imfmediaeventgenerator** -Schnittstelle, die eine Methode zum Abbrechen von asynchronen Vorgängen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-121">Extension of the **IMFMediaEventGenerator** interface that provides a method to cancel asynchronous operations.</span></span> |
| [<span data-ttu-id="c2bbd-122">**Iwmdrmindividualizationstatus**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-122">**IWMDRMIndividualizationStatus**</span></span>](iwmdrmindividualizationstatus.md)       | <span data-ttu-id="c2bbd-123">Ermöglicht das Abrufen erweiterter Statusinformationen über den Fortschritt der Individual alisierung.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-123">Enables retrieval of advanced status information about the progress of individualization.</span></span>                       |
| [<span data-ttu-id="c2bbd-124">**Iwmdrmlicense**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-124">**IWMDRMLicense**</span></span>](iwmdrmlicense.md)                                       | <span data-ttu-id="c2bbd-125">Stellt eine oder mehrere Lizenzen im lokalen Lizenz Speicher dar.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-125">Represents one or more licenses in the local license store.</span></span>                                                     |
| [<span data-ttu-id="c2bbd-126">**Iwmdrmlicenabbackuprestorestatus**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-126">**IWMDRMLicenseBackupRestoreStatus**</span></span>](iwmdrmlicensebackuprestorestatus.md) | <span data-ttu-id="c2bbd-127">Ermöglicht das Abrufen detaillierter Statusinformationen zu einer Lizenz Sicherung oder eines Wiederherstellungs Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-127">Enables retrieval of detailed status information about a license backup or restore operation.</span></span>                   |
| [<span data-ttu-id="c2bbd-128">**Iwmdrmlicenabmanagement**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-128">**IWMDRMLicenseManagement**</span></span>](iwmdrmlicensemanagement.md)                   | <span data-ttu-id="c2bbd-129">Aktiviert Verwaltungsvorgänge für den lokalen Lizenz Speicher.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-129">Enables management operations for the local license store.</span></span>                                                      |
| [<span data-ttu-id="c2bbd-130">**Iwmdrmlicenabmanagement**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-130">**IWMDRMLicenseManagement**</span></span>](iwmdrmlicensemanagement.md)                   | <span data-ttu-id="c2bbd-131">Stellt zusätzliche Verwaltungs Optionen für den lokalen Lizenz Speicher bereit.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-131">Provides additional management options for the local license store.</span></span>                                             |
| [<span data-ttu-id="c2bbd-132">**Iwmdrmlicensequery**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-132">**IWMDRMLicenseQuery**</span></span>](iwmdrmlicensequery.md)                             | <span data-ttu-id="c2bbd-133">Ermöglicht es Anwendungen, die Rechte und den Lizenzstatus für eine geschützte Datei abzufragen.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-133">Enables applications to query the rights and license state for a protected file.</span></span>                                |
| [<span data-ttu-id="c2bbd-134">**Iwmdrmnetreceiver**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-134">**IWMDRMNetReceiver**</span></span>](iwmdrmnetreceiver.md)                               | <span data-ttu-id="c2bbd-135">Stellt Methoden bereit, die zum Erstellen einer Empfänger Anwendung für Microsoft Windows Media DRM für Netzwerkgeräte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-135">Provides methods needed create a Microsoft Windows Media DRM for Network Devices receiver application.</span></span>          |
| [<span data-ttu-id="c2bbd-136">**Iwmdrmnettransmitter**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-136">**IWMDRMNetTransmitter**</span></span>](iwmdrmnettransmitter.md)                         | <span data-ttu-id="c2bbd-137">Stellt Methoden bereit, die zum Erstellen einer Microsoft Windows Media DRM for Network Devices-übermittleranwendung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-137">Provides methods needed create a Microsoft Windows Media DRM for Network Devices transmitter application.</span></span>       |
| [<span data-ttu-id="c2bbd-138">**Iwmdrmnonsilentlicenseaquisition**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-138">**IWMDRMNonSilentLicenseAquisition**</span></span>](iwmdrmnonsilentlicenseaquisition.md) | <span data-ttu-id="c2bbd-139">Stellt Methoden bereit, die den Erwerb von Lizenzen mit Benutzereingriff ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-139">Provides methods that enable license acquisition with user intervention.</span></span>                                        |
| [<span data-ttu-id="c2bbd-140">**Iwmdrmprovider**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-140">**IWMDRMProvider**</span></span>](iwmdrmprovider.md)                                     | <span data-ttu-id="c2bbd-141">Erstellt die anderen Objekte der erweiterten APIs für den Microsoft Windows Media DRM-Client.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-141">Creates the other objects of the Microsoft Windows Media DRM Client Extended APIs.</span></span>                              |
| [<span data-ttu-id="c2bbd-142">**Iwmdrmsecurity**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-142">**IWMDRMSecurity**</span></span>](iwmdrmsecurity.md)                                     | <span data-ttu-id="c2bbd-143">Verwaltet verschiedene sicherheitsbezogene Prozesse für den Client Computer und das DRM-Subsystem.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-143">Manages various security-related processes for the client computer and DRM subsystem.</span></span>                           |
| [<span data-ttu-id="c2bbd-144">**Iwmdrmsecurity**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-144">**IWMDRMSecurity**</span></span>](iwmdrmsecurity.md)                                     | <span data-ttu-id="c2bbd-145">Verwaltet die Sperrung und Verlängerung der Komponente.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-145">Manages component revocation and renewal.</span></span>                                                                       |
| [<span data-ttu-id="c2bbd-146">**Iwmsecurebuffer**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-146">**IWMSecureBuffer**</span></span>](iwmsecurebuffer.md)                                   | <span data-ttu-id="c2bbd-147">Aktiviert die Verschlüsselung und Entschlüsselung von Puffern.</span><span class="sxs-lookup"><span data-stu-id="c2bbd-147">Enables encryption and decryption of buffers.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="c2bbd-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c2bbd-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2bbd-149">**Programmierverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="c2bbd-149">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




