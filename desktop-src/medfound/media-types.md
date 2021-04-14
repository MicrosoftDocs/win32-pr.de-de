---
description: Medientypen
ms.assetid: 690fda6e-dcbd-44dc-968d-cc949126da81
title: Medientypen (Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acbfb1b637eef6acb664d3d95a0488f155c6916
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351619"
---
# <a name="media-types-media-foundation"></a><span data-ttu-id="91623-103">Medientypen (Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="91623-103">Media Types (Media Foundation)</span></span>

<span data-ttu-id="91623-104">Ein *Medientyp* ist eine Möglichkeit, das Format eines Mediendaten Stroms zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="91623-104">A *media type* is a way to describe the format of a media stream.</span></span> <span data-ttu-id="91623-105">In Media Foundation werden Medientypen durch die [**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="91623-105">In Media Foundation, media types are represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="91623-106">Anwendungen verwenden Medientypen, um das Format einer Mediendatei oder eines Mediendaten Stroms zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="91623-106">Applications use media types to discover the format of a media file or media stream.</span></span> <span data-ttu-id="91623-107">Objekte in der Media Foundation Pipeline verwenden Medientypen, um die Formate auszuhandeln, die Sie übermitteln oder empfangen.</span><span class="sxs-lookup"><span data-stu-id="91623-107">Objects in the Media Foundation pipeline use media types to negotiate the formats they will deliver or receive.</span></span>

<span data-ttu-id="91623-108">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="91623-108">This section contains the following topics.</span></span>



| <span data-ttu-id="91623-109">Thema</span><span class="sxs-lookup"><span data-stu-id="91623-109">Topic</span></span>                                                                    | <span data-ttu-id="91623-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91623-110">Description</span></span>                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="91623-111">Informationen zu Medientypen</span><span class="sxs-lookup"><span data-stu-id="91623-111">About Media Types</span></span>](about-media-types.md)                               | <span data-ttu-id="91623-112">Allgemeine Übersicht über Medientypen in Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="91623-112">General overview of media types in Media Foundation.</span></span>                             |
| [<span data-ttu-id="91623-113">Medientyp-GUIDs</span><span class="sxs-lookup"><span data-stu-id="91623-113">Media Type GUIDs</span></span>](media-type-guids.md)                                 | <span data-ttu-id="91623-114">Listet die definierten GUIDs für die wichtigsten Typen und Untertypen auf.</span><span class="sxs-lookup"><span data-stu-id="91623-114">Lists the defined GUIDs for major types and subtypes.</span></span>                            |
| [<span data-ttu-id="91623-115">Audiomedientypen</span><span class="sxs-lookup"><span data-stu-id="91623-115">Audio Media Types</span></span>](audio-media-types.md)                               | <span data-ttu-id="91623-116">Erstellen von Medientypen für Audioformate</span><span class="sxs-lookup"><span data-stu-id="91623-116">How to create media types for audio formats.</span></span>                                     |
| [<span data-ttu-id="91623-117">Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="91623-117">Video Media Types</span></span>](video-media-types.md)                               | <span data-ttu-id="91623-118">Erstellen von Medientypen für Videoformate</span><span class="sxs-lookup"><span data-stu-id="91623-118">How to create media types for video formats.</span></span>                                     |
| [<span data-ttu-id="91623-119">Vollständige und partielle Medientypen</span><span class="sxs-lookup"><span data-stu-id="91623-119">Complete and Partial Media Types</span></span>](complete-and-partial-media-types.md) | <span data-ttu-id="91623-120">Beschreibt den Unterschied zwischen vollständigen Medientypen und partiellen Medientypen.</span><span class="sxs-lookup"><span data-stu-id="91623-120">Describes the difference between complete media types and partial media types.</span></span>   |
| [<span data-ttu-id="91623-121">Medientyp Konvertierungen</span><span class="sxs-lookup"><span data-stu-id="91623-121">Media Type Conversions</span></span>](media-type-conversions.md)                     | <span data-ttu-id="91623-122">Konvertieren zwischen Media Foundation Medientypen und älteren Format Strukturen.</span><span class="sxs-lookup"><span data-stu-id="91623-122">How to convert between Media Foundation media types and older format structures.</span></span> |
| [<span data-ttu-id="91623-123">Medientyp-Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="91623-123">Media Type Helper Functions</span></span>](media-type-helper-functions.md)           | <span data-ttu-id="91623-124">Eine Liste von Funktionen, die Informationen von einem Medientyp bearbeiten oder von diesem erhalten.</span><span class="sxs-lookup"><span data-stu-id="91623-124">A list of functions that manipulate or get information from a media type.</span></span>        |
| [<span data-ttu-id="91623-125">Medientyp-Debugcode</span><span class="sxs-lookup"><span data-stu-id="91623-125">Media Type Debugging Code</span></span>](media-type-debugging-code.md)               | <span data-ttu-id="91623-126">Beispielcode, der zeigt, wie ein Medientyp beim Debuggen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="91623-126">Example code that shows how to view a media type while debugging.</span></span>                |



 

## <a name="related-topics"></a><span data-ttu-id="91623-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="91623-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91623-128">Media Foundation primitiver</span><span class="sxs-lookup"><span data-stu-id="91623-128">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> <dt>

[<span data-ttu-id="91623-129">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="91623-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 



