---
title: Implementieren von Netzwerkfunktionen
description: Implementieren von Netzwerkfunktionen
ms.assetid: 908e269b-63be-4666-a364-a894f6dcd86f
keywords:
- Windows Media-Format-SDK, Implementieren von Netzwerkfunktionen
- Windows Media-Format-SDK, Netzwerkfunktionalität
- Advanced Systems Format (ASF), Implementieren von Netzwerkfunktionen
- ASF (Advanced Systems Format), Implementieren von Netzwerkfunktionen
- Advanced Systems Format (ASF), Netzwerkfunktionalität
- ASF (Advanced Systems Format), Netzwerkfunktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e631b6a322293bffe71ce92afcb684901cc60d16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515992"
---
# <a name="implementing-network-functionality"></a><span data-ttu-id="d8cfa-109">Implementieren von Netzwerkfunktionen</span><span class="sxs-lookup"><span data-stu-id="d8cfa-109">Implementing Network Functionality</span></span>

<span data-ttu-id="d8cfa-110">In diesem Abschnitt wird beschrieben, wie die Netzwerk Features verwendet werden, die über das Windows Media Format SDK verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-110">This section describes how to use the networking features available through the Windows Media Format SDK.</span></span> <span data-ttu-id="d8cfa-111">Eine Anwendung kann diese Funktionen zum Lesen von ASF-Streams aus einem Netzwerk, zum Übertragen von ASF-Datenströmen an ein Netzwerk oder zum Übertragen von ASF-Streams an einen Publishing Point auf einem Server mit Windows Media Services verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-111">An application can use these features to read ASF streams from a network, broadcast ASF streams to a network, or push ASF streams to a publishing point on a server running Windows Media Services.</span></span>

<span data-ttu-id="d8cfa-112">In den folgenden Abschnitten werden die Netzwerk Features dieses SDK beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-112">The following sections describe the networking features of this SDK.</span></span>



| <span data-ttu-id="d8cfa-113">`Section`</span><span class="sxs-lookup"><span data-stu-id="d8cfa-113">Section</span></span>                                                                    | <span data-ttu-id="d8cfa-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8cfa-114">Description</span></span>                                                                                                          |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8cfa-115">Übersicht über Netzwerkschnittstellen</span><span class="sxs-lookup"><span data-stu-id="d8cfa-115">Overview of Networking Interfaces</span></span>](overview-of-networking-interfaces.md) | <span data-ttu-id="d8cfa-116">Benennt und beschreibt jede Schnittstelle, die Netzwerk Methoden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-116">Names and describes each interface that supports networking methods.</span></span>                                                 |
| [<span data-ttu-id="d8cfa-117">Lesen von ASF-Daten über ein Netzwerk</span><span class="sxs-lookup"><span data-stu-id="d8cfa-117">Reading ASF Data Over a Network</span></span>](reading-asf-data-over-a-network.md)     | <span data-ttu-id="d8cfa-118">Beschreibt das Abspielen von Dateien aus einer Netzwerkquelle und das Konfigurieren der Netzwerkeinstellungen für das Reader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-118">Describes how to play files from a network source and how to configure the network settings on the reader object.</span></span>    |
| [<span data-ttu-id="d8cfa-119">Senden von ASF-Daten über ein Netzwerk</span><span class="sxs-lookup"><span data-stu-id="d8cfa-119">Sending ASF Data Over a Network</span></span>](sending-asf-data-over-a-network.md)     | <span data-ttu-id="d8cfa-120">Beschreibt das Übertragen von ASF-Daten über ein Netzwerk oder das Senden von ASF-Daten an einen Publishing Point auf einem Windows Media-Server.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-120">Describes how to broadcast ASF data over a network or send ASF data to a publishing point on a Windows Media server.</span></span> |
| [<span data-ttu-id="d8cfa-121">Standard Netzwerkeinstellungen</span><span class="sxs-lookup"><span data-stu-id="d8cfa-121">Default Networking Settings</span></span>](default-networking-settings.md)             | <span data-ttu-id="d8cfa-122">Bietet eine Kurzübersicht über die Standardeinstellungen, die vom SDK verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8cfa-122">Provides a quick reference for the default settings used by the SDK.</span></span>                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="d8cfa-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8cfa-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8cfa-124">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="d8cfa-124">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




