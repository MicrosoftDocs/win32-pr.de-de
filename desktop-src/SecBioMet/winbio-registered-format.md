---
title: WINBIO_REGISTERED_FORMAT Struktur (winbio \_ types. h)
description: Gibt ein registriertes Datenformat als Besitzer/Format-Paar an.
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- WINBIO_REGISTERED_FORMAT Struktur Windows-Biometrieframework-API
- PWINBIO_REGISTERED_FORMAT Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f45293fe95627c7dfad4c9c51eb7fa74ad1738c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517807"
---
# <a name="winbio_registered_format-structure"></a><span data-ttu-id="6e63c-105">Winbio- \_ registrierte \_ Format Struktur</span><span class="sxs-lookup"><span data-stu-id="6e63c-105">WINBIO\_REGISTERED\_FORMAT structure</span></span>

<span data-ttu-id="6e63c-106">Die Struktur " **winbio- \_ registrierter \_ Format** " gibt ein registriertes Datenformat als Besitzer/Format-Paar an.</span><span class="sxs-lookup"><span data-stu-id="6e63c-106">The **WINBIO\_REGISTERED\_FORMAT** structure specifies a registered data format as an owner/format pair.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e63c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e63c-107">Syntax</span></span>


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a><span data-ttu-id="6e63c-108">Member</span><span class="sxs-lookup"><span data-stu-id="6e63c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6e63c-109">**Besitzer**</span><span class="sxs-lookup"><span data-stu-id="6e63c-109">**Owner**</span></span>
</dt> <dd>

<span data-ttu-id="6e63c-110">Einen von IBIA (International biometrische Industry Association) zugewiesenen Besitzer Wert.</span><span class="sxs-lookup"><span data-stu-id="6e63c-110">An IBIA (International Biometric Industry Association) assigned owner value.</span></span>

</dd> <dt>

<span data-ttu-id="6e63c-111">**Type**</span><span class="sxs-lookup"><span data-stu-id="6e63c-111">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="6e63c-112">Ein vom Besitzer zugewiesenes Format.</span><span class="sxs-lookup"><span data-stu-id="6e63c-112">An owner assigned format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e63c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e63c-113">Remarks</span></span>

<span data-ttu-id="6e63c-114">Da Windows derzeit nur Fingerabdruckleser unterstützt, sollten die folgenden Werte in der Struktur der im **winbio \_ registrierten \_ Format** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e63c-114">Because Windows currently supports only fingerprint readers, the following values should be used in the **WINBIO\_REGISTERED\_FORMAT** structure.</span></span>



| <span data-ttu-id="6e63c-115">Konstante</span><span class="sxs-lookup"><span data-stu-id="6e63c-115">Constant</span></span>                                    | <span data-ttu-id="6e63c-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6e63c-116">Meaning</span></span>                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e63c-117">Winbio \_ ANSI \_ 381- \_ Format \_ Besitzer</span><span class="sxs-lookup"><span data-stu-id="6e63c-117">WINBIO\_ANSI\_381\_FORMAT\_OWNER</span></span><br/> | <span data-ttu-id="6e63c-118">International Committee for Information Technology Standards (INCITS) Technical Committee M1 (Biometrics).</span><span class="sxs-lookup"><span data-stu-id="6e63c-118">InterNational Committee for Information Technology Standards (INCITS) technical committee M1 (biometrics).</span></span><br/> |
| <span data-ttu-id="6e63c-119">Winbio \_ ANSI \_ 381 \_ - \_ Formattyp</span><span class="sxs-lookup"><span data-stu-id="6e63c-119">WINBIO\_ANSI\_381\_FORMAT\_TYPE</span></span><br/>  | <span data-ttu-id="6e63c-120">ANSI-Datenaustausch (381 fingerbild-basiertes Datenaustauschformat).</span><span class="sxs-lookup"><span data-stu-id="6e63c-120">ANSI INCITS 381 finger image based data interchange format.</span></span><br/>                                                |



 

## <a name="requirements"></a><span data-ttu-id="6e63c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e63c-121">Requirements</span></span>



| <span data-ttu-id="6e63c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e63c-122">Requirement</span></span> | <span data-ttu-id="6e63c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6e63c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e63c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e63c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6e63c-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e63c-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="6e63c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e63c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6e63c-127">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e63c-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6e63c-128">Header</span><span class="sxs-lookup"><span data-stu-id="6e63c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e63c-129"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e63c-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e63c-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e63c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e63c-131">Client Anwendungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="6e63c-131">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="6e63c-132">**Winbio \_ ANSI \_ 381- \_ Format Konstanten**</span><span class="sxs-lookup"><span data-stu-id="6e63c-132">**WINBIO\_ANSI\_381\_FORMAT Constants**</span></span>](winbio-ansi-381-format-constants.md)
</dt> <dt>

[<span data-ttu-id="6e63c-133">**Winbio \_ BDB \_ ANSI \_ 381- \_ Header**</span><span class="sxs-lookup"><span data-stu-id="6e63c-133">**WINBIO\_BDB\_ANSI\_381\_HEADER**</span></span>](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[<span data-ttu-id="6e63c-134">**winbio- \_ Bir- \_ Header**</span><span class="sxs-lookup"><span data-stu-id="6e63c-134">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





