---
description: Die Medien Sitzung ist ein Objekt, das den Datenfluss in der Pipeline verwaltet. Sie kann für die Wiedergabe und Codierung von Dateien verwendet werden.
ms.assetid: dac99908-be90-415d-8837-2f97d573feb5
title: Medien Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3df4597e5461788f990f620875bce946570ab97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106351851"
---
# <a name="media-session"></a><span data-ttu-id="92792-104">Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="92792-104">Media Session</span></span>

<span data-ttu-id="92792-105">Die Medien Sitzung ist ein Objekt, das den Datenfluss in der Pipeline verwaltet.</span><span class="sxs-lookup"><span data-stu-id="92792-105">The Media Session is an object that manages data flow in the pipeline.</span></span> <span data-ttu-id="92792-106">Sie kann für die Wiedergabe und Codierung von Dateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92792-106">It can be used for both playing and encoding files.</span></span>

<span data-ttu-id="92792-107">In diesem Abschnitt wird die Medien Sitzung von einem architektonischen Standpunkt aus beschrieben.</span><span class="sxs-lookup"><span data-stu-id="92792-107">This section describes the Media Session from an architectural standpoint.</span></span> <span data-ttu-id="92792-108">Sie enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="92792-108">It contains the following sections:</span></span>



| <span data-ttu-id="92792-109">Thema</span><span class="sxs-lookup"><span data-stu-id="92792-109">Topic</span></span>                                                                                        | <span data-ttu-id="92792-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92792-110">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92792-111">Informationen zur Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="92792-111">About the Media Session</span></span>](about-the-media-session.md)                                       | <span data-ttu-id="92792-112">Bietet eine Übersicht über die Medien Sitzung, die Art und Weise, wie eine Anwendung die Medien Sitzung erstellen kann, und wie die Medien Sitzung die Präsentationszeit verwaltet.</span><span class="sxs-lookup"><span data-stu-id="92792-112">Provides an overview of the Media Session, how an application can create the Media Session, and how the Media Session manages presentation time.</span></span> |
| [<span data-ttu-id="92792-113">Topologien</span><span class="sxs-lookup"><span data-stu-id="92792-113">Topologies</span></span>](topologies.md)                                                                 | <span data-ttu-id="92792-114">Eine Topologie ist ein Objekt, das den Datenfluss in der Pipeline darstellt.</span><span class="sxs-lookup"><span data-stu-id="92792-114">A topology is an object that represents the flow of data in the pipeline.</span></span>                                                                        |
| [<span data-ttu-id="92792-115">Medien Sitzungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="92792-115">Media Session Events</span></span>](media-session-events.md)                                             | <span data-ttu-id="92792-116">Beschreibt die Ereignisse, die von einer Anwendung möglicherweise von der Medien Sitzung empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="92792-116">Describes the events that an application might receive from the Media Session.</span></span>                                                                   |
| [<span data-ttu-id="92792-117">Steuern von Präsentations Zuständen</span><span class="sxs-lookup"><span data-stu-id="92792-117">How to Control Presentation States</span></span>](how-to-control-presentation-states.md)                 | <span data-ttu-id="92792-118">Beschreibt die Transport Steuerelemente für Medien Sitzungen: wiedergeben, anhalten und anhalten.</span><span class="sxs-lookup"><span data-stu-id="92792-118">Describes the Media Session transport controls: Play, Pause, and Stop.</span></span>                                                                           |
| [<span data-ttu-id="92792-119">Verwenden von Medienquellen mit der Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="92792-119">Using Media Sources with the Media Session</span></span>](using-media-sources-with-the-media-session.md) | <span data-ttu-id="92792-120">Verwenden von Medienquellen mit der Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="92792-120">How to use media sources with the Media Session.</span></span>                                                                                                 |
| [<span data-ttu-id="92792-121">Raten Steuerung</span><span class="sxs-lookup"><span data-stu-id="92792-121">Rate Control</span></span>](rate-control.md)                                                             | <span data-ttu-id="92792-122">Beschreibt, wie die Wiedergabe Rate gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="92792-122">Describes how to control playback rate.</span></span>                                                                                                          |
| [<span data-ttu-id="92792-123">Video Qualitäts Verwaltung</span><span class="sxs-lookup"><span data-stu-id="92792-123">Video Quality Management</span></span>](video-quality-management.md)                                     | <span data-ttu-id="92792-124">Hier werden Verbesserungen an der Video Pipeline in Windows 7 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="92792-124">Describes improvements to the video pipeline in Windows 7.</span></span>                                                                                       |
| [<span data-ttu-id="92792-125">PMP-Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="92792-125">PMP Media Session</span></span>](pmp-media-session.md)                                                   | <span data-ttu-id="92792-126">Hier wird beschrieben, wie die Medien Sitzung in einem PMP-Prozess (Protected Media Path) erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="92792-126">Describes how to create the Media Session inside a Protected Media Path (PMP) process.</span></span>                                                           |



 

<span data-ttu-id="92792-127">In den folgenden Themen wird beschrieben, wie die Medien Sitzung in bestimmten Anwendungsszenarien verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="92792-127">The following topics describe how to use the Media Session in specific application scenarios:</span></span>

-   [<span data-ttu-id="92792-128">Audio-/Videowiedergabe</span><span class="sxs-lookup"><span data-stu-id="92792-128">Audio/Video Playback</span></span>](audio-video-playback.md)
-   [<span data-ttu-id="92792-129">Codierung und Dateierstellung</span><span class="sxs-lookup"><span data-stu-id="92792-129">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)

## <a name="related-topics"></a><span data-ttu-id="92792-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92792-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92792-131">Media Foundation-Architektur</span><span class="sxs-lookup"><span data-stu-id="92792-131">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="92792-132">**Imfmediasession**</span><span class="sxs-lookup"><span data-stu-id="92792-132">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> </dl>

 

 



