---
description: Definiert Algorithmen für den Videoprozessor, der von dem MF- \_ Video \_ Prozessor Algorithmus verwendet wird \_ .
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: MF_VIDEO_PROCESSOR_ALGORITHM_TYPE-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
api_type:
- HeaderDef
api_location:
- mfidl.h
ms.openlocfilehash: 604fee61ae4b6a34d876de8c2863ee6dddad73d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345170"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a><span data-ttu-id="6799d-103">\_Typ- \_ \_ \_ Enumeration des MF-Video Prozessors</span><span class="sxs-lookup"><span data-stu-id="6799d-103">MF\_VIDEO\_PROCESSOR\_ALGORITHM\_TYPE enumeration</span></span>

<span data-ttu-id="6799d-104">Definiert Algorithmen für den Videoprozessor, der von dem [MF- \_ Video \_ Prozessor \_ Algorithmus](mf-video-processor-algorithm.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6799d-104">Defines algorithms for the video processor which is use by [MF\_VIDEO\_PROCESSOR\_ALGORITHM](mf-video-processor-algorithm.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6799d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6799d-105">Syntax</span></span>


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a><span data-ttu-id="6799d-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="6799d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6799d-107"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**Standard für den MF- \_ Video \_ Prozessor \_ Algorithmus \_**</span><span class="sxs-lookup"><span data-stu-id="6799d-107"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**MF\_VIDEO\_PROCESSOR\_ALGORITHM\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="6799d-108">der Standardmodus begünstigt eine Ausgewogenheit der Qualität und Geschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="6799d-108">default mode favors a balance of quality and speed</span></span>

</dd> <dt>

<span data-ttu-id="6799d-109"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**MF- \_ Video \_ Prozessor \_ Algorithmus \_ MRF \_ CRF \_ 444**</span><span class="sxs-lookup"><span data-stu-id="6799d-109"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**MF\_VIDEO\_PROCESSOR\_ALGORITHM\_MRF\_CRF\_444**</span></span>
</dt> <dd>

<span data-ttu-id="6799d-110">Der Videoprozessor wird immer intern in ayuv verarbeitet und verwendet hochwertige Filter.</span><span class="sxs-lookup"><span data-stu-id="6799d-110">The video processor will always internally process in AYUV and use high quality filters.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6799d-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6799d-111">Requirements</span></span>



| <span data-ttu-id="6799d-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6799d-112">Requirement</span></span> | <span data-ttu-id="6799d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="6799d-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6799d-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6799d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6799d-115">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="6799d-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6799d-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6799d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6799d-117">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6799d-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6799d-118">IDL</span><span class="sxs-lookup"><span data-stu-id="6799d-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6799d-119"><dt>MFI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6799d-119"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6799d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6799d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6799d-121">Media Foundation Enumerationen</span><span class="sxs-lookup"><span data-stu-id="6799d-121">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




