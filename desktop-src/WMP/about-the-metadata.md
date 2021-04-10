---
title: Informationen zu den Metadaten
description: Informationen zu den Metadaten
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Windows-Media Player, Metadaten
- Metadaten, Informationen zu
- Metadaten, Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1c2e9782b52adc274a5b3dbaf16c48ed1a892e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309300"
---
# <a name="about-the-metadata"></a><span data-ttu-id="89567-106">Informationen zu den Metadaten</span><span class="sxs-lookup"><span data-stu-id="89567-106">About the Metadata</span></span>

<span data-ttu-id="89567-107">Windows Media Player 10 oder höher versucht, die folgenden Metadatenattribute zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="89567-107">Windows Media Player 10 or later attempts to synchronize the following metadata attributes.</span></span>



| <span data-ttu-id="89567-108">Player-Attribut</span><span class="sxs-lookup"><span data-stu-id="89567-108">Player attribute</span></span> | <span data-ttu-id="89567-109">Globale WMDM-Konstante</span><span class="sxs-lookup"><span data-stu-id="89567-109">WMDM global constant</span></span>  | <span data-ttu-id="89567-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89567-110">Description</span></span>                                                                                                 | <span data-ttu-id="89567-111">Erforderliche Version</span><span class="sxs-lookup"><span data-stu-id="89567-111">Required version</span></span>                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="89567-112">Albumartist</span><span class="sxs-lookup"><span data-stu-id="89567-112">AlbumArtist</span></span>      | <span data-ttu-id="89567-113">g \_ wszwmdmalbumartist</span><span class="sxs-lookup"><span data-stu-id="89567-113">g\_wszWMDMAlbumArtist</span></span> | <span data-ttu-id="89567-114">NULL-terminierte **Zeichenfolge** , die den Namen des primären Künstlers für das Album enthält.</span><span class="sxs-lookup"><span data-stu-id="89567-114">Null-terminated **string** containing the name of the primary artist for the album.</span></span>                         | <span data-ttu-id="89567-115">Windows Media Player 11 oder höher.</span><span class="sxs-lookup"><span data-stu-id="89567-115">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="89567-116">Aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="89567-116">Album</span></span>            | <span data-ttu-id="89567-117">g \_ wszwmdmalbumtitle</span><span class="sxs-lookup"><span data-stu-id="89567-117">g\_wszWMDMAlbumTitle</span></span>  | <span data-ttu-id="89567-118">NULL-terminierte **Zeichenfolge** , die den Titel des Albums enthält, auf dem der Inhalt ursprünglich freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="89567-118">Null-terminated **string** containing the title of the album on which the content was originally released.</span></span>  | <span data-ttu-id="89567-119">Windows Media Player 11 oder höher.</span><span class="sxs-lookup"><span data-stu-id="89567-119">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="89567-120">Autor</span><span class="sxs-lookup"><span data-stu-id="89567-120">Author</span></span>           | <span data-ttu-id="89567-121">g \_ wszwmdmauthor</span><span class="sxs-lookup"><span data-stu-id="89567-121">g\_wszWMDMAuthor</span></span>      | <span data-ttu-id="89567-122">NULL-terminierte **Zeichenfolge** mit dem Namen des Medienkünstlers oder des Actors, der dem Inhalt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="89567-122">Null-terminated **string** containing the name of the media artist or actor associated with the content.</span></span>    | <span data-ttu-id="89567-123">Windows Media Player 11 oder höher.</span><span class="sxs-lookup"><span data-stu-id="89567-123">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="89567-124">Jetzt in Kauf</span><span class="sxs-lookup"><span data-stu-id="89567-124">BuyNow</span></span>           | <span data-ttu-id="89567-125">g \_ wszwmdmbuynow</span><span class="sxs-lookup"><span data-stu-id="89567-125">g\_wszWMDMBuyNow</span></span>      | <span data-ttu-id="89567-126">**Boolescher** Wert, der angibt, ob der Benutzer den Inhalt kaufen möchte.</span><span class="sxs-lookup"><span data-stu-id="89567-126">**Boolean** indicating whether the user has chosen to purchase the content.</span></span>                                 | <span data-ttu-id="89567-127">Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="89567-127">Windows Media Player 10 or later.</span></span> |
| <span data-ttu-id="89567-128">WM/Genre</span><span class="sxs-lookup"><span data-stu-id="89567-128">WM/Genre</span></span>         | <span data-ttu-id="89567-129">g \_ wszwmdmgenre</span><span class="sxs-lookup"><span data-stu-id="89567-129">g\_wszWMDMGenre</span></span>       | <span data-ttu-id="89567-130">NULL-terminierte **Zeichenfolge** , die das Genre des Inhalts enthält.</span><span class="sxs-lookup"><span data-stu-id="89567-130">Null-terminated **string** containing the genre of the content.</span></span>                                             | <span data-ttu-id="89567-131">Windows Media Player 11 oder höher.</span><span class="sxs-lookup"><span data-stu-id="89567-131">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="89567-132">Userplaycount</span><span class="sxs-lookup"><span data-stu-id="89567-132">UserPlayCount</span></span>    | <span data-ttu-id="89567-133">g \_ wszwmdmplaycount</span><span class="sxs-lookup"><span data-stu-id="89567-133">g\_wszWMDMPlayCount</span></span>   | <span data-ttu-id="89567-134">**DWORD** , das die Häufigkeit enthält, mit der der Benutzer die digitale Mediendatei wiedergegeben hat.</span><span class="sxs-lookup"><span data-stu-id="89567-134">**DWORD** containing the number of times the user has played the digital media file.</span></span>                        | <span data-ttu-id="89567-135">Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="89567-135">Windows Media Player 10 or later.</span></span> |
| <span data-ttu-id="89567-136">ReleaseDate</span><span class="sxs-lookup"><span data-stu-id="89567-136">ReleaseDate</span></span>      | <span data-ttu-id="89567-137">g \_ wszwmdmyear</span><span class="sxs-lookup"><span data-stu-id="89567-137">g\_wszWMDMYear</span></span>        | <span data-ttu-id="89567-138">Das Datum der ursprünglichen Version des Elements.</span><span class="sxs-lookup"><span data-stu-id="89567-138">The date of the original release of the item.</span></span>                                                               | <span data-ttu-id="89567-139">Windows Media Player 11 oder höher.</span><span class="sxs-lookup"><span data-stu-id="89567-139">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="89567-140">Titel</span><span class="sxs-lookup"><span data-stu-id="89567-140">Title</span></span>            | <span data-ttu-id="89567-141">g \_ wszwmdmtitle</span><span class="sxs-lookup"><span data-stu-id="89567-141">g\_wszWMDMTitle</span></span>       | <span data-ttu-id="89567-142">Mit NULL beendete **Zeichenfolge** , die den Titel enthält.</span><span class="sxs-lookup"><span data-stu-id="89567-142">Null-terminated **string** containing the title.</span></span>                                                            | <span data-ttu-id="89567-143">Windows Media Player 11 oder höher.</span><span class="sxs-lookup"><span data-stu-id="89567-143">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="89567-144">WM/tracknumber</span><span class="sxs-lookup"><span data-stu-id="89567-144">WM/TrackNumber</span></span>   | <span data-ttu-id="89567-145">g \_ wszwmdmtrack</span><span class="sxs-lookup"><span data-stu-id="89567-145">g\_wszWMDMTrack</span></span>       | <span data-ttu-id="89567-146">**DWORD** , das die Nachverfolgung des Elements auf dem Album enthält, auf dem es ursprünglich veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="89567-146">**DWORD** containing the track number of the item on the album on which it was originally released.</span></span>         | <span data-ttu-id="89567-147">Windows Media Player 11 oder höher.</span><span class="sxs-lookup"><span data-stu-id="89567-147">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="89567-148">UserRating</span><span class="sxs-lookup"><span data-stu-id="89567-148">UserRating</span></span>       | <span data-ttu-id="89567-149">g \_ wszwmdmuserrating</span><span class="sxs-lookup"><span data-stu-id="89567-149">g\_wszWMDMUserRating</span></span>  | <span data-ttu-id="89567-150">**DWORD** mit einem Wert, der die Stern Bewertung darstellt, die der Benutzer für die digitale Mediendatei angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="89567-150">**DWORD** containing a value that represents the star rating the user specified for the digital media file.</span></span> | <span data-ttu-id="89567-151">Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="89567-151">Windows Media Player 10 or later.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="89567-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="89567-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89567-153">**Geräte Erweiterungen für die beschleunigte metadatenübertragung**</span><span class="sxs-lookup"><span data-stu-id="89567-153">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




