---
title: Medientypen für das Windows Media-Format-SDK
description: Erfahren Sie mehr über Medientypen, die vom SDK für den Windows Media-Format verwendet werden können. Medientypen sind GUID-Werte, die Konstanten im SDK zugewiesen werden.
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows Media-Format-SDK, Medientypen
- Advanced Systems Format (ASF), Medientypen
- ASF (Advanced Systems Format), Medientypen
- Medientypen, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6d15255ab311c67562a6c9dde83650240b0803
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106370975"
---
# <a name="media-types-for-windows-media-format-sdk"></a><span data-ttu-id="e843f-108">Medientypen für das Windows Media-Format-SDK</span><span class="sxs-lookup"><span data-stu-id="e843f-108">Media Types for Windows Media Format SDK</span></span>

<span data-ttu-id="e843f-109">Mit Medientypen werden die unterschiedlichen Medientypen identifiziert, die vom SDK für den Windows Media-Format verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e843f-109">Media types identify the different types of media that can be used by the Windows Media Format SDK.</span></span> <span data-ttu-id="e843f-110">Alle Medientypen sind GUID-Werte, die Konstanten im SDK zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="e843f-110">All media types are GUID values that have been assigned to constants in the SDK.</span></span> <span data-ttu-id="e843f-111">Die GUID-Werte, die von den in diesem Abschnitt aufgeführten Konstanten dargestellt werden, sind im Abschnitt [Medientyp](media-type-identifiers.md) -IDs dieses Verweises aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e843f-111">The GUID values represented by the constants listed in this section are listed in the [Media Type Identifiers](media-type-identifiers.md) section of this reference.</span></span>

<span data-ttu-id="e843f-112">In der folgenden Tabelle sind die wichtigsten Medientypen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e843f-112">The following table lists major media types.</span></span> <span data-ttu-id="e843f-113">Diese Konstanten definieren die allgemeine Klassifizierung digitaler Medien, die vom SDK für den Windows Media-Format unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e843f-113">These constants define the high level classification of digital media supported by the Windows Media Format SDK.</span></span>



| <span data-ttu-id="e843f-114">Haupttyp</span><span class="sxs-lookup"><span data-stu-id="e843f-114">Major type</span></span>                | <span data-ttu-id="e843f-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e843f-115">Description</span></span>                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e843f-116">Wmmediatype- \_ Video</span><span class="sxs-lookup"><span data-stu-id="e843f-116">WMMEDIATYPE\_Video</span></span>        | <span data-ttu-id="e843f-117">Ein Videostream.</span><span class="sxs-lookup"><span data-stu-id="e843f-117">A video stream.</span></span>                                                                                         |
| <span data-ttu-id="e843f-118">Wmmediatype \_ -Audiodatei</span><span class="sxs-lookup"><span data-stu-id="e843f-118">WMMEDIATYPE\_Audio</span></span>        | <span data-ttu-id="e843f-119">Ein Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="e843f-119">An audio stream.</span></span>                                                                                        |
| <span data-ttu-id="e843f-120">Wmmediatype- \_ Skript</span><span class="sxs-lookup"><span data-stu-id="e843f-120">WMMEDIATYPE\_Script</span></span>       | <span data-ttu-id="e843f-121">Ein Skript Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="e843f-121">A script stream.</span></span>                                                                                        |
| <span data-ttu-id="e843f-122">Wmmediatype- \_ Filetransfer</span><span class="sxs-lookup"><span data-stu-id="e843f-122">WMMEDIATYPE\_FileTransfer</span></span> | <span data-ttu-id="e843f-123">Ein Datenstrom, der Datendateien enthält.</span><span class="sxs-lookup"><span data-stu-id="e843f-123">A stream that contains data files.</span></span> <span data-ttu-id="e843f-124">Webstreams, die aus HTML-Dateien bestehen, haben ebenfalls diesen Haupttyp.</span><span class="sxs-lookup"><span data-stu-id="e843f-124">Web streams, which consist of HTML files, also have this major type.</span></span> |
| <span data-ttu-id="e843f-125">Wmmediatype- \_ Image</span><span class="sxs-lookup"><span data-stu-id="e843f-125">WMMEDIATYPE\_Image</span></span>        | <span data-ttu-id="e843f-126">Ein JPEG-Bildstream für eine dargestellte Audiodatei (wie in einer Folien Anzeige).</span><span class="sxs-lookup"><span data-stu-id="e843f-126">A JPEG image stream for an illustrated audio file (as in a slide show).</span></span>                                 |
| <span data-ttu-id="e843f-127">Wmmediatype- \_ Text</span><span class="sxs-lookup"><span data-stu-id="e843f-127">WMMEDIATYPE\_Text</span></span>         | <span data-ttu-id="e843f-128">Ein Textstream.</span><span class="sxs-lookup"><span data-stu-id="e843f-128">A text stream.</span></span>                                                                                          |



 

<span data-ttu-id="e843f-129">Zusätzlich zu den explizit unterstützten Hauptmedien Typen können Sie auch eigene beliebige Datentypen erstellen.</span><span class="sxs-lookup"><span data-stu-id="e843f-129">In addition to the explicitly supported major media types, you can create your own arbitrary data types.</span></span> <span data-ttu-id="e843f-130">Für benutzerdefinierte beliebige Datentypen müssen Sie sicherstellen, dass die von Ihnen verwendete GUID nicht mit einem vorhandenen Haupttyp identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e843f-130">For custom arbitrary data types, you must ensure that the GUID you use does not match an existing major type.</span></span>

<span data-ttu-id="e843f-131">Ein Mediendaten Strom weist neben seinem Haupttyp häufig einen Untertyp auf.</span><span class="sxs-lookup"><span data-stu-id="e843f-131">A media stream will often have a subtype in addition to its major type.</span></span> <span data-ttu-id="e843f-132">In den folgenden Abschnitten sind die Untertypen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e843f-132">The following sections list the supported subtypes.</span></span>



| <span data-ttu-id="e843f-133">`Section`</span><span class="sxs-lookup"><span data-stu-id="e843f-133">Section</span></span>                                                        | <span data-ttu-id="e843f-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e843f-134">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e843f-135">Nicht komprimierte Medien Untertypen</span><span class="sxs-lookup"><span data-stu-id="e843f-135">Uncompressed Media Subtypes</span></span>](uncompressed-media-subtypes.md) | <span data-ttu-id="e843f-136">Beschreibt die Untertypen, die für nicht komprimierte Medien verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e843f-136">Describes the subtypes available for uncompressed media.</span></span> <span data-ttu-id="e843f-137">Dabei handelt es sich um Typen, die normalerweise mit Eingabe-oder Ausgabemedien verknüpft sind</span><span class="sxs-lookup"><span data-stu-id="e843f-137">These are the types typically associated with input or output media.</span></span>              |
| [<span data-ttu-id="e843f-138">Komprimierte Medien Untertypen</span><span class="sxs-lookup"><span data-stu-id="e843f-138">Compressed Media Subtypes</span></span>](compressed-media-subtypes.md)     | <span data-ttu-id="e843f-139">Beschreibt die Untertypen, die für komprimierte Medien verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="e843f-139">Describes the subtypes available for compressed media.</span></span> <span data-ttu-id="e843f-140">Dabei handelt es sich um die Typen, die normalerweise Medien in einem Stream innerhalb einer ASF-Datei zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e843f-140">These are the types typically associated with media in a stream within an ASF file.</span></span> |
| [<span data-ttu-id="e843f-141">Video Eingabeformate</span><span class="sxs-lookup"><span data-stu-id="e843f-141">Video Input Formats</span></span>](video-input-formats.md)                 | <span data-ttu-id="e843f-142">Listet die Videoformate auf, die als Eingaben für den Windows Media Video 9-Codec akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="e843f-142">Lists the video formats accepted as inputs for the Windows Media Video 9 codec.</span></span>                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="e843f-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e843f-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e843f-144">**Medientyp-IDs**</span><span class="sxs-lookup"><span data-stu-id="e843f-144">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="e843f-145">**Programmierverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="e843f-145">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




