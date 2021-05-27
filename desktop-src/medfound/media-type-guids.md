---
description: Hauptmedientypen
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Hauptmedientypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56553ac635f0e767e43e057b2a468027dcefb730
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549575"
---
# <a name="major-media-types"></a><span data-ttu-id="7c7e7-103">Hauptmedientypen</span><span class="sxs-lookup"><span data-stu-id="7c7e7-103">Major Media Types</span></span>

<span data-ttu-id="7c7e7-104">In einem Medientyp beschreibt der *Haupttyp* die Gesamtkategorie der Daten, z. B. Audio oder Video.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-104">In a media type, the *major type* describes the overall category of the data, such as audio or video.</span></span> <span data-ttu-id="7c7e7-105">Der *Untertyp*, sofern vorhanden, verfeinern den Haupttyp weiter.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-105">The *subtype*, if present, further refines the major type.</span></span> <span data-ttu-id="7c7e7-106">Wenn der Haupttyp beispielsweise video ist, kann der Untertyp 32-Bit-RGB-Video sein.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-106">For example, if the major type is video, the subtype might be 32-bit RGB video.</span></span> <span data-ttu-id="7c7e7-107">Untertypen unterscheiden auch codierte Formate, z.B. H.264-Video, von nicht komprimierten Formaten.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-107">Subtypes also distinguish encoded formats, such as H.264 video, from uncompressed formats.</span></span>

<span data-ttu-id="7c7e7-108">Haupttyp und Untertyp werden durch GUIDs identifiziert und in den folgenden Attributen gespeichert:</span><span class="sxs-lookup"><span data-stu-id="7c7e7-108">Major type and subtype are identified by GUIDs and stored in the following attributes:</span></span>



| <span data-ttu-id="7c7e7-109">attribute</span><span class="sxs-lookup"><span data-stu-id="7c7e7-109">Attribute</span></span>                                             | <span data-ttu-id="7c7e7-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c7e7-110">Description</span></span> |
|-------------------------------------------------------|-------------|
| [<span data-ttu-id="7c7e7-111">MF \_ \_ MT-HAUPTTYP \_</span><span class="sxs-lookup"><span data-stu-id="7c7e7-111">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="7c7e7-112">Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-112">Major type.</span></span> |
| [<span data-ttu-id="7c7e7-113">MF \_ \_ MT-UNTERTYP</span><span class="sxs-lookup"><span data-stu-id="7c7e7-113">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="7c7e7-114">Untertyp.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-114">Subtype.</span></span>    |



 

<span data-ttu-id="7c7e7-115">Die folgenden Haupttypen sind definiert.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-115">The following major types are defined.</span></span>



| <span data-ttu-id="7c7e7-116">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="7c7e7-116">Major Type</span></span>                    | <span data-ttu-id="7c7e7-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c7e7-117">Description</span></span>                                                                                                                                                | <span data-ttu-id="7c7e7-118">Untertypen</span><span class="sxs-lookup"><span data-stu-id="7c7e7-118">Subtypes</span></span>                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7c7e7-119">**MFMediaType \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="7c7e7-119">**MFMediaType\_Audio**</span></span>        | <span data-ttu-id="7c7e7-120">Audio.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-120">Audio.</span></span>                                                                                                                                                     | <span data-ttu-id="7c7e7-121">[Audiountertyp-GUIDs](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="7c7e7-121">[Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>      |
| <span data-ttu-id="7c7e7-122">**MFMediaType \_ Binary**</span><span class="sxs-lookup"><span data-stu-id="7c7e7-122">**MFMediaType\_Binary**</span></span>       | <span data-ttu-id="7c7e7-123">Binärer Stream.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-123">Binary stream.</span></span>                                                                                                                                             | <span data-ttu-id="7c7e7-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-124">None.</span></span>                                                |
| <span data-ttu-id="7c7e7-125">**MFMediaType \_ FileTransfer**</span><span class="sxs-lookup"><span data-stu-id="7c7e7-125">**MFMediaType\_FileTransfer**</span></span> | <span data-ttu-id="7c7e7-126">Ein Stream, der Datendateien enthält.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-126">A stream that contains data files.</span></span>                                                                                                                         | <span data-ttu-id="7c7e7-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-127">None.</span></span>                                                |
| <span data-ttu-id="7c7e7-128">**MFMediaType \_ HTML**</span><span class="sxs-lookup"><span data-stu-id="7c7e7-128">**MFMediaType\_HTML**</span></span>         | <span data-ttu-id="7c7e7-129">HTML-Stream.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-129">HTML stream.</span></span>                                                                                                                                               | <span data-ttu-id="7c7e7-130">Keine.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-130">None.</span></span>                                                |
| <span data-ttu-id="7c7e7-131">**MFMediaType-Image \_**</span><span class="sxs-lookup"><span data-stu-id="7c7e7-131">**MFMediaType\_Image**</span></span>        | <span data-ttu-id="7c7e7-132">Noch-Bilddatenstrom.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-132">Still image stream.</span></span>                                                                                                                                        | <span data-ttu-id="7c7e7-133">[WIC-GUIDs und CLSIDs](../wic/-wic-guids-clsids.md).</span><span class="sxs-lookup"><span data-stu-id="7c7e7-133">[WIC GUIDs and CLSIDs](../wic/-wic-guids-clsids.md).</span></span>       |
| <span data-ttu-id="7c7e7-134">**MFMediaType-Metadaten \_**</span><span class="sxs-lookup"><span data-stu-id="7c7e7-134">**MFMediaType\_Metadata**</span></span>        | <span data-ttu-id="7c7e7-135">Metadatenstream.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-135">Metadata stream.</span></span>                                                                                                                                        | <span data-ttu-id="7c7e7-136">Keine.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-136">None.</span></span>       |
| <span data-ttu-id="7c7e7-137">**MFMediaType \_ Protected**</span><span class="sxs-lookup"><span data-stu-id="7c7e7-137">**MFMediaType\_Protected**</span></span>    | <span data-ttu-id="7c7e7-138">Geschützte Medien.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-138">Protected media.</span></span>                                                                                                                                           | <span data-ttu-id="7c7e7-139">Der Untertyp gibt das Inhaltsschutzschema an.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-139">The subtype specifies the content protection scheme.</span></span> |
| <span data-ttu-id="7c7e7-140">**MFMediaType \_ Perception**</span><span class="sxs-lookup"><span data-stu-id="7c7e7-140">**MFMediaType\_Perception**</span></span>   | <span data-ttu-id="7c7e7-141">Datenströme von einem Kamerasensor oder einer Verarbeitungseinheit, die unformatiert Videodaten auslösen und verstehen und ein Verständnis der Umgebung oder der Menschen in ihr bieten.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-141">Streams from a camera sensor or processing unit that reasons and understands raw video data and provides understanding of the environment or humans in it.</span></span> | <span data-ttu-id="7c7e7-142">Keine.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-142">None.</span></span>                                                |
| <span data-ttu-id="7c7e7-143">**MFMediaType \_ SAMI**</span><span class="sxs-lookup"><span data-stu-id="7c7e7-143">**MFMediaType\_SAMI**</span></span>         | <span data-ttu-id="7c7e7-144">Synchronisierte SAMI-Untertitel (Accessible Media Interchange).</span><span class="sxs-lookup"><span data-stu-id="7c7e7-144">Synchronized Accessible Media Interchange (SAMI) captions.</span></span>                                                                                                 | <span data-ttu-id="7c7e7-145">Keine.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-145">None.</span></span>                                                |
| <span data-ttu-id="7c7e7-146">**MFMediaType-Skript \_**</span><span class="sxs-lookup"><span data-stu-id="7c7e7-146">**MFMediaType\_Script**</span></span>       | <span data-ttu-id="7c7e7-147">Skriptstream.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-147">Script stream.</span></span>                                                                                                                                             | <span data-ttu-id="7c7e7-148">Keine.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-148">None.</span></span>                                                |
| <span data-ttu-id="7c7e7-149">**MFMediaType-Stream \_**</span><span class="sxs-lookup"><span data-stu-id="7c7e7-149">**MFMediaType\_Stream**</span></span>       | <span data-ttu-id="7c7e7-150">Multiplexstream oder elementarer Stream.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-150">Multiplexed stream or elementary stream.</span></span>                                                                                                                   | [<span data-ttu-id="7c7e7-151">GuiDs des Streamuntertyps</span><span class="sxs-lookup"><span data-stu-id="7c7e7-151">Stream Subtype GUIDs</span></span>](stream-subtype-guids.md)     |
| <span data-ttu-id="7c7e7-152">**\_MFMediaType-Video**</span><span class="sxs-lookup"><span data-stu-id="7c7e7-152">**MFMediaType\_Video**</span></span>        | <span data-ttu-id="7c7e7-153">Video.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-153">Video.</span></span>                                                                                                                                                     | <span data-ttu-id="7c7e7-154">[Video-Untertyp-GUIDs](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="7c7e7-154">[Video Subtype GUIDs](video-subtype-guids.md).</span></span>      |



 

<span data-ttu-id="7c7e7-155">Komponenten von Drittanbietern können neue Haupttypen und neue Untertypen definieren.</span><span class="sxs-lookup"><span data-stu-id="7c7e7-155">Third-party components can define new major types and new subtypes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c7e7-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7c7e7-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c7e7-157">**ARCHEMEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="7c7e7-157">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="7c7e7-158">Medientypen</span><span class="sxs-lookup"><span data-stu-id="7c7e7-158">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
