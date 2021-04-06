---
title: MDM_AppLocker_MSI03-Klasse
description: Die MDM \_ AppLocker \_ MSI03-Klasse definiert die Richtlinien Einschränkungen für die Verarbeitung von MSI-Dateien.
ms.assetid: b7b6602d-38b7-46f0-9542-71228ab0c303
keywords:
- MDM_AppLocker_MSI03-Klasse
- MDM_AppLocker_MSI03-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_AppLocker_MSI03
- MDM_AppLocker_MSI03.InstanceID
- MDM_AppLocker_MSI03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5bd17a979ac0e4a6dcbbc07a38ba72bfd50ede4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743568"
---
# <a name="mdm_applocker_msi03-class"></a><span data-ttu-id="954ba-105">MDM \_ AppLocker \_ MSI03-Klasse</span><span class="sxs-lookup"><span data-stu-id="954ba-105">MDM\_AppLocker\_MSI03 class</span></span>

<span data-ttu-id="954ba-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="954ba-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="954ba-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="954ba-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="954ba-108">Die **MDM \_ AppLocker \_ MSI03** -Klasse definiert die Richtlinien Einschränkungen für die Verarbeitung von MSI-Dateien.</span><span class="sxs-lookup"><span data-stu-id="954ba-108">The **MDM\_AppLocker\_MSI03** class defines the policy restrictions for processing MSI files.</span></span>

<span data-ttu-id="954ba-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="954ba-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="954ba-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="954ba-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_MSI03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="954ba-111">Member</span><span class="sxs-lookup"><span data-stu-id="954ba-111">Members</span></span>

<span data-ttu-id="954ba-112">Die **MDM \_ AppLocker \_ MSI03** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="954ba-112">The **MDM\_AppLocker\_MSI03** class has these types of members:</span></span>

-   [<span data-ttu-id="954ba-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="954ba-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="954ba-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="954ba-114">Properties</span></span>

<span data-ttu-id="954ba-115">Die **MDM- \_ AppLocker- \_ MSI03** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="954ba-115">The **MDM\_AppLocker\_MSI03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="954ba-116">**Enforcementmode**</span><span class="sxs-lookup"><span data-stu-id="954ba-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="954ba-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="954ba-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="954ba-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="954ba-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="954ba-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="954ba-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="954ba-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="954ba-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="954ba-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="954ba-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="954ba-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="954ba-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="954ba-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="954ba-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="954ba-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="954ba-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="954ba-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="954ba-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="954ba-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="954ba-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="954ba-127">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="954ba-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="954ba-128">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="954ba-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="954ba-129">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions".</span><span class="sxs-lookup"><span data-stu-id="954ba-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="954ba-130">**Policy**</span><span class="sxs-lookup"><span data-stu-id="954ba-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="954ba-131">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="954ba-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="954ba-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="954ba-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="954ba-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="954ba-133">Requirements</span></span>



| <span data-ttu-id="954ba-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="954ba-134">Requirement</span></span> | <span data-ttu-id="954ba-135">Wert</span><span class="sxs-lookup"><span data-stu-id="954ba-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="954ba-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="954ba-136">Minimum supported client</span></span><br/> | <span data-ttu-id="954ba-137">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="954ba-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="954ba-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="954ba-138">Minimum supported server</span></span><br/> | <span data-ttu-id="954ba-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="954ba-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="954ba-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="954ba-140">Namespace</span></span><br/>                | <span data-ttu-id="954ba-141">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="954ba-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="954ba-142">MOF</span><span class="sxs-lookup"><span data-stu-id="954ba-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="954ba-143"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="954ba-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="954ba-144">DLL</span><span class="sxs-lookup"><span data-stu-id="954ba-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="954ba-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="954ba-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="954ba-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="954ba-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="954ba-147">Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter</span><span class="sxs-lookup"><span data-stu-id="954ba-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

