---
description: Flags, die die festzulegenden oder zurück zugegenden Daten einschränken.
title: Srrf (shlwapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c9dbffd1-3b3e-4a25-89ee-1666e2812a62
api_name:
- SRRF_RT_REG_NONE
- SRRF_RT_REG_SZ
- SRRF_RT_REG_EXPAND_SZ
- SRRF_RT_REG_BINARY
- SRRF_RT_REG_DWORD
- SRRF_RT_REG_MULTI_SZ
- SRRF_RT_REG_QWORD
- SRRF_RT_DWORD
- SRRF_RT_QWORD
- SRRF_RT_ANY
- SRRF_RM_ANY
- SRRF_RM_NORMAL
- SRRF_RM_SAFE
- SRRF_RM_SAFENETWORK
- SRRF_NOEXPAND
- SRRF_ZEROONFAILURE
- SRRF_NOVIRT
api_type:
- HeaderDef
api_location:
- Shlwapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3ba36b64496413a54e6d8b8b96c16c265367d05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042416"
---
# <a name="srrf"></a><span data-ttu-id="85f8a-103">Srrf</span><span class="sxs-lookup"><span data-stu-id="85f8a-103">SRRF</span></span>

<span data-ttu-id="85f8a-104">Flags, die die festzulegenden oder zurück zugegenden Daten einschränken.</span><span class="sxs-lookup"><span data-stu-id="85f8a-104">Flags that restrict the data to be set or returned.</span></span>



| <span data-ttu-id="85f8a-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="85f8a-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="85f8a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85f8a-106">Description</span></span>                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SRRF_RT_REG_NONE"></span><span id="srrf_rt_reg_none"></span><dl> <span data-ttu-id="85f8a-107"><dt>**Srrf \_ RT \_ reg \_ None**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-107"><dt>**SRRF\_RT\_REG\_NONE**</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="85f8a-108">Geben Sie reg \_ None ein.</span><span class="sxs-lookup"><span data-stu-id="85f8a-108">Type REG\_NONE.</span></span><br/>                                                                                                                                                                                             |
| <span id="SRRF_RT_REG_SZ"></span><span id="srrf_rt_reg_sz"></span><dl> <span data-ttu-id="85f8a-109"><dt>**Srrf \_ RT \_ reg \_ SZ**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-109"><dt>**SRRF\_RT\_REG\_SZ**</dt> <dt>0x00000002</dt></span></span> </dl>                       | <span data-ttu-id="85f8a-110">Geben Sie reg \_ SZ ein.</span><span class="sxs-lookup"><span data-stu-id="85f8a-110">Type REG\_SZ.</span></span> <span data-ttu-id="85f8a-111">REG-Erweiterungs- \_ \_ SZ-Typen werden automatisch in REG SZ konvertiert, \_ es sei denn, das srrf \_ NOEXPAND-Flag ist angegeben.</span><span class="sxs-lookup"><span data-stu-id="85f8a-111">REG\_EXPAND\_SZ types are automatically converted to REG\_SZ unless the SRRF\_NOEXPAND flag is specified.</span></span><br/>                                                                                     |
| <span id="SRRF_RT_REG_EXPAND_SZ"></span><span id="srrf_rt_reg_expand_sz"></span><dl> <span data-ttu-id="85f8a-112"><dt>**Srrf \_ RT \_ reg \_ Expand \_ SZ**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-112"><dt>**SRRF\_RT\_REG\_EXPAND\_SZ**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="85f8a-113">Typ reg \_ Expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="85f8a-113">Type REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="85f8a-114">Wenn Sie einen Wert abrufen, müssen Sie auch das srrf \_ NOEXPAND-Flag abrufen, oder " [**shreggetvalue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) " schlägt mit einem \_ ungültigen \_ Parameter fehl.</span><span class="sxs-lookup"><span data-stu-id="85f8a-114">If retrieving a value, you must also get the SRRF\_NOEXPAND flag, or [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) fails with ERROR\_INVALID\_PARAMETER.</span></span><br/>                                     |
| <span id="SRRF_RT_REG_BINARY"></span><span id="srrf_rt_reg_binary"></span><dl> <span data-ttu-id="85f8a-115"><dt>**Srrf \_ RT \_ reg \_ Binary**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-115"><dt>**SRRF\_RT\_REG\_BINARY**</dt> <dt>0x00000008</dt></span></span> </dl>           | <span data-ttu-id="85f8a-116">Geben Sie reg \_ Binary ein.</span><span class="sxs-lookup"><span data-stu-id="85f8a-116">Type REG\_BINARY.</span></span><br/>                                                                                                                                                                                           |
| <span id="SRRF_RT_REG_DWORD"></span><span id="srrf_rt_reg_dword"></span><dl> <span data-ttu-id="85f8a-117"><dt>**Srrf \_ RT \_ reg \_ DWORD**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-117"><dt>**SRRF\_RT\_REG\_DWORD**</dt> <dt>0x00000010</dt></span></span> </dl>              | <span data-ttu-id="85f8a-118">Geben Sie reg \_ DWORD ein.</span><span class="sxs-lookup"><span data-stu-id="85f8a-118">Type REG\_DWORD.</span></span><br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_REG_MULTI_SZ"></span><span id="srrf_rt_reg_multi_sz"></span><dl> <span data-ttu-id="85f8a-119"><dt>**Srrf \_ RT \_ reg \_ \_ MultiSZ**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-119"><dt>**SRRF\_RT\_REG\_MULTI\_SZ**</dt> <dt>0x00000020</dt></span></span> </dl>    | <span data-ttu-id="85f8a-120">Geben Sie \_ reg \_ MultiSZ ein.</span><span class="sxs-lookup"><span data-stu-id="85f8a-120">Type REG\_MULTI\_SZ.</span></span><br/>                                                                                                                                                                                        |
| <span id="SRRF_RT_REG_QWORD"></span><span id="srrf_rt_reg_qword"></span><dl> <span data-ttu-id="85f8a-121"><dt>**Srrf \_ RT \_ reg \_ QWORD**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-121"><dt>**SRRF\_RT\_REG\_QWORD**</dt> <dt>0x00000040</dt></span></span> </dl>              | <span data-ttu-id="85f8a-122">Geben Sie reg \_ QWORD ein.</span><span class="sxs-lookup"><span data-stu-id="85f8a-122">Type REG\_QWORD.</span></span><br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_DWORD"></span><span id="srrf_rt_dword"></span><dl> <span data-ttu-id="85f8a-123"><dt>**Srrf \_ RT \_ DWORD**</dt> <dt>0x00000018</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-123"><dt>**SRRF\_RT\_DWORD**</dt> <dt>0x00000018</dt></span></span> </dl>                           | <span data-ttu-id="85f8a-124">Reg \_ DWORD-und 32-Bit-reg- \_ Binär Typen.</span><span class="sxs-lookup"><span data-stu-id="85f8a-124">REG\_DWORD and 32-bit REG\_BINARY types.</span></span> <span data-ttu-id="85f8a-125">Dies entspricht srrf \_ RT \_ reg \_ Binary \| srrf \_ RT \_ reg \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="85f8a-125">This is equivalent to SRRF\_RT\_REG\_BINARY \| SRRF\_RT\_REG\_DWORD.</span></span> <span data-ttu-id="85f8a-126">Wenn beim Abrufen eines Werts die Binärdaten des Werts größer als 32 Bits sind, werden Sie nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85f8a-126">If retrieving a value, if the value's binary data is larger than 32 bits, it is not returned.</span></span><br/> |
| <span id="SRRF_RT_QWORD"></span><span id="srrf_rt_qword"></span><dl> <span data-ttu-id="85f8a-127"><dt>**Srrf \_ RT \_ QWORD**</dt> <dt>0x00000048</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-127"><dt>**SRRF\_RT\_QWORD**</dt> <dt>0x00000048</dt></span></span> </dl>                           | <span data-ttu-id="85f8a-128">Reg \_ QWORD-und 64-Bit-reg- \_ Binär Typen.</span><span class="sxs-lookup"><span data-stu-id="85f8a-128">REG\_QWORD and 64-bit REG\_BINARY types.</span></span> <span data-ttu-id="85f8a-129">Dies entspricht srrf \_ RT \_ reg \_ Binary \| srrf \_ RT \_ reg \_ QWORD.</span><span class="sxs-lookup"><span data-stu-id="85f8a-129">This is equivalent to SRRF\_RT\_REG\_BINARY \| SRRF\_RT\_REG\_QWORD.</span></span> <span data-ttu-id="85f8a-130">Wenn beim Abrufen eines Werts die Binärdaten des Werts größer als 64 Bits sind, werden Sie nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85f8a-130">If retrieving a value, if the value's binary data is larger than 64 bits, it is not returned.</span></span><br/> |
| <span id="SRRF_RT_ANY"></span><span id="srrf_rt_any"></span><dl> <span data-ttu-id="85f8a-131"><dt>**Srrf \_ RT \_ beliebige**</dt> <dt>0X0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-131"><dt>**SRRF\_RT\_ANY**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                                 | <span data-ttu-id="85f8a-132">Alle Typen.</span><span class="sxs-lookup"><span data-stu-id="85f8a-132">All types.</span></span> <span data-ttu-id="85f8a-133">Legen Sie dieses Flag fest, wenn kein anderer srrf \_ RT-Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="85f8a-133">Set this flag if no other SRRF\_RT value is set.</span></span><br/>                                                                                                                                                 |
| <span id="SRRF_RM_ANY"></span><span id="srrf_rm_any"></span><dl> <span data-ttu-id="85f8a-134"><dt>**Srrf \_ RM \_ beliebige**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-134"><dt>**SRRF\_RM\_ANY**</dt> <dt>0x00000000</dt></span></span> </dl>                                 | <span data-ttu-id="85f8a-135">Keine Modus-Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="85f8a-135">No mode restriction.</span></span> <span data-ttu-id="85f8a-136">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="85f8a-136">This is the default value.</span></span><br/>                                                                                                                                                             |
| <span id="SRRF_RM_NORMAL"></span><span id="srrf_rm_normal"></span><dl> <span data-ttu-id="85f8a-137"><dt>**Srrf \_ RM \_ Normal**</dt> <dt>0x00010000 bis</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-137"><dt>**SRRF\_RM\_NORMAL**</dt> <dt>0x00010000</dt></span></span> </dl>                        | <span data-ttu-id="85f8a-138">Schränken Sie den Systemstart Modus auf "normaler Start" ein.</span><span class="sxs-lookup"><span data-stu-id="85f8a-138">Restrict system startup mode to "normal boot".</span></span><br/>                                                                                                                                                              |
| <span id="SRRF_RM_SAFE"></span><span id="srrf_rm_safe"></span><dl> <span data-ttu-id="85f8a-139"><dt>**Srrf \_ RM- \_ sicheres**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-139"><dt>**SRRF\_RM\_SAFE**</dt> <dt>0x00020000</dt></span></span> </dl>                              | <span data-ttu-id="85f8a-140">Beschränken Sie den Systemstart Modus auf "Abgesicherter Modus".</span><span class="sxs-lookup"><span data-stu-id="85f8a-140">Restrict system startup mode to "safe mode".</span></span><br/>                                                                                                                                                                |
| <span id="SRRF_RM_SAFENETWORK"></span><span id="srrf_rm_safenetwork"></span><dl> <span data-ttu-id="85f8a-141"><dt>**Srrf \_ RM \_ SafeWork**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-141"><dt>**SRRF\_RM\_SAFENETWORK**</dt> <dt>0x00040000</dt></span></span> </dl>         | <span data-ttu-id="85f8a-142">Beschränken Sie den Systemstart Modus auf "Abgesicherter Modus mit Netzwerk".</span><span class="sxs-lookup"><span data-stu-id="85f8a-142">Restrict system startup mode to "safe mode with networking".</span></span><br/>                                                                                                                                                |
| <span id="SRRF_NOEXPAND"></span><span id="srrf_noexpand"></span><dl> <span data-ttu-id="85f8a-143"><dt>**Srrf \_ NOEXPAND**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-143"><dt>**SRRF\_NOEXPAND**</dt> <dt>0x10000000</dt></span></span> </dl>                            | <span data-ttu-id="85f8a-144">Erweitern Sie keine automatischen Erweiterungs-und Erweiterungs Zeichenfolgen \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="85f8a-144">Do not automatically expand REG\_EXPAND\_SZ environment strings.</span></span><br/>                                                                                                                                            |
| <span id="SRRF_ZEROONFAILURE"></span><span id="srrf_zeroonfailure"></span><dl> <span data-ttu-id="85f8a-145"><dt>**Srrf \_ Zeroonfailure**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-145"><dt>**SRRF\_ZEROONFAILURE**</dt> <dt>0x20000000</dt></span></span> </dl>             | <span data-ttu-id="85f8a-146">Wenn *pvData* beim Abrufen eines Werts nicht **null** ist, legen Sie den Inhalt des *pvData* -Puffers bei einem Fehler auf Nullen fest.</span><span class="sxs-lookup"><span data-stu-id="85f8a-146">If retrieving a value, if *pvData* is not **NULL**, set the contents of the *pvData* buffer to all zeros on failure.</span></span><br/>                                                                                        |
| <span id="SRRF_NOVIRT"></span><span id="srrf_novirt"></span><dl> <span data-ttu-id="85f8a-147"><dt>**Srrf \_ Novirt**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-147"><dt>**SRRF\_NOVIRT**</dt> <dt>0x40000000</dt></span></span> </dl>                                  | <span data-ttu-id="85f8a-148">Wenn beim Abrufen eines Werts der angeforderte Schlüssel virtualisiert ist, wird der Fehler mit der Fehler \_ Datei \_ nicht \_ gefunden.</span><span class="sxs-lookup"><span data-stu-id="85f8a-148">When retrieving a value, if the requested key is virtualized, fail with ERROR\_FILE\_NOT\_FOUND.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="85f8a-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85f8a-149">Remarks</span></span>

<span data-ttu-id="85f8a-150">Diese Werte werden in "shlwapi. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="85f8a-150">These values are defined in Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="85f8a-151">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="85f8a-151">Requirements</span></span>



| <span data-ttu-id="85f8a-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85f8a-152">Requirement</span></span> | <span data-ttu-id="85f8a-153">Wert</span><span class="sxs-lookup"><span data-stu-id="85f8a-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="85f8a-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85f8a-154">Minimum supported client</span></span><br/> | <span data-ttu-id="85f8a-155">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85f8a-155">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="85f8a-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85f8a-156">Minimum supported server</span></span><br/> | <span data-ttu-id="85f8a-157">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85f8a-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="85f8a-158">Header</span><span class="sxs-lookup"><span data-stu-id="85f8a-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="85f8a-159"><dt>Shlwapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="85f8a-159"><dt>Shlwapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85f8a-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="85f8a-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85f8a-161">**Shregsetvalue**</span><span class="sxs-lookup"><span data-stu-id="85f8a-161">**SHRegSetValue**</span></span>](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)
</dt> <dt>

[<span data-ttu-id="85f8a-162">**Shreggetvalue**</span><span class="sxs-lookup"><span data-stu-id="85f8a-162">**SHRegGetValue**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea)
</dt> </dl>

 

 




