---
description: Wichtige Medientypen
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Wichtige Medientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a93a1aa430a720ff4b2f3591071d0bc8b178d6a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961190"
---
# <a name="major-media-types"></a><span data-ttu-id="f613f-103">Wichtige Medientypen</span><span class="sxs-lookup"><span data-stu-id="f613f-103">Major Media Types</span></span>

<span data-ttu-id="f613f-104">In einem Medientyp beschreibt der *Haupttyp* die Gesamtkategorie der Daten, z. b. Audiodaten oder Videos.</span><span class="sxs-lookup"><span data-stu-id="f613f-104">In a media type, the *major type* describes the overall category of the data, such as audio or video.</span></span> <span data-ttu-id="f613f-105">Wenn der *Untertyp* vorhanden ist, wird der Haupttyp weiter verfeinert.</span><span class="sxs-lookup"><span data-stu-id="f613f-105">The *subtype*, if present, further refines the major type.</span></span> <span data-ttu-id="f613f-106">Wenn der Haupttyp z. b. "Video" ist, kann der Untertyp "32-Bit RGB Video" lauten.</span><span class="sxs-lookup"><span data-stu-id="f613f-106">For example, if the major type is video, the subtype might be 32-bit RGB video.</span></span> <span data-ttu-id="f613f-107">Untertypen unterscheiden auch codierte Formate, wie z. b. H. 264-Video, von nicht komprimierten Formaten.</span><span class="sxs-lookup"><span data-stu-id="f613f-107">Subtypes also distinguish encoded formats, such as H.264 video, from uncompressed formats.</span></span>

<span data-ttu-id="f613f-108">Der Haupttyp und der Untertyp werden von GUIDs identifiziert und in den folgenden Attributen gespeichert:</span><span class="sxs-lookup"><span data-stu-id="f613f-108">Major type and subtype are identified by GUIDs and stored in the following attributes:</span></span>



| <span data-ttu-id="f613f-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="f613f-109">Attribute</span></span>                                             | <span data-ttu-id="f613f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f613f-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| [<span data-ttu-id="f613f-111">Haupt-Typ des MF- \_ MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="f613f-111">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="f613f-112">Der Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="f613f-112">Major type.</span></span> |
| [<span data-ttu-id="f613f-113">MF- \_ MT- \_ Untertyp</span><span class="sxs-lookup"><span data-stu-id="f613f-113">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="f613f-114">Untertyp.</span><span class="sxs-lookup"><span data-stu-id="f613f-114">Subtype.</span></span>    |



 

<span data-ttu-id="f613f-115">Die folgenden Haupttypen sind definiert.</span><span class="sxs-lookup"><span data-stu-id="f613f-115">The following major types are defined.</span></span>



| <span data-ttu-id="f613f-116">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="f613f-116">Major Type</span></span>                    | <span data-ttu-id="f613f-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f613f-117">Description</span></span>                                                                                                                                                | <span data-ttu-id="f613f-118">Untertypen</span><span class="sxs-lookup"><span data-stu-id="f613f-118">Subtypes</span></span>                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f613f-119">**MF MediaType \_ -Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="f613f-119">**MFMediaType\_Audio**</span></span>        | <span data-ttu-id="f613f-120">Audio.</span><span class="sxs-lookup"><span data-stu-id="f613f-120">Audio.</span></span>                                                                                                                                                     | <span data-ttu-id="f613f-121">[Audiountertyp-GUIDs](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="f613f-121">[Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>      |
| <span data-ttu-id="f613f-122">**MF MediaType- \_ Binärdatei**</span><span class="sxs-lookup"><span data-stu-id="f613f-122">**MFMediaType\_Binary**</span></span>       | <span data-ttu-id="f613f-123">Binärer Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="f613f-123">Binary stream.</span></span>                                                                                                                                             | <span data-ttu-id="f613f-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="f613f-124">None.</span></span>                                                |
| <span data-ttu-id="f613f-125">**MF MediaType- \_ Filetransfer**</span><span class="sxs-lookup"><span data-stu-id="f613f-125">**MFMediaType\_FileTransfer**</span></span> | <span data-ttu-id="f613f-126">Ein Datenstrom, der Datendateien enthält.</span><span class="sxs-lookup"><span data-stu-id="f613f-126">A stream that contains data files.</span></span>                                                                                                                         | <span data-ttu-id="f613f-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="f613f-127">None.</span></span>                                                |
| <span data-ttu-id="f613f-128">**MF MediaType- \_ HTML**</span><span class="sxs-lookup"><span data-stu-id="f613f-128">**MFMediaType\_HTML**</span></span>         | <span data-ttu-id="f613f-129">HTML-Stream.</span><span class="sxs-lookup"><span data-stu-id="f613f-129">HTML stream.</span></span>                                                                                                                                               | <span data-ttu-id="f613f-130">Keine.</span><span class="sxs-lookup"><span data-stu-id="f613f-130">None.</span></span>                                                |
| <span data-ttu-id="f613f-131">**MF MediaType- \_ Image**</span><span class="sxs-lookup"><span data-stu-id="f613f-131">**MFMediaType\_Image**</span></span>        | <span data-ttu-id="f613f-132">Image Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="f613f-132">Still image stream.</span></span>                                                                                                                                        | <span data-ttu-id="f613f-133">[WIC-GUIDs und CLSIDs](../wic/-wic-guids-clsids.md).</span><span class="sxs-lookup"><span data-stu-id="f613f-133">[WIC GUIDs and CLSIDs](../wic/-wic-guids-clsids.md).</span></span>       |
| <span data-ttu-id="f613f-134">**MF MediaType \_ geschützt**</span><span class="sxs-lookup"><span data-stu-id="f613f-134">**MFMediaType\_Protected**</span></span>    | <span data-ttu-id="f613f-135">Geschützte Medien.</span><span class="sxs-lookup"><span data-stu-id="f613f-135">Protected media.</span></span>                                                                                                                                           | <span data-ttu-id="f613f-136">Der Untertyp gibt das Inhalts Schutzschema an.</span><span class="sxs-lookup"><span data-stu-id="f613f-136">The subtype specifies the content protection scheme.</span></span> |
| <span data-ttu-id="f613f-137">**MF MediaType- \_ Wahrnehmung**</span><span class="sxs-lookup"><span data-stu-id="f613f-137">**MFMediaType\_Perception**</span></span>   | <span data-ttu-id="f613f-138">Datenströme von einem Kamerasensor oder einer Verarbeitungseinheit, die auf unformatierte Videodaten und das Verständnis der Umgebung oder der Menschen in der IT-Abteilung verzichten.</span><span class="sxs-lookup"><span data-stu-id="f613f-138">Streams from a camera sensor or processing unit that reasons and understands raw video data and provides understanding of the environment or humans in it.</span></span> | <span data-ttu-id="f613f-139">Keine.</span><span class="sxs-lookup"><span data-stu-id="f613f-139">None.</span></span>                                                |
| <span data-ttu-id="f613f-140">**MF MediaType \_ Sami**</span><span class="sxs-lookup"><span data-stu-id="f613f-140">**MFMediaType\_SAMI**</span></span>         | <span data-ttu-id="f613f-141">Synchronisierte, barrierefreie Medienaustausch Beschriftungen (Sami).</span><span class="sxs-lookup"><span data-stu-id="f613f-141">Synchronized Accessible Media Interchange (SAMI) captions.</span></span>                                                                                                 | <span data-ttu-id="f613f-142">Keine.</span><span class="sxs-lookup"><span data-stu-id="f613f-142">None.</span></span>                                                |
| <span data-ttu-id="f613f-143">**MF MediaType- \_ Skript**</span><span class="sxs-lookup"><span data-stu-id="f613f-143">**MFMediaType\_Script**</span></span>       | <span data-ttu-id="f613f-144">Skript Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="f613f-144">Script stream.</span></span>                                                                                                                                             | <span data-ttu-id="f613f-145">Keine.</span><span class="sxs-lookup"><span data-stu-id="f613f-145">None.</span></span>                                                |
| <span data-ttu-id="f613f-146">**MF MediaType-Daten \_ Strom**</span><span class="sxs-lookup"><span data-stu-id="f613f-146">**MFMediaType\_Stream**</span></span>       | <span data-ttu-id="f613f-147">Multiplexed-Stream oder elementare Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="f613f-147">Multiplexed stream or elementary stream.</span></span>                                                                                                                   | [<span data-ttu-id="f613f-148">Stream-Untertyp-GUIDs</span><span class="sxs-lookup"><span data-stu-id="f613f-148">Stream Subtype GUIDs</span></span>](stream-subtype-guids.md)     |
| <span data-ttu-id="f613f-149">**MF MediaType- \_ Video**</span><span class="sxs-lookup"><span data-stu-id="f613f-149">**MFMediaType\_Video**</span></span>        | <span data-ttu-id="f613f-150">Video.</span><span class="sxs-lookup"><span data-stu-id="f613f-150">Video.</span></span>                                                                                                                                                     | <span data-ttu-id="f613f-151">[Video Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="f613f-151">[Video Subtype GUIDs](video-subtype-guids.md).</span></span>      |



 

<span data-ttu-id="f613f-152">Komponenten von Drittanbietern können neue Haupttypen und neue Untertypen definieren.</span><span class="sxs-lookup"><span data-stu-id="f613f-152">Third-party components can define new major types and new subtypes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f613f-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f613f-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f613f-154">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="f613f-154">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="f613f-155">Medientypen</span><span class="sxs-lookup"><span data-stu-id="f613f-155">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
