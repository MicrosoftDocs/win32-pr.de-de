---
title: WMDRMNET_POLICY_MINIMUM_ENVIRONMENT Struktur (wmdrmsdk. h)
description: Die minimale Umgebungs Struktur der wmdrmnet- \_ Richtlinie \_ \_ enthält die minimalen Sicherheitsanforderungen für Windows Media DRM für Netzwerkgeräte.
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf53fdec186a44eff375dd2e9cf9badfe0ba715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368663"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a><span data-ttu-id="cd507-105">\_ \_ Minimale \_ Umgebungs Struktur der wmdrmnet-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="cd507-105">WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT structure</span></span>

<span data-ttu-id="cd507-106">Die **\_ \_ minimale \_ Umgebungs Struktur der wmdrmnet-Richtlinie** enthält die minimalen Sicherheitsanforderungen für Windows Media DRM für Netzwerkgeräte.</span><span class="sxs-lookup"><span data-stu-id="cd507-106">The **WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT** structure contains the minimum security requirements for Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd507-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd507-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_MINIMUM_ENVIRONMENT {
  WORD  wMinimumSecurityLevel;
  DWORD dwMinimumAppRevocationListVersion;
  DWORD dwMinimumDeviceRevocationListVersion;
} ;
```



## <a name="members"></a><span data-ttu-id="cd507-108">Member</span><span class="sxs-lookup"><span data-stu-id="cd507-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd507-109">**wminimumsecuritylevel**</span><span class="sxs-lookup"><span data-stu-id="cd507-109">**wMinimumSecurityLevel**</span></span>
</dt> <dd>

<span data-ttu-id="cd507-110">Mindestens erforderliche Anwendungs Sicherheitsstufe.</span><span class="sxs-lookup"><span data-stu-id="cd507-110">Minimum application security level required.</span></span>

</dd> <dt>

<span data-ttu-id="cd507-111">**dwminimumapprevocationlistversion**</span><span class="sxs-lookup"><span data-stu-id="cd507-111">**dwMinimumAppRevocationListVersion**</span></span>
</dt> <dd>

<span data-ttu-id="cd507-112">Mindestens erforderliche Version für die Sperr Liste für das Anwendungs Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="cd507-112">Minimum application certificate revocation list version required.</span></span>

</dd> <dt>

<span data-ttu-id="cd507-113">**dwminimumdevicerevocationlistversion**</span><span class="sxs-lookup"><span data-stu-id="cd507-113">**dwMinimumDeviceRevocationListVersion**</span></span>
</dt> <dd>

<span data-ttu-id="cd507-114">Mindestens erforderliche Sperr Liste für das Gerätezertifikat.</span><span class="sxs-lookup"><span data-stu-id="cd507-114">Minimum device certificate revocation list required.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd507-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd507-115">Remarks</span></span>

<span data-ttu-id="cd507-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="cd507-116">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd507-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd507-117">Requirements</span></span>



| <span data-ttu-id="cd507-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd507-118">Requirement</span></span> | <span data-ttu-id="cd507-119">Wert</span><span class="sxs-lookup"><span data-stu-id="cd507-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd507-120">Header</span><span class="sxs-lookup"><span data-stu-id="cd507-120">Header</span></span><br/> | <dl> <span data-ttu-id="cd507-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd507-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd507-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd507-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd507-123">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="cd507-123">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="cd507-124">**wmdrmnet- \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="cd507-124">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





