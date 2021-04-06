---
title: MPSTATUS_DATA Struktur (mpclient. h)
description: Enthält Daten über den aktuellen Status einer Komponente des Produkts.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- MPSTATUS_DATA Struktur Funktionen der Legacy-Windows-Umgebung
- PMPSTATUS_DATA Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPSTATUS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5da4ea9c8c51d8ee74d3242e5020df23f758228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742304"
---
# <a name="mpstatus_data-structure"></a><span data-ttu-id="2c26f-105">Mpstatus- \_ Datenstruktur</span><span class="sxs-lookup"><span data-stu-id="2c26f-105">MPSTATUS\_DATA structure</span></span>

<span data-ttu-id="2c26f-106">Enthält Daten über den aktuellen Status einer Komponente des Produkts.</span><span class="sxs-lookup"><span data-stu-id="2c26f-106">Contains data about the current status of a component of the product.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c26f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c26f-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_DATA {
  MPCOMPONENT_ID ComponentID;
  BOOL           fEnable;
  union {
    PMPSTATUS_DATAEX_UNUSED p1;
    PMPSTATUS_DATAEX_UNUSED p2;
    PMPSTATUS_DATAEX_UNUSED p3;
    PMPSTATUS_DATAEX_UNUSED p4;
    PMPSTATUS_DATAEX_UNUSED p5;
    PMPSTATUS_DATAEX_UNUSED p6;
    PMPSTATUS_DATAEX_UNUSED p7;
    PMPSTATUS_DATAEX_UNUSED p8;
    PMPSTATUS_DATAEX_UNUSED p9;
    PMPSTATUS_DATAEX_UNUSED pa;
    PMPSTATUS_DATAEX_UNUSED pb;
  } ComponentStatus;
} MPSTATUS_DATA, *PMPSTATUS_DATA;
```



## <a name="members"></a><span data-ttu-id="2c26f-108">Member</span><span class="sxs-lookup"><span data-stu-id="2c26f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2c26f-109">**ComponentID**</span><span class="sxs-lookup"><span data-stu-id="2c26f-109">**ComponentID**</span></span>
</dt> <dd>

<span data-ttu-id="2c26f-110">Typ: **[ **mpcomponent- \_ ID**](mpcomponent-id.md)**</span><span class="sxs-lookup"><span data-stu-id="2c26f-110">Type: **[**MPCOMPONENT\_ID**](mpcomponent-id.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2c26f-111">Bestimmte Komponenten-ID, für die der Status gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="2c26f-111">Specific component ID for which status is reported.</span></span>

</dd> <dt>

<span data-ttu-id="2c26f-112">**fenckbar**</span><span class="sxs-lookup"><span data-stu-id="2c26f-112">**fEnable**</span></span>
</dt> <dd>

<span data-ttu-id="2c26f-113">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="2c26f-113">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="2c26f-114">Der für die Komponente angeforderte Status.</span><span class="sxs-lookup"><span data-stu-id="2c26f-114">Status requested for the component.</span></span> <span data-ttu-id="2c26f-115">**HRESULT** in den Rückruf Daten bedeutet, dass die Anforderung erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="2c26f-115">**hResult** in the callback data signifies success or failure for the request.</span></span>

</dd> <dt>

<span data-ttu-id="2c26f-116">**Componentstatus**</span><span class="sxs-lookup"><span data-stu-id="2c26f-116">**ComponentStatus**</span></span>
</dt> <dd>

<span data-ttu-id="2c26f-117">Zusätzliche Statusdaten, abhängig vom Wert von " **ComponentID**".</span><span class="sxs-lookup"><span data-stu-id="2c26f-117">Extra status data depending on value of **ComponentID**.</span></span>

> [!Note]  
> <span data-ttu-id="2c26f-118">Führt derzeit zu einem Zeiger auf eine dummystruktur für alle möglichen Werte von " **ComponentID**".</span><span class="sxs-lookup"><span data-stu-id="2c26f-118">Currently results in a pointer to a dummy structure for all possible values of **ComponentID**.</span></span>

 

<dl> <dt>

<span data-ttu-id="2c26f-119">**Parkplatz**</span><span class="sxs-lookup"><span data-stu-id="2c26f-119">**p1**</span></span>
</dt> <dd>

<span data-ttu-id="2c26f-120">Typ: **pmpstatus \_ dataex nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="2c26f-120">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="2c26f-121">Bei **ComponentID**  ==  **mpcomponent \_ als \_ Signatur**.</span><span class="sxs-lookup"><span data-stu-id="2c26f-121">When **ComponentID** == **MPCOMPONENT\_AS\_SIGNATURE**.</span></span> <span data-ttu-id="2c26f-122">Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="2c26f-122">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c26f-123">**P2**</span><span class="sxs-lookup"><span data-stu-id="2c26f-123">**p2**</span></span>
</dt> <dd>

<span data-ttu-id="2c26f-124">Typ: **pmpstatus \_ dataex nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="2c26f-124">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="2c26f-125">Wenn **ComponentID**  ==  **mpcomponent \_ AV- \_ Signatur**.</span><span class="sxs-lookup"><span data-stu-id="2c26f-125">When **ComponentID** == **MPCOMPONENT\_AV\_SIGNATURE**.</span></span> <span data-ttu-id="2c26f-126">Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="2c26f-126">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c26f-127">**P3**</span><span class="sxs-lookup"><span data-stu-id="2c26f-127">**p3**</span></span>
</dt> <dd>

<span data-ttu-id="2c26f-128">Typ: **pmpstatus \_ dataex nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="2c26f-128">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="2c26f-129">Beim Überwachen von " **ComponentID**  ==  **mpcomponent \_ Realtime \_**".</span><span class="sxs-lookup"><span data-stu-id="2c26f-129">When **ComponentID** == **MPCOMPONENT\_REALTIME\_MONITOR**.</span></span> <span data-ttu-id="2c26f-130">Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="2c26f-130">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c26f-131">**P4**</span><span class="sxs-lookup"><span data-stu-id="2c26f-131">**p4**</span></span>
</dt> <dd>

<span data-ttu-id="2c26f-132">Typ: **pmpstatus \_ dataex nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="2c26f-132">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="2c26f-133">Wenn **ComponentID**  ==  **mpcomponent \_ OnAccess \_ Protection**.</span><span class="sxs-lookup"><span data-stu-id="2c26f-133">When **ComponentID** == **MPCOMPONENT\_ONACCESS\_PROTECTION**.</span></span> <span data-ttu-id="2c26f-134">Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="2c26f-134">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c26f-135">**betragen**</span><span class="sxs-lookup"><span data-stu-id="2c26f-135">**p5**</span></span>
</dt> <dd>

<span data-ttu-id="2c26f-136">Typ: **pmpstatus \_ dataex nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="2c26f-136">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="2c26f-137">Wenn **ComponentID**  ==  **mpcomponent \_ ioav- \_ Schutz**.</span><span class="sxs-lookup"><span data-stu-id="2c26f-137">When **ComponentID** == **MPCOMPONENT\_IOAV\_PROTECTION**.</span></span> <span data-ttu-id="2c26f-138">Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="2c26f-138">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c26f-139">**verständigt**</span><span class="sxs-lookup"><span data-stu-id="2c26f-139">**p6**</span></span>
</dt> <dd>

<span data-ttu-id="2c26f-140">Typ: **pmpstatus \_ dataex nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="2c26f-140">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="2c26f-141">Wenn das Verhalten der **ComponentID-**  ==  **mpcomponent- \_ \_ Überwachung** erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2c26f-141">When **ComponentID** == **MPCOMPONENT\_BEHAVIOR\_MONITOR**.</span></span> <span data-ttu-id="2c26f-142">Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="2c26f-142">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c26f-143">**P7**</span><span class="sxs-lookup"><span data-stu-id="2c26f-143">**p7**</span></span>
</dt> <dd>

<span data-ttu-id="2c26f-144">Typ: **pmpstatus \_ dataex nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="2c26f-144">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="2c26f-145">Beim automatischen Scannen von **ComponentID**  ==  **\_ \_ mpcomponent**.</span><span class="sxs-lookup"><span data-stu-id="2c26f-145">When **ComponentID** == **MPCOMPONENT\_AUTO\_SCAN**.</span></span> <span data-ttu-id="2c26f-146">Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="2c26f-146">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c26f-147">**übrig**</span><span class="sxs-lookup"><span data-stu-id="2c26f-147">**p8**</span></span>
</dt> <dd>

<span data-ttu-id="2c26f-148">Typ: **pmpstatus \_ dataex nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="2c26f-148">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="2c26f-149">Wenn **ComponentID**  ==  **mpcomponent \_ automatisch \_ sigupdate**.</span><span class="sxs-lookup"><span data-stu-id="2c26f-149">When **ComponentID** == **MPCOMPONENT\_AUTO\_SIGUPDATE**.</span></span> <span data-ttu-id="2c26f-150">Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="2c26f-150">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c26f-151">**P9**</span><span class="sxs-lookup"><span data-stu-id="2c26f-151">**p9**</span></span>
</dt> <dd>

<span data-ttu-id="2c26f-152">Typ: **pmpstatus \_ dataex nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="2c26f-152">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="2c26f-153">Wenn **ComponentID**  ==  **mpcomponent \_ IPC**.</span><span class="sxs-lookup"><span data-stu-id="2c26f-153">When **ComponentID** == **MPCOMPONENT\_IPC**.</span></span> <span data-ttu-id="2c26f-154">Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="2c26f-154">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c26f-155">**pa**</span><span class="sxs-lookup"><span data-stu-id="2c26f-155">**pa**</span></span>
</dt> <dd>

<span data-ttu-id="2c26f-156">Typ: **pmpstatus \_ dataex nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="2c26f-156">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="2c26f-157">Wenn **ComponentID**  ==  **mpcomponent \_ NIS** ist.</span><span class="sxs-lookup"><span data-stu-id="2c26f-157">When **ComponentID** == **MPCOMPONENT\_NIS**.</span></span> <span data-ttu-id="2c26f-158">Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="2c26f-158">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c26f-159">**PB**</span><span class="sxs-lookup"><span data-stu-id="2c26f-159">**pb**</span></span>
</dt> <dd>

<span data-ttu-id="2c26f-160">Typ: **pmpstatus \_ dataex nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="2c26f-160">Type: **PMPSTATUS\_DATAEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="2c26f-161">Wenn **ComponentID**  ==  **mpcomponent \_ Elam** ist.</span><span class="sxs-lookup"><span data-stu-id="2c26f-161">When **ComponentID** == **MPCOMPONENT\_ELAM**.</span></span> <span data-ttu-id="2c26f-162">Siehe [**mpstatus \_ dataex nicht \_ verwendet**](mpstatus-dataex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="2c26f-162">See [**MPSTATUS\_DATAEX\_UNUSED**](mpstatus-dataex-unused.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c26f-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c26f-163">Requirements</span></span>



| <span data-ttu-id="2c26f-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c26f-164">Requirement</span></span> | <span data-ttu-id="2c26f-165">Wert</span><span class="sxs-lookup"><span data-stu-id="2c26f-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c26f-166">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c26f-166">Minimum supported client</span></span><br/> | <span data-ttu-id="2c26f-167">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c26f-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2c26f-168">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c26f-168">Minimum supported server</span></span><br/> | <span data-ttu-id="2c26f-169">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c26f-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c26f-170">Header</span><span class="sxs-lookup"><span data-stu-id="2c26f-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c26f-171"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c26f-171"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c26f-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c26f-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c26f-173">**mpcomponent- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="2c26f-173">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)
</dt> <dt>

[<span data-ttu-id="2c26f-174">**mpstatus \_ dataex nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="2c26f-174">**MPSTATUS\_DATAEX\_UNUSED**</span></span>](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





