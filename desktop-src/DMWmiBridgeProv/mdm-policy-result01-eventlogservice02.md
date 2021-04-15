---
title: MDM_Policy_Result01_EventLogService02-Klasse
description: Die MDM- \_ Richtlinie \_ Result01 \_ EventLogService02-Klasse stellt das Ereignisprotokoll Verhalten dar.
ms.assetid: 6d4908e9-d283-486a-8309-57d5c5ec83d0
keywords:
- MDM_Policy_Result01_EventLogService02-Klasse
- MDM_Policy_Result01_EventLogService02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_EventLogService02
- MDM_Policy_Result01_EventLogService02.InstanceID
- MDM_Policy_Result01_EventLogService02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914a00c3646490e5d4679579aab7a38474a34f00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476905"
---
# <a name="mdm_policy_result01_eventlogservice02-class"></a><span data-ttu-id="7d194-105">MDM- \_ Richtlinie \_ Result01 \_ EventLogService02-Klasse</span><span class="sxs-lookup"><span data-stu-id="7d194-105">MDM\_Policy\_Result01\_EventLogService02 class</span></span>

<span data-ttu-id="7d194-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="7d194-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7d194-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="7d194-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7d194-108">Die MDM- \_ Richtlinie \_ Result01 \_ EventLogService02-Klasse stellt das Ereignisprotokoll Verhalten dar.</span><span class="sxs-lookup"><span data-stu-id="7d194-108">The MDM\_Policy\_Result01\_EventLogService02 class represents the event log behavior.</span></span>

<span data-ttu-id="7d194-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="7d194-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d194-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d194-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_EventLogService02
{
  string InstanceID;
  string ParentID;
  string ControlEventLogBehavior;
  string SpecifyMaximumFileSizeApplicationLog;
  string SpecifyMaximumFileSizeSecurityLog;
  string SpecifyMaximumFileSizeSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="7d194-111">Member</span><span class="sxs-lookup"><span data-stu-id="7d194-111">Members</span></span>

<span data-ttu-id="7d194-112">Die **MDM- \_ Richtlinie \_ Result01 \_ EventLogService02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7d194-112">The **MDM\_Policy\_Result01\_EventLogService02** class has these types of members:</span></span>

-   [<span data-ttu-id="7d194-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d194-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d194-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d194-114">Properties</span></span>

<span data-ttu-id="7d194-115">Die **MDM- \_ Richtlinie \_ Result01 \_ EventLogService02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7d194-115">The **MDM\_Policy\_Result01\_EventLogService02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7d194-116">Controleventlogbehavior</span><span class="sxs-lookup"><span data-stu-id="7d194-116">ControlEventLogBehavior</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-controleventlogbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d194-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7d194-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d194-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7d194-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d194-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7d194-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d194-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7d194-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d194-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7d194-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d194-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7d194-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d194-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7d194-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d194-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7d194-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d194-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="7d194-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d194-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7d194-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d194-127">Specifymaximumfilesizeapplicationlog</span><span class="sxs-lookup"><span data-stu-id="7d194-127">SpecifyMaximumFileSizeApplicationLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizeapplicationlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d194-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7d194-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d194-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7d194-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d194-130">Specifymaximumfilesizesecuritylog</span><span class="sxs-lookup"><span data-stu-id="7d194-130">SpecifyMaximumFileSizeSecurityLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesecuritylog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d194-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7d194-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d194-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7d194-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7d194-133">Specifymaximumfilesizesystemlog</span><span class="sxs-lookup"><span data-stu-id="7d194-133">SpecifyMaximumFileSizeSystemLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesystemlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d194-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="7d194-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d194-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="7d194-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d194-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d194-136">Requirements</span></span>



| <span data-ttu-id="7d194-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d194-137">Requirement</span></span> | <span data-ttu-id="7d194-138">Wert</span><span class="sxs-lookup"><span data-stu-id="7d194-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d194-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d194-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7d194-140">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7d194-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d194-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d194-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7d194-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7d194-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7d194-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d194-143">Namespace</span></span><br/>                | <span data-ttu-id="7d194-144">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="7d194-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7d194-145">MOF</span><span class="sxs-lookup"><span data-stu-id="7d194-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d194-146"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7d194-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d194-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7d194-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d194-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d194-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

