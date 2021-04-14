---
title: MPTHREAT_INFO Struktur (mpclient. h)
description: Enthält Informationen zu einer Bedrohung.
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- MPTHREAT_INFO Struktur Funktionen der Legacy-Windows-Umgebung
- PMPTHREAT_INFO Struktur Zeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MPTHREAT_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa850a4293006a2f4b107a3f2579fdc14c1ea6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478738"
---
# <a name="mpthreat_info-structure"></a><span data-ttu-id="3002f-105">Mpthreat- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="3002f-105">MPTHREAT\_INFO structure</span></span>

<span data-ttu-id="3002f-106">Enthält Informationen zu einer Bedrohung.</span><span class="sxs-lookup"><span data-stu-id="3002f-106">Contains information about a threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="3002f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3002f-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFO {
  MPTHREAT_ID           ThreatID;
  GUID                  DetectionID;
  MP_MIDL_STRING LPWSTR Name;
  MPTHREAT_TYPE         ThreatType;
  MPTHREAT_SEVERITY     ThreatCriticality;
  MPTHREAT_CATEGORY     ThreatCategory;
  DWORD                 ThreatShortDescriptionID;
  DWORD                 ThreatAdviseDescriptionID;
  MPTHREAT_STATUS       ThreatStatus;
  DWORD                 SuggestedActionCount;
  MPTHREAT_ACTION       SuggestedActionArray[MP_MAX_SUGGESTIONS];
  DWORD                 ResourceCount;
  PMPRESOURCE_INFO      *ResourceList[ResourceCount];
  ULARGE_INTEGER        ThreatStatusTime;
  HRESULT               ThreatStatusCode;
  MPTHREAT_DETECTION    ThreatDetection;
  GUID                  QuarantineGuid;
  MPEXECUTION_STATUS    ExecutionStatus;
  union {
    PMPTHREAT_INFOEX_UNUSED   pKnownBad;
    PMPTHREAT_INFOEX_BEHAVIOR pBehavior;
    PMPTHREAT_INFOEX_UNUSED   pUnknown;
    PMPTHREAT_INFOEX_UNUSED   pKnownGood;
    PMPTHREAT_INFOEX_NIS      pNis;
  } Data;
  MPDETECTION_STATE     State;
  MP_MIDL_STRING LPWSTR DetectionUser;
  MPSOURCE              DetectionSource;
  MP_MIDL_STRING LPWSTR ProcessName;
  MPDETECTION_ORIGIN    DetectionOrigin;
  DWORD                 reserved1;
  ULARGE_INTEGER        DetectionTime;
  MPEXECUTION_STATUS    PreExecutionStatus;
  ULARGE_INTEGER        RemediationTime;
  MPEXECUTION_STATUS    PostExecutionStatus;
  BOOL                  CriticalFailure;
  DWORD                 NonCriticalReason;
  MP_MIDL_STRING LPWSTR RemediationUser;
  DWORD                 RemediationResourceCount;
  PMPRESOURCE_INFO      RemediationResourceList[RemediationResourceCount];
  BOOL                  FailureResolved;
  MPRESOLVED_REASON     ResolvedReason;
  DWORD                 AdditionalActions;
  DWORD                 ResolvedActions;
  DWORD                 dwThreatStatusFlag;
} MPTHREAT_INFO, *PMPTHREAT_INFO;
```



## <a name="members"></a><span data-ttu-id="3002f-108">Member</span><span class="sxs-lookup"><span data-stu-id="3002f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3002f-109">**Threatid**</span><span class="sxs-lookup"><span data-stu-id="3002f-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-110">Typ: **mpthreat- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="3002f-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-111">Bedrohungs Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="3002f-111">Threat identifier.</span></span> <span data-ttu-id="3002f-112">Das obere Bit ist festgelegt, um antivirenbezogene Bedrohungen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3002f-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-113">**Detectionid**</span><span class="sxs-lookup"><span data-stu-id="3002f-113">**DetectionID**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-114">Typ: **GUID**</span><span class="sxs-lookup"><span data-stu-id="3002f-114">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-115">Erkennungs-ID.</span><span class="sxs-lookup"><span data-stu-id="3002f-115">Detection ID.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="3002f-116">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-117">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3002f-117">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-118">Bedrohungs Name.</span><span class="sxs-lookup"><span data-stu-id="3002f-118">Threat name.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-119">**Typ**</span><span class="sxs-lookup"><span data-stu-id="3002f-119">**ThreatType**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-120">Typ: **[ **mpthreat- \_ Typ**](mpthreat-type.md)**</span><span class="sxs-lookup"><span data-stu-id="3002f-120">Type: **[**MPTHREAT\_TYPE**](mpthreat-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-121">Bedrohungstyp.</span><span class="sxs-lookup"><span data-stu-id="3002f-121">Threat type.</span></span> <span data-ttu-id="3002f-122">Wird zur Unterscheidung zwischen unterschiedlichen Bedrohungs Typen verwendet, wie z. b. bekanntermaßen "schlecht", "unbekannt"</span><span class="sxs-lookup"><span data-stu-id="3002f-122">Used to differentiate among different threat types such as known bad, unknown, or known good.</span></span> <span data-ttu-id="3002f-123">Siehe [**mpthreat- \_ Typ**](mpthreat-type.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-123">See [**MPTHREAT\_TYPE**](mpthreat-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-124">**Gefährlichkeit**</span><span class="sxs-lookup"><span data-stu-id="3002f-124">**ThreatCriticality**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-125">Typ: **[ **mpthreat- \_ Schweregrad**](mpthreat-severity.md)**</span><span class="sxs-lookup"><span data-stu-id="3002f-125">Type: **[**MPTHREAT\_SEVERITY**](mpthreat-severity.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-126">Bedrohungs Gefahr.</span><span class="sxs-lookup"><span data-stu-id="3002f-126">Threat criticality.</span></span> <span data-ttu-id="3002f-127">Siehe [**mpthreat- \_ Schweregrad**](mpthreat-severity.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-127">See [**MPTHREAT\_SEVERITY**](mpthreat-severity.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-128">**ThreatCategory**</span><span class="sxs-lookup"><span data-stu-id="3002f-128">**ThreatCategory**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-129">Typ: **[ **mpthreat- \_ Kategorie**](mpthreat-category.md)**</span><span class="sxs-lookup"><span data-stu-id="3002f-129">Type: **[**MPTHREAT\_CATEGORY**](mpthreat-category.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-130">Bedrohungs Kategorie, z. b. ein Trojaner oder eine Keylogger.</span><span class="sxs-lookup"><span data-stu-id="3002f-130">Threat category, such as a trojan or a keylogger.</span></span> <span data-ttu-id="3002f-131">Siehe [**mpthreat- \_ Kategorie**](mpthreat-category.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-131">See [**MPTHREAT\_CATEGORY**](mpthreat-category.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-132">**"Bedrohlich shortdescriptionid"**</span><span class="sxs-lookup"><span data-stu-id="3002f-132">**ThreatShortDescriptionID**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-133">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3002f-133">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-134">ID der Bedrohungs Kurzbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="3002f-134">Threat short description ID.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-135">**"Bedrohlich advimendescriptionid"**</span><span class="sxs-lookup"><span data-stu-id="3002f-135">**ThreatAdviseDescriptionID**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-136">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3002f-136">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-137">ID der Bedrohungs Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="3002f-137">Threat advise description ID.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-138">**ThreatStatus**</span><span class="sxs-lookup"><span data-stu-id="3002f-138">**ThreatStatus**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-139">Typ: **[ **mpthreat- \_ Status**](mpthreat-status.md)**</span><span class="sxs-lookup"><span data-stu-id="3002f-139">Type: **[**MPTHREAT\_STATUS**](mpthreat-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-140">Bedrohungs Status, z. b. erkannt, bereinigt oder unter Quarantäne.</span><span class="sxs-lookup"><span data-stu-id="3002f-140">Threat status such as detected, cleaned, or quarantined.</span></span> <span data-ttu-id="3002f-141">Siehe [**mpthreat- \_ Status**](mpthreat-status.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-141">See [**MPTHREAT\_STATUS**](mpthreat-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-142">**Vorschlags stedactioncount**</span><span class="sxs-lookup"><span data-stu-id="3002f-142">**SuggestedActionCount**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-143">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3002f-143">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-144">Anzahl der vorgeschlagenen Aktionen in "Vorschlags **stedactionarray**".</span><span class="sxs-lookup"><span data-stu-id="3002f-144">Count of suggested actions in **SuggestedActionArray**.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-145">**Vorschlag**</span><span class="sxs-lookup"><span data-stu-id="3002f-145">**SuggestedActionArray**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-146">Typ: **[**mpthreat \_ Action**](mpthreat-action.md) \[ MP \_ Maximale \_ Vorschläge\]**</span><span class="sxs-lookup"><span data-stu-id="3002f-146">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)\[MP\_MAX\_SUGGESTIONS\]**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-147">Array von vorgeschlagenen Aktionen.</span><span class="sxs-lookup"><span data-stu-id="3002f-147">Array of suggested actions.</span></span> <span data-ttu-id="3002f-148">Siehe [**mpthreat- \_ Aktion**](mpthreat-action.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-148">See [**MPTHREAT\_ACTION**](mpthreat-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-149">**ResourceCount**</span><span class="sxs-lookup"><span data-stu-id="3002f-149">**ResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-150">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3002f-150">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-151">Anzahl der Ressourcen in **resourceList**.</span><span class="sxs-lookup"><span data-stu-id="3002f-151">Count of resources in **ResourceList**.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-152">**ResourceList**</span><span class="sxs-lookup"><span data-stu-id="3002f-152">**ResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-153">Typ: \**pmpresource \_ Info \** _</span><span class="sxs-lookup"><span data-stu-id="3002f-153">Type: \**PMPRESOURCE\_INFO\** _</span></span>

</dd> <dd>

<span data-ttu-id="3002f-154">Liste der mit der Bedrohung identifizierten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="3002f-154">List of resources identified with the threat.</span></span> <span data-ttu-id="3002f-155">Weitere Informationen finden Sie unter [_ *mpresource- \_ Informationen* \*](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-155">See [_ *MPRESOURCE\_INFO*\*](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-156">**Bedrohung**</span><span class="sxs-lookup"><span data-stu-id="3002f-156">**ThreatStatusTime**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-157">Typ: **ularge \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="3002f-157">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-158">Zeitpunkt, zu dem der Bedrohungs Status zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="3002f-158">Time when threat status last changed.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-159">**"Bedrohlich Statuscode"**</span><span class="sxs-lookup"><span data-stu-id="3002f-159">**ThreatStatusCode**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-160">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3002f-160">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-161">Statuscode, der mit dem Bedrohungs Status verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="3002f-161">Status code associated with the threat status.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-162">**Erkennung**</span><span class="sxs-lookup"><span data-stu-id="3002f-162">**ThreatDetection**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-163">Typ: **[ **mpthreat- \_ Erkennung**](mpthreat-detection.md)**</span><span class="sxs-lookup"><span data-stu-id="3002f-163">Type: **[**MPTHREAT\_DETECTION**](mpthreat-detection.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-164">Bedrohungs Erkennungs Typen, z. b. konkret, verdächtig oder generisch.</span><span class="sxs-lookup"><span data-stu-id="3002f-164">Threat detection type, such as concrete, suspicious, or generic.</span></span> <span data-ttu-id="3002f-165">Siehe [**mpthreat- \_ Erkennung**](mpthreat-detection.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-165">See [**MPTHREAT\_DETECTION**](mpthreat-detection.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-166">**Quarantäne-GUID**</span><span class="sxs-lookup"><span data-stu-id="3002f-166">**QuarantineGuid**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-167">Typ: **GUID**</span><span class="sxs-lookup"><span data-stu-id="3002f-167">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-168">Quarantäne-GUID.</span><span class="sxs-lookup"><span data-stu-id="3002f-168">Quarantine guid.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-169">**ExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="3002f-169">**ExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-170">Typ: **[ **mpexecution- \_ Status**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="3002f-170">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-171">Ausführungs Status der Bedrohung, z. b. nicht bekannt, blockiert oder aktiv.</span><span class="sxs-lookup"><span data-stu-id="3002f-171">Execution status of the threat, such as not known, blocked, or active.</span></span> <span data-ttu-id="3002f-172">Siehe [**mpexecution- \_ Status**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-172">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-173">**Daten**</span><span class="sxs-lookup"><span data-stu-id="3002f-173">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-174">Weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="3002f-174">Extra information.</span></span> <span data-ttu-id="3002f-175">Der Zeiger auf die entsprechende-Struktur hängt vom Wert von "- **Typ**" ab.</span><span class="sxs-lookup"><span data-stu-id="3002f-175">The pointer to the appropriate structure depends on the value of **ThreatType**.</span></span>

<dl> <dt>

<span data-ttu-id="3002f-176">**pknownbad**</span><span class="sxs-lookup"><span data-stu-id="3002f-176">**pKnownBad**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-177">Typ: **pmpthreat \_ INFOEX nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="3002f-177">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-178">Wenn der **Typ**  ==  **mpthreat den \_ Typ \_ knownbad** hat.</span><span class="sxs-lookup"><span data-stu-id="3002f-178">When **ThreatType** == **MPTHREAT\_TYPE\_KNOWNBAD**.</span></span> <span data-ttu-id="3002f-179">Weitere Informationen finden Sie unter [**mpthreat \_ INFOEX nicht \_ verwendet**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-179">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-180">**pbehavior**</span><span class="sxs-lookup"><span data-stu-id="3002f-180">**pBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-181">Typ: **pmpthreat \_ INFOEX- \_ Verhalten**</span><span class="sxs-lookup"><span data-stu-id="3002f-181">Type: **PMPTHREAT\_INFOEX\_BEHAVIOR**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-182">Wenn der **Typ**  ==  **mpthreat \_ Type \_ Verhalten** hat.</span><span class="sxs-lookup"><span data-stu-id="3002f-182">When **ThreatType** == **MPTHREAT\_TYPE\_BEHAVIOR**.</span></span> <span data-ttu-id="3002f-183">Siehe [**mpthreat \_ INFOEX- \_ Verhalten**](mpthreat-infoex-behavior.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-183">See [**MPTHREAT\_INFOEX\_BEHAVIOR**](mpthreat-infoex-behavior.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-184">**pUnknown**</span><span class="sxs-lookup"><span data-stu-id="3002f-184">**pUnknown**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-185">Typ: **pmpthreat \_ INFOEX nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="3002f-185">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-186">Wenn **der Typ**  ==  **mpthreat \_ Type \_ unbekannt** ist.</span><span class="sxs-lookup"><span data-stu-id="3002f-186">When **ThreatType** == **MPTHREAT\_TYPE\_UNKNOWN**.</span></span> <span data-ttu-id="3002f-187">Weitere Informationen finden Sie unter [**mpthreat \_ INFOEX nicht \_ verwendet**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-187">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-188">**pknowngood**</span><span class="sxs-lookup"><span data-stu-id="3002f-188">**pKnownGood**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-189">Typ: **pmpthreat \_ INFOEX nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="3002f-189">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-190">Wenn **gefährtype** = = mpthreat \_ Type \_ knowngood ist.</span><span class="sxs-lookup"><span data-stu-id="3002f-190">When **ThreatType** == MPTHREAT\_TYPE\_KNOWNGOOD.</span></span> <span data-ttu-id="3002f-191">Weitere Informationen finden Sie unter [**mpthreat \_ INFOEX nicht \_ verwendet**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-191">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-192">**pnis**</span><span class="sxs-lookup"><span data-stu-id="3002f-192">**pNis**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-193">Typ: **pmpthreat \_ INFOEX \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="3002f-193">Type: **PMPTHREAT\_INFOEX\_NIS**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-194">Wenn der **Typ**  ==  **mpthreat \_ Type \_ NIS** ist.</span><span class="sxs-lookup"><span data-stu-id="3002f-194">When **ThreatType** == **MPTHREAT\_TYPE\_NIS**.</span></span> <span data-ttu-id="3002f-195">Weitere Informationen finden Sie unter [**mpthreat \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-195">See [**MPTHREAT\_INFOEX\_NIS**](mpthreat-infoex-nis.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3002f-196">**State**</span><span class="sxs-lookup"><span data-stu-id="3002f-196">**State**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-197">Typ: **[ **mperkennungs- \_ Status**](mpdetection-state.md)**</span><span class="sxs-lookup"><span data-stu-id="3002f-197">Type: **[**MPDETECTION\_STATE**](mpdetection-state.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-198">Der aktuelle Zustand der Erkennung.</span><span class="sxs-lookup"><span data-stu-id="3002f-198">The current state of the detection.</span></span> <span data-ttu-id="3002f-199">Siehe [**mperkennungs- \_ Status**](mpdetection-state.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-199">See [**MPDETECTION\_STATE**](mpdetection-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-200">**Erkenctionuser**</span><span class="sxs-lookup"><span data-stu-id="3002f-200">**DetectionUser**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-201">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3002f-201">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-202">Der Benutzer, der der Erkennung zugeordnet ist, im Format "Domäne/Benutzer".</span><span class="sxs-lookup"><span data-stu-id="3002f-202">The user associated with the detection, in the format "domain/user".</span></span>

</dd> <dt>

<span data-ttu-id="3002f-203">**Detectionsource**</span><span class="sxs-lookup"><span data-stu-id="3002f-203">**DetectionSource**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-204">Typ: **[ **mpsource**](mpsource.md)**</span><span class="sxs-lookup"><span data-stu-id="3002f-204">Type: **[**MPSOURCE**](mpsource.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-205">Die Quelle der Erkennung.</span><span class="sxs-lookup"><span data-stu-id="3002f-205">The source of the detection.</span></span> <span data-ttu-id="3002f-206">Siehe [**mpsource**](mpsource.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-206">See [**MPSOURCE**](mpsource.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-207">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="3002f-207">**ProcessName**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-208">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3002f-208">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-209">Der Prozess Name, der der Erkennung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3002f-209">Process name associated with the detection.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-210">**Detectionorigin**</span><span class="sxs-lookup"><span data-stu-id="3002f-210">**DetectionOrigin**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-211">Typ: **[ **mperkennungs- \_ Ursprung**](mpdetection-origin.md)**</span><span class="sxs-lookup"><span data-stu-id="3002f-211">Type: **[**MPDETECTION\_ORIGIN**](mpdetection-origin.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-212">Der Ursprung der Erkennung, z. b. local oder Network.</span><span class="sxs-lookup"><span data-stu-id="3002f-212">The origin of the detection, such as local or network.</span></span> <span data-ttu-id="3002f-213">Siehe [**mperkennungs- \_ Ursprung**](mpdetection-origin.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-213">See [**MPDETECTION\_ORIGIN**](mpdetection-origin.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-214">**"reserved1"**</span><span class="sxs-lookup"><span data-stu-id="3002f-214">**reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-215">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3002f-215">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-216">Reservierte Metadaten zur Erkennung.</span><span class="sxs-lookup"><span data-stu-id="3002f-216">Reserved metadata about the detection.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-217">**Erkenctiontime**</span><span class="sxs-lookup"><span data-stu-id="3002f-217">**DetectionTime**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-218">Typ: **ularge \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="3002f-218">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-219">Der Zeitpunkt der ersten Erkennung.</span><span class="sxs-lookup"><span data-stu-id="3002f-219">The time of the initial detection.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-220">**Preexecutionstatus**</span><span class="sxs-lookup"><span data-stu-id="3002f-220">**PreExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-221">Typ: **[ **mpexecution- \_ Status**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="3002f-221">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-222">Ausführungs Status direkt vor der Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="3002f-222">Execution status right before remediation.</span></span> <span data-ttu-id="3002f-223">Siehe [**mpexecution- \_ Status**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-223">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-224">**Wiederbehebe Zeit**</span><span class="sxs-lookup"><span data-stu-id="3002f-224">**RemediationTime**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-225">Typ: **ularge \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="3002f-225">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-226">Die Zeit für die Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="3002f-226">The time remediation occured.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-227">**Postexecutionstatus**</span><span class="sxs-lookup"><span data-stu-id="3002f-227">**PostExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-228">Typ: **[ **mpexecution- \_ Status**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="3002f-228">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-229">Ausführungs Status nach der Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="3002f-229">Execution status after remediation.</span></span> <span data-ttu-id="3002f-230">Siehe [**mpexecution- \_ Status**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-230">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-231">**CriticalFailure**</span><span class="sxs-lookup"><span data-stu-id="3002f-231">**CriticalFailure**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-232">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="3002f-232">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-233">True, wenn der Wiederherstellungs Fehler kritisch war.</span><span class="sxs-lookup"><span data-stu-id="3002f-233">True if the remediation failure was critical.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-234">**Nicht criticalreason**</span><span class="sxs-lookup"><span data-stu-id="3002f-234">**NonCriticalReason**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-235">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3002f-235">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-236">Der Grund für den Fehler bei der Wiederherstellung ist nicht wichtig.</span><span class="sxs-lookup"><span data-stu-id="3002f-236">The reason the remediation failure is not critical.</span></span> <span data-ttu-id="3002f-237">Dies wird in Zukunft nicht garantiert unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3002f-237">This is not guaranteed to be supported in the future.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-238">**Wiederbeheationuser**</span><span class="sxs-lookup"><span data-stu-id="3002f-238">**RemediationUser**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-239">Typ: **MP- \_ Mittell- \_ Zeichenfolge LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3002f-239">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-240">Der Benutzer, der die Wiederherstellung angefordert hat, im Format Domäne/Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3002f-240">User that requested the remediation, in the format "domain/user".</span></span>

</dd> <dt>

<span data-ttu-id="3002f-241">**Wiederbeheationresourcecount**</span><span class="sxs-lookup"><span data-stu-id="3002f-241">**RemediationResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-242">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3002f-242">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-243">Anzahl der Ressourcen in der **wiederbehebe**-Ressourcen Liste.</span><span class="sxs-lookup"><span data-stu-id="3002f-243">Count of resources in **RemediationResourceList**.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-244">**Wiederherstellung von wiedersourcelist**</span><span class="sxs-lookup"><span data-stu-id="3002f-244">**RemediationResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-245">Typ: **pmpresource \_ Info \[ wiederbeheationresourcecount \]**</span><span class="sxs-lookup"><span data-stu-id="3002f-245">Type: **PMPRESOURCE\_INFO\[RemediationResourceCount\]**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-246">Liste der Ressourcen, die während der Wiederherstellung nicht erfolgreich waren</span><span class="sxs-lookup"><span data-stu-id="3002f-246">List of resources that failed during remediation.</span></span> <span data-ttu-id="3002f-247">Informationen finden Sie unter [**mpresource- \_ Informationen**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-247">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-248">**Failureresolved**</span><span class="sxs-lookup"><span data-stu-id="3002f-248">**FailureResolved**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-249">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="3002f-249">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-250">True, wenn der Wiederherstellungs Fehler behoben wurde.</span><span class="sxs-lookup"><span data-stu-id="3002f-250">True if remediation failure been resolved.</span></span> <span data-ttu-id="3002f-251">Dadurch wird der Bucket entweder auf Complete oder eine zusätzliche Aktion verschoben.</span><span class="sxs-lookup"><span data-stu-id="3002f-251">This will move the bucket to either complete or an additional action.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-252">**Resolvedreason**</span><span class="sxs-lookup"><span data-stu-id="3002f-252">**ResolvedReason**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-253">Typ: **[ **mpregelöste \_ Ursache**](mpresolved-reason.md)**</span><span class="sxs-lookup"><span data-stu-id="3002f-253">Type: **[**MPRESOLVED\_REASON**](mpresolved-reason.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-254">Der Grund für die Behebung des Fehlers bei der Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="3002f-254">Reason for remediation failure being resolved.</span></span> <span data-ttu-id="3002f-255">Dies ist der Grund, warum die Erkennung von nicht zu weiteren Aktionen verschoben wurde oder abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3002f-255">This is the reason the detection moved from failed to additional action or finished.</span></span> <span data-ttu-id="3002f-256">Weitere Informationen finden Sie unter [**mpregelöste \_ reason**](mpresolved-reason.md).</span><span class="sxs-lookup"><span data-stu-id="3002f-256">See [**MPRESOLVED\_REASON**](mpresolved-reason.md).</span></span>

</dd> <dt>

<span data-ttu-id="3002f-257">**Additionalactions**</span><span class="sxs-lookup"><span data-stu-id="3002f-257">**AdditionalActions**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-258">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3002f-258">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-259">Sind zusätzliche Aktionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3002f-259">Are additional actions required.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-260">**Resolvedactions**</span><span class="sxs-lookup"><span data-stu-id="3002f-260">**ResolvedActions**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-261">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3002f-261">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-262">Alle weiteren Aktionen, die ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="3002f-262">Any additional actions that have been performed.</span></span>

</dd> <dt>

<span data-ttu-id="3002f-263">**dwbilistatusflag**</span><span class="sxs-lookup"><span data-stu-id="3002f-263">**dwThreatStatusFlag**</span></span>
</dt> <dd>

<span data-ttu-id="3002f-264">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3002f-264">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3002f-265">Zusätzliche Informationen zur Bedrohungserkennung.</span><span class="sxs-lookup"><span data-stu-id="3002f-265">Additonal information about the threat detection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3002f-266">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3002f-266">Requirements</span></span>



| <span data-ttu-id="3002f-267">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3002f-267">Requirement</span></span> | <span data-ttu-id="3002f-268">Wert</span><span class="sxs-lookup"><span data-stu-id="3002f-268">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3002f-269">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3002f-269">Minimum supported client</span></span><br/> | <span data-ttu-id="3002f-270">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3002f-270">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3002f-271">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3002f-271">Minimum supported server</span></span><br/> | <span data-ttu-id="3002f-272">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3002f-272">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3002f-273">Header</span><span class="sxs-lookup"><span data-stu-id="3002f-273">Header</span></span><br/>                   | <dl> <span data-ttu-id="3002f-274"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3002f-274"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3002f-275">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3002f-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3002f-276">**Mpfrememory**</span><span class="sxs-lookup"><span data-stu-id="3002f-276">**MpFreeMemory**</span></span>](mpfreememory.md)
</dt> <dt>

[<span data-ttu-id="3002f-277">**Mpzerenumerate**</span><span class="sxs-lookup"><span data-stu-id="3002f-277">**MpThreatEnumerate**</span></span>](mpthreatenumerate.md)
</dt> <dt>

[<span data-ttu-id="3002f-278">**Mpbedrohlich Query**</span><span class="sxs-lookup"><span data-stu-id="3002f-278">**MpThreatQuery**</span></span>](mpthreatquery.md)
</dt> <dt>

[<span data-ttu-id="3002f-279">**mperkennungs- \_ Ursprung**</span><span class="sxs-lookup"><span data-stu-id="3002f-279">**MPDETECTION\_ORIGIN**</span></span>](mpdetection-origin.md)
</dt> <dt>

[<span data-ttu-id="3002f-280">**mperkennungs- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="3002f-280">**MPDETECTION\_STATE**</span></span>](mpdetection-state.md)
</dt> <dt>

[<span data-ttu-id="3002f-281">**mpexecution- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="3002f-281">**MPEXECUTION\_STATUS**</span></span>](mpexecution-status.md)
</dt> <dt>

[<span data-ttu-id="3002f-282">**mpregelösten \_ Grund**</span><span class="sxs-lookup"><span data-stu-id="3002f-282">**MPRESOLVED\_REASON**</span></span>](mpresolved-reason.md)
</dt> <dt>

[<span data-ttu-id="3002f-283">**mpresource- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="3002f-283">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="3002f-284">**Mpsource**</span><span class="sxs-lookup"><span data-stu-id="3002f-284">**MPSOURCE**</span></span>](mpsource.md)
</dt> <dt>

[<span data-ttu-id="3002f-285">**mpthreat- \_ Aktion**</span><span class="sxs-lookup"><span data-stu-id="3002f-285">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> <dt>

[<span data-ttu-id="3002f-286">**mpthreat- \_ Kategorie**</span><span class="sxs-lookup"><span data-stu-id="3002f-286">**MPTHREAT\_CATEGORY**</span></span>](mpthreat-category.md)
</dt> <dt>

[<span data-ttu-id="3002f-287">**mpthreat- \_ Erkennung**</span><span class="sxs-lookup"><span data-stu-id="3002f-287">**MPTHREAT\_DETECTION**</span></span>](mpthreat-detection.md)
</dt> <dt>

[<span data-ttu-id="3002f-288">**mpthreat- \_ INFOEX- \_ Verhalten**</span><span class="sxs-lookup"><span data-stu-id="3002f-288">**MPTHREAT\_INFOEX\_BEHAVIOR**</span></span>](mpthreat-infoex-behavior.md)
</dt> <dt>

[<span data-ttu-id="3002f-289">**mpthreat \_ INFOEX \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="3002f-289">**MPTHREAT\_INFOEX\_NIS**</span></span>](mpthreat-infoex-nis.md)
</dt> <dt>

[<span data-ttu-id="3002f-290">**mpthreat \_ INFOEX nicht \_ verwendet**</span><span class="sxs-lookup"><span data-stu-id="3002f-290">**MPTHREAT\_INFOEX\_UNUSED**</span></span>](mpthreat-infoex-unused.md)
</dt> <dt>

[<span data-ttu-id="3002f-291">**mpthreat- \_ Schweregrad**</span><span class="sxs-lookup"><span data-stu-id="3002f-291">**MPTHREAT\_SEVERITY**</span></span>](mpthreat-severity.md)
</dt> <dt>

[<span data-ttu-id="3002f-292">**mpthreat- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="3002f-292">**MPTHREAT\_STATUS**</span></span>](mpthreat-status.md)
</dt> <dt>

[<span data-ttu-id="3002f-293">**mpthreat- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="3002f-293">**MPTHREAT\_TYPE**</span></span>](mpthreat-type.md)
</dt> </dl>

 

 





