---
title: WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX Struktur (wmdrmsdk. h)
description: Die WMDRM-unterschiedlichen \_ analogen \_ Video \_ Einschränkungen \_ in der Struktur enthalten erweiterte Informationen zu einer Einschränkung für die Wiedergabe von Inhalten als analoges Video.
ms.assetid: fe9092fe-a717-4377-9653-1cc07795319f
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59c9ca5f58cf2adadeb5a6a0618457472cde976c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364650"
---
# <a name="wmdrm_analog_video_restrictions_ex-structure"></a><span data-ttu-id="3a63b-105">WMDRM \_ - \_ Einschränkungen für analoge Videos Ex- \_ \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="3a63b-105">WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX structure</span></span>

<span data-ttu-id="3a63b-106">Die **WMDRM-unterschiedlichen \_ analogen \_ Video \_ Einschränkungen \_** in der Struktur enthalten erweiterte Informationen zu einer Einschränkung für die Wiedergabe von Inhalten als analoges Video.</span><span class="sxs-lookup"><span data-stu-id="3a63b-106">The **WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX** structure holds extended information about a restriction for playing back content as analog video.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a63b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a63b-107">Syntax</span></span>


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS_EX {
  DWORD dwVersion;
  GUID  guidRestrictionID;
  DWORD cbRestrictionData;
  BYTE  *pbRestrictionData;
} ;
```



## <a name="members"></a><span data-ttu-id="3a63b-108">Member</span><span class="sxs-lookup"><span data-stu-id="3a63b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3a63b-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="3a63b-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="3a63b-110">Versionsnummer:</span><span class="sxs-lookup"><span data-stu-id="3a63b-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="3a63b-111">**guidrestrictionid**</span><span class="sxs-lookup"><span data-stu-id="3a63b-111">**guidRestrictionID**</span></span>
</dt> <dd>

<span data-ttu-id="3a63b-112">Einschränkungs-ID.</span><span class="sxs-lookup"><span data-stu-id="3a63b-112">Restriction ID.</span></span>

</dd> <dt>

<span data-ttu-id="3a63b-113">**cbrestrictiondata**</span><span class="sxs-lookup"><span data-stu-id="3a63b-113">**cbRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="3a63b-114">Größe der Einschränkungs Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3a63b-114">Size of restriction data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3a63b-115">**pbrestrictiondata**</span><span class="sxs-lookup"><span data-stu-id="3a63b-115">**pbRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="3a63b-116">Einschränkungs Daten.</span><span class="sxs-lookup"><span data-stu-id="3a63b-116">Restriction data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a63b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a63b-117">Remarks</span></span>

<span data-ttu-id="3a63b-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="3a63b-118">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a63b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a63b-119">Requirements</span></span>



| <span data-ttu-id="3a63b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a63b-120">Requirement</span></span> | <span data-ttu-id="3a63b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3a63b-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a63b-122">Header</span><span class="sxs-lookup"><span data-stu-id="3a63b-122">Header</span></span><br/> | <dl> <span data-ttu-id="3a63b-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a63b-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a63b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a63b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a63b-125">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="3a63b-125">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="3a63b-126">**\_Einschränkungen für analoge \_ Videos \_ in WMDRM**</span><span class="sxs-lookup"><span data-stu-id="3a63b-126">**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS**</span></span>](wmdrm-analog-video-restrictions.md)
</dt> </dl>

 

 





