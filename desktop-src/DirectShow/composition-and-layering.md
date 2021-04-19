---
description: Komposition und Ebenenerstellung
ms.assetid: c1aefd92-b47f-4af1-8299-9ba401ad5fe8
title: Komposition und Ebenenerstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7dce1e1df87b5ffc5c65e9090c6fb7266b972d3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346390"
---
# <a name="composition-and-layering"></a><span data-ttu-id="1471c-103">Komposition und Ebenenerstellung</span><span class="sxs-lookup"><span data-stu-id="1471c-103">Composition and Layering</span></span>

<span data-ttu-id="1471c-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="1471c-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="1471c-105">In einer Auflistung von Spuren hat der erste Titel die niedrigste Priorität (Priorität 0), und jede nachfolgende Spur hat eine Priorität, die eine Ebene höher ist.</span><span class="sxs-lookup"><span data-stu-id="1471c-105">In a collection of tracks, the first track has the lowest priority (priority 0) and each subsequent track has a priority one level higher.</span></span> <span data-ttu-id="1471c-106">Auf jeder Prioritätsstufe blenden die Quell Clips in dieser Nachverfolgung die Quell Clips in den nachstehenden Spuren aus, es sei denn, diese Ebene enthält auch einen Übergang.</span><span class="sxs-lookup"><span data-stu-id="1471c-106">At each priority level, the source clips in that track hide the source clips in the tracks below it, unless that layer also contains a transition.</span></span> <span data-ttu-id="1471c-107">Daher können Sie sich vorstellen, dass es beim Rendern mehrere Durchgänge gibt.</span><span class="sxs-lookup"><span data-stu-id="1471c-107">Thus you can imagine DES making several passes when it renders.</span></span>

<span data-ttu-id="1471c-108">Zuerst wird Track 0 gerendert.</span><span class="sxs-lookup"><span data-stu-id="1471c-108">First, it renders track 0.</span></span> <span data-ttu-id="1471c-109">Es gibt keine "unter"-Nachverfolgung 0, sodass leere Bereiche als solides schwarzes Bild gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="1471c-109">There is nothing "under" Track 0, so empty regions are rendered as a solid black image.</span></span> <span data-ttu-id="1471c-110">Übergänge in dieser Ebene treten zwischen dem schwarzen Bild und der Nachverfolgung 0 oder umgekehrt auf.</span><span class="sxs-lookup"><span data-stu-id="1471c-110">Transitions in this layer occur between the black image and track 0 or vice versa.</span></span> <span data-ttu-id="1471c-111">Des legt den Titel 1 auf der Nachverfolgung 0 fest und erzeugt dabei alle Übergänge zwischen den beiden Titeln.</span><span class="sxs-lookup"><span data-stu-id="1471c-111">DES lays track 1 on top of track 0, generating any transitions between the two tracks.</span></span> <span data-ttu-id="1471c-112">Das Ergebnis ist die Zusammensetzung der beiden Titel.</span><span class="sxs-lookup"><span data-stu-id="1471c-112">The result is the composite of the two tracks.</span></span> <span data-ttu-id="1471c-113">Anschließend wird Track 2 auf diesem zusammengesetzten platziert.</span><span class="sxs-lookup"><span data-stu-id="1471c-113">Next, it places track 2 onto this composite.</span></span> <span data-ttu-id="1471c-114">Übergänge auf dieser Ebene treten zwischen dem zusammengesetzten und dem Track 2 auf.</span><span class="sxs-lookup"><span data-stu-id="1471c-114">Transitions at this layer occur between the composite and track 2.</span></span> <span data-ttu-id="1471c-115">Der Prozess wird fortgesetzt, bis die letzte (höchste Priorität) nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="1471c-115">The process continues until the last (highest-priority) track is put down.</span></span>

<span data-ttu-id="1471c-116">Wenn mehrere Spuren zusammengeführt werden, Verhalten Sie sich wie ein einzelner Track (virtueller Titel genannt).</span><span class="sxs-lookup"><span data-stu-id="1471c-116">When several tracks are composited together, they behave like a single track (called a virtual track).</span></span> <span data-ttu-id="1471c-117">Das Kompositions Objekt kapselt dieses Verhalten, sodass komplexe Übergänge möglich sind.</span><span class="sxs-lookup"><span data-stu-id="1471c-117">The composition object encapsulates this behavior, making complex transitions possible.</span></span> <span data-ttu-id="1471c-118">Beispielsweise kann ein Videoclip auf einen zweiten Clip gesetzt werden, während der zusammengesetzte (beide Clips und das Löschen) zu einem dritten Clip werden.</span><span class="sxs-lookup"><span data-stu-id="1471c-118">For example, one video clip can wipe to a second clip, while the composite (both clips plus the wipe) fades to a third clip.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1471c-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1471c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1471c-120">Einführung in DirectShow-Bearbeitungs Dienste</span><span class="sxs-lookup"><span data-stu-id="1471c-120">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> </dl>

 

 



