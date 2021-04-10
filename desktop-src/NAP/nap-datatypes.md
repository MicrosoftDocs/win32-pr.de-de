---
title: NAP-Datentypen (naptypes. h)
description: 'Beachten Sie, dass die Netzwerk Zugriffsschutz-Plattform ab Windows 10 nicht mehr verfügbar ist: die Datentypen für die NAP-API (Network Access Protection, Netzwerk Zugriffsschutz) lauten wie folgt.'
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- Probationtime
- Protocolmaxsize
- Napcomponentid
- Systemhealthentityid
- Enforcemententityid
- Systemhealthentitycount
- Enforcemententitycount
- Stringcorrelationid
- ConnectionId
- Prozentwert
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5780d73701354a12b244c5e5ea6167c2cfba70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956966"
---
# <a name="nap-datatypes"></a><span data-ttu-id="51737-114">NAP-Datentypen</span><span class="sxs-lookup"><span data-stu-id="51737-114">NAP Datatypes</span></span>

> [!Note]  
> <span data-ttu-id="51737-115">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="51737-115">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="51737-116">Die Datentypen für die NAP-API (Network Access Protection, Netzwerk Zugriffsschutz) lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="51737-116">The datatypes for the Network Access Protection (NAP) API are as follows.</span></span>


```C++
typedef FILETIME ProbationTime;
typedef UINT32 ProtocolMaxSize;
typedef UINT32 NapComponentId;
typedef NapComponentId SystemHealthEntityId;
typedef NapComponentId EnforcementEntityId;
typedef UINT16 SystemHealthEntityCount;
typedef UINT16 EnforcementEntityCount;
typedef CountedString StringCorrelationId;
typedef GUID ConnectionId;
typedef UINT8 Percentage;
typedef UINT32 MessageId;
```



<dl> <dt>

<span data-ttu-id="51737-117">**Probationtime**</span><span class="sxs-lookup"><span data-stu-id="51737-117">**ProbationTime**</span></span>
</dt> <dd>

<span data-ttu-id="51737-118">Eine [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur, die eine Zeit im Zusammenhang mit der Bewährungsprobe eines Client Computers enthält.</span><span class="sxs-lookup"><span data-stu-id="51737-118">A [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains a time related to a client machine's probation.</span></span>

</dd> <dt>

<span data-ttu-id="51737-119">**Protocolmaxsize**</span><span class="sxs-lookup"><span data-stu-id="51737-119">**ProtocolMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="51737-120">Ein-Wert, der den Bereich möglicher Werte für die maximale Größe (in Bytes) eines [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Pakets angibt, wie nach Bereich definiert ([**minprotocolmaxsize, maxprotocolmaxsize**](nap-type-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="51737-120">A value that specifies the range of possible values for the maximum size, in bytes, of an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet as defined by range([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="51737-121">**Napcomponentid**</span><span class="sxs-lookup"><span data-stu-id="51737-121">**NapComponentId**</span></span>
</dt> <dd>

<span data-ttu-id="51737-122">Ein eindeutiger 4-Byte-Bezeichner, der von SHAs, SHVs und Erzwingungs Clients zur Identifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51737-122">A unique 4-byte identifier used by SHAs, SHVs and enforcement clients to identify themselves.</span></span> <span data-ttu-id="51737-123">Die ersten drei Bytes sind der durch IETF zugewiesene SMI-Code des Anbieters, und das letzte Byte identifiziert die Komponente selbst.</span><span class="sxs-lookup"><span data-stu-id="51737-123">The first three bytes are the IETF-assigned SMI code of the vendor, and the last byte identifies the component itself.</span></span>

</dd> <dt>

<span data-ttu-id="51737-124">**Systemhealthentityid**</span><span class="sxs-lookup"><span data-stu-id="51737-124">**SystemHealthEntityId**</span></span>
</dt> <dd>

<span data-ttu-id="51737-125">Ein **napcomponentid-** Wert, mit dem SHA/SHV-Paare identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="51737-125">A **NapComponentId** value used to identify SHA/SHV pairs.</span></span>

</dd> <dt>

<span data-ttu-id="51737-126">**Enforcemententityid**</span><span class="sxs-lookup"><span data-stu-id="51737-126">**EnforcementEntityId**</span></span>
</dt> <dd>

<span data-ttu-id="51737-127">Ein **napcomponentid-** Wert, mit dem Erzwingungs Clients identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="51737-127">A **NapComponentId** value used to identify enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="51737-128">**Systemhealthentitycount**</span><span class="sxs-lookup"><span data-stu-id="51737-128">**SystemHealthEntityCount**</span></span>
</dt> <dd>

<span data-ttu-id="51737-129">Ein-Wert, der die Anzahl der registrierten SHAs im NAP-System im Bereich von 0 (null) bis [**maxsystemhealthentitycount**](nap-type-constants.md)angibt.</span><span class="sxs-lookup"><span data-stu-id="51737-129">A value that specifies the number of registered SHAs in the NAP system in the range 0 (zero) to [**maxSystemHealthEntityCount**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="51737-130">**Enforcemententitycount**</span><span class="sxs-lookup"><span data-stu-id="51737-130">**EnforcementEntityCount**</span></span>
</dt> <dd>

<span data-ttu-id="51737-131">Ein-Wert, der die Anzahl der Erzwingungs Clients im NAP-System im Bereich von 0 (null) bis [**maxenforcercount**](nap-type-constants.md)angibt.</span><span class="sxs-lookup"><span data-stu-id="51737-131">A value that specifies the number of enforcement clients in the NAP system in the range 0 (zero) to [**maxEnforcerCount**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="51737-132">**Stringcorrelationid**</span><span class="sxs-lookup"><span data-stu-id="51737-132">**StringCorrelationId**</span></span>
</dt> <dd>

<span data-ttu-id="51737-133">Die " [**waytedstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) "-Version einer [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) -Struktur, die für die Kopplung von [**sohrequests**](/windows/win32/api/naptypes/ns-naptypes-soh) an **sohantworten** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51737-133">The [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) version of a [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure used to pair [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) to **SoHResponses**.</span></span>

</dd> <dt>

<span data-ttu-id="51737-134">**ConnectionID**</span><span class="sxs-lookup"><span data-stu-id="51737-134">**ConnectionId**</span></span>
</dt> <dd>

<span data-ttu-id="51737-135">Eine eindeutige GUID (Global Unique Identifier) zum Identifizieren von NAP-Verbindungen, die von Erzwingungs Clients verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="51737-135">A unique Globally Unique Identifier (GUID) used to identify a NAP connections maintained by enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="51737-136">**Percentage**</span><span class="sxs-lookup"><span data-stu-id="51737-136">**Percentage**</span></span>
</dt> <dd>

<span data-ttu-id="51737-137">Ein-Wert, der den Prozentsatz von 0 (null) und 100 der abgeschlossenen Wiederherstellung enthält.</span><span class="sxs-lookup"><span data-stu-id="51737-137">A value that contains the percentage between 0 (zero) and 100 of remediation that is complete</span></span>

</dd> <dt>

<span data-ttu-id="51737-138">**MessageId**</span><span class="sxs-lookup"><span data-stu-id="51737-138">**MessageId**</span></span>
</dt> <dd>

<span data-ttu-id="51737-139">Ein eindeutiger Wert, mit dem NAP-Systemmeldungen identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="51737-139">A unique value used to identify NAP system messages.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51737-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51737-140">Requirements</span></span>



| <span data-ttu-id="51737-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51737-141">Requirement</span></span> | <span data-ttu-id="51737-142">Wert</span><span class="sxs-lookup"><span data-stu-id="51737-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51737-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51737-143">Minimum supported client</span></span><br/> | <span data-ttu-id="51737-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51737-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                                                                                      |
| <span data-ttu-id="51737-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51737-145">Minimum supported server</span></span><br/> | <span data-ttu-id="51737-146">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51737-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                                |
| <span data-ttu-id="51737-147">Header</span><span class="sxs-lookup"><span data-stu-id="51737-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="51737-148"><dt>Naptypes. h; </dt> <dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="51737-148"><dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt></span></span> </dl> |



 

