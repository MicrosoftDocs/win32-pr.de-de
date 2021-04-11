---
title: MDM_Policy_Config01_Cellular02-Klasse
description: Die MDM- \_ Richtlinie \_ Config01 \_ Cellular02-Klasse konfiguriert die Mobilfunk-Richtlinien.
ms.assetid: e5926a21-a375-4d1c-8b37-7fe7f7532c50
keywords:
- MDM_Policy_Config01_Cellular02-Klasse
- MDM_Policy_Config01_Cellular02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Cellular02
- MDM_Policy_Config01_Cellular02.InstanceID
- MDM_Policy_Config01_Cellular02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1b6d9163723299b144368d9d2b73a12ccc7a91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103315"
---
# <a name="mdm_policy_config01_cellular02-class"></a><span data-ttu-id="6280e-105">MDM- \_ Richtlinie \_ Config01 \_ Cellular02-Klasse</span><span class="sxs-lookup"><span data-stu-id="6280e-105">MDM\_Policy\_Config01\_Cellular02 class</span></span>

<span data-ttu-id="6280e-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="6280e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6280e-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="6280e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6280e-108">Die MDM- \_ Richtlinie \_ Config01 \_ Cellular02-Klasse konfiguriert die Mobilfunk-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="6280e-108">The MDM\_Policy\_Config01\_Cellular02 class configures the cellular policies.</span></span>

<span data-ttu-id="6280e-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="6280e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6280e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6280e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Cellular02
{
  string InstanceID;
  string ParentID;
  string LetAppsAccessCellularData_UserInControlOfTheseApps;
  string LetAppsAccessCellularData_ForceDenyTheseApps;
  string LetAppsAccessCellularData_ForceAllowTheseApps;
  sint32 LetAppsAccessCellularData;
  string ShowAppCellularAccessUI;
};
```

## <a name="members"></a><span data-ttu-id="6280e-111">Member</span><span class="sxs-lookup"><span data-stu-id="6280e-111">Members</span></span>

<span data-ttu-id="6280e-112">Die **MDM- \_ Richtlinie \_ Config01 \_ Cellular02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6280e-112">The **MDM\_Policy\_Config01\_Cellular02** class has these types of members:</span></span>

-   [<span data-ttu-id="6280e-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6280e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6280e-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6280e-114">Properties</span></span>

<span data-ttu-id="6280e-115">Die **MDM- \_ Richtlinie \_ Config01 \_ Cellular02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6280e-115">The **MDM\_Policy\_Config01\_Cellular02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6280e-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6280e-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6280e-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6280e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6280e-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6280e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6280e-119">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6280e-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6280e-120">Letappsaccesscellulardata</span><span class="sxs-lookup"><span data-stu-id="6280e-120">LetAppsAccessCellularData</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6280e-121">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6280e-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6280e-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6280e-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6280e-123">Letappsaccesscellulardata \_ forceallowtheseapps</span><span class="sxs-lookup"><span data-stu-id="6280e-123">LetAppsAccessCellularData\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6280e-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6280e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6280e-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6280e-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6280e-126">Letappsaccesscellulardata \_ forcedenytheseapps</span><span class="sxs-lookup"><span data-stu-id="6280e-126">LetAppsAccessCellularData\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6280e-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6280e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6280e-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6280e-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6280e-129">Letappsaccesscellulardata \_ userincontrolof theseapps</span><span class="sxs-lookup"><span data-stu-id="6280e-129">LetAppsAccessCellularData\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6280e-130">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6280e-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6280e-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6280e-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6280e-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6280e-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6280e-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6280e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6280e-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6280e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6280e-135">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6280e-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6280e-136">Showappcellularaccessui</span><span class="sxs-lookup"><span data-stu-id="6280e-136">ShowAppCellularAccessUI</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-showappcellularaccessui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6280e-137">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6280e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6280e-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6280e-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6280e-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6280e-139">Requirements</span></span>



| <span data-ttu-id="6280e-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6280e-140">Requirement</span></span> | <span data-ttu-id="6280e-141">Wert</span><span class="sxs-lookup"><span data-stu-id="6280e-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6280e-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6280e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6280e-143">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6280e-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6280e-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6280e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6280e-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6280e-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6280e-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="6280e-146">Namespace</span></span><br/>                | <span data-ttu-id="6280e-147">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="6280e-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6280e-148">MOF</span><span class="sxs-lookup"><span data-stu-id="6280e-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6280e-149"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6280e-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6280e-150">DLL</span><span class="sxs-lookup"><span data-stu-id="6280e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6280e-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6280e-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

