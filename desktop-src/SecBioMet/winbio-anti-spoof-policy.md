---
title: WINBIO_ANTI_SPOOF_POLICY Struktur (winbio \_ types. h)
description: Stellt die Richtlinie für Antispoofing für einen Benutzer dar.
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- WINBIO_ANTI_SPOOF_POLICY Struktur Windows-Biometrieframework-API
- PWINBIO_ANTI_SPOOF_POLICY Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3da8b7811afb1de1ad464675125f125ef0ceab73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477499"
---
# <a name="winbio_anti_spoof_policy-structure"></a><span data-ttu-id="c048c-105">Struktur der winbio- \_ \_ antispoof- \_ Richtlinien</span><span class="sxs-lookup"><span data-stu-id="c048c-105">WINBIO\_ANTI\_SPOOF\_POLICY structure</span></span>

<span data-ttu-id="c048c-106">Stellt die Richtlinie für Antispoofing für einen Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="c048c-106">Represents the antispoofing policy for a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="c048c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c048c-107">Syntax</span></span>


```C++
typedef struct _WINBIO_ANTI_SPOOF_POLICY {
  WINBIO_ANTI_SPOOF_POLICY_ACTION Action;
  WINBIO_POLICY_SOURCE            Source;
} WINBIO_ANTI_SPOOF_POLICY, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="members"></a><span data-ttu-id="c048c-108">Member</span><span class="sxs-lookup"><span data-stu-id="c048c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c048c-109">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="c048c-109">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="c048c-110">Der Typ der Aktion, die für die Antispoofing-Richtlinie ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c048c-110">The type of action to take for the antispoofing policy.</span></span>

</dd> <dt>

<span data-ttu-id="c048c-111">**Quelle**</span><span class="sxs-lookup"><span data-stu-id="c048c-111">**Source**</span></span>
</dt> <dd>

<span data-ttu-id="c048c-112">Die Quelle für die Antispoofing-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="c048c-112">The source for the antispoofing policy.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c048c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c048c-113">Requirements</span></span>



| <span data-ttu-id="c048c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c048c-114">Requirement</span></span> | <span data-ttu-id="c048c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c048c-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c048c-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c048c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c048c-117">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c048c-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="c048c-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c048c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c048c-119">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c048c-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="c048c-120">Header</span><span class="sxs-lookup"><span data-stu-id="c048c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c048c-121"><dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="c048c-121"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c048c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c048c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c048c-123">**Aktion für winbio- \_ \_ antispoof- \_ Richtlinie \_**</span><span class="sxs-lookup"><span data-stu-id="c048c-123">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[<span data-ttu-id="c048c-124">**Quelle der winbio- \_ Richtlinie \_**</span><span class="sxs-lookup"><span data-stu-id="c048c-124">**WINBIO\_POLICY\_SOURCE**</span></span>](winbio-policy-source.md)
</dt> <dt>

[<span data-ttu-id="c048c-125">**winbio \_ Async- \_ Ergebnis**</span><span class="sxs-lookup"><span data-stu-id="c048c-125">**WINBIO\_ASYNC\_RESULT**</span></span>](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[<span data-ttu-id="c048c-126">**Winbiogetproperty**</span><span class="sxs-lookup"><span data-stu-id="c048c-126">**WinBioGetProperty**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[<span data-ttu-id="c048c-127">**Winbiosetproperty**</span><span class="sxs-lookup"><span data-stu-id="c048c-127">**WinBioSetProperty**</span></span>](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





