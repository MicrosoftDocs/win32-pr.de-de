---
title: Healthclassvalue-Enumeration (napprotocol. h)
description: Gibt den Wert der Integritäts Klasse TLV an.
ms.assetid: af80c27a-a686-494b-8795-73eb366deaa0
keywords:
- Healthclassvalue-Enumeration NAP
topic_type:
- apiref
api_name:
- HealthClassValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ade44b74d03a69d6ccf410a042adf3819b8cc782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475069"
---
# <a name="healthclassvalue-enumeration"></a><span data-ttu-id="20e2b-104">Healthclassvalue-Enumeration</span><span class="sxs-lookup"><span data-stu-id="20e2b-104">HealthClassValue enumeration</span></span>

> [!Note]  
> <span data-ttu-id="20e2b-105">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="20e2b-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="20e2b-106">Der " **healthclassvalue** "-Enumerationstyp gibt den Wert der Integritäts Klasse "TLV" an.</span><span class="sxs-lookup"><span data-stu-id="20e2b-106">The **HealthClassValue** enumeration type indicates the value of the health class TLV.</span></span>

## <a name="syntax"></a><span data-ttu-id="20e2b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="20e2b-107">Syntax</span></span>


```C++
typedef enum tagHealthClassValue { 
  healthClassFirewall        = 0,
  healthClassPatchLevel      = 1,
  healthClassAntiVirus       = 2,
  healthClassCriticalUpdate  = 3,
  healthClassReserved        = 128
} HealthClassValue;
```



## <a name="constants"></a><span data-ttu-id="20e2b-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="20e2b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="20e2b-109"><span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthclassfirewall**</span><span class="sxs-lookup"><span data-stu-id="20e2b-109"><span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**</span></span>
</dt> <dd>

<span data-ttu-id="20e2b-110">Die Integritäts Klasse TLV ist Firewall.</span><span class="sxs-lookup"><span data-stu-id="20e2b-110">The health class TLV is firewall.</span></span>

</dd> <dt>

<span data-ttu-id="20e2b-111"><span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthclasspatchlevel**</span><span class="sxs-lookup"><span data-stu-id="20e2b-111"><span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**</span></span>
</dt> <dd>

<span data-ttu-id="20e2b-112">Die Integritäts Klasse TLV ist die Patchebene.</span><span class="sxs-lookup"><span data-stu-id="20e2b-112">The health class TLV is patch level.</span></span>

</dd> <dt>

<span data-ttu-id="20e2b-113"><span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthclassantivirus**</span><span class="sxs-lookup"><span data-stu-id="20e2b-113"><span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**</span></span>
</dt> <dd>

<span data-ttu-id="20e2b-114">Die Integritäts Klasse TLV ist Antivirus.</span><span class="sxs-lookup"><span data-stu-id="20e2b-114">The health class TLV is antivirus.</span></span>

</dd> <dt>

<span data-ttu-id="20e2b-115"><span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthclasscriticalupdate**</span><span class="sxs-lookup"><span data-stu-id="20e2b-115"><span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="20e2b-116">Die Integritäts Klasse TLV ist ein kritisches Update.</span><span class="sxs-lookup"><span data-stu-id="20e2b-116">The health class TLV is critical update.</span></span>

</dd> <dt>

<span data-ttu-id="20e2b-117"><span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthclassreserved**</span><span class="sxs-lookup"><span data-stu-id="20e2b-117"><span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**</span></span>
</dt> <dd>

<span data-ttu-id="20e2b-118">Nur für die Verwendung durch das System reserviert.</span><span class="sxs-lookup"><span data-stu-id="20e2b-118">Reserved for system use only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20e2b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20e2b-119">Requirements</span></span>



| <span data-ttu-id="20e2b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20e2b-120">Requirement</span></span> | <span data-ttu-id="20e2b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="20e2b-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="20e2b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20e2b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="20e2b-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20e2b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="20e2b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20e2b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="20e2b-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20e2b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="20e2b-126">Header</span><span class="sxs-lookup"><span data-stu-id="20e2b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="20e2b-127"><dt>Napprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="20e2b-127"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="20e2b-128">IDL</span><span class="sxs-lookup"><span data-stu-id="20e2b-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="20e2b-129"><dt>Napprotocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="20e2b-129"><dt>NapProtocol.idl</dt></span></span> </dl> |



 

 





