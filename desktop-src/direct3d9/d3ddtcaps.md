---
description: Konstanten, die die von einem Gerät unterstützten Scheitelpunktdatentypen beschreiben.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ded570b8f451ea7e99050467f70f945d202bd4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343237"
---
# <a name="d3ddtcaps"></a><span data-ttu-id="c8622-103">D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="c8622-103">D3DDTCAPS</span></span>

<span data-ttu-id="c8622-104">Konstanten, die die von einem Gerät unterstützten Scheitelpunktdatentypen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c8622-104">Constants describing the vertex data types supported by a device.</span></span>



| <span data-ttu-id="c8622-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="c8622-105">\#define</span></span>              | <span data-ttu-id="c8622-106">Wert</span><span class="sxs-lookup"><span data-stu-id="c8622-106">Value</span></span>       | <span data-ttu-id="c8622-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8622-107">Description</span></span>                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8622-108">D3DDTCAPS \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="c8622-108">D3DDTCAPS\_UBYTE4</span></span>     | <span data-ttu-id="c8622-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="c8622-109">0x00000001L</span></span> | <span data-ttu-id="c8622-110">4D-Byte ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c8622-110">4D unsigned byte.</span></span>                                                                                                             |
| <span data-ttu-id="c8622-111">D3DDTCAPS \_ UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="c8622-111">D3DDTCAPS\_UBYTE4N</span></span>    | <span data-ttu-id="c8622-112">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="c8622-112">0x00000002L</span></span> | <span data-ttu-id="c8622-113">Normalisiertes, 4D-Byte ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="c8622-113">Normalized, 4D unsigned byte.</span></span> <span data-ttu-id="c8622-114">Jedes der vier Bytes wird durch Division in 255.0 normalisiert.</span><span class="sxs-lookup"><span data-stu-id="c8622-114">Each of the four bytes is normalized by dividing to 255.0.</span></span>                                      |
| <span data-ttu-id="c8622-115">D3DDTCAPS \_ SHORT2N</span><span class="sxs-lookup"><span data-stu-id="c8622-115">D3DDTCAPS\_SHORT2N</span></span>    | <span data-ttu-id="c8622-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="c8622-116">0x00000004L</span></span> | <span data-ttu-id="c8622-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="c8622-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span></span>                                     |
| <span data-ttu-id="c8622-118">D3DDTCAPS \_ SHORT4N</span><span class="sxs-lookup"><span data-stu-id="c8622-118">D3DDTCAPS\_SHORT4N</span></span>    | <span data-ttu-id="c8622-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="c8622-119">0x00000008L</span></span> | <span data-ttu-id="c8622-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span><span class="sxs-lookup"><span data-stu-id="c8622-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span></span>  |
| <span data-ttu-id="c8622-121">D3DDTCAPS \_ USHORT2N</span><span class="sxs-lookup"><span data-stu-id="c8622-121">D3DDTCAPS\_USHORT2N</span></span>   | <span data-ttu-id="c8622-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="c8622-122">0x00000010L</span></span> | <span data-ttu-id="c8622-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="c8622-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span></span>                                   |
| <span data-ttu-id="c8622-124">D3DDTCAPS \_ USHORT4N</span><span class="sxs-lookup"><span data-stu-id="c8622-124">D3DDTCAPS\_USHORT4N</span></span>   | <span data-ttu-id="c8622-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="c8622-125">0x00000020L</span></span> | <span data-ttu-id="c8622-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span><span class="sxs-lookup"><span data-stu-id="c8622-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span></span> |
| <span data-ttu-id="c8622-127">D3DDTCAPS \_ UDEC3</span><span class="sxs-lookup"><span data-stu-id="c8622-127">D3DDTCAPS\_UDEC3</span></span>      | <span data-ttu-id="c8622-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="c8622-128">0x00000040L</span></span> | <span data-ttu-id="c8622-129">Das Format 3D ohne Vorzeichen 10 10 10 wurde auf (Wert, Wert, Wert, 1) erweitert.</span><span class="sxs-lookup"><span data-stu-id="c8622-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span></span>                                                             |
| <span data-ttu-id="c8622-130">D3DDTCAPS \_ DEC3N</span><span class="sxs-lookup"><span data-stu-id="c8622-130">D3DDTCAPS\_DEC3N</span></span>      | <span data-ttu-id="c8622-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="c8622-131">0x00000080L</span></span> | <span data-ttu-id="c8622-132">Das Format 3D mit Vorzeichen 10 10 10 normalisiert und erweitert auf \[ (v0 \] /511.0, v \[ 1 \] /511.0, v \[ 2 \] /511.0, 1).</span><span class="sxs-lookup"><span data-stu-id="c8622-132">3D signed 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>                           |
| <span data-ttu-id="c8622-133">D3DDTCAPS \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="c8622-133">D3DDTCAPS\_FLOAT16\_2</span></span> | <span data-ttu-id="c8622-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="c8622-134">0x00000100L</span></span> | <span data-ttu-id="c8622-135">2D 16-Bit-Gleitkommazahlen.</span><span class="sxs-lookup"><span data-stu-id="c8622-135">2D 16-bit floating point numbers.</span></span>                                                                                             |
| <span data-ttu-id="c8622-136">D3DDTCAPS \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="c8622-136">D3DDTCAPS\_FLOAT16\_4</span></span> | <span data-ttu-id="c8622-137">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="c8622-137">0x00000200L</span></span> | <span data-ttu-id="c8622-138">4D 16-Bit-Gleitkommazahlen.</span><span class="sxs-lookup"><span data-stu-id="c8622-138">4D 16-bit floating point numbers.</span></span>                                                                                             |



 

<span data-ttu-id="c8622-139">Diese Konstanten werden vom DeclTypes-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8622-139">These constants are used by the DeclTypes member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="c8622-140">Konstanteninformationen</span><span class="sxs-lookup"><span data-stu-id="c8622-140">Constant Information</span></span>



|  <span data-ttu-id="c8622-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8622-141">Requirement</span></span>                        | <span data-ttu-id="c8622-142">Wert</span><span class="sxs-lookup"><span data-stu-id="c8622-142">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="c8622-143">Header</span><span class="sxs-lookup"><span data-stu-id="c8622-143">Header</span></span>                   | <span data-ttu-id="c8622-144">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="c8622-144">d3d9caps.h</span></span> |
| <span data-ttu-id="c8622-145">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="c8622-145">Minimum operating system</span></span> | <span data-ttu-id="c8622-146">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c8622-146">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c8622-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c8622-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8622-148">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="c8622-148">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



