---
title: Kompilieren eines Katalog Updates aus vollständigen Katalogen
description: Kompilieren eines Katalog Updates aus vollständigen Katalogen
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Windows Media Player Online Stores, Kompilieren von Katalogen
- Online Stores, Kompilieren von Katalogen
- Geben Sie 1 Online Stores ein, kompilieren Sie Kataloge.
- Windows Media Player Online Stores, Katalog Updates
- Online Stores, Katalog Updates
- Typ 1 Online Stores, Katalog Updates
- Windows Media Player Online Stores, vollständige Kataloge
- Online Stores, vollständige Kataloge
- Typ 1 Online Stores, vollständige Kataloge
- Kompilieren von Katalogen
- Katalog Updates
- vollständige Kataloge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaa6d1bc0d3dbc4fefaffe1498be03259716a5e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314213"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a><span data-ttu-id="14bd9-115">Kompilieren eines Katalog Updates aus vollständigen Katalogen</span><span class="sxs-lookup"><span data-stu-id="14bd9-115">Compiling a Catalog Update from Full Catalogs</span></span>

<span data-ttu-id="14bd9-116">Ein Katalog Update, das die Änderungen zwischen zwei Versionen eines kompilierten Katalogs enthält, kann mithilfe der unten stehenden Syntax erstellt werden. dabei ist *path1* das Verzeichnis, das den ersten Katalog enthält, *path2* ist das Verzeichnis, das den zweiten Katalog enthält, und das Debuggen kann optional eingeschlossen werden, um detaillierte Fehlerinformationen auf dem Bildschirm anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="14bd9-116">A catalog update containing the changes between two versions of a compiled catalog can be created by using the syntax below, where *path1* is the directory containing the first catalog, *path2* is the directory containing the second catalog, and debug can be optionally included to display detailed error information on the screen.</span></span> <span data-ttu-id="14bd9-117">Die Katalogdateien müssen in unkomprimierter Form vorliegen – der Dateiname des kompilierten Katalogs lautet catalog. wmdb anstelle von Catalog. wmdb. LZ.</span><span class="sxs-lookup"><span data-stu-id="14bd9-117">The catalog files must be in uncompressed form—the file name of the compiled catalog would be catalog.wmdb, rather than catalog.wmdb.lz.</span></span>


```C++
catcomp diff <path1> <path2> [debug]
```



<span data-ttu-id="14bd9-118">Wenn das Verzeichnis c: Catalog210 z. b. \\ \\ Version 210 eines vollständig kompilierten Katalogs enthält und C: \\ Catalog211 \\ Version 211 enthält, erstellt der folgende Befehl eine Differenz Datei, die die Änderungen zwischen den beiden Versionen enthält:</span><span class="sxs-lookup"><span data-stu-id="14bd9-118">For example, if the C:\\Catalog210\\ directory contains version 210 of a full compiled catalog and C:\\Catalog211\\ contains version 211, the following command creates a difference file that contains the changes between the two versions:</span></span>


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



<span data-ttu-id="14bd9-119">Um ausführliche Fehlerinformationen anzuzeigen, können Sie den optionalen Debug-Parameter wie folgt hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="14bd9-119">To display detailed error information, you can add the optional debug parameter as follows:</span></span>


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



<span data-ttu-id="14bd9-120">Wenn die Kompilierung erfolgreich ist, erstellt catcomp.exe die unten aufgeführten Ausgabedateien und speichert Sie in dem Verzeichnis, das den ersten Katalog enthält.</span><span class="sxs-lookup"><span data-stu-id="14bd9-120">If compilation is successful, catcomp.exe creates the output files listed below and saves them in the directory that contains the first catalog.</span></span>



| <span data-ttu-id="14bd9-121">Dateiname</span><span class="sxs-lookup"><span data-stu-id="14bd9-121">File name</span></span>             | <span data-ttu-id="14bd9-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14bd9-122">Description</span></span>                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14bd9-123">Catalog. diff</span><span class="sxs-lookup"><span data-stu-id="14bd9-123">catalog.diff</span></span>          | <span data-ttu-id="14bd9-124">Nicht komprimierte kompilierte Differenz Datei.</span><span class="sxs-lookup"><span data-stu-id="14bd9-124">Uncompressed compiled difference file.</span></span>                                                                                                                                                           |
| <span data-ttu-id="14bd9-125">Catalog. diff. LZ</span><span class="sxs-lookup"><span data-stu-id="14bd9-125">catalog.diff.lz</span></span>       | <span data-ttu-id="14bd9-126">Komprimierte Version der Katalog Update Datei.</span><span class="sxs-lookup"><span data-stu-id="14bd9-126">Compressed version of catalog update file.</span></span> <span data-ttu-id="14bd9-127">Ihr Plug-in kann den Speicherort dieser Datei an Windows Media Player in [iwmpcontentpartner:: getcatalogurl](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)übergeben.</span><span class="sxs-lookup"><span data-stu-id="14bd9-127">Your plug-in can give the location of this file to Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> |
| <span data-ttu-id="14bd9-128">Catalog. wmdb. Delta</span><span class="sxs-lookup"><span data-stu-id="14bd9-128">catalog.wmdb.delta</span></span>    | <span data-ttu-id="14bd9-129">Zwischen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="14bd9-129">Intermediate output file.</span></span> <span data-ttu-id="14bd9-130">Wird nicht von Windows Media Player verwendet</span><span class="sxs-lookup"><span data-stu-id="14bd9-130">Not used by Windows Media Player</span></span>                                                                                                                                       |
| <span data-ttu-id="14bd9-131">Catalog. wmdb. modified</span><span class="sxs-lookup"><span data-stu-id="14bd9-131">catalog.wmdb.modified</span></span> | <span data-ttu-id="14bd9-132">Zwischen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="14bd9-132">Intermediate output file.</span></span> <span data-ttu-id="14bd9-133">Wird nicht von Windows Media Player verwendet</span><span class="sxs-lookup"><span data-stu-id="14bd9-133">Not used by Windows Media Player</span></span>                                                                                                                                       |



 

 

 




