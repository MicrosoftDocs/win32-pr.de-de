---
description: Konstanten, die die von einem Gerät unterstützten Scheitelpunktdatentypen beschreiben.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 094ca568554722f4da2606233f4ad2c1e59e892f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999447"
---
# <a name="d3ddtcaps"></a><span data-ttu-id="95465-103">D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="95465-103">D3DDTCAPS</span></span>

<span data-ttu-id="95465-104">Konstanten, die die von einem Gerät unterstützten Scheitelpunktdatentypen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="95465-104">Constants describing the vertex data types supported by a device.</span></span>



| <span data-ttu-id="95465-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="95465-105">\#define</span></span>              | <span data-ttu-id="95465-106">Wert</span><span class="sxs-lookup"><span data-stu-id="95465-106">Value</span></span>       | <span data-ttu-id="95465-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95465-107">Description</span></span>                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95465-108">D3DDTCAPS \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="95465-108">D3DDTCAPS\_UBYTE4</span></span>     | <span data-ttu-id="95465-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="95465-109">0x00000001L</span></span> | <span data-ttu-id="95465-110">4D-Byte ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="95465-110">4D unsigned byte.</span></span>                                                                                                             |
| <span data-ttu-id="95465-111">D3DDTCAPS \_ UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="95465-111">D3DDTCAPS\_UBYTE4N</span></span>    | <span data-ttu-id="95465-112">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="95465-112">0x00000002L</span></span> | <span data-ttu-id="95465-113">Normalisiertes, 4D-Byte ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="95465-113">Normalized, 4D unsigned byte.</span></span> <span data-ttu-id="95465-114">Jedes der vier Bytes wird durch Division in 255,0 normalisiert.</span><span class="sxs-lookup"><span data-stu-id="95465-114">Each of the four bytes is normalized by dividing to 255.0.</span></span>                                      |
| <span data-ttu-id="95465-115">D3DDTCAPS \_ SHORT2N</span><span class="sxs-lookup"><span data-stu-id="95465-115">D3DDTCAPS\_SHORT2N</span></span>    | <span data-ttu-id="95465-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="95465-116">0x00000004L</span></span> | <span data-ttu-id="95465-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="95465-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span></span>                                     |
| <span data-ttu-id="95465-118">D3DDTCAPS \_ SHORT4N</span><span class="sxs-lookup"><span data-stu-id="95465-118">D3DDTCAPS\_SHORT4N</span></span>    | <span data-ttu-id="95465-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="95465-119">0x00000008L</span></span> | <span data-ttu-id="95465-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span><span class="sxs-lookup"><span data-stu-id="95465-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span></span>  |
| <span data-ttu-id="95465-121">D3DDTCAPS \_ USHORT2N</span><span class="sxs-lookup"><span data-stu-id="95465-121">D3DDTCAPS\_USHORT2N</span></span>   | <span data-ttu-id="95465-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="95465-122">0x00000010L</span></span> | <span data-ttu-id="95465-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="95465-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span></span>                                   |
| <span data-ttu-id="95465-124">D3DDTCAPS \_ USHORT4N</span><span class="sxs-lookup"><span data-stu-id="95465-124">D3DDTCAPS\_USHORT4N</span></span>   | <span data-ttu-id="95465-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="95465-125">0x00000020L</span></span> | <span data-ttu-id="95465-126">Normalisiert 4D unsigned short, erweitert auf (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span><span class="sxs-lookup"><span data-stu-id="95465-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span></span> |
| <span data-ttu-id="95465-127">D3DDTCAPS \_ UDEC3</span><span class="sxs-lookup"><span data-stu-id="95465-127">D3DDTCAPS\_UDEC3</span></span>      | <span data-ttu-id="95465-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="95465-128">0x00000040L</span></span> | <span data-ttu-id="95465-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span><span class="sxs-lookup"><span data-stu-id="95465-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span></span>                                                             |
| <span data-ttu-id="95465-130">D3DDTCAPS \_ DEC3N</span><span class="sxs-lookup"><span data-stu-id="95465-130">D3DDTCAPS\_DEC3N</span></span>      | <span data-ttu-id="95465-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="95465-131">0x00000080L</span></span> | <span data-ttu-id="95465-132">3D signiertes 10 10 10-Format normalisiert und erweitert auf (v \[ 0 \] /511.0, v \[ 1 \] /511.0, v \[ 2 \] /511.0, 1).</span><span class="sxs-lookup"><span data-stu-id="95465-132">3D signed 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>                           |
| <span data-ttu-id="95465-133">D3DDTCAPS \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="95465-133">D3DDTCAPS\_FLOAT16\_2</span></span> | <span data-ttu-id="95465-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="95465-134">0x00000100L</span></span> | <span data-ttu-id="95465-135">2D-16-Bit-Gleitkommazahlen.</span><span class="sxs-lookup"><span data-stu-id="95465-135">2D 16-bit floating point numbers.</span></span>                                                                                             |
| <span data-ttu-id="95465-136">D3DDTCAPS \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="95465-136">D3DDTCAPS\_FLOAT16\_4</span></span> | <span data-ttu-id="95465-137">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="95465-137">0x00000200L</span></span> | <span data-ttu-id="95465-138">4D-16-Bit-Gleitkommazahlen.</span><span class="sxs-lookup"><span data-stu-id="95465-138">4D 16-bit floating point numbers.</span></span>                                                                                             |



 

<span data-ttu-id="95465-139">Diese Konstanten werden vom DeclTypes-Member von [**D3DCAPS9 verwendet.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="95465-139">These constants are used by the DeclTypes member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="95465-140">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="95465-140">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="95465-141">Header</span><span class="sxs-lookup"><span data-stu-id="95465-141">Header</span></span>                   | <span data-ttu-id="95465-142">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="95465-142">d3d9caps.h</span></span> |
| <span data-ttu-id="95465-143">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="95465-143">Minimum operating system</span></span> | <span data-ttu-id="95465-144">Windows 98</span><span class="sxs-lookup"><span data-stu-id="95465-144">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="95465-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95465-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95465-146">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="95465-146">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



