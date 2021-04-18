---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Windows Media Player Online Stores artist.csv
- Online Stores, artist.csv
- Geben Sie 1 Online Stores, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f548c419f01d23b76172c44cd6e50263c4e9197
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311351"
---
# <a name="artistcsv"></a><span data-ttu-id="03275-107">artist.csv</span><span class="sxs-lookup"><span data-stu-id="03275-107">artist.csv</span></span>

<span data-ttu-id="03275-108">Diese Datei enthält einen Eintrag für jeden Künstler im Katalog.</span><span class="sxs-lookup"><span data-stu-id="03275-108">This file contains an entry for each artist in the catalog.</span></span> <span data-ttu-id="03275-109">Jeder Eintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="03275-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="03275-110">Felder müssen in der aufgeführten Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="03275-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="03275-111">Alle Felder in artist.csv sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="03275-111">All fields in artist.csv are required.</span></span>

<span data-ttu-id="03275-112">In der Spalte Format in der folgenden Tabelle wird beschrieben, wie jedes Unicode-Textfeld formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="03275-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="03275-113">Er verweist nicht auf den Datentyp des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="03275-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="03275-114">Wenn beispielsweise eine ganze Zahl in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen Ganzzahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="03275-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="03275-115">Feld</span><span class="sxs-lookup"><span data-stu-id="03275-115">Field</span></span>                  | <span data-ttu-id="03275-116">Format</span><span class="sxs-lookup"><span data-stu-id="03275-116">Format</span></span>                                            | <span data-ttu-id="03275-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03275-117">Description</span></span>                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03275-118">ArtistId</span><span class="sxs-lookup"><span data-stu-id="03275-118">ArtistID</span></span>               | <span data-ttu-id="03275-119">Nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="03275-119">Non-negative integer.</span></span> <span data-ttu-id="03275-120">Beispiel: 65832</span><span class="sxs-lookup"><span data-stu-id="03275-120">Example: 65832</span></span>              | <span data-ttu-id="03275-121">Eindeutiger Bezeichner für den in artist.csv eindeutigen Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="03275-121">Unique identifier for the artist, unique within artist.csv.</span></span> <span data-ttu-id="03275-122">Muss kleiner als 2 ^ 32 sein.</span><span class="sxs-lookup"><span data-stu-id="03275-122">Must be less than 2^32.</span></span>                        |
| <span data-ttu-id="03275-123">ArtistName</span><span class="sxs-lookup"><span data-stu-id="03275-123">ArtistName</span></span>             | <span data-ttu-id="03275-124">Unicode-Zeichenfolge. Beispiel: Don Funk</span><span class="sxs-lookup"><span data-stu-id="03275-124">Unicode string.Example: Don Funk</span></span><br/>       | <span data-ttu-id="03275-125">Anzeige Name für den Künstler.</span><span class="sxs-lookup"><span data-stu-id="03275-125">Display name for the artist.</span></span>                                                                               |
| <span data-ttu-id="03275-126">Linkedgenreid</span><span class="sxs-lookup"><span data-stu-id="03275-126">LinkedGenreID</span></span>          | <span data-ttu-id="03275-127">Nicht negative ganze Zahl. Beispiel: 313</span><span class="sxs-lookup"><span data-stu-id="03275-127">Non-negative integer.Example: 313</span></span><br/>      | <span data-ttu-id="03275-128">GenreID des primären Genres des Künstlers.</span><span class="sxs-lookup"><span data-stu-id="03275-128">GenreID of the artist's primary genre.</span></span> <span data-ttu-id="03275-129">Muss ein Haupt Genre und kein unter Genre sein.</span><span class="sxs-lookup"><span data-stu-id="03275-129">Must be a main genre and not a subgenre.</span></span> <span data-ttu-id="03275-130">Es ist nur ein Wert zulässig.</span><span class="sxs-lookup"><span data-stu-id="03275-130">Only one value is allowed.</span></span> |
| <span data-ttu-id="03275-131">Linkedsimilarartistids</span><span class="sxs-lookup"><span data-stu-id="03275-131">LinkedSimilarArtistIDs</span></span> | <span data-ttu-id="03275-132">–</span><span class="sxs-lookup"><span data-stu-id="03275-132">N/A</span></span>                                               | <span data-ttu-id="03275-133">Wird in dieser Version nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="03275-133">Not used in this release.</span></span> <span data-ttu-id="03275-134">Muss leer sein.</span><span class="sxs-lookup"><span data-stu-id="03275-134">Should be empty.</span></span>                                                                 |
| <span data-ttu-id="03275-135">Beliebtheit</span><span class="sxs-lookup"><span data-stu-id="03275-135">Popularity</span></span>             | <span data-ttu-id="03275-136">Kann ein ganzzahliger Wert oder ein Dezimalwert sein.</span><span class="sxs-lookup"><span data-stu-id="03275-136">Can be integer or decimal value.</span></span> <span data-ttu-id="03275-137">Beispiel: 1252,25</span><span class="sxs-lookup"><span data-stu-id="03275-137">Example: 1252.25</span></span> | <span data-ttu-id="03275-138">Rangfolgenbewertung.</span><span class="sxs-lookup"><span data-stu-id="03275-138">Popularity ranking.</span></span> <span data-ttu-id="03275-139">Kann die Position in der Liste sein, wenn Sie nach Beliebtheit sortiert ist.</span><span class="sxs-lookup"><span data-stu-id="03275-139">Can be the position in the list when sorted by popularity.</span></span>                             |
| <span data-ttu-id="03275-140">Feedsavailable</span><span class="sxs-lookup"><span data-stu-id="03275-140">FeedsAvailable</span></span>         | <span data-ttu-id="03275-141">Boolesch.</span><span class="sxs-lookup"><span data-stu-id="03275-141">Boolean.</span></span> <span data-ttu-id="03275-142">Format: \[ 0 \| 1 \] Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="03275-142">Format: \[0\|1\]Example: 0</span></span><br/>    | <span data-ttu-id="03275-143">Wird in dieser Version nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="03275-143">Not used in this release.</span></span> <span data-ttu-id="03275-144">Muss leer sein.</span><span class="sxs-lookup"><span data-stu-id="03275-144">Should be empty.</span></span>                                                                 |



 

 

 





