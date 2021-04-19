---
description: Schreiben von DirectShow-Filtern
ms.assetid: ffbc92b2-4f45-439b-b140-49a66fc4d914
title: Schreiben von DirectShow-Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b266f3bbb9781dddcd2d0fb065b63d895a732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360121"
---
# <a name="writing-directshow-filters"></a><span data-ttu-id="d9b9b-103">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="d9b9b-103">Writing DirectShow Filters</span></span>

<span data-ttu-id="d9b9b-104">Wenn Sie einen Filter für die Verwendung in einem Microsoft DirectShow-Filter Diagramm entwickeln, lesen Sie die Artikel in diesem Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="d9b9b-104">If you are developing a filter for use in a Microsoft DirectShow filter graph, read the articles in this section.</span></span> <span data-ttu-id="d9b9b-105">Im Allgemeinen müssen Sie diesen Abschnitt nicht lesen, wenn Sie eine DirectShow-Anwendung schreiben.</span><span class="sxs-lookup"><span data-stu-id="d9b9b-105">In general, you do not have to read this section if you are writing a DirectShow application.</span></span> <span data-ttu-id="d9b9b-106">Die meisten Anwendungen greifen nicht auf Filter oder auf das Filter Diagramm auf der Ebene zu, die in diesem Abschnitt erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="d9b9b-106">Most applications do not access filters or the filter graph at the level discussed in this section.</span></span>

-   [<span data-ttu-id="d9b9b-107">Einführung in die DirectShow-Filter Entwicklung</span><span class="sxs-lookup"><span data-stu-id="d9b9b-107">Introduction to DirectShow Filter Development</span></span>](introduction-to-directshow-filter-development.md)
-   [<span data-ttu-id="d9b9b-108">Aufbauen von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="d9b9b-108">Building DirectShow Filters</span></span>](building-directshow-filters.md)
-   [<span data-ttu-id="d9b9b-109">Herstellen der Verbindung von Filtern</span><span class="sxs-lookup"><span data-stu-id="d9b9b-109">How Filters Connect</span></span>](how-filters-connect.md)
-   [<span data-ttu-id="d9b9b-110">Datenfluss für Filter Entwickler</span><span class="sxs-lookup"><span data-stu-id="d9b9b-110">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="d9b9b-111">Threads und kritische Abschnitte</span><span class="sxs-lookup"><span data-stu-id="d9b9b-111">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
-   [<span data-ttu-id="d9b9b-112">Qualitäts Steuerungs Verwaltung</span><span class="sxs-lookup"><span data-stu-id="d9b9b-112">Quality-Control Management</span></span>](quality-control-management.md)
-   [<span data-ttu-id="d9b9b-113">DirectShow und com</span><span class="sxs-lookup"><span data-stu-id="d9b9b-113">DirectShow and COM</span></span>](directshow-and-com.md)
-   [<span data-ttu-id="d9b9b-114">Schreiben von Quell Filtern</span><span class="sxs-lookup"><span data-stu-id="d9b9b-114">Writing Source Filters</span></span>](writing-source-filters.md)
-   [<span data-ttu-id="d9b9b-115">Schreiben von Transformations Filtern</span><span class="sxs-lookup"><span data-stu-id="d9b9b-115">Writing Transform Filters</span></span>](writing-transform-filters.md)
-   [<span data-ttu-id="d9b9b-116">Schreiben von Videorenderer</span><span class="sxs-lookup"><span data-stu-id="d9b9b-116">Writing Video Renderers</span></span>](writing-video-renderers.md)
-   [<span data-ttu-id="d9b9b-117">Schreiben von Erfassungs Filtern</span><span class="sxs-lookup"><span data-stu-id="d9b9b-117">Writing Capture Filters</span></span>](writing-capture-filters.md)
-   [<span data-ttu-id="d9b9b-118">Verfügbar machen von Erfassung und Komprimierungs Formaten</span><span class="sxs-lookup"><span data-stu-id="d9b9b-118">Exposing Capture and Compression Formats</span></span>](exposing-capture-and-compression-formats.md)
-   [<span data-ttu-id="d9b9b-119">Registrieren eines benutzerdefinierten Dateityps</span><span class="sxs-lookup"><span data-stu-id="d9b9b-119">Registering a Custom File Type</span></span>](registering-a-custom-file-type.md)
-   [<span data-ttu-id="d9b9b-120">Erstellen einer Filter Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="d9b9b-120">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)

 

 



