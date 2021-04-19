---
title: Anwenden eines Updates auf einen Katalog
description: Anwenden eines Updates auf einen Katalog
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Windows Media Player Online Stores, Anwenden von Updates auf Kataloge
- Online Stores, Anwenden von Updates auf Kataloge
- Typ 1 Online Stores, Anwenden von Updates auf Kataloge
- Windows Media Player Online Stores, Aktualisieren von Katalogen
- Online Stores, Kataloge aktualisieren
- Typ 1 Online Stores, Kataloge aktualisieren
- Windows Media Player Online Stores, Katalog Updates
- Online Stores, Katalog Updates
- Typ 1 Online Stores, Katalog Updates
- Katalog Updates
- Aktualisieren von Katalogen
- Anwenden von Updates auf Kataloge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d468edb7d09b8804fa924f7c31fc1be45d27c8fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339844"
---
# <a name="applying-an-update-to-a-catalog"></a><span data-ttu-id="ec55e-115">Anwenden eines Updates auf einen Katalog</span><span class="sxs-lookup"><span data-stu-id="ec55e-115">Applying an Update To a Catalog</span></span>

> [!Note]  
> <span data-ttu-id="ec55e-116">Dies erfolgt in der Regel nicht mit Ausnahme von Diagnose Zwecken – beispielsweise, um zu überprüfen, ob eine Differenz Datei gültig ist.</span><span class="sxs-lookup"><span data-stu-id="ec55e-116">This is not normally done except for diagnostic purposes—for instance, to help verify that a difference file is valid.</span></span> <span data-ttu-id="ec55e-117">Der auf diese Weise generierte Katalog befindet sich nicht in komprimierter Form und sollte nicht an Windows Media Player übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="ec55e-117">The catalog generated in this way is not in compressed form and should not be passed to Windows Media Player.</span></span>

 

<span data-ttu-id="ec55e-118">Eine neue Katalog Datei kann mithilfe der unten stehenden Syntax erstellt werden, wobei *Input Catalog* der Speicherort des ursprünglichen Katalogs und *inputdiff* der Speicherort der anzuwendenden Differenz Datei ist.</span><span class="sxs-lookup"><span data-stu-id="ec55e-118">A new catalog file can be created by using the syntax below, where *inputcatalog* is the location of the original catalog, and *inputdiff* is the location of the difference file to apply.</span></span> <span data-ttu-id="ec55e-119">Die Katalogdateien müssen in unkomprimierter Form vorliegen.</span><span class="sxs-lookup"><span data-stu-id="ec55e-119">The catalog files must be in uncompressed form.</span></span>


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



<span data-ttu-id="ec55e-120">Der folgende Code erstellt z. b. einen neuen Katalog aus C: \\ Catalog210 \\ catalog. wmdb und c: \\ Catalog210 \\ catalog. diff.</span><span class="sxs-lookup"><span data-stu-id="ec55e-120">For example, the following creates a new catalog from C:\\Catalog210\\catalog.wmdb and C:\\Catalog210\\catalog.diff.</span></span>


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



<span data-ttu-id="ec55e-121">Wenn die Kompilierung erfolgreich ist, erstellt catcomp.exe die folgenden Ausgabedateien.</span><span class="sxs-lookup"><span data-stu-id="ec55e-121">If compilation is successful, catcomp.exe creates the follow output files.</span></span>



| <span data-ttu-id="ec55e-122">Dateiname</span><span class="sxs-lookup"><span data-stu-id="ec55e-122">File name</span></span>        | <span data-ttu-id="ec55e-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec55e-123">Description</span></span>       |
|------------------|-------------------|
| <span data-ttu-id="ec55e-124">Catalog. wmdb. New</span><span class="sxs-lookup"><span data-stu-id="ec55e-124">catalog.wmdb.new</span></span> | <span data-ttu-id="ec55e-125">Neue Katalog Datei.</span><span class="sxs-lookup"><span data-stu-id="ec55e-125">New catalog file.</span></span> |



 

 

 




