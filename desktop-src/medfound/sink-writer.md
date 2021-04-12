---
description: Der senkwriter ist eine Komponente zum Codieren von Audiodateien oder Videodateien.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Senke-Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b30d75e369de343bae61ba56dfd05c0d5d12a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344388"
---
# <a name="sink-writer"></a><span data-ttu-id="aa6a9-103">Senke-Writer</span><span class="sxs-lookup"><span data-stu-id="aa6a9-103">Sink Writer</span></span>

<span data-ttu-id="aa6a9-104">Der senkwriter ist eine Komponente zum Codieren von Audiodateien oder Videodateien.</span><span class="sxs-lookup"><span data-stu-id="aa6a9-104">The sink writer is a component for encoding audio or video files.</span></span>

<span data-ttu-id="aa6a9-105">Das folgende Diagramm zeigt, wie eine Anwendung den senkwriter zum Codieren der Audiodatei und der Audiodatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="aa6a9-105">The following diagram shows, at a high level, how an application uses the sink writer to encode and audio/video file.</span></span>

![ein Diagramm, das den Senke-Writer anzeigt.](images/encoding09.png)

<span data-ttu-id="aa6a9-107">Der Senke Writer hostet eine Medien Senke und optional einen oder mehrere Encoder.</span><span class="sxs-lookup"><span data-stu-id="aa6a9-107">The sink writer hosts a media sink and optionally one or more encoders.</span></span> <span data-ttu-id="aa6a9-108">Die Encoder konvertieren unkomprimierte Audiodaten oder Videodaten in codierte Bitstreams.</span><span class="sxs-lookup"><span data-stu-id="aa6a9-108">The encoders convert uncompressed audio or video data to encoded bitstreams.</span></span> <span data-ttu-id="aa6a9-109">Die Medien Senke gibt die Bitstreams in einer Datei aus.</span><span class="sxs-lookup"><span data-stu-id="aa6a9-109">The media sink outputs the bitstreams to a file.</span></span> <span data-ttu-id="aa6a9-110">Der Senke-Writer führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="aa6a9-110">The sink writer performs the following tasks:</span></span>

-   <span data-ttu-id="aa6a9-111">Lädt die Medien Senke.</span><span class="sxs-lookup"><span data-stu-id="aa6a9-111">Loads the media sink.</span></span>
-   <span data-ttu-id="aa6a9-112">Findet und lädt die Encoder.</span><span class="sxs-lookup"><span data-stu-id="aa6a9-112">Finds and loads the encoders.</span></span>
-   <span data-ttu-id="aa6a9-113">Verwaltet den Datenfluss zu den Encodern und der Medien Senke.</span><span class="sxs-lookup"><span data-stu-id="aa6a9-113">Manages the data flow to the encoders and the media sink.</span></span>

<span data-ttu-id="aa6a9-114">Die Anwendung übergibt Audiodaten und Videodaten als Eingabe an den senkwriter.</span><span class="sxs-lookup"><span data-stu-id="aa6a9-114">The application passes audio/video data to the sink writer as input.</span></span> <span data-ttu-id="aa6a9-115">Es spielt keine Rolle, wie die Anwendung die Eingabedaten abruft oder generiert.</span><span class="sxs-lookup"><span data-stu-id="aa6a9-115">It does not matter how the application obtains or generates the input data.</span></span> <span data-ttu-id="aa6a9-116">Eine Möglichkeit ist die Verwendung des [Quell Readers](source-reader.md), wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="aa6a9-116">One option is to use the [Source Reader](source-reader.md), as shown in the following diagram.</span></span> <span data-ttu-id="aa6a9-117">Der sendende Writer erfordert jedoch nicht die Verwendung des Quell Readers.</span><span class="sxs-lookup"><span data-stu-id="aa6a9-117">However, the sink writer does not require the use of the source reader.</span></span> <span data-ttu-id="aa6a9-118">Diese beiden Komponenten sind unabhängig voneinander.</span><span class="sxs-lookup"><span data-stu-id="aa6a9-118">These two components are independent.</span></span>

![ein Diagramm, in dem der Quell-und der Senke Writer angezeigt werden.](images/encoding02.png)

## <a name="in-this-section"></a><span data-ttu-id="aa6a9-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="aa6a9-120">In this section</span></span>

-   [<span data-ttu-id="aa6a9-121">Verwenden des Senke Writers</span><span class="sxs-lookup"><span data-stu-id="aa6a9-121">Using the Sink Writer</span></span>](using-the-sink-writer.md)
-   [<span data-ttu-id="aa6a9-122">Tutorial: Verwenden des senkwriter zum Codieren von Videos</span><span class="sxs-lookup"><span data-stu-id="aa6a9-122">Tutorial: Using the Sink Writer to Encode Video</span></span>](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a><span data-ttu-id="aa6a9-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aa6a9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa6a9-124">Codierung und Dateierstellung</span><span class="sxs-lookup"><span data-stu-id="aa6a9-124">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="aa6a9-125">Übersicht über die Codierung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aa6a9-125">Overview of Encoding in Media Foundation</span></span>](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



