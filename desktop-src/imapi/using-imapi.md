---
title: Verwenden von IMAPI
description: In den folgenden Themen wird die Verwendung der Image-Mastering-API veranschaulicht.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccd44d01e925d07d251e93a29c5268cc7e9c5076
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856948"
---
# <a name="using-imapi"></a><span data-ttu-id="930f9-103">Verwenden von IMAPI</span><span class="sxs-lookup"><span data-stu-id="930f9-103">Using IMAPI</span></span>

<span data-ttu-id="930f9-104">In den folgenden Themen wird die Verwendung der Image-Mastering-API veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="930f9-104">The following topics demonstrate the use of the image mastering API.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="930f9-105">Verwendungsszenarien</span><span class="sxs-lookup"><span data-stu-id="930f9-105">Usage Scenarios</span></span>

<span data-ttu-id="930f9-106">In der folgenden Dokumentation finden Sie ausführliche Anleitungen für gängige IMAPI-Szenarios.</span><span class="sxs-lookup"><span data-stu-id="930f9-106">The following documentation provides detailed guidance for common IMAPI scenarios.</span></span>



| <span data-ttu-id="930f9-107">Szenario</span><span class="sxs-lookup"><span data-stu-id="930f9-107">Scenario</span></span>                                                                                                         | <span data-ttu-id="930f9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="930f9-108">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="930f9-109">Überprüfen der Laufwerk Unterstützung</span><span class="sxs-lookup"><span data-stu-id="930f9-109">Checking Drive Support</span></span>](checking-drive-support.md)                                                             | <span data-ttu-id="930f9-110">Veranschaulicht das Erkennen der Unterstützung für ein Medienlaufwerk.</span><span class="sxs-lookup"><span data-stu-id="930f9-110">Demonstrates the detection of support for a media drive.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="930f9-111">Überprüfen der Medien Unterstützung</span><span class="sxs-lookup"><span data-stu-id="930f9-111">Checking Media Support</span></span>](checking-media-support.md)                                                             | <span data-ttu-id="930f9-112">Veranschaulicht das Erkennen der Unterstützung für Medien.</span><span class="sxs-lookup"><span data-stu-id="930f9-112">Demonstrates the detection of support for media.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="930f9-113">Brennen eines Festplatten Bilds</span><span class="sxs-lookup"><span data-stu-id="930f9-113">Burning a Disc Image</span></span>](burning-a-disc.md)                                                                       | <span data-ttu-id="930f9-114">Veranschaulicht das Mastering (Brennen eines Datenträgers) mithilfe von IMAPI.</span><span class="sxs-lookup"><span data-stu-id="930f9-114">Demonstrates mastering (burning a disc) using IMAPI.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="930f9-115">Hinzufügen eines Start Abbilds</span><span class="sxs-lookup"><span data-stu-id="930f9-115">Adding a Boot Image</span></span>](adding-a-boot-image.md)                                                                   | <span data-ttu-id="930f9-116">Basiert auf dem Beispiel zum [Brennen eines Festplatten Bilds](burning-a-disc.md) durch Hinzufügen von Code, um ein startbares Image in den Startbereich der Festplatte einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="930f9-116">Builds on the [Burning a Disc Image](burning-a-disc.md) example by adding code to include a bootable image in the boot section of the disc.</span></span><br/>               |
| [<span data-ttu-id="930f9-117">Erstellen einer Multi-Session-CD</span><span class="sxs-lookup"><span data-stu-id="930f9-117">Creating a Multisession Disc</span></span>](creating-a-multisession-disc.md)                                                 | <span data-ttu-id="930f9-118">Veranschaulicht die Erstellung einer mehr sitzungsdatenträger mithilfe von IMAPI.</span><span class="sxs-lookup"><span data-stu-id="930f9-118">Demonstrates the creation of a multisession disc using IMAPI.</span></span><br/>                                                                                              |
| [<span data-ttu-id="930f9-119">Überwachen des Fortschritts mit Ereignissen</span><span class="sxs-lookup"><span data-stu-id="930f9-119">Monitoring Progress With Events</span></span>](monitoring-progress-with-events.md)                                           | <span data-ttu-id="930f9-120">Veranschaulicht die Verwendung spezifischer Schnittstellen, um die Implementierung eines Ereignis Handlers zuzulassen, damit Statusinformationen empfangen werden können.</span><span class="sxs-lookup"><span data-stu-id="930f9-120">Demonstrates the use of specific interfaces in order to allow the implementation of an event handler so that progress information may be received.</span></span> <br/>        |
| [<span data-ttu-id="930f9-121">Verhindern der Abmeldung oder aussetzen während eines Burn-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="930f9-121">Preventing Logoff or Suspend During a Burn</span></span>](preventing-logoff-or-suspend-during-a-burn.md)                     | <span data-ttu-id="930f9-122">Enthält Informationen über Aspekte der Anwendungsentwicklung in Bezug auf Szenarien, in denen der Benutzer "Abmeldung" und "Suspend" in Windows berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="930f9-122">Contains information detailing application development considerations to be made in regards to scenarios involving user 'Logoff' and 'Suspend' in Windows.</span></span><br/> |
| [<span data-ttu-id="930f9-123">Bereitstellen von Benutzerberechtigungen für Medien brennende Geräte</span><span class="sxs-lookup"><span data-stu-id="930f9-123">Providing User Permissions for Media Burning Devices</span></span>](providing-user-permissions-for-media-burning-devices.md) | <span data-ttu-id="930f9-124">Erläutert den Prozess, der erforderlich ist, um sicherzustellen, dass ein Benutzer über die erforderlichen Berechtigungen zum Verwenden von Medien brennen auf Windows XP und Windows Server 2003 verfügt.</span><span class="sxs-lookup"><span data-stu-id="930f9-124">Details the process required to ensure a user has adequate permissions to utilize media burning devices on Windows XP and Windows Server 2003.</span></span><br/>             |



 

## <a name="application-compatibility"></a><span data-ttu-id="930f9-125">Anwendungskompatibilität</span><span class="sxs-lookup"><span data-stu-id="930f9-125">Application Compatibility</span></span>

<span data-ttu-id="930f9-126">Die folgende Dokumentation enthält wichtige Informationen, die beim Entwickeln einer Anwendung, die IMAPI verwendet, berücksichtigt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="930f9-126">The following documentation contains important information to take consideration while developing an application that utilizes IMAPI.</span></span>



| <span data-ttu-id="930f9-127">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="930f9-127">Guidance</span></span>                                                   | <span data-ttu-id="930f9-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="930f9-128">Description</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="930f9-129">Layout von IMAPI-Multisession</span><span class="sxs-lookup"><span data-stu-id="930f9-129">IMAPI Multisession Layout</span></span>](imapi-multisession-layout.md) | <span data-ttu-id="930f9-130">Erläutert das Festplattenlayout, das von IMAPI zum Implementieren von mehreren Sitzungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="930f9-130">Details the disc layout that IMAPI utilizes to implement multisession.</span></span> <span data-ttu-id="930f9-131">Diese Informationen werden verwendet, um die Interoperabilität zwischen IMAPI und anderer brennender Software zu gewährleisten und das Erstellen von IMAPI-kompatiblen Festplatten Abbildern mit mehreren Sitzungen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="930f9-131">This information is used to ensure interoperability between IMAPI and other burning software, as well as allow the creation of IMAPI-compatible multisession disc images.</span></span><br/> |



 

 

 





