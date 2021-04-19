---
title: DRM_AUDIO_OUTPUT_PROTECTION_IDS Struktur (wmdrmsdk. h)
description: Die Struktur der DRM \_ -audioausgabeschutz- \_ \_ \_ IDs enthält eine Liste der audioausgabeschutzbezeichner.
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3c7142f5f575413f72885aa60a0ccb826ecfab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366876"
---
# <a name="drm_audio_output_protection_ids-structure"></a><span data-ttu-id="b0bcd-105">Struktur der DRM \_ -audioausgabeschutzids \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b0bcd-105">DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS structure</span></span>

<span data-ttu-id="b0bcd-106">Die Struktur der **DRM \_ -audioausgabeschutz- \_ \_ \_ IDs** enthält eine Liste der audioausgabeschutzbezeichner.</span><span class="sxs-lookup"><span data-stu-id="b0bcd-106">The **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS** structure contains a list of audio output protection identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0bcd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0bcd-107">Syntax</span></span>


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a><span data-ttu-id="b0bcd-108">Member</span><span class="sxs-lookup"><span data-stu-id="b0bcd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b0bcd-109">**centries**</span><span class="sxs-lookup"><span data-stu-id="b0bcd-109">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="b0bcd-110">Anzahl der Einträge im **rgaop** -Array.</span><span class="sxs-lookup"><span data-stu-id="b0bcd-110">Number of entries in the **rgAop** array.</span></span>

</dd> <dt>

<span data-ttu-id="b0bcd-111">**rgaop**</span><span class="sxs-lookup"><span data-stu-id="b0bcd-111">**rgAop**</span></span>
</dt> <dd>

<span data-ttu-id="b0bcd-112">Array von **DRM \_ - \_ audioausgabeschutzstrukturen \_** .</span><span class="sxs-lookup"><span data-stu-id="b0bcd-112">Array of **DRM\_AUDIO\_OUTPUT\_PROTECTION** structures.</span></span> <span data-ttu-id="b0bcd-113">**DRM \_ Der \_ audioausgabeschutz \_** ist ein Typ, der als [**DRM- \_ Ausgabe \_ Schutz**](drm-output-protection.md)definiert ist</span><span class="sxs-lookup"><span data-stu-id="b0bcd-113">**DRM\_AUDIO\_OUTPUT\_PROTECTION** is a type defined as [**DRM\_OUTPUT\_PROTECTION**](drm-output-protection.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0bcd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0bcd-114">Remarks</span></span>

<span data-ttu-id="b0bcd-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="b0bcd-115">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0bcd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0bcd-116">Requirements</span></span>



| <span data-ttu-id="b0bcd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0bcd-117">Requirement</span></span> | <span data-ttu-id="b0bcd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b0bcd-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0bcd-119">Header</span><span class="sxs-lookup"><span data-stu-id="b0bcd-119">Header</span></span><br/> | <dl> <span data-ttu-id="b0bcd-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0bcd-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0bcd-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0bcd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0bcd-122">**DRM \_ - \_ audioausgabeschutz- \_ \_ IDs \_ Ex**</span><span class="sxs-lookup"><span data-stu-id="b0bcd-122">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="b0bcd-123">**DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs**</span><span class="sxs-lookup"><span data-stu-id="b0bcd-123">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="b0bcd-124">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="b0bcd-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





