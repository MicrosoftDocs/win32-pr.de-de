---
title: MDM_AppLocker_DLL03-Klasse
description: Die MDM \_ AppLocker \_ DLL03-Klasse definiert die Richtlinien Einschränkungen für die Verarbeitung von DLL-Dateien.
ms.assetid: 956b2ec0-f8a8-41d1-a571-01e73c4cebf9
keywords:
- MDM_AppLocker_DLL03-Klasse
- MDM_AppLocker_DLL03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_AppLocker_DLL03
- MDM_AppLocker_DLL03.InstanceID
- MDM_AppLocker_DLL03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c332a7d606b21ed9641c3c25f10a011cf7bea6e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338796"
---
# <a name="mdm_applocker_dll03-class"></a><span data-ttu-id="dbdce-105">MDM \_ AppLocker \_ DLL03-Klasse</span><span class="sxs-lookup"><span data-stu-id="dbdce-105">MDM\_AppLocker\_DLL03 class</span></span>

<span data-ttu-id="dbdce-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="dbdce-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dbdce-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="dbdce-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dbdce-108">Die **MDM \_ AppLocker \_ DLL03** -Klasse definiert die Richtlinien Einschränkungen für die Verarbeitung von DLL-Dateien.</span><span class="sxs-lookup"><span data-stu-id="dbdce-108">The **MDM\_AppLocker\_DLL03** class defines the policy restrictions for processing DLL files.</span></span>

<span data-ttu-id="dbdce-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="dbdce-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbdce-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbdce-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_DLL03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a><span data-ttu-id="dbdce-111">Member</span><span class="sxs-lookup"><span data-stu-id="dbdce-111">Members</span></span>

<span data-ttu-id="dbdce-112">Die **MDM \_ AppLocker \_ DLL03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dbdce-112">The **MDM\_AppLocker\_DLL03** class has these types of members:</span></span>

-   [<span data-ttu-id="dbdce-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dbdce-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbdce-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dbdce-114">Properties</span></span>

<span data-ttu-id="dbdce-115">Die **MDM- \_ AppLocker- \_ DLL03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dbdce-115">The **MDM\_AppLocker\_DLL03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="dbdce-116">**Enforcementmode**</span><span class="sxs-lookup"><span data-stu-id="dbdce-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbdce-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbdce-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbdce-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dbdce-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dbdce-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dbdce-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbdce-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbdce-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbdce-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbdce-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbdce-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dbdce-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dbdce-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="dbdce-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="dbdce-124">**Noninteractiveprocessenforcement**</span><span class="sxs-lookup"><span data-stu-id="dbdce-124">**NonInteractiveProcessEnforcement**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbdce-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbdce-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbdce-126">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dbdce-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dbdce-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dbdce-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbdce-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbdce-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbdce-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dbdce-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbdce-130">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dbdce-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dbdce-131">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="dbdce-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="dbdce-132">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions".</span><span class="sxs-lookup"><span data-stu-id="dbdce-132">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="dbdce-133">**Policy**</span><span class="sxs-lookup"><span data-stu-id="dbdce-133">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbdce-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dbdce-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbdce-135">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="dbdce-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbdce-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbdce-136">Requirements</span></span>



| <span data-ttu-id="dbdce-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbdce-137">Requirement</span></span> | <span data-ttu-id="dbdce-138">Wert</span><span class="sxs-lookup"><span data-stu-id="dbdce-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbdce-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbdce-139">Minimum supported client</span></span><br/> | <span data-ttu-id="dbdce-140">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbdce-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dbdce-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbdce-141">Minimum supported server</span></span><br/> | <span data-ttu-id="dbdce-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="dbdce-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dbdce-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbdce-143">Namespace</span></span><br/>                | <span data-ttu-id="dbdce-144">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="dbdce-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="dbdce-145">MOF</span><span class="sxs-lookup"><span data-stu-id="dbdce-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbdce-146"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dbdce-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbdce-147">DLL</span><span class="sxs-lookup"><span data-stu-id="dbdce-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbdce-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbdce-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbdce-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbdce-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbdce-150">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="dbdce-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

