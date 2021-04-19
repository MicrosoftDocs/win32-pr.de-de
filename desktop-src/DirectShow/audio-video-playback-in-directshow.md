---
description: In diesem Tutorial wird gezeigt, wie Sie eine DirectShow-Anwendung schreiben, die eine Mediendatei wieder gibt.
ms.assetid: 88f4762a-e6e6-4b1e-9951-a409d9d80da9
title: Audiowiedergabe und Video Wiedergabe in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca3d681386d85eafc4f32b4e688b920253a51a7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346813"
---
# <a name="audiovideo-playback-in-directshow"></a><span data-ttu-id="da676-103">Audiowiedergabe und Video Wiedergabe in DirectShow</span><span class="sxs-lookup"><span data-stu-id="da676-103">Audio/Video Playback in DirectShow</span></span>

<span data-ttu-id="da676-104">In diesem Tutorial wird gezeigt, wie Sie eine DirectShow-Anwendung schreiben, die eine Mediendatei wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="da676-104">This tutorial shows how to write a DirectShow application that plays a media file.</span></span>

<span data-ttu-id="da676-105">Bevor Sie dieses Tutorial lesen, sollten Sie die folgenden Themen lesen:</span><span class="sxs-lookup"><span data-stu-id="da676-105">Before reading this tutorial, you might want to read the following topics:</span></span>

-   [<span data-ttu-id="da676-106">Einführung in die DirectShow-Anwendungsprogrammierung</span><span class="sxs-lookup"><span data-stu-id="da676-106">Introduction to DirectShow Application Programming</span></span>](introduction-to-directshow-application-programming.md)
-   [<span data-ttu-id="da676-107">Wiedergeben einer Datei</span><span class="sxs-lookup"><span data-stu-id="da676-107">How To Play a File</span></span>](how-to-play-a-file.md)
-   [<span data-ttu-id="da676-108">Informationen zu DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="da676-108">About DirectShow Filters</span></span>](about-directshow-filters.md)
-   [<span data-ttu-id="da676-109">Informationen zum Filter Graph-Manager</span><span class="sxs-lookup"><span data-stu-id="da676-109">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)

## <a name="in-this-section"></a><span data-ttu-id="da676-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="da676-110">In this section</span></span>

-   [<span data-ttu-id="da676-111">Schritt 1: Deklarieren der dshowplayer-Klasse</span><span class="sxs-lookup"><span data-stu-id="da676-111">Step 1: Declare the DShowPlayer Class</span></span>](step-1--declare-the-dshowplayer-class.md)
-   [<span data-ttu-id="da676-112">Schritt 2: Deklarieren von cvideorenderer und abgeleiteten Klassen</span><span class="sxs-lookup"><span data-stu-id="da676-112">Step 2: Declare CVideoRenderer and Derived Classes</span></span>](step-2--declare-cvideorenderer-and-derived-classes.md)
-   [<span data-ttu-id="da676-113">Schritt 3: Erstellen des Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="da676-113">Step 3: Build the Filter Graph</span></span>](step-3--build-the-filter-graph.md)
-   [<span data-ttu-id="da676-114">Schritt 4: Hinzufügen des Videorenderers</span><span class="sxs-lookup"><span data-stu-id="da676-114">Step 4: Add the Video Renderer</span></span>](step-4--add-the-video-renderer.md)
-   [<span data-ttu-id="da676-115">Schritt 5: Hinzufügen von Video Funktionen</span><span class="sxs-lookup"><span data-stu-id="da676-115">Step 5: Add Video Functionality</span></span>](step-5--add-video-functionality.md)
-   [<span data-ttu-id="da676-116">Schritt 6: Behandeln von Diagramm Ereignissen</span><span class="sxs-lookup"><span data-stu-id="da676-116">Step 6: Handle Graph Events</span></span>](step-6--handle-graph-events.md)
-   [<span data-ttu-id="da676-117">Schritt 7: Transport Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="da676-117">Step 7: Transport Controls</span></span>](step-7--transport-controls.md)
-   [<span data-ttu-id="da676-118">Beispiel zur DirectShow-Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="da676-118">DirectShow Playback Example</span></span>](directshow-playback-example.md)

## <a name="related-topics"></a><span data-ttu-id="da676-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="da676-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da676-120">Verwenden von DirectShow</span><span class="sxs-lookup"><span data-stu-id="da676-120">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



