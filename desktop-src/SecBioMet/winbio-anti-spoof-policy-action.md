---
title: WINBIO_ANTI_SPOOF_POLICY_ACTION-Enumeration (winbio \_ types. h)
description: Gibt die Typen von Aktionen an, die Sie für die Antispoofing-Richtlinie eines Benutzers durchführen.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- WINBIO_ANTI_SPOOF_POLICY_ACTION Enumeration Windows-Biometrieframework-API
- PWINBIO_ANTI_SPOOF_POLICY enumerationszeiger Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY_ACTION
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5905624bad252475cdde12c003f31a734e64dd2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956691"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a><span data-ttu-id="20651-105">\_ \_ \_ Aktions Enumeration für winbio Anti Spoof-Richtlinie \_</span><span class="sxs-lookup"><span data-stu-id="20651-105">WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION enumeration</span></span>

<span data-ttu-id="20651-106">Gibt die Typen von Aktionen an, die Sie für die Antispoofing-Richtlinie eines Benutzers durchführen.</span><span class="sxs-lookup"><span data-stu-id="20651-106">Specifies the types of actions you take for the antispoofing policy of a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="20651-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="20651-107">Syntax</span></span>


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a><span data-ttu-id="20651-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="20651-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="20651-109"><span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**winbio \_ - \_ antispoof \_ Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="20651-109"><span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO\_ANTI\_SPOOF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="20651-110">Deaktiviert die Erkennung des Spoofing für einen biometrischen Faktor.</span><span class="sxs-lookup"><span data-stu-id="20651-110">Turns off the detection of spoofing for a biometric factor.</span></span>

</dd> <dt>

<span data-ttu-id="20651-111"><span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**winbio \_ - \_ antispoof \_ aktivieren**</span><span class="sxs-lookup"><span data-stu-id="20651-111"><span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO\_ANTI\_SPOOF\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="20651-112">Schaltet die Erkennung von Spoofing für einen biometrischen Faktor ein.</span><span class="sxs-lookup"><span data-stu-id="20651-112">Turns on the detection of spoofing for a biometric factor.</span></span>

</dd> <dt>

<span data-ttu-id="20651-113"><span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**winbio \_ Anti \_ Spoof \_ Entfernen**</span><span class="sxs-lookup"><span data-stu-id="20651-113"><span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**WINBIO\_ANTI\_SPOOF\_REMOVE**</span></span>
</dt> <dd>

<span data-ttu-id="20651-114">Entfernt die gesamte Antispoofing-Richtlinie für den biometrischen Faktor aus dem Konto.</span><span class="sxs-lookup"><span data-stu-id="20651-114">Removes the entire antispoofing policy for the biometric factor from the account.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20651-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20651-115">Requirements</span></span>



| <span data-ttu-id="20651-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20651-116">Requirement</span></span> | <span data-ttu-id="20651-117">Wert</span><span class="sxs-lookup"><span data-stu-id="20651-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20651-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20651-118">Minimum supported client</span></span><br/> | <span data-ttu-id="20651-119">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20651-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="20651-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20651-120">Minimum supported server</span></span><br/> | <span data-ttu-id="20651-121">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20651-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="20651-122">Header</span><span class="sxs-lookup"><span data-stu-id="20651-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="20651-123"><dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="20651-123"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20651-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20651-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20651-125">**Aktion für winbio- \_ \_ antispoof- \_ Richtlinie \_**</span><span class="sxs-lookup"><span data-stu-id="20651-125">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[<span data-ttu-id="20651-126">**Quelle der winbio- \_ Richtlinie \_**</span><span class="sxs-lookup"><span data-stu-id="20651-126">**WINBIO\_POLICY\_SOURCE**</span></span>](winbio-policy-source.md)
</dt> </dl>

 

 





