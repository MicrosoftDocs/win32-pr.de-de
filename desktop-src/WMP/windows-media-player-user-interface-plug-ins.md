---
title: Plug-Ins für Windows Media Player-Benutzeroberfläche
description: Plug-Ins für Windows Media Player-Benutzeroberfläche
ms.assetid: 71f53abe-310f-429a-bb23-5291bebdc432
keywords:
- Windows Media Player-Plug-ins
- Windows Media Player, Benutzerschnittstellen-Plug-ins
- Windows Media Player-Plug-ins, Benutzeroberfläche
- Plug-ins, Benutzeroberfläche
- Plug-Ins für die Benutzeroberfläche, Informationen zu
- UI-Plug-ins, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24050f24ef4412d3de9efd5faac6c2af90451dc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338378"
---
# <a name="windows-media-player-user-interface-plug-ins"></a><span data-ttu-id="ec310-109">Plug-Ins für Windows Media Player-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="ec310-109">Windows Media Player User Interface Plug-ins</span></span>

<span data-ttu-id="ec310-110">Microsoft Windows Media Player stellt eine Architektur bereit, die es dem Benutzer ermöglicht, Plug-in-Programme zu installieren und zu aktivieren, die Benutzeroberflächen Funktionen zum vollständigen Modus des Players hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ec310-110">Microsoft Windows Media Player provides an architecture that enables the user to install and activate plug-in programs that add user interface (UI) functionality to the full mode of the player.</span></span> <span data-ttu-id="ec310-111">Ein typisches Plug-in für die Benutzeroberfläche kann es einem Benutzer ermöglichen, die CD zu kaufen, die die aktuell wiedergegebene Spur enthält, oder auf zusätzliche Informationen über den Künstler zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ec310-111">A typical UI plug-in might allow a user to buy the CD that contains the currently playing track or to access additional information about the artist.</span></span> <span data-ttu-id="ec310-112">In diesem Abschnitt des Windows Media Player Software Development Kit (SDK) finden Sie die Programmierinformationen, die Sie benötigen, um Ihr eigenes UI-Plug-in zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec310-112">This section of the Windows Media Player Software Development Kit (SDK) provides you with the programming information you need to create your own UI plug-in.</span></span>

<span data-ttu-id="ec310-113">Die Benutzeroberflächen-Plug-in-Dokumentation ist in drei Abschnitte unterteilt:</span><span class="sxs-lookup"><span data-stu-id="ec310-113">The UI plug-in documentation is divided into three sections:</span></span>



| <span data-ttu-id="ec310-114">`Section`</span><span class="sxs-lookup"><span data-stu-id="ec310-114">Section</span></span>                                                                                            | <span data-ttu-id="ec310-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec310-115">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec310-116">Informationen zu Benutzeroberflächen-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="ec310-116">About User Interface Plug-ins</span></span>](about-user-interface-plug-ins.md)                                 | <span data-ttu-id="ec310-117">Bietet eine Übersicht über die Architektur, die für Benutzeroberflächen-Plug-ins verwendet wird. Lesen Sie diesen Abschnitt, um sich mit den allgemeinen Konzepten dieser Technologie vertraut zu machen.</span><span class="sxs-lookup"><span data-stu-id="ec310-117">Provides an overview of the architecture used for UI plug-ins. Read this section to learn the general concepts involved with this technology.</span></span> |
| [<span data-ttu-id="ec310-118">Programmier Handbuch für Benutzeroberflächen-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="ec310-118">User Interface Plug-ins Programming Guide</span></span>](user-interface-plug-ins-programming-guide.md)         | <span data-ttu-id="ec310-119">Erläutert, was Sie tun müssen, um ein UI-Plug-in zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec310-119">Explains what you need to do to create a UI plug-in.</span></span> <span data-ttu-id="ec310-120">Dieser Abschnitt enthält Beispielcode und schrittweise Anleitungen.</span><span class="sxs-lookup"><span data-stu-id="ec310-120">This section contains example code and step-by-step procedures.</span></span>                          |
| [<span data-ttu-id="ec310-121">Programmier Referenz zu Benutzeroberflächen-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="ec310-121">User Interface Plug-ins Programming Reference</span></span>](user-interface-plug-ins-programming-reference.md) | <span data-ttu-id="ec310-122">Bietet eine ausführliche Referenz für die COM-Schnittstelle und Methoden, die vom Windows Media Player SDK für UI-Plug-Ins unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ec310-122">Provides a detailed reference for the COM interface and methods supported by the Windows Media Player SDK for UI plug-ins.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="ec310-123">Windows Media Player 10 Mobile bietet das gleiche Plug-in-Modell wie die Windows-Desktop Media Player.</span><span class="sxs-lookup"><span data-stu-id="ec310-123">Windows Media Player 10 Mobile provides the same plug-in model as the desktop Windows Media Player.</span></span> <span data-ttu-id="ec310-124">Mit diesem Plug-in-Modell können Sie Hintergrund-Plug-ins zum Überwachen von Ereignissen, zum Anzeigen des Status von Eigenschaften usw. verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec310-124">This plug-in model enables you to use background plug-ins for monitoring events, displaying the status of properties, and so on.</span></span> <span data-ttu-id="ec310-125">Im Programmier Handbuch in diesem Abschnitt wird beschrieben, wie Sie ein Plug-in für die Benutzeroberfläche für Windows Media Player 10 Mobile mithilfe des Assistenten für Desktop-Windows-Media Player Plug-in erstellen.</span><span class="sxs-lookup"><span data-stu-id="ec310-125">The programming guide in this section describes how to create a background UI plug-in for Windows Media Player 10 Mobile by using the desktop Windows Media Player Plug-in Wizard.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ec310-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ec310-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec310-127">**Windows Media Player-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="ec310-127">**Windows Media Player Plug-ins**</span></span>](windows-media-player-plug-ins.md)
</dt> </dl>

 

 




