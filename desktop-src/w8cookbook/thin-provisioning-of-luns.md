---
title: Schlanke Speicherzuweisung logischer Einheiten
description: Schlanke Speicherzuweisung logischer Einheiten
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- LUN
- LBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4abb6fa3cec112737b23e3cd658a48984cb0fcd1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104039745"
---
# <a name="thin-provisioning-of-logical-units"></a><span data-ttu-id="210b6-105">Schlanke Speicherzuweisung logischer Einheiten</span><span class="sxs-lookup"><span data-stu-id="210b6-105">Thin provisioning of logical units</span></span>

## <a name="platforms"></a><span data-ttu-id="210b6-106">Plattformen</span><span class="sxs-lookup"><span data-stu-id="210b6-106">Platforms</span></span>

<span data-ttu-id="210b6-107">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="210b6-107">**Clients** – Windows 8</span></span>  
<span data-ttu-id="210b6-108">**Server** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="210b6-108">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="210b6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="210b6-109">Description</span></span>

<span data-ttu-id="210b6-110">Die schlanke Windows-Bereitstellung ist eine Schnittstelle zur Lösung für die End-to-End-Speicher Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="210b6-110">Windows Thin Provisioning is an interface to the end-to-end storage provisioning solution.</span></span> <span data-ttu-id="210b6-111">Zum Bereitstellen eines hoch verfügbaren, skalierbaren und benutzerfreundlichen Speicher Bereitstellungs Diensts sind robuste Implementierungen vom Server Host zum Speicher Zielgerät erforderlich.</span><span class="sxs-lookup"><span data-stu-id="210b6-111">To deliver a highly available, scalable and user-friendly storage provisioning service requires robust implementations from the server host to the storage target device.</span></span> <span data-ttu-id="210b6-112">Das Windows-Feature für die schlanke Speicherzuweisung bietet dem Systemadministrator, dem IT-Manager und dem Speicher Administrator eine synchrone Ansicht der Speichergeräte für die schlanke Speicherzuweisung für den Systemadministrator, den IT-Manager und den Speicher Administrator, indem es die (LUN)-Identifikation der logischen Einheit (LUN), Schwellenwert Benachrichtigung, Ressourcen Auslastungs Behandlung, Speicherplatz Rückgewinnung und</span><span class="sxs-lookup"><span data-stu-id="210b6-112">The Windows thin provisioning feature provides a synchronous view of the thin provisioning storage devices to the system administrator, IT manager, and storage administrator through the thinly provisioned logical unit’s (LUN’s) identification, threshold notification, resource exhaustion handling, space reclamation, and logical block addressing (LBA) state retrieval.</span></span> <span data-ttu-id="210b6-113">Das Windows-Feature für die schlanke Speicherzuweisung stellt ein stabiles Speicher Bereitstellungs Dienstmodell dar, das auf Client-Server-Speichersysteme, virtualisierungsspeicher und cloudspeicherdienste angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="210b6-113">The Windows thin provisioning feature presents a robust storage provisioning service model that can be applied to client-server storage systems, virtualization storage, and cloud storage services.</span></span> <span data-ttu-id="210b6-114">Microsoft gewährleistet die hohe Qualität des Features für die schlanke Speicherzuweisung durch erzwingen der Anforderungen an das Hardware-zertifizierungskit für Windows Thin Bereitstellung für Speicher Array Produkte.</span><span class="sxs-lookup"><span data-stu-id="210b6-114">Microsoft will ensure the high quality of the thin provisioning feature by enforcing the Windows Thin Provisioning Hardware Certification Kit requirements for storage array products.</span></span>

<span data-ttu-id="210b6-115">Die Speicherlösung für die Bereitstellung von Windows schlank:</span><span class="sxs-lookup"><span data-stu-id="210b6-115">The Windows Thin Provisioning storage solution:</span></span>

-   <span data-ttu-id="210b6-116">Ermöglicht Speicher Administratoren das Erstellen einer größeren LUN mit weniger physischen Datenträger Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="210b6-116">Allows storage administrators to create a larger LUN with fewer physical disk resources</span></span>
-   <span data-ttu-id="210b6-117">Fügt physische Datenträger Ressource hinzu oder entfernt Sie, ohne den Speicher Bereitstellungs Dienst zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="210b6-117">Adds or removes physical disk resource without interrupting the storage provisioning service</span></span>
-   <span data-ttu-id="210b6-118">Benachrichtigt Benutzer über die Schwellenwert Einstellung auf die Auslastung des Speichervolumes.</span><span class="sxs-lookup"><span data-stu-id="210b6-118">Alerts users to the storage volume usage through the threshold setting</span></span>
-   <span data-ttu-id="210b6-119">Unterstützt die Speicher Bereitstellung über die freigegebene Speicherpool Konfiguration</span><span class="sxs-lookup"><span data-stu-id="210b6-119">Supports storage provisioning through the shared storage pool configuration</span></span>
-   <span data-ttu-id="210b6-120">Erhöht oder verringert die Größe des Speicherpools entsprechend der Nachfrage und Verwendung von Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="210b6-120">Increases or decreases the size of the storage pool according to the demand and usage of storage space</span></span>

<span data-ttu-id="210b6-121">Zusammenfassung der Features der Windows-Thin Bereitstellung:</span><span class="sxs-lookup"><span data-stu-id="210b6-121">Summary of the Windows Thin Provisioning features:</span></span>

-   <span data-ttu-id="210b6-122">LUN-Identifikation der schlank Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="210b6-122">Thin Provisioning LUN identification</span></span>
-   <span data-ttu-id="210b6-123">Handles für Schwellenwert Benachrichtigung, temporäre Ressourcenauslastung und permanente Ressourcenauslastung</span><span class="sxs-lookup"><span data-stu-id="210b6-123">Handles for threshold notification, temporary resource exhaustion, and permanent resource exhaustion</span></span>
-   <span data-ttu-id="210b6-124">Speicherplatz Rückgewinnung</span><span class="sxs-lookup"><span data-stu-id="210b6-124">Storage space reclamation</span></span>
-   <span data-ttu-id="210b6-125">Zuordnung von Zustands Abfragen logischer Blöcke</span><span class="sxs-lookup"><span data-stu-id="210b6-125">Mapping state queries of logical blocks</span></span>

## <a name="manifestation"></a><span data-ttu-id="210b6-126">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="210b6-126">Manifestation</span></span>

<span data-ttu-id="210b6-127">Ohne das richtige Verständnis der Windows-Handles für die LUN mit schlanker Speicherzuweisung kann die APP mit unerwartetem Verhalten oder aus unbekannter Ursache fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="210b6-127">Without the proper understanding of the Windows handles for thin provisioning LUN, the app could fail with unexpected behavior or for an unknown cause.</span></span>

## <a name="using-thin-provisioning-luns"></a><span data-ttu-id="210b6-128">Verwenden von LUNs mit schlanker Speicherzuweisung</span><span class="sxs-lookup"><span data-stu-id="210b6-128">Using thin provisioning LUNs</span></span>

<span data-ttu-id="210b6-129">Zur Verwendung von schlank bereitgestellten LUNs in Windows 8 oder Windows Server 2012 sollten System-und Speicher Administratoren Folgendes beachten:</span><span class="sxs-lookup"><span data-stu-id="210b6-129">To use thinly provisioned LUNs in Windows 8 or Windows Server 2012, system and storage administrators should be aware of these matters:</span></span>

-   <span data-ttu-id="210b6-130">LUN-Identifikation der Thin Bereitstellung; Systemadministratoren oder Endbenutzer können Defrag und das Dienstprogramm für den Speicher Optimierer verwenden, um den Medientyp des Speichergeräts zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="210b6-130">Thin provisioning LUN identification; system administrators or end users can use Defrag and the Storage Optimizer utility to identify the media type of the storage device</span></span>
-   <span data-ttu-id="210b6-131">Wenn ein Schwellenwert oder ein dauerhaftes Ressourcen Auslastungs Ereignis erreicht wird, protokolliert Windows ein System Ereignis, um den Systemadministrator zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="210b6-131">When a threshold or a permanent resource exhaustion event is hit, Windows will log a system event to alert the system administrator</span></span>
-   <span data-ttu-id="210b6-132">Die Speicherplatz Rückgewinnung kann manuell oder automatisch durch Datei Lösch Benachrichtigung oder den Scheduler des Speicher Optimierers ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="210b6-132">Storage space reclamation can be performed manually or automatically by file delete notification or the scheduler of the storage optimizer</span></span>
-   <span data-ttu-id="210b6-133">Der Speicher Administrator sollte die Schwellenwert Benachrichtigung für Warnungs Systemadministrator oder Endbenutzer implementieren und unerwartete Speicherdienst Unterbrechungen vermeiden.</span><span class="sxs-lookup"><span data-stu-id="210b6-133">Storage administrator should implement the threshold notification to alert system administrator or end user and avoid any unexpected storage service interruption</span></span>

## <a name="tests"></a><span data-ttu-id="210b6-134">Tests</span><span class="sxs-lookup"><span data-stu-id="210b6-134">Tests</span></span>

-   <span data-ttu-id="210b6-135">Das Speicher Array muss ein Zertifikat für die schlanke Windows 8-Bereitstellung erhalten, um die Windows Thin Provisioning-Funktionen</span><span class="sxs-lookup"><span data-stu-id="210b6-135">Storage array must receive Windows 8 Thin Provisioning certificate to support Windows Thin Provisioning features</span></span>
-   <span data-ttu-id="210b6-136">Das Hardware-zertifizierungskit für die Windows-schlanke Speicherzuweisung für das Speicher Array ist ein nützliches Testtool zum Überprüfen der Funktion von Speicherarrays für die Unterstützung von Windows schlank</span><span class="sxs-lookup"><span data-stu-id="210b6-136">Windows Thin Provisioning Hardware Certification Kit for storage array will be a useful test tool to verify storage array’s capability for Windows Thin Provisioning feature support</span></span>
-   <span data-ttu-id="210b6-137">Windows erwartet, dass die LUN mit schlanker Speicherzuweisung und die LUN für die vollständige Bereitstellung ohne Probleme in demselben System funktionieren.</span><span class="sxs-lookup"><span data-stu-id="210b6-137">Windows expects the Thin Provisioning LUN and Full Provisioning LUN to work in the same system without any issue</span></span>

## <a name="resources"></a><span data-ttu-id="210b6-138">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="210b6-138">Resources</span></span>

-   [<span data-ttu-id="210b6-139">T10-SCSI-Block-Befehls Spezifikation (SBC3r27)</span><span class="sxs-lookup"><span data-stu-id="210b6-139">T10 SCSI Block Command Spec (SBC3r27)</span></span>](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [<span data-ttu-id="210b6-140">Hardware-Dashboard-Dienste</span><span class="sxs-lookup"><span data-stu-id="210b6-140">Hardware Dashboard Services</span></span>](/windows-hardware/drivers/dashboard/)

 

 