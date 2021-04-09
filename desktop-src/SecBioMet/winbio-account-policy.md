---
title: WINBIO_ACCOUNT_POLICY Struktur (winbio \_ Adapter. h)
description: Enthält entweder eine Standard-oder eine kontospezifische Antispoofing-Richtlinie.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- WINBIO_ACCOUNT_POLICY Struktur Windows-Biometrieframework-API
- PWINBIO_ACCOUNT_POLICY Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_ACCOUNT_POLICY
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c734fa6d98615b7708a65ebad1dddc47cdc77cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956463"
---
# <a name="winbio_account_policy-structure"></a><span data-ttu-id="bd0de-105">Struktur der winbio- \_ Konto \_ Richtlinien</span><span class="sxs-lookup"><span data-stu-id="bd0de-105">WINBIO\_ACCOUNT\_POLICY structure</span></span>

<span data-ttu-id="bd0de-106">Die Struktur der **winbio- \_ Konto \_ Richtlinien** enthält entweder eine Standard-oder eine kontospezifische antispoofinganchtlinie.</span><span class="sxs-lookup"><span data-stu-id="bd0de-106">The **WINBIO\_ACCOUNT\_POLICY** structure contains either a default or account-specific antispoofing policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd0de-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd0de-107">Syntax</span></span>


```C++
typedef struct _WINBIO_ACCOUNT_POLICY {
  WINBIO_IDENTITY                 Identity;
  WINBIO_ANTI_SPOOF_POLICY_ACTION AntiSpoofBehavior;
} WINBIO_ACCOUNT_POLICY, *PWINBIO_ACCOUNT_POLICY;
```



## <a name="members"></a><span data-ttu-id="bd0de-108">Member</span><span class="sxs-lookup"><span data-stu-id="bd0de-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bd0de-109">**Identität**</span><span class="sxs-lookup"><span data-stu-id="bd0de-109">**Identity**</span></span>
</dt> <dd>

<span data-ttu-id="bd0de-110">Eine [**winbio- \_ Identitäts**](winbio-identity.md) Struktur, die die Kontoinformationen angibt.</span><span class="sxs-lookup"><span data-stu-id="bd0de-110">A [**WINBIO\_IDENTITY**](winbio-identity.md) structure that specifies the account information.</span></span>

</dd> <dt>

<span data-ttu-id="bd0de-111">**Antispoofverhalten**</span><span class="sxs-lookup"><span data-stu-id="bd0de-111">**AntiSpoofBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="bd0de-112">Einer der [**winbio \_ Anti \_ Spoof \_ Policy \_ Action**](winbio-anti-spoof-policy-action.md) -Enumerationswerte, der angibt, welche Aktion für Antispoofing-Richtlinien für das Konto verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd0de-112">One of the [**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**](winbio-anti-spoof-policy-action.md) enumeration values that specifies what antispoofing policy action to use for the account.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd0de-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd0de-113">Remarks</span></span>

<span data-ttu-id="bd0de-114">Eine Beschreibung der Verwendung dieser Struktur finden Sie in der Beschreibung der [**engineadaptersetaccountpolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bd0de-114">See the discussion of the [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) method for a description of how this structure is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd0de-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd0de-115">Requirements</span></span>



| <span data-ttu-id="bd0de-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd0de-116">Requirement</span></span> | <span data-ttu-id="bd0de-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bd0de-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd0de-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd0de-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bd0de-119">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd0de-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="bd0de-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd0de-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bd0de-121">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd0de-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="bd0de-122">Header</span><span class="sxs-lookup"><span data-stu-id="bd0de-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd0de-123"><dt>Winbio \_ Adapter. h (Include winbio \_ Adapter. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd0de-123"><dt>Winbio\_adapter.h (include Winbio\_adapter.h)</dt></span></span> </dl> |



 

 





