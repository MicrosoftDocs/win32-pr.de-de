---
title: Windows Media Device Manager 11 SDK
description: Windows Media Device Manager 11 SDK
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Media Device Manager, Informationen zu
- Device Manager, Informationen zu
- Media Transfer Protocol (MTP)
- MTP (Media Transfer Protocol)
- Massenspeicher Klasse (MSC)
- MSC (Massenspeicher Klasse)
- Windows Media Device Manager, Desktop Anwendungen
- Device Manager, Desktop Anwendungen
- Desktop Anwendungen, Informationen zu
- Windows Media Device Manager, Dienstanbieter
- Device Manager, Dienstanbieter
- Dienstanbieter, Informationen zu
- Windows Media Device Manager, Plug-ins
- Device Manager, Plug-in
- Plug-ins, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391147"
---
# <a name="windows-media-device-manager-11-sdk"></a><span data-ttu-id="d4208-118">Windows Media Device Manager 11 SDK</span><span class="sxs-lookup"><span data-stu-id="d4208-118">Windows Media Device Manager 11 SDK</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4208-119">Die Windows Media Device Manager-APIs sind nun in der Windows SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="d4208-119">The Windows Media Device Manager APIs are now included in the Windows SDK.</span></span> <span data-ttu-id="d4208-120">Es sind keine zusätzlichen SDK-Downloads erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4208-120">No additional SDK downloads are required.</span></span>

 

<span data-ttu-id="d4208-121">Mit dem Microsoft Windows Media Device Manager Software Development Kit (SDK) können Sie Desktop Anwendungen und-Komponenten erstellen, die mit verbundenen tragbaren Geräten kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="d4208-121">The Microsoft Windows Media Device Manager Software Development Kit (SDK) enables you to build desktop applications and components that can communicate with connected portable devices.</span></span> <span data-ttu-id="d4208-122">Windows Media Device Manager ermöglicht der Anwendung oder Komponente das auflisten, durchsuchen und Austauschen von Dateien mit einem Gerät, das Abfragen von Metadaten und das Anfordern von Informationen zur Wiedergabe Anzahl.</span><span class="sxs-lookup"><span data-stu-id="d4208-122">Windows Media Device Manager enables your application or component to enumerate, explore, and exchange files with a device, query for metadata, and request play count information.</span></span> <span data-ttu-id="d4208-123">Anwendungen oder Komponenten, die auf Windows Media-Device Manager erstellt wurden, verfügen über eine konsistente API für die Kommunikation mit einer großen Bandbreite von Geräten, einschließlich Media Transfer Protocol (MTP), Massenspeicher Klasse (MSC), RAPI und anderen Geräten, die auf der neuesten und früheren Version der Windows Media-Technologie basieren.</span><span class="sxs-lookup"><span data-stu-id="d4208-123">Applications or components built on Windows Media Device Manager have a consistent API for communicating with a wide range of devices including Media Transfer Protocol (MTP), Mass Storage Class (MSC), RAPI, and other devices built on both the latest and previous versions of Windows Media technology.</span></span>

<span data-ttu-id="d4208-124">Mithilfe des Windows Media Device Manager SDK können Sie die folgenden Elemente erstellen:</span><span class="sxs-lookup"><span data-stu-id="d4208-124">You can build the following items using the Windows Media Device Manager SDK:</span></span>

-   <span data-ttu-id="d4208-125">Desktop Anwendungen, z. b. benutzerdefinierte Medien Player.</span><span class="sxs-lookup"><span data-stu-id="d4208-125">Desktop applications, such as custom media players.</span></span> <span data-ttu-id="d4208-126">Die gesamte Kommunikation zwischen einer Anwendung und einem tragbaren Gerät muss über Windows Media Device Manager durchlaufen werden, das als Broker zwischen der Anwendung, dem Microsoft Digital Rights Management System und dem Dienstanbieter fungiert.</span><span class="sxs-lookup"><span data-stu-id="d4208-126">All communication between an application and a portable device must go through Windows Media Device Manager, which acts as a broker between the application, the Microsoft digital rights management system, and the service provider.</span></span>
-   <span data-ttu-id="d4208-127">Dienstanbieter, die als Kommunikationsverbindung zwischen einem benutzerdefinierten Gerät und einer Desktop Anwendung fungieren.</span><span class="sxs-lookup"><span data-stu-id="d4208-127">Service providers, which act as the communication link between a custom device and a desktop application.</span></span> <span data-ttu-id="d4208-128">Obwohl Microsoft eine Reihe von Dienstanbietern bereitstellt, die standardmäßig mit den meisten Geräten kommunizieren können, können Sie einen benutzerdefinierten Dienstanbieter erstellen, um die Kommunikation zwischen einem Gerät und einer Desktop Anwendung anzupassen.</span><span class="sxs-lookup"><span data-stu-id="d4208-128">Although Microsoft provides a number of service providers that can communicate with most devices out of the box, you can build a custom service provider to customize the communication between a device and a desktop application.</span></span>
-   <span data-ttu-id="d4208-129">Plug-ins, die Aufgaben ausführen können, z. b. das anfordern und Protokollieren der Wiedergabe Anzahl auf Geräten.</span><span class="sxs-lookup"><span data-stu-id="d4208-129">Plug-ins, which can perform tasks such as requesting and logging play counts on devices.</span></span> <span data-ttu-id="d4208-130">Diese Plug-Ins können an andere Desktop Anwendungen angefügt werden, wie z. b. die Windows-Media Player, um Informationen an Inhaltsanbieter zu senden, um die Lizenzzahlungen an die Künstler zu verarbeiten</span><span class="sxs-lookup"><span data-stu-id="d4208-130">These plug-ins can be attached to other desktop applications, such as the Windows Media Player to send information to content providers to handle royalty payments to artists.</span></span>

<span data-ttu-id="d4208-131">Informationen zum Herunterladen des Windows Media Device Manager SDK finden Sie auf der MSDN-Website auf [der Windows Media-Downloadseite](https://msdn.microsoft.com/windows/desktop/aa904949) .</span><span class="sxs-lookup"><span data-stu-id="d4208-131">To download the Windows Media Device Manager SDK, see [the Windows Media Download page](https://msdn.microsoft.com/windows/desktop/aa904949) on the MSDN Web site.</span></span>

<span data-ttu-id="d4208-132">Dieses SDK ist eine Komponente des Microsoft Windows Media Software Development Kit.</span><span class="sxs-lookup"><span data-stu-id="d4208-132">This SDK is a component of the Microsoft Windows Media Software Development Kit.</span></span> <span data-ttu-id="d4208-133">Weitere Komponenten sind das Windows Media-Format-SDK, das Windows Media Services SDK, das Windows Media Encoder SDK, das Windows Media Rights Manager SDK und das Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="d4208-133">Other components include the Windows Media Format SDK, the Windows Media Services SDK, the Windows Media Encoder SDK, the Windows Media Rights Manager SDK, and the Windows Media Player SDK.</span></span>

<span data-ttu-id="d4208-134">Diese Dokumentation enthält die folgenden Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="d4208-134">This documentation includes the following sections.</span></span>



| <span data-ttu-id="d4208-135">`Section`</span><span class="sxs-lookup"><span data-stu-id="d4208-135">Section</span></span>                                            | <span data-ttu-id="d4208-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4208-136">Description</span></span>                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4208-137">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="d4208-137">Getting Started</span></span>](getting-started.md)             | <span data-ttu-id="d4208-138">Beschreibt die Neuerungen in dieser Version von Windows Media Device Manager, bietet einen Überblick über die Funktionsweise von Windows Media Device Manager, beschreibt, was zum Entwickeln einer Anwendung oder eines Dienstanbieters erforderlich ist, und erläutert die Beispiele, die mit dem SDK ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="d4208-138">Describes what is new in this version of Windows Media Device Manager, gives an overview of how Windows Media Device Manager works, describes what will be needed to develop an application or service provider, and explains the samples shipped with the SDK.</span></span> |
| [<span data-ttu-id="d4208-139">Programmierhandbuch</span><span class="sxs-lookup"><span data-stu-id="d4208-139">Programming Guide</span></span>](programming-guide.md)         | <span data-ttu-id="d4208-140">Erläutert, wie Anwendungen und Dienstanbieter erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="d4208-140">Discusses how to build applications and service providers.</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="d4208-141">Programmierverzeichnis</span><span class="sxs-lookup"><span data-stu-id="d4208-141">Programming Reference</span></span>](programming-reference.md) | <span data-ttu-id="d4208-142">Bietet C++-Referenzinformationen für die Schnittstellen, Methoden, Klassen und Strukturen, die vom Windows Media Device Manager SDK unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d4208-142">Provides C++ reference information for the interfaces, methods, classes, and structures supported by the Windows Media Device Manager SDK.</span></span>                                                                                                                      |
| [<span data-ttu-id="d4208-143">*Glossar*</span><span class="sxs-lookup"><span data-stu-id="d4208-143">*Glossary*</span></span>](wmdm-glossary.md)                    | <span data-ttu-id="d4208-144">Definiert Begriffe, die in dieser Dokumentation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4208-144">Defines terms used in this documentation.</span></span>                                                                                                                                                                                                                       |



 

 

 




