---
description: Die patternmatch-Struktur definiert Musterelemente, die zum Auswerten eines Frames verwendet werden.
ms.assetid: 3ad27197-92da-49e5-bb0e-daf54de6c54c
title: Patternmatch-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATTERNMATCH
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 286a331f4baeb1dde79a720385c61606835248f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960022"
---
# <a name="patternmatch-structure"></a><span data-ttu-id="776f6-103">Patternmatch-Struktur</span><span class="sxs-lookup"><span data-stu-id="776f6-103">PATTERNMATCH structure</span></span>

<span data-ttu-id="776f6-104">Die **patternmatch** -Struktur definiert Musterelemente, die zum Auswerten eines Frames verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="776f6-104">The **PATTERNMATCH** structure defines pattern elements used to evaluate a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="776f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="776f6-105">Syntax</span></span>


```C++
typedef struct _PATTERNMATCH {
  DWORD        Flags;
  BYTE         OffsetBasis;
  GENERIC_PORT Port;
  WORD         Offset;
  WORD         Length;
  BYTE         PatternToMatch[MAX_PATTERN_LENGTH];
} PATTERNMATCH, *LPPATTERNMATCH;
```



## <a name="members"></a><span data-ttu-id="776f6-106">Member</span><span class="sxs-lookup"><span data-stu-id="776f6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="776f6-107">**Flags**</span><span class="sxs-lookup"><span data-stu-id="776f6-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="776f6-108">Muster Übereinstimmungs Flags:</span><span class="sxs-lookup"><span data-stu-id="776f6-108">Pattern match flags:</span></span>



| <span data-ttu-id="776f6-109">Wert</span><span class="sxs-lookup"><span data-stu-id="776f6-109">Value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="776f6-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="776f6-110">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="PATTERN_MATCH_FLAGS_NOT"></span><span id="pattern_match_flags_not"></span><dl> <span data-ttu-id="776f6-111"><dt>**Muster \_ Übereinstimmungs \_ Flags \_ nicht**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="776f6-111"><dt>**PATTERN\_MATCH\_FLAGS\_NOT**</dt> <dt>0x00000001</dt></span></span> </dl>                                   | <span data-ttu-id="776f6-112">Wenn festgelegt, behält dieses Flag Frames bei, die das angegebene Muster nicht an der richtigen Stelle haben.</span><span class="sxs-lookup"><span data-stu-id="776f6-112">When set, this flag retains frames that lack the specified pattern in the proper spot.</span></span><br/> |
| <span id="PATTERN_MATCH_FLAGS_PORT_SPECIFIED"></span><span id="pattern_match_flags_port_specified"></span><dl> <span data-ttu-id="776f6-113"><dt>**Muster \_ Port der Übereinstimmungs \_ Flags \_ \_ angegeben**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="776f6-113"><dt>**PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED**</dt> <dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="776f6-114">Sucht einen Wert für die Portnummer.</span><span class="sxs-lookup"><span data-stu-id="776f6-114">Seeks a port number value.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="776f6-115">**Offsetbasis**</span><span class="sxs-lookup"><span data-stu-id="776f6-115">**OffsetBasis**</span></span>
</dt> <dd>

<span data-ttu-id="776f6-116">Typen von Offset, bei denen es sich um einen der folgenden Typen handeln kann:</span><span class="sxs-lookup"><span data-stu-id="776f6-116">Types of offset, which can be one of the following:</span></span>



| <span data-ttu-id="776f6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="776f6-117">Value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="776f6-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="776f6-118">Meaning</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="OFFSET_BASIS_RELATIVE_TO_FRAME"></span><span id="offset_basis_relative_to_frame"></span><dl> <span data-ttu-id="776f6-119"><dt>**Offset- \_ Basis \_ relativ \_ zum \_ Frame**</dt></span><span class="sxs-lookup"><span data-stu-id="776f6-119"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_FRAME**</dt></span></span> </dl>                                         | <span data-ttu-id="776f6-120">Legt einen Offset (in Bytes) relativ zum Start des Frames fest.</span><span class="sxs-lookup"><span data-stu-id="776f6-120">Sets an offset, in bytes, relative to start of the frame.</span></span><br/>                   |
| <span id="OFFSET_BASIS_RELATIVE_TO_EFFECTIVE_PROTOCOL"></span><span id="offset_basis_relative_to_effective_protocol"></span><dl> <span data-ttu-id="776f6-121"><dt>**Offset \_ - \_ Basis \_ in Bezug auf das \_ effektive \_ Protokoll**</dt></span><span class="sxs-lookup"><span data-stu-id="776f6-121"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_EFFECTIVE\_PROTOCOL**</dt></span></span> </dl> | <span data-ttu-id="776f6-122">Legt einen Offset (in Bytes) relativ zum Anfang des Protokolls fest, auf das verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="776f6-122">Sets an offset, in bytes, relative to the start of the referenced protocol.</span></span><br/> |
| <span id="OFFSET_BASIS_RELATIVE_TO_IPX"></span><span id="offset_basis_relative_to_ipx"></span><dl> <span data-ttu-id="776f6-123"><dt>**Offset \_ - \_ Basis \_ in Bezug auf \_ IPX**</dt></span><span class="sxs-lookup"><span data-stu-id="776f6-123"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_IPX**</dt></span></span> </dl>                                               | <span data-ttu-id="776f6-124">Legt einen Offset (in Bytes) nur relativ zu IPX fest.</span><span class="sxs-lookup"><span data-stu-id="776f6-124">Sets an offset, in bytes, only relative to IPX.</span></span><br/>                             |
| <span id="OFFSET_BASIS_RELATIVE_TO_IP"></span><span id="offset_basis_relative_to_ip"></span><dl> <span data-ttu-id="776f6-125"><dt>**Offset \_ \_ -Basis relativ \_ zu \_ IP**</dt></span><span class="sxs-lookup"><span data-stu-id="776f6-125"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_IP**</dt></span></span> </dl>                                                  | <span data-ttu-id="776f6-126">Legt einen Offset (in Bytes) nur relativ zu IP fest.</span><span class="sxs-lookup"><span data-stu-id="776f6-126">Sets an offset, in bytes, only relative to IP.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="776f6-127">**Port**</span><span class="sxs-lookup"><span data-stu-id="776f6-127">**Port**</span></span>
</dt> <dd>

<span data-ttu-id="776f6-128">Der Portwert, falls angegeben.</span><span class="sxs-lookup"><span data-stu-id="776f6-128">Port value, if specified.</span></span>

</dd> <dt>

<span data-ttu-id="776f6-129">**Offset**</span><span class="sxs-lookup"><span data-stu-id="776f6-129">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="776f6-130">Der Offset in Bytes relativ zu **Offsetbasis**.</span><span class="sxs-lookup"><span data-stu-id="776f6-130">The offset, in bytes, relative to the **OffsetBasis**.</span></span>

</dd> <dt>

<span data-ttu-id="776f6-131">**Länge**</span><span class="sxs-lookup"><span data-stu-id="776f6-131">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="776f6-132">Länge des übereinstimmenden Musters.</span><span class="sxs-lookup"><span data-stu-id="776f6-132">Length of the matched pattern.</span></span>

</dd> <dt>

<span data-ttu-id="776f6-133">**Patterntomatch**</span><span class="sxs-lookup"><span data-stu-id="776f6-133">**PatternToMatch**</span></span>
</dt> <dd>

<span data-ttu-id="776f6-134">Das zu Übereinstimmungs Muster.</span><span class="sxs-lookup"><span data-stu-id="776f6-134">Pattern to match.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="776f6-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="776f6-135">Remarks</span></span>

<span data-ttu-id="776f6-136">Diese Struktur wird verwendet, um einen Erfassungs Filter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="776f6-136">This structure is used to construct a capture filter.</span></span> <span data-ttu-id="776f6-137">Weitere Informationen zum Implementieren dieser Struktur finden Sie unter [Erfassungs Filter](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="776f6-137">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

<span data-ttu-id="776f6-138">Ein Erfassungs Filter kann bis zu vier **patternmatch** -Strukturen enthalten.</span><span class="sxs-lookup"><span data-stu-id="776f6-138">A capture filter can contain up to four **PATTERNMATCH** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="776f6-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="776f6-139">Requirements</span></span>



| <span data-ttu-id="776f6-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="776f6-140">Requirement</span></span> | <span data-ttu-id="776f6-141">Wert</span><span class="sxs-lookup"><span data-stu-id="776f6-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="776f6-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="776f6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="776f6-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="776f6-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="776f6-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="776f6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="776f6-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="776f6-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="776f6-146">Header</span><span class="sxs-lookup"><span data-stu-id="776f6-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="776f6-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="776f6-147"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="776f6-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="776f6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="776f6-149">Capturefilter</span><span class="sxs-lookup"><span data-stu-id="776f6-149">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




