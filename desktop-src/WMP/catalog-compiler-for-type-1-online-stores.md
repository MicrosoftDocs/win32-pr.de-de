---
title: Katalog Compiler für Typ 1-Online Speicher
description: Katalog Compiler für Typ 1-Online Speicher
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Windows Media Player Online Stores, Katalog Compiler
- Online Stores, Katalog Compiler
- Typ 1 Online Stores, Katalog Compiler
- Windows Media Player Online Stores catcomp.exe
- Online Stores, catcomp.exe
- Geben Sie 1 Online Stores, catcomp.exe
- Katalog Compiler
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c54ffd054c5e72b04ddd32eef12c7fe6b6cc89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341501"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a><span data-ttu-id="66be9-111">Katalog Compiler für Typ 1-Online Speicher</span><span class="sxs-lookup"><span data-stu-id="66be9-111">Catalog Compiler for Type 1 Online Stores</span></span>

<span data-ttu-id="66be9-112">Der Katalog Compiler (catcomp.exe) ist ein Befehlszeilen Tool, das vom Typ 1 Online Stores verwendet wird, um den Satz von TSV-Dateien, die die Katalogdaten des Online Stores enthalten, in einen komprimierten Katalog zu kompilieren, der von Windows Media Player heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="66be9-112">The catalog compiler (catcomp.exe) is a command-line tool used by Type 1 online stores to compile the set of tab-separated-value (TSV) files containing the online store's catalog data into a compressed catalog that can be downloaded by Windows Media Player.</span></span> <span data-ttu-id="66be9-113">Der Katalog Compiler kompiliert auch Katalog Update Dateien, die nur die Katalog Informationen enthalten, die seit dem letzten Katalog Update geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="66be9-113">The catalog compiler also compiles catalog update files containing only the catalog information that has changed since the last catalog update.</span></span>

<span data-ttu-id="66be9-114">Die komprimierten Katalogdateien oder Katalog Update Dateien sollten für Windows-Media Player bereitgestellt werden, um Sie in der Implementierung von [iwmpcontentpartner:: getcatalogurl](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)des Online Store-Plug-ins herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="66be9-114">The compressed catalog files or catalog update files should be provided to Windows Media Player for download in the online store plug-in's implementation of [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span>

<span data-ttu-id="66be9-115">Allgemeine Aufgaben</span><span class="sxs-lookup"><span data-stu-id="66be9-115">Common Tasks</span></span>

-   [<span data-ttu-id="66be9-116">Kompilieren eines vollständigen Katalogs aus TSV-Dateien</span><span class="sxs-lookup"><span data-stu-id="66be9-116">Compiling a Full Catalog from TSV Files</span></span>](compiling-a-full-catalog-from-tsv-files.md)
-   [<span data-ttu-id="66be9-117">Kompilieren eines Katalog Updates aus vollständigen Katalogen</span><span class="sxs-lookup"><span data-stu-id="66be9-117">Compiling a Catalog Update from Full Catalogs</span></span>](compiling-a-catalog-update-from-full-catalogs.md)

<span data-ttu-id="66be9-118">Diagnose Tasks</span><span class="sxs-lookup"><span data-stu-id="66be9-118">Diagnostic Tasks</span></span>

-   [<span data-ttu-id="66be9-119">Anzeigen der Hilfe</span><span class="sxs-lookup"><span data-stu-id="66be9-119">Displaying Help</span></span>](displaying-help.md)
-   [<span data-ttu-id="66be9-120">Abrufen von Katalog Informationen</span><span class="sxs-lookup"><span data-stu-id="66be9-120">Retrieving Catalog Information</span></span>](retrieving-catalog-information.md)
-   [<span data-ttu-id="66be9-121">Anwenden eines Updates auf einen Katalog</span><span class="sxs-lookup"><span data-stu-id="66be9-121">Applying an Update To a Catalog</span></span>](applying-an-update-to-a-catalog.md)

 

 




