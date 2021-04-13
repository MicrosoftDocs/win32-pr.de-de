---
title: WINBIO_POLICY_SOURCE-Enumeration (winbio \_ types. h)
description: Listet die möglichen Quellen der Richtlinien Informationen für die Erkennung von Spoofing für biometrische Faktoren auf.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- WINBIO_POLICY_SOURCE Enumeration Windows-Biometrieframework-API
- PWINBIO_POLICY_SOURCE enumerationszeiger Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866d1d82d939f143c4385caa5d94c68ffe3758f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341267"
---
# <a name="winbio_policy_source-enumeration"></a><span data-ttu-id="f5196-105">Quellenumeration der winbio- \_ Richtlinie \_</span><span class="sxs-lookup"><span data-stu-id="f5196-105">WINBIO\_POLICY\_SOURCE enumeration</span></span>

<span data-ttu-id="f5196-106">Listet die möglichen Quellen der Richtlinien Informationen für die Erkennung von Spoofing für biometrische Faktoren auf.</span><span class="sxs-lookup"><span data-stu-id="f5196-106">Lists the possible sources of policy information for the detection of spoofing for biometric factors.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5196-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5196-107">Syntax</span></span>


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a><span data-ttu-id="f5196-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="f5196-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f5196-109"><span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**winbio- \_ Richtlinie \_ unbekannt**</span><span class="sxs-lookup"><span data-stu-id="f5196-109"><span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**WINBIO\_POLICY\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="f5196-110">Die Quelle der Richtlinie ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="f5196-110">The source of the policy is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="f5196-111"><span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**Standard für winbio- \_ Richtlinie \_**</span><span class="sxs-lookup"><span data-stu-id="f5196-111"><span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**WINBIO\_POLICY\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="f5196-112">Die Richtlinie ist die Standard Richtlinie, die die Windows-Biometrieframework bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f5196-112">The policy is the default policy that the Windows Biometric Framework provides.</span></span>

</dd> <dt>

<span data-ttu-id="f5196-113"><span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**lokale winbio- \_ Richtlinie \_**</span><span class="sxs-lookup"><span data-stu-id="f5196-113"><span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**WINBIO\_POLICY\_LOCAL**</span></span>
</dt> <dd>

<span data-ttu-id="f5196-114">Die Richtlinie, die der jeweilige Benutzer für sein Konto mithilfe der App " **Einstellungen** " festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="f5196-114">The policy that the individual user set for their account by using the **Settings** app.</span></span> <span data-ttu-id="f5196-115">Diese Richtlinie überschreibt die Standard Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="f5196-115">This policy overrides the default policy.</span></span>

</dd> <dt>

<span data-ttu-id="f5196-116"><span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**Administrator der winbio- \_ Richtlinie \_**</span><span class="sxs-lookup"><span data-stu-id="f5196-116"><span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**WINBIO\_POLICY\_ADMIN**</span></span>
</dt> <dd>

<span data-ttu-id="f5196-117">Eine Gruppenrichtlinie, die der IT-Administrator für das Unternehmen festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="f5196-117">A group policy that the IT administrator set for the enterprise.</span></span> <span data-ttu-id="f5196-118">Einzelne Benutzer können diese Richtlinie nicht außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="f5196-118">Individual users cannot override this policy.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5196-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5196-119">Requirements</span></span>



| <span data-ttu-id="f5196-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5196-120">Requirement</span></span> | <span data-ttu-id="f5196-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f5196-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5196-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5196-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f5196-123">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5196-123">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="f5196-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5196-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f5196-125">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5196-125">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="f5196-126">Header</span><span class="sxs-lookup"><span data-stu-id="f5196-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5196-127"><dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="f5196-127"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5196-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5196-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5196-129">**Aktion für winbio- \_ \_ antispoof- \_ Richtlinie \_**</span><span class="sxs-lookup"><span data-stu-id="f5196-129">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





