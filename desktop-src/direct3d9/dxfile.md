---
description: Die folgenden Flags werden verwendet, um anzugeben, auf welchen Kanälen in einer Textur gearbeitet werden soll. Veraltet.
ms.assetid: 6e421a0a-7e82-4640-a96c-7ec648df970d
title: Dxfile-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f1651d17f5acb2ef24ff9dae2ef547c3df7c0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041235"
---
# <a name="dxfile-constants"></a><span data-ttu-id="ef03f-104">Dxfile-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ef03f-104">DXFILE Constants</span></span>

<span data-ttu-id="ef03f-105">Die folgenden Flags werden verwendet, um anzugeben, auf welchen Kanälen in einer Textur gearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef03f-105">The following flags are used to specify which channels in a texture to operate on.</span></span> <span data-ttu-id="ef03f-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ef03f-106">Deprecated.</span></span>

## <a name="dxfileformat"></a><span data-ttu-id="ef03f-107">Dxfileformat</span><span class="sxs-lookup"><span data-stu-id="ef03f-107">DXFILEFORMAT</span></span>



|                          |       |                  |
|--------------------------|-------|------------------|
| <span data-ttu-id="ef03f-108">\#definieren</span><span class="sxs-lookup"><span data-stu-id="ef03f-108">\#define</span></span>                 | <span data-ttu-id="ef03f-109">Wert</span><span class="sxs-lookup"><span data-stu-id="ef03f-109">Value</span></span> | <span data-ttu-id="ef03f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef03f-110">Description</span></span>      |
| <span data-ttu-id="ef03f-111">dxfileformat- \_ Binärdatei</span><span class="sxs-lookup"><span data-stu-id="ef03f-111">DXFILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="ef03f-112">0</span><span class="sxs-lookup"><span data-stu-id="ef03f-112">0</span></span>     | <span data-ttu-id="ef03f-113">Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="ef03f-113">Binary file.</span></span>     |
| <span data-ttu-id="ef03f-114">dxfileformat- \_ Text</span><span class="sxs-lookup"><span data-stu-id="ef03f-114">DXFILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="ef03f-115">1</span><span class="sxs-lookup"><span data-stu-id="ef03f-115">1</span></span>     | <span data-ttu-id="ef03f-116">Textdatei.</span><span class="sxs-lookup"><span data-stu-id="ef03f-116">Text file.</span></span>       |
| <span data-ttu-id="ef03f-117">dxfileformat \_ komprimiert</span><span class="sxs-lookup"><span data-stu-id="ef03f-117">DXFILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="ef03f-118">2</span><span class="sxs-lookup"><span data-stu-id="ef03f-118">2</span></span>     | <span data-ttu-id="ef03f-119">Komprimierte Datei.</span><span class="sxs-lookup"><span data-stu-id="ef03f-119">Compressed file.</span></span> |



 

<span data-ttu-id="ef03f-120">Diese \# Definitionen werden in "dxfile. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="ef03f-120">These \#defines are declared in Dxfile.h.</span></span>

## <a name="dxfileloadoptions"></a><span data-ttu-id="ef03f-121">Dxfileloadoption</span><span class="sxs-lookup"><span data-stu-id="ef03f-121">DXFILELOADOPTIONS</span></span>



|                          |       |                              |
|--------------------------|-------|------------------------------|
| <span data-ttu-id="ef03f-122">\#definieren</span><span class="sxs-lookup"><span data-stu-id="ef03f-122">\#define</span></span>                 | <span data-ttu-id="ef03f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ef03f-123">Value</span></span> | <span data-ttu-id="ef03f-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef03f-124">Description</span></span>                  |
| <span data-ttu-id="ef03f-125">dxfileload \_ FromFile</span><span class="sxs-lookup"><span data-stu-id="ef03f-125">DXFILELOAD\_FROMFILE</span></span>     | <span data-ttu-id="ef03f-126">0x00l</span><span class="sxs-lookup"><span data-stu-id="ef03f-126">0x00L</span></span> | <span data-ttu-id="ef03f-127">Lädt eine Datei aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="ef03f-127">Load a file from a file.</span></span>     |
| <span data-ttu-id="ef03f-128">dxfileload \_ FromResource</span><span class="sxs-lookup"><span data-stu-id="ef03f-128">DXFILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="ef03f-129">0x01l</span><span class="sxs-lookup"><span data-stu-id="ef03f-129">0x01L</span></span> | <span data-ttu-id="ef03f-130">Lädt eine Datei aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="ef03f-130">Load a file from a resource.</span></span> |
| <span data-ttu-id="ef03f-131">dxfileload \_ frommemory</span><span class="sxs-lookup"><span data-stu-id="ef03f-131">DXFILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="ef03f-132">0x02l</span><span class="sxs-lookup"><span data-stu-id="ef03f-132">0x02L</span></span> | <span data-ttu-id="ef03f-133">Lädt eine Datei aus dem Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ef03f-133">Load a file from memory.</span></span>     |
| <span data-ttu-id="ef03f-134">dxfileload \_ FromStream</span><span class="sxs-lookup"><span data-stu-id="ef03f-134">DXFILELOAD\_FROMSTREAM</span></span>   | <span data-ttu-id="ef03f-135">0x04l</span><span class="sxs-lookup"><span data-stu-id="ef03f-135">0x04L</span></span> | <span data-ttu-id="ef03f-136">Lädt eine Datei aus einem Stream.</span><span class="sxs-lookup"><span data-stu-id="ef03f-136">Load a file from a stream.</span></span>   |
| <span data-ttu-id="ef03f-137">dxfileload \_ FromUrl</span><span class="sxs-lookup"><span data-stu-id="ef03f-137">DXFILELOAD\_FROMURL</span></span>      | <span data-ttu-id="ef03f-138">0x08l</span><span class="sxs-lookup"><span data-stu-id="ef03f-138">0x08L</span></span> | <span data-ttu-id="ef03f-139">Lädt eine Datei aus einer URL.</span><span class="sxs-lookup"><span data-stu-id="ef03f-139">Load a file from a URL.</span></span>      |



 

<span data-ttu-id="ef03f-140">Diese \# Definitionen werden in "dxfile. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="ef03f-140">These \#defines are declared in Dxfile.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef03f-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef03f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef03f-142">X-Datei Verweis (Legacy)</span><span class="sxs-lookup"><span data-stu-id="ef03f-142">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



