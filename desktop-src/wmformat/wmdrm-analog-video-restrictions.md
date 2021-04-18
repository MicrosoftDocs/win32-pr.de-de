---
title: WMDRM_ANALOG_VIDEO_RESTRICTIONS Struktur (wmdrmsdk. h)
description: Die Struktur der analogen WMDRM- \_ \_ Video \_ Einschränkungen enthält Informationen zu einer Einschränkung für die Wiedergabe von Inhalten als analoges Video.
ms.assetid: 13b38115-bd18-45b9-a1d5-542e043a4bde
keywords:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRM_ANALOG_VIDEO_RESTRICTIONS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3d6b8fe957468baebb6da06f45ba7b37756413c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358334"
---
# <a name="wmdrm_analog_video_restrictions-structure"></a><span data-ttu-id="c530f-105">WMDRM \_ - \_ Struktur für analoge Video \_ Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="c530f-105">WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS structure</span></span>

<span data-ttu-id="c530f-106">Die Struktur der **analogen WMDRM- \_ \_ Video \_ Einschränkungen** enthält Informationen zu einer Einschränkung für die Wiedergabe von Inhalten als analoges Video.</span><span class="sxs-lookup"><span data-stu-id="c530f-106">The **WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS** structure holds information about a restriction for playing back content as analog video.</span></span>

## <a name="syntax"></a><span data-ttu-id="c530f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c530f-107">Syntax</span></span>


```C++
typedef struct WMDRM_ANALOG_VIDEO_RESTRICTIONS {
  GUID  guidRestrictionID;
  DWORD dwRestrictionData;
} ;
```



## <a name="members"></a><span data-ttu-id="c530f-108">Member</span><span class="sxs-lookup"><span data-stu-id="c530f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c530f-109">**guidrestrictionid**</span><span class="sxs-lookup"><span data-stu-id="c530f-109">**guidRestrictionID**</span></span>
</dt> <dd>

<span data-ttu-id="c530f-110">Einschränkungs Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c530f-110">Restriction identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c530f-111">**dwrestrictiondata**</span><span class="sxs-lookup"><span data-stu-id="c530f-111">**dwRestrictionData**</span></span>
</dt> <dd>

<span data-ttu-id="c530f-112">Einschränkungs Daten.</span><span class="sxs-lookup"><span data-stu-id="c530f-112">Restriction data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c530f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c530f-113">Remarks</span></span>

<span data-ttu-id="c530f-114">Diese Struktur wird empfangen, wenn Sie [**iwmdrmlicense:: getanalogvideorestrictionlevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c530f-114">This structure is received when you call [**IWMDRMLicense::GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c530f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c530f-115">Requirements</span></span>



| <span data-ttu-id="c530f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c530f-116">Requirement</span></span> | <span data-ttu-id="c530f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c530f-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c530f-118">Header</span><span class="sxs-lookup"><span data-stu-id="c530f-118">Header</span></span><br/> | <dl> <span data-ttu-id="c530f-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c530f-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c530f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c530f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c530f-121">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="c530f-121">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="c530f-122">**Einschränkungen für Analog zum WMDRM- \_ \_ Video \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c530f-122">**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS\_EX**</span></span>](wmdrm-analog-video-restrictions-ex.md)
</dt> </dl>

 

 





