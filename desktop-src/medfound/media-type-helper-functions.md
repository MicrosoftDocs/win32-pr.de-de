---
description: Die folgenden Funktionen beziehen sich auf Medientyp-Objekte.
ms.assetid: 7d4f3581-8cb9-4d31-b2f7-c8fbde24cf2a
title: Medientyp-Hilfsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e5edb9748bad8ee16903eb9ff1ada50c1c043b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530530"
---
# <a name="media-type-helper-functions"></a><span data-ttu-id="45f8e-103">Medientyp-Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="45f8e-103">Media Type Helper Functions</span></span>

<span data-ttu-id="45f8e-104">Die folgenden Funktionen beziehen sich auf Medientyp-Objekte.</span><span class="sxs-lookup"><span data-stu-id="45f8e-104">The following functions pertain to media type objects.</span></span>



| <span data-ttu-id="45f8e-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="45f8e-105">Function</span></span>                                                                     | <span data-ttu-id="45f8e-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45f8e-106">Description</span></span>                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="45f8e-107">**Mfaveragetimeperframeumframerate**</span><span class="sxs-lookup"><span data-stu-id="45f8e-107">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | <span data-ttu-id="45f8e-108">Berechnet die Framerate aus der durchschnittlichen Dauer eines Video Frames.</span><span class="sxs-lookup"><span data-stu-id="45f8e-108">Calculates the frame rate from the average duration of a video frame.</span></span> |
| [<span data-ttu-id="45f8e-109">**MF calculateimagesize**</span><span class="sxs-lookup"><span data-stu-id="45f8e-109">**MFCalculateImageSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | <span data-ttu-id="45f8e-110">Ruft die Bildgröße für ein unkomprimiertes Videoformat ab.</span><span class="sxs-lookup"><span data-stu-id="45f8e-110">Retrieves the image size for an uncompressed video format.</span></span>            |
| [<span data-ttu-id="45f8e-111">**Mficomparefulltopartialmediatype**</span><span class="sxs-lookup"><span data-stu-id="45f8e-111">**MFCompareFullToPartialMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcomparefulltopartialmediatype)   | <span data-ttu-id="45f8e-112">Vergleicht einen vollständigen Medientyp mit einem partiellen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="45f8e-112">Compares a full media type to a partial media type.</span></span>                   |
| [<span data-ttu-id="45f8e-113">**MF | atemediatype**</span><span class="sxs-lookup"><span data-stu-id="45f8e-113">**MFCreateMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype)                               | <span data-ttu-id="45f8e-114">Erstellt einen leeren Medientyp.</span><span class="sxs-lookup"><span data-stu-id="45f8e-114">Creates an empty media type.</span></span>                                          |
| [<span data-ttu-id="45f8e-115">**Mfframerateesaveragetimeperframe**</span><span class="sxs-lookup"><span data-stu-id="45f8e-115">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | <span data-ttu-id="45f8e-116">Konvertiert eine Video Frame Rate in eine Frame Dauer.</span><span class="sxs-lookup"><span data-stu-id="45f8e-116">Converts a video frame rate into a frame duration.</span></span>                    |
| [<span data-ttu-id="45f8e-117">**Mfgetstrideforbitmapinfoheader**</span><span class="sxs-lookup"><span data-stu-id="45f8e-117">**MFGetStrideForBitmapInfoHeader**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | <span data-ttu-id="45f8e-118">Ruft den minimalen Oberflächen Schritt für ein Videoformat ab.</span><span class="sxs-lookup"><span data-stu-id="45f8e-118">Retrieves the minimum surface stride for a video format.</span></span>              |
| [<span data-ttu-id="45f8e-119">**Mfisformatyuv**</span><span class="sxs-lookup"><span data-stu-id="45f8e-119">**MFIsFormatYUV**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | <span data-ttu-id="45f8e-120">Fragt ab, ob ein FourCC-Code oder **D3DFORMAT** -Wert ein YUV-Format ist.</span><span class="sxs-lookup"><span data-stu-id="45f8e-120">Queries whether a FOURCC code or **D3DFORMAT** value is a YUV format.</span></span> |
| [<span data-ttu-id="45f8e-121">**MF validatemediatypesize**</span><span class="sxs-lookup"><span data-stu-id="45f8e-121">**MFValidateMediaTypeSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfvalidatemediatypesize)                   | <span data-ttu-id="45f8e-122">Überprüft die Größe eines Puffers für einen Videoformat Block.</span><span class="sxs-lookup"><span data-stu-id="45f8e-122">Validates the size of a buffer for a video format block.</span></span>              |
| [<span data-ttu-id="45f8e-123">**MF wrapmediatype**</span><span class="sxs-lookup"><span data-stu-id="45f8e-123">**MFWrapMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype)                                   | <span data-ttu-id="45f8e-124">Erstellt einen Medientyp, der einen anderen Medientyp umschließt.</span><span class="sxs-lookup"><span data-stu-id="45f8e-124">Creates a media type that wraps another media type.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="45f8e-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="45f8e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45f8e-126">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="45f8e-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="45f8e-127">Medientyp Konvertierungen</span><span class="sxs-lookup"><span data-stu-id="45f8e-127">Media Type Conversions</span></span>](media-type-conversions.md)
</dt> <dt>

[<span data-ttu-id="45f8e-128">Medientypen</span><span class="sxs-lookup"><span data-stu-id="45f8e-128">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



