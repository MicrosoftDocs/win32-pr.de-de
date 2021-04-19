---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Windows Media Player Online Stores subgenre.csv
- Online Stores, subgenre.csv
- Geben Sie 1 Online Stores, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f004eb8cecaaae64a5cc95348ac93e8a7db230
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341471"
---
# <a name="subgenrecsv"></a><span data-ttu-id="1d006-107">subgenre.csv</span><span class="sxs-lookup"><span data-stu-id="1d006-107">subgenre.csv</span></span>

<span data-ttu-id="1d006-108">Diese Datei enthält einen Eintrag für jedes unter Genre, das im Katalog dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1d006-108">This file contains an entry for each subgenre represented in the catalog.</span></span> <span data-ttu-id="1d006-109">Jeder Eintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1d006-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="1d006-110">Felder müssen in der aufgeführten Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1d006-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="1d006-111">In der Spalte Format in der folgenden Tabelle wird beschrieben, wie jedes Unicode-Textfeld formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="1d006-111">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="1d006-112">Er verweist nicht auf den Datentyp des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="1d006-112">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="1d006-113">Wenn beispielsweise eine ganze Zahl in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen Ganzzahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="1d006-113">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="1d006-114">Feld</span><span class="sxs-lookup"><span data-stu-id="1d006-114">Field</span></span>             | <span data-ttu-id="1d006-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1d006-115">Required</span></span> | <span data-ttu-id="1d006-116">Format</span><span class="sxs-lookup"><span data-stu-id="1d006-116">Format</span></span>                                                                                            | <span data-ttu-id="1d006-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d006-117">Description</span></span>                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d006-118">Subgenreid</span><span class="sxs-lookup"><span data-stu-id="1d006-118">SubGenreID</span></span>        | <span data-ttu-id="1d006-119">Ja</span><span class="sxs-lookup"><span data-stu-id="1d006-119">Yes</span></span>      | <span data-ttu-id="1d006-120">Nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="1d006-120">Non-negative integer.</span></span>                                                                             | <span data-ttu-id="1d006-121">Der in subgenre.csv eindeutige Subgenre Bezeichner (ID).</span><span class="sxs-lookup"><span data-stu-id="1d006-121">Subgenre identifier (ID), unique within subgenre.csv.</span></span> <span data-ttu-id="1d006-122">Bis zu 1024 Subgenres sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="1d006-122">Up to 1024 subgenres are allowed.</span></span>                                                                   |
| <span data-ttu-id="1d006-123">Subgenretitle</span><span class="sxs-lookup"><span data-stu-id="1d006-123">SubGenreTitle</span></span>     | <span data-ttu-id="1d006-124">Ja</span><span class="sxs-lookup"><span data-stu-id="1d006-124">Yes</span></span>      | <span data-ttu-id="1d006-125">Unicode-Zeichenfolge. Beispiel: Intelligent Dance Music (IDM)</span><span class="sxs-lookup"><span data-stu-id="1d006-125">Unicode string.Example: Intelligent Dance Music (IDM)</span></span><br/>                                  | <span data-ttu-id="1d006-126">Der Anzeige Name des Subgenres.</span><span class="sxs-lookup"><span data-stu-id="1d006-126">Subgenre display name.</span></span>                                                                                                                                    |
| <span data-ttu-id="1d006-127">Subgenreuntertitel</span><span class="sxs-lookup"><span data-stu-id="1d006-127">SubGenreSubtitle</span></span>  | <span data-ttu-id="1d006-128">Nein</span><span class="sxs-lookup"><span data-stu-id="1d006-128">No</span></span>       | <span data-ttu-id="1d006-129">Unicode-Zeichenfolge. Beispiel: neue, perkussive Elektronische Musik, die nicht ganz rein Techno ist.</span><span class="sxs-lookup"><span data-stu-id="1d006-129">Unicode string.Example: New, percussive electronic music that's not quite pure techno.</span></span><br/> | <span data-ttu-id="1d006-130">Beschreibt die Bedeutung des Anzeige namens des unter Genres.</span><span class="sxs-lookup"><span data-stu-id="1d006-130">Describe the meaning of the subgenre display name.</span></span> <span data-ttu-id="1d006-131">Sollte kleiner als 64 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="1d006-131">Should be less than 64 characters.</span></span>                                                                     |
| <span data-ttu-id="1d006-132">Feedsareavailable</span><span class="sxs-lookup"><span data-stu-id="1d006-132">FeedsAreAvailable</span></span> | <span data-ttu-id="1d006-133">Ja</span><span class="sxs-lookup"><span data-stu-id="1d006-133">Yes</span></span>      | <span data-ttu-id="1d006-134">Boolescher Wert. Format: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="1d006-134">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="1d006-135">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="1d006-135">Example: 0</span></span><br/>                                         | <span data-ttu-id="1d006-136">Gibt an, ob "Radio Play" durch springen zu einem Feed möglich ist.</span><span class="sxs-lookup"><span data-stu-id="1d006-136">Indicates whether "radio play" is possible by jumping to a feed.</span></span>                                                                                          |
| <span data-ttu-id="1d006-137">Verknüpfte \_ GenreID</span><span class="sxs-lookup"><span data-stu-id="1d006-137">Linked\_GenreID</span></span>   | <span data-ttu-id="1d006-138">Ja</span><span class="sxs-lookup"><span data-stu-id="1d006-138">Yes</span></span>      | <span data-ttu-id="1d006-139">Nicht negative Ganzzahl (GenreID). Beispiel: 12</span><span class="sxs-lookup"><span data-stu-id="1d006-139">Non-negative integer (GenreID).Example: 12</span></span><br/>                                             | <span data-ttu-id="1d006-140">Der GenreID des übergeordneten Genres.</span><span class="sxs-lookup"><span data-stu-id="1d006-140">The GenreID of the parent genre.</span></span> <span data-ttu-id="1d006-141">Es ist nur ein übergeordnetes Element zulässig.</span><span class="sxs-lookup"><span data-stu-id="1d006-141">Only one parent is allowed.</span></span>                                                                                              |
| <span data-ttu-id="1d006-142">Sorrenderrank</span><span class="sxs-lookup"><span data-stu-id="1d006-142">SortOrderRank</span></span>     | <span data-ttu-id="1d006-143">Ja</span><span class="sxs-lookup"><span data-stu-id="1d006-143">Yes</span></span>      | <span data-ttu-id="1d006-144">Nicht negative ganze Zahl. Beispiel: 23</span><span class="sxs-lookup"><span data-stu-id="1d006-144">Non-negative integer.Example: 23</span></span><br/>                                                       | <span data-ttu-id="1d006-145">Eine Rangfolge, die im Idealfall eindeutig ist, wird zum Sortieren von unter Genres in der Benutzeroberfläche verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d006-145">A ranking, ideally unique, used for sorting subgenres in the user interface.</span></span> <span data-ttu-id="1d006-146">Wenn das übergeordnete Genre 10 unter Genres hat, kann dies eine ganze Zahl zwischen 1 und 10 sein.</span><span class="sxs-lookup"><span data-stu-id="1d006-146">If the parent genre has 10 subgenres, this might be an integer from 1 to 10.</span></span> |



 

 

 





