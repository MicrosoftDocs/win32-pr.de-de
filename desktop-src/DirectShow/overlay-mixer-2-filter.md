---
description: Filter für Überlagerungs Mixer 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Filter für Überlagerungs Mixer 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22976a58b272cf04c098c102d32d154e361b8b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342558"
---
# <a name="overlay-mixer-2-filter"></a><span data-ttu-id="8b8b1-103">Filter für Überlagerungs Mixer 2</span><span class="sxs-lookup"><span data-stu-id="8b8b1-103">Overlay Mixer 2 Filter</span></span>

<span data-ttu-id="8b8b1-104">Der Filter für den Overlay-Mixer 2 ist mit dem [Überlagerungs-Mischungs](overlay-mixer-filter.md) Filter identisch, außer:</span><span class="sxs-lookup"><span data-stu-id="8b8b1-104">The Overlay Mixer 2 filter is identical to the [Overlay Mixer](overlay-mixer-filter.md) filter, except:</span></span>

-   <span data-ttu-id="8b8b1-105">Es werden nur Medientypen mit [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Formaten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8b8b1-105">It supports only media types with [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats.</span></span>
-   <span data-ttu-id="8b8b1-106">Sie hat einen höheren Wert, der die automatische Hinzufügung zu einem Filter Diagramm ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="8b8b1-106">It has a higher merit, which enables it to be added to a filter graph automatically.</span></span>

<span data-ttu-id="8b8b1-107">Der Overlay-Mixer 2 wird bereitgestellt, damit der Filter Graph-Manager ihn dem Diagramm hinzufügt, wenn er ein nicht-DVD-MPEG-2-Video rendert.</span><span class="sxs-lookup"><span data-stu-id="8b8b1-107">The Overlay Mixer 2 is provided so that the Filter Graph Manager will add it to the graph when it renders non-DVD MPEG-2 video.</span></span> <span data-ttu-id="8b8b1-108">Die Wahl, ob der Overlay-Mixer oder der Überlagerungs-Mixer 2 verwendet werden soll, wird von der Komponente behandelt, die das Diagramm erstellt, entweder mit dem Filter Graph-Manager, dem Erfassungs Diagramm-Generator oder dem DVD-Diagramm-Generator.</span><span class="sxs-lookup"><span data-stu-id="8b8b1-108">The choice of whether to use the Overlay Mixer or the Overlay Mixer 2 is handled by the component that builds the graph, either the Filter Graph Manager, the Capture Graph Builder, or the DVD Graph Builder.</span></span> <span data-ttu-id="8b8b1-109">Aus Sicht der Anwendung sind Sie derselbe Filter mit denselben Schnittstellen und Funktionen.</span><span class="sxs-lookup"><span data-stu-id="8b8b1-109">From an application perspective, they are the same filter, with the same interfaces and functionality.</span></span>

<span data-ttu-id="8b8b1-110">Die folgende Tabelle enthält spezifische Informationen zum Overlay-Mixer 2.</span><span class="sxs-lookup"><span data-stu-id="8b8b1-110">The following table contains information specific to the Overlay Mixer 2.</span></span> <span data-ttu-id="8b8b1-111">Alle anderen Filterdaten finden Sie in der Dokumentation für den Overlay-Mixer.</span><span class="sxs-lookup"><span data-stu-id="8b8b1-111">For all other filter data, refer to the documentation for the Overlay Mixer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8b8b1-112">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="8b8b1-112">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="8b8b1-113">Formattyp: Format_VIDEOINFO2</span><span class="sxs-lookup"><span data-stu-id="8b8b1-113">Format Type: Format_VIDEOINFO2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b8b1-114">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="8b8b1-114">Filter CLSID</span></span></td>
<td><span data-ttu-id="8b8b1-115">CLSID_OverlayMixer2</span><span class="sxs-lookup"><span data-stu-id="8b8b1-115">CLSID_OverlayMixer2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b8b1-116"><a href="merit.md">Verdienst</a></span><span class="sxs-lookup"><span data-stu-id="8b8b1-116"><a href="merit.md">Merit</a></span></span></td>
<td><ul>
<li><span data-ttu-id="8b8b1-117">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="8b8b1-117">MERIT_UNLIKELY</span></span></li>
<li><span data-ttu-id="8b8b1-118">Windows Vista oder höher: MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="8b8b1-118">Windows Vista or later: MERIT_DO_NOT_USE</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8b8b1-119">In Windows Vista oder höher ist die Verwendung des Filters für den Overlay-Mixer 2 \_ nicht sinnvoll, \_ \_ da die neueren Videorenderer (VMR-7, VMR-9 und EVR) alle **VIDEOINFOHEADER2** -Formate unterstützen, und daher ist es nicht notwendig, den Overlay-Mixer zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8b8b1-119">In Windows Vista or later, the merit of the Overlay Mixer 2 filter is MERIT\_DO\_NOT\_USE, because the newer video renderers (VMR-7, VMR-9, and EVR) all support **VIDEOINFOHEADER2** formats, and therefore it is not necessary to use the Overlay Mixer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b8b1-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8b8b1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b8b1-121">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="8b8b1-121">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



