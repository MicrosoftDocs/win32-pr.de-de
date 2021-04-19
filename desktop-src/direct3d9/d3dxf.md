---
description: X Dateiformat-, Lade-und Speicheroptionen.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073887c6cc93754ead01ce379310a9be09edc88f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342930"
---
# <a name="d3dxf"></a><span data-ttu-id="cee02-103">D3DXF</span><span class="sxs-lookup"><span data-stu-id="cee02-103">D3DXF</span></span>

<span data-ttu-id="cee02-104">X Dateiformat-, Lade-und Speicheroptionen.</span><span class="sxs-lookup"><span data-stu-id="cee02-104">X file format, load, and save options.</span></span>

## <a name="file-formats"></a><span data-ttu-id="cee02-105">Dateiformate</span><span class="sxs-lookup"><span data-stu-id="cee02-105">File Formats</span></span>

<span data-ttu-id="cee02-106">In der folgenden Tabelle sind die Datei Datentypen angegeben:</span><span class="sxs-lookup"><span data-stu-id="cee02-106">The following table specifies the type of file data:</span></span>



| <span data-ttu-id="cee02-107">\#definiert das Datei Format.</span><span class="sxs-lookup"><span data-stu-id="cee02-107">\#defines for File Format</span></span>     | <span data-ttu-id="cee02-108">Wert</span><span class="sxs-lookup"><span data-stu-id="cee02-108">Value</span></span> | <span data-ttu-id="cee02-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cee02-109">Description</span></span>                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cee02-110">D3DXF \_ File Format- \_ Binärdatei</span><span class="sxs-lookup"><span data-stu-id="cee02-110">D3DXF\_FILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="cee02-111">0</span><span class="sxs-lookup"><span data-stu-id="cee02-111">0</span></span>     | <span data-ttu-id="cee02-112">Binärdatei im Legacy Format.</span><span class="sxs-lookup"><span data-stu-id="cee02-112">Legacy-format binary file.</span></span> <span data-ttu-id="cee02-113">Siehe [Referenz zu X-Dateien (Legacy)](dx9-graphics-reference-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="cee02-113">See [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span> |
| <span data-ttu-id="cee02-114">D3DXF \_ File Format- \_ Text</span><span class="sxs-lookup"><span data-stu-id="cee02-114">D3DXF\_FILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="cee02-115">1</span><span class="sxs-lookup"><span data-stu-id="cee02-115">1</span></span>     | <span data-ttu-id="cee02-116">Textdatei.</span><span class="sxs-lookup"><span data-stu-id="cee02-116">Text file.</span></span>                                                                                     |
| <span data-ttu-id="cee02-117">D3DXF \_ File Format \_ komprimiert</span><span class="sxs-lookup"><span data-stu-id="cee02-117">D3DXF\_FILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="cee02-118">2</span><span class="sxs-lookup"><span data-stu-id="cee02-118">2</span></span>     | <span data-ttu-id="cee02-119">Komprimierte Datei.</span><span class="sxs-lookup"><span data-stu-id="cee02-119">Compressed file.</span></span> <span data-ttu-id="cee02-120">Mit diesem Flag müssen Sie auch das Binärformat oder das Textformat angeben.</span><span class="sxs-lookup"><span data-stu-id="cee02-120">With this flag, you must also specify the binary format or the text format.</span></span>   |



 

## <a name="file-load-options"></a><span data-ttu-id="cee02-121">Optionen zum Laden von Dateien</span><span class="sxs-lookup"><span data-stu-id="cee02-121">File Load Options</span></span>

<span data-ttu-id="cee02-122">In der folgenden Tabelle sind die Optionen zum Laden von Dateien mit x-Dateien angegeben:</span><span class="sxs-lookup"><span data-stu-id="cee02-122">The following table specifies file load options with .x files:</span></span>



| <span data-ttu-id="cee02-123">\#definieren</span><span class="sxs-lookup"><span data-stu-id="cee02-123">\#define</span></span>                      | <span data-ttu-id="cee02-124">Wert</span><span class="sxs-lookup"><span data-stu-id="cee02-124">Value</span></span> | <span data-ttu-id="cee02-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cee02-125">Description</span></span>                |
|-------------------------------|-------|----------------------------|
| <span data-ttu-id="cee02-126">D3DXF \_ fileload \_ FromFile</span><span class="sxs-lookup"><span data-stu-id="cee02-126">D3DXF\_FILELOAD\_FromFile</span></span>     | <span data-ttu-id="cee02-127">0</span><span class="sxs-lookup"><span data-stu-id="cee02-127">0</span></span>     | <span data-ttu-id="cee02-128">Laden von Daten aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="cee02-128">Load data from a file.</span></span>     |
| <span data-ttu-id="cee02-129">D3DXF \_ fileload \_ fromwfile</span><span class="sxs-lookup"><span data-stu-id="cee02-129">D3DXF\_FILELOAD\_FROMWFILE</span></span>    | <span data-ttu-id="cee02-130">1</span><span class="sxs-lookup"><span data-stu-id="cee02-130">1</span></span>     | <span data-ttu-id="cee02-131">Laden von Daten aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="cee02-131">Load data from a file.</span></span>     |
| <span data-ttu-id="cee02-132">D3DXF \_ fileload \_ FromResource</span><span class="sxs-lookup"><span data-stu-id="cee02-132">D3DXF\_FILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="cee02-133">2</span><span class="sxs-lookup"><span data-stu-id="cee02-133">2</span></span>     | <span data-ttu-id="cee02-134">Laden von Daten aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="cee02-134">Load data from a resource.</span></span> |
| <span data-ttu-id="cee02-135">D3DXF \_ fileload \_ frommemory</span><span class="sxs-lookup"><span data-stu-id="cee02-135">D3DXF\_FILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="cee02-136">3</span><span class="sxs-lookup"><span data-stu-id="cee02-136">3</span></span>     | <span data-ttu-id="cee02-137">Laden von Daten aus dem Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="cee02-137">Load data from memory.</span></span>     |



 

## <a name="file-save-options"></a><span data-ttu-id="cee02-138">Optionen zum Speichern von Dateien</span><span class="sxs-lookup"><span data-stu-id="cee02-138">File Save Options</span></span>

<span data-ttu-id="cee02-139">In der folgenden Tabelle sind die Optionen zum Speichern und Laden von Dateien mit x-Dateien angegeben:</span><span class="sxs-lookup"><span data-stu-id="cee02-139">The following table specifies file save and load options with .x files:</span></span>



| <span data-ttu-id="cee02-140">\#definieren</span><span class="sxs-lookup"><span data-stu-id="cee02-140">\#define</span></span>                 | <span data-ttu-id="cee02-141">Wert</span><span class="sxs-lookup"><span data-stu-id="cee02-141">Value</span></span> | <span data-ttu-id="cee02-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cee02-142">Description</span></span>                    |
|--------------------------|-------|--------------------------------|
| <span data-ttu-id="cee02-143">Datei "D3DXF \_ filesave" \_</span><span class="sxs-lookup"><span data-stu-id="cee02-143">D3DXF\_FILESAVE\_TOFILE</span></span>  | <span data-ttu-id="cee02-144">0</span><span class="sxs-lookup"><span data-stu-id="cee02-144">0</span></span>     | <span data-ttu-id="cee02-145">In einer Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="cee02-145">Save to a file.</span></span>                |
| <span data-ttu-id="cee02-146">D3DXF \_ filesave \_ towfile</span><span class="sxs-lookup"><span data-stu-id="cee02-146">D3DXF\_FILESAVE\_TOWFILE</span></span> | <span data-ttu-id="cee02-147">1</span><span class="sxs-lookup"><span data-stu-id="cee02-147">1</span></span>     | <span data-ttu-id="cee02-148">In einer breit Zeichen Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="cee02-148">Save to a wide-character file.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="cee02-149">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="cee02-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="cee02-150">Header</span><span class="sxs-lookup"><span data-stu-id="cee02-150">Header</span></span>                   | <span data-ttu-id="cee02-151">d3dx9xof. h</span><span class="sxs-lookup"><span data-stu-id="cee02-151">d3dx9xof.h</span></span> |
| <span data-ttu-id="cee02-152">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="cee02-152">Minimum operating system</span></span> | <span data-ttu-id="cee02-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="cee02-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cee02-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cee02-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cee02-155">D3DX X-Datei Konstanten</span><span class="sxs-lookup"><span data-stu-id="cee02-155">D3DX X File Constants</span></span>](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[<span data-ttu-id="cee02-156">**D3DXSaveMeshToX**</span><span class="sxs-lookup"><span data-stu-id="cee02-156">**D3DXSaveMeshToX**</span></span>](d3dxsavemeshtox.md)
</dt> </dl>

 

 



