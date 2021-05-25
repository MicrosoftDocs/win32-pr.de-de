---
description: X-Dateiformat, Lade- und Speicheroptionen.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e230fc08ac4d7f8713959f2025f67262046ecea5
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343645"
---
# <a name="d3dxf"></a><span data-ttu-id="7c95d-103">D3DXF</span><span class="sxs-lookup"><span data-stu-id="7c95d-103">D3DXF</span></span>

<span data-ttu-id="7c95d-104">X-Dateiformat, Lade- und Speicheroptionen.</span><span class="sxs-lookup"><span data-stu-id="7c95d-104">X file format, load, and save options.</span></span>

## <a name="file-formats"></a><span data-ttu-id="7c95d-105">Dateiformate</span><span class="sxs-lookup"><span data-stu-id="7c95d-105">File Formats</span></span>

<span data-ttu-id="7c95d-106">In der folgenden Tabelle wird der Typ der Dateidaten angegeben:</span><span class="sxs-lookup"><span data-stu-id="7c95d-106">The following table specifies the type of file data:</span></span>



| <span data-ttu-id="7c95d-107">\#definiert für Das Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="7c95d-107">\#defines for File Format</span></span>     | <span data-ttu-id="7c95d-108">Wert</span><span class="sxs-lookup"><span data-stu-id="7c95d-108">Value</span></span> | <span data-ttu-id="7c95d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c95d-109">Description</span></span>                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c95d-110">D3DXF \_ FILEFORMAT \_ BINARY</span><span class="sxs-lookup"><span data-stu-id="7c95d-110">D3DXF\_FILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="7c95d-111">0</span><span class="sxs-lookup"><span data-stu-id="7c95d-111">0</span></span>     | <span data-ttu-id="7c95d-112">Binärdatei im Legacyformat.</span><span class="sxs-lookup"><span data-stu-id="7c95d-112">Legacy-format binary file.</span></span> <span data-ttu-id="7c95d-113">Weitere Informationen [finden Sie unter X-Dateireferenz (Legacy).](dx9-graphics-reference-x-file.md)</span><span class="sxs-lookup"><span data-stu-id="7c95d-113">See [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span> |
| <span data-ttu-id="7c95d-114">D3DXF \_ FILEFORMAT \_ TEXT</span><span class="sxs-lookup"><span data-stu-id="7c95d-114">D3DXF\_FILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="7c95d-115">1</span><span class="sxs-lookup"><span data-stu-id="7c95d-115">1</span></span>     | <span data-ttu-id="7c95d-116">Textdatei.</span><span class="sxs-lookup"><span data-stu-id="7c95d-116">Text file.</span></span>                                                                                     |
| <span data-ttu-id="7c95d-117">D3DXF \_ FILEFORMAT \_ COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="7c95d-117">D3DXF\_FILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="7c95d-118">2</span><span class="sxs-lookup"><span data-stu-id="7c95d-118">2</span></span>     | <span data-ttu-id="7c95d-119">Komprimierte Datei.</span><span class="sxs-lookup"><span data-stu-id="7c95d-119">Compressed file.</span></span> <span data-ttu-id="7c95d-120">Mit diesem Flag müssen Sie auch das Binärformat oder das Textformat angeben.</span><span class="sxs-lookup"><span data-stu-id="7c95d-120">With this flag, you must also specify the binary format or the text format.</span></span>   |



 

## <a name="file-load-options"></a><span data-ttu-id="7c95d-121">Optionen zum Laden von Dateien</span><span class="sxs-lookup"><span data-stu-id="7c95d-121">File Load Options</span></span>

<span data-ttu-id="7c95d-122">In der folgenden Tabelle werden Optionen zum Laden von Dateien mit X-Dateien angegeben:</span><span class="sxs-lookup"><span data-stu-id="7c95d-122">The following table specifies file load options with .x files:</span></span>



| <span data-ttu-id="7c95d-123">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="7c95d-123">\#define</span></span>                      | <span data-ttu-id="7c95d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="7c95d-124">Value</span></span> | <span data-ttu-id="7c95d-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c95d-125">Description</span></span>                |
|-------------------------------|-------|----------------------------|
| <span data-ttu-id="7c95d-126">D3DXF \_ FILELOAD \_ FromFile</span><span class="sxs-lookup"><span data-stu-id="7c95d-126">D3DXF\_FILELOAD\_FromFile</span></span>     | <span data-ttu-id="7c95d-127">0</span><span class="sxs-lookup"><span data-stu-id="7c95d-127">0</span></span>     | <span data-ttu-id="7c95d-128">Laden von Daten aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="7c95d-128">Load data from a file.</span></span>     |
| <span data-ttu-id="7c95d-129">D3DXF \_ FILELOAD \_ FROMWFILE</span><span class="sxs-lookup"><span data-stu-id="7c95d-129">D3DXF\_FILELOAD\_FROMWFILE</span></span>    | <span data-ttu-id="7c95d-130">1</span><span class="sxs-lookup"><span data-stu-id="7c95d-130">1</span></span>     | <span data-ttu-id="7c95d-131">Laden von Daten aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="7c95d-131">Load data from a file.</span></span>     |
| <span data-ttu-id="7c95d-132">D3DXF \_ FILELOAD \_ FROMRESOURCE</span><span class="sxs-lookup"><span data-stu-id="7c95d-132">D3DXF\_FILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="7c95d-133">2</span><span class="sxs-lookup"><span data-stu-id="7c95d-133">2</span></span>     | <span data-ttu-id="7c95d-134">Laden von Daten aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="7c95d-134">Load data from a resource.</span></span> |
| <span data-ttu-id="7c95d-135">D3DXF \_ FILELOAD \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="7c95d-135">D3DXF\_FILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="7c95d-136">3</span><span class="sxs-lookup"><span data-stu-id="7c95d-136">3</span></span>     | <span data-ttu-id="7c95d-137">Laden von Daten aus dem Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="7c95d-137">Load data from memory.</span></span>     |



 

## <a name="file-save-options"></a><span data-ttu-id="7c95d-138">Dateispeicheroptionen</span><span class="sxs-lookup"><span data-stu-id="7c95d-138">File Save Options</span></span>

<span data-ttu-id="7c95d-139">In der folgenden Tabelle werden Optionen zum Speichern und Laden von Dateien mit X-Dateien angegeben:</span><span class="sxs-lookup"><span data-stu-id="7c95d-139">The following table specifies file save and load options with .x files:</span></span>



| <span data-ttu-id="7c95d-140">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="7c95d-140">\#define</span></span>                 | <span data-ttu-id="7c95d-141">Wert</span><span class="sxs-lookup"><span data-stu-id="7c95d-141">Value</span></span> | <span data-ttu-id="7c95d-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c95d-142">Description</span></span>                    |
|--------------------------|-------|--------------------------------|
| <span data-ttu-id="7c95d-143">D3DXF \_ FILESAVE \_ TOFILE</span><span class="sxs-lookup"><span data-stu-id="7c95d-143">D3DXF\_FILESAVE\_TOFILE</span></span>  | <span data-ttu-id="7c95d-144">0</span><span class="sxs-lookup"><span data-stu-id="7c95d-144">0</span></span>     | <span data-ttu-id="7c95d-145">Speichern sie in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="7c95d-145">Save to a file.</span></span>                |
| <span data-ttu-id="7c95d-146">D3DXF \_ FILESAVE \_ TOWFILE</span><span class="sxs-lookup"><span data-stu-id="7c95d-146">D3DXF\_FILESAVE\_TOWFILE</span></span> | <span data-ttu-id="7c95d-147">1</span><span class="sxs-lookup"><span data-stu-id="7c95d-147">1</span></span>     | <span data-ttu-id="7c95d-148">Speichern Sie in einer Breitzeichendatei.</span><span class="sxs-lookup"><span data-stu-id="7c95d-148">Save to a wide-character file.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="7c95d-149">Konstanteninformationen</span><span class="sxs-lookup"><span data-stu-id="7c95d-149">Constant Information</span></span>



| <span data-ttu-id="7c95d-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c95d-150">Requirement</span></span>                         | <span data-ttu-id="7c95d-151">Wert</span><span class="sxs-lookup"><span data-stu-id="7c95d-151">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="7c95d-152">Header</span><span class="sxs-lookup"><span data-stu-id="7c95d-152">Header</span></span>                   | <span data-ttu-id="7c95d-153">d3dx9xof.h</span><span class="sxs-lookup"><span data-stu-id="7c95d-153">d3dx9xof.h</span></span> |
| <span data-ttu-id="7c95d-154">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="7c95d-154">Minimum operating system</span></span> | <span data-ttu-id="7c95d-155">Windows 98</span><span class="sxs-lookup"><span data-stu-id="7c95d-155">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7c95d-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7c95d-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c95d-157">D3DX X-Dateikonstanten</span><span class="sxs-lookup"><span data-stu-id="7c95d-157">D3DX X File Constants</span></span>](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[<span data-ttu-id="7c95d-158">**D3DXSaveMeshToX**</span><span class="sxs-lookup"><span data-stu-id="7c95d-158">**D3DXSaveMeshToX**</span></span>](d3dxsavemeshtox.md)
</dt> </dl>

 

 



