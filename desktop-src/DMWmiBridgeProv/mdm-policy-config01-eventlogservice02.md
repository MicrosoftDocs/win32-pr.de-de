---
title: MDM_Policy_Config01_EventLogService02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ EventLogService02-Klasse konfiguriert das Ereignisprotokoll Verhalten.
ms.assetid: 206934c4-6671-4f13-be79-22ff1fb7ce7e
keywords:
- MDM_Policy_Config01_EventLogService02-Klasse
- MDM_Policy_Config01_EventLogService02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_EventLogService02
- MDM_Policy_Config01_EventLogService02.InstanceID
- MDM_Policy_Config01_EventLogService02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e39d3e78e686886e689ab2333b073108207446a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949681"
---
# <a name="mdm_policy_config01_eventlogservice02-class"></a><span data-ttu-id="a16dc-105">MDM- \_ Richtlinie \_ Config01 \_ EventLogService02-Klasse</span><span class="sxs-lookup"><span data-stu-id="a16dc-105">MDM\_Policy\_Config01\_EventLogService02 class</span></span>

<span data-ttu-id="a16dc-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="a16dc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a16dc-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="a16dc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a16dc-108">Die MDM- \_ Richtlinie \_ Config01 \_ EventLogService02-Klasse konfiguriert das Ereignisprotokoll Verhalten.</span><span class="sxs-lookup"><span data-stu-id="a16dc-108">The MDM\_Policy\_Config01\_EventLogService02 class configures the event log behavior.</span></span>

<span data-ttu-id="a16dc-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="a16dc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a16dc-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a16dc-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_EventLogService02
{
  string InstanceID;
  string ParentID;
  string ControlEventLogBehavior;
  string SpecifyMaximumFileSizeApplicationLog;
  string SpecifyMaximumFileSizeSecurityLog;
  string SpecifyMaximumFileSizeSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="a16dc-111">Member</span><span class="sxs-lookup"><span data-stu-id="a16dc-111">Members</span></span>

<span data-ttu-id="a16dc-112">Die **MDM- \_ Richtlinie \_ Config01 \_ EventLogService02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="a16dc-112">The **MDM\_Policy\_Config01\_EventLogService02** class has these types of members:</span></span>

-   [<span data-ttu-id="a16dc-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a16dc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a16dc-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a16dc-114">Properties</span></span>

<span data-ttu-id="a16dc-115">Die **MDM- \_ Richtlinie \_ Config01 \_ EventLogService02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a16dc-115">The **MDM\_Policy\_Config01\_EventLogService02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a16dc-116">Controleventlogbehavior</span><span class="sxs-lookup"><span data-stu-id="a16dc-116">ControlEventLogBehavior</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-controleventlogbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16dc-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a16dc-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a16dc-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a16dc-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a16dc-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a16dc-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16dc-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a16dc-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a16dc-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a16dc-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a16dc-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a16dc-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a16dc-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a16dc-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16dc-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a16dc-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a16dc-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="a16dc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a16dc-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a16dc-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a16dc-127">Specifymaximumfilesizeapplicationlog</span><span class="sxs-lookup"><span data-stu-id="a16dc-127">SpecifyMaximumFileSizeApplicationLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizeapplicationlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16dc-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a16dc-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a16dc-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a16dc-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a16dc-130">Specifymaximumfilesizesecuritylog</span><span class="sxs-lookup"><span data-stu-id="a16dc-130">SpecifyMaximumFileSizeSecurityLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesecuritylog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16dc-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a16dc-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a16dc-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a16dc-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a16dc-133">Specifymaximumfilesizesystemlog</span><span class="sxs-lookup"><span data-stu-id="a16dc-133">SpecifyMaximumFileSizeSystemLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesystemlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a16dc-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="a16dc-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a16dc-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="a16dc-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a16dc-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a16dc-136">Requirements</span></span>



| <span data-ttu-id="a16dc-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a16dc-137">Requirement</span></span> | <span data-ttu-id="a16dc-138">Wert</span><span class="sxs-lookup"><span data-stu-id="a16dc-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a16dc-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a16dc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a16dc-140">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a16dc-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a16dc-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a16dc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a16dc-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a16dc-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a16dc-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="a16dc-143">Namespace</span></span><br/>                | <span data-ttu-id="a16dc-144">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="a16dc-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a16dc-145">MOF</span><span class="sxs-lookup"><span data-stu-id="a16dc-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a16dc-146"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a16dc-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a16dc-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a16dc-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a16dc-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a16dc-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

