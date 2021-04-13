---
title: Modus für beibehaltene Modus und unmittelbarer
description: Grafik-APIs können in beibehaltene Modus-APIs und APIs für den unmittelbaren Modus aufgeteilt werden.
ms.assetid: 0a98e8ee-4bc1-490c-867e-42bceae8a1f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec3b89cd300f957211a9d4990c35ccbb70fa2b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104559486"
---
# <a name="retained-mode-versus-immediate-mode"></a><span data-ttu-id="43426-103">Modus für beibehaltene Modus und unmittelbarer</span><span class="sxs-lookup"><span data-stu-id="43426-103">Retained Mode Versus Immediate Mode</span></span>

<span data-ttu-id="43426-104">Grafik-APIs können in *beibehaltene Modus-* APIs und APIs für den *unmittelbaren Modus* aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="43426-104">Graphics APIs can be divided into *retained-mode* APIs and *immediate-mode* APIs.</span></span> <span data-ttu-id="43426-105">Direct2D ist eine API im unmittelbaren Modus.</span><span class="sxs-lookup"><span data-stu-id="43426-105">Direct2D is an immediate-mode API.</span></span> <span data-ttu-id="43426-106">Windows Presentation Foundation (WPF) ist ein Beispiel für eine API im beibehaltenen Modus.</span><span class="sxs-lookup"><span data-stu-id="43426-106">Windows Presentation Foundation (WPF) is an example of a retained-mode API.</span></span>

<span data-ttu-id="43426-107">Eine API im beibehaltenen Modus ist deklarativ.</span><span class="sxs-lookup"><span data-stu-id="43426-107">A retained-mode API is declarative.</span></span> <span data-ttu-id="43426-108">Die Anwendung erstellt eine Szene aus Grafik primitiven, z. b. Formen und Linien.</span><span class="sxs-lookup"><span data-stu-id="43426-108">The application constructs a scene from graphics primitives, such as shapes and lines.</span></span> <span data-ttu-id="43426-109">In der Grafikbibliothek wird ein Modell der Szene im Arbeitsspeicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="43426-109">The graphics library stores a model of the scene in memory.</span></span> <span data-ttu-id="43426-110">Um einen Frame zu zeichnen, transformiert die Grafikbibliothek die Szene in eine Reihe von Zeichnungs Befehlen.</span><span class="sxs-lookup"><span data-stu-id="43426-110">To draw a frame, the graphics library transforms the scene into a set of drawing commands.</span></span> <span data-ttu-id="43426-111">Zwischen Frames hält die Grafikbibliothek die Szene im Speicher.</span><span class="sxs-lookup"><span data-stu-id="43426-111">Between frames, the graphics library keeps the scene in memory.</span></span> <span data-ttu-id="43426-112">Um zu ändern, was gerendert wird, gibt die Anwendung einen Befehl zum Aktualisieren der Szene aus, z. –. um eine Form hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="43426-112">To change what is rendered, the application issues a command to update the scene—for example, to add or remove a shape.</span></span> <span data-ttu-id="43426-113">Die Bibliothek ist dann für das Neuzeichnen der Szene verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="43426-113">The library is then responsible for redrawing the scene.</span></span>

![ein Diagramm, das Grafik im beibehaltenen Modus anzeigt.](images/graphics06.png)

<span data-ttu-id="43426-115">Eine API im sofortigen Modus ist Verfahrensweise.</span><span class="sxs-lookup"><span data-stu-id="43426-115">An immediate-mode API is procedural.</span></span> <span data-ttu-id="43426-116">Jedes Mal, wenn ein neuer Frame gezeichnet wird, gibt die Anwendung die Zeichnungs Befehle direkt aus.</span><span class="sxs-lookup"><span data-stu-id="43426-116">Each time a new frame is drawn, the application directly issues the drawing commands.</span></span> <span data-ttu-id="43426-117">Die Grafikbibliothek speichert kein Szenen Modell zwischen Frames.</span><span class="sxs-lookup"><span data-stu-id="43426-117">The graphics library does not store a scene model between frames.</span></span> <span data-ttu-id="43426-118">Stattdessen wird die Szene von der Anwendung nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="43426-118">Instead, the application keeps track of the scene.</span></span>

![ein Diagramm, das Grafik im unmittelbaren Modus anzeigt.](images/graphics07.png)

<span data-ttu-id="43426-120">APIs im beibehaltenen Modus können einfacher zu verwenden sein, da die API mehr Arbeit für Sie erledigt, wie z. b. Initialisierung, Zustands Verwaltung und Bereinigung.</span><span class="sxs-lookup"><span data-stu-id="43426-120">Retained-mode APIs can be simpler to use, because the API does more of the work for you, such as initialization, state maintenance, and cleanup.</span></span> <span data-ttu-id="43426-121">Sie sind dagegen oft weniger flexibel, da die API ein eigenes Szenen Modell erzwingt.</span><span class="sxs-lookup"><span data-stu-id="43426-121">On the other hand, they are often less flexible, because the API imposes its own scene model.</span></span> <span data-ttu-id="43426-122">Außerdem kann eine API im beibehaltenen Modus höhere Speicheranforderungen aufweisen, da Sie ein allgemeines Szenen Modell bereitstellen muss.</span><span class="sxs-lookup"><span data-stu-id="43426-122">Also, a retained-mode API can have higher memory requirements, because it needs to provide a general-purpose scene model.</span></span> <span data-ttu-id="43426-123">Mit einer API im unmittelbaren Modus können Sie gezielte Optimierungen implementieren.</span><span class="sxs-lookup"><span data-stu-id="43426-123">With an immediate-mode API, you can implement targeted optimizations.</span></span>

## <a name="next"></a><span data-ttu-id="43426-124">Nächste</span><span class="sxs-lookup"><span data-stu-id="43426-124">Next</span></span>

[<span data-ttu-id="43426-125">Ihr erstes Direct2D-Programm</span><span class="sxs-lookup"><span data-stu-id="43426-125">Your First Direct2D Program</span></span>](your-first-direct2d-program.md)

 

 




