---
description: Allgemeine Anforderungen für die Anwendungsentwicklung
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Allgemeine Anforderungen für die Anwendungsentwicklung (WPD-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16be9656f72324b8f3687bca72146320561b0d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216804"
---
# <a name="general-requirements-for-application-development-wpd-api"></a><span data-ttu-id="137ca-103">Allgemeine Anforderungen für die Anwendungsentwicklung (WPD-API)</span><span class="sxs-lookup"><span data-stu-id="137ca-103">General Requirements for Application Development (WPD API)</span></span>

<span data-ttu-id="137ca-104">Zum Erstellen einer Anwendung für tragbare Windows-Geräte muss das [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads) auf dem Computer installiert sein.</span><span class="sxs-lookup"><span data-stu-id="137ca-104">To create a Windows Portable Devices application, you must have the [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads) installed on your computer.</span></span> <span data-ttu-id="137ca-105">Die erforderlichen Header und Bibliotheken werden in der folgenden Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="137ca-105">The required headers and libraries appear in the following list.</span></span>

-   <span data-ttu-id="137ca-106">Portabledeviceguids. lib</span><span class="sxs-lookup"><span data-stu-id="137ca-106">PortableDeviceGuids.lib</span></span>
-   <span data-ttu-id="137ca-107">Portabledevice. h</span><span class="sxs-lookup"><span data-stu-id="137ca-107">PortableDevice.h</span></span>
-   <span data-ttu-id="137ca-108">Portablede vicetypes. h</span><span class="sxs-lookup"><span data-stu-id="137ca-108">PortableDeviceTypes.h</span></span>
-   <span data-ttu-id="137ca-109">PortableDeviceApi. h</span><span class="sxs-lookup"><span data-stu-id="137ca-109">PortableDeviceApi.h</span></span>
-   <span data-ttu-id="137ca-110">Alle anderen erforderlichen Bibliotheken und Header, die von Ihrer Anwendung für die Nutzung oder das Rendering von Mediendateien benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="137ca-110">Any other required libraries and headers required by your application to consume or render media files.</span></span>

<span data-ttu-id="137ca-111">Wenn Ihre Anwendung die neuen Schnittstellen der Geräte Dienste unterstützt, umfasst Sie auch eine oder mehrere der folgenden Header Dateien.</span><span class="sxs-lookup"><span data-stu-id="137ca-111">If your application supports the new Device Services interfaces, it will also include one or more of the following header files.</span></span>

-   <span data-ttu-id="137ca-112">Anchorsyncdeviceservice. h</span><span class="sxs-lookup"><span data-stu-id="137ca-112">AnchorSyncDeviceService.h</span></span>
-   <span data-ttu-id="137ca-113">Bridgedebug Service. h</span><span class="sxs-lookup"><span data-stu-id="137ca-113">BridgeDeviceService.h</span></span>
-   <span data-ttu-id="137ca-114">Calendardebug Service. h</span><span class="sxs-lookup"><span data-stu-id="137ca-114">CalendarDeviceService.h</span></span>
-   <span data-ttu-id="137ca-115">Contactdebug Service. h</span><span class="sxs-lookup"><span data-stu-id="137ca-115">ContactDeviceService.h</span></span>
-   <span data-ttu-id="137ca-116">Geräte bereitstell. h</span><span class="sxs-lookup"><span data-stu-id="137ca-116">DeviceServices.h</span></span>
-   <span data-ttu-id="137ca-117">Fullenum syncdeviceservice. h</span><span class="sxs-lookup"><span data-stu-id="137ca-117">FullEnumSyncDeviceService.h</span></span>
-   <span data-ttu-id="137ca-118">Hintde viceservice. h</span><span class="sxs-lookup"><span data-stu-id="137ca-118">HintsDeviceService.h</span></span>
-   <span data-ttu-id="137ca-119">Messagedebug Service. h</span><span class="sxs-lookup"><span data-stu-id="137ca-119">MessageDeviceService.h</span></span>
-   <span data-ttu-id="137ca-120">MetadataDeviceService. h</span><span class="sxs-lookup"><span data-stu-id="137ca-120">MetadataDeviceService.h</span></span>
-   <span data-ttu-id="137ca-121">Notesdebug Service. h</span><span class="sxs-lookup"><span data-stu-id="137ca-121">NotesDeviceService.h</span></span>
-   <span data-ttu-id="137ca-122">Ringtonedeviceservice. h</span><span class="sxs-lookup"><span data-stu-id="137ca-122">RingtoneDeviceService.h</span></span>
-   <span data-ttu-id="137ca-123">Status Update Service. h</span><span class="sxs-lookup"><span data-stu-id="137ca-123">StatusDeviceService.h</span></span>
-   <span data-ttu-id="137ca-124">Syncdeviceservice. h</span><span class="sxs-lookup"><span data-stu-id="137ca-124">SyncDeviceService.h</span></span>
-   <span data-ttu-id="137ca-125">Taskdebug Service. h</span><span class="sxs-lookup"><span data-stu-id="137ca-125">TaskDeviceService.h</span></span>

<span data-ttu-id="137ca-126">Von den Dateien in der vorherigen Liste sind bridgedeviceservice. h und deviceservice. h für fast jede Anwendung erforderlich, die Geräte Dienste unterstützt. die anderen Dateien definieren verschiedene Typen von Geräte Diensten und werden gegebenenfalls eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="137ca-126">Of the files in the previous list, BridgeDeviceService.h and DeviceService.h are required for almost any application that supports Device Services; the other files define different types of device services and would be included as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="137ca-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="137ca-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="137ca-128">**Tragbare Windows-Geräte**</span><span class="sxs-lookup"><span data-stu-id="137ca-128">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
