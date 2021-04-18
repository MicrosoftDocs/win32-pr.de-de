---
title: DRM_COPY_OPL Struktur (wmdrmsdk. h)
description: Die DRM- \_ Kopier- \_ OPL-Struktur enthält Informationen zu den in einer Lizenz für Kopieraktionen angegebenen Ausgabe Schutz Ebenen (opls).
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- DRM_COPY_OPL Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_COPY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28655e220588bb704567de033e1117dd569d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372182"
---
# <a name="drm_copy_opl-structure"></a><span data-ttu-id="172eb-105">DRM- \_ Kopier- \_ OPL-Struktur</span><span class="sxs-lookup"><span data-stu-id="172eb-105">DRM\_COPY\_OPL structure</span></span>

<span data-ttu-id="172eb-106">Die **DRM- \_ Kopier- \_ OPL** -Struktur enthält Informationen zu den in einer Lizenz für Kopieraktionen angegebenen Ausgabe Schutz Ebenen (opls).</span><span class="sxs-lookup"><span data-stu-id="172eb-106">The **DRM\_COPY\_OPL** structure holds information about the output protection levels (OPLs) specified in a license for copy actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="172eb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="172eb-107">Syntax</span></span>


```C++
typedef struct DRM_COPY_OPL {
  WORD               wMinimumCopyLevel;
  DRM_OPL_OUTPUT_IDS oplIdIncludes;
  DRM_OPL_OUTPUT_IDS oplIdExcludes;
} ;
```



## <a name="members"></a><span data-ttu-id="172eb-108">Member</span><span class="sxs-lookup"><span data-stu-id="172eb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="172eb-109">**wminimumcopylevel**</span><span class="sxs-lookup"><span data-stu-id="172eb-109">**wMinimumCopyLevel**</span></span>
</dt> <dd>

<span data-ttu-id="172eb-110">Minimale OPL für Kopieraktionen.</span><span class="sxs-lookup"><span data-stu-id="172eb-110">Minimum OPL for copy actions.</span></span>

</dd> <dt>

<span data-ttu-id="172eb-111">**oplidincludes**</span><span class="sxs-lookup"><span data-stu-id="172eb-111">**oplIdIncludes**</span></span>
</dt> <dd>

<span data-ttu-id="172eb-112">[**DRM \_ Struktur der OPL- \_ Ausgabe- \_ IDs**](drmdrm-opl-output-ids.md) , die die Bezeichner der zu Zulassungs enden Technologien enthält.</span><span class="sxs-lookup"><span data-stu-id="172eb-112">[**DRM\_OPL\_OUTPUT\_IDS**](drmdrm-opl-output-ids.md) structure containing the identifiers of technologies to allow.</span></span> <span data-ttu-id="172eb-113">Dieser Member wird für Ausgabe Technologien verwendet, denen opls zugewiesen sind, die niedriger als die mindestkopieebene sind, aber auf die der Inhalt kopiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="172eb-113">This member is used for output technologies that are assigned OPLs lower than the minimum copy level, but to which the content may be copied.</span></span>

</dd> <dt>

<span data-ttu-id="172eb-114">**oplidexcludes**</span><span class="sxs-lookup"><span data-stu-id="172eb-114">**oplIdExcludes**</span></span>
</dt> <dd>

<span data-ttu-id="172eb-115">[**DRM \_ Struktur der OPL- \_ Ausgabe- \_ IDs**](drmdrm-opl-output-ids.md) , die die Ausgabe Bezeichner der zu Beschränkungs enden Technologien enthält.</span><span class="sxs-lookup"><span data-stu-id="172eb-115">[**DRM\_OPL\_OUTPUT\_IDS**](drmdrm-opl-output-ids.md) structure containing the output identifiers of technologies to restrict.</span></span> <span data-ttu-id="172eb-116">Dieser Member wird für Ausgabe Technologien verwendet, denen opls zugewiesen sind, die die mindestkopieebene überschreiten, aber dass der Lizenz Aussteller keine Rechte zum Kopieren in erteilt.</span><span class="sxs-lookup"><span data-stu-id="172eb-116">This member is used for output technologies that are assigned OPLs that exceed the minimum copy level, but that the license issuer does not grant rights for copying to.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="172eb-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="172eb-117">Requirements</span></span>



| <span data-ttu-id="172eb-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="172eb-118">Requirement</span></span> | <span data-ttu-id="172eb-119">Wert</span><span class="sxs-lookup"><span data-stu-id="172eb-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="172eb-120">Header</span><span class="sxs-lookup"><span data-stu-id="172eb-120">Header</span></span><br/> | <dl> <span data-ttu-id="172eb-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="172eb-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="172eb-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="172eb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="172eb-123">**DRM- \_ Wiedergabe- \_ OPL**</span><span class="sxs-lookup"><span data-stu-id="172eb-123">**DRM\_PLAY\_OPL**</span></span>](drmdrm-play-opl.md)
</dt> <dt>

[<span data-ttu-id="172eb-124">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="172eb-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





