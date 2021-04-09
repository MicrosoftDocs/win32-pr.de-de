---
description: Stellt eine Beschreibung eines Textur Formats dar.
MS-HAID: vspixengine.PixEngineTextureFormatDesc
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixenginetextureformatdebug-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 685DC746-544D-4ACB-AB1F-9FA62C5CF416
api_name:
- PixEngineTextureFormatDesc
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 960186f0c28be88805c1df65f1a517c4ce4a4c64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957965"
---
# <a name="span-idvspixenginepixenginetextureformatdescspanpixenginetextureformatdesc-structure"></a><span data-ttu-id="ffba8-103"><span id="vspixengine.pixenginetextureformatdesc"></span>Pixenginetextureformatdebug-Struktur</span><span class="sxs-lookup"><span data-stu-id="ffba8-103"><span id="vspixengine.pixenginetextureformatdesc"></span>PixEngineTextureFormatDesc structure</span></span>

<span data-ttu-id="ffba8-104">Stellt eine Beschreibung eines Textur Formats dar.</span><span class="sxs-lookup"><span data-stu-id="ffba8-104">Represents a description of a texture format.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffba8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffba8-105">Syntax</span></span>


```C++
} PixEngineTextureFormatDesc;
```

## <a name="members"></a><span data-ttu-id="ffba8-106">Member</span><span class="sxs-lookup"><span data-stu-id="ffba8-106">Members</span></span>

<span data-ttu-id="ffba8-107">**dxgiformat**</span><span class="sxs-lookup"><span data-stu-id="ffba8-107">**dxgiFormat**</span></span>  
<span data-ttu-id="ffba8-108">Das DXGI-Format der Textur.</span><span class="sxs-lookup"><span data-stu-id="ffba8-108">The DXGI format of the texture.</span></span>

<span data-ttu-id="ffba8-109">**DataFormat**</span><span class="sxs-lookup"><span data-stu-id="ffba8-109">**dataFormat**</span></span>  
<span data-ttu-id="ffba8-110">Das Datenformat der Textur.</span><span class="sxs-lookup"><span data-stu-id="ffba8-110">The data format of the texture.</span></span>

<span data-ttu-id="ffba8-111">**blockbytes**</span><span class="sxs-lookup"><span data-stu-id="ffba8-111">**blockBytes**</span></span>  
<span data-ttu-id="ffba8-112">Die Anzahl von Bytes in einem Datenblock.</span><span class="sxs-lookup"><span data-stu-id="ffba8-112">The number of bytes in a data block.</span></span>

<span data-ttu-id="ffba8-113">**blockheight**</span><span class="sxs-lookup"><span data-stu-id="ffba8-113">**blockHeight**</span></span>  
<span data-ttu-id="ffba8-114">Die Höhe (Number Samples in der Y-Achse) des Blocks.</span><span class="sxs-lookup"><span data-stu-id="ffba8-114">The height (number samples in the Y axis) of the block.</span></span>

<span data-ttu-id="ffba8-115">**blockWidth**</span><span class="sxs-lookup"><span data-stu-id="ffba8-115">**blockWidth**</span></span>  
<span data-ttu-id="ffba8-116">Die Breite (Anzahl der Stichproben in der X-Achse) des Blocks.</span><span class="sxs-lookup"><span data-stu-id="ffba8-116">The width (number of samples in the X axis) of the block.</span></span>

<span data-ttu-id="ffba8-117">**channelx**</span><span class="sxs-lookup"><span data-stu-id="ffba8-117">**channelX**</span></span>  
<span data-ttu-id="ffba8-118">Beschreibt die Eigenschaften des X-Kanals.</span><span class="sxs-lookup"><span data-stu-id="ffba8-118">Describes properties of the X channel.</span></span> <span data-ttu-id="ffba8-119">Weitere Informationen finden Sie in der pixenginechanneldescription-Struktur.</span><span class="sxs-lookup"><span data-stu-id="ffba8-119">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="ffba8-120">**channelely**</span><span class="sxs-lookup"><span data-stu-id="ffba8-120">**channelY**</span></span>  
<span data-ttu-id="ffba8-121">Beschreibt die Eigenschaften des Y-Kanals.</span><span class="sxs-lookup"><span data-stu-id="ffba8-121">Describes properties of the Y channel.</span></span> <span data-ttu-id="ffba8-122">Weitere Informationen finden Sie in der pixenginechanneldescription-Struktur.</span><span class="sxs-lookup"><span data-stu-id="ffba8-122">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="ffba8-123">**channelz**</span><span class="sxs-lookup"><span data-stu-id="ffba8-123">**channelZ**</span></span>  
<span data-ttu-id="ffba8-124">Beschreibt die Eigenschaften des Z-Kanals.</span><span class="sxs-lookup"><span data-stu-id="ffba8-124">Describes properties of the Z channel.</span></span> <span data-ttu-id="ffba8-125">Weitere Informationen finden Sie in der pixenginechanneldescription-Struktur.</span><span class="sxs-lookup"><span data-stu-id="ffba8-125">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="ffba8-126">**channelw**</span><span class="sxs-lookup"><span data-stu-id="ffba8-126">**channelW**</span></span>  
<span data-ttu-id="ffba8-127">Beschreibt die Eigenschaften des W-Kanals.</span><span class="sxs-lookup"><span data-stu-id="ffba8-127">Describes properties of the W channel.</span></span> <span data-ttu-id="ffba8-128">Weitere Informationen finden Sie in der pixenginechanneldescription-Struktur.</span><span class="sxs-lookup"><span data-stu-id="ffba8-128">For more information, see the PixEngineChannelDescription structure.</span></span>

<span data-ttu-id="ffba8-129">**Swizzle**</span><span class="sxs-lookup"><span data-stu-id="ffba8-129">**swizzle**</span></span>  
<span data-ttu-id="ffba8-130">Beschreibt das auf das Beispiel angewendete Swizzle (Channel-Swap).</span><span class="sxs-lookup"><span data-stu-id="ffba8-130">Describes the swizzle (channel-swapping) applied to the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffba8-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffba8-131">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ffba8-132">Header</span><span class="sxs-lookup"><span data-stu-id="ffba8-132">Header</span></span></p></td><td><span data-ttu-id="ffba8-133">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ffba8-133">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



