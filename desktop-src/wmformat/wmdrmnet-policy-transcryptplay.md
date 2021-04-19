---
title: WMDRMNET_POLICY_TRANSCRYPTPLAY Struktur (wmdrmsdk. h)
description: Die transryptplay-Struktur der wmdrmnet- \_ Richtlinie \_ enthält die Richtlinien Informationen für die Wiedergabe von Inhalten mithilfe von Windows Media DRM für Netzwerkgeräte.
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- WMDRMNET_POLICY_TRANSCRYPTPLAY Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TRANSCRYPTPLAY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0681251428b87b323c9ad3e73277ec8cdd2b95f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357937"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a><span data-ttu-id="cfbfd-105">\_Transryptplay-Struktur der wmdrmnet-Richtlinie \_</span><span class="sxs-lookup"><span data-stu-id="cfbfd-105">WMDRMNET\_POLICY\_TRANSCRYPTPLAY structure</span></span>

<span data-ttu-id="cfbfd-106">Die **\_ \_ transryptplay-Struktur der wmdrmnet-Richtlinie** enthält die Richtlinien Informationen für die Wiedergabe von Inhalten mithilfe von Windows Media DRM für Netzwerkgeräte.</span><span class="sxs-lookup"><span data-stu-id="cfbfd-106">The **WMDRMNET\_POLICY\_TRANSCRYPTPLAY** structure holds the policy information for playing content using Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfbfd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfbfd-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a><span data-ttu-id="cfbfd-108">Member</span><span class="sxs-lookup"><span data-stu-id="cfbfd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cfbfd-109">**Globals**</span><span class="sxs-lookup"><span data-stu-id="cfbfd-109">**globals**</span></span>
</dt> <dd>

<span data-ttu-id="cfbfd-110">Globale Richtlinien Struktur.</span><span class="sxs-lookup"><span data-stu-id="cfbfd-110">Global policy structure.</span></span>

</dd> <dt>

<span data-ttu-id="cfbfd-111">**playopls**</span><span class="sxs-lookup"><span data-stu-id="cfbfd-111">**playOPLs**</span></span>
</dt> <dd>

<span data-ttu-id="cfbfd-112">Ausgabe Schutz Ebenen für die Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="cfbfd-112">Output protection levels for playback.</span></span> <span data-ttu-id="cfbfd-113">**Wmdrmnet \_ Die Richtlinien \_ Wiedergabe- \_ OPL** ist ein Typ, der als [**DRM \_ Play \_ OPL \_ Ex**](drm-play-opl-ex.md)definiert ist.</span><span class="sxs-lookup"><span data-stu-id="cfbfd-113">**WMDRMNET\_POLICY\_PLAY\_OPL** is a type defined as [**DRM\_PLAY\_OPL\_EX**](drm-play-opl-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cfbfd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfbfd-114">Remarks</span></span>

<span data-ttu-id="cfbfd-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="cfbfd-115">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfbfd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfbfd-116">Requirements</span></span>



| <span data-ttu-id="cfbfd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfbfd-117">Requirement</span></span> | <span data-ttu-id="cfbfd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cfbfd-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbfd-119">Header</span><span class="sxs-lookup"><span data-stu-id="cfbfd-119">Header</span></span><br/> | <dl> <span data-ttu-id="cfbfd-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfbfd-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfbfd-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfbfd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfbfd-122">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="cfbfd-122">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="cfbfd-123">**wmdrmnet- \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="cfbfd-123">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





