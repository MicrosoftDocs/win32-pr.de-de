---
title: Leitfaden zum Erstellen von Skin
description: Leitfaden zum Erstellen von Skin
ms.assetid: 86c77764-5c8c-4493-ac2d-15268c1ba564
keywords:
- Windows-Media Player, Skins
- Windows Media Player Skins, Erstellungs Handbuch
- Skins, Erstellungs Handbuch
- Erstellen von Skins, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7214accedf24bd80449bf8952bc9268f9b9bf49d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341444"
---
# <a name="skin-creation-guide"></a><span data-ttu-id="7fef7-107">Leitfaden zum Erstellen von Skin</span><span class="sxs-lookup"><span data-stu-id="7fef7-107">Skin Creation Guide</span></span>

<span data-ttu-id="7fef7-108">Dieses Handbuch stellt eine Reihe ausführlicher Erläuterungen zum Erstellen verschiedener Arten von Skins dar.</span><span class="sxs-lookup"><span data-stu-id="7fef7-108">This guide is a series of detailed explanations of how to create different kinds of skins.</span></span> <span data-ttu-id="7fef7-109">Weitere allgemeine Informationen zu Skins finden Sie unter [about Skins](about-skins.md)(Informationen zu Skins).</span><span class="sxs-lookup"><span data-stu-id="7fef7-109">For more general information on skins, see [About Skins](about-skins.md).</span></span> <span data-ttu-id="7fef7-110">Spezifische Details zu allen Attributen, Methoden und Ereignissen, die in Skins verwendet werden, finden Sie in der Referenz zur Design- [Programmierung](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="7fef7-110">For specific details about every attribute, method, and event used in skins, see the [Skin Programming Reference](skin-programming-reference.md).</span></span> <span data-ttu-id="7fef7-111">Wenn Sie mehr an der Programmierung ihrer Skin interessiert sind, möchten Sie möglicherweise den Teil dieses SDK lesen, der das [Windows Media Player-Objektmodell](windows-media-player-object-model.md)abdeckt.</span><span class="sxs-lookup"><span data-stu-id="7fef7-111">As you get more involved in the programming of your skin, you may want to read the part of this SDK covering the [Windows Media Player Object Model](windows-media-player-object-model.md).</span></span>

<span data-ttu-id="7fef7-112">In diesem Handbuch erhalten Sie eine Anleitung zum Erstellen der Kunst für Adobe Photoshop 5,5, ein gängiges Programm zur Bearbeitung von Grafiken.</span><span class="sxs-lookup"><span data-stu-id="7fef7-112">In this guide, instructions for creating the art will be given for Adobe Photoshop 5.5, a popular art manipulation program.</span></span> <span data-ttu-id="7fef7-113">Die speziellen Anweisungen können sich unterscheiden, wenn Sie über ein ähnliches Kunstprogramm wie z. b. "Jasc Paint-Pro" oder "sonfoundry" verfügen, aber die Konzepte sind identisch.</span><span class="sxs-lookup"><span data-stu-id="7fef7-113">The specific instructions may be different if you have a similar art program such as Jasc Paint Shop Pro or Sonic Foundry Viscosity, but the concepts will be the same.</span></span> <span data-ttu-id="7fef7-114">Photoshop wurde aus zwei Gründen gewählt: Es ist ein beliebtes Kunstprogramm für kommerzielle Künstler und funktioniert mit Ebenen.</span><span class="sxs-lookup"><span data-stu-id="7fef7-114">Photoshop was chosen for two reasons: it is a popular art program for commercial artists, and it works with layers.</span></span> <span data-ttu-id="7fef7-115">Wie Sie in den Tutorials sehen werden, sind Ebenen für die Erstellung von Skin sehr nützlich.</span><span class="sxs-lookup"><span data-stu-id="7fef7-115">As you will see in the tutorials, layers are very useful for skin creation.</span></span>

<span data-ttu-id="7fef7-116">In diesem Handbuch werden die folgenden Aufgaben behandelt.</span><span class="sxs-lookup"><span data-stu-id="7fef7-116">This guide will cover the following tasks.</span></span>



| <span data-ttu-id="7fef7-117">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="7fef7-117">Task</span></span>                                                     | <span data-ttu-id="7fef7-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fef7-118">Description</span></span>                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fef7-119">Aufbauen Ihrer ersten Skin</span><span class="sxs-lookup"><span data-stu-id="7fef7-119">Building Your First Skin</span></span>](building-your-first-skin.md) | <span data-ttu-id="7fef7-120">Eine exemplarische Vorgehensweise für eine einfache Skin, mit der Windows Media Player gestartet und beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7fef7-120">A walk-through of a simple skin that starts and stops Windows Media Player.</span></span>                     |
| [<span data-ttu-id="7fef7-121">Hinzufügen einer Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="7fef7-121">Adding a Playlist</span></span>](adding-a-playlist.md)               | <span data-ttu-id="7fef7-122">Verwenden einer einfachen Wiedergabeliste</span><span class="sxs-lookup"><span data-stu-id="7fef7-122">How to use a simple playlist.</span></span>                                                                   |
| [<span data-ttu-id="7fef7-123">Auswählen von Dateien</span><span class="sxs-lookup"><span data-stu-id="7fef7-123">Choosing Files</span></span>](choosing-files.md)                     | <span data-ttu-id="7fef7-124">Gewusst wie: Auswählen von Dateien mit dem Dialogfeld "Datei öffnen"</span><span class="sxs-lookup"><span data-stu-id="7fef7-124">How to pick files with an open file dialog box.</span></span>                                                 |
| [<span data-ttu-id="7fef7-125">Hinzufügen von Videos</span><span class="sxs-lookup"><span data-stu-id="7fef7-125">Adding Video</span></span>](adding-video.md)                         | <span data-ttu-id="7fef7-126">Gewusst wie: Platzieren eines Videofensters in der Skin</span><span class="sxs-lookup"><span data-stu-id="7fef7-126">How to put a video window into your skin.</span></span>                                                       |
| [<span data-ttu-id="7fef7-127">Hinzufügen von Visualisierungen</span><span class="sxs-lookup"><span data-stu-id="7fef7-127">Adding Visualizations</span></span>](adding-visualizations.md)       | <span data-ttu-id="7fef7-128">Vorgehensweise beim Hinzufügen von Visualisierungen</span><span class="sxs-lookup"><span data-stu-id="7fef7-128">How to add visualizations.</span></span>                                                                      |
| [<span data-ttu-id="7fef7-129">Fügen eines Schiebereglers</span><span class="sxs-lookup"><span data-stu-id="7fef7-129">Adding a Slider</span></span>](adding-a-slider.md)                   | <span data-ttu-id="7fef7-130">So verwenden Sie einen Schieberegler, um den Fortschritt des Medien Inhalts zu verfolgen... und lassen Sie den Benutzer die Änderungen ändern!</span><span class="sxs-lookup"><span data-stu-id="7fef7-130">How to use a slider to track the progress of your media content ... and let the user change it!</span></span> |
| [<span data-ttu-id="7fef7-131">Erstellen benutzerdefinierter Schieberegler</span><span class="sxs-lookup"><span data-stu-id="7fef7-131">Creating Custom Sliders</span></span>](creating-custom-sliders.md)   | <span data-ttu-id="7fef7-132">Steuern des Volumes mit einem benutzerdefinierten Schieberegler.</span><span class="sxs-lookup"><span data-stu-id="7fef7-132">How to control the volume with a custom slider.</span></span>                                                 |
| [<span data-ttu-id="7fef7-133">Weitere Skin-Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fef7-133">Other Skin Samples</span></span>](other-skin-samples.md)             | <span data-ttu-id="7fef7-134">Weitere Informationen finden Sie im Abschnitt mit den Beispielen des SDK.</span><span class="sxs-lookup"><span data-stu-id="7fef7-134">See the samples section of the SDK.</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="7fef7-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7fef7-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fef7-136">**Windows Media Player Skins**</span><span class="sxs-lookup"><span data-stu-id="7fef7-136">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




