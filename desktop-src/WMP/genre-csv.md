---
title: genre.csv
description: genre.csv
ms.assetid: e05517f4-a69b-4db7-943d-3490253b92f3
keywords:
- Windows Media Player Online Stores genre.csv
- Online Stores, genre.csv
- Geben Sie 1 Online Stores, genre.csv
- genre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a077cadccc0b2da318e60ca2e0636d96319e5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947926"
---
# <a name="genrecsv"></a><span data-ttu-id="10175-107">genre.csv</span><span class="sxs-lookup"><span data-stu-id="10175-107">genre.csv</span></span>

<span data-ttu-id="10175-108">Diese Datei enthält einen Eintrag für jedes Genre, das im Katalog dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="10175-108">This file contains an entry for each genre represented in the catalog.</span></span> <span data-ttu-id="10175-109">Jeder Eintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="10175-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="10175-110">Felder müssen in der aufgeführten Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="10175-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="10175-111">Alle Felder in genre.csv sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="10175-111">All fields in genre.csv are required.</span></span>

<span data-ttu-id="10175-112">In der Spalte Format in der folgenden Tabelle wird beschrieben, wie jedes Unicode-Textfeld formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="10175-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="10175-113">Er verweist nicht auf den Datentyp des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="10175-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="10175-114">Wenn beispielsweise eine ganze Zahl in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen Ganzzahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="10175-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="10175-115">Feld</span><span class="sxs-lookup"><span data-stu-id="10175-115">Field</span></span>             | <span data-ttu-id="10175-116">Format</span><span class="sxs-lookup"><span data-stu-id="10175-116">Format</span></span>                                                    | <span data-ttu-id="10175-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10175-117">Description</span></span>                                                                                                                                        |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10175-118">Genre- \_ ID</span><span class="sxs-lookup"><span data-stu-id="10175-118">Genre\_ID</span></span>         | <span data-ttu-id="10175-119">Nicht negative ganze Zahl. Beispiel: 22</span><span class="sxs-lookup"><span data-stu-id="10175-119">Non-negative integer.Example: 22</span></span><br/>               | <span data-ttu-id="10175-120">Der Genre Bezeichner, der innerhalb genre.csv eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="10175-120">Genre identifier, unique within genre.csv.</span></span> <span data-ttu-id="10175-121">Muss kleiner als 2 ^ 32 sein.</span><span class="sxs-lookup"><span data-stu-id="10175-121">Must be less than 2^32.</span></span> <span data-ttu-id="10175-122">Maximal 64 Genres sind möglich.</span><span class="sxs-lookup"><span data-stu-id="10175-122">A maximum of 64 genres is possible.</span></span>                                             |
| <span data-ttu-id="10175-123">Genretitle</span><span class="sxs-lookup"><span data-stu-id="10175-123">GenreTitle</span></span>        | <span data-ttu-id="10175-124">Unicode-Zeichenfolge. Beispiel: Rock</span><span class="sxs-lookup"><span data-stu-id="10175-124">Unicode string.Example: Rock</span></span><br/>                   | <span data-ttu-id="10175-125">Genre Anzeige Name.</span><span class="sxs-lookup"><span data-stu-id="10175-125">Genre display name.</span></span>                                                                                                                                |
| <span data-ttu-id="10175-126">Feedsareavailable</span><span class="sxs-lookup"><span data-stu-id="10175-126">FeedsAreAvailable</span></span> | <span data-ttu-id="10175-127">Boolescher Wert. Format: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="10175-127">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="10175-128">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="10175-128">Example: 0</span></span><br/> | <span data-ttu-id="10175-129">Gibt an, ob "Radio Play"-Verhalten durch springen zu einem Feed möglich ist.</span><span class="sxs-lookup"><span data-stu-id="10175-129">Indicates whether "radio play" behavior is possible by jumping to a feed.</span></span>                                                                          |
| <span data-ttu-id="10175-130">Hascomposer</span><span class="sxs-lookup"><span data-stu-id="10175-130">HasComposer</span></span>       | <span data-ttu-id="10175-131">Boolescher Wert. Format: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="10175-131">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="10175-132">Beispiel: 1</span><span class="sxs-lookup"><span data-stu-id="10175-132">Example: 1</span></span><br/> | <span data-ttu-id="10175-133">True, wenn dieses Genre Composer-Informationen im Katalog speichern soll.</span><span class="sxs-lookup"><span data-stu-id="10175-133">True if this genre should save composer information in the catalog.</span></span> <span data-ttu-id="10175-134">Wenn nicht festgelegt, werden die Ersteller-Informationen ignoriert und nicht in den Katalog kompiliert.</span><span class="sxs-lookup"><span data-stu-id="10175-134">If not set, composer information is ignored and not compiled into the catalog.</span></span> |



 

 

 





