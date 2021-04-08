---
title: MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02-Klasse
description: Die MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02-Klasse wird zum Abrufen der Protokolle verwendet, die innerhalb von StartTime und stopTime vorhanden sind.
ms.assetid: e360bc76-f006-45e1-b78a-29125fbcd5ae
keywords:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02-Klasse
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbbe47dfb3ff23c1d1bd891053375e19d6e503e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740064"
---
# <a name="mdm_reporting_securityauditing01_retrievebytimerange02-class"></a><span data-ttu-id="2a546-105">MDM- \_ Berichterstellung \_ SecurityAuditing01 RetrieveByTimeRange02- \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="2a546-105">MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02 class</span></span>

<span data-ttu-id="2a546-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="2a546-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2a546-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="2a546-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2a546-108">Die **MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02** -Klasse wird zum Abrufen der Protokolle verwendet, die innerhalb von StartTime und stopTime vorhanden sind. "StartTime" und "stopTime" werden im ISO 8601-Format ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="2a546-108">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class is used to retrieve the logs that exist within the StartTime and StopTime.The StartTime and StopTime are expressed in ISO 8601 format.</span></span> <span data-ttu-id="2a546-109">Wenn "StartTime" und "stopTime" nicht angegeben sind, werden die Werte entweder als erste vorhandene oder letzte vorhandene Zeit interpretiert.</span><span class="sxs-lookup"><span data-stu-id="2a546-109">If the StartTime and StopTime are not specified, then the values are interpreted as either first existing or last existing time.</span></span>

<span data-ttu-id="2a546-110">Dies sind die anderen möglichen Szenarien:</span><span class="sxs-lookup"><span data-stu-id="2a546-110">Here are the other possible scenarios:</span></span>

-   <span data-ttu-id="2a546-111">Wenn "StartTime" und "stopTime" nicht angegeben sind, werden alle vorhandenen Protokolle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2a546-111">If the StartTime and StopTime are not specified, then it returns all existing logs.</span></span>
-   <span data-ttu-id="2a546-112">Wenn die stopTime angegeben ist, aber StartTime nicht angegeben ist, werden alle Protokolle, die vor der stopTime vorhanden sind, zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2a546-112">If the StopTime is specified, but the StartTime is not specified, then all logs that exist before the StopTime are returned.</span></span>
-   <span data-ttu-id="2a546-113">Wenn "StartTime" angegeben ist, aber "stopTime" nicht angegeben ist, werden alle Protokolle zurückgegeben, die aus "StartTime" bestehen.</span><span class="sxs-lookup"><span data-stu-id="2a546-113">If the StartTime is specified, but the StopTime is not specified, then all that logs that exist from the StartTime are returned.</span></span>

<span data-ttu-id="2a546-114">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="2a546-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a546-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a546-115">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
};
```

## <a name="members"></a><span data-ttu-id="2a546-116">Member</span><span class="sxs-lookup"><span data-stu-id="2a546-116">Members</span></span>

<span data-ttu-id="2a546-117">Die **MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2a546-117">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class has these types of members:</span></span>

-   [<span data-ttu-id="2a546-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a546-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a546-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a546-119">Properties</span></span>

<span data-ttu-id="2a546-120">Die **MDM \_ Reporting \_ SecurityAuditing01 \_ RetrieveByTimeRange02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a546-120">The **MDM\_Reporting\_SecurityAuditing01\_RetrieveByTimeRange02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a546-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2a546-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a546-122">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2a546-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a546-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a546-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a546-124">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2a546-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2a546-125">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="2a546-125">Identifies the name of the parent node.</span></span> <span data-ttu-id="2a546-126">Für diese Klasse ist die Zeichenfolge "retrievebytimerange".</span><span class="sxs-lookup"><span data-stu-id="2a546-126">For this class, the string is "RetrieveByTimeRange".</span></span>

</dd> <dt>

[<span data-ttu-id="2a546-127">Protokolle</span><span class="sxs-lookup"><span data-stu-id="2a546-127">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a546-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2a546-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a546-129">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2a546-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2a546-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2a546-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a546-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2a546-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a546-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2a546-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a546-133">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2a546-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2a546-134">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="2a546-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="2a546-135">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/SecurityAuditing".</span><span class="sxs-lookup"><span data-stu-id="2a546-135">For this class, the string is "./Vendor/MSFT/SecurityAuditing"</span></span>

</dd> <dt>

[<span data-ttu-id="2a546-136">StartTime</span><span class="sxs-lookup"><span data-stu-id="2a546-136">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a546-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2a546-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a546-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2a546-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2a546-139">StopTime</span><span class="sxs-lookup"><span data-stu-id="2a546-139">StopTime</span></span>](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a546-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2a546-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a546-141">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2a546-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a546-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a546-142">Requirements</span></span>



| <span data-ttu-id="2a546-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a546-143">Requirement</span></span> | <span data-ttu-id="2a546-144">Wert</span><span class="sxs-lookup"><span data-stu-id="2a546-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a546-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a546-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2a546-146">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a546-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2a546-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a546-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2a546-148">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2a546-148">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="2a546-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a546-149">Namespace</span></span><br/>                | <span data-ttu-id="2a546-150">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="2a546-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="2a546-151">MOF</span><span class="sxs-lookup"><span data-stu-id="2a546-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a546-152"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2a546-152"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="2a546-153">DLL</span><span class="sxs-lookup"><span data-stu-id="2a546-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a546-154"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="2a546-154"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

