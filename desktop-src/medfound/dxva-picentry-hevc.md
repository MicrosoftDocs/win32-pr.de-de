---
description: Gibt einen Verweis auf eine nicht komprimierte Oberfläche an.
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: DXVA_PicEntry_HEVC-Struktur (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicEntry_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: a2c4856452d0f8010e8f97126b4e660557ea40ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344383"
---
# <a name="dxva_picentry_hevc-structure"></a><span data-ttu-id="ba6af-103">DXVA \_ picentry \_ hevc-Struktur</span><span class="sxs-lookup"><span data-stu-id="ba6af-103">DXVA\_PicEntry\_HEVC structure</span></span>

<span data-ttu-id="ba6af-104">Gibt einen Verweis auf eine nicht komprimierte Oberfläche an.</span><span class="sxs-lookup"><span data-stu-id="ba6af-104">Specifies a reference to an uncompressed surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba6af-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba6af-105">Syntax</span></span>


```C++
typedef struct _DXVA_PicEntry_HEVC {
  union {
    struct {
      UCHAR  Index7Bits  :7;
      UCHAR  AssociatedFlag   :1;
    };
    UCHAR  bPicEntry;
  };
} DXVA_PicEntry_HEVC, *PDXVA_PicEntry_HEVC;
```



## <a name="members"></a><span data-ttu-id="ba6af-106">Member</span><span class="sxs-lookup"><span data-stu-id="ba6af-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ba6af-107">**Index7Bits**</span><span class="sxs-lookup"><span data-stu-id="ba6af-107">**Index7Bits**</span></span>
</dt> <dd>

<span data-ttu-id="ba6af-108">Ein Index, der eine unkomprimierte Oberfläche identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ba6af-108">An index that identifies an uncompressed surface .</span></span>

</dd> <dt>

<span data-ttu-id="ba6af-109">**Associatedflag**</span><span class="sxs-lookup"><span data-stu-id="ba6af-109">**AssociatedFlag**</span></span> 
</dt> <dd>

<span data-ttu-id="ba6af-110">Optionales 1-Bit-Flag, das der Oberfläche zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ba6af-110">Optional 1-bit flag associated with the surface.</span></span> <span data-ttu-id="ba6af-111">Die Bedeutung des Flags hängt vom Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="ba6af-111">The meaning of the flag depends on the context.</span></span> <span data-ttu-id="ba6af-112">Beispielsweise kann festgelegt werden, ob der Verweis Rahmen ein langfristiger Verweis oder ein kurzfristiger Verweis ist.</span><span class="sxs-lookup"><span data-stu-id="ba6af-112">For example, it can specify whether the reference frame is a long-term reference or a short-term reference.</span></span>

</dd> <dt>

<span data-ttu-id="ba6af-113">**bpicentry**</span><span class="sxs-lookup"><span data-stu-id="ba6af-113">**bPicEntry**</span></span>
</dt> <dd>

<span data-ttu-id="ba6af-114">Greift auf die gesamten 8 Bits der Union zu.</span><span class="sxs-lookup"><span data-stu-id="ba6af-114">Accesses the entire 8 bits of the union.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba6af-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba6af-115">Requirements</span></span>



| <span data-ttu-id="ba6af-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba6af-116">Requirement</span></span> | <span data-ttu-id="ba6af-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ba6af-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ba6af-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba6af-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ba6af-119">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="ba6af-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ba6af-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba6af-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ba6af-121">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba6af-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ba6af-122">Header</span><span class="sxs-lookup"><span data-stu-id="ba6af-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba6af-123"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba6af-123"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba6af-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba6af-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba6af-125">Media Foundation Strukturen</span><span class="sxs-lookup"><span data-stu-id="ba6af-125">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




