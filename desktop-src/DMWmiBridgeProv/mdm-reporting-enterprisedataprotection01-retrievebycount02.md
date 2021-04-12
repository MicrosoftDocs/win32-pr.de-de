---
title: MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02-Klasse
description: Die MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByCount02-Klasse wird verwendet, um eine angegebene Anzahl von Protokollen aus "StartTime" abzurufen.
ms.assetid: 0a581d5a-129b-48c3-a7a1-3947cc1e2ee9
keywords:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02-Klasse
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fcc6e7ed3ccb630b500179d7273bdd09a21477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475276"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebycount02-class"></a><span data-ttu-id="bf5fa-105">MDM- \_ Berichterstellung \_ EnterpriseDataProtection01 RetrieveByCount02- \_ Klasse</span><span class="sxs-lookup"><span data-stu-id="bf5fa-105">MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02 class</span></span>

<span data-ttu-id="bf5fa-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bf5fa-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="bf5fa-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bf5fa-108">Die **MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByCount02** -Klasse wird verwendet, um eine angegebene Anzahl von Protokollen aus "StartTime" abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-108">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class is used to retrieve a specified number of logs from the StartTime.</span></span> <span data-ttu-id="bf5fa-109">Der StartTime-Wert wird im ISO 8601-Format ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-109">The StartTime is expressed in ISO 8601 format.</span></span> <span data-ttu-id="bf5fa-110">Sie können die Anzahl der erforderlichen Protokolle festlegen, indem Sie "logcount" und "StartTime" festlegen.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-110">You can set the number of logs required by setting LogCount and StartTime.</span></span> <span data-ttu-id="bf5fa-111">Wenn die Gesamtzahl der Protokolle kleiner als logcount ist, wird die angegebene Anzahl von Protokollen oder weniger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-111">It returns the specified number of log or less, if the total number logs is less than LogCount.</span></span>

<span data-ttu-id="bf5fa-112">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-112">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf5fa-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf5fa-113">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
{
  string InstanceID;
  string ParentID;
  string Logs;
  sint32 LogCount;
  string StartTime;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="bf5fa-114">Member</span><span class="sxs-lookup"><span data-stu-id="bf5fa-114">Members</span></span>

<span data-ttu-id="bf5fa-115">Die **MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByCount02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bf5fa-115">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class has these types of members:</span></span>

-   [<span data-ttu-id="bf5fa-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bf5fa-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf5fa-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bf5fa-117">Properties</span></span>

<span data-ttu-id="bf5fa-118">Die **MDM \_ Reporting \_ EnterpriseDataProtection01 \_ RetrieveByCount02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-118">The **MDM\_Reporting\_EnterpriseDataProtection01\_RetrieveByCount02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf5fa-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bf5fa-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf5fa-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bf5fa-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf5fa-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bf5fa-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf5fa-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bf5fa-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bf5fa-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="bf5fa-124">Für diese Klasse ist die Zeichenfolge "retrievebycount".</span><span class="sxs-lookup"><span data-stu-id="bf5fa-124">For this class, the string is "RetrieveByCount".</span></span>

</dd> <dt>

[<span data-ttu-id="bf5fa-125">Logcount</span><span class="sxs-lookup"><span data-stu-id="bf5fa-125">LogCount</span></span>](/windows/client-management/mdm/reporting-csp#logcount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf5fa-126">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf5fa-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf5fa-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bf5fa-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf5fa-128">Protokolle</span><span class="sxs-lookup"><span data-stu-id="bf5fa-128">Logs</span></span>](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf5fa-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bf5fa-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf5fa-130">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bf5fa-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bf5fa-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bf5fa-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf5fa-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bf5fa-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf5fa-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bf5fa-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf5fa-134">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bf5fa-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bf5fa-135">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="bf5fa-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="bf5fa-136">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/EnterpriseDataProtection".</span><span class="sxs-lookup"><span data-stu-id="bf5fa-136">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="bf5fa-137">StartTime</span><span class="sxs-lookup"><span data-stu-id="bf5fa-137">StartTime</span></span>](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf5fa-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bf5fa-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf5fa-139">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bf5fa-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bf5fa-140">Type</span><span class="sxs-lookup"><span data-stu-id="bf5fa-140">Type</span></span>](/windows/client-management/mdm/reporting-csp#type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf5fa-141">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf5fa-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf5fa-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="bf5fa-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf5fa-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf5fa-143">Requirements</span></span>



| <span data-ttu-id="bf5fa-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf5fa-144">Requirement</span></span> | <span data-ttu-id="bf5fa-145">Wert</span><span class="sxs-lookup"><span data-stu-id="bf5fa-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf5fa-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf5fa-146">Minimum supported client</span></span><br/> | <span data-ttu-id="bf5fa-147">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf5fa-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bf5fa-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf5fa-148">Minimum supported server</span></span><br/> | <span data-ttu-id="bf5fa-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bf5fa-149">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="bf5fa-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="bf5fa-150">Namespace</span></span><br/>                | <span data-ttu-id="bf5fa-151">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="bf5fa-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="bf5fa-152">MOF</span><span class="sxs-lookup"><span data-stu-id="bf5fa-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf5fa-153"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bf5fa-153"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="bf5fa-154">DLL</span><span class="sxs-lookup"><span data-stu-id="bf5fa-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf5fa-155"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="bf5fa-155"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

