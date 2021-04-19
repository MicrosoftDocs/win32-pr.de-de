---
description: Konstanten, die die von einem Gerät unterstützten Scheitelpunkt Datentypen beschreiben.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49131fed9961782a6ade3d3ec5f541bb0fe63a50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346639"
---
# <a name="d3ddtcaps"></a><span data-ttu-id="bb1ea-103">D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="bb1ea-103">D3DDTCAPS</span></span>

<span data-ttu-id="bb1ea-104">Konstanten, die die von einem Gerät unterstützten Scheitelpunkt Datentypen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="bb1ea-104">Constants describing the vertex data types supported by a device.</span></span>



|                       |             |                                                                                                                               |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb1ea-105">\#definieren</span><span class="sxs-lookup"><span data-stu-id="bb1ea-105">\#define</span></span>              | <span data-ttu-id="bb1ea-106">Wert</span><span class="sxs-lookup"><span data-stu-id="bb1ea-106">Value</span></span>       | <span data-ttu-id="bb1ea-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb1ea-107">Description</span></span>                                                                                                                   |
| <span data-ttu-id="bb1ea-108">D3DDTCAPS \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="bb1ea-108">D3DDTCAPS\_UBYTE4</span></span>     | <span data-ttu-id="bb1ea-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="bb1ea-109">0x00000001L</span></span> | <span data-ttu-id="bb1ea-110">4D-Byte ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="bb1ea-110">4D unsigned byte.</span></span>                                                                                                             |
| <span data-ttu-id="bb1ea-111">D3DDTCAPS \_ UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="bb1ea-111">D3DDTCAPS\_UBYTE4N</span></span>    | <span data-ttu-id="bb1ea-112">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="bb1ea-112">0x00000002L</span></span> | <span data-ttu-id="bb1ea-113">Normalisiertes, 4D-Byte ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="bb1ea-113">Normalized, 4D unsigned byte.</span></span> <span data-ttu-id="bb1ea-114">Alle vier Bytes werden normalisiert, indem Sie auf 255,0 dividiert werden.</span><span class="sxs-lookup"><span data-stu-id="bb1ea-114">Each of the four bytes is normalized by dividing to 255.0.</span></span>                                      |
| <span data-ttu-id="bb1ea-115">D3DDTCAPS \_ SHORT2N</span><span class="sxs-lookup"><span data-stu-id="bb1ea-115">D3DDTCAPS\_SHORT2N</span></span>    | <span data-ttu-id="bb1ea-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="bb1ea-116">0x00000004L</span></span> | <span data-ttu-id="bb1ea-117">Normalized, 2D signed Short, erweitert auf (erstes Byte/32767.0, zweites Byte/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="bb1ea-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span></span>                                     |
| <span data-ttu-id="bb1ea-118">D3DDTCAPS \_ SHORT4N</span><span class="sxs-lookup"><span data-stu-id="bb1ea-118">D3DDTCAPS\_SHORT4N</span></span>    | <span data-ttu-id="bb1ea-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="bb1ea-119">0x00000008L</span></span> | <span data-ttu-id="bb1ea-120">Normalized, 4D signed Short, erweitert auf (erstes Byte/32767.0, zweites Byte/32767.0, Drittes Byte/32767.0, viertes Byte/32767.0).</span><span class="sxs-lookup"><span data-stu-id="bb1ea-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span></span>  |
| <span data-ttu-id="bb1ea-121">D3DDTCAPS \_ USHORT2N</span><span class="sxs-lookup"><span data-stu-id="bb1ea-121">D3DDTCAPS\_USHORT2N</span></span>   | <span data-ttu-id="bb1ea-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="bb1ea-122">0x00000010L</span></span> | <span data-ttu-id="bb1ea-123">Normalized, 2D Ganzzahl ohne Vorzeichen Short, erweitert auf (First Byte/65535.0, Second Byte/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="bb1ea-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span></span>                                   |
| <span data-ttu-id="bb1ea-124">D3DDTCAPS \_ USHORT4N</span><span class="sxs-lookup"><span data-stu-id="bb1ea-124">D3DDTCAPS\_USHORT4N</span></span>   | <span data-ttu-id="bb1ea-125">0x00000020l</span><span class="sxs-lookup"><span data-stu-id="bb1ea-125">0x00000020L</span></span> | <span data-ttu-id="bb1ea-126">Normalisierte 4D (Ganzzahl ohne Vorzeichen Short), erweitert auf (erstes Byte/65535.0, zweites Byte/65535.0, Drittes Byte/65535.0, viertes Byte/65535.0).</span><span class="sxs-lookup"><span data-stu-id="bb1ea-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span></span> |
| <span data-ttu-id="bb1ea-127">D3DDTCAPS \_ UDEC3</span><span class="sxs-lookup"><span data-stu-id="bb1ea-127">D3DDTCAPS\_UDEC3</span></span>      | <span data-ttu-id="bb1ea-128">0x00000040l</span><span class="sxs-lookup"><span data-stu-id="bb1ea-128">0x00000040L</span></span> | <span data-ttu-id="bb1ea-129">3D-Format ohne Vorzeichen 10 10 10 erweitert auf (Wert, Wert, Wert, 1).</span><span class="sxs-lookup"><span data-stu-id="bb1ea-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span></span>                                                             |
| <span data-ttu-id="bb1ea-130">D3DDTCAPS \_ DEC3N</span><span class="sxs-lookup"><span data-stu-id="bb1ea-130">D3DDTCAPS\_DEC3N</span></span>      | <span data-ttu-id="bb1ea-131">0x00000080l</span><span class="sxs-lookup"><span data-stu-id="bb1ea-131">0x00000080L</span></span> | <span data-ttu-id="bb1ea-132">3D-signiertes 10 10 10-Format normalisiert und erweitert auf (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).</span><span class="sxs-lookup"><span data-stu-id="bb1ea-132">3D signed 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>                           |
| <span data-ttu-id="bb1ea-133">D3DDTCAPS \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="bb1ea-133">D3DDTCAPS\_FLOAT16\_2</span></span> | <span data-ttu-id="bb1ea-134">0x00000100l</span><span class="sxs-lookup"><span data-stu-id="bb1ea-134">0x00000100L</span></span> | <span data-ttu-id="bb1ea-135">2D-16-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="bb1ea-135">2D 16-bit floating point numbers.</span></span>                                                                                             |
| <span data-ttu-id="bb1ea-136">D3DDTCAPS \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="bb1ea-136">D3DDTCAPS\_FLOAT16\_4</span></span> | <span data-ttu-id="bb1ea-137">0x00000200l</span><span class="sxs-lookup"><span data-stu-id="bb1ea-137">0x00000200L</span></span> | <span data-ttu-id="bb1ea-138">4D-16-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="bb1ea-138">4D 16-bit floating point numbers.</span></span>                                                                                             |



 

<span data-ttu-id="bb1ea-139">Diese Konstanten werden vom decltypes-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb1ea-139">These constants are used by the DeclTypes member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="bb1ea-140">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="bb1ea-140">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="bb1ea-141">Header</span><span class="sxs-lookup"><span data-stu-id="bb1ea-141">Header</span></span>                   | <span data-ttu-id="bb1ea-142">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="bb1ea-142">d3d9caps.h</span></span> |
| <span data-ttu-id="bb1ea-143">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="bb1ea-143">Minimum operating system</span></span> | <span data-ttu-id="bb1ea-144">Windows 98</span><span class="sxs-lookup"><span data-stu-id="bb1ea-144">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bb1ea-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb1ea-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb1ea-146">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="bb1ea-146">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



