---
description: Erstellen einer Zeitachse
ms.assetid: 4909f797-d296-4c9f-83fb-543e48bbe75d
title: Erstellen einer Zeitachse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c16b1134eb92b3e3ac5a0f1919d7c4a2736b206
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392722"
---
# <a name="constructing-a-timeline"></a><span data-ttu-id="16ecc-103">Erstellen einer Zeitachse</span><span class="sxs-lookup"><span data-stu-id="16ecc-103">Constructing a Timeline</span></span>

<span data-ttu-id="16ecc-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="16ecc-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="16ecc-105">In diesem Artikel wird beschrieben, wie Sie eine Zeitachse in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) erstellen.</span><span class="sxs-lookup"><span data-stu-id="16ecc-105">This article describes how to construct a timeline in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="16ecc-106">Sie enthält eine Beispiel Konsolenanwendung, die eine Zeitachse erstellt und rendert.</span><span class="sxs-lookup"><span data-stu-id="16ecc-106">It presents an example console application that creates a timeline and renders it.</span></span> <span data-ttu-id="16ecc-107">Die Zeitachse ist minimal und besteht aus einer einzelnen Videogruppe mit einem Quell Clip, aber Sie veranschaulicht die meisten Konzepte, die zum Erstellen komplexerer Zeitachsen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="16ecc-107">The timeline is minimal, consisting of a single video group with one source clip, but it demonstrates most of the concepts needed to create more complex timelines.</span></span>

<span data-ttu-id="16ecc-108">Dieser Artikel enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="16ecc-108">This article contains the following topics.</span></span>

-   [<span data-ttu-id="16ecc-109">Erstellen von Zeitachsen Objekten</span><span class="sxs-lookup"><span data-stu-id="16ecc-109">Creating Timeline Objects</span></span>](creating-timeline-objects.md)
-   [<span data-ttu-id="16ecc-110">Erstellen von Gruppen, Kompositionen und Spuren</span><span class="sxs-lookup"><span data-stu-id="16ecc-110">Creating Groups, Compositions, and Tracks</span></span>](creating-groups-compositions-and-tracks.md)
-   [<span data-ttu-id="16ecc-111">Festlegen des Medientyps "Gruppe"</span><span class="sxs-lookup"><span data-stu-id="16ecc-111">Setting the Group Media Type</span></span>](setting-the-group-media-type.md)
-   [<span data-ttu-id="16ecc-112">Hinzufügen einer Quelle</span><span class="sxs-lookup"><span data-stu-id="16ecc-112">Adding a Source</span></span>](adding-a-source.md)
-   [<span data-ttu-id="16ecc-113">Erstellen einer Zeitachse: Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="16ecc-113">Creating a Timeline: Example Code</span></span>](creating-a-timeline--example-code.md)

## <a name="related-topics"></a><span data-ttu-id="16ecc-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="16ecc-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16ecc-115">Verwenden von DirectShow-Bearbeitungs Diensten</span><span class="sxs-lookup"><span data-stu-id="16ecc-115">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



