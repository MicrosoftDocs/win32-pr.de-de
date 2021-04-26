---
description: Die folgenden Flags werden verwendet, um anzugeben, welche Kanäle in einer Textur verwendet werden sollen. Veraltet.
ms.assetid: 6e421a0a-7e82-4640-a96c-7ec648df970d
title: DXFILE-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42b20ca9934b9a4203e05f477ea8c40853a0a836
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997297"
---
# <a name="dxfile-constants"></a><span data-ttu-id="90d9c-104">DXFILE-Konstanten</span><span class="sxs-lookup"><span data-stu-id="90d9c-104">DXFILE Constants</span></span>

<span data-ttu-id="90d9c-105">Die folgenden Flags werden verwendet, um anzugeben, welche Kanäle in einer Textur verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="90d9c-105">The following flags are used to specify which channels in a texture to operate on.</span></span> <span data-ttu-id="90d9c-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="90d9c-106">Deprecated.</span></span>

## <a name="dxfileformat"></a><span data-ttu-id="90d9c-107">DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="90d9c-107">DXFILEFORMAT</span></span>



| <span data-ttu-id="90d9c-108">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="90d9c-108">\#define</span></span>                 | <span data-ttu-id="90d9c-109">Wert</span><span class="sxs-lookup"><span data-stu-id="90d9c-109">Value</span></span> | <span data-ttu-id="90d9c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90d9c-110">Description</span></span>      |
|--------------------------|-------|------------------|
| <span data-ttu-id="90d9c-111">DXFILEFORMAT \_ BINARY</span><span class="sxs-lookup"><span data-stu-id="90d9c-111">DXFILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="90d9c-112">0</span><span class="sxs-lookup"><span data-stu-id="90d9c-112">0</span></span>     | <span data-ttu-id="90d9c-113">Binärdatei.</span><span class="sxs-lookup"><span data-stu-id="90d9c-113">Binary file.</span></span>     |
| <span data-ttu-id="90d9c-114">DXFILEFORMAT \_ TEXT</span><span class="sxs-lookup"><span data-stu-id="90d9c-114">DXFILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="90d9c-115">1</span><span class="sxs-lookup"><span data-stu-id="90d9c-115">1</span></span>     | <span data-ttu-id="90d9c-116">Textdatei.</span><span class="sxs-lookup"><span data-stu-id="90d9c-116">Text file.</span></span>       |
| <span data-ttu-id="90d9c-117">DXFILEFORMAT \_ COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="90d9c-117">DXFILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="90d9c-118">2</span><span class="sxs-lookup"><span data-stu-id="90d9c-118">2</span></span>     | <span data-ttu-id="90d9c-119">Komprimierte Datei.</span><span class="sxs-lookup"><span data-stu-id="90d9c-119">Compressed file.</span></span> |



 

<span data-ttu-id="90d9c-120">Diese \# Definitionen werden in Dxfile.h deklariert.</span><span class="sxs-lookup"><span data-stu-id="90d9c-120">These \#defines are declared in Dxfile.h.</span></span>

## <a name="dxfileloadoptions"></a><span data-ttu-id="90d9c-121">DXFILELOADOPTIONS</span><span class="sxs-lookup"><span data-stu-id="90d9c-121">DXFILELOADOPTIONS</span></span>



| <span data-ttu-id="90d9c-122">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="90d9c-122">\#define</span></span>                 | <span data-ttu-id="90d9c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="90d9c-123">Value</span></span> | <span data-ttu-id="90d9c-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90d9c-124">Description</span></span>                  |
|--------------------------|-------|------------------------------|
| <span data-ttu-id="90d9c-125">DXFILELOAD \_ FROMFILE</span><span class="sxs-lookup"><span data-stu-id="90d9c-125">DXFILELOAD\_FROMFILE</span></span>     | <span data-ttu-id="90d9c-126">0x00L</span><span class="sxs-lookup"><span data-stu-id="90d9c-126">0x00L</span></span> | <span data-ttu-id="90d9c-127">Laden sie eine Datei aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="90d9c-127">Load a file from a file.</span></span>     |
| <span data-ttu-id="90d9c-128">DXFILELOAD \_ FROMRESOURCE</span><span class="sxs-lookup"><span data-stu-id="90d9c-128">DXFILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="90d9c-129">0x01L</span><span class="sxs-lookup"><span data-stu-id="90d9c-129">0x01L</span></span> | <span data-ttu-id="90d9c-130">Laden sie eine Datei aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="90d9c-130">Load a file from a resource.</span></span> |
| <span data-ttu-id="90d9c-131">DXFILELOAD \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="90d9c-131">DXFILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="90d9c-132">0x02L</span><span class="sxs-lookup"><span data-stu-id="90d9c-132">0x02L</span></span> | <span data-ttu-id="90d9c-133">Laden Sie eine Datei aus dem Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="90d9c-133">Load a file from memory.</span></span>     |
| <span data-ttu-id="90d9c-134">DXFILELOAD \_ FROMSTREAM</span><span class="sxs-lookup"><span data-stu-id="90d9c-134">DXFILELOAD\_FROMSTREAM</span></span>   | <span data-ttu-id="90d9c-135">0x04L</span><span class="sxs-lookup"><span data-stu-id="90d9c-135">0x04L</span></span> | <span data-ttu-id="90d9c-136">Laden sie eine Datei aus einem Stream.</span><span class="sxs-lookup"><span data-stu-id="90d9c-136">Load a file from a stream.</span></span>   |
| <span data-ttu-id="90d9c-137">DXFILELOAD \_ FROMURL</span><span class="sxs-lookup"><span data-stu-id="90d9c-137">DXFILELOAD\_FROMURL</span></span>      | <span data-ttu-id="90d9c-138">0x08L</span><span class="sxs-lookup"><span data-stu-id="90d9c-138">0x08L</span></span> | <span data-ttu-id="90d9c-139">Laden sie eine Datei aus einer URL.</span><span class="sxs-lookup"><span data-stu-id="90d9c-139">Load a file from a URL.</span></span>      |



 

<span data-ttu-id="90d9c-140">Diese \# Definitionen werden in Dxfile.h deklariert.</span><span class="sxs-lookup"><span data-stu-id="90d9c-140">These \#defines are declared in Dxfile.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90d9c-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90d9c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90d9c-142">X-Dateiverweis (Legacy)</span><span class="sxs-lookup"><span data-stu-id="90d9c-142">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



