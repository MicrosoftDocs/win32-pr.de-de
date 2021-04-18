---
title: DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX Struktur (wmdrmsdk. h)
description: Die- \_ IDs der DRM- \_ audioausgabeschutz- \_ \_ IDs \_ in der Struktur enthalten eine Liste von Schutz Bezeichnungen für den Diese Struktur erweitert DRM \_ - \_ audioausgabeschutz- \_ \_ IDs durch Hinzufügen einer Versionsnummer.
ms.assetid: e650ddeb-5e41-4ff8-b872-40c85ab519c1
keywords:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb687b5600e75f845c2d980f73f3b8c2eeda970a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354764"
---
# <a name="drm_audio_output_protection_ids_ex-structure"></a><span data-ttu-id="6d98a-106">DRM \_ - \_ audioausgabeschutz- \_ \_ IDs \_ Ex-Struktur</span><span class="sxs-lookup"><span data-stu-id="6d98a-106">DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX structure</span></span>

<span data-ttu-id="6d98a-107">Die **- \_ IDs der DRM-audioausgabeschutz- \_ \_ \_ IDs \_** in der Struktur enthalten eine Liste von Schutz Bezeichnungen für den</span><span class="sxs-lookup"><span data-stu-id="6d98a-107">The **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX** structure contains a list of audio output protection identifiers.</span></span> <span data-ttu-id="6d98a-108">Diese Struktur erweitert **DRM \_ - \_ audioausgabeschutz- \_ \_ IDs** durch Hinzufügen einer Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="6d98a-108">This structure extends **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS** by adding a version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d98a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d98a-109">Syntax</span></span>


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION_EX *rgAop;
} ;
```



## <a name="members"></a><span data-ttu-id="6d98a-110">Member</span><span class="sxs-lookup"><span data-stu-id="6d98a-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="6d98a-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="6d98a-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="6d98a-112">Versionsnummer:</span><span class="sxs-lookup"><span data-stu-id="6d98a-112">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="6d98a-113">**centries**</span><span class="sxs-lookup"><span data-stu-id="6d98a-113">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="6d98a-114">Anzahl der Einträge im **rgaop** -Array.</span><span class="sxs-lookup"><span data-stu-id="6d98a-114">Number of entries in the **rgAop** array.</span></span>

</dd> <dt>

<span data-ttu-id="6d98a-115">**rgaop**</span><span class="sxs-lookup"><span data-stu-id="6d98a-115">**rgAop**</span></span>
</dt> <dd>

<span data-ttu-id="6d98a-116">Array von **DRM \_ - \_ audioausgabeschutz \_ \_ -und-** Strukturen.</span><span class="sxs-lookup"><span data-stu-id="6d98a-116">Array of **DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** structures.</span></span> <span data-ttu-id="6d98a-117">**DRM \_ Der \_ \_ \_ audioausgabeschutz** ist ein Typ, der als [**DRM- \_ Ausgabe \_ Schutz \_ Ex**](drm-output-protection-ex.md)definiert ist.</span><span class="sxs-lookup"><span data-stu-id="6d98a-117">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** is a type defined as [**DRM\_OUTPUT\_PROTECTION\_EX**](drm-output-protection-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d98a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d98a-118">Remarks</span></span>

<span data-ttu-id="6d98a-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="6d98a-119">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d98a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d98a-120">Requirements</span></span>



| <span data-ttu-id="6d98a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d98a-121">Requirement</span></span> | <span data-ttu-id="6d98a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6d98a-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d98a-123">Header</span><span class="sxs-lookup"><span data-stu-id="6d98a-123">Header</span></span><br/> | <dl> <span data-ttu-id="6d98a-124"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d98a-124"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d98a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d98a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d98a-126">**DRM \_ - \_ Audioausgabe- \_ Schutz- \_ IDs**</span><span class="sxs-lookup"><span data-stu-id="6d98a-126">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drm-audio-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="6d98a-127">**DRM- \_ Video- \_ Ausgabe Schutz- \_ \_ IDs \_ Ex**</span><span class="sxs-lookup"><span data-stu-id="6d98a-127">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="6d98a-128">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="6d98a-128">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





