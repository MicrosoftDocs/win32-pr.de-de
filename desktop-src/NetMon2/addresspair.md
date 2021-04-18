---
description: Die "adresssspair"-Struktur erstellt einen Erfassungs Filter.
ms.assetid: 0dd2bcaa-5e0f-448f-969e-14b923a01a2f
title: Adresssspair-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESSPAIR
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7960a8bb1c3ed1b2fc86c93f371b2f05d299b97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358564"
---
# <a name="addresspair-structure"></a><span data-ttu-id="bddee-103">Adresssspair-Struktur</span><span class="sxs-lookup"><span data-stu-id="bddee-103">ADDRESSPAIR structure</span></span>

<span data-ttu-id="bddee-104">Die " **adresssspair** "-Struktur erstellt einen Erfassungs Filter.</span><span class="sxs-lookup"><span data-stu-id="bddee-104">The **ADDRESSPAIR** structure constructs a capture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="bddee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bddee-105">Syntax</span></span>


```C++
typedef struct _ADDRESSPAIR {
  WORD    AddressFlags;
  WORD    NalReserved;
  ADDRESS DstAddress;
  ADDRESS SrcAddress;
} ADDRESSPAIR, *LPADDRESSPAIR;
```



## <a name="members"></a><span data-ttu-id="bddee-106">Member</span><span class="sxs-lookup"><span data-stu-id="bddee-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bddee-107">**Addressflags**</span><span class="sxs-lookup"><span data-stu-id="bddee-107">**AddressFlags**</span></span>
</dt> <dd>

<span data-ttu-id="bddee-108">Flags, die die von einem Erfassungs Filter verwendeten Adressen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="bddee-108">Flags that describe the addresses used by a capture filter.</span></span> <span data-ttu-id="bddee-109">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="bddee-109">See Remarks for more information.</span></span>



| <span data-ttu-id="bddee-110">Wert</span><span class="sxs-lookup"><span data-stu-id="bddee-110">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="bddee-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bddee-111">Meaning</span></span>                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="ADDRESS_FLAGS_MATCH_DST"></span><span id="address_flags_match_dst"></span><dl> <span data-ttu-id="bddee-112"><dt>**\_adressflags \_ entsprechen " \_ DST"**</dt></span><span class="sxs-lookup"><span data-stu-id="bddee-112"><dt>**ADDRESS\_FLAGS\_MATCH\_DST**</dt></span></span> </dl>                 | <span data-ttu-id="bddee-113">Entspricht der Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="bddee-113">Matches the destination address.</span></span><br/>                              |
| <span id="ADDRESS_FLAGS_MATCH_SRC"></span><span id="address_flags_match_src"></span><dl> <span data-ttu-id="bddee-114"><dt>**\_adressflags \_ entsprechen \_ src**</dt></span><span class="sxs-lookup"><span data-stu-id="bddee-114"><dt>**ADDRESS\_FLAGS\_MATCH\_SRC**</dt></span></span> </dl>                 | <span data-ttu-id="bddee-115">Entspricht der Quelladresse.</span><span class="sxs-lookup"><span data-stu-id="bddee-115">Matches the source address.</span></span><br/>                                   |
| <span id="ADDRESS_FLAGS_EXCLUDED"></span><span id="address_flags_excluded"></span><dl> <span data-ttu-id="bddee-116"><dt>**\_ \_ ausgeschlossene adressflags**</dt></span><span class="sxs-lookup"><span data-stu-id="bddee-116"><dt>**ADDRESS\_FLAGS\_EXCLUDED**</dt></span></span> </dl>                     | <span data-ttu-id="bddee-117">Schließt den Frame aus, wenn diese Adresse gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="bddee-117">Excludes the frame if this address is found.</span></span><br/>                  |
| <span id="ADDRESS_FLAGS_DST_GROUP_ADDR"></span><span id="address_flags_dst_group_addr"></span><dl> <span data-ttu-id="bddee-118"><dt>**\_adressflags \_ DST \_ Group \_ addr**</dt></span><span class="sxs-lookup"><span data-stu-id="bddee-118"><dt>**ADDRESS\_FLAGS\_DST\_GROUP\_ADDR**</dt></span></span> </dl> | <span data-ttu-id="bddee-119">Entspricht nur dem Gruppen Bit.</span><span class="sxs-lookup"><span data-stu-id="bddee-119">Matches group bit only.</span></span> <span data-ttu-id="bddee-120">Verwenden Sie dies für Broadcast-/typnachrichten.</span><span class="sxs-lookup"><span data-stu-id="bddee-120">Use this for broadcast-type messages.</span></span><br/> |
| <span id="ADDRESS_FLAGS_MATCH_BOTH"></span><span id="address_flags_match_both"></span><dl> <span data-ttu-id="bddee-121"><dt>**\_adressflags \_ stimmen mit \_ beiden identisch.**</dt></span><span class="sxs-lookup"><span data-stu-id="bddee-121"><dt>**ADDRESS\_FLAGS\_MATCH\_BOTH**</dt></span></span> </dl>              | <span data-ttu-id="bddee-122">Entspricht den Ziel-und Quelladressen.</span><span class="sxs-lookup"><span data-stu-id="bddee-122">Matches destination and source addresses.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="bddee-123">**Nalreserved**</span><span class="sxs-lookup"><span data-stu-id="bddee-123">**NalReserved**</span></span>
</dt> <dd>

<span data-ttu-id="bddee-124">Dies ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="bddee-124">This is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bddee-125">**Dstaddress**</span><span class="sxs-lookup"><span data-stu-id="bddee-125">**DstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="bddee-126">Die Zieladresse des Adress paar Elements.</span><span class="sxs-lookup"><span data-stu-id="bddee-126">Destination address of the address pair element.</span></span>

</dd> <dt>

<span data-ttu-id="bddee-127">**Srcaddress**</span><span class="sxs-lookup"><span data-stu-id="bddee-127">**SrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="bddee-128">Die Quelladresse des Adress paar Elements.</span><span class="sxs-lookup"><span data-stu-id="bddee-128">Source address of the address pair element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bddee-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bddee-129">Remarks</span></span>

<span data-ttu-id="bddee-130">Die Flags des **addressflags** -Members können kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="bddee-130">The flags of the **AddressFlags** member can be combined.</span></span> <span data-ttu-id="bddee-131">Die folgende Einstellung schließt z. b. den Frame aus, wenn die angegebene Quelladresse erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="bddee-131">For example the following setting excludes the frame if the specified source address is detected.</span></span>

``` syntax
ADDRESS_FLAGS_MATCH_SOURCE|ADDRESS_FLAGS_EXCLUDED
```

<span data-ttu-id="bddee-132">Weitere Informationen zum Implementieren dieser Struktur finden Sie unter [Erfassungs Filter](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="bddee-132">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bddee-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bddee-133">Requirements</span></span>



| <span data-ttu-id="bddee-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bddee-134">Requirement</span></span> | <span data-ttu-id="bddee-135">Wert</span><span class="sxs-lookup"><span data-stu-id="bddee-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bddee-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bddee-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bddee-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bddee-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bddee-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bddee-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bddee-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bddee-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bddee-140">Header</span><span class="sxs-lookup"><span data-stu-id="bddee-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bddee-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bddee-141"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bddee-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bddee-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bddee-143">Capturefilter</span><span class="sxs-lookup"><span data-stu-id="bddee-143">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




