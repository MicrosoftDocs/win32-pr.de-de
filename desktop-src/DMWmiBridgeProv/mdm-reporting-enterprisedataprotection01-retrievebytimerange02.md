---
title: MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02-Klasse
description: Die MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02-Klasse wird zum Abrufen der Protokolle verwendet, die innerhalb von StartTime und stopTime vorhanden sind.
ms.assetid: 6abec00e-901f-4f79-840d-a4ef3a4d392d
keywords:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02-Klasse
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec266e68bbaaafb1f1e3a78fba7ea6b91805096a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040139"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebytimerange02-class"></a><span data-ttu-id="bd1d6-105">MDM- \_ Berichterstellung \_ EnterpriseDataProtection01 RetrieveByTimeRange02- \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="bd1d6-105">MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02 class</span></span>

<span data-ttu-id="bd1d6-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bd1d6-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="bd1d6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bd1d6-108">Die **MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** -Klasse wird zum Abrufen der Protokolle verwendet, die innerhalb von StartTime und stopTime vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-108">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class is used to retrieve the logs that exist within the StartTime and StopTime.</span></span> <span data-ttu-id="bd1d6-109">StartTime und stopTime werden im ISO 8601-Format ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-109">The StartTime and StopTime are expressed in ISO 8601 format.</span></span> <span data-ttu-id="bd1d6-110">Wenn "StartTime" und "stopTime" nicht angegeben sind, werden die Werte entweder als erste vorhandene oder letzte vorhandene Zeit interpretiert.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-110">If the StartTime and StopTime are not specified, then the values are interpreted as either first existing or last existing time.</span></span>

<span data-ttu-id="bd1d6-111">Dies sind die anderen möglichen Szenarien:</span><span class="sxs-lookup"><span data-stu-id="bd1d6-111">Here are the other possible scenarios:</span></span>

-   <span data-ttu-id="bd1d6-112">Wenn "StartTime" und "stopTime" nicht angegeben sind, werden alle vorhandenen Protokolle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-112">If the StartTime and StopTime are not specified, then it returns all existing logs.</span></span>
-   <span data-ttu-id="bd1d6-113">Wenn die stopTime angegeben ist, aber StartTime nicht angegeben ist, werden alle Protokolle, die vor der stopTime vorhanden sind, zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-113">If the StopTime is specified, but the StartTime is not specified, then all logs that exist before the StopTime are returned.</span></span>
-   <span data-ttu-id="bd1d6-114">Wenn "StartTime" angegeben ist, aber "stopTime" nicht angegeben ist, werden alle Protokolle zurückgegeben, die aus "StartTime" bestehen.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-114">If the StartTime is specified, but the StopTime is not specified, then all that logs that exist from the StartTime are returned.</span></span>

<span data-ttu-id="bd1d6-115">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-115">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd1d6-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd1d6-116">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="bd1d6-117">Member</span><span class="sxs-lookup"><span data-stu-id="bd1d6-117">Members</span></span>

<span data-ttu-id="bd1d6-118">Die **MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bd1d6-118">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class has these types of members:</span></span>

-   [<span data-ttu-id="bd1d6-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bd1d6-119">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd1d6-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bd1d6-120">Properties</span></span>

<span data-ttu-id="bd1d6-121">Die **MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-121">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByTimeRange02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd1d6-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bd1d6-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd1d6-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bd1d6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd1d6-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bd1d6-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd1d6-125">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bd1d6-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bd1d6-126">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="bd1d6-127">Für diese Klasse ist die Zeichenfolge "retrievebytimerange".</span><span class="sxs-lookup"><span data-stu-id="bd1d6-127">For this class, the string is "RetrieveByTimeRange".</span></span>

</dd> <dt>

[<span data-ttu-id="bd1d6-128">Protokolle</span><span class="sxs-lookup"><span data-stu-id="bd1d6-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd1d6-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bd1d6-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd1d6-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bd1d6-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bd1d6-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bd1d6-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd1d6-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bd1d6-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd1d6-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bd1d6-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd1d6-134">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bd1d6-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bd1d6-135">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="bd1d6-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="bd1d6-136">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/EnterpriseDataProtection".</span><span class="sxs-lookup"><span data-stu-id="bd1d6-136">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="bd1d6-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="bd1d6-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd1d6-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bd1d6-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd1d6-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bd1d6-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bd1d6-140">StopTime</span><span class="sxs-lookup"><span data-stu-id="bd1d6-140">StopTime</span></span>](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd1d6-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bd1d6-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd1d6-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bd1d6-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bd1d6-143">Type</span><span class="sxs-lookup"><span data-stu-id="bd1d6-143">Type</span></span>](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd1d6-144">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bd1d6-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd1d6-145">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bd1d6-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd1d6-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd1d6-146">Requirements</span></span>



| <span data-ttu-id="bd1d6-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd1d6-147">Requirement</span></span> | <span data-ttu-id="bd1d6-148">Wert</span><span class="sxs-lookup"><span data-stu-id="bd1d6-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd1d6-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd1d6-149">Minimum supported client</span></span><br/> | <span data-ttu-id="bd1d6-150">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd1d6-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bd1d6-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd1d6-151">Minimum supported server</span></span><br/> | <span data-ttu-id="bd1d6-152">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bd1d6-152">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="bd1d6-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd1d6-153">Namespace</span></span><br/>                | <span data-ttu-id="bd1d6-154">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="bd1d6-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="bd1d6-155">MOF</span><span class="sxs-lookup"><span data-stu-id="bd1d6-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd1d6-156"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bd1d6-156"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="bd1d6-157">DLL</span><span class="sxs-lookup"><span data-stu-id="bd1d6-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd1d6-158"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="bd1d6-158"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

