---
UID: ''
title: Lsamanagesidnamemapping-Funktion
description: Fügt sid/Name-Zuordnungen aus dem im LSA-lookupdienst registrierten Zuordnungs Satz hinzu oder entfernt Sie.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: ''
ms.topic: reference
req.header: Ntsecapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Secur32.lib
req.dll:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
- API-MS-Win-security-lsalookup-l2-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name:
- LsaManageSidNameMapping
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: fc0065c3964718d690149693f3c71ec4e9f676ec
ms.sourcegitcommit: 382c7259008374408368c173e0027fb641c848fe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "104314494"
---
# <a name="lsamanagesidnamemapping-function"></a><span data-ttu-id="a1d76-103">Lsamanagesidnamemapping-Funktion</span><span class="sxs-lookup"><span data-stu-id="a1d76-103">LsaManageSidNameMapping function</span></span>

## <a name="description"></a><span data-ttu-id="a1d76-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1d76-104">Description</span></span>

<span data-ttu-id="a1d76-105">Die **lsamanagesidnamemapping** -Funktion fügt sid/Name-Zuordnungen aus dem mit dem LSA-lookupdienst registrierten Zuordnungs Satz hinzu oder entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="a1d76-105">The **LsaManageSidNameMapping** function adds or removes SID/name mappings from the mapping set registered with the LSA Lookup Service.</span></span>

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a><span data-ttu-id="a1d76-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1d76-106">Parameters</span></span>

### <a name="optype-in"></a><span data-ttu-id="a1d76-107">Optype [in]</span><span class="sxs-lookup"><span data-stu-id="a1d76-107">OpType [in]</span></span>

<span data-ttu-id="a1d76-108">Gibt an, ob diese Funktion aufgerufen wird, um eine SID/Name-Zuordnung hinzuzufügen oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a1d76-108">Indicates if a this function is being called to add or remove an SID/name mapping.</span></span>

### <a name="opinput-in"></a><span data-ttu-id="a1d76-109">Opinput [in]</span><span class="sxs-lookup"><span data-stu-id="a1d76-109">OpInput [in]</span></span>

<span data-ttu-id="a1d76-110">Gibt die Domänen-, Konto-und sid-Werte an, die während dieses Vorgangs verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a1d76-110">Indicates the domain, account, and SID values to use during this operation.</span></span> <span data-ttu-id="a1d76-111">Zusätzliche Flags können auch in dieser Struktur festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a1d76-111">Additional flags can also be set within this structure.</span></span>

### <a name="opoutput-out"></a><span data-ttu-id="a1d76-112">Opoutput [out]</span><span class="sxs-lookup"><span data-stu-id="a1d76-112">OpOutput [out]</span></span>

<span data-ttu-id="a1d76-113">Enthält den Wert [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) , der einen erfolgreichen oder fehlgeschlagener Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="a1d76-113">Contains a value of [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) that indicates operation success or failure.</span></span>

| <span data-ttu-id="a1d76-114">Wert</span><span class="sxs-lookup"><span data-stu-id="a1d76-114">Value</span></span> | <span data-ttu-id="a1d76-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a1d76-115">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="a1d76-116">**Erfolgreich**</span><span class="sxs-lookup"><span data-stu-id="a1d76-116">**Success**</span></span> | <span data-ttu-id="a1d76-117">Der Vorgang ist ohne Fehler beendet.</span><span class="sxs-lookup"><span data-stu-id="a1d76-117">Operation is complete without error.</span></span> |
| <span data-ttu-id="a1d76-118">**Nonmappingerror**</span><span class="sxs-lookup"><span data-stu-id="a1d76-118">**NonMappingError**</span></span> | <span data-ttu-id="a1d76-119">Ein Fehler, der nicht mit der SID-Namenszuordnung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a1d76-119">An error unrelated to SID-name mapping has occurred.</span></span> |
| <span data-ttu-id="a1d76-120">**Namecollision**</span><span class="sxs-lookup"><span data-stu-id="a1d76-120">**NameCollision**</span></span> | <span data-ttu-id="a1d76-121">Vorgangs Fehler aufgrund eines Namens Konflikts.</span><span class="sxs-lookup"><span data-stu-id="a1d76-121">Operation failure due to name collision.</span></span> |
| <span data-ttu-id="a1d76-122">**Sidcollision**</span><span class="sxs-lookup"><span data-stu-id="a1d76-122">**SidCollision**</span></span> | <span data-ttu-id="a1d76-123">Vorgangs Fehler aufgrund eines sid-Konflikts.</span><span class="sxs-lookup"><span data-stu-id="a1d76-123">Operation failure due to SID collision.</span></span> |
| <span data-ttu-id="a1d76-124">**DomainNotFound**</span><span class="sxs-lookup"><span data-stu-id="a1d76-124">**DomainNotFound**</span></span> | <span data-ttu-id="a1d76-125">Die zugehörige Domäne wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="a1d76-125">Corresponding domain not found.</span></span> |
| <span data-ttu-id="a1d76-126">**Domainsidprefixmismatch**</span><span class="sxs-lookup"><span data-stu-id="a1d76-126">**DomainSidPrefixMismatch**</span></span> | <span data-ttu-id="a1d76-127">Die angegebene sid weist nicht das richtige Domänen Präfix auf.</span><span class="sxs-lookup"><span data-stu-id="a1d76-127">Provided SID doesn't have the correct domain prefix.</span></span> |
| <span data-ttu-id="a1d76-128">**Mappingnotfound**</span><span class="sxs-lookup"><span data-stu-id="a1d76-128">**MappingNotFound**</span></span> | <span data-ttu-id="a1d76-129">Die Zuordnung wurde im Cache nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="a1d76-129">Mapping not found in the cache.</span></span> |

## <a name="returns"></a><span data-ttu-id="a1d76-130">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="a1d76-130">Returns</span></span>

<span data-ttu-id="a1d76-131">Wenn die Zuordnung erfolgreich eingefügt wird, wird der Rückgabewert STATUS_SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="a1d76-131">If the mapping is inserted successfully, the return value is STATUS_SUCCESS.</span></span>
<span data-ttu-id="a1d76-132">Wenn die Funktion andernfalls aufgrund von sid-oder Namenskonflikten fehlschlägt, wird STATUS_INVALID_PARAMETER Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a1d76-132">Otherwise, if the function fails due to SID or name conflicts, STATUS_INVALID_PARAMETER error will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1d76-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1d76-133">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="a1d76-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1d76-134">See also</span></span>
