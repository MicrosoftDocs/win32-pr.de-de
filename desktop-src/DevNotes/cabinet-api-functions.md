---
description: Weitere Informationen finden Sie in den CAB-API-Funktionen.
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: CAB-API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327490332d2fe0cb9384eeaaad11215d551f4f0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860911"
---
# <a name="cabinet-api-functions"></a><span data-ttu-id="a3c77-103">CAB-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a3c77-103">Cabinet API Functions</span></span>

<span data-ttu-id="a3c77-104">In diesem Abschnitt werden die folgenden CAB-API-Funktionen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="a3c77-104">This section describes the following Cabinet API functions:</span></span>

## <a name="fci-functions"></a><span data-ttu-id="a3c77-105">FCI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a3c77-105">FCI Functions</span></span>

<span data-ttu-id="a3c77-106">Die FCI (File Compression Interface)-Bibliothek bietet die Möglichkeit zum Erstellen von schränken (auch als "CAB-Dateien" bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="a3c77-106">The FCI (File Compression Interface) library provides the ability to create cabinets (also known as "CAB files").</span></span> <span data-ttu-id="a3c77-107">Außerdem bietet die Bibliothek Komprimierung, um die Größe der in den Schränken gespeicherten Datei Daten zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="a3c77-107">Additionally, the library provides compression to reduce the size of the file data stored in cabinets.</span></span>



| <span data-ttu-id="a3c77-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="a3c77-108">Function</span></span>                                   | <span data-ttu-id="a3c77-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3c77-109">Description</span></span>                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3c77-110">**Datei "file"**</span><span class="sxs-lookup"><span data-stu-id="a3c77-110">**FCIAddFile**</span></span>](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | <span data-ttu-id="a3c77-111">Fügt der CAB-Datei eine Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="a3c77-111">Adds a file to the cabinet currently being contructed.</span></span><br/>                                           |
| [<span data-ttu-id="a3c77-112">**"F" erstellen**</span><span class="sxs-lookup"><span data-stu-id="a3c77-112">**FCICreate**</span></span>](/windows/desktop/api/Fci/nf-fci-fcicreate)             | <span data-ttu-id="a3c77-113">Erstellt einen FCI-Kontext.</span><span class="sxs-lookup"><span data-stu-id="a3c77-113">Creates an FCI context.</span></span><br/>                                                                          |
| [<span data-ttu-id="a3c77-114">**Mit der Verschlüsselung**</span><span class="sxs-lookup"><span data-stu-id="a3c77-114">**FCIDestroy**</span></span>](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | <span data-ttu-id="a3c77-115">Löscht einen geöffneten FCI-Kontext, wodurch alle dem Kontext zugeordneten Speicher-und temporären Dateien freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a3c77-115">Deletes an open FCI context, freeing any memory and temporary files associated with the context.</span></span><br/> |
| [<span data-ttu-id="a3c77-116">**"Sciflushcabinet"**</span><span class="sxs-lookup"><span data-stu-id="a3c77-116">**FCIFlushCabinet**</span></span>](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | <span data-ttu-id="a3c77-117">Schließt den aktuellen Schrank ab.</span><span class="sxs-lookup"><span data-stu-id="a3c77-117">Completes the current cabinet.</span></span><br/>                                                                   |
| [<span data-ttu-id="a3c77-118">**Ordner "sciflushfolder"**</span><span class="sxs-lookup"><span data-stu-id="a3c77-118">**FCIFlushFolder**</span></span>](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | <span data-ttu-id="a3c77-119">Erzwingt, dass der aktuelle Ordner in der Konstruktion sofort abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="a3c77-119">Forces the current folder under construction to be completed immediately.</span></span><br/>                        |



 

## <a name="fdi-functions"></a><span data-ttu-id="a3c77-120">FDI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a3c77-120">FDI Functions</span></span>

<span data-ttu-id="a3c77-121">Die Bibliothek "FDI (File decompression Interface)" bietet die Möglichkeit, Dateien aus schränken zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="a3c77-121">The FDI (File Decompression Interface) library provides the ability to extract files from cabinets.</span></span>



| <span data-ttu-id="a3c77-122">Funktion</span><span class="sxs-lookup"><span data-stu-id="a3c77-122">Function</span></span>                                         | <span data-ttu-id="a3c77-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3c77-123">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a3c77-124">**Nicht kopieren**</span><span class="sxs-lookup"><span data-stu-id="a3c77-124">**FDICopy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | <span data-ttu-id="a3c77-125">Extrahiert Dateien aus kabinatendateien.</span><span class="sxs-lookup"><span data-stu-id="a3c77-125">Extracts files from cabinets.</span></span><br/>                                                          |
| [<span data-ttu-id="a3c77-126">**"F" erstellen**</span><span class="sxs-lookup"><span data-stu-id="a3c77-126">**FDICreate**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | <span data-ttu-id="a3c77-127">Erstellt einen FDI-Kontext.</span><span class="sxs-lookup"><span data-stu-id="a3c77-127">Creates an FDI context.</span></span><br/>                                                                |
| [<span data-ttu-id="a3c77-128">**Nicht löschen**</span><span class="sxs-lookup"><span data-stu-id="a3c77-128">**FDIDestroy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | <span data-ttu-id="a3c77-129">Löscht einen geöffneten FDI-Kontext.</span><span class="sxs-lookup"><span data-stu-id="a3c77-129">Deletes an open FDI context.</span></span><br/>                                                           |
| [<span data-ttu-id="a3c77-130">**"F"**</span><span class="sxs-lookup"><span data-stu-id="a3c77-130">**FDIIsCabinet**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | <span data-ttu-id="a3c77-131">Bestimmt, ob eine Datei eine CAB-Datei ist, und gibt ggf. beschreibende Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="a3c77-131">Determines whether a file is a cabinet and, if it is, returns descriptive information.</span></span><br/> |
| [<span data-ttu-id="a3c77-132">**"F"**</span><span class="sxs-lookup"><span data-stu-id="a3c77-132">**FDITruncateCabinet**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | <span data-ttu-id="a3c77-133">Verkürzt eine CAB-Datei ab der angegebenen Ordner Nummer.</span><span class="sxs-lookup"><span data-stu-id="a3c77-133">Truncates a cabinet file starting at the specified folder number.</span></span><br/>                      |



 

## <a name="deprecated-functions"></a><span data-ttu-id="a3c77-134">Veraltete Funktionen</span><span class="sxs-lookup"><span data-stu-id="a3c77-134">Deprecated Functions</span></span>

-   [<span data-ttu-id="a3c77-135">**Deleteextractedfiles**</span><span class="sxs-lookup"><span data-stu-id="a3c77-135">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
-   [<span data-ttu-id="a3c77-136">**Dllgetversion**</span><span class="sxs-lookup"><span data-stu-id="a3c77-136">**DllGetVersion**</span></span>](dllgetversion.md)
-   [<span data-ttu-id="a3c77-137">**Extrahieren**</span><span class="sxs-lookup"><span data-stu-id="a3c77-137">**Extract**</span></span>](extract.md)
-   [<span data-ttu-id="a3c77-138">**Getdllversion**</span><span class="sxs-lookup"><span data-stu-id="a3c77-138">**GetDllVersion**</span></span>](getdllversion.md)

## <a name="related-topics"></a><span data-ttu-id="a3c77-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a3c77-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3c77-140">CAB-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="a3c77-140">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="a3c77-141">Verwenden der CAB-API</span><span class="sxs-lookup"><span data-stu-id="a3c77-141">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 




