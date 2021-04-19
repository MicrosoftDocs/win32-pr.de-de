---
description: Die capturefilter-Struktur enthält Erfassungs Filterdaten.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: Capturefilter-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILTER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 129575ba401aed0e78f52695a49139f4143c9c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358563"
---
# <a name="capturefilter-structure"></a><span data-ttu-id="82850-103">Capturefilter-Struktur</span><span class="sxs-lookup"><span data-stu-id="82850-103">CAPTUREFILTER structure</span></span>

<span data-ttu-id="82850-104">Die **capturefilter** -Struktur enthält Erfassungs Filterdaten.</span><span class="sxs-lookup"><span data-stu-id="82850-104">The **CAPTUREFILTER** structure contains capture filter data.</span></span>

## <a name="syntax"></a><span data-ttu-id="82850-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="82850-105">Syntax</span></span>


```C++
typedef struct _CAPTUREFILTER {
  DWORD          FilterFlags;
  LPBYTE         lpSapTable;
  LPWORD         lpEtypeTable;
  WORD           nSaps;
  WORD           nEtypes;
  LPADDRESSTABLE AddressTable;
  EXPRESSION     FilterExpression;
  TRIGGER        Trigger;
  DWORD          nFrameBytesToCopy;
  RESERVED       Reserved;
} CAPTUREFILTER, *LPCAPTUREFILTER;
```



## <a name="members"></a><span data-ttu-id="82850-106">Member</span><span class="sxs-lookup"><span data-stu-id="82850-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="82850-107">**Filterflags**</span><span class="sxs-lookup"><span data-stu-id="82850-107">**FilterFlags**</span></span>
</dt> <dd>

<span data-ttu-id="82850-108">Flags, die den Inhalt des Erfassungs Filters beschreiben.</span><span class="sxs-lookup"><span data-stu-id="82850-108">Flags that describe the contents of the capture filter.</span></span>



| <span data-ttu-id="82850-109">Wert</span><span class="sxs-lookup"><span data-stu-id="82850-109">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="82850-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="82850-110">Meaning</span></span>                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <span data-ttu-id="82850-111"><dt>**Capturefilter \_ Flags \_ enthalten \_ alle \_ SAPS**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="82850-111"><dt>**CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS**</dt> <dt>0x0001</dt></span></span> </dl>       | <span data-ttu-id="82850-112">Schließt alle SAPS als akzeptable Frames ein.</span><span class="sxs-lookup"><span data-stu-id="82850-112">Includes all SAPs as acceptable frames.</span></span><br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <span data-ttu-id="82850-113"><dt>**Capturefilter \_ Flags \_ enthalten \_ alle \_ ETYPEs**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="82850-113"><dt>**CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="82850-114">Alle ETYPEs als akzeptable Frames einschließen.</span><span class="sxs-lookup"><span data-stu-id="82850-114">Include all Etypes as acceptable frames.</span></span><br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <span data-ttu-id="82850-115"><dt>**Capturefilter \_ Flags \_ \_ nur lokal**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="82850-115"><dt>**CAPTUREFILTER\_FLAGS\_LOCAL\_ONLY**</dt> <dt>0x0008</dt></span></span> </dl>                          | <span data-ttu-id="82850-116">Kein P-Modus</span><span class="sxs-lookup"><span data-stu-id="82850-116">No P-mode</span></span><br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <span data-ttu-id="82850-117"><dt>**Capturefilter \_ Flags \_ behalten den \_ Rohdaten**</dt> - <dt>0x0020</dt> bei</span><span class="sxs-lookup"><span data-stu-id="82850-117"><dt>**CAPTUREFILTER\_FLAGS\_KEEP\_RAW**</dt> <dt>0x0020</dt></span></span> </dl>                                | <span data-ttu-id="82850-118">Halten Sie SMT-und TokenRing-Mac-Frames</span><span class="sxs-lookup"><span data-stu-id="82850-118">Keep SMT and token ring MAC frames.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="82850-119">**lpsaptable**</span><span class="sxs-lookup"><span data-stu-id="82850-119">**lpSapTable**</span></span>
</dt> <dd>

<span data-ttu-id="82850-120">Zeiger auf ein Array von SAP-Werten.</span><span class="sxs-lookup"><span data-stu-id="82850-120">Pointer to an array of SAP values.</span></span> <span data-ttu-id="82850-121">Dieser Member gibt die SAP-Werte an, die für die Übergabe an den Treiber gültig sind.</span><span class="sxs-lookup"><span data-stu-id="82850-121">This member indicates the SAP values that are valid to pass to the driver.</span></span> <span data-ttu-id="82850-122">Wenn die capturefilter- \_ Flags \_ \_ alle \_ SAPS enthalten, wird dies zu einer Ausnahmeliste (einschließlich aller SAPS außer diesen).</span><span class="sxs-lookup"><span data-stu-id="82850-122">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS is set, this becomes an exception list (include all SAPS except these).</span></span>

</dd> <dt>

<span data-ttu-id="82850-123">**lpeer typetable**</span><span class="sxs-lookup"><span data-stu-id="82850-123">**lpEtypeTable**</span></span>
</dt> <dd>

<span data-ttu-id="82850-124">Zeiger auf ein Array von ETYPE-Werten.</span><span class="sxs-lookup"><span data-stu-id="82850-124">Pointer to an array of Etype values.</span></span> <span data-ttu-id="82850-125">Dies gibt die ETYPE-Werte an, die für die Übergabe an den Treiber gültig sind.</span><span class="sxs-lookup"><span data-stu-id="82850-125">This indicates those Etype values that are valid to pass to the driver.</span></span> <span data-ttu-id="82850-126">Wenn die capturefilter- \_ Flags \_ \_ alle \_ ETYPEs festgelegt sind, wird dies zu einer Ausnahmeliste (alle ETYPEs mit Ausnahme dieser).</span><span class="sxs-lookup"><span data-stu-id="82850-126">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES is set, this becomes an exception list (include all Etypes except these).</span></span>

</dd> <dt>

<span data-ttu-id="82850-127">**NSAPs**</span><span class="sxs-lookup"><span data-stu-id="82850-127">**nSaps**</span></span>
</dt> <dd>

<span data-ttu-id="82850-128">Anzahl der SAPS in der SAP-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="82850-128">Number of SAPs in the SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="82850-129">**"ntypes"**</span><span class="sxs-lookup"><span data-stu-id="82850-129">**nEtypes**</span></span>
</dt> <dd>

<span data-ttu-id="82850-130">Anzahl der ETYPEs in der ETYPE-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="82850-130">Number of Etypes in the Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="82850-131">**Adresssstable**</span><span class="sxs-lookup"><span data-stu-id="82850-131">**AddressTable**</span></span>
</dt> <dd>

<span data-ttu-id="82850-132">Der Name der Adress Tabelle.</span><span class="sxs-lookup"><span data-stu-id="82850-132">Name of the address table.</span></span>

</dd> <dt>

<span data-ttu-id="82850-133">**Filter Expression**</span><span class="sxs-lookup"><span data-stu-id="82850-133">**FilterExpression**</span></span>
</dt> <dd>

<span data-ttu-id="82850-134">Eine Ausdrucks Struktur.</span><span class="sxs-lookup"><span data-stu-id="82850-134">An EXPRESSION structure.</span></span> <span data-ttu-id="82850-135">Diese enthält den Muster Übereinstimmungs Teil des Erfassungs Filters.</span><span class="sxs-lookup"><span data-stu-id="82850-135">This contains the pattern match portion of the capture filter.</span></span>

</dd> <dt>

<span data-ttu-id="82850-136">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="82850-136">**Trigger**</span></span>
</dt> <dd>

<span data-ttu-id="82850-137">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="82850-137">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="82850-138">**nframebytestokopie**</span><span class="sxs-lookup"><span data-stu-id="82850-138">**nFrameBytesToCopy**</span></span>
</dt> <dd>

<span data-ttu-id="82850-139">Wenn dieser Member nicht 0 ist, gibt er an, wie viele Bytes für jeden empfangenen Frame aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="82850-139">If this member is not 0, then it specifies how many bytes to keep of each frame received.</span></span> <span data-ttu-id="82850-140">Wenn der Wert 0 ist, behalten Sie den gesamten Frame bei.</span><span class="sxs-lookup"><span data-stu-id="82850-140">If it is 0, then keep the whole frame.</span></span>

</dd> <dt>

<span data-ttu-id="82850-141">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="82850-141">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="82850-142">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="82850-142">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82850-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82850-143">Remarks</span></span>

<span data-ttu-id="82850-144">Die Kombination aus Flags, Werten und Ausdrücken bestimmt, welche Frames vom Treiber, der diese Strukturdaten verwendet, übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="82850-144">The combination of flags, values, and expressions determine which frames will be passed by the driver that uses this structure data.</span></span> <span data-ttu-id="82850-145">Weitere Informationen zum Implementieren einer **capturefilter** -Struktur finden Sie unter [Capture Filters](capture-filters.md)(Aufzeichnen von Filtern).</span><span class="sxs-lookup"><span data-stu-id="82850-145">For more information about implementing a **CAPTUREFILTER** structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82850-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82850-146">Requirements</span></span>



| <span data-ttu-id="82850-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82850-147">Requirement</span></span> | <span data-ttu-id="82850-148">Wert</span><span class="sxs-lookup"><span data-stu-id="82850-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="82850-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82850-149">Minimum supported client</span></span><br/> | <span data-ttu-id="82850-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82850-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="82850-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82850-151">Minimum supported server</span></span><br/> | <span data-ttu-id="82850-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82850-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="82850-153">Header</span><span class="sxs-lookup"><span data-stu-id="82850-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="82850-154"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="82850-154"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82850-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82850-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82850-156">Adresssstable</span><span class="sxs-lookup"><span data-stu-id="82850-156">ADDRESSTABLE</span></span>](addresstable.md)
</dt> <dt>

[<span data-ttu-id="82850-157">Adresssspair</span><span class="sxs-lookup"><span data-stu-id="82850-157">ADDRESSPAIR</span></span>](addresspair.md)
</dt> <dt>

[<span data-ttu-id="82850-158">Begriff</span><span class="sxs-lookup"><span data-stu-id="82850-158">EXPRESSION</span></span>](expression.md)
</dt> <dt>

[<span data-ttu-id="82850-159">Andexp</span><span class="sxs-lookup"><span data-stu-id="82850-159">ANDEXP</span></span>](andexp.md)
</dt> <dt>

[<span data-ttu-id="82850-160">Patternmatch</span><span class="sxs-lookup"><span data-stu-id="82850-160">PATTERNMATCH</span></span>](patternmatch.md)
</dt> </dl>

 

 




