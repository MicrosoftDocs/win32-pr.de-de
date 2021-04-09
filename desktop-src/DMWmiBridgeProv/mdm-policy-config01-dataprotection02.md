---
title: MDM_Policy_Config01_DataProtection02-Klasse
description: Die Config01 DataProtection02-Klasse der MDM- \_ Richtlinie \_ \_ stellt die verfügbaren Datenschutzrichtlinien dar.
ms.assetid: 54750bae-ee5d-4db9-896f-28d9550c4d5d
keywords:
- MDM_Policy_Config01_DataProtection02-Klasse
- MDM_Policy_Config01_DataProtection02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DataProtection02
- MDM_Policy_Config01_DataProtection02.InstanceID
- MDM_Policy_Config01_DataProtection02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692dfd675c07ddc7eebbfcd75e09cb521126c746
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957035"
---
# <a name="mdm_policy_config01_dataprotection02-class"></a><span data-ttu-id="0f9d7-105">MDM- \_ Richtlinie \_ Config01 \_ DataProtection02-Klasse</span><span class="sxs-lookup"><span data-stu-id="0f9d7-105">MDM\_Policy\_Config01\_DataProtection02 class</span></span>

<span data-ttu-id="0f9d7-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="0f9d7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0f9d7-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="0f9d7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0f9d7-108">Die **\_ \_ Config01 \_ DataProtection02-Klasse der MDM-Richtlinie** stellt die verfügbaren Datenschutzrichtlinien dar.</span><span class="sxs-lookup"><span data-stu-id="0f9d7-108">The **MDM\_Policy\_Config01\_DataProtection02** class represents the data protection policies available.</span></span>

<span data-ttu-id="0f9d7-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="0f9d7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f9d7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f9d7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DataProtection02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDirectMemoryAccess;
  string LegacySelectiveWipeID;
};
```

## <a name="members"></a><span data-ttu-id="0f9d7-111">Member</span><span class="sxs-lookup"><span data-stu-id="0f9d7-111">Members</span></span>

<span data-ttu-id="0f9d7-112">Die **MDM- \_ Richtlinie \_ Config01 \_ DataProtection02** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0f9d7-112">The **MDM\_Policy\_Config01\_DataProtection02** class has these types of members:</span></span>

-   [<span data-ttu-id="0f9d7-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f9d7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f9d7-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0f9d7-114">Properties</span></span>

<span data-ttu-id="0f9d7-115">Die **MDM- \_ Richtlinie \_ Config01 \_ DataProtection02** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0f9d7-115">The **MDM\_Policy\_Config01\_DataProtection02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0f9d7-116">Allowdirectmemoryaccess</span><span class="sxs-lookup"><span data-stu-id="0f9d7-116">AllowDirectMemoryAccess</span></span>](/windows/client-management/mdm/policy-csp-dataprotection#dataprotection-allowdirectmemoryaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9d7-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0f9d7-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f9d7-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0f9d7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0f9d7-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0f9d7-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9d7-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f9d7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9d7-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f9d7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9d7-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0f9d7-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0f9d7-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="0f9d7-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="0f9d7-124">Für diese Klasse ist die Zeichenfolge "DataProtection".</span><span class="sxs-lookup"><span data-stu-id="0f9d7-124">For this class, the string is "DataProtection".</span></span>

</dd> <dt>

[<span data-ttu-id="0f9d7-125">Legacyselectivewipeid</span><span class="sxs-lookup"><span data-stu-id="0f9d7-125">LegacySelectiveWipeID</span></span>](/windows/client-management/mdm/policy-csp-dataprotection#dataprotection-legacyselectivewipeid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9d7-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f9d7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9d7-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0f9d7-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0f9d7-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0f9d7-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f9d7-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0f9d7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f9d7-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="0f9d7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f9d7-131">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0f9d7-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0f9d7-132">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="0f9d7-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="0f9d7-133">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Policy/config".</span><span class="sxs-lookup"><span data-stu-id="0f9d7-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f9d7-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f9d7-134">Requirements</span></span>



| <span data-ttu-id="0f9d7-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f9d7-135">Requirement</span></span> | <span data-ttu-id="0f9d7-136">Wert</span><span class="sxs-lookup"><span data-stu-id="0f9d7-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f9d7-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f9d7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0f9d7-138">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f9d7-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f9d7-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f9d7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0f9d7-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0f9d7-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0f9d7-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f9d7-141">Namespace</span></span><br/>                | <span data-ttu-id="0f9d7-142">Root \\ CIMv2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="0f9d7-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="0f9d7-143">MOF</span><span class="sxs-lookup"><span data-stu-id="0f9d7-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f9d7-144"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0f9d7-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f9d7-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0f9d7-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f9d7-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f9d7-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f9d7-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f9d7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f9d7-148">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="0f9d7-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

