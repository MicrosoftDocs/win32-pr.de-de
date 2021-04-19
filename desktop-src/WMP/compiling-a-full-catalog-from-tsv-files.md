---
title: Kompilieren eines vollständigen Katalogs aus TSV-Dateien
description: Kompilieren eines vollständigen Katalogs aus TSV-Dateien
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Windows Media Player Online Stores, Kompilieren von Katalogen
- Online Stores, Kompilieren von Katalogen
- Geben Sie 1 Online Stores ein, kompilieren Sie Kataloge.
- Windows Media Player Online Stores, TSV-Dateien
- Online Stores, TSV-Dateien
- Typ 1 Online Stores, TSV-Dateien
- Windows Media Player Online Stores catcomp.exe
- Online Stores, catcomp.exe
- Geben Sie 1 Online Stores, catcomp.exe
- catcomp.exe
- Kompilieren von Katalogen
- durch Tabstopps getrennte Dateien (TSV)
- TSV-Dateien (durch Tabstopps getrennt)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b68af019a5e2302f52f615d5a1dba2180e27cfe5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341502"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a><span data-ttu-id="17e10-116">Kompilieren eines vollständigen Katalogs aus TSV-Dateien</span><span class="sxs-lookup"><span data-stu-id="17e10-116">Compiling a Full Catalog from TSV Files</span></span>

<span data-ttu-id="17e10-117">Neue Kataloge werden aus einer Reihe von TSV-Dateien (Registerkarten getrennte Werte) erstellt.</span><span class="sxs-lookup"><span data-stu-id="17e10-117">New catalogs are created from a set of tab-separated-value (TSV) files.</span></span> <span data-ttu-id="17e10-118">Die Dateien müssen im Unicode-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="17e10-118">The files must be in Unicode format.</span></span> <span data-ttu-id="17e10-119">Platzieren Sie die unten aufgeführten erforderlichen TSV-Dateien in einem Ordner (dem Eingabe Pfad Argument für catcomp.exe), und wenden Sie catcomp.exe mithilfe der folgenden Syntax an:</span><span class="sxs-lookup"><span data-stu-id="17e10-119">Place the required TSV files listed below into a folder (the input path argument to catcomp.exe), and call catcomp.exe using the following syntax:</span></span>


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



<span data-ttu-id="17e10-120">Wenn keine Versionsnummer angegeben wird, wird die Versionsnummer auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="17e10-120">If a version number is not provided, the version number will be set to 0.</span></span> <span data-ttu-id="17e10-121">Wenn keine Gebiets Schema-ID angegeben ist, wird das Gebiets Schema des Systems verwendet.</span><span class="sxs-lookup"><span data-stu-id="17e10-121">If no locale ID is provided, the system locale is used.</span></span> <span data-ttu-id="17e10-122">Wenn nur ein numerisches optionales Argument angegeben wird, wird davon ausgegangen, dass es sich um die Versionsnummer handelt.</span><span class="sxs-lookup"><span data-stu-id="17e10-122">If only one numeric optional argument is provided, it is assumed to be the version number.</span></span> <span data-ttu-id="17e10-123">Wenn Debug angegeben wird, stellt die Ausgabe auf dem Bildschirm ausführlichere Diagnoseinformationen bereit.</span><span class="sxs-lookup"><span data-stu-id="17e10-123">If debug is specified, the output to the screen will provide more detailed diagnostic information.</span></span>

<span data-ttu-id="17e10-124">Der folgende Code kompiliert beispielsweise einen Katalog aus den Dateien in "C: \\ CatalogData \\ 210" und gibt dem Katalog eine Versionsnummer von 210:</span><span class="sxs-lookup"><span data-stu-id="17e10-124">For example, the following will compile a catalog from the files in C:\\CatalogData\\210 and give the catalog a version number of 210:</span></span>


```C++
catcomp C:\CatalogData\210 210
```



<span data-ttu-id="17e10-125">Um ausführlichere Fehlermeldungen anzuzeigen, kann das optionale Debug-Argument wie folgt hinzugefügt werden:</span><span class="sxs-lookup"><span data-stu-id="17e10-125">To display more detailed error messages, the optional debug argument can be added, as follows:</span></span>


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a><span data-ttu-id="17e10-126">Erforderliche TSV-Dateien</span><span class="sxs-lookup"><span data-stu-id="17e10-126">Required TSV Files</span></span>

<span data-ttu-id="17e10-127">Jede der folgenden Dateien muss vorhanden sein, aber es kann eine leere Datei verwendet werden, wenn keine Daten für eine Datei vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="17e10-127">Each of the following files must be present, but an empty file can be used if there is no data for a file.</span></span> <span data-ttu-id="17e10-128">Wenn der Katalog beispielsweise keine Funkkanäle enthält, kann radio.csv leer sein.</span><span class="sxs-lookup"><span data-stu-id="17e10-128">For instance, if your catalog contains no radio channels, radio.csv can be empty.</span></span> <span data-ttu-id="17e10-129">Die Dateien müssen genau wie aufgeführt benannt werden.</span><span class="sxs-lookup"><span data-stu-id="17e10-129">The files must be named exactly as listed.</span></span>

[<span data-ttu-id="17e10-130">track.csv</span><span class="sxs-lookup"><span data-stu-id="17e10-130">track.csv</span></span>](track-csv.md)

[<span data-ttu-id="17e10-131">album.csv</span><span class="sxs-lookup"><span data-stu-id="17e10-131">album.csv</span></span>](album-csv.md)

[<span data-ttu-id="17e10-132">artist.csv</span><span class="sxs-lookup"><span data-stu-id="17e10-132">artist.csv</span></span>](artist-csv.md)

[<span data-ttu-id="17e10-133">genre.csv</span><span class="sxs-lookup"><span data-stu-id="17e10-133">genre.csv</span></span>](genre-csv.md)

[<span data-ttu-id="17e10-134">subgenre.csv</span><span class="sxs-lookup"><span data-stu-id="17e10-134">subgenre.csv</span></span>](subgenre-csv.md)

[<span data-ttu-id="17e10-135">list.csv</span><span class="sxs-lookup"><span data-stu-id="17e10-135">list.csv</span></span>](list-csv.md)

[<span data-ttu-id="17e10-136">listitem.csv</span><span class="sxs-lookup"><span data-stu-id="17e10-136">listitem.csv</span></span>](listitem-csv.md)

[<span data-ttu-id="17e10-137">radio.csv</span><span class="sxs-lookup"><span data-stu-id="17e10-137">radio.csv</span></span>](radio-csv.md)

> [!Note]  
> <span data-ttu-id="17e10-138">Obwohl die Dateinamen über CSV-Erweiterungen verfügen müssen, sind die Dateien nicht im CSV-Format (Komma getrennte Werte) enthalten.</span><span class="sxs-lookup"><span data-stu-id="17e10-138">Although the file names must have .csv extensions, the files are not in Comma Separated Values (CSV) format.</span></span> <span data-ttu-id="17e10-139">Die Dateien müssen im TSV-Format (Tabulator getrennte Werte) vorliegen.</span><span class="sxs-lookup"><span data-stu-id="17e10-139">The files must be in Tab Separated Values (TSV) format.</span></span>

 

<span data-ttu-id="17e10-140">Wenn die Kompilierung erfolgreich ist, erstellt catcomp.exe drei Ausgabedateien.</span><span class="sxs-lookup"><span data-stu-id="17e10-140">If compilation is successful, catcomp.exe creates three output files.</span></span>



| <span data-ttu-id="17e10-141">Dateiname</span><span class="sxs-lookup"><span data-stu-id="17e10-141">File name</span></span>                   | <span data-ttu-id="17e10-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17e10-142">Description</span></span>                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17e10-143">Catalog. wmdb</span><span class="sxs-lookup"><span data-stu-id="17e10-143">catalog.wmdb</span></span>                | <span data-ttu-id="17e10-144">Nicht komprimierter kompilierter Katalog.</span><span class="sxs-lookup"><span data-stu-id="17e10-144">Uncompressed compiled catalog.</span></span>                                                                                                                                                      |
| <span data-ttu-id="17e10-145">Catalog. wmdb. LZ</span><span class="sxs-lookup"><span data-stu-id="17e10-145">catalog.wmdb.lz</span></span>             | <span data-ttu-id="17e10-146">Katalog in komprimiertem Format.</span><span class="sxs-lookup"><span data-stu-id="17e10-146">Catalog in compressed format.</span></span> <span data-ttu-id="17e10-147">Ihr Plug-in kann den Speicherort dieser Datei an Windows Media Player in [iwmpcontentpartner:: getcatalogurl](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)übergeben.</span><span class="sxs-lookup"><span data-stu-id="17e10-147">Your plug-in can give the location of this file to Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> |
| <span data-ttu-id="17e10-148">kompilierte \_ eindeutige \_words.txt</span><span class="sxs-lookup"><span data-stu-id="17e10-148">compiled\_unique\_words.txt</span></span> | <span data-ttu-id="17e10-149">Eine zwischen Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="17e10-149">An intermediate output file.</span></span> <span data-ttu-id="17e10-150">Wird nicht von Windows Media Player verwendet.</span><span class="sxs-lookup"><span data-stu-id="17e10-150">Not used by Windows Media Player.</span></span>                                                                                                                      |



 

 

 




