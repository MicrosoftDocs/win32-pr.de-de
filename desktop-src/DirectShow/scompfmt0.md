---
description: Enthält Formatinformationen für die intelligente Neukomprimierung.
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: SCompFmt0-Struktur (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCompFmt0
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: ad5a5277718e8d414d64a86b9c31739cf576736a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368427"
---
# <a name="scompfmt0-structure"></a><span data-ttu-id="4c88a-103">SCompFmt0-Struktur</span><span class="sxs-lookup"><span data-stu-id="4c88a-103">SCompFmt0 structure</span></span>

> [!Note]  
> <span data-ttu-id="4c88a-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="4c88a-104">\[Deprecated.</span></span> <span data-ttu-id="4c88a-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="4c88a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4c88a-106">Enthält Formatinformationen für die intelligente Neukomprimierung.</span><span class="sxs-lookup"><span data-stu-id="4c88a-106">Contains format information for smart recompression.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c88a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c88a-107">Syntax</span></span>


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a><span data-ttu-id="4c88a-108">Member</span><span class="sxs-lookup"><span data-stu-id="4c88a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4c88a-109">**nformatid**</span><span class="sxs-lookup"><span data-stu-id="4c88a-109">**nFormatId**</span></span>
</dt> <dd>

<span data-ttu-id="4c88a-110">Bleiben muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="4c88a-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4c88a-111">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="4c88a-111">**MediaType**</span></span>
</dt> <dd>

<span data-ttu-id="4c88a-112">[**Am \_ \_Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die das Komprimierungs Format beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4c88a-112">[**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that describes the compression format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c88a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c88a-113">Requirements</span></span>



| <span data-ttu-id="4c88a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c88a-114">Requirement</span></span> | <span data-ttu-id="4c88a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4c88a-115">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c88a-116">Header</span><span class="sxs-lookup"><span data-stu-id="4c88a-116">Header</span></span><br/> | <dl> <span data-ttu-id="4c88a-117"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4c88a-117"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c88a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c88a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c88a-119">**Iamtimelinegroup:: gezmartrecompressformat**</span><span class="sxs-lookup"><span data-stu-id="4c88a-119">**IAMTimelineGroup::GetSmartRecompressFormat**</span></span>](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[<span data-ttu-id="4c88a-120">\**Iamtimelinegroup:: *-martrecompressformat**</span><span class="sxs-lookup"><span data-stu-id="4c88a-120">**IAMTimelineGroup::SetSmartRecompressFormat**</span></span>](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




